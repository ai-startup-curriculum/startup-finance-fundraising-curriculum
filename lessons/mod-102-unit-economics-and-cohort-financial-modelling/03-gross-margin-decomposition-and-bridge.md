# Gross-Margin Decomposition and the Bridge

## Why this matters

Gross margin is the single number that determines whether a startup is a *software business* or something else wearing software's clothing. Every downstream metric that matters — LTV, payback, Rule of 40, revenue multiples — is anchored to gross margin. A $10M-ARR business at 80% gross margin has $8M of contribution to cover S&M, R&D, and G&A. The same business at 55% gross margin has $5.5M — 30%+ less capital-efficient with everything else held constant. In fundraising, gross margin is the number an investor uses to decide which *comp set* your company belongs to: SaaS companies in the 75-85% range, marketplaces in the 15-40% take-rate range, network-effect consumer businesses in the 30-70% range, hardware-plus-software in the 40-60% range. Land in the wrong band and the revenue multiple applied to your business collapses by half.

The failure mode: a founder reports "80% gross margin" as a headline and, in diligence, the number turns out to include some or all of these missteps — customer-success salaries booked as G&A instead of COGS (inflates GM by 5-15 points), free-tier infrastructure booked as R&D instead of COGS (inflates GM by 3-8 points), payment-processing fees booked as contra-revenue instead of COGS (inflates GM by 2-4 points), or a marketplace reporting GMV as revenue instead of net take-rate (can inflate revenue by 5-20×). The reconstructed number after diligence is 10-25 gross-margin points lower, and the round re-prices.

This chapter installs the CFO-grade gross-margin discipline: what belongs in COGS, how to decompose it into buckets that a board and an investor recognise, the SaaS and marketplace bands that trigger investor scepticism, and the gross-margin *bridge* — the reconciliation from revenue down to gross profit that survives diligence.

## What GAAP says and where the judgement is

GAAP is prescriptive about revenue recognition (ASC 606, covered in [`mod-101`](../mod-101-startup-accounting-foundations/)) but relatively silent on the specific line-item classification of costs on the P&L. The SEC's [Regulation S-X, Rule 5-03](https://www.sec.gov/) prescribes the format for public-company income statements but leaves the definition of "cost of revenue" to management judgement within the constraint that the classification be consistent and disclosed. FASB provides no equivalent to ASC 606 for COGS classification.

The consequence: two SaaS companies with identical economics can report gross margins that differ by 15+ points based on where they draw the line between COGS and operating expenses. This is not fraud — it is judgement — but a CFO who does not have a defensible position on where every dollar sits will lose the argument with a diligence firm applying a stricter definition.

The judgement is anchored to the [SaaS-metrics practitioner canon](https://www.forentrepreneurs.com/saas-metrics-2/), Bessemer's public benchmarks and comp reports (via [Bessemer Cloud Index / Nasdaq: EMCLOUD](https://cloudindex.bvp.com/)), Meritech Capital's [SaaS comps](https://www.meritechcapital.com/saas-comps-table), and the public-company disclosure practice observable in 10-K "cost of revenue" footnotes of listed SaaS companies. The convergent industry practice sets the norm; deviations are permissible but must be disclosed.

## The five canonical COGS buckets for a SaaS business

The bucketisation that a board and an investor will recognise decomposes cost of revenue into five categories. All five belong in COGS, above the gross-profit line.

**1. Hosting and infrastructure.** Cloud compute (AWS, GCP, Azure), managed database services, storage, bandwidth, CDN. Any infrastructure whose cost scales with customers or with customer usage. For companies with materially different unit economics in specific cloud regions, this should be decomposed further; for most companies a single line is enough. Do *not* include the corporate IT laptop-and-Zoom bill (that is G&A) or the development / staging cloud environments (that is R&D).

**2. Third-party cost of revenue.** Any per-customer or per-transaction third-party fee: payment processing (Stripe, Adyen), telephony (Twilio) for a customer-facing communications product, LLM inference fees passed through to end customers, per-message SMS fees, per-customer identity-provider fees (Auth0 above the free tier), per-customer analytics fees where the cost scales with customer volume. This is the fastest-growing COGS bucket in the AI-native cohort of startups where inference is a material fraction of unit cost. <!-- needs-research: cite a recent OpenView / Bessemer / Emergence report on AI-native COGS structure and the inference-cost bucket size at Series-A and Series-B -->

**3. Customer support.** Fully-loaded compensation for the customer-support function — Level 1 support that responds to tickets, escalation engineers, on-call rotations for enterprise-tier customers. The rule: *if the function's headcount scales with customer count, it belongs in COGS.* A support team that today serves 500 customers with 10 people and expects to serve 5,000 customers with 25 people is a COGS function; if that team's headcount is decoupled from customer count and grows on a strategic schedule, it is closer to G&A. Most companies at Series-A and beyond have crossed the threshold where support belongs in COGS.

**4. Customer success (delivery-portion) and professional services.** The customer-success function usually splits between an *ongoing account-management* portion and an *implementation and delivery* portion. The delivery portion — the CSMs and implementation engineers who are on-site or on-Zoom performing the initial deployment of the product — belongs in COGS. The ongoing account-management and expansion-selling portion is more properly S&M (it is buying expansion revenue) and should not be in COGS. Companies with a formal professional-services line — paid implementation, custom-integration engineering, embedded training — book both the associated revenue and the associated cost above the gross-profit line; the professional-services gross margin is typically 15-40% (thin) and drags the blended gross margin down, which is why it is often reported separately from the SaaS-subscription gross margin.

**5. Application and integration hosting for customer environments.** For companies that operate customer-specific environments (dedicated single-tenant deployments, on-premises appliances, per-customer VPCs), the incremental infrastructure and DevOps effort to run those environments belongs here. This bucket is often trivial for pure multi-tenant SaaS and material for regulated-industry SaaS (health tech, fintech, defense tech) that runs isolated tenant infrastructure.

Two categories that a founder often tries to put in COGS but generally do *not* belong there:

- **R&D salaries** — engineering headcount building the product is R&D, not COGS. The narrow exception: DevOps and site-reliability engineering whose day-to-day is production operations rather than product development. A defensible split allocates SRE compensation between R&D (build) and COGS (run) based on time-tracked activity.
- **General-and-administrative overhead** — finance, HR, IT, executive compensation. These are G&A regardless of how much of it "supports" the customer function. Attempting to allocate G&A into COGS to improve gross margin is a red-flag pattern in diligence.

## The SaaS gross-margin bands and the 70% threshold

The published SaaS-benchmark data — [OpenView's annual SaaS Benchmarks report](https://openviewpartners.com/), [Bessemer's Cloud Index](https://cloudindex.bvp.com/), [Meritech's SaaS comps](https://www.meritechcapital.com/saas-comps-table), and the 10-K disclosures of listed SaaS companies — converge on approximately these bands for subscription-revenue gross margin:

| Segment | Typical subscription gross margin | Notes |
|---|---|---|
| Best-in-class pure SaaS | 80-90% | Slack, Zoom, DataDog, Snowflake historical range |
| Standard SaaS | 70-80% | The typical band for a healthy multi-tenant SaaS at Series-B and beyond |
| Investor-scepticism zone | 60-70% | Requires an explanation — heavy infrastructure, thin third-party stack, unfavourable customer mix |
| Distressed / structurally challenged | Below 60% | Business model likely not a pure SaaS; often marketplace, hardware, or heavily services-driven |

The 70% threshold is not a hard rule but a common heuristic used by growth investors and board members to screen the "is this really SaaS?" question. Below 70%, the diligence conversation shifts from *"how large is the market"* to *"why is the gross margin structurally low, and what does that mean for the terminal multiple."* AI-native startups where LLM inference dominates cost-of-revenue are a current active discussion point; a company at 55% gross margin whose largest COGS line is Anthropic or OpenAI API bills is not necessarily broken, but the CFO must have a credible story for how the margin evolves as inference costs decline or as the product moves upmarket.

The other decomposition metric investors watch: **subscription gross margin** (excluding professional services) reported separately from **blended gross margin** (including professional services). Companies with material services revenue report both; investors value the subscription gross margin because it is the recurring-revenue segment that supports a multiple.

## Marketplaces — the take-rate framing and the 20% floor

Marketplaces are not SaaS and should not be gross-margin-benchmarked as SaaS. The equivalent question for a marketplace is *how much of GMV does the platform capture as revenue* — the take-rate — and *what fraction of the take-rate is gross profit* after payment processing, seller support, trust-and-safety operations, and any subsidy the marketplace pays to acquire liquidity.

Take-rate bands from published marketplace benchmarks:

| Segment | Typical net take-rate | Examples cited in industry commentary |
|---|---|---|
| High-take-rate marketplaces | 20-40% | App stores, verticalised SaaS-plus-marketplace hybrids, some talent marketplaces |
| Standard marketplaces | 10-20% | eBay historical, Etsy, Airbnb (booking fee + host fee combined) |
| Investor-scepticism zone | Below 10-15% | Requires an explanation — scale advantages, network-effect moat, ancillary monetisation |

The 20% take-rate is a commonly cited threshold — cited in the a16z marketplace playbook and in Bill Gurley's [essays on marketplace economics](https://abovethecrowd.com/) — below which investors ask whether the platform captures enough of the value it creates to sustain the fixed-cost base it needs to operate. Marketplaces below 15% take-rate typically justify the take-rate with either extraordinary network effects (winner-take-all dynamics) or ancillary monetisation (advertising, financial services) that raises the effective take-rate.

Once take-rate is set, the marketplace's gross margin is take-rate revenue minus the direct cost of servicing the transaction (payment processing, seller-side support, trust-and-safety operations). Well-run marketplaces report 60-80% gross margin on their take-rate revenue — that is, of every $100 in take-rate revenue, $60-80 flows through to gross profit.

The failure mode: a marketplace founder reports GMV as revenue on the deck (a $500M marketplace with a 15% take-rate reports "$500M in transactions" as though it were $500M of revenue). Under ASC 606's principal-vs.-agent framework (covered in [`mod-101` chapter 5](../mod-101-startup-accounting-foundations/05-gross-vs-net-and-contra-revenue.md)) a marketplace is almost always the agent and must report net revenue (the take-rate). The gross-reporting error is caught in the first diligence conversation and the CFO who let it onto the deck loses the round.

## The gross-margin bridge — what a board pack shows

A gross-margin bridge is a walk from revenue to gross profit that names every material COGS bucket and shows the trend. The canonical presentation in a board pack:

```
Q3 revenue                                                    $4.2M
  Less: Hosting and infrastructure               (7% of rev)  ($0.30M)
  Less: Third-party COGS (inference, payments)   (4% of rev)  ($0.17M)
  Less: Customer support (fully loaded)          (6% of rev)  ($0.25M)
  Less: CS delivery / implementation             (5% of rev)  ($0.21M)
  Less: Application hosting (single-tenant)      (1% of rev)  ($0.04M)
= Total cost of revenue                          (23% of rev) ($0.97M)
= Gross profit                                   (77% of rev)  $3.23M
```

Paired with the same table for the prior quarter and the year-ago quarter, and a one-paragraph narrative on the trend — *"Gross margin improved 200 bps YoY driven by hosting-efficiency projects and mix shift toward multi-tenant customers; third-party COGS grew as a percentage of revenue driven by LLM-inference workloads in the new AI-agents product line and is projected to decline as we finish the internal-inference-cache buildout in Q1"* — this is the CFO-authored gross-margin story that a board and an investor absorb in one glance.

The trend is what matters. A 200-bps improvement in gross margin at a company doing $50M ARR is $1M of gross profit annually — real money that the CFO is expected to be able to explain. A 200-bps decline requires either a good reason (mix shift toward a strategic segment with structurally lower margin but higher LTV) or a corrective action plan.

## Cohort gross margin and its relationship to blended gross margin

For unit-economics purposes, the gross margin used in the cohort-LTV computation (chapter 2) and the cohort table (chapter 4) should be a *cohort-specific* number, not the blended company gross margin. Cohorts of different sizes, sourced through different channels, and with different customer segments will have different cost-to-serve profiles:

- **Enterprise cohorts** often have higher CSM allocations and higher support ticket volumes per dollar of ARR, giving cohort gross margins 5-15 points below the blended number.
- **PLG cohorts** on lower-tier plans have very low per-customer support and CSM cost but higher share of the free-tier infrastructure cost pool, which can push cohort gross margin down or up depending on the free-to-paid conversion economics.
- **Cohorts on legacy pricing** (customers who signed contracts before the last price increase) have lower ARPU with the same cost-to-serve, dragging cohort GM down until they roll off or upgrade.

The practical convention: compute cohort GM as the cohort's revenue in the period minus (that cohort's directly-allocable cost to serve + the cohort's proportional share of the shared cost pool). The allocation key for the shared pool is usually the cohort's share of company revenue for the period.

For the LTV calculation in chapter 2 to work, cohort GM must be re-computed for each cohort each month — a mature cohort's GM is typically higher than a young cohort's (the shared allocation is the same, but expansion revenue lifts the numerator). A single "80% gross margin" plugged into the LTV formula for every cohort every month is the sort of shortcut a diligence firm catches quickly.

## The three-way gross-margin reconciliation

A CFO-authored unit-economics pack should contain three gross-margin views that reconcile to each other:

1. **P&L gross margin** — the number that appears on the accrual-basis income statement, decomposed into the five canonical buckets.
2. **Product-line gross margin** — subscription vs. professional services (and any other product lines) reported separately, both reconciling to the P&L blended number.
3. **Cohort gross margin** — the per-cohort per-month number that feeds the cohort table and the LTV computation, with a walk from the P&L number.

If any two of the three don't reconcile, the model has a bug — usually an allocation-key drift where cohort-level allocations don't sum to the P&L pool. The reconciliation is the third piece a lead investor's diligence firm rebuilds; producing it up front saves a diligence cycle.

## Common gross-margin mistakes

A pre-diligence checklist:

- **CSM salaries in G&A instead of COGS** — inflates gross margin 5-15 points; typically caught within the first hour of the diligence call.
- **Free-tier hosting in R&D instead of COGS** — for PLG companies, the free-tier infrastructure is a customer-acquisition cost and belongs somewhere between COGS and S&M; the specific classification is debatable but leaving it in R&D and calling the paid gross margin "clean" is a common founder error.
- **Payment processing as contra-revenue** — reduces revenue instead of reducing gross profit, inflating gross margin. For most SaaS companies payment processing (Stripe fees) is COGS; for marketplaces it is a direct cost of the transaction and is contra-revenue only under specific ASC 606 principal-agent facts. Get the classification right.
- **Attribution of infrastructure cost to R&D environments** — development, staging, and CI/CD infrastructure is R&D. Production infrastructure serving customer traffic is COGS. Companies with weak tagging often lump both into COGS, understating margin; more commonly, they lump both into R&D, overstating margin.
- **Third-party inference costs booked as R&D "AI model training"** — inference cost per customer request is COGS; model *training* on internal data may be a fair R&D classification. This distinction is a live discussion in the AI-native segment and warrants explicit disclosure.
- **Professional services bundled into subscription revenue** — reports the blended gross margin only, hiding the fact that the subscription segment is meaningfully higher-margin. Best practice: report both, and let the investor pick which one they price against.
- **Missing SBC in COGS-eligible salaries** — the fully-loaded compensation for support and CS staff includes stock-based compensation, employer taxes, and benefits. Salary-only loading understates COGS by 25-40%.

## Summary

- GAAP is largely silent on COGS classification; the SaaS-metrics canon (Skok / a16z / Bessemer / Meritech) and public-company 10-K disclosure practice define the norm.
- The five canonical COGS buckets for SaaS: hosting, third-party COGS, customer support, CS delivery/professional services, and application hosting for customer environments. R&D and G&A stay out.
- SaaS gross-margin bands: 70-80% is standard, 80%+ is best-in-class, below 70% triggers investor scepticism and requires explanation.
- Marketplaces are benchmarked against take-rate (below 20% is the scepticism zone), and then against the gross margin on the take-rate. GMV is not revenue; ASC 606 principal-agent analysis governs.
- The gross-margin bridge — revenue → cost buckets → gross profit — is the board-pack presentation. Paired with prior-period and year-ago comparisons and a narrative on the trend.
- Cohort gross margin differs from blended gross margin and must be re-computed per cohort for the LTV calculation to be defensible.
- The three-way reconciliation (P&L GM, product-line GM, cohort GM) is a diligence-artefact that saves a diligence cycle when produced up front.

Chapter 4 builds the cohort table that consumes this chapter's cohort-GM number. Chapter 5 turns to NRR and GRR as the second lever that (alongside CAC and GM) determines whether the LTV:CAC math works.
