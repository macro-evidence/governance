# Macro Evidence — Documentation Standards

> Version 1.3.1 · Active · Last updated 2026-08-20

---

## 1. Principle

Documentation is an engineering artifact, produced alongside the work it describes—not after it. A change without updated documentation is not considered complete.

Documentation evolves with the systems it describes and must remain synchronized with implementation. Current-state documentation records what is true now. Documents whose explicit purpose includes vision, roadmap, proposals, or other future direction may describe that direction, but it must be clearly identified as future-facing and must never be presented as already delivered.

---

## 2. Writing Principles

- Precise over persuasive — avoid marketing language in engineering documentation.
- Current-state claims state what is true now. Planned or aspirational capability is labeled explicitly and is never written as though it is already delivered.
- Status is always explicit (`Draft`, `Active`, `Superseded`), never implied.
- Paraphrase and consolidate rather than duplicate. If two documents would communicate the same information, one links to the other instead.
- Every document has a clearly defined owner and purpose.

---

## 3. Documentation Ownership

| Content | Canonical Home |
|---------|----------------|
| Organization mission, vision, platform scope, roadmap | [`ORGANIZATION_CHARTER.md`](ORGANIZATION_CHARTER.md) |
| Governance principles, decision-making, review cadence | [`GOVERNANCE.md`](GOVERNANCE.md) |
| Documentation conventions and writing standards | This document |
| Architecture Decision Records (ADRs) — repository-specific | That repository's own `decisions/` (e.g. [`macro-data-observatory/decisions/`](https://github.com/macro-evidence/macro-data-observatory/tree/main/decisions)) |
| Architecture Decision Records (ADRs) — cross-cutting | [`decisions/`](decisions/) in this repository |
| Trademark, brand, and organizational identity policy | [`TRADEMARKS.md`](TRADEMARKS.md) |
| Repository-specific setup, development, usage | That repository's own `README.md` |
| Public organization overview | [`.github` profile README](https://github.com/macro-evidence/.github/blob/main/profile/README.md) |

A topic should have exactly one canonical owner. Other documents reference that owner instead of duplicating its content.

---

## 4. Formatting Conventions

- Use tables for structured information (status, comparisons, roadmaps, inventories).
- Use prose for rationale, assumptions, and explanations.
- Include a one-line blockquote tagline beneath the title of the organization's brand-facing documents (e.g., the `.github` profile README). Governance and policy documents use the version/status blockquote only, not a tagline.
- Separate major sections with horizontal rules in long-form documents.
- Use fenced code blocks for commands, configuration, and examples.
- Use directory trees when documenting repository or project structure.
- Use absolute URLs where content must render correctly outside a normal repository context (organization profile README, issue templates). Use relative links elsewhere.

---

## 5. Naming Conventions

Repository, module, dataset, directory, and variable naming standards are introduced only when they become necessary—beginning with MDO's schema and engineering work—rather than being defined speculatively.

This section evolves incrementally and is updated through a **MINOR** version bump (see [`GOVERNANCE.md`](GOVERNANCE.md)).

---

## 6. Commit Conventions

Macro Evidence follows the Conventional Commits specification.

Supported prefixes include:

- `feat:`
- `fix:`
- `docs:`
- `refactor:`
- `test:`
- `chore:`

Guidelines:

- One logical change per commit.
- Commit messages are written in the present tense.
- Avoid combining unrelated changes into a single commit.

---

## Changelog

- **1.3.1** (2026-08-20)
  - Clarified §§1–2 so current-state claims must describe what is true now while explicitly future-facing document sections (such as vision or roadmap) may state future direction when clearly labeled; this reconciles the writing rule with the existing documentation ownership of organization vision and roadmap.
  - Tightened the tagline formatting rule (§4) to match actual practice: taglines are reserved for brand-facing documents, while governance and policy documents use their version/status blockquote without a tagline.
  - PATCH — both changes clarify existing document types and practice; documentation ownership and the prohibition on presenting planned capability as already delivered are unchanged.

- **1.3.0** (2026-08-09)
  - Split ADR ownership: repository-specific ADRs are owned by that repository's own `decisions/`; only cross-cutting ADRs are owned by this repository's `decisions/`. See `GOVERNANCE.md` 1.4.0 and `macro-data-observatory` decision 0008.

- **1.2.0** (2026-08-08)
  - Added Documentation Ownership entry for `TRADEMARKS.md`.

- **1.1.0** (2026-07-24)
  - Renamed **Voice** to **Writing Principles**.
  - Added documentation synchronization principle.
  - Clarified documentation ownership and canonical sources.
  - Expanded formatting conventions.
  - Expanded commit conventions.
  - Updated references following creation of the dedicated `governance` repository.

- **1.0.0** (2026-07-23)
  - Initial version. Formalized documentation conventions established during the organization foundation phase.
  