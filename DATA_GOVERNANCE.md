# Data Governance

## 1. Core rule

The schedule database is the product’s highest-value asset. A polished interface cannot compensate for unverified or misleading data.

## 2. Source hierarchy

Use sources in this order:

1. Official parish event calendar
2. Official parish worship or sacrament page
3. Current official parish bulletin
4. Official family-of-parishes website
5. Archdiocese of Cincinnati directory
6. Official parish social account
7. Direct parish-office confirmation
8. Secondary Catholic directory
9. User report

Secondary sources may identify a lead but do not establish a public schedule by themselves.

## 3. Required church fields

- Stable church ID
- Official church name
- Parish-family name
- Street address
- City, state, ZIP
- Latitude and longitude
- Phone
- Official website
- Travel zone
- Active/inactive status
- Accessibility and entrance notes when verified
- Last church-record verification date

## 4. Required event fields

- Stable event ID
- Church ID
- Event category and subtype
- Public title
- Start and end time
- Timezone
- Recurrence rule
- Effective start date
- Effective end date
- Exception dates
- Location within the church campus
- Language
- Public-attendance status
- Associated confession, Mass, adoration, or Benediction flags
- Notes
- Source ID
- Verification status
- Last verified date
- Next review date
- Created and updated timestamps
- Change history

## 5. Verification statuses

### Confirmed

Current official source supports the record.

### Confirmed with caution

Official source is current but warns of interruptions, funerals, holidays, academic breaks, priest availability, or similar conditions.

### Conflicting official sources

Two official sources disagree. Display only with an explicit caution if the Product Owner approves the practical interpretation.

### Seasonal

Valid only in the recorded season or date range.

### Needs reverification

Review deadline has passed.

### Unverified

Not yet supported by a current official or direct source. Do not display as confidently available.

### Retired

Schedule ended but remains in history.

## 6. Review cadence

Default maximum review windows:

- Confession: 30 days
- Adoration: 30 days
- Daily and Sunday Mass: 60–90 days
- Monthly devotions: 60 days
- Academic schedules: at semester boundaries
- Holy Days and seasonal events: reviewed for each occurrence
- Conflicts: immediate review
- Direct phone confirmations: record date, office contacted, and summary

The interface should not silently treat an overdue record as fully current.

## 7. Conflict handling

When official sources disagree:

1. Preserve both source records.
2. Record the exact conflict.
3. Check publication and effective dates.
4. Prefer a current parish calendar or bulletin over an undated page when appropriate.
5. Contact the parish when the conflict affects a likely user trip.
6. Do not overwrite the disagreement without an audit note.
7. Show a caution or suppress the event until resolved.

## 8. User-submitted corrections

A report creates a review item. It does not directly edit the public schedule.

Required report information:

- Church
- Event
- Observed issue
- Date observed
- Optional source
- Optional contact information

Avoid collecting unnecessary personal information.

## 9. Automation policy

Automated page checks may:

- Detect changed text
- Detect a new bulletin
- Compare hashes
- Flag missing schedule language
- Create a review task

Automation may not publish a new time, cancel an event, or resolve a conflict without human review.

## 10. Data quality checks

Automated validation should detect:

- End before start
- Missing timezone
- Invalid recurrence
- Review date before verification date
- Event outside effective window
- Missing official source for Confirmed status
- Duplicate church
- Duplicate overlapping event
- Coordinates outside the approved region
- Public event tied to inactive church
- “Available now” from an expired record

## 11. Liturgical calendar boundary

The national liturgical calendar may identify seasons and dates, but it does not supply local parish times. Local schedules must remain source-backed at the parish level.
