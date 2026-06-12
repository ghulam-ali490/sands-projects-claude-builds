# Project 3 — `sands-sales-engine`

**Lever: selling the stock.** Off-the-plan sales follow-through, Claude only.

## The business problem
Enquiries on off-the-plan apartments (website, agents, referrals) are revenue, but they land in a noisy inbox and get slow, inconsistent follow-up. There is no single live view of the sales pipeline per project, so leads go cold without anyone noticing. A single leaked or slow enquiry on an off-the-plan unit is a six-figure miss.

## The solution (Claude)
A Claude skill that:
- catches each enquiry from the inbox,
- qualifies it (project, budget, timeframe, finance status),
- shows the operator one plain-English preview,
- drafts an on-brand reply (a draft, never auto-sent),
- logs the lead to a simple CRM in Notion, moving it from enquiry to deposit to contract.

## What Paul gets
- First response in minutes, not days, on every enquiry.
- A live pipeline he can see at a glance, per project.
- Nothing leaked: every enquiry is captured and tracked.

## How we build it
- **Phase 1:** Claude skill that triages enquiries, drafts replies, and logs to Notion.
- **Phase 2:** Claude runs a weekly pipeline review, flags any lead going cold, and drafts the follow-up for the operator to approve and send.

## Reuses
The email classifier already in place plus Notion. Same approval pattern as our other follow-up kits: preview, approve, then write.

## Success looks like
Every enquiry answered within the day, zero leads lost to silence, and a pipeline the operator trusts without asking.
