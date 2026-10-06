# Macro Evidence — Organization & Platform Charter

> Version 1.3.1 · Active · Last updated 2026-10-06

---

## 1. Organization

### Mission

Macro Evidence builds open macroeconomic data infrastructure around provenance, validation, reproducibility, and transparency. It develops shared foundations, products, reference layers, and interfaces, each with clear canonical ownership.

### Vision

To become a lasting, trusted steward of open macroeconomic data infrastructure, built incrementally on evidence, one disciplined decision at a time.

### Engineering philosophy

- engineering rigor over presentation;
- reproducibility over one-off solutions;
- transparency over opacity;
- maintainability over short-term convenience;
- modular architecture over monoliths;
- documentation alongside implementation; and
- incremental capability growth over speculative scope.

---

## 2. Flagship and Foundational Platform — Macro Data Observatory (MDO)

Macro Data Observatory (MDO) is Macro Evidence's flagship and foundational macro-data platform.

Its role is to acquire, validate, structure, and maintain macroeconomic data from authoritative public sources through reproducible engineering. MDO owns the canonical technical and data truth for its data sources, series, metadata, transformations, interfaces, and runtime behavior.

MDO's durable objectives are to:

- maintain one coherent macroeconomic data foundation across authoritative public sources;
- normalize heterogeneous source data into consistent, researchable series;
- make provenance, validation, reproducibility, and maintainability explicit infrastructure requirements;
- provide the shared macro-data foundation for Macro Evidence products and interfaces that require canonical macroeconomic data; and
- keep implementation and architectural decisions documented in MDO's own canonical repository and runtime evidence.

MDO's implementation details, current provider coverage, live runtime state, schemas, and release status belong to the MDO repository and verified runtime evidence rather than this organization charter.

---

## 3. Product Ecosystem

Macro Evidence may develop products, interfaces, and reference layers with distinct roles while preserving one coherent macro-data foundation.

| Entity | Organization-level role | Canonical boundary |
| --- | --- | --- |
| Macro Evidence | Organization, governance, identity, and stewardship | Organization governance and public institutional records |
| Macro Data Observatory (MDO) | Flagship and foundational macro-data platform | MDO repository, canonical sources, decisions, and verified runtime evidence |
| Macro Data Dictionary (MDD) | Organization-level reference and explanatory layer | MDD repository and future MDD-specific canonical records |

MDD is an organization-owned sibling of MDO under Macro Evidence, not a child or subproject of MDO. It may explain macroeconomic terminology, metadata concepts, and reference material that applies across Macro Evidence products.

Where MDD presents MDO-specific technical or data facts, those facts derive from MDO's canonical sources. MDD does not create an independent competing source of truth for MDO's implementation or data.

Future products that require the same canonical macroeconomic data should build on, consume, expose, or otherwise operate on MDO's shared foundation rather than recreating a parallel macro-data foundation. Reference layers may span products without becoming independent data foundations.

Each new material product or layer is evaluated through the governance decision process before implementation. Product-specific architecture, URLs, identity, licensing, schemas, and feature scope remain repository-level or separately governed decisions unless they genuinely require organization-wide treatment.

---

## 4. Durable Direction

Macro Evidence is intended to mature as an ecosystem of professionally engineered public infrastructure centered on trustworthy macroeconomic data.

Growth remains evidence-paced. New capabilities are added when they solve a demonstrated problem and can be integrated without fragmenting canonical ownership, duplicating the macro-data foundation, or creating maintenance obligations disproportionate to their value.

Macro Evidence's organizational identity rests on stewarding one coherent infrastructure system while allowing its products, interfaces, reference layers, and implementation choices to evolve as evidence changes.

---

## Changelog

### 1.3.1 (2026-10-06)

- Clarifies the Mission's second sentence so that clear canonical ownership applies to each of the listed shared foundations, products, reference layers, and interfaces rather than only to interfaces.
- Records that release 1.3.0 also changed the Vision's punctuation, replacing an em dash with a comma, without a changelog entry; the Vision's wording is otherwise unchanged.
- Preserves all previously released changelog entries exactly as historical record.
- PATCH — clarification and a changelog correction only; the Mission's meaning, the Vision, platform roles, and product relationships are unchanged.

### 1.3.0 (2026-09-24)

- Adds the organization-level MDD relationship while keeping MDO as the flagship and foundational macro-data platform.
- Reframes the mission around durable macroeconomic infrastructure rather than a collection of isolated processing components, while preserving clear canonical ownership.
- Clarifies that products, reference layers, and interfaces may evolve without creating competing sources of truth.
- Preserves all previously released changelog entries exactly as historical record.
- MINOR — adds the organization-level MDD relationship and reframes the mission statement's supporting language; MDO's role as flagship and foundational platform and the organization/platform architecture are unchanged.

### 1.2.0 (2026-08-20)

- Refined Mission and Vision (§1) to establish open macroeconomic data infrastructure, evidence-grounded trust, and long-term stewardship as the organization-level direction.
- Removed personal-portfolio and career-audience framing from the charter and replaced it with organization/platform language appropriate to the current public entity.
- Reframed MDO as Macro Evidence's flagship and foundational platform, with core objectives centered on one coherent macroeconomic data foundation rather than skill demonstration or portfolio value.
- Removed repository-specific Technical Foundation details from the organization charter; current implementation details belong to the MDO repository and its technical documentation.
- Replaced the fixed five-stage Development Roadmap (§2) with evidence-paced directional guidance. Current MDO capability remains owned by the authoritative repository/runtime state rather than being cached here.
- Removed speculative roadmap capabilities from Engineering Scope and replaced them with durable platform-scope categories.
- Replaced the milestone-gated Future Products entry (§3) with the one-foundation growth rule: future products extend, expose, or operate on MDO's shared infrastructure rather than creating parallel macroeconomic-data foundations.
- Restructured Project Characteristics into Current Status (§4), retaining only current organization-level facts that belong in this charter.
- Updated Long-Term Vision (§5) to align organization, foundational platform, and future-product growth around one coherent infrastructure.
- Removed the header consolidation note and brand tagline; their content is either historical changelog information or owned outside this governance document.
- MINOR: the public roadmap and future-product governance rules changed in substance while the organization-wide execution model in `GOVERNANCE.md` §3 remains unchanged.

### 1.1.0 (2026-07-24)

- Aligned cross-references with the dedicated Governance repository.
- Expanded the MDO platform description and clarified its role as Macro Evidence's flagship platform.
- Updated engineering standards to reference `GOVERNANCE.md` and `DOCUMENTATION_STANDARDS.md`.
- Refined roadmap wording and long-term platform governance for consistency with the Governance Charter.
- Improved organizational wording and document consistency without changing project direction.

### 1.0.0 (2026-07-23)

- Initial finalized version.
- Consolidated the MDO summary and the Macro Evidence/MDO synthesis into one canonical charter.
- Removed duplicated Documentation Philosophy section (now maintained in `DOCUMENTATION_STANDARDS.md`).
