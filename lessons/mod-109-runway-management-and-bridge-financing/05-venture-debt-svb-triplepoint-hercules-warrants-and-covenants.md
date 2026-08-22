# Venture Debt — SVB / TriplePoint / Runway Growth / Hercules-Style Term Loans, Warrants, and Covenants

## Why this matters

Venture debt is a term loan extended to a venture-backed company by a specialised lender, typically sized as a fraction of the most recent equity round, secured by all assets of the company, drawn to extend runway between priced rounds, and paired with **warrant coverage** and a **covenant package** that give the lender equity-linked upside and a set of triggers under which the loan can be accelerated. It is a well-established capital-instrument class with a specific right-fit range and a well-known failure mode.

The active lenders in this segment are largely known by name — the historical anchor **Silicon Valley Bank** (now part of First Citizens BancShares after the March 2023 failure and receivership); the specialty BDCs and specialty-finance lenders **Hercules Capital (NYSE: HTGC)**, **TriplePoint Venture Growth BDC (NYSE: TPVG)**, and **Runway Growth Finance (Nasdaq: RWAY)**; the platform lenders emerging from bank consolidation (**HSBC Innovation Banking**, **Stifel Venture Banking**, **Comerica**); and various specialty structured-credit providers. Each has broadly similar term-sheet architecture but different appetite (stage, sector, cheque size) and different covenant styles.

The CFO's job is to read a venture-debt term sheet against the specific architecture the market has settled on, to price the debt against the equity alternative, and — critically — to know when venture debt is the right tool for extending runway to a better next round versus when it is the wrong tool that will accelerate a failure. That last diagnostic is what makes this a CFO-grade decision.

## When venture debt fits — and when it does not

**Venture debt extends runway when:**

- The company is on plan or credibly ahead of plan and needs 6-12 months of additional runway to hit a specific milestone that will materially improve the next round's price. The debt costs a modest coupon and 1-2% warrant coverage; the milestone unlock is worth several times that.
- The company has recently closed a well-priced equity round and is drawing debt as a "non-dilutive top-up" that extends the runway that round bought by 6-9 months. This is the classic and most common use pattern — draw debt within 12 months of the equity close.
- The company has predictable revenue (SaaS ARR with strong NRR), well-understood unit economics, and cash-flow-positive-within-the-facility-term visibility. The lender can underwrite the amortisation schedule against the projected cash generation.
- The proceeds fund a defined use (working capital in a defined ramp, a defined product build, a defined customer implementation) that the company can point to as the source of the return.

**Venture debt accelerates failure when:**

- The company is off-plan and running low on cash, and is using debt to defer the equity conversation. When the debt draws down and the next equity round still cannot close, the lender's covenants tighten, the facility is accelerated, and the cash the company thought it had is now claimed by the debt.
- The company draws the debt against a plan whose covenant thresholds (usually a minimum-cash covenant of one or two months' burn) will be violated in a plausible KPI-slippage scenario. The covenant breach triggers the lender's rights and the CFO ends up negotiating a workout at the worst possible time.
- The debt is drawn shortly before an expected priced round and the priced round slips or downsizes. The debt now compresses the runway available to close the next round, sometimes below the six-month leverage band.
- The debt is used to fund a strategy the equity investors would have declined to fund at their price. The debt was cheaper, but the equity investors' pass was a signal about the strategy — and the debt lender may not have had the same insight.

The general framing: **venture debt is a tool for adding runway on top of an already-viable equity plan, not for substituting for equity in a distressed situation.** A stress-priced venture-debt draw usually makes the next crisis worse, not better, because the lender is a secured creditor whose interests will be paid before the shareholders' when the crisis resolves.

## The market-standard venture-debt term sheet

**Facility size.** Typically 20-35% of the most recent equity round for a "growth stage" term loan; smaller (up to $2-5M) for very-early-stage or bank-provided lines. Very growth-stage-plus BDC-provided facilities can be $30-100M+ for larger companies.

**Structure — term loan.** The classic venture-debt structure is a term loan with:

- **Draw period** — typically 6-12 months from close during which the borrower can draw the loan (either as a single lump sum or in defined tranches). Undrawn amounts terminate at the end of the draw period.
- **Interest-only period** — typically 12-24 months from close during which the borrower pays only interest. This is the runway-extension window.
- **Amortisation period** — typically 24-36 months after the interest-only period during which principal amortises monthly.
- **Total tenor** — commonly 36-60 months from close, sometimes longer for the largest BDC deals.
- **Interest rate** — floating, tied to the Prime Rate or SOFR plus a spread. A typical spread for a growth-stage venture-debt facility is 300-700 bps over the reference rate, which puts effective coupons in the high-single-digit to low-double-digit range in most rate environments. Investment-grade or particularly-attractive borrowers pay lower; earlier-stage or higher-risk borrowers pay higher.

**Fees.**

- **Commitment fee** — 0.5-1.0% of the facility size, paid at close.
- **End-of-term (backend) fee** — 3-8% of the drawn amount, paid at maturity or upon prepayment. This is a material cost and often overlooked in first-pass modelling.
- **Prepayment penalty** — declining schedule (typically 3% in year 1, 2% in year 2, 1% in year 3), designed to lock in the lender's expected yield.
- **Legal fees** — the borrower typically pays the lender's counsel fees (often capped at a stated amount).

**Warrant coverage.** The lender receives warrants for common or preferred (usually the most recent preferred class, or a "shadow" preferred that mirrors the most recent class), sized as a percentage of the loan amount. Typical coverage: 1-3% of the loan for lower-risk / larger deals, 3-7% for higher-risk / smaller deals. Strike price at the last-round price per share; term commonly 7-10 years. The warrants are the venture-debt lender's equity kicker; a company that grows well through the facility term makes the warrants meaningfully valuable.

**Security interest.** All-asset first-priority lien on the company's assets. The lender files a UCC-1 covering substantially all assets. Some facilities negative-pledge intellectual property (allowing sale of IP under defined conditions) rather than taking a security interest in the IP directly; others take the IP lien too. Subordination arrangements exist for junior facilities and for IP-specific carveouts.

**Guarantees / cross-guarantees.** Subsidiaries typically guarantee the parent's borrowings and vice-versa. Foreign subsidiaries are sometimes excluded to avoid deemed-dividend tax issues.

## The covenant package

The covenant package is where the CFO does the most careful reading. Covenants come in three classes.

**Affirmative covenants.** Things the borrower must do. Deliver audited annual financials within a defined window (typically 120-150 days post fiscal-year end). Deliver quarterly unaudited financials (typically 45-60 days post quarter-end). Deliver monthly management-prepared financials (typically 30 days post month-end). Deliver an annual budget by a defined date. Maintain insurance. Maintain corporate existence. Comply with laws.

**Negative covenants.** Things the borrower may not do without the lender's consent. Incur additional debt above defined thresholds. Make investments outside a defined permitted-investments basket. Grant liens outside a defined permitted-liens basket. Pay dividends. Buy back stock. Make loans to affiliates. Merge or dispose of a material subsidiary. Change fundamental business.

**Financial covenants.** The load-bearing covenants for a venture-debt facility. Two are near-universal:

- **Minimum cash / liquidity covenant.** The borrower must maintain a minimum cash balance (or minimum cash-plus-available-borrowing-base) at all times. Typical formulations: (a) a hard-dollar floor (say $10M); (b) a coverage ratio (say 1.0x-2.0x months of trailing burn); (c) a combination. This is the covenant that fires first in a distress scenario — if burn accelerates or a receivable is delayed, the cash floor can be breached in a month.
- **Minimum ARR / revenue / growth covenant.** The borrower must maintain (or grow toward) a defined ARR or revenue level. Typical formulations: (a) trailing quarter ARR ≥ $X; (b) ARR growth over trailing 12 months ≥ Y%; (c) net-new-ARR quarterly ≥ $Z. Growth-stage lenders lean heavily on ARR growth; earlier-stage lenders may use gross-revenue floor instead.

Some facilities add additional financial covenants — minimum gross margin, minimum EBITDA (rare in venture debt because most borrowers are burning cash), maximum debt/ARR ratio.

**Trigger covenants (Material Adverse Change).** The **MAC clause** gives the lender the right to accelerate the facility or refuse further draws upon a "material adverse change" in the borrower's business, prospects, or financial condition. The MAC is broadly worded by lender-favoured drafters and narrowly qualified by borrower-favoured drafters. A well-negotiated MAC excludes changes that affect the industry generally, pre-existing conditions the lender knew about at close, and specifically-enumerated events the borrower can control. Broad MAC clauses effectively give the lender an at-will termination right; narrow MACs give the lender a specific tool for genuine deterioration.

The MAC is what wakes the CFO up. Financial-covenant breaches happen mechanically and are usually curable within the negotiated cure period. MAC calls are subjective and can be triggered by events the CFO cannot cure — a market-wide downturn, the departure of a founder, a critical customer loss. The CFO's fight in negotiation is to narrow the MAC to specifically-enumerated triggers and to obtain notice-and-cure periods that provide meaningful protection.

## Covenant cure periods and grace periods

Well-drafted facilities give the borrower a **cure period** after a financial-covenant breach — usually 30-60 days during which the borrower must restore compliance (typically by raising equity, negotiating a waiver, or paying down debt to restore the covenant). Some facilities allow **equity cure rights** — the borrower can restore a minimum-cash covenant by raising additional equity of a defined amount and adding it to the cash calculation. Equity cure rights are borrower-favourable and worth negotiating for.

**Anti-hair-trigger drafting.** The CFO reads the covenants against the reasonable variance in the operating plan and asks: "if we miss the plan by 10-15%, do we breach any of these covenants? If we lose one major customer, do we breach? If the market turns for six months, do we breach?" The covenant thresholds should be set with realistic margin against the plan, not at the exact plan level.

## Warrant coverage — the specific economics

**Warrant coverage as a fraction of loan amount.** A typical formulation: "warrants covering 2% of the loan amount at the Series-B price per share." If the loan is $20M and the Series-B price was $10 per share, the warrants cover $400,000 / $10 = 40,000 shares. If the Series-B post-money was $200M and there were 20M shares outstanding, that is 0.2% of the fully-diluted cap table.

**Strike price and term.** Strike at the last-round price is standard; some facilities strike at the "next round" price (which forces a fair-market-value redetermination if the next round is not imminent). Term is usually 7-10 years, sometimes with early-termination clauses on change-of-control.

**Cashless exercise.** Warrants typically allow cashless exercise (the holder receives shares equal to the value of the exercised warrants divided by the current FMV, without paying cash strike). This is the standard mechanic that makes venture-debt warrants easy to exercise in an IPO or a sale.

**The CFO's model.** Effective yield on the debt is not just the coupon. It is the coupon plus fees plus the amortised warrant value. A 2% warrant on a $20M loan whose issuer eventually is worth 10× the strike value delivers $4M of value to the lender ($20M × 2% × 10× - $20M × 2%). That value has to be modelled as part of the "true cost" of the debt against the equity alternative.

## Venture debt vs. equity — the trade-off

At the moment the CFO is choosing between drawing venture debt and raising equity to add runway, the trade-off has three axes:

**Dilution.** The equity alternative dilutes the founders and existing preferred by the round-size fraction of post-money (say 15-20%). The debt dilutes by only the warrant coverage (say 0.2%). This is the axis on which venture debt looks most attractive.

**Cost.** The equity alternative has no cash cost until exit; the debt has a coupon (say 10% annualised on the drawn amount), fees (say 3% at close and 5% at back-end), and prepayment penalties if you pay it down early. The interest is a real cash cost that reduces runway.

**Risk.** The equity alternative places all risk on the shareholders — no covenants, no acceleration, no maturity date. The debt places specific risks on the shareholders through the covenant package — a covenant breach or MAC call can accelerate the facility, and the secured position means the lender is paid before the shareholders in a distress scenario. In the extreme, a covenant breach that the company cannot cure can force a sale of the company on terms that primarily benefit the lender.

The default reading is: **draw venture debt within 6-12 months of a strong equity round to extend runway to a well-defined next milestone; do not draw venture debt as a substitute for equity when the equity round is difficult to close.** The right-time draw compounds a good story; the wrong-time draw compounds a bad one.

## What the CFO produces before signing a venture-debt term sheet

The pre-signing package:

- **The term sheet, marked up.** Against a well-drafted market-standard reference (a company that has signed one before, or counsel's template), the CFO's mark-up flags: covenant thresholds (are they set with margin?), MAC drafting (is it narrow?), warrant coverage (is it at market?), backend and prepayment fees (are they in the market range?), draw-period length, cure rights, and any lender-specific provisions.
- **The covenant sensitivity model.** A model that runs the base case, the +/- 10% variance, the +/- 20% variance, and a customer-loss scenario against every financial covenant. The output: for each scenario, does any covenant breach? If yes, what is the cure path? If no, how much margin does the covenant have?
- **The effective-cost analysis.** All-in cost of the debt including coupon, fees, warrant value under multiple exit scenarios, and prepayment penalty if repayment is triggered by the next equity round. Compared to the equity alternative on a per-share-of-founder-dilution basis.
- **The board memo.** One-to-two page recommendation. Includes: why debt is being drawn now (specific runway extension to specific milestone), lender selection and why, term-sheet marked up, covenant sensitivity results, effective cost, and the plan-B path if covenants tighten.
- **The board consent.** Standard consent authorising the facility, the warrants, the security interest, and the officer signatures on the loan documents. Reviewed against the protective-provisions list — venture debt above threshold usually requires preferred approval.

## Common failure modes

- **Signing a facility whose covenants would be breached by a 10-15% miss to plan.** The plan-to-covenant margin is the CFO's real protection. Set covenants against a realistically-conservative plan, not against the aspirational plan.
- **Signing a broad-MAC facility without pushing to narrow it.** A broad MAC gives the lender an at-will exit; the CFO who accepts a broad MAC has under-negotiated the most important protection in the facility.
- **Underestimating the backend fee.** A 6% end-of-term fee on a $30M loan is $1.8M of true cost that shows up at maturity — well after the plan was made. Model it upfront.
- **Drawing debt to postpone an equity conversation.** The specific failure mode. If the equity round is difficult, the debt makes the next equity round harder (more debt to be paid off; more covenants to be navigated).
- **Not maintaining the lender relationship after close.** Lenders who see the borrower's monthly financials on time, who get honest updates when trends change, and who are consulted before major decisions become collaborative when covenants tighten. Lenders who first hear from the borrower via a missed covenant certificate become adversarial.
- **Underestimating the warrant value in the effective-cost model.** A 2% warrant on a growth company can be worth many times the coupon. Model it against realistic exit scenarios.
- **Assuming the lender will always be willing to waive.** In a benign market, lenders waive covenant breaches routinely. In a stressed market — the moment when the breach is most likely to happen — waivers become more expensive and can require pledging additional collateral, drawing on the equity investors for an equity cure, or amendment fees.

## What good looks like

A CFO who has this material installed:

- Draws venture debt as a runway extension on top of a strong equity plan, not as a substitute for a difficult equity raise.
- Sets covenant thresholds with realistic margin against the operating plan, not at the plan level.
- Negotiates the MAC to specifically-enumerated triggers with notice-and-cure periods, and pushes hard against broad "prospects and financial condition" language.
- Models the effective cost including coupon, fees, warrant value, and prepayment implications, and compares it to the equity alternative on a per-founder-share basis.
- Maintains the lender relationship with on-time financials, proactive updates on trends, and consultation before material decisions.
- Reserves the plan-B path (an equity raise or a paydown from a subsequent round) that would restore compliance if covenants tighten, and documents it in the board memo.
- Repays or refinances the facility on a schedule that leaves the next equity round with clean debt.

## Summary

- Venture debt is a term loan from a specialised lender (SVB / HSBC IB / Hercules / TriplePoint / Runway Growth / Stifel / Comerica), typically 20-35% of the most recent equity round, secured by all assets, with an interest-only period followed by amortisation.
- Standard economics: floating coupon of Prime or SOFR plus a spread (all-in high-single to low-double digits in most rate environments), commitment fee at close, 3-8% back-end fee at maturity or prepayment, warrant coverage of 1-3% (large / lower-risk) to 3-7% (small / higher-risk) at the last-round price.
- The covenant package includes affirmative and negative covenants and financial covenants (near-universal: minimum cash / liquidity and minimum ARR / growth). The MAC clause is the load-bearing subjective trigger; narrow it.
- Venture debt fits when the company is on plan and drawing debt within 6-12 months of a strong equity round to extend runway to a defined milestone. It accelerates failure when drawn as a substitute for a difficult equity raise.
- The CFO's pre-signing artifacts: marked-up term sheet, covenant sensitivity model, all-in effective-cost analysis (coupon + fees + warrant value), board memo, and board consent.
- Common failure modes: covenants without margin; broad MAC; underestimating backend fees and warrant value; drawing to postpone equity; letting the lender relationship go cold before covenants tighten.

Chapter 6 turns to a different non-dilutive instrument — revenue-based financing — with a very different fit range (short-term working capital against predictable ARR, not runway extension) and a different set of failure modes centred on the "wrong-instrument-substitute-for-equity" trap.
