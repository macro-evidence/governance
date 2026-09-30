# Macro Evidence - GitHub Contributor-Rights Enforcement

> Version 1.0.1 · Active · Last updated 2026-09-30

---

This document specifies the security invariants for GitHub merge enforcement. It does not replace the contributor agreement, Contribution Policy, or private contributor-rights register.

---

## Trust boundary

The privileged check may use secrets only when the workflow source is taken from a trusted base branch. It must never check out, fetch, build, import, or execute pull-request code. Pull-request titles, bodies, branch names, commit messages, patches, file contents, or contributor-supplied strings are not inserted into privileged shell code.

The reusable workflow receives only the GitHub numeric account ID, structured actor type, repository numeric ID, pull-request number, current head commit, organization-controlled coverage configuration, and—only where HMAC-backed verification is needed—the HMAC secret. It also receives the trusted caller's GitHub token solely to publish the derived commit status on the exact pull-request head. The workflow verifies that the repository numeric ID supplied by the caller equals GitHub's own current repository ID before evaluating coverage.

---

## Coverage domains

### Human actor tokens

Version 1 uses HMAC-SHA256 with an organization-controlled random key of at least 256 bits. Each human actor entry has an inclusive UTC calendar `valid_through` date and a matching HMAC. The token payload is:

```text
macro-evidence:contributor-rights:v1:actor:<github_numeric_account_id>:<valid_through_yyyy-mm-dd>
```

Trusted configuration stores entries as `YYYY-MM-DD:<64-hex-HMAC>`. The `valid_through` date may not exceed the private account-binding revalidation deadline. The workflow checks the UTC date and HMAC on every run, so a forgotten stale configuration entry cannot authorize merges after its stated validity. An actor entry may be generated only from an active private contributor-rights record whose GitHub numeric account ID has completed account binding. Organization membership, collaborator status, username, email domain, prior successful contribution, or `author_association` is not sufficient.

### Non-human system actors

A specifically approved non-human automation account may be represented without an HMAC secret by a trusted entry in the form `YYYY-MM-DD:<github_numeric_account_id>:<repository_numeric_id>`. The date is an inclusive UTC `valid_through` date. The workflow requires an exact match on both immutable IDs and GitHub's structured actor type `Bot`; an actor ID alone is insufficient. The private register must record the system identity and independently reviewed rights basis. This path exists so platform automation that cannot receive Actions secrets can still be handled without weakening human-contributor verification. It is not a wildcard bot bypass and must never match by username, naming pattern, organization membership, or author association. System-actor coverage expires automatically and is re-reviewed at least annually and when the platform account, provider, or rights basis materially changes.

### Pull-request-specific exceptions

A non-CLA or otherwise exceptional rights path must not become reusable merely because one pull request is approved. Its token payload is:

```text
macro-evidence:contributor-rights:v1:pr:<repository_numeric_id>:<pull_request_number>:<head_sha>:<valid_through_yyyy-mm-dd>
```

Any new head commit invalidates the exception cryptographically and requires a new review and token. Each exception also has an inclusive UTC `valid_through` date no more than 90 days after issuance, so an unchanged but abandoned pull request cannot retain exceptional clearance indefinitely.

The HMAC token domains are deliberately different so an actor token cannot be reused as a PR exception or vice versa. The HMAC component of each HMAC-backed token entry is exactly 64 hexadecimal characters. Legal names, private email addresses, addresses, agreement files, or reversible derivatives of private fields are never inputs to public automation.

---

## Caller workflow requirements

Each repository that enforces the gate maintains a small caller workflow on its trusted default branch. The caller:

- uses `pull_request_target` only for the narrowly audited privileged verification/status-publication path;
- grants only `statuses: write` to the `GITHUB_TOKEN`; every other token permission is `none`;
- passes `github.event.pull_request.user.id`, `github.event.pull_request.user.type`, `github.repository_id`, `github.event.pull_request.number`, and `github.event.pull_request.head.sha` directly as structured event inputs;
- passes human actor entries, system-actor entries, and PR-exception tokens only from organization/repository Actions configuration, not PR-controlled values;
- passes the HMAC key only through an Actions secret;
- invokes the reusable workflow by reviewed immutable commit SHA after the first published workflow commit exists;
- contains no checkout or execution of the PR head; and
- relies on the reusable workflow to publish a commit status with the fixed context `Contributor rights coverage` directly to the exact `github.event.pull_request.head.sha`. The `pull_request_target` workflow job's own Actions check is not the merge-control status because that run is associated with the trusted base context rather than the pull-request head.

Before activation, GitHub's applicable Actions event policy must explicitly permit the audited `pull_request_target` use in each selected public repository. A real fork-pull-request fixture must prove that the workflow can publish `Contributor rights coverage` to the exact fork head SHA and that the repository's required-status rule recognizes that head status. The rule must require that exact context from the configured trusted source, with no bypass actor permitted for ordinary contributor merges. GitHub can bind a required status to an expected GitHub App, not to one specific workflow within that App. Therefore activation also requires an inventory of every workflow, GitHub App, token, or integration able to create commit statuses in the repository: no other authorized publisher may be able to emit the exact `Contributor rights coverage` context through the expected source. Other GitHub Actions workflows must not receive `statuses: write` unless independently required, and any independently authorized status publisher must use a distinct context. If status publication is rejected, attaches to the wrong commit, can be spoofed through another authorized publisher, or cannot be bound unambiguously enough to the trusted source, activation fails closed and the repository remains on the manual no-external-merge baseline, under which external copyrightable Contributions are not merged through this automated gate.

The version 1 gate is defined only for pull-request head commits. GitHub merge queue must remain disabled in a repository that relies on this gate unless a separately reviewed and hosted-tested `merge_group` path publishes an equivalent contributor-rights result for the synthetic merge-group commit and the repository rules require it. Enabling merge queue without that path is a control change that reopens this enforcement design.

GitHub currently applies special secret/token restrictions to some Dependabot-triggered workflows. Therefore no non-human system actor—including Dependabot—is enabled merely because its ID appears suitable in source review. Each system actor must pass a hosted fixture proving the exact actor type, repository binding, available token permissions, head-status publication, and rights basis before its entry is activated. If GitHub's event, status-check, ruleset, secret, or reusable-workflow semantics materially change, enforcement is re-audited before continued reliance.

---

## Configuration validation

Trusted configuration is fail-closed:

- numeric identifiers must contain decimal digits only;
- the pull-request head must be a valid Git object hash in the accepted length range;
- system-actor entries use `YYYY-MM-DD:<numeric-account-id>:<numeric-repository-id>`, contain a parseable inclusive UTC date, require an exact current base-repository ID match and the structured GitHub actor type to equal `Bot`, and do not authorize after that date;
- human actor entries use `YYYY-MM-DD:<64-hex-HMAC>`, contain a parseable inclusive UTC date, and do not authorize after that date;
- neither human nor system actor entries may be configured with a validity date more than 366 days beyond the workflow run date;
- PR-exception configuration uses `YYYY-MM-DD:<64-hex-HMAC>`, the date is included in the HMAC payload, the entry does not authorize after that date, and no exception may be issued more than 90 days into the future;
- persistent human actor coverage applies only when GitHub reports actor type `User`; a bot cannot pass through a human actor token;
- a human actor or PR-specific exception cannot pass if the HMAC key is absent or shorter than 256 bits; and
- a system actor passes without HMAC only on an unexpired exact actor-ID plus repository-ID entry and the required `Bot` actor type.

---

## Revalidation, revocation, and timing risk

Human actor account control is revalidated at least every 12 months before further merge clearance. Each derived actor entry carries a `valid_through` date no later than that revalidation deadline, giving the workflow an automatic expiry in addition to the private register as the administrative source of current coverage state.

Removing an actor token makes subsequent workflow runs fail, but a completed green check may remain visible after private coverage changes. Therefore suspension, expiry of account revalidation, or future-coverage termination is incomplete until every affected open PR has its contributor-rights status invalidated, re-run, or otherwise replaced before merge. A stale green check is not authoritative after the private source of truth changes.

---

## Key compromise and rotation

If the HMAC key may have been exposed:

1. suspend reliance on HMAC-derived statuses until rotation is complete;
2. generate a fresh random key;
3. regenerate human actor and PR-exception tokens from private source records;
4. update the secret and token variables through trusted administration;
5. re-run the contributor-rights status on affected open PRs; and
6. preserve an internal incident/audit record without publishing the old key or private rights records.

Key rotation changes only derived automation data and does not amend or invalidate an executed contributor agreement. Approved system-actor entries are separately reviewed and expire on their stated validity date because they do not depend on the HMAC key.

---

## Scale boundary

The v1 configuration-list design is intentionally small-scale. Before token volume approaches platform limits, annual account revalidation becomes operationally fragile, or merge-time current-state guarantees become materially weaker than a service can provide, migrate to a private first-party lookup service or narrowly scoped GitHub App. The private contributor-rights register remains the administrative source of current coverage state through that migration, while executed agreements remain authoritative for the contractual rights they grant.

---

## Changelog

### 1.0.1 (2026-09-30)

- Changes the document status from "Activation pending" to "Active" following hosted verification of the merge gate against a fork pull request.
- No security invariant, coverage domain, caller-workflow requirement, or revocation/rotation rule changed.
- PATCH — status update only; the specification's requirements are unchanged.

### 1.0.0 (2026-09-24)

- Initial version. Specifies the security invariants for GitHub contributor-rights merge enforcement: trust boundary, coverage domains, caller workflow requirements, configuration validation, revalidation/revocation/timing risk, key compromise and rotation, and scale boundary.
