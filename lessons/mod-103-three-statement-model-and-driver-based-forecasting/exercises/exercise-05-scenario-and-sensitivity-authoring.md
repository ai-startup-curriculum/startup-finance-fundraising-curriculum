# Exercise 05 — Scenario and Sensitivity Authoring

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 6 (scenario and sensitivity analysis). Exercises 01-03 (the driver architecture with the scenario switch stubbed in, the hiring plan, and the funnel-driven revenue).

## Problem statement

For the same model you built in exercises 01-03, fill out the scenario switch with three coordinated scenarios (Base, Upside, Downside), produce single-variable sensitivity tables for the four levers that dominate cash-out date, and produce the two-variable cash-out-date heatmap for the two dominant levers.

The point of the exercise is to turn the single-point forecast the model produces today into a range of outcomes with named drivers. When the CEO asks *"how bad is it if the outbound channel deteriorates and gross margin slips two points?"* the CFO must have the number ready without going back to rebuild the model. The scenario switch and the sensitivity tables are the artefacts that make that answer instant.

## Scenario — extend your existing model

Extend the model from exercises 01-03. You already have the scenario switch cell and the per-variable table (stubbed in exercise 01, with only the Base column populated). This exercise fills the Upside and Downside columns with coordinated stories, builds the sensitivity infrastructure, and produces the two-variable heatmap.

You will need, additionally:

- A written *upside story* — 2-3 named things that go better than the base case, with a specific operational cause for each. Not "everything is 20% better"; concrete named improvements the team is investing in.
- A written *downside story* — 2-3 named things that go worse than the base case, with a specific operational cause for each. Not a doomsday scenario; concrete named risks that would plausibly materialise together.
- A defined *output that matters most*: for most Series-A SaaS models, the output is cash-out date; for a company with a specific ARR target or profitability target, it may be year-3 ARR or the month of EBITDA breakeven. Choose one output that the sensitivity tables measure against.

## Requirements

Add the following to the workbook.

1. **Scenario switch — populated.** Chapter 6's scenario table architecture. In the assumption tab:
   - The `Scenario_index` cell (1 = Base, 2 = Upside, 3 = Downside), with a `Scenario_name` cell that resolves via `CHOOSE`.
   - The per-variable table with 6-12 rows covering the levers that flex by scenario. Chapter 6 lists the typical set — growth rate, ACV, gross margin, CAC / cost per lead, SDR / AE productivity, close rate, retention (M12 NDR), non-payroll opex ratio, hiring pace.
   - Base / Upside / Downside columns populated with numbers grounded in your named stories.
   - Active column formula (`=CHOOSE(Scenario_index, Base, Upside, Downside)`) — every downstream driver in the model references the Active column.
2. **Scenario story documentation.** A section on the scenarios tab that documents each scenario in 2-3 sentences per case:
   - Upside story: the 2-3 named improvements and their operational causes.
   - Downside story: the 2-3 named risks and their operational causes.
   - What has to be true for each scenario to hold, and what would refute it.
3. **Scenario propagation check.** Flip the switch Base → Upside → Downside and verify the three critical outputs update correctly:
   - Total ARR at year-end for each of years 1, 2, 3.
   - Total burn per month across the horizon.
   - Cash-out date under each scenario.
   Document the three-scenario output on the scenarios tab as a small comparison table.
4. **Single-variable sensitivity tables.** Four tables, one per lever, showing the chosen output (cash-out date, or your chosen alternative) across a range of values for that lever. Chapter 6 lists the levers; for a standard Series-A B2B SaaS, use:
   - Growth rate (or bookings volume) — 5-7 values spanning below and above the base.
   - Gross margin — 5-7 values spanning below and above the base.
   - CAC (or cost per lead) — 5-7 values spanning below and above the base.
   - NRR at M12 (or retention curve shift) — 5-7 values spanning below and above the base.
   Each table has the columns: `Variable value | Output value | Δ vs. base`. Base value highlighted.
   Use Excel's `Data Table` (Data → What-If Analysis → Data Table) if available; in Google Sheets, hand-author the helper block that re-runs the model at each variable value.
5. **Two-variable sensitivity heatmap.** For the two levers the single-variable tables identify as the largest movers of cash-out date. Chapter 6's typical pairing is `growth rate × gross margin` or `growth rate × NRR`; use whichever pair actually dominates in your model.
   - Grid: 5 values on each axis, so a 5×5 cell heatmap.
   - Cells: cash-out date (or the chosen output) at each intersection.
   - Conditional formatting: green for acceptable, yellow for marginal, red for action required. Choose the thresholds and document them.
6. **Consolidation summary (one page).** The output that goes into the board pack, per chapter 6:
   - Base / Upside / Downside numbers: year-end ARR, cash-out date, EBITDA-breakeven month for each.
   - The 1-2 sentence upside and downside stories.
   - The one or two levers to watch weekly, named specifically.
   - The heatmap (embedded or referenced).
   - The fundraise-timing implication for each case.

## The scenario-authoring rules

Chapter 6 warned about two failure modes. Both must be avoided in this exercise:

- **No scalar scenarios.** The Upside column cannot be "every Base value × 1.15" and the Downside cannot be "every Base value × 0.85". Each scenario is a coordinated story with 2-3 named levers moving. The other levers stay at Base (or move only slightly in a way that is caused by the named story — e.g., if the upside story includes "outbound channel matures", both SDR productivity and CAC move because both are consequences of that maturation).
- **No scenario proliferation.** Exactly three scenarios (Base, Upside, Downside). If you find yourself wanting a "recession case" or a "product-2-launch case", make it a versioned copy of the model rather than a fourth scenario column.

## Starter guidance

- **Write the two stories on paper first.** Which two or three levers in the Upside story move, and what is the specific operational programme that produces the movement? Same for Downside. If you cannot write the story in 3 sentences, the scenario isn't coherent yet.
- **Ground the scenario values in the historical range.** The Base value is where you are today (or the plan-of-record). Upside and Downside values should be inside a plausible range of the historical variance for that lever, not fantasy numbers. Growth rate has a plausible range of 60-150% for a growing Series-A; ACV has a plausible range of ±20-30% year-over-year absent a product-repositioning; NRR has a plausible range of 100-135% for a healthy B2B SaaS.
- **Run the scenario propagation check with the reconciliation checks watching.** A scenario flip that breaks the balance-sheet identity or the cash-tie means the scenario switch is flipping a variable that isn't wired through consistently.
- **For the sensitivity tables, use the same base value across all four tables.** The Δ-vs-base numbers only make sense if the "base" they're compared against is the same run.
- **The heatmap needs an interpretable colour scheme.** Green = "cash-out date is beyond our planned fundraise close date"; yellow = "cash-out date is inside the fundraise cushion window"; red = "cash-out date is before the planned fundraise close, triggering emergency action". Document the exact thresholds you chose.
- **Choose the heatmap axes AFTER the single-variable tables produce their numbers.** Chapter 6's rule of thumb (grid the two largest movers) requires knowing which are the largest. Do not pre-commit to the axes.

## Acceptance criteria

- **The scenario switch flips one cell and all three statements update consistently.** Balance-sheet identity, cash tie, and retained-earnings walk all still hold under every scenario.
- **Every scenario-flexed variable is in the scenario table.** No lever flexes by scenario outside the table. (Check: search the assumption tab for any cell whose value differs between scenarios but isn't in the switch table.)
- **The Upside and Downside columns each represent a coordinated story**, not a scalar multiple of Base. The story is documented in 2-3 sentences on the scenarios tab.
- **All four single-variable sensitivity tables produce sensible numeric ranges** — no `#DIV/0!`, no cash-out dates in year 40, no negative-runway numbers displayed as positive. The base value is highlighted in every table.
- **The two-variable heatmap grids the two largest movers** as identified by the single-variable tables (not a pre-committed pair).
- **The heatmap has a documented colour-threshold scheme** — every colour band has a written rule.
- **The consolidation summary is one page** and contains the base / upside / downside numbers, the two stories, the levers to watch, the heatmap or a reference, and the fundraise-timing implication.
- **All three reconciliations from exercise 01 still hold** under every scenario.

## Deliverables

- The updated workbook with the populated scenario switch, story documentation on the scenarios tab, four single-variable sensitivity tables, and the two-variable heatmap.
- The one-page consolidation summary (Markdown or PDF).
- A short (max half-page) methodology memo naming the base / upside / downside stories, the reasoning behind the range of each lever's values, and the heatmap-threshold justification.

## Extensions (optional)

- Add a fourth scenario as a temporary versioned model copy (not a fourth column on the switch): a specific what-if run for a decision the CEO is weighing (e.g., "delay the London launch six months" or "accelerate the enterprise-motion hire plan"). Report on the answer.
- Author a Monte Carlo run: for the four sensitivity-table levers, define a plausible distribution (triangular or normal), run 1,000 trials, and report the distribution of cash-out dates. This is chapter 6's fourth vocabulary term (Monte Carlo modelling) applied.
- For the downside case, produce the *action plan* — the specific cost-cut or hiring-freeze the CFO would recommend if the downside indicators start to appear. Document as a one-page contingency memo.
- Add a scenario that models a specific fundraise event (a Series-A close at month 12 vs. month 18) as an additional switch dimension. Report on the sensitivity of runway to fundraise timing.
