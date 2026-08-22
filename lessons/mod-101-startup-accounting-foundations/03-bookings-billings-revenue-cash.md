# Bookings, Billings, Revenue, Cash — The Four SaaS Numbers a CFO Reports Separately

## Why this matters

A CFO reports four separate numbers for a SaaS quarter. A founder frequently reports one, calls it "revenue," and inadvertently means whichever of the four is highest that quarter. The four numbers are:

1. **Bookings** — total contract value signed in the period (a sales metric).
2. **Billings** — total amount invoiced to customers in the period (an AR / AP timing metric).
3. **Revenue** — total ASC 606 revenue recognised in the period (a GAAP P&L metric).
4. **Cash** — total cash collected from customers in the period (a treasury metric).

In any given quarter, all four can differ, and their differences are the story of the quarter. Bookings > billings means the sales team wrote long-dated or milestone-billed contracts. Billings > revenue means annual-prepay or upfront-billed multi-period contracts built the deferred-revenue balance. Revenue > cash means AR grew (customers were slow to pay). Cash > revenue means either prepaid contracts landed or old AR was collected. The four numbers together explain the quarter; any one alone hides more than it reveals.

## Working definitions

**Bookings.** The sum of the total contract value (TCV) or annual contract value (ACV) — whichever the company reports — of contracts *signed* in the period. Bookings recognise a sale at signature, regardless of when the contract is billed, delivered, or paid. A one-year $120K contract signed on the last day of Q1 is $120K of Q1 bookings (measured as TCV) or $120K of ACV. A three-year $360K contract signed on the last day of Q1 is $360K of Q1 TCV bookings or $120K of Q1 ACV bookings. The distinction matters — most companies report ACV internally, TCV externally, or both. Bookings are not a GAAP concept; they are a sales-operations measure.

**Billings.** The sum of amounts invoiced to customers in the period. Billing terms are contractually driven — annual prepay bills the full year at signature; monthly bills monthly; quarterly bills quarterly; milestone-billed engagements bill on completion of defined milestones. Billings show up on the balance sheet as the "increase in accounts receivable" if the customer has not yet paid, and as an "increase in deferred revenue" (contract liability) if the customer has paid ahead of delivery. Billings are not a GAAP concept either; they are the invoice-cycle output.

**Revenue.** ASC 606 revenue recognised in the period. This is the GAAP P&L number and the only one that appears on the income statement. Chapter 2's five-step model is how each dollar of a contract's transaction price is turned into a monthly stream of P&L revenue. For a subscription contract with straight-line recognition, monthly revenue is the allocated subscription price divided by the number of months in the contract term.

**Cash.** Cash actually received from customers in the period. This is the treasury number and appears in the cash-flow statement (indirectly, via changes in AR and deferred revenue in the operating-activities section, or directly via the direct method). Cash timing is driven by customer payment behaviour — net 30, net 60, net 90 payment terms; enterprise customers with 60-90 day cycles; consumer customers with card-on-file collection.

## Why the four separate — a small worked example

Consider a hypothetical quarter (Q3) for a SaaS company. Continue for illustration only:

| Contract | Term | ACV | Signed | Billing terms | First invoice | Customer pays |
|---|---|---|---|---|---|---|
| A | 12 months | $120K | Jul 15 | Annual prepay | Jul 15 | Jul 25 |
| B | 12 months | $60K | Aug 1 | Monthly | Aug 1 | Aug 15 (each month) |
| C | 24 months | $240K TCV / $120K ACV | Sep 20 | Annual prepay, year 1 only | Sep 20 | Oct 5 (past Q3) |
| D | 12 months | $180K | Jan 1 (prior quarter) | Annual prepay | Jan 1 | Jan 20 (prior quarter) |

Q3 accounting:

- **Bookings** — sum of ACV of contracts signed in Q3: A ($120K) + B ($60K) + C ($120K ACV, or $240K TCV) = $300K ACV / $420K TCV. Contract D is not a Q3 booking; it was signed in Q1.
- **Billings** — sum of invoices raised in Q3: A ($120K, annual prepay in July) + B ($5K × 3 months = $15K, monthly starting August) + C ($120K, year-1 annual prepay in September) = $255K. Contract D was billed in Q1, not Q3.
- **Revenue** — sum of ASC 606 revenue recognised in Q3. Contract A: signed and started Jul 15, ~$120K / 12 = $10K/mo, so ~$25K in Q3 (half of July + August + September, roughly). Contract B: signed and started Aug 1, $5K/mo × 2 months = $10K. Contract C: signed Sep 20, service starts Sep 20 or Oct 1 depending on the go-live date; assume Oct 1 start, so $0 Q3 revenue. Contract D: $15K × 3 months = $45K. Q3 revenue ≈ $80K. (Exact numbers depend on go-live and proration assumptions.)
- **Cash** — sum of customer cash receipts in Q3: A ($120K in July) + B ($5K × 2 = $10K in August/September) + C ($0 — customer paid on Oct 5) + D ($0 — paid in Q1) + any Q2-billed collections landing in Q3 = at minimum $130K in Q3.

Four different numbers, all for the same "quarter." Bookings ($300K ACV) tells you the sales team's output. Billings ($255K) tells you the invoicing cycle. Revenue ($80K) tells you what appeared on the P&L. Cash ($130K) tells you what hit the bank. Reporting any one number as "the quarter" tells a different story.

## Reconciling the four — the flow

The four numbers connect via balance-sheet accounts. Every dollar of bookings that eventually becomes cash flows through this chain:

```
Bookings         (contract signed)
   ↓  (bill customer per contract billing terms)
Billings         (invoice issued, AR up)
   ↓  (customer pays)
Cash             (AR down, cash up)

Bookings         (contract signed)
   ↓  (allocated transaction price recognised as delivered under ASC 606)
Revenue          (P&L)

Billings > Revenue: excess sits in deferred revenue     (contract liability)
Revenue > Billings: excess sits in unbilled receivable  (contract asset)
Billings > Cash:    excess sits in accounts receivable
Cash > Billings:    excess is a customer prepayment / advance — deferred revenue
```

The full reconciliation for a period:

```
Beginning deferred revenue
  + Billings for the period
  − Revenue for the period
  ± Contract-modification adjustments
= Ending deferred revenue
```

and separately

```
Beginning AR
  + Billings for the period
  − Cash collected
  − Write-offs
= Ending AR
```

The two identities together let you back into any missing number if you have the balance-sheet snapshots and any three of the four. In practice, the CFO tracks each independently in the financial system and reconciles quarterly.

## The KPIs that live on top of the four

Investor-facing SaaS KPIs are derived from these four numbers or from related contract-level facts, not from a single P&L number:

- **ARR (annual recurring revenue)** — the annualised value of currently-active subscription contracts at a point in time. ARR is a snapshot metric (like the balance sheet), not a period metric (like revenue). Beginning ARR + new ARR + expansion ARR − contraction ARR − churned ARR = ending ARR.
- **MRR (monthly recurring revenue)** — ARR / 12.
- **NRR (net revenue retention)** — cohort-level: current ARR from a cohort of customers ÷ their ARR one year ago. Includes expansion, contraction, churn.
- **GRR (gross revenue retention)** — cohort-level, excludes expansion. Captures pure churn + downsell.
- **CAC payback** — CAC ÷ (new ARR × gross margin). See mod-102.
- **Burn multiple** — net burn ÷ net-new ARR. See mod-102.

None of these are a P&L revenue number. They are pieced together from bookings, billings, revenue, and cash — plus per-contract signature dates, expansions, and churn events tracked in the CRM and billing system. mod-102 covers these at CFO grade.

## Which number to report where

The CFO's practice:

- **P&L / income statement.** Revenue only. This is GAAP.
- **Cash-flow statement.** Cash-from-operations reconciles net income to cash via working-capital changes; the reader can see billings vs. revenue via the change in deferred revenue and revenue vs. cash via the change in AR.
- **Balance sheet.** AR, deferred revenue, contract assets. These are the plumbing between the four numbers.
- **KPI dashboard for the board.** All four separately, plus ARR, plus growth rates on each. This is where a CFO explains what happened this quarter.
- **Investor deck.** ARR as the headline, with revenue and cash growth rates as supporting metrics. Never conflate bookings with revenue; investors will catch it in diligence and re-price.
- **Fundraising conversations.** ARR, growth rate, NRR, GRR, gross margin, burn multiple. Bookings, billings, and cash are supporting metrics that the CFO must be able to produce on request but that do not lead the conversation.

## Common failure modes

- **Conflating bookings with revenue.** "We did $2M in Q4" when Q4 bookings were $2M and Q4 revenue was $400K. Investors will catch this; the fix is to always state which metric.
- **Conflating billings with revenue.** "We invoiced $500K in September, that's $6M ARR" — no. Billings depend on billing terms; annual prepay concentrates a year of billings into one month.
- **Conflating cash with revenue.** "We had $1M in the bank at month-end, that's our revenue" — no. Cash is a treasury number and includes prepayments, financing proceeds, and old-AR collections.
- **Not tracking the four separately.** If the finance system does not produce all four on a per-period basis, the CFO cannot explain the quarter. Every accounting stack from QBO up produces them if configured correctly.
- **Reporting only the flattering one.** Every quarter, one of the four looks better than the others. A CFO reports all four consistently; a founder reports the highest.

## Summary

- Bookings, billings, revenue, and cash are four distinct SaaS numbers, all for the same period, and they routinely differ.
- Only revenue is a GAAP P&L concept, driven by ASC 606; bookings and billings are operational; cash is treasury.
- The four reconcile via deferred revenue and accounts receivable on the balance sheet.
- Investor KPIs (ARR, NRR, GRR) are built on these four numbers plus contract-level facts.
- The CFO reports all four separately; the founder frequently conflates them into "revenue," and the accrual-GAAP number is often the smallest.

Chapter 4 walks the deferred-revenue liability that carries the gap between billings and revenue. Chapter 5 addresses the gross-vs.-net question that decides how much of the transaction price counts as revenue at all.
