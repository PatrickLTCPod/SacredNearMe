# Work Item: Phase 0 Public Repository Readiness and Protected Main

**ID:** PHASE-0-PUBLIC-READINESS  
**Phase:** Phase 0 — Governance and repository foundation  
**Type:** Governance  
**Decision class:** C — Architecture, data, privacy, or security  
**Owner:** Patrick  
**Status:** Approved  
**Implementation branch:** `phase-0/public-readiness`  

## Problem

The repository is technically safe to publish, but its governance status and public presentation do not yet accurately reflect the repository's current state.

## User value

Public visibility will permit GitHub Free branch protection while keeping the project transparent and governed.

## Product Owner decisions

The Product Owner records these decisions effective August 5, 2026:

1. The `PatrickLTCPod/SacredNearMe` repository is approved to become public.
2. Public visibility is intended to support transparency and GitHub branch protection.
3. Public visibility does not currently grant an open-source license.
4. No open-source license will be added during this work item.
5. Until a later Product Owner decision, the repository remains under default copyright with no permission granted for reuse, modification, or redistribution.
6. The existing initial-commit email exposure is accepted.
7. Git history will not be rewritten to remove or replace the initial-commit email.
8. Future commits should use the authenticated GitHub account's private `noreply` commit address when available.
9. Existing references to Patrick and Katie and their project roles are accepted for public visibility.
10. Issues will remain enabled because the governance workflow requires issue templates and work management.
11. Projects will remain enabled because the governance pack defines a project-board workflow.
12. Outside contributions are not being accepted during Phase 0.
13. A public contribution notice must clearly communicate that unsolicited pull requests may be closed without review.
14. The repository must not become public until the approved public-presentation remediation is complete.
15. The repository must not remain publicly unprotected longer than necessary. Visibility change and `main` protection must occur in one controlled follow-up task.

These decisions do not approve ADR-001, an open-source license, application implementation, or contributions from outside the project.

## In scope

The implementation governed by this work item must:

1. Update `README.md` so it accurately describes the existing repository instead of instructing the reader to create or copy it.
2. Update `CURRENT_PHASE.md` to accurately record completed Phase 0 criteria supported by repository evidence.
3. Record the Product Owner's public-repository decisions in an appropriate canonical governance location.
4. Preserve the proposed status of ADR-001 unless it is separately approved.
5. Add a clear repository licensing statement explaining that no open-source license has been granted.
6. Add a contribution notice stating that outside contributions are not accepted during Phase 0 and that unsolicited pull requests may be closed without review.
7. Add or configure the GitHub labels `type:bug` and `type:feature`, which are referenced by the issue templates.
8. Confirm that both issue templates remain active.
9. Add a concise GitHub repository description.
10. Configure the repository-local Git commit email to the authenticated account's private GitHub `noreply` address if one can be reliably determined.
11. Change the repository visibility from private to public only after the documentation remediation is complete.
12. Immediately configure protection for `main` with all of the following settings:
    - Pull requests required.
    - Zero approving reviews required.
    - Administrator enforcement enabled.
    - Pull-request conversation resolution required.
    - No required status checks yet.
    - No code-owner review requirement.
    - Force pushes disabled.
    - Branch deletion disabled.
    - No bypass actors.
13. Verify through GitHub that the repository is public and `main` is protected with the approved settings.
14. Update applicable Phase 0 exit-criterion status only when supported by direct verification.

## Explicit non-goals

- Application code
- Next.js setup
- Supabase setup
- Vercel setup
- GitHub Actions
- Continuous integration
- Database schemas
- UI work
- Event research
- Church inventory
- Recurrence modeling
- Approval of ADR-001
- Selection of an open-source license
- History rewriting
- Removal of Patrick or Katie from governance documents
- Opening the project to outside contributions

## Acceptance criteria

- [ ] The August 5, 2026 Product Owner public-readiness decisions are recorded in an appropriate canonical governance location.
- [ ] `README.md` accurately describes the repository and the project's present pre-development state.
- [ ] `CURRENT_PHASE.md` marks only Phase 0 criteria that are supported by direct repository or GitHub evidence.
- [ ] The repository states clearly that no open-source license has been granted and that default copyright applies.
- [ ] The repository states clearly that outside contributions are not accepted during Phase 0 and unsolicited pull requests may be closed without review.
- [ ] GitHub labels `type:bug` and `type:feature` exist and correspond to the active issue templates.
- [ ] Both issue templates remain active after remediation.
- [ ] The GitHub repository description is populated with concise, accurate project status and purpose.
- [ ] The repository-local Git commit email uses the authenticated account's private GitHub `noreply` address when that address can be reliably determined; otherwise the blocker and evidence are reported without guessing.
- [ ] Repository visibility is verified as public only after all approved public-presentation remediation is complete.
- [ ] GitHub API verification confirms the approved `main` protection settings, including required pull requests, zero approvals, administrator enforcement, conversation resolution, no required status checks, no code-owner review, no force pushes, no deletion, and no bypass actors.
- [ ] No application code, application configuration, package, dependency, database artifact, deployment configuration, or continuous-integration workflow is created.
- [ ] No unrelated repository file or GitHub setting changes.
- [ ] The working tree is clean after implementation is completed.
- [ ] The completion report identifies every changed file, GitHub setting, command, API request, and verification result.

## Expected areas affected

- Code: None
- Database: None
- Documentation: `README.md`, `CURRENT_PHASE.md`, an approved canonical governance decision location, contribution and licensing notices, and any required synchronized consolidated governance copy
- Data: None
- UI: None
- Git/GitHub: repository-local commit identity, issue labels, repository description, visibility, and `main` branch protection

## Required tests

- Unit: Not applicable
- Integration: Not applicable
- E2E: Not applicable
- Manual: Verify documentation accuracy, required labels, active issue templates, repository description, local Git identity, visibility, clean working tree, and absence of unrelated changes
- Accessibility: Not applicable; no user interface is in scope
- GitHub API: Verify visibility, default branch, `main` protection settings, absence of bypass actors, and unchanged unrelated repository settings

## Security and privacy impact

This work intentionally makes repository contents and Git history public. The Product Owner accepts the existing initial-commit email exposure and the existing references to Patrick and Katie. No additional personal information may be added. Branch protection must be applied immediately after visibility changes so `main` is not left publicly unprotected longer than necessary. The implementation must preserve the prohibition on force pushes, branch deletion, and bypass actors.

## Data and migration impact

None. No application data, database schema, seed data, migration, or production system is in scope.

## Dependencies

- Product Owner review and approval of this work item for implementation
- A clean repository at the verified Phase 0 baseline
- Authenticated GitHub CLI access as `PatrickLTCPod`
- GitHub Free branch-protection availability after the repository becomes public
- Reliable determination of the authenticated account's private GitHub `noreply` commit address before configuring repository-local identity
- Ability to update repository labels, description, visibility, and branch protection through GitHub CLI and API

## Risks

- Public disclosure is effectively irreversible once the repository is cloned or forked.
- A public repository does not grant an open-source license.
- Public users may still open issues even when outside contributions are discouraged.
- Repository visibility could change before branch protection succeeds.
- Governance status could become inaccurate if criteria are checked without direct evidence.
- Repository-local commit identity could be configured incorrectly.
- `MASTER_GOVERNANCE_PACK.md` may drift from standalone governance files if only one copy is edited.
- Public-facing documentation could create conflicting sources of truth if licensing or contribution notices are duplicated inconsistently.

## Rollback or recovery

- Repository visibility can be returned to private, but public copies, caches, clones, and forks cannot be recalled.
- GitHub settings can be reverted.
- Tracked documentation changes can be reverted through Git.
- Git history must not be rewritten as part of rollback.
- If branch protection fails after visibility changes, stop all development and either complete protection immediately or return the repository to private.
- If repository-local commit identity cannot be verified, do not guess; leave it unchanged and report the blocker.

## Approval

**Product Owner approval:** Patrick  
**Date:** August 5, 2026  
