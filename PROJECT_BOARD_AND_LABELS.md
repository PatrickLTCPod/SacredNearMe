# Project Board and Labels

## Board columns

1. Inbox
2. Needs Definition
3. Ready
4. In Progress
5. Review
6. Blocked
7. Done
8. Deferred

Only Ready items may move to In Progress.

## Required fields

- Phase
- Work type
- Priority
- Owner
- Decision class
- Risk level
- Target release
- Verification status when data-related

## Recommended labels

### Work type

- `type:feature`
- `type:bug`
- `type:data`
- `type:research`
- `type:governance`
- `type:security`
- `type:accessibility`
- `type:maintenance`

### Phase

- `phase:0-governance`
- `phase:1-inventory`
- `phase:2-recurrence`
- `phase:3-admin-data`
- `phase:4-core-ui`
- `phase:5-location`
- `phase:6-pwa`
- `phase:7-field-test`
- `phase:8-release`

### Priority

- `priority:critical`
- `priority:high`
- `priority:normal`
- `priority:low`

### Status and control

- `needs-decision`
- `needs-source`
- `scope-change`
- `blocked`
- `breaking-change`
- `migration`
- `security-review`
- `accessibility-review`

## Work-in-progress limit

No more than:

- One major feature item in progress
- One defect item in progress
- One research item in progress

Finish or explicitly block current work before starting another major item.
