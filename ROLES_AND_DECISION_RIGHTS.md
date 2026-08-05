# Roles and Decision Rights

## 1. Named roles

### Product Owner — Patrick

Final authority over:

- Scope
- Priorities
- User experience
- Geographic boundary
- Release approval
- Budget and service choices
- Acceptance of risk
- Public launch

### Field Tester and Visual-Usability Partner — Katie

Primary responsibilities:

- Test real-world usefulness during errands.
- Evaluate visual scanning and touch-target clarity.
- Report unclear language, excessive density, and navigation friction.
- Validate whether the app is practical in passenger use and before driving.

Katie is not automatically responsible for project administration or data maintenance.

### Research, Planning, and Governance Partner — ChatGPT

Primary responsibilities:

- Research official and authoritative sources.
- Maintain coherent project scope and order of operations.
- Draft specifications, acceptance criteria, tests, data rules, and governance updates.
- Compare proposed work against approved scope.
- Identify drift, missing prerequisites, and contradictions.
- Review outputs supplied by the user or local Codex.

ChatGPT may recommend changes but may not treat a recommendation as approved.

### Implementation Agent — Local Codex

Primary responsibilities:

- Implement only approved work items.
- Read governance files before changing code.
- Make the smallest complete change that satisfies acceptance criteria.
- Run and report tests.
- Avoid unrelated refactoring.
- Stop when a change would alter approved scope, architecture, data semantics, security posture, or release behavior.

Codex does not approve its own scope changes and does not merge to the protected production branch.

### Data Steward — Patrick initially

Primary responsibilities:

- Approve the church inventory.
- Resolve ambiguous local coverage.
- Approve source and verification policies.
- Decide whether conflicting official schedules can be displayed with caution.
- Own the final call on corrections before public release.

## 2. Decision classes

### Class A — Routine implementation

Examples:

- Styling within an approved design
- Adding a test for approved behavior
- Fixing a defect without changing expected behavior
- Refactoring limited to the active work item

**Decision authority:** Codex may implement; Product Owner accepts through review.

### Class B — Product behavior

Examples:

- New filter
- Ranking change
- New event status
- Revised card content
- New notification behavior

**Decision authority:** Product Owner approval required before implementation.

### Class C — Architecture, data, privacy, or security

Examples:

- New hosting provider
- Authentication change
- Database-schema redesign
- New third-party API
- Storing location history
- Automated publication from scraped sources
- Destructive migration

**Decision authority:** ADR plus Product Owner approval required.

### Class D — Scope or mission

Examples:

- Expanding geography
- Adding social events
- Building a native app
- Adding public accounts, comments, payments, or parish administration tools

**Decision authority:** Formal change request and Product Owner approval.

## 3. RACI summary

| Activity | Patrick | Katie | ChatGPT | Local Codex |
|---|---|---|---|---|
| Approve scope | A | C | R/C | I |
| Define requirements | A | C | R | C |
| Research sources | A | I | R | C |
| Implement code | A | I | C | R |
| Approve architecture | A | I | R/C | C |
| Test usability | A | R | C | C |
| Verify schedules | A/R | C | R/C | I |
| Approve release | A | C | C | I |
| Maintain governance | A | I | R | C |

A = Accountable, R = Responsible, C = Consulted, I = Informed.

## 4. Conflict rule

When instructions conflict, use this order:

1. Latest explicit Product Owner decision recorded in the repository
2. Approved ADR
3. Current phase gate
4. Project charter and scope
5. Active work item
6. Existing implementation and tests
7. Chat history

Chat history is context, not the canonical project record.
