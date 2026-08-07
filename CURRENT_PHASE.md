# Current Phase

**Active phase:** Phase 1 — Church inventory and source map  
**Status:** In progress  
**Last updated:** August 7, 2026  
**Release target:** None approved yet

## Current objective

Build a complete, deduplicated, source-backed inventory of in-scope Catholic worship locations and an official-source map before collecting event schedules.

## Phase transition

Phase 0 is complete. The approved Phase 1 work item is the controlling implementation artifact.

Phase 1 research and artifact creation may begin only through the approved work item. Event schedule collection, recurrence modeling, database work, and application development remain prohibited.

## Implementation status

The first Archdiocese-only official-source discovery pass for all 41 approved areas was completed on task branch `phase-1/aoc-directory-discovery` on August 7, 2026 and awaits Product Owner review. Twenty official Archdiocese source records and 31 candidate physical destinations were recorded; 32 area controls have at least one candidate and nine have no directly attributable candidate from this pass. The canonical inventory remains header-only because required travel-zone and status/type semantics are unresolved. Current official parish and family-of-parishes website verification remains, and worship-schedule collection remains prohibited.

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

Obtain Product Owner decisions on the required inventory-field semantics identified by the Archdiocese discovery pass, then verify the candidates and no-candidate gaps through current official parish and family-of-parishes websites. Record location identities and source evidence only. Do not collect worship schedules.
