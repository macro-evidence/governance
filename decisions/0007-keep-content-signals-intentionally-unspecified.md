# 0007. Keep Content Signals intentionally unspecified

**Status:** Accepted
**Date:** 2026-09-24

## Context

Macro Evidence publishes public material under several materially different rights instruments. Software repositories may use software licenses; governance and other documentation may use open-content licenses; official identity assets and trademarks have separate rules; and third-party material remains subject to its own terms.

Cloudflare's [Content Signals](https://developers.cloudflare.com/bots/additional-configurations/managed-robots-txt/#content-signals-policy) mechanism expresses machine-readable positions for uses such as `search`, `ai-input`, and `ai-train`. As of 2026-09-24, Cloudflare documents an omitted directive as neither granting nor restricting permission through Content Signals for that use. An organization-wide signal would therefore compress several distinct rights classes into one machine-readable statement unless Macro Evidence first has a defensible mapping from each class of material to the available directives.

Cloudflare also documents managed features that can emit signals on an origin's behalf. [Markdown for Agents](https://developers.cloudflare.com/fundamentals/reference/markdown-for-agents/) currently preserves an origin `Content-Signal` header when present and otherwise supplies its own defaults. That behavior makes infrastructure configuration relevant to whether a deliberate non-assertion remains a non-assertion in practice.

Four broad approaches are available:

- publish permissive organization-wide signals, which are easy for automated consumers to interpret but may communicate permission more broadly than the underlying rights instruments support;
- publish restrictive organization-wide signals, which make a strong reservation clear but may communicate a more restrictive position than Macro Evidence's open licenses and public-good posture warrant;
- publish content-specific signals, which could be more precise but require a stable classification/mapping architecture and additional operational complexity; or
- deliberately make no Content Signals assertion for now, leaving the applicable licenses, policies, and third-party terms authoritative while accepting less machine-readable guidance.

Non-assertion is only meaningful if infrastructure does not silently replace it with vendor defaults. Platform features that can inject Content Signals therefore require review before they are enabled.

## Decision

Do not publish one organization-wide affirmative or negative Content Signals rights assertion at this time.

Until Macro Evidence has a stable, evidence-backed mapping from its distinct public-content rights classes to the available Content Signals directives, leave `search`, `ai-input`, `ai-train`, and the experimental `use` extension unspecified through this mechanism.

This is a deliberate non-assertion within the Content Signals mechanism. It does not itself grant permission, prohibit use, alter repository or content licenses, change trademark policy, classify a crawler as trustworthy or malicious, or change ordinary crawl access.

Do not enable a managed platform feature that would substitute vendor Content Signals defaults for this deliberate non-assertion without first reviewing those defaults against the applicable rights classes and this decision.

Revisit this decision when evidence supports a defensible explicit mapping, including when the mechanism materially stabilizes or changes, Macro Evidence's rights classes change, content-specific signaling becomes operationally proportionate, or reliable evidence shows that an explicit signal would materially improve rights expression without contradicting governing terms.

## Consequences

- Existing licenses, policies, and third-party terms remain authoritative within their own scopes.
- Macro Evidence avoids making a blanket machine-readable statement that may be broader or narrower than the rights actually attached to different public materials.
- Automated consumers receive less organization-wide machine-readable guidance until a more precise mapping is justified.
- Platform features that inject default Content Signals cannot be treated as neutral infrastructure changes; their defaults must be reviewed before activation.
- A future explicit organization-wide or content-specific signaling policy requires a new evidence-based decision rather than a website-only configuration change.
