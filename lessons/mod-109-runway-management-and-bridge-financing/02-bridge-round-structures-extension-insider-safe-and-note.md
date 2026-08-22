# Bridge Round Structures — Extension, Insider SAFE, and Bridge Convertible Note

## Why this matters

A **bridge** is capital raised between priced rounds to extend runway to a specific event — usually the next priced round, sometimes an M&A close, sometimes a specific product or revenue milestone that will unlock a better-priced next round. Almost all bridges are led by an **insider** (an existing investor with pro-rata rights and material stake), because outsiders will discount hard for the signalling risk of a company that is raising interim capital. That inside-led property shapes every dimension of the structure: the price, the instrument, the dilution, and the message the next-round lead reads off the bridge when it lands in diligence.

There are three canonical bridge structures a CFO chooses among: an **extension of the existing preferred class** at the last-round price, an **insider-led bridge SAFE** at a friendlier cap, and a **bridge convertible note** with a maturity date. Each has different signalling, different dilution mechanics, and — critically — a different effect on the next round's price. The CFO's job is to pick the structure that fits the situation, not to default to the one that was easiest to close last time.

Note: this chapter builds on the convertible-instrument mechanics from [mod-105](../mod-105-convertible-instruments/) and the preferred-stock mechanics from [mod-108](../mod-108-term-sheets-and-preferred-stock-economics/). The math of a SAFE at a given cap and the math of an extension at the last-round preferred price are covered there; this chapter is about the choice among structures.

## Structure 1 — Extension of the existing preferred class

**Mechanics.** The company issues additional shares of the existing preferred class (Series A, Series B, etc.) at the same per-share price as the original financing. Existing investors — usually led by the lead of the round being extended — write additional cheques for their pro-rata share; new investors, if any, sign the existing Series-A Stock Purchase Agreement with a "supplemental closing" amendment. The charter does not have to be amended (a new series is not created). Existing preferred rights (liquidation preference, anti-dilution, protective provisions) are unchanged, applied to the new shares at the same multiplier and mechanics.

**Signalling.** The strongest signal a bridge can send. An extension at the last-round price says: "The lead investor and the existing preferred stack believe the last-round price is still fair. We are extending runway because a specific event is coming that will justify a higher price at the next round, not because the company has to raise at whatever it can get." That message reads well in next-round diligence — the next lead sees a company whose insiders were willing to double down at the same price.

**Dilution.** Purely additive at the last-round price. If the extension adds 10% new money against post-money, the founder is diluted by ~10% (adjusted for the option pool and existing preferred). No re-pricing of prior shares, no anti-dilution recalculation.

**Effect on next-round price.** Neutral to positive. The extension establishes a market-tested price floor at the last-round level; the next-round lead has to price above it or explain why the extension was not the right price. The last-round investors, having just added at the price, have a strong incentive to defend it in the next round's negotiation.

**When it fits.**
- The company is meaningfully on plan (or the story of the miss is credible and self-limiting), the last round was priced at a defensible level, and the primary reason for the bridge is timing — a large event (large customer close, product launch, acquisition close) is imminent and worth waiting for.
- The lead of the existing round has capacity in the fund and conviction on the story.
- The extension size is modest — typically 20-40% of the original round, in the range where "extension" is a credible label. Larger sizes look like "we couldn't raise" and start to attract next-round-lead scepticism.

**When it does not fit.**
- The last-round price was materially above what the current KPIs support. The extension at that price would require existing investors to double down at a valuation they no longer believe. Push for a bridge SAFE at a friendlier cap or explicitly re-price via a down round (chapter 3).
- The lead of the last round is a small fund with no dry powder for follow-on. The extension will not be lead-able.
- The company has structural issues (missed critical hires, product delay, retention collapse) that would make the "extension at the same price" story unbelievable at next-round diligence.

## Structure 2 — Insider-led bridge SAFE

**Mechanics.** The company issues one or more YC post-money SAFEs (or, less commonly, pre-money SAFEs — see mod-105 chapter 2) to insiders, usually with a valuation cap set below the last-round post-money and often with a discount to the next priced round. The SAFEs convert at the next priced round on the same mechanics as any other SAFE — cap-vs.-discount-vs.-priced-price, holder picks the better. No charter amendment; no additional preferred class created. Sometimes accompanied by a **side letter** granting the bridge SAFE holders pro-rata rights in the next round (see mod-105 chapter 5 on side letters and MFN).

**Signalling.** Weaker than an extension. The lead is signalling "we are willing to put in more money, but not at the last-round price." A bridge SAFE at a cap below the last-round post-money is a soft acknowledgement that the company is worth less than the last round said it was, and the next-round lead will read it that way. The signal can be softened by pricing the SAFE at or very near the last-round post-money (essentially an extension in SAFE form) — but that starts to look like an extension done badly (SAFE form when preferred form was available), which sends its own signal.

**Dilution.** Depends on where the priced next round comes in. If the next round prices at or above the SAFE cap, the SAFE holder gets the cap-implied percentage — potentially materially more dilutive to the founder than an extension would have been at the same dollar size. If the next round prices well below the cap, the SAFE holder converts at the priced-round price and the dilution is proportional to the check size.

**Effect on next-round price.** Depends critically on where the SAFE cap sits. A cap materially below the last-round post-money is a soft down-round signal — the next-round lead reads the cap as the market-tested price the insiders were willing to pay and will price against it. A cap at or above the last-round post-money is a neutral-to-positive signal (essentially: "the insiders think the price is at least the last round, but we're leaving room for the next lead to price above").

**When it fits.**
- The company needs a bridge but the last-round price is now clearly high; a small down-cap SAFE lets the insiders participate at a defensible price without triggering an explicit down-round mechanic (pay-to-play, anti-dilution recalc).
- Speed matters. A SAFE closes in days with minimal legal work — no charter amendment, no lengthy SPA drafting, no board consent beyond the standard SAFE authorisation. This can be the difference between a bridge that closes in three weeks and an extension that takes three months.
- The insider set is small and known — one or two existing investors writing checks each. SAFEs are efficient for small closings and become clumsy for a wider syndicate.
- The company is late-seed / early Series-A and the market is used to seeing SAFEs on the cap table.

**When it does not fit.**
- The company is Series-B or later and the market expectation is that bridges are priced-preferred. A SAFE bridge at Series-B is unusual and reads as "the CFO couldn't get a priced extension closed."
- The insider set is large or includes strategic / corporate investors with strict internal-process requirements that don't map cleanly onto a SAFE.
- The next priced round is expected to price at a valuation much higher than the SAFE cap. The cap-implied dilution then becomes material and the "extension-shaped instrument would have been cheaper" retrospective becomes hard to defend.

## Structure 3 — Bridge convertible note

**Mechanics.** The company issues convertible notes to insiders, with principal, an interest rate (typically 4-8% simple, accruing), a maturity date (typically 12-24 months out), a discount to the next priced round (typically 10-25%), and often a valuation cap. On a "qualified financing" (a priced round above a defined threshold), the notes convert per the note terms; at maturity without a qualified financing, the notes come due — either repaid, converted at a defined mechanic, or restructured. Frequently secured by all assets of the company (a UCC filing), giving the note holders a debt-like priority in bankruptcy that the SAFE holders do not have.

**Signalling.** The strongest bear signal of the three. A convertible note in the middle of a bridge says: "The insiders wanted the protections of debt (interest, maturity, security interest) — they were not confident enough in the near-term conversion event to accept the SAFE's equity-shaped risk profile." Well-run companies use notes when there is a specific and defensible reason (a mid-way milestone that determines conversion terms, a bridge-to-M&A situation where the note is expected to be repaid at close), and this reason should be stated up front in the memo to the next-round lead.

**Dilution.** Similar to the SAFE at conversion — cap or discount picks the better price, and the holder converts at that price plus accrued interest converting into shares as well. Additional dilution comes from any warrants attached to the note (common in "bridge note plus warrants" packages that give the noteholders an equity kicker in exchange for the debt risk).

**Effect on next-round price.** The note's cap or discount sets the effective floor on the founder's share of the next round. If the note has an aggressive discount (25% or more) or a cap materially below the last round, the next-round lead reads both as a price signal against the founder's story.

**When it fits.**
- The bridge is explicitly to a defined event with a defined price mechanic — most commonly a bridge to an M&A close, where the note is expected to be repaid at closing (with interest) and the maturity date is set inside the expected close window.
- The insider set wants explicit repayment optionality — the ability to be paid back cash, not converted to equity, if the situation changes. This is common when the insiders are family offices, sovereign or corporate strategics with debt-oriented internal frameworks, or when the CFO wants to leave open the option of repaying from a debt facility drawn later.
- The company has known future revenue milestones or product certifications that will materially change the pricing of the next round, and the note's discount is priced to reflect the crossing of that milestone.

**When it does not fit.**
- The bridge is to a normal equity-financed next round and the insiders are conventional VC funds. The note's debt features (interest, maturity, security interest) add complexity and legal cost that a SAFE avoids without adding meaningful value.
- The note's maturity is short and the qualified-financing event is uncertain. The failure mode — notes come due at maturity, no priced round has happened, the noteholders are entitled to demand repayment or renegotiate at leverage — is the specific failure mode the mod-105 chapter 7 warns about. Do not use a note for a bridge whose landing event is uncertain.

## The signalling table

| Structure | Signal | Dilution | Next-round price effect | Legal complexity |
|---|---|---|---|---|
| Extension of existing preferred | Strongest positive — insiders re-price at last round | Linear at last-round price | Neutral to positive (floor at last-round price) | Modest (supplemental closing, no charter amendment) |
| Insider-led bridge SAFE | Mixed — depends on cap vs. last-round post-money | Cap-implied at priced round; can be worse than extension | Cap sets an effective ceiling on next-round pricing conversation | Low (SAFE only, board consent) |
| Bridge convertible note | Weakest — debt features imply insider hedging | Cap or discount plus interest converts to shares | Cap or discount sets floor; interest adds to conversion | Higher (note, security agreement, UCC filing) |

The signalling row is what makes structure choice a first-order decision. The CFO cannot control what the next-round lead reads off the bridge, only which signal they read.

## Deciding — the framework

Work the decision in this order:

**Step 1. Establish the last-round price defensibility.** If the last-round pre-money is still defensible given current KPIs (or the story of any miss is credible), the extension is on the menu. If it is not, the extension is off the menu — the insiders will not double down at a price they no longer believe, and the choice narrows to SAFE (implicit price re-set) or note (with a cap that re-prices).

**Step 2. Establish the landing event.** If the bridge is to a specific and defensible priced next round in the next 6-12 months, the extension or SAFE fits. If the bridge is to a specific M&A event or a specific product / regulatory milestone that will determine whether the next-round price justifies conversion, the note may fit. If there is no specific landing event and the bridge is "let's see how the market recovers," rethink whether a bridge is even the right tool — the runway extension may need to come from cost cuts or from venture debt (chapter 5), not from a bridge that has no defined resolution.

**Step 3. Establish the insider set.** If the lead of the last round has follow-on capacity and conviction, the extension is closable. If not, the SAFE or note is closable with a smaller check-writing set but at a signalling cost the CFO has to price.

**Step 4. Establish the speed constraint.** If the bridge has to close in three weeks (imminent payroll risk, imminent M&A close), the SAFE wins on legal-work speed. If the timeline is normal (6-8 weeks), any of the three is deliverable.

**Step 5. Establish the size.** Small (10-25% of the last round) fits any structure. Medium (25-50% of the last round) fits extension or SAFE. Large (>50% of the last round) is not a bridge — it is either a full priced round that should be marketed as such, or the company is in a distressed situation where the down-round mechanics of chapter 3 apply.

## Documentation the CFO produces

For any bridge, the CFO produces a package that:

- **The bridge memo.** Two to three pages, addressed to the CEO and the board. Covers: reason for the bridge, size, structure choice with the reasoning (walked through the framework above), target investor(s), target close date, expected dilution range, expected next-round-price effect. This is the document the board approves in the bridge consent.
- **The pro-forma cap table.** Post-bridge cap table under two scenarios: (a) next priced round closes at expected valuation; (b) next priced round closes at a stressed valuation. Both scenarios show the SAFE / note conversion math and the resulting founder and insider ownership. Reconciled to the current cap table.
- **The board consent.** The board authorises the bridge (issuance of new preferred shares under an existing series; authorisation of the SAFE issuance; authorisation of the note and any security agreement). Standard consent, one page plus the term-sheet or SAFE form as exhibit.
- **The investor communication.** A short update to the broader investor list (existing preferred, angel investors) explaining the bridge, the structure, and the pro-rata rights that will apply to their participation. Pro-rata rights matter here — existing investors have rights that the CFO cannot ignore even in an insider-led bridge, and the CFO who runs a bridge without offering pro-rata (where required) is creating a governance problem.
- **The updated capital plan.** The post-bridge cash-out date, the new distance to the trigger points, and the updated next-round timeline. Slotted back into the runway-planning artifact from chapter 1.

## Common failure modes

- **Choosing SAFE for legal-work speed when an extension was appropriate.** The SAFE at a lower cap looks like a soft down-round signal; the extension at the last-round price would have signalled strength. Cost: measurable in the next round's negotiation dynamics.
- **Not offering pro-rata to eligible existing investors.** Existing preferred with pro-rata rights (per the IRA — see mod-108 chapter 5) are entitled to participate in the bridge on standard terms. Skipping them for speed or convenience is a governance failure that will surface in next-round diligence when the missed investors flag it.
- **Using a note when there is no defined landing event.** The maturity clock starts and the CFO ends up managing it in twelve months with the same problem the bridge was supposed to solve.
- **Sizing the bridge as "just enough."** A bridge that lands the company back at 3-6 months of runway if the next raise slips leaves no margin. Sizing to 9-12 months of post-bridge runway is the discipline.
- **Not reconciling the bridge with the option pool.** A bridge that dilutes the option pool below the level needed to support the next-round hiring plan creates a downstream problem — the next round will require an option-pool top-up that dilutes existing shareholders (including the bridge participants).
- **Assuming the bridge will not affect the next round's valuation.** A cap on a SAFE and a discount on a note both set economic anchors that the next-round lead will price against. The bridge is not neutral; the CFO's job is to know what price it locks in.

## What good looks like

A CFO who has this material installed:

- Chooses the bridge structure deliberately, walking the five-step framework and defending the choice to the CEO and board in writing.
- Sizes the bridge for 9-12 months of post-bridge runway, not for "just enough to close the next round."
- Offers pro-rata rights to all entitled existing investors in the bridge, on standard terms.
- Produces the pro-forma cap table under multiple next-round-price scenarios before the term sheet is signed.
- Anticipates and documents the signalling effect the bridge will have on the next-round negotiation, so the CEO and the next-round lead see the same reading.
- Closes the bridge with legal work proportional to the instrument (fast for SAFE, careful for note, standard for extension) and does not over-engineer for a small, insider-only closing.

## Summary

- A bridge is capital between priced rounds to extend runway to a specific event; almost all bridges are insider-led.
- Three canonical structures: extension of existing preferred, insider-led bridge SAFE, bridge convertible note.
- Each has a different signal (extension = strongest positive; SAFE = mixed; note = weakest), different dilution mechanics, and a different effect on next-round pricing.
- The decision framework: last-round price defensibility → landing event → insider set → speed → size.
- The CFO produces a bridge memo, a pro-forma cap table under stressed and expected next-round-price scenarios, the board consent, the investor communication, and the updated capital plan.
- Common failure modes: choosing SAFE for speed when an extension fit; skipping pro-rata; using a note without a landing event; sizing too tight; ignoring the signalling and pricing effect on the next round.

Chapter 3 turns to the harder case — the situation where the bridge conversation is no longer available because the last-round price cannot be defended and a down round is the honest next step. That chapter covers pay-to-play mechanics, senior-preference stacking, and the anti-dilution interaction the CFO models in advance.
