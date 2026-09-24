# Macro Evidence CLA - Provenance and Customization Map

> Version 1.0.0 · Active · Last updated 2026-09-24

---

This document records the source, selection, and purpose of the Macro Evidence ICLA/ECLA customization surface. It is intended to make the legal instrument auditable and to prevent future edits from drifting into unexplained bespoke contract language.

---

## Primary contractual source

The contractual spine is the official **Harmony Individual Contributor License Agreement v1.0** and **Harmony Entity Contributor License Agreement v1.0**, dated July 4, 2011.

The verified upstream files used for version 1.0.0 are:

- `ha-cla-i-v1.odt` - SHA-256 `319226A66A26EE8E5A2D126BB5A738D51ADFB788291D628CBB2657DCEAEA5085`
- `ha-cla-e-v1.odt` - SHA-256 `DF669346DDB37C60623C93C455F701A29C9CFE32FA5B004A0F349CD2A69B736D`
- `ha-combined-v1.odt` - SHA-256 `B560D62BC13C3E6AB69F9715592482171CF8D350635558AAD41272F918CF52D0`

Harmony's template notice makes the template available under **Creative Commons Attribution 3.0 Unported**. Macro Evidence preserves that provenance boundary rather than replacing it with a repository-wide content license.

---

## Secondary design source

The Apache Software Foundation contributor-agreement model is used as a mature design reference for safeguards that Harmony leaves comparatively light, especially:

- originality and third-party-material disclosure;
- employer/entity-rights handling;
- continuing notification when representations change;
- private handling of residence/address information;
- individual agreements plus supplementary entity coverage where employer/entity rights are implicated; and
- operational treatment of signing and agreement records.

Macro Evidence does not import Apache-specific nonprofit/public-benefit promises, Foundation governance, Apache IDs, PMC mechanics, or other ASF institutional language.

---

## Deliberate Harmony selections

- contributor **license**, not copyright assignment;
- Individual and Entity variants;
- Outbound **Option Five**;
- no optional additional Harmony Media-license list;
- contributor ownership retained;
- reciprocal warranty disclaimer using the option contemplated by Harmony's combined template;
- reciprocal consequential-damages waiver using the option contemplated by Harmony's combined template, subject to explicit carve-outs;
- Harmony assignment/successor architecture retained but hardened so assignment does not silently release pre-assignment obligations and future Macro Evidence succession is explicit; and
- India selected as governing law for version 1.0.0 while the present rights recipient is the contracting party identified in the agreement forms.

---

## Macro Evidence-specific changes and rationale

### Contracting identity

The forms distinguish the public **Macro Evidence** project identity from the present legal rights recipient. `We/Us` is the present contracting party identified in the agreement forms for version 1.0.0, with successor continuity handled through Section 6.3. The forms do not describe Macro Evidence as an incorporated company, sole proprietorship, or other legal form not established by evidence.

### Covered-project scope

A `Covered Project` definition permits one agreement to cover multiple Macro Evidence repositories while preventing automatic scope expansion to a project that has not expressly adopted the agreement.

### Coverage and effective dates

Version 1.0.0 separates the private **Coverage Start Date** from the **Effective Date**. A Coverage Start Date before execution establishes only the earliest eligibility boundary for retroactive coverage; each pre-Effective-Date Submission must also be specifically identified in the private execution record or incorporated schedule by project and durable Submission identifier. Those identified earlier Contributions become licensed when the parties execute the Agreement; future Contributions become licensed when they come into existence and are Submitted on or after the Effective Date. This avoids treating a written licence as effective before execution or sweeping unidentified historical work into the agreement.

### India-specific copyright licence particulars

Because the Copyright Act applies section 19 formalities to licences through section 30A, version 1.0.0 expressly states:

- how each licensed work is identified through Covered Project submission records;
- the licensed rights;
- worldwide territory;
- duration for the full term of the rights;
- zero royalty and zero monetary consideration, with the parties' mutual covenants identified as consideration;
- that rights do not lapse merely because they are not exercised within one year; and
- when a licence for future work takes effect.

### Database rights

Version 1.0.0 adds an express licence for sui generis database rights or analogous rights that may exist in jurisdictions outside India. This is relevant to a data-infrastructure organization and avoids relying on copyright terminology alone for database contributions.

### Moral rights

Harmony's waiver/non-assertion concept is retained only to the maximum extent permitted by law. Version 1.0.0 expressly preserves rights that applicable law makes non-waivable and adds consent to authorized modifications and uses where effective.

### Contributor representations and independent controls

Section 3 strengthens provenance and authority protections using Apache's mature agreement model as a design source. The additions cover originality, employer/entity authorization, third-party restrictions, generated/model-assisted material, sensitive information, reasonable inquiry, account-control representations, continuing correction, and the rule that Macro Evidence review or merge does not validate or waive contributor representations.

The operational process does not treat a signer, GitHub account, entity authorization, automation result, or provenance statement as conclusive by itself. Cross-channel account binding, periodic account-control revalidation, risk-based evidence requests, suspension controls, a time-of-submission `Not a Contribution` rule, and separate technical/human merge gates are used as independent controls.

### Risk allocation

Schedule A adds:

- no agency and no authority to bind;
- the principle that responsibility follows the actor;
- a scoped third-party-claim indemnity tied to specified contributor-side breaches or misconduct;
- direct, documented remediation-cost recovery for foreseeable contributor-side breaches;
- defense and settlement mechanics;
- an explicit responsibility boundary excluding independent Macro Evidence wrongdoing; and
- survival language.

The clauses do not claim to prevent a third party from naming Macro Evidence, the contracting party, a future entity, or another participant in a legal proceeding.

### Electronic and private execution

The public forms are reference copies. Private execution copies contain the legally necessary identity, address, signature, coverage, and integrity fields.

A GitHub checkbox is not contract execution. Version 1.0.0 requires a handwritten signature or an electronic-signature method verified as legally sufficient for the applicable execution. The process can adopt a different signing provider later if the legal terms and evidence of identity, intent, signature, and document integrity remain materially equivalent.

Document integrity is recorded in three layers: the canonical agreement-terms SHA-256 identified in the execution copy, the SHA-256 of the complete unsigned execution file actually issued, and the SHA-256 of the complete signed file returned after execution. File hashes are recorded in the private register rather than inserted into the file being hashed. The entire-agreement clause also states that private execution fields, schedules, and administrative records cannot silently amend the substantive agreement except where the public agreement expressly permits those records to supply or update identified information.

### Stamp formalities

The public agreement does not guess a stamp classification. The activation process requires an authoritative pre-execution determination where classification or duty is uncertain and retains the resulting evidence privately.

### Privacy and automation boundary

Private addresses, signatures, private contacts, executed documents, stamp-administration evidence, identity/authority evidence, account-binding evidence, entity schedules, and the full contributor-rights register remain private. Public automation receives only derived, non-sensitive coverage data and the structured GitHub event identifiers necessary to enforce merge coverage.

Automated coverage is not proof of authorship or provenance. Human and approved system-actor coverage is derived from the applicable private rights records, while any pull-request-specific exception remains narrowly bound to the applicable repository and pull request. Account bindings are periodically revalidated, and coverage suspension requires affected open pull requests to be rechecked before merge. The technical controls, token formats, expiry rules, exception binding, and stale-status handling are defined canonically in the [GitHub Contributor-Rights Enforcement](GITHUB_ENFORCEMENT.md) specification.

---

## Change-control rule

Future edits to the substantive rights grant, Covered Project scope, representations, indemnity, direct-loss allocation, no-agency rule, governing law, assignment/successor mechanism, outbound-license option, coverage-date mechanics, or execution-signature standard require explicit governance review and a new agreement version where existing signatories' legal terms would change.

Operational improvements to secure storage, GitHub status-check plumbing, or signing-provider implementation do not by themselves require a new CLA version if they do not alter the legal terms or the evidence of assent required by the approved process.

---

## Changelog

### 1.0.0 (2026-09-24)

- Initial version. Records the primary contractual source and secondary design source for the Macro Evidence ICLA/ECLA, the deliberate Harmony selections made, Macro Evidence-specific changes and their rationale, and the change-control rule governing future edits.
- Makes the legal instrument's customization surface auditable and constrains future edits from drifting into unexplained bespoke contract language.
- Does not repeat the present contracting party's personal name where the agreement forms already provide the necessary contracting-party identity.
