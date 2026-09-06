# Exercise 05 — Revenue-Based-Financing Decision Drill

**Estimated time:** ~2.5 hours
**Prerequisites:** Chapter 6 (Revenue-Based Financing — Pipe, Capchase, Founderpath, Arc, and the Right-Instrument Diagnosis). Familiarity with chapter 5 (venture debt) and mod-102 (unit economics) for the payback / LTV framing.

## Problem statement

Given six SaaS working-capital scenarios of varying shapes, diagnose each against the RBF right-instrument criteria from chapter 6, choose the correct funding instrument (RBF vs. bank line vs. venture debt vs. equity vs. do-nothing) for each, and defend the choice on effective-yield and use-of-proceeds grounds in a per-scenario memo. The point of the drill is to build the diagnostic muscle that distinguishes RBF's genuine right-fit range (short-term working capital against predictable ARR with a defined ROI horizon) from its most common misuse (as substitute for equity or as generic runway extension), and to translate the headline fee language of an RBF term into an apples-to-apples effective yield comparison.

## The six scenarios

Diagnose each scenario in turn.

### Scenario 1 — Channel-acquisition ramp against defined LTV

B2B SaaS, ARR $8M growing 6% MoM, NRR 122%, gross margin 78%, CAC payback 14 months, LTV/CAC 4.2x. Company wants to accelerate paid-acquisition spend in a proven channel (Google Ads on a specific keyword set with 18-month LTV data). Current spend $150K/month; company would ramp to $400K/month for six months to capture demand and expand market share. Needs $1.5M of incremental capital. Cash on hand $6M, 12 months of runway on the current plan. Equity round (Series-B) planned for 8-10 months out.

**RBF term offered:** Capchase-style advance of $1.5M against MRR, 8% flat fee ($120K), repaid via 10% of monthly revenue until $1.62M total ($1.5M + $120K) is repaid.

### Scenario 2 — Runway extension while difficult equity round is pending

B2B SaaS, ARR $4.5M growing 3% MoM (down from 7% MoM two quarters ago), NRR 102%, gross margin 71%, CAC payback 24 months. Series-A was $12M at $45M post-money 16 months ago; Series-B pipeline is thin and the CFO estimates 40% probability of closing a Series-B in the next 6 months at a flat-to-up price. Cash on hand $3M, burn $600K/month — 5 months of runway. Founder is reluctant to accept a down round or a bridge SAFE at a punitive cap.

**RBF term offered:** Arc-style RBF advance of $2M against ARR, 12% flat fee ($240K), repaid via 12% of monthly revenue until $2.24M total is repaid.

### Scenario 3 — Product build with 18-month engineering horizon

B2B SaaS, ARR $12M growing 5% MoM, NRR 118%, gross margin 74%, CAC payback 18 months. Wants to fund a dedicated 8-engineer team to build a new product line targeting an adjacent market segment. Estimated 18-month build to a shippable product; new ARR from the product not expected until month 20+. Needs $3M to fund the build. Cash on hand $9M, 10 months of runway on the current plan (excluding the new build). Series-B recently closed 6 months ago at $75M post-money.

**RBF term offered:** Founderpath-style RBF advance of $3M against contracted ARR, 15% total-repayment factor ($450K), repaid via 15% of monthly revenue until $3.45M total is repaid.

### Scenario 4 — Contracted annual-payment monetisation

B2B SaaS, ARR $20M, NRR 130%, gross margin 82%. 60% of contracts are annual paid up-front; 40% are monthly billed. The 40% monthly-billed cohort has strong retention (churn <3% per year) and represents ~$8M in contracted ARR receivables. Company has $10M cash, 8 months of runway on the current plan. Wants to accelerate hiring by 20 heads over the next 6 months to hit a Series-C-defining ARR milestone; this incremental spend adds ~$500K/month to burn. Total additional capital need: ~$3-4M for the 6-month ramp.

**RBF term offered:** Pipe-style marketplace sale of $4M of contracted monthly subscription payments at a 6% discount to face value (receives $3.76M cash upfront; obligation is to remit the future payments as customers pay). Non-recourse (customer defaults are the buyer's risk).

### Scenario 5 — Volatile / project-based revenue

Vertical-SaaS company serving the construction industry, ARR $6M but very lumpy month-to-month (seasonal patterns; some project-based contracts). Trailing quarter revenue $1.5M / $2.1M / $0.9M by month. NRR 108%, gross margin 66% (services-heavy), CAC payback 30 months. Cash on hand $4M, average burn $350K/month but variable — 12 months on the base case, 8 months in a stress case. Wants working capital of $1M to fund a specific hardware-inventory buy for a large-customer implementation (payback expected in ~9 months from that customer's payment schedule).

**RBF term offered:** Provider-A RBF advance of $1M against average trailing-12-month revenue, 10% flat fee ($100K), repaid via 15% of monthly revenue until $1.10M total is repaid.

### Scenario 6 — Stacking a fourth advance

B2B SaaS, ARR $15M growing 8% MoM, NRR 125%. Three prior RBF advances already outstanding:
- Advance 1 (Capchase): $2M drawn 8 months ago; remaining balance $0.8M; monthly obligation $180K (12% of revenue).
- Advance 2 (Arc): $1.5M drawn 4 months ago; remaining balance $1.3M; monthly obligation $110K (7.5% of revenue).
- Advance 3 (Founderpath): $1M drawn 2 months ago; remaining balance $1.05M; monthly obligation $95K (6.5% of revenue).
- Aggregate current monthly revenue-share obligation: **$385K / month, or ~26% of current MRR**.

Cash on hand $5M, burn $700K/month post-obligations (i.e., after the RBF revenue-share is remitted). Wants to draw a fourth RBF advance of $2M to fund an ambitious hiring plan ahead of the Series-B raise expected in 5-7 months.

**RBF term offered:** Provider-D RBF advance of $2M, 14% flat fee ($280K), repaid via 12% of monthly revenue until $2.28M is repaid. This would bring aggregate monthly revenue-share obligation to ~38% of current MRR.

Also note: the company has an existing venture-debt facility (from chapter 5 pattern) with a negative-covenant cap of $500K on additional indebtedness outside the facility; the RBF providers' terms are ambiguous on whether they count as indebtedness for this purpose.

## Requirements

Produce a single deliverable pack containing the following.

### Part A — the effective-yield calculation

1. **Effective annualised yield calculation for each scenario.** For each of the six scenarios:
   - Calculate the effective annualised yield on the RBF advance assuming the *expected* repayment speed given the company's stated revenue trajectory.
   - Recompute the effective yield if repayment is 30% faster than expected (favourable revenue upside).
   - Recompute the effective yield if repayment is 30% slower than expected (revenue disappoints).
   - Note explicitly that faster repayment usually means a higher effective yield in RBF structures (fixed fee amortised over shorter period) and slower repayment means a lower effective yield. Confirm the direction for each of your scenarios.
2. **Comparison-to-alternatives table.** For each scenario, compare the effective yield of the offered RBF to:
   - A bank line of credit at Prime + 200 bps (if the company would plausibly qualify).
   - A venture-debt facility on chapter-5-style terms (assume 10% coupon plus 2% warrant plus 5% backend, though smaller scenarios may not attract venture-debt lenders).
   - An equity extension at the last-round price (compute the equivalent-cost-of-capital by dividing the effective interest cost by the equivalent dilution).
   - Doing nothing (deferring the spend, running slower, or absorbing the impact on the trajectory).

### Part B — the right-instrument diagnosis

3. **Chapter 6 diagnostic checklist for each scenario.** For each scenario, walk the four right-instrument criteria:
   - Use of proceeds — short-term working capital with defined ROI horizon? Or open-ended runway extension?
   - Predictable revenue — genuinely contracted, low-churn, low-volatility ARR? Or volatile, seasonal, project-based revenue?
   - Absorbable repayment share — does the revenue-share obligation compress runway or is it comfortably within the operating margin?
   - Alternative availability — is a cheaper option (bank line, venture debt) available? Is this the best option or just the fastest?
   Categorise each scenario as right-instrument, borderline, or wrong-instrument, with the specific criterion that determines the diagnosis.

### Part C — per-scenario decision memo

4. **Per-scenario memo (half a page each).** For each of the six scenarios, write a compact memo that:
   - States the diagnosis (right-instrument / borderline / wrong-instrument).
   - Names the recommended action: take the RBF, take a specific alternative instrument, take a hybrid (e.g., RBF for the working-capital portion plus equity for the growth portion), or defer / decline the spend entirely.
   - Quantifies the effective yield of the recommended action vs. the RBF alternative.
   - Notes any specific covenant, board-consent, or existing-facility interaction the CFO must address before drawing.
   - Names the specific risk that would flip the recommendation (e.g., "if the Series-B slips by 3+ months, the RBF stack becomes the problem the Series-B has to solve").

### Part D — the consolidated CFO recommendations memo

5. **Consolidated CFO memo (2 pages).** Delivered to the CEO covering the six scenarios in a single view. Contents:
   - A comparison table showing scenario / recommended instrument / effective yield / diagnostic-category.
   - The specific "yes, right instrument" cases and why.
   - The specific "no, wrong instrument" cases and why — with the alternative recommendation.
   - The general lessons the CFO wants the CEO to internalise from the exercise (RBF is not "cheap non-dilutive capital"; effective yield depends on repayment speed; aggregate obligation is the load-bearing constraint; use-of-proceeds discipline is what separates right from wrong instrument).
   - A pattern statement the CFO wants included in the capital-plan memo going forward — "RBF may be drawn up to an aggregate monthly obligation of X% of MRR, only against use-of-proceeds satisfying [criteria], only after a documented alternative-instrument comparison, only with lender-and-board consent."

## Starter guidance

- **Compute effective yield with the amortising balance in mind.** A simple approximation: for a $1M advance with a $100K fee repaid over 12 months from 12% of $500K/month revenue = $60K/month = 12 months to repay $1.1M... but the balance amortises during those 12 months. A more precise calculation uses the average outstanding balance (~$550K over the 12 months, giving effective yield of $100K / $550K ≈ 18% annualised). Even more precisely, treat it as a schedule of payments with time-value-of-money and solve for the internal rate of return. Any of these approaches is defensible for the drill; pick one and be consistent across scenarios.
- **Faster repayment increases effective yield in most RBF products.** The fixed fee is amortised over a shorter period. A company that grows faster than expected pays a higher effective yield. This is the inverse of most debt products; expect readers to be surprised by it and call it out explicitly in the per-scenario memos.
- **The use-of-proceeds test is the hard one.** RBF for a channel-marketing ramp with a defined payback (scenario 1) is right-instrument. RBF for general runway (scenario 2) is wrong-instrument. RBF for an 18-month engineering build with revenue realisation in month 20+ (scenario 3) is wrong-instrument even though the company itself has predictable revenue — the *use* is long-horizon and the revenue-share obligation begins immediately.
- **The Pipe-style marketplace sale in scenario 4 is not legally a loan.** It is a sale of a receivable. This has accounting and cap-table implications (no debt liability created), which matters for the negative-covenant interaction with venture debt if the company has one. It also means the CFO does not have a maturity clock — the obligation is discharged as the customers pay.
- **Scenario 5's revenue volatility is the wrong-instrument tell.** A 15%-of-revenue obligation on a company whose monthly revenue oscillates from $900K to $2.1M means the dollar obligation is $135K in a low month vs. $315K in a high month — both variance dimensions hurt (in a low month, cash pressure; in a high month, less capital captured for the company). The advance is possible; the fit is poor.
- **Scenario 6 is a stacking-failure diagnostic.** A 38%-of-MRR aggregate revenue-share obligation compresses operating cash flow past the absorption threshold chapter 6 warns about. The right answer is almost certainly to decline the fourth advance and instead accelerate the Series-B raise. The venture-debt negative-covenant interaction adds a second reason to decline — a technical breach that the CFO can neither cure nor deny is a governance failure.
- **The comparison-to-alternatives table matters even when RBF is the right answer.** Even in scenario 1, the CFO wants to know whether a bank line would have been cheaper — and, if so, why the company is not using it (perhaps not qualified, perhaps too slow, perhaps a covenant issue with the bank).
- **The consolidated memo is the deliverable that generalises the lessons.** The six scenarios are pedagogical devices; the pattern statement the CFO commits to in the capital-plan memo is the operating discipline chapter 6 argues for.

## Acceptance criteria

- **Every scenario has an effective-yield calculation** with expected, faster, and slower repayment cases.
- **Every scenario has a comparison-to-alternatives table** across at least three alternatives (bank line, venture debt, equity — or noting "not available" with reasoning).
- **Every scenario has a right-instrument-diagnosis output** with the specific criterion that determined the classification.
- **Every scenario has a per-scenario memo** with a specific recommendation and a named risk-that-would-flip-the-recommendation.
- **The consolidated memo captures the general lessons** (repayment-speed / effective-yield inversion; use-of-proceeds discipline; aggregate obligation as operating constraint) and includes a specific pattern-commitment for the capital-plan memo.
- **The wrong-instrument cases (scenarios 2, 3, 6) are diagnosed as such** with specific reasoning; the borderline cases (scenarios 4, 5) are handled with nuance.

## Deliverables

- The effective-yield calculation workbook (spreadsheet).
- The per-scenario diagnostic and comparison tables (spreadsheet or Markdown).
- Six per-scenario memos (Markdown or PDF; can be one document with sections).
- The consolidated CFO memo (Markdown or PDF).

## Extensions (optional)

- **Model the stacking-cliff.** For scenario 6, compute the specific monthly-cash-flow impact of the fourth advance across the 6-month Series-B pipeline window. When does the RBF stack begin consuming more monthly cash than the venture-debt covenants require the company to maintain (i.e., where does the RBF force a covenant breach on the venture debt)?
- **Alternative provider-mix modelling.** For scenario 1, model a hybrid: $750K RBF + $750K bank line. Compute the blended effective yield and compare to the pure RBF and pure bank-line paths.
- **Retrospective at Series-B close.** For each of the six scenarios, write a one-paragraph retrospective assuming the Series-B closes as expected. Which of the RBF advances (if taken) would the Series-B investors ask to be paid off from Series-B proceeds? Which would be left outstanding? What is the effective cost of each path?
- **Provider-market check.** Research the current market participants in RBF. Are the four providers named in chapter 6 (Pipe, Capchase, Founderpath, Arc) still operating with the products described? What has changed? What new entrants have appeared? Produce a one-page current-provider landscape.
- **Cap-table impact modelling.** RBF is often described as "non-dilutive." Model the *cash-flow-dilution* effect in scenario 3 (product-build) explicitly — as the RBF revenue-share consumes a growing fraction of monthly cash, the free cash flow the equity holders have a claim on shrinks. Quantify the compression on the equity-holder claim at Series-C close.
