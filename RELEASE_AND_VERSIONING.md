# Release and Versioning

## 1. Environments

- Local: developer machine and local database
- Preview: pull-request deployment and test database
- Production: approved public or private release

Do not point local or preview builds at production administrative credentials.

## 2. Release process

1. Work item accepted
2. Pull request opened
3. Required checks pass
4. Preview reviewed
5. Data migrations reviewed
6. Backup status confirmed where applicable
7. Product Owner approves
8. Merge to protected `main`
9. Production deployment
10. Smoke test
11. Release notes
12. Rollback if severity-1 issue appears

## 3. Versioning

Before first formal release, use `0.x.y`.

After stable public release:

- MAJOR: incompatible data, API, or behavior change
- MINOR: backward-compatible feature
- PATCH: backward-compatible correction

Released versions are immutable. A correction receives a new version.

## 4. Rollback requirements

Every release must identify:

- Prior known-good deployment
- Migration rollback or forward-fix strategy
- Backup availability
- Smoke-test checklist
- Person authorized to roll back

## 5. Release blockers

- Severity 1 or unresolved Severity 2 defect
- Failed migration
- Failed RLS test
- Missing official-source traceability for new public schedules
- Unapproved scope or architecture change
- Unresolved accessibility barrier in a core flow
- Production secrets found in client code
- No rollback path
