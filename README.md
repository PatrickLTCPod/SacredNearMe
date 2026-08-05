# Sacred Near Me — Project Governance Pack

**Purpose:** Keep the product owner, ChatGPT, and the local Codex implementation environment aligned while building the Clermont County and Cincinnati East Side Catholic worship finder.

**Pack version:** 1.0.0  
**Created:** August 3, 2026  
**Project status:** Pre-development governance and data-foundation stage  
**Canonical timezone:** America/New_York

## How to use this pack

1. Copy this entire folder into the root of the Sacred Near Me repository.
2. Keep `AGENTS.md` at the repository root so the local Codex sees it before making changes.
3. Read `CURRENT_PHASE.md` before beginning any work.
4. Create a work item from `templates/WORK_ITEM_TEMPLATE.md`.
5. Do not begin work that is outside the active phase or lacks acceptance criteria.
6. Record architecture, scope, security, or data-model decisions in `decisions/`.
7. Update `CURRENT_PHASE.md`, `RISK_REGISTER.md`, and the applicable decision record when approved changes occur.
8. Treat repository governance files—not chat history—as the project’s source of truth.

## Reading order

1. `PROJECT_CHARTER.md`
2. `SCOPE_AND_PRODUCT_RULES.md`
3. `ROLES_AND_DECISION_RIGHTS.md`
4. `CURRENT_PHASE.md`
5. `ROADMAP_AND_PHASE_GATES.md`
6. `WORK_MANAGEMENT_AND_CHANGE_CONTROL.md`
7. `ARCHITECTURE_GUARDRAILS.md`
8. `DATA_GOVERNANCE.md`
9. `QUALITY_SECURITY_ACCESSIBILITY.md`
10. `RISK_REGISTER.md`
11. `AGENTS.md`

## The governing principle

> Build the smallest verified product that reliably answers: “What Catholic worship, sacramental, or communal prayer opportunity is available near me now or later today?”

No feature, refactor, integration, or design improvement outranks schedule accuracy, arrival feasibility, source transparency, and simple mobile use.
