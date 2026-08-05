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
