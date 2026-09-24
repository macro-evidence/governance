# Macro Evidence - Third-Party Material Process

> Version 1.0.0 · Active · Last updated 2026-09-24

---

A contributor agreement can grant only rights the applicable rights holder owns, controls, or is authorized to grant. This process applies when a proposed Contribution contains or depends on material whose rights or provenance are not entirely the contributor's own.

---

## 1. Material that must be disclosed

Disclose relevant non-owned or externally restricted material before merge, including where applicable:

- third-party source code, patches, snippets, examples, or generated code;
- documentation, text, images, diagrams, audio, video, fonts, or other media;
- datasets, database extracts, schemas, metadata, or data compilations;
- material subject to a third-party open-source, open-content, commercial, research, data, or API license;
- material subject to patent, trademark, confidentiality, privacy, contractual, export, or field-of-use restrictions;
- employer-, client-, university-, institution-, or other entity-controlled material; and
- generated or model-assisted material where tool terms, source provenance, incorporated material, or the circumstances of generation could affect ownership, licensing, confidentiality, privacy, or other rights.

Use of a generation tool does not by itself establish that the resulting material is original, unrestricted, or safe to contribute.

---

## 2. Required disclosure

For each material item requiring separate treatment, provide enough information to evaluate it, including where known:

- a clear description of the material and where it appears in the proposed Contribution;
- source or upstream location;
- rights holder or provider;
- applicable license, permission, terms, or authorization;
- required notices, attribution, source-offer, share-alike, copyleft, or other obligations;
- known patent, trademark, confidentiality, privacy, data, contractual, or technical restrictions; and
- any modification made before submission.

Do not remove or obscure an upstream notice merely to make the material appear original to the contributor.

---

## 3. Review outcomes

Macro Evidence may:

- accept the material under its applicable upstream terms;
- require a notice, attribution, source reference, licensing map, or file-level license marker;
- require separate written permission;
- require an employer/entity authorization or ECLA;
- request replacement with independently created material;
- exclude the material from the Contribution; or
- decline the Contribution where the rights position is insufficiently clear or incompatible with the repository.

Review of third-party material does not guarantee acceptance of the Contribution. A maintainer's review, test result, merge, or prior acceptance of similar material is not a representation that the contributor's provenance or authority was independently verified and does not waive the contributor's agreement representations.

---

## 4. Security, secrets, privacy, and confidential information

Do not submit live credentials, access tokens, private keys, confidential information, trade secrets, or personal data that you are not authorized to disclose.

Security-test fixtures or deliberately sensitive examples must use synthetic or properly authorized material and follow the affected repository's security process.

If sensitive information is accidentally submitted, stop public discussion of the sensitive content and follow the affected repository's [security policy](https://github.com/macro-evidence/.github/blob/main/SECURITY.md) or the legal reporting route immediately.

---

## 5. Generated or model-assisted material

When a Contribution materially uses generated or model-assisted output, the contributor remains responsible for the rights and provenance representations made under the applicable contributor agreement.

Disclose the use when it is material to rights review, especially where:

- the provider's terms impose restrictions relevant to downstream use;
- the output appears to reproduce identifiable third-party material;
- confidential, proprietary, or personal data was provided to the tool;
- a dataset or model license may carry downstream obligations; or
- the contributor cannot reasonably establish the provenance needed for the repository's licensing position.

Macro Evidence may require independent replacement or additional provenance evidence where generated material creates material uncertainty.

---

## 6. Multiple authors or rightsholders

Where proposed material has multiple material co-authors, joint owners, employers, clients, institutions, or other rightsholders whose permission is necessary, the submitter must identify them and provide the applicable rights basis for each required interest. Coverage for the pull-request author does not by itself cover separately owned rights. Macro Evidence may require each relevant natural person to have an [ICLA](ICLA.md) and each relevant entity rights-holder to provide an [ECLA](ECLA.md) or other documented authorization, unless an existing licence or permission already supplies the needed rights.

---

## 7. Enhanced review for higher-risk material

Macro Evidence may require additional evidence before merge when a Contribution creates elevated provenance or legal risk. Examples include substantial copied or ported work, binary-only artifacts, unusually large code drops, generated/model-assisted material with unclear source history, employer- or client-controlled work, patent-sensitive implementations, datasets or database extracts with non-obvious rights, security tooling, or material whose provenance or history materially conflicts with the contributor's stated provenance.

Depending on the risk, the contributor may be asked for upstream locations, exact licence or permission text, rights-holder or employer authorization, source-to-output comparisons, generation/transformation history, reproducible build or generation instructions, hashes, or other evidence reasonably proportionate to the question. Macro Evidence may independently compare the proposed material against likely upstream sources or reject material whose provenance cannot be established to the required standard.

Retyping, reformatting, translating, lightly modifying, or passing material through an automated or generative tool does not make third-party material original or erase upstream obligations. Git commit authorship, a repository username, or a contributor's assertion is evidence but is not conclusive proof of ownership or authority.

---

## 8. `Not a Contribution` and contribution intent

Material conspicuously designated `Not a Contribution` at the time it is submitted is excluded from that Submission and is not merge-eligible on the strength of that excluded communication. A later designation does not retroactively withdraw rights already granted for an earlier Submission. If a contributor later wants excluded material merged, the contributor must deliberately re-submit it for inclusion under the applicable agreement in a durable project record and satisfy the ordinary contributor-rights and provenance requirements. Maintainer review or merge does not silently convert excluded material into a Contribution.

---

## 9. Continuing duty to correct

If a contributor or entity later learns that previously supplied provenance, authorization, restriction, identity, or contribution-account information was materially inaccurate, notify [legal@macro-evidence.com](mailto:legal@macro-evidence.com) promptly. Macro Evidence may suspend merge clearance, remove or replace affected material, preserve evidence, or take other reasonable steps while the issue is resolved.

---

## Changelog

### 1.0.0 (2026-09-24)

- Initial version. Defines third-party-material disclosure, review outcomes, sensitive-material handling, generated or model-assisted material review, multi-rightsholder coverage, enhanced provenance review, `Not a Contribution` handling, and continuing correction.
