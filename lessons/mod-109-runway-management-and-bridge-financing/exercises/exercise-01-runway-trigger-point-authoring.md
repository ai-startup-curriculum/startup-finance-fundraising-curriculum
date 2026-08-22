# Exercise 01 — Runway Trigger-Point Authoring

**Estimated time:** ~2.5 hours
**Prerequisites:** Chapter 1 (Runway Discipline — 18-24 Month Planning, Monthly Re-Forecast, and the 12 / 9 / 6-Month Trigger Points).

## Problem statement

For a specified hypothetical company, author the full 12 / 9 / 6-month runway trigger-point set, hard-wire the triggers into the monthly re-forecast pack, and produce the capital-plan memo that names the primary and plan-B paths at each trigger. The point of the drill is to build muscle memory around the "trigger fires on the calendar, not on the feel" discipline and to develop the CFO-side artifact set (re-forecast pack template + capital-plan memo + standing CEO-CFO agenda) that keeps the discipline operational across months.

## Scenario — build your own company profile

Construct a hypothetical company with the following minimum shape (numbers are examples — feel free to change them, but keep the same rough scale):

- Series-A SaaS company, ~40 employees, closed a $12M Series-A 8 months ago at $40M post-money.
- Current cash: $8M. Current monthly burn: $700K (trending $650K → $720K over the last three months).
- Current ARR: $4.5M growing at 8% month-over-month over the last three months (down from 12% in the previous six).
- Current NRR: 108%. Gross margin: 74%. CAC payback: 18 months.
- Hiring plan for next 12 months adds 15 heads (approved in the last board meeting), taking headcount to ~55 and monthly burn to ~$900K by month 12.
- Board expectation: Series-B at $80-120M post-money in 12-18 months' time, gated on hitting $8-10M ARR and demonstrating a clear ramp.

## Requirements

Produce a single deliverable pack containing the following artifacts.

### Part A — the runway model and re-forecast pack template

1. **Base-case runway model.** A simple spreadsheet showing monthly cash on hand, monthly burn (with the hiring-plan step-ups), monthly ARR, monthly revenue and gross-margin cash contribution, and net monthly cash flow. Compute the cash-out date on the base case.
2. **Alternative-scenario runway.** Roll forward the current-actuals trend (revenue growth at the trailing-three-month rate, burn at the trailing-three-month rate) instead of the plan. Compute the alternative cash-out date. Compare to the base-case cash-out date and note the delta in months.
3. **Re-forecast pack template.** A one-page (or one-tab) monthly re-forecast pack that includes: actuals vs. plan by line, YTD actuals vs. plan, updated cash-out date under both the plan-forward and actuals-forward views, KPI dashboard (ARR, net-new-ARR, NRR, gross margin, burn, headcount), and a top-of-page "trigger status" indicator showing distance in months from each of the 12 / 9 / 6 triggers. The template will be reused monthly.

### Part B — the trigger-point set

4. **Authored trigger definitions.** In a one-page memo, define each of the three primary triggers (12 / 9 / 6 months) for this specific company:
   - What specifically fires the trigger (e.g., "actuals-forward cash-out date is 12 months or less at the end of any monthly re-forecast").
   - What actions the trigger requires by the CFO (specific artifacts produced, specific conversations opened).
   - What decisions the trigger requires by the CEO / board.
   - What the "clearing condition" is (what would move the company back above the trigger — a specific KPI improvement, a specific raise closing).
5. **Emergency-band definition.** Define what happens below the 3-month band. Name the specific handoff (the CFO-side conversation with the board about `startup-exit-curriculum` paths).

### Part C — the capital plan memo

6. **Two-page capital plan memo** to the CEO and board. Contents:
   - Current runway status (cash, burn, actuals-forward and plan-forward cash-out dates, current classification against triggers).
   - Primary path: the Series-B raise. Target size, target valuation, target milestones (which KPI level opens the round), target investor set, target close date.
   - Plan B: at the 9-month trigger, activate an insider-led bridge conversation with the Series-A lead. Sketch the bridge parameters (size, structure preference — extension vs. SAFE vs. note per chapter 2, expected dilution).
   - Plan C: at the 6-month trigger, activate a venture-debt facility conversation (or explicit alternative). Sketch the facility parameters.
   - The specific dates each trigger is projected to fire on the current forecast, so that the CEO and board can plan around them.

### Part D — the standing meeting

7. **Standing monthly CFO-CEO runway meeting agenda.** One page. Cadence, participants, defined agenda (per chapter 1's spec), defined outputs. Includes a short "sample meeting minutes" template that shows what a completed meeting output looks like.

## Starter guidance

- **Do not skip the actuals-forward view.** The re-forecast that only rolls the plan is the failure mode. Use the trailing-three-month actuals as the baseline; only revert to plan when a specific event justifies it.
- **Set the triggers on the calendar, not on the feel.** The 12-month trigger fires the first month the actuals-forward cash-out date is ≤ 12 months. Do not add subjective qualifiers ("if the trend continues," "if the raise doesn't close").
- **The capital plan is not the fundraise plan.** The primary path is the fundraise, but the plan B is the specific capital-instrument-of-last-resort with named parameters and named counterparties.
- **Reconcile the KPI dashboard on the re-forecast pack to the operating KPIs the CEO reports at the board.** They should be the same numbers.
- **Do the standing meeting even in flat months.** The empty-agenda meeting still confirms the classification. That confirmation is the discipline.

## Acceptance criteria

- **The base-case and actuals-forward runway models produce numeric cash-out dates** that differ by a meaningful amount (typically 2-6 months). The delta is explicitly noted.
- **The re-forecast pack template is operational** — a fresh monthly close's actuals can be dropped in and the pack recomputes.
- **The trigger definitions are unambiguous** — a reader can determine from the definitions whether a trigger has fired, without having to interpret CFO judgment.
- **The capital plan memo names the primary path with a specific target valuation range, milestone gate, and close date; and names the plan B and plan C with specific parameters and counterparties.**
- **The standing meeting agenda specifies defined participants, agenda items, and outputs.**
- **The document is written as if it will be handed to a new CFO joining the company** — self-contained, with enough context for the reader to operate the discipline without additional briefing.

## Deliverables

- The runway-model workbook (spreadsheet).
- The re-forecast pack template (spreadsheet or Markdown, whichever fits the workflow).
- The trigger-definitions memo (Markdown or PDF).
- The capital-plan memo (Markdown or PDF).
- The standing-meeting agenda (Markdown or PDF).

## Extensions (optional)

- Add a **two-variable sensitivity heatmap** (net-new ARR growth × opex growth) showing the runway consequence across a 5×5 grid. This is the mod-103 chapter 6 material applied to the runway question.
- Author a **retrospective memo** covering a fictional "we should have activated the 9-month trigger three months ago" scenario. Walk what would have happened differently.
- Model an **insider bridge closing at the 6-month trigger** using chapter 2's framework and produce the pro-forma cash-out date after the bridge closes. Compare to the emergency-band handoff scenario.
