# The Pre-Money Legacy SAFE — Recognition, Mechanics, and Correct Conversion

## Why this matters

YC replaced the pre-money SAFE with the post-money SAFE in September 2018, but the pre-money form does not disappear from the world at that moment. It disappears from the world at the moment every 2013-2018 vintage SAFE it authored converts or expires. In practice that means: for as long as a company on your cap table today closed anything before mid-2018, or bought an instrument from a fund that recycled the pre-money form after 2018, or accepted a friends-and-family SAFE that was xeroxed from an old copy someone had lying around, there is still a pre-money legacy SAFE on somebody's cap table.

The consequence of missing one is not a rounding error. A pre-money SAFE and a post-money SAFE for identical `investment / cap` on paper produce *different* ownership percentages at conversion, and the difference compounds when they are stacked with other convertibles. A CFO who models a pre-money SAFE using the post-money formula will over-issue shares to earlier holders and under-dilute the founder — or the reverse, depending on which direction the mistake goes. Either way the cap table breaks, the diligence firm catches it, and the priced round closes on a re-worked table with a new founder number.

This chapter installs the mechanic and the recognition heuristics.

## What "pre-money" means in the pre-money legacy SAFE

The pre-money legacy SAFE (YC 2013 vintage, sometimes republished as "SAFE (Cap)", "SAFE (Discount)", "SAFE (MFN)", "SAFE (Cap and Discount)") defines the valuation cap as a **pre-money** valuation of the priced round the SAFE converts into. Under the pre-money mechanic, the SAFE's conversion price is `cap / pre-money-fully-diluted-share-count`, where the pre-money FD count is computed *before* the SAFE conversion adds any shares (though including the option-pool per the priced-round's negotiated pool size).

This is functionally different from the post-money mechanic in one specific way: **the SAFE holder's ownership percentage is not fixed at signing**. It depends on:

- How many other SAFEs and notes are added later. Each additional convertible shares the pre-money pool, diluting the earlier SAFE holder's implied share.
- The size of the option pool the priced round assumes. A bigger pool shrinks the SAFE holder's percentage (the pool is inside the pre-money FD denominator).
- Any anti-dilution or MFN adjustments made to any of the other convertibles.

The pre-money legacy SAFE holder does not learn their final percentage until the priced round is priced. The post-money SAFE holder does — that is the point of the 2018 rewrite.

## The two-way dilution property

Consider two SAFEs on a pre-close cap table. Both are pre-money legacy, each is $500K, each has a $5M pre-money cap.

**If we model them as post-money SAFEs by mistake:** each holder ends up with $500K / $5M = 10% of the post-conversion company. Combined SAFE ownership 20%. Founder 80%.

**Correctly, as pre-money SAFEs:** both SAFEs convert against the same pre-money FD denominator. Under the pre-money mechanic, each SAFE's conversion price is `cap / pre-money-FD-count-including-both-SAFEs-plus-pool`. Solve:

- Let founder pre-money common = 8,000,000 shares. Pool assumed for the priced round = 1,000,000 shares (10% of a post-money target — we'll take it as given for now). Both SAFEs contribute shares to be solved.
- Conversion price per SAFE = `$5,000,000 / (8,000,000 + 1,000,000 + SAFE1 shares + SAFE2 shares)`. Both SAFEs use the same price because they share the cap.
- Each SAFE invests $500,000, so each buys `$500,000 / price` shares. If SAFE1 and SAFE2 have the same investment and cap, they buy the same share count. Call it *s*. Total SAFE shares = *2s*.
- Substitute: `price = $5,000,000 / (9,000,000 + 2s)`, and `s × price = $500,000`, so `s = $500,000 × (9,000,000 + 2s) / $5,000,000 = 0.1 × (9,000,000 + 2s) = 900,000 + 0.2s`, so `0.8s = 900,000`, so `s = 1,125,000`.
- Each SAFE holder gets 1,125,000 shares. Both SAFE holders combined get 2,250,000 shares. Pre-money FD (post-conversion, pre-new-money) = 8,000,000 + 1,000,000 + 2,250,000 = 11,250,000.
- Each SAFE holder's percentage of pre-money-FD = 1,125,000 / 11,250,000 = 10.0%. Combined SAFE percentage = 20.0%.

At first glance this looks like the same 20% answer as the post-money mistake. It isn't. Two differences appear as soon as the priced round happens:

- **The 20% is 20% of pre-money-FD, not of post-money-FD.** After the new investor's cheque hits, both SAFE holders and the founder are diluted by the new investor together. Under the post-money SAFE mechanic, the SAFE holders would *not* be diluted by the new investor's cheque up to their fixed pre-money slice — they hold constant at their `investment / post-money cap` percentage of the post-conversion company (before new money). Under the pre-money SAFE mechanic, they share the priced-round dilution alongside the founder.
- **If a third SAFE is added later at a lower cap**, the third SAFE's higher percentage in the pre-money pool shrinks both earlier SAFEs' percentages. Under the post-money mechanic, adding a third SAFE only dilutes the founder; the two earlier holders keep their fixed slices.

The pre-money mechanic therefore *shares* dilution across the SAFE stack and across the founder. The post-money mechanic *concentrates* dilution on the founder alone (see chapter 1).

## Recognising a pre-money SAFE on an existing cap table

The clearest tell is the form itself. YC publishes the legacy pre-money forms and the current post-money forms as distinct documents with different section titles. The pre-money forms are stamped "SAFE" in the header; the post-money forms are stamped "POST-MONEY SAFE". If the document says "post-money" anywhere on page 1, you have a post-money SAFE. If it doesn't, and the closing date is 2013-2018, you almost certainly have a pre-money SAFE.

If the closing date is post-2018 and the header says just "SAFE" without a post-money designation, dig further — some non-YC drafts and some post-2018 investor-authored templates continued to use pre-money mechanics for a couple of years. The definitive test is in the "SAFE Price" definition inside the form:

- **Pre-money SAFE.** The SAFE Price definition references "Pre-money Valuation Cap" or "Company Capitalization" defined as excluding shares to be issued in the priced-round financing. The Valuation Cap is a pre-money number.
- **Post-money SAFE.** The SAFE Price definition references "Post-money Valuation Cap" and "Company Capitalization" defined as including all SAFEs and convertible-note conversions. The Valuation Cap is a post-money number.

If a cap table you inherit reports SAFE ownership percentages that are visibly the arithmetic `investment / cap` for each SAFE and those percentages sum to something the previous CFO was calling "SAFE stack", it is almost certainly a post-money model. If the reported percentages *don't* match `investment / cap` and are lower than that arithmetic suggests, it is almost certainly a pre-money model (because the earlier SAFEs have been diluted by later ones).

If the cap table has a mix, get the form for every SAFE and confirm one at a time. Do not assume homogeneity — the [chapter 7](07-convertible-instrument-failure-modes-and-remediation.md) failure mode called "mixed pre- and post-money SAFEs on the same table" is the direct consequence of a founder who signed some 2017 pre-money forms, then in 2019 signed some post-money forms without noticing the difference, and now has a stack with mixed mechanics.

## The correct pre-money conversion arithmetic

The pre-money SAFE conversion requires an iterative solve (or a small system of equations) because every pre-money SAFE's share count depends on every other pre-money SAFE's share count via the shared pre-money FD denominator. The general procedure:

**Step 1.** Fix the priced-round option pool at its target size in shares (from the term-sheet target percentage of post-money, back-solved into shares — see [`mod-104`](../mod-104-cap-tables-and-equity-compensation/02-pre-vs-post-money-math-and-the-option-pool-shuffle.md)).

**Step 2.** For each pre-money SAFE, write its per-share conversion price as `cap_i / (existing_common + existing_options + post-round pool + Σ_j SAFE_j_shares)`, subject to a floor at the discounted priced-round price if the SAFE has a discount.

**Step 3.** Each SAFE's share count is `investment_i / conversion_price_i`.

**Step 4.** Solve the system of equations. In closed form for the common case where all pre-money SAFEs share the same cap: total SAFE shares `S` satisfies `S × cap / (existing_denom + S) = Σ investments`, i.e. `S = (Σ investments × existing_denom) / (cap - Σ investments)`.

**Step 5.** If any SAFE hits its discount floor before its cap-implied price (i.e., the priced-round price × (1 - discount) is lower than the cap-implied price), that SAFE converts at the discount price instead; recompute the remaining SAFEs' shares against the unchanged pre-money denominator.

**Step 6.** Add the priced-round investors' shares at the priced-round price. The founder's post-round percentage is `founder_common / (existing_common + existing_options + post-round pool + all SAFE shares + priced-round shares)`.

Do this in a spreadsheet with named cells and let the solver iterate; the arithmetic is straightforward but the solve is fiddly and hand-computation is error-prone once you have three or more SAFEs at different caps. Chapter 4 walks the full stacked-SAFE calculation end-to-end.

## Worked example — pre-money conversion, three SAFEs

Setup (all pre-money legacy SAFEs, no discounts, no MFNs, no notes):

- Founder common: 8,000,000 shares.
- Granted options + unissued pool at signing: 1,000,000 shares.
- SAFE A: $500K, $5M pre-money cap.
- SAFE B: $500K, $8M pre-money cap.
- SAFE C: $500K, $10M pre-money cap.
- Priced round: $10M raised on $30M pre / $40M post, with a 10% post-money option pool.

**Step 1.** Compute the post-round option pool shares. Under the pre-money shuffle default, the pool is topped up to 10% of post-money before the money hits. Solve for total post-round FD `X` and pool size:

- Pool = 0.10 × `X`. New investor = 0.25 × `X`. Founder common + granted options + all SAFE shares = 0.65 × `X`.
- Iteratively (with SAFE shares also depending on the pool via each SAFE's own pre-money denominator), this converges to `X ≈ 15,300,000` for concreteness under this stack — the exact number depends on the SAFE solve below. For simplicity fix the post-round pool at 1,530,000 shares for the calculation and iterate the whole system once more at the end if the pool assumption drifts.

**Step 2.** SAFE conversion prices. Each SAFE's price is `cap_i / (8,000,000 + 1,530,000 + SAFE_A + SAFE_B + SAFE_C)`. Let `D = 9,530,000 + s_A + s_B + s_C`. Then:

- `p_A = $5,000,000 / D`, `s_A = $500,000 / p_A = $500,000 × D / $5,000,000 = 0.10 × D`.
- `p_B = $8,000,000 / D`, `s_B = $500,000 / p_B = $500,000 × D / $8,000,000 = 0.0625 × D`.
- `p_C = $10,000,000 / D`, `s_C = $500,000 / p_C = 0.05 × D`.
- `s_A + s_B + s_C = (0.10 + 0.0625 + 0.05) × D = 0.2125 × D`.

**Step 3.** Solve for D: `D = 9,530,000 + 0.2125 × D`, so `0.7875 × D = 9,530,000`, so `D = 12,101,270`.

- `s_A = 0.10 × 12,101,270 = 1,210,127`.
- `s_B = 0.0625 × 12,101,270 = 756,329`.
- `s_C = 0.05 × 12,101,270 = 605,064`.
- Total SAFE shares = 2,571,520.

**Step 4.** Check the SAFE-holder percentages of pre-money-FD (before new-money):

- SAFE A: 1,210,127 / 12,101,270 = 10.00%.
- SAFE B: 756,329 / 12,101,270 = 6.25%.
- SAFE C: 605,064 / 12,101,270 = 5.00%.
- Total SAFE: 21.25% of pre-money FD.

**Step 5.** Founder's share of pre-money-FD: 8,000,000 / 12,101,270 = 66.11%. Founder's share after the priced-round money hits: `66.11% × (pre-money-FD / total post-round FD)`. If the priced-round investor buys 25% of post-money and pre-money-FD is 75% of post-money, then post-round total FD = 12,101,270 / 0.75 = 16,135,027 shares. Founder's post-round percentage = 8,000,000 / 16,135,027 = 49.58%.

**Compare with the post-money model.** If these three SAFEs were post-money at the same caps, each holder would own `investment / post-money cap` of the pre-new-money post-conversion company:

- SAFE A: $500K / $5M = 10.00%.
- SAFE B: $500K / $8M = 6.25%.
- SAFE C: $500K / $10M = 5.00%.
- Total SAFE: 21.25% of *post-money* pre-new-money company (the exact same headline number as the pre-money outcome above, before the priced-round dilution).

The difference emerges when the priced-round money hits:

- **Post-money mechanic.** The SAFE holders' percentages are preserved through the priced round *up to the pre-priced-round line*. The 21.25% they collectively hold pre-money is *not* diluted by the new investor's cheque. The founder's share falls further; the SAFE holders' does not. So post-round: founder ends around 46-48%, SAFEs collectively around 21.25% of post-round FD (not just of pre-money FD).
- **Pre-money mechanic.** The SAFE holders share the priced-round dilution with the founder pro-rata. The SAFE holders' collective 21.25% of pre-money-FD becomes 21.25% × 75% = 15.94% of post-round FD. Founder falls to 49.58%. New investor at 25%. Pool at 10%.

The *pre-money* result is that the founder retains **more** post-round share than under the *post-money* model with the same headline caps, because the pre-money mechanic shares the priced-round dilution across SAFE holders too. That is the point of the 2018 rewrite in reverse: the pre-money form was founder-preserving through the priced round; the post-money form is founder-punishing through the priced round.

That difference — a few percentage points at the priced round, larger at every subsequent round — is why "pre-money vs post-money" is not a cosmetic label. It is a specific mechanic that materially changes the founder's outcome.

## Anti-dilution behaviour of pre-money SAFEs

Under both the pre-money and post-money forms, a SAFE has no explicit anti-dilution provision that fires *after* conversion. Once the SAFE converts into preferred shares at the priced round, the preferred anti-dilution formula (typically broad-based weighted-average — see [`mod-108`](../mod-108-term-sheets-and-preferred-stock-economics/)) applies to the resulting preferred shares in the same way it applies to all other Series-A preferred.

But the pre-money SAFE has a **de facto** anti-dilution behaviour before conversion: because each additional SAFE at a lower cap shrinks earlier SAFEs' percentages (in the shared pre-money denominator), pre-money SAFE holders have an incentive to police what the company does with subsequent SAFEs. In practice, sophisticated pre-money SAFE holders sometimes insist on an "MFN" that back-propagates any later SAFE with a lower cap into the earlier SAFE. That is one of the failure modes chapter 5 handles.

Post-money SAFEs have no such incentive: the earlier SAFE holder's slice is fixed regardless of what caps later SAFEs have. The founder eats the difference alone.

## Common founder traps when pre-money SAFEs are on the table

- **Assuming all "SAFEs" behave the same way.** They don't. Confirm each SAFE's form before you compute anything.
- **Using the `investment / cap` shortcut for pre-money SAFEs.** That shortcut only works for post-money SAFEs (where it is the correct answer) and produces a wrong answer for pre-money SAFEs (where it treats them as if they held their percentage post-money — they don't).
- **Adding a post-money SAFE to a table that already has pre-money SAFEs without a plan.** The two mechanics interact at the priced-round conversion in a way that dilutes the pre-money SAFE holders more than they might expect (because the post-money SAFE holder's slice is preserved and doesn't share the priced-round dilution). Some investors will notice and push back; some will not. Chapter 4 walks the mixed-stack calculation.
- **Assuming a "SAFE" from 2019 or 2020 is post-money because "everyone uses post-money now."** Not everyone did. Confirm the form.
- **Reporting a pre-money SAFE's ownership as `investment / cap` in the cap table.** That number is wrong until the priced round is priced and the pool is fixed. The correct pre-conversion representation is `investment / cap = target-percentage-of-pre-money-if-no-other-SAFEs-existed` — a hypothetical number, not an actual holding.

## What good looks like

A CFO or founder with pre-money SAFEs on the table:

- Maintains a SAFE register with a "form" column that names each SAFE as post-money or pre-money legacy, sourced from the actual signed document.
- Runs the pre-money conversion arithmetic in a spreadsheet solver, not by hand.
- Reports pre-money SAFE ownership on the cap table as a computed as-converted percentage against the *current* pre-money FD denominator, with an "assumes N SAFEs currently outstanding and X pool" note.
- Flags any post-money SAFE added later that would sit alongside pre-money SAFEs, and models the mixed-stack conversion before signing the new SAFE.
- Considers whether to offer legacy SAFE holders a **conversion to post-money** amendment (chapter 5) if the mixed-stack outcome is going to surprise everyone at the priced round. Some companies clean this up during the priced round itself.

## Summary

- The pre-money legacy SAFE (YC 2013 vintage) defines its cap as a pre-money valuation and shares dilution across all pre-money holders, including earlier SAFE holders, when a new SAFE is added or a priced round closes.
- The post-money SAFE (YC 2018 rewrite) defines its cap as a post-money valuation and fixes the SAFE holder's ownership at signing; every subsequent SAFE, pool top-up, and priced-round dilution comes out of the founder alone.
- The two forms produce different founder outcomes even at the same headline `investment / cap`. Pre-money is more generous to the founder through the priced round; post-money is more generous to the founder through subsequent SAFE additions.
- Recognise a pre-money SAFE from the form itself (no "post-money" designation, pre-money-referenced cap in the SAFE Price definition), from the closing date (2013-2018 is nearly always pre-money), and from the cap-table percentages (pre-money percentages are lower than `investment / cap` when multiple SAFEs share the pre-money base).
- The pre-money conversion arithmetic is a small system of equations requiring an iterative solve. The stacked calculation is fiddly enough that it should always be done in a spreadsheet, not by hand.
- Mixed stacks (some pre-money, some post-money) require the full stacked-conversion calculation in chapter 4 and should never be modelled with a single formula.

Chapter 3 turns to the convertible note — the other seed-stage instrument, structurally different from a SAFE (debt-shaped rather than contract-shaped), and with its own set of founder-side risks that a SAFE does not carry.
