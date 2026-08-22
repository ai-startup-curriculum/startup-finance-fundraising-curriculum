# Scenario and Sensitivity Analysis

## Why this matters

A model that produces one number for year-3 ARR and one number for cash-out date is a single-point forecast. It answers the question "what will happen if we execute exactly to plan?" — a question the CFO can only answer with "we won't." Every startup misses at least one significant assumption in every planning cycle. The single-point forecast pretends otherwise, and when the miss happens, the board asks *"how bad is it?"* and the CFO doesn't have the number ready.

Scenario and sensitivity analysis is the discipline that turns the single-point forecast into a *range* of outcomes with named drivers. The base case is the plan-of-record. The upside case is what happens if the two or three most favourable levers move together. The downside case is what happens if the two or three most unfavourable levers move together. The sensitivity analysis identifies which specific levers dominate the cash-out date so the CFO knows what to watch weekly and monthly.

This chapter installs the scenario switch (base / upside / downside), the single-variable sensitivity tables for the top four levers, and the two-variable sensitivity heatmap for the pair of levers that dominate the cash-out date.

## The vocabulary — scenarios vs. sensitivities

The terms are often used interchangeably but mean different things:

- **Scenario analysis.** A named alternative view of the world with *many* variables moving together in a coordinated way. Base / upside / downside are the canonical three; some CFOs add "stretch" (upside beyond upside) or "recession" (downside driven by a specific macro shock). Each scenario is a self-contained plan.

- **Sensitivity analysis.** The effect of *one* variable moving on a specific output while everything else holds. "If growth rate is 80% instead of 100%, cash-out date moves from month 22 to month 18." Sensitivities isolate the drivers.

- **Two-variable sensitivity (heatmap).** Two variables moving together on a specific output. "If growth rate is 80% and gross margin is 70% (both worse), cash-out date is month 16." Heatmaps show the interaction of two levers.

- **Monte Carlo (stochastic) modelling.** All variables moving independently with assumed distributions, run over many trials to produce a probability distribution of outcomes. Rare in startup modelling; useful when several inputs have genuine known distributions (rare in early-stage forecasts) and when the decision requires a probability rather than a range.

Scenarios answer the CEO's question ("what are the plan versions we're planning against?"). Sensitivities answer the CFO's question ("which lever should I watch and which won't move the needle?"). Both belong in the model.

## Scenario architecture — the single switch

Chapter 2 introduced the scenario switch as the architectural discipline: a single cell on the assumption tab that flips the active-scenario column, with every downstream driver referencing the active column rather than a specific scenario. The mechanics:

```
Assumption tab, scenario switch:

  Scenario_index:      2         (1 = Base, 2 = Upside, 3 = Downside)
  Scenario_name:      "Upside"   (=CHOOSE(Scenario_index, "Base", "Upside", "Downside"))

  Per-variable table (one row per variable that flexes by scenario):

  Variable                 Base       Upside      Downside      Active
  Growth-rate assumption   +100%      +150%       +60%          =CHOOSE(Scenario_index, ...)  → 150%
  Gross-margin target       75%        78%         70%          =CHOOSE(Scenario_index, ...)  →  78%
  ACV                      $12K       $13K        $10K          =CHOOSE(Scenario_index, ...)  → $13K
  Cost per lead            $130       $110        $180          =CHOOSE(Scenario_index, ...)  → $110
  SDR productivity (SQL/mo) 15         18          12           =CHOOSE(Scenario_index, ...)  →  18
  Close rate                22%        26%         18%          =CHOOSE(Scenario_index, ...)  →  26%
  Retention (M12 NDR)      118%       125%        108%          =CHOOSE(Scenario_index, ...)  → 125%
  Non-payroll opex ratio    0.5x       0.5x        0.6x         =CHOOSE(Scenario_index, ...)  →  0.5x

  (Every downstream driver in the model references the "Active" column.)
```

Every downstream cell — cohort revenue, P&L opex, working capital, cash balance — updates on scenario switch because the drivers reference `Active_growth_rate`, `Active_gross_margin`, etc.

The discipline: **every variable that flexes by scenario is in this table.** A variable that appears in one scenario's assumption but not in the table means the scenario switch is silently inconsistent — one lever is scenario-dependent, another lever is stuck in Base. Every scenario-flexed variable belongs in the table.

## Base / upside / downside — what each represents

The three canonical scenarios are not "high / medium / low" of every variable — that produces implausibly extreme cases where everything simultaneously goes right or wrong. They are *coordinated* stories.

**Base case.** The plan-of-record. Every driver at the value the CFO and CEO agree on for the current planning cycle. This is the number reported to the board as "the plan" and against which actuals are measured. Base should be achievable but not trivial — a base case that the company is likely to beat by 15% is either sandbagging or a signal the plan should be raised.

**Upside case.** The plan works AND two or three specific things go better than assumed. These "specific things" are the levers the team is actively investing in improving — the new SDR playbook lifts SQL productivity, the pricing test lifts ACV, the retention initiative lifts M12 NDR. The upside case is what the team gets if the investments pay off, not what happens if everything is 20% better.

**Downside case.** The plan works AND two or three specific things go worse than assumed. Also coordinated — the CAC rises because a channel deteriorates, the retention curve slips because of a specific customer-experience issue, the ACV compresses because the buyer moves toward a lower-priced SKU. The downside case is what the team gets if two or three specific risks materialise, not a doomsday.

The three cases produce three cash trajectories, three ARR trajectories, three cash-out dates. The delta between base and downside is the number the CEO needs — how much runway is at risk from the identified downside factors, and does the company need to raise sooner or cut faster in the downside case?

## Choosing the levers that flex by scenario

Not every variable belongs in the scenario switch. The rule: only variables that are (a) plausibly wrong in either direction by a material amount, and (b) load-bearing on the outputs the model reports.

The typical set of scenario-flex variables for a Series-A B2B SaaS:

- **Growth rate / bookings volume** — the top-line driver.
- **ACV** — the price driver.
- **Gross margin** — the unit-economics driver.
- **CAC / cost per lead** — the S&M-efficiency driver.
- **SDR / AE productivity** — the sales-execution driver.
- **Close rate / win rate** — the sales-motion-maturity driver.
- **Retention (NDR at M12)** — the compounding growth driver.
- **Non-payroll opex ratio** — the burn-discipline driver.
- **Hiring pace** — the burn-timing driver. (Often a scenario chooses "hire everyone on plan" vs. "delay non-critical hires 3 months.")

Variables that usually don't flex by scenario because they are relatively predictable or externally determined:

- Tax rate.
- Interest rate on cash (unless a specific rate scenario is being run).
- Depreciation schedules.
- Fixed lease payments.
- Regulatory / compliance costs.

The scenario table has 6-12 rows in most working models. More than 15 rows and the scenarios stop being coherent stories; fewer than 5 and the scenario switch isn't distinguishing enough views.

## Single-variable sensitivity tables

The scenario switch tells the CEO what happens under coordinated moves. Single-variable sensitivity tables tell the CFO which lever *individually* has the largest effect on the output that matters most.

The output that usually matters most: **cash-out date**. (For a company with a specific ARR target or profitability target, the output could be *year-3 ARR* or *quarter-of-EBITDA-breakeven* instead.)

A sensitivity table is a two-column artefact: variable value on the left, cash-out date on the right, with the base value highlighted:

```
Sensitivity: Cash-out date to Growth Rate
Growth rate      Cash-out date       Δ vs. base
   +50%           Month 21             -6 months
   +75%           Month 24             -3 months
   +100% (Base)   Month 27              0
   +125%          Month 30             +3 months
   +150%          Month 34             +7 months
   +200%          Month 42             +15 months

Sensitivity: Cash-out date to Gross Margin
Gross margin     Cash-out date       Δ vs. base
   65%            Month 22             -5 months
   70%            Month 24             -3 months
   75% (Base)     Month 27              0
   78%            Month 29             +2 months
   82%            Month 31             +4 months

Sensitivity: Cash-out date to CAC
CAC              Cash-out date       Δ vs. base
   $12K           Month 32             +5 months
   $18K           Month 29             +2 months
   $23K (Base)    Month 27              0
   $28K           Month 25             -2 months
   $35K           Month 23             -4 months

Sensitivity: Cash-out date to NRR (M12)
NRR              Cash-out date       Δ vs. base
   105%           Month 24             -3 months
   110%           Month 25             -2 months
   118% (Base)    Month 27              0
   125%           Month 30             +3 months
   135%           Month 35             +8 months
```

Two things read straight off the tables:

- **Which levers matter most.** In the (illustrative) numbers above, growth rate moves cash-out date by ±7 months across the range; NRR moves it by ±8 months; gross margin moves it by ±5 months; CAC moves it by ±5 months. All four are load-bearing.
- **Where the asymmetry is.** Growth rate is asymmetric — beating plan by 50% extends runway by 15 months (favourable), missing by 50% shortens by 6 months (less favourable per unit). NRR is roughly linear. This asymmetry tells the CFO where beat-vs.-miss produces different-scale consequences.

The mechanics in Excel: use a `Data Table` (Data → What-If Analysis → Data Table) with a row / column input pointing at the assumption cell and the target formula pointing at the cash-out-date cell. In Google Sheets, no native data table exists; write a helper block manually that runs the model at each variable value.

## Two-variable sensitivity heatmap

The single-variable tables treat each lever in isolation. Real-world outcomes come from combinations. The two-variable heatmap shows the cash-out date across a grid of two levers' values.

The two levers to grid: the two that the sensitivity tables identify as the largest movers of cash-out date. For most Series-A SaaS models, this is `growth rate × gross margin` or `growth rate × NRR`. Some cash-burn-heavy models are dominated by `hiring pace × close rate` instead.

```
Two-variable sensitivity: Cash-out date (in months)
                              Growth rate
                       50%    75%    100%   125%   150%
                   ─────────────────────────────────────
      65%           17     19     22     25     28
      70%           19     22     24     28     32
GM    75%           22     24     27     30     34
      78%           24     26     29     32     37
      82%           26     28     31     34     40
                   ─────────────────────────────────────
```

The heatmap makes two things visible that neither single-variable table does:

- **The cell you're planning to live in.** Base case is (100% growth, 75% GM) → month 27. Right at the intersection.
- **The regions around it that require action.** If growth slips to 75% and gross margin slips to 70% simultaneously, cash-out date is month 22 — 5 months earlier. That combination is a fundraise-timing-decision trigger; the CFO watches those two metrics together and starts the fundraise conversation the moment both are trending toward the (75%, 70%) cell.

In practice the heatmap is coloured — green cells for "acceptable runway", yellow for "marginal", red for "action required". Conditional formatting in Excel or Google Sheets handles this automatically.

## Choosing the two heatmap levers

The two-variable heatmap is a limited resource — most CFOs produce one, occasionally two, for a given planning cycle. The choice of which two levers to grid is a diagnostic decision.

- **If the single-variable sensitivity table shows two levers with roughly equal impact,** grid those two. The interaction between them is where the plan is most exposed.
- **If one lever dominates all others,** grid it against the second-largest. The heatmap will show the cell most sensitive to the dominant lever, and the second axis reveals whether it's a linear or non-linear compound.
- **If the plan is at an inflection point** (a new sales motion coming online, a new market entry), grid the two levers most connected to that inflection.

A working convention: choose the two heatmap axes at the start of the planning cycle, and re-visit the choice at each quarterly re-forecast. The dominant levers change as the company grows — CAC dominates at Series-A, retention dominates at Series-B onward.

## Scenario cadence — when to re-run

Scenarios are not a one-time artefact. They are re-run:

- **Before every board meeting.** The board expects to see the plan-of-record and the two alternate cases.
- **Before every fundraise.** Round-sizing depends on the runway trajectory under each scenario; investors will run downside scenarios themselves and the CFO wants to have run them first.
- **At every quarterly re-forecast.** Actuals replace forecasts for the elapsed quarter; the remaining forecast is re-run under updated assumptions.
- **On any material assumption change.** A new sales-comp plan, a change in the hiring plan, a large enterprise deal closing that shifts the cohort — any of these triggers a re-forecast under all three scenarios.

The version-control discipline: at every re-forecast, snapshot the previous plan-of-record as a locked reference (a copy of the model file, or an archived tab set), and forecast the new plan-of-record from actuals forward. The plan-vs.-actuals variance in each subsequent board pack is against the locked reference, not the current-run number.

## The two failure modes to avoid

**Failure 1: Scenarios that are Base × 0.8 and Base × 1.2.** Every driver simultaneously scaled by a constant factor. This produces mathematically consistent scenarios that tell no story — there is no operational lever the CEO can invest in or watch, because "everything went 20% worse" isn't a signal, it's a shrug.

Correct alternative: coordinated scenarios where 2-3 specific levers move together with a named story. "Downside case: the outbound channel deteriorates because our top 2 SDRs leave, so cost per SQL rises by 30% and SDR productivity falls by 20%; concurrently, one large enterprise customer at 8% of ARR churns, dropping M12 NDR from 118% to 110%."

**Failure 2: A model with 8 scenarios.** The temptation is to add scenarios as new possibilities emerge — "recession case", "China entry case", "product-2-launch case", etc. Beyond 3-4 scenarios, no one remembers what each represents, the scenario switch becomes unwieldy, and the board discussion loses focus.

Correct alternative: 3 core scenarios (Base / Upside / Downside), with additional scenarios spun up as short-term what-if runs saved as versioned model copies rather than added to the switch. "Product-2-launch case" is a modelling exercise, not a permanent scenario.

## The output that consolidates the analysis

At the end of a planning cycle, the CFO consolidates scenarios and sensitivities into a single summary — usually one slide or one page — that answers the questions a board actually asks:

- **Base case:** ARR, revenue, cash-out date, EBITDA breakeven month.
- **Upside case:** same numbers, with the two-line story of what has to go right.
- **Downside case:** same numbers, with the two-line story of what could go wrong.
- **The one or two levers to watch weekly.** Named specifically — "close rate on deals over $50K ACV" or "SDR-sourced SQL productivity in the new outbound segment."
- **The two-variable heatmap.** For the two dominant levers.
- **The fundraise-timing implication.** "Under base case, next raise conversations begin month 18. Under downside case, we need to start month 12."

This one-page consolidation is the artefact that goes in the board pack (chapter 7 covers the dashboard build; the scenario summary is a companion slide) and in the data room for fundraise (see [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/)).

## Summary

- Single-point forecasts are a failure of financial planning; every model needs a scenario switch, single-variable sensitivities on the top levers, and a two-variable heatmap on the two levers that dominate cash-out date.
- The scenario switch is a single cell that flips an "active" column on the assumption tab; every downstream driver references the active column, not a specific scenario. This is what makes one-cell scenario changes ripple through all three statements consistently.
- Base / Upside / Downside are coordinated stories, not scalar multiples of Base. Each has 2-3 specific levers moving with a named operational cause.
- Single-variable sensitivity tables identify which levers move cash-out date most, and where the asymmetry lives. Growth rate, gross margin, CAC, and NRR are the usual top four for a Series-A SaaS.
- Two-variable heatmaps grid the two dominant levers and show the runway consequence of joint movement. The base case sits in one cell; the surrounding region shows where action is triggered.
- Scenarios are re-run before every board meeting, before every fundraise, at every quarterly re-forecast, and on any material assumption change. Locked reference snapshots enable plan-vs.-actuals reporting.
- Avoid two failure modes: uniform-scalar scenarios that tell no story, and scenario-proliferation past 3-4 that loses focus.
- The output consolidation is a one-page summary: base / upside / downside numbers, the levers to watch, the heatmap, and the fundraise-timing implication.

Chapter 7 turns to the KPI dashboard — the board-ready output that every scenario feeds into, sourced from the model tabs so it cannot drift from the underlying financials.
