# Month-End Close Design and the Five-Business-Day Target

## Why this matters

The monthly close is the finance function's heartbeat. It is the process that turns a month of transactions into a P&L, a balance sheet, and a cash-flow statement that reconcile to each other and are trusted by the CFO, the board, and eventually the auditor. Every downstream artifact — the monthly investor update (mod-110 chapter 1), the board pack (mod-110 chapter 2), the actuals-vs.-plan variance (chapter 2 of this module's FP&A layer), the audit workpapers (chapter 4 of this module) — sits on top of the close.

The specific target that separates the pre-Series-A finance function from the Series-A-and-later one is the **5-business-day close**. Before Series-A, a company can close in 15-25 business days and no one downstream notices. From Series-A on, a board that wants the September flash by October 8 (business day 6) and the September book close by October 8 (business day 6) is asking for the whole close in five business days. A finance function that cannot deliver at that cadence produces late board packs, late investor updates, and late variance analysis — and the CFO's calendar gets consumed reconciling closing entries when it should be doing capital-allocation work.

The 5-day close is not primarily about speed. It is about *discipline* — every subledger reconciled, every accrual booked with support, every cutoff verified. A company that runs a 5-day close cleanly can extend to a 3-day close (the pre-IPO / public-company target) with tooling and headcount; a company that runs a slow-and-messy 25-day close cannot fix it by adding tooling because the underlying discipline is not installed.

## The close as a process, not an event

The close is one workflow with a well-defined start (the end of the accounting period) and end (the reviewed and reported financial statements). It has five stages, each with owned tasks and deliverables. Naming the stages, mapping each task to a stage and an owner, and running the close as a project with a daily standup is the discipline that produces the 5-day target.

**Stage 1 — Sub-ledger cutoff (Business Day 1-2).** Every sub-ledger that feeds the GL is *closed* — no more entries backdated into the closed month.
- Payroll cutoff and reconciliation (Rippling / Gusto → GL).
- AP cutoff (Bill.com / Ramp bill-pay closed for the month).
- AR / billing cutoff (Stripe / Chargebee closed and revenue-recognition run).
- Corporate-card cutoff (Ramp / Brex statement close and coding review).
- Bank cutoff and cash reconciliation (bank statements match GL cash).
- Deferred-revenue subledger cutoff — every contract's remaining performance obligation snapshot as of month-end.

**Stage 2 — Accruals and cutoff entries (Business Day 2-3).** The month-end journal entries that turn cash-timing into accrual-timing.
- Accrue unpaid vendor invoices received for services rendered in the month (accrued liabilities).
- Accrue employee wages / commissions / bonuses / PTO earned but not yet paid.
- Accrue prepaid expense amortisation (insurance, subscriptions, retainers).
- Accrue depreciation on fixed assets (per the fixed-asset schedule).
- Accrue amortisation of intangible assets (capitalised software, acquired IP).
- Accrue stock-based compensation expense (per the ASC 718 waterfall from Carta / Shareworks).
- Book the revenue-recognition journal (from the subledger — turns billings into ratable revenue and updates deferred-revenue liability).
- Book cost-of-revenue matching entries (hosting invoices from the coming month that relate to services delivered in the closing month, per matching principle).
- Book any customer-refund / credit-note entries with proper reversal of prior revenue.
- Book FX revaluation entries for non-functional-currency balance-sheet accounts.

**Stage 3 — Trial balance and self-reconciliation (Business Day 3-4).** The controller reviews the trial balance, runs the roll-forward checks, and clears the exceptions.
- **The five reconciliations** — every balance-sheet account must reconcile: cash (bank statement → GL), AR (aging → GL), AP (aging → GL), deferred revenue (subledger roll-forward → GL), and accrued liabilities (support schedule → GL). Every unreconciled account is either a bookkeeping error or an unrecorded transaction.
- **The roll-forward tests:** beginning AR + billings − cash collected = ending AR; beginning deferred revenue + billings − revenue recognised = ending deferred revenue; beginning accumulated depreciation + depreciation expense = ending accumulated depreciation.
- **The tie-outs:** cash on balance sheet = ending cash on cash-flow statement; retained earnings = beginning retained earnings + net income; total equity balances against issued capital plus retained earnings plus stock-based comp APIC.
- **Cutoff testing:** the first invoice of the following month is dated after the close date; the last invoice of the closing month is dated before the close date; large purchases and large customer bookings around period-end are reviewed for cutoff correctness.

**Stage 4 — Review and P&L / balance-sheet analytics (Business Day 4-5).** The Head of Accounting or CFO reviews the closing package and signs off.
- **Variance walk:** every P&L line variance vs. prior month and vs. plan explained; large unexplained variances chased before sign-off.
- **Balance-sheet review:** every material balance movement explained (why did AR grow 20% this month; why did prepaid expenses drop; why is accrued PTO $200K higher than last quarter).
- **Un-recorded liability review:** the AP / procurement team confirms any material vendor liability incurred but not yet invoiced was accrued.
- **Sign-off sheet:** each reconciliation and each accrual has a preparer and a reviewer signature (or e-signature in FloQast / Blackline). This is the audit trail chapter 4 will look at.

**Stage 5 — Reporting and distribution (Business Day 5-6).** The closed books produce the deliverables.
- **Internal financial package:** P&L (actual vs. plan vs. prior month), balance sheet, cash-flow statement, KPI dashboard reconciled to the P&L (mod-110 chapter 2).
- **Board / investor update:** the flash goes to the CFO for review before it goes into the monthly investor update (mod-110 chapter 1) or the board pack (mod-110 chapter 2).
- **FP&A handoff:** the actuals hit the model, variance analysis begins, and re-forecast conversations start with each department head.

Business Day 6 lands the flash to the CFO and the FP&A team. Business Day 8-10 lands the monthly investor update to the cap table. Business Day 12-15 lands the board pack for a mid-month board meeting. The whole downstream cadence sits on the discipline of the close finishing by business day 5.

## What each sub-ledger owns

The close is only 5 days because each sub-ledger runs *itself* — the AP owner produces the AP aging and the AP accrual, the payroll owner produces the payroll reconciliation, the revenue-ops or billing owner produces the revenue-recognition journal — and the controller's job is to *integrate* those into the trial balance, not to *produce* them.

- **AR / billing owner** produces the AR aging, the billings summary, the deferred-revenue roll-forward, and the revenue-recognition journal.
- **AP owner** produces the AP aging, the accrued-liability schedule, and the vendor payment run.
- **Payroll owner** produces the payroll reconciliation, the accrued-payroll / accrued-PTO schedule, the ESPP / 401k / benefit accrual entries, and the stock-based-compensation journal (from Carta / Shareworks).
- **Treasury owner** produces the bank reconciliations for every operating account, the investment-account reconciliations, and the FX revaluation.
- **Fixed-asset owner** (often the controller directly at Series-A/B) produces the depreciation / amortisation journal and the fixed-asset roll-forward.
- **Tax owner** (often outsourced at Series-A/B) produces the sales-tax accrual, the income-tax provision, and the R&D-credit-related entries.

At Series-A/B, the owners are one or two people wearing multiple hats. At Series-C+, each sub-ledger has a dedicated senior manager / accountant. The naming and the accountability do not change with team size — every close task has *one* owner, one preparer signature, and one reviewer signature.

## The close calendar as a shared artifact

The close calendar is the single most useful artifact the finance team maintains. Format:

- Every close task, listed row by row.
- Owner (name), reviewer (name), stage (1-5), target completion (business day).
- Status column updated live during the close: not-started / in-progress / prepared-not-reviewed / reviewed / complete / blocked.
- Blocker column: what is waiting on what.

FloQast, Blackline, Numeric, or a shared Google Sheet all work at the Series-A/B scale. At Series-B+ the FloQast / Blackline / Numeric investment pays for itself in reviewer-sign-off audit-trail alone.

Daily standup during the close (10-15 min, 9am, whole team) walks the calendar: what is completed since yesterday, what is on today, what is blocking. This is the same daily-standup pattern engineering teams use for sprints, and it works for the same reason.

## Cost-of-revenue matching — the failure mode

The single most common close error at Series-A/B is *cost-of-revenue matching failure* — the hosting invoice arrives in the following month covering services consumed in the closing month, and either (a) it is booked in the following month (understating cost of revenue in the closing month and inflating gross margin), or (b) it is booked correctly against the closing month but without support and the auditor flags it as an unsupported accrual.

The correct pattern: **cost of revenue is accrued to the period in which the revenue was earned, regardless of invoice timing.** This means the closing-month accrual includes an estimate of AWS / GCP / Azure hosting for the closing month (based on the mid-month usage report or the prior-month invoice as proxy), an estimate of Twilio / SendGrid / Segment usage, an estimate of the third-party data / API costs baked into unit economics. When the actual invoice arrives, it clears the accrual with any true-up going to the following month.

This is not optional past Series-A. A gross-margin metric that fluctuates with vendor billing timing rather than actual unit economics is unusable for board reporting or unit-economics analysis (mod-102).

## Deferred-revenue schedule — the other failure mode

The second most common close error is the deferred-revenue schedule drifting out of tie with the GL. Root cause: contract modifications (upgrades, downgrades, cancellations, credits) are booked in the billing system but the deferred-revenue subledger is not updated with the same modification. Over 6-12 months the deferred-revenue subledger and the GL deferred-revenue balance diverge, and the auditor's roll-forward test in chapter 4 exposes the drift.

The correct pattern: **every contract modification triggers a subledger update in the same close cycle it is booked in billing.** Contract-level detail (customer, contract, start date, term, ACV, remaining performance obligation, monthly recognition amount) is maintained per contract. The subledger's remaining-performance-obligation balance rolls forward as:

```
Beginning RPO
  + New contracts signed and billed
  + Contract-modification adds
  - Contract-modification removes (downgrades, cancellations)
  - Revenue recognised
= Ending RPO
```

which must equal the GL deferred-revenue balance to the dollar. If it does not, the delta is either (a) an un-booked contract modification or (b) a revenue-recognition journal that was booked without a matching subledger movement. Both are diagnosable in one close cycle if the discipline is installed; both compound into a two-week reconciliation exercise if not.

## The close cadence by stage

- **PRE-SEED / SEED:** 15-25 business days on cash basis; the outsourced accountant produces the close on their schedule.
- **SERIES-A:** target 10 business days on accrual basis in the first six months post-Series-A, compressing toward 5 business days as the controller (hire #3) installs the discipline.
- **SERIES-B:** 5 business days on accrual basis. NetSuite (or Intacct) in place. Sub-ledgers reconciled. FloQast / Blackline / Numeric usually deployed by mid-Series-B.
- **SERIES-C:** 3-5 business days. Automation deep enough that reconciliations run themselves and the team's time is on analysis and review.
- **PRE-IPO / PUBLIC:** 3 business days for month-end, 4-6 business days for quarter-end (with the added 10-Q / 10-K workstream). Public-company close is a separately-orchestrated project on top of month-end (chapter 8).

## Handling the exceptions

The 5-day close breaks when an exception lands mid-close. Common exceptions and the disciplined response:

- **Bank reconciliation off by $X.** Do not force-plug. Trace the specific transaction; usually a duplicate deposit, a foreign-currency conversion timing difference, or a wire that hit the bank but not the GL yet. Fix root cause; if not resolvable in-close, book the unreconciled item to a suspense account, close the books, and clear the suspense next cycle with a written note.
- **AR aging shows a $250K balance for a customer that paid in the prior month.** Trace: the payment was applied to the wrong invoice. Re-apply, verify AR reconciles.
- **Revenue-recognition subledger produces a number different from the billing system's ARR report.** Verify: ARR is a snapshot of active-contract-run-rate; recognised revenue is a period integral. They *should* differ; the reconciliation reduces one to the other. If the CFO cannot walk the reconciliation, the process is broken and the auditor will flag it in chapter 4.
- **A prior-period entry needs to be corrected.** Depending on materiality, this is either an out-of-period adjustment (immaterial, corrected in the current period with a memo) or a restatement (material, formal restatement with disclosure). The Head of Accounting owns the call; the CFO is looped in for anything approaching quantitative materiality.

## Summary

- The close is a five-stage workflow: sub-ledger cutoff → accruals and cutoff entries → trial balance and reconciliations → review and analytics → reporting and distribution.
- The 5-business-day close is the Series-A-and-later target; the whole downstream cadence (flash, investor update, board pack, variance analysis, forecast refresh) sits on it.
- Each sub-ledger has one owner, one preparer signature, one reviewer signature; the controller *integrates*, does not *produce*.
- The two most common failure modes are cost-of-revenue matching failure (gross margin fluctuates with invoice timing) and deferred-revenue subledger drift; both are diagnosable in one close cycle if the discipline is installed.
- The close cadence compresses stage over stage: 15-25 days at pre-seed, 5 days at Series-B, 3 days at pre-IPO.

Chapter 4 turns to the auditor, who will read the last twelve months of closes.
