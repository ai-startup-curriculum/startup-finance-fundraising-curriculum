# Exercise 04 — Cohort Table Build and Read

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 4 (cohort table construction and reading). Chapter 3 (gross margin) for the layer-5 cohort-GP input. Exercise 01 (fully-loaded CAC) for payback comparison.

## Problem statement

Build the full five-layer cohort table for a startup with at least 12 months of customer-signup history. Produce the four canonical readings — retention curves, payback per cohort, cohort LTV and LTV:CAC per cohort, and NDR-at-M12 trend across cohorts — and author the CFO narrative that reads the cohort behaviour (retention, expansion, churn pattern) directly off the table.

The point of the exercise is to install the mechanics of the cohort-table build (data preparation, cohort assignment, layer stacking) and then to develop the qualitative reading skill — recognising the four cohort-shape patterns from chapter 4 (smiling, healthy plateau, steady leak, falling-out-of-bed) and calling out any cross-cohort drift signal.

## Scenario — build your own

Use a real or hypothetical startup with:

- At least 12 monthly signup cohorts, ideally 18-24 for a stronger read.
- Per-customer MRR history from signup through the observation date — for every customer, MRR at each month-end since signup.
- Change events (upgrades, downgrades, plan changes, churn) with dates. A well-designed billing system produces the MRR movement ledger this requires; if reconstructing, use invoice history.
- Per-cohort or per-month cohort gross margin from exercise 03 (or a defensible allocation of the blended gross margin to each cohort).
- Fully-loaded CAC per cohort from exercise 01 (or per-signup-month CAC if that's what's available).

If constructing hypothetical data, aim for 30-100 customers per monthly cohort — enough to make retention percentages statistically meaningful without becoming unwieldy in a spreadsheet.

## Requirements

Produce the following:

1. **Data-quality reconciliation (input check).** Before building the table, produce a data-quality report:
   - Every active customer has a signup date.
   - Sum of MRR across all customers at last month-end reconciles to the P&L / ARR run rate (within a documented reconciliation adjustment).
   - Every churn event has a date and, ideally, a reason code.
   - Cohort assignment is stable (no customer changes cohorts due to re-classification).
2. **Layer 1 — Signup count.** Rows = signup cohorts (Jan Y, Feb Y, ..., last-full-month). Columns = cohort-relative months (M0 through M12+ where data supports). Cells = retained customer count.
3. **Layer 2 — Retention percentage.** Same shape as layer 1, cells = retained percentage of M0.
4. **Layer 3 — Revenue per cohort per month.** Same shape, cells = MRR from retained customers in the cohort-month.
5. **Layer 4 — Net dollar retention per cohort.** Same shape, cells = layer-3 value divided by M0 layer-3 value.
6. **Layer 5 — Cohort gross profit and cumulative gross profit.** Cells = layer-3 revenue × cohort gross margin per cohort-month. Plus a cumulative column at the right.
7. **Reading 1 — Retention curves chart.** Cohort-relative months on the x-axis, retention percentage on the y-axis, one line per signup cohort (or grouped by quarter for readability if you have 18+ monthly cohorts). Produce two versions: customer retention (layer 2) and net dollar retention (layer 4).
8. **Reading 2 — Payback period per cohort table.** For each cohort: M0 count, fully-loaded CAC per customer, cumulative gross profit through the current observation window, and the cohort-month at which cumulative gross profit crossed CAC. Include an "extrapolated" flag for cohorts too young to have crossed empirically.
9. **Reading 3 — Cohort LTV and LTV:CAC table.** For each cohort with at least 12 months of data: cohort LTV (36-month discounted at a stated rate, from exercise 02 methodology), CAC, LTV:CAC ratio.
10. **Reading 4 — NDR at M12 trend chart.** Cross-cohort trend: for cohorts old enough to have reached M12, the NDR at M12 by signup cohort. This reveals vintage effects.
11. **Cohort-shape diagnosis memo (max one page).** Read the four patterns from the layer-2 and layer-4 shapes: which pattern describes recent cohorts (last 6-12 months)? Is there a specific segment or channel driving a different pattern? Is there cross-cohort drift — recent cohorts systematically worse than older cohorts?
12. **CFO narrative (max one page).** The story the CFO tells the board about cohort behaviour: retention direction (improving / stable / deteriorating), the primary driver, expansion motion strength, any red flags visible in the layer-4 view, and any recommended intervention.

## Starter guidance

- Data preparation is the hard part; budget the first hour to reconciliation before building any layer. If the sum of MRR across customers doesn't match the P&L ARR (within a documented reconciliation), stop and fix the data first.
- Build layer 1 first as a pivot table on the customer-and-MRR-history data — signup month on rows, observation month on columns, customer count as values. Convert observation month to cohort-relative month with `MONTHS(observation_month) - MONTHS(signup_month)`.
- Layer 2, 3, and 4 stack on layer 1 — each is a different aggregation on the same underlying pivot.
- For layer 5, the per-cohort per-month gross margin should come from exercise 03. If you have a single blended number, use it consistently but note the limitation.
- For the retention-curves chart, grouping cohorts by quarter or half-year is usually more readable than one line per monthly cohort when you have 18+ cohorts.
- For the payback per cohort, cohorts too young to have crossed CAC in cumulative gross profit are flagged as "TBD" — do not extrapolate.
- The cohort-shape diagnosis is qualitative; practice describing the shape in one sentence per pattern.

## Acceptance criteria

- **All five layers are computable from the same underlying data and reconcile to each other.** Layer 3 aggregated across all cohorts and months equals total MRR revenue on the P&L for the period (with the documented reconciliation adjustment).
- **The retention curves chart is legible.** Fewer than 12 lines on a single chart; grouped cohorts if the count is high.
- **Payback per cohort is empirically read.** Not "arithmetic payback"; the actual month at which cumulative GP crossed CAC. Extrapolated cohorts are flagged.
- **NDR-at-M12 trend chart is a single line across cohorts.** Trend direction (improving, stable, declining) is called out in the narrative.
- **The cohort-shape diagnosis names the pattern from the four options.** Not "our retention is OK" — a specific pattern label (smiling, healthy plateau, steady leak, or falling-out-of-bed) with the shape justification.
- **Cross-cohort drift is either present and named, or explicitly ruled out.** A CFO who doesn't check for drift will be surprised by it in diligence.
- **CFO narrative is one page maximum** and follows the direction / driver / expansion / red flags / intervention structure.

## Deliverables

- Spreadsheet or notebook with the five layers on separate tabs.
- All four readings (retention chart, payback table, LTV table, NDR trend chart).
- Cohort-shape diagnosis memo.
- CFO narrative.

## Extensions (optional)

- Slice the cohort table by acquisition channel (produce the layer-2 view for each channel's cohorts separately). Report which channels have the healthiest cohort shapes.
- Slice by ARPU tier or by industry vertical. Report which segments have the healthiest cohort shapes.
- Produce the "logo cohort" (customer count) view and the "revenue cohort" (dollar) view side by side; comment on any divergence (e.g., logos churn faster than dollars, indicating small-customer mortality).
- Author the two slides that go into the fundraise deck: the cohort retention curves and the NDR-at-M12 trend chart, each with a one-line narrative.
