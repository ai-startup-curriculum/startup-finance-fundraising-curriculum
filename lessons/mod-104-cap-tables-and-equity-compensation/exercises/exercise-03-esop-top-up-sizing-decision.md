# Exercise 03 — ESOP Top-Up Sizing Decision

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 3 (ESOP top-ups and pool sizing through rounds). Uses the cap table from Exercises 01-02 as context.

## Problem statement

For the Series-A closing scenario from Exercise 02, author a defensible pool-sizing recommendation from the ground up — starting with an 18-month hiring plan, layering refresh grants, adding a buffer, and comparing against Carta / Pave benchmark data (or reasonable proxy data if the current-year benchmark reports aren't available to you). Produce a memo the CFO would send to the CEO recommending a specific pool size in *shares* (not just a percent), backed by the hiring plan and defensible against the investor's benchmark-driven ask.

The exercise fills in the "hiring-plan-derived pool" gesture from Exercise 02 with a real bottom-up build.

## Scenario — build your own

Use the pre-close cap table from Exercise 01 and the Series-A parameters from Exercise 02. Assume the current team is 20 people (or whatever your Exercise 01 scenario used). Series-A closes with $10M in the door, and the round is expected to fund 18 months of runway. During those 18 months the company plans to hire.

Design an 18-month hiring plan. Suggested minimum shape:

- 4 senior engineers (Staff or Principal level).
- 8 mid-level engineers.
- 2 engineering managers.
- 3 senior GTM hires (AE, CSM, or sales manager).
- 5 mid GTM hires.
- 2 senior product / design hires.
- 1 VP-level hire (VP Engineering, VP Product, or VP Sales — pick one).
- 1 executive hire (CFO, GM, or head of new function — pick one).

Total: ~26 hires. You may modify the plan to suit your scenario but keep the total in the 20-30 range for realism.

## Requirements

Produce a single spreadsheet workbook with the following tabs:

1. **Hiring plan tab.** One row per planned hire with role, level, department, expected start month (spread across the 18-month window; don't cluster all hires at month 1), and estimated grant size in percent of fully-diluted post-Series-A. Sum the total planned new-hire grants at the bottom.
2. **Grant-size benchmark tab.** For each of your role / level combinations, cite the Pave, Carta, or reasonable industry-source range you're using. If you don't have access to current-year Pave / Carta data, use a defensible published proxy (e.g., a well-cited AngelList / a16z / Peter Walker post; use `<!-- needs-research: ... -->` markers where you're extrapolating). The goal is that a reviewer can see *why* the grant-size assumptions are what they are.
3. **Refresh-grant reserve tab.** For the existing 20 employees + the 26 new hires, estimate the annual refresh-grant activity over the 18-month window. Typical assumption: refresh grants start 24 months after the original grant, at 25-50% of the original grant size. For the 18-month window from Series-A close, only employees hired well before Series-A will be in-window for a refresh. Compute the refresh-grant reserve.
4. **Buffer tab.** Add a documented buffer to the sum of new-hire grants + refresh grants:
   - 15-25% for over-hiring / upgrades within the plan.
   - 10-20% for the last 3-6 months of the 18-month window as a safety margin before the next top-up conversation.
   - Explain the specific percentages you're using.
5. **Pool sizing summary.** Total pool ask = new hires + refreshes + buffers, expressed in both percent of post-close FD and absolute share count (using the post-close FD from Exercise 02, Treatment 1 or 2 — pick one and note which).
6. **Benchmark comparison.** Cite the Carta State of Private Markets Series-A pool-size distribution (or a reasonable proxy). Compare your bottom-up number to the benchmark median and top quartile. Explain the divergence.
7. **Pool-sizing memo (1-2 pages).** Written to the CEO. Contents:
   - The bottom-up pool number (in shares and percent).
   - The benchmark-derived pool number (in shares and percent).
   - The recommendation — which number to use, and why.
   - The trade-off framing (over-sizing vs. under-sizing cost).
   - The implication for the Series-A term sheet — how this pool number changes the founder-dilution outcome versus the term-sheet default (from Exercise 02).
   - The between-rounds monitoring plan — the specific pool-remaining threshold at which the CFO will start the next top-up conversation.
8. **Monthly pool-remaining projection.** For 18 months post-close, project the pool balance: opening balance − grants issued that month + forfeitures. Show the month at which the pool crosses the 20%-remaining threshold (indicating "start planning the Series-B top-up conversation").

## Starter guidance

- **Distribute the hires across the 18 months.** A pool that runs out at month 12 because 24 of the 26 hires cluster in months 1-6 is planned poorly. Realistic ramp: 3-5 hires per quarter, weighted slightly toward the middle of the window.
- **The VP-level and executive grants are the concentrated dilution.** A single VP grant at 0.75-1.5% is 5-15% of the total pool by itself. These are the grants whose sizing sensitivity matters most.
- **Refresh grants are the reserve founders forget.** A retro-diligence firm doing pool analysis on a Series-A company usually finds that the pool did *not* have a refresh reserve at Series-A and got squeezed by refresh grants in year 2. Model it in.
- **The buffer is not a fudge factor.** Document what the buffer covers — a specific list of "over-hiring for retention / upgrading a mid-level to a senior after an unexpectedly good hire / plan flex for a critical unmet role" — not just "in case."
- **The benchmark comparison should not shame the bottom-up.** If bottom-up is 6% and the benchmark median is 12%, that is a *finding*, not an error. The benchmark median may reflect companies without a bottom-up plan; yours has one.
- **The memo should be actionable at a term-sheet negotiation.** The CFO who has done Exercises 02 and 03 walks into the negotiation with the pool size they want, backed by the plan.

## Acceptance criteria

- **The hiring plan has one row per hire** with role, level, department, start month, and grant size — not just aggregate numbers.
- **Grant sizes have cited benchmarks** (or `<!-- needs-research: ... -->` markers where extrapolating). No unsourced numbers.
- **Refresh grants are explicitly modelled**, not hidden in the buffer.
- **The buffer is documented with a specific list of what it covers**, not just a percentage.
- **The pool ask is expressed in both shares and percent**, tied to a specific pre-close FD.
- **The benchmark comparison names the source** and shows the divergence between bottom-up and benchmark.
- **The pool-sizing memo makes a specific recommendation** the CEO can bring into the term-sheet negotiation.
- **The monthly pool projection shows the top-up-conversation trigger** at a specific month.

## Deliverables

- The workbook with all eight tabs / sections.
- The 1-2-page memo (Markdown or PDF).

## Extensions (optional)

- Author a second scenario in which the company mis-sizes the pool (chooses the benchmark median instead of the bottom-up). Project 18 months forward and demonstrate the emergency top-up event just before Series-B.
- Add a "high-growth" version of the hiring plan (40 hires instead of 26) and show the corresponding pool ask. Discuss the diminishing marginal defensibility of very-large pool asks even with a hiring plan.
- Integrate the pool-remaining KPI into a monthly board dashboard (see [`mod-103`](../../mod-103-three-statement-model-and-driver-based-forecasting/07-kpi-dashboard-reconciled-to-the-model.md) for the dashboard construction pattern).
- Interview a real founder / CFO about how they defended a pool ask at their Series-A. Compare to your bottom-up defence.
