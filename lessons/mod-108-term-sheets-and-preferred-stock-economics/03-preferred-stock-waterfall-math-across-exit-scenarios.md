# Preferred-Stock Waterfall Math Across Exit Scenarios

## Why this matters

Every preferred-stock preference structure resolves at exit into the same question — "who gets what dollars when the company sells for $X?" — and the answer is a waterfall calculation the CFO must be able to build, defend, and read against alternative preference structures. The clause language of chapter 2 defines the *rules*; the waterfall is the *engine* that turns exit price into dollars-per-holder.

Two specific patterns get missed by founders who don't build the waterfall:

- The **exit-above-the-last-valuation-but-common-still-gets-little trap**. A founder who reads "we raised the last round at $50M post-money and we sold for $75M — that's a gain!" without running the waterfall can be shocked to discover that under a participating stack, the common walks with dollars that don't feel like a "gain" at all.
- The **crossover regime shift**. Preferred-stock outcomes are piecewise — one regime applies below the crossover, a different regime above. A CFO who doesn't identify the crossover doesn't understand what specifically has to change to move the common's outcome across the regime boundary.

This chapter walks the actual arithmetic. Chapter 2 handled the structures; this chapter handles the numbers.

## The waterfall model — anatomy

A preferred-stock waterfall is a sequential calculation:

- **Start with exit proceeds** (cash from sale, or the value of stock received in a stock deal, or a mix — chapter 3 assumes all-cash for clarity; mixed-consideration deals are covered in the module's lab).
- **Apply transaction expenses**. Investment banker fee, legal fees, escrow, insurance tail, other closing costs. Nets down to "net exit proceeds available to the cap table."
- **Apply the preference stack**, in seniority order. Each class of preferred is paid its preference amount (multiple × original purchase price + accrued dividends, if cumulative) *in seniority order* and *within a class in proportion to preference amount* if pari passu.
- **After the preference stack, distribute the residual to common**, plus any participating-preferred participation as defined by each class's specific structure.
- **The greater-of election** for each non-participating class: the class holder elects at exit between (a) taking its preference or (b) converting to common and taking its as-converted share. Chosen at the whole-class level (all shares of a class elect together, per the charter language).

For a multi-class stack with mixed participation and seniority, the algorithm is:

1. **Test each non-participating class's election.** For each non-participating class, compute the preference amount and the as-converted amount at the given exit price. The class elects the greater.
2. **Assemble the "preference pool"** — the sum of preferences elected by non-participating classes plus the preference component of participating classes.
3. **Distribute the preference pool in seniority order**. Senior classes are paid in full before junior classes; classes at the same seniority level split proportionally to preference amount.
4. **Compute the residual** = net exit proceeds − preference-pool distributions.
5. **Distribute the residual to common plus any participating-preferred classes** on an as-converted basis. Non-participating classes that elected preference receive nothing from the residual; non-participating classes that elected as-converted are already in the "as-converted" pool. Participating classes get their preference *and* their as-converted share of the residual.
6. **Apply capped-participation caps**. If a participating class's total (preference + participation) exceeds its cap, it is capped at the cap — but the excess residual then re-distributes to the remaining participants (common and any other participating classes).
7. **Test the "convert to common" election** for capped-participation classes at very high exits — if converting to common yields more than the cap, the class converts and takes its full as-converted share instead.
8. **Sum per-holder distributions** and reconcile: total distributions should equal net exit proceeds exactly.

## Base scenario — single-round Series A

Setup:

- Company sold on all-cash exit. Various exit prices.
- **Series A Preferred.** $10,000,000 raised at $5.00 per share (2,000,000 shares). 1x non-participating. No dividend. Pari passu with any junior classes if any exist.
- **Common Stock.** 8,000,000 shares (founders and early common).
- **Options.** 1,000,000 shares fully vested and exercised (or treated as exercised at exit, with strike-price mechanics ignored for simplicity in this base case).
- Fully-diluted total: 11,000,000 shares. Series A as-converted percentage: 2,000,000 / 11,000,000 = 18.18%.

**Preference and as-converted crossover.**

- Preference = $10M.
- As-converted at exit price X: 18.18% × X.
- Crossover: 0.1818 × X = $10M → X = $55M. At exit prices above $55M, the Series A converts and takes its 18.18% share; at exit prices below $55M, Series A takes the $10M preference.

**Waterfall at defined exit prices** (all-cash, ignoring transaction expenses):

| Exit price | Series A preference-vs-AC decision | Series A takes | Common takes (81.82%) | Common $/share (8M common; ignore options for now) |
|---|---|---|---|---|
| $10M | Preference dominates | $10M | $0 | $0.00 |
| $30M | Preference ($10M > $5.45M AC) | $10M | $20M | $2.50 |
| $50M | Preference ($10M > $9.09M AC) | $10M | $40M | $5.00 |
| $55M | Indifferent ($10M = $10M) | $10M | $45M | $5.625 |
| $75M | AC ($13.64M > $10M) — converts | $13.64M | $61.36M | $7.67 |
| $150M | AC ($27.27M) — converts | $27.27M | $122.73M | $15.34 |
| $300M | AC ($54.55M) — converts | $54.55M | $245.45M | $30.68 |

Read: at the $55M crossover, the Series A is indifferent and the common gets $45M / 8M = $5.625 per common share. Above the crossover, Series A converts and the common's per-share climbs with the exit price on an as-converted basis. Below the crossover, the Series A eats $10M off the top and the common gets whatever remains.

**Chart-shape intuition.** Common takes zero at any exit price ≤ $10M (preference dominates entirely), grows linearly (with slope 1.0 on total exit) from $10M to $55M in the "preference-controls" regime, then grows linearly (with slope 0.8182 on total exit — the common's as-converted share) above $55M in the "convert-controls" regime. There is a kink at the crossover — the common's slope shifts from 1.0 to 0.8182 as the Series A stops taking a fixed $10M and starts taking a proportional share of the whole exit.

## Same scenario with 1x participating

Change one thing: make the Series A 1x participating (uncapped) instead of 1x non-participating.

Mechanics: Series A takes $10M preference *and then* participates alongside the common in the residual on an as-converted basis. There is no election — Series A always gets both.

Series A participation share = 18.18% (same as as-converted percentage).

| Exit price | Series A preference | Series A participation | Series A total | Common (81.82% of residual) | Common $/share |
|---|---|---|---|---|---|
| $10M | $10M | 18.18% × $0 = $0 | $10M | $0 | $0.00 |
| $30M | $10M | 18.18% × $20M = $3.64M | $13.64M | $16.36M | $2.05 |
| $50M | $10M | 18.18% × $40M = $7.27M | $17.27M | $32.73M | $4.09 |
| $55M | $10M | 18.18% × $45M = $8.18M | $18.18M | $36.82M | $4.60 |
| $75M | $10M | 18.18% × $65M = $11.82M | $21.82M | $53.18M | $6.65 |
| $150M | $10M | 18.18% × $140M = $25.45M | $35.45M | $114.55M | $14.32 |
| $300M | $10M | 18.18% × $290M = $52.73M | $62.73M | $237.27M | $29.66 |

**Common-cost delta from participating vs. non-participating** at each exit:

| Exit | Non-participating common $/share | Participating common $/share | Δ per share | Founder cost on 4M founder shares |
|---|---|---|---|---|
| $30M | $2.50 | $2.05 | −$0.45 | −$1.82M |
| $50M | $5.00 | $4.09 | −$0.91 | −$3.64M |
| $75M | $7.67 | $6.65 | −$1.02 | −$4.09M |
| $150M | $15.34 | $14.32 | −$1.02 | −$4.09M |
| $300M | $30.68 | $29.66 | −$1.02 | −$4.09M |

The participating penalty asymptotes at $1.02 per share ($4.09M for 4M founder shares) at high exits — that's just the founder's proportional share of the $10M preference that gets "double-dipped" (81.82% × $10M / 8M = $1.02). At the $150M+ exit prices, the participating structure costs the founder approximately $4M in exit proceeds compared to non-participating. At mid-band exits (say $50M-$75M), the participating structure costs a similar or slightly greater dollar amount but a much larger *percentage* of the founder's take.

## Same scenario with capped participation

Now 1x participating with a 3x cap (i.e., total preferred take capped at $30M inclusive of preference and participation). Series A can also convert to common if converting yields more than the cap.

| Exit price | Uncapped participating would yield | Cap ($30M) hits? | AC ($18.18% × exit) exceeds cap? | Series A takes | Common takes | Common $/share |
|---|---|---|---|---|---|---|
| $30M | $13.64M | No | No ($5.45M) | $13.64M | $16.36M | $2.05 |
| $50M | $17.27M | No | No | $17.27M | $32.73M | $4.09 |
| $75M | $21.82M | No | No | $21.82M | $53.18M | $6.65 |
| $100M | $10M + 18.18% × $90M = $26.36M | No | No | $26.36M | $73.64M | $9.20 |
| $150M | $10M + 18.18% × $140M = $35.45M | Yes | No ($27.27M) | $30M (capped) | $120M | $15.00 |
| $200M | $10M + 18.18% × $190M = $44.55M | Yes | No ($36.36M) | $30M (capped) | $170M | $21.25 |
| $220M | $10M + 18.18% × $210M = $48.18M | Yes | Yes-ish ($40M > $30M) → converts | $40M (AC) | $180M | $22.50 |
| $300M | Would be $62.73M | AC ($54.55M) > cap ($30M) → converts | Yes | $54.55M | $245.45M | $30.68 |

Note the piecewise structure:

- **Regime 1** (exit ≤ preference-only crossover): preferred takes preference (in this participating case, always takes preference + participation).
- **Regime 2** (crossover < exit ≤ cap-binding point): preferred takes preference + participation without the cap binding.
- **Regime 3** (cap-binding point < exit ≤ AC-exceeds-cap threshold): preferred is capped at the cap. Common absorbs the "return" above the cap.
- **Regime 4** (exit > AC-exceeds-cap threshold): preferred converts to common and takes its full as-converted share; capped structure is now equivalent to non-participating.

The **cap-binding point** = the exit at which uncapped participation would equal the cap = $10M + 18.18% × (X − $10M) = $30M → X = $120M.

The **AC-exceeds-cap threshold** = the exit at which as-converted share = cap = 18.18% × X = $30M → X = $165M.

Between $120M and $165M the preferred is capped at $30M. Above $165M the preferred converts to common and stops being capped. Below $120M the participating math applies uncapped.

The **capped-participation common-per-share is intermediate** between full participating and non-participating — better than participating in regimes 3 and 4, but worse than non-participating in regimes 1 and 2 (because the participation still applies at lower exits).

## Adding Series B — the multi-class stack

Now consider the same company after a Series B closes. Assume:

- **Series A.** 2,000,000 shares at $5.00 = $10M invested. 1x non-participating.
- **Series B.** 4,000,000 new shares at $10.00 = $40M invested. 1x non-participating. Pari passu with Series A on liquidation (the modal-market Series B structure).
- **Common.** 8,000,000 shares.
- **Options.** 1,500,000 shares (500K new pool top-up at Series B, all vested and exercised for the base case).
- Fully-diluted total: 15,500,000. Series A as-converted percentage: 12.90%. Series B as-converted percentage: 25.81%. Common + options as-converted: 61.29%.

**Aggregate preference.** Series A $10M + Series B $40M = $50M.

**Individual crossovers.**

- Series A crossover (Series A prefers convert vs. take preference): 12.90% × X = $10M → X = $77.5M.
- Series B crossover: 25.81% × X = $40M → X = $155M.

**Full-stack waterfall — pari-passu case.**

At exit prices below $50M, aggregate preference exceeds exit; Series A and Series B split the exit proportionally to preference: Series A takes X × $10M/$50M, Series B takes X × $40M/$50M. Common takes $0.

At exit prices between $50M and $77.5M, both A and B take their preferences (aggregate $50M) and common takes the residual (X − $50M).

At exit prices between $77.5M and $155M, Series A prefers to convert (as-converted > $10M preference); Series B still prefers preference. Series B takes $40M; Series A takes 12.90% × X; common takes X − $40M − 12.90% × X = 0.8710 × X − $40M. Actually — careful — if Series A converts, then the as-converted denominator has to be recomputed to reflect the conversion. In practice at 12.90% Series A and a decision to convert, the Series A moves from the preference pool into the as-converted pool with the common; the common + Series A as-converted then share `(X − $40M)` proportionally to their as-converted shares.

Redo — at $100M exit under pari-passu with Series B taking preference and Series A converting:

- Series B takes $40M preference.
- Residual = $60M.
- Series A (2M shares) and common+options (9.5M shares) share $60M as-converted. Series A takes 2 / 11.5 × $60M = $10.43M. Common+options take 9.5 / 11.5 × $60M = $49.57M.
- Common per-share (8M common of 9.5M common+options): common's share of the $49.57M = 8/9.5 × $49.57M = $41.75M / 8M shares = $5.22 per share.
- Alternative: at $100M exit if Series A had taken its preference instead of converting: Series A $10M, Series B $40M, common+options $50M. Common per-share: 8/9.5 × $50M / 8M = $5.26 per share. Series A takes $10M vs. $10.43M by converting. Series A chose correctly ($10.43M > $10M).

Above $155M, both Series A and Series B convert. All classes are in the as-converted pool.

- At $200M: Series A = 2/15.5 × $200M = $25.81M; Series B = 4/15.5 × $200M = $51.61M; common = 8/15.5 × $200M = $103.23M; options = 1.5/15.5 × $200M = $19.35M. Total $200M. Common per-share: $12.90.
- At $500M: Series A $64.52M; Series B $129.03M; common $258.06M; options $48.39M. Common per-share: $32.26.

**Founder-friendly frame.** Below $50M the founder gets zero. Between $50M and $77.5M the founder starts getting something but at a modest per-share number. Between $77.5M and $155M the founder benefits from Series A's conversion but Series B is still eating $40M off the top. Above $155M both convert and the founder gets full as-converted share.

**Senior-stack alternative.** If Series B is senior to Series A (instead of pari passu), the math shifts at low-to-mid-band exits:

- At $40M exit: Series B takes $40M in full (all exit proceeds). Series A takes $0. Common takes $0. (Under pari passu, Series A would have taken $40M × $10M/$50M = $8M and Series B $32M.)
- At $60M exit: Series B takes $40M. Residual $20M. Series A takes $10M preference. Common takes $10M.
- At $75M exit: Series B $40M; Series A prefers preference ($10M > 12.90% × $75M = $9.68M); common $25M.
- At $80M exit: Series B $40M; Series A close to crossover (12.90% × $80M = $10.32M > $10M preference); Series A converts; but if Series A converts, the residual = $40M shared by A+common+options as-converted. Careful math needed on the stacked case.

Senior stacks compress the common's outcome at low-to-mid-band exits; above the fully-converted range the effect vanishes.

## The "sale above the last valuation" trap

A common founder-facing scenario:

- Company raises Series B at $200M post-money on $40M Series B raise. Aggregate preference stack: $10M Series A + $40M Series B = $50M. Total FD: 15.5M shares.
- Sale two years later at $200M — "the same as the last round's post-money valuation, so surely everyone's whole."

Under 1x non-participating pari passu (worked above at $200M exit): Series B converts, takes $51.6M; Series A converts, takes $25.8M; common+options take $122.6M (of which founders' share depends on common breakdown). Total $200M. Founders (assume 4M of 8M common) take 4/15.5 × $200M = $51.6M. That's the "priced round math" answer.

Under 1x participating pari passu at $200M:

- Series B takes $40M preference + 25.81% × ($200M − $50M) = $40M + $38.71M = $78.71M.
- Series A takes $10M preference + 12.90% × ($200M − $50M) = $10M + $19.35M = $29.35M.
- Common+options take (8+1.5)/15.5 × ($200M − $50M) = 61.29% × $150M = $91.94M.
- Founders (4M of 8M common) take 4/9.5 × $91.94M share of common+options × the common's share within common+options: 4/9.5 × 8/9.5 = 0.354; but simpler: 4M shares of 15.5M FD × the common's residual share of the pot. Under participating, common+options got $91.94M, of which the founders' 4M common of 9.5M common+options is 4/9.5 = 42.1%, so founders take $38.7M.

**Delta.** Non-participating founder outcome at $200M sale = $51.6M. Participating founder outcome = $38.7M. Difference: $12.9M — 25% of the founder's take, on an exit that headline-matched the last round's post-money valuation. The founder feels the loss even at a "flat" exit.

Under **senior-stack** participating at the same $200M exit: Series B takes $40M + 25.81% × ($200M − $40M) = $40M + $41.29M = $81.29M. Series A residual: $200M − $81.29M = $118.71M. Series A takes $10M + 12.90% × ($118.71M − $10M) — no, the math is different under senior stack. Under senior stack, Series B is paid first in full, then the residual goes to the Series A preference pool. Careful mechanics:

- Series B $81.29M (its preference + its participation on the *entire* residual after its preference).
- Residual after Series B: $118.71M.
- Series A takes $10M preference + participation on remainder.
- Then common on the tail.

This chapter avoids over-drilling the senior-stack participating combined case — it is unusual and appears mainly in stressed late-stage rounds. The point: the compounding of participation and seniority produces founder outcomes at "flat" exits that can materially undershoot the intuitive "sale = last valuation = par" reading.

## What the CFO produces — the waterfall workbook

Every priced-round negotiation should be accompanied by an exit-scenario waterfall workbook the CFO produces before accepting the term sheet. Minimum structure:

- **Cap-table input tab.** All classes of preferred (share count, invested capital, preference multiple, participation flag, cap if any, seniority rank, dividend rate and cumulation), common, options, warrants.
- **Preference-stack summary tab.** Aggregate preference amount, seniority order, key crossover points computed from the class structure.
- **Exit-scenario table.** 5-9 exit prices (low, low-mid, mid, mid-high, high; a "sale at last-round post-money" scenario; a "sale at 2x last-round" scenario; a "sale at last-round pre-money" stressed scenario). For each: per-class take, per-share for common, and total-check to reconcile to exit proceeds.
- **Alternative-structure comparison.** Same exit prices, but re-run under (a) 1x non-participating baseline, (b) 1x participating uncapped, (c) 1x capped at 2x or 3x, and (d) any hybrid the term sheet contemplates. Founder-per-share and founder-total under each.
- **Sensitivity to specific term parameters.** Multiple, participation cap, seniority. What is the marginal founder-cost of accepting each shift?
- **Founder-facing memo.** One page: "Under the proposed 1x participating structure, at the following four scenarios the founder walks with $X vs. $Y under 1x non-participating. The mid-band scenarios ($75M-$150M) are where the participating structure costs the founder most in percentage terms." Names the specific asks for the negotiation.

The workbook is a live artefact — it updates as the term sheet moves through negotiation rounds and as the cap table's shape changes.

## Common founder traps

- **Not building the waterfall before accepting the term sheet.** The most common failure. The founder accepts a participating clause because "the pre-money is high" and doesn't quantify the mid-band cost until years later at the exit meeting.
- **Only running one exit scenario.** The waterfall's structure changes across regimes. Running only the "target" or "aspirational" exit misses the mid-band trap.
- **Confusing per-share and total distribution.** Common per-share numbers are the wrong metric for the founder; the founder cares about their total dollar walk, which is per-share × their specific founder share count net of any secondary sales or repurchases.
- **Ignoring options and warrants.** Vested-but-unexercised options at exit convert into option-payout mechanics that follow the common waterfall; ignoring them overstates the founder's per-common-share outcome.
- **Reading "sale above last valuation" as automatically neutral for the common.** Under a participating stack, a flat exit at the last-round post-money can still cost the founder 20-30% of their take relative to a non-participating structure.
- **Assuming the crossover point is fixed.** Each preferred class's crossover depends on the specific invested-capital, share-count, and preference structure. Adding a Series B changes the Series A crossover (through fully-diluted denominator changes).
- **Not modelling the "management carve-out"** that a board would negotiate at exit if the preference stack absorbs too much of the exit proceeds. This is a real dollar amount that offsets some of the waterfall cost to the founder.

## What good looks like

A CFO who has this material installed:

- Builds and maintains a live waterfall workbook for every priced-round company they support.
- Runs the 5-9 exit-scenario table under multiple preference structures before accepting any term sheet.
- Identifies the crossover points and the regime shifts explicitly.
- Produces the founder-facing memo that quantifies the term-sheet cost in dollars at named exit scenarios.
- Refreshes the waterfall after each subsequent round to keep the crossover analysis honest.
- Coordinates with the board on the management-carve-out negotiation if a mid-band exit is on the near horizon and the preference stack is heavy.

## Summary

- The waterfall is the arithmetic that turns any preference structure into dollars-per-holder at defined exit prices. Every preference clause in chapter 2 resolves into the waterfall.
- The single-round Series A 1x non-participating waterfall has a "preference-controls" regime below the crossover and an "as-converted-controls" regime above. The crossover is the exit at which preference dollars equal as-converted dollars.
- 1x participating waterfalls give the preferred both the preference and the as-converted share; the founder cost asymptotes to the founder's proportional share of the preference amount at very high exits, but is proportionally largest at mid-band exits.
- Capped participation is piecewise — participation up to a cap, capped above, and then the preferred converts to common at very high exits when converting yields more than the cap. Four regimes.
- Multi-class stacks require careful ordering of preference distribution and residual re-distribution; pari-passu classes split proportionally to preference amount, senior classes are paid first in full.
- Senior stacks compress the common's outcome at low-to-mid-band exits; the effect vanishes above the fully-converted threshold.
- A "sale above the last valuation" can still shortchange the common under a participating or senior-stack structure — the founder feels the loss even at "flat" exits.
- The CFO's output is a live waterfall workbook with cap-table input, exit-scenario table, alternative-structure comparison, sensitivity block, and a founder-facing memo naming the specific term-sheet asks.

Chapter 4 turns to the second-largest single economic term in the charter — the anti-dilution provision — which adjusts the preferred conversion price after a down round and, under a full-ratchet or narrow-based-weighted-average formula, can materially compress the common's share of the cap table before the exit waterfall is even run.
