# Model Failures, Review Checklist, and When to Graduate off Spreadsheets

## Why this matters

Every practitioner who has spent time inside startup financial models has stories about broken ones — the model whose balance sheet was off by $12M and no one had noticed for six months; the model that showed 24 months of runway because a hard-coded cash injection had never been removed after the scenario was rejected; the model that produced two different ARR numbers for the same month on two different tabs. The failure isn't the model's fault. It's the failure of a review discipline.

This chapter installs two things: the taxonomy of common model failures with the signs to look for, and the review checklist a CFO runs before every board pack and every diligence hand-off. It closes with the CFO-level decision on when the model has outgrown a spreadsheet and needs to move to a purpose-built FP&A platform.

## The seven common failure modes

**1. Circular references without a documented intention.**

Symptom: the formula bar shows a cell whose formula references itself, directly or transitively. Excel or Google Sheets flags this with a `#REF!` or a status-bar warning ("iterative calculation is disabled"), *unless* iterative calculation has been enabled — in which case the sheet silently converges to a wrong number.

Cause: usually an accidental cross-reference — the P&L revenue line references the KPI dashboard's growth-rate cell, which references the P&L revenue line. Sometimes intentional (interest-on-cash tie, chapter 2), but every intentional circular should be documented on the cover tab.

Fix: trace the loop with Excel's `Trace Precedents` / `Trace Dependents` tools. Break the loop by extracting the calculation to a driver-tab formula that references only the assumption tab, not the P&L. If iterative calc must remain on for the interest-on-cash tie, document it and cap the iteration count at 100 with a convergence threshold of 0.001.

**2. Hard-coded numbers overwriting formulas.**

Symptom: a cell in a calculation tab (P&L, balance sheet, CFS, driver) contains a typed number instead of a formula. In a well-colour-coded model, this shows up as a blue cell in a black-cell region.

Cause: someone wanted a specific number to appear ("adjust Q3 revenue to $2.4M") and typed it in rather than tracing it back to the assumption that would produce it. The typed number now doesn't update on scenario changes; the balance sheet may no longer balance; the P&L doesn't reconcile to the cohort schedule.

Fix: find every hard-code in the calculation region (Excel: `Ctrl-A` on the P&L tab, then `F5` → Special → Constants → Numbers highlights them). Every one is a bug. Either restore the formula or update the assumption tab so the formula produces the desired number.

**3. Orphan tabs and orphan rows ("spreadsheet monkeys").**

Symptom: tabs in the workbook that no other tab references, rows in the driver tab that no other row references, calculations that produce numbers used nowhere. The model was refactored at some point and the old pieces were left in place "just in case."

Cause: models grow organically. A tab was useful for one analysis, then superseded, but nobody deleted it. Now the reviewer wonders whether the orphan is relevant, wastes time trying to figure it out, and eventually stops trusting the model.

Fix: use `Trace Dependents` on every tab's key output cells; if nothing external references a tab, delete or archive it. Same for rows within a tab. A tight model has 100% of its cells contributing to at least one output.

**4. P&L-to-cash-flow-statement mismatches.**

Symptom: the CFS operating-activities section starts with a net income number that doesn't match the P&L, or the CFS working-capital lines don't reconcile to balance-sheet movements.

Cause: the CFS was constructed by typing lines rather than being derived from the P&L and balance sheet. When the P&L changes (a scenario switch), the typed CFS doesn't update.

Fix: rebuild the CFS to reference the P&L (`Net_income[M]` from the P&L tab) and the balance-sheet movements (`AR[M] − AR[M-1]` from the balance-sheet tab). The CFS becomes a derived tab, not an authored one. Verify the reconciliation from chapter 1 — cash on the balance sheet ties to ending cash on the CFS every period.

**5. Opening-balance breaks between periods.**

Symptom: the balance-sheet closing balance in month M does not equal the opening balance in month M+1 for some line items. The balance-sheet identity may still hold within each period, but the continuity between periods is broken.

Cause: usually a hard-coded override in a month's balance-sheet cell. The next month's cell references the prior month's *formula* result, but the current month's cell has been typed over, so the chain is broken.

Fix: for every balance-sheet row, add a check row: `= Closing_balance[M-1] − Opening_balance[M]`. This should be zero for every period. Non-zero flags where the chain broke.

**6. Balance-sheet identity failures.**

Symptom: `Total assets − Total liabilities − Total stockholders' equity` is non-zero in one or more forecast periods. The three-statement model is not internally consistent.

Cause: a P&L movement (net income, SBC) landed without a corresponding balance-sheet counter-entry (accumulated deficit, APIC), or a balance-sheet movement (deferred revenue increase) landed without a corresponding P&L or CFS entry. The double-entry principle is violated somewhere.

Fix: work through the diagnostic tree. If accumulated deficit doesn't walk by net income, look for equity entries that landed in retained earnings instead of APIC (a fundraise proceed entered wrong). If deferred revenue doesn't tie to `bookings billed upfront − revenue recognised`, look at the revenue-recognition schedule. Every non-zero month has a specific broken link; the diagnostic is patient tracing.

**7. Version confusion — plan-of-record drift.**

Symptom: the "plan" cited in the board pack doesn't match the plan cited in the fundraise memo, which doesn't match the plan cited in the CEO's OKR document. Three versions, no single source.

Cause: no version-control discipline. Each time the model gets updated, the previous plan-of-record isn't archived, and each subsequent document authored from the model uses whatever the current-run number is.

Fix: at every plan cycle (annual plan; quarterly re-forecast), snapshot the plan-of-record as a locked-and-dated version (either a saved copy of the file, or a snapshot tab within the model). Every subsequent document cites the specific plan version. Plan-vs.-actual reporting compares actuals against the locked reference, not the current-run number.

## Additional failure modes worth naming

- **Wrong sign convention.** Cost of revenue entered as positive (should be negative to subtract from revenue), or working-capital movement direction inverted (an *increase* in AR is a *decrease* to cash, not the reverse). Rebuild the P&L or CFS section with a consistent sign convention documented on the cover tab.
- **Mismatched period conventions.** Some tabs use fiscal months (13-week quarters), others use calendar months. Reconcile every tab to the same period grid.
- **Broken external references.** Formulas linking to files not present, or to closed workbook cells. Excel shows `#REF!`; Google Sheets shows `#ERROR!`. Either fix the reference or replace with the underlying value.
- **Volatile function overuse.** `TODAY()`, `NOW()`, `RAND()`, `OFFSET()`, `INDIRECT()` recalculate on every workbook change and can slow large models to a crawl. Replace with static dates and index/match / xlookup where possible.
- **Merged cells in calculation regions.** Merged cells break formulas that reference cell ranges and cannot be filled with `Ctrl-D` / `Ctrl-R`. Never merge cells in a calculation region; header rows only.
- **Named-range collisions.** Two named ranges with the same name in different tabs, or a named range that shadows a built-in function. Use the Name Manager to audit and rename.

## The model-review checklist

The checklist a CFO runs before every model hand-off — board pack, fundraise, diligence, quarterly re-forecast. Organised by section, with each item being a specific check the reviewer can do in seconds.

### Structural checks

- [ ] **Tab order matches convention:** Cover → Assumptions → Drivers → Hiring → Funnel → Cohort → P&L → Balance sheet → CFS → Schedules → Scenarios → Sensitivity → Dashboard → Checks.
- [ ] **Every tab has a colour-coded key or references the workbook-level key on the cover tab.**
- [ ] **Cover tab documents:** model version, author, date, active scenario, iterative-calc status, and known issues.
- [ ] **Historical actuals region is clearly separated from forecast region** (a bold vertical line, coloured background, or a locked-cells convention).
- [ ] **No orphan tabs** — every tab feeds at least one downstream tab (verify with Trace Dependents on the tab's output cells).

### Assumption / driver checks

- [ ] **Every assumption cell is blue-formatted** (or the workbook's convention for user-editable inputs).
- [ ] **Every assumption has a unit label** (`$`, `%`, `months`, `count`, `bps`).
- [ ] **Every scenario-flexed assumption is in the scenario switch table**, not scattered across the assumption tab.
- [ ] **Driver-tab forecast cells are formulas only** (Ctrl-A on the tab, F5 → Special → Constants → Numbers highlights only historical actuals).
- [ ] **Cohort revenue schedule sums to total P&L revenue** for every month.
- [ ] **Hiring plan payroll sums to P&L payroll by department** for every month.

### Reconciliation checks (the three-plus-one)

- [ ] **Balance-sheet identity holds:** `Assets − Liabilities − Equity = 0` for every forecast month.
- [ ] **Cash on the balance sheet ties to ending cash on the CFS** for every forecast month.
- [ ] **Retained earnings walks forward by net income:** `RE[M] = RE[M-1] + NI[M]` for every forecast month.
- [ ] **Balance-sheet opening balances equal prior-period closing balances** for every line item, every month.

### Statement checks

- [ ] **P&L reconciles to itself:** revenue − COGS = gross profit; gross profit − opex = operating income; operating income + non-op − taxes = net income. Every subtotal correct.
- [ ] **Sign convention consistent** — costs are negative subtractions, working-capital movements follow the standard direction convention.
- [ ] **P&L annual sum matches the annual roll-up** on any annual summary tab.
- [ ] **Deferred revenue on the balance sheet reconciles** to `beginning balance + new billings upfront − revenue recognised = ending balance`.
- [ ] **Deferred contract costs (commissions) on the balance sheet reconcile** to `beginning + new capitalisations − amortisation = ending`.
- [ ] **PPE and intangibles net values reconcile** to `beginning + capex − depreciation = ending`, per asset class.

### Scenario and sensitivity checks

- [ ] **Scenario switch flips one cell and rippled correctly** — test by switching Base → Downside and verify at least 5 downstream cells changed as expected.
- [ ] **Every scenario has a named story documented** on the scenarios tab (2-3 sentences per scenario).
- [ ] **Sensitivity tables produce plausible ranges** — no `#DIV/0!`, no cash-out dates in year 40, no negative runways displayed as positive numbers.
- [ ] **Two-variable heatmap axes are the two dominant levers** from the single-variable sensitivity tables.

### Dashboard checks

- [ ] **Every KPI cell is a formula** with a documented source (comment or footnote).
- [ ] **Current-period ARR on dashboard equals sum of MRR × 12 from the P&L or cohort schedule** — exactly.
- [ ] **Current-period runway on dashboard equals cash / trailing-3-month net burn** — exactly.
- [ ] **Plan-vs.-actual column references the locked plan-of-record snapshot**, not the current-run number.
- [ ] **Charts source ranges are named ranges or structured references**, not hard-coded ranges that break when rows are added.

### Documentation

- [ ] **Methodology memo is present or referenced** — how CAC is defined, what "gross margin" includes, what SBC valuation method, what scenario stories.
- [ ] **Known limitations documented** — e.g., "cohort retention curve based on 14 months of history; extrapolation past month 14 is directional."
- [ ] **Change log for the current version** documents what changed since the prior version.

The checklist runs in 20-30 minutes for a familiar model. It is the last thing done before the model leaves the CFO's screen.

## The failure teardown as a training exercise

A CFO cannot become fluent in the checklist by reading it. The fluency comes from working through a broken model — identifying the specific failure by symptom, tracing to the cause, applying the fix, running the reconciliations. This is what exercise 7 in this module is for.

The pattern: given a deliberately broken model (some subset of the seven failure modes above), the reviewer produces (a) a diagnosis memo naming each failure, its symptom, its cause, and its fix; (b) a rebuilt model with all reconciliations holding; and (c) a review-checklist audit of the rebuilt model showing green on every item. The exercise teaches the pattern-recognition that reading cannot.

## When to graduate off spreadsheets — the CFO decision

Spreadsheet financial models (Excel, Google Sheets) work well for early-stage startups. They are cheap, universal, flexible, and every finance professional knows them. The rule of thumb: from IDEA-stage through Series-A, and often through Series-B, the three-statement model lives in a spreadsheet.

There is a stage — usually Series-B or later, sometimes earlier for companies with unusual model complexity — where the spreadsheet becomes the limiting factor. The signals:

- **The model takes >30 seconds to recalculate** on a modern laptop. Iteration cost is now high enough that scenario runs are painful.
- **More than 2-3 people need to edit the model concurrently.** Google Sheets multi-user works up to a point; concurrent edits on complex models produce merge conflicts and race conditions.
- **The FP&A team is spending >40% of its time on model maintenance** (formula debugging, tab reconciliation, version control) rather than on analysis.
- **The organisation has multiple entities, currencies, or subsidiaries** that need to be consolidated. Spreadsheet consolidation is brittle at scale.
- **The dashboard needs live actuals from the accounting system.** Spreadsheet integrations (Google Sheets IMPORTDATA, Excel Power Query, custom scripts) are possible but fragile; purpose-built tools have this as a native feature.
- **The board or investors want direct read-only access to a live model** rather than a periodic export. Spreadsheet models don't share well.
- **Version control is failing** — the "final v3 real final actual.xlsx" file naming problem has become endemic.

When three or more of these signals are present, it is time to evaluate an FP&A platform.

## The modern FP&A platform landscape

The category has consolidated and matured in the last decade. Four tiers of platform, each with different strengths:

**Native cloud (spreadsheet-successor) — best fit for early- to mid-stage startups.**

- **[Causal](https://www.causal.app/)** — cloud-first, formula-driven, treats time as a first-class dimension. Strong scenario/sensitivity story; native Monte Carlo modelling. Fits Series-A through Series-C.
- **[Runway](https://runway.com/)** — Series-A through Series-B, positioned as a spreadsheet successor with strong version control and multi-scenario modelling. Emphasis on operational-model integration.
- **[Mosaic](https://www.mosaic.tech/)** — Series-B onward, closer to a lightweight EPM (enterprise performance management) with integrated dashboarding, workforce planning, and actuals-connectors to accounting systems.

**Established mid-market — best fit for growth-stage.**

- **[Anaplan](https://www.anaplan.com/)** — mid-market to enterprise. Multi-dimensional modelling language (Hyperblock); strong for large, multi-entity organisations. Requires implementation partner; heavy configuration.
- **[Workday Adaptive Planning](https://www.workday.com/en-us/products/adaptive-planning/overview.html)** (formerly Adaptive Insights) — mid-market to enterprise, strong actuals-integration to Workday and other ERPs. Heavy but proven.
- **[Vena](https://www.venasolutions.com/)** — Excel-native workflow layer on top of Excel; a compromise for teams that want tooling capabilities without leaving Excel.

**Enterprise / legacy — best fit for very large companies.**

- **[Oracle Hyperion / EPM Cloud](https://www.oracle.com/performance-management/)** — enterprise-scale, heavy implementation.
- **[SAP BPC / Analytics Cloud](https://www.sap.com/products/technology-platform/cloud-analytics.html)** — enterprise-scale, tight ERP integration for SAP-heavy organisations.
- **[IBM Planning Analytics](https://www.ibm.com/products/planning-analytics)** (formerly Cognos TM1) — enterprise-scale, multi-dimensional modelling.

**Startup-native and adjacent — narrower use cases.**

- **[Pry](https://www.pry.co/)** (acquired by Brex) — targeted at very-early-stage startups; simple cash-flow forecasting.
- **[Finmark](https://www.finmark.com/)** — targeted at Seed / Series-A; automated three-statement modelling and cash forecasting.
- **[Jirav](https://www.jirav.com/)** — SMB / small business, integrated with QBO / Xero.

## The buy decision — what to evaluate

When evaluating an FP&A platform, the CFO's decision criteria:

- **Data integration.** Can the platform pull actuals from the accounting system, HRIS, CRM, and billing system automatically? Manual data loading defeats a large part of the tooling's value.
- **Modelling flexibility.** Can the platform express the model's specific driver logic, or does it force a template? A rigid template that doesn't match the business creates two systems of record — the "official" tool and the shadow spreadsheet the CFO actually trusts.
- **Multi-user and permissioning.** Can multiple people edit different parts of the model concurrently? Can departments own their own budget line items with the CFO approving?
- **Scenario / sensitivity native.** Are scenarios and sensitivities first-class features, or are they retrofitted on top of a single-scenario model?
- **Reporting and dashboarding.** Does the platform produce the board-ready reports natively, or does it require export to another tool?
- **Implementation cost.** Enterprise platforms (Anaplan, Adaptive, Oracle) typically require $50-250K+ of implementation partner fees plus $50-500K annual licence. Startup-native platforms are $10-50K annual licence with lighter implementation.
- **Migration cost.** Migrating a working spreadsheet model to a platform is a 2-6 month project depending on complexity. The migration must produce reconciled outputs against the spreadsheet; otherwise the CFO cannot trust the transition.

## The buy-vs.-defer decision — the failure mode in either direction

Both directions of the decision have failure modes.

**Buying too early.** The company spends $150K on a platform and 4 months of implementation for a model that could have lived in Google Sheets for another two years. The FP&A team's time is consumed by implementation rather than analysis. The platform's rigidity forces the model into a template that doesn't quite fit, and the CFO reverts to a shadow spreadsheet within a year.

**Buying too late.** The company is at Series-C, the model has 40+ tabs, the FP&A team spends most of its time debugging formula errors, the board pack is authored 3 days after the target date every quarter because the model refresh takes so long. The platform migration that should have happened 18 months ago is now an urgent-and-large project because too much has been built on the wrong foundation.

The middle path: a CFO who has read the signals list above and has a written trigger for evaluation ("we will evaluate FP&A platforms when 3 of the 7 signals are present") is likely to make the buy decision at the right time. A CFO who has no written trigger tends to buy too early (a category peer bought a tool and it looks impressive) or too late (the pain is so slow-boiling that no single moment triggers the decision).

## Summary

- The seven common model-failure modes: undocumented circular references, hard-coded overrides in calculation cells, orphan tabs and rows, P&L-to-CFS mismatches, opening-balance breaks between periods, balance-sheet identity failures, and version-of-record drift.
- The model-review checklist runs in 20-30 minutes and covers structure, assumptions, reconciliations, statement integrity, scenarios, dashboard, and documentation. Every model hand-off — board pack, fundraise, diligence — runs the checklist.
- The failure teardown exercise (exercise 7 in this module) builds the pattern-recognition that reading the checklist alone doesn't produce.
- Spreadsheets are appropriate from IDEA-stage through Series-A, and often through Series-B. Beyond that, seven signals accumulate — recalculation time, concurrent-edit needs, FP&A time-on-maintenance, multi-entity consolidation, live actuals, external access, version-control failure — that trigger the platform-evaluation decision.
- The FP&A platform landscape has four tiers: native cloud (Causal, Runway, Mosaic) fits early- to mid-stage; established mid-market (Anaplan, Adaptive, Vena) fits growth-stage; enterprise/legacy (Hyperion, SAP BPC, IBM Planning Analytics) fits very large companies; startup-native (Pry, Finmark, Jirav) targets pre-Series-A and lightweight use cases.
- Evaluation criteria: data integration, modelling flexibility, multi-user, native scenarios, reporting, implementation cost, migration cost. Both buying too early and buying too late are failure modes; the middle path is a written trigger tied to the seven signals.

This closes the module. The exercises apply the concepts — driver architecture, hiring-plan integration, funnel integration, reconciliation, scenarios, dashboard, review checklist — to build a working three-statement model that survives Series-A diligence.
