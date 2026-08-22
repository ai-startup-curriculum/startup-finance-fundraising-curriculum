# The Ownership Boundary with GTM and the Fundraising Narrative

## Why this matters

CAC, LTV, payback, and magic number are metrics that appear in two very different playbooks — the GTM-operator playbook that owns the *movement* of the numbers, and the CFO-finance playbook that owns the *board-defensible presentation* of the numbers and the fundraise narrative on top. The distinction is not academic: it determines who owns which artefact, who does the diligence conversation, and how the pack this module produces plugs into the next four modules of the track.

The failure mode this chapter prevents is the CFO overreaching into GTM territory (recommending channel-mix reallocations without the operational context to defend them) or GTM overreaching into CFO territory (reporting unit economics on the deck that don't survive diligence math). Both happen; both are visible from the outside as "the CFO and the head of growth don't seem to have talked to each other." This chapter names the boundary explicitly, describes the two teams' handoffs, and then turns to the second half: how the unit-economics pack this module authored becomes the fundraise narrative in [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/), the valuation anchor in [`mod-106`](../mod-106-startup-valuation-frameworks/), and the KPI substrate in [`mod-110`](../mod-110-board-and-investor-governance-for-the-cfo/).

## The sideways boundary — what each team owns

The [`startup-product-gtm-curriculum`](https://github.com/ai-startup-curriculum/startup-product-gtm-curriculum) track covers the GTM-operator view of the same numbers this module has been building. To be precise about what each track owns:

**GTM-operator view (owned by `startup-product-gtm-curriculum`):**
- Channel selection and channel-strategy design — which channels to invest in, why, when to enter and when to exit.
- Funnel-stage instrumentation — MQL/SQL/opportunity/close conversion, stage-transition velocity, funnel-stage drop-off diagnostics.
- Sales-motion mechanics — SDR pod design, AE quotas, territory design, commission structures, deal-desk workflow.
- Pricing and packaging — price-point selection, tier design, feature-gating, discount governance.
- Customer-success operating cadence — health scores, expansion motions, renewal choreography, playbook design.
- Magic-number-style operator metrics — sales-efficiency ratios, ACV trends, quota-attainment analysis, ramp-time metrics for AE hires.
- The *management dashboard* view of CAC, LTV, and payback used to make weekly and monthly operational decisions.

**CFO-finance view (owned by this module):**
- The *board and investor* view of CAC, LTV, and payback: fully loaded, cohort-based, discount-rate-adjusted, benchmarked against published venture data.
- The gross-margin bridge and its decomposition into buckets that reconcile to the accrual P&L.
- The cohort table as a diligence-artefact.
- NRR / GRR walk reconciled to the accrual P&L.
- Burn multiple, cash conversion score, Rule of 40 — the capital-efficiency scorecard for board and investor consumption.
- The methodology memo that documents every definition, every allocation choice, and every attribution model.
- The three-way reconciliation between the cohort table, the retention aggregates, and the accrual P&L.

The two views share the underlying data (customer records, MRR movement ledger, S&M spend records, cost-to-serve model) but present it differently and answer different questions. The GTM view answers *"what should we do this quarter to improve the numbers?"* The CFO view answers *"what should we tell the board and the lead investor about what the numbers mean and what they support?"*

## The two-track handoff

At a well-run Series-B startup, the two views operate on a monthly handoff cadence:

- **Weekly** — the GTM team reviews the operator dashboard (per-channel CAC current-week, funnel-stage conversion, quota pacing) and adjusts execution.
- **Monthly** — the CFO's finance-and-strategy team produces the cohort table, updates the fully-loaded per-channel per-cohort CAC, updates the NRR / GRR walk, and refreshes the capital-efficiency scorecard for the board.
- **Quarterly** — the CFO and the Head of Growth (or CRO) sit in the same room to reconcile the two views, resolve any divergences (usually attribution-model differences or spend-allocation edge cases), and align on the narrative for the board pack.
- **Ad hoc — around a fundraise** — the CFO owns the unit-economics-pack production for the data room; the CRO owns the operator narrative for the investor's calls with the sales leadership. Both need to align on the story being told.

The friction points are predictable and worth planning around:

- **Attribution-model disagreements.** The CRO's dashboard may use last-touch attribution because it's what Salesforce ships by default; the CFO's cohort table may use first-touch or multi-touch because it's more defensible in diligence. The reconciliation should be explicit: two views of the same customer base, each defensible for its purpose, and the CFO's view is what appears in external materials.
- **Spend-allocation disputes.** The CRO wants to attribute a specific customer to a specific channel; the CFO's model has to account for the growth-engineering effort or the shared demand-gen operations cost that supported the acquisition. The allocation methodology should be documented and signed off jointly.
- **Timing-lag disputes.** The CRO's monthly attribution treats each month independently; the CFO's cohort framing lags spend behind acquisition by the channel's cycle time (chapter 1). Both are correct for their purposes; the delta is worth naming so no one is surprised.

The rule of thumb: if the numbers on the CRO's operating dashboard don't reconcile to the numbers in the CFO's board pack, one of the two is wrong (or both are computed on different-but-defensible definitions) — and the CFO owes the CEO an explicit reconciliation before the board meeting. Discovering the divergence inside a board meeting is a specific failure mode that erodes CFO credibility.

## The relationship to `startup-foundations` — the level-10 layer below

The [`startup-foundations`](https://github.com/ai-startup-curriculum/startup-foundations) track (level 10) owns the *founder-numbers slice* — runway, burn, growth rate, default-alive / default-dead, and North-Star metric selection. This module does not re-teach those. Where they intersect:

- **Runway and burn** — foundations covers "how many months of runway do we have"; this module covers "what does the burn multiple say about how capital-efficient our burn is." The runway question is a resource-planning question; the burn-multiple question is a capital-efficiency-diagnostic question. Both matter; each track owns one.
- **Growth rate** — foundations covers "are we growing or not"; this module (via chapter 6) covers "is our growth rate on the Rule of 40 frontier we should be on for our stage." Same input, different output.
- **North-Star metric** — foundations covers "which single number should the team optimise for"; this module doesn't intersect with that choice but consumes it (the North Star for a PLG company is usually a signup or activation metric that determines the top-of-funnel for the cohort table).

At Series-A and beyond, the CFO layer sits on top of the founder-numbers layer. A founder with a solid grip on the level-10 material can absorb this module quickly; a founder who has skipped the level-10 material will be missing the mental scaffolding this module assumes.

## The fundraising narrative — how the pack becomes the deck

The unit-economics pack this module produces feeds specific slides in a Series-A or Series-B fundraise deck. The convention:

**The "unit economics" slide** — a single slide typically appearing after the traction/growth slide and before the market/TAM slide. Standard contents:

- Fully-loaded CAC by channel (the per-channel un-blended view, trailing-twelve-months).
- Cohort LTV (discounted, at a stated rate and horizon).
- LTV:CAC ratio (per channel and blended).
- Payback period (cohort-derived, in months).
- One-line methodology note pointing to the appendix.

**The "cohort retention" slide** — a chart with per-cohort retention curves (layer 2 of the cohort table). Typically shows either monthly cohorts grouped by quarter (12-line chart) or half-yearly cohorts (2-4 line chart). The shape tells the story; a smiling-cohort pattern with recent cohorts above older cohorts is the strongest single visual an investor can see.

**The "NRR and GRR" slide** — the walk from starting ARR through churn, downgrade, expansion, and new logos to ending ARR. Best-practice format: the walk in the middle, the trailing-12-month NRR / GRR numbers as two large headline stats above it, the benchmark comparison ("Best-in-class SaaS NRR is 115-130%; we are at 122%") below it.

**The "capital efficiency" slide** — usually at Series-B and beyond, showing the burn multiple, cash conversion score, and Rule of 40 numbers alongside the benchmark bands from chapter 6. Includes a small chart of the trend over the last 8 quarters.

**Appendix slides** — the methodology memo (one to two slides), the cohort table itself for the last 12 signup cohorts (one to two slides), the per-channel CAC waterfall (one slide), the gross-margin bridge (one slide). These appear in the data room and in the follow-up-questions section of a partner-meeting deck rather than in the pitched-live deck.

The full architecture of a fundraise deck — 12-16 slides, Sequoia and YC patterns, DocSend-tracked iteration — is covered in [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/). This module's job is to produce the specific slides above and ensure they survive investor scrutiny.

## The relationship to valuation — the multiple your unit economics support

[`mod-106`](../mod-106-startup-valuation-frameworks/) covers valuation methods in depth. This chapter names the specific link: the unit-economics pack constrains the revenue multiple applied to a company.

The Meritech-and-Bessemer public-SaaS data set (chapter 6 for sources) shows a strong correlation between three variables — growth rate, NRR, and Rule of 40 — and the revenue multiple public SaaS companies trade at. The correlations are not linear, but the pattern is consistent:

- A public SaaS company at 30% growth, 110% NRR, and Rule of 40 = 40% trades at a very different revenue multiple than one at 60% growth, 130% NRR, and Rule of 40 = 65%.
- Private-company valuation applies a discount to public multiples (typically 30-50% for growth-stage, more for earlier stages) but the ordering is preserved.
- The narrower the unit-economics pack, the narrower the plausible valuation range — a company with 90% NRR and 3× burn multiple cannot credibly ask for a revenue multiple in the top decile of public SaaS.

The fundraise conversation is anchored: the CFO's unit-economics pack determines the plausible range of revenue multiples the market will apply, and the negotiation with the lead investor is bounded by that range. A CFO who understands the pack understands the negotiation floor and ceiling.

## The relationship to board governance — the KPI dashboard

[`mod-110`](../mod-110-board-and-investor-governance-for-the-cfo/) covers the CFO's board-and-investor governance work in depth. The unit-economics pack from this module directly becomes the board pack's KPI dashboard.

Standard board-pack KPI dashboard, sourced from this module:

| KPI | Source in this module |
|---|---|
| ARR (current, YoY growth) | Cohort table (chapter 4) roll-up |
| NRR (TTM) | NRR walk (chapter 5) |
| GRR (TTM) | NRR walk (chapter 5) |
| Fully-loaded CAC by channel | Per-channel CAC matrix (chapter 1) |
| Payback period (cohort-derived) | Cohort table layer 5 (chapter 4) |
| Gross margin | Gross-margin bridge (chapter 3) |
| Burn multiple (TTM) | Capital-efficiency scorecard (chapter 6) |
| Cash conversion score | Capital-efficiency scorecard (chapter 6) |
| Rule of 40 | Capital-efficiency scorecard (chapter 6) |
| Runway (months) | Owned by `startup-foundations` / [`mod-109`](../mod-109-runway-management-and-bridge-financing/) |

Every KPI in the dashboard must reconcile to the underlying source in the pack. A dashboard number that doesn't tie to the pack is a diligence-week trap in a future fundraise and a credibility hit in a board conversation. This is a specific pattern [`mod-103`](../mod-103-three-statement-model-and-driver-based-forecasting/) reinforces — the dashboard must be *derived from the model tabs*, not typed in by hand, so drift is impossible.

## The three artefacts this module produces for the fundraise pack

The lab for this module (`lab-01-publish-a-unit-economics-pack-for-one-startup`) produces the end-to-end pack. Its outputs feed [`project-101-seed-to-series-a-fundraise-pack`](../../projects/project-101-seed-to-series-a-fundraise-pack/) directly. The three artefacts a CFO owns:

**Artefact 1 — The unit-economics pack** (typically 8-12 pages / slides). Fully-loaded per-channel CAC, cohort LTV with discount rate, cohort table (last 12-24 monthly cohorts), gross-margin bridge, NRR / GRR walk, capital-efficiency scorecard, methodology memo. Lives in the data room. Refreshed monthly.

**Artefact 2 — The KPI dashboard** (one slide + supporting appendix). The board-pack summary sourced from the pack. Refreshed monthly for the internal ops review; a snapshot appears in each board pack.

**Artefact 3 — The unit-economics slide sequence for the deck** (4-6 slides). The subset of the pack that appears in the pitched-live deck. Refreshed for each fundraise cycle with DocSend tracking (per [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/)) to iterate on which slides investors are actually engaging with.

## What a Series-A investor's diligence firm actually rebuilds

The lead-investor pattern that most Series-A and Series-B deals follow: after signing a term sheet, the lead engages a specialist diligence firm (a big-four accounting firm, a boutique diligence practice, or an in-house partner-firm team) to independently verify the numbers on the deck. The firm's typical unit-economics deliverable:

- Pulls the raw customer, billing, and S&M-spend data from the data room.
- Rebuilds the cohort table from customer records.
- Rebuilds the per-channel CAC from S&M spend records and attribution data.
- Rebuilds NRR and GRR from the MRR movement ledger.
- Rebuilds the gross-margin bridge from the P&L and cost-allocation records.
- Rebuilds the capital-efficiency scorecard from the historical cash-flow statements and ARR series.
- Produces a report to the lead investor comparing the rebuilt numbers to the ones on the deck.

The CFO's job is that the rebuild produces approximately the same numbers as the deck. Differences within 2-3% on any metric are normal and expected (methodology differences); differences beyond 10% are diligence findings that reprice the round.

Producing a pack that survives this specific rebuild is the point of every convention this module has installed: fully-loaded CAC (matches the firm's re-computation), cohort-based LTV with a disclosed discount rate (the firm applies the same rate and gets the same number), cohort table with a documented methodology (the firm rebuilds from the same data), gross-margin bridge decomposed into standard buckets (the firm classifies the same lines the same way), NRR / GRR walk reconciled to the P&L (the firm can trace every dollar). A pack built to this standard closes diligence in one to two weeks; a pack that requires re-work costs the round two or more weeks and often costs valuation.

## Summary

- The GTM-operator view of CAC / LTV / payback / magic number is owned by [`startup-product-gtm-curriculum`](https://github.com/ai-startup-curriculum/startup-product-gtm-curriculum) — the *management dashboard* used to make weekly and monthly operational decisions.
- This module owns the CFO-finance view — the *board and investor* view of the same numbers, fully loaded, cohort-based, discount-rate-adjusted, benchmarked, and packaged for external audiences.
- The two views share the underlying data but answer different questions; the CFO and the Head of Growth reconcile them on a documented cadence.
- Below both views sits [`startup-foundations`](https://github.com/ai-startup-curriculum/startup-foundations) — runway, burn, growth rate, North Star — which this module does not re-teach.
- The unit-economics pack becomes specific slides in a Series-A or Series-B deck: unit economics, cohort retention, NRR/GRR walk, capital efficiency, plus appendix.
- The pack constrains the plausible revenue multiple (via the Meritech / Bessemer data set) and therefore the valuation floor and ceiling.
- The pack becomes the KPI dashboard in board packs, sourced from the same underlying data so drift is impossible.
- A lead investor's diligence firm rebuilds every number in the pack from raw data. Producing the pack to a standard that matches the rebuild is the point of every methodological choice in this module.

This closes mod-102. The module's outputs feed forward: cohort retention curves become drivers in the three-statement model ([`mod-103`](../mod-103-three-statement-model-and-driver-based-forecasting/)), the pack bounds the valuation range ([`mod-106`](../mod-106-startup-valuation-frameworks/)), the pack becomes the data-room and deck substrate ([`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/)), and the KPI dashboard becomes the board-pack backbone ([`mod-110`](../mod-110-board-and-investor-governance-for-the-cfo/)). Every subsequent CFO-side artefact in the track builds on top of the pack this module authors.
