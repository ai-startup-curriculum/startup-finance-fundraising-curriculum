# Exercise 03 — Convertible Note Authoring and Maturity Mechanics

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 3 (convertible note mechanics — principal, interest, maturity), chapter 7 (failure modes).

## Problem statement

Draft the full term sheet and instrument body for a $500,000 convertible note issued by a hypothetical seed-stage company, then model three canonical outcomes at maturity: (1) a qualified financing closes on time and the note converts, (2) a qualified financing does not close and the note reaches maturity, and (3) an acquisition happens before maturity. For each outcome, compute the note holder's specific payoff (in shares or cash) and the founder's specific dilution / cash impact. Author a decision memo to the founder recommending whether to sign the note as offered or renegotiate specific terms.

The point of the drill is to internalise that a note is not a SAFE — the maturity clause and the interest accrual are load-bearing terms that shape the founder's downside — and to build the muscle memory to author a note with defensible terms and to negotiate against an over-aggressive draft.

## Scenario — build your own

Construct a hypothetical company at the moment of note signing:

- **Company:** Delaware C-corp, 18 months old.
- **Cap table:** 8,000,000 founder common, 500,000 granted options, 500,000 unissued pool. Pre-note starting FD: 9,000,000 shares.
- **Existing convertibles:** none.
- **Runway:** 12 months at current burn.
- **Expected next milestone:** Series-A raise of $5-8M, expected in 18-24 months.

The prospective note investor offers the following terms:

- Principal: $500,000.
- Interest rate: 8% simple, per annum.
- Maturity: 18 months from closing.
- Discount: 20%.
- Valuation cap: $8,000,000 pre-money.
- Qualified financing threshold: $3,000,000.
- Maturity conversion (if no QF): automatic conversion into common stock at a $4,000,000 fully-diluted valuation.
- Change of control: 2x principal payout (no interest) as cash, ahead of common, in a sale before maturity.

These terms are aggressive on the founder side (short maturity, high interest, low cap, low fallback conversion). Part of the exercise is to identify which of these terms to renegotiate.

## Requirements

Produce a workbook plus a memo with the following:

1. **Note register tab.** All terms of the note as offered, plus the terms as recommended by the memo. Include principal, interest rate and convention (simple vs. compound; day-count), maturity date (absolute date, not just months), discount, cap (pre-money), QF threshold, maturity conversion mechanism, change-of-control premium, and any assignment or subordination provisions.
2. **Interest accrual schedule tab.** Month-by-month accrued interest on the note from signing through maturity + 12 months (to cover any extension). Show the "effective conversion investment" (principal + accrued interest) at each month.
3. **Scenario 1 — QF conversion.** Assume a $5,000,000 raise closes 12 months after note signing on a $15,000,000 pre-money / $20,000,000 post-money valuation with a 10% post-close pool. Compute:
   - Note conversion price (cap-implied vs. discounted QF price; identify controlling mechanic).
   - Note-holder shares.
   - Note-holder percentage of the post-conversion pre-new-money company.
   - Founder percentage before and after the note conversion + priced round.
   - The dollar value transferred to the note holder at the $20M post-money valuation.
4. **Scenario 2 — maturity without QF.** Assume no priced round closes and 18 months pass. Compute:
   - Note value at maturity (principal + accrued interest).
   - Under the maturity conversion mechanism (auto-conversion into common at $4M FD valuation): note holder's share count, percentage of resulting FD, and founder-percentage impact.
   - Under an extension scenario: draft the specific extension terms the founder would offer (typical: extend maturity 12 months, offer a 10-15% cap reduction and/or a 2 percentage point interest bump). Model the resulting note terms and the note-holder's implied percentage if a QF then closes 6 months later at the same terms as scenario 1.
   - Under a repayment scenario: the note holder demands cash. Compute the impact on the company's runway (draw down cash by $500K + interest). Show the resulting runway compression.
5. **Scenario 3 — change of control before maturity.** Assume the company is acquired 12 months after note signing for $30,000,000 in cash. Compute:
   - Note holder's payout under the change-of-control premium (2x principal = $1,000,000).
   - Remaining consideration to be distributed to preferred and common (in this scenario there is no preferred, so all remaining goes to common).
   - Founder payout, employee payout (from vested-common-plus-vested-options assuming standard change-of-control vesting acceleration for the founder), and the note holder's cheque.
   - Compare the note holder's $1M payout to what they would have received if the note had converted at the QF (scenario 1) and the founders had then done the sale — the note holder would have participated pro-rata in the $30M sale as a preferred holder in that alternative.
6. **Decision memo (2 pages).** Written to the founder. Contents:
   - The specific terms of the note as offered, with each aggressive term flagged and quantified.
   - A recommended renegotiated version (typical asks: extend maturity to 24 months for the 12-month buffer past expected Series-A; drop interest to 6%; raise cap to $10M or $12M; raise QF threshold to $2M or $3M; soften the maturity conversion to a "convert at QF pricing to preferred" rather than "convert at $4M valuation to common"; drop the change-of-control premium from 2x to 1.5x or 1x principal + interest).
   - The dollar value of each renegotiated term at the modelled scenarios.
   - A recommendation on whether to sign at all: if the renegotiated terms are still worse than alternatives (SAFE, extending runway some other way), decline.
   - A red-line of the note's maturity clause and change-of-control clause specifically.

## Starter guidance

- **Author the note using a standard template.** NVCA does not maintain an authoritative convertible-note template (they defer to SAFEs and priced-round docs); options include SeedInvest / Republic templates, YC's older convertible-note template, or a template from Cooley, Wilson Sonsini, Fenwick, or Gunderson. Cite the template you used.
- **Use "actual/365" day-count convention** for interest accrual unless the note specifies otherwise. This is the default in most templates.
- **Compute the maturity date as a real date**, not just "18 months." Interest accrues on the actual day count.
- **The QF conversion arithmetic mirrors a SAFE with cap + discount** (chapter 3). Use the mechanic from chapter 3.
- **The maturity-conversion mechanism is the founder-adverse variable.** A well-drafted note either has no automatic maturity conversion (repayment demand only) or converts into preferred at a "reasonable" implied valuation. A note that auto-converts into common at a punitive fallback valuation is the founder-adverse draft.
- **The change-of-control premium** in the offered terms is 2x principal-only. Some drafts use 1x principal + interest, some use 2x principal + interest, some use "greater of X or as-converted." Model the specific number and compare alternatives.
- **The memo should quantify each renegotiation ask.** "Extend maturity to 24 months" is worth `Y dollars of avoided extension-cost expected value` — hand-wave a probability of hitting the QF by month 18 vs. month 24 and multiply by the expected extension cost.

## Acceptance criteria

- **The full note is drafted** using a real template with the specific terms filled in.
- **The interest accrual schedule is correct** and matches at least one independent check (a second computation, or a spreadsheet formula, or a manual verification of one month).
- **All three scenarios are modelled** with per-scenario cash and share outputs for the founder and for the note holder.
- **The QF scenario's cap-vs-discount identification is explicit** and the controlling mechanic is called out.
- **The maturity scenario's three sub-outcomes** (auto-conversion, extension, repayment) are each modelled with founder impact.
- **The change-of-control scenario correctly applies the 2x premium** ahead of common and shows the resulting founder payout.
- **The decision memo makes a specific renegotiation ask** on at least 4 of the 8 terms in the offered note, with each ask quantified in dollar terms at at least one scenario.
- **The red-line is a specific line-edit** of the maturity and change-of-control clauses, not a general description.

## Deliverables

- The workbook with the register, interest schedule, three scenarios, and comparison outputs.
- The drafted note (Word or PDF).
- The two-page decision memo (Markdown or PDF).

## Extensions (optional)

- Add a **second note** at a different closing (say, $250K at same terms but signed 6 months later) and model the two-note stack at maturity and at QF. The two-note case surfaces the "same maturity clock on multiple notes" complexity and is a realistic bridge-financing pattern.
- Model the **cross-default interaction with a venture-debt facility**: assume the company takes a $2M SVB venture-debt facility 12 months after the note signing. Draft the intercreditor / subordination language and show what happens at maturity if the note defaults.
- Add a **noteholder demand for board observer rights** to the note terms and compute the cost to the founder in terms of governance and information rights.
- Compare the **founder outcomes at exit under the note vs. under a SAFE with equivalent economics** (post-money SAFE at the same cap and no interest). Show the differential in the change-of-control scenario, which is where the note vs. SAFE choice most visibly matters.
