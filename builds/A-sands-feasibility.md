# Build A — `sands-feasibility`

**Site go / no-go in one page.** Highest leverage, no dependencies, best single demo.

## Business problem
The biggest money decision a developer makes is "do I buy this site?". Today that screen is a manual, per-deal spreadsheet exercise, so good sites stall behind weak ones and the analysis is inconsistent.

## What we build
A Claude skill where the operator pastes a site (address, price, land area, zoning) and gets a one-page first-pass feasibility: indicative unit yield, build cost ballpark, gross realisation from comparable sales, residual land value and margin, and the obvious red flags. Every number labelled indicative. It screens deals so the paid work (QS, valuer, planner) only happens on the survivors.

## Surface and phases
- **Phase 1:** Claude skill (Projects or Claude Code). Output saved to the document store.
- **Phase 2 (optional):** a simple intake form so the operator can run it from a phone in the field.

## Reuses
New skill plus a comparable-sales lookup. Optional save to existing document storage. No dependency on other builds.

## Why it leads
Standalone, fast to show value, and it is recognisably the developer's own work, not inbox admin.

## The full spec
See [`skills/sands-feasibility/SKILL.md`](../skills/sands-feasibility/SKILL.md) for the complete, installable version of this build.
