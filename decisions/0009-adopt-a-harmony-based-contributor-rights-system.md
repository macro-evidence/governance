# 0009. Adopt a Harmony-based contributor-rights system

**Status:** Accepted
**Date:** 2026-09-24

## Context

Decision 0006 establishes the organization-level requirement to obtain contributor-rights coverage before merging an external copyrightable contribution when the ordinary repository license does not provide the rights needed for long-term stewardship and possible additional licensing. The next durable question is which contributor-agreement architecture should provide that coverage.

The legal architecture needs to preserve contributor ownership, support both natural-person and entity-controlled rights, provide the rights required by decision 0006, and remain explicit about the distinction between the Macro Evidence project identity and the legal contracting party identified in the agreement forms. It also needs a maintainable provenance boundary so future edits can be traced to a standard source rather than becoming an unexplained bespoke contract.

Harmony Contributor License Agreement Version 1.0 provides the contractual base. Its Individual and Entity forms, contributor-ownership model, and Outbound Option Five provide the required general structure. Apache Software Foundation contributor agreements are used only as a design reference for safeguards such as originality, third-party-material disclosure, employer/entity authority, continuing correction, and private-record handling. Apache-specific institutional language is not adopted.

## Decision

Adopt a Harmony-based contributor-rights architecture for version 1.0.0 with bounded Macro Evidence-specific additions documented in [`legal/cla/PROVENANCE_AND_CUSTOMIZATION.md`](../legal/cla/PROVENANCE_AND_CUSTOMIZATION.md).

The architecture is:

- maintain Individual and Entity Contributor License Agreement forms;
- require an ICLA for each natural person whose covered external copyrightable contribution may be merged;
- require an ECLA or another documented sufficient rights path when an employer, company, institution, or other legal entity owns or may control relevant rights;
- use a contributor license rather than copyright assignment as the default rights model;
- use Harmony Outbound Option Five;
- omit the optional additional Harmony Media-licence list for version 1.0.0;
- retain contributor ownership while obtaining the approved copyright, patent, database-right, sublicensing, and relicensing grants;
- include bounded safeguards for originality, third-party material, employer/entity authority, continuing correction, privacy, no agency, and contributor-side responsibility;
- distinguish the Macro Evidence project identity from the present contracting party identified in the agreement forms and preserve a documented successor path without representing an unestablished legal entity as already existing;
- use the laws of India as the governing law for agreement version 1.0.0;
- require an approved signed execution record rather than treating a GitHub checkbox, pull-request comment, typed name, DCO sign-off, or ordinary email acknowledgement as the agreement itself; and
- keep executed agreements, signatures, private addresses, private contacts, identity and authority evidence, account-binding evidence, entity schedules, execution evidence, and the contributor-rights register private.

The public agreement forms and the public contributor-agreement process define the operative legal and administrative details. Future changes to the substantive rights grant, outbound-license option, responsibility architecture, governing law, assignment or successor mechanism, or execution standard require renewed governance review and, where existing signatories' terms would change, a new agreement version.

Operational GitHub merge enforcement is a separate governance boundary. Its security invariants, activation requirements, and fail-closed behavior are recorded in decision 0012 and [`legal/cla/GITHUB_ENFORCEMENT.md`](../legal/cla/GITHUB_ENFORCEMENT.md). This ADR does not declare that the automated merge gate is active.

## Consequences

- Macro Evidence has a defined standard agreement family instead of an open-ended bespoke drafting model.
- Contributors retain ownership while the approved agreement provides the rights needed for long-term stewardship and possible additional licensing.
- Natural-person and entity-controlled rights are handled through distinct but compatible agreement paths.
- The public forms retain their Harmony provenance and their separate CC BY 3.0 licensing boundary.
- Private execution and contributor records remain outside the public repository.
- Operational merge enforcement can evolve without changing the substantive legal terms of the agreement merely because its implementation changes.
- The contributor-rights mechanism remains unavailable for external copyrightable merge until the separate activation requirements are satisfied.
