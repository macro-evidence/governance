# Architecture Decision Records

Non-trivial technical decisions for Macro Evidence platforms are recorded here, per [`GOVERNANCE.md`](../GOVERNANCE.md) §5.

## Format

One file per decision: `NNNN-short-title.md`, numbered sequentially, using:

```
# NNNN. Short title

**Status:** Proposed / Accepted / Superseded
**Date:** YYYY-MM-DD

## Context
What problem or question this addresses.

## Decision
What was decided.

## Alternatives Considered
What other options were evaluated and why they were not chosen.

## Rationale
Why this decision was selected over the alternatives.

## Consequences
Expected benefits, trade-offs, risks, and follow-up implications.
```

## Decisions

- [0001. Single flat table for Stage 1 ETL, not a dimensional model](0001-single-table-schema-for-stage-1-etl.md)
- [0002. Hard-fail structural checks, soft-warn data anomalies](0002-data-quality-validation.md)
- [0003. Generalize the pipeline runner for pluggable sources](0003-generalized-pipeline-runner.md)
- [0004. IMF source starts on DataMapper, not SDMX](0004-imf-datamapper-discovery-phase.md)
- [0005. Widen validation's year ceiling for forecast-carrying sources](0005-widen-validation-year-ceiling.md)
