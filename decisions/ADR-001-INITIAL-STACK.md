# ADR-001: Initial application stack

**Status:** Proposed for Product Owner acceptance  
**Date:** August 3, 2026  
**Decision owner:** Patrick  

## Context

The project needs an installable mobile experience, structured recurring schedules, a protected administrative interface, preview deployments, and a low-complexity path to private testing.

## Decision

Use:

- Next.js and TypeScript
- Progressive Web App behavior
- Supabase/PostgreSQL
- Supabase Auth for administrators
- GitHub
- Vercel
- Google Maps URL handoff
- America/New_York timezone
- RFC 5545-compatible recurrence concepts

## Alternatives considered

- Native Android first
- Separate Android and iOS applications
- Spreadsheet as the production database
- Static JSON schedules
- Custom navigation map
- General-purpose CMS

## Consequences

### Positive

- One codebase for phones and desktop
- Installable without an app-store launch
- Structured relational data
- Preview deployments
- Administrative security controls
- Lower initial operational complexity

### Negative

- PWA behavior varies by device
- Offline behavior requires careful cache design
- Supabase and Vercel introduce vendor dependencies
- Recurrence logic still requires custom domain testing

## Guardrail

This decision does not approve implementation beyond the active phase. It freezes the baseline only after Product Owner acceptance.

## Approval

**Product Owner:**  
**Date:**
