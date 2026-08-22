# Drag-Along, Tag-Along, Redemption, Dividend Accrual, and MFN — The Quiet Clauses

## Why this matters

A term sheet's headline clauses — pre-money, liquidation preference, anti-dilution, board composition — attract almost all of a founder-CEO's attention in a first read. The "quiet" clauses in the back half of the term sheet get a two-minute glance and a "that's boilerplate, right?" nod. They usually are boilerplate — but the specific parameters inside them can transform an exit outcome, block a bridge, force a redemption, or trigger a cascading amendment across the preferred stack. The CFO's job is to read them with the same discipline as the headline clauses.

This chapter walks the five clauses that most frequently produce late-stage surprises when read casually:

- **Drag-along** — the obligation of the minority to vote for and sell into an approved sale of the company. The drafting parameters (who has to approve, at what threshold, with what exceptions) determine which exits can be forced and which can be blocked.
- **Tag-along / Right of Co-Sale** — the right of preferred to sell alongside a founder or key holder in a secondary transaction. Sits alongside the ROFR in the ROFR/Co-Sale agreement.
- **Redemption** — the right of the preferred to force the company to buy back its shares after a defined period at a defined price. Rare to exercise but sometimes appears in charters, and the drafting parameters materially affect the company's balance-sheet risk.
- **Dividend accrual** — the specific mechanics of the preferred's dividend (rate, cumulation, when it accrues, when it converts). The dollar amount added to the liquidation preference over time can be substantial in cumulative-dividend structures.
- **MFN (Most-Favoured-Nation) in a preferred round** — distinct from the SAFE MFN of [mod-105](../mod-105-convertible-instruments/), the preferred-round MFN entitles a preferred holder to adopt more-favourable terms granted to any later preferred holder. Less common but present in some late-stage rounds.

This chapter walks each in turn, with the drafting parameters and the negotiation posture.

## Drag-along

The drag-along clause obligates every shareholder (common, preferred, options-that-convert) to vote in favour of, and to participate in, a sale of the company that has been approved by a defined threshold of shareholders. Without a drag-along, a small minority of shareholders could block an otherwise-desirable sale — either by refusing to vote for it or by refusing to sell their shares in a private-company acquisition where the acquirer wants 100%.

The drag-along lives in the **Voting Agreement** and applies to the specific parties who signed it (typically founders, preferred, and Major Investor common holders).

The key drafting parameters:

**Approval threshold.** Who has to approve the sale to trigger the drag? Common patterns:

- **Majority of the board** — least common at seed/Series-A because it gives the board full drag authority without a shareholder check.
- **Majority of the preferred** + **majority of the common** — the founder-favourable pattern. Requires both classes to approve.
- **Majority of the preferred** only — investor-favourable. Preferred alone can force the sale.
- **Supermajority of the preferred** (66.7% or 75%) — more restrictive than majority; requires broader preferred consent.
- **Majority of the preferred + board approval + specific founder approval** — the most founder-favourable, and increasingly rare.

The NVCA-typical draft has "majority of the preferred + majority of the common (voting as separate classes)" as the trigger, sometimes with a floor on the price (see below). The classification:

- Majority-of-preferred-alone: tier-3 aggressive at Series-A.
- Majority-of-preferred + majority-of-common: tier-1 market.
- Majority-of-preferred + majority-of-common + board approval: tier-1-to-tier-2, common variation.
- Supermajority-of-preferred + majority-of-common: tier-2 negotiated, common in some drafts as a founder-favourable variant.

**Price floor.** Some drafts include a minimum price at which the drag can be exercised. Common floors:

- **A defined per-share price** (e.g., "the drag may only be exercised at a sale price above the Series A original issue price").
- **A defined preference-multiple** ("above 1.5x aggregate preference stack").
- **A defined per-common-share amount** ("above a minimum common per-share of $X").

Founders push for a floor to prevent the preferred from forcing a low-price sale that satisfies the preference but leaves the common with little. Investors resist floors because they constrain the ability to exit in stressed situations. The compromise in some drafts is a floor that expires after a defined period (e.g., "no floor after 5 years").

**Excluded transactions.** Some drafts carve out defined transaction types from the drag:

- **Transactions with an affiliate of a preferred holder** — the "no forced sale to your own portfolio company" carve-out.
- **Transactions below a defined size threshold** — small asset sales that don't rise to a sale-of-the-company level.
- **Transactions requiring specific regulatory approval** — carve-outs for regulated industries.

**Individual-founder carve-outs.** Some drafts protect specific founders from the drag if the transaction terms treat them unequally — e.g., no forced sale of a founder's shares under terms different from other common holders'.

**Rep-and-warranty / indemnification cap.** The drag-along typically includes provisions on what reps the dragged shareholders make and how they are capped. Common: dragged shareholders make only fundamental reps (title, capacity), pro-rata indemnification limited to sale proceeds received, no personal liability beyond the transaction.

The specific drafting of these parameters determines whether the drag is a "market-standard sale-facilitation clause" or an "investor-can-force-any-sale clause." The CFO reads for the specific parameters, not just the presence of a drag.

## Tag-along / Right of Co-Sale

The tag-along (or right of co-sale) applies when a founder or key holder sells shares in a secondary transaction. If the ROFR is not exercised by the company or the preferred, the preferred (typically Major Investors) has the right to sell alongside the founder proportionally.

Mechanics:

- Founder proposes to sell N shares to a third party at $X per share.
- Company gets first refusal to buy at $X.
- If company declines, preferred (Major Investors) get second refusal.
- If preferred also declines, the transaction proceeds — but preferred may elect to "tag" and sell some of their shares proportionally into the transaction, reducing the founder's sold shares proportionally.

The co-sale prevents the founder from "cashing out" quietly while the investors are locked in illiquid preferred. It also prevents a founder from selling a controlling position without giving the preferred an option to reduce their exposure alongside.

The tag-along lives in the **ROFR/Co-Sale Agreement** (one of the seven NVCA documents).

Key drafting parameters:

- **Which holders have tag rights.** Major Investors (typical). Sometimes all preferred; sometimes only specific series.
- **What securities are subject to co-sale.** Typically all founder common; sometimes limited to specific founders. Occasionally covers any preferred holder's sale as well.
- **The pro-rata calculation.** Typically pro-rata on an as-converted basis. The tag holder can sell up to their pro-rata share of the proposed sale.
- **Excluded transfers.** Transfers to permitted transferees (family members, trusts, estate-planning vehicles) are typically excluded. Also transfers on death or divorce, transfers under a Rule 10b5-1 plan post-IPO, secondary sales through a company-sponsored tender.
- **Threshold for triggering.** Some drafts have a minimum transfer size (e.g., 1% of the founder's shares); below the threshold, the tag doesn't apply.

The tag-along is largely uncontested at Series-A. It is a market-standard clause that prevents specific quiet-founder-exit patterns; founders don't usually push back on the core mechanic. The specific parameters (permitted-transferee list, transfer threshold, tag pro-rata definition) are negotiated when they matter to specific founder plans.

## Redemption right

The redemption right entitles the preferred to force the company to buy back its shares at a defined price after a defined period. Mechanics:

- **Trigger period.** Typically the preferred cannot exercise redemption for the first 5-7 years after the round. This gives the company time to build value.
- **Redemption price.** Typically the original purchase price plus any accrued but unpaid dividends. Some drafts include a modest premium (e.g., 1x + accrued dividends + 8% per annum).
- **Redemption schedule.** Typically ratable over 2-3 years after the trigger. So a $10M redemption right doesn't require immediate $10M cash; it requires $3-5M per year over the redemption period.
- **Company's ability to defer.** Some drafts allow the company to defer redemption if it would create a financial impossibility (insufficient legally-available funds under Delaware law) or a specified operational threshold.

**Why redemption exists at all.** Venture funds have a defined life (typically 10 years plus extensions). If a portfolio company hasn't exited by the fund's end-of-life, the fund needs a mechanism to get its capital back. Redemption is the theoretical mechanism.

**Why it is rarely exercised.** Companies that reach the redemption trigger period without exiting are typically either (a) doing well and can raise a subsequent round that provides liquidity to the redemption-eligible preferred, or (b) doing poorly and don't have the cash to redeem. Actual redemption exercise is rare in practice — but the existence of the right shapes the negotiation between the company and the preferred in the late-stage situation.

**Frequency.** Fenwick and Wilson Sonsini data historically shows redemption rights on a meaningful minority of preferred financings (roughly 15-25%), with wide variation across quarters and stages. The clause is more common at growth stages than at Series-A, and more common in stressed markets.

**Drafting posture.**

- **Founder-favourable:** Omit the redemption right entirely. Institutional Series-A leads increasingly accept this.
- **Investor-favourable:** Redemption after 5 years at 1x + accrued dividends, ratable over 3 years.
- **Aggressive:** Redemption after 3 years, at 1x + 8% per annum, immediate payment.
- **Unusual:** Redemption on-demand at any time; redemption at a preference-multiple; redemption tied to specific corporate events.

The clause interacts with dividends (below) — if the dividend is cumulative and the redemption price includes accrued dividends, the redemption dollar amount grows over time.

## Dividend accrual

Dividend clauses on preferred stock have a specific structure:

**Dividend rate.** Typically expressed as a percentage of the original purchase price (e.g., "6% per annum"). Sometimes expressed as a dollar amount per share.

**Cumulation.**

- **Non-cumulative.** Dividend is only owed if the board declares it. Unpaid dividends do not accumulate. Most Series-A dividends are non-cumulative.
- **Cumulative.** Dividend accrues each year regardless of whether declared. Unpaid amounts accumulate as a payable on the preferred's liquidation preference. Investor-favourable; substantially harsher.
- **Cumulative with a compounding element.** Rare; sometimes compounded annually rather than simple. Adds meaningfully to the accrual over time.

**When paid.**

- **On declaration by the board.** Standard for non-cumulative structures.
- **On liquidation event.** Cumulative dividends are typically paid at liquidation (added to the preference amount).
- **On mandatory conversion.** Some drafts allow the accrued dividends to be paid in stock at conversion.

**Priority.** The dividend is typically senior to any common dividend; the preferred must be paid its dividend before the common can receive any distribution.

**Interaction with liquidation preference.** Under most drafts, "liquidation preference" is defined as `1x purchase price + accrued but unpaid dividends`. A 6% cumulative dividend accruing over 5 years adds `5 × 6% = 30%` to the preference. On a $10M investment, that's a $3M addition to the preference — meaningful.

**Dividend classifications:**

- **Non-cumulative at 0-8%:** tier-1 market. Non-cumulative dividends are essentially a formality — they are rarely declared and effectively don't accrue.
- **Cumulative at 6-8%:** tier-3 aggressive at Series-A. Meaningful accrual over time, materially inflates the liquidation preference at a 5-7-year exit.
- **Cumulative at higher rates or with compounding:** tier-4 unusual. Very rarely accepted at Series-A.

Fenwick and Wilson Sonsini data historically show non-cumulative dividends as dominant at Series-A (frequently 80-90%+), with cumulative appearing more often at Series-B and later, and in stressed markets. Cumulative-dividend incidence is a meaningful market-conditions indicator.

The CFO's negotiation posture: accept non-cumulative at any rate (it doesn't matter economically); refuse cumulative at Series-A absent specific circumstances; accept cumulative at Series-B if the negotiation environment requires it, but push for a rate at the low end and simple (non-compounding) accumulation.

## MFN in a preferred round

The Most-Favoured-Nation (MFN) clause in a preferred-round context (distinct from the SAFE MFN of [mod-105](../mod-105-convertible-instruments/) chapter 5) entitles a specific preferred holder to adopt more-favourable terms granted to any subsequent preferred holder or to any subsequent amendment of the preferred rights.

Common patterns:

- **Series-specific MFN.** A specific series (typically the most recent one at the time the MFN is granted) gets the MFN. If a later series is granted better terms — a higher preference multiple, more favourable anti-dilution, a broader protective-provisions list — the MFN-holding series can elect to adopt those terms.
- **All-preferred MFN.** All preferred series get the MFN. Any subsequent series' better terms cascade to all existing preferred.
- **Bounded MFN.** The MFN applies only to specific enumerated terms (e.g., liquidation preference and anti-dilution only) rather than to all terms.

The MFN cascades similarly to a SAFE MFN — later amendments back-propagate to earlier holders. The cap-table impact can be material:

- A later-round narrow-based anti-dilution cascades to earlier rounds under MFN, converting the earlier rounds' broad-based clauses to narrow-based.
- A later-round higher preference multiple cascades, upgrading the earlier rounds' preference multiples.
- A later-round senior stack cascades, potentially upgrading the earlier rounds' seniority.

**When MFN appears.** MFN clauses in preferred rounds are less common than in SAFEs. They appear more often:

- In seed-to-Series-A transitions where a seed investor gets an MFN to convert-into-Series-A-with-then-current-Series-A-terms.
- In strategic-investor rounds where the strategic investor wants protection against future rounds' better terms.
- In stressed rounds where the company grants MFN as a concession to secure the round.

**Drafting posture.** The founder-favourable position is to refuse MFN in preferred rounds. If the investor insists, the compromise is:

- Bounded MFN (specific terms only, not all terms).
- Time-limited MFN (rights terminate after 12-24 months).
- Excluded-issuances list (MFN doesn't apply to specific defined round types).

Cascading MFN across multiple series with un-bounded reach is a specific pattern that produces large late-stage surprises; the CFO should refuse this pattern outright.

## The interaction table

For a comprehensive term-sheet read, these quiet clauses interact:

- **Drag-along + preference structure.** If the drag can be exercised at any price and the preference structure is heavy, the preferred can force a sale at a price that satisfies the preference and leaves the common with little.
- **Redemption + dividend accrual.** Redemption price includes accrued dividends; cumulative dividends over 5-7 years can substantially inflate the redemption dollar amount.
- **MFN + anti-dilution.** A later-round narrow-based anti-dilution can cascade backward via MFN to earlier rounds, compounding the founder-dilution impact of the later round.
- **Tag-along + secondary sales.** If the founder-CEO plans to do a secondary sale, tag-along mechanics determine how much of the sale proceeds the founder actually receives after the preferred tags.
- **Drag-along + protective provisions.** The drag-along requires majority-of-preferred vote; the protective provisions also require a class vote on sale-of-company. Both have to align for a sale to proceed.

## What the CFO produces

For every priced-round term sheet, the CFO's clause-by-clause memo should cover these quiet clauses explicitly, not merely mark them "boilerplate." Specific items:

- **Drag-along.** Approval threshold (majority-of-preferred + majority-of-common or otherwise), price floor if any, excluded transactions, individual-founder carve-outs.
- **Tag-along.** Which holders, which securities, pro-rata definition, permitted-transferee list, transfer threshold.
- **Redemption.** Presence or absence, trigger period, redemption price mechanic, schedule, ability to defer.
- **Dividend.** Rate, cumulation, payment mechanic, interaction with liquidation preference.
- **MFN.** Presence or absence, scope (bounded or all-terms), duration, cascading behavior.

Each item classified into the four tiers (market / negotiated / aggressive / unusual) and, where deviation from market appears, a specific counter-language proposal.

## Common founder traps

- **Not reading past the front-half clauses.** Drag, tag, redemption, dividend, and MFN clauses in the back half get skipped in the CEO's first read.
- **Accepting an unlimited drag-along.** Without a price floor and without a common-vote requirement, the preferred can force a low-price sale that leaves the common with little.
- **Accepting cumulative dividends "because they're just 6%."** Cumulative dividends over 5-7 years add materially to the liquidation preference and are a real economic term.
- **Missing MFN clauses in the "Other" or "Miscellaneous" sections of the term sheet.** MFN clauses sometimes appear as a specific paragraph rather than under a labelled header; missed on skim reads.
- **Accepting redemption "because it's rarely exercised."** True, but the drafting parameters matter, and a poorly-drafted redemption right creates balance-sheet risk that has downstream effects on subsequent financings.
- **Not reconciling drag-along with the sale-of-company protective provisions.** The two clauses interact and should be drafted consistently.
- **Missing the interaction between dividend accrual and redemption.** Cumulative dividends inflate the redemption amount; the two clauses combined can produce a large future obligation.
- **Not tracking MFN cascades across multiple rounds.** Each subsequent round's terms cascade backward under MFN; the compounded effect can materially reshape the earlier rounds' economics.

## What good looks like

A CFO who has this material installed:

- Reads the drag-along, tag-along, redemption, dividend, and MFN clauses with the same discipline as the headline clauses.
- Classifies each into the four tiers and produces specific counter-language for aggressive and unusual items.
- Coordinates the drag-along with the sale-of-company protective provisions and with the price-floor negotiation.
- Refuses cumulative dividends at Series-A absent specific reason; accepts non-cumulative at any rate as economically inconsequential.
- Refuses redemption at Series-A absent specific reason; if it appears, negotiates the trigger period, price mechanic, and deferral mechanics.
- Refuses MFN in preferred rounds absent specific reason; if it appears, negotiates the scope, duration, and cascading behavior.
- Tracks the interaction between these clauses and coordinates with counsel on drafting consistency.
- Maintains a preferred-terms inventory across rounds and flags cascading MFN, cumulative-dividend accrual, and redemption-approach warnings for the board.

## Summary

- The "quiet" clauses — drag-along, tag-along, redemption, dividend accrual, and MFN — get less CEO attention in a first term-sheet read, but the specific parameters can materially reshape exit outcomes, block bridges, force redemptions, or cascade cap-table amendments.
- Drag-along: obligates minority to sell into an approved sale. Key parameters: approval threshold (majority-of-preferred + majority-of-common is market), price floor, excluded transactions, individual-founder carve-outs.
- Tag-along: right of preferred to sell alongside a founder in a secondary. Key parameters: which holders, which securities, pro-rata definition, permitted-transferee list.
- Redemption: right to force the company to buy back preferred after a defined period. Rare in practice; drafting parameters affect balance-sheet risk. Refuse at Series-A when possible.
- Dividend: accrues at a defined rate. Non-cumulative is market and economically inconsequential; cumulative accrues to the liquidation preference and is meaningful.
- MFN in a preferred round: cascades better later-round terms to earlier rounds. Less common than SAFE MFN but present in some late-stage and stressed rounds. Refuse or bound narrowly.
- The clauses interact — drag with preference, redemption with dividend, MFN with anti-dilution — and require reconciled drafting.
- The CFO's memo should cover each of these clauses explicitly with the four-tier classification and specific counter-language for deviations.

Chapter 9 turns to the quarterly deal-terms data — Fenwick Silicon Valley Venture Survey, Wilson Sonsini Entrepreneurs Report, Carta liquidation-preference data — that anchors every clause classification in chapters 2-8 to the current market. The classifications drift with market conditions, and the CFO's job is to read the current position before opening the negotiation.
