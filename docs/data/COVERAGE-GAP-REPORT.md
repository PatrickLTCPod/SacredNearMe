# Coverage Gap Report

**Document status:** Archdiocese-only discovery pass completed — open gaps require later verification and Product Owner decisions

## Purpose

This report documents evidence-backed gaps that prevent the Phase 1 inventory from being considered complete after the first current Archdiocese-only discovery pass.

## Coverage summary

All 41 approved area controls received the same Archdiocese directory and relevant Archdiocese family-evidence review on 2026-08-07. Thirty-one unique candidate physical destinations were identified across 32 area controls. Nine area controls had no directly attributable candidate in the reviewed South and Southeast datasets. These are discovery results, not completeness claims.

## Geographic-area findings

- No directly attributable candidate was found for CC-08, CC-16, CC-17, CC-18, CES-04, CES-10, CES-11, CES-12, or CES-18.
- Candidate-to-area boundaries remain unverified for several township and Cincinnati-neighborhood controls.
- CC-07 `Loveland vicinity` and CES-23 `Loveland` remain distinct approved controls even though the same two physical candidates plausibly serve both.

## Missing-source findings

- Current official parish and family-of-parishes websites have not yet been reviewed; only official Archdiocese sources were in scope for this pass.
- The current family-name registry provides no selected name for Southeast Family 4.
- The live directory page's 205-parish statement conflicts with the 206 feature records in its six linked regional datasets.

## Incomplete-location-data findings

- No canonical rows were created because `travel_zone` is required but has no approved values, and the requiredness or permitted values of `location_type`, `active_status`, and `research_status` remain undecided.
- Coordinates exposed by the official directory were not copied into the header-only inventory while canonical candidate entry remained blocked.
- Several candidate-to-area associations require boundary evidence before they can support an accepted coverage claim.

## Direct-confirmation needs

No direct-confirmation request is justified yet. Current official parish and family-site verification must be attempted before escalation to direct confirmation.

## Boundary ambiguities

Boundary ambiguities are preserved in the findings table and geographic checklist. Street names, postal-city labels, and nearby locations were not treated as proof of municipal, township, or neighborhood boundaries.

## Conditions preventing completeness

Phase 1 cannot be considered complete until required field semantics are approved; current parish and family-site verification is performed; all area, address, coordinate, relationship, and duplicate questions are resolved or explicitly dispositioned; and the canonical inventory has accepted records and traceable sources. Worship schedule collection remains prohibited.

## Product Owner decisions required

The smallest decision needed before canonical candidate entry is approval of controlled values and requiredness for `travel_zone`, `location_type`, `active_status`, and `research_status`, including whether candidate-stage records may remain incomplete until acceptance. A later boundary decision may be needed for the two distinct Loveland controls if official boundary evidence does not resolve their intended coverage treatment.

## Findings table

| gap_id | coverage_id | approved_area_name | gap_type | description | evidence | required_action | decision_owner | status | notes |
|---|---|---|---|---|---|---|---|---|---|
| GAP-AOC-001 | All | All approved areas | Required field semantics | Required travel-zone values and status/type encodings are undefined, blocking canonical rows. | CHURCH-INVENTORY-FIELD-DEFINITIONS.md | Approve controlled values, requiredness, and candidate-stage nullability. | Product Owner | Open | No canonical church ID was assigned. |
| GAP-AOC-002 | All | All approved areas | Source coverage | Current official parish and family-of-parishes websites have not yet been reviewed. | SRC-AOC-20260807-001 through -016 | Perform the next official-source hierarchy pass without collecting schedule data. | Research implementation | Open | Archdiocese-only boundary was observed. |
| GAP-AOC-003 | All | Archdiocese context | Official count conflict | Directory narrative says 205 parishes; six current datasets total 206 feature records. | SRC-AOC-20260807-001; SRC-AOC-20260807-002; SRC-AOC-20260807-003; SRC-AOC-20260807-017; SRC-AOC-20260807-018; SRC-AOC-20260807-019; SRC-AOC-20260807-020 | Preserve discrepancy and reassess only if it affects a local candidate. | Research implementation | Open | Do not reconcile by altering local records. |
| GAP-AOC-004 | CC-07; CES-23 | Loveland vicinity; Loveland | Coverage overlap | The same two physical candidates plausibly serve both separately approved controls. | CAND-AOC-008; CAND-AOC-009 | Seek official boundary evidence; if still ambiguous, request Product Owner disposition. | Research implementation; Product Owner if unresolved | Open | Do not duplicate physical destinations. |
| GAP-AOC-005 | CC-03 | Eastgate/Union Township | Boundary ambiguity | St. Veronica's official address and label do not prove approved-area inclusion. | CAND-AOC-004; SRC-AOC-20260807-003 | Verify through a current official parish or family source. | Research implementation | Open | Road-name inference is insufficient. |
| GAP-AOC-006 | CC-06 | Miami Township | Boundary ambiguity | St. Elizabeth Ann Seton's Milford label does not prove township inclusion. | CAND-AOC-007; SRC-AOC-20260807-003 | Verify through current official boundary evidence. | Research implementation | Open |  |
| GAP-AOC-007 | CC-14 | Pierce Township | Boundary ambiguity | St. Bernadette's Amelia label does not prove township inclusion. | CAND-AOC-003; SRC-AOC-20260807-003 | Verify through current official boundary evidence. | Research implementation | Open |  |
| GAP-AOC-008 | CC-15 | Tate Township | Boundary ambiguity | St. Mary's Bethel label does not prove township inclusion. | CAND-AOC-012; SRC-AOC-20260807-003 | Verify through current official boundary evidence. | Research implementation | Open |  |
| GAP-AOC-009 | CES-16; CES-17; CES-19; CES-20 | South Family 6 candidate areas | Family configuration conflict | The current-linked 2022 family page and current 2026 appointment evidence do not present identical South Family 6 membership. | SRC-AOC-20260807-005; SRC-AOC-20260807-009 | Verify the current family composition through a current official family or parish source. | Research implementation | Open | Preserve the newer and older official evidence without silent reconciliation. |
| GAP-AOC-010 | CES-05 | Columbia Tusculum | Boundary ambiguity | St. Stephen's directory label is Cincinnati rather than the approved neighborhood. | CAND-AOC-022; SRC-AOC-20260807-002 | Verify through a current official parish or family source. | Research implementation | Open |  |
| GAP-AOC-011 | CES-06 | Mt. Lookout | Boundary ambiguity | Christ the King's directory label is Cincinnati rather than the approved neighborhood. | CAND-AOC-023; SRC-AOC-20260807-002 | Verify through a current official parish or family source. | Research implementation | Open |  |
| GAP-AOC-012 | CES-08 | Oakley | Boundary ambiguity | St. Cecilia's directory label is Cincinnati rather than the approved neighborhood. | CAND-AOC-025; SRC-AOC-20260807-002 | Verify through a current official parish or family source. | Research implementation | Open |  |
| GAP-AOC-013 | CES-09 | Madisonville | Relationship conflict | Directory and linked family page include St. Anthony in S9; current appointment evidence omits it. | CAND-AOC-026; SRC-AOC-20260807-002; SRC-AOC-20260807-005; SRC-AOC-20260807-011 | Verify the current family relationship through a newer official family or parish source. | Research implementation | Open | Preserve all official evidence. |
| GAP-AOC-014 | CES-14; CES-15; CES-16 | Kenwood; Montgomery; Blue Ash | Boundary ambiguity | All Saints may serve multiple approved areas, but the directory does not establish each association. | CAND-AOC-029; SRC-AOC-20260807-002 | Verify each association through current official evidence. | Research implementation | Open | One physical destination only. |
| GAP-AOC-015 | CES-15; CES-16 | Montgomery; Blue Ash | Boundary ambiguity | Good Shepherd may serve both controls, but the directory does not explicitly establish either approved-area association. | CAND-AOC-017; SRC-AOC-20260807-002 | Verify through current official evidence. | Research implementation | Open |  |
| GAP-AOC-016 | CES-21 | East Walnut Hills | Boundary ambiguity | St. Francis de Sales' directory label is Cincinnati rather than the approved neighborhood. | CAND-AOC-030; SRC-AOC-20260807-002 | Verify through a current official parish or family source. | Research implementation | Open |  |
| GAP-AOC-017 | CES-22 | Mt. Adams | Boundary ambiguity | Holy Cross/Immaculata's directory label is Cincinnati rather than the approved neighborhood. | CAND-AOC-031; SRC-AOC-20260807-002 | Verify through a current official parish or family source. | Research implementation | Open |  |
| GAP-AOC-018 | CC-07; CES-23 | Loveland vicinity; Loveland | Missing relationship name | Current family registry has no selected name for Southeast Family 4. | CAND-AOC-008; CAND-AOC-009; SRC-AOC-20260807-004; SRC-AOC-20260807-005 | Verify whether a current official family name exists; retain the family identifier meanwhile. | Research implementation | Open | Do not invent a name. |
| GAP-AOC-019 | CC-08 | Goshen | No candidate found | No directly attributable candidate was found in the reviewed directory datasets. | SRC-AOC-20260807-002; SRC-AOC-20260807-003 | Review current official parish and family sites and document a confirmed absence if appropriate. | Research implementation | Open |  |
| GAP-AOC-020 | CC-16 | Washington Township | No candidate found | No directly attributable candidate was found in the reviewed directory datasets. | SRC-AOC-20260807-002; SRC-AOC-20260807-003 | Continue with current official parish and family-site verification. | Research implementation | Open |  |
| GAP-AOC-021 | CC-17 | Monroe Township | No candidate found | No directly attributable candidate was found in the reviewed directory datasets. | SRC-AOC-20260807-002; SRC-AOC-20260807-003 | Continue with current official parish and family-site verification. | Research implementation | Open |  |
| GAP-AOC-022 | CC-18 | Jackson Township | No candidate found | No directly attributable candidate was found in the reviewed directory datasets. | SRC-AOC-20260807-002; SRC-AOC-20260807-003 | Continue with current official parish and family-site verification. | Research implementation | Open |  |
| GAP-AOC-023 | CES-04 | California | No candidate found | No directly attributable candidate was found; a street named California was not treated as neighborhood evidence. | SRC-AOC-20260807-002 | Continue with current official parish and family-site verification. | Research implementation | Open |  |
| GAP-AOC-024 | CES-10 | Mariemont | No candidate found | No directly attributable candidate was found in the reviewed directory datasets. | SRC-AOC-20260807-002 | Continue with current official parish and family-site verification. | Research implementation | Open |  |
| GAP-AOC-025 | CES-11 | Terrace Park | No candidate found | No directly attributable candidate was found in the reviewed directory datasets. | SRC-AOC-20260807-002 | Continue with current official parish and family-site verification. | Research implementation | Open |  |
| GAP-AOC-026 | CES-12 | Indian Hill | No candidate found | No directly attributable candidate was found; nearby candidates were not assigned without evidence. | SRC-AOC-20260807-002 | Continue with current official parish and family-site verification. | Research implementation | Open |  |
| GAP-AOC-027 | CES-18 | Silverton | No candidate found | No directly attributable candidate was found in the reviewed directory datasets. | SRC-AOC-20260807-002 | Continue with current official parish and family-site verification. | Research implementation | Open |  |

## Completion checklist

- [x] Every approved geographic area has a documented Archdiocese-pass review result.
- [x] Areas with candidates and areas with no candidate from this pass are distinguished.
- [x] Missing official sources found in this pass are documented.
- [x] Known incomplete coordinate and travel-zone conditions are documented.
- [x] Current direct-confirmation posture is documented.
- [x] Boundary ambiguities and completeness blockers found in this pass are documented.
- [x] Required Product Owner decisions are recorded as explicitly outstanding.
