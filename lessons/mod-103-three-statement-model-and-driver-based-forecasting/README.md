# mod-103 — Three-Statement Model & Driver-Based Forecasting

**Building the CFO's Financial Model**

**Track:** [Startup Finance & Fundraising](../../CURRICULUM.md)
**Stage:** SEED
**Hours:** 26 (8 chapters + 7 exercises + 1 lab + 1 quiz)

## What this module installs

The driver-based, monthly-reconciled, three-statement financial model that a startup CFO builds and lives inside. This is the artefact the Series-A investor's diligence firm re-builds from scratch; it is the artefact the CEO points to when the board asks *"what happens to runway if we miss Q3 sales by 20%?"*; it is the source of truth every KPI on the dashboard reconciles back to. A pack of tabs whose numbers don't tie to each other is not a model — it is a slide deck in spreadsheet clothing. Specifically:

- **Three-statement architecture** — P&L, balance sheet, and cash-flow statement built together, on the same monthly grid, reconciled so that a single assumption change ripples correctly through all three. The balance sheet balances every period, cash on the balance sheet ties to cash on the cash-flow statement, retained earnings walks forward by net income, and opening balances tie to closing balances of the prior period. If the reconciliation breaks, you do not have a model.
- **Driver architecture** — the assumptions tab, the drivers tab, the hiring plan, and the GTM funnel as the small set of inputs from which every P&L line, every balance-sheet movement, and every cash movement is derived. No hard-coded overrides in the statement tabs. One assumption change ripples everywhere.
- **Hiring plan as the opex driver** — role, start month, fully-loaded cost, department, capitalisation policy — as the single source of truth for payroll, S&M / R&D / G&A opex, deferred-commission asset movement, and the SBC line on the P&L.
- **GTM funnel as the revenue driver** — leads → MQL → SQL → close-won × ACV × cohort retention as the bottom-up revenue build; not a top-line ARR growth-rate assumption imposed on the P&L.
- **Top-down and bottom-up reconciliation** — the TAM × penetration-rate top-down view sanity-checks the funnel × cohort bottom-up view. A Series-A investor asks for both; if the two are miles apart, one of the two assumption stacks needs to move.
- **Scenario and sensitivity analysis** — base / upside / downside cases, single-variable sensitivity tables (growth rate, ACV, CAC, NRR), and the two-variable heatmap for the pair of levers that dominate the cash-out date. A single-point forecast is a failure of financial planning.
- **KPI dashboard reconciled to the model** — ARR, MRR, growth rate, NRR, GRR, burn, runway, magic number, Rule of 40 — every dashboard number sourced from a model tab, not typed in, so the dashboard cannot drift from the underlying financials.
- **Model failure diagnosis and review checklist** — circular references without an iterative-calculation intention, hard-coded numbers overwriting formulas, orphaned rows and unused tabs, P&L-to-cash-flow mismatches, opening-balance breaks between periods — the review checklist a CFO runs before every board pack and every diligence hand-off.
- **When to graduate off spreadsheets** — the CFO-level decision on when the model outgrows Excel / Google Sheets and moves to a modern FP&A platform (Causal, Runway, Mosaic, Anaplan, Adaptive), and the migration cost of getting it wrong in either direction.

## Chapters

1. [`01-three-statement-architecture-and-monthly-reconciliation.md`](01-three-statement-architecture-and-monthly-reconciliation.md) — the P&L, balance sheet, and cash-flow statement built together on a monthly grid, and the three reconciliations that make it a model rather than three unrelated tabs.
2. [`02-driver-architecture-and-assumption-tab-design.md`](02-driver-architecture-and-assumption-tab-design.md) — the assumption tab, the driver tab, and the rule that no statement cell contains a raw input — every number in the P&L, balance sheet, and cash-flow statement is derived from a driver.
3. [`03-hiring-plan-as-the-opex-driver.md`](03-hiring-plan-as-the-opex-driver.md) — role / start-month / fully-loaded cost / department as the single source of truth for payroll, opex-by-function, deferred-commission asset movement, and the SBC line.
4. [`04-gtm-funnel-as-the-revenue-driver.md`](04-gtm-funnel-as-the-revenue-driver.md) — leads → MQL → SQL → close-won × ACV × cohort retention as the bottom-up revenue build, and how it ties to the cohort table from `mod-102`.
5. [`05-top-down-vs-bottom-up-reconciliation.md`](05-top-down-vs-bottom-up-reconciliation.md) — the TAM × penetration-rate top-down view, the funnel × cohort bottom-up view, the walk that ties them, and the diligence question each answers.
6. [`06-scenario-and-sensitivity-analysis.md`](06-scenario-and-sensitivity-analysis.md) — base / upside / downside scenario architecture, single-variable sensitivity tables, and the two-variable heatmap for the pair of levers that dominates the cash-out date.
7. [`07-kpi-dashboard-reconciled-to-the-model.md`](07-kpi-dashboard-reconciled-to-the-model.md) — ARR, MRR, growth rate, NRR, GRR, burn, runway, magic number, Rule of 40 — the board-ready dashboard sourced from the model tabs so it cannot drift from the financials.
8. [`08-model-failures-review-checklist-and-when-to-graduate-off-spreadsheets.md`](08-model-failures-review-checklist-and-when-to-graduate-off-spreadsheets.md) — circular refs, hard-coded overrides, orphaned tabs, opening-balance breaks; the review checklist; and the CFO-level decision on when to move to Causal / Runway / Mosaic / Anaplan / Adaptive.

## Exercises

1. [`exercises/exercise-01-driver-tab-and-assumption-architecture.md`](exercises/exercise-01-driver-tab-and-assumption-architecture.md) — build the assumption tab and driver tab, and demonstrate that a single input change ripples correctly through the model (~3h).
2. [`exercises/exercise-02-hiring-plan-to-p-and-l-integration.md`](exercises/exercise-02-hiring-plan-to-p-and-l-integration.md) — build the hiring-plan tab and wire it into the payroll, opex-by-function, and SBC lines on the P&L (~3h).
3. [`exercises/exercise-03-gtm-funnel-to-revenue-integration.md`](exercises/exercise-03-gtm-funnel-to-revenue-integration.md) — build the GTM funnel tab, layer the cohort retention curve, and wire the resulting bookings / MRR into the P&L revenue line (~4h).
4. [`exercises/exercise-04-top-down-vs-bottom-up-reconciliation.md`](exercises/exercise-04-top-down-vs-bottom-up-reconciliation.md) — author both the top-down TAM view and the bottom-up funnel view for the same forecast horizon, and write the reconciliation memo (~3h).
5. [`exercises/exercise-05-scenario-and-sensitivity-authoring.md`](exercises/exercise-05-scenario-and-sensitivity-authoring.md) — author the three-case scenario switch, single-variable sensitivity tables for four levers, and the two-variable cash-out-date heatmap (~4h).
6. [`exercises/exercise-06-kpi-dashboard-reconciled-to-model.md`](exercises/exercise-06-kpi-dashboard-reconciled-to-model.md) — build the board-ready KPI dashboard sourced entirely from model tabs, including the ARR walk, burn / runway, and Rule-of-40 read (~3h).
7. [`exercises/exercise-07-model-review-checklist-and-failure-teardown.md`](exercises/exercise-07-model-review-checklist-and-failure-teardown.md) — apply the model-review checklist to a deliberately broken model, diagnose every failure, and rebuild it correctly (~4h).

## Lab

- `lab-01-publish-a-24-month-three-statement-model-with-scenarios-and-dashboard` — planned; produces the end-to-end 24-month driver-based three-statement model, scenario switch, sensitivity tables, KPI dashboard, and model-review checklist for one hypothetical or real startup, in the shape a Series-A data room expects. Placeholder to be authored in a subsequent content cycle.

## Quiz

- `quiz-01` — planned; 12-15 questions covering the eight chapter objectives, including at least one open-response question that requires reading a broken model excerpt and naming the failure. Placeholder to be authored in a subsequent content cycle.

## Reference

- [`resources.md`](resources.md) — the citable financial-modelling canon, spreadsheet-modelling standards, SaaS-metric benchmark sources, and modern FP&A tooling documentation behind the module.

## How this module fits

The module sits on the accrual-basis vocabulary from [`mod-101`](../mod-101-startup-accounting-foundations/README.md) (P&L / balance sheet / cash-flow / deferred revenue / bookings vs. billings vs. revenue vs. cash) and consumes the cohort table and unit-economics outputs from [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/README.md) (cohort retention becomes the retention driver, fully-loaded CAC becomes the CAC driver, gross-margin bridge feeds the gross-margin driver, NRR / GRR become expansion / contraction drivers).

The model this module builds is the input to almost every subsequent module: [`mod-106`](../mod-106-startup-valuation-frameworks/) (the DCF and revenue-multiple valuations run off the forecast this module produces), [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/) (the model is a required data-room artefact and the "what round size and what use of proceeds" question is answered by running the scenarios), [`mod-109`](../mod-109-runway-management-and-bridge-financing/) (runway management is a live re-forecast of this model as actuals come in and assumptions move), and [`mod-110`](../mod-110-board-and-investor-governance-for-the-cfo/) (the board-pack KPI dashboard is the dashboard this module builds, and the quarterly re-forecast is a versioned rebuild of this model).

The module *does not* teach: cohort-table construction (that is `mod-102`), valuation-method application (that is [`mod-106`](../mod-106-startup-valuation-frameworks/)), or the FP&A platform-selection decision at growth stage in detail (that is a Series-B+ question addressed at CFO-decision level in [`mod-111`](../mod-111-finance-operations-controls-and-team-design/)). It teaches how a CFO builds and defends the monthly-reconciled, driver-based, scenario-capable three-statement model — the artefact everything downstream consumes.
