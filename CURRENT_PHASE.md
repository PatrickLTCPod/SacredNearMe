# Current Phase

**Active phase:** Phase 0 — Governance and repository foundation  
**Status:** In progress  
**Last updated:** August 5, 2026  
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

- [x] Governance pack committed
- [x] `AGENTS.md` located at repository root
- [x] Product Owner approves project name
- [x] Product Owner approves geographic boundary
- [x] Product Owner approves event taxonomy
- [x] Product Owner approves baseline stack or records an alternative ADR
- [x] GitHub repository created
- [ ] Protected `main` configured
- [x] Pull-request template active
- [x] Issue templates active
- [ ] Initial ADR approved
- [ ] Phase 1 work item created with acceptance criteria

## Immediate next action

Complete the approved public-readiness work item by publishing the remediated repository, immediately protecting `main`, and opening the review pull request. Do not begin application code.
