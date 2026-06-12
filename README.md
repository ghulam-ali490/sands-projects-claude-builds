# S&S Projects — Claude build proposals

> **Status: proposal.** This repo is a menu of Claude builds we could ship for S&S Projects, written in the Selr kit pattern. Nothing here is committed scope. It exists so the team can browse the options and pick the first 2 to 3 to take to the client.

S&S Projects designs and delivers luxury apartments across South East Queensland. The work below points Claude at where a developer actually makes or loses money: buying the right sites, selling stock, and delivering projects on time and on budget.

Each build follows the same house rules as our other kits:

- **Self-installing** for a non-technical operator.
- **Read-only or draft-only first.** Claude drafts, the operator approves, Claude executes. Nothing is auto-sent.
- **Reuses connectors already in place** (Outlook email and calendar, Xero, Notion, document storage) rather than standing up new plumbing.
- **Approval-gated and reversible.** One plain-English preview before any write.

---

## The menu

| # | Build | What it does | First surface |
|---|-------|--------------|---------------|
| **A** | [`sands-feasibility`](builds/A-sands-feasibility.md) | Paste a site, get a one-page first-pass feasibility before you chase it | Claude skill |
| **B** | [`sands-enquiry-runner`](builds/B-sands-enquiry-runner.md) | Off-the-plan enquiry, qualified, drafted reply, tracked to contract | Skill, then runner + form |
| **C** | [`sands-control-room`](builds/C-sands-control-room.md) | Per-project tracker, Claude drafts the consultant chase emails and a weekly status | Claude skill |
| **D** | [`sands-contract-intelligence`](builds/D-sands-contract-intelligence.md) | Contract or DA notice in, the dates that matter on the calendar | Claude skill |
| **E** | [`sands-jv-report`](builds/E-sands-jv-report.md) | Monthly investor and JV-partner one-pager drafted from Xero | Claude skill |

**Bonus, near-zero build:** stand up our existing `xero-skills` suite (cash-flow forecast, AR ageing, BAS prep, invoice chase) against the client's orgs.

---

## Recommended first picks

- **A · `sands-feasibility`** — standalone wow factor, no dependency on anything else. Best single thing to demo.
- **C · `sands-control-room`** — pure reuse of the email and task connectors already in place.
- **E · `sands-jv-report`** — a cheap bolt-on once the finance feed is wired, because the data layer already exists.

The lead build, A, is fully specified in [`skills/sands-feasibility/SKILL.md`](skills/sands-feasibility/SKILL.md) so the team can see exactly what "done" looks like for one of these.

---

## Repo layout

```
README.md                         this menu
builds/                           one brief per proposed build (A–E)
skills/
  sands-feasibility/
    SKILL.md                      the lead build, fully written as an installable skill
```

## How to read this with the client

These are options to react to, not a quote. Once the team picks the first builds, each becomes a short SOW plus a PRD in the usual format, then a real kit repo.
