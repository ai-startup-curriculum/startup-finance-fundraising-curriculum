# Exercise 07 — Model Review Checklist and Failure Teardown

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 8 (model failures, review checklist, when to graduate off spreadsheets). All prior exercises (01-06) — you need a working three-statement model to compare a broken one against.

## Problem statement

You will apply the model-review checklist from chapter 8 to a *deliberately broken* three-statement model, diagnose every failure, produce a written diagnosis memo, then rebuild the model so it passes the full checklist. The exercise closes with a *when-to-graduate* memo — the CFO-level written trigger for evaluating whether the spreadsheet should move to an FP&A platform.

The point of the exercise is the pattern-recognition. Reading the checklist teaches you the names of the failure modes; working through a broken model teaches you to *see* them — the symptom that flags each cause, the diagnostic trace, and the fix that survives future scenario changes. This is the fluency a CFO needs before the model leaves for a diligence review.

## Setup — build (or receive) a deliberately broken model

You have two options for the starting artefact:

**Option A — inherit the broken model.** If your instructor, cohort, or study group provides a deliberately broken model, use it. This is the cleanest version of the exercise because you have not seen the injected failures.

**Option B — inject the failures yourself, then have a partner shuffle them.** Take your working model from exercises 01-06 (or a copy of it). Inject at least six of the seven common failure modes from chapter 8:

- **Undocumented circular reference.** Create a cycle (e.g., have the KPI dashboard's growth-rate cell reference back into the P&L's revenue formula, which already references the growth rate).
- **Hard-coded number overwriting a formula.** Type a number into one P&L cell for one specific month, overwriting the formula.
- **Orphan tab or orphan row.** Copy an existing tab (`Cohort_Schedule_v2`), leave it in the workbook but do not connect it to anything.
- **P&L-to-CFS mismatch.** Change the CFS operating-activities net-income row from `=P&L!Net_Income[M]` to a typed number for one month.
- **Opening-balance break.** Type a value into one month's balance-sheet cash cell that differs from the prior month's closing cash cell.
- **Balance-sheet identity failure.** Adjust an asset by $50K without a corresponding liability or equity entry for one month.
- **Version confusion.** Rename the plan-of-record snapshot tab so the dashboard's plan-vs.-actual references break silently.

If you choose Option B, hand the injected model to a partner (or set it aside for 48 hours) so you are diagnosing without full knowledge of every failure's location — the exercise loses its value if you are just retracing what you injected.

## Requirements

Produce four artefacts.

1. **Diagnosis memo.** For each identified failure in the broken model:
   - **Symptom** — what you observed (a check row flagging non-zero, a `#REF!`, a cell whose colour is wrong for its content, a KPI on the dashboard that doesn't match the source tab, a scenario switch that doesn't propagate).
   - **Trace** — the diagnostic steps you took to move from the symptom to the cause. Which formulas you inspected, which `Trace Precedents` / `Trace Dependents` you ran, which cell-range comparisons you made.
   - **Cause** — the specific formula, cell, or reference that was broken and the failure-mode name from chapter 8's taxonomy.
   - **Fix** — the specific change you made to restore correctness. Not just "restored the formula" — the exact formula you replaced it with and why that formula is the correct one.
   Structure the memo as one section per failure, ordered by severity (balance-sheet identity failures first; orphan-tab clutter last).
2. **Rebuilt model.** The broken model with all identified failures fixed. Every reconciliation check green for every forecast month. Every KPI on the dashboard tying to its model source.
3. **Model-review checklist audit.** Chapter 8's full review checklist run against the rebuilt model. For each of the ~35 checklist items, mark PASS / FAIL with a one-line note. Every FAIL is either a failure you didn't catch (go back and diagnose) or a known limitation of the rebuilt model (document as such).
4. **When-to-graduate memo (one page).** The CFO-level written trigger for evaluating whether this specific model — at its current complexity and the company's current stage — should move to an FP&A platform. Structured per chapter 8:
   - Which of the seven signals from chapter 8 are currently present in the model, and with what severity.
   - The written trigger — the specific condition ("3 of 7 signals present for 2 consecutive quarters" or your alternative) that will initiate a platform evaluation.
   - A shortlist of 2-3 candidate platforms from chapter 8's landscape that fit the current stage and complexity, and the reason each is on the list.
   - A shortlist of 2-3 platforms explicitly *not* considered at the current stage, with the reason (too heavy / too rigid / wrong tier).
   - The migration-cost estimate range (order of magnitude — thousands, tens of thousands, hundreds of thousands) for the shortlist.

## The three-part rebuild discipline

Chapter 8's rebuild pattern is more than "fix the symptoms." It is:

- **Fix in the right layer.** A hard-coded number in the P&L is not fixed by typing the "right" number — it is fixed by updating the assumption tab so the formula produces the right number. A P&L-to-CFS mismatch is not fixed by typing the P&L number into the CFS — it is fixed by making the CFS row reference the P&L row so it can never diverge again.
- **Add the check row that would have caught it.** For each failure, ask: what check row would have flagged this if it had existed? A hard-code check (blue cells in a black region), an orphan-tab check (Trace Dependents on every tab's outputs), a closing-vs-opening balance-continuity check. Add the missing check row for future protection.
- **Update the review checklist if the failure isn't covered.** If a failure was not caught by the existing 35-item checklist, the checklist has a gap. Add a new item that would have caught it. This is how the checklist grows over the CFO's career — each real-world failure produces a new checklist row.

## Starter guidance

- **Run the reconciliation checks FIRST.** Chapter 1's three reconciliations (balance-sheet identity, cash tie, retained-earnings walk) plus the opening-vs-closing continuity are the fastest way to localise most failures. Non-zero check cells narrow the search to a specific period and a specific line item.
- **Then run the hard-code scan.** `Ctrl-A` on each calculation tab, `F5` → Special → Constants → Numbers. Every hit in the forecast region is a bug. In the historical actuals region, hits are correct — they are the actuals.
- **Then run the orphan scan.** For each tab, run `Trace Dependents` on the tab's main output cells. If no other tab references any output of a given tab, the tab is orphaned.
- **Then trace the circulars.** Excel status bar shows "Circular references" when iterative calc is disabled; enable iterative calc, then hunt down each cycle with `Trace Precedents`. Every intentional circular must be documented on the cover tab; unintentional ones are broken.
- **Do not fix failures in the order you find them.** Fix the balance-sheet identity failures first — until the balance sheet balances, no downstream check is reliable. Then fix P&L-to-CFS mismatches. Then fix opening-balance breaks. Then hard-codes. Then orphans. Then version confusion. Then intentional circulars documented properly.
- **After every fix, re-run the reconciliation checks.** A "fixed" failure that breaks another check has just moved the bug; keep going until every check is green.
- **The when-to-graduate memo is not "we should move to Causal because Causal is cool."** It is a specific, defensible, written trigger. If the answer is "we should NOT graduate — spreadsheets are still the right tool for this model at this stage" — that is also a valid and often correct answer. Chapter 8 warns that buying too early is as much a failure as buying too late.

## Acceptance criteria

- **Every injected failure is diagnosed** in the diagnosis memo with symptom / trace / cause / fix documented.
- **The rebuilt model passes every reconciliation check** for every forecast month. Balance-sheet identity, cash tie, retained-earnings walk, opening-vs-closing continuity — all green.
- **The hard-code scan on the rebuilt model returns zero hits in the forecast region** across P&L, balance sheet, CFS, and driver tabs.
- **No orphan tabs remain.** Every tab feeds at least one downstream tab, verified by `Trace Dependents`.
- **The dashboard's KPI cells all tie to their model sources** — the ten reconciliation checks from exercise 06 all pass.
- **The scenario switch propagates cleanly** — Base → Downside changes the expected cells without breaking any reconciliation.
- **The model-review checklist audit marks PASS on every item** or documents any FAIL as an explicit known limitation with rationale.
- **The when-to-graduate memo is one page** and contains: current signals present, the written trigger, shortlist of platforms to consider, shortlist of platforms explicitly not considered (with reason), and a migration-cost estimate range.
- **At least one new check row is added to the rebuilt model** as a durable protection against a failure that the original checklist did not catch.

## Deliverables

- The diagnosis memo (Markdown or PDF).
- The rebuilt workbook with all failures fixed and every reconciliation check green.
- The model-review checklist audit (checklist with PASS / FAIL for every item, notes attached).
- The one-page when-to-graduate memo.
- A short (max half-page) methodology memo naming: the diagnostic order you followed, any check rows you added, any checklist items you added to the review checklist, and any failures the original checklist did not cover.

## Extensions (optional)

- Trade broken models with a peer. Diagnose each other's models without knowing the injected failures. Compare diagnosis memos to see which failures were caught quickly, which took longer, and which were missed entirely.
- Author a "failure of the week" catalogue — one broken-model excerpt per week for eight weeks, each isolating a different failure mode. Use as a training set for future CFO / FP&A hires.
- Instrument the rebuilt model with an *automated* checklist run — a macro or Apps Script that runs every check row and produces a green/red summary tab. This turns the 20-30 minute manual audit into a 30-second click.
- Author the migration-plan draft: if the when-to-graduate memo concludes "yes, evaluate now", produce a two-page plan for the evaluation project — vendor shortlist, evaluation criteria, timeline, budget, migration approach, and the specific proof-of-reconciliation gate that the platform must pass before the spreadsheet is retired.
- Compare the rebuilt spreadsheet model to a Causal (or Runway / Mosaic) rebuild of the same model. Report on where each tool is more expressive, where each is more rigid, and which model shape (small-and-simple vs. large-and-complex) each is better suited to.
