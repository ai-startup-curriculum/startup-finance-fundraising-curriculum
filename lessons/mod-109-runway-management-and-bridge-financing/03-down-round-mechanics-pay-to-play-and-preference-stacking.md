# Down Round Mechanics — Pay-to-Play and Senior-Preference Stacking

## Why this matters

A **down round** is a priced financing at a pre-money valuation lower than the post-money of the previous round — the company is worth less, in the market's judgement, than it was last time. Down rounds are unavoidable in some market conditions and unavoidable for some companies whose KPIs did not deliver. They are also mechanically the hardest priced round to structure: the anti-dilution formulae from [mod-108](../mod-108-term-sheets-and-preferred-stock-economics/) chapter 4 re-trigger, the preference stack from mod-108 chapter 2 has to be re-run, existing investors who don't want to take the mark can force a class-vote deadlock, and the cap table can end up in a state where the founders and employees have very little economic upside on any near-term exit.

Two mechanisms exist to make down rounds close-able in these harder cases: **pay-to-play**, which conditions the preservation of existing preferred rights on the existing preferred participating in the down round pro-rata, and **senior-preference stacking**, which layers a new preferred class ahead of the existing stack to give the new lead a preference that would otherwise be unavailable in a stack of pari-passu rounds. Both are aggressive tools. Both re-shape the cap table in ways the founder has to model in advance to be able to negotiate against them.

This chapter covers the mechanics of both. Chapter 4 covers the harder cousins — recapitalisations, cram-downs, and the common-employee re-up grants that restore team economics after either mechanic fires.

## The economics of a down round

Before the mechanics, the basic economics. A down round hurts three classes differently:

- **Common (founders and employees).** Hurt by the new-money dilution at the lower valuation, and hurt again by anti-dilution recalculation that reduces the conversion price of existing preferred (increasing their as-converted share count and further diluting common). If pay-to-play converts non-participating existing preferred to common, the founders and employees actually *gain* from that specific mechanic (because the participating preferred that would have taken preference out in a sale is now voting alongside them as common) — but the offsetting damage from the down-round dilution and anti-dilution is usually larger.
- **Existing preferred that participates in the down round.** Takes the mark on the existing shares (some of that mark is offset by the anti-dilution recalculation, which increases their as-converted count on the existing shares). Adds new capital at the lower per-share price, which gives them a lower average per-share cost basis and better economics on a subsequent recovery. Preserves whatever rights (seniority, protective provisions) the pay-to-play preserves.
- **Existing preferred that does not participate in the down round.** Takes the mark on the existing shares, gets the anti-dilution recalculation (partial offset), does not get the lower-cost-basis new-money shares, and — if pay-to-play fires — loses seniority (converted to a lower-preference class or to common), loses protective provisions, and loses pro-rata rights. This is the specific incentive pay-to-play creates.

The CFO's first job is to run the pro-forma waterfall under each combination of "who participates and who does not" and to understand which existing investors will find it economically attractive to participate and which will not. That determines what pay-to-play actually accomplishes when applied to this specific stack.

## Pay-to-play — mechanics

**The concept.** In a down round, the incoming lead conditions the closing on the existing preferred participating in the new round pro-rata (or up to some defined threshold). Existing preferred that participates keeps its rights; existing preferred that does not participate loses defined rights per the pay-to-play mechanic in the charter amendment.

**The load-bearing consequence.** The most common formulation is: non-participating existing preferred is **converted to common** (or to a "shadow" preferred class with 1x preference but no participation, no anti-dilution, no protective provisions, no pro-rata). The non-participant has lost the economics of seniority. If the company sells for the amount of the preference stack, the non-participant now recovers pro-rata as common, not preferentially — and the participants recover their preference first. If the company is doing well later, the non-participant has been meaningfully punished for having declined to write the down-round check.

**The variants.**

- **Full conversion to common.** The strongest version. Non-participants become common. Loses all preferred rights.
- **Conversion to a shadow preferred.** A slightly softer version. Non-participants keep 1x liquidation preference (as protection against ending up with zero in a low-value sale) but lose participation rights, anti-dilution, and other protective provisions.
- **Pro-rata threshold.** Non-participation is defined as failure to invest a specified fraction of pro-rata (often 50% or 75%), rather than any short-fall from full pro-rata. Softer than "any short-fall triggers."
- **Time-limited.** Pay-to-play applies to this specific round; if the same investor participates in the next round, rights are restored. Or the reverse: pay-to-play is a durable feature of the charter that applies to every subsequent down round. The durable version is unusual and aggressive.

**The charter mechanics.** Pay-to-play lives in the Amended and Restated Certificate of Incorporation. On closing of the down round, the charter is amended to add the pay-to-play trigger (or to activate a dormant pay-to-play clause that was in the earlier charter). Existing preferred votes to approve the amendment (class vote required per protective provisions); the pay-to-play conversion happens by mechanical operation of the charter at closing, based on which existing preferred wrote checks that closed alongside.

The vote itself is the choke point. Existing preferred with protective-provision veto over the amendment can block the pay-to-play — but blocking the amendment blocks the closing, and blocking the closing means the company runs out of cash. The CFO's job is to walk each existing preferred through the pro-forma waterfall so that they understand the economic reality: participating in the down round preserves value; blocking closes the doors.

**The negotiation dynamics.**

- The incoming lead pushes for the strongest possible pay-to-play (full conversion to common, no thresholds). The lead's incentive: the fewer existing investors that participate, the more of the new round the lead can allocate to itself, and the more damaged the existing non-participant preferred stack becomes, giving the incoming lead a cleaner top-of-stack position.
- The existing preferred pushes for the softest possible version (shadow preferred, high thresholds, time-limited). Their incentive: some existing investors physically cannot invest (fund life ended, allocation used up, LP restrictions) and don't want to be punished for that.
- The founder / CFO is in the middle. The interest is in closing the round (which requires the lead to be satisfied) and in not damaging relationships with existing investors that will still be around after the round.

The typical negotiated outcome is a shadow-preferred version with pro-rata threshold at 50% or 75%. That gives non-participants a 1x-preference floor while still creating meaningful punishment for defection.

## Senior-preference stacking — mechanics

**The concept.** In a typical Series-A → Series-B priced-round sequence, the new series is either **pari-passu** with the earlier series (they share the same "1x preference paid first" tier) or **senior** to it (the new series is paid its preference before the earlier series receives anything). The NVCA default at Series-B is pari-passu. In a down round, the new lead frequently demands **senior** preference — the new money is paid out first in a sale, ahead of the existing preferred, and only after the new lead is fully paid does the earlier preferred begin to recover.

**The consequence.** In a low-to-medium-value exit (a sale in the range of one to two times the total preference stack), senior preference means the new lead recovers substantially or entirely and the existing preferred and common recover very little or nothing. In a high-value exit, senior preference is less material — everyone is above the preference stack and the difference between senior and pari-passu is small.

**Stacked seniority.** If the down round is a Series-C after existing Series-A pari-passu and Series-B pari-passu, and the incoming Series-C demands seniority, the stack looks like this in a sale:

1. Series-C preference paid first (senior).
2. Series-A and Series-B preferences paid next (still pari-passu with each other, junior to Series-C).
3. Any participation (if applicable) paid.
4. Common (including any converted preferred that opted-in to conversion because their as-converted value beat the preference recovery).

Successive down rounds can stack further seniority — a distressed Series-D senior to a distressed Series-C senior to Series-A/B — and the cap table becomes a queue of preference tiers where the common holders at the bottom see almost nothing in most exit scenarios.

**The negotiation dynamics.**

- The incoming lead pushes for senior preference and often for a **multiple** (2x, 3x, sometimes higher) to compensate for the perceived risk. A 3x senior preference on a $30M down-round Series-B means the lead has to recover $90M before anyone else receives a dollar.
- The existing preferred pushes for pari-passu with the new round, or at least for the new round's seniority to apply only to a bounded portion. Fully-diluted, the existing preferred typically would prefer to be pari-passu with the new lead (protecting their exit economics) than to be senior over the common (which would be defensive but of limited value in a down-round trajectory).
- The founder / CFO's interest is to keep the preference multiple at 1x. Even senior preference at 1x is far less punishing to common than participating preference or multi-x preference.

The typical negotiated outcome in a distressed round is 1x senior non-participating for the new lead, pari-passu among the existing preferred series, with pay-to-play conditioning the preservation of the existing pari-passu status. That structure gives the new lead the priority they need to underwrite the deal and gives the participating existing preferred a preservation of value; the non-participating existing preferred takes the mark.

## Anti-dilution interaction

The anti-dilution mechanics from [mod-108 chapter 4](../mod-108-term-sheets-and-preferred-stock-economics/04-anti-dilution-broad-based-narrow-based-full-ratchet.md) fire automatically in any down round. The existing preferred's conversion price is reduced per the formula in the charter (broad-based weighted-average is standard; narrow-based or full-ratchet is aggressive), which increases the as-converted share count of existing preferred and further dilutes the common.

**Pay-to-play interacts with anti-dilution.** A common pattern:

- The existing preferred with anti-dilution normally gets the recalculation automatically in a down round, whether or not they participate.
- A pay-to-play charter provision conditions the anti-dilution recalculation on participation. Existing preferred that does not participate loses not only seniority but also loses the anti-dilution recalculation. The as-converted count for non-participants stays at the pre-down-round level; they are diluted both by the down-round issuance and by their inability to convert at the new lower price.

That double-punishment is what makes a "pay-to-play with anti-dilution forfeiture" combination such a strong tool for compelling existing preferred participation. It is also the mechanic that experienced founder-side counsel will fight hardest against, because it stacks the punishment for defection well past what the "loss of seniority" alone accomplishes.

**Under a full-ratchet regime** (rare — mostly a legacy artefact), the down round can be catastrophic for common. The full-ratchet resets the existing preferred's conversion price to the new-round per-share price, which for a materially-lower down-round price can dramatically increase the existing preferred's as-converted share count. The founder-and-common ownership can collapse under a full ratchet applied at a stress-priced down round. This is the single most important reason the CFO fights for broad-based weighted-average anti-dilution at the original financing.

## Next-round price interaction

A down round sets the market price of the company at the down-round pre-money. That new price becomes the reference the *next* round is priced against. The specific consequence:

- **Anti-dilution on the down round itself.** The incoming lead's preferred stock will have anti-dilution — usually broad-based weighted-average — that will fire in the next round if the next round is also a down round. The incoming lead's preferred is protected on the downside.
- **The next-round lead's underwriting.** A next-round lead looks at the current-round price as one data point in the price they will pay. A round priced through a stress-driven down round can be discounted further by the next lead as "the market for this company is fragile" — the next round can end up priced even below the current down-round price if the KPIs have not recovered.
- **The signalling of stress.** The next-round lead reads the down round as a market signal about the company. Recovery is possible, but the KPIs have to show it materially — a strong ARR reacceleration, an NRR improvement, a gross-margin turnaround — before the next lead is willing to price above the down-round level.

The CFO's job is to price the current down round realistically. Setting the down-round price too high (in an attempt to soften the mark) creates a false floor that will be violated at the next round; setting it too low compresses the founder's ownership needlessly. The reference points for the pricing are: current KPIs (revenue multiple against the current-quarter comparable-company data — Meritech, Bessemer Cloud Index, mod-106), the last-round price and the story of the miss, and the incoming lead's underwriting model.

## The pro-forma waterfall the CFO builds before the term sheet closes

Before a down-round term sheet is signed, the CFO produces a waterfall model that shows, for at least four exit-price scenarios and under each of the negotiated structure combinations:

- Each existing preferred series' recovery.
- The incoming preferred's recovery.
- The common's recovery.
- The specific numeric consequence of non-participation for each existing preferred series (both the seniority loss and — if applicable — the anti-dilution forfeiture).
- The break-even exit price at which non-participation costs each existing investor the check size they would have written to participate.

That last number is the persuasion lever. When a specific existing investor is told "at any exit above $X, your decision to skip this round costs you more than the check would have been," most rational investors reconsider. The CFO's job is to make the number defensible, deliver it in a written memo, and let the arithmetic close the participation gap.

## Common failure modes

- **Modelling the down round without pay-to-play consequences.** A pro-forma waterfall that just assumes everyone participates hides the specific damage to non-participants that makes the mechanic work.
- **Accepting narrow-based or full-ratchet anti-dilution at the original financing to unlock a cheaper priced round.** The down-round consequence is measurable in real dilution to common. Broad-based weighted-average is the market-standard for a reason.
- **Structuring the down round without a pay-to-play when the incoming lead's underwriting depends on it.** The lead closes without alignment mechanics; some existing investors free-ride; the round takes longer and closes at worse terms than a well-structured pay-to-play version.
- **Setting the pay-to-play threshold too high or too low.** Too high (100% pro-rata) will punish investors who physically cannot participate (fund life issues) and creates enemies for no strategic gain. Too low (10% of pro-rata) makes the trigger meaningless.
- **Accepting multi-x senior preference to close a down round.** The multi-x preference has a large economic cost that will not become visible until the exit. If the alternative to multi-x is the round not closing at all, the CFO may have no choice — but the CFO's job is to make sure that trade is understood, not silently signed.
- **Not communicating the mechanic to the broader employee base.** Down rounds and pay-to-play mechanics are traumatic for the option-holding team; the CFO who says nothing while a stressed round closes signals to the team that the leadership is not owning the situation. Chapter 4 covers the communication practice.

## What good looks like

A CFO who has this material installed:

- Produces the pro-forma waterfall under all negotiated structure combinations before the term sheet is signed.
- Walks each existing preferred investor through the specific economic consequence of participation vs. non-participation in a written memo.
- Negotiates pay-to-play down to a "shadow preferred with 50% pro-rata threshold" or similar defensible middle position.
- Fights hardest for 1x senior non-participating on the incoming preferred (avoids multi-x and participation) and pari-passu on the existing preferred if the alternative is stacked seniority across many rounds.
- Models the anti-dilution effect explicitly and communicates it (especially the pay-to-play-plus-anti-dilution-forfeiture double effect) to the existing preferred.
- Prices the down round realistically against current KPIs and the current-quarter market data, not aspirationally against the last round.
- Coordinates the communication cascade — board, existing preferred, employees, hires-in-flight — so no stakeholder learns of the down round through a leak or through diligence documents.

## Summary

- A down round re-triggers anti-dilution on existing preferred, re-runs the preference stack, and re-shapes founder / common ownership through both mechanisms.
- **Pay-to-play** conditions preservation of existing preferred rights (usually seniority, sometimes anti-dilution) on participation in the down round pro-rata (or above a threshold). Non-participants are converted to common or to a shadow preferred with reduced rights.
- **Senior-preference stacking** places the new preferred ahead of the existing preferred in the sale waterfall. In distressed rounds, incoming leads often demand seniority; the CFO's fight is to keep the multiple at 1x and to preserve pari-passu among the existing series where possible.
- The anti-dilution mechanics fire automatically; a pay-to-play with anti-dilution forfeiture creates a double-punishment for non-participants that is the strongest lever for compelling participation but requires careful negotiation.
- The CFO's pre-signing artifact is the pro-forma waterfall showing each investor's consequence of participation vs. non-participation across exit scenarios. The break-even exit price at which non-participation costs more than participation is the persuasion lever.
- Common failure modes: understating the mechanic in the model; accepting multi-x preference to close; setting the pay-to-play threshold poorly; leaving employees uninformed. Chapter 4 covers the recapitalisation, cram-down, and common re-up work that often accompanies the down round.

Chapter 4 turns to the harder cases where a down round with pay-to-play is not enough — full recapitalisations that collapse the existing preference stack, cram-downs of holdout investors, and the common-employee re-up grants that restore team economics after either mechanic fires.
