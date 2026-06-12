# Build E — `sands-jv-report`

**Investor and JV-partner reporting.** Monthly partner update drafted from Xero in a click. Cheapest win once the finance feed lands.

## Business problem
The client holds directorships and JV positions, so partner and investor updates are a recurring monthly chore across multiple entities, and the data lives in Xero and the operator's head.

## What we build
A Claude skill that generates a monthly one-pager per project: budget vs actual, milestone status, sales tally, cash position, and next-period focus. The operator edits and sends.

## Surface
Claude skill, run monthly per entity.

## Reuses
The Xero finance feed already being wired. This is the lowest-effort build on the menu because the data layer exists; it is mostly presentation.

## Why it matters
Reporting drops from a few hours each month to minutes, with a consistent format partners can rely on.
