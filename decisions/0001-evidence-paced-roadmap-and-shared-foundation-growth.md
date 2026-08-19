# 0001. Evidence-paced roadmap and shared-foundation product growth

**Status:** Accepted
**Date:** 2026-08-20

## Context

`ORGANIZATION_CHARTER.md` 1.1.0 describes MDO through a fixed five-stage roadmap and gates future products on MDO clearing a specific milestone.

Subsequent MDO development has shown that meaningful architectural requirements emerge from live implementation rather than from a fixed feature sequence. Multiple independent sources now operate through a shared series-first architecture, and the next useful work is determined by what the existing system still needs rather than by advancing a predetermined stage label.

The existing charter also lists future products as separate roadmap items. That framing leaves open the possibility of parallel products recreating the same macroeconomic-data foundation, which conflicts with Macro Evidence's established direction toward one coherent, extensible infrastructure.

Both questions affect organization-level platform scope and future repository/product decisions, so they are recorded here as a cross-cutting organizational decision rather than remaining implicit in a charter rewrite.

## Decision

Replace the fixed public five-stage MDO roadmap with an **evidence-paced trajectory**. The organization charter states durable direction rather than precommitting to a fixed sequence of features. Current MDO capability remains owned by the MDO repository and verified runtime evidence; non-trivial architectural and scope changes continue through the applicable ADR process.

Future Macro Evidence products **extend, expose, or operate on MDO's shared macroeconomic-data foundation rather than recreating the same underlying infrastructure in parallel**. Product form may evolve as evidence warrants, and any later decision to change this one-foundation relationship requires its own explicit organizational decision.

## Consequences

- `ORGANIZATION_CHARTER.md` 1.2.0 replaces the fixed five-stage roadmap with evidence-paced directional guidance.
- Future products are no longer gated by an arbitrary milestone label; each material addition is evaluated against the decision criteria in `GOVERNANCE.md`.
- The charter does not cache a detailed capability roadmap. Current implementation and maturity claims remain in the MDO repository and runtime evidence.
- Macro Evidence can add new interfaces and products without duplicating the canonical macroeconomic-data foundation.
- This does not change `GOVERNANCE.md` §3's organization-wide execution model: tasks still require objectives, review, approval, and real deliverables.
