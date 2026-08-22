# Three-Statement Architecture and Monthly Reconciliation

## Why this matters

The founder-authored "financial model" a Series-A investor sees most often is a P&L that projects revenue growth and opex against it, produces a monthly net-income line, and derives a runway number by dividing cash balance by average burn. There is no balance sheet. There is no cash-flow statement. The cash number driving runway is guessed, not built. When the investor asks *"walk me through the working-capital assumption behind the Q3 cash trough,"* the founder cannot answer, because the model does not have working capital — it has revenue, opex, and a plug.

A three-statement model — P&L, balance sheet, and cash-flow statement built together on the same monthly grid — is the artefact that answers the question. Cash is not guessed; it is derived, month by month, from operating activity plus working-capital movement plus investing activity plus financing activity, and the derived cash on the cash-flow statement ties to the cash line on the balance sheet, which ties to the opening-balance cash from the prior month. If any of those three ties break, the model is broken, and the runway number the CEO puts in front of the board is fiction.

This chapter installs the architecture: the monthly grid, the three statements as three views of the same underlying transactions, and the three reconciliation checks that prove the model is internally consistent. Everything else in the module — drivers, hiring plan, GTM funnel, scenarios, dashboard — assumes this architecture exists and holds.

## The monthly grid

CFO-grade startup models are built on a monthly grid. Quarterly is what a board deck usually shows; annual is what a long-range plan usually shows; monthly is the resolution at which the model *lives*. The three reasons monthly is non-negotiable:

- **Hiring hits the P&L monthly.** A senior engineer who starts on 15 March produces half a month of payroll in March. Modelling annually rounds the start date to a full year and misses the first-year burn.
- **Revenue recognises monthly.** An annual prepay contract signed in April recognises 9/12 of the ACV in year one, unwinding one month at a time from deferred revenue. Modelling annually loses the deferred-revenue balance sheet movement entirely (see [`mod-101`](../mod-101-startup-accounting-foundations/04-deferred-revenue-liability.md)).
- **Runway is a monthly count.** "How many months until we run out of cash under the current plan" cannot be answered at annual resolution. The cash trough that determines the fundraise timing is usually two or three months before year-end, and the annual model averages over it.

The grid is columns; the rows are the P&L, balance sheet, and cash-flow-statement line items plus every driver row that feeds them. Historical actuals sit in the leftmost columns; forecast periods sit to the right. A 24-36-month forward horizon is the usual working length — enough to see through the current round to the next, without extending into speculation the model can't support.

Every tab in the model shares this grid. The hiring plan is a monthly grid of hires. The GTM funnel is a monthly grid of leads. The P&L is a monthly grid of revenue and opex. If two tabs disagree on what "month 15" means, formulas will silently pick the wrong column and the reconciliations will fail.

## The three statements as three views of the same transactions

Every economic event in a startup produces entries on more than one statement. The three-statement model exists because looking at any one statement in isolation misses two-thirds of the picture.

**Signing a $120K annual prepay contract on 1 April.** On the P&L: recognise $10K of revenue in April, $10K/month for the remaining 11 months. On the balance sheet: cash increases by $120K, deferred revenue (a liability) increases by $120K, then decreases by $10K/month as revenue recognises. On the cash-flow statement: $120K of cash from operating activity in April (the $10K of revenue plus a $110K increase in deferred revenue as a working-capital source), then $0 of incremental cash-flow impact in subsequent months (the $10K of revenue is offset by a $10K reduction in deferred revenue). A P&L-only model shows $10K of revenue per month; the CFO's model shows the $120K cash bulge in April and the working-capital unwind against it.

**Hiring a senior engineer at $250K fully-loaded on 1 May, paid semi-monthly.** On the P&L: $20.8K of R&D opex per month from May onward. On the balance sheet: accrued payroll increases and decreases within the month as pay days pass; cash decreases with each payroll cycle. On the cash-flow statement: operating cash outflow of $20.8K/month starting in May (the P&L expense plus the small working-capital movement in accrued payroll). If the engineer capitalises software-development costs under ASC 350-40, some of that cost lands on the balance sheet as an intangible asset and unwinds via amortisation on the P&L over subsequent periods — the same underlying transaction with a different accounting treatment produces a different balance-sheet and cash-flow shape.

**Paying a $60K annual sales commission on 15 May for a contract signed in April.** On the P&L: under ASC 340-40, the commission is capitalised as a deferred contract cost and amortised over the expected customer life; if the customer life is 36 months, that's $1.67K/month of amortisation as S&M expense from April onward. On the balance sheet: cash decreases by $60K on 15 May, deferred contract cost (an asset) increases by $60K on 15 May, then amortises down by $1.67K/month. On the cash-flow statement: $60K of cash outflow in May (the small amortisation expense on the P&L plus a large increase in the deferred contract cost asset as a working-capital use). A P&L-only model shows a smooth $1.67K/month line; the CFO's model shows the $60K cash shock in May.

These three examples are enough to make the point: the transactions the CFO cares about — signing customers, hiring people, paying commissions, buying servers, raising rounds — do not fit into a P&L. They fit into a three-statement view. If the model is P&L-only, the CFO is guessing about cash.

## The three statements — starting shape

**P&L (income statement)** for each forecast month:

```
Revenue                                       ← from the GTM funnel / cohort retention (chapter 4)
  − Cost of revenue                           ← from the cost-to-serve driver × units
= Gross profit
  − Sales & marketing                         ← from the hiring plan (chapter 3) + non-payroll S&M
  − Research & development                    ← from the hiring plan + non-payroll R&D
  − General & administrative                  ← from the hiring plan + non-payroll G&A
= Operating income (loss)
  ± Interest income / interest expense        ← from cash balance × yield − debt balance × rate
  − Taxes                                     ← usually zero for a loss-making startup
= Net income (loss)
```

**Balance sheet** at each forecast month-end:

```
Assets
  Cash & cash equivalents                     ← plug that ties to CFS ending cash
  Accounts receivable (AR)                    ← derived from revenue × DSO driver
  Prepaid expenses                            ← from prepaid-schedule driver
  Deferred contract costs (ST + LT)           ← from deferred-commission amortisation schedule
  Property & equipment (net)                  ← from capex schedule − accumulated depreciation
  Intangibles / capitalised software (net)    ← from cap-software schedule − amortisation
  Right-of-use assets (leases)                ← if ASC 842 is in scope
  Other assets

Liabilities
  Accounts payable (AP)                       ← derived from operating expense × DPO driver
  Accrued liabilities                         ← from payroll cycle + accrual schedules
  Deferred revenue (contract liability)       ← from bookings − revenue recognised
  Debt (venture debt, notes, term loans)      ← from debt schedule
  Lease liabilities                           ← if ASC 842 is in scope
  Other liabilities

Stockholders' equity
  Preferred stock (by series)                 ← from cap-table schedule
  Common stock                                ← from cap-table schedule
  Additional paid-in capital (APIC)           ← from financing rounds + option exercises
  Accumulated deficit                         ← walks by net income each period
```

The identity `Assets = Liabilities + Stockholders' equity` must hold every period.

**Cash-flow statement** for each forecast month, indirect method (the standard SaaS presentation):

```
Cash from operating activities
  Net income                                  ← from the P&L
  + Depreciation & amortisation               ← from asset schedules
  + Stock-based compensation                  ← from the SBC schedule
  ± Changes in working capital
      − Increase in AR                        ← − Δ AR
      − Increase in prepaid expenses          ← − Δ prepaid
      − Increase in deferred contract costs   ← − Δ DCC
      + Increase in AP                        ← + Δ AP
      + Increase in accrued liabilities       ← + Δ accrued
      + Increase in deferred revenue          ← + Δ deferred revenue
= Cash from operating activities              ← "CFO" in the presentation (not to be confused with the officer)

Cash from investing activities
  − Capex                                     ← from capex schedule
  − Capitalised software                      ← from cap-software schedule
  + Sale of investments / assets              ← from investing schedule
= Cash from investing activities              ← "CFI"

Cash from financing activities
  + Proceeds from equity issuance             ← from financing rounds
  + Proceeds from debt                        ← from debt schedule
  − Debt repayment                            ← from debt schedule
  + Proceeds from option exercises            ← from cap-table schedule
= Cash from financing activities              ← "CFF"

Net change in cash                            ← CFO + CFI + CFF
+ Opening cash                                ← prior period's ending cash
= Ending cash                                 ← must tie to cash on the balance sheet
```

The two dozen driver-fed line items on the three statements are the entire scope of the model. Every one of them is derived from a driver on an assumptions / drivers / hiring / funnel tab. None of them is typed in directly.

## The three reconciliations that make it a model

A collection of tabs on a monthly grid does not constitute a three-statement model. Three specific ties must hold every period for the model to be internally consistent:

**Reconciliation 1: The balance sheet balances.** `Total assets − Total liabilities − Total stockholders' equity = 0` for every forecast column. This is the accounting identity and it is non-negotiable. A well-built model has a check row at the bottom of the balance-sheet tab that flags any period where the identity fails, coloured in a way that a reviewer's eye lands on it. In practice, the identity breaks when a P&L movement lacks a corresponding balance-sheet counter-entry — depreciation flows to opex without reducing PPE, deferred revenue changes without a corresponding cash or AR entry, an equity raise adds cash without adding APIC. A balance-sheet-imbalance check is the first thing you write and the last thing you look at.

**Reconciliation 2: Cash on the balance sheet ties to ending cash on the cash-flow statement.** The cash line on the balance sheet at the end of month M equals `Cash beginning of month + CFO + CFI + CFF` from the cash-flow statement for month M. If this tie fails, the cash-flow statement is wrong (a working-capital movement is missing or double-counted), or the balance sheet is wrong (a non-cash movement is not being flagged as non-cash). Write this check row on both tabs; both should flag zero every period.

**Reconciliation 3: Retained earnings walks forward by net income.** Retained earnings (or accumulated deficit) at the end of month M equals `Retained earnings beginning of month + Net income for month M`. Any period where this fails means either an equity-financing entry is landing in retained earnings instead of APIC, or a non-operating entry (a stock split, a one-time equity adjustment, a dividend — none of which usually apply to an early-stage startup) is happening without being modelled. This check catches most of the "the balance sheet is off by $47" mysteries.

A fourth, less canonical check that catches a common failure: **opening-balance continuity between periods.** The closing balance of every balance-sheet line item in month M equals the opening balance in month M+1. In practice this is enforced by construction — month M+1's balance-sheet formula references month M's closing balance — but a hard-coded override in one month breaks the chain and the closing-balance-vs.-next-opening tie is what surfaces it.

Every model tab has a row of check cells at the bottom, coloured red when non-zero. A reviewer scans the check row before reading anything else; a broken check disqualifies every number above it until fixed.

## Indirect method vs. direct method for the cash-flow statement

There are two conventions for building the cash-flow statement, both permitted under GAAP (see FASB ASC 230):

**Indirect method** starts from net income and walks to cash by adjusting for non-cash items (depreciation, amortisation, SBC) and changes in working capital. This is what almost every SaaS company presents on its 10-K and what almost every operating three-statement model uses. It is the presentation that lets the reviewer see *why* cash differs from net income — the working-capital movements are the reconciling items on the same page.

**Direct method** lists actual cash receipts and cash payments by category (cash received from customers, cash paid to suppliers, cash paid to employees). It is closer to what a payments dashboard shows, but is rarely used in SaaS reporting because reconstructing the categories requires either transaction-level access or a supplemental disclosure that adds complexity without changing the ending cash number.

Use indirect. Every diligence reviewer expects it, every FP&A tool defaults to it, and it is the presentation that makes the P&L-to-cash-flow reconciliation visible on the same page.

## What "reconciles monthly" actually means

The phrase gets thrown around loosely. Precisely:

- Every forecast month has all three statements produced from the same underlying driver set.
- The three reconciliations (balance-sheet identity, cash tie, retained-earnings walk) hold for every month.
- The opening balance of every balance-sheet line in month M+1 equals the closing balance in month M.
- The sum of monthly P&L lines across a quarter equals the quarterly P&L; across a year equals the annual P&L.
- The KPI dashboard (ARR, MRR, growth rate, burn, runway) is sourced from the monthly model; the quarterly and annual roll-ups are computed from the monthly grid, not typed in separately.

If you cannot answer "does the balance sheet balance in every forecast month" with a numerical proof from a check row, you do not have a monthly-reconciled model — you have a P&L with two extra tabs.

## Historicals as a load-bearing input, not a decoration

The forecast columns are the work product; the historical columns are the calibration input. Every driver has a historical trajectory: gross-margin % over the last 12 months, S&M-as-percent-of-revenue trending, ACV progression by cohort, cost-to-serve per unit trending, DSO drifting.

A model whose forecast drivers are unrelated to their historical values is guessing. A defensible model produces each forecast driver from a documented rule: "gross margin holds at the trailing-3-month average for the next 6 months, then improves by 50bps/quarter as we exit the hosting-migration project"; "S&M-as-percent-of-revenue drops from 65% to 55% over the forecast horizon as the outbound investment matures." These rules — the driver-forecasting logic — are documented on the driver tab (chapter 2).

The historical columns also drive the KPI dashboard's actuals-vs.-plan variance (chapter 7). The board pack that shows "Q2 revenue was $2.1M vs. plan of $2.4M" is running the actual number against the *original* forecast number, which requires versioning the model — snapshotting a plan-of-record and then forecasting forward from actuals.

## The tab list

A working three-statement startup model typically has this tab structure, in this order:

1. **Cover / README** — model version, date, author, scenario active, macro-warning ("iterative calculation intentionally on, see check row"), and a table of contents.
2. **Assumptions** — every user-editable input, one section per assumption category, colour-coded (blue-for-input is the near-universal convention; see chapter 8).
3. **Drivers** — every derived driver, sourced from assumptions with a documented rule.
4. **Hiring plan** — every planned hire, per month, with role / start date / fully-loaded cost / department (chapter 3).
5. **GTM funnel** — the leads → MQL → SQL → close-won × ACV funnel (chapter 4).
6. **Cohort revenue schedule** — bookings × cohort retention → recognised revenue by month.
7. **P&L** — monthly income statement.
8. **Balance sheet** — monthly balance sheet.
9. **Cash-flow statement** — monthly indirect-method CFS.
10. **Supporting schedules** — depreciation, amortisation, capex, capitalised software, deferred contract costs (commissions), debt, cap-table / SBC, lease.
11. **Scenarios** — scenario switch and per-scenario input overrides (chapter 6).
12. **Sensitivity** — single-variable and two-variable sensitivity tables (chapter 6).
13. **KPI dashboard** — the board-ready dashboard (chapter 7).
14. **Checks** — a consolidated check tab pulling every reconciliation check row into one place.

Order matters — inputs before outputs, drivers before statements, statements before dashboard, checks last. A reviewer navigates by tab order; a chaotic order signals a chaotic model.

## Summary

- CFO-grade startup models are built on a monthly grid because hiring, revenue recognition, and runway are all monthly phenomena that annual resolution loses.
- The three statements are three views of the same underlying transactions; a P&L-only model cannot answer the working-capital questions a Series-A investor asks.
- The three reconciliations that turn a set of tabs into a model: the balance-sheet identity holds; cash on the balance sheet ties to ending cash on the CFS; retained earnings walks by net income each period. A fourth check on opening-vs.-closing continuity catches most hard-coded overrides.
- Use the indirect method for the CFS — it is what every SaaS 10-K uses, what every FP&A tool defaults to, and the presentation that makes the P&L-to-cash reconciliation visible on one page.
- "Reconciles monthly" is a precise claim: every month, all three statements produced from the same drivers, all three reconciliation checks holding, opening balances continuous, roll-ups computed not typed.
- Historical columns calibrate the driver rules; the forecast columns apply those rules forward. A model whose forecast drivers are disconnected from history is guessing.
- The tab list has a canonical order — inputs → drivers → hiring & funnel → cohort revenue → statements → schedules → scenarios & sensitivity → dashboard → checks. Order signals discipline.

Chapter 2 turns to the assumption and driver tabs — the layer that keeps every statement cell derived rather than typed.
