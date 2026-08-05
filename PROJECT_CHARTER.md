# Project Charter

## 1. Project identity

**Working name:** Sacred Near Me  
**Product type:** Installable mobile-first Progressive Web App  
**Initial territory:** Clermont County, Ohio, and Cincinnati’s eastern communities  
**Initial audience:** Patrick and Katie, followed by a limited private test group  
**Long-term possibility:** Public local Catholic worship finder

## 2. Product mission

Sacred Near Me helps a Catholic quickly identify a nearby opportunity for Mass, confession, Eucharistic adoration, a Holy Hour, or another approved recurring sacred event without searching multiple parish websites, bulletins, and calendars.

## 3. Primary user question

> What can I attend nearby now or later today, and can I realistically arrive before it begins or ends?

## 4. Product outcomes

The project succeeds when a user can:

- Find the next viable confession in under 15 seconds.
- See adoration currently available or opening later that day.
- Find the next Mass by time, distance, language, or area.
- Distinguish weekly, monthly, seasonal, and special schedules.
- Open directions, call the parish, and view the official source in one tap.
- See when each schedule was last verified.
- Use the core app without an account.
- Trust that uncertain or conflicting schedules are visibly labeled.

## 5. Foundational product principles

1. **Accuracy before breadth.**
2. **Official sources before secondary directories.**
3. **Arrival feasibility before simple geographic proximity.**
4. **Structured recurrence before copied schedule text.**
5. **Mobile speed before visual ornament.**
6. **Human review before automatic publication.**
7. **Minimal personal data collection.**
8. **Accessibility from the first functional version.**
9. **No general parish-event sprawl.**
10. **Every change must serve a documented user need.**

## 6. Initial approved technology direction

The provisional baseline is:

- Next.js with TypeScript
- Progressive Web App behavior
- Supabase/PostgreSQL
- GitHub source control
- Vercel deployment
- Google Maps direction links rather than a custom navigation system
- America/New_York as the canonical operating timezone

Changing a major platform or introducing a second overlapping platform requires an Architecture Decision Record and product-owner approval.

## 7. Success metrics

### Product usefulness

- Median time to find a viable event: 15 seconds or less.
- Directions accessible in one tap.
- At least 95% of displayed recurring events have a current official source and verification date.
- No event marked “available now” when its recurrence or effective date excludes it.
- Field testers choose the app over a manual browser search in most relevant situations.

### Maintenance

- Routine schedule correction requires no code change.
- Administrators can identify all records due for reverification.
- Seasonal overrides do not require duplicating an entire recurring schedule.
- Database changes are migration-controlled and recoverable.

## 8. Project constraints

- Initial development is performed by a local Codex environment under human direction.
- ChatGPT may research, plan, review, and create governance or test artifacts but does not silently change approved scope.
- Parish schedules can change without notice.
- “Complete” geographic coverage is only meaningful when paired with a repeatable verification process.
- The app must remain useful when location permission is denied.
- No system should imply sacramental eligibility or replace pastoral judgment.
