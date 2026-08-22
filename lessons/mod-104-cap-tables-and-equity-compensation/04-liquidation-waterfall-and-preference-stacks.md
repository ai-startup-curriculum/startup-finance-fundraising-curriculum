# Liquidation Waterfall and Preference Stacks

## Why this matters

The cap table shows who owns the company. The waterfall shows who gets **paid** when the company is sold.

Those are different questions, and the difference is where founder-side surprises happen at exit. A sale price above the last round's post-money valuation intuitively feels like a win — the company sold for more than the investors paid. But under a 2x participating preferred stack with senior liquidation preferences, that same headline exit can leave common shareholders with dramatically less than the pro-rata share of the sale price their cap-table percentage implies. The preferred waterfall runs first, and only what remains flows to common.

The instrument that governs the waterfall is the certificate of incorporation, specifically the certificate-of-designation sections for each preferred series that specify: liquidation preference multiple (usually 1x, occasionally higher), participation right (non-participating, participating, or capped participation), seniority (senior to prior series, pari passu with prior series, or subordinate), and the deemed-liquidation-event definition that determines what triggers the waterfall (usually a change of control or an asset sale, per Delaware GCL 251 and the certificate's own language). The NVCA model financing documents — specifically the Model Certificate of Incorporation and Model Voting Agreement — are the reference against which most term sheets and charter language are drafted.

This chapter installs the waterfall mechanics. Chapter 8 (in mod-108) picks up the *negotiation* of these terms; this chapter is about the *math* of what those terms produce at exit.

## The three questions the waterfall asks

Every exit waterfall answers the same three questions in the same order:

1. **What is the exit consideration** — how much cash-equivalent is the acquirer paying, in total, for 100% of the equity? (Deal structures: all-cash, stock-for-stock, cash-plus-earnout, cash-plus-holdback, secondary-plus-primary tender.)
2. **How does the preferred stack extract its liquidation preference** — in what order, at what multiple, and with what participation rights?
3. **How does the residual pool split among the common holders** — including the option-holders whose options accelerate on change of control, the ex-employees whose vested options were exercised into common, the founders' common, and any preferred that converted to common (having declined its preference) to participate at the common line?

The math is a cascade: preferred preferences come off the top; the residual flows to common; participating preferred may also participate in the residual; caps and conversion decisions are optimised at each preferred series to maximise that series' payout.

## The four preference structures

**1x non-participating preferred (founder-favourable baseline).** Each series gets *either* its 1x invested capital back *or* its pro-rata as-converted share of the exit proceeds — whichever is greater. The preferred cannot "double dip". At exit, each series computes both amounts and picks the larger; below a threshold the series takes the preference, above the threshold it converts and takes the pro-rata. The conversion decision is per-series and is done automatically by the certificate (the series "converts to common" for waterfall purposes when its pro-rata share exceeds its preference).

The threshold is the point where `1x preference = ownership% × (exit − sum of prior-series preferences taken)`. Below the threshold the preferred takes its 1x back and nothing more; between the threshold and infinity the preferred converts and takes its pro-rata share.

**1x participating preferred (investor-favourable, "double-dip").** Each series gets 1x invested capital back *and then* participates pro-rata with common in the residual as if it had converted. The preferred effectively double-dips: it gets its preference off the top *and* its ownership share of what remains. The founder-dilutive cost of participation is the preference dollars that come off the top and then are also included in the pro-rata calculation.

**1x capped participation (compromise structure).** Participating preferred with a cap on the total payout — usually expressed as "1x preference plus participation up to a 3x cap." Once the participating payout reaches 3x the invested capital, the series stops participating and behaves as if it were non-participating. In practice, at exit the series compares (1x + participation up to cap) against (pro-rata as-converted) and takes whichever is larger. Caps are typically 2x-3x.

**Participation with multiple preferences.** Non-1x preferences (e.g., 2x non-participating) are legal and were more common in the 2000-2010 era. They are also possible with participation (e.g., 2x participating). These are aggressive and unusual in modern venture rounds; they show up at Series-B and later in down-round bridges (mod-109) and as pay-to-play terms in distressed situations.

The NVCA reference for the certificate language sits in the Model Certificate of Incorporation, Article IV. The typical modern Series-A term sheet defaults to **1x non-participating**; the aggressive term sheet asks for **1x participating** with or without a cap; anything above 1x preference or uncapped participation is a warning sign about the round conditions.

## Seniority — senior vs. pari passu vs. subordinate

When multiple preferred series exist (Seed, Series A, Series B, etc.), the certificate specifies the *order* in which their preferences are paid at exit.

**Senior stack (later rounds senior to earlier).** The Series-B preference is paid first; then Series-A; then Seed; then common. Under this stack, if the exit is only large enough to cover Series-B's preference, Series-A and Seed get zero preference and only participate if they convert to common — which they generally will not, because there is nothing left for common. This is the modern default and is the "senior liquidation preferences" case most Series-A term sheets specify.

**Pari passu stack (all series equal).** All preferred series' preferences are paid *pro-rata among themselves* out of the exit proceeds. If aggregate preference exceeds available proceeds, each series takes its share of the available pool proportional to its preference amount. Pari passu is more founder-common friendly in a low exit scenario because early-round investors don't get zeroed out; it is less investor-B friendly because their preference sits alongside earlier investors', so they get less at low exit prices.

**Subordinate stack.** Rare and hostile — the *later* round's preference is subordinated to the earlier. Almost never happens at Series-B; can appear at recap / cramdown moments where earlier investors insist their preference stays intact even under the new money.

The seniority stack matters most at *low exit prices*. At a $200M exit for a company that raised $50M total, all preferences are covered and seniority is a rounding question. At a $30M exit for a company that raised $50M total, seniority determines *who gets zeroed out first*.

## Worked waterfall — 1x non-participating

Set up:

- **Cap table at exit** (fully-diluted):
  - Founders common: 8,000,000 shares (40%)
  - Employees common (exercised): 500,000 shares (2.5%)
  - Options outstanding (accelerate on change of control): 1,500,000 shares (7.5%) — treated as common at exit
  - Series Seed preferred: 2,000,000 shares (10%), 1x preference on $2M raised
  - Series A preferred: 3,000,000 shares (15%), 1x preference on $10M raised
  - Series B preferred: 5,000,000 shares (25%), 1x preference on $30M raised
  - Total FD: 20,000,000 shares
- **Preference stack:** all 1x non-participating, senior stack (B senior to A senior to Seed).
- **Total preference obligation:** $2M + $10M + $30M = $42M.

**Exit at $30M.** Below the aggregate preference. Waterfall:

- Series B claims $30M preference. Only $30M available. Series B takes all $30M. Series A, Seed, common: **zero**.
- Series A and Seed will not convert to common because pro-rata of $0 residual is still $0. They take their preference of $0 (a partial preference under a strict reading of the certificate — many certificates specify preferences are paid in order but capped at available proceeds).
- Founder / employee common: **$0**.
- Series B recovers 100% of principal. Series A and Seed recover 0%.

**Exit at $50M.** Above aggregate preference.

- First, compute conversion decisions per series. If Series B converts, it takes 25% × $50M = $12.5M. Its 1x preference is $30M. Non-participating: takes the larger, which is $30M preference. **B stays preferred.**
- If Series A converts, it takes 15% × ($50M − $30M) = 15% × $20M = $3M. Its 1x preference is $10M. Takes $10M preference. **A stays preferred.**
- If Seed converts, it takes 10% × ($50M − $40M) = 10% × $10M = $1M. Its 1x preference is $2M. Takes $2M preference. **Seed stays preferred.**
- Preferred total: $42M. Residual for common: $50M − $42M = $8M.
- Common line consists of founders (8M) + employees (500K) + options (1.5M) = 10M shares. Founders get 8M / 10M × $8M = **$6.4M**. Employees get **$400K**. Options exercise and net $6M × (options / common line) − strike-price paid: **$1.2M in intrinsic value**.

At $50M exit — 20% above the aggregate raised — the founders collectively get $6.4M for 40% ownership on a cap-table basis. Their share of the exit is $6.4M / $50M = 12.8%. The preferred stack extracted 84% of the exit and the option-holders got the residual.

**Exit at $200M.** Well above aggregate preference and the conversion thresholds.

- If Series B converts: 25% × $200M = $50M vs. 1x preference of $30M. **B converts.**
- If Series A converts: 15% × $200M = $30M vs. 1x preference of $10M. **A converts.**
- If Seed converts: 10% × $200M = $20M vs. 1x preference of $2M. **Seed converts.**
- All preferred converts to common. Exit distributes on a pure pro-rata basis. Founders get 40% × $200M = **$80M**. Employees $10M. Options ~$27M intrinsic. Series B $50M, A $30M, Seed $20M.

Notice the shape: below a threshold, the founder gets crushed. Above it, the founder is on the same distribution line as everyone else and the exit price scales cleanly. The threshold is where preferred conversion decisions flip. For this stack, the threshold is roughly the point where every preferred series' pro-rata exceeds its preference — which is somewhere between $100M and $150M for this cap table.

## Worked waterfall — 1x participating (the "double dip")

Same cap table. Same exit prices. Now all preferred is **1x participating** (no cap).

**Exit at $50M.**

- Preferred total off the top: $42M.
- Residual: $8M.
- But now preferred participates in the residual on an as-converted basis. Total shares participating: 10M common + 2M Seed + 3M A + 5M B = 20M.
- Preferred share of residual: 10M / 20M = 50%. So preferred takes another $4M from the residual, pro-rata among the series (B: 5M/10M × $4M = $2M; A: 3M/10M = $1.2M; Seed: 2M/10M = $800K).
- Common's share of residual: $8M − $4M = $4M. Founders take 8M / 10M × $4M = $3.2M.

Compare: under non-participating, the founder took $6.4M at a $50M exit. Under participating, the founder takes $3.2M. **Participating cost the founder half their exit at this price point.**

**Exit at $200M.**

- Preferred takes $42M off the top.
- Residual: $158M.
- Preferred share of residual pro-rata: 50% × $158M = $79M.
- Common share of residual: $79M.
- Founder: 8M / 10M × $79M = **$63.2M**.
- Preferred total: $42M off-top + $79M residual = $121M. Vs. under non-participating (all converted), preferred would have taken $100M ($200M × 50%). Participating extracted an additional $21M from common.

At the $200M exit under participating, the founder loses $80M − $63.2M = **$16.8M** to the participation right. That is a real cost of the participating structure even at large exits.

The participation right is why founders push hard for non-participating and investors sometimes push for participating in exchange for other concessions (higher pre-money, less pool). The negotiation math (mod-108) trades these dimensions against each other.

## Worked waterfall — capped participation

Same cap table. Series B: 1x participating with a 3x cap ($90M cap). Series A and Seed: 1x non-participating.

**Exit at $200M.**

- Series B: compute participating payout (with cap) vs. converted payout. Choose the larger.
  - Participating: $30M preference + 5M / 20M × ($200M − $42M) = $30M + $39.5M = $69.5M. Under the 3x cap ($90M), unclamped. Series B participating payout: **$69.5M** (cap not reached).
  - Converted: 5M / 20M × $200M = $50M.
  - Series B takes participating: **$69.5M**.
- Series A: non-participating. Compare 1x preference ($10M) vs. converted (15% × ($200M − $69.5M − Seed prefs computed next)). Iterate — this requires the residual to be defined, which requires other series' decisions... in practice the certificate specifies the calculation order.
- Simplifying: assume A and Seed both convert (their converted payouts exceed their preferences at this exit). Then residual after B: $200M − $69.5M = $130.5M. Distributed pro-rata among converted A + converted Seed + common = 3M + 2M + 10M = 15M shares. Founder: 8M / 15M × $130.5M = **$69.6M**.

Compare across structures at $200M for the founder:
- Non-participating: **$80M**
- 1x participating (no cap): **$63.2M**
- 1x participating with 3x cap on B only: **$69.6M**

The cap matters. Between capped and uncapped participation the founder recovers ~$6M at this exit price. At exit prices where the cap actually binds (higher exit, closer to 3x on the round), the cap matters much more.

**Exit at $500M.**

- Series B participating (capped at $90M = 3x on the $30M raise): $90M.
- Series A converted: 15% × ($500M − $90M) = 15% × $410M... but wait — under participating-with-cap, once B hits its cap it stops participating and behaves as converted. So we need to recompute: at what point does capped participation flip to converted-preferred?
- Series B: converted payout is 25% × $500M = $125M. Participating (capped) payout is $90M. **B converts** at the $500M exit (converted > capped-participating).
- Series A converted: 15% × $500M = $75M vs. 1x = $10M. A converts.
- Seed converted: 10% × $500M = $50M vs. 1x = $2M. Seed converts.
- All preferred converts. Founder: 40% × $500M = **$200M**. Clean pro-rata.

The capped-participation structure has a **flip point** at exit prices where the cap makes participating worse than converting. Above the flip, the structure behaves like non-participating. Below the flip (but above the aggregate preference), participation extracts value from common. The founder's job in negotiation is to make sure the cap is low enough that the flip happens at a plausible exit range.

## Senior vs. pari passu on the same cap table

Take the earlier cap table. Aggregate preference $42M. Now compare a **senior stack** vs. **pari passu**.

**Exit at $30M.**

- Senior stack: Series B takes all $30M. Series A and Seed take $0. Common: $0.
- Pari passu: all $30M distributed pro-rata among the $42M of preferences. B: $30M × 30/42 = $21.4M. A: $30M × 10/42 = $7.1M. Seed: $30M × 2/42 = $1.4M. Common: $0.

Neither is good for common, but the earlier investors take something under pari passu. This is why pari passu is sometimes preferred by early-round holders and pushed for in Series-B negotiations by Series-A investors — it prevents the later round from zeroing them out.

At larger exits the difference disappears (all preferences fully covered under both structures), so the seniority-vs.-pari-passu question is really a question about the low-exit tail risk.

## Deemed liquidation events — what triggers the waterfall

The certificate defines a **deemed liquidation event** — the trigger that requires the waterfall to run. Standard definition (following NVCA Model Certificate): any of

- A merger or consolidation where the company is not the surviving entity (or is surviving but stockholders receive a change of >50% ownership).
- A sale of all or substantially all of the company's assets.
- Certain qualifying licensing transactions (unusual but seen in life sciences).

A **qualified financing** — a large priced round — is typically not a deemed liquidation event; it just adds a preference series to the stack. IPOs generally trigger mandatory conversion of preferred to common (not a waterfall).

A related but separate concept: **redemption rights**. Some preferred series have a right to require the company to repurchase them after a defined period (typically 5-7 years) at 1x + accrued dividends. Redemption is rare in modern venture (Fenwick / WSGR data typically shows single-digit-percent incidence in recent years) and effectively behaves like a debt-like preference conversion at maturity. When it does appear it interacts with the waterfall at the redemption date, not at exit.

<!-- needs-research: cite current Fenwick and WSGR quarterly terms surveys on the incidence of redemption rights in venture rounds; the specific incidence percentages vary by quarter. -->

## Anti-dilution overlays

The waterfall math assumes no anti-dilution recalculation. If a series has broad-based weighted-average anti-dilution (the most common modern default) and there has been a down round between issuance and exit, the series' conversion ratio has been adjusted upward — the series converts to more common than its original as-converted share count would suggest. Full-ratchet is even more aggressive but rare.

Anti-dilution is fully treated in mod-108 (term sheets). For waterfall purposes, the CFO's job at exit is to apply the *actual conversion ratio* (which lives in the certificate as amended and in the cap-table software's conversion columns) to compute the correct as-converted share count for each preferred series, then run the waterfall against those adjusted numbers.

## The "sale above the last round" trap

Return to the opening claim: a sale price above the last round's post-money valuation is not always a founder win.

Consider a company at Series-B with $30M pre-money on a $10M raise (post-money $40M) and, before that, a Series-A that raised $10M and a Seed that raised $2M. Aggregate preference: $42M. Post-money value at last round: $40M.

**"Sale above the last round"** at $45M. Aggregate preference $42M. Common residual: $3M. Founder at 40% ownership: 8M / 10M × $3M = $2.4M. **The company sold for more than the last round's post-money and the founder got $2.4M for 40% ownership.** The headline reads "successful sale"; the founder's actual take is not.

The threshold at which the founder starts to feel the sale price as their headline percent is much higher than the last round's post-money. The rule of thumb: **the founder's participation only starts to look like their cap-table percent above 2-3x the aggregate preference stack**. Below that, the preferred stack is extracting most of the value and the founder gets a small residual.

This is the shape that surprises founders and the reason exit-scenario waterfall analysis belongs on the CFO's regular strategic-planning calendar, not just at the moment of exit. Board discussions of "should we take this offer" should be conducted against the waterfall, not against the headline sale price.

## The mechanics of running the waterfall in practice

A defensible waterfall is a spreadsheet or a Carta / Pulley scenario with:

- **Per-series inputs:** shares outstanding, preference per share, participation flag, participation cap, seniority rank, conversion ratio (from cert as amended).
- **Common inputs:** shares outstanding (including exercised options), unexercised options with strike price (accelerated on CoC per the plan and grant terms).
- **Exit consideration input:** one cell, in dollars, that the model iterates against.
- **Per-series conversion decision:** compute (preference + participation if applicable, subject to cap) vs. (pro-rata as-converted); take the larger; label the choice.
- **Residual distribution:** what remains after each preferred series has been paid, distributed on the common line and to any preferred that converted.
- **Per-holder payout table:** who gets what. Founders separately (each), employee groups aggregated, VC investors separately, option-holders as a group.
- **Sensitivity chart:** founder payout, VC payout, employee payout as a function of exit price across a range ($10M to $500M or so, log scale).

The sensitivity chart is the artefact for board conversations. It shows visually where the "flip points" are — the exit prices at which each preferred series converts, the price at which common becomes materially positive, and the price above which the founder's payout scales linearly with exit price.

## Summary

- The cap table shows who owns the company. The waterfall shows who gets *paid* when it is sold. A sale above the last round's valuation is not always a founder win.
- The four preference structures — 1x non-participating (founder-favourable baseline), 1x participating (double-dip), capped participation (compromise), and above-1x preferences (aggressive, unusual) — produce dramatically different waterfalls at the same exit price.
- Seniority (senior vs. pari passu vs. subordinate) matters most at low exit prices; at high exits all preferences convert and the stack becomes a pro-rata question.
- The certificate of incorporation is the instrument — specifically the certificate-of-designation sections for each preferred series. Waterfall math against a term sheet without pulling the actual cert is guessing.
- The conversion decision per series (take preference vs. take pro-rata) is the mechanic that determines when preferred behaves as debt vs. equity at the given exit. Participation caps create flip points that shift the shape.
- The rule-of-thumb: the founder's participation looks like their cap-table percent only above 2-3x the aggregate preference stack. Below that, most exits are absorbed by the preferred stack.
- The waterfall belongs on the CFO's regular strategic-planning calendar — as a sensitivity chart across exit prices — not just at the moment of exit.

Chapter 5 turns to 409A: the fair-market-value determination that governs option strike prices, the appraisal cadence, and the safe-harbor rules that a startup must live under.
