# Exercise 05 — Gross vs. Net and Contra-Revenue Teardown

**Estimated time:** ~2 hours
**Prerequisites:** Chapter 5 (gross vs. net revenue, contra-revenue, agent vs. principal).

## Problem statement

Analyse a set of ambiguous revenue arrangements — hybrid SaaS + pass-through, marketplace-style transactions, referral rebates, sales-tax collection, MDF payments — under ASC 606's agent-vs.-principal framework and contra-revenue rules. For each, produce the revenue classification, the P&L presentation, and the disclosure implications. Then contrast the P&L, gross margin, and EV/revenue multiple implied under two competing (but defensible) classifications for one of the arrangements.

The goal is fluency in the classification decision: after this drill you should be able to look at any revenue arrangement and produce a defensible gross-vs.-net / contra-revenue answer that survives audit and investor scrutiny.

## Scenario — six arrangements

Analyse each of the following. Use realistic dollar amounts (five or six figures each) and specific contract terms; do not analyse abstractions.

**Arrangement 1 — SaaS + third-party AI-model pass-through.** A vertical SaaS vendor bundles third-party AI-model API access into its offering. The customer signs a $10K/month subscription; $2K/month is metered AI-model access at a 40% markup over the vendor's underlying cost from the model provider. The vendor holds the customer contract, invoices for the full $10K, and bears the SLA obligation. Analyse the AI-model pass-through under agent-vs.-principal.

**Arrangement 2 — Marketplace take-rate.** A managed-services marketplace facilitates $100K/month in transactions between service buyers and independent professionals. The marketplace charges a 20% take-rate to the buyer and remits 80% to the professional. The marketplace vets professionals but does not guarantee quality, does not hold funds beyond the transaction cycle, and does not set the professional's price (professional bids their own price for each job). Analyse the classification and produce the revenue line for the month.

**Arrangement 3 — Referral rebate to customer.** A SaaS vendor offers customers who successfully refer new customers a $500 credit toward their next month's subscription. In the month, 20 referrals convert, resulting in $10K of referral rebates issued as credits. Analyse whether the rebate is contra-revenue or S&M expense and cite the ASC 606 paragraph.

**Arrangement 4 — MDF paid to a channel partner.** A SaaS vendor pays $50K in the quarter to a channel-partner reseller for jointly-branded marketing collateral and events. The partner delivers documented marketing activities (case studies produced, webinars co-hosted, trade-show booth staffed) with a verifiable fair value close to $50K. Analyse whether the $50K is contra-revenue or S&M and describe the documentation needed to support the classification.

**Arrangement 5 — Sales tax collection.** A SaaS vendor invoices customers for a $5K/month subscription and collects an additional $400/month in sales tax that it remits to state authorities. The company has not made a formal ASC 606-10-32-2A policy election. Advise on whether to make the election, the P&L impact of the election vs. no election, and the disclosure required.

**Arrangement 6 — SLA credit issuance.** A SaaS vendor's 99.9% uptime SLA was breached in the month; the vendor issues $30K in credits across affected customers. The vendor's monthly-invoiced revenue for these customers before credits would have been $500K. Analyse whether the $30K reduces revenue or is a separate expense, and how the vendor should have estimated the SLA credit exposure at the start of the contracts under the variable-consideration rules.

## Requirements

For each of the six arrangements, produce a one-page analysis with:

1. **Facts.** Restate the arrangement in your own words, calling out the contractual terms and economic realities that will drive the analysis.
2. **Framework.** State the ASC 606 test being applied (agent-vs.-principal indicators from ASC 606-10-55-36 to 55-40, or the consideration-payable-to-customer rule from ASC 606-10-32-25 to 32-27, etc.).
3. **Analysis.** Walk each indicator or criterion against the facts. For agent-vs.-principal, walk the three principal-indicators (primary responsibility, inventory risk, pricing discretion) individually.
4. **Conclusion.** State the classification. Compute the revenue amount that will appear on the P&L for the arrangement.
5. **Policy memo language.** Write the paragraph that would appear in the company's revenue-recognition policy memo describing how this class of arrangement is treated.

Then produce a **contrast analysis for arrangement 1 (the AI-model pass-through)** showing the P&L, gross margin, and hypothetical EV / revenue multiple under both defensible interpretations:

- **Principal interpretation** — full $10K/month revenue, $1.4K/month third-party cost in COGS
- **Agent interpretation** — $8K/month revenue (net of the $2K pass-through), no third-party cost in COGS (or presented separately)

For a hypothetical annualised revenue level and applied multiple, show the delta in implied enterprise value between the two interpretations. This is the exercise's punch line: classification affects headline numbers materially.

## Starter guidance

- The agent-vs.-principal analysis is fact-specific and requires all three indicators to be considered together. No single indicator is dispositive. If two indicators point one way and one the other, describe the weighting and cite ASC 606-10-55-38 through 55-39.
- For arrangement 3 (referral rebate), the key question is whether the rebate is in exchange for a distinct good or service that the vendor receives at fair value. A customer's referral of another customer is not typically a distinct good/service; the rebate is contra-revenue. Cite ASC 606-10-32-26.
- For arrangement 4 (MDF to channel partner), the key question is whether the marketing activities are distinct from the reseller relationship and delivered at fair value. Documented marketing services at documented fair value typically qualify as S&M; general rebates disguised as MDF do not. Cite ASC 606-10-32-25 and the AICPA Audit and Accounting Guide *Revenue Recognition*.
- For arrangement 5 (sales tax), the ASC 606-10-32-2A election permits the vendor to exclude sales tax from the transaction price. Most SaaS vendors elect it. Without the election, the vendor must analyse each tax individually and disclose the resulting gross revenue inclusive of tax — an unattractive presentation.
- For arrangement 6 (SLA credit), the credit reduces the transaction price (variable consideration under ASC 606-10-32-6 to 32-9). Ideally the vendor estimated the expected credit at contract inception and constrained it. If not, the credit is a "true-up" adjustment to variable consideration in the period issued.

## Acceptance criteria

- **Each arrangement has a documented five-part analysis** (facts, framework, analysis, conclusion, policy language).
- **Every judgement is tied to specific ASC 606 text.** No conclusions without a paragraph reference.
- **The AI-model contrast analysis quantifies the impact.** Both P&L presentations, both gross-margin computations, and both implied-EV computations for a specified hypothetical annualised scale and multiple.
- **The policy language is portable.** The paragraphs written for each arrangement should be usable, without rewriting, in a company's revenue-recognition policy memo.
- **Judgement is transparent.** Where facts could support more than one conclusion, name the ambiguity, state the preferred conclusion, and explain the reasoning. Do not hide close calls.

## Deliverables

- Six one-page analyses (one per arrangement), together in a single document or as separate files under a folder.
- A separate short document containing the AI-model pass-through contrast analysis with the P&L and EV computations side-by-side.

## Extensions (optional)

- Pull the revenue-recognition footnote from a real public SaaS company's most recent 10-K (SEC EDGAR) and identify which of the six arrangement patterns above their disclosure addresses. Compare their policy language to yours.
- Add a seventh arrangement — a payment-processing embedded-payments pattern where the SaaS vendor collects payments on behalf of the customer's downstream users and remits to the customer minus a processing fee. Analyse both the payment-processing component and the SaaS subscription component separately.
- For arrangement 2 (marketplace take-rate), analyse what would change if the marketplace held funds in escrow for 30 days pending buyer acceptance and guaranteed refunds for non-performance. Does that shift the classification?
