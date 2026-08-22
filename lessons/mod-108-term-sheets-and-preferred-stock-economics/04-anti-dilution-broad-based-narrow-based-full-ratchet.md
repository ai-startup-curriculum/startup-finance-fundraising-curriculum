# Anti-Dilution Provisions — Broad-Based, Narrow-Based, and Full Ratchet

## Why this matters

Anti-dilution is the clause that adjusts the preferred's conversion price *downward* if the company later issues equity at a lower price per share than the preferred paid. The lower conversion price means the preferred converts into *more* common shares at exit or on a voluntary conversion, which mechanically dilutes the common (founders and employees) in favour of the preferred.

Three specific things make the clause matter to the CFO:

- **The clause fires without a shareholder vote.** Anti-dilution is a self-executing formula in the charter. The moment a down round closes at a lower price, the earlier preferred's conversion price recalculates automatically. There is no negotiation window at the trigger event; the negotiation is at the term-sheet stage before the down round is on the table.
- **The formula choice moves cap-table percentages materially.** The three formulae — broad-based weighted-average, narrow-based weighted-average, full ratchet — produce very different post-down-round cap tables. Broad-based is the market-standard, moderate protection; full ratchet is punitive and can transfer 10-20 percentage points of the founder's ownership to the earlier preferred in one recalculation.
- **The clause interacts with pay-to-play.** Pay-to-play is an anti-dilution modifier that requires the preferred to invest their pro-rata in the down round *in order to keep* their anti-dilution protection (and sometimes their preference and voting rights). It changes the incentive structure of the down round and can be either founder-favourable (by forcing sitting-out investors to convert to common) or investor-favourable (by giving participating investors both anti-dilution protection *and* a preference bump), depending on how it's drafted.

This chapter walks the three formulae, the recalculation mechanics, the pay-to-play interaction, and what the CFO produces before signing.

## The three formulae

**Broad-based weighted-average.** The market-standard formula at Series-A in the US. The new conversion price is a weighted average of the old conversion price and the new (lower) issue price, weighted by the pre-issuance broad-based fully-diluted share count and the down-round issue size.

Formula (the NVCA model form):

$$\text{NCP} = \text{OCP} \times \frac{\text{OS} + \text{IS}}{\text{OS} + \text{DS}}$$

where:
- **NCP** = new conversion price of the earlier preferred series.
- **OCP** = old conversion price (typically the original issue price of the earlier series).
- **OS** = "outstanding shares" — the broad-based fully-diluted share count immediately before the down round (common + all preferred on an as-converted basis + all outstanding options + unissued option pool + all outstanding warrants and convertibles on an as-converted basis).
- **IS** = "shares that would have been issued" at the *old* conversion price for the money raised in the down round = `down-round investment / OCP`.
- **DS** = shares actually issued in the down round (at the new lower price) = `down-round investment / down-round price`.

The "broad-based" in the name refers to the OS denominator including everything on the cap table on a broad basis — common, preferred as-converted, options and warrants and reservations, unissued pool. The broader the base, the smaller the recalculation adjustment, hence "broad-based" is founder-favourable within the weighted-average family.

**Narrow-based weighted-average.** Same formula, but OS excludes the option pool (and sometimes excludes warrants or other reserved-but-unissued securities). Some formulations restrict OS to outstanding common + outstanding preferred as-converted only.

The narrower the base, the larger the recalculation adjustment, hence "narrow-based" produces harsher protection than broad-based. The difference in the down-round outcome depends on the ratio of pool-and-reserved shares to outstanding shares — for a typical Series A company with a 15-20% option pool, narrow-based produces a materially larger conversion-price reduction than broad-based.

**Full ratchet.** The new conversion price is simply set to the down-round price:

$$\text{NCP} = \text{down-round price per share}$$

No weighting. If the earlier preferred was issued at $5.00 and the down round prices at $2.00, the earlier preferred's conversion price becomes $2.00. It converts into 2.5x the common it would otherwise have converted into, regardless of how small the down round was.

Full ratchet is the most punitive of the three, and its punitiveness scales with the size of the down-round price drop. A $500K down round at half the earlier price does the same thing to the earlier preferred's conversion price under full ratchet as a $50M down round at half the earlier price. This makes it particularly dangerous — a token-sized bridge at a low price can trigger the ratchet and materially dilute the founder.

## Worked recalculation — the same down round under three formulae

Setup:

- **Prior state.** Series A raised $10M at $5.00 per share (2,000,000 shares issued). Company has: 8,000,000 common; 1,500,000 options granted + 500,000 unissued pool (2,000,000 total options); 2,000,000 Series A. Broad-based FD = 12,000,000. Series A conversion price: $5.00.
- **Down round.** Series B raises $10M at $2.50 per share (4,000,000 shares issued). Post-Series-B FD (before anti-dilution adjustment): 16,000,000.

**Broad-based weighted-average.**

- OS = 12,000,000. IS = $10M / $5.00 = 2,000,000. DS = $10M / $2.50 = 4,000,000.
- NCP = $5.00 × (12,000,000 + 2,000,000) / (12,000,000 + 4,000,000) = $5.00 × 14/16 = $4.375.
- Series A's new effective per-share entitlement: at conversion, each Series A share converts into ($5.00 / $4.375) = 1.1429 common shares. Series A now converts into 2,285,714 common (up from 2,000,000).
- Additional common issued to Series A on conversion: 285,714 shares. Founder / other-common dilution: 285,714 / (12,000,000 + 4,000,000 + 285,714) ≈ 1.75% of post-conversion FD.

**Narrow-based weighted-average** (defining OS to exclude the option pool):

- OS = 10,000,000 (12M minus 2M options). IS = 2,000,000. DS = 4,000,000.
- NCP = $5.00 × (10,000,000 + 2,000,000) / (10,000,000 + 4,000,000) = $5.00 × 12/14 = $4.286.
- Series A converts into $5.00 / $4.286 × 2,000,000 = 2,333,333 common.
- Additional common: 333,333 shares. Common dilution: ~2.05% of post-conversion FD.

**Full ratchet.**

- NCP = $2.50 (the down-round price).
- Series A converts into $5.00 / $2.50 × 2,000,000 = 4,000,000 common. Series A's converted share count *doubles*.
- Additional common issued to Series A on conversion: 2,000,000 shares. Common dilution: 2,000,000 / (12,000,000 + 4,000,000 + 2,000,000) = 11.1% of post-conversion FD.

Read: broad-based costs ~1.75% of common dilution; narrow-based costs ~2.05%; full ratchet costs 11.1%. Full ratchet delivers roughly 5-6x the dilution of broad-based on this specific example, and the multiplier grows if the down-round price drop is larger.

## The pay-to-play modifier

Pay-to-play is a clause that conditions the preferred's anti-dilution protection (and sometimes preference, protective provisions, and board seats) on the preferred participating in the down round pro-rata to their existing ownership.

Two common variants:

**Soft pay-to-play (loss of anti-dilution only).** A preferred holder who does not invest its pro-rata in the down round loses its anti-dilution protection for that round. Its conversion price is *not* adjusted; the round is completed and the preferred's ownership dilutes on a per-share basis without protection. This is common as a "carrot-plus-stick" — participating investors get their anti-dilution kick, non-participating investors take the dilution.

**Hard pay-to-play (forced conversion to common).** A preferred holder who does not invest its pro-rata in the down round has its preferred shares converted to common — losing not just anti-dilution but also the preference, the anti-dilution formula going forward, the protective-provision votes, and any board seat. This is a much more aggressive tool used in recapitalisations and stressed-round scenarios to force existing investors to either write another cheque or accept full downside conversion.

**A shadow-preferred variant.** In some pay-to-play drafts, non-participating preferred is converted to a "shadow" or "junior" preferred class that retains some rights (typically the preference at the original per-share cost) but loses others (anti-dilution, protective provisions). This is a compromise structure that appears in some late-stage recapitalisations.

The pay-to-play mechanic combined with a preferred anti-dilution formula and a bumped-multiple preference on the *new* investment creates the classic "wash-out" or "recap" structure: existing preferred that participates gets a bumped preference plus anti-dilution kick; existing preferred that doesn't participate gets its shares converted to common; new investment sits on top with a large preference stack and the majority of the going-forward cap table. This is [`mod-109`](../mod-109-runway-management-and-bridge-financing/) territory in detail; the term-sheet stage question is only "is there a pay-to-play clause, is it soft or hard, and what specifically does it condition."

## What triggers the anti-dilution clause

Not every subsequent equity issuance triggers anti-dilution. The NVCA form carves out a defined set of "excluded issuances" that do not trigger the recalculation:

- **Options and restricted stock** issued under the equity incentive plan up to a defined pool size, at fair market value.
- **Shares issued on conversion of the preferred** itself.
- **Shares issued in connection with acquisitions** approved by the board.
- **Shares issued to strategic partners, lessors, lenders, or vendors** — typically in defined amounts.
- **Warrants issued in connection with debt** or in specific board-approved circumstances.
- **Shares issued in a public offering** above a defined price threshold.
- **Shares issued in a firm-commitment underwritten IPO** at a specified minimum price.

Deviations from the NVCA excluded-issuances list are a common negotiation battleground. An aggressive term sheet may narrow the excluded-issuances list (fewer carve-outs, so more issuances trigger anti-dilution). A founder-favourable term sheet may broaden it (more carve-outs).

The trigger is a *lower* per-share issue price than the earlier preferred's conversion price. An issuance *at* the same price or *above* the conversion price does not trigger. A partial-price down round (a Series B at a slightly-lower price per share than Series A but where the pre-money is much higher because the company has grown) still triggers on the per-share comparison, not the pre-money comparison.

## Multiple down rounds — the ratchet-of-ratchets pattern

If the company does a second down round, the earlier preferred's anti-dilution recalculates again against the *new* (already-adjusted) conversion price. Multiple down rounds compound the dilution effect on the common under any of the three formulae; full ratchet compounds most aggressively because each recalculation resets to the newest lowest price without weighting.

Worked example: same Series A above, followed by Series B at $2.50, then Series C at $1.00.

- After Series B (broad-based): Series A conversion price = $4.375.
- Series C: OS at the time of Series C includes the Series B shares as-converted (4,000,000), so broad OS ≈ 20,000,000; IS at $4.375 for a $5M Series C = $5M / $4.375 = 1,142,857; DS at $1.00 = 5,000,000. NCP = $4.375 × (20,000,000 + 1,142,857) / (20,000,000 + 5,000,000) = $4.375 × 21.14 / 25 = $3.70.
- Series A now converts at $3.70, into $5.00 / $3.70 × 2,000,000 = 2,702,703 common. Additional common vs. original: 702,703 shares.

Under full ratchet after the same Series C, Series A conversion price = $1.00 (the Series C price), converting into $5.00 / $1.00 × 2,000,000 = 10,000,000 common. Additional common vs. original: 8,000,000 shares — which now exceeds the founder's original 8,000,000 common holding. The founder is diluted to less than 50% of the pre-anti-dilution common on a full-ratchet second down round even without adding the Series B and Series C new shares.

The compounding is the reason full ratchet is treated as a tier-4 "unusual" clause even at Series-A: a single Series A signing with full ratchet exposes the founder to a compounding cap-table risk that is almost impossible to model against real down-round scenarios.

## What the CFO does at the term-sheet stage

Before accepting the anti-dilution clause, the CFO should:

- **Identify the formula.** Broad-based weighted-average is tier-1 market. Narrow-based is tier-3 aggressive. Full ratchet is tier-4 unusual and should be refused. Any variant beyond the three (e.g., "narrow-based but with the pool included in OS") should be normalised to one of the three for classification.
- **Identify the excluded-issuances list.** The NVCA-standard list is tier-1. Deviations that narrow the list are tier-3. Deviations that broaden the list are tier-1 (founder-favourable) but rare.
- **Identify pay-to-play.** Presence at Series-A is unusual; presence at later rounds is more common in stressed markets. Soft pay-to-play (loss of anti-dilution only) is a milder tier-3 clause; hard pay-to-play (forced conversion) is tier-4.
- **Model a defined down-round scenario.** Take a hypothetical Series B at 50% of the current price, run the recalculation under the three formulae, and quantify the common's dilution. This is the founder-facing memo attached to the term-sheet analysis. It makes the abstract formula choice concrete.
- **Cross-check against the current-quarter data.** Fenwick and Wilson Sonsini publish anti-dilution formula frequencies quarterly. Broad-based should be near-universal in a normal market (95%+). Narrow-based should appear in the low single digits. Full ratchet should be near zero. Deviations in the current-quarter data signal a market drift the CFO should account for. Chapter 9.
- **Coordinate with counsel on the excluded-issuances drafting.** The list is drafted in the charter and requires legal precision. The CFO's job is to identify the specific carve-outs that matter for the business (e.g., a specific known bridge lender arrangement that would trigger a narrowed list) and to hand counsel the specific asks.

## The founder-facing memo

A specific memo the CFO produces for the CEO and board when the received term sheet has anything other than a tier-1 broad-based weighted-average clause with the NVCA-standard exclusions:

- **Bottom-line.** "The received term sheet has [narrow-based weighted-average / full ratchet / pay-to-play modifier]. Under a defined 50% down-round scenario in Year 2, this costs the founder [X] percentage points of ownership vs. the broad-based baseline."
- **Recalculation table.** For a defined down-round scenario, the recalculated conversion price, the incremental Series A converted-share count, and the incremental founder dilution under each of the three formulae plus the proposed clause.
- **Sensitivity table.** How the incremental cost scales with the down-round size (25% price drop, 50%, 75%) and the down-round investment amount ($5M, $10M, $20M).
- **Market-context anchor.** The current-quarter frequency of the proposed formula from Fenwick / Wilson Sonsini / Carta.
- **Negotiation ask.** The specific counter — typically "revise to broad-based weighted-average with the NVCA-standard excluded-issuances list."
- **Fall-back position.** If the lead insists on narrow-based, what parameters bring it closer to broad-based (specifically, an OS definition that includes the pool but excludes some warrants — the "middle-ground" formulation that appears in some late-stage rounds).

## Common founder traps

- **Not distinguishing the three formulae by name.** "Anti-dilution protection" without specifying formula is inadequate. The three formulae are 5-10x apart in impact.
- **Signing full ratchet on the assumption that "we won't do a down round."** Companies plan not to; they still do. The clause should be assumed to fire.
- **Missing the pay-to-play modifier hidden in the charter.** Pay-to-play mechanics sometimes appear in the charter's separate "conversion" or "protective provisions" sections rather than in the anti-dilution clause itself. Read the whole charter, not just the labelled clause.
- **Accepting a narrowed excluded-issuances list without noticing.** A carve-out that says "excluded issuances shall not include shares issued to lenders, lessors, or strategic partners" narrows the founder-favourable NVCA list and can trigger the ratchet on issuances the CFO wouldn't have considered dilutive.
- **Not modelling the compounding effect of multiple down rounds.** Each subsequent down round re-recalculates. Compounding matters. A single-down-round model understates full-ratchet risk.
- **Confusing anti-dilution with liquidation preference.** Anti-dilution adjusts *conversion* price. Liquidation preference is a separate dollar-amount claim on exit proceeds. Both change on a Series B, but through different clauses in the charter.
- **Assuming the option-pool top-up at the next round is anti-dilution-neutral.** Options issued under the plan at fair-market-value are typically an excluded issuance, but option grants below FMV or in unusual circumstances can trigger. Coordinate with counsel.

## What good looks like

A CFO who has this material installed:

- Identifies the anti-dilution formula in every term sheet at first read and classifies it against the market-standard broad-based weighted-average baseline.
- Reads the excluded-issuances list against the NVCA-standard and identifies narrowing or broadening.
- Identifies pay-to-play mechanics wherever they hide in the term sheet or charter.
- Models a defined down-round scenario and quantifies the incremental founder dilution under each formula.
- References current-quarter Fenwick / Wilson Sonsini / Carta data on formula incidence.
- Coordinates the drafting of the excluded-issuances list with counsel to address business-specific carve-outs (bridge lenders, strategic partners, key vendors).
- Refuses full ratchet at Series-A without a specific and documented reason.
- Communicates the anti-dilution cost to the CEO and board in dollar-and-percentage terms tied to a specific scenario, not as an abstract clause classification.

## Summary

- Anti-dilution adjusts the preferred conversion price downward when the company issues new equity at a lower price than the preferred paid. The clause is self-executing at the trigger event; negotiation happens at the term-sheet stage.
- Three formulae: broad-based weighted-average (market-standard, moderate protection), narrow-based weighted-average (harsher), full ratchet (rare and punitive, ratchets to the new price without weighting).
- The formula difference produces 5-10x variation in the down-round dilution outcome; full ratchet can transfer 10-20 percentage points of founder ownership on a single 50% down-round.
- The excluded-issuances list defines what issuances do not trigger anti-dilution. The NVCA-standard list is market; deviations that narrow the list are aggressive.
- Pay-to-play conditions the anti-dilution protection on participating in the down round pro-rata; soft variants strip anti-dilution only, hard variants force conversion to common. Rare at Series-A, more common in later stressed rounds.
- Multiple down rounds compound the anti-dilution effect. Full ratchet compounds most aggressively.
- The CFO's output before signing: identify the formula and excluded-issuances list, model a defined down-round scenario, quantify the founder-cost per formula, and produce the counter-ask with the market-context anchor.

Chapter 5 turns to pro-rata rights — the right of existing investors to invest their proportional share of the next round to maintain their ownership — and to the specific compression math that shows how much of the next round is absorbed by existing pro-rata before the new lead's allocation is set.
