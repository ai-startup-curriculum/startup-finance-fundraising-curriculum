# Liquidation Preferences — Non-Participating, Participating, Capped, and the Stack

## Why this matters

The liquidation-preference clause is the single largest economic term in the preferred-stock charter. Every other clause redistributes value in narrower ways; this one defines the *order and mechanics* by which the sale price of the company is divided among the preferred and the common at exit. A 1x non-participating stack and a 1x participating stack against the same headline pre-money valuation can produce founder outcomes that differ by 20-30 percentage points of exit proceeds at mid-band exit prices.

The clause has three moving parts:

- **Multiple.** How many times the invested capital the preferred is entitled to as its preference. Modal current-market: 1x. Sometimes 2x or 3x in stressed rounds or in later stages; in the historical extreme, 5x-10x has appeared in the very-late-stage growth market.
- **Participation.** Whether the preferred, after receiving its preference, also participates alongside the common in the residual (participating), participates up to a cap (capped participation), or does not participate at all (non-participating, in which case the preferred chooses at exit between taking its preference or converting to common and taking its as-converted share of the whole exit price — the "convert or preference" election).
- **Seniority.** Where this class of preferred sits relative to other classes when there are multiple rounds. Options: **senior** (this class is paid first, in full, before junior classes get anything), **pari passu** (all preferred classes are paid proportionally out of the preference pool), or **junior** (this class is paid after other classes — very rare and only in some late-round pay-to-play situations).

This chapter walks the three axes, the current market standard at Series-A, and the specific patterns that appear at Series-B, Series-C, and in stressed rounds. Chapter 3 handles the waterfall arithmetic that translates these structures into dollars-per-holder at defined exit prices.

## The 1x non-participating baseline

The current Series-A market standard in the US is a 1x non-participating liquidation preference. The mechanics:

- The preferred is entitled to receive, before any distribution to common, the greater of (a) 1x its original purchase price plus any accrued but unpaid dividends, or (b) the amount it would receive if it had converted to common immediately before the liquidation event.
- "1x non-participating" is often expressed in the charter as: "In the event of a Liquidation Event, the holders of Series A Preferred shall be entitled to receive, prior and in preference to any distribution to holders of Common Stock, an amount equal to the greater of (i) one times the Original Purchase Price per share plus any accrued but unpaid dividends, or (ii) the amount they would receive on an as-converted basis."
- The "greater of" mechanic is the key. It defines the "convert or preference" election: the preferred holder gets the *better* of the preference outcome or the as-converted-to-common outcome.

The "convert or preference" election drives the entire waterfall logic:

- At a **low exit price** (below the amount at which as-converted equals the preference), the preferred takes its preference. The common gets whatever is left.
- At a **high exit price** (above the amount at which as-converted equals the preference), the preferred converts and takes its as-converted share of the whole pot. Common takes the rest.
- The **crossover point** between these two regimes is the exit price at which the preferred's preference dollars equal the preferred's as-converted-share dollars. Above the crossover, converting is better; below, taking the preference is better. Chapter 3 works the crossover algebra.

Why 1x non-participating is founder-favourable:

- **The preferred never gets both.** Either the preference or the as-converted share, not both.
- **At high-price exits, the preferred converts and the common takes their share.** The common's economics are simple as-converted arithmetic once the preferred has converted.
- **The "extra" money in a good exit goes to the common (and the pool).** The preferred's upside is capped at their as-converted share — they don't skim off the top.

Why 1x non-participating became market:

- Founder pushback (post-2003 dot-com-bust, then reinforced in the 2010s founder-favourable market) drove the frequency of participating preferred down materially. Data from Fenwick, Wilson Sonsini, and Carta over the last decade has consistently shown 1x non-participating as the dominant structure at Series-A.
- Institutional VC funds recognised that the participating-preferred "double-dip" earned a reputation as founder-punitive and adjusted their template term sheets to lead with non-participating in most cases.
- Under a 1x non-participating structure, the VC's return depends primarily on the company's exit-price outcome, not on the specific preference gymnastics. This aligns incentives.

The 1x non-participating structure is what the CFO expects on a Series-A term sheet from a top-tier institutional lead in a normal market. Deviations upward (participating, or higher-than-1x multiple) are the ones the CFO negotiates.

## Participating preferred — the "double-dip"

Under a 1x participating structure, the preferred is entitled to receive its preference (1x invested capital) *and* to participate proportionally alongside the common in the residual. Mechanically:

- **Step 1.** Preferred takes 1x its invested capital as the preference (senior to common).
- **Step 2.** The remainder of the exit proceeds is distributed to the preferred and common *together*, proportionally on an as-converted basis.

The preferred gets *both* — hence "double-dip." No "greater of" election; the preferred always gets its preference plus its as-converted share.

Worked comparison — the same $50M exit under the two structures, with a single Series-A preferred class ($10M invested, 25% as-converted ownership):

- **1x non-participating.** Preferred elects the better outcome. Preference: $10M. As-converted: 25% × $50M = $12.5M. Preferred takes $12.5M (as-converted is higher). Common takes $37.5M.
- **1x participating.** Preferred takes $10M preference, then 25% of the remaining $40M = $10M residual. Total preferred: $20M. Common takes 75% × $40M = $30M.
- **Founder-side delta:** $37.5M vs. $30M common — participating costs the common $7.5M on this exit, or 15% of total exit value.

The delta grows in absolute terms with the exit price but shrinks in percentage terms:

- At $20M exit: non-participating (preferred converts if better — here preference dominates, so preferred takes $10M, common takes $10M) vs. participating ($10M preference + 25% × $10M = $12.5M preferred, $7.5M common). Participating cost the common $2.5M / $10M = 25% of what the common otherwise would have received.
- At $100M exit: non-participating ($25M preferred, $75M common) vs. participating ($10M + 25% × $90M = $32.5M preferred, $67.5M common). Participating cost the common $7.5M / $75M = 10% of what the common otherwise would have received.
- At $500M exit: non-participating ($125M preferred, $375M common) vs. participating ($10M + 25% × $490M = $132.5M preferred, $367.5M common). Participating cost the common $7.5M / $375M = 2% of what the common otherwise would have received.

The participating penalty is a fixed dollar amount (the preference multiple × the invested capital, minus the difference in the as-converted math), so it becomes a smaller percentage as the exit grows. This is why participating preferred hurts most at *mid-band* exits and least at *unicorn* exits — the mid-band is the range where "the preference amount is a meaningful fraction of the exit."

**Market frequency.** Fenwick and Wilson Sonsini data over the last decade show participating preferred at Series-A oscillating typically in the low-teens to low-twenties percent range, with the incidence rising in stressed markets and falling in founder-favourable ones. Series-B and later see somewhat higher participating incidence, particularly in growth-stage crossover-fund deals. Carta's cap-table data set produces broadly consistent readings. Consult the current-quarter reports (chapter 9) for the current number.

**When to accept 1x participating anyway.** A CFO may accept a 1x participating structure in specific contexts:

- The pre-money valuation is materially above the market median — the "you get a higher headline, they get a slightly better preference" trade.
- The company is in a stressed situation (down round, restructuring) where the alternative is walking away.
- The participating clause is *capped* (see below), which materially reduces the mid-band cost.

## Capped participation

Capped participation is a compromise structure: the preferred participates alongside the common up to a defined cap (typically 2x or 3x invested capital, inclusive of the preference), above which the preferred stops participating.

Mechanically:

- **Step 1.** Preferred takes 1x preference.
- **Step 2.** Preferred participates with common up to the cap.
- **Step 3.** Above the cap, the preferred's total take is fixed at the cap (which is 2x or 3x of invested capital). It stops receiving further residual distributions.
- **Step 4.** But the preferred has the option to *convert to common* at any time — so if the exit price is so high that its converted-common share would exceed the cap, it converts and takes its full as-converted share.

The cap creates a piecewise outcome curve for the preferred:

- Below the "preference-only" crossover: preferred takes 1x preference.
- Between the crossover and the cap: preferred takes 1x preference + participation.
- Above the cap (but below the as-converted-exceeds-cap threshold): preferred is capped at 2x or 3x.
- Above the as-converted-exceeds-cap threshold: preferred converts and takes full as-converted share.

Worked example — 1x participation with a 3x cap on the $10M Series A above:

- Exit $20M: preferred takes $10M preference + 25% × $10M = $12.5M (below the $30M cap). Common $7.5M.
- Exit $50M: preferred takes $10M + 25% × $40M = $20M (below the $30M cap). Common $30M.
- Exit $100M: preferred would take $10M + 25% × $90M = $32.5M under uncapped participation, but the cap is $30M, so preferred is capped at $30M. Common $70M. But: as-converted share at $100M = 25% × $100M = $25M, which is less than $30M; so the preferred takes the capped $30M rather than converting. Common $70M.
- Exit $200M: uncapped participation would be $10M + 25% × $190M = $57.5M; capped at $30M; but as-converted = 25% × $200M = $50M > $30M cap, so preferred converts to common and takes $50M. Common $150M.
- Exit $500M: uncapped $10M + 25% × $490M = $132.5M; capped at $30M; as-converted 25% × $500M = $125M >> $30M cap, converts to common. Common $375M.

The cap protects the common at very high exits (the preferred converts and stops taking the double-dip); the preference plus participation still hurts at mid-band; the cap has no effect at low-band exits where the preference-only regime dominates.

**Market frequency.** Capped participation appears less frequently than either 1x non-participating or full participating; it is a specific compromise negotiated when the parties want to bridge a valuation disagreement or when the market is mid-cycle. A cap of 2x is investor-favourable-of-the-caps; a cap of 3x is closer to a founder-favourable capped structure; higher caps (5x+) exist but converge on uncapped participation.

## Preference multiples above 1x

The multiple is the second axis. A "2x non-participating" preferred is entitled to 2x its invested capital as the preference (or its as-converted share, whichever is greater). A "3x participating" preferred is entitled to 3x invested capital plus participation.

Higher multiples are unusual at Series-A in a normal market — the CFO who sees a 2x on a Series-A term sheet from an institutional lead should treat it as an "unusual" tier-4 clause and negotiate hard to 1x. Higher multiples appear more frequently:

- In late-stage growth rounds where a large check earns preferential treatment ("preference stacking" — the growth investor gets 1.5x or 2x on a large late-stage cheque).
- In bridge financings where the bridge investor gets a preference premium (typically as a warrant coverage feature rather than a straight multiple, but sometimes structured as a multiple in a formal bridge financing — chapter 8 of [mod-109](../mod-109-runway-management-and-bridge-financing/) has depth on this).
- In pay-to-play recapitalisations where the participating investors get a bumped-multiple preferred and the non-participating investors get diluted or converted to common (see chapter 4 on anti-dilution and [mod-109](../mod-109-runway-management-and-bridge-financing/) on pay-to-play).
- In distressed situations (a company that is nearly-out-of-cash accepts a preference multiple to secure the emergency capital).

The dollar cost of a multiple upgrade is straightforward — 2x on a $10M investment is $20M in preference vs. $10M for 1x. The common gets $10M less at low-to-mid-band exits. Above the crossover (where the preferred converts to common), the multiple has no effect (converting to common doesn't get you 2x, only your as-converted share).

## Senior vs. pari-passu stacks

By Series-B, there are two classes of preferred on the cap table (Series A + Series B); by Series-C there are three; and so on. The seniority axis defines how the preference pool is divided when there is more than one class:

**Pari passu across series** (the modal current-market structure at Series-B and beyond). All preferred classes are treated as one preference pool. If exit proceeds are less than the aggregate preference of all classes together, they are distributed *proportionally* to the preference amounts. Example: Series A preference $10M, Series B preference $20M. Exit is $15M cash. Aggregate preference: $30M. Distribution: Series A takes $15M × $10M/$30M = $5M; Series B takes $15M × $20M/$30M = $10M. Common takes $0.

**Senior stack (Series B senior to Series A senior to common).** The most-recent series is paid first, in full, before earlier series get any preference. This is investor-favourable to the *later* series and increasingly appears in late-stage rounds or in stressed rounds where the later-stage investor demands seniority as a condition of investment. Example: same $10M Series A / $20M Series B / $15M exit. Series B is senior and takes its full $15M before Series A gets anything. Series A takes $0 (nothing left). Common takes $0.

**Junior stack (Series B junior to Series A).** Very rare, and only appears in specific late-stage bridge situations where a later investor takes a junior preferred as part of a specific structure. Not something the CFO expects to see at Series-A.

The senior-vs.-pari-passu distinction is a live Series-B / Series-C / Series-D negotiation. Later-stage investors sometimes push for senior preference; earlier-stage investors want pari passu to protect their earlier preference from being subordinated. Founders sit in the middle — a senior stack at later stages accelerates the common's downside in a mid-band exit because the entire senior preference is paid before any lower class or the common sees anything.

**Charter language.** The Model Certificate of Incorporation contains a bracketed choice — "senior" vs. "pari passu" — that gets filled in per the negotiated term. A founder-favourable Series-B term sheet says "the Series B Preferred shall rank pari passu with the Series A Preferred with respect to liquidation preference"; an investor-favourable version says "the Series B Preferred shall rank senior to all other classes of Preferred and to the Common."

**Which is market at Series-B?** Data from Fenwick and Wilson Sonsini historically shows pari passu as the dominant structure at Series-B and Series-C in normal markets, with senior-stack incidence rising in stressed markets and in growth-stage rounds. Series-D and later see more senior-stack structures. Consult current-quarter data (chapter 9).

## The interaction with founders and options

The preferred stack sits above **all** common stock — including founder common, exercised-option common, and vested-but-unexercised options at exit (which typically convert at exit into option-payout mechanics that follow the common waterfall).

The specific implication: at exit prices below the crossover point, the entire preference stack is paid before *any* common holder — founder, employee, or exercised option-holder — sees any distribution. If the preference stack aggregate is $50M and the exit is $60M cash, the preferred takes $50M and the common (all of it) takes $10M. Founders receive their share of that $10M, minus any option exercise proceeds paid at exit, and minus any transaction bonuses or retention pool designated out of the common proceeds.

This is why *mid-band* exits — the range from $50M to $250M where many acquisitions land — are the range in which the preference structure matters most for the founder and employees. Above $500M-$1B, the preferred typically converts and the arithmetic simplifies; below the aggregate preference amount, the common gets zero regardless of structure. It is in the middle that participating vs. non-participating, senior vs. pari passu, and the specific multiples move real dollars.

## The common-employee retention pool

A related but distinct topic: at exit, when the preference stack absorbs a large fraction of exit proceeds and the common's take is small, boards typically approve a **management carve-out** or **employee retention pool** — a pool of exit proceeds carved off the top (before the preferred is paid, in some structures, or off the preferred's take, in others) to compensate the founders and key employees who otherwise would receive little.

The mechanics vary but the common patterns:

- **Pre-preference carve-out.** A fixed dollar amount (say, 10% of exit proceeds, capped at $X) is set aside for the management team before the waterfall runs. The preferred and common then split the remainder.
- **Preferred-side carve-out.** The preferred agrees to reduce its preference by a defined amount to fund the pool.
- **Board-approved MIP (management incentive plan).** A retention plan approved by the board that pays founders and executives a defined amount at closing.

Preference-structure design and management-carve-out design interact — the more punitive the preference stack (participating, senior, high multiple), the more the board typically has to negotiate a carve-out to keep the management team engaged through closing. The CFO who understands the waterfall can model this and negotiate the carve-out at the exit-transaction stage.

## The full-cycle CFO read

For every preferred-stock financing the CFO is negotiating, the liquidation-preference clause should be read as a five-question checklist:

1. **What is the multiple?** 1x is market. Anything above 1x should be treated as tier-3 or tier-4 and negotiated hard.
2. **Is it participating or non-participating?** 1x non-participating is market at Series-A. Participating is a real economic ask that the CFO must price and (usually) push back on.
3. **If participating, is there a cap?** Uncapped participating is worse than capped. A 2x cap is investor-favourable-of-the-caps; a 3x cap is more founder-favourable. Uncapped-with-no-cap at Series-A is tier-4 and should not be accepted.
4. **What is the seniority relative to prior series?** Pari passu is market at Series-B (and preserves the earlier series' position). Senior is a real ask by later-stage investors and should be negotiated against.
5. **Where does this preference structure land the common at three exit-price scenarios?** Chapter 3 walks the waterfall arithmetic; the CFO should model at least a low-band, mid-band, and high-band scenario before accepting the term.

## What good looks like

A CFO who has this chapter installed:

- Reads any liquidation-preference clause against the multiple, participation, cap, and seniority axes and classifies it immediately.
- Knows the current-quarter incidence of participating preferred and higher-than-1x multiples from the Fenwick / Wilson Sonsini / Carta data.
- Runs the three-scenario waterfall (low-band, mid-band, high-band exit) before accepting any deviation from 1x non-participating.
- Pushes for pari passu at Series-B and beyond by default, and negotiates against senior-stack proposals with specific counter-language.
- Coordinates the interaction between the preference structure and the potential management carve-out with counsel and the board.

## Summary

- The liquidation-preference clause is the largest single economic term in the preferred-stock charter. It has three moving parts: multiple (1x is market), participation (non-participating is market at Series-A), and seniority (pari passu is market at Series-B and beyond).
- 1x non-participating is founder-favourable and current-market at Series-A. The "greater of preference or as-converted" mechanic gives the preferred the better outcome without the double-dip.
- 1x participating gives the preferred both the preference and its as-converted share — the "double-dip." Historically an investor-favourable position with meaningful mid-band cost to the common. Incidence oscillates with market conditions.
- Capped participation compromises between the two: participation up to a defined cap, above which the preferred stops participating. A 2x or 3x cap is typical when the structure is used.
- Preference multiples above 1x are unusual at Series-A and appear more frequently in later-stage rounds, bridges, and stressed situations.
- Seniority defines how multiple classes of preferred share the preference pool. Pari passu is market at Series-B and beyond; senior stacks appear in stressed markets and in growth-stage rounds where a later-stage investor demands seniority.
- The preference structure has its largest founder cost at *mid-band* exit prices — the range where the preference is a meaningful fraction of the exit and the common's share is materially compressed. Above the crossover point the preferred converts to common and the structure has less effect.
- Boards frequently negotiate management-carve-out pools at exit to compensate the common when the preference stack has absorbed most of the exit proceeds.

Chapter 3 turns to the specific waterfall arithmetic — the math that turns any preference structure into dollars per holder at defined exit prices, the crossover points that define the regimes, and the "sale above the last valuation but the common still gets very little" trap that surprises many founders on their first mid-band exit.
