# 0004. Adopt tailored Contributor Covenant 3.0

**Status:** Accepted
**Date:** 2026-08-21

## Context

Macro Evidence uses an organization-wide default Code of Conduct from `macro-evidence/.github` for repositories that do not publish their own conduct policy.

The current default is an adaptation of Contributor Covenant 2.1. It established an appropriate baseline for community conduct, but parts of its enforcement language no longer describe Macro Evidence's operating model accurately. In particular, it repeatedly assigns enforcement to plural community leaders, promises prompt investigation, and describes an enforcement sequence more rigidly than Macro Evidence can responsibly guarantee at its current single-maintainer capacity.

Macro Evidence reviewed whether to retain and further adapt Contributor Covenant 2.1 or move to Contributor Covenant 3.0.

Contributor Covenant 3.0 more clearly distinguishes ordinary community conflict from Code of Conduct violations, treats its enforcement ladder as a guideline rather than a mandatory sequence, and expressly anticipates community-specific reporting and enforcement procedures. Its published guidance also supports enforcement by a single responsible individual in smaller communities.

Contributor Covenant 3.0 is licensed under Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0). Governance decision 0003 separately establishes CC BY-SA 4.0 as the licensing direction for the `.github` community infrastructure. The conduct-policy decision and repository-license decision remain independently revisitable.

## Decision

Adopt an appropriately tailored Contributor Covenant 3.0 as Macro Evidence's organization-wide default Code of Conduct.

The adaptation will preserve the substantive community standards, scope, and attribution of Contributor Covenant 3.0 while tailoring reporting and enforcement language to Macro Evidence's actual operating capacity.

In particular, the implementation will:

- provide a private, documented route for reporting possible Code of Conduct violations;
- describe enforcement in terms consistent with Macro Evidence's current single-maintainer capacity rather than implying that a moderation committee or multiple community leaders exist;
- avoid promising a response-time or investigation SLA that Macro Evidence cannot reliably guarantee;
- treat the Contributor Covenant enforcement ladder as guidance that may be applied proportionately rather than as a mandatory sequence;
- preserve appropriate confidentiality and discretion in investigation and enforcement;
- retain Contributor Covenant 3.0's scope boundary for community spaces and official representation rather than extending ordinary Code of Conduct enforcement to unrelated private or external conduct; and
- retain the required Contributor Covenant attribution and applicable CC BY-SA 4.0 licensing terms.

The organization-wide default applies where GitHub's community-health-file precedence makes it applicable. A repository may publish its own Code of Conduct when repository-specific circumstances justify one.

Adoption is pinned to Contributor Covenant version 3.0. A later Contributor Covenant release is not adopted automatically and requires separate review before replacing this policy.

## Consequences

- The existing Contributor Covenant 2.1-based organization-wide default will be replaced by a Contributor Covenant 3.0-based policy.
- Macro Evidence retains a recognized external conduct framework while adapting operational language to what the organization can actually support.
- The policy will no longer imply the existence of a moderation committee or multiple enforcement leaders at the current stage.
- The policy will not promise a guaranteed acknowledgement, investigation, or resolution timeframe.
- Enforcement remains capable of escalating directly when severity warrants it; the published ladder is guidance rather than a required progression through every step.
- Conduct outside community spaces remains outside the policy's ordinary enforcement scope unless an individual is officially representing Macro Evidence, consistent with the adopted framework's scope.
- Repository-specific conduct policies may override the organization-wide default where GitHub's precedence rules apply.
- Contributor Covenant attribution and CC BY-SA 4.0 obligations remain part of the adapted policy.
- Governance decision 0003 governs `.github` repository licensing separately; changing or superseding either decision does not automatically supersede the other.
