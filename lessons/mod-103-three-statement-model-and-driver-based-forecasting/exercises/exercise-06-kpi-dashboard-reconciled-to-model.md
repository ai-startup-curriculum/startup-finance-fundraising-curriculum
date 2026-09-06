# Exercise 06 — KPI Dashboard Reconciled to the Model

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 7 (KPI dashboard reconciled to the model). Exercises 01-05 (the driver architecture, hiring plan, funnel-driven revenue, TAM reconciliation, and scenario switch). Chapter 5 of [`mod-102`](../../mod-102-unit-economics-and-cohort-financial-modelling/) for NRR / GRR definitions and chapter 6 for burn multiple / magic number / Rule of 40 definitions.

## Problem statement

Build the KPI dashboard tab for the three-statement model such that every KPI cell is a formula sourced from a driver, statement, or schedule tab — no typed numbers. Then produce the four dashboard views (current-period snapshot, trailing-12 monthly trend, plan-vs.-actual, scenario comparison) and the five-slide board pack derived from the tab.

The point of the exercise is to install the *no-drift* discipline: the dashboard cannot show a different number from the model, because they are the same underlying calculation. When the CEO shows a board slide with ARR of $8.2M and the CFO opens the P&L and it also shows $8.2M for the same period, the credibility of the whole pack is preserved. When the two numbers differ, everything above is in doubt.

## Scenario — extend your existing model

Extend the model from exercises 01-05. The cohort revenue schedule, hiring plan, scenario switch, and reconciled statements are all already in place. This exercise adds the dashboard tab that pulls from them and the board-slide format that pulls from the dashboard tab.

Additionally, you will need:

- A defined *plan-of-record snapshot* — a locked version of the base-case model (either a saved copy of the file, or an archived tab set) captured at a specific date. Chapter 7's plan-vs.-actual view compares actuals against this locked reference; without it, "plan" and "actual" cannot be distinguished.
- At least 3-6 months of *historical actuals* in the leftmost columns of the statement tabs, populated with realistic-shaped monthly numbers so the trailing-12 and plan-vs.-actual views have something to render.

If the model is entirely forecast (no historical actuals), populate 6 months of hypothetical actuals that vary reasonably around the forecasted trajectory (e.g., ARR came in 3% under plan in month 1, 1% under in month 2, 5% over in month 3) so the plan-vs.-actual variance discussion has content.

## Requirements

Add the following to the workbook.

1. **Dashboard tab — architecture.** Structured per chapter 7:
   - No typed numbers. Every cell is a formula, a link, or a reference to a chart source range.
   - Organised into sections by KPI family: ARR & growth; retention; unit economics; efficiency & burn; hiring; cash.
   - Each KPI cell has a source comment or footnote naming the tab and row it references.
   - Both current-period value and a link to the trailing-12 series (used by the trend charts).
2. **KPI set — the Series-A canonical subset.** Chapter 7 lists 25+ possible KPIs; a working board pack shows 8-12. Author the following minimum set:
   - **ARR & growth (5):** ARR at period-end, new ARR in period, expansion ARR, churned ARR, MoM growth rate.
   - **Retention (3):** NRR at M12, GRR at M12, logo retention at M12.
   - **Unit economics (3):** Blended CAC, CAC payback, gross margin %.
   - **Efficiency & burn (5):** Monthly cash burn, net burn, runway (months), burn multiple, Rule of 40.
   - **Hiring (2):** Headcount at period-end, hires added in period.
   - **Cash (2):** Cash and equivalents at period-end, cash-out date.
   Every KPI's source cell is documented — CAC = P&L S&M for period ÷ funnel closed-won for period; NRR = cohort schedule ratio; runway = balance-sheet cash ÷ trailing-3-month net burn; and so on.
3. **Current-period snapshot view.** A single column showing each KPI's value for the current month (or the most recent closed month if you have actuals). Formatted for direct copy-to-slide.
4. **Trailing-12 monthly trend view.** For each of the top 6 KPIs (ARR, MRR, net burn, runway, NRR, CAC), a chart showing the trailing 12 months. Chart source ranges are structured references or named ranges, not hard-coded ranges that break when a new month is added.
5. **Plan-vs.-actual view.** For the current period (last closed month), a table showing:
   - Metric | Actual | Plan | Variance ($) | Variance (%) | Direction (On / Off)
   - For each of at least 8 KPIs.
   - Plan column references the locked plan-of-record snapshot; actual column references the model's actuals region.
6. **Scenario comparison view.** For each of the top 6 KPIs, the base / upside / downside forecast values at a fixed future month (choose one — e.g., month 12 or month 24 from period-start). This view references the scenario switch from exercise 05.
7. **ARR walk.** The graphical waterfall — `Beginning ARR + New + Expansion − Contraction − Churned = Ending ARR` — for the current period. Sourced from the ARR walk on the dashboard tab (or from the cohort schedule).
8. **Variance narrative.** For every Off row in the plan-vs.-actual table, write 1-2 sentences naming the specific reason for the variance and the current response. Chapter 7 gives examples; your narratives should be equally specific.
9. **Board-slide artefact.** The five slides described in chapter 7, produced as a slide deck (Google Slides, Keynote, PowerPoint) or as five Markdown/PDF pages:
   - Slide 1: current-period KPI snapshot.
   - Slide 2: ARR walk (waterfall).
   - Slide 3: trailing-12 trend (small multiples of top 4-6 KPIs).
   - Slide 4: plan-vs.-actual table with the variance narrative below.
   - Slide 5: scenarios / cash outlook (base / upside / downside cash trajectory and cash-out date).
   Every number on every slide traces back to a cell on the dashboard tab; no re-typing.

## The reconciliation each KPI must pass

Chapter 7's discipline is that every KPI on the dashboard reconciles to a specific model source. The reviewer runs these checks:

- **ARR on the dashboard = sum of MRR × 12 from the cohort revenue schedule** for the same month. Exactly.
- **MoM growth rate on the dashboard = `ARR[M] / ARR[M-1] − 1`** using dashboard ARR cells.
- **NRR on the dashboard matches the cohort schedule's NRR calculation** for the cohort active 12 months ago. Chapter 5 of mod-102 covers the cohort NRR walk.
- **CAC on the dashboard = P&L S&M for the period ÷ funnel closed-won for the period.** Both inputs are model tabs.
- **Gross margin on the dashboard = P&L gross profit ÷ P&L revenue** for the period.
- **Monthly cash burn on the dashboard = trailing-3-month average of `− (CFO + CFI)`** from the CFS. Excludes financing.
- **Runway on the dashboard = ending cash on the balance sheet ÷ trailing-3-month average net burn.**
- **Cash-out date on the dashboard = the first forecast month** where the balance-sheet cash line goes below zero (or below a defined operational cash floor).
- **Burn multiple on the dashboard = net burn (from CFS) ÷ net new ARR (from ARR walk)** for the period.
- **Rule of 40 on the dashboard = YoY revenue growth (%) + LTM EBITDA margin (%)**, both computed from P&L rows.

If any of these checks fail, the dashboard has drifted from the model and the fix is a formula update, not a typed number.

## Starter guidance

- **Build the dashboard AFTER the plan-of-record snapshot is locked.** Otherwise the plan-vs.-actual view has nothing to reference and will silently point at the current-run number.
- **Use the same units and sign conventions as the model tabs.** Dashboard shows revenue as positive, burn as positive (not negative). Do not flip signs in dashboard formulas; flip them in the presentation only.
- **Chart source ranges via named ranges or structured references, not `A1:A13`.** Charts that break when a row is added are the most common dashboard bug.
- **Do not build the trailing-12 chart by copy-pasting values.** The chart's source range points at the model's monthly grid; when the grid extends by a month, the chart updates automatically.
- **For plan-vs.-actual, decide on your On/Off threshold.** Common convention: Off if variance exceeds ±5% or a fixed dollar amount. Document the threshold on the dashboard tab.
- **The variance narrative is where CFO judgement lives.** Numbers alone identify what is Off; the narrative names why. If you cannot write a specific reason, the variance is not yet diagnosed and the CFO owes the board a follow-up.
- **The board slide is not the dashboard tab.** The dashboard tab is dense (60+ cells, 6 charts, source comments). The slide is sparse (8-12 numbers, 1 chart, 3 sentences). Do the compression deliberately.

## Acceptance criteria

- **Every dashboard KPI cell is a formula** — Ctrl-A on the dashboard tab, F5 → Special → Constants → Numbers highlights nothing (or only labels, not numeric KPI values).
- **All ten reconciliation checks above pass** for the current period. Any failure is a formula bug, not a typed override.
- **The trailing-12 charts update automatically** when a new month is added to the model grid — verify by extending the model horizon and checking that the chart extends.
- **Plan-vs.-actual references the locked plan-of-record snapshot**, not the current-run number. Verify by changing an assumption on the assumption tab and confirming the "plan" column in the plan-vs.-actual view does NOT change (only the "actual" column does).
- **Every Off row in the plan-vs.-actual view has a variance narrative** — one to two sentences naming the specific reason and the current response.
- **The board deck's five slides each derive their numbers from the dashboard tab.** No slide contains a typed number that isn't sourced.
- **Scenario switch propagates to the dashboard.** Flipping Base → Downside on the scenario switch changes the appropriate dashboard cells (the scenario-comparison section) and does not change the current-period-snapshot cells (which are actuals).
- **All three reconciliations from exercise 01 still hold** under every scenario.

## Deliverables

- The updated workbook with the dashboard tab and the four dashboard views.
- The five-slide board pack (deck or Markdown/PDF).
- A short (max half-page) methodology memo naming: the KPI subset chosen and why, the On/Off variance threshold, the plan-of-record snapshot date, the source tab for each KPI, and any KPIs whose definition differs from the chapter 7 default with the reason.

## Extensions (optional)

- Add a *live actuals* pipeline: connect the model to a live-data source (Google Sheets IMPORTDATA, an API pull to a QBO / Xero / NetSuite export, or a BI-tool reference). The actuals column updates automatically without manual copy-paste. Report on the plumbing choices and their fragility.
- Author a second dashboard variant for a growth-stage (Series-B+) audience — swap in LTV:CAC ratio, magic number, cash conversion score, and drop some of the ARR-motion detail. Report on which KPIs shifted and why the shift matches the stage.
- For the scenario-comparison view, produce a fan chart of monthly cash under all three scenarios overlaid (a "cone-of-uncertainty" chart). Include the current-period actual as a single dot so the reader can see whether trajectory is tracking to base, upside, or downside.
- Author the "operator scorecard" version of the dashboard — the CRO's / COO's KPI set (pipeline coverage, win rate, product-usage metrics, customer-health) sourced from the same underlying model where possible. Document the overlap with the CFO's dashboard and the boundary between the two.
