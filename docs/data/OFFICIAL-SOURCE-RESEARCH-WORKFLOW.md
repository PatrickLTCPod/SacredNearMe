# Official-Source Research Workflow

**Document status:** Scaffold — operational details not yet complete

## Purpose

This workflow governs Phase 1 research for public location identity, relationships, contact details, active status, and future source mapping. It preserves source traceability and uncertainty while preventing premature schedule collection.

## Scope boundary

- Research is limited to the approved geographic boundary and in-scope Catholic worship locations.
- Phase 1 establishes physical destinations and their official sources; it does not collect worship schedules or event times.
- Missing facts remain missing rather than being guessed.
- Automated publication is prohibited.

## Approved source hierarchy

Use the source hierarchy in `DATA_GOVERNANCE.md`, in this order:

1. Official parish event calendar
2. Official parish worship or sacrament page
3. Current official parish bulletin
4. Official family-of-parishes website
5. Archdiocese of Cincinnati directory
6. Official parish social account
7. Direct parish-office confirmation
8. Secondary Catholic directory
9. User report

Official sources take priority over secondary directories. Secondary directories and user reports may identify research leads but do not establish final authority by themselves. During Phase 1, these source types may be used only to establish or map location identity and related evidence; worship schedules must not be extracted.

## Required research sequence

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

## Source-recording requirements

For each source used, record:

- A stable source identifier
- The related church identifier when one exists
- Source type
- Publisher
- Exact URL or direct-confirmation method
- Date accessed or confirmation date
- Authority level
- Intended future use
- Current availability
- Notes, limitations, or conflicts

Distinguish authoritative evidence from a research lead. Recording a worship, bulletin, or calendar URL as a potential future schedule source does not authorize schedule extraction during Phase 1.

## Conflict-handling requirements

- Preserve conflicting official information rather than silently selecting one version.
- Record each conflicting source, the conflict, and its access date.
- Do not infer a resolution from unsupported assumptions.
- Escalate unresolved identity, boundary, active-status, address, or relationship conflicts when Product Owner judgment is required.

## Direct-confirmation requirements

- Use direct parish-office confirmation only when needed under the approved source hierarchy.
- Record the confirmation date, confirmation method, and a factual summary.
- Record only public institutional information needed for the inventory.
- Do not record private contact details, unnecessary personal information, credentials, or production data.

## Prohibited activity

- Collecting Mass, confession, adoration, devotion, or other event schedules
- Extracting event times, recurrence rules, seasonal schedules, or Holy Day schedules
- Transcribing bulletin schedules
- Treating secondary directories as final authority by themselves
- Guessing missing facts
- Automated scraping or automated publication
- Research outside the approved geographic boundary
- Application, database, migration, deployment, or user-interface work

## Quality-control checklist

- [ ] The approved geographic checklist row is identified.
- [ ] Sources were considered in the approved hierarchy.
- [ ] Exact publisher, URL or confirmation method, and access date are recorded.
- [ ] Authoritative evidence is distinguished from research leads.
- [ ] Missing information remains blank and is documented as a gap.
- [ ] Conflicting official information is preserved.
- [ ] Direct confirmation includes a date and factual summary when used.
- [ ] Active or inactive status has supporting evidence.
- [ ] No worship schedule or event time was collected.
- [ ] No private or unnecessary personal information was recorded.

## Product Owner escalation conditions

Escalate when official-source semantics are unclear, official sources conflict without a supportable resolution, the geographic boundary is ambiguous, a duplicate or shared-campus relationship cannot be resolved, the data model cannot represent the evidence, or completing the work would require a scope change.
