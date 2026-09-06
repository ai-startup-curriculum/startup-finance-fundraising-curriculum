# Exercise 05 — Market-Conditions Read from Fenwick, Wilson Sonsini, PitchBook-NVCA, and Carta

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 6 (quarterly deal-terms reports) and chapter 7 (Carta State of Private Markets).

## Problem statement

Read one recent Fenwick Silicon Valley Venture Survey, one recent Wilson Sonsini Entrepreneurs Report, one recent PitchBook-NVCA Venture Monitor, and one recent Carta State of Private Markets. Triangulate the four sources into a market-conditions memo tied to a specific fundraising target. Produce a defensible current-quarter pre-money range, a predicted term-sheet-feature profile, and an assessment of financing outcome probabilities (up-round / flat / down / bridge).

The drill's goal is to build the muscle of *reading four different market datasets against each other* — recognising where they agree, where they diverge, and why — and to install the habit of never negotiating a valuation against stale or single-source market data.

## Scenario — build your own

Construct a hypothetical fundraising target that will use the market-conditions memo as its context:

- Company stage: pick one — pre-seed, seed, Series-A, Series-B, or Series-C.
- Vertical: pick one that Carta and PitchBook publish vertical cuts for (e.g., SaaS, fintech, health tech, consumer, deep tech).
- Geography: US-domiciled; pick a specific region (California, NYC, Boston, Texas, other).
- Fundraising target: a specific dollar amount and a target pre-money you will validate against the market data.
- Runway status: current runway (e.g., 12 months) and a specific "we need to close by month N" constraint.
- Prior round context: prior-round post-money and date (if not first round), or the initial-capitalisation cap-table if pre-seed.
- Target lead-investor pool profile: seed-only funds, multi-stage funds, corporate strategics, etc. (This informs the term-sheet-feature reading.)

## Requirements

Produce a workbook with source-extraction tabs plus a market-conditions memo.

1. **Source-index tab.**
   - For each of the four reports, note the specific issue used, source URL, publication date, coverage period (e.g., "Q2 [year]"), and the date you accessed it. Sources:
     - **Fenwick & West — Silicon Valley Venture Survey** — [fenwick.com/insights](https://www.fenwick.com/insights) (search "Silicon Valley Venture Survey").
     - **Wilson Sonsini — Entrepreneurs Report** — [wsgr.com/en/insights](https://www.wsgr.com/en/insights.html) (search "Entrepreneurs Report").
     - **PitchBook-NVCA Venture Monitor** — [nvca.org/research/pitchbook-nvca-venture-monitor](https://nvca.org/research/pitchbook-nvca-venture-monitor/).
     - **Carta State of Private Markets** — [carta.com/data](https://carta.com/data).

2. **Fenwick extract tab.**
   - Pull the current-quarter Fenwick Barometer value (magnitude and direction).
   - Up-round / flat / down-round percentages.
   - Average and median price change (all rounds; then by round type if disclosed).
   - Term-sheet feature frequencies: participating vs. non-participating preferred, senior vs. pari passu, anti-dilution provisions (broad-based / narrow-based / full-ratchet), pay-to-play, redemption rights, dividend rates.
   - Trailing 4-quarter values for each above, from the same report.

3. **Wilson Sonsini extract tab.**
   - Median and average pre-money by round type (Series-A / B / C / D+, plus seed if available).
   - Median amounts raised by round type.
   - Up / flat / down-round frequencies by round type.
   - Bridge-round frequency and characteristics.
   - Convertible-note and SAFE volumes (cap ranges, discount ranges, MFN incidence).
   - Term-sheet feature frequencies (liquidation preferences, anti-dilution, pro-rata, protective provisions, board composition, drag-along).
   - Trailing 4-quarter values where disclosed.

4. **PitchBook-NVCA extract tab.**
   - Deal count and total capital deployed (US venture, current quarter and YoY change).
   - Median pre-money valuations by stage (angel/seed, early stage, later stage, growth).
   - Median deal size by stage.
   - Time between rounds (median months from prior to current round) by stage.
   - First-time vs. follow-on financings share.
   - Exit activity — IPOs, M&A, count and value.
   - LP commitments to new venture funds (current-quarter, YoY change).
   - Regional cuts (California / Northeast / Midwest / South) or sector cuts for the target's geography and vertical.

5. **Carta extract tab.**
   - Median pre-money at target stage in target vertical.
   - Median dilution per round at target stage.
   - Median ESOP / option-pool sizing at target stage.
   - Down-round frequency at target stage (current quarter and trailing).
   - Bridge-round frequency at target stage (current quarter and trailing).
   - Secondary-transaction volume and median-price-vs.-prior-primary if disclosed.
   - Founder ownership evolution or median founder retention at target stage if disclosed.
   - Any additional cut relevant to the target (vertical-specific dilution, industry-specific pool sizing, etc.).

6. **Triangulation tab.**
   - Side-by-side of the median pre-money at the target stage from all four sources.
   - Note the range (min to max) and the reason for any divergence >20% (sample bias — Fenwick is SV-only, Carta is platform-tech-heavy, PitchBook-NVCA is national; methodology definition — what counts as "Series-B" varies; timing lag — Carta may under-report the most recent quarter).
   - Compute a triangulated pre-money range for the target — usually the intersection of the four sources' interquartile ranges (or, if they don't overlap, the reasoned midpoint with a discussion of the divergence).
   - Cross-check bridge-round and down-round frequencies across Fenwick / Wilson Sonsini / Carta. If frequencies are converging upward, the market is compressing further; if diverging, one source is picking up something the others aren't.

7. **Trend tab.**
   - Trailing 4-6 quarter values for each source's key cuts (median pre-money at target stage; up/flat/down-round frequencies; bridge frequency; deal count and capital deployed).
   - Chart the trends. Is the market compressing, stable, or expanding?
   - Note the direction and magnitude of change over the trailing year.

8. **Market-conditions memo (3-5 pages).**
   Written to the CEO / board with the following structure:
   
   - **Section 1 — Macro market read.**
     - Total US venture capital deployed (current quarter, YoY change) from PitchBook-NVCA.
     - Deal count (current quarter, YoY change).
     - LP-side fundraising (current quarter, YoY change).
     - Read: market is expanding / stable / contracting.
   - **Section 2 — Stage-specific pricing.**
     - Median pre-money at target stage from each of the four sources.
     - The triangulated pre-money range.
     - YoY change in the stage-specific median.
     - Read: how the target's target pre-money compares to market medians.
   - **Section 3 — Round-outcome frequencies.**
     - Up / flat / down / bridge frequencies at target stage.
     - Time-between-rounds at target stage from PitchBook-NVCA and Carta.
     - Read: probability distribution over financing outcomes for the target.
   - **Section 4 — Term-sheet feature context.**
     - Current-quarter frequencies for liquidation preferences, anti-dilution, pro-rata, protective provisions, board composition, drag-along, from Fenwick and Wilson Sonsini.
     - Read: what terms is the target likely to see in the incoming term sheet, and are they moving founder-favourable or investor-favourable?
   - **Section 5 — Cap-table mechanics anchors.**
     - Dilution per round from Carta.
     - ESOP / pool sizing at target stage from Carta.
     - Read: what dilution and pool asks should the CFO expect and negotiate against.
   - **Section 6 — Application to the specific fundraise.**
     - Target pre-money against the triangulated range: aggressive / market-standard / conservative.
     - Target raised amount against the median.
     - Predicted term-sheet features.
     - Recommended negotiation posture and the specific pre-money floor / ceiling / walk-away.
     - Runway-and-timing recommendation given the time-between-rounds trend.

## Starter guidance

- **Do not use single-source data.** Every published quarterly report has a sample bias. Fenwick is Silicon Valley-only; Wilson Sonsini skews toward companies with Wilson Sonsini as counsel; PitchBook-NVCA is announcement-biased; Carta is platform-user-biased. Triangulation is required.
- **Read multiple trailing quarters.** A single-quarter median can be a blip. The trend is what matters.
- **Distinguish stage-specific from aggregate cuts.** Aggregate medians conflate seed and growth; the numbers relevant to your specific fundraise are the stage-specific cuts.
- **Note the definitions.** Fenwick's definition of "up-round" and Carta's may differ slightly. If a specific data cut looks anomalous, check the definition footnote in the source report before writing the anomaly into the memo.
- **Read the LP-side data.** LP commitments to new funds are a 12-24 month leading indicator of capital availability. A quarter with strong current-quarter deal activity but weak LP-side fundraising is a market on the way down. The CFO's runway plan has to account for the lag.
- **Cross-reference bridge frequency and down-round frequency.** Rising bridge frequency with stable down-round frequency suggests companies are extending rather than pricing (a slow signal). Rising bridge frequency with rising down-round frequency is a market in active compression. The interpretations are different.
- **Read the term-sheet-feature context alongside the pricing.** A market with rising median pre-moneys but rising participating-preferred incidence is not obviously founder-favourable overall; the terms are moving in the opposite direction from the headline.

## Acceptance criteria

- **All four sources are cited by specific issue and access date** in the source-index tab.
- **Each source has a dedicated extract tab** with the specific cuts named in the requirements.
- **The triangulation tab produces a triangulated pre-money range** for the target with a discussion of any divergence >20%.
- **The trend tab charts trailing 4-6 quarters** of key metrics and names the trend direction.
- **The memo is 3-5 pages** and covers all six sections above with specific data citations for every claim.
- **The recommendation section produces a specific pre-money floor, ceiling, and walk-away** anchored in the four-source triangulation.
- **The runway-and-timing recommendation** references the specific time-between-rounds data from PitchBook-NVCA and Carta.

## Deliverables

- The workbook with all eight tabs.
- The market-conditions memo (Markdown or PDF, 3-5 pages).
- A one-page board-briefing summary with the four-source triangulated range, trend direction, and specific recommendation.

## Extensions (optional)

- **Add a Cooley GO Venture Financing Report cross-check.** Cooley's [quarterly venture financing report](https://www.cooleygo.com/venture-financing-report/) covers similar cuts to Fenwick and Wilson Sonsini with a different sample. Adds a fifth source for cross-check.
- **Add an Aumni Venture Beacon cross-check.** Aumni (a JPM subsidiary) publishes venture-terms data drawn from its own dataset. Useful especially for term-sheet features.
- **Author a founder-facing FAQ.** For each of the "board and employees will ask" questions ("why is our pre-money lower than the last round?", "why is the incoming term sheet asking for participating preferred?", "why is the time to next round longer than we planned?"), provide the specific market-conditions-anchored answer with cited data.
- **Rerun the memo assuming the target is in a downcycle.** Discount the derived pre-money range by 25% (or use a specific historical downcycle quarter as the reference). Note how the term-sheet-feature predictions shift.
- **Add a comparable-fundraise reference set.** Pull three specific recent priced rounds from the target's vertical and stage (announced financings from PitchBook, TechCrunch, The Information, or SEC Form D filings) and compare their pre-moneys and disclosed terms against the memo's derived range. Discuss any target-specific factors that would justify pricing above or below the reference set.
- **Author a "when to delay" trigger memo.** Given the market-conditions read, define the specific conditions under which the founder should delay the raise (further compression, LP-side deterioration, sector-specific dislocation) and the specific bridge-financing plan for the delay. Cross-reference [mod-109](../../mod-109-runway-management-and-bridge-financing/).
