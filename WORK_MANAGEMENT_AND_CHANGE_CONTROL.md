# Work Management and Change Control

## 1. One active objective

At any time, the project should have:

- One active phase
- One clearly stated phase objective
- A small number of active work items
- One identified next action

Do not use a large undifferentiated backlog as a substitute for sequencing.

## 2. Work-item requirements

No implementation begins without:

- Problem statement
- User value
- In-scope behavior
- Explicit non-goals
- Acceptance criteria
- Expected files or system areas
- Required tests
- Data or migration impact
- Security/privacy impact
- Dependencies
- Rollback notes where applicable

Use `templates/WORK_ITEM_TEMPLATE.md`.

## 3. Definition of Ready

A work item is Ready when:

- It belongs to the active phase.
- The user problem is clear.
- Acceptance criteria are testable.
- Required decisions are approved.
- Dependencies are available.
- Data semantics are defined.
- No unresolved scope conflict exists.

## 4. Definition of Done

A work item is Done when:

- Acceptance criteria pass.
- Required tests pass.
- Linting and type checks pass.
- Database migrations are included and reversible where feasible.
- No secrets or private data are committed.
- Documentation is updated.
- Screens include loading, empty, error, and stale states where applicable.
- Accessibility implications are checked.
- The change was reviewed by the Product Owner.
- Unresolved risks are logged.
- The pull request explains what changed and how it was verified.

## 5. Change levels

### Level 0 — Correction

Typo, documentation clarification, or defect correction with no behavior change.

Record in the work item or pull request.

### Level 1 — Controlled implementation variation

A technical implementation choice that remains within the approved architecture and acceptance criteria.

Document in the pull request.

### Level 2 — Product change

Changes behavior, adds a filter, changes ranking, modifies information displayed, or alters an event category.

Requires Product Owner approval and a change request.

### Level 3 — Structural change

Changes architecture, database semantics, privacy, authentication, security controls, hosting, or project mission.

Requires an ADR, impact analysis, and Product Owner approval.

## 6. Drift-control questions

Before starting any task, ask:

1. Is this required for the current phase exit gate?
2. Is it listed in the approved work item?
3. Does it introduce a new dependency or service?
4. Does it change user-visible behavior?
5. Does it alter the data model?
6. Does it collect or retain more user data?
7. Could the work be deferred without blocking the current phase?
8. Is this refactor necessary for the requested change?

If questions 3–8 reveal unapproved work, stop and raise it rather than implementing it.

## 7. Stop-work triggers

Codex must stop and report when:

- Instructions conflict with governance.
- A required file or decision is missing.
- A migration may lose data.
- Tests reveal unrelated major defects.
- A dependency requires a paid plan or new account.
- A source or schedule cannot be represented by the approved data model.
- A requested change expands scope.
- Credentials or secrets appear in the repository.
- The implementation would require storing precise location.
- The requested task would bypass a phase gate.

## 8. Status reporting

At the end of each work session, record:

- Objective attempted
- Work completed
- Files changed
- Commands run
- Tests and results
- Decisions made
- Risks or blockers
- Exact next action

Use `templates/STATUS_REPORT_TEMPLATE.md`.
