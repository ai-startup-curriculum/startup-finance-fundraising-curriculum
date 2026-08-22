# GTM Funnel as the Revenue Driver

## Why this matters

Founder-authored revenue forecasts almost always look like this: current ARR × (1 + growth rate)^months. If the current ARR is $2M and the plan assumes 8% MoM growth, month-12 ARR is projected at $5M. The number is a shape, not a build; there is no view of how many customers close in each month, no view of what those customers pay, no view of how many leads it takes to close each customer, and no view of what the sales team has to do to hit the number.

A CFO's revenue forecast is bottom-up: leads generated per month × MQL-conversion rate × SQL-conversion rate × close rate × ACV × cohort retention. Every step of the funnel is a driver on an assumption tab; every step's output feeds the next; the aggregate is the revenue line on the P&L. The funnel is what makes the top-line number *defensible* — the CEO can walk it forward from S&M budget to lead volume to closed customers, and the CFO can walk it backward from a revenue miss to which specific funnel stage broke.

This chapter installs the GTM funnel as the revenue driver — the funnel stages, the conversion-rate assumptions, the ACV assumption, the cohort retention layered on top, and the integration with the cohort table from [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/).

## The funnel — canonical stages

A B2B SaaS sales-motion funnel with a standard demand-generation-plus-sales-close pattern has these stages (terminology varies; the shape does not):

```
S&M spend
    │
    ▼
Leads (raw inquiries, form fills, downloads, sign-ups)                    ← from marketing programmes
    │  × MQL-qualification rate
    ▼
Marketing-qualified leads (MQLs — leads that pass the ICP filter)
    │  × SQL-conversion rate
    ▼
Sales-qualified leads (SQLs — MQLs that a rep has qualified for pipeline)
    │  × Opportunity-creation rate
    ▼
Opportunities (SQOs — sales-accepted, discovery-completed)
    │  × Close rate (or "win rate")
    ▼
Closed-won customers                                                       ← new logos
    │  × ACV
    ▼
New bookings (ARR-book, contract-value terms)
    │  ± billing terms
    ▼
Billings, deferred revenue, and recognised revenue                        ← the P&L revenue line
```

Different companies name stages differently. A PLG motion has "sign-ups" (equivalent to leads), "activated users" (equivalent to MQLs), "paid conversions" (equivalent to closed-won). An enterprise motion has "opportunities" broken into stage-1 through stage-6 (early discovery through verbal commit through signed). A partner-channel motion has "partner-sourced opportunities" that skip the top of the funnel entirely.

The model should reflect the actual motion. A generic six-stage funnel imposed on a PLG company misses the shape; a two-stage funnel imposed on an enterprise sales motion loses the diagnostic power of tracking pipeline in each intermediate stage. Build the funnel for the motion you have.

## The funnel tab — shape

The funnel tab is a table with stages as rows and calendar months as columns. Each cell is the count of funnel entities in that stage in that month.

```
Funnel tab                         Jan Y+1  Feb Y+1  Mar Y+1   ...
├─ S&M spend ($K)                   250      280      320
├─ Cost per lead ($)                125      130      130
├─ Leads (S&M / CPL)                2,000    2,153    2,461
├─ MQL rate (%)                     35%      35%      35%
├─ MQLs                             700      754      861
├─ SQL rate (%)                     20%      20%      22%    (improving with better qualification)
├─ SQLs                             140      151      189
├─ Opps rate (%)                    80%      80%      80%
├─ Opps                             112      121      152
├─ Close rate (%)                   22%      22%      22%
├─ Closed-won customers             25       27       33
├─ ACV ($)                          12,000   12,000   12,600   (5% quarterly)
├─ New bookings ($)                 300K     324K     416K
```

Two things about this layout worth calling out:

- **Every count is a formula** — leads = S&M / CPL, MQLs = leads × MQL rate, and so on. The only cells with typed numbers on this tab are the historical actuals (leftmost columns, locked). The forecast columns' conversion rates and ACV come from the assumption tab.
- **Every stage has a lag consideration.** In practice, an SDR's outbound sequence in March doesn't produce closed-won customers in March — it produces SQLs in April, opps in May, and closed-won in June. A month-M-close, month-M-SQL layout imposes a same-month attribution that's fine for a fast-cycle motion (PLG, self-serve) but wrong for outbound and enterprise. For medium- and long-cycle motions, the funnel needs a lag adjustment (see below).

## Conversion-rate assumptions — where the numbers come from

The conversion rates from stage to stage are the largest source of variance in a bottom-up forecast. A defensible model sources them from actual historical performance, not aspiration.

- **Lead-to-MQL rate.** From marketing-ops attribution — what fraction of raw inquiries pass the ICP filter (right industry, right size, right role). Typical range for B2B SaaS: 20-50%, with lower rates indicating either broad-net top-of-funnel programs (paid social, content download) or a tight ICP.
- **MQL-to-SQL rate.** From the SDR team's qualification funnel — what fraction of MQLs get qualified as pipeline-ready. Typical range: 15-30%. Below 10% suggests weak marketing programs; above 40% suggests a very tight top-of-funnel that may be missing volume.
- **SQL-to-opportunity rate.** From the AE team's discovery process — what fraction of SQLs make it to a working opportunity. Typical range: 50-80%. Below 50% suggests a mismatch between SDR qualification standards and AE standards.
- **Opportunity close rate.** From the AE team's pipeline reviews. Typical range for B2B SaaS: 15-30% for outbound, 20-40% for inbound, 30-50% for PLG-derived enterprise conversions. Highly stage-dependent — early-stage funnels have wider dispersion than mature ones.

Each rate should have a trailing-3-month or trailing-6-month historical value visible on the tab, and any forecast improvement should be justified by a specific programme (a new SDR playbook, an ICP refinement, a discovery-training initiative). The pattern to avoid: forecast rates that step up by 500bps every quarter with no operational change to justify them.

Benchmark ranges are widely published — [OpenView SaaS Benchmarks](https://openviewpartners.com/), [SaaStr Benchmarks](https://www.saastr.com/), David Skok's [ForEntrepreneurs](https://www.forentrepreneurs.com/), the KeyBanc / Meritech State of the Cloud reports — but a company's own history is the more reliable calibration once it has 12+ months of data.

## ACV progression and mix

The ACV assumption is where a bottom-up model most often diverges from reality. Sources of ACV movement:

- **Package-mix shift.** A company selling Starter ($5K), Growth ($15K), and Enterprise ($50K) SKUs has an ACV that changes as the mix shifts — if enterprise closes go from 10% of new logos to 20%, blended ACV moves materially even with no per-SKU price change.
- **Price increases.** A list-price bump on a specific SKU flows through to new bookings from the price-effective date. Existing customers may or may not roll into the new price at renewal (contractually depends on the renewal terms).
- **Seat expansion at close.** Enterprise deals often close at a larger seat count than the initial ICP; SMB self-serve deals often close at the minimum seat count. Track the initial-seat-count assumption separately from list price.
- **Multi-year discount.** Enterprise deals with multi-year commitments often trade a 5-15% price discount for the extended term. The ACV (annual contract value) is unchanged; the total contract value is 2× or 3× ACV.
- **Free tier or freemium.** A large fraction of "closed-won" may be $0 ACV free-tier signups, with revenue coming from a later upsell. If the funnel counts free-tier signups as closed-won, ACV must reflect the blend (very small) and expansion revenue models a large delayed uplift.

The ACV assumption can be a single monthly value on the funnel tab, or a package-mix model with per-package ACV. For a Series-A B2B SaaS with a limited SKU set, a per-package model is worth the complexity — it lets scenarios flex the mix and show the ARR impact of enterprise motion investment.

## Bookings vs. billings vs. revenue

The funnel produces new bookings — the ACV × new logo count. Bookings is not revenue. Chapter 3 of [`mod-101`](../mod-101-startup-accounting-foundations/03-bookings-billings-revenue-cash.md) covers the four numbers in detail; the summary for this chapter:

- **Bookings.** ACV × new logos in the month. Signed contracts. Not on the P&L.
- **Billings.** What the customer is invoiced this month — usually the full ACV upfront for annual prepay, or ACV/12 monthly for month-to-month, or ACV/4 quarterly. Not on the P&L.
- **Revenue (recognised).** For a subscription contract, the monthly value of the service delivered. For an annual prepay contract signed on 1 April at $12K ACV, this is $1K per month from April through March of the next year. This is what appears on the P&L revenue line.
- **Cash.** What actually hits the bank account, usually 30-60 days after invoice depending on payment terms.

The funnel tab produces bookings and passes them to the driver tab, which produces:

1. **Billings schedule** — per-contract, based on the billing-term assumption (annual prepay, monthly, etc.).
2. **Deferred revenue movement** — new bookings in the month billed upfront add to deferred revenue; revenue recognised each month reduces it.
3. **Recognised revenue** — sum of monthly recognition across all active contracts, feeds the P&L revenue line.
4. **AR** — invoices billed but not yet collected, based on the DSO assumption.

The three lines that reference the funnel indirectly:

- **P&L revenue** ← recognised revenue driver.
- **Balance sheet deferred revenue** ← deferred revenue roll-forward.
- **Balance sheet AR** ← billings × DSO driver.

## Cohort retention layered on top

Every closed-won customer in month M starts a cohort. That cohort's revenue in month M + k is a function of the retention curve and the expansion rate at that point in the cohort's life.

The cohort-revenue schedule on the driver tab is a large matrix: rows = signup cohorts, columns = calendar months of the forecast. The cell at (row = cohort M, column = calendar month M + k) is:

```
new-customer count in month M
  × (retention curve at k)
  × (initial ACV of cohort M)
  × (1 + expansion rate)^(k/12)                    ← if expansion is modelled as an annual uplift
  / 12                                              ← monthly recognition
```

For a cohort of 25 customers signed in month M at $12K ACV each, with a retention curve of 100/95/92/90/89/88/87/... and no expansion:

- Month M: 25 × 100% × $1K = $25K MRR from cohort M.
- Month M+1: 25 × 95% × $1K = $23.75K MRR.
- Month M+2: 25 × 92% × $1K = $23K MRR.
- ...

The total MRR in any calendar month is the sum across all cohorts of that cohort's MRR in that month:

```
Total MRR in calendar month M = Σ (over all cohorts k ≤ M) cohort k's MRR in month (M - k)
```

The schedule can be built in a spreadsheet either as a full matrix (large, slow, transparent) or as a compressed formula per cohort (smaller, faster, harder to audit). For a 24-36-month forward horizon, the full matrix is manageable and preferable for readability.

The retention curve on the assumption tab is either:

- A single retention curve applied to all cohorts (simplest, appropriate if the historical cohort table shows stable cohort shapes).
- A per-cohort retention curve (more complex, appropriate if cohort quality is changing — e.g., recent cohorts show better retention because the ICP has been refined).
- A segment-specific retention curve (SMB retention vs. mid-market vs. enterprise), used with the package-mix ACV model above.

Exercise 04 in [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/exercises/exercise-04-cohort-table-build-and-read.md) builds the empirical cohort table that produces the retention-curve numbers. The funnel model here consumes those numbers as inputs.

## Expansion and contraction

Once a cohort is retained, its revenue can grow (expansion) or shrink (contraction) even before any customer churns. Modelling this correctly matters because expansion is a large share of NRR (net revenue retention) in the top-line ARR walk (see [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/05-nrr-and-grr-as-capital-efficiency-levers.md)).

Two conventions:

- **Retention curve captures net dollar movement.** The retention curve is denominated in dollars, not in customer counts. A retention curve of `100/98/97/98/100/102/...` implies dollar retention above 100% after month 4 — expansion is happening. This is the simplest way to encode expansion but hides the mechanic (are customers expanding, or is churn low + a small expansion?).
- **Retention curve captures customer retention; expansion is a separate driver.** The retention curve is `100/95/92/...`, purely customer count. A separate expansion driver (e.g., 8% annual per-customer ARPU growth for retained customers) multiplies through. This is more mechanistic and lets scenarios flex retention and expansion independently.

The latter is preferred for CFO-grade modelling because a Series-A investor will ask, "is your NRR of 118% coming from expansion or from unusually strong retention?" and the model needs to answer with the mechanic. The former is fine for smaller companies where the mechanic isn't yet a diligence question.

Contraction (a customer downgrading a plan) is usually modelled as a subtraction from the expansion rate rather than a separate driver, unless the company has a large-enough downgrade motion that separate modelling is warranted (rare at Series-A; sometimes relevant at growth stage in specific verticals).

## The three revenue outputs from the funnel

The funnel and cohort-revenue schedule together produce three outputs the rest of the model consumes:

1. **New bookings ARR by month** — ACV × new logo count. Feeds the ARR walk on the KPI dashboard (chapter 7).
2. **Recognised revenue by month** — the P&L revenue line. Sum of monthly recognition across active contracts and cohorts.
3. **Billed amount by month** — the input to AR and deferred revenue on the balance sheet, based on the billing-term assumption per contract.

Each of these has a corresponding closing balance:

- **Ending ARR** — MRR × 12 at month-end. This is the number most SaaS dashboards call out prominently.
- **Ending deferred revenue** — sum of unearned portion of all active billed contracts.
- **Ending AR** — billings less collections; drives DSO.

The three outputs and their balance-sheet counterparts flow into the P&L, balance sheet, and cash-flow statement via the driver tab. Every one of them updates when the funnel's inputs change, or when the cohort retention curve changes, or when the ACV assumption changes.

## The relationship to CAC — the S&M input side

The funnel's top-of-funnel input is S&M spend. The bottom-of-funnel output is closed-won customers. The ratio of `S&M spend / closed-won customers` is CAC — the metric [`mod-102`](../mod-102-unit-economics-and-cohort-financial-modelling/01-fully-loaded-cac-per-channel-and-cohort.md) covers in depth.

The funnel model is where CAC becomes a *forecast* rather than a historical read. If the assumption tab is:

- S&M spend increasing 15% per quarter (from the hiring plan and the non-payroll ratio).
- Cost per lead constant at $130.
- MQL rate constant at 35%.
- SQL rate improving from 20% to 25% over 6 quarters.
- Close rate constant at 22%.

Then the *forecast CAC* is derived — S&M / closed-won in each month — and the model can be asked, "at this forecast CAC, what is the LTV:CAC ratio implied by our cohort curve?" A model where forecast CAC drifts unfavourably as S&M scales (the classic diseconomy-of-scale in paid channels) needs to be flagged in the CFO narrative.

The board pack question this feeds: *"our S&M plan for next year is $18M. Given our funnel conversion assumptions, that produces 380 new logos, blended CAC of $47K, and LTV:CAC of 4.1× based on the cohort curve — sourced from mod-102's exercise 4."* This is a defensible ask.

## Bottom-up funnel model vs. top-down growth rate

The top-down alternative — "revenue grows at 8% MoM" — is what a founder deck often shows. It is not wrong in the sense of being arithmetically incorrect; it is wrong in the sense of being unfalsifiable.

A bottom-up funnel is falsifiable because each step can be checked against reality. If the plan says the SDR team will produce 900 SQLs in Q2 and the actual is 400, the CFO knows exactly which stage broke and can re-forecast from there. A top-down model whose Q2 revenue is 44% below plan gives the CFO no leverage on the diagnostic — is it a lead-volume problem, a qualification problem, a close-rate problem, or an ACV problem?

The other reason to build bottom-up: it forces the S&M plan and the revenue plan to be internally consistent. If the hiring plan doesn't have enough SDRs to produce the assumed SQL volume, the funnel model surfaces the gap immediately (SDR × SQLs-per-SDR is below the required SQL number). A top-down model can happily assume 200% growth while the hiring plan hires zero SDRs; only the funnel connects the two.

Chapter 5 covers the top-down view specifically — TAM × penetration-rate — as a *sanity check* on the bottom-up build, not a replacement for it.

## Summary

- The GTM funnel is the bottom-up revenue driver: S&M spend → leads → MQLs → SQLs → opps → closed-won × ACV × cohort retention → revenue.
- The funnel tab has stages as rows and calendar months as columns; every count is a formula sourced from the assumption tab, only historicals contain typed numbers.
- Conversion rates come from historical actuals with justified improvements from specific programs, not aspirational step-ups. Benchmark ranges from OpenView / SaaStr / KeyBanc apply, but the company's own history is the more reliable calibration.
- ACV modelling should reflect package mix, price increases, and multi-year discount mechanics — a per-package model is worth the complexity for a Series-A company with multiple SKUs.
- Bookings are not revenue. The funnel produces bookings; the driver tab converts bookings → billings → recognised revenue (via the deferred-revenue roll-forward) → AR (via DSO). The three outputs feed the P&L, balance sheet, and CFS.
- Cohort retention is layered on top of the funnel via a cohort-revenue schedule (matrix of cohorts × calendar months). The retention curve comes from the cohort table built in mod-102.
- Expansion is best modelled as a separate driver from retention so that a Series-A investor's "is the NRR from expansion or retention" question can be answered with the mechanic.
- The funnel and hiring plan are interlocked: SDR / AE headcount and productivity coefficients feed the funnel; the funnel's S&M-spend input comes from the hiring plan's S&M payroll plus non-payroll ratios.
- Bottom-up funnel forecasts are falsifiable at every stage — a miss can be traced to lead volume, conversion, close rate, or ACV. Top-down growth-rate forecasts are not.

Chapter 5 turns to the reconciliation between bottom-up funnel forecasts and top-down TAM × penetration-rate forecasts — the two views a Series-A investor asks for side by side.
