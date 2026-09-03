# Macro Evidence — Governance & Decision-Making Charter

> Version 1.5.0 · Active · Last updated 2026-09-03

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

Each ADR records the context, decision, and consequences of the decision.

ADRs are recorded where the decision actually applies: repository-specific decisions live in that repository's own `decisions/` folder (e.g. [`macro-data-observatory/decisions/`](https://github.com/macro-evidence/macro-data-observatory/tree/main/decisions)); decisions that genuinely apply across multiple repositories or to the organization's structure itself are recorded in this repository under [`decisions/`](decisions/). The exact ADR format is defined in each location's own `decisions/README.md`.

---

## 6. Governance Hierarchy

Governance documents have explicit precedence.

When guidance overlaps, higher-level documents take priority.

| Level | Canonical Document |
|--------|--------------------|
| Organization mission, vision, scope | [`ORGANIZATION_CHARTER.md`](ORGANIZATION_CHARTER.md) |
| Organization governance and decision-making | [`GOVERNANCE.md`](GOVERNANCE.md) |
| Documentation standards and conventions | [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md) |
| Organization policies within their defined subject | [`CONTRIBUTION_POLICY.md`](CONTRIBUTION_POLICY.md); [`TRADEMARKS.md`](TRADEMARKS.md) |
| Repository policies | Repository-specific governance documents |
| Repository implementation details | Repository `README.md` and technical documentation |

The hierarchy is scope-aware. Precedence applies when documents genuinely govern the same question; a higher-listed document does not become canonical for a subject outside its defined scope. Organization policies at the same level are canonical within their own subjects, and their listing order does not allow one to override another outside its scope. If two scope-specific policies genuinely conflict, the conflict must be reconciled deliberately under the higher-level organization and governance rules rather than resolved by silently choosing one.

Repository documentation may extend organization standards but must never contradict them.

---

## 7. Versioning Foundational Documents

This charter `GOVERNANCE.md`, [`ORGANIZATION_CHARTER.md`](ORGANIZATION_CHARTER.md), [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md), [`CONTRIBUTION_POLICY.md`](CONTRIBUTION_POLICY.md), and [`TRADEMARKS.md`](TRADEMARKS.md) are versioned independently using Semantic Versioning (`MAJOR.MINOR.PATCH`).

| Version | Meaning |
|----------|---------|
| **MAJOR** | Fundamental governance principles or execution models change. |
| **MINOR** | New governance capabilities, sections, or materially expanded guidance are introduced. |
| **PATCH** | Editorial, formatting, wording, or clarification changes that do not alter governance policy. |

Every released version includes a changelog entry.

Governance documents are never silently modified.

---

## Changelog

### 1.5.0 (2026-09-03)

- Added `CONTRIBUTION_POLICY.md` to the governance hierarchy as the canonical organization-wide owner of contribution participation, acceptance, and contributor-rights policy.
- Clarified that scope-specific organization policies at the same hierarchy level govern within their own subjects and do not silently override one another.
- Added the Contribution Policy to the independently versioned governance-document set.
- Normalized the 1.0.0 changelog summary to the canonical governance/policy-document structure defined in `DOCUMENTATION_STANDARDS.md` §4; no governance semantics changed.
- MINOR — introduces a new cross-repository governance capability and makes the policy-precedence boundary explicit without changing the existing decision criteria, execution model, or ADR placement rules.

### 1.4.1 (2026-08-20)

- Corrected §5's ADR-content description to match the repository-owned ADR templates: ADRs record context, decision, and consequences, while each applicable `decisions/README.md` owns the exact format. Removed the stale requirement for separate "Alternatives considered" and "Rationale" sections. PATCH — clarification only; the decision-record process and ADR placement rules are unchanged.

### 1.4.0 (2026-08-09)

- §5: ADRs now split by scope — repository-specific decisions live in that repository's own `decisions/`; only genuinely cross-cutting decisions stay in this repository. See `macro-data-observatory` decision 0008 for the full reasoning. All 7 prior ADRs moved to `macro-data-observatory/decisions/`, none having turned out to be cross-cutting on review.

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

- Initial version. Formalized the decision criteria and staged execution model established during the organization's foundation phase.
