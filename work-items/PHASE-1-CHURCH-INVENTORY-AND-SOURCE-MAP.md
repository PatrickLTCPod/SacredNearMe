# Work Item: Phase 1 Church Inventory and Official-Source Map

**ID:** PHASE-1-CHURCH-INVENTORY-AND-SOURCE-MAP  
**Phase:** Phase 1 — Church inventory and source map  
**Type:** Data  
**Decision class:** C — Architecture, data, privacy, or security  
**Priority:** High  
**Owner:** Patrick  
**Product Owner:** Patrick  
**Status:** Approved  
**Proposed date:** August 5, 2026  
**Approval date:** August 5, 2026  
**Implementation status:** Not started  
**Implementation branch:** Not yet created  

## Problem

Sacred Near Me cannot collect or model worship schedules reliably until the project has a complete, deduplicated, source-backed inventory of Catholic churches and other approved public worship locations within the established geographic boundary.

Parish names, church names, family-of-parishes relationships, mailing addresses, campus locations, and official websites may differ across sources. Beginning schedule research before resolving the church universe would create duplicates, omissions, weak source traceability, and avoidable rework.

## User value

A canonical inventory gives every later event, recurrence rule, source record, verification record, direction link, and church detail page a stable location identity.

Completing this phase first supports:

- Accurate geographic coverage
- Reliable source traceability
- Duplicate prevention
- Consistent church naming
- Future schedule maintenance without code changes
- Clear identification of research gaps
- A defensible boundary for Phase 2 event modeling

## In scope

### Governing boundary

The later implementation must use the already approved geographic boundary in `SCOPE_AND_PRODUCT_RULES.md`. It must not redefine or expand that boundary.

The inventory should include Catholic locations within the approved area that are relevant to the approved sacred-event scope:

- Active parish churches
- Additional churches within a parish or family of parishes
- Public Catholic chapels with recurring public worship opportunities
- Adoration chapels when they represent a distinct physical destination
- Other Catholic worship locations only when they regularly host approved public sacred events and have an official source

Do not automatically include:

- Parish offices without a worship location
- Schools without independently scheduled public worship
- Cemeteries
- Retreat centers requiring registration
- Private chapels
- Convents or religious houses not normally open to the public
- Non-Catholic churches
- Closed or merged churches as active destinations

Closed, merged, renamed, or inactive locations may be recorded when needed for duplicate resolution or historical clarity, but they must be clearly marked inactive.

## Required deliverables

### 1. Canonical church inventory

Create a machine-readable inventory with one row or record per physical worship destination.

**Proposed artifact:** `data/churches/church-inventory.csv`

The inventory must include at least these fields:

- `church_id`
- `official_name`
- `parish_name`
- `parish_family_name`
- `location_type`
- `active_status`
- `street_address`
- `city`
- `state`
- `zip_code`
- `latitude`
- `longitude`
- `phone`
- `official_website`
- `travel_zone`
- `county`
- `accessibility_notes`
- `entrance_notes`
- `primary_source_id`
- `last_verified_date`
- `research_status`
- `notes`

Inventory rules:

- `church_id` is stable, unique, and non-semantic.
- One physical destination receives one canonical record.
- A parish organization and a physical church are not automatically the same entity.
- Blank values remain blank rather than being guessed.
- Accessibility and entrance notes are included only when officially verified.
- Coordinates must be source-backed or geocoded and manually checked before acceptance.

### 2. Field-definition document

**Proposed artifact:** `docs/data/CHURCH-INVENTORY-FIELD-DEFINITIONS.md`

It must define:

- Every inventory field
- Required versus optional fields
- Permitted status values
- Location-type values
- Travel-zone values
- Naming rules
- Address-normalization rules
- Coordinate-quality rules
- Treatment of inactive, merged, renamed, and multi-campus locations
- Treatment of parish-family relationships
- Treatment of a church and an adoration chapel sharing one campus

### 3. Official-source research workflow

**Proposed artifact:** `docs/data/OFFICIAL-SOURCE-RESEARCH-WORKFLOW.md`

The workflow must use the source hierarchy in `DATA_GOVERNANCE.md` and require researchers to:

1. Begin with official parish, family-of-parishes, or archdiocesan sources.
2. Record the exact source URL and publisher.
3. Record the date the source was accessed.
4. Distinguish authoritative evidence from a research lead.
5. Preserve conflicting official information rather than silently choosing one version.
6. Record direct parish-office confirmation when used.
7. Avoid treating secondary directories as final authority.
8. Document missing information rather than inferring it.
9. Avoid collecting worship schedules during this phase except when a page URL is recorded as a future schedule source.
10. Record evidence supporting active or inactive status.

### 4. Official-source map

**Proposed artifact:** `docs/data/OFFICIAL-SOURCE-MAP.md`

For every canonical church record, the source map must identify applicable official sources, including when available:

- Parish home page
- Parish-family page
- Official church or campus page
- Archdiocese directory entry
- Official sacrament or worship page
- Official calendar
- Official bulletin location
- Official contact page
- Official social account only when needed
- Direct-confirmation record

Each source entry must include:

- `source_id`
- `church_id`
- Source type
- Publisher
- URL or confirmation method
- Access date
- Authority level
- Intended future use
- Current availability
- Notes or conflicts

Recording a worship, bulletin, or calendar URL does not authorize schedule extraction during Phase 1.

### 5. Coverage-gap report

**Proposed artifact:** `docs/data/COVERAGE-GAP-REPORT.md`

It must identify:

- Every approved geographic area reviewed
- Areas with confirmed Catholic worship locations
- Areas with no confirmed location
- Locations with missing official sources
- Locations with incomplete contact or address data
- Locations requiring direct confirmation
- Boundary ambiguities requiring Product Owner review
- Any reason the inventory cannot yet be considered complete

### 6. Duplicate-resolution report

**Proposed artifact:** `docs/data/DUPLICATE-RESOLUTION-REPORT.md`

It must document:

- Potential duplicates reviewed
- Alternate names
- Parish-versus-church distinctions
- Merged or renamed entities
- Shared-campus relationships
- Conflicting addresses
- Resolution decision
- Evidence supporting the decision
- Any unresolved duplicate requiring Product Owner review

## Required research order

Later implementation must proceed in this order:

1. Establish the list of approved municipalities, neighborhoods, and townships from the governance boundary.
2. Locate official Archdiocese of Cincinnati directory records covering those areas.
3. Locate official parish and family-of-parishes sources.
4. Create candidate physical worship locations.
5. Normalize names and addresses.
6. Resolve parish, church, chapel, and campus relationships.
7. Identify possible duplicates and inactive locations.
8. Verify official contact and website information.
9. Validate coordinates and travel zones.
10. Build the official-source map.
11. Produce coverage-gap and duplicate-resolution reports.
12. Submit the completed inventory for Product Owner approval.

Do not begin event schedule collection before the inventory is approved.

## Explicit non-goals

- Mass, confession, adoration, or devotion schedule collection
- Event-time extraction
- Bulletin transcription
- Recurrence rules
- Seasonal or Holy Day schedules
- Database schema implementation
- Supabase tables
- Data migrations
- Application code
- User interface work
- Maps embedded in the application
- Geolocation
- Ranking logic
- Driving-time calculations
- Administrative interfaces
- Automated scraping
- Automated publication
- Public launch
- Expansion beyond the approved geographic boundary
- Non-Catholic worship locations
- General parish social events
- Native mobile applications

## Acceptance criteria

- [ ] A canonical machine-readable church inventory exists.
- [ ] Every record has a stable, unique `church_id`.
- [ ] Every approved geographic area has been explicitly reviewed.
- [ ] Every known in-scope Catholic worship location has been included or documented as a research gap.
- [ ] Every active location has an official name and normalized physical address.
- [ ] Every active location has coordinates that were checked against the approved region.
- [ ] Every location has an approved travel zone.
- [ ] Parish, church, chapel, campus, and family-of-parishes relationships are represented without conflation.
- [ ] No known duplicate remains unresolved without being listed in the duplicate-resolution report.
- [ ] Every active location has at least one official source or a documented source gap.
- [ ] Every source has a source ID, publisher, type, URL or confirmation method, and access date.
- [ ] Secondary sources are used only as research leads unless the governance rules explicitly permit otherwise.
- [ ] Conflicting official information is preserved and documented.
- [ ] Closed, merged, renamed, and inactive locations are clearly distinguished from active destinations.
- [ ] Field definitions and permitted values are documented.
- [ ] Coverage gaps are documented by geographic area.
- [ ] Duplicate-resolution decisions include supporting evidence.
- [ ] Accessibility and entrance notes contain only verified information.
- [ ] No worship schedules or event times are entered into the canonical inventory.
- [ ] No application code, dependencies, database schema, workflows, migrations, or deployment configuration are created.
- [ ] The completed inventory is reviewed and approved by the Product Owner before Phase 2 begins.
- [ ] No event schedule work depends on a church missing from the approved inventory.
- [ ] All created artifacts are version-controlled through a task branch and pull request.
- [ ] Required validation and a completion report are produced.
- [ ] The working tree is clean after implementation.

## Expected areas affected

- Code: None
- Database: None; no schema or migration work
- Documentation: field definitions, research workflow, official-source map, coverage-gap report, duplicate-resolution report, and completion documentation
- Data: `data/churches/church-inventory.csv`
- UI: None

## Required tests

- Unit: Not applicable; no application code is in scope
- Integration: Validate referential consistency between the inventory and official-source map
- E2E: Not applicable; no application behavior is in scope
- Manual: Review naming, addresses, relationships, boundary coverage, duplicates, official-source authority, coordinates, travel zones, and active/inactive classifications
- Accessibility: Verify that accessibility and entrance notes contain only officially verified information; no interface accessibility test is applicable

## Required validation approach

Later validation must include:

- Unique-ID check
- Duplicate-name and duplicate-address check
- Missing required-field report
- Invalid state or ZIP check
- Coordinate-boundary check
- Official-source presence check
- Broken-link check for recorded web sources
- Source access-date check
- Travel-zone validation
- Active/inactive consistency check
- Parish-family relationship review
- Inventory-to-source-map referential check
- Coverage checklist against every approved geographic area
- Secret and private-data scan
- Confirmation that no schedules or application artifacts were introduced

Validation results must be preserved in the completion report or a dedicated validation artifact.

## Security and privacy impact

Research must use public official sources and collect only information necessary to identify public worship destinations. Do not collect unnecessary personal information, private contact details, precise user location, credentials, or production data. Accessibility and entrance notes may be recorded only when officially verified. No authentication or access-control change is in scope.

## Data and migration impact

Phase 1 creates version-controlled research artifacts, including a CSV inventory, but no application database, schema, seed data, migration, or production-data change.

## Dependencies

- Approved geographic boundary
- Approved event inclusion rules
- Accepted ADR-001
- Accepted ADR-002
- Protected `main`
- Active source hierarchy in `DATA_GOVERNANCE.md`
- Product Owner availability for boundary and duplicate decisions

## Risks

- A church may be omitted because its mailing city differs from its physical municipality.
- Parish and church names may be conflated.
- Family-of-parishes websites may obscure individual church locations.
- Closed, merged, or renamed churches may appear active in older sources.
- Secondary directories may contain stale addresses or names.
- A shared campus may be duplicated as multiple destinations.
- A distinct adoration chapel may be incorrectly collapsed into the church record.
- Coordinates may point to a parish office rather than the worship entrance.
- Geographic boundary interpretation may drift.
- Schedule research may begin prematurely.
- The inventory may appear complete while official-source gaps remain.
- Personal or private information may be collected unnecessarily.
- The machine-readable inventory and human-readable reports may drift apart.

## Rollback or recovery

- Research artifacts can be reverted through Git.
- Incorrect records should be corrected through reviewed commits rather than history rewriting.
- Stable IDs should not be casually reassigned after approval.
- Removed or inactive locations should retain an audit trail.
- If a task branch includes schedule data or application code, close the pull request without merging and recreate the branch from current `main`.
- Do not delete evidence needed to explain duplicate or boundary decisions.
- No production data or application rollback is required because Phase 1 creates research artifacts only.

## Definition of Ready

Phase 1 implementation is Ready only when:

- The Product Owner approves this work item.
- Scope and acceptance criteria are unchanged or explicitly reapproved.
- Required artifact locations are confirmed.
- The researcher has web access to official sources.
- Any known boundary ambiguity has an identified escalation path.
- No conflicting Phase 0 work remains open.

## Definition of Done

Phase 1 is Done only when:

- All acceptance criteria pass.
- Every approved geographic area is accounted for.
- The inventory and source map are internally consistent.
- Coverage and duplicate reports are complete.
- Product Owner review is complete.
- The pull request is merged to protected `main`.
- The repository records the approved Phase 1 completion status.
- Phase 2 has not begun prematurely.

## Approval

**Product Owner approval:** Patrick  
**Date:** August 5, 2026
