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
