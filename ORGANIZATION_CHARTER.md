# Macro Evidence — Organization & Platform Charter

> Version 1.1.0 · Active · Last updated 2026-07-24
> Supersedes the originally drafted MDO summary and the Macro Evidence/MDO consolidated summary — both are consolidated here as the single canonical version.

> Evidence infrastructure for macroeconomic intelligence, built one disciplined decision at a time.

---

## 1. Organization

### Mission

Macro Evidence exists to build professional data infrastructure that improves access to high-quality macroeconomic evidence through transparent engineering, reproducible data systems, and disciplined technical practices—not opinion or commentary.

### Vision

To become a trusted builder of open macroeconomic data infrastructure through platforms and products that combine engineering quality, reproducibility, and long-term maintainability.

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

Macro Data Observatory (MDO) is the flagship platform of Macro Evidence.

It is a long-term data engineering platform that acquires, processes, organizes, and maintains macroeconomic data from authoritative public sources through professional engineering practice. MDO is an engineering platform first—not a dashboard, blog, or visualization product.

### Core Objectives

- Build practical, end-to-end data engineering capability
- Develop modular ETL pipelines using industry-standard technologies
- Create a structured repository of macroeconomic datasets from trusted public sources
- Demonstrate software architecture, infrastructure design, and engineering documentation
- Establish the engineering foundation for future Macro Evidence products
- Produce a credible technical portfolio

### Engineering Scope

- Data acquisition (World Bank, IMF, FRED)
- Validation, cleaning, transformation
- Structured storage (PostgreSQL)
- Modular, reproducible ETL workflows
- Data warehouse foundations
- Analytics-ready datasets
- Workflow automation and orchestration
- Architectural Decision Records (ADRs) and implementation logs

### Engineering Standards

- Organization governance (see [`GOVERNANCE.md`](GOVERNANCE.md))
- Standardized naming conventions (see [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md) §5)
- Modular repository organization
- Reproducible development environments using free-tier infrastructure
- Conventional Commits (see [`DOCUMENTATION_STANDARDS.md`](DOCUMENTATION_STANDARDS.md) §6)
- Architectural review cadence defined in [`GOVERNANCE.md`](GOVERNANCE.md)
- Continuous complexity management

### Technical Foundation

| Layer | Choice |
|---|---|
| Language | Python |
| Storage | PostgreSQL |
| Processing | Pandas + supporting libraries |
| Data sources | Public REST APIs (World Bank, IMF, FRED) |
| Version control | Git / GitHub |
| Repository layout | Separated source, ETL, datasets, docs, tests, config, notebooks |

### Development Roadmap

| Stage | Focus |
|---|---|
| 1 | Local ETL Pipelines — reliable ingestion and transformation |
| 2 | Structured Data Warehouse — scalable relational architecture |
| 3 | Analytics Layer — SQL-ready, dashboard-ready datasets |
| 4 | Pipeline Automation — orchestration and scheduling |
| 5 | Forecasting & Advanced Models — predictive analytics on curated historical data |

Each stage requires the previous stage to be completed, documented, and accepted before the next begins.

---

## 3. Product Ecosystem

| Layer | Entity | Status |
|---|---|---|
| Organization | Macro Evidence | Governance, brand, accounts, sponsors |
| Flagship platform | Macro Data Observatory | Under active development |
| Future products | Analytical applications, research tools, forecasting services, APIs, educational products | Roadmap only — no repository until MDO clears its first milestone |

---

## 4. Project Characteristics

| Attribute | Description |
|---|---|
| Project type | Personal data engineering platform |
| Domain | Macroeconomic data systems |
| Developer | Single developer |
| Time horizon | Multi-year |
| Technology stack | Python, PostgreSQL, Pandas, Public REST APIs, Git |
| Engineering approach | Governance-driven, documentation-first, infrastructure-focused |
| Primary focus | Scalable, reproducible data engineering systems |
| Target audience | Technical recruiters, future collaborators, graduate admissions committees, sponsors |

---

## 5. Long-Term Vision

Macro Evidence is intended to mature into an ecosystem of professionally engineered products centered on trustworthy macroeconomic data infrastructure, with Macro Data Observatory serving as the foundational platform.

As MDO matures through structured warehousing, automation, analytics, and forecasting capabilities, additional products are built on top of that foundation—not alongside it. Every future platform or repository is evaluated against the decision criteria defined in [`GOVERNANCE.md`](GOVERNANCE.md) before it is created.

---

## Changelog

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