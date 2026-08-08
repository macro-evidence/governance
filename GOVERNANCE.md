# Macro Evidence — Governance & Decision-Making Charter

> Version 1.3.1 · Active · Last updated 2026-08-08

---

## 1. Purpose

This charter defines how decisions are made across Macro Evidence and its platforms.

At the current single-maintainer stage, its purpose is less about coordinating multiple people and more about keeping one person's decisions consistent, auditable, and reversible. This discipline establishes stable governance today while providing a foundation that future collaborators can adopt without renegotiating first principles.

---

## 2. Decision Criteria

Every non-trivial addition—including a tool, dependency, dataset, repository, architectural change, workflow, or product—is evaluated against the following criteria.

| Criterion | Question asked |
|-----------|----------------|
| Necessity | Does this solve a real, current problem rather than a hypothetical future one? |
| Simplicity | Is this the simplest solution that fully addresses the problem? |
| Consistency | Does this align with existing standards and conventions rather than introducing a one-off pattern? |
| Maintainability | Can this still be understood and evolved a year from now by a single maintainer? |
| Reproducibility | Can this be recreated from scratch using documented procedures on free-tier infrastructure? |

If a proposal fails more than one criterion, implementation is deferred until it satisfies the governance criteria.

---

## 3. Execution Model

Work proceeds through explicit, ordered stages.

1. Tasks are proposed with objectives, dependencies, and expected deliverables clearly defined.
2. Each task is reviewed and approved before implementation begins.
3. Once approved, a decision becomes the project's baseline unless a concrete technical issue—not a preference change—requires reconsideration.
4. Completing a task means producing a real, usable deliverable (repository, document, deployment, implementation, or automation), not merely planning one.

This staged execution model applies across all Macro Evidence initiatives.

---

## 4. Review Cadence

Governance documents and architectural decisions are reviewed weekly by the maintainer during the organization's current stage.

Any decision affecting an existing public interface, schema, API, governance principle, or long-term architectural direction must be documented through an Architecture Decision Record (ADR) rather than remaining implicit.

---

## 5. Decision Records

Non-trivial technical and organizational decisions are documented as Architecture Decision Records (ADRs).

Each ADR records:

- Decision
- Context
- Alternatives considered
- Rationale
- Consequences

ADRs are maintained in this repository under [`decisions/`](decisions/). The ADR format is defined in [`decisions/README.md`](decisions/README.md).

---

## 6. Governance Hierarchy

Governance documents have explicit precedence.

When guidance overlaps, higher-level documents take priority.

| Level | Canonical Document |
|--------|--------------------|
| Organization mission, vision, scope | [`ORGANIZATION_CHARTER.md`](ORGANIZATION_CHARTER.md) |
| Organization governance and decision-making | [`GOVERNANCE.md`](GOVERNANCE.md) |
| Documentation standards and conventions | [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md) |
| Trademark, brand, and organizational identity | [`TRADEMARKS.md`](TRADEMARKS.md) |
| Repository policies | Repository-specific governance documents |
| Repository implementation details | Repository `README.md` and technical documentation |

Repository documentation may extend organization standards but must never contradict them.

---

## 7. Versioning Foundational Documents

This charter `GOVERNANCE.md`, [`ORGANIZATION_CHARTER.md`](ORGANIZATION_CHARTER.md), [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md), and [`TRADEMARKS.md`](TRADEMARKS.md) are versioned independently using Semantic Versioning (`MAJOR.MINOR.PATCH`).

| Version | Meaning |
|----------|---------|
| **MAJOR** | Fundamental governance principles or execution models change. |
| **MINOR** | New governance capabilities, sections, or materially expanded guidance are introduced. |
| **PATCH** | Editorial, formatting, wording, or clarification changes that do not alter governance policy. |

Every released version includes a changelog entry.

Governance documents are never silently modified.

---

## Changelog

### 1.3.1 (2026-08-08)

- Removed stale "No ADRs exist yet" text — 7 ADRs are on record as of this correction, and a live count in prose would itself go stale over time; `decisions/` is the source of truth.

### 1.3.0 (2026-08-08)

- Added `TRADEMARKS.md` to the Governance Hierarchy and to the list of independently versioned foundational documents.

### 1.2.0 (2026-07-24)

- Added Governance Hierarchy defining document precedence.
- Expanded Architecture Decision Record guidance.
- Improved execution model wording.
- Added explicit ADR structure and repository links.
- Clarified Semantic Versioning guidance.
- Preserved single-maintainer governance philosophy while preparing for future collaboration.

### 1.1.0 (2026-07-24)

- Defined ADR storage under `decisions/`.
- Linked sibling governance documents.
- Added ADR format reference.

### 1.0.0 (2026-07-23)

Initial version. Formalized the decision criteria and staged execution model established during the organization's foundation phase.