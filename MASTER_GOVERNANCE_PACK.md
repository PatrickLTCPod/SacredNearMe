# Sacred Near Me — Consolidated Project Governance Pack

**Version:** 1.0.0  
**Date:** August 3, 2026


---

# Project Charter

## 1. Project identity

**Working name:** Sacred Near Me  
**Product type:** Installable mobile-first Progressive Web App  
**Initial territory:** Clermont County, Ohio, and Cincinnati’s eastern communities  
**Initial audience:** Patrick and Katie, followed by a limited private test group  
**Long-term possibility:** Public local Catholic worship finder

## 2. Product mission

Sacred Near Me helps a Catholic quickly identify a nearby opportunity for Mass, confession, Eucharistic adoration, a Holy Hour, or another approved recurring sacred event without searching multiple parish websites, bulletins, and calendars.

## 3. Primary user question

> What can I attend nearby now or later today, and can I realistically arrive before it begins or ends?

## 4. Product outcomes

The project succeeds when a user can:

- Find the next viable confession in under 15 seconds.
- See adoration currently available or opening later that day.
- Find the next Mass by time, distance, language, or area.
- Distinguish weekly, monthly, seasonal, and special schedules.
- Open directions, call the parish, and view the official source in one tap.
- See when each schedule was last verified.
- Use the core app without an account.
- Trust that uncertain or conflicting schedules are visibly labeled.

## 5. Foundational product principles

1. **Accuracy before breadth.**
2. **Official sources before secondary directories.**
3. **Arrival feasibility before simple geographic proximity.**
4. **Structured recurrence before copied schedule text.**
5. **Mobile speed before visual ornament.**
6. **Human review before automatic publication.**
7. **Minimal personal data collection.**
8. **Accessibility from the first functional version.**
9. **No general parish-event sprawl.**
10. **Every change must serve a documented user need.**

## 6. Initial approved technology direction

The provisional baseline is:

- Next.js with TypeScript
- Progressive Web App behavior
- Supabase/PostgreSQL
- GitHub source control
- Vercel deployment
- Google Maps direction links rather than a custom navigation system
- America/New_York as the canonical operating timezone

Changing a major platform or introducing a second overlapping platform requires an Architecture Decision Record and product-owner approval.

## 7. Success metrics

### Product usefulness

- Median time to find a viable event: 15 seconds or less.
- Directions accessible in one tap.
- At least 95% of displayed recurring events have a current official source and verification date.
- No event marked “available now” when its recurrence or effective date excludes it.
- Field testers choose the app over a manual browser search in most relevant situations.

### Maintenance

- Routine schedule correction requires no code change.
- Administrators can identify all records due for reverification.
- Seasonal overrides do not require duplicating an entire recurring schedule.
- Database changes are migration-controlled and recoverable.

## 8. Project constraints

- Initial development is performed by a local Codex environment under human direction.
- ChatGPT may research, plan, review, and create governance or test artifacts but does not silently change approved scope.
- Parish schedules can change without notice.
- “Complete” geographic coverage is only meaningful when paired with a repeatable verification process.
- The app must remain useful when location permission is denied.
- No system should imply sacramental eligibility or replace pastoral judgment.

---

# Scope and Product Rules

## 1. Approved Version 1 event categories

### Core

- Daily Mass
- Saturday vigil Mass
- Sunday Mass
- Holy Day Mass
- Regular public confession
- Communal penance services with individual confession
- Eucharistic adoration
- Adoration chapels
- Holy Hours
- Benediction

### Approved supporting sacred events

- Public Rosaries
- Liturgy of the Hours
- Divine Mercy Chaplets and Holy Hours
- First Friday devotions
- First Saturday devotions
- Stations of the Cross
- Public Masses or services with Anointing of the Sick
- Recurring healing Masses
- Corpus Christi and other Eucharistic processions
- Forty Hours and extended Eucharistic vigils
- Major Holy Week and liturgical-season services

## 2. Version 1 exclusions

Do not add these without an approved scope change:

- Fish fries, bingo, festivals, dinners, or fundraisers
- General parish social events
- School events
- Bible studies, book clubs, and formation classes
- Men’s, women’s, youth, or membership-based groups
- Retreats requiring registration
- Private baptisms, weddings, confirmations, or funerals
- Parish business meetings
- News feeds
- Social networking
- Donations or payment processing
- Livestream aggregation
- Parish bulletin archiving
- Public comments or reviews
- AI-generated spiritual advice
- Sacramental eligibility determinations
- Native Android or iOS applications before the PWA is proven

## 3. Inclusion test

An event belongs in the core product only when all are true:

1. It is Catholic liturgical, sacramental, Eucharistic, or an approved communal devotion.
2. A person can normally attend without registration or invitation.
3. It has a reliable time and location.
4. It can be verified through an official or directly confirmed source.
5. It helps answer “what can I attend now or later today?”

## 4. Geographic boundary

The approved initial area is:

### Clermont County

Batavia, Amelia, Eastgate/Union Township, Withamsville, Milford, Miami Township, Loveland vicinity, Goshen, Owensville, Williamsburg, Bethel, New Richmond, Stonelick Township, Pierce Township, Tate Township, Washington Township, Monroe Township, and Jackson Township.

### Cincinnati East Side

Anderson, Newtown, Mt. Washington, California, Columbia Tusculum, Mt. Lookout, Hyde Park, Oakley, Madisonville, Mariemont, Terrace Park, Indian Hill, Madeira, Kenwood, Montgomery, Blue Ash, Deer Park, Silverton, Pleasant Ridge, Norwood, East Walnut Hills, Mt. Adams, and Loveland.

Boundary expansion requires a change request explaining maintenance capacity and data-verification ownership.

## 5. Product language rules

- Use official church and parish-family names.
- Use plain language for event status.
- Say “official schedule,” “last verified,” and “source.”
- Do not say a schedule is guaranteed.
- Do not imply that confession will remain open after the published end time.
- For anointing, do not imply that every attendee is necessarily an appropriate recipient.
- Separate “by appointment” from public walk-in confession.
- Distinguish chapel access from exposition of the Blessed Sacrament.
- Distinguish recurring schedules from seasonal or one-time events.

## 6. Ranking policy

Results should prioritize:

1. Event is currently active or begins soon.
2. User can realistically arrive before the useful attendance window closes.
3. Official verification confidence.
4. Travel time and distance.
5. Event duration.
6. Relevant combined opportunities, such as confession during adoration.
7. User favorites.

Distance alone must never determine the “best” result.

---

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

---

# Current Phase

**Active phase:** Phase 0 — Governance and repository foundation  
**Status:** In progress  
**Last updated:** August 3, 2026  
**Release target:** None approved yet

## Current objective

Establish a controlled project repository and freeze the initial product rules before application code is built.

## Approved work now

- Install this governance pack in the project repository.
- Establish Git version control.
- Create protected `main`.
- Create issue and pull-request templates.
- Confirm the project name and repository name.
- Confirm the initial geographic boundary.
- Confirm Version 1 included and excluded event types.
- Build the canonical church-inventory template.
- Prepare the official-source research workflow.
- Create an empty but migration-controlled application skeleton only after Phase 0 exit criteria are met.

## Work not approved yet

- Full user interface implementation
- Production database tables
- Automatic scraping
- Geolocation
- Ranking algorithms
- Notifications
- Public launch
- Native mobile apps
- Visual polish
- Bulk parish data import

## Phase 0 exit criteria

All must be complete:

- [ ] Governance pack committed
- [ ] `AGENTS.md` located at repository root
- [ ] Product Owner approves project name
- [ ] Product Owner approves geographic boundary
- [ ] Product Owner approves event taxonomy
- [ ] Product Owner approves baseline stack or records an alternative ADR
- [ ] GitHub repository created
- [ ] Protected `main` configured
- [ ] Pull-request template active
- [ ] Issue templates active
- [ ] Initial ADR approved
- [ ] Phase 1 work item created with acceptance criteria

## Immediate next action

Create the repository and place this pack at its root. Do not begin product code until the unchecked Phase 0 items are resolved and recorded.

---

# Roadmap and Phase Gates

Work progresses only through approved gates. A later phase may be researched, but implementation may not bypass an unmet gate.

## Phase 0 — Governance and repository foundation

### Deliverables

- Governance pack
- Repository
- Protected main branch
- Issue and PR templates
- Initial architecture decision
- Product boundary and taxonomy approval

### Exit gate

See `CURRENT_PHASE.md`.

---

## Phase 1 — Church inventory and source map

### Objective

Identify the complete in-scope church universe before entering schedules.

### Deliverables

- Canonical church table
- Official names, addresses, coordinates, phones, websites
- Parish-family relationships
- Travel zones
- Official source map
- Coverage-gap report
- Duplicate-resolution report

### Exit criteria

- Every in-scope Catholic church has a unique identifier.
- No known duplicate churches remain unresolved.
- Every church has at least one official source or a documented research gap.
- Geographic coverage is approved by the Product Owner.
- No event schedule work depends on a church that is missing from the inventory.

---

## Phase 2 — Event and recurrence model

### Objective

Design and prove the schedule engine before bulk data entry or UI work.

### Deliverables

- Event taxonomy
- Database schema
- Recurrence representation
- Effective-date rules
- Exception and cancellation model
- Timezone handling
- Verification records
- Sample fixtures
- Unit tests for recurrence edge cases

### Required edge cases

- First Friday
- First Saturday
- Second and fourth Saturday
- Academic-year-only schedules
- Lent-only events
- Holy Day overrides
- Events crossing midnight
- Daylight-saving transitions
- Funeral or parish-event cancellation notes
- Conflicting official schedules
- Open-ended chapel hours
- Adoration with overlapping confession

### Exit criteria

- Sample events calculate correctly for at least one full calendar year.
- Exceptions override recurrence without deleting history.
- All times use America/New_York and preserve source wording.
- Tests prove “available now” behavior at boundaries.
- Data model is approved in an ADR.

---

## Phase 3 — Data administration and verified seed dataset

### Objective

Make schedule maintenance possible without code changes.

### Deliverables

- Admin authentication
- Church editor
- Event editor
- Source and verification editor
- Review-due queue
- Conflict status
- Audit history
- Seed schedules for a small pilot zone

### Exit criteria

- Admin actions are protected by Row Level Security.
- Public users cannot modify data.
- A schedule correction requires no deployment.
- Destructive changes are recoverable.
- At least one pilot zone is fully verified.

---

## Phase 4 — Core read-only mobile experience

### Objective

Prove the central user journey without location or design complexity.

### Deliverables

- Home
- Available now
- Later today
- Category lists
- Church details
- Official-source links
- Call and directions links
- Manual zone selector
- Verification labels

### Exit criteria

- Core flows work on a Pixel-sized screen and common iPhone viewport.
- A user can find the next confession in under 15 seconds in a usability test.
- No account is required.
- Empty, loading, error, and stale-data states are clear.
- WCAG 2.2 AA issues found in automated and manual review are resolved or logged.

---

## Phase 5 — Location and practical ranking

### Objective

Rank events based on actual usefulness.

### Deliverables

- Optional geolocation
- Distance and drive-time strategy
- Arrival-feasibility logic
- “Starts soon” and “ends soon” states
- Favorites
- Map handoff

### Exit criteria

- App works fully when location is denied.
- No precise location is retained without explicit future approval.
- Tests cover arrival before start and before end.
- Nearby ranking never overrides an impossible arrival window.

---

## Phase 6 — PWA, offline, and resilience

### Deliverables

- Installable manifest
- Service worker
- Recent-schedule cache
- Offline status
- Staleness warning
- Recovery behavior
- Production monitoring

### Exit criteria

- App installs on the Pixel 9.
- Offline mode never presents cached data as live.
- Updates do not strand the client on an incompatible cache.
- Production rollback is documented and tested.

---

## Phase 7 — Private field test

### Duration

At least several weeks of real-world use.

### Deliverables

- Test diary
- Usability issues
- Schedule errors
- Ranking failures
- Maintenance time log
- Go/no-go report

### Exit criteria

- No unresolved severity-1 defects.
- Schedule-verification workflow is sustainable.
- Patrick and Katie prefer the app over manual search in the target situations.
- Public-release risks are explicitly accepted or mitigated.

---

## Phase 8 — Public release

### Deliverables

- Privacy notice
- Disclaimer
- Correction-reporting process
- Production domain
- Full source and schedule review
- Support and maintenance plan
- Release notes

### Exit criteria

- Product Owner signs off.
- Backup and rollback tested.
- Security and accessibility checks complete.
- Every public event is within its re-verification window.

---

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

---

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

---

# Data Governance

## 1. Core rule

The schedule database is the product’s highest-value asset. A polished interface cannot compensate for unverified or misleading data.

## 2. Source hierarchy

Use sources in this order:

1. Official parish event calendar
2. Official parish worship or sacrament page
3. Current official parish bulletin
4. Official family-of-parishes website
5. Archdiocese of Cincinnati directory
6. Official parish social account
7. Direct parish-office confirmation
8. Secondary Catholic directory
9. User report

Secondary sources may identify a lead but do not establish a public schedule by themselves.

## 3. Required church fields

- Stable church ID
- Official church name
- Parish-family name
- Street address
- City, state, ZIP
- Latitude and longitude
- Phone
- Official website
- Travel zone
- Active/inactive status
- Accessibility and entrance notes when verified
- Last church-record verification date

## 4. Required event fields

- Stable event ID
- Church ID
- Event category and subtype
- Public title
- Start and end time
- Timezone
- Recurrence rule
- Effective start date
- Effective end date
- Exception dates
- Location within the church campus
- Language
- Public-attendance status
- Associated confession, Mass, adoration, or Benediction flags
- Notes
- Source ID
- Verification status
- Last verified date
- Next review date
- Created and updated timestamps
- Change history

## 5. Verification statuses

### Confirmed

Current official source supports the record.

### Confirmed with caution

Official source is current but warns of interruptions, funerals, holidays, academic breaks, priest availability, or similar conditions.

### Conflicting official sources

Two official sources disagree. Display only with an explicit caution if the Product Owner approves the practical interpretation.

### Seasonal

Valid only in the recorded season or date range.

### Needs reverification

Review deadline has passed.

### Unverified

Not yet supported by a current official or direct source. Do not display as confidently available.

### Retired

Schedule ended but remains in history.

## 6. Review cadence

Default maximum review windows:

- Confession: 30 days
- Adoration: 30 days
- Daily and Sunday Mass: 60–90 days
- Monthly devotions: 60 days
- Academic schedules: at semester boundaries
- Holy Days and seasonal events: reviewed for each occurrence
- Conflicts: immediate review
- Direct phone confirmations: record date, office contacted, and summary

The interface should not silently treat an overdue record as fully current.

## 7. Conflict handling

When official sources disagree:

1. Preserve both source records.
2. Record the exact conflict.
3. Check publication and effective dates.
4. Prefer a current parish calendar or bulletin over an undated page when appropriate.
5. Contact the parish when the conflict affects a likely user trip.
6. Do not overwrite the disagreement without an audit note.
7. Show a caution or suppress the event until resolved.

## 8. User-submitted corrections

A report creates a review item. It does not directly edit the public schedule.

Required report information:

- Church
- Event
- Observed issue
- Date observed
- Optional source
- Optional contact information

Avoid collecting unnecessary personal information.

## 9. Automation policy

Automated page checks may:

- Detect changed text
- Detect a new bulletin
- Compare hashes
- Flag missing schedule language
- Create a review task

Automation may not publish a new time, cancel an event, or resolve a conflict without human review.

## 10. Data quality checks

Automated validation should detect:

- End before start
- Missing timezone
- Invalid recurrence
- Review date before verification date
- Event outside effective window
- Missing official source for Confirmed status
- Duplicate church
- Duplicate overlapping event
- Coordinates outside the approved region
- Public event tied to inactive church
- “Available now” from an expired record

## 11. Liturgical calendar boundary

The national liturgical calendar may identify seasons and dates, but it does not supply local parish times. Local schedules must remain source-backed at the parish level.

---

# Quality, Security, Privacy, and Accessibility

## 1. Quality strategy

The testing pyramid should include:

### Unit tests

- Recurrence calculation
- Effective dates
- Exception dates
- Timezone and daylight-saving boundaries
- Ranking calculations
- Verification status
- Arrival feasibility
- Event grouping

### Integration tests

- Database constraints
- Row Level Security
- Admin permissions
- Public reads
- Migration behavior
- Source and verification relationships

### End-to-end tests

- Find confession now
- Find adoration today
- Find next Mass
- Deny location permission
- Open directions
- View official source
- See stale-data warning
- Admin corrects a schedule
- Seasonal override replaces a normal schedule

### Manual field tests

- Pixel 9
- At least one iPhone viewport
- Passenger use
- Bright outdoor light
- Weak connection
- Large text settings
- Keyboard navigation
- Screen-reader smoke test

## 2. Required checks before merge

- Formatting
- Linting
- Type checking
- Unit tests
- Applicable integration tests
- Build
- Migration validation
- Secret scan
- Dependency vulnerability review
- Accessibility smoke check for user-interface changes

## 3. Security baseline

Use NIST Secure Software Development Framework practices as a high-level development baseline and OWASP ASVS as the web-application verification checklist.

Minimum controls:

- Protected development environment
- No secrets in source control
- Least privilege
- Supabase Row Level Security on exposed tables
- Server-only service credentials
- Validated and encoded inputs
- Authenticated administrative mutations
- Audit trail for schedule changes
- Dependency review
- Backups
- Recovery procedure
- Security-relevant logging without sensitive personal data
- Review before production deployment

## 4. Privacy baseline

Version 1:

- No public account required
- No advertising
- No sale or sharing of user data
- Optional location only
- No permanent precise-location history
- Favorites stored locally unless later approved
- No record of confession or Mass attendance
- Minimal correction-form information
- No analytics platform until purpose and privacy impact are approved

Any future account, analytics, notification, or cross-device sync feature requires a privacy impact review.

## 5. Accessibility target

Target WCAG 2.2 Level AA.

Key project-specific requirements:

- Large touch targets
- Visible focus
- Keyboard operability
- Sufficient contrast
- Text resizing
- No color-only status communication
- Clear labels
- Predictable navigation
- Accessible error messages
- Reduced-motion support
- Status messages exposed to assistive technology
- Directions and call links with meaningful accessible names

## 6. Mobile-driving safety

The application is not designed for active manipulation by a driver.

Design choices should favor:

- Pre-trip use
- Passenger use
- One-tap handoff to navigation
- Minimal typing
- Large controls
- No dense dashboard while moving
- No attention-demanding animation
- Clear confirmation before changing destination

## 7. Severity levels

### Severity 1 — Release blocker

- Wrong event marked available now
- Data exposure
- Unauthorized admin change
- Destructive migration
- Core app unusable
- Directions to wrong church

### Severity 2 — High

- Major recurrence error
- Location-denied path broken
- Critical accessibility barrier
- Stale-data warning missing
- Official-source link wrong

### Severity 3 — Medium

- Confusing sort
- Minor layout failure
- Incomplete notes
- Non-core filter defect

### Severity 4 — Low

- Cosmetic inconsistency
- Minor copy issue

Severity 1 and 2 defects must be resolved or explicitly accepted before release.

---

# Project Board and Labels

## Board columns

1. Inbox
2. Needs Definition
3. Ready
4. In Progress
5. Review
6. Blocked
7. Done
8. Deferred

Only Ready items may move to In Progress.

## Required fields

- Phase
- Work type
- Priority
- Owner
- Decision class
- Risk level
- Target release
- Verification status when data-related

## Recommended labels

### Work type

- `type:feature`
- `type:bug`
- `type:data`
- `type:research`
- `type:governance`
- `type:security`
- `type:accessibility`
- `type:maintenance`

### Phase

- `phase:0-governance`
- `phase:1-inventory`
- `phase:2-recurrence`
- `phase:3-admin-data`
- `phase:4-core-ui`
- `phase:5-location`
- `phase:6-pwa`
- `phase:7-field-test`
- `phase:8-release`

### Priority

- `priority:critical`
- `priority:high`
- `priority:normal`
- `priority:low`

### Status and control

- `needs-decision`
- `needs-source`
- `scope-change`
- `blocked`
- `breaking-change`
- `migration`
- `security-review`
- `accessibility-review`

## Work-in-progress limit

No more than:

- One major feature item in progress
- One defect item in progress
- One research item in progress

Finish or explicitly block current work before starting another major item.

---

# Release and Versioning

## 1. Environments

- Local: developer machine and local database
- Preview: pull-request deployment and test database
- Production: approved public or private release

Do not point local or preview builds at production administrative credentials.

## 2. Release process

1. Work item accepted
2. Pull request opened
3. Required checks pass
4. Preview reviewed
5. Data migrations reviewed
6. Backup status confirmed where applicable
7. Product Owner approves
8. Merge to protected `main`
9. Production deployment
10. Smoke test
11. Release notes
12. Rollback if severity-1 issue appears

## 3. Versioning

Before first formal release, use `0.x.y`.

After stable public release:

- MAJOR: incompatible data, API, or behavior change
- MINOR: backward-compatible feature
- PATCH: backward-compatible correction

Released versions are immutable. A correction receives a new version.

## 4. Rollback requirements

Every release must identify:

- Prior known-good deployment
- Migration rollback or forward-fix strategy
- Backup availability
- Smoke-test checklist
- Person authorized to roll back

## 5. Release blockers

- Severity 1 or unresolved Severity 2 defect
- Failed migration
- Failed RLS test
- Missing official-source traceability for new public schedules
- Unapproved scope or architecture change
- Unresolved accessibility barrier in a core flow
- Production secrets found in client code
- No rollback path

---

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

---

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

---

# ChatGPT Operating Rules

When helping with Sacred Near Me:

1. Treat this repository pack as the source of truth.
2. Do not restart planning from scratch when an approved artifact already exists.
3. Compare every recommendation against the active phase and exit gate.
4. Distinguish:
   - researched fact,
   - recommendation,
   - approved decision,
   - implemented behavior.
5. Use official parish, archdiocesan, standards-body, and vendor documentation for current facts.
6. Do not mark a schedule verified without a current official or direct source.
7. Do not propose broad UI work before the data and recurrence foundations are ready.
8. Keep one clearly recommended next action.
9. Update or propose updates to:
   - Current Phase
   - ADRs
   - Risk Register
   - Work item
   when a decision changes.
10. When reviewing Codex output, check:
    - scope alignment,
    - phase alignment,
    - acceptance criteria,
    - tests,
    - migrations,
    - security,
    - privacy,
    - accessibility,
    - source traceability.
11. Prefer partial verified progress over speculative completeness.
12. Do not confuse a chat agreement with a repository-recorded decision; recommend recording it.

---

# Standards and Official References

These sources informed the governance baseline. They are not substitutes for project-specific decisions.

## Secure development

- NIST SP 800-218, Secure Software Development Framework  
  https://csrc.nist.gov/pubs/sp/800/218/final
- NIST SSDF project  
  https://csrc.nist.gov/projects/ssdf
- OWASP Application Security Verification Standard  
  https://owasp.org/www-project-application-security-verification-standard/
- OWASP Top 10  
  https://owasp.org/www-project-top-ten/

## Accessibility

- W3C Web Content Accessibility Guidelines 2.2  
  https://www.w3.org/TR/WCAG22/
- W3C WCAG 2.2 Quick Reference  
  https://www.w3.org/WAI/WCAG22/quickref/

## Recurring schedules

- RFC 5545, Internet Calendaring and Scheduling Core Object Specification  
  https://www.rfc-editor.org/info/rfc5545/

## Repository governance

- GitHub protected branches  
  https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule
- GitHub issue and pull-request templates  
  https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates
- GitHub CODEOWNERS  
  https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners

## Application and platform operations

- Next.js testing guidance  
  https://nextjs.org/docs/app/guides/testing
- Supabase production checklist  
  https://supabase.com/docs/guides/deployment/going-into-prod
- Supabase Row Level Security  
  https://supabase.com/docs/guides/database/postgres/row-level-security
- Supabase backups  
  https://supabase.com/docs/guides/platform/backups
- Vercel environments  
  https://vercel.com/docs/deployments/environments
- Vercel deployment protection  
  https://vercel.com/docs/deployment-protection

## Versioning

- Semantic Versioning 2.0.0  
  https://semver.org/
