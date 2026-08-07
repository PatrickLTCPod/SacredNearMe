# Church Inventory Field Definitions

**Document status:** Scaffold — definitions not yet complete

## Purpose

This document defines the approved fields and governing constraints for the canonical Phase 1 church inventory. It is a scaffold for completing definitions during Phase 1 implementation and does not authorize church research, schedule collection, or application development.

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
| `church_id` | Required | Stable, unique, non-semantic identifier for one physical worship destination. | TBD during Phase 1 implementation | Confirm uniqueness and one-to-one use within the canonical inventory. | Must not be casually reassigned after approval. |
| `official_name` | Required for active locations | Official name of the physical worship destination. | TBD during Phase 1 implementation | Verify using an official source. | Leave blank rather than guessing while unresolved. |
| `parish_name` | TBD during Phase 1 implementation | Name of the associated parish organization, kept distinct from the physical destination. | TBD during Phase 1 implementation | Verify using an official source. | Do not conflate parish and church identities. |
| `parish_family_name` | TBD during Phase 1 implementation | Name of the associated family of parishes. | TBD during Phase 1 implementation | Verify using an official source. | Relationship conventions remain to be completed. |
| `location_type` | TBD during Phase 1 implementation | Classification of the physical worship destination. | TBD during Phase 1 implementation | Support the classification with official evidence. | Permitted values require completion. |
| `active_status` | TBD during Phase 1 implementation | Current active or inactive classification of the physical destination. | TBD during Phase 1 implementation | Record evidence supporting the classification. | Closed, merged, renamed, and inactive locations must be distinguished from active destinations. |
| `street_address` | Required for active locations | Normalized street address of the physical worship destination. | TBD during Phase 1 implementation | Verify against official evidence; do not substitute an office address without evidence that it is the worship destination. | Normalization rules remain to be completed. |
| `city` | Required for active locations | City component of the normalized physical address. | TBD during Phase 1 implementation | Verify as part of the physical address. | Do not infer geographic coverage from mailing city alone. |
| `state` | Required for active locations | State component of the normalized physical address. | TBD during Phase 1 implementation | Verify as part of the physical address. | Format remains to be completed. |
| `zip_code` | Required for active locations | ZIP code component of the normalized physical address. | TBD during Phase 1 implementation | Verify as part of the physical address. | Format and validation rules remain to be completed. |
| `latitude` | Required for active locations before inventory acceptance | Latitude of the physical worship destination. | TBD during Phase 1 implementation | Must be source-backed or geocoded, manually checked, and checked against the approved region. | Coordinate tolerance and precision remain to be completed. |
| `longitude` | Required for active locations before inventory acceptance | Longitude of the physical worship destination. | TBD during Phase 1 implementation | Must be source-backed or geocoded, manually checked, and checked against the approved region. | Coordinate tolerance and precision remain to be completed. |
| `phone` | TBD during Phase 1 implementation | Official public contact telephone number associated with the location or responsible parish. | TBD during Phase 1 implementation | Record only public, official contact information. | Leave blank when not officially verified. |
| `official_website` | TBD during Phase 1 implementation | Official public website associated with the location or responsible parish. | TBD during Phase 1 implementation | Verify publisher and authority using the approved source hierarchy. | Exact source records belong in the official-source map. |
| `travel_zone` | Required | Approved travel-zone classification for the location. | TBD during Phase 1 implementation | Validate against the travel-zone rules once approved. | Permitted values remain to be completed. |
| `county` | TBD during Phase 1 implementation | County associated with the physical destination. | TBD during Phase 1 implementation | Verify from reliable location evidence. | Requiredness and format remain to be completed. |
| `accessibility_notes` | TBD during Phase 1 implementation | Public accessibility information about the physical destination. | TBD during Phase 1 implementation | Include only officially verified information. | Leave blank when not officially verified. |
| `entrance_notes` | TBD during Phase 1 implementation | Public entrance information needed to identify access to the physical destination. | TBD during Phase 1 implementation | Include only officially verified information. | Leave blank when not officially verified. |
| `primary_source_id` | TBD during Phase 1 implementation | Identifier of the primary source record supporting the location. | TBD during Phase 1 implementation | Must refer to a source recorded in the official-source map when populated. | Source gaps must be documented rather than filled by inference. |
| `last_verified_date` | TBD during Phase 1 implementation | Date of the most recent verification of the inventory record. | TBD during Phase 1 implementation | Derive from a documented verification activity and source access record. | Date format remains to be completed. |
| `research_status` | TBD during Phase 1 implementation | Current Phase 1 research state of the inventory record. | TBD during Phase 1 implementation | Update only when supported by documented research progress. | Permitted values remain to be completed. |
| `notes` | TBD during Phase 1 implementation | Concise record-specific context, unresolved issue, or evidence limitation. | TBD during Phase 1 implementation | Preserve uncertainty and conflicts; do not guess missing facts. | Must not contain worship schedules or unnecessary personal information. |

## Permitted values

### Location type

TBD during Phase 1 implementation.

### Active status

TBD during Phase 1 implementation.

### Research status

TBD during Phase 1 implementation.

### Travel zone

TBD during Phase 1 implementation.

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

- Approve permitted values for location type, active status, research status, and travel zone.
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
- [ ] Open Product Owner decisions are resolved or explicitly recorded.
