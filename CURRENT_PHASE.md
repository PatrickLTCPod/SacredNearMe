# Current Phase

**Active phase:** Phase 1 — Church inventory and source map  
**Status:** In progress  
**Last updated:** August 20, 2026
**Release target:** None approved yet

## Current objective

Build a complete, deduplicated, source-backed inventory of in-scope Catholic worship locations and an official-source map before collecting event schedules.

## Phase transition

Phase 0 is complete. The approved Phase 1 work item is the controlling implementation artifact.

Phase 1 research and artifact creation may begin only through the approved work item. Event schedule collection, recurrence modeling, database work, and application development remain prohibited.

## Implementation status

PR #7 was authoritatively verified merged at `2dc4bd39fd481390df39cfeefc0c4677e90d08b0`, and local `main` was synchronized before the geographic-verification branch was created. The parish/family pass remains merged. An authoritative county and municipal government-geography pass reviewed all 30 canonical locations, CAND-AOC-009, all 41 controls, all candidate-to-area ambiguities, and all geography-related duplicate cases. The canonical county distribution is 12 Clermont and 18 Hamilton; all existing travel zones remain supported. Twenty-nine canonical rows are now `candidate`; St. Columban remains `needs_resolution` only for the Southeast Family 4 name and the operational distinction between the two Loveland controls. Government evidence resolved the Pierce, Union, Tate, Columbia Tusculum, Good Shepherd, All Saints, and Deer Park/Silverton questions. CAND-AOC-009 is verified in Warren County, unincorporated Deerfield Township, outside Loveland City and remains outside the CSV because neither approved travel zone applies without Product Owner boundary and controlled-field disposition. Catholic-source follow-up remains for destination existence/activity in Goshen, Washington Township, Monroe Township, Jackson Township, California, Mariemont, Terrace Park, Indian Hill, and Blue Ash, plus the Southeast Family 4 name. All 30 canonical rows still require an approved coordinate convention and entrance-level coordinate verification before final acceptance. Worship-schedule collection remains prohibited.

## Approved work now

- Implement `work-items/PHASE-1-CHURCH-INVENTORY-AND-SOURCE-MAP.md` on a dedicated task branch.
- Establish the geographic coverage checklist from the approved boundary.
- Create the approved Phase 1 artifact scaffolding.
- Research official sources only for location identity, relationships, contact details, active status, and future source mapping.
- Build the canonical church inventory and official-source map.
- Produce the field definitions, research workflow, coverage-gap report, and duplicate-resolution report.
- Record source gaps, conflicts, boundary ambiguities, and duplicate decisions without guessing.
- Submit the completed Phase 1 artifacts for Product Owner review before Phase 2 begins.

## Work not approved yet

- Event schedule collection, event-time extraction, or bulletin transcription
- Recurrence modeling, seasonal schedules, or Holy Day schedule work
- Database schemas, Supabase tables, seed data, or migrations
- Application code, Next.js initialization, or user-interface work
- Geolocation, ranking logic, or driving-time calculations
- Automated scraping or automated publication
- Continuous integration, deployment configuration, or production setup
- Phase 2 event modeling or later-phase implementation
- Public launch or native mobile applications
- Expansion beyond the approved geographic boundary

## Phase 0 exit criteria

All must be complete:

- [x] Governance pack committed
- [x] `AGENTS.md` located at repository root
- [x] Product Owner approves project name
- [x] Product Owner approves geographic boundary
- [x] Product Owner approves event taxonomy
- [x] Product Owner approves baseline stack or records an alternative ADR
- [x] GitHub repository created
- [x] Protected `main` configured
- [x] Pull-request template active
- [x] Issue templates active
- [x] Initial ADR approved
- [x] Phase 1 work item created with acceptance criteria

## Immediate next action

Product Owner decides whether CC-07 `Loveland vicinity` intentionally includes the St. Margaret of York campus in unincorporated Deerfield Township, Warren County. If included, approve the required scope/controlled-field change defining travel-zone treatment; if excluded, record that disposition. Do not collect worship schedules.
