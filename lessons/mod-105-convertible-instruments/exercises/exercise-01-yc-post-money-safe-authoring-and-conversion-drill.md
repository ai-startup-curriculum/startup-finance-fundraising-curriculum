# Exercise 01 — YC Post-Money SAFE Authoring and Conversion Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 1 (YC post-money SAFE anatomy and the four variants).

## Problem statement

Author one signed-and-dated SAFE in each of the four YC post-money variants (Valuation Cap only; Discount only; MFN only; Valuation Cap and Discount) for the same hypothetical company at the same closing, then model the conversion of all four into the same hypothetical Series-A. Produce the per-variant conversion table, quantify what each SAFE holder actually receives at conversion, and author a one-page memo to the founder explaining which variant is most and least dilutive under the modelled priced round, why, and what that means for the founder's next SAFE-signing decisions.

The point of the drill is to build muscle memory around the `investment / post-money cap` identity, to see all four variants side-by-side on a single conversion, and to develop the reading habit of "which variant is this SAFE, and what does that mean at conversion" that carries into every subsequent chapter.

## Scenario — build your own

Construct a hypothetical company with the following minimum shape:

- Delaware C-corp incorporated 12 months ago.
- Two founders, each with 4,000,000 shares of common. Both on 4-year vests, 12 months in.
- 1,000,000 shares of unissued option pool (no grants yet).
- No preferred stock, no warrants, no notes.

Now author four separate SAFE closings, one per variant, to different fictional investors, on the same closing day:

- **SAFE A — Valuation Cap only.** $250,000 investment, $8,000,000 post-money cap.
- **SAFE B — Discount only.** $250,000 investment, 20% discount.
- **SAFE C — MFN only.** $250,000 investment. No cap, no discount at signing; MFN clause active.
- **SAFE D — Valuation Cap and Discount.** $250,000 investment, $10,000,000 post-money cap, 15% discount.

For each, use the actual current YC post-money SAFE form (available at [`resources.md`](../resources.md); direct link at YC's site). Fill in the company name, investor name, closing date, investment amount, and variant-specific terms. Do not modify the substantive form language.

## Requirements

Produce a single workbook (Excel or Google Sheets) with the following:

1. **SAFE register tab.** One row per SAFE with columns: investor, variant, investment amount, cap, discount, MFN flag, closing date, corporate-record reference (a fictional document ID is fine — SAFE-A-001, SAFE-B-001, etc.).
2. **Pre-conversion cap-table tab.** The company's cap table before any priced round — founder common, unissued pool, and the four SAFEs shown as-converted at the assumption that the Series-A prices exactly at the caps (for SAFE A and D) or exactly at the pre-conversion pre-money FD implied price (for SAFE B and C, which have no cap).
3. **Priced-round assumption tab.** Series-A parameters: $5,000,000 new money on $20,000,000 pre-money / $25,000,000 post-money, with a 10% post-close option pool placed pre-money per the term-sheet default. Also compute a scenario where the priced round is instead $5M on $12M pre / $17M post (a "down-cap" scenario relative to some of the SAFEs).
4. **Conversion computation tab.** For each SAFE under each of the two priced-round scenarios:
   - Compute the priced-round price per share.
   - Compute the SAFE-implied conversion price per the variant's mechanic.
   - Identify which mechanic controls (cap vs. discount vs. priced-round price with no benefit).
   - Compute the SAFE holder's converted share count.
   - Compute the SAFE holder's percentage of the post-conversion company (pre-new-money) and of post-money.
5. **Cross-variant comparison table.** A summary table with rows = variants (A, B, C, D), columns = priced-round scenarios (base $20M pre, down-cap $12M pre), and cells = SAFE holder's share count, cap-controls-vs-discount-controls indicator, and post-money percentage. For the MFN-only SAFE C, assume no other SAFE with better terms was issued in the base scenario (so the MFN doesn't fire), and in a third scenario assume a later hypothetical SAFE at $5M cap was signed just before Series A and the MFN adopted those terms.
6. **One-page founder memo.** Written to the founder explaining:
   - The identity `investment / post-money cap = % of post-conversion company` (for the cap variants) and the discount identity for the discount variant.
   - Which variant produced the highest SAFE-holder ownership in each scenario, and why.
   - Which variant produced the lowest SAFE-holder ownership in each scenario, and why.
   - The specific dilution consequence for the founder from each variant under the base priced round.
   - Guidance for the founder's next SAFE closing: which variant to prefer, which to accept only under specific conditions.

## Starter guidance

- **Use the actual YC form for each SAFE.** Do not paraphrase. Filling in the form is part of the drill and reveals the specific "SAFE Price" definition each variant uses.
- **Compute the `investment / post-money cap` shortcut first for the cap variants.** Confirm your iterative solve yields the same percentage. If it doesn't, you've made an error somewhere in the denominator definition.
- **For the discount variant**, remember the discount applies to the priced-round price per share, so the SAFE holder's shares = `investment / (priced-round price × (1 - discount))`. This produces a percentage that depends on the priced-round valuation — a variant whose SAFE holder outcome is directly tied to how well the founder does at the priced round.
- **For the MFN variant, the base scenario should show the SAFE converting at the priced-round price with no discount and no cap** — a very small share count if the priced round is at a high valuation. The MFN's value comes from the option to adopt later terms, so the "MFN triggered" scenario is where the variant matters.
- **For the cap + discount variant, both mechanics fire and the holder picks the better.** Compute both and take the more-favourable (lower) price.
- **The pool top-up under the pre-money shuffle is founder-dilutive.** Model it explicitly, don't shortcut around it.

## Acceptance criteria

- **All four SAFEs are authored on the actual YC forms** with the specific variant's terms filled in and a fictional signature block.
- **The `investment / post-money cap` identity is verified numerically** for the cap variants (A and D under cap-controlling scenarios).
- **The conversion computation table is complete** for each SAFE under each priced-round scenario, with explicit cap-vs-discount identification.
- **The cross-variant comparison table shows** at least one scenario in which the discount variant beats the cap variant for the SAFE holder (typically the down-cap scenario), and at least one in which the cap variant beats the discount variant (typically the base scenario).
- **The MFN-triggered scenario correctly rewrites SAFE C's terms** and produces a materially different share count from the un-triggered base.
- **The founder memo makes a specific recommendation** on which variant the founder should offer at the next closing (and under what conditions), with the specific dilution consequences quantified.

## Deliverables

- The workbook with the register, cap-table, priced-round assumption, conversion, and comparison tabs.
- The four filled-in SAFE forms (Word or PDF, one per variant).
- The one-page founder memo (Markdown or PDF, or as a memo tab in the workbook).

## Extensions (optional)

- Add a **fifth scenario** where the priced round is exactly at the cap of SAFE A ($8M pre-money on the pre-conversion FD), producing the edge case where the cap mechanic and priced-round mechanic are indifferent for SAFE A.
- Add a **pro-rata rights side letter** to one of the four SAFEs and model the pro-rata cheque the SAFE holder would write at the priced round. Show the post-round cap-table impact.
- Author a **rejection memo** explaining why the founder declined a fifth SAFE that would have brought the aggregate `Σ (investment / cap)` from ~15% to 30%. Reference the overhang failure mode from chapter 7.
- Model the **acquisition scenario** — a sale of the company for $50M cash before any priced round — under the SAFE's "Liquidity Event" mechanic. Compare the four variants' payouts at the sale.
