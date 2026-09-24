# 0011. Use mixed licensing for .github community content and executable automation

**Status:** Accepted
**Date:** 2026-09-24

## Context

Governance decision 0003 adopted CC BY-SA 4.0 for `macro-evidence/.github` when the repository's substantive role was organization profile/community-health content plus small declarative GitHub configuration and no material executable automation had been identified.

The contributor-rights system introduces a reusable GitHub Actions workflow that performs contributor-rights coverage checks for pull requests. That workflow is executable software/configuration with security-sensitive behavior, not merely community-health prose. Treating it as though the earlier content-only premise had not changed would create an avoidable software/content licensing ambiguity.

The existing profile, contribution guidance, security policy, pull-request template, issue forms, and Code of Conduct remain community/participation content. Their current CC BY-SA 4.0 default remains appropriate subject to existing third-party provenance.

## Decision

 With the contributor-rights coverage workflow now introduced, replace decision 0003's repository-wide content-only licensing premise with a mixed licensing map:

- CC BY-SA 4.0 remains the default for `.github` community-health and organization-profile content;
- executable GitHub Actions workflows and first-party helper software in the repository are licensed under Apache License 2.0 unless a file-specific notice states otherwise;
- `LICENSING.md` identifies the boundary and points to the applicable license texts;
- third-party content retains its upstream terms; and
- public workflow code contains no private contributor-agreement records or secrets.

This decision supersedes governance decision 0003 as the canonical `.github` licensing architecture.

## Consequences

- Community content retains reciprocal open-content licensing while executable automation receives a software-appropriate permissive licence.
- The repository gains a mixed-license map but avoids pretending one licence is equally suitable for materially different artifact types.
- Future executable automation must be assigned to the software side of the map explicitly rather than inheriting CC BY-SA by accident.
- The contributor-rights workflow still requires separate security review, hosted Actions-event policy, required-check configuration, and runtime verification before it becomes an active merge gate.
