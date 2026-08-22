# Driver Architecture and Assumption Tab Design

## Why this matters

The difference between a model and a spreadsheet is the driver layer. A spreadsheet has revenue in row 12 and lets you type over any cell. A model has revenue in row 12 derived from `new bookings × cohort retention` on the cohort tab, which is derived from `SQLs × close rate × ACV` on the GTM funnel tab, which is derived from `leads × MQL rate × SQL rate` on the funnel tab, which is derived from `S&M spend × cost-per-lead` on the assumptions tab. Change the S&M budget on the assumptions tab and every revenue cell, opex cell, cash cell, and balance-sheet cell in every forecast month updates in one recalculation.

The reason to enforce this discipline: startups are constantly changing assumptions. Board meetings change assumptions. New hires change assumptions. Missed quarters change assumptions. Every raise cycle changes assumptions. A model where each change requires editing 40 cells across 8 tabs is broken by construction — the CFO will not make the change consistently, some cells will drift, and the model will slowly rot into a spreadsheet.

This chapter installs the driver architecture: the assumption tab as the sole home of user-editable inputs, the driver tab as the layer that transforms assumptions into the inputs each statement consumes, and the rule that no statement cell contains a raw number.

## The three-layer discipline

The rule is simple and stated by nearly every practitioner modelling standard (see [FAST Standard](https://www.fast-standard.org/) and the [ICAEW Twenty Principles for Good Spreadsheet Practice](https://www.icaew.com/technical/technology/excel/twenty-principles)):

1. **Inputs (assumptions)** — user-editable numbers, one section per assumption category, colour-coded (typically blue-for-input).
2. **Calculations (drivers and statements)** — formulas only, no typed numbers, sourced entirely from inputs.
3. **Outputs (dashboard, scenario summaries)** — formulas that reference calculations, formatted for a reader who will not open the underlying tabs.

Every cell in the workbook belongs to exactly one of these three layers. The failure mode is mixing — a "calculation" cell that hard-codes an override next to a real formula, an "input" cell that contains a formula referencing another input, an "output" cell that types over the formula because "the number came out wrong." Every mix silently breaks the model's reconcilability.

The colour convention is universal enough to be a signalling tool:

| Cell type | Font colour | Background | Purpose |
|---|---|---|---|
| Input (assumption) | Blue | White or light blue | User can edit; every scenario change lives here |
| Calculation (driver, statement, dashboard) | Black | White | Formula only; never edit directly |
| Link to another sheet | Green | White | Cross-tab reference — signal to trace the source |
| Hard-coded override in a calculation area | Red on yellow | Bright yellow | Emergency-only; every one is a bug in waiting |

The colour convention is not decoration — it is the visual grammar a reviewer uses to spot problems in seconds. A cell that should be blue and is black means an input has been rewritten as a formula (and the reviewer needs to find where the underlying assumption now lives); a cell that should be black and is blue means a calculation has been overwritten with a hard-code (and the model no longer reconciles under a scenario change).

## The assumption tab — structure

The assumption tab is one long tab, organised by category, with a header block at the top for meta-information. A working structure:

```
Assumption tab
├─ Meta (top block)
│   ├─ Model version, author, date, active scenario
│   ├─ Model start date, forecast horizon (24m / 36m), fiscal-year end
│   └─ Colour-coding key
├─ Company & context
│   ├─ Business model (SaaS subscription, PLG, marketplace, enterprise SaaS)
│   ├─ Currency, tax jurisdiction, entity type
│   └─ Historical actuals-through date
├─ Revenue drivers (per scenario)
│   ├─ New bookings by channel by month (or top-down growth-rate override)
│   ├─ ACV progression (starting ACV, monthly / quarterly growth)
│   ├─ Cohort retention curve (M0=100%, M1, M2, …, M24+)
│   ├─ Contract term mix (monthly, annual, multi-year)
│   ├─ Billing terms (monthly-in-advance, annual-prepay, quarterly)
│   └─ Expansion rate, contraction rate, gross churn rate
├─ Cost-of-revenue drivers
│   ├─ Hosting cost per unit / per customer
│   ├─ Third-party COGS (%)
│   ├─ Payment-processing fees (%)
│   ├─ Customer-support headcount per N customers ratio
│   └─ Gross-margin target
├─ Hiring & compensation
│   ├─ Salary bands by level and function (or reference to a hiring tab)
│   ├─ Benefits load (%), employer taxes (%), bonus target (%)
│   ├─ Stock-based comp policy (grants per level, vest schedule, expected forfeiture)
│   └─ Commission plan (rates, quotas, capitalisation term)
├─ Opex driver benchmarks (non-payroll)
│   ├─ S&M non-payroll (paid media, tools, events, agency) as % of S&M payroll or % of revenue
│   ├─ R&D non-payroll (cloud infra for eng, tools, contractors) — same convention
│   ├─ G&A non-payroll (rent, insurance, legal, tax, audit, tools) — same convention
│   └─ CAC per lead / per SQL / per customer by channel (mod-102 output)
├─ Working-capital drivers
│   ├─ DSO (days sales outstanding) → AR
│   ├─ DPO (days payable outstanding) → AP
│   ├─ Prepaid schedule (list of prepaid contracts)
│   └─ Deferred-commission amortisation term (months)
├─ Capex, cap-software, and depreciation
│   ├─ Planned capex by month
│   ├─ Cap-software policy (capitalise Y/N, threshold, useful life)
│   └─ Useful lives by asset class
├─ Financing
│   ├─ Existing cash balance
│   ├─ Existing debt (principal, rate, term)
│   ├─ Planned raises (round size, close month, pre-money)
│   └─ Planned debt (facility size, draw schedule, rate)
├─ Scenarios (switch)
│   ├─ Active scenario name (Base / Upside / Downside)
│   ├─ Per-scenario overrides table (see chapter 6)
│   └─ (Every driver above pulls from the active-scenario column)
└─ Other
    ├─ Tax rate (if positive net income is modelled)
    ├─ Interest rate on cash balance
    └─ FX rates (if multi-currency)
```

Every input is a single cell. Every input has a label to its left and a unit to its right (`$`, `%`, `months`, `count`, `bps`). Every input has a source comment or footnote explaining where the number came from — trailing-3-month actual, budget-committee decision, board-approved plan, benchmark from Bessemer / OpenView, etc.

The tab is one long list not because it's elegant but because it is *searchable*. `Ctrl-F` for "DSO" lands on the DSO input. A reviewer can audit every driving assumption without traversing the model.

## The driver tab — structure

The driver tab is where assumptions get transformed into the shape each statement consumes. It exists because assumptions and statement inputs are not the same shape.

A concrete example. The assumption is:

- Cohort retention: `M0 100%, M1 95%, M2 92%, M3 90%, M4 89%, ...`
- New bookings: `Jan 100 customers, Feb 110, Mar 125, ...`
- ACV: `$12,000, growing 5% per quarter`

The P&L revenue cell needs:

- Total MRR in month M = sum over all prior cohorts of `(cohort N's new customers × cohort retention at M - N × ACV at cohort N's signup / 12)`.

The driver tab is where that sum gets built — the cohort-revenue schedule, one row per signup cohort, columns for cohort-relative months, with the retention curve applied and the ACV progression applied. The bottom row of the schedule is total MRR by calendar month, which is the row the P&L revenue cell references.

The same shape applies to opex-by-function:

- Assumptions: hiring plan (role, start month, fully-loaded cost, department), benefits load, SBC policy, non-payroll ratios.
- Driver: derived monthly opex by department (S&M / R&D / G&A) — sum of payroll for that department's active headcount in each month, plus non-payroll allocation, plus SBC allocation.
- P&L: three rows for S&M, R&D, G&A — each references the corresponding driver row.

And working capital:

- Assumptions: DSO = 45 days.
- Driver: `AR at month-end = revenue for the last (DSO/30) months × (DSO/30 fraction of the earliest month)`.
- Balance sheet: AR references the driver.
- Cash-flow statement: `−Δ AR` in the working-capital section references the same driver.

The driver tab is dense with formulas and thin on numeric inputs — the *only* numbers it contains are the ones in the historical-actuals columns. Every forecast column is a formula.

## The rule: no statement cell contains a raw number

This is the discipline that separates the model from the spreadsheet.

- Every cell in the P&L tab is either historical actual (locked) or a formula pointing at the driver tab.
- Every cell in the balance-sheet tab is either historical actual, a formula pointing at the driver tab, or a formula referencing the prior period's closing balance and the current period's movement.
- Every cell in the cash-flow-statement tab is a formula — CFO's items reference net income and working-capital drivers; CFI references capex / cap-software schedules; CFF references the financing schedule.

A single hard-coded number in a statement tab — the CFO who "adjusts" Q3 revenue up by $200K to match a board expectation — silently breaks the model. Change any assumption on the input tab and the driver tab and the rest of the statement cells update; the hard-coded Q3 revenue cell does not. The next scenario run produces a P&L that doesn't tie to the drivers, and the balance sheet doesn't balance, and no one knows which of the twelve possible failures is the cause.

The enforcement is a review procedure: on every model version, `Ctrl-A` on the P&L / balance-sheet / cash-flow tab, then `Alt-F5` (Excel: Find & Select → Constants → Numbers) should return the historical-actuals region only. Anything highlighted in the forecast region is a hard-coded number in a calculation cell, and every one of them is a bug.

## Single-variable ripple — the acceptance test

The functional test that the driver architecture is working: change one number on the assumption tab and every dependent cell across every statement should update, consistently, in one recalculation.

Concrete tests to run on every new model:

- Change annual growth-rate assumption from 100% to 150%. Every downstream cell (revenue, gross profit, opex if scaled to revenue, CAC-payback, cash-flow trajectory, KPI dashboard) updates. Runway shortens if S&M scales with revenue growth; extends if S&M is fixed.
- Change gross-margin from 75% to 70%. COGS increases, gross profit decreases, opex is unchanged, cash burn accelerates by exactly the delta in dollar gross profit.
- Change DSO from 30 days to 60 days. AR on the balance sheet increases by roughly one month of revenue; cash decreases correspondingly; CFO in the CFS shows a working-capital use; revenue and net income on the P&L are unchanged.
- Change deferred-commission amortisation term from 24 months to 36 months. Commission expense on the P&L declines (spread longer); deferred contract cost on the balance sheet increases; CFO on the CFS shows a working-capital use that offsets the smaller P&L expense — total cash effect is unchanged, only the timing shifts.
- Add a $5M debt facility drawing in month 12. Cash increases by $5M in month 12 (CFF); debt on the balance sheet increases; interest expense begins accruing from month 13 forward; net income declines; balance sheet stays balanced.
- Push a Series-A raise from month 15 to month 18. Cash trajectory shifts; runway shortens if burn is unchanged; every scenario dashboard cell (cash-out date, months of runway) updates.

If any of these tests produces an unexpected result, or breaks a reconciliation check, the model has a driver-linkage bug. Fix it before the model leaves the CFO's screen.

## Circular references — the intentional and the accidental

Some three-statement models have an unavoidable circular reference: interest income on cash depends on the cash balance, which depends on CFO, CFI, and CFF, which depend on net income, which depends on interest income. This is the "interest-on-cash circular" and is the one circular that is usually acceptable.

The Excel setting to enable is **Iterative Calculation** (File → Options → Formulas → Enable iterative calculation), typically with a maximum iteration count of 100 and a maximum change of 0.001. Google Sheets has the same setting under File → Settings → Calculation.

Iterative calc turned on without a documented reason is a red flag; every accidental circular in the model will now compute a wrong answer silently instead of throwing a `#REF!`. The convention: iterative calc is off by default; if the model needs it for the interest-on-cash tie, the cover tab documents the reason, the specific formula chain that requires it, and the maximum-iteration setting. Every other circular is a bug and gets refactored out (chapter 8).

## Named ranges and structured references — legibility over cleverness

The choice between `='Assumptions'!$B$47` and `=DSO_days` is a legibility choice. Named ranges (or Google Sheets' named ranges / Excel Tables' structured references) turn formulas into readable prose.

The trade-off:

- **Named ranges** work everywhere but require discipline — every input needs a stable, documented name, and rename-refactoring across a large model is manual.
- **Excel Tables (structured references)** — `=Bookings[@[Jan-2027]]` — work well for tabular data (the hiring plan, the funnel, the cohort schedule) but are awkward for scalar inputs.

A working convention: named ranges for scalar inputs (`Gross_Margin_Target`, `DSO_days`, `Iterative_Cap`), Excel Tables for the hiring plan / funnel / cohort schedule / debt schedule, direct cell references for everything else. Google Sheets equivalents work the same way; the discipline transfers.

The formula `= Bookings_new_customers * ACV_starting * (1 + ACV_qtr_growth)^(FLOOR(month_offset/3,1))` is auditable by a reviewer who has never seen the model. The formula `=Sheet2!$B$47 * Sheet4!$D$12 * (1 + Sheet2!$B$52)^(FLOOR(Sheet4!$D$14/3,1))` is not. On a diligence call the CFO who has to translate the second version to the investor in real time has already lost the round.

## What to hide on the drivers tab vs. surface on the assumptions tab

A frequent design question: should the retention curve live on the assumptions tab (blue, editable) or the drivers tab (calculated)?

The rule: if the number is a *user decision*, it belongs on the assumptions tab. If it is a *derived intermediate*, it belongs on the drivers tab.

- The 24-month retention curve *values* (M1=95%, M2=92%, ...) are user decisions — they are the scenario assumption. Assumptions tab.
- The cohort-revenue matrix (rows = cohorts, columns = calendar months, values = monthly revenue from each cohort in each month) is a derived intermediate. Drivers tab.
- Total MRR by calendar month (the P&L revenue line) is a derived intermediate summed from the cohort matrix. Drivers tab, referenced from the P&L.

A concrete failure mode: a modeller who puts total MRR directly on the assumptions tab is typing over the whole cohort mechanic. The model looks like it has retention driving revenue, but the top-line number is now decoupled from the cohorts. A scenario change to the retention curve produces zero P&L movement, and no one notices until the reconciliation check on cohort-revenue-sum-to-P&L-revenue starts failing.

## The scenario switch — one place, all downstream

Every assumption that varies by scenario lives in a per-scenario table on the assumptions tab, with a scenario-switch cell that picks the active column. Concretely:

```
Assumption tab, scenarios section:

  Scenario:   [Base]   Upside   Downside
  Active:      X

  Growth-rate assumption:
    Base       Upside   Downside
    +100%      +150%    +60%
  Active growth rate:    =CHOOSE(scenario_index, Base, Upside, Downside)   → 100%

  Gross-margin target:
    Base       Upside   Downside
    75%        78%      70%
  Active gross margin:   =CHOOSE(scenario_index, Base, Upside, Downside)   → 75%

  ... one row per variable that differs by scenario ...

  (Every downstream driver references "Active <variable>", NOT the per-scenario columns.)
```

Chapter 6 goes deep on scenarios. The point here: the scenario switch is a *single* cell that flips the active column. If any downstream cell references a per-scenario column directly instead of the "active" row, changing scenarios produces an inconsistent model — some cells switch, others don't.

## Summary

- The driver architecture separates every workbook cell into three layers: inputs (assumptions, blue, editable), calculations (drivers and statements, black, formula-only), and outputs (dashboard, formatted). Every cell belongs to exactly one layer.
- The colour convention (blue-for-input, black-for-formula, green-for-cross-sheet-link, red-on-yellow-for-emergency-override) is a visual grammar reviewers use to audit the model in seconds.
- The assumption tab is one long, searchable list — company context, revenue drivers, COGS drivers, hiring & comp, opex non-payroll ratios, working-capital drivers, capex, financing, scenarios, other. One cell per input, unit and source labelled.
- The driver tab transforms assumptions into the shape each statement consumes — cohort-revenue schedules, opex-by-function derivations, working-capital calculations, depreciation and amortisation schedules.
- The rule that separates a model from a spreadsheet: no statement cell contains a raw number. Every P&L, balance-sheet, and cash-flow-statement forecast cell is a formula pointing at the driver tab or the prior period's balance.
- The acceptance test: change one number on the assumption tab and every dependent cell updates in one recalculation, and every reconciliation check still holds.
- Circular references are off by default; iterative calc is enabled only for the documented interest-on-cash tie. Every other circular is a bug to refactor.
- Named ranges and structured references turn formulas into auditable prose. On a diligence call, this is the difference between explaining the model in real time and losing the round.
- The scenario switch is a single cell that flips an "active" column; every downstream driver references the active row, never a per-scenario column directly.

Chapter 3 turns to the hiring plan — the tab that drives the largest cash line in most startups' P&L.
