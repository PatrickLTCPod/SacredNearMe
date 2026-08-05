# AGENTS.md — Local Codex Operating Instructions

You are implementing **Sacred Near Me**, a mobile-first Catholic worship finder for Clermont County and Cincinnati’s East Side.

## Read before doing anything

Read these files in order:

1. `PROJECT_CHARTER.md`
2. `SCOPE_AND_PRODUCT_RULES.md`
3. `CURRENT_PHASE.md`
4. `ROADMAP_AND_PHASE_GATES.md`
5. `WORK_MANAGEMENT_AND_CHANGE_CONTROL.md`
6. `ARCHITECTURE_GUARDRAILS.md`
7. `DATA_GOVERNANCE.md`
8. `QUALITY_SECURITY_ACCESSIBILITY.md`
9. The active work item

If any file is absent or conflicts with the task, stop and report the conflict.

## Non-negotiable behavior

- Work only within the active phase.
- Implement only the active approved work item.
- Do not redesign the product.
- Do not add features because they seem useful.
- Do not add dependencies without documenting the need.
- Do not refactor unrelated code.
- Do not change governance files unless explicitly instructed.
- Do not commit secrets.
- Do not use production credentials locally.
- Do not bypass tests, branch protections, or migrations.
- Do not directly modify production data.
- Do not merge to `main`.
- Do not publish automatically scraped schedule changes.
- Do not store a user’s precise location.
- Do not begin UI polish before the functional phase permits it.

## Before editing

Report:

1. The requested outcome
2. Why it belongs to the active phase
3. Files likely to change
4. Tests to add or run
5. Data, security, privacy, accessibility, and migration impact
6. Any ambiguity or governance conflict

Do not ask broad design questions when the approved files already answer them.

## Implementation standard

Make the smallest complete change that satisfies the acceptance criteria.

Prefer:

- Clear domain functions
- Strong TypeScript types
- Database constraints
- Explicit errors
- Deterministic tests
- Accessible HTML
- Simple components
- Reversible migrations
- Official-source traceability

Avoid:

- Premature abstraction
- Generic frameworks inside the project
- Duplicate sources of truth
- Hidden behavior
- Magic dates or timezone assumptions
- Plain-text recurrence logic scattered across components
- Unrequested dashboards
- Unrequested AI features

## Required validation

Run all applicable:

- Formatting
- Lint
- Type check
- Unit tests
- Integration tests
- End-to-end tests
- Build
- Migration checks
- Accessibility checks

Never claim a check passed unless it actually ran.

## Completion report

Provide:

- Summary
- Files changed
- Behavior added or corrected
- Tests added
- Commands run and results
- Migrations
- Security/privacy/accessibility notes
- Unresolved risks
- Exact recommended next action

## Stop conditions

Stop immediately if:

- The task changes scope.
- A destructive migration is needed.
- A new paid service or account is required.
- The data model cannot represent the requirement.
- Official-source semantics are unclear.
- Secrets or private information are exposed.
- The active phase gate would be bypassed.
- The work item lacks testable acceptance criteria.

When stopping, explain the smallest decision needed from the Product Owner.
