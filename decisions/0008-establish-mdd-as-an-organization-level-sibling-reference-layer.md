# 0008. Establish MDD as an organization-level sibling reference layer

**Status:** Accepted
**Date:** 2026-09-24

## Context

Governance decision 0001 established that Macro Evidence should extend one coherent macro-data foundation rather than create parallel foundations for related products. Macro Data Dictionary (MDD) has been initialized as a Macro Evidence repository and needs an explicit organization-level relationship to Macro Data Observatory (MDO) before substantive implementation begins.

Treating MDD as a child of MDO would make an organization-level reference layer appear to be an MDO-only subproject. Treating it as an independent data foundation would create the opposite problem: duplicated technical/data truth and a competing source of record.

The durable boundary is therefore between organizational relationship and source-of-truth ownership. MDD can be a sibling product layer while still depending on the canonical sources of whichever Macro Evidence product a referenced fact belongs to.

## Decision

Macro Data Dictionary (MDD) is an organization-owned sibling of Macro Data Observatory (MDO) under Macro Evidence. It is not a child or subproject of MDO, and it is not an independent macro-data foundation.

MDO remains Macro Evidence's flagship and foundational macro-data platform. Canonical technical and data facts about MDO's data processing, schemas, series, metadata, units, allowed values, and implementation remain owned by MDO's repository, runtime, and other designated MDO canonical sources.

MDD is a bounded reference and explanatory layer. It may define and explain macroeconomic terminology, metadata concepts, and organization-wide reference material, and it may serve MDO and future Macro Evidence products where their subject matter overlaps. When MDD presents product-specific technical or data facts, it derives or references those facts from that product's canonical sources rather than maintaining a conflicting copy as an independent source of truth.

This decision preserves governance decision 0001's one-foundation rule. It does not decide MDD's implementation architecture, schema, deployment URL, visual identity, substantial reference-content license, or substantive feature scope.

## Consequences

- `ORGANIZATION_CHARTER.md` records MDO and MDD as organization-level siblings with distinct roles while preserving MDO's flagship/foundational status.
- MDD may eventually explain concepts across more than one Macro Evidence product without being structurally subordinate to MDO.
- MDO remains authoritative for its own implementation and data facts; MDD does not create a second technical source of truth.
- MDD may remain intentionally minimal until a separate implementation-start decision is approved.
- Before substantial reference content is added, MDD's reference-content licensing boundary must be decided explicitly rather than inherited accidentally from the repository's software-oriented root license.
- Product URLs, identity design, schemas, deployment architecture, and substantive feature scope remain outside this ADR.
