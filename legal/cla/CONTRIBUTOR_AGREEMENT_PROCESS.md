# Macro Evidence - Contributor Agreement Process

> Version 1.0.0 · Active · Last updated 2026-09-24

---

Macro Evidence welcomes external proposals and reviews them on their merits. Covered external copyrightable Contributions are not merged until the required contributor-rights basis is verified. No single signal—an account, signature, automation result, authorship claim, or provenance statement—is treated as conclusive by itself; the agreement, private records, public declarations, technical gate, and human review provide independent controls.

---

## 1. Coverage model

Every natural person whose external copyrightable Contribution may be merged must have an active Macro Evidence Individual Contributor License Agreement (ICLA) on file unless Macro Evidence has documented another sufficient rights path for the specific case.

A signatory must be legally competent to enter the agreement. The standard v1 path is for adults who can contract in their own right. If the standard path is not legally sufficient for a contributor, the Contribution is not merged until Macro Evidence has documented another sufficient rights path.

If an employer, company, institution, or other legal entity owns or may control relevant rights, an Entity Contributor License Agreement (ECLA) is additionally required unless Macro Evidence has documented another sufficient authorization for the specific rights issue. The ECLA supplements rather than ordinarily replaces the natural person's ICLA.

An agreement is not required merely to open an issue, discuss a proposal, or open and review a pull request. The gate is fail-closed at merge.

---

## 2. Public reference copies and private execution copies

The public ICLA and ECLA are reference copies. They intentionally omit private addresses, signatures, private contact information, entity coverage schedules, and identity/authority evidence.

Before signing, Macro Evidence prepares or approves a private execution copy that contains:

- the exact agreement version and SHA-256 identifier of the approved canonical agreement terms;
- the signatories' legally necessary identity and private contact information;
- the applicable Coverage Start Date and, if earlier Contributions are intended to be covered, the exact pre-Effective-Date Submissions identified by repository or Covered Project and durable Submission identifier;
- the parties' signature fields and execution dates;
- the public contribution identities being bound to the agreement; and
- for an ECLA, the private Entity Coverage Schedule and authority information.

Only designated private execution fields and schedules may be completed in an issued execution copy; the substantive agreement terms must remain identical to the approved version. Before delivery, the private register records the SHA-256 of the complete unsigned execution file actually issued. After all required signatures are present, the register separately records the SHA-256 of the complete executed file. Neither file is required to contain its own file hash, avoiding a self-referential integrity field. Any other substantive alteration requires a new approved template/version rather than silent execution-copy editing.

---

## 3. Identity and contribution-account binding

A signed agreement and a GitHub account are separate evidence. Before an account receives actor-level merge coverage, Macro Evidence binds the signer's asserted legal identity to the account's immutable GitHub numeric account ID using a cross-channel control.

The initial binding procedure is:

1. the signer returns the executed agreement through the approved private legal route using the private contact recorded in the agreement;
2. Macro Evidence records the exact GitHub numeric account ID and current username supplied for contribution matching;
3. Macro Evidence issues a one-time random challenge containing no private identity data;
4. the signer proves current control of the declared GitHub account by publishing or returning that challenge through a Macro Evidence-designated GitHub surface; and
5. Macro Evidence verifies the response, records the evidence privately, and only then activates the derived merge-coverage token.

The challenge proves control of the contribution account at that time; it is not government identity verification and does not make later account activity conclusive evidence that the signer personally authorized it. Macro Evidence may require reasonable additional identity or entity-authority evidence when facts create material doubt. Failure to provide sufficient evidence means coverage is not activated.

A contributor who wants to use an additional GitHub account must bind that account separately. Account renames are tracked by numeric account ID. Account sale, transfer, shared use, compromise, or loss of control must be reported promptly to [legal@macro-evidence.com](mailto:legal@macro-evidence.com).

Account binding is revalidated at least every 12 months before further actor-level merge clearance, regardless of ordinary account activity. Each human actor coverage entry carries a validity date no later than that revalidation deadline, so the automated gate expires stale actor coverage even if trusted configuration was not cleaned up on time. Revalidation confirms current account control; it does not require re-signing an otherwise valid agreement. Revalidation is required immediately when credible evidence suggests compromise, transfer, shared control, material identity uncertainty, or loss of control.

---

## 4. Execution method

Version 1.0.0 uses a conservative signing baseline because the agreement grants intellectual-property rights for which applicable law may impose writing, signature, or evidentiary requirements.

An approved execution method must provide reliable evidence of identity, intent, document integrity, and the exact terms accepted. The initial approved methods are:

- a handwritten wet-ink signature on a complete paper counterpart. The signed counterpart is scanned in full and returned as a complete PDF through the private legal route, and the signer retains the original physical counterpart unless Macro Evidence requires delivery of the original for the specific execution; or
- an electronic or digital signature method that Macro Evidence has verified for the actual execution as legally sufficient under applicable law and that preserves an auditable signed document and signature-validation evidence.

A GitHub checkbox, pull-request comment, typed name, DCO sign-off, or ordinary email acknowledgment alone is not accepted as execution of the CLA.

Macro Evidence may add or replace an execution provider without changing agreement version 1.0.0 if the provider does not alter the substantive legal terms and continues to provide legally sufficient evidence of signature, identity, intent, document integrity, and retention.

Executed agreements are delivered and administered privately through [legal@macro-evidence.com](mailto:legal@macro-evidence.com) unless the published process identifies another private first-party route.

---

## 5. Stamp and execution formalities

Before the first live agreement is executed under a new instrument version, Macro Evidence verifies and satisfies the stamp, execution, and similar formalities applicable to that instrument and the actual place and method of execution.

Where the proper stamp classification or duty is uncertain, Macro Evidence uses an available statutory adjudication process or other authoritative government mechanism before relying on an assumption. Evidence of the determination and payment, where applicable, is retained privately with the agreement administration record.

Contributors are not expected to infer or independently determine Macro Evidence's stamp-administration obligations.

---

## 6. Contribution intent and the `Not a Contribution` exclusion

The agreement's `Not a Contribution` exclusion is administered through this process with auditable timing. A communication is excluded only when it is conspicuously designated `Not a Contribution` at the time it is sent. A later designation cannot retroactively withdraw rights already granted for an earlier Submission.

Material originally sent as `Not a Contribution` is not merge-eligible on the strength of that excluded communication. If the contributor later wants Macro Evidence to merge the material, the contributor must deliberately re-submit the material for inclusion under the applicable agreement in a durable project record and satisfy the ordinary contributor-rights and provenance requirements. Silence, review activity, or a maintainer's merge action does not convert excluded material into a Contribution.

Before merge, the pull-request author must make a durable declaration that the material requested for merge is intended as a Contribution under the applicable contributor-rights process. This declaration is evidence of contribution intent. It is not the contributor-agreement signature and does not cure missing ownership or authority.

---

## 7. GitHub contributor-rights merge gate

The normal merge-enforcement experience is automated even though the legal agreement and detailed rights records remain private.

The required status is named Contributor rights coverage. A covered pull request must receive a passing status on its current head before merge. The underlying basis may be an active ICLA, supplementary ECLA coverage where required, a separately documented internal/system rights basis, or a narrowly approved exception permitted by the Contribution Policy.

The automated gate is derived from the private coverage state and does not establish authorship, ownership, employer authority, provenance, or truth of contributor representations. Those matters remain subject to the contributor agreement, account binding, provenance review, and human review.

The technical security invariants, trusted-workflow requirements, token formats, expiry rules, exception binding, stale-status controls, and activation requirements are maintained in the [GitHub Contributor-Rights Enforcement](GITHUB_ENFORCEMENT.md) specification.

---

## 8. Coverage suspension, account compromise, and stale-check control

Automated coverage is a revocable merge authorization even when intellectual-property rights already granted by an executed agreement are irrevocable for prior covered Contributions.

Macro Evidence suspends future automated clearance when it receives credible evidence of account compromise, loss or transfer of account control, material identity or authority uncertainty, a material provenance dispute, suspected fraud, an agreement-status problem, or another condition that makes continued automatic reliance unsafe.

On suspension or future-coverage termination:

- remove the affected actor-level coverage token from the trusted configuration;
- mark the private record accordingly without deleting prior execution evidence;
- identify every open pull request relying on that actor-level coverage;
- invalidate, re-run, or otherwise replace any earlier passing contributor-rights check before merge; and
- do not rely on a green status produced before the coverage-state change merely because the pull-request head has not changed.

A compromised account may be rebound only after the contributor-rights administrator obtains sufficient evidence of restored or replacement account control. A human actor-level binding that has reached its revalidation deadline fails automated clearance through the dated actor entry and is treated as not current until revalidated. Prior rights already granted for legitimately covered Contributions are not silently revoked by suspending or expiring future merge clearance.

Because GitHub status results do not automatically become stale merely because private coverage configuration changed after a completed run, this revalidation rule is a mandatory human operational control in v1. If future GitHub functionality or a first-party GitHub App can enforce current-state coverage atomically at merge with less operational risk, Macro Evidence should migrate deliberately rather than pretending the v1 check solves that timing problem.

---

## 9. Private agreement and coverage register

Executed contributor agreements are authoritative for the contractual rights and obligations they grant. The private contributor-rights register is the administrative source of truth for current coverage state and merge authorization derived from those rights. It records the minimum information needed to administer and evidence the applicable basis, including where relevant:

- immutable internal record ID;
- rights-basis type, such as ICLA, ICLA+ECLA, present rights recipient, documented internal rights basis, approved non-human system actor, or pull-request-specific exception;
- agreement variant and version where an agreement applies;
- legal signatory or rights-holder identity;
- public GitHub numeric account ID and current username used for contribution matching;
- account-binding method, challenge identifier/hash, verification date, next revalidation due date, derived actor-entry validity date, and evidence reference;
- private administrative contact;
- Coverage Start Date, any specifically identified pre-Effective-Date covered Submission identifiers, and Effective Date where applicable;
- canonical agreement-terms SHA-256, issued unsigned execution-file SHA-256, and complete executed-file SHA-256 where applicable;
- entity, Covered Affiliate, Authorized Contributor, and authority information where applicable;
- status and status-effective date, including active, suspended, future-coverage-terminated, replaced, or voided-before-effect; for approved system actors, the covered repository numeric ID and next rights-basis review/coverage-expiry date;
- replacement, assignment, or successor history; and
- secure storage reference.

A pull-request-specific exception additionally records the repository, PR number, exact head commit, `valid_through` date, reason, approver, evidence, and expiry or completion state. It never becomes a reusable actor exemption merely because one PR was approved.

The full register, executed agreements, authority evidence, and account-binding evidence are not stored in public repositories.

---

## 10. Agreement versioning, replacement, and successor transition

A contributor remains governed by the agreement version they executed for Contributions within that agreement's scope unless a later executed agreement expressly replaces or amends it.

A new substantive agreement version does not silently rewrite an existing signed agreement. Macro Evidence may require a new version before future Contributions are merged if the new version changes material rights or obligations.

Administrative changes to storage, signing-provider implementation, token derivation, or GitHub status-check plumbing do not by themselves require contributors to re-execute the agreement when substantive legal terms and evidence of assent remain materially equivalent.

If rights and obligations are transferred to a future legally capable Macro Evidence entity or another permitted successor, the transition must be documented through the agreement's assignment/succession mechanism or applicable law. The private register records the effective transfer and assumption. Public contributor instructions are updated before new signatures are taken under a changed counterparty. A material counterparty or governing-law change is reviewed for whether a new agreement version is required for future Contributions.

This process improves continuity but does not pretend that an unincorporated project is already a legal person independent of its present contracting party.

---

## 11. Entity administration

An ECLA must be executed by a person with authority to bind the Legal Entity. The private Entity Coverage Schedule identifies Covered Affiliates, the basis for the signatory entity's authority to make grants for them, Authorized Contributors, bound contribution identities, and the applicable coverage dates.

Changes to Authorized Contributors or the administrative contact may be accepted through a signed private notice without re-executing the substantive ECLA when the Legal Entity, Covered Affiliate rights basis, agreement terms, and rights grant remain unchanged. Adding a Covered Affiliate requires documented authority sufficient for that Affiliate. Removal affects future submissions and does not revoke rights already granted for prior Contributions.

A material merger, dissolution, change of legal identity, change of authority, or other event that makes the existing entity record unreliable suspends future merge clearance until the record is reconciled.

---

## 12. Third-party material, enhanced provenance review, and continuing accuracy

A contributor agreement cannot grant rights that the signatory does not own, control, or have authority to license. Contributors must follow the published Third-Party Material Process and disclose applicable restrictions and provenance. Where material has multiple material co-authors or rightsholders, every necessary rights interest must be covered by an applicable agreement, licence, permission, employer/entity authorization, or other documented sufficient basis before merge; one pull-request author cannot create coverage for another rightsholder merely by submitting the work.

For a substantial, binary, copied, generated/model-assisted, employer-controlled, patent-sensitive, security-sensitive, unusually licensed, or otherwise high-risk Contribution, Macro Evidence may require enhanced evidence before merge, including upstream locations, licence texts, author/rights-holder confirmation, generation or transformation history, source-to-output comparison, reproducible build or generation instructions, or other evidence proportionate to the risk. Git author metadata and a contributor's self-description are not conclusive proof of ownership or authority.

Contributors and entity signatories must notify Macro Evidence at [legal@macro-evidence.com](mailto:legal@macro-evidence.com) if they later become aware that a material representation in an executed agreement was inaccurate or if identity, entity authority, or provenance relevant to future Contributions changes.

---

## 13. No automatic contribution entitlement

Signing an ICLA or ECLA, passing an automated status check, or previously having a Contribution accepted does not guarantee that another Contribution will be accepted, merged, published, maintained, supported, or prioritized. None creates governance authority, employment, agency, partnership, sponsorship status, compensation, or authority to bind Macro Evidence.

Macro Evidence may decline a Contribution when the rights, provenance, security, legal, maintainability, or operational position remains materially uncertain even if the automated contributor-rights status passes.

---

## 14. Administrative contact

Questions about agreement execution, entity authority, account binding, coverage suspension, record correction, or a copy of an executed agreement may be sent privately to [legal@macro-evidence.com](mailto:legal@macro-evidence.com).

---

## Changelog

### 1.0.0 (2026-09-24)

- Initial version. Defines contributor-rights coverage, account binding, execution, stamp formalities, contribution intent, merge-control requirements, suspension, private-record administration, agreement versioning, entity administration, provenance review, and administrative contact.
