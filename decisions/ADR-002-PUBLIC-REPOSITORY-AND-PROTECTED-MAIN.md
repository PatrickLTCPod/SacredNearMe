# ADR-002: Public repository and protected main

**Status:** Accepted  
**Date:** August 5, 2026  
**Decision owner:** Patrick  
**Related work item:** `work-items/PHASE-0-PUBLIC-READINESS.md`  

## Context

Sacred Near Me needs a protected `main` branch and transparent project governance. GitHub Free does not provide traditional branch protection for this repository while it is private, but protection is available when the repository is public. A public-readiness inspection found no secrets or sensitive historical blobs, while identifying licensing, contribution, and personal-information decisions that required Product Owner acceptance.

## Decision

- Make `PatrickLTCPod/SacredNearMe` public to support project transparency and GitHub Free branch protection.
- Accept the existing initial-commit email exposure and the named project roles for Patrick and Katie.
- Do not rewrite Git history.
- Grant no open-source license. Public visibility does not authorize reuse, modification, or redistribution, and all rights remain reserved unless a later license is explicitly approved.
- Do not accept outside contributions during Phase 0. Unsolicited pull requests may be closed without review.
- Require changes to reach `main` through pull requests.
- Require zero approving reviews while the repository remains single-owner, so the pull-request author is not blocked by an impossible self-approval requirement.
- Enforce protection for administrators, including the repository owner.
- Require pull-request conversations to be resolved before merging.
- Prohibit force pushes and deletion of `main`.
- Add required status checks only after continuous integration is separately approved and implemented.
- Require no code-owner review, merge queue, deployment rule, branch lock, branch-creation restriction, or bypass actor at this stage.

## Alternatives considered

- Keep the repository private without branch protection.
- Purchase GitHub Pro solely for private-repository branch protection.
- Make the repository public and grant an open-source license.
- Rewrite the initial commit to replace its author email.
- Require an approving review in the single-owner repository.

## Consequences

### Positive

- `main` can be protected under GitHub Free.
- Governance and project status are transparent.
- Changes remain reviewable through pull requests.
- Licensing and contribution expectations are explicit.

### Negative

- Repository content and Git history become publicly accessible.
- Public users may still open issues even though outside contributions are not accepted.
- Zero required approvals provides process visibility but not independent reviewer enforcement.

### Risks

- Public copies, clones, caches, or forks cannot be recalled.
- Visibility could change before branch protection succeeds.
- Public visibility could be mistaken for an open-source license despite the repository notice.
- Protection settings could drift unless they are periodically verified.

## Security, privacy, accessibility, and data effects

The Product Owner accepts disclosure of the existing initial-commit email and the existing named project roles. No additional private information is approved for publication. Branch protection must be applied immediately after the visibility change. This decision creates no application data, migration, user interface, accessibility behavior, dependency, or production-system change.

## Rollback or replacement path

The repository may later return to private visibility and GitHub settings may be reverted, but already-public copies cannot be recalled. Documentation changes may be reverted through Git. History must not be rewritten as part of rollback. If protection cannot be established promptly after publication, return the repository to private visibility and stop development until the failure is resolved.

## Approval

**Product Owner:** Patrick  
**Date:** August 5, 2026  
