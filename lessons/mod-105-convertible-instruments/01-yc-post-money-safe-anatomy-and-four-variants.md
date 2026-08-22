# The YC Post-Money SAFE — Anatomy and the Four Variants

## Why this matters

A SAFE — Simple Agreement for Future Equity — is the single most common seed-round instrument in the United States and the one most founders sign without reading. YC published the original in 2013 and rewrote it in September 2018 as the **post-money** SAFE. Almost every SAFE closed since is one of four YC post-money variants (valuation cap only; discount only; MFN only; cap + discount) or a lightly-edited derivative. The old pre-money legacy variant still lives on real cap tables from that era — chapter 2 handles it — but every new instrument you author today should be a post-money SAFE, and every founder you support has to understand what it does at conversion.

The core reason the 2018 rewrite matters is not that the paperwork got shorter. It is that the post-money SAFE **fixes the SAFE holder's ownership at close** as a percentage of the *post-money* company, meaning any subsequent SAFE, any option-pool top-up, or any priced-round dilution comes out of the founder alone, not out of the SAFE holder. That property is deliberately designed to give the SAFE holder an "investor-honest" number and to give the founder a "you know what you sold" number. The trade is that stacked-SAFE cap-table modelling stops being additive — you cannot just sum SAFE percentages — and starts requiring the iterative solve introduced in [`mod-104`](../mod-104-cap-tables-and-equity-compensation/01-cap-table-anatomy-issued-outstanding-fully-diluted.md).

This chapter installs the anatomy. Chapter 2 contrasts the pre-money legacy behaviour. Chapter 4 stacks multiple instruments together into the pro-forma Series-A calculation the CFO actually has to produce.

## What a SAFE is (and is not)

A SAFE is a **contract**, not stock and not debt. Its economic content is a single promise: at the next equity financing that meets a defined threshold, the SAFE converts into shares of the same class of preferred stock as the new investors buy, at a price per share determined by the cap and/or discount terms baked into the SAFE.

Structurally that means a SAFE has none of the mechanics of the two other instruments a founder considers at the seed stage:

- It is **not equity** at the time it is signed. There is no share issued, no vote, no dividend, no liquidation preference, no board seat.
- It is **not debt**. There is no principal to repay, no interest rate, no maturity date, no default event. If the company never raises a priced round, a SAFE holder never becomes a shareholder and never gets money back (subject only to the equity-financing / liquidity / dissolution triggers baked into the form).
- It is **not a security exempt from Reg D just because it says "simple" in the title**. Every SAFE closing is a private placement subject to the exemptions in [chapter 6](06-reg-d-exemptions-504-506b-506c-and-form-d.md). A Form D filing is required (with a limited exception for very small closings under state-only exemptions).

The trigger events that produce a payout for the SAFE holder are three, all defined inside the form itself:

- An **equity financing** (a priced preferred round) — the SAFE converts into preferred shares.
- A **liquidity event** (an acquisition of the company, an IPO, or in some drafts a change-of-control) — the SAFE holder elects between two computed payouts.
- A **dissolution event** — the SAFE holder is paid out of the remaining assets ahead of common stockholders but behind creditors.

The rest of this chapter is about the mechanics of the equity-financing conversion, which is the trigger that fires in the overwhelming majority of cases.

## The two share-price mechanics — cap and discount

A SAFE's economic content is delivered through one or both of two mechanics that determine the price per share at which the SAFE converts.

**Discount.** A discount is a fixed percentage off the priced-round price-per-share, typically 15-25% (20% is the modal number in the current-vintage YC templates and in most VC seed programmes). At a $2.00 Series-A price and a 20% discount, the SAFE holder buys shares at $1.60. On a $500K SAFE, that's `$500,000 / $1.60 = 312,500` shares versus the `$500,000 / $2.00 = 250,000` shares a new investor buys with the same cash. The 62,500-share delta is the discount payout.

**Valuation cap.** A cap is a maximum pre-money (in the legacy SAFE) or post-money (in the post-money SAFE) valuation at which the SAFE converts. The SAFE's effective per-share price is `cap / applicable-fully-diluted-share-count`, and the SAFE converts at the *lower* of that price or the priced-round price. If the priced round is done above the cap, the cap controls; if the priced round is done below the cap, the priced-round price controls (subject to the discount, if any).

The cap and the discount interact:

- **Cap only.** SAFE converts at `min(priced-round price, cap-implied price)`.
- **Discount only.** SAFE converts at `priced-round price × (1 - discount)`.
- **Cap + discount.** SAFE converts at the *lower* of the cap-implied price and the discounted priced-round price — whichever gives the SAFE holder the better (lower) price. This is the "MFN over itself" property: the holder gets whichever mechanic is more favourable.
- **MFN only.** SAFE has neither a cap nor a discount at signing. Instead it contains a clause: if the company later issues a SAFE with a cap or discount, the earlier SAFE amends itself to adopt those terms. This variant is the topic of [chapter 5](05-side-letters-and-mfn-amendments.md); the mechanics of MFN cascades merit their own chapter.

## The post-money reframe — what changed in 2018

The pre-money legacy SAFE (2013 vintage) defined its cap as a **pre-money** valuation. The post-money SAFE redefines the cap as a **post-money** valuation, where "post-money" refers specifically to the post-money capitalisation *after all SAFEs and convertible notes have converted but before the new priced-round money has been added*. That reframing changes the arithmetic of the SAFE holder's ownership in a way that has cap-table consequences at every stage:

- Under the **pre-money** SAFE, the SAFE holder's ownership percentage was not knowable at signing because it depended on how many other SAFEs would be added later and how the pool would be sized at the priced round. All SAFEs converted against the same pre-money denominator and their percentages diluted one another.
- Under the **post-money** SAFE, the SAFE holder's ownership percentage *is* knowable at signing: `investment / post-money cap = % of post-conversion company (before new-money and before post-conversion option-pool top-up)`. That percentage does not change if another SAFE is added later; the new SAFE creates its own additional line of shares, and the pool of shares the first SAFE holds is preserved on a post-money basis.

The trade the post-money reframe makes:

- **The SAFE holder** gets a stable, predictable ownership number at signing. This is why the post-money SAFE is popular with investors: they can quote "I own 5% of the company post-conversion" at the moment of signing and know that number will hold.
- **The founder** bears the entire cost of every subsequent SAFE, of every option-pool top-up before the priced round, and of the priced-round dilution *outside* the SAFE holders' fixed slice. The pre-money SAFE spread these costs across all pre-money holders including earlier SAFE holders; the post-money SAFE concentrates them on the founder.

The mechanical consequence: stacked-SAFE conversion under the post-money model is not additive. If you close a $1M post-money SAFE at a $10M post-money cap and follow it with another $1M post-money SAFE at a $10M post-money cap, the two holders each end up owning 10% of the post-conversion company. Together they own 20%. The founder ownership is `100% - 20% = 80%` of a company whose total FD grew from `100/100` to `100/80` — the founder's absolute FD shares are unchanged, but their percentage falls from the pre-first-SAFE 100% to 80%. If a *third* $1M post-money SAFE at $10M cap arrives, the two earlier SAFE holders still own 10% each (unchanged — that's the point) and the new SAFE holder also owns 10%. Founder falls to 70%. Every additional SAFE adds its ownership percentage on top; each addition dilutes only the founder.

Contrast the pre-money legacy behaviour (chapter 2 in detail): under the pre-money SAFE, when the second SAFE is added, the *first* SAFE's implied ownership percentage falls because the two SAFEs share a pre-money base that now has to accommodate both. Under the post-money SAFE it doesn't — but the founder eats the entire second SAFE's dilution alone.

That single design change is why "the SAFE holder ownership is fixed at close" is the load-bearing property of the post-money SAFE, and why every downstream cap-table modelling exercise has to treat the post-money mechanic differently.

## The four YC post-money variants

YC publishes the current post-money SAFEs as four separate signed forms on its site (see [`resources.md`](resources.md)). Each is a full, standalone document — you pick one and use it; you do not mix-and-match clauses across the four (except through the MFN mechanic itself, which is intended to promote a later-issued SAFE's better terms into an earlier SAFE).

**Variant 1 — Valuation Cap, no Discount.** The most common variant. The SAFE has a specific dollar post-money cap (e.g., $10,000,000) and no discount clause. At the priced round the SAFE converts at the lower of the priced-round price and the cap-implied price.

- Founder framing: "You bought at a $10M ceiling. If the priced round is at $12M pre-money, you get the ceiling. If it is at $6M pre-money, you convert at the priced-round price because that's better for us and it's what an unrelated new investor would pay."
- The dominant risk to the founder is signing a cap that turns out to be a hard ceiling on the next priced round's pre-money because the SAFE holders will fight to keep their conversion economics.

**Variant 2 — Discount, no Valuation Cap.** The SAFE has a discount percentage (e.g., 20%) and no cap. At the priced round the SAFE converts at `priced-round price × (1 - discount)`.

- Founder framing: "You get a 20% break on whatever the next round prices at, and the upside is uncapped." This variant is friendly to founders who genuinely have no idea what their next-round valuation will be and want the SAFE holder to share the upside.
- The dominant risk to the founder is that a very-high-price priced round transfers a lot of value to the SAFE holder if the founder had not intended the SAFE to participate that far up the curve.

**Variant 3 — MFN, no Valuation Cap, no Discount.** The SAFE has neither a cap nor a discount at signing. Instead it contains an MFN clause: if the company later issues any SAFE (or SAFE-like instrument) to another investor before the priced round, the earlier MFN-only SAFE holder can elect to adopt the terms of that later instrument.

- Founder framing: "You get whatever the best next-SAFE gets." This variant is common for very-early "friends and family" money where a specific cap has not been agreed and the parties want to pin the terms to whatever a later, more-sophisticated investor negotiates.
- The dominant risk to the founder is losing control of the ceiling: the MFN holder inherits every subsequent cap and discount, so a later-signed 2% discount can turn a founder-favourable no-cap-no-discount MFN into a materially more expensive instrument. Chapter 5 walks the MFN cascade in detail.

**Variant 4 — Valuation Cap and Discount.** The SAFE has both a cap and a discount. At the priced round the SAFE holder gets the conversion price that is more favourable to them — i.e., the lower of the cap-implied price and the discounted priced-round price.

- Founder framing: "You have a ceiling and a discount, whichever is better for you." This is the maximum-flexibility variant for the SAFE holder and, correspondingly, the most-generous-to-the-holder variant for the founder to sign.
- The dominant risk to the founder is that this variant is often signed on the assumption that "the discount is the one that will trigger" (because the founder assumes the priced round will happen below the cap) when in practice the priced round happens above the cap and both mechanics collide to produce the most generous outcome for the holder.

All four variants are otherwise identical in the rest of the document — the definitions of equity financing, liquidity event, dissolution, pro-rata rights (or absence thereof), representations, and governing law are the same. The difference is only in the pricing mechanic.

## The conversion math — worked example, Variant 1 (cap only)

Setup:

- SAFE: $1,000,000 investment, $10,000,000 post-money cap, no discount.
- Priced round: Series-A closing at $10,000,000 raised on a $30,000,000 pre-money / $40,000,000 post-money valuation.
- Priced-round pre-money fully-diluted share count (before SAFE conversion, before pool top-up): 10,000,000 shares.
- Post-close target option pool: 10% of post-money (pre-money-shuffle placement per [`mod-104`](../mod-104-cap-tables-and-equity-compensation/02-pre-vs-post-money-math-and-the-option-pool-shuffle.md)).

**Step 1. Compute the priced-round price per share.**

- Priced-round price per share = `pre-money valuation / pre-money fully-diluted share count (post-shuffle, post-SAFE-conversion)`.
- This is circular because the SAFE conversion depends on the priced-round price and the priced-round price depends on the SAFE-converted share count. Solve iteratively (spreadsheets handle it natively; solve analytically below).

**Step 2. Compute the SAFE-implied price per share.**

- Post-money cap = $10,000,000. Post-money capitalisation = pre-priced-round fully-diluted share count post-SAFE-conversion, post-pool-top-up.
- The YC form defines the "SAFE price" as `post-money cap / company-capitalisation`, where "company capitalisation" is defined in the form to include all outstanding common, all outstanding options plus the unissued pool, and all converted SAFEs but *not* the new-money-issued preferred shares.
- If the founder + prior common + granted options + unissued pool + (any earlier SAFEs converted) sum to a known number, and this SAFE's share count is what we're solving for, the SAFE price is `$10M / (that known number + this SAFE's share count)`. Solve.

**Step 3. Choose the lower of the two prices.**

- If the priced-round price is higher than the SAFE-implied price, the cap controls. The SAFE converts at the SAFE-implied price.
- If the priced-round price is lower than the SAFE-implied price, the priced-round price controls (there is no cap benefit — the SAFE holder converts as if they had participated in the priced round at the priced-round price with no discount).

**Concrete numbers for the example above.** Assume just one SAFE (this one) and no earlier convertibles. Pre-priced-round FD ex-SAFE = 10,000,000 shares. Priced round is $10M on $30M pre.

- Post-money cap SAFE-implied "SAFE price" is `$10,000,000 / (10,000,000 + SAFE shares)`. The SAFE holder invests $1,000,000 at the SAFE price, so SAFE shares = `$1,000,000 / SAFE price`.
- Substitute: `SAFE price = $10,000,000 / (10,000,000 + $1,000,000 / SAFE price)`, i.e. `SAFE price × (10,000,000 + $1,000,000 / SAFE price) = $10,000,000`, i.e. `10,000,000 × SAFE price + $1,000,000 = $10,000,000`, i.e. `SAFE price = $9,000,000 / 10,000,000 = $0.90`.
- SAFE shares = `$1,000,000 / $0.90 ≈ 1,111,111`.
- Sanity check: SAFE holder's percentage of the post-conversion (pre-new-money, pre-additional-pool) company = `1,111,111 / (10,000,000 + 1,111,111) ≈ 10.00%`. Exactly `investment / post-money cap = $1M / $10M = 10%`. That is the post-money SAFE property. The number is the same whether you compute it via the SAFE price mechanic or via `investment / post-money cap` directly — the mechanic is designed to yield that identity.
- Priced-round price per share, on the same base: `$30,000,000 / (10,000,000 + 1,111,111 + [pool top-up shares])`. If the pool top-up mechanics (chapter 4 in detail) resolve the top-up at ~1,234,568 additional shares to reach a 10% post-money pool, the priced-round FD-ex-new-money is ~12,345,679, so the priced-round price is `$30M / 12,345,679 = $2.43 per share`. The SAFE price ($0.90) is lower, so the cap controls. The SAFE holder converted at the cap.

The SAFE holder now owns 10.0% of the post-conversion company (pre-new-money), which is exactly `investment / post-money cap`. This is the property that made the post-money SAFE popular with investors and unforgiving to founders — every subsequent post-money SAFE the founder signs will produce another fixed slice, and every one of those slices comes out of the founder's residual, not out of the earlier SAFE holders'.

## The pro-rata rights side letter

YC's current post-money SAFE forms do **not** grant the SAFE holder pro-rata rights (the right to invest in the next round to maintain their ownership percentage). This is a deliberate 2018 change from the pre-money legacy form, which had a pro-rata clause built in.

Instead, YC publishes a **separate side letter** that grants pro-rata rights on an opt-in basis. The founder decides whether to attach the pro-rata side letter to a given SAFE. Most institutional seed investors (Sequoia's seed programme, Andreessen Horowitz's seed programme, Kleiner's early programme, First Round, Initialized, and dozens of others) expect the pro-rata side letter as a condition of investment. Angels and friends-and-family often do not have the leverage to demand it.

The side letter is short — one page in the YC form — and does one thing: it obligates the company to offer the SAFE holder the opportunity to purchase their pro-rata share of the next priced round at the priced-round terms. It does not obligate the SAFE holder to buy; it only obligates the company to offer.

Chapter 5 handles side-letter drafting more broadly. What matters here is that the pro-rata question is not part of the SAFE itself under the current post-money form. It is a separate document, and its absence in a signed SAFE means the SAFE holder does not have pro-rata rights unless the company later grants them.

## What actually gets negotiated

The four variants and the cap/discount numbers are the visible negotiation. The full list of what changes hands in a modern post-money SAFE closing:

- **Variant choice** (cap-only, discount-only, MFN, cap + discount). Usually driven by the investor's playbook. Most institutional seed investors ask for cap-only or cap + discount.
- **Cap dollar amount.** The single biggest negotiation. A $10M post-money cap on a $500K cheque is 5% of the company on the SAFE holder's line; the same cheque at $20M cap is 2.5%.
- **Discount percentage** (if applicable). Typically 15-25%; 20% is the modal number in the YC template.
- **Pro-rata side letter, yes or no.** Institutional seed funds usually get one; angels often do not.
- **MFN, yes or no** (in variants other than variant 3). Some cap-only SAFEs are amended to add a "most-favoured-nation" clause outside the variant-3 template. This is where the failure mode in chapter 5 tends to originate.
- **Investment amount.** Standard, but note that the SAFE is issued at a specific per-dollar-invested price of the cap-implied slice, so raising the investment amount and the cap in tandem is the way to preserve the SAFE holder's target ownership.

## Common founder traps in the SAFE-signing moment

- **Signing a post-money SAFE thinking the cap is pre-money.** The post-money framing is easy to miss on a quick read of the form. If the SAFE holder's target ownership is 5% and the founder is thinking of the cap in pre-money terms, the founder ends up signing an ~11-15% ownership stake instead. Check the form.
- **Sequencing multiple SAFEs and treating them as additive.** They are additive on the SAFE-holders' aggregate ownership; they are subtractive from the founder's *only*. Four $500K SAFEs at $10M post-money caps sum to 20% of the company on the SAFE-holders' lines; the founder does not "share the dilution" with earlier SAFE holders.
- **Assuming the SAFE holder shares dilution from the option-pool top-up at the priced round.** They do not — under the post-money mechanic — up to the pre-priced-round line. The pool top-up is founder-dilutive on top of the SAFE-holders' fixed slice.
- **Signing a cap + discount SAFE assuming "one of the two will trigger."** Both trigger, and the holder picks the better one. The founder always pays the more-expensive of the two mechanics.
- **Adding an MFN to a cap-only SAFE as a "courtesy" without thinking about the cascade.** Every subsequent SAFE with a lower cap will now amend this SAFE, and every subsequent SAFE with a discount will now graft that discount on. Chapter 5.
- **Signing the pro-rata side letter without modelling the pro-rata cost.** The pro-rata obligation gets exercised at the priced round for a real cheque; the founder needs to know how much of the round will be absorbed by pro-rata rights before they set the round size and the lead-investor allocation.

## What good looks like

A CFO or founder who has this material installed:

- Signs only YC-form post-money SAFEs (or a lightly-edited derivative reviewed by counsel), not one-off custom drafts.
- Knows which of the four variants is on the table and can defend the variant choice to the investor.
- Runs the `investment / post-money cap` calculation *before* signing and shows the founder what their post-conversion ownership drops to across a full-stack scenario.
- Maintains a live SAFE register (chapter 4) with per-SAFE variant, cap, discount, MFN flag, pro-rata flag, investment amount, and as-converted percentage of the current fully-diluted-plus-SAFEs base.
- Files Form D for each closing per chapter 6.
- Treats the pro-rata side letter as a distinct decision and does not sign it on autopilot.

## Summary

- A SAFE is a contract, not stock and not debt. Its only economic content is the promise to convert into preferred shares at a defined price at the next equity financing.
- YC replaced the pre-money legacy SAFE with the post-money SAFE in September 2018. The post-money reframe fixes the SAFE holder's ownership at close as a percentage of the post-conversion company; every subsequent SAFE and every option-pool top-up dilutes the founder alone, not the SAFE holders.
- YC publishes four post-money variants: cap only, discount only, MFN only, and cap + discount. Each is a full standalone form; you pick one and use it.
- The conversion mechanic reduces to `investment / post-money cap = % of post-conversion company` for the cap variants and to `priced-round price × (1 - discount)` for the discount variant. The cap + discount variant picks whichever is more favourable to the holder.
- Pro-rata rights are not built into the current SAFE form; they are a separate opt-in side letter.
- The stacked-SAFE calculation is not additive on the founder side: the founder eats the entire dilution from every additional SAFE and every option-pool top-up. This is the property that makes chapter 4's pro-forma calculation non-trivial.

Chapter 2 turns to the pre-money legacy SAFE — the form you still find on real cap tables from the 2013-2018 vintage — and shows how its shared-dilution mechanic differs from the post-money form and how to model it correctly when it sits on a table alongside a post-money SAFE.
