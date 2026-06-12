# Project 1 — `sands-feasibility`  (lead build)

**Lever: buying the right sites.** Site go / no-go in one page. Claude only.

## The business problem
The biggest money decision a developer makes is "do I buy this site?". Today that screen is a manual, per-deal spreadsheet exercise, so good sites stall behind weak ones and the analysis is inconsistent. Sites arrive faster than they can be properly looked at, and the paid work (QS, valuer, planner) gets spent on deals that were never going to stack up.

## The solution (Claude)
A Claude skill where the operator pastes a site (address, price, land area, zoning) and gets a one-page first-pass feasibility: indicative unit yield, build cost ballpark, gross realisation from comparable sales, residual land value and margin, and the obvious red flags. Every number labelled indicative. It is a screen, not a feasibility study: it kills weak sites fast and flags strong ones.

## What Paul gets
- A consistent go / no-go on every site that lands, in minutes.
- The slow paid work spent only on deals that survive the screen.
- A growing folder of screened sites, all in the same format.

## How we build it
- **Phase 1:** Claude skill (Projects or Claude Code). Output saved to the document store.
- **Phase 2 (optional):** a Claude-driven intake so the operator can run it from a phone in the field by pasting a listing.

## Reuses
New skill plus a comparable-sales lookup. Optional save to existing document storage. No dependency on the other two projects, which is why it leads.

## Success looks like
Every incoming site gets a one-pager the same day, and the team can point to weak sites that were passed in minutes instead of analysed for an afternoon.

## The full spec
This build is written out in full as an installable skill: [`skills/sands-feasibility/SKILL.md`](../skills/sands-feasibility/SKILL.md).
