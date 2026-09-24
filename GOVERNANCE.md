# Macro Evidence — Governance & Decision-Making Charter

> Version 2.0.0 · Active · Last updated 2026-09-24

---

## 1. Purpose

This charter defines how Macro Evidence evaluates, records, reviews, and changes material organizational and technical decisions.

The objective is durable decision quality: choices should be explicit, evidence-based, auditable, maintainable, and reversible when new evidence or changed conditions justify reconsideration. The process is intentionally lightweight enough to remain practical while remaining clear enough to adopt without renegotiating first principles.

---

## 2. Decision Criteria

Every non-trivial addition, including a tool, dependency, dataset, repository, architectural change, workflow, policy, or product, is evaluated against the following criteria.

| Criterion | Question asked |
| --- | --- |
| Necessity | Does this solve a real, current problem rather than a hypothetical future one? |
| Simplicity | Is this the simplest solution that fully addresses the problem? |
| Consistency | Does this align with existing standards and conventions rather than creating unnecessary one-off behavior? |
| Maintainability | Can this remain understandable, operable, and evolvable over time without disproportionate maintenance burden? |
| Reproducibility | Can this be recreated and verified from documented procedures without depending on access unavailable to the intended users or maintainers? |

The criteria are not a scorecard. A proposal does not become acceptable merely because most criteria pass. Implementation is deferred while any material unresolved failure remains.

Trade-offs are permitted when they are explicit, proportionate, and justified by evidence. A decision may accept a bounded weakness in one criterion when doing so is necessary to satisfy a more material requirement and the resulting risk is understood and documented.

---

## 3. Execution Model

Work proceeds through explicit, ordered stages.

1. A task or decision is defined with its objective, evidence, dependencies, scope, and expected deliverable.
2. Material alternatives and constraints are considered before implementation when they could change the decision boundary.
3. The selected direction is approved before consequential implementation begins.
4. Once accepted, the decision becomes the working baseline and is not reopened for preference alone. Reconsideration requires new evidence, changed conditions, or a material defect.
5. Completion means producing and verifying the real deliverable, such as code, documentation, configuration, deployment, policy, or operational process, rather than merely planning it.

This execution model applies across Macro Evidence initiatives. Repository-specific workflows may add implementation stages, but they must preserve the same decision discipline.

---

## 4. Review Cadence

Governance is reviewed when material change is proposed, when new evidence creates a concrete conflict or stale claim, and as a whole at least quarterly while Macro Evidence remains actively maintained. A periodic review may conclude that no change is needed.

A review date does not itself reopen an accepted decision. Reconsideration requires new evidence, changed conditions, or a material defect. Whole-corpus review checks for contradictions across canonical documents, stale current-state claims, unresolved proposals, and external dependencies whose material change could affect an existing rule or decision.

Time-bound or externally dependent claims should be reverified when they materially affect a decision or public statement, rather than being assumed current because they were true at an earlier review.

---

## 5. Decision Records

Non-trivial technical and organizational decisions are recorded as Architecture Decision Records (ADRs) when preserving the decision boundary, rationale, and consequences will materially help future maintenance or governance.

Repository-specific decisions live in that repository's own `decisions/` directory. Decisions that genuinely apply across multiple repositories or to Macro Evidence's organization-level structure live in this repository under [`decisions/`](decisions/).

The organization-wide ADR contract, including placement, repository-local numbering, filenames, cross-repository references, lifecycle metadata, required sections, decision-boundary grammar, and index responsibilities, is defined in [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md) §5. Repository indexes may add local orientation, but they must not redefine that shared contract.

An ADR is not required for every implementation detail. Use an ADR when the decision has durable architectural, public-interface, policy, rights, governance, or cross-cutting consequences, or when the cost of later rediscovery would be material.

---

## 6. Governance Hierarchy

Governance documents have explicit precedence within their scopes.

| Level | Canonical document |
| --- | --- |
| Organization mission, vision, platform roles, product relationships, durable direction | [`ORGANIZATION_CHARTER.md`](ORGANIZATION_CHARTER.md) |
| Organization governance and decision-making | [`GOVERNANCE.md`](GOVERNANCE.md) |
| Documentation and ADR standards | [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md) |
| Organization policies within their defined subjects | [`CONTRIBUTION_POLICY.md`](CONTRIBUTION_POLICY.md); [`TRADEMARKS.md`](TRADEMARKS.md) |
| Approved legal instruments and their public operating process | [`legal/cla/`](legal/cla/) within the scope established by applicable policy and ADRs |
| Repository policies and ADRs | Repository-specific governance documents and decisions |
| Repository implementation and current runtime behavior | Repository documentation, source, configuration, and verified runtime evidence |

Precedence is scope-aware. A higher-listed document does not become canonical for a subject outside its defined role. Policies at the same level govern their own subjects; listing order does not let one silently override another.

When two canonical sources appear to conflict, resolve the conflict by scope, freshness, and authority rather than silently selecting the more convenient statement. Repository documentation may extend organization standards but must not contradict them.

---

## 7. Versioning Foundational Documents

This charter, [`ORGANIZATION_CHARTER.md`](ORGANIZATION_CHARTER.md), [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md), [`CONTRIBUTION_POLICY.md`](CONTRIBUTION_POLICY.md), and [`TRADEMARKS.md`](TRADEMARKS.md) are versioned independently using Semantic Versioning (`MAJOR.MINOR.PATCH`).

| Version | Meaning |
| --- | --- |
| **MAJOR** | Fundamental governance principles, authority boundaries, or execution models change. |
| **MINOR** | New governance capabilities, materially expanded rules, or new durable subject boundaries are introduced. |
| **PATCH** | Editorial, formatting, factual-correction, or clarification changes that do not alter policy. |

Every released version includes a changelog entry. A version enters release history only when that version is published in canonical repository history. Uncommitted candidates do not create historical releases.

When one release contains changes of different levels, use the highest applicable SemVer level. Changelog entries should distinguish policy/capability changes from mechanical or editorial cleanup so the version choice remains auditable.

Governance documents are never silently modified.

---

## Changelog

### 2.0.0 (2026-09-24)

- Replaces the earlier weekly review model with event-driven review plus a quarterly whole-corpus review, while keeping reconsideration tied to new evidence, changed conditions, or material defects.
- Reframes decision criteria as material gates rather than a scorecard and clarifies proportionate trade-offs.
- Makes the shared ADR contract, repository implementation truth, legal-instrument scope, and release-history rules explicit in the governance hierarchy.
- Makes governance records durable public documents that are self-contained and understandable from their public context.
- Clarifies that accepted decisions are not cosmetically rewritten to fit later conventions and that material changes require a new decision.
- Preserves all previously released changelog entries exactly as historical record.
- MAJOR — replaces the fixed weekly review cadence with event-driven plus quarterly whole-corpus review and reframes decision criteria from a scorecard into material gates; the shared ADR contract and governance hierarchy precedence are unchanged.

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
