# Exercise 03 — Bookings, Billings, Revenue, Cash Reconciliation

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 3 (bookings, billings, revenue, cash) and exercise 01.

## Problem statement

Reconcile the four SaaS numbers — bookings, billings, revenue, cash — for a real or hypothetical startup's quarter. Produce a single quarter-end reconciliation view that shows all four side-by-side, explains why they differ, and traces the differences through the balance-sheet working-capital accounts. Produce a one-page CFO commentary explaining the quarter to a board.

The goal is the ability to explain a quarter using all four numbers rather than one. After this drill, if a board member says "I thought you had a $2M quarter but revenue is $400K — what happened?" you should be able to answer in three sentences.

## Scenario

Use the same startup and quarter as exercise 01 (either extend exercise 01's contract register or start fresh with the same shape requirements). For this drill, add:

- At least one contract signed in the quarter with a signature in month 3 that will not bill until the following quarter's month 1 (per its billing terms)
- At least one contract with milestone billing (e.g., 25% at signature, 25% at go-live, 50% at year-end)
- At least one enterprise contract with net-60 payment terms (customer pays 60 days after invoice)
- At least one contract renewal (a customer whose annual contract renewed during the quarter)
- One customer that churned during the quarter (contract terminated; note the terms — pro-rata refund of unearned deferred revenue? no refund? penalty?)

## Requirements

Produce the following:

1. **Quarterly contract-activity register.** For every contract active at any point in the quarter, columns for: customer, ACV (or MRR × 12), contract signature date, billing terms, invoice(s) issued in the quarter with dates and amounts, cash receipt(s) in the quarter with dates and amounts, service delivery pattern (start date, end date, any go-live delay), renewal or churn events.
2. **Per-metric computation.**
   - **Bookings for the quarter** — total ACV (or TCV, per your reporting policy — state which and be consistent) of contracts signed in the quarter. Break out new-logo bookings vs. expansion bookings vs. renewal bookings.
   - **Billings for the quarter** — sum of invoices issued in the quarter, from the contract-activity register.
   - **Revenue for the quarter** — ASC 606 revenue recognised in the quarter (from exercise 01's or exercise 02's methodology).
   - **Cash for the quarter** — sum of customer cash receipts in the quarter (net of refunds).
3. **Balance-sheet plumbing view.** Beginning and ending balances for AR, deferred revenue (short-term and long-term), and unbilled contract assets. Compute the deltas.
4. **Reconciliation table.** A single table with the four metrics for the quarter, side-by-side, plus the differences between adjacent metrics, plus the balance-sheet accounts that carry each difference:
   - Bookings − Billings = new signed value not yet invoiced this quarter (contributes to backlog / RPO; may create contract assets if revenue recognised before billing)
   - Billings − Revenue = change in deferred revenue (billed but not yet earned)
   - Revenue − Cash = change in AR (earned but not yet collected) minus write-offs
5. **RPO / backlog computation (optional but recommended).** RPO at quarter-end = Deferred revenue + Unbilled backlog on signed contracts. Show the arithmetic.
6. **CFO commentary (one page).** Written narrative explaining what happened this quarter in each metric — why bookings vs. billings diverged, why billings vs. revenue diverged, why revenue vs. cash diverged. Name the specific contracts driving each divergence. Frame the commentary so a board member reading only this page understands the quarter's shape.

## Starter guidance

- Bookings, billings, revenue, and cash are all *period* metrics measured over the quarter. ARR is a *point-in-time* metric measured at quarter-end. Do not confuse them.
- The reconciliation identities are:
  - Ending deferred revenue = Beginning deferred revenue + Billings − Revenue ± modifications
  - Ending AR = Beginning AR + Billings − Cash collected − Write-offs
- The bookings-to-billings gap does not sit on the balance sheet unless the contract is billed in a future period and the current period recognised revenue (in which case, a contract asset). If everything signed this quarter will be billed next quarter, the gap is invisible on the balance sheet; it lives in the CRM as future billings.
- For the CFO commentary, avoid the failure mode of "bookings were $X, billings were $Y, revenue was $Z, cash was $W" — restate what a board member already sees. Instead, explain *why* they diverged.

## Acceptance criteria

- **All four metrics are computed and stated.** No conflation of any two.
- **Reconciliation identities tie.** Deferred-revenue delta = billings − revenue (± any modifications, called out explicitly). AR delta = billings − cash collected − write-offs.
- **Each divergence is attributed to specific contracts.** The commentary names the contract or the pattern (e.g., "Contract X signed in March under our new annual-prepay incentive drove $Y of the billings-to-revenue divergence").
- **RPO is computed if backlog exists.** For a business with multi-year contracts or with signed-but-not-billed backlog, RPO is not just the deferred-revenue balance.
- **The commentary would survive a board reading.** No jargon dumped without context; no unexplained metric.

## Deliverables

- Spreadsheet with the contract-activity register, per-metric computation, reconciliation table, and balance-sheet plumbing view.
- One-page CFO commentary (Markdown or PDF).

## Extensions (optional)

- Extend to a full year (four quarters) and show how the four metrics diverge and reconverge across the year for an annual-prepay-heavy business. Plot the four series on one chart.
- Introduce a large one-time enterprise deal in month 3 of the quarter with a $500K annual-prepay component and separately-billed $200K implementation. Walk how the four metrics all move differently.
- Recompute the four metrics under a hypothetical policy change — the sales team shifts from annual-prepay-preferred to monthly-billed-preferred. Show the near-term impact on each metric and on deferred revenue.
