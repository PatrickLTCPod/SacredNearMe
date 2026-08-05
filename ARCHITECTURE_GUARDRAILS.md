# Architecture Guardrails

## 1. Baseline

Unless changed by an approved ADR:

- Framework: Next.js
- Language: TypeScript
- Database: PostgreSQL through Supabase
- Authentication: Supabase Auth for administrators only
- Hosting: Vercel
- Repository: GitHub
- Application type: Progressive Web App
- Mapping: Google Maps URL handoff
- Timezone: America/New_York

## 2. Architectural principles

- Keep schedule data separate from display code.
- Use migrations for every schema change.
- Store recurring schedules as structured rules, not copied future instances.
- Preserve event history and effective dates.
- Keep public reads separate from authenticated administration.
- Prefer server-side protection for privileged actions.
- Do not embed service-role credentials in the browser.
- Avoid vendor-specific behavior in the core event model where practical.
- Use standards-compatible recurrence concepts based on iCalendar/RFC 5545.
- Do not add a custom map, CMS, message queue, search engine, analytics platform, or native shell until a measured need exists.

## 3. Repository structure

Recommended baseline:

```text
/
├── AGENTS.md
├── README.md
├── docs/
│   ├── governance/
│   ├── product/
│   ├── data/
│   └── testing/
├── decisions/
├── app/
├── components/
├── lib/
│   ├── events/
│   ├── recurrence/
│   ├── ranking/
│   ├── sources/
│   └── validation/
├── supabase/
│   ├── migrations/
│   └── seed/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
└── .github/
```

The exact Next.js-generated directories may differ, but domain logic must not be scattered through page components.

## 4. Dependency policy

A new runtime dependency requires:

- Problem it solves
- Why built-in or existing tools are insufficient
- Maintenance status
- License
- Security considerations
- Bundle or operational effect
- Removal or rollback plan

Do not add dependencies solely to shorten a small amount of straightforward code.

Lockfiles are committed. Dependency upgrades are isolated from feature changes when practical.

## 5. Database policy

- Every table has a documented purpose.
- Primary keys are stable and non-semantic.
- Foreign keys protect relationships.
- Required business invariants use database constraints where possible.
- Public tables have explicit Row Level Security policies.
- Service-role access is server-only.
- Production changes use reviewed migrations.
- No manual production schema edits without a matching migration.
- Destructive migrations require backup confirmation and explicit approval.
- Seed data is separated from production verification records.

## 6. Recurrence policy

Use structured recurrence capable of representing:

- Weekly schedules
- Monthly ordinal weekdays
- Effective start and end dates
- Exceptions and cancellations
- Seasonal windows
- Overnight events
- Timezone-aware evaluation

Do not generate years of future event rows as the canonical source. Materialized occurrences may be cached, but recurring rules remain authoritative.

## 7. Environment separation

Maintain distinct:

- Local
- Preview/test
- Production

Environment variables and databases must not be casually shared across environments. Production data must not be copied into development when it contains private administrative information.

## 8. Branch and release policy

- `main` is protected.
- No force pushes to `main`.
- Changes arrive through pull requests.
- Required checks must pass before merge.
- Codex works on a task-specific branch.
- The Product Owner controls merge and release.
- Preview deployments are used for review.
- Releases use semantic versioning after the first formal release.
