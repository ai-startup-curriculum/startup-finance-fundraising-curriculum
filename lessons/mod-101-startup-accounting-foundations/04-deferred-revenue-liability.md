# Deferred Revenue — The Liability That Runs a SaaS Balance Sheet

## Why this matters

Deferred revenue (called a **contract liability** under ASC 606-10-45-2) is the balance-sheet account that carries the gap between billings and revenue. It is the single largest liability on most subscription-SaaS balance sheets, often larger than debt. It is also the account that decouples cash from revenue: a company can be growing deferred revenue (cash coming in, obligations to deliver stacking up) while its revenue is flat, and vice versa. Understanding how it accretes and unwinds is the difference between a founder who thinks the bank balance is the business and a CFO who can explain why cash and revenue moved in opposite directions this quarter.

## The mechanical definition

**Deferred revenue** is a liability representing the obligation to deliver a good or service in the future for which the customer has already been billed (or has already paid). Under ASC 606, this is a *contract liability*: the entity has received (or has an unconditional right to receive) consideration before performance is complete.

The double-entry recognition, when a customer is billed $120,000 upfront for an annual subscription:

```
Dr Accounts receivable                    120,000
    Cr Deferred revenue (contract liability)      120,000
```

When the customer pays:

```
Dr Cash                                    120,000
    Cr Accounts receivable                        120,000
```

Each month, as one twelfth of the service is delivered under ASC 606's step-5 over-time recognition:

```
Dr Deferred revenue                         10,000
    Cr Revenue                                     10,000
```

After twelve months, deferred revenue for this contract has fully unwound to zero, and the P&L has recognised $120,000 of revenue.

If the customer had signed but not been billed yet (billed monthly rather than upfront), no deferred revenue arises until each monthly invoice is issued; the amount then oscillates near zero. Deferred revenue is the byproduct of *billing ahead of delivery*, not the byproduct of signing a long contract.

## Short-term vs. long-term deferred revenue

Under US GAAP, deferred revenue is split on the balance sheet between:

- **Short-term deferred revenue** (current liability) — the portion expected to be recognised as revenue within twelve months of the balance-sheet date.
- **Long-term deferred revenue** (non-current liability) — the portion expected to be recognised beyond twelve months.

For an annual-prepay company, essentially all deferred revenue is short-term. For a multi-year prepay contract (rarer but present in enterprise deals with prepayment discounts), the portion recognisable more than twelve months out sits in long-term deferred revenue and rolls to short-term as the twelve-month window advances.

## The deferred-revenue roll-forward — the required disclosure

Every quarter, the CFO produces a deferred-revenue roll-forward. This is both an internal reconciliation and a public-company disclosure under ASC 606-10-50-8. The schedule:

```
Beginning deferred revenue
  + Additions (billings for future performance)
  − Revenue recognised (unwind onto P&L)
  ± Modifications (contract changes, cancellations)
  ± Foreign-currency remeasurement                     (if applicable)
= Ending deferred revenue
```

If the schedule does not tie to the change in deferred revenue on the balance sheet, the numbers are wrong. This is the single most common reconciliation error in a founder-authored model.

## Why a startup's cash balance can grow while revenue is flat (and vice versa)

Two illustrative shapes:

**Shape 1 — cash grows faster than revenue.** A SaaS company shifts from monthly billing to annual prepay with a discount ("$5K/mo or $54K/yr — a 10% discount"). Sales close a wave of annual contracts. Cash comes in as $54K lumps at each contract's signature; revenue recognises at $4,500/mo per contract. In the first quarter of the shift:

- Cash inflows spike (lots of annual prepays landing).
- Deferred revenue balloons.
- P&L revenue barely moves — it is still recognising the same monthly rate per contract.
- Cash from operations (indirect method) shows a large positive "increase in deferred revenue" adjustment, causing operating cash to run well ahead of net income.

The founder looking at the bank balance says "we're crushing it." The accrual P&L says "revenue is flat." Both are correct. The story is entirely explained by the billing-term change.

**Shape 2 — revenue grows faster than cash.** A SaaS company wins several large enterprise deals with net-60 or net-90 payment terms and phased milestone billing (25% at signature, 25% at go-live, 50% at year-end). Contract signatures pull ACV forward; revenue starts recognising ratably from go-live; but cash lags by 60-90 days on each milestone. In the quarter of the shift:

- ARR jumps as the deals go live.
- P&L revenue starts recognising in month 2 or 3.
- Cash inflows are delayed one or two full quarters behind billings.
- AR balloons; DSO (days sales outstanding) spikes.
- Cash from operations shows a large negative "increase in AR" adjustment.

The founder looking at the bank balance says "we're bleeding." The accrual P&L says "revenue is growing 30% QoQ." Both are correct. The story is entirely explained by the enterprise billing-term shift.

Deferred revenue and accounts receivable are the two working-capital accounts that translate between the P&L clock and the treasury clock. A CFO who cannot explain them will be caught out at the first serious board question about the working-capital cycle.

## Deferred revenue vs. RPO — the FASB disclosure requirement

ASC 606-10-50-13 requires public entities (and encourages private entities) to disclose the amount of the transaction price allocated to performance obligations not yet satisfied — the **remaining performance obligation (RPO)**. RPO is deferred revenue *plus* the value of contract commitments that have not yet been billed (backlog).

```
RPO = Deferred revenue + Unbilled backlog on signed contracts
```

For a monthly-billed multi-year contract, RPO can be much larger than deferred revenue — the customer has committed to future spend that has not yet been invoiced. RPO is the closest ASC 606-disclosed number to "ARR" in a public-company filing; investor packs at Series-B onward increasingly report both.

## Cash-basis P&L has no deferred revenue — and no roll-forward

On cash basis, there is no deferred revenue account. Every dollar received from a customer is January revenue if it arrives in January. There is nothing on the balance sheet to unwind. This is the accounting simplification that makes cash basis attractive at IDEA-stage and dangerous everywhere else — you cannot see the obligations you owe your customers, and you cannot see the mismatch between the sales team's output and the delivery organisation's actual work.

The moment a startup takes its first annual prepay, cash basis materially misrepresents the company. Chapter 6 covers when this becomes a required (not elective) transition.

## Related contract-cost accounts under ASC 606

Two smaller balance-sheet accounts sit alongside deferred revenue and complete the picture:

- **Contract assets** (ASC 606-10-45-3) — the mirror of deferred revenue: revenue has been recognised, but consideration has not yet been billed or is contingent on something other than the passage of time. Rare for pure subscription SaaS; common for milestone-based professional services or usage-based components with contractual minimums.
- **Deferred contract costs / capitalised commissions** (ASC 340-40) — incremental costs of obtaining a contract (typically sales commissions) that are capitalised and amortised over the *expected customer life* (not the contract term — commissions on the initial contract are amortised over the initial contract plus the expected renewal period). ASC 340-40 permits a practical expedient to expense commissions when the amortisation period would be one year or less. This is a separate topic from deferred revenue; mentioned here for completeness. mod-102's unit economics treatment of CAC assumes GAAP-capitalised commissions where applicable.

## Common deferred-revenue failure modes

- **No deferred-revenue account at all.** A cash-basis P&L masquerading as accrual. Deferred revenue is missing, all annual-prepay cash lands as revenue, revenue is overstated.
- **Deferred revenue not unwinding.** Billings accumulate into the account but revenue is booked on invoice date. Deferred revenue grows forever, P&L revenue matches billings. Roll-forward does not tie. Common in QBO / Xero installs where the revenue-recognition module is not configured.
- **Deferred revenue never split into short vs. long.** The balance sheet has one line for a company with 30-month contracts. Working-capital ratios are distorted.
- **Modifications not reflected.** A customer downgrades from a $12K annual to a $6K annual mid-year. Deferred revenue for that contract should be reduced to reflect the new remaining performance obligation; a partial refund or credit is issued. Missed modifications leave deferred revenue overstated.
- **Refunds treated as expenses.** A customer prepaid $12K in month 1, cancels in month 3 with a $9K refund. The correct entry reduces cash and reduces deferred revenue by the pro-rata unearned portion; if the refund exceeds unearned deferred revenue (early-cancellation with a full refund), the excess reduces recognised revenue as a contra-revenue adjustment. Refunds should not be classified as an operating expense.

## Summary

- Deferred revenue (contract liability under ASC 606) carries the gap between billings and revenue: cash-in-hand for services not yet delivered.
- It is the largest liability on most subscription-SaaS balance sheets and the account that decouples cash from revenue.
- The deferred-revenue roll-forward — beginning balance + billings − revenue ± modifications = ending balance — is a required disclosure and a required internal reconciliation.
- Cash can grow while revenue is flat (billing-term shift to annual prepay) and revenue can grow while cash is flat (enterprise net-60/90 with milestone billing); both are entirely explained by the working-capital cycle.
- Cash-basis accounting has no deferred revenue, which is exactly the problem it creates.

Chapter 5 covers the gross-vs.-net revenue question, contra-revenue treatment, and the agent-vs.-principal analysis that ASC 606 uses to decide whether a payment collected from a customer is even *your* revenue at all.
