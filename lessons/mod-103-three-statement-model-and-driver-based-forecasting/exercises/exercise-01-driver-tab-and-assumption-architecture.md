# Exercise 01 — Driver Tab and Assumption Architecture

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 1 (three-statement architecture) and chapter 2 (driver architecture and assumption tab design).

## Problem statement

Build the assumption tab and the driver tab for a Series-A B2B SaaS startup's three-statement model, in a spreadsheet, from scratch. Wire a minimal skeleton P&L, balance sheet, and cash-flow statement to those tabs so that changing any single assumption on the input tab produces a correctly-propagated change on all three statements. Prove the propagation with the six single-variable ripple tests listed under Requirements.

The point of the exercise is to install the *architectural discipline* — every user-editable input on one tab, every derivation on the driver tab, every statement cell a formula sourced from the driver tab, colour-coded, named where useful, with the scenario switch mechanic in place even if only one scenario is populated. Later exercises build the hiring plan (exercise 02), the funnel (exercise 03), and the scenario switch content (exercise 05); this exercise builds the skeleton those bolt into.

## Scenario — build your own

Pick either a real startup you have direct knowledge of (with anonymised numbers) or construct a hypothetical company with the following minimum shape:

- B2B SaaS with recurring subscription revenue and a mixed sales motion (some inbound, some sales-led).
- Current ARR in the $1M-$8M range.
- Team of 15-40 people, mixed across S&M, R&D, and G&A.
- At least one annual-prepay contract (produces deferred revenue balance-sheet movement).
- At least one enterprise customer with committed multi-year (produces long-dated deferred contract cost from commissions).
- A planned Series-A raise sometime in the 24-month forecast horizon (produces a financing-activity event on the CFS).
- Some historical cash burn — enough that runway is a live number.

The numbers do not need to be realistic in every dimension, but they should be internally consistent — if ARR is $4M and gross margin is 75%, then gross profit is $3M and opex less than gross profit for a profitable state (or more than gross profit for a burn state).

## Requirements

Produce a single spreadsheet workbook (Excel or Google Sheets) with the following:

1. **Cover / README tab.** Model version, author, date, workbook conventions (colour key, iterative calc status, tab order), and a table of contents linking to each other tab.
2. **Assumption tab.** Structured per chapter 2:
   - Company & context (currency, entity, historical-actuals-through date).
   - Revenue drivers (starting ARR, monthly growth rate, ACV, cohort retention curve, contract term mix).
   - Cost-of-revenue drivers (gross-margin target, hosting cost, third-party COGS %).
   - Hiring & compensation (a small placeholder — full hiring plan is exercise 02; here, use a total-headcount roll-up).
   - Non-payroll opex ratios (S&M %, R&D %, G&A %).
   - Working-capital drivers (DSO, DPO, deferred-commission amortisation term).
   - Capex and depreciation (minimal — just a monthly capex line and a useful-life assumption).
   - Financing (starting cash, planned Series-A month and amount).
   - Scenario switch table (populated for at least Base; Upside and Downside can be blank stubs — exercise 05 fills them).
   - Every input coloured blue, unit-labelled, and with a source comment.
3. **Driver tab.** Every downstream calculation:
   - Monthly total revenue (starting ARR × growth trajectory ÷ 12 for simplicity; full cohort integration comes in exercise 03).
   - Monthly COGS from gross-margin target.
   - Monthly opex by function (payroll + non-payroll ratio × payroll).
   - Working-capital positions (AR, AP, deferred revenue, deferred contract costs) derived from the assumption tab.
   - Depreciation schedule.
   - Interest expense from debt (if any) and interest income from cash.
4. **P&L tab.** Monthly income statement for a 24-month forecast horizon. Every forecast cell is a formula pointing to the driver tab.
5. **Balance sheet tab.** Monthly balance sheet for the same horizon. Every forecast cell is a formula pointing to the driver tab or referencing the prior period's closing balance.
6. **Cash-flow statement tab.** Indirect-method CFS for the same horizon. Every forecast cell is a formula.
7. **Checks tab (or check row at the bottom of each statement tab).** The three reconciliations from chapter 1:
   - Balance-sheet identity.
   - Cash-on-BS ties to ending cash on CFS.
   - Retained earnings walks forward by net income.
   - Plus opening-vs.-closing balance continuity check.
8. **Ripple-test log.** A short (max half-page) memo listing the six single-variable ripple tests below, the change made, the expected result, and the observed result.

## The six ripple tests to run

Each test changes one number on the assumption tab and verifies the expected propagation. Every test should leave all reconciliation checks green.

1. **Growth rate.** Change from Base (whatever you chose) to +50% higher. Verify: revenue increases across all forecast months; COGS scales; gross profit scales; opex either scales with S&M-ratio or holds fixed depending on your ratio setup; cash trajectory shifts as expected; runway extends or shortens.
2. **Gross-margin target.** Change from Base to 5 percentage points lower. Verify: COGS increases by the delta × revenue; gross profit decreases by the same amount; opex is unchanged; net income falls by the delta; cash burn accelerates by exactly the dollar-margin delta.
3. **DSO.** Change from Base to +30 days. Verify: AR on the balance sheet increases by roughly one additional month of revenue; cash on the balance sheet decreases by the same amount; CFO on the CFS shows a working-capital use of that amount; revenue and net income on the P&L are unchanged.
4. **Deferred-commission amortisation term.** Change from Base to double the term. Verify: commission expense on the P&L declines (spread longer); deferred contract cost on the balance sheet increases; CFO on the CFS shows an offsetting working-capital use; total cash effect is unchanged (only P&L-vs.-cash timing shifts).
5. **Add a $10M Series-A raise in month 12.** Add the row to the assumption tab's financing section. Verify: cash increases by $10M in month 12 on the CFS (CFF line); cash balance on the balance sheet increases by $10M; APIC on the balance sheet increases by $10M; balance sheet still balances; runway extends materially.
6. **Push the Series-A raise from month 12 to month 15.** Verify: the cash trough between months 6 and 15 deepens; cash-out date on the dashboard (or check row) shifts; scenarios where the base case is running out of cash before month 15 are now flagged.

For each test, either the model produces the expected result (and the reconciliations all hold), or it fails and you diagnose the failure and fix it. Document each test in the ripple-test log.

## Starter guidance

- **Build the assumption tab first.** It is one long list of blue cells; do not touch any other tab until every input you'll need is placed. Adding assumptions later requires re-touching the driver tab and the statements, which is where bugs enter.
- **Set the monthly grid consistently across all tabs.** The columns are the same on the driver tab, the statement tabs, and the check tab. Use a header row of dates that every tab references.
- **Colour code from day one.** Blue-for-input, black-for-formula, green-for-cross-tab-link. Don't add colours "later"; do them as you type.
- **Build the driver tab in one big pass.** Every cell that a statement will reference is a formula on the driver tab. Do not put working-capital calculations directly on the balance-sheet tab; put them on the driver tab and reference them from the balance sheet.
- **Build the balance sheet next, then the CFS, then the P&L.** The order matters because the balance sheet references the driver tab, the CFS references the P&L and balance-sheet movements, and the P&L references the driver tab. Building in this order surfaces missing driver-tab lines before you've written statement formulas that depend on them.
- **Add the check row before running the ripple tests.** A ripple test that "seems to work" but breaks a reconciliation is a false pass.
- **Do not skip the scenario switch even though scenarios are exercise 05.** Set up the switch cell, the scenario-name lookup, and the per-variable table. Leave Upside and Downside cells empty. This puts the architecture in place so exercise 05 is a fill-in rather than an architectural retrofit.

## Acceptance criteria

- **Every forecast cell in the P&L, balance sheet, and CFS is a formula.** `Ctrl-A` on any statement tab, then `F5` → Special → Constants → Numbers highlights only historical actuals; nothing in the forecast region.
- **All three reconciliations hold for every forecast month.** Balance-sheet identity = 0; cash-tie between BS and CFS = 0; retained earnings walks by net income; opening = prior period closing.
- **The colour convention is applied consistently.** No blue in a calculation region, no black on an editable input, no bare numbers where a formula belongs.
- **All six ripple tests pass** with expected results and no reconciliation failures.
- **The ripple-test log documents each test** with change / expected / observed.
- **The assumption tab is searchable.** Any assumption in the model can be found by `Ctrl-F` on the assumption tab in under 30 seconds.
- **The scenario switch cell and per-variable table exist**, wired to at least the Base column. Upside and Downside may be stubs.

## Deliverables

- The workbook (.xlsx or Google Sheets link) with all seven tabs.
- The half-page ripple-test log (Markdown or PDF).
- A short (max half-page) methodology memo naming your workbook conventions (colour code, sign convention, period convention, iterative-calc setting).

## Extensions (optional)

- Add a second scenario (Downside) with 2-3 flexed variables and verify the scenario switch flips all three statements consistently.
- Add named ranges for the top 10 most-referenced assumptions and refactor the driver-tab formulas to use them; report on legibility improvement.
- Add a dashboard tab with three KPIs (ARR, monthly burn, runway) sourced from the model tabs; verify each of the six ripple tests updates the dashboard correctly.
- Introduce a deliberate error (a hard-coded override in one balance-sheet cell) and demonstrate that the reconciliation checks catch it.
