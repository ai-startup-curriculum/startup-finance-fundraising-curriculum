# Fully-Loaded CAC per Channel per Cohort

## Why this matters

Almost every founder-authored deck reports CAC as *total sales and marketing spend for the year divided by new customers acquired for the year.* That number is a **blended, annualised, mid-cohort average** of a distribution that a Series-A investor treats as three or four different distributions bolted together. In a mixed-motion startup — some paid search, some outbound SDR, some product-led signup, some partner referrals — the blended number hides the two facts an investor actually needs: which channels have healthy economics, and which are consuming cash to buy customers whose gross-profit stream will never pay the acquisition back.

The failure mode is concrete. A startup at $3M ARR reports blended CAC of $8K and blended LTV of $32K — a 4:1 ratio that reads "efficient." The CFO who breaks the number apart discovers: inbound signups have $500 CAC and $30K LTV (excellent), paid search has $6K CAC and $18K LTV (marginal), and outbound has $22K CAC and $35K LTV (barely paying back, and only if the retention curve holds). The blend hid a segment burning $9K of gross profit per new customer, and the CFO who cannot show the un-blended view will lose the round or take a lower valuation because the diligence firm will do the decomposition and hand it back with different conclusions than the deck.

This chapter installs the CFO-grade definition of CAC — **fully loaded**, **per acquisition channel**, and **per monthly cohort** — and names the failure modes of anything cheaper.

## The three degrees of freedom in the CAC number

A CAC number is under-specified until you have committed to three choices.

**1. What goes in the numerator ("what is spend").** The narrow founder-instinct answer is "the ad bill." The correct answer is *every dollar of sales and marketing expense in the period, plus any cost-to-serve line that produced the signup.* Loading rules are covered in the next section, but the summary: paid-media spend + all S&M payroll + commissions + agency fees + content and creative production + tools stack + attributable share of events + attributable share of partner or referral incentives + the customer-success onboarding hours that were the condition of the customer closing.

**2. What goes in the denominator ("what is a customer").** New logos in the period is the standard denominator for a SaaS motion. But watch for: paid signups vs. free-tier signups (PLG motions), self-serve vs. sales-assisted (which typically have very different CAC), and multi-product cross-sells (are you counting a customer once when they buy the first product or once per product?). Every choice needs to be documented in the CAC methodology memo — you will be asked in diligence.

**3. What is the period.** Annual is the default reporting cadence. Monthly is the correct modelling cadence. Quarterly is what a board deck usually shows. The trap: quarterly S&M spend divided by quarterly new customers hides an important lag — the customers who closed this quarter were generated in part by spend in the previous quarter (paid search closes fast; outbound and content close slowly). The cohort framing in the next section is the fix.

Any CAC number that has not answered all three questions is untrustworthy. The blended number implicitly answers "everything in S&M / all new logos / annual" but rolls three-plus channels with different cycle times into a single ratio.

## "Fully loaded" — what actually goes in

The fully-loaded CAC treats S&M as an operating function whose entire cost base exists to acquire customers. Every line that would disappear if the S&M organisation were removed belongs in the numerator.

A defensible S&M loading has, at minimum, these buckets:

- **Paid media** — search, social, display, retargeting, sponsored newsletters, podcast reads, ABM-targeted ads.
- **S&M payroll** — fully-loaded compensation (salary + bonus + benefits + employer taxes + stock-based compensation) for every person in sales, marketing, sales development, sales engineering, revenue operations, and the marketing side of demand generation. For CFOs building the model, use the fully-loaded employee cost from the hiring plan, not the salary line — the burdened number is 25-40% higher than salary alone depending on jurisdiction and benefits load.
- **Sales commissions and SPIFs** — commissions on new bookings closed in the period, plus any sales-performance incentive payments. Under [ASC 606's companion standard ASC 340-40](https://asc.fasb.org/), incremental costs of obtaining a contract (typically sales commissions) are capitalised and amortised over the expected customer life — the P&L expense in the period is the amortisation, but the CAC calculation typically uses the *incremental cash cost of acquisition* in the period, which is a different number. Pick a convention (either works; the SaaS-metrics canon uses the cash view) and document it.
- **Agency and contractor fees** — outsourced content, creative, PR, SDR-as-a-service, media buying, SEO retainers.
- **Content and creative production** — video production, whitepaper and blog production (in-house or contracted), design assets, landing-page development.
- **Marketing tools stack** — CRM (Salesforce, HubSpot), marketing automation (Marketo, Pardot, Braze), attribution (Bizible, Attribution, Full Circle), enrichment (ZoomInfo, Clearbit, 6sense), sales engagement (Outreach, Salesloft, Apollo).
- **Events, sponsorships, and field marketing** — booth spend, event travel, sponsorship fees, dinners, executive briefings.
- **Partner and referral incentives** — cash referral bonuses, revenue-share on channel deals for the acquisition period (ongoing rev-share is typically COGS, not CAC — see chapter 3).
- **Attributable customer-success onboarding effort** — the hours spent in the sales cycle by CSMs to close the deal (product demos, technical onboarding required to convert a trial, executive briefings for enterprise closes). For PLG motions with no dedicated sales team this can be trivial; for enterprise motions this can be 15-25% of a CSM's time and belongs in CAC.

The line that is *always* debated: which R&D or product spend "belongs" in CAC. The default answer is *none*. Product spend builds the product that the customer buys; it is not an acquisition cost. The exception is the small subset of engineering effort spent on demand-generation infrastructure — the growth-engineering team that owns onboarding, in-product upsell hooks, and free-tier optimisation is often loaded into S&M rather than R&D at Series-B and later. Whatever convention you pick, document it and be consistent across periods; the ratio movement over time is what diligence looks at, and a definition change mid-series is a red flag.

## Per channel — the un-blend

The blended CAC is a weighted average across channels with structurally different economics. The un-blend requires attributing both sides of the ratio to a channel dimension.

**Numerator attribution.** Every dollar of S&M spend is tagged to a channel. Paid media is easy (the ad bill is inherently per channel). S&M payroll and tools need an allocation key — hours by function, or a simpler percent-of-team split, or a percent-of-attributable-revenue split — but the allocation *must exist*. A tool called "marketing automation" that supports every channel gets a proportional split; a CSM whose entire day is closing outbound-sourced deals gets 100% loaded to outbound.

**Denominator attribution.** Every new customer is tagged to the channel that produced them. This is the operationally hard part — attribution across a multi-touch buyer journey is contested, and reasonable people prefer different models (first-touch, last-touch, position-weighted, data-driven). For unit-economics purposes, pick one model, apply it consistently, and disclose it in the methodology memo. First-touch attribution is the simplest and most robust for young companies; multi-touch models get more useful as data volumes grow. Time-based attribution windows also matter (a 90-day window catches most B2B software cycles; enterprise sales with 6-month cycles need longer windows).

A minimum channel taxonomy for a mixed-motion B2B startup:

| Channel | Typical loading | Typical cycle time | Notes |
|---|---|---|---|
| Paid search (Google, Bing) | Ad spend + a share of demand-gen ops | Days to weeks | Fastest feedback loop; per-keyword CAC is available |
| Paid social (LinkedIn, Meta, X) | Ad spend + creative production + a share of demand-gen ops | Weeks | LinkedIn CAC for B2B is materially higher than search; document why you pay it |
| Content / organic search | Content production + SEO ops + a share of demand-gen ops | Months to quarters | Cycle time lag is the main modelling challenge |
| Outbound (SDR-sourced) | SDR payroll + sales-engagement tools + list enrichment + AE close time | Weeks to months | Highest per-customer CAC in most B2B motions |
| Inbound sales (marketing-qualified → AE) | Marketing programme costs upstream + AE close time | Weeks | Often the healthiest CAC in the mix |
| Partner / channel | Partner-programme payroll + referral incentives + partner-attributable AE time | Weeks to months | Model the ongoing rev-share as COGS, not CAC |
| Product-led (self-serve conversion) | Growth-eng allocation + free-tier COGS + PLG-specific marketing | Days to weeks | Nearly-zero CAC is a common founder claim; check the growth-eng and free-tier COGS load before believing it |
| Events / field | Event spend + travel + attributable sales time | Months | Cycle time and multi-touch attribution make this the hardest channel to trust |

A defensible per-channel CAC table is a monthly matrix: channels down the side, months across the top, fully-loaded CAC per new customer in each cell. Exercise 01 builds this artefact.

## Per cohort — the temporal fix for spend-lead-to-close lag

Spend in month M does not produce customers only in month M. Paid search converts within days; outbound sequences might take 60-120 days; content investment made in Q1 produces organic traffic in Q3. Naïvely dividing month-M S&M spend by month-M new customers assigns spend to the wrong cohort.

The cohort framing fixes this by attributing every dollar of spend to the *cohort of customers it produced* rather than the calendar month it was booked in. Operationally:

- **For fast-cycle channels** (paid search, most paid social, some inbound), same-month attribution is close enough. Book the spend against the new customers acquired that same month.
- **For medium-cycle channels** (outbound, some inbound, some events), a spend-to-close lag of 60-90 days should be modelled. The spend on outbound in month M produces closed customers 2-3 months later; the CAC for the *acquisition cohort* attributes month-M spend to month M+2 or M+3 customers.
- **For slow-cycle channels** (content, SEO, brand), a rolling-average or amortised-spend approach is more defensible than trying to attribute a single month's spend to a specific customer. The convention is to compute a trailing-12-month average of content spend and divide by trailing-12-month organic-attributable signups.

The critical rule: the cohort-based CAC per channel per month should sum, weighted by new-customer counts, to the total S&M spend across all channels. If it doesn't, you have leakage — either spend that isn't attributed to any channel (a bucket for "shared / brand / unattributable" is fine, but must be shown), or customers that aren't attributed to any channel (a "self-attributed / referral / unknown" bucket, also fine, also must be shown). The reconciliation is a diligence-question deflection: it demonstrates that the CAC methodology is internally consistent.

## The relationship between CAC and payback period

The payback period is the number of months of gross profit from a cohort required to earn back the CAC that acquired it.

Naïvely: `payback (months) = CAC / (ARPU × gross margin per month)`. This is the number that lives on most decks; it is a simplification that assumes constant ARPU, no churn during the payback window, and no expansion.

Correctly, off the cohort table: sum the monthly gross-profit contribution from a cohort month by month; the payback period is the month in which cumulative gross profit crosses CAC. This number is often 20-30% longer than the arithmetic version because it accounts for early-cohort churn eating into the retained base before payback is reached. Investors expect the cohort-derived number at Series-A onward. Chapter 4 builds the table; the payback read is one line off the cumulative gross-profit column.

Rules of thumb from the SaaS-metrics canon:

- **SMB SaaS:** payback under 12 months is healthy; 12-18 months is acceptable; over 18 months requires a very strong retention story.
- **Mid-market SaaS:** 12-18 months is healthy; up to 24 months is acceptable at Series-B and later where LTV is well-established.
- **Enterprise SaaS:** 18-24 months is common; 24-36 months requires strong NRR (see chapter 5) to justify.
- **Consumer / PLG:** 6-12 months is expected; longer typically means the growth loop isn't compounding.

These are directional; specific investor expectations track [OpenView's SaaS Benchmarks](https://openviewpartners.com/) and other published series and shift year to year. Chapter 6 covers the benchmark diagnostic in detail.

## Why blended CAC and blended LTV are lagging and lossy

Two failure modes in the same framing:

**Lagging.** Blended metrics compute a long moving average of a variable that a founder is trying to move. If a startup shifts investment from an $8K-CAC channel to a $2K-CAC channel in month M, the blended CAC for the trailing 12 months will still look like the pre-shift number for another 8-11 months. The founder who fixed the problem cannot see the fix in the metric; the investor who reads the blend will diligence a healthier number than the current-quarter reality (or a worse one). Per-channel per-monthly-cohort CAC updates in the current month; the blend can't.

**Lossy.** Blended metrics arithmetically hide the segment-level economics. Two channels with a 4:1 LTV:CAC and one channel with 1.2:1 LTV:CAC can blend to a healthy 3:1 that a Series-A investor will accept — and then in month 15 the unhealthy channel is 40% of new bookings and the blended number crashes. The un-blended view names the risk before it materialises.

The un-blended view is also a decision-making instrument. When a channel's CAC drifts up (SDR productivity falls, paid-CPC inflates), the CFO can see the drift in real time and either fix the operational cause or cut the spend. The blend is only useful as a historical scoreboard; the un-blend is useful as a management dashboard.

## The three CAC numbers that appear in a deck

For CFO-authored external materials, the convention that survives diligence is to show three CAC numbers side by side:

1. **Blended CAC** — the simple all-in ratio. This is what the founder started with and what the naïve reader will look for. Show it once, source it, and move on.
2. **New-customer CAC by channel** — the un-blended matrix, typically the trailing-12-month per-channel view. This is the number a CRO or Head of Growth reads.
3. **Fully-loaded cohort CAC by channel** — the cohort-based view with all S&M loading, per acquisition channel per acquisition month. This is the number a lead investor's diligence firm will re-build. If yours matches theirs, you get through diligence quickly; if it doesn't, you spend two weeks negotiating methodology.

The methodology memo — one to two pages — accompanies all three: what's in the numerator, what's in the denominator, what attribution model, what channels, what cohort convention, and what edge cases (free-tier, cross-sell, upgrade paths). It is a diligence-question deflector and one of the standard artefacts in the data room (see [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/)).

## Summary

- CAC is under-specified until you have committed to what's in the numerator (all S&M plus attributable cost-to-serve), what's in the denominator (a documented definition of a customer), and the period (monthly cohort for CFO-grade work).
- Fully loaded means every dollar of S&M — paid media, payroll (burdened), commissions, tools, agency, content, events, partner incentives, and attributable CSM onboarding time. R&D typically stays out; growth-engineering may be loaded in at scale.
- Per channel un-blends the arithmetic average into segment-level economics that reveal which channels have healthy LTV:CAC and which are consuming cash.
- Per cohort attributes spend to the customers it produced (not the calendar month it was booked), respecting spend-to-close lag by channel.
- Payback should be read off the cohort table's cumulative gross-profit column, not from `CAC ÷ (ARPU × gross margin)`.
- Blended metrics are lagging (moving averages of a variable the founder is trying to move) and lossy (they hide segment-level problems that will surface later). Un-blended, cohort-based CAC is the CFO-grade artefact.
- The three-number pattern for external materials — blended CAC, per-channel CAC, fully-loaded cohort CAC — paired with a methodology memo, is what survives diligence.

The rest of this module extends this framework: chapter 2 turns the numerator's counterpart (LTV) into a discounted stream, chapters 3-4 build the gross-margin bridge and cohort table that feed both sides, chapter 5 covers NRR / GRR as the compounding capital-efficiency lever, chapter 6 covers the capital-efficiency instruments the whole thing feeds into, and chapter 7 places the module against the GTM-owned view.
