# Build B — `sands-enquiry-runner`

**Off-the-plan sales follow-through.** Every apartment enquiry qualified, answered, and tracked, the follow-through a contact form skips.

## Business problem
Enquiries on off-the-plan apartments (website, agents, referrals) are revenue, but they land in a noisy inbox and get slow, inconsistent follow-up. There is no single live view of the sales pipeline per project.

## What we build
A workflow that catches each enquiry, qualifies it (project, budget, timeframe), shows the operator one plain-English preview, drafts an on-brand reply (a draft, never auto-sent), and logs the lead to a simple CRM from enquiry to deposit to contract. Stale leads surface for a nudge.

## Surface and phases
- **Phase 1:** Claude skill that triages and drafts replies, logging to Notion.
- **Phase 3 (optional):** a hosted runner with a "register your interest" form on the project site, in the same shape as our on-site quote runner.

## Reuses
The email classifier already in place plus Notion. Same approval pattern as our meeting-copilot kit (preview, then write).

## Why it matters
A single leaked or slow enquiry on an off-the-plan unit is a six-figure miss. This makes first response minutes, not days, and gives a pipeline the operator can see at a glance.
