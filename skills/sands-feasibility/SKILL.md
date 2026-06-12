---
name: sands-feasibility
description: First-pass development feasibility for a potential apartment site. Give it an address, asking price, land area and zoning, and it returns a one-page go / no-go: indicative yield, build cost, gross realisation, residual land value, margin, and red flags. Indicative only, not a QS or valuation sign-off.
status: proposal
---

# sands-feasibility

A first-pass "should I even chase this site?" check. The operator pastes a few facts about a development opportunity and Claude returns a single page that says, in plain numbers, whether the deal is worth a closer look.

This is a screening tool, not a feasibility study. Every number is indicative and clearly labelled as such. It exists to kill weak sites fast and flag strong ones, so the slow paid work (QS, valuer, town planner) only happens on the deals that survive this.

## When to use

Use it the moment a site lands (agent email, off-market tip, a listing). Do not use its output to commit to a purchase, only to decide whether to take the next step.

## Inputs

Required:
- **Address or suburb**
- **Asking price** (or guide)
- **Land area** (m2)

Helpful if known:
- **Zoning / planning scheme designation** and any **height or density control**
- **Site dimensions or frontage**
- **Known constraints** (flood, easements, heritage, slope)

If a required input is missing, ask one short question for it. Do not invent it.

## What it produces

A one-page screen with these sections:

1. **Snapshot** — address, price, land area, zoning, and the headline verdict (Chase / Maybe / Pass) with one sentence of reasoning.
2. **Indicative yield** — an estimated developable area and unit count, with the assumption used (e.g. site coverage, average unit size, height limit). Show the working.
3. **Gross realisation** — estimated end sales value, built from comparable apartment sales in the area. List the comps used.
4. **Cost ballpark** — indicative construction cost at an area rate, plus a rough allowance for soft costs and contingency. State the rate used.
5. **Residual land value and margin** — gross realisation minus costs minus a target margin, giving a land value the deal can support. Compare it to the asking price.
6. **Red flags** — flood overlay, height limit, setbacks, heritage, access, anything that materially changes the picture.
7. **What to verify next** — the two or three things a human must confirm before spending money (e.g. confirm planning controls with council, get a QS rate).

## Steps

1. Confirm the required inputs are present. Ask once for anything missing.
2. Establish the planning envelope: from the zoning and any height or density control, estimate developable GFA and a plausible unit count. State every assumption inline.
3. Pull comparable apartment sales for the area to build the gross realisation. Prefer recent, nearby, similar-product comps. List them so the operator can sanity-check.
4. Apply an indicative build cost at a stated area rate, add soft-cost and contingency allowances.
5. Compute residual land value at a stated target margin, and compare to the asking price.
6. Surface red flags from the inputs and from the planning controls.
7. Output the one-pager. Save a copy to the document store if configured.

## Output rules

- Label every figure **indicative**. Never present a number as a valuation or a QS cost plan.
- Always show the assumption behind each number. A figure with no stated assumption is not allowed.
- If the data to support a section is thin, say so plainly rather than guessing with false confidence.
- Keep it to one page. This is a screen, not a report.

## Guardrails

- This skill does not approve, recommend, or commit to a purchase. It screens.
- Do not auto-send the output anywhere. The operator reviews it first.
- No emojis, no em dashes in the output.
- When the verdict is close to the line, default to **Maybe** and list what would move it, rather than forcing a Chase or Pass.

## Connectors

- **Comparable sales lookup** — web research, or a property-data source if the client provides one.
- **Document storage** (optional) — save each one-pager (SharePoint or Dropbox), so screened sites accumulate in one place.

## Not in scope (deliberately)

- Detailed feasibility modelling, cashflow, or funding structure.
- Town-planning advice.
- Anything that replaces a QS, valuer, or planner. This is the step before those.
