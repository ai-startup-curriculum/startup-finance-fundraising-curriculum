# Exercise 03 — Month-End Close Checklist Authoring

**Estimated time:** ~3 hours
**Prerequisites:** Chapters 1-3 (stack selection, first-ten hires, month-end close design).

## Problem statement

Author the day-by-day close checklist that a Series-A SaaS company would run to hit a 5-business-day close target. The checklist covers all five close stages (sub-ledger cutoff, accruals and cutoff entries, trial balance and reconciliations, review and analytics, reporting and distribution), names owner and reviewer per task, cites the source ledger / subledger / system for each task, and quantifies the cutover from a 10-business-day close (typical Series-A landing pattern) to the 5-business-day target.

The goal is to produce a runnable operating artifact — something a controller could literally hand to their AP owner, revenue-ops owner, and payroll owner on business day 1 and expect back on business day 5.

## Scenario — build your own

Construct (or use a real one) a Series-A SaaS company with the following minimum shape:

- ~$8M ARR, ~50 employees, ~180 active customer contracts.
- Billing on Stripe with a mix of monthly and annual-prepay.
- GL on QBO or Xero (pick one).
- AP on Ramp bill-pay + Brex corporate cards (or equivalent).
- Payroll on Rippling or Gusto (pick one).
- Bank operating account at Mercury or Brex, plus a treasury / MMF account.
- Deferred-revenue subledger currently in a Google Sheet, ~1,200 active contract-months tracked.
- One outsourced accounting firm engagement in place for month-end close review and quarterly tax provision; a controller was hired 6 months ago and is the primary close owner.
- No international subsidiary yet.

Optional adjustments: add a small international entity, add usage-based revenue on top of subscription, or add a services / implementation revenue stream that triggers separate performance-obligation identification under ASC 606.

## Requirements

Produce the following artifacts.

### Artifact 1 — The close calendar

A spreadsheet with one row per task, and columns:

- Task ID (FIN-CLOSE-XXX)
- Task description
- Close stage (1 sub-ledger cutoff / 2 accruals / 3 trial balance / 4 review / 5 reporting)
- Owner (name or role)
- Reviewer (name or role)
- Source system / sub-ledger (Stripe, Ramp, Rippling, bank, Carta, etc.)
- Preparer target completion (business day)
- Reviewer target completion (business day)
- Evidence produced (schedule, journal entry, reconciliation, sign-off)
- Dependency (task IDs that must complete first)

Target minimum: 40-60 tasks across the five stages.

### Artifact 2 — The visual close-calendar (Gantt-style)

Business days 1 through 6 on the x-axis, task categories on the y-axis (sub-ledger owners, accountant team, controller, CFO), with each task as a coloured bar. Overlays: the daily 9am close-standup, the CFO review milestone (end of business day 4), the flash-to-CFO milestone (end of business day 5), the flash-to-board / investor-update-drafting milestone (business day 6).

### Artifact 3 — The five reconciliations template

For the five load-bearing reconciliations from chapter 3 (cash, AR, AP, deferred revenue, accrued liabilities), produce a template reconciliation format that:

- Names the beginning-balance source and the ending-balance source.
- Walks the roll-forward: beginning + additions − reductions = ending.
- Includes a variance / exception field with categorical options (timing / classification / cutoff / posting error / unresolved).
- Requires preparer and reviewer sign-off with date and name.

### Artifact 4 — The cost-of-revenue and deferred-revenue policy memos

Two short memos (1 page each):

- **Cost-of-revenue matching policy.** Naming which vendor invoices are accrued to the closing period regardless of invoice date (AWS / GCP / Azure, Twilio, Segment, third-party APIs baked into unit economics), the accrual methodology (mid-month usage report as estimate; true-up next cycle), and the reversal / true-up mechanic.
- **Deferred-revenue subledger policy.** Naming the roll-forward equation (beginning RPO + new contracts + modification-adds − modification-removes − revenue recognised = ending RPO), the tie-out required to GL, the contract-modification workflow (billing update + subledger update in the same close cycle), and the escalation for a tie-out variance above materiality.

### Artifact 5 — The 10-to-5 compression memo

A short memo (2-3 pages) explaining the *specific process changes* that take a Series-A close from a 10-business-day landing pattern (typical when the controller has just been hired) to the 5-business-day target six months later. Name at least six specific changes — sub-ledger ownership handoffs, automation additions (FloQast / Blackline / Numeric), close-calendar-tool adoption, daily-standup discipline, exception-log discipline, one-shot cutoff enforcement, etc. — with the specific pain point each change addresses and the estimated day-count saving.

## Starter guidance

- Start with the reconciliations, not the journal entries. The reconciliations are the load-bearing structure; every other task supports one of the five reconciliations.
- Enumerate the sub-ledger owners before assigning tasks. If your Series-A team has one controller and one part-time bookkeeper, that constrains the owner list; if you have a controller, an AP-and-payroll clerk, and a revenue-ops-shared analyst, the ownership pattern looks different.
- Use chapter 3's stage structure literally — every task fits into stage 1-5.
- For each accrual, be specific about the support required (a report, an invoice, a vendor statement, a subledger extract). Vague "accrual" line items are the pattern that produces auditor exception findings.
- Read a reference close checklist (FloQast, Blackline, or the Kruze Consulting or Pilot public examples) before writing your own, but do not copy verbatim — the point is to build the checklist against your specific stack and team.

## Acceptance criteria

- **Checklist has ≥ 40 tasks** across the five stages.
- **Every task has an owner and a reviewer.** Same person as owner and reviewer only permitted with a documented compensating-control note.
- **The five reconciliations template roll-forward equations are correct.** AR = beginning + billings − cash collected; deferred revenue = beginning + billings − revenue recognised; etc.
- **The visual calendar shows the close completing by end of business day 5**, with the CFO review milestone on day 4 and the flash on day 5-6.
- **The cost-of-revenue memo names specific vendors** to accrue and specific methodologies.
- **The 10-to-5 compression memo names ≥ 6 specific process changes** each with a pain point and a day-count saving.

## Deliverables

- The close-calendar spreadsheet.
- The visual Gantt-style calendar (spreadsheet chart, Figma, PDF).
- The five reconciliations template.
- The cost-of-revenue and deferred-revenue policy memos.
- The 10-to-5 compression memo.

## Extensions (optional)

- Add the *international-entity* wrinkle: an EU subsidiary is added mid-cycle; walk the additional FX revaluation, intercompany elimination, and multi-entity consolidation tasks and their impact on the close calendar.
- Add the *first-audit-year* wrinkle: the auditor is now in for their first year of fieldwork; walk the additional PBC-response tasks that thread through the close and add ~1 business day to the total.
- Extend to the *public-company close pattern* (chapter 8): 3-5 business day month-end, 5-7 business day quarter-end plus the additional 10-Q / 10-K workstream. Compare the two calendars side-by-side.
