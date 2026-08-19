# Macro Evidence — Organization & Platform Charter

> Version 1.2.0 · Active · Last updated 2026-08-20

---

## 1. Organization

### Mission

Macro Evidence builds open macroeconomic data infrastructure designed around provenance, validation, reproducibility, and transparency — engineered as one coherent, extensible system rather than a collection of disconnected pipelines.

### Vision

To become a lasting, trusted steward of open macroeconomic data infrastructure — built incrementally, on evidence, one disciplined decision at a time.

### Engineering Philosophy

- Engineering rigor over presentation
- Reproducibility over one-off solutions
- Transparency over opacity
- Maintainability over short-term convenience
- Modular architecture over monoliths
- Documentation-first development
- Incremental capability growth over speculative scope

---

## 2. Flagship Platform — Macro Data Observatory (MDO)

### Purpose

Macro Data Observatory (MDO) is the flagship and foundational platform of Macro Evidence.

It is a long-term data engineering platform that acquires, processes, organizes, and maintains macroeconomic data from authoritative public sources through disciplined engineering practice. MDO is infrastructure-led: catalogue, research, visualization, and programmatic-access experiences build on the same underlying data system rather than defining separate products or data foundations.

### Core Objectives

- Build and maintain one coherent macroeconomic data foundation across authoritative public sources
- Normalize heterogeneous source data into consistent, researchable economic series
- Apply validation, reproducibility, provenance, and maintainability as explicit infrastructure requirements
- Provide the shared foundation for Macro Evidence's catalogue, research, programmatic-access, and future product layers
- Keep architecture and implementation decisions documented and auditable as the platform evolves

### Engineering Scope

- Data acquisition from authoritative public sources
- Validation, cleaning, and transformation
- Canonical series storage and metadata
- Reproducible ETL workflows
- Provenance and data-quality infrastructure
- Architectural Decision Records (ADRs) and technical documentation

### Engineering Standards

- Organization governance (see [`GOVERNANCE.md`](GOVERNANCE.md))
- Standardized naming conventions (see [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md) §5)
- Modular repository organization
- Reproducible development environments using free-tier infrastructure
- Conventional Commits (see [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md) §6)
- Architectural review cadence defined in [`GOVERNANCE.md`](GOVERNANCE.md)
- Continuous complexity management

### Development Roadmap

MDO has demonstrated through live implementation and verification that one canonical system can ingest, validate, and structure macroeconomic data from multiple independent sources.

Development continues by strengthening that shared foundation and extending its discoverability, research usability, and accessibility as evidence justifies each addition. This is directional guidance, not a fixed sequence of features or a substitute for the current MDO repository and runtime evidence.

Pacing is decided against evidence as work progresses, not fixed in advance. Non-trivial architectural and scope decisions are recorded through the applicable Architecture Decision Record process (see [`GOVERNANCE.md`](GOVERNANCE.md)) rather than committed to here ahead of implementation evidence.

---

## 3. Product Ecosystem

| Layer | Entity | Status |
|---|---|---|
| Organization | Macro Evidence | Governance, identity, stewardship, and organizational infrastructure |
| Flagship and foundational platform | Macro Data Observatory | Under active development |

Future products extend, expose, or operate on Macro Data Observatory's shared infrastructure rather than recreating the same underlying macroeconomic-data foundation in parallel. Product form may change as Macro Evidence grows, but the one-foundation relationship remains the default unless a later organizational decision deliberately changes it.

Each material addition is evaluated against the decision criteria in [`GOVERNANCE.md`](GOVERNANCE.md) before implementation begins.

---

## 4. Current Status

| Attribute | Description |
|---|---|
| Domain | Macroeconomic data systems |
| Maintainers | One |
| Time horizon | Multi-year |

---

## 5. Long-Term Vision

Macro Evidence is intended to mature into an ecosystem of professionally engineered products centered on open, trustworthy macroeconomic data infrastructure, with Macro Data Observatory serving as the shared foundational platform.

As MDO's infrastructure matures, additional products build on that foundation rather than forming parallel or duplicate data infrastructures. Macro Evidence's identity rests on stewarding one coherent system while allowing its interfaces, products, and implementation choices to evolve with evidence.

---

## Changelog

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
