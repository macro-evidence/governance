# Macro Evidence — Documentation Standards

> Version 1.7.0 · Active · Last updated 2026-10-11

---

## 1. Principle

Documentation is an engineering artifact. It is maintained with the work it describes, not reconstructed after the fact.

Current-state documentation states what is true now. Future-facing material may describe proposals, direction, or planned capability only when that role is explicit; it must never present an unimplemented state as delivered.

Public documentation must also be understandable from the public record itself. It must contain sufficient context to explain the documented subject without relying on information that is not part of the public record.

---

## 2. Writing and Public-Boundary Principles

- Prefer precise, testable language over persuasive or promotional language in engineering and governance documentation.
- Distinguish current fact, accepted decision, proposal, and future direction explicitly.
- Preserve the public/private boundary: explain the durable reason for a decision without reproducing non-public process or context.
- Do not expose non-public information unless it is necessary to understand a public rule, accepted decision, or documented behavior.
- Paraphrase and consolidate rather than duplicate. If one document already owns a rule or current fact, other documents link to it instead of restating it in full.
- Every durable document has a defined purpose and canonical owner.
- Documents and decisions with an independent lifecycle carry explicit status metadata. Repository/index READMEs and supporting documents whose currency is defined by the repository revision do not require artificial lifecycle metadata.

---

## 3. Documentation Ownership

| Content | Canonical home |
| --- | --- |
| Organization mission, vision, platform roles, product relationships, durable direction | [`ORGANIZATION_CHARTER.md`](ORGANIZATION_CHARTER.md) |
| Governance principles, decision-making, review cadence, document precedence | [`GOVERNANCE.md`](GOVERNANCE.md) |
| Documentation conventions, ADR grammar, naming and commit conventions | This document |
| Repository-specific Architecture Decision Records (ADRs) | That repository's own `decisions/` |
| Cross-cutting Architecture Decision Records (ADRs) | [`decisions/`](decisions/) in this repository |
| Trademark, brand, and organizational identity policy | [`TRADEMARKS.md`](TRADEMARKS.md) |
| Organization-wide contribution participation, acceptance, and contributor-rights policy | [`CONTRIBUTION_POLICY.md`](CONTRIBUTION_POLICY.md) |
| Contributor-agreement legal forms, execution process, privacy notice, third-party-material process, and provenance | [`legal/cla/`](legal/cla/) |
| Organization-wide GitHub community-health files | [`macro-evidence/.github`](https://github.com/macro-evidence/.github) |
| Repository-specific setup, development, implementation, usage, and current runtime behavior | That repository's own documentation |
| Public organization overview | [`.github` profile README](https://github.com/macro-evidence/.github/blob/main/profile/README.md) |

A subject should have one canonical owner at a given scope. Other documents may summarize for orientation, but they must not maintain a second normative copy that can drift from the owner.

---

## 4. Document Lifecycle and Versioning

Current-state supporting documents are revised in place, with repository history providing chronology. Documents whose policy or governance state must be independently auditable use explicit version/status metadata and changelogs.

For independently versioned governance and policy documents:

- the title is followed by one version/status blockquote;
- `## Changelog` contains one level-three heading per released version in the form `### MAJOR.MINOR.PATCH (YYYY-MM-DD)`, newest first;
- each release heading is followed by a bulleted summary whose first bullet states the change class (`MAJOR`, `MINOR`, or `PATCH`) and a concise rationale under the owning policy's definitions, and whose later bullets record notable changes rather than commit history; an initial release states "Initial version." in place of a change class;
- historical entries are not rewritten to adopt this order unless a factual defect makes correction necessary;
- only a version actually published in canonical repository history enters the changelog as a released version;
- an unreleased revision uses explicit candidate/not-active metadata and, if a change summary is useful, records it under `## Candidate changes for MAJOR.MINOR.PATCH` outside the released changelog;
- uncommitted candidate numbering does not create release history; and
- on publication, the approved candidate summary becomes the dated changelog entry and candidate/not-active metadata is removed.

Where Semantic Versioning is used for governance documents, the owning policy defines the meaning of `MAJOR`, `MINOR`, and `PATCH`.

---

## 5. Architecture Decision Records

ADRs record durable decisions, not meeting notes or private deliberation. An ADR should be self-contained for a future reader who has the repository and its public references.

### 5.1 Placement and numbering

- Repository-specific decisions live in that repository's own `decisions/` directory.
- Decisions that genuinely apply across multiple repositories or to Macro Evidence's organization-level structure live in this repository's `decisions/` directory.
- Decision numbering is repository-local and sequential.
- One file records one decision boundary, named `NNNN-short-title.md`.
- Within the repository that owns a decision, refer to it as `decision NNNN` when qualification is unnecessary.
- When referring to a decision owned by another repository, qualify it with the repository name, for example `governance decision 0001` or `macro-data-observatory decision 0008`.

### 5.2 Lifecycle metadata

Use these metadata forms:

```markdown
**Status:** Proposed
```

```markdown
**Status:** Accepted
**Date:** YYYY-MM-DD
```

```markdown
**Status:** Superseded
**Superseded by:** [decision NNNN](relative-link.md)
```

Rules:

- `Date` records acceptance and appears only while the ADR is `Accepted`.
- Proposed ADRs do not carry an acceptance date.
- When an ADR is superseded, remove its acceptance `Date`, set `Status` to `Superseded`, and identify the replacement decision or decisions under `Superseded by`.
- Superseding a decision does not delete the earlier ADR. Git history and the retained ADR preserve chronology.
- An accepted ADR is not cosmetically rewritten merely to conform to a later editorial convention. A material change in the decision is recorded in a new ADR. A narrowly scoped correction to an active ADR may be made when it fixes a factual error or removes ambiguity without changing the decision; the change must remain auditable in repository history.

### 5.3 Required structure

A new ADR uses:

```markdown
# NNNN. Short title

**Status:** Proposed

## Context

What durable problem or question this decision addresses, including the evidence needed to understand the choice.

## Decision

What is decided and the boundary of that decision.

## Consequences

Expected benefits, costs, trade-offs, risks, and follow-up implications.
```

Use the singular `## Decision` heading for one coherent decision boundary. Use `## Decisions` only when multiple choices are genuinely inseparable and must stand or fall together. Choices that can be accepted, revisited, or superseded independently receive separate decision numbers.

Alternatives do not require a separate heading, but a non-obvious decision should make the material alternatives and trade-offs understandable in `Context`, `Decision`, or `Consequences` rather than presenting a conclusion without the competing options that made the decision necessary.

### 5.4 Decision indexes

A repository's `decisions/README.md` is an orientation and index surface. It should contain only:

- what class of decisions belongs in that repository;
- a link to this shared ADR standard;
- genuinely repository-local context, if any; and
- a title-only index of decisions.

Decision indexes do not duplicate lifecycle status, the shared ADR template, numbering grammar, cross-repository reference grammar, or singular/plural decision rules.

---

## 6. Mechanical Documentation Verification

Maintained Markdown must pass a documented repository verification path before documentation changes are released.

Macro Evidence uses the standard `markdownlint` rule set with line-length enforcement disabled by default. Long prose lines, tables, and URLs are not mechanically reflowed merely to satisfy an arbitrary column width.

Repository-specific exceptions are permitted only when a default rule is semantically wrong for a specific document role or preserved historical record. Exceptions must be narrow, explained, and no broader than necessary.

CI automation is not mandatory in every repository. A documentation-only repository may use a documented local verification command when dedicated automation would add disproportionate tooling, maintenance, or licensing surface. Repositories that already operate suitable CI should integrate documentation verification when doing so is simple and maintainable.

Automatic formatting is not an organization-wide requirement. Formatters must not silently rewrite prose, policy wording, tables, or other editorial structure merely to impose a tool's preferred layout.

Exact verification tools, versions, dependency locks, and CI implementation are repository-local details. A repository must not knowingly rely on a verification toolchain with an unresolved material security defect when a reasonable maintained alternative is available.

---

## 7. Formatting Conventions

- Use tables when they materially improve structured comparison or inventories; do not use them merely to make prose look formal.
- Use prose for rationale, assumptions, decisions, and explanations.
- Use fenced code blocks for commands, configuration, and examples.
- Use directory trees when repository structure is itself relevant.
- Use absolute URLs where content must render correctly outside a repository context; use relative links for same-repository references.
- Governance and policy documents use their version/status blockquote rather than a brand tagline.
- Standalone brand-facing documents may use a one-line descriptor or tagline when it is part of that document's role and does not duplicate surrounding platform identity.

---

## 8. Naming Conventions

Use names that are descriptive, stable, and scoped to the artifact they identify. Do not introduce organization-wide naming rules speculatively when the organization has no repeated pattern to govern.

Repository-specific naming rules belong with the repository or subsystem they constrain. A local naming convention becomes an organization-wide standard only when the same recurring problem exists across repositories and centralizing the rule reduces ambiguity or duplication.

---

## 9. Commit Conventions

Macro Evidence uses Conventional Commits for repository history.

Supported types include:

- `feat:`
- `fix:`
- `docs:`
- `refactor:`
- `test:`
- `chore:`

A commit may include an optional scope in parentheses after the type when the scope materially clarifies the affected area, using `type(scope): description`.

Scope guidelines:

- Scopes are optional; do not add one merely for consistency with nearby commits.
- Use a concise noun that identifies a coherent affected area.
- Reuse an existing scope when it accurately describes the same concern.
- Do not force a change into an inaccurate scope merely to reuse one.
- Use an unscoped commit when the change is repository-wide or the type and description are already clear.

Commit guidelines:

- one logical change per commit;
- present-tense descriptions; and
- no unrelated changes combined only for convenience.

---

## Changelog

### 1.7.0 (2026-10-11)

- MINOR — standardizes how each release entry in the changelogs of independently versioned governance and policy documents is written, by requiring its first bullet to state the change class and a concise rationale; the existing version-heading form, ordering, and release-publication rules are unchanged.
- Requires later bullets to record notable changes rather than commit history, and requires an initial release to state "Initial version." in place of a change class.
- Preserves all previously released changelog entries exactly as historical record unless a factual defect makes correction necessary.

### 1.6.0 (2026-09-24)

- Makes public self-containment and the public/private boundary explicit as core documentation requirements.
- Establishes one canonical owner for each durable subject and separates normative owners from orientation/index surfaces.
- Defines the shared ADR contract for placement, numbering, lifecycle metadata, required structure, decision boundaries, alternatives, and decision indexes.
- Adds reproducible Markdown verification, formatting safeguards, and documentation-tooling security requirements without requiring CI in every documentation-only repository.
- Clarifies repository-local naming and commit conventions while preserving the existing organization-wide boundaries.
- Preserves repository history by leaving all previously released changelog entries unchanged.
- MINOR — introduces the public self-containment principle, the one-canonical-owner rule, the shared ADR contract, and reproducible Markdown verification as new documentation requirements; existing document ownership assignments, naming conventions, and the commit-type list are unchanged.

### 1.5.0 (2026-09-03)

- Added canonical ownership for the organization-wide Contribution Policy.
- Distinguished cross-repository contribution policy in `governance` from organization-wide GitHub community-health files in `.github`.
- Standardized changelog structure for independently versioned governance and policy documents: each released version is represented as a level-three heading followed by a bulleted release summary.
- MINOR — introduces documentation ownership for a new governance capability and standardizes changelog structure; other writing, formatting, naming, and commit conventions are unchanged.

### 1.4.0 (2026-08-21)

- Expanded §6 with explicit guidance for optional Conventional Commit scopes, including when to reuse an existing scope, when to introduce a new scope, and when to leave a commit unscoped.
- MINOR — formalizes established scope usage already present across Macro Evidence repository history; the supported commit types and one-logical-change rule are unchanged.

### 1.3.2 (2026-08-20)

- Clarified §4 so the tagline convention applies to standalone brand-facing documents, while documents rendered within platform surfaces do not repeat equivalent organization identity or descriptive text already supplied by the surrounding interface.
- PATCH — reconciles the formatting convention with §2's no-duplication principle; documentation ownership and trademark/identity policy are unchanged.

### 1.3.1 (2026-08-20)

- Clarified §§1–2 so current-state claims must describe what is true now while explicitly future-facing document sections (such as vision or roadmap) may state future direction when clearly labeled; this reconciles the writing rule with the existing documentation ownership of organization vision and roadmap.
- Tightened the tagline formatting rule (§4) to match actual practice: taglines are reserved for brand-facing documents, while governance and policy documents use their version/status blockquote without a tagline.
- PATCH — both changes clarify existing document types and practice; documentation ownership and the prohibition on presenting planned capability as already delivered are unchanged.

### 1.3.0 (2026-08-09)

- Split ADR ownership: repository-specific ADRs are owned by that repository's own `decisions/`; only cross-cutting ADRs are owned by this repository's `decisions/`. See `GOVERNANCE.md` 1.4.0 and `macro-data-observatory` decision 0008.

### 1.2.0 (2026-08-08)

- Added Documentation Ownership entry for `TRADEMARKS.md`.

### 1.1.0 (2026-07-24)

- Renamed **Voice** to **Writing Principles**.
- Added documentation synchronization principle.
- Clarified documentation ownership and canonical sources.
- Expanded formatting conventions.
- Expanded commit conventions.
- Updated references following creation of the dedicated `governance` repository.

### 1.0.0 (2026-07-23)

- Initial version. Formalized documentation conventions established during the organization foundation phase.
