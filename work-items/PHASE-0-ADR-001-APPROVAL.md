# Work Item: Phase 0 ADR-001 Approval and Governance Reconciliation

**ID:** PHASE-0-ADR-001-APPROVAL  
**Phase:** Phase 0 — Governance and repository foundation  
**Type:** Governance  
**Decision class:** C — Architecture, data, privacy, or security  
**Owner:** Patrick  
**Status:** Approved  
**Implementation branch:** `phase-0/adr-001-approval`  

## Problem

ADR-001 contains the approved baseline application stack but remains marked proposed. The repository therefore does not yet contain the Product Owner's canonical approval, and the corresponding Phase 0 exit criterion remains incomplete.

The immediate-next-action text in `CURRENT_PHASE.md` is also stale because pull request #1 has already been merged.

## User value

Recording the decision makes the approved architecture canonical, removes ambiguity for later implementation, and permits the project to complete the initial-ADR Phase 0 exit criterion without beginning application work prematurely.

## Product Owner decision to record

The Product Owner records this decision effective August 5, 2026:

> The Product Owner approves ADR-001 and the baseline application stack as written.

The approval covers the baseline stack recorded in ADR-001:

- Next.js
- TypeScript
- Progressive Web App behavior
- Supabase/PostgreSQL
- Supabase Auth for administrators
- Vercel
- GitHub
- Google Maps URL handoff
- `America/New_York` as the canonical operating timezone
- RFC 5545-compatible recurrence concepts

This approval does not authorize application development before Phase 0 is complete.

## In scope

The later implementation task governed by this work item must:

1. Update `decisions/ADR-001-INITIAL-STACK.md` to record:
   - Status: Accepted
   - Product Owner: Patrick
   - Approval date: August 5, 2026
   - The decision is approved as written
2. Preserve the existing baseline stack and architectural reasoning without expanding or redesigning it.
3. Update `CURRENT_PHASE.md` to mark:
   - Initial ADR approved
4. Update the matching Current Phase section in `MASTER_GOVERNANCE_PACK.md` so it agrees exactly with `CURRENT_PHASE.md`.
5. Correct the stale immediate-next-action language in both locations.
6. Set the new immediate next action to creating the Phase 1 church-inventory work item with acceptance criteria.
7. Leave the Phase 1 work-item exit criterion unchecked until that work item actually exists.
8. Update this work item with its approval and implementation status.
9. Implement the changes on a task-specific branch.
10. Commit and push the approved changes.
11. Open a pull request against protected `main`.
12. Leave the pull request unmerged for Product Owner review.

## Explicit non-goals

- Application code
- Next.js initialization
- Package installation
- Supabase configuration
- Vercel configuration
- GitHub Actions
- Continuous integration
- Database schemas
- Church inventory creation
- Event research
- Recurrence implementation
- UI development
- Phase 1 implementation
- Modification of ADR-002
- Changes to the approved stack
- New architecture decisions
- Dependency selection or version pinning
- Changes to repository visibility or branch protection
- Deletion of task branches

## Acceptance criteria

- [ ] ADR-001 status is `Accepted`.
- [ ] Patrick is recorded as Product Owner.
- [ ] The approval date is August 5, 2026.
- [ ] The approved baseline stack remains unchanged.
- [ ] No new architecture choices are introduced.
- [ ] `CURRENT_PHASE.md` marks the initial ADR criterion complete.
- [ ] The Phase 1 work-item criterion remains incomplete.
- [ ] `CURRENT_PHASE.md` and the matching consolidated-pack section agree exactly.
- [ ] Stale references to reviewing or merging pull request #1 are removed.
- [ ] The immediate next action identifies creation of the Phase 1 church-inventory work item.
- [ ] ADR-002 remains unchanged.
- [ ] No application code, dependencies, workflows, migrations, or deployment files are created.
- [ ] Only approved governance files change.
- [ ] The changes are committed on a task-specific branch.
- [ ] A pull request is opened and left unmerged.
- [ ] The working tree is clean after implementation.
- [ ] A completion report lists files, commits, commands, verification, and remaining Phase 0 criteria.

## Expected areas affected

- Code: None
- Database: None
- Documentation: `decisions/ADR-001-INITIAL-STACK.md`, `CURRENT_PHASE.md`, the matching Current Phase section in `MASTER_GOVERNANCE_PACK.md`, and this work item
- Data: None
- UI: None
- Git/GitHub: A task-specific branch, governance commit, task-branch push, and unmerged pull request; no repository-setting changes

## Required tests

- Unit: Not applicable
- Integration: Not applicable
- E2E: Not applicable
- Manual: Verify ADR status and approval fields, unchanged stack and reasoning, exact Current Phase synchronization, accurate Phase 0 criteria, corrected immediate-next-action text, unchanged ADR-002, and absence of unrelated files
- Accessibility: Not applicable; no user interface changes are in scope
- Git/GitHub: Verify task-specific branch use, expected commit and push, unmerged pull request against protected `main`, clean working tree, and unchanged repository settings

## Security and privacy impact

No application security or privacy behavior changes. The work records an approved architecture decision in the already-public governance repository and adds no credentials, personal data, runtime service, or access-control change.

## Data and migration impact

None. No application data, schema, seed data, migration, or production system is in scope.

## Dependencies

- The Product Owner decision recorded above
- Product Owner review and approval of this work item for implementation
- A clean task branch created from the current protected `main`
- The existing ADR-001, Current Phase documents, and consolidated governance pack
- Authenticated GitHub access for the later task-branch push and pull-request creation

## Risks

- ADR wording could be unintentionally altered while changing status.
- Phase 0 criteria could be marked complete without supporting evidence.
- `CURRENT_PHASE.md` and the consolidated governance pack could drift.
- Application work could begin before the final Phase 0 criterion is complete.
- The work item could incorrectly imply that dependency versions or detailed implementation choices are already approved.
- Changes could be committed directly to protected `main`.

## Rollback or recovery

- Documentation changes can be reverted through Git.
- ADR status can be returned to proposed if the Product Owner rescinds approval before implementation begins.
- Do not rewrite Git history.
- Do not revert or weaken branch protection.
- If the pull request contains unrelated changes, close it without merging and recreate the task branch from current `main`.

## Approval

**Product Owner approval:** Patrick  
**Date:** August 5, 2026
