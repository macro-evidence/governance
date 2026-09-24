# 0010. Preserve the governance CC BY-SA default with explicit legal-form exceptions

**Status:** Accepted
**Date:** 2026-09-24

## Context

Governance decision 0002 established CC BY-SA 4.0 as the default licence for Macro Evidence's public governance corpus. At the time, the repository was composed of Macro Evidence-authored governance/documentation material and did not contain a maintained legal form derived from a differently licensed third-party template.

The contributor-rights system introduces ICLA/ECLA reference forms adapted from Harmony Contributor License Agreement Version 1.0. Harmony's templates carry an explicit Creative Commons Attribution 3.0 Unported provenance/licensing boundary and permit modification and redistribution subject to the applicable attribution terms. Silently presenting the adapted forms as ordinary CC BY-SA governance content would blur source provenance and the file-specific rights basis.

The surrounding contribution policy, ADRs, execution process, privacy notice, third-party-material process, and Macro Evidence-authored explanatory material do not require the same exception.

## Decision

Replace the repository-wide-without-exception licensing premise of decision 0002 with an explicit licensing map:

- CC BY-SA 4.0 remains the **default** licence for Macro Evidence-authored governance and policy content;
- Harmony-derived Macro Evidence ICLA/ECLA forms and their same-terms reference-format derivatives are expressly identified under CC BY 3.0 with upstream attribution/provenance;
- `LICENSING.md` is the canonical map for repository-level exceptions to the root default licence;
- third-party material retains its own applicable terms and is not silently relicensed by repository placement; and
- repository licensing does not grant trademark, official-status, or identity rights addressed separately by the Trademarks Policy.

This decision supersedes governance decision 0002 as the canonical governance-repository licensing architecture while preserving CC BY-SA 4.0 as the default.

## Consequences

- The governance repository becomes explicitly mixed-licensed where source provenance requires it instead of obscuring a real third-party-derived legal-form boundary.
- Existing CC BY-SA 4.0 governance content remains under that licence.
- Harmony-derived forms preserve clear attribution and do not imply Harmony endorsement of Macro Evidence modifications.
- Downstream users must consult `LICENSING.md` when reusing files covered by an explicit exception.
- Future exceptions require explicit provenance and a documented licence map rather than ad hoc notices.
