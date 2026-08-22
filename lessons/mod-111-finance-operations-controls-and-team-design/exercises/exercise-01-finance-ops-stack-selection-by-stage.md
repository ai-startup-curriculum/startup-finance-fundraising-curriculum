# Exercise 01 — Finance-Ops Stack Selection by Stage

**Estimated time:** ~2.5 hours
**Prerequisites:** Chapter 1 (finance-ops stack selection by stage).

## Problem statement

Take one hypothetical (or real, if you know it well) B2B SaaS startup and produce a stack-selection memo across three stages of its life — post-seed (~$1.5M ARR, ~15 employees), post-Series-A (~$7M ARR, ~50 employees), and post-Series-B (~$25M ARR, ~150 employees, one international entity). For each stage, choose a full stack across the five layers (banking / ops, general ledger, payroll / HRIS, AP / spend, FP&A) plus the adjacent billing layer, defend each choice against stage-appropriate criteria, name the graduation events that will trigger the *next* stack transition, and estimate the whole-stack monthly cost.

The goal is not the "best" vendor list — vendor market share and features move — but the *decision framework* the CFO uses to make and defend the choice.

## Scenario — build your own company

Construct (or use an existing) company with the following characteristics filled in:

- Product: SaaS (define whether pure-subscription, usage-based, seat-based, or hybrid).
- Customer segment: SMB / mid-market / enterprise mix.
- Contract shape: monthly / annual-prepay / multi-year mix.
- Geographic footprint at each stage: US-only at post-seed, US + one international customer entity at post-A, US + international subsidiary at post-B.
- Payment mix: credit card (Stripe) at SMB tier, ACH / wire / check at enterprise tier.
- Headcount composition: engineering-heavy (roughly 40-50% of headcount), typical GTM ratios.
- Cash on balance sheet: $3M post-seed, $12M post-A, $35M post-B (before applying growth burn).

Reasonable variations are welcome; document your assumptions upfront.

## Requirements

Produce a memo (Markdown or PDF, 4-8 pages) with the following sections.

### Section 1 — The three-stage stack table

For each stage, a table with the following columns filled in per layer:

- Layer (banking / ops, GL, payroll / HRIS, AP / spend, FP&A, billing)
- Selected vendor
- One-sentence rationale
- Monthly cost estimate
- Integration touch-points with the other layers (e.g., "AP corporate-card feed lands in Ramp; Ramp syncs to QBO daily")

### Section 2 — Stage-transition memos (2 memos)

**Memo A — Seed to Series-A transition.** Write the memo the CFO would present to the CEO / board covering what changes in the stack post-Series-A, what stays, what the migration effort is, and what the CFO wants the newly-hired first controller (mod-111 chapter 2) to own. Address specifically: does the company migrate off QBO / Xero at Series-A or defer to Series-B? Why? Does the FP&A model stay in spreadsheets or move to a platform? Why?

**Memo B — Series-A to Series-B transition.** Write the memo covering the NetSuite (or Intacct) migration decision — scope, timeline, implementation-partner selection, chart-of-accounts design decisions to make in month 1, subledger scope, and the specific auditor-driven or entity-driven triggers that dictate the timing. Address specifically: what breaks in QBO / Xero at Series-B that forces the migration? What is the risk profile if the migration slips six months? What is the risk profile if the migration is pulled forward six months?

### Section 3 — Graduation-event register

A table listing each layer's graduation events, the metric that indicates the event is imminent, the lead time the CFO needs to prepare for the transition, and the owner responsible for monitoring the metric.

Example row format:
- Layer: GL
- Graduation event: QBO → NetSuite migration
- Trigger metrics: monthly transaction volume ≥ [X], second operating entity added, deferred-revenue schedule ≥ [Y] active contract-months, first audit committed within 12 months
- Lead time needed: 4-6 months (implementation)
- Owner: Head of Accounting or CFO

### Section 4 — Whole-stack cost summary

For each stage, roll up the layer-by-layer monthly costs to a total monthly and annualised finance-ops software cost. Contextualise against a benchmark (e.g., finance-ops software as % of ARR, or as % of finance-team compensation cost). Flag any layer whose cost seems anomalous vs. the benchmark and explain.

## Starter guidance

- Use chapter 1's five layers as your organising framework. Do *not* invent new layers to fit favourite vendors.
- For vendor choices, be explicit about *why this vendor for this company at this stage* — a rationale like "Rippling because we have IT device management needs" or "Anrok because our SaaS-native product would be a poor fit for Avalara's enterprise workflow" is defensible; "Rippling because everyone uses it" is not.
- For any vendor claim you cannot personally verify (transaction-volume ceilings, integration depth, current pricing), mark it with `[assumption]` in the memo — this mirrors the `<!-- needs-research: -->` discipline in the lecture chapters.
- Include the *billing / subscription-management* layer even though it is called out as adjacent — the CFO decision at Series-A about Stripe vs. Chargebee vs. Zuora vs. Maxio has downstream revenue-recognition implications.
- Treat the international entity at post-A / post-B as a real design constraint — which of the payroll / HRIS / GL vendors handle multi-entity gracefully vs. require workarounds.

## Acceptance criteria

- **Stack table is complete.** Every layer at every stage has a named vendor, rationale, cost, and integration touch-points.
- **Rationale is stage-specific.** A choice defended by "it's the market default" without any stage-fit reasoning is rejected.
- **Migration memos name what breaks.** Each transition memo names the specific limitation of the outgoing stack that forces the migration, not a generic "we've outgrown QBO."
- **Graduation-event register is measurable.** Each trigger is stated in a metric that can be tracked (transaction volume, entity count, contract-month count), not a qualitative "when it feels wrong."
- **Cost summary is realistic.** Numbers are ballpark-defensible against public pricing pages; wildly-off estimates are flagged.
- **Assumptions are explicit.** Any unverified claim is tagged `[assumption]`.

## Deliverables

- The memo (Markdown or PDF), 4-8 pages.
- Optional: a companion spreadsheet with the stack table and cost summary.

## Extensions (optional)

- Add a fourth stage: post-Series-C at ~$75M ARR with active dual-track IPO prep. Walk the Coupa / Zip procurement, Blackline / FloQast close automation, Workday Adaptive FP&A, and AuditBoard / Workiva controls-tooling additions.
- Model a stack decision under a specific *constraint*: the company is post-M&A of a smaller competitor and must consolidate onto one stack within six months. What changes about the decision framework?
- Model a stack decision for a *non-SaaS* startup — a marketplace, a hardware company, or a services / consulting company — and highlight where the SaaS-default choices from chapter 1 diverge.
