# Quality, Security, Privacy, and Accessibility

## 1. Quality strategy

The testing pyramid should include:

### Unit tests

- Recurrence calculation
- Effective dates
- Exception dates
- Timezone and daylight-saving boundaries
- Ranking calculations
- Verification status
- Arrival feasibility
- Event grouping

### Integration tests

- Database constraints
- Row Level Security
- Admin permissions
- Public reads
- Migration behavior
- Source and verification relationships

### End-to-end tests

- Find confession now
- Find adoration today
- Find next Mass
- Deny location permission
- Open directions
- View official source
- See stale-data warning
- Admin corrects a schedule
- Seasonal override replaces a normal schedule

### Manual field tests

- Pixel 9
- At least one iPhone viewport
- Passenger use
- Bright outdoor light
- Weak connection
- Large text settings
- Keyboard navigation
- Screen-reader smoke test

## 2. Required checks before merge

- Formatting
- Linting
- Type checking
- Unit tests
- Applicable integration tests
- Build
- Migration validation
- Secret scan
- Dependency vulnerability review
- Accessibility smoke check for user-interface changes

## 3. Security baseline

Use NIST Secure Software Development Framework practices as a high-level development baseline and OWASP ASVS as the web-application verification checklist.

Minimum controls:

- Protected development environment
- No secrets in source control
- Least privilege
- Supabase Row Level Security on exposed tables
- Server-only service credentials
- Validated and encoded inputs
- Authenticated administrative mutations
- Audit trail for schedule changes
- Dependency review
- Backups
- Recovery procedure
- Security-relevant logging without sensitive personal data
- Review before production deployment

## 4. Privacy baseline

Version 1:

- No public account required
- No advertising
- No sale or sharing of user data
- Optional location only
- No permanent precise-location history
- Favorites stored locally unless later approved
- No record of confession or Mass attendance
- Minimal correction-form information
- No analytics platform until purpose and privacy impact are approved

Any future account, analytics, notification, or cross-device sync feature requires a privacy impact review.

## 5. Accessibility target

Target WCAG 2.2 Level AA.

Key project-specific requirements:

- Large touch targets
- Visible focus
- Keyboard operability
- Sufficient contrast
- Text resizing
- No color-only status communication
- Clear labels
- Predictable navigation
- Accessible error messages
- Reduced-motion support
- Status messages exposed to assistive technology
- Directions and call links with meaningful accessible names

## 6. Mobile-driving safety

The application is not designed for active manipulation by a driver.

Design choices should favor:

- Pre-trip use
- Passenger use
- One-tap handoff to navigation
- Minimal typing
- Large controls
- No dense dashboard while moving
- No attention-demanding animation
- Clear confirmation before changing destination

## 7. Severity levels

### Severity 1 — Release blocker

- Wrong event marked available now
- Data exposure
- Unauthorized admin change
- Destructive migration
- Core app unusable
- Directions to wrong church

### Severity 2 — High

- Major recurrence error
- Location-denied path broken
- Critical accessibility barrier
- Stale-data warning missing
- Official-source link wrong

### Severity 3 — Medium

- Confusing sort
- Minor layout failure
- Incomplete notes
- Non-core filter defect

### Severity 4 — Low

- Cosmetic inconsistency
- Minor copy issue

Severity 1 and 2 defects must be resolved or explicitly accepted before release.
