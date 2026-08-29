# Exercise 04 — Deferred Revenue Unwind Modelling

**Estimated time:** ~2 hours
**Prerequisites:** Chapter 4 (deferred revenue liability).

## Problem statement

Build a per-contract deferred-revenue schedule and roll-forward for a full year for a SaaS startup with a mix of billing patterns. Produce the monthly deferred-revenue balance, the deferred-revenue roll-forward disclosure, and the short-term vs. long-term split at each month-end. Add three shock scenarios and show how the schedule responds.

The goal is to internalise how deferred revenue behaves as a living balance sheet account under normal operations and under stress.

## Scenario

Construct a hypothetical SaaS company with 12 active contracts across a calendar year (January through December). Include:

- At least 4 annual-prepay contracts starting in different months of the year
- At least 3 monthly-billed contracts starting in different months
- At least 2 quarterly-billed contracts
- At least 1 multi-year contract (24 or 36 months) with annual prepayment
- At least 1 contract with a distinct implementation fee ($20K-$50K, billed at signature, 4-6 week engagement)
- Contracts starting in months spread across the year, not all in January

For each contract, specify: signature date, contract term, ACV, TCV, billing schedule (dates and amounts), service delivery pattern, and any distinct performance obligations (implementation, training).

## Requirements

Produce the following in a spreadsheet:

1. **Contract register (inputs).** All 12 contracts with the fields listed above.
2. **Per-contract deferred-revenue schedule.** For each contract, a monthly row from contract start through contract end (or through December if contract extends further). Columns: billing (dollar), revenue recognised (dollar), deferred-revenue balance at month-end. The identity per contract per month: ending DR = beginning DR + billing − revenue.
3. **Consolidated monthly deferred-revenue schedule.** Sum across all contracts for each month. Show billings, revenue, ending DR balance.
4. **Short-term vs. long-term split.** For each month-end, compute the portion of the ending DR balance that will unwind (i.e., be recognised as revenue) within the next 12 months. That is short-term deferred revenue. The remainder (only relevant for multi-year contracts) is long-term.
5. **Roll-forward disclosure.** A single-table quarterly roll-forward for each of Q1-Q4:
   - Beginning deferred revenue
   - \+ Additions from billings
   - − Revenue recognised
   - ± Modifications (state whether zero this quarter)
   - = Ending deferred revenue
6. **Balance-sheet sanity check.** Verify that the change in deferred revenue across the year equals total billings − total revenue for the year (with any modifications called out). This is the year-level version of the identity.

Then, add three shock scenarios and rerun the schedule for each:

**Shock A — billing-term shift.** Assume half of the monthly-billed contracts convert to annual-prepay in October (customer accepts a 10% discount to prepay). Show the impact on ending December deferred revenue and the December monthly billings vs. revenue.

**Shock B — customer downsizing.** One large annual-prepay customer (highest-ACV in the register) downsizes at month 7 from their original ACV to half. Terms: pro-rata credit issued for the unearned portion of the reduction. Show the impact on the deferred-revenue balance in month 7 and the recognition pattern for months 7-12.

**Shock C — accelerated churn.** Three monthly-billed customers churn in month 9. Show the impact on billings and revenue in months 9-12. Since these were monthly-billed, deferred revenue impact is minimal — but show the impact on ARR, MRR, and revenue.

For each shock, produce the delta table: base-case metric vs. shock metric for each of ending December DR, Q4 billings, Q4 revenue, ARR at year-end.

## Starter guidance

- The per-contract schedule is the source of truth. Build it first, then aggregate. Do not try to build the consolidated view directly.
- For the implementation-fee contract, treat the implementation as a distinct performance obligation with a separate recognition schedule (recognised over the four-to-six week delivery, not over the annual subscription term). The implementation billing hits deferred revenue at signature and unwinds over the delivery weeks.
- Short-term vs. long-term split: for a contract signed in November 2026 with a 24-month term starting December 2026, the DR balance at year-end (December 31, 2026) has 12 months of coverage from January-December 2027 (short-term) and 11 months from January-November 2028 (long-term). Only some contracts contribute to long-term DR.
- For Shock B (downsizing), the accounting treatment is a contract modification under ASC 606. If the modification reduces the transaction price and reduces the remaining goods/services proportionally, the entity accounts for it as a modification to the existing contract by reducing revenue and deferred revenue prospectively (or as a cumulative catch-up depending on the specific facts). Read ASC 606-10-25-10 through 25-13 before implementing.
- Chart the monthly deferred revenue balance over the year — a good schedule produces a smoothly evolving curve; a jagged curve usually indicates an error.

## Acceptance criteria

- **Per-contract identity ties every month.** ending DR = beginning DR + billing − revenue, per contract, per month.
- **Consolidated schedule matches sum of per-contract.** The consolidated ending DR equals the sum of per-contract ending DR at every month-end.
- **Short-term / long-term split is well-defined.** Every dollar of ending DR is classified into short-term (unwinds within 12 months of the balance-sheet date) or long-term.
- **Quarterly roll-forward table ties.** Beginning + additions − revenue ± mods = ending, for each of Q1-Q4.
- **Year-total identity holds.** Change in DR = Billings − Revenue ± mods for the full year.
- **Each shock scenario is quantified.** Delta tables for the three shocks show base vs. shock for ending DR, Q4 billings, Q4 revenue, ARR.
- **Contract-modification treatment (Shock B) is defensible.** The applied ASC 606 modification treatment is cited (proportional reduction, cumulative catch-up, or separate contract) with rationale.

## Deliverables

- Spreadsheet with: contract register, per-contract schedules (one tab or sub-block per contract), consolidated schedule, quarterly roll-forward, short-term/long-term split, and the three shock-scenario tabs with delta summary.
- A short (half-page) memo explaining the ASC 606 treatment applied to Shock B (the downsizing).

## Extensions (optional)

- Add a chart plotting monthly deferred-revenue balance, monthly billings, and monthly revenue on the same axes for the base case and for Shock A (billing-term shift). The shape difference is the point.
- Compute RPO (deferred revenue + unbilled backlog) at year-end for the base case and each shock.
- Add a fourth shock — the company begins offering a "3-year prepay for 25% discount" that lands three new contracts in November. Show the impact on long-term deferred revenue and the significant-financing-component analysis under ASC 606.
