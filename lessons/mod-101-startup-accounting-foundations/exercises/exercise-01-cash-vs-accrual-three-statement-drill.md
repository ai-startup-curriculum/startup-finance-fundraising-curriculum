# Exercise 01 — Cash vs. Accrual Three-Statement Drill

**Estimated time:** ~2 hours
**Prerequisites:** Chapter 1 (three-statement financials on cash and accrual basis).

## Problem statement

Take one hypothetical SaaS startup's operating quarter and produce the P&L, balance sheet, and cash-flow statement on both cash basis and accrual basis. Reconcile the two — quantify the difference between cash-basis and accrual-basis revenue for the quarter, explain where the difference lives on the accrual balance sheet, and show how the accrual cash-flow-statement operating section bridges back to the cash-basis P&L revenue.

The goal is muscle memory: after this drill you should be able to look at any startup's cash-basis P&L and reconstruct its accrual-basis view (approximately) from the balance-sheet deltas alone.

## Scenario — build your own

Pick either your own real startup, one you know well from prior work, or construct a hypothetical company with the following minimum shape:

- SaaS subscription business
- Between 5 and 15 active customer contracts during the quarter
- A mix of billing terms — at minimum, one annual-prepay contract and one monthly-billed contract
- At least one contract signed mid-quarter and at least one contract signed in the prior quarter and still active
- At least one operating expense with a timing mismatch between incur and pay (e.g., an annual insurance premium paid in month 1 that covers 12 months; a legal-fee invoice received in the last week of the quarter but not paid until the next quarter)
- Payroll paid on a monthly cycle
- A hosting/infra bill invoiced monthly but paid on net-30 terms
- Ending cash balance you specify (or actual, if using a real startup)

If constructing hypothetical data, keep numbers small (five-figure ACVs) and specific enough to actually reconcile.

## Requirements

Produce the following in a spreadsheet (Excel, Google Sheets, or Numbers) or in a well-structured notebook:

1. **Contract register (input).** Every contract in force during the quarter: signature date, contract term, ACV, billing terms, invoice dates in the quarter, cash-receipt dates in the quarter, service start date.
2. **Expense register (input).** Every operating expense recognised or paid in the quarter: expense category (S&M, R&D, G&A, COGS), incurrence date, invoice date, payment date, amount.
3. **Cash-basis P&L for the quarter.** Revenue = cash received from customers in the quarter. Expenses = cash paid to vendors / payroll in the quarter. Net income = revenue − expenses.
4. **Accrual-basis P&L for the quarter.** Revenue = ASC 606 revenue recognised per contract per month (straight-line for subscription; separate treatment for any distinct implementation or training performance obligations). Expenses = incurred (accrued) in the quarter regardless of payment timing.
5. **Accrual-basis balance sheet at quarter-end.** All standard line items: cash, AR, prepaid expenses, PP&E (if any), AP, accrued liabilities, deferred revenue (split short-term / long-term), equity. Must balance.
6. **Accrual-basis cash-flow statement for the quarter (indirect method).** Start from accrual net income; adjust for non-cash items; adjust for changes in working-capital accounts. Ending cash on the CFS must equal cash on the balance sheet.
7. **Reconciliation memo (max one page).** Compute the difference between cash-basis and accrual-basis revenue for the quarter, in dollars and as a percentage of accrual revenue. Explain where that difference lives on the accrual balance sheet (AR + deferred revenue movements). Explain any operating-expense difference the same way (AP + accrued liabilities + prepaid expenses).

## Starter guidance

- Build the contract register first. Every downstream number derives from it.
- Compute monthly recognised revenue per contract using the ASC 606 five-step model from chapter 2. For a straight subscription with straight-line recognition, this is ACV ÷ 12; for a mid-month go-live, prorate the first month.
- Do not use QBO, Xero, or NetSuite for this drill. Build the statements by hand in a spreadsheet — the point is to see every entry, not to trust the software.
- Structure the spreadsheet so a reviewer can trace each P&L line back to the contract register or expense register with no black boxes.
- For the accrual balance sheet, start with the beginning balance sheet (assume zero for a startup at inception, or make explicit opening balances if the quarter is not Q1 of Year 1) and layer each quarter's activity.
- The cash-flow statement should not have a plug. If it does not tie, one of the working-capital deltas is wrong.

## Acceptance criteria

- **Balance sheet balances.** Assets = Liabilities + Equity at the end of the quarter, to the dollar.
- **Retained earnings tie.** Accumulated deficit (retained earnings) at quarter-end equals the beginning balance plus net income for the quarter.
- **Ending cash ties.** Ending cash on the balance sheet equals ending cash on the cash-flow statement.
- **Deferred-revenue roll-forward ties.** Beginning deferred revenue + billings − revenue = ending deferred revenue.
- **AR roll-forward ties.** Beginning AR + billings − cash collected = ending AR.
- **Cash-basis vs. accrual revenue reconciled.** The dollar difference is explained by the change in AR and deferred revenue (with sign convention documented).
- **Reconciliation memo names the drivers.** Not just "$X difference"; the memo should call out which contracts contributed most to the delta and why (e.g., "annual prepay from Customer X in month 1 added $Y to cash revenue that will recognise as accrual revenue over months 2-12").

## Deliverables

- Spreadsheet file (or notebook) with all six numeric artefacts on separate tabs / sections.
- One-page reconciliation memo (Markdown or PDF).

## Extensions (optional)

- Extend to two quarters and produce the roll-forwards across both, showing how deferred revenue peaks and unwinds.
- Add one contract modification mid-quarter (customer downsizes from $12K annual to $6K annual; issue a $3K credit) and walk the balance-sheet and P&L impact.
- Add one refund event (customer prepaid $12K, cancels in month 2 with a $10K refund) and walk the impact.
