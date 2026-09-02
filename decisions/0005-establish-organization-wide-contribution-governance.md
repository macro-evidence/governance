# 0005. Establish organization-wide contribution governance

**Status:** Accepted
**Date:** 2026-09-02

## Context

Macro Evidence intends to remain open to community participation while preserving a high and evidence-based acceptance standard as the organization grows.

The existing organization-wide `CONTRIBUTING.md` in `macro-evidence/.github` defines useful GitHub workflow expectations: where to open issues, when to discuss large changes before implementation, what a pull request should contain, and which public organizational standards apply. It does not define the organization-wide policy boundary for contribution acceptance, contributor entitlements, monetary support, or the relationship between organization policy and repository-specific contribution mechanics.

That gap matters across repositories rather than within any one codebase. Macro Evidence needs a stable public rule that participation is open, substantive acceptance remains merit- and evidence-based, and submitting work does not by itself create governance authority, roadmap priority, compensation, partnership, employment, or a right to merge.

Monetary support is handled separately through Macro Evidence's sponsorship architecture. Treating sponsorship as a contribution requirement would conflict with the organization's open participation and public-good posture.

## Decision

Establish an organization-wide `CONTRIBUTION_POLICY.md` in the governance repository as the canonical public policy for contribution participation and acceptance.

The policy will establish that:

- participation is open to the community;
- substantive contributions are evaluated on their merits and current organizational or repository needs;
- Macro Evidence retains stewardship discretion to accept, decline, request changes to, or defer a contribution;
- submission does not guarantee merge, maintenance, support, compensation, employment, partnership, sponsorship recognition, governance authority, roadmap control, or priority;
- contribution is a non-monetary participation path, while monetary support is handled through the applicable sponsorship channel;
- contributors must have the right to submit the work they offer;
- applicable repository licenses and any approved contributor-rights requirements continue to govern accepted contributions; and
- repository-specific technical contribution mechanics remain in the applicable repository or in the organization-wide `.github` community-health files.

The governance repository owns the cross-repository policy. The `.github` repository continues to own the organization-wide GitHub community-health files and links to the canonical policy. `CONTRIBUTION_POLICY.md` and `TRADEMARKS.md` are scope-specific organization policies: each is canonical within its own subject, and neither overrides the other outside that subject. Repository-specific `CONTRIBUTING.md` files may extend contribution mechanics when a repository has a real need, but they must not contradict organization-wide contribution governance.

## Consequences

- Macro Evidence gains a durable public participation model without coupling organizational policy to GitHub-specific mechanics.
- Community participation remains open while merge and stewardship decisions remain selective and evidence-based.
- Contribution and sponsorship remain distinct; financial support does not become a prerequisite for technical or documentation participation.
- Contributors receive clearer expectations about what submission does and does not imply.
- The website can describe contribution using a canonical public policy rather than inventing its own acceptance rules.
- `macro-evidence/.github/CONTRIBUTING.md` will be updated to reference the organization-wide Contribution Policy.
- Contributor intellectual-property and relicensing requirements remain governed by separate decision 0006 rather than being implied by this acceptance-policy decision.
