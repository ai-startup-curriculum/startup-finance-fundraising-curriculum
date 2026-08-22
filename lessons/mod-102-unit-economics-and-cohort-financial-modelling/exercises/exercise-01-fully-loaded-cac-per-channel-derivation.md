# Exercise 01 — Fully-Loaded CAC per Channel per Cohort Derivation

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 1 (fully-loaded CAC per channel per cohort).

## Problem statement

Take one hypothetical startup's S&M ledger, its channel-tagged new-customer log, and its headcount roster for a single quarter, and produce a fully-loaded, per-channel, per-monthly-cohort CAC matrix. Reconcile the three CAC views a CFO reports externally — blended CAC, per-channel CAC (trailing-12-months), and fully-loaded cohort CAC — and author the methodology memo that survives diligence.

The point of the exercise is to install the mechanics: what belongs in the numerator, how to allocate shared costs to channels, how to attribute customers to channels, and how to respect cycle-time lag when assigning spend to a cohort.

## Scenario — build your own

Pick either your own real startup (with anonymised numbers if needed), one you know well from prior work, or construct a hypothetical company with the following minimum shape:

- Mixed-motion B2B SaaS with at least three acquisition channels — pick from: paid search, paid social, content / organic, outbound (SDR-sourced), inbound sales, partner / channel, product-led signup, events.
- Between 30 and 150 new customers acquired during the quarter.
- ARR at quarter-end in the $2M-$20M range.
- An S&M organisation with at least 5 people (mix of marketing, sales development, AEs, and revenue operations) — provides enough headcount that the payroll allocation is meaningful.
- At least one shared-cost line (e.g., a marketing-automation tool, a demand-gen ops manager) that must be allocated across channels.
- At least one channel with a spend-to-close cycle time meaningfully different from same-month (outbound at 60-90 days, or content at 90+ days).
- A monthly ARPU distribution that varies across channels (typical: SMB inbound at low ARPU, enterprise outbound at high ARPU).

If constructing hypothetical data, keep the numbers specific and reproducible — every dollar in the numerator and every customer in the denominator should be traceable back to a line in the underlying ledgers.

## Requirements

Produce the following in a spreadsheet or a well-structured notebook:

1. **Channel-tagged new-customer log (input).** One row per new customer signed in the quarter: customer name, signup date, first-touch channel, contract ACV, contract term, first-billed MRR.
2. **S&M spend ledger (input).** One row per S&M expense line for the quarter: vendor / description, expense category (paid media / payroll / commissions / tools / agency / content / events / partner / attributable CSM effort), amount, channel attribution (or "shared"), month incurred.
3. **Headcount roster (input).** One row per S&M team member: name / role, function (marketing / SDR / AE / RevOps / SE / attributable CS), fully-loaded monthly cost (salary + benefits + employer taxes + SBC), channel allocation (percentages summing to 100%, or "shared").
4. **Cost-allocation methodology memo (max one page).** For every "shared" cost line and every "shared" headcount allocation, name the allocation key (percent-of-team, percent-of-revenue-attributable, percent-of-hours-tracked, etc.). Include a sanity-check that all allocations across all channels sum to 100% of the total shared pool.
5. **Attribution-model methodology memo (max half a page).** Which attribution model (first-touch, last-touch, position-weighted, multi-touch, self-reported) is used to assign customers to channels. Include the time-window (e.g., "60-day first-touch window") and the tie-breaker for edge cases.
6. **Per-channel per-month cohort CAC matrix.** Channels down the side, months across the top (three columns for the quarter), fully-loaded per-customer CAC in each cell. Include a "blended / shared" row and a "self-attributed / unknown" column so the reconciliation ties.
7. **Cycle-time-adjusted cohort CAC.** For channels where the spend-to-close cycle is materially longer than one month (typically outbound, content, events), a second matrix that attributes spend to the cohort of customers it produced (spend from month M attributed to cohort M+lag) rather than the calendar month it was booked.
8. **Three-CAC-views summary.** A single table showing the three views side by side:
   - Blended CAC (total quarter S&M ÷ total quarter new customers).
   - Per-channel CAC (per-channel trailing-quarter view).
   - Fully-loaded cohort CAC (from your matrix, weighted average).
9. **Reconciliation check.** Total fully-loaded spend across all channels-and-months (including the shared bucket) must equal total S&M expense on the P&L for the quarter, to the dollar.

## Starter guidance

- Start with the headcount roster and build the fully-loaded compensation for every S&M person. Use a 30% burden rate as a default (salary × 1.30) unless your scenario specifies otherwise. Include SBC if the company has meaningful equity comp.
- For the channel allocation on shared roles, be explicit — a demand-gen manager who spends 40% on content, 30% on paid, 20% on events, and 10% on general ops has 4 channel allocations summing to 100% (with the 10% general ops going to the "shared" bucket).
- For the spend ledger, treat every line as either channel-attributable or shared. A Salesforce license is shared (all channels use it); a Google Ads bill is 100% paid-search.
- For the customer attribution, pick one model and apply it consistently. First-touch is the simplest defensible model for a young company.
- For cycle-time adjustment, model each channel's lag independently. Paid search: 0 months. Inbound sales: 0-1 months. Outbound: 2-3 months. Content: 3-6 months (or use a trailing-12-month rolling-average approach if the horizon is long).
- The reconciliation must tie exactly — if it doesn't, you have leakage. The "shared / brand / unattributable" bucket is fine as an explicit line; leakage is not.

## Acceptance criteria

- **All three CAC views produce a defensible number.** No division-by-zero errors, no negative CACs, no channels with only 1-2 customers in the denominator (which produces noisy CACs; document any low-denominator channels explicitly).
- **The reconciliation ties.** Total fully-loaded spend across all channels and months equals total S&M P&L expense for the quarter, to the dollar.
- **The methodology memo names every allocation key and every attribution choice.** A reviewer can look at any number in the matrix and trace it back to (a) an input row and (b) the methodology decision that produced the allocation.
- **Cycle-time-adjusted matrix reflects channel-specific lag.** Same-month spend-to-close for fast channels, lagged for slow channels.
- **Blended vs. un-blended comparison names the segment risk.** The comparison of blended CAC to per-channel CAC should identify any channels where the per-channel CAC is materially above the blended (implicit LTV:CAC risk) or materially below (channels to double-down on).
- **Three-view summary reads as one page.** A CRO or lead investor should be able to absorb it in 60 seconds and know which channel to ask about next.

## Deliverables

- Spreadsheet or notebook with all seven numeric artefacts on separate tabs / sections.
- One-page cost-allocation methodology memo (Markdown or PDF).
- Half-page attribution-model methodology memo.
- One-page three-CAC-views summary and diagnosis (Markdown or PDF).

## Extensions (optional)

- Add a fourth channel that requires a different allocation methodology (e.g., a partner-referral channel where the incremental customer produces ongoing rev-share — model the rev-share as COGS, not CAC, and justify the split).
- Extend to a full trailing-twelve-months view and show how the CAC by channel drifts over time.
- Model the LTV:CAC ratio per channel (using a placeholder LTV number; you'll compute real cohort LTV in exercise 2).
- Author the "channel reallocation" memo — given the per-channel view, what S&M dollar reallocation would you recommend to the CEO?
