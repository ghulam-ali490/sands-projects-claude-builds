# Build C — `sands-control-room`

**Per-project delivery tracker.** One source of truth per development, and Claude does the chasing. Recommended early pick for pure reuse.

## Business problem
Each active development has a team (architect, planner, engineers, certifier, builder, council) with deliverables, deadlines and a budget. Status lives in the operator's head and scattered across email threads, so things slip. A missed deadline or a slipped consultant deliverable pushes settlement and burns holding costs.

## What we build
A Claude skill that:
- holds a per-project register of who owes what by when, in Notion,
- watches the email threads it already reads for overdue items,
- drafts the chase emails for the operator or EA to send (draft, never auto-sent),
- produces a weekly one-page status per project: milestones, risks, and budget vs actual from the finance feed.

## Surface
Claude skill, run on demand ("status on project X") or as a weekly digest.

## Reuses
The Outlook connector and Notion already in place, plus the finance feed once wired. Almost no new plumbing.

## Why it matters
This is exactly the low-value chasing the client wants off their plate, and it turns scattered threads into one reliable view per project.
