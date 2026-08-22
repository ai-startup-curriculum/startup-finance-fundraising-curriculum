# Exercise 02 — Hiring Plan to P&L Integration

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 3 (hiring plan as the opex driver). Exercise 01 (driver / assumption architecture) — this exercise extends that model.

## Problem statement

Build a full hiring-plan tab and integrate it into the payroll, opex-by-function, deferred-commission asset, and stock-based-comp schedule of the three-statement model from exercise 01. Verify the four integrations by running a set of hiring-plan changes and observing the correct propagation across the P&L, balance sheet, and cash-flow statement.

The point of the exercise is to install the *single-source-of-truth* pattern for payroll: every P&L cost line that has any headcount in it — S&M, R&D, G&A, and COGS-embedded (customer support) — is derived from one row per employee on the hiring plan. No headcount total is typed anywhere.

## Scenario — build your own

Extend the exercise 01 model to include the following hiring context:

- Current headcount at model start: 15-40 employees, split roughly 40% R&D / 30% S&M / 15% G&A / 15% COGS-embedded (customer support).
- Planned hires over the 24-month forecast horizon: 20-60 additional employees.
- At least one executive hire (VP or C-level) with equity-heavy compensation to exercise the SBC schedule.
- At least three sales-role hires (AE, SDR) with commission plans to exercise the ASC 340-40 capitalisation mechanic.
- At least two international hires (UK, Canada, Germany, or elsewhere) to exercise the location-varying burden rate.
- A defined attrition assumption (annual attrition rate by function).
- A defined ramp assumption for sales roles (months to full quota attainment).

If you can, use realistic salary bands sourced from a published benchmark (e.g., [Pave](https://www.pave.com/) or [Carta Total Comp](https://carta.com/blog/carta-total-comp/) benchmarks) — the fully-loaded numbers matter for the ripple tests.

## Requirements

Add the following to the exercise 01 workbook:

1. **Hiring-plan tab.** An Excel Table (or Google Sheets structured range) with one row per current or planned employee. Columns per chapter 3: employee ID, role, level, department (S&M / R&D / G&A / COGS-embedded), location, start month, end month (nullable), base salary, target bonus %, benefits load %, employer taxes %, fully-loaded monthly cost (formula), equity grant, vest schedule, commission-capitalisation flag.
2. **Monthly cost grid.** To the right of the hiring-plan table, a monthly grid of fully-loaded cost per employee across the 24-month forecast. Each cell is either the fully-loaded monthly cost (if the month is between start and end) or zero.
3. **Payroll summary by department per month.** Derived on the hiring-plan tab or on the driver tab: sum of fully-loaded cost across active headcount per department per month.
4. **Non-payroll opex by department per month.** Driven from the assumption-tab ratios (as % of department payroll or % of revenue) — updated to reflect the new payroll base.
5. **SBC schedule.** Per-employee SBC expense per month (grant fair value ÷ vest months, with forfeiture adjustment), summed by department per month. This is a non-cash expense.
6. **Deferred-commission (ASC 340-40) schedule.** For sales-role hires with commission-capitalisation flag = Y: per-hire commission accrual on new bookings (assume a bookings distribution across the forecast that ties loosely to the funnel exercise 03 will build, or use a placeholder linear ramp), capitalisation to deferred contract cost, amortisation over the assumed customer-life.
7. **P&L integration.** Update the P&L S&M, R&D, and G&A lines to reference `payroll (by department) + non-payroll (by department) + SBC (by department)`. COGS to reference the customer-support payroll allocation. No P&L cell contains a raw payroll number.
8. **Balance-sheet integration.**
   - APIC increases each month by total SBC expense (all departments).
   - Deferred contract cost (short-term + long-term) walks per the ASC 340-40 schedule.
   - Accrued payroll (if you model within-month accrual) walks per pay-cycle assumption.
9. **CFS integration.**
   - SBC added back as a non-cash item in operating-activities section.
   - Change in deferred contract cost shows as a working-capital movement.
10. **Hiring-change ripple-test log.** Documented tests below.

## The ripple tests to run

Each test changes one aspect of the hiring plan and verifies correct propagation across all three statements plus the KPI dashboard (headcount, department mix, payroll expense, cash burn, runway).

1. **Push a specific hire's start date by three months.** Verify: payroll expense drops in the pushed months for the affected department; cash burn drops correspondingly; SBC expense drops in the pushed months if the grant was tied to hire date; runway extends by a small amount.
2. **Cancel a planned hire entirely.** Verify: department payroll drops by the fully-loaded monthly cost from the cancelled hire's start month onward; SBC drops; cash burn improves; the runway extension for a single senior IC is 1-3 months in most models.
3. **Change the US burden rate assumption from 30% to 33%.** Verify: every US employee's fully-loaded monthly cost updates; total payroll increases across all departments; opex increases across all departments; non-payroll opex (if driven as % of payroll) also increases; cash burn accelerates.
4. **Add a new $10K/month AE ramp assumption** (AE productive at 50% for months 1-3, then full). Verify: this doesn't change P&L payroll (the AE is paid full salary from day one) but should change the funnel exercise 03 will use. Document the effect that the P&L side is unchanged and where the ramp effect shows up.
5. **Extend the deferred-commission amortisation term from 24 to 36 months.** Verify: commission expense on the P&L declines (spread longer); deferred contract cost on the balance sheet increases; CFO on CFS shows an offsetting working-capital use; total cash paid to sales reps is unchanged (only P&L-vs.-cash timing shifts).
6. **Add a Series-A raise event that includes a new-hire cohort of 8 people starting month 13.** Verify: total headcount grows by 8 from month 13; payroll grows by the aggregate fully-loaded cost; opex grows correspondingly; cash decreases as expected; balance sheet still balances.

## Starter guidance

- **Build the hiring-plan table as an Excel Table (structured references) or a Google Sheets named range with formula-fill discipline.** Adding a new row should extend all formulas automatically.
- **Do not model per-employee non-payroll opex.** Non-payroll is at the department level, driven by the ratio on the assumption tab. Per-employee non-payroll is over-engineered for this model.
- **Model burden rate at the location level, not per employee.** `US_burden_rate`, `UK_burden_rate`, `Germany_burden_rate` on the assumption tab; each employee row references the burden rate for their location.
- **Do not build the SBC fair-value calculation from scratch.** Assume a per-employee grant fair-value (based on the current 409A) provided as an input; the schedule just amortises that value over the vest schedule. Chapter 4 of [`mod-104`](../../mod-104-cap-tables-and-equity-compensation/) covers the fair-value methodology.
- **Model commission capitalisation at the aggregate level, not per contract.** Per-hire monthly commission accrual = (commission rate × bookings closed × pro-rata share). Capitalise the total; amortise over the assumed customer life. Per-contract capitalisation is auditor-grade detail that is overkill for a management model.
- **Verify each ripple test with the checks tab from exercise 01.** A hiring-plan change should never break the balance-sheet identity or the cash-tie. If it does, the SBC or deferred-commission entries aren't landing on all three statements consistently.

## Acceptance criteria

- **Every P&L opex cell references the hiring-plan aggregate**, either directly or via the driver tab. No P&L cell contains a raw payroll number.
- **Total headcount by department on the KPI dashboard** (if present) matches the count of active hires per department on the hiring-plan tab, for every month.
- **Total payroll expense in a given month across all departments** equals the sum of fully-loaded monthly costs across all active employees on the hiring-plan tab, exactly.
- **SBC on the P&L equals total per-employee SBC** from the SBC schedule, for every month.
- **APIC on the balance sheet increases by total SBC expense** for every month.
- **SBC added back on the CFS equals P&L SBC** for every month.
- **Deferred contract cost roll-forward reconciles:** `opening + new capitalisation − amortisation = closing`, for every month.
- **All six ripple tests pass** with the expected results and no reconciliation failures.
- **All three reconciliations from exercise 01 still hold** in every forecast month.

## Deliverables

- The updated workbook with the hiring-plan tab, SBC schedule, deferred-commission schedule, and updated P&L / balance sheet / CFS integration.
- The hiring-change ripple-test log (max one page).
- A short (max half-page) memo on the specific hiring-plan conventions you chose: timing convention (full-month, half-month, prorated), burden rates by location, SBC vesting assumption, deferred-commission amortisation term, ramp coefficients.

## Extensions (optional)

- Model a specific hiring cohort tied to a Series-A raise event (raise closes, 8 hires begin the following month). Verify the model handles both cash inflow and the multi-hire payroll increase correctly.
- Add a departure event (a VP leaves month 8; the role is backfilled month 11). Verify the payroll dip and recovery propagate correctly.
- Add a change of geography for an existing employee (US → UK) mid-forecast. Verify the burden rate applied for the pre-change months is US, post-change months is UK.
- Model a graded-vesting equity grant (front-loaded to year 1) for a founder-level hire and compare P&L SBC trajectory to the standard 4-year straight-line.
