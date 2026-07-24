# Macro Evidence — Documentation Standards

> Version 1.1.0 · Active · Last updated 2026-07-24

---

## 1. Principle

Documentation is an engineering artifact, produced alongside the work it describes—not after it. A change without updated documentation is not considered complete.

Documentation evolves with the systems it describes and must remain synchronized with implementation. Documentation records the current state of the project, not future intentions.

---

## 2. Writing Principles

- Precise over persuasive — avoid marketing language in engineering documentation.
- Every document states what is true now, not what is aspirational.
- Status is always explicit (`Draft`, `Active`, `Superseded`), never implied.
- Paraphrase and consolidate rather than duplicate. If two documents would communicate the same information, one links to the other instead.
- Every document has a clearly defined owner and purpose.

---

## 3. Documentation Ownership

| Content | Canonical Home |
|---------|----------------|
| Organization mission, vision, platform scope, roadmap | `ORGANIZATION_CHARTER.md` |
| Governance principles, decision-making, review cadence | `GOVERNANCE.md` |
| Documentation conventions and writing standards | This document |
| Organization-wide engineering decisions | Architecture Decision Records (ADRs) |
| Repository-specific setup, development, usage | That repository's own `README.md` |
| Public organization overview | `.github/profile/README.md` |

A topic should have exactly one canonical owner. Other documents reference that owner instead of duplicating its content.

---

## 4. Formatting Conventions

- Use tables for structured information (status, comparisons, roadmaps, inventories).
- Use prose for rationale, assumptions, and explanations.
- Include a one-line blockquote tagline beneath the title of public-facing documents where appropriate.
- Separate major sections with horizontal rules in long-form documents.
- Use fenced code blocks for commands, configuration, and examples.
- Use directory trees when documenting repository or project structure.
- Use absolute URLs where content must render correctly outside a normal repository context (organization profile README, issue templates). Use relative links elsewhere.

---

## 5. Naming Conventions

Repository, module, dataset, directory, and variable naming standards are introduced only when they become necessary—beginning with MDO's schema and engineering work—rather than being defined speculatively.

This section evolves incrementally and is updated through a **MINOR** version bump (see `GOVERNANCE.md`).

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

- **1.1.0** (2026-07-24)
  - Renamed **Voice** to **Writing Principles**.
  - Added documentation synchronization principle.
  - Clarified documentation ownership and canonical sources.
  - Expanded formatting conventions.
  - Expanded commit conventions.
  - Updated references following creation of the dedicated `governance` repository.

- **1.0.0** (2026-07-23)
  - Initial version. Formalized documentation conventions established during the organization foundation phase.