# Convertible Notes — Principal, Interest, Maturity, and Why Notes Are Not SAFEs

## Why this matters

A convertible note is the older cousin of the SAFE and, at first glance, its close functional analogue: both are seed-stage instruments that convert into preferred stock at the next priced round at a discount and/or valuation cap. The similarity ends at the first structural detail. A convertible note is **debt** — it carries principal, interest, and a maturity date, with the legal consequences that follow. A SAFE is a contract that carries none of those.

That single structural difference (contract vs. debt) is why the note is more dangerous for the founder. If a SAFE never converts, nothing happens — the SAFE holder is disappointed and eventually gets paid out at dissolution behind creditors. If a note never converts because the qualified financing never happens, the note *matures*. Maturity is a default event unless the parties do something about it: the noteholder can demand repayment (which most seed startups cannot fund), force conversion at a fallback price (which is typically punitive to the founder), or extend the note (which requires the noteholder's consent and often costs the founder more equity).

Notes are less common at seed today than they were pre-2013 and much less common than SAFEs — but they still show up on real cap tables, especially in:

- **Bridges between rounds.** Priced-round bridges are often structured as notes with a discount to the next round rather than SAFEs. Chapter [mod-109](../mod-109-runway-management-and-bridge-financing/) covers the runway-management framing.
- **Investor-preferred structures.** Some investors prefer the interest accrual and the maturity-date leverage of a note over the contract nature of a SAFE.
- **International jurisdictions.** In several countries (UK, Canada, Australia) the SAFE has not fully displaced the note; some funds still default to notes.
- **Second-time-founder rounds.** More sophisticated founders sometimes prefer notes for tax reasons (interest may be deductible) or for the negotiating dynamics.

This chapter installs the note anatomy. Chapter 4 stacks notes alongside SAFEs at the priced round. Chapter 7 handles the failure modes of notes that mature.

## The four terms that define a note

A convertible note is defined by the interaction of four terms — five if you count the conversion mechanics that overlap with the SAFE from chapter 1.

### Principal

The face amount of the loan. Straightforward. $500K principal is a note where the noteholder wired $500K to the company at closing and the company owes them (at least) $500K plus accrued interest at any point before conversion or repayment.

### Interest rate

Notes carry a stated interest rate — typically 4-8% simple interest per annum, sometimes compounded quarterly or annually. The two mechanical questions:

- **Does the interest convert into equity along with principal, or is it paid in cash at conversion?** Almost always the former: at conversion, the noteholder receives shares equal to `(principal + accrued interest) / conversion price`. The interest is "converted" as if it were additional principal.
- **What is the compounding convention?** Simple interest at the stated rate is the default in most templates; some templates specify quarterly or annual compounding. On an 18-month note at 8% simple, `$500,000 × 0.08 × 1.5 = $60,000` of accrued interest converts alongside the principal. On the same terms with annual compounding: `$500,000 × 1.08 × 1.04 = $561,600`, or effectively $61,600. The difference is small in the short term but grows if the note extends past maturity.

Interest accrual matters because it turns the note's economic value into a moving target. A $500K note at 8% is $560K after 18 months, $600K after 30 months, and so on. If the priced round is delayed, the noteholder's implied ownership at conversion grows by the interest rate every year. This is a founder-adverse property that a SAFE does not have (a SAFE's implied ownership is fixed at the moment the SAFE is signed and does not grow with time).

### Maturity

The date on which, absent conversion or extension, the note becomes due and payable in full. Typical seed-stage maturity is 18-24 months from closing; some templates go to 36 months and some go as short as 12. Maturity is the load-bearing risk of a note: the SAFE has no maturity, so the founder has no time pressure. The note has one, so the founder does.

The three canonical outcomes at maturity:

- **The qualified financing (QF) closes on time.** The note converts at the QF into preferred stock per the SAFE-like discount/cap mechanic. This is the intended outcome and the one most founders assume will happen when they sign.
- **The QF does not happen and the maturity date passes.** The note is now in default (or in a technical default that has been contractually deferred). What happens next is what the note says happens next — typically one of:
  - **Repayment in cash.** The noteholder demands repayment of principal + accrued interest. Most seed-stage companies do not have this cash on hand. If they do not pay, the noteholder has a debt claim they can pursue in court (unlikely) or use as leverage to negotiate an alternative outcome.
  - **Automatic conversion at maturity into common stock at a formula price.** Some notes contain a "conversion at maturity" clause that fires the note into common (not preferred) at a pre-negotiated fallback price or valuation. This is founder-adverse both in economics (the note takes a large slug of common) and in cap-table structure (common with no preferred protections attached).
  - **Automatic conversion at maturity into preferred stock at a formula price.** Better for the noteholder than common; still punitive to the founder relative to a QF conversion because the pre-negotiated fallback price is typically lower than what a real priced round would set.
  - **Extension.** The parties amend the note to push maturity out (typically another 6-18 months), often in exchange for a better cap, a higher discount, or a higher interest rate for the note. This is the most common real-world outcome for notes that reach maturity without a QF.
- **A change of control (acquisition) happens before maturity.** The note usually pays out at a defined premium — often `1x principal + accrued interest` plus a change-of-control premium (2x is a common number, sometimes higher for early notes) — as a cash payment ahead of common. Some notes convert into common at a defined valuation instead.

Read the "maturity" and "change of control" clauses of every note on your cap table. The maturity clause defines what happens at hour zero of maturity + 1 second; the change-of-control clause defines what happens at exit. Both matter.

### Qualified financing threshold

A qualified financing (QF) is defined in the note as the priced-round event that triggers automatic conversion. The typical definition is: **a preferred-stock financing raising at least $X of new money**. `$X` is the "qualified-financing threshold" and is typically set at a level the parties expect the intended next round to clear — $1M for a Seed-to-Series-A bridge, $5M for a Seed round that follows a small pre-seed note, $10M for a Series-A note that pre-dates a Series-B.

A financing that raises less than the QF threshold does not trigger automatic conversion. The note holder then has a choice, defined in the note:

- **Convert voluntarily at the sub-QF financing price** (with the discount/cap applied).
- **Decline to convert and wait for the next QF-qualifying round.**

The distinction matters because a company that closes a small "friends and family" bridge as a preferred round for $500K is not, under a $1M QF threshold, triggering the note. If the noteholder wants to convert into that small preferred round they can, but they can also stand on their note and wait.

## The conversion price — a note is a SAFE plus interest plus maturity

Under normal QF conversion, the mechanic mirrors a SAFE with cap and discount:

- The note's principal + accrued interest at the conversion date is the "investment amount" for purposes of the conversion.
- The note has a valuation cap and/or a discount (same taxonomy as a SAFE — cap only, discount only, cap + discount).
- The conversion price is `min(QF price × (1 - discount), cap-implied price)`, exactly like the SAFE mechanic.
- The number of preferred shares issued is `(principal + accrued interest) / conversion price`.

The one wrinkle: whether the cap is pre-money or post-money. Historically, convertible notes used a **pre-money** valuation cap analogous to the pre-money legacy SAFE. In the post-2018 world, some notes have followed the SAFE into post-money framing and some have not. Read the definition in the note before you compute anything. The correct calculation follows [chapter 1](01-yc-post-money-safe-anatomy-and-four-variants.md) or [chapter 2](02-pre-money-legacy-safe-mechanics-and-conversion.md) depending on which mechanic the note uses.

## Worked example — QF conversion, cap + discount note

Setup:

- Note: $500,000 principal, 6% simple interest per annum, 24-month maturity, 20% discount, $8,000,000 pre-money cap.
- Closing date: 1 January 2025.
- QF: Series-A closing on 1 January 2026 (12 months later) at $15,000,000 pre-money / $5M raise. Pre-money FD (before the note converts, with pool top-up) = 10,000,000 shares. QF threshold = $1M.
- $5M raise exceeds the $1M QF threshold, so the note converts.

**Interest accrual.** 12 months at 6% simple = `$500,000 × 0.06 × 1.0 = $30,000`. Note value at conversion = `$530,000`.

**Conversion price.**

- Priced-round price = `$15,000,000 / 10,000,000 shares = $1.50 per share`.
- Discounted priced-round price = `$1.50 × 0.80 = $1.20 per share`.
- Cap-implied price (pre-money cap of $8M on 10,000,000 pre-money FD-ex-note shares) = `$8,000,000 / 10,000,000 = $0.80 per share`.
- Conversion price = `min($1.20, $0.80) = $0.80`. Cap controls.

Note this is the same iterative-solve wrinkle as chapter 2 — the cap-implied price technically depends on the note's own converted share count if the cap is treated as a post-money-of-note-conversion base, but for a pre-money cap on the pre-money FD excluding the note, the calculation is direct.

**Note-holder shares.** `$530,000 / $0.80 = 662,500 shares` of Series-A preferred.

**Note-holder percentage of the post-QF-conversion company (before new money):** `662,500 / (10,000,000 + 662,500) = 6.22%`.

**Compare with a SAFE at the same terms.** A post-money SAFE at $500K investment on an $8M post-money cap would give the SAFE holder `$500,000 / $8,000,000 = 6.25%` of the post-conversion company (before new money). Very similar percentages — the difference is the interest accrual on the note (30,000 / 500,000 = 6% of the note's investment, moved into the note-holder's share) and the fact that the cap is a pre-money cap here versus a post-money cap on the SAFE.

The economic content is close. The **risk profile** is not.

## Worked example — maturity without a QF

Same note. Assume 24 months pass and no priced round has closed. Interest accrual = `$500,000 × 0.06 × 2 = $60,000`. Note value at maturity = `$560,000`.

The note's maturity clause typically offers one of three outcomes:

**Outcome A — repayment demand.** The noteholder demands $560,000 in cash. The company has $200,000 in the bank and a 6-month runway. It cannot pay. The noteholder now has:
- A debt claim they could pursue in court. Practically, this is the "nuclear option" — the noteholder usually does not want to bankrupt the company, since the payout from bankruptcy is typically zero for unsecured seed-stage debt.
- Leverage to demand terms in an extension.

**Outcome B — automatic conversion at maturity at a fallback formula.** Some notes specify that on maturity, the note converts into common (or preferred at a stated valuation) at a fallback conversion price. If the note says "at maturity the note converts into common stock at $5M valuation on a fully-diluted basis," the conversion price is `$5,000,000 / 10,000,000 FD = $0.50 per share`. Note-holder shares = `$560,000 / $0.50 = 1,120,000 shares of common`. That is 10.1% of the post-conversion FD (11,120,000 shares) — a materially larger slice than the 6.22% they would have gotten at the QF at the $8M cap. And it is common, which means it does not carry preferred protections; but for the founder, the note-holder now holds common at a much lower effective price than the founder paid at formation.

**Outcome C — extension.** The parties amend the note. Typical amendments:
- Push maturity out 12 months.
- Increase the discount from 20% to 30% (or raise the interest rate to 10%, or lower the cap to $6M).
- Sometimes accompanied by a small pro-rata rights side letter.

Outcome C is the most common real-world outcome for a seed-stage note that reaches maturity. The founder pays for the extension in equity terms.

## Why notes are riskier for founders than SAFEs

Distilling the mechanical differences:

- **Maturity pressure.** A SAFE has no deadline; a note has one, and the deadline is a real trigger with real consequences. Founders sign notes assuming a QF will happen before maturity; a material fraction of the time, it doesn't.
- **Interest accrual.** A note's implied conversion price gets more favourable to the noteholder every year that passes without conversion. A SAFE's implied conversion price is fixed.
- **Debt characterisation.** In an acquisition or dissolution, note-holders are creditors and stand ahead of both preferred and common in the waterfall. SAFE holders stand ahead of common but behind creditors — and are usually treated as economically equivalent to preferred at a hypothetical priced round for waterfall purposes.
- **Bankruptcy exposure.** Notes can precipitate an involuntary bankruptcy filing if the company cannot repay at maturity and the noteholder chooses to press the claim. This is rare in practice but the possibility affects the negotiating leverage of an extension.
- **Tax and accounting treatment.** Notes are debt on the balance sheet, which affects debt covenants (if any), venture-debt facility eligibility, and the interest deduction (which is generally allowable for the company). SAFEs sit in a category the FASB has not authoritatively addressed as of the last codification update — see [`resources.md`](resources.md) — and are usually classified as equity or as a component of equity on the balance sheet.
- **Fewer subordination protections.** A note taken as unsecured debt is *pari passu* with other unsecured debt of the company; a subsequent venture-debt facility from SVB or a similar lender may require the seed noteholder to subordinate, and that negotiation happens with the noteholder from a position of leverage the SAFE holder never has.

## When a note makes sense despite the risks

For all the above, notes still occupy specific niches where they beat SAFEs:

- **Bridge financings between two known priced rounds.** The maturity date lines up with the expected close of the next priced round; the QF threshold is set at the expected round size; the note is priced with a discount to force conversion at the next round. The founder-adverse maturity risk is small if the next round is genuinely imminent.
- **Investor preference.** Some investors (particularly non-YC-network funds and international funds) still prefer notes for institutional reasons. Turning down their money over the instrument choice is rarely the right call.
- **Tax planning.** In some jurisdictions the interest on a note is deductible to the company, adding a small tax benefit that SAFEs do not provide. In the US the deduction is typically de minimis at seed stage and often not worth the complexity.
- **Regulatory / audit context.** Some auditors (particularly non-Big-Four firms in early-audit engagements) are more comfortable with notes than SAFEs because the debt classification is unambiguous.

## Common founder traps with notes

- **Signing a note with a maturity you don't have a plan to hit.** If you sign an 18-month note in month 6 of your fundraise and the priced round doesn't close by month 24, you are in an extension negotiation from a weak position.
- **Setting the QF threshold too high.** If the QF is $5M but the next preferred round is a $2M bridge, the note doesn't convert. The company then has *two* notes on the table (the original plus the new bridge), and the maturity clock on the original is still running.
- **Not modelling the accrued interest at conversion.** The $500K note at 8% for 30 months converts as if it were $600K. If the cap-table model assumes the note converts at $500K principal, the founder is short 20% of a note's worth of shares at close.
- **Assuming the maturity clause is boilerplate.** It is not. The maturity conversion clauses vary widely: common vs. preferred, at what fallback price, with what noteholder consent right. Read every note.
- **Signing a note without an intercreditor arrangement in mind.** If the company later takes venture debt, the seed noteholder may be asked to subordinate. If the note is silent on that, the negotiation happens live.
- **Treating the discount and the interest rate as substitutable.** They are not: the discount is applied to the priced-round price at conversion, so it scales with the priced-round valuation. The interest rate is applied to the principal, so it scales with the amount and the elapsed time. A 20% discount on a $2.00 priced-round price is worth $0.40 per share; the interest at 8% on $500K for 24 months is $80K, or roughly $80K / $500K = 16% additional shares. These are the same order of magnitude but they compound differently.

## What good looks like

A CFO or founder authoring or holding a note:

- Uses a standard template — the NVCA convertible-note precedent or a well-known investor template — with counsel red-lining for the specific closing, rather than a bespoke draft.
- Sets a QF threshold that matches the expected next-round size, not a hopeful stretch number.
- Sets a maturity date that leaves a buffer of at least 6 months past the expected priced-round close, so an extension negotiation is not always imminent.
- Maintains a note register (chapter 4) with per-note principal, interest rate, closing date, maturity date, QF threshold, cap (pre- or post-money), discount, and current accrued interest.
- Runs a maturity-forecast every quarter: "if the priced round does not close by X, we are in maturity discussions with these note-holders on the following dates."
- Has a written maturity-extension policy: what the company will offer (typically a modest cap reduction, a modest interest rate bump, and maturity extension of 12 months) and what it will not (typically not "convert to common at a low common price," which reshapes the cap table more than the founder appreciates).
- Reports notes on the cap table on an as-converted basis at the current cap and discount, with principal + accrued interest as the dollar input, not just principal.

## Summary

- A convertible note is debt: principal, interest, maturity, with the legal consequences that follow. It differs structurally from a SAFE (which is a contract, not debt) even though the conversion mechanic at a QF is essentially the same.
- The four terms that define a note are principal, interest rate (typically 4-8% simple), maturity (typically 18-24 months), and the QF threshold. The cap and discount at conversion overlay these terms with the same taxonomy as a SAFE.
- At a QF, the note converts at `(principal + accrued interest) / min(discounted QF price, cap-implied price)`, mirroring the SAFE mechanic with the extra interest layer.
- At maturity without a QF, the note becomes due. The three canonical outcomes are repayment demand (usually infeasible for a seed startup), automatic conversion at a fallback formula (usually founder-adverse), and extension (the most common outcome, typically at a cost to the founder in equity terms).
- Notes are riskier for founders than SAFEs primarily because of maturity (a hard deadline), interest accrual (implied ownership grows with time), and debt characterisation (creditor status in the waterfall, potential bankruptcy exposure).
- Notes still make sense in specific niches: bridges between priced rounds, investor-preferred structures, some international jurisdictions, and some audit/regulatory contexts. Outside those niches, the SAFE dominates.

Chapter 4 stacks these instruments — five SAFEs plus a note — into a single priced-round conversion and walks the pro-forma calculation the CFO produces before closing.
