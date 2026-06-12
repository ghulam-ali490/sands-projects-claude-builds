# S&S Projects — Claude build proposal

> **Status: proposal.** Three projects we recommend building for S&S Projects, in the Selr kit pattern. Nothing here is committed scope. It exists so the team can pick what goes to the client.

S&S Projects designs and delivers luxury apartments across South East Queensland. A developer makes or loses money on three levers: **the sites they buy, the projects they deliver, and the stock they sell.** Each project below takes one lever and gives the operator a tool that does the heavy lifting, with a human approving every action.

House rules, same as our other kits:

- **Self-installing** for a non-technical operator.
- **Read-only or draft-only first.** Claude drafts, the operator approves, Claude executes. Nothing is auto-sent.
- **Reuses connectors already in place** (Outlook email and calendar, Xero, Notion, document storage).
- **Approval-gated and reversible.** One plain-English preview before any write.

---

## The three projects

### 1. Site Feasibility Assistant — `sands-feasibility`  (the lead build)
**Lever: buying the right sites.**
Paste a site (address, price, land area, zoning) and get a one-page first-pass feasibility: indicative yield, build cost, gross realisation from comparable sales, residual land value, margin, and red flags. It screens deals in minutes so the slow paid work (QS, valuer, planner) only happens on the ones worth it.
**Why it leads:** standalone, no dependencies, instantly recognisable as the developer's own work. Best single thing to demo.
→ Brief: [`builds/A-sands-feasibility.md`](builds/A-sands-feasibility.md) · Full spec: [`skills/sands-feasibility/SKILL.md`](skills/sands-feasibility/SKILL.md)

### 2. Project Delivery Control Room — `sands-control-room`
**Lever: delivering projects on time and on budget.**
One source of truth per development. Holds a register of who owes what by when (architect, planner, engineers, certifier, builder, council), watches the email threads for overdue items, drafts the chase emails, and produces a weekly one-page status with budget vs actual.
**Why it matters:** a slipped consultant or missed council deadline pushes settlement and burns holding costs. This is the low-value chasing the operator wants off their plate, and it is almost pure reuse of connectors already live.
→ Brief: [`builds/C-sands-control-room.md`](builds/C-sands-control-room.md)

### 3. Off-the-Plan Sales Engine — `sands-sales-engine`
**Lever: selling the stock.**
Captures every apartment enquiry (website, agent, referral), qualifies it, drafts an on-brand reply for the operator to approve, and tracks each lead from enquiry to deposit to contract in a simple CRM. A later phase has Claude run a weekly pipeline review and draft the follow-ups for any lead going cold.
**Why it matters:** a single leaked or slow enquiry on an off-the-plan unit is a six-figure miss. This makes first response minutes, not days, and gives a live sales pipeline.
→ Brief: [`builds/B-sands-sales-engine.md`](builds/B-sands-sales-engine.md)

---

## Recommended order

1. **`sands-feasibility`** first — fastest to value, no dependencies, strongest demo.
2. **`sands-control-room`** next — heavy reuse, immediate daily relief.
3. **`sands-sales-engine`** as the revenue play, phased (skill first, voice agent later).

## Also on the table (not in this three)
- **`sands-contract-intelligence`** — pull the key dates out of long contracts and DA notices onto the calendar. [`builds/D-sands-contract-intelligence.md`](builds/D-sands-contract-intelligence.md)
- **`sands-jv-report`** — monthly investor and JV-partner one-pager from Xero. [`builds/E-sands-jv-report.md`](builds/E-sands-jv-report.md)

---

## Repo layout

```
README.md                         this proposal
builds/                           one brief per project
skills/
  sands-feasibility/
    SKILL.md                      the lead build, fully written as an installable skill
```

These are options to react to, not a quote. Once the team picks, each becomes a short SOW plus a PRD, then a real kit repo.
