# Revenue-Based Financing — Pipe, Capchase, Founderpath, Arc, and the Right-Instrument Diagnosis

## Why this matters

Revenue-based financing (RBF) is a non-dilutive financing in which a provider advances capital against future recurring revenue — typically SaaS subscription payments or contracted ARR — in exchange for either a fixed repayment above the advance (a factor over the advance amount) or a claim on a percentage of future revenue until a total repayment cap is reached. The category has grown into a distinct capital-instrument class alongside venture debt, and includes providers like **Pipe** (a marketplace for trading contracted future subscription cash flows), **Capchase**, **Arc** (formerly Arc Technologies), **Founderpath**, and various providers targeting adjacent categories (RBF for e-commerce, RBF for creators). The specifics vary — some structures are "sell future revenue for a discount today," others are "borrow against an ARR pool with revenue-linked repayment" — but the common thread is: **capital sized to a fraction of ARR, advanced quickly, repaid from revenue, non-dilutive, non-recourse (in most structures) beyond the ARR pledged, and priced as an effective yield the CFO has to unpack from headline fee language.**

The CFO's job is to distinguish RBF's actual fit — short-term working capital against genuinely predictable ARR — from its most common misuse: as a substitute for equity growth capital when the equity round is difficult. Correctly deployed, RBF is a cheap and flexible working-capital tool that funds a specific spend against a specific cash-flow claim. Incorrectly deployed, it stacks non-dilutive-looking debt on the company that will surface as a real problem when the next equity round or a downturn comes.

## The RBF product landscape

**Pipe.** A marketplace that lets SaaS companies sell contracted future subscription cash flows to institutional buyers at a discount to face value. A company with $10K/month in contracted ARR on annual-paid contracts can sell the future 12 months of payments (or a subset) at a discount, receiving cash upfront and — economically — converting an annual contract into a paid-upfront contract for the seller (with the discount as the price). The seller (SaaS company) is not on the hook if the customer stops paying (though customer default reduces the effective yield the buyer receives). Pipe's product has evolved and the mechanics vary by cohort; historically the bid-ask spreads on the marketplace were narrow, giving effective yields to sellers that were competitive with bank lines for the same duration.

**Capchase.** A direct lender providing "growth financing" advances against monthly recurring revenue, typically as a line-of-credit-like structure. The company draws advances against a defined percentage of MRR (say 30-70%), repays via a small ongoing percentage of future revenue plus a fixed fee, and can re-draw as revenue grows. Capchase and similar providers have positioned as complements to venture debt — smaller cheque sizes, faster underwriting, more revenue-linked repayment.

**Founderpath.** RBF specifically for bootstrapped and small-VC-backed SaaS companies. Similar mechanics: advance against ARR, repayment from future revenue, non-dilutive. Founderpath and adjacent providers (Uncapped, Wayflyer for e-commerce, Clearco pre-2022) built businesses on the "capital for SaaS founders who don't want to dilute" narrative.

**Arc.** A neobank plus RBF product for early-stage software companies. Combines banking (like Mercury / Brex) with advance-against-revenue mechanics. Positions RBF as a natural adjunct to the company's operating account, with underwriting drawing on the banking-side visibility into cash flows.

The category has consolidated and evolved since 2022. Some providers have exited or been acquired (e.g., Clearco's restructuring); others have re-focused. The CFO should treat the specific provider list as time-varying and re-check current market participants when evaluating an RBF path.

## The mechanics — advance, repayment, and effective yield

The specific mechanics vary by provider, but the two dominant structures are:

**Structure 1 — Discounted-purchase of future cash flows.** The provider (or a buyer on a marketplace) purchases the right to receive a defined stream of future subscription payments at a discount to face value. The company receives cash upfront equal to face minus discount. The company's obligation is to remit the future payments as they are received; the company is not a borrower and does not have a debt liability (from an accounting standpoint) — the transaction is a sale of a receivable. Effective yield to the buyer is the discount amortised over the payment period.

**Structure 2 — Line of credit against ARR with revenue-share repayment.** The provider extends a line of credit or a series of advances, drawing against a defined percentage of ARR or MRR. Repayment is via automatic debit of a defined percentage of future revenue (say 8-15% of monthly revenue) plus a fixed fee, until a total repayment cap is reached (typically 1.05× to 1.20× the advance amount, sometimes higher for smaller / riskier companies). This is legally a loan; the company records a debt liability. Effective yield to the provider varies by how quickly the revenue-share repays the advance.

**The effective-yield unpack.** The CFO's job with any RBF term sheet is to translate the headline fee language into an effective annualised yield, so the RBF cost can be compared to a bank line, venture debt, or credit-card working-capital cost on the same basis.

Simple example: an advance of $500K with a $50K fee (total repayment $550K), repaid over 12 months from 10% of monthly revenue. If revenue is $250K / month, the repayment runs 10% × $250K = $25K / month, and $550K takes 22 months to repay. The effective yield calculation has to account for the outstanding balance amortising as repayments come in; a rough approximation for this example produces an effective annualised yield in the ~10-12% range. Note the same product with a $50K fee but repaid in only 6 months (much higher monthly revenue capture) produces a much higher effective yield — the fixed fee is amortised over a shorter period, so faster repayment increases the effective yield.

The pattern to internalise: **the same RBF product can be cheap or expensive depending on repayment speed.** A company with strong revenue growth that repays fast is paying a higher effective yield than the company that repays over a longer horizon. This is the inverse of most debt products (where faster repayment saves interest) and is often mis-modelled in first-pass analysis.

**The compare-to-alternatives table.** Once the effective yield is calculated, the CFO compares:

- Bank line of credit — usually the cheapest for companies that qualify (mid-single digits over a reference rate), but often unavailable to pre-cash-flow-positive startups.
- Venture debt (chapter 5) — high-single to low-double digit effective yield including fees and warrants, longer duration.
- Credit-card working-capital advance — expensive (mid-teens or higher effective yield) but fastest to underwrite.
- RBF — highly variable depending on structure and repayment speed; competitive with venture debt for the right use case, expensive for the wrong one.

## When RBF is the right instrument

**Right-instrument diagnosis.** RBF fits when *all* of the following hold:

- The use of proceeds is **short-term working capital** with a defined return horizon. Fund a specific inventory buy, a specific channel-marketing spend against a defined LTV, a specific ramp of a new customer segment where the payback is measured in months, not years.
- The revenue against which the advance is drawn is **genuinely predictable** — real contracted ARR with strong NRR, low churn, defined customer cohorts, defensible margin. RBF against volatile revenue re-prices badly.
- The company can absorb the revenue-share repayment (or the discount on the receivable sale) **without impairing runway** on the underlying operating plan. RBF that consumes a growing fraction of monthly revenue quietly compresses the equity investors' claim on future cash flows.
- The alternative is either not available (bank line unavailable, venture debt too slow to underwrite) or would be materially more expensive on the effective-yield basis.

**Common right-fit examples.**

- SaaS company with strong NRR wants to accelerate a customer acquisition ramp in a defined channel with a known payback period (12-18 months). RBF advances 6-12 months of ARR against the ramp; the ramp produces the ARR that repays the advance.
- SaaS company with mature, predictable ARR wants to fund a specific product build (18 months of dedicated engineering headcount) without a fresh equity raise. RBF drawn against ARR funds the build; the incremental ARR the build generates repays.
- E-commerce or usage-based company wants inventory or infrastructure to serve a known demand pull. RBF (from an e-commerce-specialist provider) funds the inventory; the sale of that inventory repays.

## When RBF is the wrong instrument

**Wrong-instrument diagnosis.** RBF is a poor fit when *any* of the following hold:

- The use of proceeds is **runway extension** without a specific ROI horizon. RBF drawn to fund general operations while the equity raise closes stacks a revenue-share obligation on the company that will compress its future cash flows even after the equity closes.
- The revenue against which the advance is drawn is **not genuinely predictable** — churn is high or trending up, cohort economics are still being worked out, contracts are month-to-month, or the growth rate is highly volatile. RBF against un-predictable revenue may still close but re-prices at a much higher effective yield.
- The company is **using RBF as a substitute for equity growth capital**. Equity is the appropriate instrument for funding growth against multi-year returns; RBF's revenue-share mechanic makes it structurally wrong for long-horizon investments.
- The company would have to draw enough RBF that the revenue-share consumes a **material fraction of monthly revenue** (typically 10-20% or more). At that point the RBF is throttling the operating cash flow and reducing the runway the company thought it had.

**Common wrong-fit examples.**

- Company on a difficult equity fundraise takes RBF to extend runway to close the equity. RBF closes fast; equity slips; RBF revenue-share consumes 15% of monthly revenue; the next equity conversation now includes "how do we pay off the RBF stack" as a term.
- Company with lumpy revenue (seasonal, project-based, enterprise contracts with long ramp periods) takes RBF against average ARR. Revenue-share in low-revenue months eats disproportionately into cash; the company breaches an implicit or explicit minimum-revenue threshold and re-negotiates from weakness.
- Company builds an R&D-heavy product (18-month build to a new large market) with RBF-funded engineering. The revenue during the build period is insufficient to make meaningful repayment progress; the company arrives at product-launch time with the RBF outstanding, consuming a growing fraction of the new-product revenue.

## The stacking failure mode

Because RBF closes fast and doesn't dilute, it is easy to draw repeatedly. A company that takes an RBF advance in Q1, another in Q2, and another in Q3 can find that the aggregate revenue-share obligation is consuming 25-30% of monthly revenue. That fraction becomes the cash flow the equity investors would otherwise have had a claim on. The next equity raise is now underwritten against a company whose operating margin is compressed by the RBF stack; the equity investors either pay less (lower valuation) or require the RBF to be paid off from the equity proceeds (which reduces the proceeds available for growth).

The discipline: **treat each RBF advance as a discrete decision with a specific ROI and a specific repayment horizon.** Do not treat the RBF facility as a continuous working-capital source that can be tapped at will. Track the aggregate revenue-share obligation as a percentage of monthly revenue and cap it (typically at 5-10%) as a hard operating constraint.

## The CFO's pre-signing package

For any RBF advance:

- **Use-of-proceeds memo.** One paragraph. Specifically what this advance funds, what the expected ROI is, and over what horizon the ROI materialises. If the answer is "runway extension" without a specific use, the answer is "not RBF — reconsider."
- **Effective-yield calculation.** All-in effective annualised yield including headline fee, expected repayment speed, and any additional charges. Compared to bank line (if available), venture debt (if under negotiation), and other RBF providers on the same basis.
- **Repayment-share sensitivity.** How does the revenue-share fraction change under +/- 20% revenue variance? Is any threshold triggered under a downside case?
- **Aggregate-obligation check.** What is the total monthly revenue-share obligation across all RBF facilities post-advance? Compared to a hard cap (say 5-10% of monthly revenue).
- **Board and lender consent.** RBF above a threshold typically requires board consent and may require existing lender (venture-debt lender if any) consent under negative-covenant restrictions on incurring debt.

## RBF and venture debt — the interaction

Companies with a venture-debt facility need to read the negative-covenant restrictions on additional indebtedness before drawing RBF. Some venture-debt facilities include RBF within the debt-incurrence cap; others explicitly exclude it (treating discounted-purchase-of-receivables as a sale rather than borrowing); others require lender consent above a defined amount. The CFO who draws RBF without checking risks a technical covenant breach that gives the venture-debt lender a wedge for future negotiation.

Reverse case: RBF providers may restrict future debt incurrence by the company. The CFO reads all restrictions before drawing.

## Common failure modes

- **Treating headline fee as effective cost.** A 5% fee sounds cheap. A 5% fee on capital repaid over 5 months is a ~24% annualised effective yield. Do the math.
- **Drawing RBF to extend runway to a difficult equity raise.** The specific wrong-instrument case. RBF stacked while the equity slips creates the double problem the next equity round has to solve.
- **Not tracking the aggregate revenue-share fraction.** Multiple advances in the same year can quietly stack the monthly obligation past the operating-margin absorption capacity.
- **Not modelling repayment speed against realistic revenue growth.** Faster repayment means higher effective yield in most RBF structures; a company that under-estimated its own growth over-paid.
- **Skipping the interaction with venture debt covenants.** Silently breaching a debt-incurrence covenant is a governance error that shows up at the worst time.
- **Assuming RBF is "non-dilutive" in a full sense.** RBF is dilutive in a cash-flow sense — the revenue-share reduces the cash available to equity holders. It does not dilute the cap table, but it does dilute the free cash the equity claim rests on.

## What good looks like

A CFO who has this material installed:

- Diagnoses each RBF opportunity against the right-instrument criteria: short-term working capital, predictable revenue, defined ROI horizon, absorb-able repayment share.
- Rejects RBF for runway-extension-without-purpose and for substitute-for-equity use cases.
- Calculates the effective annualised yield on every advance, comparing against alternatives on the same basis.
- Tracks aggregate revenue-share obligation as a hard operating-constraint metric.
- Checks negative-covenant interactions with venture debt and other facilities before drawing.
- Treats RBF as a discrete, small, purposeful working-capital tool — not as a continuous funding source that can be tapped freely.
- Communicates to the board that RBF is being used, at what effective cost, and against what specific ROI horizon. Includes RBF in the capital-plan document from chapter 1.

## Summary

- Revenue-based financing (Pipe / Capchase / Founderpath / Arc / adjacent providers) advances capital against future recurring revenue, non-dilutive, repaid via revenue share or discounted receivable purchase.
- Right instrument: short-term working capital against predictable ARR, funding a specific ROI within a defined horizon. Wrong instrument: runway extension without purpose, or substitute for equity growth capital.
- Effective yield depends critically on repayment speed. Faster repayment usually means higher effective yield in RBF structures. Model it explicitly.
- Aggregate revenue-share obligation across stacked advances can compress operating cash flow past absorption capacity. Cap it as a hard operating metric.
- RBF interacts with venture debt and other facilities via negative-covenant restrictions on debt incurrence. Check before drawing.
- RBF is dilutive in a cash-flow sense even though it does not dilute the cap table. Communicate that honestly in the board memo.

Chapter 7 turns to the **growth-stage capital menu** — the ATM offerings, PIPEs, Reg A+ mini-IPOs, and 144A private placements that a pre-IPO or newly-public CFO adds to the equity / venture-debt / RBF choice set as the company scales.
