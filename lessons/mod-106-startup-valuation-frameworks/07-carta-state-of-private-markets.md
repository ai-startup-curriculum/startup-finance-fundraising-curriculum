# Carta State of Private Markets — Cap-Table-Data Primary Source

## Why this matters

The three quarterly reports in chapter 6 are compiled from law-firm-representation data (Fenwick, Wilson Sonsini) and announced-financing data (PitchBook-NVCA). Each is a strong reference for market conditions, and each has a specific sample bias. There is one additional data source whose position in the reference stack is different: **Carta's State of Private Markets**, which is compiled from Carta's own cap-table platform data.

Carta hosts a large share of US venture-backed startup cap tables — the company reports serving tens of thousands of private companies across its platform. Every issuance, every conversion, every secondary transaction, and every option grant on those cap tables is recorded in Carta's underlying database. The State of Private Markets report is a periodic aggregation of that dataset, published free at [carta.com/data](https://carta.com/data). Because it is drawn from the actual cap tables rather than from announced financings, it captures data that the other three reports miss — particularly on dilution, ESOP sizing, secondary volume, and bridge-round activity — and captures them at a level of granularity that no other public source provides.

This chapter walks the specific cuts Carta publishes, how to read them alongside the reports in chapter 6, and how to use them as the primary-source benchmark against which the CFO checks a specific valuation target.

## Carta's coverage and methodology

**Publisher.** Carta (formerly eShares). Public reports at [carta.com/data](https://carta.com/data). Historical releases are archived; the current issue is the primary reference.

**Coverage.** Cap tables managed on the Carta platform. Carta's disclosed platform scale runs into the tens of thousands of active private-company cap tables, dominated by US venture-backed startups. Coverage is heavily weighted toward companies that use Carta as their equity-management provider — that is, primarily seed-and-beyond venture-backed companies, and disproportionately those in tech / software.

**Methodology strengths.**

- **Primary-source data.** The dataset is the actual cap table, not a reported financing announcement or a legal-representation observation. This means Carta observes the transaction as it is recorded, including the specific share counts, cap-table entries, and downstream conversions.
- **Continuous coverage.** Because the cap table is updated continuously as transactions occur, Carta sees the full round mechanics (pool refresh, SAFE conversion, pro-rata cheques) rather than a single announced-price data point.
- **Cross-cut segmentation.** Cap tables include the underlying share classes, so Carta can cut the data by round type, share class, transaction type (primary vs. secondary), founder retention, and dilution mechanics that other sources cannot resolve.

**Methodology cautions.**

- **Platform bias.** Carta's user base skews toward certain profiles (US, tech, venture-backed at seed and beyond). Coverage of very-early pre-seed (before the company has adopted an equity-management platform), non-US companies, and non-venture-backed private companies is thinner.
- **Timing lag.** Some transactions are recorded on Carta with a delay after they close. Very-current-quarter data may be revised in subsequent releases.
- **Definitional consistency.** Carta's category definitions (what counts as a "Series-A," what counts as a "down-round") are Carta's definitions; they broadly match industry usage but may differ from the definitions used by Fenwick / Wilson Sonsini / PitchBook-NVCA in specific edge cases.

## Key data cuts Carta publishes

The State of Private Markets report is reorganised release-to-release, but the following cuts have been consistent recent-year features. Read the current issue for the specific set and the specific definitions.

### Valuation by stage

- Median and quartile pre-money valuations at pre-seed, seed, Series-A, Series-B, Series-C, Series-D, and later.
- Time series showing quarter-over-quarter change.
- Sub-cuts by geography (US regions, sometimes international) and by industry vertical (SaaS, fintech, health tech, etc.).

Reading this alongside PitchBook-NVCA (chapter 6): Carta's medians and PitchBook's medians should broadly agree for stages Carta covers well (seed through Series-C). Where they diverge, the difference is usually explainable by sample bias (Carta's tech-heavy platform skew produces different medians than PitchBook's broader sample).

### Dilution per round

- Median dilution taken by investors at each round type (seed / Series-A / B / C / D+).
- Distribution around the median (quartiles or deciles).
- Time-series showing how per-round dilution has moved.

Carta is one of the few public sources that publishes per-round dilution as its own cut. The reason is methodological — Carta sees the actual issuances, so it can compute the pre-round-holder dilution directly. Chapter-2's VC-method calculation and chapter-8's negotiation-failure-mode analysis both rely on this cut.

Typical recent-vintage medians (order-of-magnitude, will move with market cycles; check the current issue):

- Seed: 15-25% dilution.
- Series-A: 15-25% dilution.
- Series-B: 15-20% dilution.
- Series-C: 10-20% dilution.
- Later stages: 10-15% dilution.

Note that these medians *include* the pool refresh (typically 5-10% of the total dilution comes from a pool refresh at the round). Some Carta cuts separate the pool refresh from the new-money dilution; read the specific chart.

### ESOP (option pool) sizing

- Median unissued option pool as a percentage of fully-diluted shares at each stage.
- Distribution of pool sizes.
- Refresh cadence — how often pools get topped up between rounds.

This is directly relevant to the pre-money / post-money pool-shuffle mechanic ([mod-104 chapter 2](../mod-104-cap-tables-and-equity-compensation/02-pre-vs-post-money-math-and-the-option-pool-shuffle.md)). A CFO negotiating a Series-A term sheet with a "10% post-close pool" ask can look up Carta's data to defend a smaller pool or accept the ask against a market comparable.

### Secondary-transaction volume

- Number and dollar volume of secondary transactions on the Carta platform, by stage.
- Median secondary price relative to the most recent primary-round price.
- Concentration — which stages have the most secondary activity.

Secondary transactions matter for valuation in a specific way: a secondary transaction closing at a materially different price than the last primary round is a market signal about the company's valuation between primary rounds. Carta's secondary data is one of the few public sources on secondary pricing patterns. Detail lives in the [`startup-exit-curriculum`](https://github.com/ai-startup-curriculum/startup-exit-curriculum) for transaction execution; this data is a market-context read.

### Down-round frequency

- Percentage of primary rounds that priced below the prior round's post-money (a down round).
- Trend line over multiple quarters.
- Sub-cuts by stage (down-round frequency at Series-C differs from at Series-A).

Down-round frequency is the single most direct signal of market-conditions compression. A quarter with 5% down rounds is a very different market from a quarter with 25%. This cut is directly comparable to Fenwick's up-vs.-down-round data and Wilson Sonsini's equivalent cut.

### Bridge-round frequency

- Percentage of companies raising a bridge round (extension SAFE, insider-led bridge note, extension of prior preferred) between priced rounds.
- Sub-cuts by prior-round stage.
- Time series.

Bridge-round frequency is a slower-moving signal than down-round frequency but a more forward-looking one. A market with rising bridge-round frequency has companies extending because a priced round at the target level is not available. That is a leading indicator of further pricing compression. See [mod-109 chapter 2](../mod-109-runway-management-and-bridge-financing/) for the mechanics of the bridge instruments themselves.

### Other cuts sometimes published

- **Cash raised by stage** — median amount raised per round.
- **Time between rounds** — comparable to PitchBook-NVCA's cut.
- **Founder ownership evolution** — median founder ownership at each stage.
- **Employee equity concentration** — how much of the pool is held by non-founder employees, distribution of grant sizes.
- **Vesting acceleration frequency** — how often single-trigger vs. double-trigger acceleration is present in equity documents.
- **Repricing / exchange offers** — frequency of underwater-option repricing events (a stress signal).

Not all of these appear in every release; read the current issue.

## How Carta complements the chapter-6 reports

Carta is not a substitute for the reports in chapter 6; it is a complement. The specific complementarity:

| Data cut | Best source(s) |
|---|---|
| Deal count and total capital deployed | PitchBook-NVCA |
| Median pre-money by stage | Cross-check across Carta, PitchBook-NVCA, Wilson Sonsini |
| Dilution per round | **Carta** (primary), Wilson Sonsini (secondary) |
| ESOP / pool sizing | **Carta** (primary) |
| Secondary-transaction pricing | **Carta** (primary among public sources) |
| Down-round frequency | Cross-check across Carta, Fenwick, Wilson Sonsini |
| Bridge-round frequency | **Carta** and Wilson Sonsini |
| Term-sheet feature frequencies | **Fenwick** (primary), Wilson Sonsini |
| Time between rounds | PitchBook-NVCA and Carta |
| LP-side fundraising | **PitchBook-NVCA** (primary) |
| Founder ownership evolution | **Carta** (primary) |

The pattern: Carta is the primary reference for cap-table-mechanics data (dilution, pool, secondary, founder ownership); the chapter-6 reports remain primary for term-sheet features (Fenwick), macro market activity (PitchBook-NVCA), and geographic-national aggregation (Wilson Sonsini and PitchBook-NVCA).

## Using Carta in a valuation memo

The specific ways Carta data enters a valuation memo:

### Cross-check on the pre-money target

- Look up Carta's current-quarter median pre-money at the target stage in the target's vertical.
- Compare against the CFO's derived target (from the VC method and multiples framework).
- If the derived target is >1 standard deviation above the Carta median, prepare to defend the premium with specific arguments (comparable-set placement, growth-band placement, Rule of 40).

### Dilution assumption in the VC method

- Chapter 2's VC method requires an assumed dilution schedule from today's round through exit.
- Carta's per-round dilution medians are the primary anchor for this assumption.
- Build the round-by-round dilution ladder using Carta's medians (with adjustments for company-specific factors like anticipated pool refreshes and secondary transactions).

### Pool-refresh negotiation

- Chapter 3 of mod-104 (ESOP top-ups) walks the pool-refresh negotiation.
- Carta's median pool sizing at the target stage is the anchor for what an incoming investor will ask for.
- If Carta shows median 8% post-close pool at Series-B and the term sheet asks for 12%, the CFO has a specific comparable to negotiate against.

### Bridge-vs.-priced round decision

- If Carta's bridge-round frequency has risen sharply and down-round frequency has followed, the market is signalling that a priced round at the target level may be difficult.
- The CFO's decision to price the round vs. do a bridge (mod-109) has to consider these signals.

### Down-round context

- If the target round is priced below the prior post-money, the down-round is not a signal that the company failed — it may be a signal that the market moved.
- Carta's down-round frequency (and Fenwick's) gives the CFO the market context to explain the down-round to the board and to employees.

## Reading Carta over time

Carta publishes retrospective reports (annual "State of Private Markets" reviews) alongside the quarterly updates. Reading two-to-three years of Carta data alongside the chapter-6 reports is the standard practice for establishing the current-quarter's placement in the market cycle:

- **Where does the current-quarter median pre-money at the target stage sit in the trailing-12-quarter distribution?** 25th percentile? 75th? Extreme?
- **How has per-round dilution moved?** Up (investors demanding more), down (investors accepting less), or stable?
- **How has bridge-round frequency moved?** Rising / falling / stable?
- **How has down-round frequency moved?** Rising / falling / stable?

The answers to those four questions constitute the market-cycle read that anchors the rest of the valuation memo.

## Common founder traps

- **Treating Carta's medians as the "right" price.** Carta's data is a *comparable* — one of several. The right price for a specific company is a triangulation of the multiples framework, the VC method, the anchor bracket, and the market-conditions data. Anchoring exclusively to Carta produces the same problem as anchoring exclusively to any single source: the specific circumstances of the company aren't being priced.
- **Using Carta alone and ignoring PitchBook-NVCA / Fenwick / Wilson Sonsini.** Carta's platform bias is real; cross-checking across sources is required.
- **Reading a single Carta release.** The trend across multiple releases matters more than any single median.
- **Confusing per-round dilution with SAFE overhang.** [mod-105 chapter 7](../mod-105-convertible-instruments/07-convertible-instrument-failure-modes-and-remediation.md) walks the SAFE-overhang mechanic. Carta's per-round dilution median is the priced-round dilution alone; if the target has significant SAFE overhang, the effective dilution at the priced round will be higher than Carta's median (SAFEs plus new money plus pool refresh all diluting together).
- **Missing the vertical / sub-sector cut.** Carta typically publishes vertical cuts (SaaS vs. fintech vs. health tech, etc.). The aggregate median is often not the right comparable; the sub-sector median usually is.
- **Assuming Carta covers non-US or non-venture data cleanly.** Coverage is US venture-heavy. For a European fundraise or a non-venture private-company valuation, Carta's data is a partial input at best.

## What good looks like

A finance leader reading Carta State of Private Markets alongside the chapter-6 reports:

- Downloads and reads the current issue in full at the start of the fundraise process.
- Cross-references the specific data cuts that matter for the target fundraise (median pre-money at target stage, per-round dilution, pool sizing, bridge frequency, down-round frequency) against Fenwick / Wilson Sonsini / PitchBook-NVCA.
- Uses Carta's dilution medians as the anchor for the VC-method dilution schedule (chapter 2).
- Uses Carta's pool sizing data as the anchor for pool-refresh negotiations (mod-104 chapter 3).
- Reads at least two-to-three years of Carta history to place the current quarter in the market cycle.
- Cites specific Carta data cuts in the valuation memo and in board decks — the CFO who says "Carta's Q3 State of Private Markets shows Series-B median dilution at 19% and pool sizing at 10%" is quantitatively more defensible than the CFO who says "the market is compressing."

## Summary

- Carta's State of Private Markets is a periodic, freely-published report drawn from Carta's proprietary cap-table platform data. It is the primary public reference for cap-table-mechanics data — dilution per round, ESOP sizing, secondary volume, founder ownership evolution — that the chapter-6 reports cover less directly.
- Carta's methodology strengths are primary-source data (actual cap tables, not announced financings), continuous coverage of full round mechanics, and cross-cut segmentation by stage / vertical / geography. Its weakness is a platform bias toward US venture-backed tech companies at seed and beyond.
- Key data cuts include: median pre-money by stage; dilution per round (with distribution); ESOP sizing; secondary-transaction volume and pricing relative to prior primary; down-round frequency; bridge-round frequency; time between rounds; founder ownership evolution.
- Carta complements rather than substitutes for Fenwick, Wilson Sonsini, and PitchBook-NVCA. The full market-conditions read triangulates across all four sources, with Carta the primary source for cap-table mechanics and the chapter-6 reports the primary sources for term-sheet features, macro activity, and geographic-national aggregation.
- The main uses in a valuation memo: cross-check on the pre-money target, dilution assumption in the VC method, pool-refresh negotiation anchor, bridge-vs.-priced decision context, and down-round market-context defence.
- Common failure modes: treating Carta as the "right" price without triangulation, single-release reading, ignoring vertical cuts, and assuming Carta covers non-US or non-venture cleanly.

Chapter 8 turns to the three canonical valuation-negotiation failure modes — anchoring to last round's post-money, chasing a public-comp multiple that ignores growth-and-margin bands, and ignoring the VC's fund math — and prescribes the specific fix for each.
