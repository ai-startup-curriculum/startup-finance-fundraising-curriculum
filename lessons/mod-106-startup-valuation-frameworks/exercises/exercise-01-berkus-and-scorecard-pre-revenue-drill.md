# Exercise 01 — Berkus, Payne Scorecard, and Risk-Factor Summation Pre-Revenue Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 1 (pre-revenue anchor methods).

## Problem statement

Apply all three pre-revenue anchor methods — the Berkus Method, the Payne Scorecard Method, and risk-factor summation — to the same hypothetical pre-revenue startup. Produce the three individual outputs, produce the triangulated bracket, and author a one-page memo to the founder that (a) recommends a specific defensible point in the bracket for the round pricing, (b) names the argument for that specific point, and (c) cross-checks the point against the current-quarter market-conditions data.

The drill's goal is to build muscle memory around the specific mechanics of each method, to see the outputs side-by-side on a single company, and to develop the discipline of always presenting a bracket-with-defence rather than a single number.

## Scenario — build your own

Construct a hypothetical pre-revenue startup with the following minimum shape:

- Delaware C-corp, incorporated 6 months ago.
- Two co-founders. Founder A: 5-year engineering experience at a well-known tech company, no prior startup exit. Founder B: 8-year sales experience at a large enterprise software company, no prior startup exit.
- One additional engineering hire (30% commitment, deferred cash comp).
- Product: a horizontal SaaS collaboration tool for a specific vertical (pick one: legal, healthcare-provider admin, construction PM, or another vertical you can plausibly describe).
- Prototype: working alpha, used by 4 design-partner customers on a pilot basis with no paying contracts yet.
- Market: TAM of $3B+ (defended by public reports you can cite — Gartner, Forrester, or an industry association).
- Competition: 2-3 well-funded direct competitors and 3-5 adjacent players.
- Runway: 8 months of cash on hand from founder capital.
- Fundraising target: **$1M seed round** on a pre-money to be determined.

Extend the scenario with any additional detail needed to run the three methods coherently.

## Requirements

Produce a single workbook (Excel or Google Sheets) plus a one-page memo:

1. **Berkus tab.**
   - Score each of the five Berkus components (sound idea, prototype, quality management team, strategic relationships, product rollout / sales) for the scenario company.
   - Use the classic 0-$500K scale with a $2.5M ceiling. If you use a different vintage (Berkus's inflation-adjusted per-component caps), name it explicitly and defend the choice.
   - Show the per-component score and the Berkus total.

2. **Payne Scorecard tab.**
   - Look up a regional-average pre-money for pre-seed or seed-stage rounds in the target company's geography and vertical. Use a specific, dated, real data source (Angel Capital Association HALO Report, PitchBook, CB Insights, a regional angel-group summary, or a Carta State of Private Markets extract). Cite the source and the specific number used.
   - Apply the Payne factor weights (management 30% / opportunity 25% / product 15% / competition 10% / marketing 10% / additional investment 5% / other 5%).
   - Rate the target company against the regional-average on each factor (50%-200% scale).
   - Compute the weighted multiplier and the Payne pre-money.

3. **Risk-factor summation tab.**
   - Use the same regional-average baseline as the Payne tab.
   - Apply the 12-factor scoring on the -$500K / -$250K / $0 / +$250K / +$500K scale.
   - Sum the twelve adjustments and produce the risk-factor pre-money.

4. **Triangulation tab.**
   - Show the three outputs side-by-side.
   - Compute the range spanned by the three (min, max, spread).
   - Identify the defensible point in the bracket you would use as the negotiation anchor.
   - Argue explicitly for that point — which method(s) support it, why the others should be discounted, what specific factors about the target justify the placement.

5. **Market-conditions cross-check tab.**
   - Pull the current-quarter median pre-seed / seed pre-money for comparable US venture-backed startups from at least one of the reports covered in chapters 6-7 (Fenwick / Wilson Sonsini / PitchBook-NVCA / Carta).
   - Compare the anchor-method bracket to the current-quarter median.
   - Note whether the bracket sits at, above, or below the market median. If above or below, note by how much and consider whether the anchor bracket needs adjustment.

6. **One-page founder memo.**
   Written to the founder explaining:
   - The three method outputs and the triangulated bracket.
   - The specific defensible point in the bracket for the round pricing.
   - The market-conditions cross-check and any adjustment implied.
   - The two or three factors the founder should be prepared to defend in the angel-group screen or partner meeting.
   - A caveat naming which anchor-method assumptions are the most subjective and would move the answer most if a counterparty pushed back.

## Starter guidance

- **Use a real regional-average baseline.** The load-bearing input to Payne and risk-factor summation is the regional average. Do not invent it. Use a dated, cited number from a public data source. If the number is stale, note it and add a manual adjustment for market-conditions movement since the source's date.
- **Score Berkus components honestly.** The temptation is to score all five near the top of the scale. Resist. The point of the drill is to show a triangulated bracket, not to inflate the anchor.
- **Berkus's ceiling is a real ceiling.** If the classic $2.5M ceiling is well below what Payne and risk-factor produce, the divergence is informative and should be discussed in the memo. Do not paper over it.
- **The scorecard and risk-factor methods share a baseline.** They will usually produce answers within 30% of each other. Large divergence between them typically means one of the factor scores is wrong on one side or the other; investigate before finalising.
- **The market-conditions cross-check is not optional.** A bracket that is defensible in a normal market is not defensible in a compressed market at half the median pre-money. Do the cross-check even if the anchor bracket is what you're primarily defending.
- **Name the vintage of every method.** Berkus 1996 vs. Berkus inflation-adjusted; Payne classic weights vs. modified weights; risk-factor summation 12-factor vs. 10-factor variant. The vintage matters.

## Acceptance criteria

- **All three methods are run on the same scenario** with the specific per-component / per-factor scores documented.
- **The regional-average baseline is a real, dated, cited number** from a public data source, not an invented plug.
- **The triangulation tab shows the three outputs, the bracket range, and the defensible point** with an explicit argument for the placement.
- **The market-conditions cross-check references a specific quarterly report** (Fenwick / Wilson Sonsini / PitchBook-NVCA / Carta) with the specific data cut used and the source date.
- **The founder memo makes a specific pre-money recommendation** with a walk-through of the factors that support it, prepared for pushback.
- **The vintage of each anchor method is named** (Berkus 1996 / inflation-adjusted; Payne classic / modified; risk-factor 12-factor / other) with an explicit choice justification.

## Deliverables

- The workbook with all five tabs (Berkus, Payne, risk-factor, triangulation, market-conditions).
- The one-page founder memo (Markdown, PDF, or a memo tab in the workbook).
- A list of the specific citations used (regional-average baseline, market-conditions data, TAM sources).

## Extensions (optional)

- Add a **VC-method cross-check** (chapter 2) — assume a $1M cheque from a lead pre-seed fund of $50M with a target 30× MOIC on winners, an assumed $200M target exit, and a four-round dilution ladder. Compute the VC-method pre-money and compare against the anchor bracket.
- Add a **scenario-based sensitivity** — rerun all three methods under a "market-corrected" baseline (regional-average pre-money 30% lower) and note how the bracket shifts.
- **Author a rejection memo** to the founder if a demanded pre-money at the top of the bracket ($X) is not defensible against the market-conditions data. Recommend a delay, a bridge round, or a lower target pre-money with the specific rationale.
- **Add a Payne-only stress test** — rerun the scorecard with each of the seven factors moved by ±25% (one at a time) to identify which factor the answer is most sensitive to. The one that moves the answer most is the one the negotiation will concentrate on.
