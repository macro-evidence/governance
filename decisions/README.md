# Architecture Decision Records

This folder contains decisions that genuinely apply across multiple Macro Evidence repositories or to the organization's structure itself, per [`GOVERNANCE.md`](../GOVERNANCE.md) §5.

Repository-specific decisions are recorded in that repository's own `decisions/` folder — e.g. [`macro-data-observatory/decisions/`](https://github.com/macro-evidence/macro-data-observatory/tree/main/decisions). The 7 decisions formerly recorded here were moved to MDO on 2026-08-09 after review showed that all were MDO-specific. See [`macro-data-observatory` decision 0008](https://github.com/macro-evidence/macro-data-observatory/blob/main/decisions/0008-adr-placement-per-repository.md) for the migration decision and rationale.

## Numbering and references

Decision numbering is repository-local. Following that migration, the governance sequence starts at `0001`; each repository maintains its own independent sequence.

Within the repository that owns a decision, refer to it as `decision NNNN`. When referring to a decision from another repository, qualify it with the repository name — for example, `governance decision 0001` or `macro-data-observatory decision 0008`.

## Format

One ADR per file: `NNNN-short-title.md`, numbered sequentially, using:

```
# NNNN. Short title

**Status:** Proposed / Accepted / Superseded
**Date:** YYYY-MM-DD

## Context
What problem or question this addresses.

## Decision
What was decided.

## Consequences
Expected benefits, trade-offs, risks, and follow-up implications.
```

**Decision count per ADR:** Most ADRs record one coherent decision boundary under the singular `## Decision` heading. An ADR may use a plural `## Decisions` heading when multiple decisions are inseparable — for example, when an explicit exclusion or deferral is necessary to define what the primary decision does and does not include. Decisions that can be accepted, revisited, or superseded independently receive separate ADR numbers.

## Decisions

- [0001. Evidence-paced roadmap and shared-foundation product growth](0001-evidence-paced-roadmap-and-shared-foundation-growth.md)
- [0002. License governance content under CC BY-SA 4.0](0002-license-governance-content-under-cc-by-sa-4.0.md)
- [0003. License .github community infrastructure under CC BY-SA 4.0](0003-license-github-community-infrastructure-under-cc-by-sa-4.0.md)
- [0004. Adopt tailored Contributor Covenant 3.0](0004-adopt-tailored-contributor-covenant-3.0.md)
