# Pre-Money vs. Post-Money Math and the Option-Pool Shuffle

## Why this matters

Every priced round is expressed on a term sheet with three numbers: **pre-money valuation**, **investment amount**, and **post-money valuation** — where the third equals the first plus the second, and the investor's ownership is *investment ÷ post-money*. The math looks arithmetical. It is not.

Buried under the pre-money line is a fourth number that controls 2-5% of the founder's stake at the close: the size of the option pool the round assumes, and whether that pool is expanded **before** the money hits (the "pre-money pool") or **after** (the "post-money pool"). The NVCA model term sheet defaults to pre-money — the founder-dilutive treatment — and the reason it defaults there is that the pre-money treatment shields the new investor from the pool expansion. This is the option-pool **shuffle**, and it is the highest-leverage negotiation on a Series-A term sheet after the valuation itself.

Founders regularly sign term sheets thinking they've negotiated a valuation, only to find at closing that a top-up requirement in the fine print has expanded the pool from 8% to 12% pre-money — a 4% founder-dilutive move worth, at a $30M pre-money, roughly $1.2M of founder value shifted to the pool for the incoming investor's benefit. The pool expansion is not a gift to future employees; the pool expansion is a price cut on the investor's shares, dressed up as a hiring plan.

This chapter installs the math to see the shuffle clearly, price it in a term-sheet analysis, and negotiate against it.

## The three numbers on the term-sheet cover

A priced round is quoted as, e.g., **"$10M on $30M pre / $40M post"**. The numbers mean:

- **Pre-money valuation:** the agreed valuation of the company *before* the new investment. Here: $30M.
- **Investment amount:** the cash the round contributes. Here: $10M.
- **Post-money valuation:** pre-money + investment. Here: $40M.

The investor's post-money ownership on a fully-diluted basis is `investment / post-money`. Here: $10M / $40M = 25%. The existing holders (founders + option pool + prior SAFEs / notes converted at this round + prior preferred if any) own the remaining 75%.

Those numbers determine the **share price** the round is done at: `pre-money / pre-money fully-diluted share count = price per share`. If the pre-money fully-diluted is 10,000,000 shares, the price is $30M / 10M = $3.00 per share. The investor then buys `$10M / $3.00 = 3,333,333 shares` of the new Series-A preferred.

That's the arithmetic. The subtlety is what "pre-money fully-diluted share count" contains. The option-pool shuffle is the argument over exactly that denominator.

## The two option-pool treatments

Every priced round assumes a target post-close option pool — the reserved-but-unissued pool the company will have after the round closes, expressed as a percent of post-money fully diluted. The NVCA term sheet defaults to something like "10-15% of post-money fully diluted." That percent has to be created out of shares that come from somewhere. The two choices:

**Pre-money option-pool expansion (the shuffle, founder-dilutive).** The pool is expanded to the target size *before* the money hits. The expansion happens on the pre-money fully-diluted share count. The new investor's price-per-share is calculated against the *post-expansion* pre-money count, which is a larger denominator, which is a smaller per-share price. The founder — whose pre-money ownership was based on the *pre-expansion* count — gets diluted by the entire pool expansion, and the new investor gets more shares at a lower per-share price.

**Post-money option-pool expansion (all-parties-dilutive).** The pool is expanded to the target size *after* the money hits. The expansion happens on the post-money fully-diluted share count. Every existing holder (founders, prior preferred, prior SAFE / note holders that just converted) and the new investor are all diluted pro-rata by the pool expansion. This is the fair treatment — the pool is for the benefit of future employees who will work for all current holders, so all current holders should share the cost.

The NVCA reference term sheet defaults to the pre-money treatment. This is not because it is fairer; it is because the reference document was written from the investor's perspective and this is the investor-favourable default.

## Worked example — pre-money shuffle vs. post-money treatment

Set up the pre-close cap table:

```
Pre-close fully-diluted:
  Founder common                            8,000,000    82.1%
  Options granted                             200,000     2.1%
  Existing option pool (unissued)             800,000     8.2%
  SAFEs as-converted at this round            750,000     7.7%   (illustrative)
------------------------------------------------------------
  Pre-close FD                              9,750,000   100.0%
```

The Series-A term sheet: **$10M on $30M pre / $40M post**, with a **10% post-close option pool**.

**Post-money treatment (fair).** The 10% pool sits on the post-money fully-diluted count. The new investor is `$10M / $40M = 25%`. The pool is 10%. Existing holders are diluted to `100% - 25% - 10% = 65%` of post-money.

Post-close fully-diluted total (call it `X`):
- Existing FD (9,750,000) = 65% of `X`, so `X = 9,750,000 / 0.65 = 15,000,000`
- New investor shares = 25% of `X` = 3,750,000
- Post-close pool = 10% of `X` = 1,500,000

But the existing pool already contains 800,000 shares. The top-up amount is `1,500,000 - 800,000 = 700,000` new shares issued into the pool.

Share price the investor pays: `$30M / (9,750,000 + 700,000 in post-money treatment) = $30M / 10,450,000 = $2.871 per share`... but this is where the post-money treatment gets subtle. In a *true* post-money treatment, the price per share is set based on the pre-money valuation divided by the pre-money fully-diluted count *without* the pool expansion, because the pool expansion is being borne by everyone including the investor. So the price is `$30M / 9,750,000 = $3.077 per share`, and the new investor gets `$10M / $3.077 = 3,250,000 shares`.

Now the post-close breakdown, post-money treatment:

```
Founder common                            8,000,000    50.79%   (diluted from 82.1%)
Options granted                             200,000     1.27%
Existing option pool + top-up             1,500,000     9.52%
SAFEs (as-converted)                        750,000     4.76%
Series A preferred                        3,250,000    20.63%
Additional pool for post-close 10% target   [need iter]
------------------------------------------------------------
```

Iterating for the 10% post-close pool target (a small circular calc because the pool sits inside the denominator that defines its 10% target), the top-up settles at `~1,472,000 additional shares` for a total pool of `~2,272,000` and a post-close FD of `~15,222,000`, at which point the investor's 3,250,000 shares are `~21.35%`, not 25%. Which is not what the term sheet said. Which is why the investor doesn't want the post-money treatment.

**Pre-money treatment (the shuffle, founder-dilutive).** The 10% pool is created *before* the money hits, and the investor's 25% is calculated against the post-expansion base. The share price is set so that the new investor lands at 25% of post-money after the expansion. Iterating:

- Post-close FD `X`. New investor = 25% × `X`. Pool (post-close) = 10% × `X`. Existing (founder + options + SAFEs, unchanged) = `9,750,000 - 800,000 = 8,950,000` (existing without the pool). So `8,950,000 + 0.10X + 0.25X = X`, i.e. `8,950,000 = 0.65X`, so `X = 13,769,000`.
- Post-close pool: `0.10 × 13,769,000 = 1,377,000` shares. Top-up from existing 800,000 pool: `577,000` new pool shares.
- New investor: `0.25 × 13,769,000 = 3,442,000` shares.
- Pre-money fully-diluted (post-expansion): `13,769,000 - 3,442,000 = 10,327,000` shares.
- Share price: `$30M / 10,327,000 = $2.905 per share`.

Now the post-close breakdown, pre-money treatment:

```
Founder common                            8,000,000    58.10%   (diluted from 82.1%)
Options granted                             200,000     1.45%
Post-close option pool                    1,377,000    10.00%   (was 800K, +577K top-up)
SAFEs (as-converted)                        750,000     5.45%
Series A preferred                        3,442,000    25.00%
------------------------------------------------------------
Total post-close FD                      13,769,000   100.00%
```

**Compare the founder's stake between the two treatments:**

- Post-money (fair): founder ~50.8%.
- Pre-money (shuffle): founder ~58.1%.

Hold on — the pre-money treatment leaves the founder with *more*? No — because in the post-money treatment we set the pool target properly and the investor absorbed part of the pool cost, but we also let the investor drop to 21.35% instead of 25%. If we hold the investor's 25% target constant in both treatments, the difference reverses and the pre-money treatment costs the founder 2-5% more dilution than the post-money treatment.

The correct apples-to-apples comparison: **hold investor ownership constant at the term-sheet 25%, hold post-close pool constant at 10%, and see who bears the cost of the pool.** In the pre-money treatment, the founder + existing common bears the whole cost. In the post-money treatment, the founder + existing common + the new investor share the cost, so the pre-money valuation must be adjusted downward (or the investor's cheque up) to still yield 25% for the investor. The founder's stake improves by the investor-share-of-pool-cost, typically 2-5% of the post-close company depending on pool size.

The rule of thumb: **each 1% of post-close pool the founder is asked to source pre-money is worth roughly 0.25-0.30% of the founder's post-close stake** at typical Series-A ownership splits. A 4-percentage-point pool bump (say from 8% to 12%) is worth ~1.0-1.2% of founder ownership — at a $30M pre-money, roughly $300-$400K of founder value shifted to the investor. Multiply through the pool sizes seen in practice (10-15%) and the shuffle regularly moves 2-5% of the founder's post-close stake.

## The three levers to negotiate against the shuffle

Founders who understand the shuffle push back on it in three ways:

1. **Right-size the pool to the actual hiring plan, not to a benchmark.** The investor's ask is often "12% pool" because 12% is what Carta's benchmarks show at Series-A. But the *right* pool size is what the company will actually grant between now and the next round. If the hiring plan calls for 15 hires over 18 months at typical Series-A grant sizes, the pool required is often 6-8%, not 12%. A hiring-plan-derived pool sizing (chapter 3) is the specific counter to the benchmark ask.
2. **Push some of the pool to post-money.** A negotiated position: "The next 4% of pool comes pre-money; anything above that is post-money." This splits the cost — the pre-money portion is founder-dilutive, the post-money portion is all-parties-dilutive. Investors will usually accept some version of this because the split acknowledges that not all of the pool will be needed for the near-term hiring plan the current investor's cheque funds.
3. **Trade the pool size against valuation.** A term sheet at "$10M on $30M pre with 12% pool" is roughly equivalent to "$10M on $28M pre with 8% pool" in terms of founder-dilution. Founders who understand the shuffle math negotiate against the combined footprint — pool + pre-money — not against either in isolation. Investors sometimes negotiate hardest on the pre-money line because it's the visible one; conceding the pool line is often easier for the investor because the pool doesn't come out of their return.

Number 3 is the leverage move: the pre-money valuation is a headline number that the founder and the investor both care about publicly. The pool size is a fine-print number the founder cares about privately. A founder who trades a lower headline pre-money for a lower pool sometimes ends up with more founder-equity at closing and a more defensible headline number to the market at the next round.

## What the term sheet actually says

The NVCA model term sheet phrases the pool as:

> *"Immediately prior to the Closing, an aggregate of __\_\_\_\__ shares of Common Stock shall be reserved for issuance to employees, directors and consultants pursuant to the Company's stock option plan (the 'Option Pool'), which reservation shall represent __\_\_\_\_% of the Company's fully diluted post-Closing capitalization."*

Read that closely. "Immediately prior to the Closing" — that is the pre-money placement. "__\_\_% of the Company's fully diluted post-Closing capitalization" — that is the target as a percent of post-money. The construction is a percentage target on a post-money base achieved by a pre-money expansion — which is the shuffle.

The founder-favourable red-line replaces "immediately prior to the Closing" with "immediately following the Closing" (or "concurrent with the Closing on a pro-rata basis with the New Investors") to flip to the post-money treatment. This one word change is the point of the negotiation.

A more elegant and increasingly common red-line: specify a **shares number** for the pool, not a percentage, derived from a hiring plan the founder shows the investor. This defuses the shuffle by making the pool size a defensible operational number rather than a benchmark-driven percentage. The counter-signal is that this shows the founder has thought about hiring specifically, not aspirationally.

## Common founder traps in the term-sheet mechanics

- **Reading pre-money as "how the market values my company" and missing that a 10-15% pool tucked underneath is the actual valuation baseline.** The right internal number to compare across term sheets is "effective pre-money per fully-diluted share" — the post-close per-share price — not the headline pre-money.
- **Signing the term sheet with the pool percentage but not the shares number.** The percentage becomes shares only at closing when the pre-close FD is fixed. Any ambiguity about which SAFEs converted at what discount, whether a warrant should have been exercised, or what the actual grant register looks like moves the shares number and therefore the actual dilution.
- **Not modelling the post-close cap table before signing.** The three-line calculation above should be run — with a scenario range on pool size — before the term sheet is signed, not after.
- **Missing that the shuffle also dilutes SAFE holders.** Post-money SAFEs are protected against future round dilution *up to the SAFE's target ownership*, but the pool expansion at the priced round hits SAFE holders too. A founder who thinks the SAFE holders will bear part of the shuffle cost has misread the SAFE mechanics.
- **Missing the compounding across rounds.** A 4% pool bump at Series-A followed by another 4% bump at Series-B is not 8% dilution — it compounds. A founder at Series-Seed at 80% could realistically end at Series-B at 40% with two rounds of pool shuffling on top of the round itself.

## What good looks like

A CFO or founder who has this material installed walks into a term-sheet negotiation with:

- A **pre-close fully-diluted cap table** with every SAFE / note conversion modelled at this round's cap.
- A **hiring-plan-derived pool size** for the coming 18 months (chapter 3), in shares.
- A **scenario table** showing three post-close outcomes: term-sheet-as-written (pre-money shuffle), split (some pre / some post), and post-money treatment — with the founder's stake in each and the effective pre-money-per-share in each.
- A **red-line of the option-pool clause** in the term sheet, prepared before the negotiation, that they can bring out when the pool language comes up.
- A **trade-space read** — the pool-vs.-pre-money combined footprint — so they can negotiate the whole envelope rather than either line in isolation.

If a founder shows up with just the term sheet and no post-close cap-table model, the investor's math is the only math in the room, and the shuffle prices in without a debate.

## Summary

- The three term-sheet numbers (pre-money, investment, post-money) do not tell the whole story. A fourth number — the target option pool and whether it is placed pre-money or post-money — controls 2-5% of the founder's post-close stake.
- The pre-money option-pool "shuffle" is the founder-dilutive default: the pool is expanded before the money hits, so the entire expansion cost falls on existing holders and the investor's per-share price is calculated against the larger pre-expansion base.
- The post-money treatment is all-parties-dilutive: the pool is expanded after the money hits, so the new investor bears their pro-rata share of the pool cost.
- The three counter-moves are right-sizing the pool to the hiring plan, splitting the pool between pre-money and post-money, and trading pool size against pre-money valuation as a combined footprint.
- The NVCA model term sheet defaults to the pre-money placement; the founder-favourable red-line flips it to post-money or replaces the percentage with a hiring-plan-derived shares number.
- Modelling the post-close cap table under both treatments *before* signing is the mechanic that surfaces the shuffle in dollar terms. Signing without that model concedes 2-5% of the founder's stake by default.

Chapter 3 turns to ESOP sizing: how big the pool should actually be, per round, per stage, benchmarked against Carta and Pave data and the practical hiring-plan mechanic.
