# mod-105 — Convertible Instruments

**SAFEs, Notes, and the Cap-Table Impact of Stacking**

**Track:** [Startup Finance & Fundraising](../../CURRICULUM.md)
**Stage:** SEED
**Hours:** 22 (7 chapters + 6 exercises + planned lab + planned quiz)

## What this module installs

By the time a company runs a priced round, most of the cap-table damage that will surface in diligence has already been done — quietly, one convertible at a time, across a seed programme that stretched from a first friends-and-family SAFE to a bridge note eighteen months later. Every one of those instruments is a promise about future dilution, and every one of them behaves differently at the conversion event. This module installs the mechanics.

Specifically:

- The **YC post-money SAFE** as it stands today — the four variants (valuation cap, discount, MFN, cap + discount), the "fixed post-money ownership" property that separates it from the pre-money legacy SAFE, and what that property costs the founder at conversion.
- The **pre-money legacy 2013 SAFE** you still find on real cap tables — how it dilutes the founder *and* prior investors together instead of the founder alone, why that makes stacked-SAFE modelling non-trivial, and how to recognise it so you don't accidentally convert it the wrong way.
- The **convertible note** — principal, interest rate, maturity, discount, cap, qualified-financing threshold, forced-conversion clauses — and the specific risks it puts on the founder that a SAFE does not.
- The **stacking calculation** — five SAFEs at different valuation caps plus a bridge note plus an MFN'd side letter converting simultaneously into a Series-A with a target post-money option pool — and the pro-forma cap table that shows the founder exactly what closes.
- **Side letters and MFN clauses** — the "best terms" back-propagation mechanic that quietly rewrites the cap table, when it triggers, and how to author (or refuse) it deliberately.
- **Reg D** — Rules 504, 506(b), 506(c) — and the accredited-investor / general-solicitation / Form D decision behind every convertible raise you close.
- The **failure modes** — SAFE overhang, mixed pre- and post-money SAFEs on the same table, notes maturing because the qualified financing never happened — and the prescribed remediation for each.

## Chapters

1. [`01-yc-post-money-safe-anatomy-and-four-variants.md`](01-yc-post-money-safe-anatomy-and-four-variants.md) — the current YC post-money SAFE, the four variants (cap, discount, MFN, cap + discount), and why fixed post-money ownership changes the founder's dilution arithmetic.
2. [`02-pre-money-legacy-safe-mechanics-and-conversion.md`](02-pre-money-legacy-safe-mechanics-and-conversion.md) — the 2013 pre-money SAFE, its shared-dilution mechanic, how to spot it on an existing cap table, and how to model the conversion correctly.
3. [`03-convertible-note-mechanics-principal-interest-maturity.md`](03-convertible-note-mechanics-principal-interest-maturity.md) — note structure end-to-end (principal, interest, maturity, discount, cap, QF threshold, forced conversion), and the founder-side risks that make a note not a SAFE.
4. [`04-stacking-multiple-convertibles-priced-round-pro-forma.md`](04-stacking-multiple-convertibles-priced-round-pro-forma.md) — five SAFEs plus a note plus the priced-round option-pool shuffle: how to build and reconcile a pro-forma Series-A cap table.
5. [`05-side-letters-and-mfn-amendments.md`](05-side-letters-and-mfn-amendments.md) — side-letter mechanics, the MFN "best terms" clause, back-propagation of amended terms, and the drafting discipline that keeps an MFN from surprising you.
6. [`06-reg-d-exemptions-504-506b-506c-and-form-d.md`](06-reg-d-exemptions-504-506b-506c-and-form-d.md) — the three Reg D safe harbours, accredited-investor verification, general-solicitation rules, and the Form D filing timeline.
7. [`07-convertible-instrument-failure-modes-and-remediation.md`](07-convertible-instrument-failure-modes-and-remediation.md) — SAFE overhang, mixed pre- and post-money stacks, notes converting at maturity because no QF happened; the specific remediation for each.

## Exercises

1. [`exercises/exercise-01-yc-post-money-safe-authoring-and-conversion-drill.md`](exercises/exercise-01-yc-post-money-safe-authoring-and-conversion-drill.md) — author a post-money SAFE in each of the four variants and compute the conversion into a hypothetical Series-A.
2. [`exercises/exercise-02-pre-money-vs-post-money-safe-cap-table-comparison.md`](exercises/exercise-02-pre-money-vs-post-money-safe-cap-table-comparison.md) — same round, same investors, run both mechanics and quantify the founder-dilution delta.
3. [`exercises/exercise-03-convertible-note-authoring-and-maturity-mechanics.md`](exercises/exercise-03-convertible-note-authoring-and-maturity-mechanics.md) — draft the note terms, model interest accrual, and walk the three maturity outcomes (QF conversion, non-QF conversion, repay-or-restructure).
4. [`exercises/exercise-04-stacked-convertibles-priced-round-pro-forma.md`](exercises/exercise-04-stacked-convertibles-priced-round-pro-forma.md) — build the pro-forma Series-A cap table from a stack of five SAFEs plus a note plus an option-pool top-up, reconciled to the term sheet.
5. [`exercises/exercise-05-side-letter-and-mfn-clause-analysis.md`](exercises/exercise-05-side-letter-and-mfn-clause-analysis.md) — trace an MFN cascade across three closings, redline a problem side letter, and quantify the cap-table impact.
6. [`exercises/exercise-06-reg-d-506b-vs-506c-decision-drill.md`](exercises/exercise-06-reg-d-506b-vs-506c-decision-drill.md) — pick the correct exemption for each of six raise scenarios and author the compliance memo.

## Lab

- `lab-01-end-to-end-seed-programme-to-series-a-close` — planned; walks a founder from first SAFE through a stacked seed programme into a priced Series-A close, producing the full document trail (SAFEs, note, MFN side letters, Form D filings, pro-forma cap table, closing memo). Placeholder to be authored in a subsequent content cycle.

## Quiz

- `quiz-01` — planned; 12-15 questions covering the seven chapter objectives. Placeholder to be authored in a subsequent content cycle.

## Reference

- [`resources.md`](resources.md) — YC SAFE templates, SEC Reg D releases and CFR sections, NVCA model documents, and the practitioner content behind the module.

## How this module fits

Directly depends on [`mod-104`](../mod-104-cap-tables-and-equity-compensation/) — the cap-table anatomy, four share-count conventions, and pre-vs.-post-money math in mod-104 are prerequisites. This module extends the mod-104 as-converted view with the mechanics that produce the "as-converted" shares in the first place.

Directly feeds [`mod-106`](../mod-106-startup-valuation-frameworks/) (valuation frameworks — the valuation-cap in a SAFE is a de facto ceiling on the next round's pre-money), [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/) (fundraising strategy — the choice of instrument shapes the raise), [`mod-108`](../mod-108-term-sheets-and-preferred-stock-economics/) (the priced round that all these convertibles convert into), and [`mod-109`](../mod-109-runway-management-and-bridge-financing/) (bridge notes as an explicit runway-management instrument).

The module *does not* teach: term-sheet negotiation for preferred stock (that is mod-108), the priced-round option-pool shuffle in isolation (mod-104 chapter 2), or the securities-law depth beyond the private-placement safe harbours (that lives outside the track, in the LP-focused legal literature). It teaches the CFO-level mechanics of the instruments themselves and the arithmetic of what they do to the cap table at conversion.
