# Macro Evidence — Governance

Canonical governance for the Macro Evidence organization and its platforms.

## Contents

| Document | Covers |
| --- | --- |
| [ORGANIZATION_CHARTER.md](ORGANIZATION_CHARTER.md) | Organization mission, vision, platform roles, product relationships, durable direction |
| [GOVERNANCE.md](GOVERNANCE.md) | Decision criteria, execution model, review cadence, governance hierarchy, versioning |
| [DOCUMENTATION_STANDARDS.md](DOCUMENTATION_STANDARDS.md) | Documentation ownership, public-boundary rules, ADR contract, verification, naming, commit conventions |
| [TRADEMARKS.md](TRADEMARKS.md) | Trademark, brand, and organizational identity policy |
| [CONTRIBUTION_POLICY.md](CONTRIBUTION_POLICY.md) | Organization-wide contribution participation, acceptance, contributor-rights, and stewardship policy |
| [decisions/](decisions/) | Cross-cutting Architecture Decision Records; repository-specific decisions remain with the repository they govern |
| [legal/cla/](legal/cla/) | Contributor-agreement reference forms, execution/privacy/provenance process, and third-party-material handling |

## Versioning

Each independently versioned governance or policy document carries its own version and changelog. There is no single version number for this repository as a whole; see [`GOVERNANCE.md`](GOVERNANCE.md) §7.

## Scope

This repository owns organization-wide governance, policy, documentation standards, and genuinely cross-cutting decisions. Repository-specific architecture, implementation, setup, runtime behavior, and technical decisions remain with the repository they govern.

## Community and participation

The organization-wide Contribution Policy is canonical here because it defines cross-repository participation, acceptance, and contributor-rights principles.

GitHub-specific contribution mechanics, the Code of Conduct, security reporting, and default community-health templates remain in [`macro-evidence/.github`](https://github.com/macro-evidence/.github).

## Verification

This documentation-only repository uses a local Markdown verification path rather than dedicated CI. With Node.js 22 or later available, run:

```text
npx --yes markdownlint-cli@0.49.1 "**/*.md"
```

The repository configuration enables the standard `markdownlint` rule set except line-length enforcement (`MD013`). The direct tool version is pinned; verification tooling should be re-evaluated when its dependency or security state materially changes.

## Licensing

The repository default and file-specific exceptions are defined by [`LICENSING.md`](LICENSING.md). The repository `LICENSE` file supplies the default CC BY-SA 4.0 terms. Repository licensing does not itself grant rights to use Macro Evidence's names, marks, or visual identity; see [`TRADEMARKS.md`](TRADEMARKS.md).
