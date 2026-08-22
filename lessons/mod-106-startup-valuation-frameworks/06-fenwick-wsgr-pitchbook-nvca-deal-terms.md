# Quarterly Deal-Terms Data — Fenwick, WSGR, PitchBook-NVCA

## Why this matters

A valuation the CFO produces from the anchor methods (chapter 1), the VC method (chapter 2), and the multiples framework (chapters 3-4) is a bottom-up derivation. What it does not tell the CFO is **what the market is actually pricing this quarter**. Multiples move. Median pre-moneys move. The frequency of up-rounds versus down-rounds moves. The time between rounds moves. Deal size moves. A defensible valuation memo has to name the current-quarter market context because a term sheet negotiated against a stale market read is a term sheet that goes off-market and either doesn't close or closes on terms the founder didn't understand.

Three quarterly reports dominate as market-conditions references for US venture financings:

- **Fenwick & West Silicon Valley Venture Survey** — quarterly, focused on Silicon Valley pricing and terms; long history (2003+) and continuous methodology.
- **Wilson Sonsini Entrepreneurs Report** — quarterly, formerly the *WSGR Entrepreneurs Report* (WSGR being the firm's prior branding — see resources); broader US coverage than Fenwick and includes seed/pre-seed detail.
- **PitchBook-NVCA Venture Monitor** — quarterly, jointly published by PitchBook and the National Venture Capital Association; the most comprehensive dataset covering deal activity, valuations, and exits across US venture stages.

Each report has a different methodology, a different constituent set, and a different set of specific data cuts. A CFO preparing a fundraise typically reads all three and triangulates. This chapter walks what each report contains, how to read them, and how to use them in a valuation memo.

Chapter 7 covers Carta's *State of Private Markets*, which uses Carta's proprietary cap-table data set and produces different (and more granular) cuts than the three reports here.

## The Fenwick & West Silicon Valley Venture Survey

**Publisher.** Fenwick & West LLP, a Silicon Valley law firm with a large venture-financing practice. Public at [fenwick.com](https://www.fenwick.com/) → Insights → *Silicon Valley Venture Survey* (search "Silicon Valley Venture Survey" if the URL structure changes). Also often carried on legal-industry aggregators.

**Coverage.** Financings of Silicon Valley-based companies for which Fenwick has visibility, quarterly, going back to 2002. The sample is not the entire Silicon Valley venture universe but is a substantial and consistent-methodology cut.

**Key data points published per quarter:**

- **Fenwick & West Barometer** — the Fenwick's own quarterly index of valuation change between the current round and each company's most recent prior round. Expressed as up-vs.-flat-vs.-down direction and as the magnitude of change.
- **Percentage of up-rounds, flat rounds, and down-rounds** in the quarter.
- **Average and median percentage price change** from prior round.
- **Valuation trends by round type** (Series-A / B / C / D+). Median pre-money and median post-money by series.
- **Term-sheet feature frequencies** — liquidation preferences (senior vs. pari passu, participating vs. non-participating, capped participation), anti-dilution provisions (broad-based weighted-average vs. narrow-based vs. full ratchet), pay-to-play provisions, redemption rights, dividend rates, cumulative-vs.-non-cumulative dividends.
- **Terminology-consistent time-series data** going back multiple quarters and years, allowing "current quarter vs. trailing 4-quarter average vs. same-quarter-prior-year" reads.

**How to read it.**

- **Direction first.** Are up-rounds increasing or decreasing? Is the average price change positive or negative? A quarter where 25% of financings are down-rounds is a very different market from a quarter where 5% are.
- **Magnitude next.** The average up-round price change tells you how much the market has moved for the winning companies. A quarter where up-rounds averaged +30% is a market where median-quality companies are being repriced upward.
- **Stage specificity.** Series-A pricing and Series-D pricing move differently. Read the specific-series tables, not just the aggregate.
- **Terms as a leading indicator.** When the frequency of aggressive terms (participating preferred, full-ratchet anti-dilution, pay-to-play) increases, the market is shifting toward investor-favourable terms — often a leading indicator of pricing compression. When those frequencies decrease, the market is shifting founder-favourable.

**Illustrative interpretation.**

Suppose a recent Fenwick quarterly shows:

- 75% up-rounds, 15% flat, 10% down-rounds.
- Average price change +18%, median +12%.
- Series-C median pre-money down 20% quarter-over-quarter but up 8% year-over-year.
- Percentage of financings with participating preferred: 12% (down from 18% four quarters ago).

Reading: the market is mixed — up-rounds still dominate, but Series-C pre-moneys have compressed quarter-over-quarter, while the recovery of founder-favourable terms (participating preferred incidence falling) suggests the compression is not yet showing up in term-sheet aggressiveness. A CFO fundraising a Series-C should target a pre-money below the year-ago median and expect the term sheet to be closer to non-participating.

**Where Fenwick is strong.**

- **Consistent methodology across quarters.** The time-series is comparable back to 2002+, which is unusual — most other data sources have methodology breaks.
- **Term-sheet-feature frequencies.** The most reliable public source for how often specific preferred-stock terms appear.
- **Barometer as a single-number market read.** A useful shorthand in board decks and investor conversations.

**Where Fenwick is weak.**

- **Sample bias.** The dataset is companies where Fenwick has visibility, not a random sample. It skews toward the Silicon Valley company universe.
- **Coverage of very early stages.** Fenwick's sample is thinner at pre-seed and seed than at Series-B onwards.
- **Geographic scope.** Silicon Valley only. For a NYC / Boston / European / rest-of-world fundraise, Fenwick is a partial data point at best.

## The Wilson Sonsini Entrepreneurs Report

**Publisher.** Wilson Sonsini Goodrich & Rosati (referred to as "Wilson Sonsini" in current branding; historically "WSGR"), a Silicon Valley-anchored law firm with the largest venture-financing practice in the US. Public at [wsgr.com](https://www.wsgr.com/) → Insights (search "Entrepreneurs Report" if the URL structure changes).

**Coverage.** Financings of US companies for which Wilson Sonsini has visibility, quarterly. Coverage is materially larger than Fenwick's — Wilson Sonsini's overall venture practice touches a very large share of US venture deals — and the geographic scope is national rather than Silicon Valley-only.

**Key data points published per quarter:**

- **Median and average pre-money valuations by round type** (Series-A / B / C / D+).
- **Median amounts raised by round type.**
- **Percentage of up-rounds, flat rounds, and down-rounds** by round type.
- **Bridge-round frequency** and characteristics.
- **Convertible-note and SAFE volumes** and characteristics (cap, discount ranges, MFN incidence).
- **Term-sheet feature frequencies** for priced rounds (liquidation preferences, anti-dilution, pro-rata rights, protective provisions, board composition, drag-along, redemption).
- **Life sciences vs. tech** breakdowns for some data points.
- **Time-series** going back several quarters, allowing quarter-over-quarter and year-over-year comparisons.

**How to read it.** Similar structure to Fenwick, with three specific advantages for the CFO:

- **Seed and pre-seed data.** Wilson Sonsini's report is one of the better public sources on early-stage priced-round data, complementing the SAFE and convertible-note anchor data.
- **National geographic scope.** For a US-domiciled company outside Silicon Valley, Wilson Sonsini's data set is more representative than Fenwick's.
- **Bridge-round tracking.** Bridge rounds (extension SAFE, insider-led bridge note, extension of prior preferred) are called out separately, which matters for chapter 8 and for [mod-109](../mod-109-runway-management-and-bridge-financing/).

**Illustrative interpretation.**

Suppose a recent Wilson Sonsini quarterly shows:

- Series-A median pre-money: $22M (down 15% year-over-year, up 5% quarter-over-quarter).
- Series-B median pre-money: $85M (down 30% YoY, flat QoQ).
- Series-C median pre-money: $210M (down 45% YoY, down 8% QoQ).
- Bridge-round frequency: 18% of Series-B and later financings, up from 12% year-ago.
- Down-round percentage: 22% of priced rounds (up from 8% year-ago).

Reading: the compression is stage-dependent — Series-A pricing is stabilising while Series-C pricing is still compressing. Bridge-round frequency at 18% is elevated relative to historical norms and consistent with an environment where later-stage companies are extending rather than pricing. A CFO targeting a Series-C should expect the compression to continue for another quarter and price accordingly.

**Where Wilson Sonsini is strong.**

- **National scope.**
- **Seed and pre-seed coverage** better than Fenwick.
- **Bridge-round tracking.**
- **Convertible-instrument data cuts** (SAFE cap ranges, note discount ranges).

**Where Wilson Sonsini is weak.**

- **Sample bias** toward companies where Wilson Sonsini has representation. Very large but not random.
- **Methodology changes** over time have caused some breaks in the time-series (fewer than Fenwick's, but present).

## The PitchBook-NVCA Venture Monitor

**Publisher.** PitchBook Data (data provider) in partnership with the National Venture Capital Association (industry association). Public at [nvca.org/research/pitchbook-nvca-venture-monitor](https://nvca.org/research/pitchbook-nvca-venture-monitor/). Full report requires PitchBook access for the deepest data; the summary release and the top-level charts are public.

**Coverage.** US venture-financing activity, quarterly and annually, drawn from PitchBook's comprehensive dataset of announced financings supplemented by NVCA member data. The largest of the three reports by sample size and coverage scope.

**Key data points published per quarter:**

- **Deal count and total capital deployed** by stage (angel/seed, early stage, later stage, growth).
- **Median pre-money valuations by stage.**
- **Median deal size by stage.**
- **Time between rounds** (median months from one financing to the next) by stage.
- **First-time financings vs. follow-on financings.**
- **Exit activity** — IPOs, M&A, secondary transactions, by count and value.
- **Fundraising activity by venture funds** (LP commitments to new funds).
- **Regional cuts** (California / Northeast / South / Midwest and international).
- **Sector cuts** — software, biotech, fintech, consumer, etc.
- **Time series** with quarterly data going back a decade or more.

**How to read it.**

- **The macro cuts.** Deal count and capital deployed give the overall market direction — is the venture market expanding or contracting?
- **Median deal size and pre-money by stage.** The single most useful cut for a specific fundraise. If PitchBook-NVCA shows a Series-A median at $25M pre-money and $12M raised, a CFO targeting a Series-A at $50M pre-money and $20M raised is at the upper end of the market and has to justify it.
- **Time between rounds.** If the median time from Series-A to Series-B has stretched from 18 months to 26 months, the market has slowed and the CFO's runway plan has to accommodate a longer path.
- **First-time vs. follow-on financings.** A shrinking first-time-financings share suggests investors are focusing on their existing portfolio rather than making new bets, which affects the target-investor list construction (mod-107).
- **Fundraising by venture funds.** If venture funds are not raising new capital from LPs, capital availability to portfolio companies will contract in a lag of 12-24 months.

**Illustrative interpretation.**

Suppose a recent PitchBook-NVCA quarterly shows:

- Total US venture capital deployed: down 35% YoY.
- Deal count: down 20% YoY.
- Seed median pre-money: $12M (up 5% YoY).
- Series-A median pre-money: $28M (down 12% YoY).
- Series-B median pre-money: $95M (down 28% YoY).
- Median time from Series-A to Series-B: 24 months (up from 20 months year-ago).
- First-time-financing share: 32% of deals (down from 40% year-ago).
- LP commitments to new funds: down 45% YoY.

Reading: the market is contracting across capital deployed, deal count, pre-moneys (except at seed, which is holding), and time between rounds. New investor engagement is down (fewer first-time financings). The LP-side contraction is a leading indicator that the compression will continue. A CFO targeting a Series-A should plan for a pre-money at or below the $28M median and a raised amount at or below the corresponding median, and should build runway assuming 24+ months to the next round.

**Where PitchBook-NVCA is strong.**

- **Sample size and coverage.** By far the largest of the three data sources.
- **National geographic scope.**
- **Time between rounds** — the specific cut that most affects runway planning.
- **Fundraising-by-funds data.** The leading indicator for future capital availability.
- **Exit-activity data.** Important for the target-exit-value input in the VC method (chapter 2).

**Where PitchBook-NVCA is weak.**

- **Deep detail is subscription-only.** The public summary is useful but incomplete; full PitchBook access is expensive.
- **Term-sheet-feature frequencies** less prominent than in Fenwick or Wilson Sonsini.
- **Announcement bias.** PitchBook's dataset is built on announced financings; unannounced rounds are undercounted.

## Reading the three together

The three reports produce different data cuts and often different specific medians for the same quarter. A CFO reading all three:

- **Uses PitchBook-NVCA as the macro anchor.** Deal count, capital deployed, median deal size and pre-money by stage, time between rounds.
- **Uses Fenwick for term-sheet-feature frequencies and the barometer.** The most-consistent-methodology view of preferred-stock terms.
- **Uses Wilson Sonsini for bridge rounds, seed detail, and convertible-instrument cuts.** Complements Fenwick with national scope and better early-stage detail.
- **Cross-checks specific median pre-moneys by stage across all three.** If Fenwick shows Series-A median at $30M, Wilson Sonsini at $25M, and PitchBook-NVCA at $28M, the market is somewhere in the $25M-$30M range at Series-A and the CFO can defend a target in that range.
- **Reads at least four quarters of history** to detect trend direction rather than a single-quarter blip.

## The market-conditions memo

The output of reading the three quarterly reports is a **market-conditions memo** that anchors the valuation and negotiation strategy for a specific fundraise. Typical structure:

**Section 1 — Macro market read.**

- Total venture capital deployed: current-quarter level and YoY change (from PitchBook-NVCA).
- Deal count: current-quarter level and YoY change.
- Fund fundraising: current-quarter LP commitments and YoY change.
- Read: market is expanding / stable / contracting.

**Section 2 — Stage-specific pricing.**

- Median pre-money at target stage from each of the three reports.
- Interquartile range or "top-decile" pricing at target stage.
- YoY change in stage-specific median pre-money.
- Read: stage-specific market context.

**Section 3 — Round-outcome frequencies.**

- Up-round / flat-round / down-round frequencies at target stage.
- Bridge-round frequency at target stage.
- Time-between-rounds at target stage.
- Read: probability distribution over financing outcomes.

**Section 4 — Term-sheet feature context.**

- Liquidation-preference frequencies (participating vs. non-participating, capped vs. uncapped).
- Anti-dilution provisions (broad-based weighted average dominant, or drift toward narrow-based / full-ratchet).
- Pro-rata rights, protective provisions, board composition patterns.
- Read: what terms are the CFO likely to see in the target term sheet, and are they moving founder-favourable or investor-favourable?

**Section 5 — Application to the specific fundraise.**

- Target pre-money against the three-report range.
- Target raised amount against the median.
- Target term-sheet terms against the current-quarter feature frequencies.
- Read: is the target aggressive, market-standard, or conservative? What is the specific defensible negotiation posture?

The memo is typically 3-5 pages. It ships to the CEO and lead investor conversations as the "here is the market context we are pricing against" reference.

## Common founder traps

- **Using a single quarterly report and ignoring the others.** Each has a bias; triangulation is required.
- **Using a single quarter and ignoring the trend.** Multi-quarter direction matters more than a single-quarter median.
- **Reading the aggregate medians and ignoring the stage-specific data.** Seed and Series-B move very differently; the aggregate is not directly useful for a specific fundraise.
- **Using medians without the interquartile range.** A $25M median with a $15M-$40M interquartile range gives very different pricing latitude than a $25M median with a $22M-$28M interquartile range.
- **Reading pricing without reading terms.** A market with rising median pre-moneys but rising participating-preferred incidence is not obviously founder-favourable overall.
- **Skipping the fund-fundraising data.** LP-side commitments are a 12-24 month leading indicator of capital availability, and CFOs sometimes overlook it in favour of current-quarter deal data.
- **Assuming Silicon Valley is the market.** Fenwick is Silicon Valley; PitchBook-NVCA is national; Wilson Sonsini is national with strong Silicon Valley presence. For non-SV companies, PitchBook-NVCA is the primary anchor.

## What good looks like

A finance leader building a market-conditions memo:

- Reads the current-quarter Fenwick, Wilson Sonsini, and PitchBook-NVCA reports in full.
- Reads at least four trailing quarters of each to establish trend direction.
- Triangulates the stage-specific medians and produces a defensible pre-money range for the target fundraise.
- Cross-checks bridge-round frequency and time-between-rounds against the CFO's runway plan.
- Notes the current-quarter term-sheet feature frequencies and predicts the likely term-sheet terms on the target round.
- Ships the memo to the CEO with a specific target pre-money, target raised amount, and predicted term-sheet features.
- Refreshes the memo quarterly during the fundraise so that no negotiation happens against stale market data.

## Summary

- Three quarterly deal-terms reports dominate as market-conditions references: **Fenwick & West Silicon Valley Venture Survey**, **Wilson Sonsini Entrepreneurs Report**, and **PitchBook-NVCA Venture Monitor**. Each has different coverage, methodology, and strengths.
- Fenwick is strongest on term-sheet-feature frequencies and the barometer (a single-number market direction indicator), with consistent methodology going back to 2002+ but Silicon Valley scope only.
- Wilson Sonsini is strongest on seed / pre-seed detail, bridge-round tracking, and convertible-instrument data, with national scope.
- PitchBook-NVCA is strongest on macro market data (deal count, capital deployed, LP-side fundraising), median deal size and pre-money by stage, and time between rounds, with the largest sample and national scope.
- Reading the three together produces a triangulated market-conditions memo that anchors valuation and negotiation strategy for a specific fundraise. The memo covers macro read, stage-specific pricing, round-outcome frequencies, term-sheet feature context, and application to the specific fundraise.
- Common failure modes: single-source reading, single-quarter reads without trend, using aggregate medians instead of stage-specific data, and ignoring term-sheet feature frequencies alongside pricing.

Chapter 7 turns to Carta's *State of Private Markets*, which uses Carta's proprietary cap-table data set to produce complementary — and often more granular — cuts than the three legal/data-vendor reports here, especially on dilution per round, ESOP sizing, secondary volume, down-round frequency, and bridge-round frequency.
