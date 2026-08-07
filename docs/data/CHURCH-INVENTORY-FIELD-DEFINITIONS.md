# Church Inventory Field Definitions

**Document status:** In progress — canonical controlled-field semantics approved; unrelated definitions remain open

## Purpose

This document defines the approved fields and governing constraints for the canonical Phase 1 church inventory. It does not authorize schedule collection or application development.

## Governing rules

- One physical worship destination receives one canonical record.
- A parish organization and a physical church are not automatically the same entity.
- Blank values remain blank rather than being guessed.
- Every stable identifier must refer to only one physical destination.
- Active locations require an official name and normalized physical address.
- Coordinates must be source-backed or geocoded, manually checked, and checked against the approved region before acceptance.
- Every location requires an approved travel zone.
- Accessibility and entrance notes may be recorded only when officially verified.
- Inactive, merged, renamed, and multi-campus locations must remain distinguishable.
- The inventory must not contain worship schedules or event times.

## Field-definition table

| Field | Requiredness | Definition | Permitted values or format | Verification/source rule | Notes |
|---|---|---|---|---|---|
| `church_id` | Required | Stable, unique, non-semantic identifier for one physical worship destination. | Canonical lowercase UUID version 4 text | Generate once when a research candidate first enters the canonical inventory; confirm UUIDv4 format, uniqueness, and one-to-one use. | Must not encode name, address, ZIP, geography, parish, or ranking and must not be regenerated because the destination changes name, parish relationship, or research status. |
| `official_name` | Required for active locations | Official name of the physical worship destination. | TBD during Phase 1 implementation | Verify using an official source. | Leave blank rather than guessing while unresolved. |
| `parish_name` | TBD during Phase 1 implementation | Name of the associated parish organization, kept distinct from the physical destination. | TBD during Phase 1 implementation | Verify using an official source. | Do not conflate parish and church identities. |
| `parish_family_name` | TBD during Phase 1 implementation | Name of the associated family of parishes. | TBD during Phase 1 implementation | Verify using an official source. | Relationship conventions remain to be completed. |
| `location_type` | Required | Classification of the physical worship destination, distinct from canonical parish status, Family-of-Parishes status, research status, and event type. | `church`; `oratory`; `chapel`; `other_public_worship_location` | Assign only when current official evidence supports the physical-destination type. | A distinct adoration chapel may use `chapel` only when it is a distinct physical destination under the approved scope. Do not create an `adoration_chapel` value. |
| `active_status` | Required | Current active or inactive status of the physical worship destination. | `active`; `inactive` | Use `active` only when current official evidence supports that the physical destination remains current; use `inactive` only when current official evidence establishes closure or inactivity. | Merged, renamed, conflicting, under-review, canonically unified, and Family-of-Parishes restructuring conditions belong in relationship evidence, notes, duplicate-resolution records, historical context, or `research_status`. |
| `street_address` | Required for active locations | Normalized street address of the physical worship destination. | TBD during Phase 1 implementation | Verify against official evidence; do not substitute an office address without evidence that it is the worship destination. | Normalization rules remain to be completed. |
| `city` | Required for active locations | City component of the normalized physical address. | TBD during Phase 1 implementation | Verify as part of the physical address. | Do not infer geographic coverage from mailing city alone. |
| `state` | Required for active locations | State component of the normalized physical address. | TBD during Phase 1 implementation | Verify as part of the physical address. | Format remains to be completed. |
| `zip_code` | Required for active locations | ZIP code component of the normalized physical address. | TBD during Phase 1 implementation | Verify as part of the physical address. | Format and validation rules remain to be completed. |
| `latitude` | Required for active locations before inventory acceptance | Latitude of the physical worship destination. | TBD during Phase 1 implementation | Must be source-backed or geocoded, manually checked, and checked against the approved region. | Coordinate tolerance and precision remain to be completed. |
| `longitude` | Required for active locations before inventory acceptance | Longitude of the physical worship destination. | TBD during Phase 1 implementation | Must be source-backed or geocoded, manually checked, and checked against the approved region. | Coordinate tolerance and precision remain to be completed. |
| `phone` | TBD during Phase 1 implementation | Official public contact telephone number associated with the location or responsible parish. | TBD during Phase 1 implementation | Record only public, official contact information. | Leave blank when not officially verified. |
| `official_website` | TBD during Phase 1 implementation | Official public website associated with the location or responsible parish. | TBD during Phase 1 implementation | Verify publisher and authority using the approved source hierarchy. | Exact source records belong in the official-source map. |
| `travel_zone` | Required | Physical destination's primary operating zone. | `clermont_county`; `cincinnati_east_side` | Assign `clermont_county` to an approved Clermont County destination and `cincinnati_east_side` to an approved Cincinnati East Side destination. Escalate a boundary location that cannot be assigned without interpreting the approved boundary. | Does not represent every geographic checklist area served by, overlapping with, or related to the destination. |
| `county` | TBD during Phase 1 implementation | County associated with the physical destination. | TBD during Phase 1 implementation | Verify from reliable location evidence. | Requiredness and format remain to be completed. |
| `accessibility_notes` | TBD during Phase 1 implementation | Public accessibility information about the physical destination. | TBD during Phase 1 implementation | Include only officially verified information. | Leave blank when not officially verified. |
| `entrance_notes` | TBD during Phase 1 implementation | Public entrance information needed to identify access to the physical destination. | TBD during Phase 1 implementation | Include only officially verified information. | Leave blank when not officially verified. |
| `primary_source_id` | TBD during Phase 1 implementation | Identifier of the primary source record supporting the location. | TBD during Phase 1 implementation | Must refer to a source recorded in the official-source map when populated. | Source gaps must be documented rather than filled by inference. |
| `last_verified_date` | TBD during Phase 1 implementation | Date of the most recent verification of the inventory record. | TBD during Phase 1 implementation | Derive from a documented verification activity and source access record. | Date format remains to be completed. |
| `research_status` | Required | Current Phase 1 research lifecycle state of the inventory record. | `candidate`; `in_review`; `needs_resolution`; `ready_for_approval`; `approved`; `needs_reverification` | Update only when supported by documented research progress and the lifecycle definitions below. | First-entry records in the current pass may use only `candidate`, `in_review`, or `needs_resolution`. Product Owner review is required before `approved`. |
| `notes` | TBD during Phase 1 implementation | Concise record-specific context, unresolved issue, or evidence limitation. | TBD during Phase 1 implementation | Preserve uncertainty and conflicts; do not guess missing facts. | Must not contain worship schedules or unnecessary personal information. |

## Permitted values

### Location type

- `church` — current official evidence identifies the physical worship destination as a church.
- `oratory` — current official evidence identifies the physical worship destination as an oratory.
- `chapel` — current official evidence identifies the physical worship destination as a chapel.
- `other_public_worship_location` — the destination is clearly an approved public sacred destination, but none of the first three categories fits.

`location_type` describes the physical worship destination. It does not describe canonical parish status, Family-of-Parishes status, research status, or event type. Do not infer `chapel` merely because a destination hosts adoration, and do not create an `adoration_chapel` value.

### Active status

- `active` — current official evidence supports that the physical worship destination remains current.
- `inactive` — current official evidence establishes that the physical worship destination is closed or inactive.

Do not use this field for merged, renamed, conflicting, under-review, canonically unified, or Family-of-Parishes restructuring conditions. If activity is materially unclear, keep the research candidate outside the canonical inventory unless enough information otherwise supports canonical representation with `research_status` set to `needs_resolution`.

### Research status

- `candidate` — location has enough evidence to be represented canonically, but substantive Phase 1 verification remains.
- `in_review` — active verification is underway.
- `needs_resolution` — a material identity, boundary, source, relationship, or evidence conflict prevents advancement.
- `ready_for_approval` — Phase 1 research requirements for the record appear complete and it is awaiting Product Owner review.
- `approved` — Product Owner has accepted the record as part of the canonical inventory.
- `needs_reverification` — a previously established record requires renewed verification because evidence has aged, changed, disappeared, or conflicted.

Do not invent additional statuses without Product Owner approval. During the current verification pass, a newly entered canonical row may use only `candidate`, `in_review`, or `needs_resolution`. Do not use `approved` without explicit Product Owner review.

### Travel zone

- `clermont_county` — the physical destination's primary operating zone is the approved Clermont County zone.
- `cincinnati_east_side` — the physical destination's primary operating zone is the approved Cincinnati East Side zone.

Coverage relationships do not create additional travel-zone values. Escalate rather than guess when a boundary location cannot be assigned without interpreting the approved boundary.

## Candidate-stage nullability and canonical-entry rule

- Incomplete research candidates may remain in research artifacts with unresolved values.
- A research-only candidate must remain outside `data/churches/church-inventory.csv` until `travel_zone`, `location_type`, `active_status`, and `research_status` can all be assigned.
- Satisfying those four fields is necessary but not sufficient for canonical entry. All other requiredness and evidence rules in this document, governance, and the approved work item remain in force.
- Optional or unsupported values remain blank rather than being guessed.
- Coordinates remain required before final inventory acceptance. Missing final coordinates do not automatically prohibit an otherwise eligible `candidate`, `in_review`, or `needs_resolution` row, but such a row cannot become `ready_for_approval` or `approved` until coordinate requirements are satisfied.

## Stable identifier implementation rule

UUID version 4 is the approved Level 1 implementation choice for canonical `church_id` values.

- Store each identifier as canonical lowercase UUID text.
- Generate the UUID once when the physical destination first enters the canonical CSV.
- Do not assign a UUID to a research-only candidate that remains outside the CSV.
- The identifier must not encode church name, address, ZIP code, geography, parish name, or sequence ranking.
- Do not regenerate an identifier because the church changes name, parish relationship, Family-of-Parishes relationship, or research status.

## Naming and normalization rules

- Use an officially supported name for each physical destination.
- Keep organization names and physical-destination names in their separate fields.
- Leave unresolved values blank rather than guessing.
- Naming conventions, alternate-name handling, address formatting, abbreviations, and normalization standards are TBD during Phase 1 implementation.

## Coordinate-quality rules

- Coordinates must identify the physical worship destination rather than an unrelated office or mailing location.
- Coordinates must be source-backed or geocoded and manually checked before acceptance.
- Coordinates must be checked against the approved geographic region.
- Precision, format, tolerance, and geocoding-quality standards are TBD during Phase 1 implementation.

## Relationship-modeling rules

- A parish organization and a physical church are not automatically the same entity.
- One physical destination receives one canonical record.
- Parish, church, chapel, campus, and family-of-parishes relationships must be represented without conflation.
- A distinct adoration chapel may be a separate destination when it represents a distinct physical destination under the approved scope.
- Treatment of shared campuses, renamed entities, merged entities, and multi-campus relationships is TBD during Phase 1 implementation and must be supported by evidence.

## Open decisions and Product Owner escalations

- Approve detailed naming and address-normalization conventions.
- Approve coordinate formats, precision, and acceptance tolerances.
- Resolve boundary, duplicate, shared-campus, or relationship cases that cannot be determined from authoritative evidence.

## Completion checklist

- [ ] Every field definition is complete and consistent with the approved work item.
- [ ] Requiredness is resolved for every field.
- [ ] Permitted values and formats are approved.
- [ ] Naming and address-normalization rules are approved.
- [ ] Coordinate-quality rules are approved.
- [ ] Relationship-modeling rules cover inactive, merged, renamed, and shared-campus cases.
- [x] Open Product Owner decisions are resolved or explicitly recorded.
