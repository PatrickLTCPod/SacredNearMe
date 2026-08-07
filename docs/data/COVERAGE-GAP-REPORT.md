# Coverage Gap Report

**Document status:** Current parish/family verification checkpoint completed — open boundary, direct-contact, and coordinate gaps remain

## Purpose

This report documents evidence-backed gaps that prevent the Phase 1 inventory from being considered complete after the current Archdiocese and parish/family verification passes.

## Coverage summary

All 41 approved area controls received the Archdiocese pass and a current official parish/family-site pass on 2026-08-07. All 31 discovered physical-destination candidates received current official verification: 30 now have canonical research-stage rows and CAND-AOC-009 remains research-only because its required travel zone is unresolved. Nine area controls still have no directly attributable candidate. These are research results, not completeness claims.

## Geographic-area findings

- No directly attributable candidate was found for CC-08, CC-16, CC-17, CC-18, CES-04, CES-10, CES-11, CES-12, or CES-18 after the current official web pass. A no-result finding is not proof that no in-scope destination exists.
- Candidate-to-area boundaries remain unverified for several township and Cincinnati-neighborhood controls.
- CC-07 `Loveland vicinity` and CES-23 `Loveland` remain distinct approved controls even though the same two physical candidates plausibly serve both.

## Missing-source findings

- Current official parish and family-of-parishes websites were reviewed for all 31 candidates and the nine no-candidate controls.
- The current family-name registry provides no selected name for Southeast Family 4.
- The live directory page's 205-parish statement conflicts with the 206 feature records in its six linked regional datasets.

## Incomplete-location-data findings

- Thirty research-stage canonical rows were created after the four controlled-field semantics were approved. CAND-AOC-009 remains outside the CSV because its travel zone cannot be assigned without interpreting the approved Loveland controls.
- Coordinates remain blank for all 30 canonical rows pending source-backed geocoding and manual regional checks; no row is ready for approval.
- Several candidate-to-area associations require boundary evidence before they can support an accepted coverage claim.

## Direct-confirmation needs

The current official web pass did not resolve nine no-candidate controls, six candidate-to-area questions, or the Southeast Family 4 relationship name. The candidate-to-area questions are Pierce Township, Eastgate/Union Township, Tate Township, Columbia Tusculum, the Good Shepherd Montgomery/Blue Ash association, and the All Saints Kenwood/Montgomery/Blue Ash associations. Direct parish/family-office confirmation is now the next permitted source-hierarchy step. No direct confirmation has yet been obtained.

## Boundary ambiguities

Boundary ambiguities are preserved in the findings table and geographic checklist. Street names, postal-city labels, and nearby locations were not treated as proof of municipal, township, or neighborhood boundaries.

## Conditions preventing completeness

Phase 1 cannot be considered complete until the remaining travel-zone, area, coordinate, relationship, and duplicate questions are resolved or explicitly dispositioned; all in-scope destinations are accounted for; and the canonical inventory is reviewed and accepted by the Product Owner. Worship schedule collection remains prohibited.

## Product Owner decisions required

The four controlled-field semantics are approved. Product Owner disposition is still required if authoritative boundary evidence cannot determine CAND-AOC-009's primary travel zone or reconcile the separately approved `Loveland vicinity` and `Loveland` controls. Detailed naming/address normalization, coordinate precision/tolerance, and remaining relationship-modeling conventions also remain open in the field definitions.

## Findings table

| gap_id | coverage_id | approved_area_name | gap_type | description | evidence | required_action | decision_owner | status | notes |
|---|---|---|---|---|---|---|---|---|---|
| GAP-AOC-001 | All | All approved areas | Required field semantics | Required values, lifecycle meanings, and candidate-stage nullability are approved for `travel_zone`, `location_type`, `active_status`, and `research_status`. | CHURCH-INVENTORY-FIELD-DEFINITIONS.md | None for these four fields. | Product Owner | Closed | Thirty canonical research-stage rows were created. |
| GAP-AOC-002 | All | All approved areas | Source coverage | Current official parish and family-of-parishes websites were reviewed for all 31 candidates and nine no-candidate controls. | SRC-PARISH-20260807-001 through -037 | Continue only with documented direct-contact and boundary follow-up. | Research implementation | Closed for this web pass | Official web verification does not establish Phase 1 completeness. |
| GAP-AOC-003 | All | Archdiocese context | Official count conflict | Directory narrative says 205 parishes; six current datasets total 206 feature records. | SRC-AOC-20260807-001; SRC-AOC-20260807-002; SRC-AOC-20260807-003; SRC-AOC-20260807-017; SRC-AOC-20260807-018; SRC-AOC-20260807-019; SRC-AOC-20260807-020 | Preserve discrepancy and reassess only if it affects a local candidate. | Research implementation | Open | Do not reconcile by altering local records. |
| GAP-AOC-004 | CC-07; CES-23 | Loveland vicinity; Loveland | Coverage overlap | The same two physical candidates plausibly serve both separately approved controls. | CAND-AOC-008; CAND-AOC-009 | Seek official boundary evidence; if still ambiguous, request Product Owner disposition. | Research implementation; Product Owner if unresolved | Open | Do not duplicate physical destinations. |
| GAP-AOC-005 | CC-03 | Eastgate/Union Township | Boundary ambiguity | St. Veronica's current official address and county corroboration do not prove the specific approved-area relationship. | CAND-AOC-004; SRC-PARISH-20260807-004; SRC-OFFICIAL-20260807-033 | Seek direct parish/family-office confirmation. | Research implementation | Open; direct contact required | Road-name inference is insufficient. |
| GAP-AOC-006 | CC-06 | Miami Township | Boundary ambiguity | Current official family history identifies St. Elizabeth Ann Seton with Miami Township. | CAND-AOC-007; SRC-PARISH-20260807-034 | Retain the evidence trail and validate coordinates before final acceptance. | Research implementation | Closed for coverage identity |  |
| GAP-AOC-007 | CC-14 | Pierce Township | Boundary ambiguity | St. Bernadette's current Amelia address does not prove township inclusion. | CAND-AOC-003; SRC-PARISH-20260807-003 | Seek direct parish/family-office confirmation. | Research implementation | Open; direct contact required |  |
| GAP-AOC-008 | CC-15 | Tate Township | Boundary ambiguity | St. Mary's current Bethel address does not prove township inclusion. | CAND-AOC-012; SRC-PARISH-20260807-012 | Seek direct parish/family-office confirmation. | Research implementation | Open; direct contact required |  |
| GAP-AOC-009 | CES-16; CES-17; CES-19; CES-20 | South Family 6 candidate areas | Family configuration conflict | Current official parish evidence confirms the four physical churches merged into Transfiguration of Our Lord Parish effective August 6, 2026. | SRC-AOC-20260807-005; SRC-AOC-20260807-009; SRC-PARISH-20260807-018 through -021; SRC-PARISH-20260807-032 | Preserve the historical configuration evidence and retain four distinct physical records. | Research implementation | Closed for current relationship | No physical destination was collapsed into the parish organization. |
| GAP-AOC-010 | CES-05 | Columbia Tusculum | Boundary ambiguity | St. Stephen's current official family page verifies the location but does not identify the approved neighborhood. | CAND-AOC-022; SRC-PARISH-20260807-022 | Seek direct parish/family-office confirmation. | Research implementation | Open; direct contact required |  |
| GAP-AOC-011 | CES-06 | Mt. Lookout | Boundary ambiguity | Current official family page identifies Our Lord Christ the King with Mt. Lookout. | CAND-AOC-023; SRC-PARISH-20260807-023 | Retain evidence and validate coordinates before final acceptance. | Research implementation | Closed for coverage identity |  |
| GAP-AOC-012 | CES-08 | Oakley | Boundary ambiguity | Current official parish evidence identifies St. Cecilia with Oakley. | CAND-AOC-025; SRC-PARISH-20260807-025 | Retain evidence and validate coordinates before final acceptance. | Research implementation | Closed for coverage identity |  |
| GAP-AOC-013 | CES-09 | Madisonville | Relationship conflict | Current Eastside Catholics evidence identifies the Oratory of St. John Vianney at St. Anthony Church as a current physical destination associated with St. Cecilia Parish and the family. | CAND-AOC-026; SRC-AOC-20260807-002; SRC-AOC-20260807-005; SRC-AOC-20260807-011; SRC-PARISH-20260807-026 | Preserve the appointment omission while using the current official family relationship for canonical representation. | Research implementation | Closed for canonical representation | One physical oratory record was created. |
| GAP-AOC-014 | CES-14; CES-15; CES-16 | Kenwood; Montgomery; Blue Ash | Boundary ambiguity | All Saints is current, but reviewed official web evidence does not establish each proposed area association. | CAND-AOC-029; SRC-PARISH-20260807-029 | Seek direct parish/family-office confirmation for the proposed associations. | Research implementation | Open; direct contact required | One physical destination only. |
| GAP-AOC-015 | CES-15; CES-16 | Montgomery; Blue Ash | Boundary ambiguity | The Good Shepherd is current, but reviewed official web evidence does not explicitly establish either proposed area association. | CAND-AOC-017; SRC-PARISH-20260807-017 | Seek direct parish-office confirmation for the proposed associations. | Research implementation | Open; direct contact required |  |
| GAP-AOC-016 | CES-21 | East Walnut Hills | Boundary ambiguity | Current official parish evidence identifies St. Francis de Sales with East Walnut Hills. | CAND-AOC-030; SRC-PARISH-20260807-030 | Retain evidence and validate coordinates before final acceptance. | Research implementation | Closed for coverage identity |  |
| GAP-AOC-017 | CES-22 | Mt. Adams | Boundary ambiguity | Current official family evidence identifies Holy Cross-Immaculata Church with Mt. Adams. | CAND-AOC-031; SRC-PARISH-20260807-031 | Retain evidence and validate coordinates before final acceptance. | Research implementation | Closed for coverage identity |  |
| GAP-AOC-018 | CC-07; CES-23 | Loveland vicinity; Loveland | Missing relationship name | The current family registry and both current parish sites provide no selected family name for Southeast Family 4. | CAND-AOC-008; CAND-AOC-009; SRC-AOC-20260807-004; SRC-AOC-20260807-005; SRC-PARISH-20260807-008; SRC-PARISH-20260807-009 | Seek direct parish-office confirmation; retain the family identifier meanwhile. | Research implementation | Open; direct contact required | Do not invent a name. |
| GAP-AOC-019 | CC-08 | Goshen | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites. | SRC-AOC-20260807-003; SRC-PARISH-20260807-001 through -013 | Seek direct confirmation from the relevant Clermont parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |
| GAP-AOC-020 | CC-16 | Washington Township | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites. | SRC-AOC-20260807-003; SRC-PARISH-20260807-001 through -013 | Seek direct confirmation from the relevant Clermont parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |
| GAP-AOC-021 | CC-17 | Monroe Township | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites. | SRC-AOC-20260807-003; SRC-PARISH-20260807-001 through -013 | Seek direct confirmation from the relevant Clermont parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |
| GAP-AOC-022 | CC-18 | Jackson Township | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites. | SRC-AOC-20260807-003; SRC-PARISH-20260807-001 through -013 | Seek direct confirmation from the relevant Clermont parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |
| GAP-AOC-023 | CES-04 | California | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites; a street name was not treated as neighborhood evidence. | SRC-AOC-20260807-002; SRC-PARISH-20260807-022 through -031 | Seek direct confirmation from the relevant Cincinnati East Side parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |
| GAP-AOC-024 | CES-10 | Mariemont | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites. | SRC-AOC-20260807-002; SRC-PARISH-20260807-014 through -017; SRC-PARISH-20260807-024 through -027 | Seek direct confirmation from the relevant Cincinnati East Side parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |
| GAP-AOC-025 | CES-11 | Terrace Park | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites. | SRC-AOC-20260807-002; SRC-PARISH-20260807-014 through -017; SRC-PARISH-20260807-024 through -027 | Seek direct confirmation from the relevant Cincinnati East Side parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |
| GAP-AOC-026 | CES-12 | Indian Hill | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites; nearby candidates were not assigned without evidence. | SRC-AOC-20260807-002; SRC-PARISH-20260807-014 through -017; SRC-PARISH-20260807-027 | Seek direct confirmation from the relevant Cincinnati East Side parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |
| GAP-AOC-027 | CES-18 | Silverton | No candidate found | No directly attributable candidate was found in the Archdiocese data or current nearby official parish/family sites. | SRC-AOC-20260807-002; SRC-PARISH-20260807-018 through -021; SRC-PARISH-20260807-027 through -029 | Seek direct confirmation from the relevant Cincinnati East Side parish/family offices before claiming absence. | Research implementation | Open; direct contact required | A no-result web review is not proof of absence. |

## Completion checklist

- [x] Every approved geographic area has a documented Archdiocese-pass review result.
- [x] Areas with candidates and areas with no candidate from this pass are distinguished.
- [x] Missing official sources found in this pass are documented.
- [x] Known incomplete coordinate and travel-zone conditions are documented.
- [x] Current direct-confirmation posture is documented.
- [x] Boundary ambiguities and completeness blockers found in this pass are documented.
- [x] Required Product Owner decisions are recorded as explicitly outstanding.
