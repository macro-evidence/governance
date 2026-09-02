# 0006. Preserve licensing flexibility through contributor agreements

**Status:** Accepted
**Date:** 2026-09-02

## Context

Current Git-history review of the active governance, `.github`, and MDO repositories has not identified external project-author identities or co-authored contributions. Earlier changes from CC BY 4.0 to CC BY-SA 4.0 in the governance and `.github` repositories were therefore possible without seeking consent from an external project contributor, while separately licensed third-party material continued to be handled under its own terms. Git authorship does not by itself classify separately licensed or incorporated third-party material, which remains subject to its own provenance and license terms.

That experience exposed a long-term governance risk. If Macro Evidence begins merging external copyrightable contributions only under each repository's ordinary outbound license, future relicensing may depend on obtaining permission from every relevant copyright holder. One unavailable or unwilling contributor could therefore constrain a later licensing decision even where the proposed change is otherwise compatible with the organization's public-good mission.

The issue is most visible in Macro Data Observatory (MDO), whose public code is currently licensed under AGPL-3.0-only. Macro Evidence intends to preserve the public open-source core while retaining the option, if future evidence supports it, to make software it has sufficient rights to license available under additional terms. Granting an additional license would not by itself revoke rights validly granted under the public license and would not turn ordinary contributor participation into a paid relationship.

A Developer Certificate of Origin can certify that a contributor has the right to submit work under the project's stated license, but it does not by itself provide the broader sublicensing or relicensing rights required for this objective. Copyright assignment would centralize ownership but is stronger than necessary for the current requirement and would impose greater contributor friction.

## Decisions

Before merging an external copyrightable contribution into a Macro Evidence repository, require coverage by an approved contributor agreement. A later legally reviewed implementation may define a narrow exception where a proposed change is not copyrightable or otherwise does not require contributor-rights coverage; no such exception is presumed by this decision.

The contributor-agreement architecture will use the following principles:

- contributors retain ownership of their original contributions rather than assigning copyright by default;
- Macro Evidence receives a broad, non-exclusive grant sufficient, subject to the final legally reviewed agreement, to use, modify, distribute, sublicense, and relicense accepted contributions;
- the agreement must disclose clearly that Macro Evidence may make the covered contribution available under additional open, commercial, or proprietary license terms where it has the legal right and organizational approval to do so;
- any version of an accepted contribution released as part of a public Macro Evidence project remains subject to the public open-source or open-content license terms applicable to that release; granting an additional license does not revoke those previously granted public rights;
- an individual agreement will cover contributors who personally control the relevant rights, with an entity/corporate form available when an employer or other entity owns the work;
- one appropriately scoped agreement should cover a contributor's future eligible contributions rather than requiring a new agreement for each pull request;
- signing the agreement does not guarantee acceptance of any contribution and does not confer governance, roadmap, sponsorship, employment, payment, partnership, or support rights;
- a DCO may be considered later as an additional provenance mechanism, but DCO-only is not treated as a substitute for the relicensing rights required here;
- copyright assignment is not required by default;
- signed agreements and contributor personal information are private administrative records and are not stored in the public governance repository; and
- the agreement must identify the legally capable counterparty at the time it is executed and address lawful successor or assignment continuity if that counterparty changes in the future.

The exact individual/entity contributor-agreement text, copyright and other relevant rights grant, patent language, representations, governing law, counterparty identity, successor or assignment language, and execution mechanism are legal-instrument questions and require qualified legal review before any contributor is asked to sign.

Macro Evidence may review or adopt an additional licensing program in the future only through a separate evidence-based decision. Where practical, significant active contributors should be consulted in good faith before a material additional-licensing program is launched. Such consultation informs stewardship but does not itself create a contractual veto over rights already granted.

Until an approved contributor-agreement mechanism is available, external copyrightable pull requests may be opened and reviewed, but they must not be merged.

## Consequences

- Macro Evidence preserves future licensing optionality before contributor copyright becomes fragmented across many rights holders.
- Contributors keep ownership while granting the organization the rights required for long-term stewardship and possible additional licensing.
- Public license rights already granted for released versions remain unaffected by later additional licensing; the agreement does not require a contribution to remain included in every future project version.
- The organization accepts some contributor onboarding friction in exchange for avoiding substantially larger future relicensing debt.
- Legal review becomes a prerequisite for activating the contributor-agreement workflow, not for recording this governance architecture.
- A private agreement register and secure storage process will be required when the first agreement is executed.
- A dedicated legal/licensing contact may be activated when contributor-agreement or licensing administration becomes operational; no new public contact route is required before then.
- Repository-specific outbound licenses remain separate decisions. This ADR does not change MDO's AGPL-3.0-only public license or any other repository license.
- Any future additional commercial or proprietary license remains optional and evidence-dependent; this ADR preserves the ability to consider it rather than committing Macro Evidence to offer it.
