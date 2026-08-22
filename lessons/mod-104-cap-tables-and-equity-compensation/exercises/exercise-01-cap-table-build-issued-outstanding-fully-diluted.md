# Exercise 01 — Cap Table Build: Issued, Outstanding, Fully Diluted

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 1 (cap table anatomy).

## Problem statement

Build a complete cap table for a hypothetical (or anonymised real) startup at a point in time where the company has raised at least one seed round and stacked at least two SAFEs, has issued some options, and has at least one warrant outstanding. Produce the four share-count views — authorised, issued, outstanding, fully diluted — and reconcile the fully-diluted view against a set of underlying "corporate record" documents you either draft or reference.

The exercise is the muscle-memory equivalent for cap tables that Exercise 01 in [`mod-101`](../../mod-101-startup-accounting-foundations/exercises/exercise-01-cash-vs-accrual-three-statement-drill.md) is for cash-vs.-accrual: after this drill you should be able to read any startup's cap table (Carta screenshot, spreadsheet, or diligence PDF) and immediately identify what the four numbers are, where the SAFEs land, and which rows do or don't tie to specific instruments.

## Scenario — build your own

Pick either a real company you have direct knowledge of (with anonymised numbers) or construct a hypothetical with the following minimum shape:

- Delaware C-corp incorporated 24-36 months ago.
- Two founders, each with a restricted stock grant, each on a 4-year / 1-year cliff schedule, both currently 12-24 months into vesting.
- One equity incentive plan (equity plan, ESOP) with at least 15 grants issued and at least one grant that was forfeited when an employee left before vesting.
- At least one grant that was **early-exercised** with an 83(b) election filed (chapter 7 preview).
- At least one **Post-Money SAFE** (YC 2018 variant) and at least one **Pre-Money SAFE** (the 2013 legacy variant) both outstanding — enough to force you to model both mechanics.
- One **priced Seed round** already closed (Series Seed preferred, 1x non-participating, standard terms).
- At least one **warrant** outstanding — either a venture-debt lender warrant (e.g., 1% coverage on a $1M SVB facility struck at the Seed preferred price) or an advisor warrant.
- Currency-wise: keep everything in one currency (USD) at whole-share resolution — no fractional shares.

If constructing a hypothetical, keep the numbers small enough that a manual reconciliation is tractable. Suggested rough shape: 10M authorised common, 8M founder-issued, 1.5M pool reserved, ~200K options granted, two SAFEs of $500K-$1M each at $8-15M caps, priced Seed of $1-2M at $10-15M pre-money, warrant coverage 25K-100K shares.

## Requirements

Produce a single spreadsheet workbook (Excel, Google Sheets, or Numbers) with the following tabs:

1. **Cover / README tab.** Company name, date, author, cap-table conventions used, table of contents.
2. **Corporate record register.** One row per instrument (formation charter, certificate-of-designation for Series Seed, each SAFE, each note, each warrant, each option-grant-agreement or a link to the grant register, each restricted-stock-purchase agreement, each board / stockholder consent that authorised each issuance). For each: instrument type, date, holder, share count (or as-converted share count), price, and — critically — the specific document reference (or fictional document number).
3. **Grant register.** One row per option grant: grantee name (or anonymous ID), grant date, quantity, strike price, vest schedule, vesting-commencement date, expiration date, status (outstanding / exercised / forfeited / expired). Include the early-exercised grant with the 83(b) date noted.
4. **SAFE / note register.** One row per SAFE or note: investor, instrument type (post-money / pre-money SAFE / convertible note), investment amount, cap, discount, MFN flag, date signed, current status. Include a per-SAFE **as-converted share count** column computed at the current pre-money fully-diluted denominator, using the correct mechanic for post-money vs. pre-money SAFEs.
5. **Warrant register.** One row per warrant: holder, shares, strike, expiration, exercise conditions.
6. **Cap-table summary tab.** The four-number header (authorised, issued, outstanding, fully diluted). Then a class-by-class breakdown showing, for each class:
   - Class name (Founder Common, Employee Common (exercised), Series Seed Preferred, Options Granted, Option Pool (unissued), Warrants, SAFEs (as-converted), Convertible Notes (as-converted)).
   - Share count.
   - Percent of outstanding.
   - Percent of fully diluted.
7. **Reconciliation memo (max one page).** For each row on the cap-table summary, cite the specific instrument in the corporate record register that supports it. Flag any row that cannot be tied to a specific instrument.

## Starter guidance

- **Build the corporate record register first.** Every downstream number ties to it. If you invent a founder stock grant, invent the corresponding "restricted stock purchase agreement" reference — even a fictional document ID (RSPA-001, dated 15 Feb 2024) is fine, as long as it's referenced from the cap-table summary.
- **Compute the two SAFE conversions carefully.** The post-money SAFE mechanic is `investment / post-money cap = % of post-conversion company` on the SAFE holder's line. The pre-money SAFE mechanic is `investment / pre-money cap = % of pre-conversion company`, which then gets diluted by the priced round itself. If your as-converted computation gives the same answer for both types, you've made an error — the two mechanics produce different share counts even at the same cap and investment amount.
- **Do not use a Carta / Pulley / LTSE export as a shortcut.** Build the cap table yourself. The point is to see every line.
- **The fully-diluted view includes the unissued pool.** Don't accidentally leave it as a footnote.
- **Warrants count on fully-diluted.** Even if they're not currently exercised, they'd be exercised at exit or before, so they're in the FD denominator.
- **The founder vesting status is a diligence item.** Show unvested / vested for each founder as of the cap-table date, even if all shares are issued and outstanding.

## Acceptance criteria

- **The four-number header is present** at the top of the cap-table summary. All four numbers reconcile (issued = outstanding + treasury; fully diluted = outstanding + granted options + unissued pool + warrants + SAFEs / notes as-converted).
- **Every row on the cap-table summary ties to a specific instrument** in the corporate record register. No orphan rows.
- **Both SAFE mechanics are correctly implemented.** The post-money SAFE holder gets `investment / cap` of the post-conversion company (before priced-round dilution); the pre-money SAFE holder gets `investment / cap` of the pre-conversion company (with the pool and priced-round then diluting them further).
- **The unissued pool is on the fully-diluted view**, not just the outstanding view.
- **Warrant share count is on the fully-diluted view.**
- **The reconciliation memo cites specific instrument references** for every cap-table row, and flags any row that cannot tie.
- **A reviewer can trace any share number** on the cap-table summary back through the class breakdown, through the register, to a specific document reference in under 60 seconds.

## Deliverables

- The workbook (.xlsx or Google Sheets link) with all seven tabs.
- The one-page reconciliation memo (Markdown or PDF), or a memo tab in the workbook.

## Extensions (optional)

- Add a Series A priced round scenario column showing the pro-forma cap table after the SAFEs convert and the round closes with a $10M raise on a $30M pre-money valuation. Compare the founder's ownership before and after.
- Introduce a deliberate error (a warrant omitted, a SAFE misconverted, an option grant not recorded) and demonstrate that the reconciliation-memo tie-back catches it.
- Add a `founder vesting` sub-tab showing each founder's vested / unvested split by month for the next 24 months, with an accelerator-eligible carve-out (single-trigger vs. double-trigger).
- Model a warrant exercise and show the resulting cap-table shift (warrant becomes common; APIC increases by strike × shares; fully diluted stays the same but outstanding increases and unexercised warrant count decreases).
