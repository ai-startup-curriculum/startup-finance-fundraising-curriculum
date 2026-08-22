# Pro-Rata, Super-Pro-Rata, and Lead-Pro-Rata Rights

## Why this matters

Pro-rata is the right of an existing preferred holder to invest their proportional share of a subsequent round in order to maintain their ownership percentage. It sounds administrative — "just an option to invest more later" — but the mechanics compress the allocation available to a new lead in the next round, and if the CFO doesn't model the compression before agreeing the round size, the round can close under-allocated to the new lead and above-allocated to the existing stack. Both outcomes create problems: the new lead didn't get the ownership they underwrote to, or the round is oversized because the pro-rata pushed it past the founder's target dilution.

Three variants matter:

- **Pro-rata** — the standard right, proportional to current ownership.
- **Super-pro-rata** — the right to invest *above* pro-rata, sometimes uncapped and sometimes capped at 2x pro-rata; more common at seed and Series-A for the lead investor.
- **Lead-pro-rata** — a specific reserved allocation for the *lead* of the previous round in the next round, sometimes over and above their pro-rata.

This chapter walks the mechanics, the compression math, the drafting patterns (charter vs. IRA vs. side letter), and the term-sheet decisions the CFO makes at each round.

## The basic pro-rata clause

Under the NVCA Investors' Rights Agreement, pro-rata rights (referred to in the IRA as "preemptive rights" or "right of first offer" for new issuances) obligate the company to offer each holder of a defined preferred series the opportunity to purchase up to their pro-rata share of any new equity issuance, at the same terms as the new lead. Mechanically:

- **Trigger.** Any new issuance of equity (with defined excluded issuances similar to the anti-dilution excluded issuances — options under plan, acquisitions, etc.).
- **Notice.** Company must give notice to each pro-rata-eligible holder describing the new issuance's terms.
- **Election window.** Each holder has a defined window (typically 20-30 days) to elect to purchase up to their pro-rata share.
- **Pro-rata calculation.** Typically defined as `(holder's shares as-converted) / (total fully-diluted shares)` × new issuance size. Some drafts define it differently — e.g., `(holder's preferred shares as-converted) / (total preferred as-converted)` × new preferred issuance — which changes the percentage the holder can buy.
- **Non-election.** If a holder does not elect within the window, the right is waived for that round (but not for future rounds).

The two things the CFO watches for at drafting:

- **The exact pro-rata denominator.** Under the "fully-diluted total" denominator, existing pro-rata rights holders can only buy their FD-percentage. Under the "preferred-only" denominator, they can buy a larger absolute amount because the pro-rata slice is a bigger fraction of the round. The FD-total denominator is more founder-friendly.
- **Which securities are eligible.** Some drafts limit pro-rata to "future Preferred Stock issuances"; others cover any equity issuance including common issuances to strategic partners. The founder-favourable version is narrower (preferred only); the investor-favourable is broader (all equity).

## Worked pro-rata compression — Series A into Series B

Setup after Series A close:

- Common (founders + employees + granted options): 8,000,000 shares.
- Options (unissued pool): 500,000 shares.
- Series A Preferred: 2,000,000 shares ($10M at $5.00), pari-passu 1x non-participating, with pro-rata rights on a fully-diluted basis for the lead ($8M of the $10M cheque, i.e., 80% of the Series A round) and no pro-rata rights for the smaller Series-A-follower participants.
- Series A lead pro-rata: `1,600,000 / 10,500,000` = 15.24% of Series A FD.

Series B close:

- Target Series B raise: $30M new money on $90M pre-money / $120M post-money.
- Target Series B price per share: `$90M / 10,500,000 shares` (pre-money FD, ignoring the option pool top-up for simplicity) ≈ $8.57 per share.
- Target Series B shares issued: `$30M / $8.57` ≈ 3,500,000 shares.

Now compute Series A lead's pro-rata invitation in the Series B round:

- Series A lead's Series A FD share: 15.24% (from above).
- Under FD-total pro-rata, Series A lead may purchase up to 15.24% of the Series B issuance = 15.24% × 3,500,000 shares = 533,333 shares × $8.57 = $4.57M.
- Under preferred-only-denominator pro-rata (rarer for the lead-only case but seen in some drafts), Series A lead could purchase up to 80% of any new preferred issuance = 80% × 3,500,000 = 2,800,000 shares × $8.57 = $24M. But this variant is unusual for the base pro-rata clause; more commonly the "80% of preferred" mechanic is written as a super-pro-rata or as a specific lead-pro-rata reservation (see below).

Under the FD-total definition, the Series A lead invests $4.57M of the $30M Series B, and the new Series B lead has $30M − $4.57M = $25.43M of available room. If the new Series B lead's underwriting was to a $25M cheque with a target 20% post-money ownership, they get exactly the right allocation.

But if all Series A investors had pro-rata (not just the lead), and half of them exercise, the compression grows:

- If 50% of the Series A pro-rata is exercised (some smaller Series A followers had pro-rata too), the aggregate Series A pro-rata exercised = 50% × (2,000,000 / 10,500,000) × 3,500,000 = 333,333 shares × $8.57 = $2.86M. Adding to the lead's $4.57M: aggregate existing-investor pro-rata $7.43M. New lead has $22.57M room.

If all existing pro-rata is exercised in full ($4.57M + all-follower pro-rata if any had it), the new lead's room can be materially compressed. The CFO's job at term-sheet stage is to model this before agreeing the round size.

## The "round-size-is-a-live-negotiation" implication

If the new Series B lead has underwritten to $25M and existing pro-rata is going to absorb $10M, the round has to size up to $35M for the new lead to get their $25M — but that pushes the total dilution above the founder's target. Or the pro-rata has to be partially waived by the existing investors.

This is a live negotiation at Series B (and every subsequent round). Possible resolutions:

- **Size the round up to accommodate.** Raise $35M instead of $25M — but this increases founder dilution beyond the original plan and may push the round size past what the founder wants for milestone-bar reasons ([mod-107](../mod-107-fundraising-strategy-and-investor-targeting/) chapter 1).
- **Ask existing investors to waive part of their pro-rata.** Not automatic; requires each investor's consent. Some sophisticated funds will waive if the CFO frames it well ("we want to add a specific strategic new lead and the round-size math doesn't work with full pro-rata; we'd like you to waive down to X%").
- **Ask the new lead to accept a smaller allocation.** Rarely successful with a top-tier lead; the fund has an underwriting target and won't lead if that target isn't achievable.
- **Split the round into two closings.** The lead's closing at $25M as the "first close," then a "second close" for existing pro-rata within 30-60 days. The lead's ownership stabilises at their target, then the pro-rata investors buy in and their pro-rata further dilutes everyone including the lead — but the lead has often anti-diluted itself by writing a large enough cheque to survive the pro-rata dilution.

The compression math is a routine part of the CFO's Series B planning. The chapter's exercise walks the arithmetic in more detail.

## Super-pro-rata

Super-pro-rata is a clause that entitles an investor to invest *above* their pro-rata share in a subsequent round. Two common structures:

**Bounded super-pro-rata.** The investor may invest up to a defined multiple of their pro-rata (e.g., 1.5x pro-rata, or 2x pro-rata), subject to availability. This is common for the lead of the current round when the fund's model wants to increase ownership over time — the "we lead and want to add to the position in the next round" investor.

**Uncapped super-pro-rata.** The investor may invest as much as they want in the subsequent round, subject to the round size and other investors' pro-rata. Rare; usually only granted to a specific strategic or specific-fund lead in a specific-relationship structure.

Super-pro-rata is a real economic ask and should be treated as tier-3 negotiated territory at Series-A. Granting super-pro-rata to the Series A lead means:

- In a Series B where the new lead expects to lead-and-set-ownership, the Series A lead's super-pro-rata compresses the new lead's allocation *more* than a basic pro-rata would.
- The Series A lead's total ownership at Series B is materially higher than it would be under basic pro-rata, which shifts governance leverage.
- Founders and other investors dilute more per Series B dollar because a larger share of the round is going to existing holders.

Founders' default posture on super-pro-rata should be to decline. It gives the lead a level of ownership control that basic pro-rata (which is already market-standard) does not provide. If the lead insists, capping at a modest multiple (1.5x pro-rata rather than uncapped) is the compromise.

## Lead-pro-rata

Lead-pro-rata is a specific reserved allocation for the lead of the current round in the next round, sometimes structured as a super-pro-rata and sometimes as a specific dollar-amount reservation.

Two common patterns:

**Reserved allocation.** "The Series A Lead has the right to invest up to $Y in the Series B" — a specific dollar amount, negotiated at Series-A, that the Series B has to accommodate. Founder-adverse; forces the Series B round to size around the reservation.

**Pro-rata plus first-right-of-refusal.** "The Series A Lead has the right to invest its pro-rata plus a first right of refusal on any unallocated portion of the Series B round." This gives the Series A Lead an option on unallocated capacity, which may or may not exist depending on how the round shapes up. Milder than a reserved allocation.

Lead-pro-rata is unusual at institutional Series-A when written as a reserved allocation; it appears more often as a side-letter arrangement with strategic co-investors or with specific angel leads at seed. The CFO who sees a lead-pro-rata reserved-allocation clause on a Series-A term sheet should treat it as tier-3 aggressive and negotiate to strip it or convert it into basic pro-rata.

## Where pro-rata lives — charter, IRA, side letter

Pro-rata rights are typically drafted in the Investors' Rights Agreement (IRA) rather than in the charter, because they are a contractual right against the company rather than a share-attached right that survives transfer. In the IRA:

- **The pro-rata clause covers "Major Investors"** — a defined term, typically investors holding at least X% of the preferred (e.g., 2%, or a fixed share threshold). Smaller preferred holders below the Major Investor threshold typically do not get pro-rata rights. This limits the number of parties the CFO has to notify and coordinate at each subsequent round.
- **Some funds negotiate side-letter pro-rata** to secure their pro-rata separately from the IRA (e.g., if the fund's Major Investor threshold isn't met by their cheque size, or if the fund wants to lock in pro-rata rights that survive a change in the Major Investor definition later).
- **Transferability of pro-rata rights** is a drafting point — pro-rata rights typically do not transfer to a secondary purchaser unless the transferee is a fund affiliate. The CFO's counsel should confirm the drafting matches the intent.

Termination:

- **On IPO.** Pro-rata rights terminate at IPO (registration rights take their place).
- **On sale of the company.** Pro-rata rights don't apply because there is no future issuance.
- **On other defined events** — e.g., a defined "material recapitalisation" or a specific corporate transaction — may terminate or modify pro-rata rights depending on the IRA drafting.

## The pro-rata modelling workbook

For every priced-round term-sheet negotiation, the CFO should have a "next-round pro-rata compression" model that shows the impact of existing pro-rata on the next round's available allocation. Minimum structure:

- **Existing pro-rata rights inventory.** For each preferred holder with pro-rata (typically the Major Investors), their pro-rata percentage, and whether the pro-rata is basic, super-pro-rata (with cap), or lead-pro-rata (with specific reservation).
- **Next-round assumptions.** Target raise size, target pre-money, target price per share, target new-lead cheque size, target new-lead ownership percentage.
- **Pro-rata absorption calculation.** For each pro-rata holder, the maximum dollars they could invest under their clause; for each, an assumption on whether they will exercise (base case: 100% for institutional funds, 30-50% for angels).
- **Compression table.** Aggregate exercised pro-rata dollars; residual room for the new lead; comparison against the new lead's underwriting.
- **Sensitivity block.** How the compression changes under different pro-rata-exercise assumptions and under different round-size assumptions.
- **Round-size decision.** The founder-facing memo: given the compression, does the round size up, does the CFO negotiate pro-rata waivers, or does the new lead accept a smaller allocation?

## The CFO's decision tree at Series-A term-sheet stage

For each pro-rata-related clause in the received term sheet:

- **Basic pro-rata for Major Investors:** tier-1 market. Accept as-is with the NVCA-standard Major Investor definition (typically a share-count threshold).
- **Basic pro-rata for all preferred holders (not limited to Major Investors):** tier-2 negotiated. Push for a Major Investor threshold to reduce the notification-and-coordination burden.
- **Super-pro-rata for the lead:** tier-3 aggressive. Refuse or cap at a modest multiple (1.5x pro-rata).
- **Lead-pro-rata with reserved allocation:** tier-3-to-tier-4. Refuse or convert to a first-right-of-refusal on unallocated capacity.
- **Pro-rata on all equity issuances (not limited to preferred):** tier-3. Push for preferred-only.
- **Pro-rata surviving IPO:** tier-4 unusual. Refuse.
- **Pro-rata transferring to secondary purchasers without consent:** tier-3-to-tier-4. Push for consent requirement or limit to fund affiliates.

## The role of pro-rata in signalling and governance

Beyond the mechanical dilution consequence, pro-rata rights are a real governance and signalling tool:

- **A lead's exercise of pro-rata in the next round is a strong positive signal.** It tells the market the existing lead is doubling down. Founders who want the signalling benefit should make sure the pro-rata is clearly exercised (not just partially).
- **A lead's decision to *not* exercise is a strong negative signal.** In particular, if the Series A lead's fund has capacity to lead the Series B (fund-size math permitting) but doesn't, it reads as a vote of no-confidence. In practice this is one reason funds are careful about pro-rata drafting — they want the option, but they don't want the option to be a signal they are forced to send.
- **Some funds negotiate pro-rata waivers with the company in advance** to preserve optionality and avoid the negative signal of a non-exercise on the standard timeline. The CFO's job is to know which funds do this and to structure the notice-and-election window accordingly.

Chapter 8 (drag-along, tag-along, and other quiet clauses) revisits the signalling dimension in more depth; the specific pro-rata-signalling mechanic is worth naming here because it is often more consequential than the dilution math.

## Common founder traps

- **Not modelling pro-rata compression before agreeing the round size.** The most common failure. Series B closes and the new lead is short-allocated because the round wasn't sized for the pro-rata absorption.
- **Agreeing to a broad "any equity issuance" pro-rata trigger.** Under such a clause, issuances to strategic partners, lenders' warrants, or specific hire-related equity grants can trigger pro-rata notices that the CFO didn't anticipate.
- **Not defining Major Investor clearly.** Without a share-count threshold, every preferred holder — including small angels — has pro-rata. The notice-and-election coordination burden becomes real.
- **Accepting super-pro-rata for the lead as a "small ask."** Super-pro-rata materially shifts the ownership balance at the next round and should not be granted routinely.
- **Missing lead-pro-rata reserved allocations.** These are sometimes buried in the "Purchase Rights" clause of the term sheet as a specific dollar or percentage reservation and not prominently labelled.
- **Not coordinating with counsel on pro-rata drafting between IRA and side letters.** Duplicative or contradictory drafting between the IRA and side letters can produce disputes at the next round.
- **Assuming pro-rata is uniformly exercised.** Angels and smaller preferred holders often don't exercise; institutional leads usually do. Modelling assumptions should reflect the specific investor mix.

## What good looks like

A CFO who has this material installed:

- Maintains a live pro-rata inventory for every priced-round company they support: holder, pro-rata percentage, super-pro-rata cap if any, lead-pro-rata reservation if any, transferability, and IPO-termination.
- Models pro-rata compression before agreeing the size of any subsequent round.
- Structures the notice-and-election mechanics with counsel to allow orderly Series-B closing.
- Negotiates the Major Investor definition to a threshold that limits the notification burden.
- Refuses super-pro-rata and lead-pro-rata reserved allocations at Series-A absent specific and documented reason.
- Coordinates with the CEO on the signalling implications of the lead's pro-rata exercise or non-exercise in subsequent rounds.

## Summary

- Pro-rata rights entitle a preferred holder to invest their proportional share of a subsequent round to maintain ownership. Standard at Series-A for Major Investors.
- The pro-rata denominator (fully-diluted total vs. preferred-only) materially affects the dollar amount the holder can invest. FD-total is founder-friendly.
- Super-pro-rata is the right to invest above pro-rata; lead-pro-rata is a specific reserved allocation for the lead of the prior round. Both are tier-3 aggressive at Series-A and should be refused or capped.
- Pro-rata rights typically live in the Investors' Rights Agreement, apply only to Major Investors, terminate at IPO, and do not transfer to secondary purchasers without consent.
- Pro-rata compresses the allocation available to a new lead in the subsequent round. The CFO's job is to model the compression before agreeing the round size.
- The CFO's output: a pro-rata inventory, a compression model, a Major Investor definition negotiated to a defensible threshold, and a decision tree for the various pro-rata variants that appear in term sheets.
- Beyond the mechanical dilution consequence, pro-rata exercise is a strong signalling event at the next round.

Chapter 6 turns to protective provisions — the enumerated list of decisions that require preferred consent — and to the discipline of distinguishing a market-standard list from a veto-heavy list that would give the preferred effective control over normal operating decisions.
