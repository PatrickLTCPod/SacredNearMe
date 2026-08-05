# Risk Register

| ID | Risk | Likelihood | Impact | Trigger | Mitigation | Owner | Status |
|---|---|---:|---:|---|---|---|---|
| R-001 | Parish schedules become stale | High | High | Review date passes or user reports mismatch | Monthly review queue, visible verification dates, source links | Data Steward | Open |
| R-002 | Scope expands into a general parish directory | High | High | Requests for social, news, formation, or commerce features | Inclusion test, phase gates, formal change control | Product Owner | Open |
| R-003 | Recurrence engine gives false “available now” result | Medium | Very High | Boundary, monthly, seasonal, or DST test fails | RFC-compatible model, extensive unit fixtures, field tests | Codex | Open |
| R-004 | Official sources conflict | High | High | Two official pages show different times | Conflict status, preserve both sources, contact parish | Data Steward | Open |
| R-005 | Maintenance burden exceeds capacity | Medium | High | Overdue review queue grows | Limit geography, prioritize core categories, measure review time | Product Owner | Open |
| R-006 | Codex over-engineers before data model is proven | High | High | New services, abstractions, UI, or dependencies outside active issue | AGENTS rules, one active phase, PR review | Product Owner | Open |
| R-007 | Destructive database migration | Low | Very High | Migration drops or rewrites verified data | Backup, preview migration, explicit approval, rollback | Codex/Product Owner | Open |
| R-008 | Admin access is misconfigured | Medium | Very High | Public mutation succeeds or RLS test fails | RLS tests, least privilege, server-only service role | Codex | Open |
| R-009 | Precise location is retained unintentionally | Low | High | Logs or database include coordinates tied to user | No persistence, privacy tests, log review | Codex | Open |
| R-010 | App is difficult to use in real errands | Medium | High | Field tests require repeated scrolling or typing | Large controls, available-now home screen, Katie testing | Katie/Product Owner | Open |
| R-011 | Accessibility is deferred | Medium | High | Late audit reveals structural barriers | WCAG 2.2 AA from first UI phase, automated and manual checks | Codex | Open |
| R-012 | Preview and production environments drift | Medium | High | Different schema, variables, or behavior | Migrations, environment documentation, preview checks | Codex | Open |
| R-013 | Automatic scraping publishes bad data | Medium | Very High | Parsed page change alters public schedule | Automation flags only; human approval required | Product Owner | Controlled |
| R-014 | Third-party dependency creates cost or lock-in | Medium | Medium | New service required or free tier changes | Dependency policy, ADR, portable domain model | Product Owner | Open |
| R-015 | Cached offline data looks current | Medium | High | Offline result lacks clear timestamp | Prominent offline and last-updated status | Codex | Open |
| R-016 | Church inventory is incomplete | Medium | High | Parish discovered after bulk schedule work | Complete inventory and coverage gate before schedule phase | ChatGPT/Data Steward | Open |
| R-017 | Product makes inappropriate sacramental claims | Low | High | Copy implies eligibility, guarantee, or pastoral determination | Approved language rules and domain review | Product Owner | Open |
| R-018 | Repository governance is ignored | Medium | High | Work begins without issue or outside phase | Protected main, PR template, mandatory status report | Product Owner | Open |

## Risk review rule

Review this register:

- At each phase gate
- Before release
- After a Severity 1 or 2 incident
- When adding a third-party service
- When expanding geography or event categories
