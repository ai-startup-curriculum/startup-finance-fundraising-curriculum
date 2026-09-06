# Exercise 04 — Venture-Debt Term-Sheet Analysis

**Estimated time:** ~3.5 hours
**Prerequisites:** Chapter 5 (Venture Debt — SVB / TriplePoint / Runway Growth / Hercules-Style Term Loans, Warrants, and Covenants). Familiarity with mod-103 (Three-Statement Model and Driver-Based Forecasting) for the covenant-sensitivity work and mod-104 (Cap Tables) for the warrant-dilution modelling.

## Problem statement

Given a venture-debt term sheet from a specialty BDC lender, mark it up against the market-standard SVB / TriplePoint / Hercules / Runway Growth pattern from chapter 5, build the covenant-sensitivity model that tests every financial covenant under realistic KPI-variance scenarios, compute the all-in effective cost of the debt including warrant value, and produce the CFO's board memo defending the equity-vs-debt-vs-hybrid decision. The point of the drill is to teach the CFO to read a term sheet with the specific instincts a venture-debt facility requires: is the covenant package survivable, is the MAC clause narrow enough, is the warrant coverage priced fairly, and — most importantly — is the debt being drawn to extend a strong plan or to postpone a weak one?

## Scenario — the company and the offered facility

**Company.** B2B SaaS, ~85 employees, closed Series-B 14 months ago. Series-B was $30M at $130M post-money led by Growth Fund E. Current ARR $16M, growing ~5% MoM over trailing three months (down from 8% MoM at Series-B), NRR 116%, gross margin 76%, CAC payback 20 months. $12M cash on hand, $1.4M/month burn — 8-9 months of runway. Board expectation: Series-C at $200-300M post-money in 12-18 months gated on reaching $28-32M ARR with ARR growth reaccelerating and CAC payback improving to 16 months. The CFO is at the 9-month trigger from chapter 1 and is evaluating a venture-debt draw to extend runway to a stronger Series-C conversation.

**The offered facility** (assume delivered as a term sheet from a specialty BDC lender modelled on the TriplePoint / Hercules pattern):

- **Facility size:** $12M term loan, drawn in two tranches (Tranche A $8M at close; Tranche B $4M within 12 months of close, subject to reaching $22M ARR).
- **Draw period:** 12 months from close for Tranche B; Tranche A at close.
- **Interest-only period:** 18 months from close.
- **Amortisation period:** 30 months following interest-only.
- **Total tenor:** 48 months.
- **Interest rate:** Prime + 550 bps, floating (floor at Prime + 500 bps). Assume Prime = 8.00% for the drill.
- **Commitment fee:** 1.0% of the total facility, paid at close.
- **End-of-term (backend) fee:** 6.5% of the drawn amount, paid at maturity or upon prepayment.
- **Prepayment penalty:** 3% in year 1, 2% in year 2, 1% in year 3, 0% thereafter.
- **Warrant coverage:** 3.5% of the drawn amount, exercisable for Series-B Preferred at the Series-B price ($5.20/share), 10-year term, cashless exercise.
- **Security interest:** First-priority all-asset lien including a lien on intellectual property (no IP negative-pledge carveout).
- **Guarantees:** Delaware parent plus all domestic subsidiaries guarantee; foreign subsidiaries excluded.
- **Financial covenants:**
  - **Minimum cash covenant:** at least $4M at all times (measured monthly on the last business day).
  - **Minimum ARR covenant:** trailing quarter ARR ≥ $14M at close, stepping to $18M at month 6, $22M at month 12, $26M at month 18, $30M at month 24, $32M at month 30 and thereafter.
  - **Minimum ARR growth covenant:** year-over-year ARR growth ≥ 30%, measured quarterly.
- **Affirmative covenants:** monthly management financials within 30 days, quarterly unaudited within 45 days, annual audited within 150 days, annual budget by January 31 of the fiscal year.
- **Negative covenants:** standard basket. Additional indebtedness capped at $2M outside of the facility (this cap includes RBF and other working-capital lines). No dividends. No stock buybacks. No affiliate loans. Change-of-business restrictions. Material subsidiary disposition requires lender consent.
- **Material Adverse Change (MAC) clause:** "the Lender may, in its sole discretion, decline further disbursements, accelerate the outstanding balance, or terminate the facility, upon the occurrence of any change in the Borrower's business, operations, financial condition, or prospects that the Lender determines to be materially adverse." Broad drafting.
- **Cure rights:** 30-day cure period for financial-covenant breaches. **No** equity-cure right (i.e., the borrower cannot cure a minimum-cash breach by raising equity and adding it to the cash calculation).

**Alternative:** the company could instead raise an incremental $10M equity extension of the Series-B from Growth Fund E at the last-round price ($5.20/share, implying a post-money adjustment; assume this extension would close in ~10 weeks and dilute the pre-extension holders by ~7%).

## Requirements

Produce a single deliverable pack containing the following.

### Part A — read the term sheet against the market

1. **Term-sheet mark-up.** Against chapter 5's market-standard reference, mark up each of the following categories with (a) what the term sheet says, (b) what the market range is, (c) whether the offered term is at, above, or below the market, and (d) the specific counter-proposal you would deliver:
   - Facility size relative to the last equity round (offered = $12M / $30M = 40%; market range 20-35%). Comment on whether the sizing is aggressive and what it implies about the lender's confidence.
   - Interest-rate spread over the reference rate.
   - Commitment fee.
   - Backend (end-of-term) fee.
   - Prepayment penalty schedule.
   - Warrant coverage as a fraction of drawn amount, strike price, and term.
   - Financial covenants — minimum cash, minimum ARR, minimum ARR growth (are they set with margin against the plan?).
   - MAC clause drafting.
   - Cure period length and presence/absence of equity-cure right.
   - Security-interest scope (IP lien).
2. **Counter-proposal memo.** A one-page memo the CFO would deliver back to the lender's counsel with the counter-terms, prioritised: what the CFO must have (deal-breakers), what the CFO would like to have (nice-to-haves), and what the CFO will concede if pushed (concessions). Justify each item briefly.

### Part B — covenant-sensitivity modelling

3. **Base-case forecast.** Build a 36-month forecast (or reuse the mod-103 driver-based model) covering ARR, revenue, gross profit, opex by category, EBITDA, net cash flow, and ending cash. Assume the Series-C closes in month 15 at $250M post-money with $50M new money and that $8M of the venture-debt facility is drawn at close and $4M at month 12. Layer the interest, backend-fee accrual, and covenant thresholds onto the forecast.
4. **Covenant-check table.** For every month in the forecast, mark whether each financial covenant is met with margin, met by tight margin, or breached. Compute the margin (dollars for the cash covenant; ARR gap for the ARR covenant; percentage-points for the ARR-growth covenant).
5. **Sensitivity runs.** Run the forecast under the following scenarios and produce the covenant-check table for each:
   - **Base case as above.** (Should meet all covenants with margin.)
   - **−10% variance:** ARR grows at 4.5% MoM instead of 5% MoM starting month 1; burn grows to $1.55M/month starting month 6.
   - **−20% variance:** ARR grows at 4% MoM; burn grows to $1.7M/month starting month 3; Tranche B is not drawn (because the $22M ARR gate is not reached).
   - **Customer-loss scenario:** in month 6, a top-3 customer representing $1.8M in ARR churns; ARR flattens for two months and then resumes at 4% MoM; NRR compresses to 108%.
   - **Series-C-slip scenario:** the base case but Series-C closes in month 20 instead of month 15 (with the interim funded by continued draw of debt and cash burn).
6. **Covenant-breach path.** For each scenario that breaches a covenant, produce a one-paragraph note on:
   - Which covenant breaches, in which month, by what magnitude.
   - What the 30-day cure path is (typically: raise equity into the cash covenant, or negotiate a waiver — note the facility has no equity-cure right).
   - What the practical consequence of the breach is (lender waiver at what cost; potential MAC-clause invocation; acceleration risk).
   - What the CFO would do 30-60 days ahead of the projected breach to avoid it.
7. **Covenant-margin summary.** For each covenant, across all scenarios, produce a table showing the minimum margin (cash covenant: minimum dollars of margin; ARR covenant: minimum ARR gap; ARR-growth covenant: minimum growth-rate gap) and the month in which the minimum margin occurs. This is the "closest to breach" view the CFO uses to see where the covenants are hair-triggered.

### Part C — the effective-cost analysis

8. **All-in effective cost model.** Compute the total-cost-of-facility across the 48-month tenor under the base-case scenario (drawn amounts, interest, commitment fee, backend fee, warrant value):
   - Interest expense (sum of monthly interest on the outstanding balance).
   - Commitment fee (paid at close).
   - Backend fee (6.5% of drawn at maturity or prepayment).
   - Warrant value under three exit scenarios: (a) company sells / IPOs in month 36 at 3x Series-B post-money ($390M); (b) 6x Series-B post-money ($780M); (c) flat to Series-B ($130M — warrants worthless because strike is at Series-B price). For each exit, compute the warrant payoff (per the mod-108 warrant conversion mechanics) and the aggregate value transferred to the lender.
   - Effective annualised yield to the lender, aggregating coupon + fees + warrant value under each exit scenario.
9. **Comparison to the equity alternative.** Compute:
   - Under the equity extension ($10M at $5.20/share extending the Series-B), what is the dilution to the founders and existing preferred?
   - Under the debt facility ($8M drawn at close plus $4M at month 12 under the base case), what is the incremental dilution from the warrant coverage under each of the three exit scenarios?
   - Which is more dilutive to the founder in each exit scenario?
   - What is the incremental interest expense over 48 months as a fraction of the cash the company would have from the equity alternative?
10. **Debt-vs-equity-vs-hybrid comparison table.** Assemble a table comparing:
    - Pure equity extension ($10M).
    - Pure debt draw ($12M facility, $8M at close).
    - Hybrid: $5M equity + $8M debt draw.
    On the following axes: cash proceeds, founder dilution, effective cost, covenant exposure, Series-C-price implications, plan-B optionality if plan slips.

### Part D — the board memo

11. **Board memo, 2-3 pages.** Contents:
    - Situation summary: current runway, 9-month trigger status, why the CFO is evaluating debt now.
    - Term-sheet mark-up summary (Part A) with the specific counter-proposal.
    - Covenant-sensitivity results (Part B) with the margin table and the scenarios that come closest to breach.
    - Effective-cost analysis (Part C) with the exit-scenario warrant-value table.
    - Recommendation: draw the debt, raise the equity extension, do the hybrid, or delay both. Defend the recommendation against the alternatives.
    - Plan-B path: if covenants tighten in 6-12 months, what specific action the CFO will take (paydown from Series-C proceeds; equity cure via emergency insider bridge; covenant amendment negotiation).
    - Board consent request: authorising the facility, the warrants, the security interest, and the officer signatures.

## Starter guidance

- **The 40% facility-to-round sizing is at the top of the market range** and reflects the lender's willingness to underwrite. Not automatically bad, but it's worth asking why — is it because the plan is strong (good) or because the lender is chasing volume in a competitive quarter (needs scrutiny)?
- **The minimum ARR ramp is worth reading carefully.** ARR going from $16M to $32M over 30 months requires sustained growth. Read the ARR covenant against the base-case forecast — where does it come closest to the covenant floor? A covenant that binds in a plausible variance scenario is a hair-trigger covenant.
- **The absence of an equity-cure right is a meaningful drafting gap.** In a distressed scenario, the equity-cure right is what lets the CFO restore compliance by raising capital. Without it, the borrower has to either negotiate a waiver (which the lender may condition on additional collateral or fees) or pay down debt. The CFO should push for an equity-cure right explicitly.
- **The MAC clause as drafted is very broad.** "Prospects and financial condition" language plus "sole discretion" gives the lender near-at-will termination. Narrow it to enumerated triggers (specific KPI deterioration thresholds; specific management-departure events) with notice-and-cure periods.
- **The IP lien is above market.** Many venture-debt facilities take an IP negative-pledge (allowing the borrower to sell IP under defined conditions) rather than a security interest. Push for the negative-pledge structure.
- **Warrant strike at the Series-B price is standard.** If the Series-B was underwritten at aggressive terms, though, the CFO should think about whether "next-round strike" (which forces an FMV redetermination if Series-C is not imminent) might be worth trading for other concessions.
- **Effective cost is not just coupon.** The 6.5% backend fee on $12M drawn is $780K of cost that shows up at maturity. Model it upfront. The warrant value under the 6x-exit scenario dominates all other cost components — model it explicitly against realistic exit outcomes.
- **The equity-vs-debt-vs-hybrid framing is important.** The right answer may not be "debt or equity" but "some of each." A $5M equity + $8M debt hybrid gives less dilution than $12M equity and less covenant exposure than $12M debt.
- **The plan-B path in the board memo is the discipline chapter 5 emphasises.** The CFO who draws debt without a specific plan for what happens if covenants tighten is drawing on hope. The plan can be as simple as "Series-C proceeds will be used to pay down the facility if the ARR ramp underperforms" — but it has to exist and be committed.

## Acceptance criteria

- **The term-sheet mark-up covers all ten categories listed in Part A** and provides a specific market-range benchmark and counter-proposal for each.
- **The covenant-sensitivity model produces a per-month covenant-check across five scenarios** with computed margins and identified breach months.
- **Each scenario that breaches a covenant has a specific cure-path and consequence note.**
- **The effective-cost model correctly captures coupon, commitment fee, backend fee, and warrant value under three exit scenarios**, and produces an effective annualised yield to the lender.
- **The debt-vs-equity-vs-hybrid comparison table quantifies the trade-off** on the six specified axes.
- **The board memo makes a specific recommendation** and names a specific plan-B path.
- **The recommended answer is defensible given the scenarios** — a recommendation to draw the debt is defensible only if the covenants have margin under realistic downside; a recommendation to raise equity is defensible only if the dilution cost is acceptable.

## Deliverables

- The term-sheet mark-up (Markdown or PDF, or annotated PDF of the term sheet).
- The counter-proposal memo (Markdown or PDF).
- The covenant-sensitivity workbook (spreadsheet), including all five scenarios and the covenant-margin summary.
- The effective-cost analysis workbook (spreadsheet).
- The debt-vs-equity-vs-hybrid comparison table (Markdown or spreadsheet).
- The board memo (Markdown or PDF).

## Extensions (optional)

- **Alternative lender term sheet.** Assume a second lender delivers a competing term sheet with: $10M facility, Prime + 400 bps, 2.0% warrant, 5% backend, narrower MAC ("specifically-enumerated adverse events including a >30% ARR contraction over trailing two quarters, departure of the CEO or CTO, or a going-concern audit qualification"), and an equity-cure right. Model the second facility against the same sensitivity scenarios and produce the head-to-head comparison memo.
- **Distress scenario.** Assume in month 8 (post-close) the company breaches the minimum-ARR covenant by ~$500K and Cash covenant is at $4.2M (tight). Draft the CFO's memo to the lender proposing a covenant amendment: what specific ask, what concessions the borrower is willing to make (increased backend, additional warrant coverage, tighter reporting), what the CFO's plan-B is if the amendment negotiation fails.
- **Post-Series-C payoff modelling.** Assume the Series-C closes as expected. The Series-C investors ask the CFO to pay off the venture-debt facility from Series-C proceeds ("clean debt into the next round"). Compute the cost of payoff (remaining balance + prepayment penalty + backend fee) and compare to the cost of leaving the facility outstanding through its original maturity. Recommend one path and defend.
- **Sensitivity to interest-rate change.** Rerun the base-case forecast with Prime moving from 8.00% to 6.00% (rate cut) and to 10.00% (rate hike). Quantify the interest-expense impact and the runway consequence.
- **Cross-check against Hercules / TriplePoint / Runway Growth public disclosures.** Look up the most recent 10-Q or investor deck of Hercules Capital, TriplePoint Venture Growth, or Runway Growth Finance and identify a portfolio company with a comparable facility size. Read the deal terms disclosed (if any) and compare to the term sheet in this exercise. Note any material term differences and hypothesise why.
