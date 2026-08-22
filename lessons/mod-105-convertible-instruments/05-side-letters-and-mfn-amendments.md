# Side Letters and MFN Amendments — The Back-Propagation Mechanic

## Why this matters

A SAFE (or a note) is a standard-form document; the negotiation happens in three places. The first is the cap and discount inside the SAFE itself. The second is the choice of variant (chapter 1). The third — and the one that most quietly rewrites the cap table — is the **side letter**: a separate one-to-three-page document attached to the SAFE that adds obligations the SAFE itself does not.

The most consequential clause a side letter carries is the **Most-Favoured-Nation (MFN)** clause: a "best terms" provision that entitles the earlier holder to elect the terms of any later convertible the company issues. The MFN sounds like a courtesy — you're giving the earlier investor a guarantee that no later investor will get a better deal you don't share with them. In practice the MFN is the mechanism by which a founder's third or fourth SAFE closing can retroactively rewrite the terms of the first, changing every earlier holder's conversion economics in ways the founder may not model until the priced-round pro-forma surfaces it.

This chapter installs the MFN mechanic — how it triggers, what it adopts, how far it back-propagates, and how to author (or refuse) it deliberately. It also covers the other common side-letter clauses (pro-rata rights, information rights, board observer rights) so the founder knows which side letters are safe to sign and which reshape the deal.

## What a side letter is

A side letter is a separate signed document that supplements a SAFE or note. It is executed between the same parties (the company and the specific investor) at the same closing. It sits alongside the SAFE in the corporate record. It does not amend the SAFE itself; it adds obligations of the company to that specific investor.

The typical seed-stage side letter is one to three pages and contains some combination of:

- **Pro-rata rights** — the right to participate in the next priced round pro-rata to the SAFE holder's implied ownership at that round.
- **Information rights** — the right to receive quarterly or annual financial statements, a budget update, an annual investor letter, or (at the more-invasive end) monthly board packages.
- **Board observer rights** — the right to attend board meetings without voting (usually granted to a lead seed investor).
- **Most-Favoured-Nation (MFN) clause** — the back-propagation mechanic described below.
- **Other custom provisions** — anti-transfer restrictions, ROFR (right of first refusal) on secondary sales, redemption rights (rare in SAFEs), specific reporting obligations, or a specific representation from the founder.

Some SAFE variants (the YC MFN-only SAFE, variant 3 from chapter 1) contain the MFN inside the SAFE form itself. In that case there is no separate side letter needed for the MFN specifically — but the mechanic is the same.

## What the MFN clause says

The typical MFN clause reads (paraphrasing across common drafts):

> If, prior to the Equity Financing that would trigger conversion of this SAFE, the Company issues any other SAFE, convertible security, or similar instrument, then upon written notice from the Investor, this SAFE shall be amended to reflect the terms of the subsequent instrument, provided that the Investor may elect to adopt any subset of such terms.

Read that carefully. Three properties matter:

1. **The MFN is elective, not automatic.** The MFN-holder has to send notice. If they don't send notice, the earlier SAFE keeps its original terms. In practice, the MFN-holder will send notice if adopting the later terms is more favourable. They will not send notice if the later terms are worse.
2. **The MFN-holder can pick which terms to adopt.** They are not required to adopt the entire later SAFE — just the terms they prefer. That means an MFN-holder can adopt a later SAFE's lower cap while ignoring its higher interest rate (in a note context) or its lack of pro-rata rights.
3. **The MFN triggers on any later "SAFE, convertible security, or similar instrument"** — but the specific language matters. Some drafts say "SAFE"; some say "convertible security"; some say "similar instrument." A tighter drafting limits the trigger; a looser drafting sweeps in every note and every future convertible.

The MFN typically expires at the priced round. Once the earlier SAFE has converted into preferred stock, the MFN is spent — future convertibles the company issues (perhaps a bridge note later) cannot retroactively amend the already-converted preferred.

## Worked example — the MFN cascade

Set up:

- SAFE 1 — $250K at $10M post-money cap. MFN active on this SAFE (either variant-3 or a cap-only SAFE with an MFN side letter).
- SAFE 2 — $500K at $8M post-money cap. Signed 3 months after SAFE 1. No MFN.
- SAFE 3 — $500K at $5M post-money cap with a 20% discount. Signed 6 months after SAFE 1. Institutional investor with negotiating leverage.

The chronology:

**At the SAFE 2 closing.** SAFE 2's terms are cap $8M, no discount. SAFE 1's original terms were cap $10M, no discount. Adopting SAFE 2's $8M cap gives SAFE 1 holder more shares per dollar (`$250K / $8M = 3.125%` vs. `$250K / $10M = 2.5%`). SAFE 1 holder sends MFN notice; SAFE 1 is now cap $8M, no discount.

**At the SAFE 3 closing.** SAFE 3's terms are cap $5M with 20% discount. Adopting the $5M cap gives SAFE 1 holder even more shares (`$250K / $5M = 5%`). SAFE 1 holder sends notice again (typically drafters allow one notice per new instrument). SAFE 1 is now cap $5M with 20% discount.

Total effect: a founder who thought they had sold "$250K at $10M cap" (a 2.5% slice of the post-conversion company) at the first closing has, at Series-A time, sold "$250K at $5M cap + 20% discount" (a slice that is now 5%+ of the post-conversion company, and where the discount could push it higher if the priced round happens above the cap). The founder has been diluted an additional 2.5 percentage points on the first SAFE alone by having granted an MFN.

The math compounds across SAFE holders who all have MFN. If SAFE 1, SAFE 2, and SAFE 4 all had MFN, they would each adopt the SAFE 3 terms at SAFE 3's closing. Each one's post-conversion percentage rises. All of the extra dilution falls on the founder.

## When the MFN doesn't trigger — the founder-side lever

The MFN triggers only when the later instrument is more favourable to the MFN-holder. That gives the founder a specific structural lever: **do not issue later instruments that are more favourable to earlier holders than what the earlier holders already have**. Concretely:

- If SAFE 1 is at $10M cap and SAFE 2 needs to close at $8M cap for the new investor's cheque, the founder is stuck — the MFN will trigger. The negotiation lever is either to raise SAFE 2's cap to $10M or higher (not always possible; the new investor may refuse) or to buy out or amend SAFE 1's MFN before closing SAFE 2.
- If SAFE 1 is at $10M cap and SAFE 2 is at $12M cap, no MFN triggers. The founder has raised the ceiling on the later closing without disturbing the earlier one. This is why later closings at *higher* caps are structurally easier — they don't trigger anyone's MFN.
- The one-way-only property of the MFN means the founder's cap sequence should ideally be *monotonically non-decreasing*: each SAFE should have a cap at least as high as any earlier SAFE with an active MFN. Any decrease triggers the MFN and dilutes the founder additionally.

**Rebalancing an MFN before closing a new SAFE.** If a lower-cap later SAFE is unavoidable and an earlier MFN would trigger badly, the founder can:

- Negotiate to remove the MFN from the earlier SAFE. This usually requires the earlier holder's consent and typically costs the founder something — often a slightly lower cap on the earlier SAFE (which the earlier holder would have gotten from the MFN anyway) or a specific concession like pro-rata rights.
- Buy out the earlier SAFE. Convert it into a preferred issuance at a computed price or pay it out in cash. Rare at seed but possible.
- Ask the new investor to write their cheque at the earlier SAFE's cap. Difficult if the new investor is a real institutional check writer with their own valuation view; sometimes possible for smaller angel cheques.

## The MFN vs. the "pull-through" MFN — a specific drafting subtlety

Some MFN clauses back-propagate only when the earlier holder elects. Other MFNs — sometimes called "pull-through" or "automatic" MFNs — amend the earlier SAFE automatically without requiring election.

The automatic MFN is more dangerous to the founder because there is no gap between the trigger and the amendment. The founder cannot negotiate a workaround at the moment the later SAFE closes because the earlier SAFE has already changed. The elective MFN gives at least the possibility of a negotiation between the trigger and the notice.

The YC MFN-only SAFE (variant 3 from chapter 1) uses an elective mechanic. Non-YC drafts sometimes use an automatic mechanic. Read the specific clause on the specific SAFE before assuming which mechanic applies.

## The pro-rata rights side letter

The pro-rata rights side letter is the second most consequential seed-stage side letter after the MFN. Its content:

- The company agrees to offer the SAFE holder the opportunity to purchase, at the priced-round terms, their pro-rata share of the priced round to maintain their post-conversion ownership percentage.
- "Pro-rata" is defined as the SAFE holder's post-conversion percentage at the moment of the priced round.
- The obligation is one-way — the company must offer; the SAFE holder is not obligated to buy.

**The founder-side considerations:**

- **Institutional seed leads almost always ask for pro-rata rights.** Refusing usually costs the deal. Angels sometimes ask; friends-and-family rarely do.
- **Pro-rata rights change the round-size calculation** at the priced round. If pro-rata rights are outstanding across a large SAFE stack, a material fraction of the priced round can be absorbed by pro-rata cheques from SAFE holders, leaving less allocation for the lead. Some priced-round leads will want the founder to "waive" some pro-rata rights or negotiate them to a smaller allocation before the priced round.
- **Pro-rata rights are not the same as "super pro-rata"** — the right to invest above one's pro-rata share. Super pro-rata is rare at seed and always the subject of a specific negotiation.
- **Pro-rata rights sometimes carry a "major investor" threshold** — only SAFE holders above a certain investment amount get pro-rata rights. Threshold is typically $50K-$250K. This lets the founder concentrate pro-rata obligations on the institutional cheques and exclude the small angel cheques.
- **Pro-rata rights typically expire** at some point (either at the next priced round when the SAFE has converted and other rights take over, or after a set of rounds — "for the next two rounds only").

## Information rights and board observer rights

Two more side letters worth naming briefly:

**Information rights.** Standard institutional-seed information rights: quarterly financials (unaudited), annual financials (audited if the company has an audit, otherwise unaudited), annual budget, and a per-round investor update letter. The company incurs a modest reporting cost. This is largely benign at seed but scales into meaningful audit and finance-team overhead at Series A and beyond.

**Board observer rights.** A specific investor (usually the largest seed lead) gets the right to attend board meetings without voting. The observer sees the same materials as directors and typically participates in discussion. Costs the founder some independence and privacy of board discussion (some things you might say around a table with just directors, you might not say around a table with an observer taking notes). Usually granted to institutional seed leads.

These side letters do not rewrite the cap table the way MFN and pro-rata rights do. They shape the operational relationship with the investor.

## Side-letter hazards to watch for

A short catalogue of side-letter clauses that show up in real seed drafts and require specific attention:

- **Redemption rights.** Rare in SAFEs but occasionally proposed. The right to demand the company redeem the SAFE (buy it back) after a period, typically 3-5 years, if no priced round has happened. Turns the SAFE into a de facto debt instrument with a soft maturity. Refuse or carve out narrowly.
- **Anti-dilution provisions on the SAFE itself.** The SAFE does not have anti-dilution built in. Some drafts add a broad-based-weighted-average anti-dilution provision that fires on any subsequent SAFE at a lower cap. This is functionally a more-aggressive MFN and should be treated as such.
- **Founder-vesting acceleration triggers.** A side letter clause that requires the founder to accelerate their vesting or subjects the founder to a different vesting schedule at the SAFE holder's option. Almost always a red flag — vesting is founders' business, not investors' business at seed stage.
- **Non-compete or non-solicit provisions on the founder.** A side letter clause that binds the founder personally to non-compete or non-solicit terms. Rare but occurs in "operator-founder" contexts where the SAFE holder was a strategic partner. Read carefully.
- **Assignment restrictions on the SAFE.** The SAFE itself has some assignment restrictions; a side letter may amend them. If it makes the SAFE more transferable than the founder wants (letting the SAFE holder assign the SAFE to a downstream investor without company consent), refuse.
- **"Most favoured nation" on rights, not just economics.** A side letter clause that says "if you grant any subsequent investor better information rights, board observer rights, or transfer rights, we get them too." Similar to the MFN on economics but applied to the operational rights. Rare and worth pushing back on unless the specific investor genuinely warrants it.

## What good drafting looks like

- **MFN is elective, not automatic.** If an MFN is in the deal, insist on an elective one so the founder has a gap to negotiate.
- **MFN triggers on SAFE-shaped instruments only**, not "any convertible security" (which would sweep in bridge notes, warrants, and other things that should be scoped separately).
- **MFN excludes conversion at the priced round.** The MFN should terminate at the equity financing that converts the SAFE. Not mentioning this can leave the MFN running against future preferred issuances, which is not what any of the parties intended.
- **Pro-rata rights have a major-investor threshold** so small angel cheques don't burden the round.
- **Pro-rata rights terminate after a bounded number of rounds** (usually two or three post-conversion).
- **Information rights list a specific bounded set of deliverables** — not "such other information as the Investor may reasonably request," which is a licence to demand anything.
- **Board observer rights carry specific expected-behaviour language** (e.g., subject to confidentiality obligations, may be excluded from executive sessions).
- **A "no side letters not listed here" representation from the company** — the founder tracks the side letters and can honestly represent to a later investor that they are all listed. Missing this makes the "no undisclosed side letters" representation in the priced-round docs unreliable.

## The MFN cap-table impact — quantifying the cost

At the pro-forma stage (chapter 4), each MFN-triggered amendment shifts the effective terms of an earlier SAFE and rewrites its as-converted shares. The cap-table impact of a single MFN can be modeled directly:

- Original terms: SAFE holder gets `investment / original cap` of post-conversion company.
- MFN-adopted terms: SAFE holder gets `investment / lower cap` of post-conversion company.
- Delta on the founder's stake: `investment × (1 / lower cap - 1 / original cap)` percentage points.

For $500K at cap dropping from $10M to $5M: delta = `$500K × (1/5M - 1/10M) = $500K × (0.20 - 0.10) / $1M = 5.00 percentage points`. That is 5 percentage points transferred from the founder to the MFN'd SAFE holder because a later SAFE at a lower cap triggered the MFN. Multiply this across a stack of SAFEs with MFN and the priced-round cap table can look materially different from the "just apply each SAFE's original terms" naïve view.

The CFO's job is to run this quantification before the later SAFE is signed. If the founder is about to close a $500K SAFE at a $5M cap that would trigger a $250K MFN'd SAFE from $10M to $5M cap, the founder is transferring 2.5 percentage points of ownership on that older SAFE alone via the MFN. That may still be the right call — the new $500K is needed for runway — but the founder should know the full cost, not just the visible dilution from the new SAFE.

## What good looks like

A CFO or founder authoring side letters:

- Maintains a **side-letter register** parallel to the SAFE register: per SAFE, whether an MFN is present (and elective vs. automatic), whether pro-rata rights are granted (and at what threshold, with what expiration), whether information rights are granted (and with what deliverables), whether board observer rights are granted, and any custom clauses.
- Runs the **MFN cascade check** before signing every new convertible: is the new cap lower than any active MFN-holder's cap? Is the new discount higher than any active MFN-holder's discount? If yes, model the cascade and price it into the trade before signing.
- Prefers **elective MFN** over automatic and **scoped MFN triggers** ("SAFE at a lower cap or with a discount, but not any other kind of instrument") over broad triggers.
- Sets **major-investor thresholds** on pro-rata rights to concentrate the pro-rata obligation on the institutional cheques.
- **Reads every side letter every time.** The template convergence at YC is real for SAFEs; it is much weaker for side letters, where every institutional seed fund has their own preferred draft.
- Runs the "no undisclosed side letters" representation honestly at the priced round. If there is an MFN in a side letter, the pro-forma has to reflect it; the diligence firm will find the side letter and reconcile it against the pro-forma.

## Summary

- A side letter is a separate document attached to a SAFE that adds obligations of the company to that specific investor. The most consequential side-letter clause is the MFN.
- The MFN clause entitles the earlier SAFE holder to elect the terms of any later convertible the company issues, back-propagating the more-favourable terms into the earlier SAFE.
- MFN is typically elective — the earlier holder must send notice — but automatic-MFN drafts exist. Elective is founder-friendlier.
- The MFN mechanic constrains the founder to a monotonically-non-decreasing cap sequence across SAFE closings; any decrease triggers MFNs and transfers ownership from founder to earlier SAFE holders.
- Pro-rata rights are the second most consequential side letter. Institutional seed leads almost always require them; they shape the round-size calculation at the priced round.
- Information rights and board observer rights are the two other common side letters; they are more operational than cap-table-shaping.
- Side-letter clauses that shift the SAFE toward debt-like behaviour (redemption rights, embedded anti-dilution, MFN on rights not just economics) are hazards to watch for.
- The MFN cap-table impact can be quantified as `investment × (1 / lower cap - 1 / original cap)` percentage points shifted from founder to MFN'd SAFE holder. Run this before signing every new convertible.

Chapter 6 turns to Reg D — the securities-law exemption regime under which every one of these SAFE, note, and side-letter closings actually happens.
