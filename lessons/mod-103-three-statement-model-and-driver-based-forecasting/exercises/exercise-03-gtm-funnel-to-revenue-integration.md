# Exercise 03 — GTM Funnel to Revenue Integration

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 4 (GTM funnel as the revenue driver). Exercise 01 (assumption / driver architecture). Exercise 04 of [`mod-102`](../../mod-102-unit-economics-and-cohort-financial-modelling/exercises/exercise-04-cohort-table-build-and-read.md) (cohort table build) — the retention curve you built there is an input here.

## Problem statement

Build the GTM funnel tab and the cohort revenue schedule for the three-statement model, and wire the resulting bookings / recognised revenue / deferred revenue / AR into the P&L, balance sheet, and cash-flow statement. Verify the integration by running four scenario shifts on the funnel and observing the correct propagation across the model.

The point of the exercise is to build the bottom-up revenue mechanic that connects the marketing and sales activity — S&M spend, cost-per-lead, funnel conversion rates, ACV, cohort retention — to the top line of the P&L. When this is wired correctly, "what happens to Q4 revenue if we double SDR productivity" becomes a one-cell change on the funnel tab.

## Scenario — build your own

Extend the exercise 01 / exercise 02 model to include the following GTM context:

- A defined sales motion — a mixed B2B model with at least two channels (e.g., inbound + outbound; or PLG + enterprise sales).
- 12+ months of historical monthly actuals for the funnel stages (leads, MQLs, SQLs, opportunities, closed-won). If constructing hypothetically, use a realistic conversion cascade that matches published benchmarks.
- Historical monthly ACV progression (constant or trending).
- A cohort retention curve — either from exercise 04 of mod-102 (preferred), or a defensible construction (e.g., M1 95%, M2 92%, M3 90%, M4 89%, then a slow decline to M24 78%).
- An expansion assumption (either baked into the retention curve as NDR, or as a separate per-cohort annual expansion rate).
- A billing-terms distribution (what fraction of contracts are annual prepay, quarterly, monthly).
- A DSO assumption for the collections cycle.

## Requirements

Add the following to the model:

1. **Funnel tab.** Stages as rows, calendar months as columns. Rows: S&M spend, cost-per-lead, leads (formula: S&M / CPL), MQL rate, MQLs, SQL rate, SQLs, opportunity rate, opps, close rate, closed-won customers, ACV, new bookings ($). Historical actuals in the leftmost columns; forecast columns all formulas from assumption-tab conversion rates.
2. **Cohort revenue schedule.** A matrix on the driver tab: rows = signup cohorts (Jan Y through the last forecast month), columns = calendar months. Cell at (row = cohort C, column = month M) = MRR from cohort C in month M, computed as `new-customer count in C × retention curve at (M − C) × cohort C's initial ACV × (1 + expansion rate)^((M − C) / 12) / 12`. Sum-of-column = total MRR by calendar month.
3. **Billings schedule.** For each cohort, the amount billed each month based on billing-terms mix. Annual prepay bills the full ACV in the signup month; monthly bills 1/12 of ACV per month for the contract term.
4. **Deferred revenue roll-forward.** On the driver tab: `Opening deferred revenue + Billings − Revenue recognised = Closing deferred revenue`, monthly.
5. **AR roll-forward.** On the driver tab: `Opening AR + Billings − Collections = Closing AR`, where Collections is billings from the prior period(s) based on DSO.
6. **P&L integration.** Replace the placeholder revenue line from exercise 01 with the total MRR from the cohort revenue schedule.
7. **Balance-sheet integration.**
   - Deferred revenue (short-term + long-term) references the deferred-revenue roll-forward.
   - AR references the AR roll-forward.
8. **CFS integration.**
   - Working-capital section shows `−Δ AR` and `+Δ deferred revenue` correctly.
   - Cash effect matches actual cash-in from billings (not recognised revenue).
9. **Sanity check tab.** Two checks:
   - Total MRR from cohort schedule sums to P&L revenue for every month.
   - Sum of `new bookings ACV / 12 × cohort duration` equals total revenue recognised over the horizon (up to end-of-forecast truncation).
10. **Funnel-change ripple-test log.** Documented tests below.

## The ripple tests to run

Each test changes one funnel input and verifies correct propagation.

1. **Double SDR productivity (SQLs per SDR per month).** Verify: SQLs increase from the change-month forward; opportunities and closed-won scale proportionally; new bookings increase; ARR trajectory bends upward; deferred revenue increases as billings increase; recognised revenue increases with the appropriate lag from the billing-terms mix.
2. **Increase ACV by 20% permanently from month 6.** Verify: new bookings from month 6 forward scale by 20%; cohorts starting from month 6 contribute more MRR at every retention point; total MRR trajectory bends upward with a lag proportional to the cohort maturation.
3. **Drop close rate from 22% to 18% for three months (a "sales miss" scenario).** Verify: closed-won and new bookings drop in those three months; the affected cohorts (three specific signup months) produce less revenue over the entire retention curve; total MRR shows a temporary depression that persists into subsequent months as those cohorts under-contribute.
4. **Shift billing mix from 80% annual prepay to 40% annual prepay** (rest monthly). Verify: recognised revenue is unchanged; billings in the change-month drop (less prepay this month); deferred revenue on the balance sheet drops; cash from operating activities drops in the near term; AR patterns shift.

## Starter guidance

- **Build the funnel tab as a clean stage-cascade first, then add the cohort schedule.** Don't try to build both simultaneously; the cohort schedule references the funnel's `closed-won customers` and `ACV` outputs.
- **The cohort schedule is a large matrix.** For a 24-month forecast, you'll have 24+ cohorts each with 24-36 columns. Use structured references or a filled-formula approach — write the formula for the first cell of the matrix, then fill down and right.
- **The retention curve indexes off cohort-relative months, not calendar months.** `Retention[k]` where `k = calendar month − cohort month`. Use a lookup formula (INDEX / XLOOKUP) to fetch the right retention value.
- **For contracts extending past the forecast horizon, truncate cleanly.** The revenue from a month-18 signup with a 24-month contract runs through month 42; if your forecast is 24 months, cap the schedule at month 24 and note that residual revenue is "beyond forecast horizon" rather than pretending it doesn't exist.
- **Billings-vs.-revenue is where most mistakes happen.** Recognised revenue is smooth (1/12 of ACV per month for annual contracts). Billed amount is lumpy (full ACV in the signup month for annual prepay). Deferred revenue is the difference. Draw the picture on paper before writing the formulas; the model will feel simpler.
- **AR references billings, not revenue.** DSO is `days between invoice date and cash date`. AR at month-end = (last DSO/30 months of billings, pro-rated).
- **Sanity-check MRR against the P&L before doing anything else.** If cohort-schedule sum ≠ P&L revenue for a specific month, no other test will pass.

## Acceptance criteria

- **Every revenue-side cell in the P&L, balance sheet, and CFS is a formula sourced from the cohort schedule, billings schedule, or AR schedule.** No revenue cell contains a raw number.
- **Total MRR from the cohort schedule ties to P&L revenue** for every forecast month.
- **Deferred revenue roll-forward reconciles:** `opening + billings − revenue = closing`, for every month.
- **AR roll-forward reconciles:** `opening + billings − collections = closing`, for every month.
- **Total cash-in from billings** (visible on the CFS working-capital section) matches the sum of billings over the period, less the change in AR.
- **All four ripple tests pass** with expected results and no reconciliation failures.
- **All three reconciliations from exercise 01 still hold** in every forecast month.
- **The funnel-change ripple-test log documents each test** with change / expected / observed.

## Deliverables

- The updated workbook with the funnel tab, cohort revenue schedule, billings schedule, deferred-revenue roll-forward, AR roll-forward, and updated P&L / balance sheet / CFS.
- The funnel-change ripple-test log (max one page).
- A short (max half-page) memo on the specific funnel conventions you chose: attribution model (first-touch / last-touch), cycle-time treatment (same-month / lagged), ACV modelling (blended / per-package), expansion treatment (in-retention-curve / separate driver), billing-terms mix.

## Extensions (optional)

- Add channel dimension to the funnel — outbound vs. inbound each with their own S&M / lead / conversion / ACV. Sum by channel to total; verify the sum reconciles to the aggregate funnel.
- Add a ramp coefficient for AEs and SDRs (from exercise 02) that scales the productivity assumption in each rep's first 3-6 months. Verify that pushing a hire date changes not just payroll but also the SQL/close volume that hire produces.
- Add a per-cohort retention curve (different retention for SMB vs. enterprise cohorts) rather than a single curve applied to all. Verify the total MRR responds correctly to a mix shift.
- Compare the funnel-derived revenue trajectory to a "simple growth-rate" trajectory (revenue × 1 + monthly growth rate) at the same year-end ARR. Report where the two differ over the forecast horizon and why (the bottom-up view catches cohort-lag and billing-terms effects that a smooth growth rate hides).
