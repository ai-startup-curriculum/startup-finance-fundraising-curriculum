# mod-104 — Cap Tables & Equity Compensation

**Dilution, Waterfall, 409A, and the Equity-Comp Toolkit**

**Track:** [Startup Finance & Fundraising](../../CURRICULUM.md)
**Stage:** SEED
**Hours:** 24 (7 chapters + 7 exercises + planned lab + planned quiz)

## What this module installs

The cap table is the ledger of who owns the company. Almost every downstream CFO answer — what is the founder's stake after Series-B, what does an exit at $180M return to common, does this hire's grant fit inside the pool, does this SAFE convert into dilution the last investor did not price — reads off it. If the cap table is wrong, every one of those answers is wrong.

Alongside the cap table sits the equity-compensation regime it services: the 409A appraisal that sets option strike prices, the Rule 701 aggregate-value ceiling that private-company grants must stay under, and the choice among ISO / NSO / RSU / restricted stock that determines the employee's tax outcome and the company's ASC 718 expense. Get these mechanics right and equity is a genuine wealth-creation tool the company deploys to attract, retain, and align. Get them wrong and the diligence attorney at Series-A cannot verify the cap table against the corporate record, the option grants above the Rule 701 cap lose their exemption, and the employee's grant delivers less value than an equivalent cash bonus after tax.

Specifically:

- The **four share-count conventions** (authorised, issued, outstanding, fully diluted) and the classes that appear on a modern venture-backed cap table — founder common, employee common from exercised options, preferred by series, outstanding options, unissued option pool, warrants, and SAFEs / notes stacked on an as-converted basis. The reconciliation to the counsel-hosted stock ledger that separates a cap table from a spreadsheet with numbers on it.
- **Pre-money vs. post-money math** and the **option-pool shuffle** — the fine-print mechanic on the Series-A term sheet that expands the pool pre-money to shield the incoming investor from pool dilution, quietly shifting 2-5% of the founder's stake to the pool at the close. Why the pool expansion is a price cut on the investor's shares, dressed up as a hiring plan.
- **ESOP top-up sizing across rounds** — the seed / A / B / C top-up cadence, the trade-off between over-sizing now (founder pre-dilution) and under-sizing (an emergency top-up at the *old* round's price 12 months later), the Carta / Pave benchmarks by stage, and the between-rounds pool-remaining monitoring the CFO runs against the hiring plan.
- **Liquidation-waterfall analysis** across exit prices and preference stacks — 1x non-participating, participating, capped participation, senior vs. pari-passu preferences, common-only participation floor — and why a "sale price above the last round's valuation" can still shortchange common under a participating stack. Extended in [mod-108](../mod-108-term-sheets-and-preferred-stock-economics/) with the term-sheet negotiation of these clauses.
- **409A methodology** — the fair-market-value determination that ISO / NSO strike prices must be set against, the safe-harbour rules (independent appraisal, illiquid-startup safe harbour, formula methods), the refresh cadence (annual, and on any material event — a priced round, a term sheet, a secondary tender, a change in prospects), and the punitive Section 409A outcome that lands on the *option-holder* when a strike is set below FMV.
- **Rule 701** aggregate-value caps and the **Form S-8 graduation** — the three alternative aggregate limits under the exemption (whichever is largest), the per-grantee disclosure trigger and the rescission-right consequence of missing it, and the point at which the company must either restructure grants or register on Form S-8.
- **The equity-comp toolkit** — restricted stock (founders, 83(b) mechanics), ISO (employee-only, AMT considerations, $100K vesting cap, disqualifying-disposition treatment), NSO (non-employees and consultants, ordinary income at exercise), RSU (late-stage, double-trigger vesting), early exercise programmes, QSBS (Section 1202) planning, and secondary-tender programme design. The decision matrix mapping instrument to employee-lifecycle stage.

## Chapters

1. [`01-cap-table-anatomy-issued-outstanding-fully-diluted.md`](01-cap-table-anatomy-issued-outstanding-fully-diluted.md) — the four share-count conventions, the classes that appear on the cap table, and the reconciliation to the corporate record that makes the cap table a defensible artefact.
2. [`02-pre-vs-post-money-math-and-the-option-pool-shuffle.md`](02-pre-vs-post-money-math-and-the-option-pool-shuffle.md) — the arithmetic of pre-money vs. post-money valuation, the option-pool shuffle mechanic buried in the NVCA term-sheet default, and the founder-dilution consequence of the pre-money treatment.
3. [`03-esop-top-ups-and-pool-sizing-through-rounds.md`](03-esop-top-ups-and-pool-sizing-through-rounds.md) — the pool sizing decision at each round, the seed / A / B / C top-up cadence, the Carta / Pave benchmarks, and the between-rounds pool-remaining monitoring.
4. [`04-liquidation-waterfall-and-preference-stacks.md`](04-liquidation-waterfall-and-preference-stacks.md) — the waterfall arithmetic under 1x non-participating, participating, capped participation, senior and pari-passu stacks; the exit-price crossover points; and the "sale above the last valuation but the common still gets very little" trap.
5. [`05-409a-methodology-fmv-and-refresh-cadence.md`](05-409a-methodology-fmv-and-refresh-cadence.md) — the Section 409A regime, the FMV determination, the independent-appraisal safe harbour, the material-event refresh triggers, and the option-holder-side consequence of a below-FMV strike.
6. [`06-rule-701-caps-and-form-s-8-graduation.md`](06-rule-701-caps-and-form-s-8-graduation.md) — the Rule 701 exemption's three alternative aggregate-value caps, the per-grantee disclosure trigger and its rescission-right consequence, and the Form S-8 graduation decision.
7. [`07-equity-comp-toolkit-iso-nso-rsu-83b-qsbs-secondary.md`](07-equity-comp-toolkit-iso-nso-rsu-83b-qsbs-secondary.md) — restricted stock and the 83(b) election, ISO / NSO / RSU mechanics and tax treatment at each moment (grant / vest / exercise / sale), early-exercise programmes, QSBS planning, and secondary-tender programme design.

## Exercises

1. [`exercises/exercise-01-cap-table-build-issued-outstanding-fully-diluted.md`](exercises/exercise-01-cap-table-build-issued-outstanding-fully-diluted.md) — build a cap table from incorporation through seed with the four share-count conventions visible in the header block, reconciled to a hypothetical counsel stock-ledger (~3h).
2. [`exercises/exercise-02-pre-vs-post-money-option-pool-shuffle-drill.md`](exercises/exercise-02-pre-vs-post-money-option-pool-shuffle-drill.md) — run the same Series-A round under pre-money and post-money pool treatments; quantify the founder-dilution delta; author the counter-offer memo (~3h).
3. [`exercises/exercise-03-esop-top-up-sizing-decision.md`](exercises/exercise-03-esop-top-up-sizing-decision.md) — size the Series-A pool against a hiring plan through the next round, benchmark against Carta / Pave, and author the pool-sizing memo (~3h).
4. [`exercises/exercise-04-liquidation-waterfall-under-multiple-scenarios.md`](exercises/exercise-04-liquidation-waterfall-under-multiple-scenarios.md) — build the waterfall for a Series-A + Series-B stack across seven exit prices under 1x non-participating, 1x participating, and capped-participation preference structures; identify the crossover points; author the founder-facing memo (~4h).
5. [`exercises/exercise-05-409a-methodology-and-cadence-drill.md`](exercises/exercise-05-409a-methodology-and-cadence-drill.md) — walk the 409A appraisal cycle over an 18-month period through two priced rounds and one secondary tender, identifying each material-event refresh trigger and authoring the board-consent memo for each new strike-price adoption (~3h).
6. [`exercises/exercise-06-rule-701-cap-monitoring-drill.md`](exercises/exercise-06-rule-701-cap-monitoring-drill.md) — model the running Rule 701 aggregate-value calculation across a year of grants; identify the point at which one of the three alternative caps binds; author the S-8-or-restructure decision memo (~2h).
7. [`exercises/exercise-07-iso-nso-rsu-vs-83b-decision-matrix.md`](exercises/exercise-07-iso-nso-rsu-vs-83b-decision-matrix.md) — apply the instrument-choice decision matrix across nine employee scenarios spanning founder / early engineer / consultant / late-stage senior hire, and author the grant-package memo for each (~3h).

## Lab

- `lab-01-publish-a-cap-table-and-equity-comp-plan-for-one-startup` — planned; produces the end-to-end cap table from incorporation through Series-B (founder common with 83(b), unissued pool, stacked SAFEs and note, Series-A priced round with the option-pool shuffle, Series-B with a down-round scenario) plus the paired equity-comp plan (ISO / NSO / RSU mix by level, 409A cadence, Rule 701 tracking, secondary-tender design at Series-B) for one hypothetical startup. Placeholder to be authored in a subsequent content cycle.

## Quiz

- `quiz-01` — planned; 12-15 questions covering the seven chapter objectives, including at least one question requiring waterfall arithmetic across a specified preference stack. Placeholder to be authored in a subsequent content cycle.

## Reference

- `resources.md` — planned; the citable primary sources (Delaware General Corporation Law, IRC Sections 409A, 422, 83, 1202, SEC Rule 701 and Form S-8, NVCA model financing documents), the practitioner content (Carta and Pave benchmark reports, Cooley GO, Wilson Sonsini's Term Sheet Generator), and the industry canon behind the module.

## Ownership boundary — economics vs. policy

This module owns equity **economics**. Dilution math, option-pool math, waterfall analysis, 409A methodology, and tax-preference mechanics all live here. Equity-comp **policy** — grant guidelines by level and function, refresh cadence, promotion grants, IC-plan structure, the philosophical debate over whether engineers get more equity than sales — defers to [`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum). Where the two collide (e.g., a grant-guideline decision that requires a pool top-up), this module owns the pool math; that repo owns the guideline itself.

## How this module fits

Directly depends on [`mod-101`](../mod-101-startup-accounting-foundations/) (the accrual-basis financial vocabulary and the ASC 718 stock-based-compensation expense line the equity-comp mechanics feed) and [`mod-103`](../mod-103-three-statement-model-and-driver-based-forecasting/) (the hiring plan whose grant-per-hire assumptions size the pool this module tops up).

Directly feeds [`mod-105`](../mod-105-convertible-instruments/) (the as-converted SAFE and note lines on the cap-table live here; the priced-round conversion in mod-105 rebuilds the cap table this module's anatomy defines), [`mod-108`](../mod-108-term-sheets-and-preferred-stock-economics/) (the term-sheet negotiation of the preference structures whose waterfall math this module installs), [`mod-109`](../mod-109-runway-management-and-bridge-financing/) (down-round mechanics, pay-to-play, and the recapitalisation waterfall against an existing preference stack), and [`project-102-cap-table-and-priced-round-simulation`](../../projects/project-102-cap-table-and-priced-round-simulation/) (the multi-round cap-table simulation that exercises every mechanic in this module against stacked SAFEs and priced rounds).

The module *does not* teach: the term-sheet negotiation of preference-stack clauses (that is [`mod-108`](../mod-108-term-sheets-and-preferred-stock-economics/)), the convertible-instrument mechanics themselves (that is [`mod-105`](../mod-105-convertible-instruments/)), the founder-side tax planning depth beyond QSBS and 83(b) (that lives with individual tax counsel), or equity-compensation *policy* (that defers to [`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum)). It teaches the CFO-level economics of the cap table and the equity-comp regime it services.
