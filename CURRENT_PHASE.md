# Current Phase

**Active phase:** Phase 1 — Church inventory and source map  
**Status:** In progress  
**Last updated:** August 24, 2026
**Release target:** None approved yet

## Current objective

Build a complete, deduplicated, source-backed inventory of in-scope Catholic worship locations and an official-source map before collecting event schedules.

## Phase transition

Phase 0 is complete. The approved Phase 1 work item is the controlling implementation artifact.

Phase 1 research and artifact creation may begin only through the approved work item. Event schedule collection, recurrence modeling, database work, and application development remain prohibited.

## Implementation status

PR #8 was authoritatively verified merged at `c7577bae07132d9e83d8348b90201e8b6646ca99`, and local `main` was synchronized before the direct-confirmation branch was created. The merged government-geography pass reviewed all 30 canonical locations, CAND-AOC-009, all 41 controls, all candidate-to-area ambiguities, and all geography-related duplicate cases. The Product Owner has clarified that CC-07 `Loveland vicinity` excludes unincorporated Deerfield Township, Warren County. CAND-AOC-009 remains a preserved research lead outside the canonical CSV and outside Version 1 scope; no current travel zone applies, and future Warren County inclusion requires an approved geographic scope change. The canonical county distribution remains 12 Clermont and 18 Hamilton, with all current travel zones supported. Twenty-nine canonical rows remain `candidate`; St. Columban remains `needs_resolution` only for the Southeast Family 4 name. The current Archdiocese directory, regional datasets, family-name registry, and relevant official parish/family sites were rechecked on August 24, 2026. Seven public-office emails were successfully sent for the nine no-candidate controls and the Southeast Family 4 name. No response had been received at this checkpoint, so all nine no-candidate outcomes remain `unable_to_confirm`, the family name remains unresolved, and no direct confirmation is claimed. All 30 canonical rows still require approved naming/address conventions, an approved coordinate convention, and entrance-level coordinate verification before final Product Owner inventory approval. Worship-schedule collection remains prohibited.

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

Monitor and record responses to the seven public-office direct-confirmation emails, preserving `unable_to_confirm` until an actual factual response is received. Do not collect worship schedules.
