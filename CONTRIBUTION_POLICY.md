# Macro Evidence — Contribution Policy

> Version 1.1.0 · Active · Last updated 2026-09-24

---

## 1. Purpose

Macro Evidence is open to community participation while retaining responsibility for the quality, direction, security, maintainability, and long-term stewardship of its repositories and public infrastructure.

This policy defines the organization-wide rules for proposing and accepting contributions. Repository-specific technical instructions may extend this policy but must not contradict it.

---

## 2. Open participation, selective acceptance

Anyone may propose a legitimate contribution to Macro Evidence, subject to the affected repository's contribution process and Code of Conduct.

Opening an issue, discussion, pull request, or other contribution does not guarantee that the work will be accepted, merged, published, maintained, or supported.

Macro Evidence may accept, decline, request changes to, or defer a contribution based on factors such as:

- fit with the affected repository's scope and current needs;
- technical or editorial merit;
- evidence and verification appropriate to the change;
- maintainability and consistency with existing architecture or standards;
- security and operational risk;
- licensing and third-party provenance;
- compatibility with organization governance and accepted decisions;
- review capacity; and
- whether the contribution creates disproportionate maintenance or dependency cost.

These criteria protect stewardship quality; they do not create a promise that every contribution satisfying one criterion will be accepted.

---

## 3. What contribution does not confer

Submitting or having a contribution accepted does not by itself create:

- governance authority or voting rights;
- roadmap control or preferential feature acceptance;
- issue, review, or support priority;
- employment, contractor, partnership, or agency status;
- compensation or reimbursement;
- sponsorship status or recognition; or
- ownership of Macro Evidence's project direction, names, marks, or organizational identity.

Contribution is a non-monetary participation path. Monetary support is handled separately through Macro Evidence's sponsorship model and does not purchase technical authority.

---

## 4. Contributor rights and repository licenses

Contributors must have the right to submit the work they offer. Do not submit material that you do not have permission to contribute under the applicable terms.

Each repository's committed `LICENSE` establishes that repository's default public licensing terms, subject to any material that is explicitly identified under separate third-party or file-specific terms. If a repository has no committed license, do not infer licensing terms from another Macro Evidence repository; an external copyrightable contribution is not merged until the applicable repository licensing terms are established. Rights in Macro Evidence's names, marks, and visual identity are addressed separately by the Trademarks Policy, any express license terms, and applicable law; do not infer official status or general trademark permission from a repository license.

Macro Evidence requires an approved contributor-rights basis before an external copyrightable contribution is merged. When the need for contributor-rights coverage is uncertain, the contribution is treated as requiring coverage until the question is resolved. Automated clearance is a merge control, not proof that a contributor's identity, ownership, employer authority, or provenance statement is true.

The approved contributor-agreement architecture uses an Individual Contributor License Agreement (ICLA) for each natural person whose covered contribution may be merged. If an employer, company, institution, or other legal entity owns or may control relevant rights, an Entity Contributor License Agreement (ECLA) is additionally required unless Macro Evidence has documented another sufficient rights path for the specific situation.

Where an agreement applies:

- the contributor retains ownership of their original contribution unless a separate written agreement expressly says otherwise;
- Macro Evidence receives the copyright and patent rights stated in the applicable agreement, including rights needed to use, modify, distribute, sublicense, and relicense accepted contributions;
- the approved outbound-license provision permits additional open, commercial, or proprietary licensing while preserving the submission-date public licensing required by the agreement;
- signing an agreement does not guarantee acceptance and does not create employment, agency, partnership, sponsorship, governance authority, compensation, or authority to bind Macro Evidence; and
- executed agreements and personal administrative information are private records and are not published merely because a person contributes.

The applicable contributor agreement controls the legal terms of the grant. It cannot grant Macro Evidence rights in third-party material that the contributor or entity does not control. A pull request checkbox, issue comment, DCO sign-off, or this policy is not a substitute for an executed agreement where one is required.

The canonical public process is maintained in [`legal/cla/CONTRIBUTOR_AGREEMENT_PROCESS.md`](legal/cla/CONTRIBUTOR_AGREEMENT_PROCESS.md). The public ICLA/ECLA reference forms, privacy notice, third-party-material process, and provenance notice are maintained in the same directory. GitHub merge enforcement may be automated, but the **Contributor rights coverage** status exposes only the non-sensitive result needed for merge control. There is no blanket contributor-rights bypass merely because an account is an organization member, collaborator, or previously accepted contributor.

---

## 5. Employer, entity, and third-party material

If your employer or another organization owns or may control rights in your proposed contribution, make sure the applicable individual and entity contributor-rights coverage is in place before merge.

Third-party code, documentation, data, media, generated material, or other non-owned material must be identified and handled under the [Third-Party Material Process](legal/cla/THIRD_PARTY_MATERIAL_PROCESS.md) and must be compatible with the affected repository's licensing and provenance requirements. Do not present third-party work as your own. Provide complete source and restriction information known to you when non-owned material is proposed for inclusion.

Contributors and entity signatories must notify Macro Evidence if they later become aware that a material rights or provenance representation was inaccurate, or if entity authorization relevant to future contributions changes.

Macro Evidence may request additional identity, authority, rights, provenance, or source evidence before accepting substantial, employer-owned, patent-sensitive, generated, binary, copied/ported, security-sensitive, unusually licensed, or otherwise high-risk contributions. A contributor's self-certification, Git author metadata, automated status result, or prior successful contribution is not conclusive where contrary evidence or material uncertainty exists.

---

## 6. Contribution process

The organization-wide GitHub contribution guide is maintained in [`macro-evidence/.github`](https://github.com/macro-evidence/.github/blob/main/CONTRIBUTING.md).

Repository-specific setup, development, testing, data, architecture, and verification instructions belong to the affected repository. For substantial changes, contributors should discuss scope before investing significant implementation effort when the repository guidance asks them to do so.

Contributions are also subject to the organization-wide [Code of Conduct](https://github.com/macro-evidence/.github/blob/main/CODE_OF_CONDUCT.md) unless a repository publishes a more specific applicable policy.

Security vulnerabilities must not be reported through a public contribution. Follow the affected repository's security policy; the organization-wide default is maintained in [`macro-evidence/.github`](https://github.com/macro-evidence/.github/blob/main/SECURITY.md).

---

## 7. Stewardship and future licensing

Macro Evidence's public-good posture depends on keeping its public core openly available while maintaining enough organizational control to steward that work over the long term.

Additional licensing terms, where applicable, do not by themselves revoke open-source or open-content rights validly granted to the public.

Material changes to licensing practice will be addressed through the applicable governance and policy process. Consultation, where appropriate, informs the decision but does not change legal rights already granted or create automatic governance authority.

---

## 8. Questions

For general contribution or collaboration questions, contact [hello@macro-evidence.com](mailto:hello@macro-evidence.com).

For contributor-agreement execution, entity authority, licensing administration, or legal-record questions, contact [legal@macro-evidence.com](mailto:legal@macro-evidence.com).

---

## Changelog

### 1.1.0 (2026-09-24)

- Operationalizes the contributor-rights boundary through the approved agreement architecture and public process references.
- Clarifies that automated clearance is a merge control, not proof of identity, ownership, authority, or provenance.
- Keeps contribution participation separate from sponsorship, governance authority, and other organizational entitlements.
- MINOR — adds operational contributor-rights and merge-enforcement requirements without changing the policy's existing open-participation and merit-based acceptance principles.

### 1.0.0 (2026-09-03)

- Established the organization-wide contribution policy.
- Defined open participation with merit- and evidence-based selective acceptance.
- Separated contribution from sponsorship and other organizational entitlements.
- Established contributor-rights, third-party-provenance, and contributor-agreement boundaries.
- Preserved the public open-source/open-content core while allowing additional licensing where Macro Evidence holds the required rights and later decides such licensing is appropriate.
