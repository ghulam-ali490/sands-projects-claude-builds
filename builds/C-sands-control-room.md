# Project 2 — `sands-control-room`

**Lever: delivering projects on time and on budget.** One source of truth per development, Claude only.

## The business problem
Each active development has a team (architect, planner, engineers, certifier, builder, council) with deliverables, deadlines and a budget. Status lives in the operator's head and scattered across email threads, so things slip. A missed deadline or a slipped consultant deliverable pushes settlement and burns holding costs, and chasing people for updates is exactly the low-value work the operator wants off their plate.

## The solution (Claude)
A Claude skill that:
- holds a per-project register of who owes what by when, in Notion,
- watches the email threads it already reads for overdue or at-risk items,
- drafts the chase emails for the operator or EA to approve and send (draft, never auto-sent),
- produces a weekly one-page status per project: milestones, risks, and budget vs actual from the finance feed.

## What Paul gets
- One reliable view per project instead of scattered threads.
- The chasing done for him, as ready-to-send drafts.
- A weekly status he can forward to partners without assembling it himself.

## How we build it
- **Phase 1:** the per-project register and the weekly status one-pager.
- **Phase 2:** the overdue-item watcher and auto-drafted chase emails.

## Reuses
The Outlook connector and Notion already in place, plus the finance feed once wired. Almost no new plumbing, which makes this the cheapest of the three to stand up.

## Success looks like
Nothing critical slips unseen, the operator stops manually chasing consultants, and every project has a current status page at any moment.
