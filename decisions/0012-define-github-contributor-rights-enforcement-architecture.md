# 0012. Define GitHub contributor-rights enforcement architecture

**Status:** Accepted
**Date:** 2026-09-24

## Context

Decision 0009 defines the contributor-rights legal architecture, but an executed agreement and an automated merge control solve different problems. The merge control must derive a current, non-sensitive rights-coverage result from private records without exposing agreement records or allowing repository contributors to influence the result through pull-request-controlled inputs.

The proposed implementation uses a narrowly privileged GitHub workflow to publish a derived `Contributor rights coverage` status to the exact pull-request head commit. Human contributor coverage is derived from private records and expires automatically. Non-human system actors and rare pull-request-specific exceptions require exact repository and account binding and bounded validity. Changes in account control, agreement status, provenance, or the private source of truth must invalidate stale green statuses before an affected pull request can merge.

The implementation is security-sensitive and depends on GitHub event semantics, token permissions, required-status configuration, repository rules, and hosted runtime behavior. Those assumptions must be verified in the target repositories before activation.

## Decision

Adopt the following enforcement architecture as the operational design, subject to hosted verification and activation approval:

- treat executed contributor agreements as authoritative for the contractual rights they grant, with the private contributor-rights register serving as the administrative source of current coverage state;
- expose only a derived, non-sensitive coverage result to GitHub;
- bind persistent human coverage to the contributor's immutable GitHub numeric account identifier and a time-bounded verification record;
- require exact repository binding for repository-specific coverage;
- handle approved non-human system actors through a separately documented, exact actor-and-repository path rather than a general bot bypass;
- allow any exceptional non-CLA path only when cryptographically bound to the exact repository, pull request, head commit, and short expiry;
- run the privileged verification path from trusted default-branch code and organization-controlled configuration;
- grant the minimum GitHub token permission required to publish the derived status;
- publish the merge-control result to the exact pull-request head commit rather than relying on a base-context workflow check;
- require repository rules to require the exact observed status and prevent another authorized status publisher from spoofing that context;
- fail closed when rights coverage cannot be established, the status cannot be published or bound correctly, or a material enforcement assumption is not verified; and
- require suspension, expiry, account revalidation, or key-rotation events to trigger stale-status revalidation before affected pull requests can merge.

The detailed security invariants and configuration requirements are maintained in [`legal/cla/GITHUB_ENFORCEMENT.md`](../legal/cla/GITHUB_ENFORCEMENT.md). The contributor-agreement process remains the canonical owner of execution, private-record, suspension, and legal administration. This ADR does not activate the merge gate in any repository.

Activation requires, at minimum, a hosted fork fixture demonstrating exact-head status publication, verification of the applicable GitHub Actions event and token semantics, repository rules requiring the exact trusted status, an inventory of other authorized status publishers, verification of non-human actor paths where applicable, and a demonstrated absence of an ordinary bypass path. GitHub merge queue remains disabled for repositories relying on this version 1 gate unless an equivalent `merge_group` path is separately reviewed and hosted-tested.

## Consequences

- External copyrightable contributions remain merge-blocked until the legal coverage and operational enforcement prerequisites are both satisfied.
- Public GitHub data reveals only the derived merge-control result rather than the underlying agreement or identity records.
- The design adds GitHub Actions, repository-rule, account-binding, expiry, revalidation, and status-publication dependencies that must be maintained and reverified when platform behavior materially changes.
- The enforcement layer can change independently of the legal agreement terms when its security invariants and activation boundary remain intact.
- A material change to the trust boundary, rights-coverage semantics, token domains, bypass model, or required status source requires renewed governance review.
