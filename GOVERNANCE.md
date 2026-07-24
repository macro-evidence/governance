# Macro Evidence — Governance & Decision-Making Charter

> Version 1.1.0 · Active · Last updated 2026-07-24

---

## 1. Purpose

This charter defines how decisions are made across Macro Evidence and its platforms.

During the organization's early stages, it provides a disciplined framework for consistent, auditable, and reversible decision-making. As Macro Evidence grows, these principles remain the foundation for collaborative governance rather than being renegotiated for each new contributor, repository, or product.

---

## 2. Decision Criteria

Every non-trivial addition—including a tool, dependency, dataset, repository, architectural change, workflow, or product—is evaluated against the following criteria:

| Criterion | Question asked |
|-----------|----------------|
| Necessity | Does this solve a real, current problem rather than a hypothetical future one? |
| Simplicity | Is this the simplest solution that fully addresses the problem? |
| Consistency | Does this align with existing standards and conventions rather than introducing a one-off pattern? |
| Maintainability | Can this still be understood, maintained, and evolved a year from now? |
| Reproducibility | Can this be recreated from scratch using documented procedures and supported infrastructure? |
| Scalability | Will this remain effective as Macro Evidence grows in repositories, products, contributors, and operational complexity? |

If a proposal fails more than one criterion, implementation is deferred until the proposal satisfies the governance criteria.

---

## 3. Execution Model

Work proceeds through explicit, ordered stages:

1. Tasks are proposed with objectives, dependencies, and expected deliverables clearly defined.
2. Each task is reviewed and approved through the project's current governance process before implementation begins.
3. Once approved, a decision becomes the project's baseline unless a concrete technical issue—not a preference change—requires reconsideration.
4. Completing a task means producing a real, usable deliverable (such as a repository, document, deployment, implementation, or automation), not merely planning one.

This staged execution model applies across all Macro Evidence initiatives.

---

## 4. Review Cadence

Governance documents and architectural decisions are reviewed periodically or whenever significant architectural, organizational, or operational changes occur.

Any decision affecting an existing public interface, schema, API, governance principle, or long-term architectural direction must be documented through the decision-record process rather than remaining implicit.

---

## 5. Decision Records

Non-trivial technical and organizational decisions are documented as Architecture Decision Records (ADRs).

Each ADR records:

- The decision
- Context
- Alternatives considered
- Rationale
- Consequences

Organization-wide ADRs are maintained within the Governance repository. Repository-specific ADRs may be maintained locally when appropriate, provided they remain consistent with organization-wide governance.

---

## 6. Governance Hierarchy

Governance documents have explicit precedence. When guidance overlaps, higher-level documents take priority.

| Level | Canonical Document |
|--------|--------------------|
| Organization mission, vision, scope | `ORGANIZATION_CHARTER.md` |
| Organization governance and decision-making | `GOVERNANCE.md` |
| Documentation standards and conventions | `DOCUMENTATION_STANDARDS.md` |
| Repository policies | Repository-specific governance documents |
| Repository implementation details | Repository `README.md` and technical documentation |

Repository documentation may extend organization standards but must not contradict them.

---

## 7. Versioning Foundational Documents

The Organization Charter, Governance Charter, and Documentation Standards are versioned independently using Semantic Versioning (`MAJOR.MINOR.PATCH`).

| Version | Meaning |
|----------|---------|
| **MAJOR** | Fundamental governance principles or decision models change. |
| **MINOR** | New sections, governance capabilities, or materially expanded guidance are introduced. |
| **PATCH** | Editorial, formatting, or clarification changes without altering meaning or policy. |

Every released version includes a changelog entry. Governance documents are never silently modified.

---

## Changelog

### 1.1.0 (2026-07-24)

- Generalized governance language beyond the single-maintainer stage.
- Added **Scalability** as a formal decision criterion.
- Clarified the governance approval process.
- Replaced "fixed" decisions with governance baselines.
- Replaced a fixed weekly review schedule with principle-based review triggers.
- Defined Architecture Decision Record (ADR) ownership and storage within the Governance repository.
- Introduced a Governance Hierarchy defining document precedence.
- Expanded versioning guidance and aligned it with Semantic Versioning terminology.

### 1.0.0 (2026-07-23)

Initial version. Formalized the decision criteria and staged execution model established during the organization's foundation phase.