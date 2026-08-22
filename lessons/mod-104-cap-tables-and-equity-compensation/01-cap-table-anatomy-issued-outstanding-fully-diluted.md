# Cap Table Anatomy — Issued vs. Outstanding vs. Fully Diluted

## Why this matters

A cap table is the ledger of who owns the company. Almost every downstream question a CFO answers — *what is the founder's stake after Series-B, what does an exit at $180M return to common, does this hire's grant fit inside the pool, does this SAFE convert into dilution the last investor did not price* — reads off the cap table. If the cap table is wrong, every one of those answers is wrong.

The founder-authored cap table a Series-A diligence firm sees most often is a single-sheet common-and-preferred split with an ESOP row underneath and a running "total shares" column that does not tie to the corporate record. The pool is sized in percent but not converted to shares. Two SAFEs from the seed round are represented as `$500K @ $8M cap` in a footnote rather than as an as-converted share count. A warrant issued to a venture-debt lender is not represented at all. The counsel-hosted stock ledger (typically inside Carta, Pulley, or LTSE Equity — or a signed spreadsheet stapled to board consents at the earliest stage) shows different numbers to the CFO's cap-table tab. When the diligence attorney asks the CFO to reconcile the two, the CFO cannot, because the CFO's cap table was never designed to tie to the corporate record.

This chapter installs the anatomy that makes the cap table a defensible artefact: the four share-count conventions (authorised, issued, outstanding, fully diluted), the classes of security that appear on it (common, preferred by series, options issued and options-pool-reserved, warrants, SAFEs and convertible notes stacked as-converted), and the reconciliation to the corporate record that separates a cap table from a spreadsheet with numbers on it. Every subsequent chapter — pre-vs.-post-money math, pool top-ups, waterfall, 409A, equity comp — assumes this anatomy exists and holds.

## Ownership boundary — economics vs. policy

Before the mechanics: this module owns equity *economics*. Dilution math, option-pool math, waterfall analysis, 409A methodology, tax-preference mechanics — all live here. Equity-comp *policy* — grant guidelines by level and function, refresh cadence, promotion grants, IC-plan structure, the philosophical debate over whether engineers get more equity than sales — defers to [`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum). Where those two collide (e.g., a grant-guideline decision that requires a pool top-up), this module owns the pool math; that module owns the guideline itself.

## The four share-count conventions

Every share number in a cap table is one of four things. Confusing them is the single most common error a founder makes.

- **Authorised shares.** The maximum number of shares of a given class the company is legally permitted to issue, per the certificate of incorporation. Authorised is a ceiling, not an ownership number. A Delaware C-corp incorporated at formation typically authorises 10,000,000 shares of common stock; that number is amended (via a filed certificate of amendment) at each priced round to make room for the new preferred series and for pool top-ups. Delaware charges a franchise-tax fee that scales with authorised-share count under the default method — the reason many startups elect the assumed-par-value method instead.
- **Issued shares.** The shares the company has actually sold or granted to a specific holder. Issued shares can subsequently be repurchased and held in treasury, at which point they are issued but not outstanding.
- **Outstanding shares.** Issued shares less treasury shares — the shares currently in the hands of a holder (founders, employees who have exercised, investors). This is the number that votes and that receives dividends and liquidation distributions.
- **Fully diluted shares.** Outstanding shares plus every share that could come into existence if every convertible, exercisable, or vestable security were converted, exercised, or vested at that moment. That includes: outstanding options (vested and unvested), the unissued portion of the option pool (the reserved-but-not-granted headroom), outstanding warrants, and every SAFE or convertible note on an as-converted basis.

The founder trap is quoting one number and computing dilution against another. "The engineer's 0.5% grant" is usually 0.5% of fully diluted at grant. The Series-A investor's "20% of the company" is 20% of post-money fully diluted, including the topped-up pool. The founder's own ownership stake is best tracked as a percent of fully diluted, because that is the number that will show up on the diligence deck at the next round.

Every cap table has a header block that names, in shares, the total under each convention. If those four numbers are not visible on the top of the sheet, the cap table is not defensible.

## The classes that appear on the cap table

A modern venture-backed cap table has, at maximum, these classes. A pre-seed company might have three (founder common, employee common, option pool). A Series-C company might have all of them.

**Founder common stock.** Issued at formation for a nominal price (fractions of a cent per share), usually with a vesting schedule and a repurchase right if the founder leaves before vesting completes. Founder shares are almost always the subject of an 83(b) election (chapter 7), which locks in the tax basis at the low grant price.

**Employee common stock issued via option exercise.** When an employee exercises a vested option, the underlying common stock is issued to the employee (they pay the strike price × number of shares to the company; the company issues the shares). Post-exercise, those shares behave like founder common — they vote, they participate in liquidation, and if the employee leaves, they retain them subject to a company-side repurchase right at fair market value in some plans.

**Preferred stock, by series.** Each priced round issues a new series of preferred stock (Series Seed, Series A, Series B, etc.). Each series has its own certificate-of-designation entry in the certificate of incorporation and its own set of terms — liquidation preference, dividend rate, conversion ratio, anti-dilution formula, voting entitlements, protective provisions. The cap table lists each series as its own row (or block of rows if multiple closings). The NVCA model financing documents (see resources) are the reference certificate structure most rounds follow with red-line variations.

**Outstanding options.** Options that have been granted to a specific holder — vested or unvested — and are counted on a fully-diluted basis. Options are contracts on top of the pool; they are not shares until exercised. The cap-table entry lists each grant with grant date, quantity, strike price, vest schedule, and expiration date, or (more commonly on the CFO's rolled-up view) a per-plan aggregate with a link to the underlying grant register.

**The unissued option pool.** The pool reserved by the board for future grants but not yet granted to a specific person. On a fully-diluted basis, the pool counts as if it were already granted and outstanding, because it will be, and the mechanic that will dilute existing holders is the granting event, not the reservation. The pool is a **placeholder line on the fully-diluted view** — an important line and one whose sizing is contested at every priced round (chapters 2 and 3).

**Warrants.** A contract to buy shares at a fixed price for a defined period. Issued to venture-debt lenders (e.g., SVB, TriplePoint), sometimes to strategic partners as part of a commercial arrangement, and occasionally to advisors. Warrant coverage on a venture-debt facility is typically quoted as "1% warrant coverage on the loan amount" — 1% of the loan value in warrants, struck at the current preferred price, exercisable over a 7-10 year window. Warrants count on a fully-diluted basis and their strike-price mechanics are relevant to waterfall analysis (chapter 4).

**SAFEs and convertible notes, as-converted.** The most common cap-table modelling error at seed stage. A SAFE is a right to shares of the next preferred round at a discount or valuation cap; a convertible note is the same plus interest and maturity mechanics (see [`mod-105`](../mod-105-convertible-instruments/)). Neither is stock. But both will *become* stock at the next priced round, and both dilute the founder and the pool at that conversion. The right treatment on the cap table is an **as-converted view** — the number of preferred shares each SAFE / note would produce if it converted right now at its cap or discount, whichever is more favourable to the holder, and against the current pool. That "as-converted" line goes into the fully-diluted total and is the number the founder should track their own stake against, not the pre-conversion outstanding number.

## Common cap-table failure modes at seed

The following failure modes are what a diligence attorney flags first, in the order they usually appear:

- **The pool is quoted in percent, not shares.** "10% option pool" tells you nothing without the fully-diluted denominator, and the fully-diluted denominator moves when you convert the SAFEs and top up the pool. The pool must be in shares.
- **SAFEs are represented as dollar amounts with a footnote.** `$500K @ $8M cap` in the footer is not a cap-table entry. The as-converted share count is.
- **The pool is sized as "issued options only" not "issued + unissued reserve".** The 4% unissued pool from the last round is dilution that has already been suffered by existing holders; it must be in the fully-diluted total or the fully-diluted denominator will be wrong.
- **Warrants are omitted.** Venture-debt warrants, advisor warrants, strategic warrants — none of them are stock but all of them are dilution.
- **The cap table does not tie to the stock ledger.** The corporate record — signed board consents, executed stock-purchase agreements, executed option-grant agreements, warrant instruments — is the source of truth. If the cap-table tab does not tie to it, the cap table is wrong (see the reconciliation section below).
- **Founder shares are quoted as issued but not showing the unvested-repurchase-eligible portion.** A founder with a 4-year vest 18 months in has 62.5% unvested, subject to repurchase at cost if they leave. Diligence will want to see the vesting schedule per founder.
- **Post-conversion pool top-up numbers are not modelled.** At the next priced round the pool will almost certainly be topped up (chapter 3). A cap table that does not carry the model for that top-up in a scenario column cannot answer the "what's my post-round stake" question.

## The as-converted view — worked example at seed

Consider a company with:

- 8,000,000 founder common shares (two founders, 4,000,000 each, vesting over 4 years with 1-year cliff, 12 months in).
- 1,000,000 option-pool shares reserved by the board, of which 200,000 are granted (vested and unvested aggregated).
- Two post-money SAFEs from the seed round: $500K at a $8M post-money cap; $250K at a $10M post-money cap.
- No warrants, no notes, no preferred stock (yet — the SAFEs convert at the next priced round).

The four-number header on the fully-diluted view:

```
Authorised common:                       10,000,000
Issued common:                            8,000,000  (all founder)
Outstanding common:                       8,000,000  (no repurchases yet)

Fully-diluted:
  Founder common (outstanding)            8,000,000
  Options granted (unexercised)             200,000
  Option pool (unissued reserve)            800,000
  SAFEs (as-converted at cap)             see below
  ------------------------------------------------
  Total FD                              [derived]
```

**As-converted SAFE calculation** (post-money SAFEs, standard YC 2018 variant). A post-money SAFE is defined so that the holder owns `investment / post-money cap` of the company on an as-converted post-money basis, before the next priced round dilutes them further.

- $500K / $8M cap = 6.25% of the post-conversion company on the SAFE holder's line.
- $250K / $10M cap = 2.5% of the post-conversion company on the SAFE holder's line.

Total SAFE ownership if converting *now* against the current fully-diluted less-SAFE base (9,000,000 shares — 8M founder + 200K granted options + 800K pool):

- Combined SAFE percentage: 8.75% of the post-conversion company.
- Post-conversion fully-diluted `X`: `9,000,000 + SAFE shares = X`, and `SAFE shares / X = 0.0875`, so `SAFE shares = 0.0875 × X = 0.0875 × (9,000,000 + SAFE shares)`, i.e. `SAFE shares × (1 - 0.0875) = 0.0875 × 9,000,000`, i.e. `SAFE shares = 787,500 / 0.9125 ≈ 863,014`.
- Post-conversion fully-diluted `X ≈ 9,863,014`.

The as-converted view is therefore:

```
Founder common                            8,000,000    81.11%
Options granted                             200,000     2.03%
Option pool (unissued)                      800,000     8.11%
SAFEs as-converted                          863,014     8.75%
  of which $500K @ $8M                      616,438     6.25%
  of which $250K @ $10M                     246,576     2.50%
------------------------------------------------------------
Total fully-diluted                       9,863,014   100.00%
```

The founder's stake — the number the founder actually cares about — is 81.11%, not the 88.89% (8M / 9M) they get by ignoring the SAFEs. This is the number that carries into pre-money vs. post-money analysis at the Series-A (chapter 2).

The post-money SAFE mechanic is deliberately designed to give the founder exactly this "you know what dilution you've already sold" number before the next round. The pre-money legacy SAFE (2013 vintage) does *not* have this property — it dilutes the founder further at conversion in a way the founder frequently doesn't expect. Both variants and their differences are the subject of [`mod-105`](../mod-105-convertible-instruments/).

## Reconciliation to the corporate record

The cap table is a report; the stock ledger and the underlying legal instruments are the primary record. Reconciliation is the mechanic that connects them.

**Every common-stock entry** should tie to an executed stock-purchase agreement (or restricted-stock-purchase agreement) and, for founders, an 83(b) election filed with the IRS within 30 days of the grant (chapter 7). Every purchase agreement has a share count, a per-share price, and a date. The cap-table row references those numbers, not different ones.

**Every preferred-stock entry** should tie to the certificate of incorporation (which declares the class), the certificate of designation (which sets the class's terms), the stock-purchase agreement (which records the sale and the price), and the board and stockholder consents that authorised the issuance. The share count on the cap table equals the sum of shares across those purchase agreements.

**Every option grant** should tie to an executed option grant agreement, a board consent authorising the grant, and a set-of-the-strike-price consent that references the current 409A appraisal (chapter 5). Option-grant registers inside Carta, Pulley, or LTSE Equity live under a per-grant record with those references attached. The cap-table roll-up sums the grant register.

**Every warrant** should tie to an executed warrant instrument. Warrant instruments are stand-alone documents (not part of a purchase agreement); the cap table lists each warrant with holder, share count, strike, expiration.

**Every SAFE / note** should tie to the executed SAFE / note instrument. Since these are debt-like or contractual instruments — not stock — they live off the outstanding-shares view but must be present on the as-converted fully-diluted view with the conversion mechanic that produced the share count spelt out.

A cap-table review before a diligence hand-off runs each of these ties. If any row on the cap table does not point to a specific executed instrument, either the cap table has a phantom row or the corporate record is missing a signed document — and both need to be resolved before the diligence firm finds them.

## The cap table as a growing artefact

At formation the cap table has one row per founder and (usually) a reserved option pool. By the time the company is at Series-B it has:

- Two rows for founder common (each founder, tracked separately).
- Several rows for employee-exercised common (or an aggregated line with a linked register).
- Series Seed preferred, Series A preferred, Series B preferred — each its own row block with its own terms.
- Option grants split across two or three ESOP plans (the original plan and post-round expansions).
- Warrants from any venture-debt facilities.
- Optionally, RSUs (see chapter 7) if the company is late enough that private-company RSUs make sense.
- Potentially secondary-market blocks — shares acquired by later-round investors from earlier employees or founders in a tender offer (chapter 7).

Every priced round adds complexity: a new preferred series, a new pool top-up, a new anti-dilution recalculation on prior series (mod-108), a new pro-rata allocation among existing holders. The CFO's job is to keep the cap table sound as the complexity accumulates — which is the reason the four-number header, the class-by-class breakdown, and the reconciliation-to-record discipline installed in this chapter matter more, not less, at each round.

## Summary

- Every share number on a cap table is one of four things — authorised, issued, outstanding, or fully diluted. Confusing them is the most common founder error.
- The classes on a modern cap table are: founder common, employee-exercised common, preferred by series, outstanding options, the unissued option pool, warrants, and SAFEs / notes as-converted.
- The unissued option pool is dilution that has *already been suffered* by existing holders; it belongs in the fully-diluted total, not as a footnote.
- SAFEs and convertible notes are not stock, but their as-converted share count belongs in the fully-diluted view. The post-money SAFE mechanic — investment ÷ post-money cap — gives the holder a known share of the post-conversion company; the founder's residual is the number to track their own stake against.
- Every row on the cap table ties to a specific executed instrument in the corporate record — purchase agreement, option-grant agreement, warrant instrument, SAFE / note. If a row does not tie, the cap table is wrong.
- The cap table grows in complexity every round; the header discipline, the class-by-class breakdown, and the reconciliation-to-record are what keep it defensible as it grows.

Chapter 2 turns to the pre-money vs. post-money math and the option-pool "shuffle" that determines how a term sheet's fine print translates into dilution the founder feels at the Series-A close.
