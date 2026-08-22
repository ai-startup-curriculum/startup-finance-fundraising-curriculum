# Sizing the Round — Against the Milestone Bar, Not Backed Into From a Dilution Target

## Why this matters

The round-sizing question — "how much are we raising?" — has one right answer and many wrong ones. The right answer starts with the next round's KPI bar (the traction a Series-A partner meeting will require, or the ARR-and-efficiency profile a Series-B lead will underwrite), works out what the operating plan needs to fund to clear that bar with a milestone buffer, and prices the round at the amount that funds that plan for 18-24 months. The wrong answers start with a target dilution ("we want to sell 20%"), a target valuation ("we want a $50M pre"), or a round-size norm ("everyone raises $5M at seed"), and back-solve into an operating plan that fits.

The wrong answers are the wrong answers because a fundraising round is not a valuation transaction — it is an option on the next round. The current round exists so the company can reach a next-round bar the current traction cannot yet defend. The right size is the amount that produces the highest probability of clearing that bar in 18-24 months. Any other framing over- or under-raises against the actual optimisation, and both errors are expensive.

This chapter walks the mechanics: what the next-round bar looks like at each stage, how to compute the operating plan against the bar, how to add the milestone buffer, and why over-raising is more expensive to founders than under-raising even though it feels like the safer error.

## The three canonical wrong framings

Before the right framing, name the three canonical wrong ones. Each is common, each is intuitive, and each ends in a compromised round.

**Wrong framing 1 — start from a target dilution.** "We want to sell 20%, and if the pre-money is $20M then that's a $5M round." This anchors the raise to a *distribution* outcome (how much of the company is sold) rather than a *runway* outcome (how long the company operates before the next raise). It systematically produces rounds that are too small when the market is expensive (a 20% dilution target at a $50M pre gives you $12.5M — great — but if the market is $10M pre for your stage you only raise $2.5M and you're back on the road in six months) and too large when the market is cheap (a 20% dilution target at a $100M pre for a Series-B gives you $25M whether or not your operating plan wants to burn it). It also actively encourages the founder to accept a term sheet with a higher pre-money and *more capital* than the operating plan needs, which is the specific failure mode below.

**Wrong framing 2 — start from a target valuation.** "We want a $50M pre." This anchors the raise to a *headline* outcome (the announced valuation number) rather than an operating outcome. It is what founders do when they treat the round as a signal to the outside world — press release, LinkedIn post, industry validation — rather than as a specific amount of capital to run a specific operating plan against. It is often coupled with the target dilution framing above ("we want a $50M pre and to sell 20%") and produces the same failure mode.

**Wrong framing 3 — start from a round-size norm.** "Seed rounds are $5M." "Series-A rounds are $15M." This is a founder who has read one recent Carta or PitchBook report and internalised the median as the target. It ignores the specific operating plan the specific company needs to fund. Two companies at the same stage — a capital-efficient B2B SaaS company at $60K MRR with a 12-month CAC payback, and a hardware company at pre-revenue with a $10M NRE cost before first shipment — have entirely different capital needs. Median round sizes are a market-conditions data point (mod-106 chapters 6-7), not a sizing input.

Each wrong framing produces a round that is not sized against the operating question. The right framing is.

## The right framing — the milestone-bar plan

The right framing has four steps:

1. **Define the next round's KPI bar.** What does the target Series-A / Series-B partner meeting need to see? Name the specific KPIs, the specific thresholds, and the specific market-conditions context.
2. **Build the operating plan that clears the bar.** What does the company need to do — hire, ship, sell, retain — to move from the current KPIs to the next-round bar with room to spare?
3. **Cost the operating plan.** Under a driver-based three-statement model (mod-103), what is the total cash burn required to run the plan for 18-24 months?
4. **Add the milestone buffer.** Add 3-6 months of runway on top of the plan's monthly burn so that a slip in the operating plan does not put the company on the road out of runway.

The round size is the output of the four steps, not an input to them. If the four steps produce a $6.5M number, the round is $6.5M. It is not $5M "because that's the norm" or $10M "because the market will pay."

## Step 1 — define the next round's KPI bar

The next round's KPI bar is what the target Series-A (or Series-B) partner meeting requires to underwrite the round. It is stage- and sector-specific. It is also market-conditions-sensitive: a bar that clears a Series-A in a hot 2021-style market does not clear one in a compressed 2023-style market.

The right way to define the bar is to talk to Series-A partners in the target investor pool and ask directly. What are you underwriting for a Series-A in [sector]? What ARR do you want to see? What growth rate? What NRR? What CAC payback? What team? What product proof? Most Series-A partners will answer this question honestly for a seed founder they might invest in later. The specific-partner answers are more valuable than any general benchmark, because they are the specific bar that the specific partner will actually apply.

The general benchmarks — as of a specific vintage that a CFO should validate against the current-quarter data — are approximately:

- **Series-A benchmarks for B2B SaaS** (as historically discussed by Point Nine, OpenView, SaaStr, and Bessemer):
  - **ARR:** commonly discussed in the $1M-$2M range as a Series-A "table stakes" bar for growth-stage-selecting investors, though specific benchmarks vary by sector and year — verify with the target investor pool. <!-- needs-research: pull the current-year Series-A ARR bar from Point Nine's Series-A Napkin / OpenView SaaS Benchmarks / Bessemer's State of the Cloud rather than repeating a stale round number. -->
  - **Growth rate:** typically stated as "growing 2-3× year-over-year at the ARR band above." <!-- needs-research: confirm the current-vintage growth-rate expectation from a Point Nine / OpenView / Bessemer publication. -->
  - **NRR:** commonly discussed at 100%+ as a floor and 120%+ as a strong signal at Series-A.
  - **CAC payback:** commonly discussed in the 12-24 month range as reasonable for early-Series-A B2B SaaS.

- **Series-B benchmarks for B2B SaaS** (same source stack):
  - **ARR:** commonly discussed in the $5M-$10M range or higher at Series-B in enterprise SaaS. <!-- needs-research: confirm current-vintage Series-B ARR benchmark. -->
  - **Growth rate:** commonly discussed at 2× year-over-year at the ARR band.
  - **NRR:** 120%+ as the strong-signal band at Series-B.
  - **Efficiency:** the Rule of 40 lens starts to be underwriting-relevant (mod-106 chapter 4).
  - **Sales-motion proof:** a repeatable sales motion with a defensible CAC-payback profile — proof the go-to-market is a machine rather than a founder-selling pattern.

For **consumer** and **marketplace** businesses, the bars are structurally different — engagement metrics, cohort retention curves, take-rate proofs, GMV growth — and the sector-specific benchmarks should be pulled from the sector-specific investor content (Sequoia's consumer-thesis writing, USV's blog, a16z's consumer content, Meritech's marketplace comps).

**The specific work.** For any target company at any stage, write down the specific KPI targets the next round needs to clear. Not a general "1-2M ARR at Series-A" but a specific "$1.8M ARR at 3.5% MoM growth, 115% NRR, 18-month CAC payback, on a $150K ACP in the mid-market SaaS category." That specific bar is what the operating plan must fund.

## Step 2 — build the operating plan against the bar

Given the current KPIs and the next-round bar, what does the operating plan look like? This is a mod-103 exercise — a driver-based three-statement model — and the answer flows out of the drivers: hiring plan, product roadmap, GTM plan, retention plan.

Concretely, for a company at $250K ARR raising a seed to clear a $1.5M ARR Series-A bar in ~18 months:

- **ARR trajectory.** Under a 12% MoM growth path, $250K compounds to $1.5M ARR in ~15 months. Under 15% MoM, ~12 months. The plan lands the traction in the 12-18 month band with buffer.
- **Sales headcount to support the trajectory.** If the sales-motion proof requires two AEs closing $500K-$700K each at year-end run rate, the plan needs those two AEs signed and ramping by month 6-8.
- **Engineering headcount to support the product roadmap.** If the product needs to close specific enterprise features (SSO, SOC2, audit logs) before the Series-A traction ceiling, the roadmap needs those in the first 9-12 months.
- **CAC / marketing to support the pipeline.** If two AEs need to close $1M ARR in year 2 at a 12-month CAC payback, the marketing spend supporting the top of funnel needs to be sized against that math (mod-102).

The operating plan produces a monthly burn profile: month 1 through month 18-24, expected cash out per month, expected ARR in per month. That burn profile is the input to step 3.

## Step 3 — cost the plan

Cost the operating plan under the driver-based model (mod-103). The plan produces:

- **Total 18-month burn** — sum of expected cash out per month less expected cash in per month over the 18 months.
- **Total 24-month burn** — the same over 24 months (some plans are longer, some shorter — the target is that the plan reaches the next-round bar with 3-6 months of runway to spare on top).

Two anchor numbers a CFO should always compute alongside the burn:

- **Net burn** — cash out less cash in.
- **Gross burn** — cash out, ignoring revenue. Useful for the Series-A / B partner meeting where the partner underwrites against "how expensive is this to run" independently of the current revenue.

The burn profile also has a shape. Seed companies typically ramp: the first 3-6 months of a seed are lower burn (still hiring), the middle 6-12 months are peak burn (fully staffed against the plan), the last 3-6 months tail off (either the plan is de-risked and revenue is offsetting, or the company is prepping the next raise). Sizing needs to accommodate the peak, not just the average.

## Step 4 — add the milestone buffer

Add 3-6 months of runway on top of the plan's cash need. This is the milestone buffer. Its job is to protect the company against three specific failure modes:

- **Plan slip.** The operating plan is a best-effort forecast, not a certainty. If the hiring plan slips 2 months, the product roadmap slips 2 months, or the GTM ramp slips 2 months (each of which is normal), the milestone-bar-clearance date slips by the same amount. Without a buffer the company runs out of cash before it clears the bar.
- **Market-conditions slip.** The Series-A window that was open when the seed closed can be materially compressed 18 months later. A company that hits the bar but on a compressed timeline is one that needs cash on the shelf while it runs the process. Without a buffer the company negotiates the Series-A under duress.
- **Timing between "I'm cleared" and "term sheet in hand."** Even the best-run Series-A process from a well-cleared bar takes 8-12 weeks from start to signed term sheet, and another 4-8 weeks to closing. Without a buffer that fundraising window is unfunded.

The 3-6 month band is the practitioner default (Feld & Mendelson *Venture Deals*; Suster's *Both Sides of the Table*; Wilson's *AVC*). Companies with more binary risk — hard-tech, deep-tech, regulatory-gated markets — sometimes size to a longer buffer (6-9 months). Companies with strong repeat-founder credibility and a low-execution-risk plan sometimes size shorter (3 months). The default target is **20-24 months of total runway** — 18 months for the plan, 3-6 months for the buffer.

## Worked sizing example — seed round

**Company.** Pre-seed SaaS company. Current ARR $250K, growing 12% MoM. Founding team of 3 (2 engineers, 1 sales-founder), one design-partner customer at $50K ACV, four customers on annual contracts averaging $50K ACV.

**Next-round bar (validated with target Series-A partners).** $1.5M ARR at 8%+ MoM sustained growth, 100%+ NRR, a repeatable outbound motion with 2 AEs producing predictable pipeline, and enterprise features shipped (SSO, SOC2 in-progress, standard security review).

**Operating plan (18 months).**

| Category | Detail | Monthly cost | 18-month total |
|---|---|---|---|
| Engineering | 3 → 6 hires ramped over months 1-12; average fully-loaded $180K | ~$90K/mo peak | $1.2M |
| GTM (AEs + SDRs) | 1 → 3 hires ramped over months 3-10; average fully-loaded $200K on-target | ~$50K/mo peak | $0.7M |
| Founders + design | Founders on modest cash salary; 1 designer hire month 6 | ~$50K/mo peak | $0.8M |
| Marketing | Content + paid pilot, growing to $30K/mo by month 12 | ~$25K/mo peak | $0.3M |
| Infrastructure | Hosting, tooling, SOC2 audit, legal | ~$15K/mo peak | $0.2M |
| G&A / rent / benefits | Small, WeWork or similar | ~$15K/mo peak | $0.2M |
| **Total gross burn** | | **~$245K/mo peak** | **~$3.4M** |
| **Less: revenue offset** | Cumulative revenue expected across the 18 months as ARR ramps from $250K to $1.5M | | **~$1.0M** |
| **Total net burn** | | | **~$2.4M** |

**Milestone buffer.** 6 months at the peak burn ($245K/mo × 6 - $180K/mo × 6 revenue offset at the higher run rate) ≈ **$400K**.

**Total round size** = **$2.8M**.

Note what the sizing does *not* do. It does not:

- Anchor to a target dilution. If the pre-money the market supports is $12M, the round is 19% dilution. If it is $8M, it is 26% dilution. The sizing is independent of the pre-money — the sizing is the plan.
- Anchor to a norm. The "typical seed" number of $3M-$5M is irrelevant. This specific plan needs $2.8M. Padding to $4M "because that's the norm" would over-raise the plan by ~40%, which is exactly the failure mode below.
- Anchor to a headline. The raise is not a marketing number; it is an operating number.

## Worked sizing example — Series-A round

**Company.** Series-A B2B SaaS. Current ARR $2.0M growing at 8% MoM (~2.5x YoY), NRR 115%, GRR 90%, gross margin 78%, current headcount 22.

**Next-round bar (Series-B).** $8M-$10M ARR at 3-4% MoM sustained growth, 120%+ NRR, Rule of 40 in the 30-40% band, a defensible three-tier customer segmentation with a repeatable enterprise motion, at least one enterprise-anchor deal above $250K ACV as proof.

**Operating plan (24 months).**

| Category | Detail | Monthly cost | 24-month total |
|---|---|---|---|
| Engineering + product | 8 → 16 over months 1-18; average FL $220K | ~$275K/mo peak | $6.5M |
| GTM (AEs, SDRs, CS, SE, VP Sales) | 6 → 20 over months 1-18; average FL $230K | ~$375K/mo peak | $9.0M |
| G&A + finance / people | Additional finance / people / legal hires | ~$100K/mo peak | $2.2M |
| Marketing | Growing to $150K/mo by month 18 | ~$120K/mo peak | $2.4M |
| Infrastructure | Hosting scales with ARR at ~15% of revenue | ~$60K/mo peak | $1.2M |
| **Total gross burn** | | **~$930K/mo peak** | **~$21.3M** |
| **Less: revenue offset** | Cumulative revenue across 24 months as ARR ramps $2M → $8M-$10M | | **~$11.0M** |
| **Total net burn** | | | **~$10.3M** |

**Milestone buffer.** 6 months at peak net burn ~ **$2.5M**.

**Total round size** = **~$12.8M**, rounded to **$13M**.

## Why an over-raised round costs the founders more

The intuitive founder view is that over-raising is the safer error: extra cash on the balance sheet is optionality. In practice, the extra cash is expensive in three concrete ways, each of which shows up as a founder-cost at the next round.

**Cost 1 — immediate dilution against the plan.** A $3M plan that raises $5M sells an extra $2M of the company at today's valuation to fund cash the company does not need to spend to hit the milestone bar. At a $12M pre-money that extra $2M is ~14% additional dilution today — dilution paid for optionality the plan is not going to spend.

**Cost 2 — valuation-defence risk at the next round.** The next round is priced against the traction. The traction is set by the milestone-bar plan. Over-raising does not accelerate the traction — the plan already assumed the highest reasonable execution rate. What over-raising does is create a next-round expectation the current-round pre-money implicitly sets. An over-raised seed at a stretched pre-money creates a Series-A valuation-defence problem: the Series-A has to price at 2-3× the seed pre for the raise to feel healthy, and if the traction has cleared only the minimum bar rather than crushed it, the Series-A pre-money is under pressure. The over-raise pushes the founder into either a smaller next-round step-up (which reads as weak) or a compressed valuation (which triggers anti-dilution ratchet consequences if there are any). See mod-108 for the anti-dilution mechanics that make this concrete.

**Cost 3 — burn-rate pattern-match failure.** Series-A and Series-B partners underwrite against a "how efficient is this team?" pattern — the burn multiple, the CAC payback, the Rule of 40 (mod-102 and mod-106). A seed company sitting on $2M of extra cash tends to spend it (Parkinson's Law is a real thing in early-stage operating). Extra hires, extra marketing spend, extra tooling. What that produces at the next round is a burn multiple that reads too high for the ARR band. The over-raise has bought a slower path to the milestone bar at a lower efficiency, which is worse than the smaller round would have been.

None of these costs shows up in the current round. All of them show up 12-24 months later, at the next round's partner meeting, when the traction and efficiency are being underwritten. The founder pays them at the higher valuation the next round wants to be priced at, and the payment shows up as either a smaller step-up or an outright down round.

## Why an under-raised round also costs founders — but usually less

Under-raising has its own costs. The plan runs short. The company hits its cash-out date before the milestone bar is cleared. The founder is on the road under duress, and duress-raises price worse — sometimes materially worse.

Two mitigating factors, however:

- **The bridge market exists.** Extension SAFEs, insider-led bridges, revenue-based financing, venture debt — the market for buying more runway when a milestone bar is close is real (mod-109). It is expensive relative to a well-sized round, but it is available.
- **The under-raise diagnosis is easy.** The month a runway forecast slips is the month the CFO sees it. There is a lead time (typically 6-9 months) to react — extend runway with a bridge, cut burn, close the round early on the traction available. The over-raise diagnosis, by contrast, only shows up 12-24 months later when the next round is being priced.

So while both errors are real, the over-raise is systematically underweighted by founders and the under-raise is systematically overweighted. The right sizing is against the milestone-bar plan with a buffer — not a hedge in either direction.

## What "against the milestone bar" does *not* mean

The milestone-bar framing has three failure modes that a careful CFO avoids.

**Failure mode 1 — the milestone bar is set from founder ambition rather than investor reality.** "We're going to be at $5M ARR at Series-A, not $1.5M." This is the founder's plan, not the market's plan. The plan can be aspirational, but the round should be sized against the market bar the plan is being underwritten to. If the founder wants to overshoot, the overshoot funds itself — the extra ARR is extra revenue, which offsets extra burn.

**Failure mode 2 — the milestone bar is set from a stale investor benchmark.** The Series-A ARR bar that applied in 2021 (which was around $500K-$1M in some sectors) is materially different from what applied in 2023-2024 (higher and less flexible in many sectors). The Series-A bar in 2026-2027 will be different again. The bar has to be sourced from current-quarter investor conversations and current-quarter market data, not from a 2020 SaaStr post.

**Failure mode 3 — the milestone bar is a single point rather than a distribution.** Series-A partners do not underwrite against a single number; they underwrite against a *profile*. A company at $1.2M ARR with 130% NRR and a Rule of 40 in the 60% band is on-bar even though its ARR is below the median expectation. A company at $2M ARR with 90% NRR and 30% efficient (i.e. burning >$1 for each dollar of ARR growth) is below-bar even though its ARR is above the median. The plan must be shaped to the profile, not just the number.

## Common founder traps

- **Backing into a round size from a target dilution.** "We want 20% dilution" is a compensation question, not a sizing question. Size the plan first, then negotiate for the pre-money that produces the acceptable dilution.
- **Backing into a round size from a target valuation.** "We want a $50M pre" is a marketing question, not a sizing question. See above.
- **Sizing to the market median.** "Seed rounds are $5M" is not evidence about this specific plan's cash need.
- **Skipping the milestone-bar validation with target Series-A partners.** The bar the CFO uses is one they invented, not one that will actually underwrite the next round.
- **Confusing 18-24 months of runway with 18-24 months of *plan*.** The plan runs 18-24 months. The runway includes the buffer. Sizing to 18 months of plan without a buffer is sizing to 18 months of runway with no room for slip.
- **Over-raising because the market will pay.** A round the market will pay too generously is a round the founder should size against the plan, not against the offered capital. Taking the extra capital is a decision — usually the wrong one — that should be made explicitly, not by default.
- **Failing to update the plan when the market moves.** A plan sized to a 2021 Series-A bar with a 2024 Series-A market is a plan that needs re-sizing. The re-size happens quarterly against the current market, not once at round-close.

## What good looks like

A well-sized round has:

- A specific validated next-round bar (KPIs, thresholds, current-market context) sourced from at least three target-lead partner conversations plus current-quarter benchmark data.
- A driver-based three-statement operating plan (mod-103) that shows the KPI trajectory from today to the next-round bar over 18-24 months.
- A monthly burn profile derived from the plan, with peak burn identified.
- A milestone buffer of 3-6 months on top of the plan's cash need.
- A total round size that is the output of the four steps, not an input.
- A pre-money target derived from the valuation frameworks in mod-106 (not from a target-dilution back-solve).
- A memo to the founder / board explaining the sizing arithmetic, the specific milestone bar, and the specific reasons the round is not larger or smaller.

## Summary

- The right way to size a fundraising round is against the next round's KPI bar with an 18-24 month operating plan and a 3-6 month milestone buffer, not by backing into a target dilution or target valuation.
- The four-step sizing: define the next-round bar (KPIs, thresholds, market context validated with target investors); build the operating plan that clears the bar; cost the plan under a driver-based three-statement model; add the milestone buffer.
- Over-raising costs founders more than it feels like it does — immediate dilution against a plan the extra capital does not fund, valuation-defence risk at the next round from a stretched pre-money, and burn-rate pattern-match failure from Parkinson's Law spending.
- Under-raising is also expensive but is easier to diagnose and remediate (bridges, cost cuts, early close), so is systematically less risky than over-raising even though it feels more risky.
- The milestone bar itself has to be sourced from current-quarter target-investor conversations and current-quarter benchmarks, not from stale industry norms.
- The round size is the *output* of the sizing exercise, not an input.

Chapter 2 turns to the investor-target list — given the round size, which specific investors have the fund structure, thesis, and cheque-size band that make them capable of leading the round.
