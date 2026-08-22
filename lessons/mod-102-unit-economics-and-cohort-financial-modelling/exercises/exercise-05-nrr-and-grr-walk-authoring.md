# Exercise 05 — NRR and GRR Walk Authoring

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 5 (NRR and GRR as capital-efficiency levers). Chapter 4 (cohort table) provides the reconciliation baseline.

## Problem statement

Take one startup's MRR movement ledger for a trailing-twelve-month window and produce the NRR / GRR walk: the reconciliation from starting ARR through churn, downgrades, expansion (decomposed into the four expansion channels), and new logos to ending ARR. Reconcile the walk to the cohort table (from exercise 04) and to the accrual P&L. Report NRR and GRR at TTM, decompose expansion into the four channels, and author the CFO narrative that a board pack requires.

The point of the exercise is to install the walk mechanics, feel the compounding-capital-efficiency arithmetic, and produce the artefact that appears on every Series-A-and-later fundraise deck.

## Scenario — build your own

Use a real or hypothetical startup with:

- Trailing-twelve-month MRR movement ledger: one row per customer per event (new, upgrade, downgrade, churn, resurrection) with date, MRR delta, and event type.
- Starting-period customer roster: every customer active at the start of the 12-month window with their MRR at that time.
- Ending-period customer roster: every customer active at the end of the 12-month window with their MRR.
- Product-line and expansion-type tagging on each MRR movement: was this expansion a seat add, a usage-driven increase, a cross-sell to a new product, or a tier upgrade?
- Optional but preferred: the same data for a prior year, so you can produce a two-period NRR / GRR trend.

If constructing hypothetical data, model realistic proportions. A healthy Series-B SaaS company typically has churn+downgrade at 8-15% of starting ARR, expansion at 15-30%, and new logos at 30-60%, netting to a growth rate somewhere in the 40-80% range.

## Requirements

Produce the following:

1. **MRR movement ledger (input).** One row per event. Columns: customer, event date, event type (new / upgrade / downgrade / churn / resurrection), MRR delta, expansion channel (if applicable: seat / usage / cross-sell / tier), product line (if multi-product).
2. **Starting and ending cohort rosters.** For each of the two snapshots, customer list with MRR.
3. **Data reconciliation.** Sum of starting-cohort MRR + all movements = ending MRR. If it doesn't tie, the ledger is incomplete.
4. **The NRR / GRR walk (headline artefact).** Standard format:

   ```
   Starting ARR (M-12)                                     $X
     - Churn                                              ($X)
     - Downgrade                                          ($X)
     = Retained ARR                                        $X   → GRR = X%
     + Expansion (total)                                   $X
       - Seat expansion                                    $X
       - Usage expansion                                   $X
       - Cross-sell                                        $X
       - Tier upgrade                                      $X
     = NRR ARR                                             $X   → NRR = X%
     + New logos                                           $X
     = Ending ARR (M0)                                     $X   → Growth = X%
   ```

5. **Customer-count view of the walk.** The same walk in customer-count units — how many customers churned, how many downgraded, how many expanded, how many new logos. Both dollars and counts are informative and both should appear.
6. **Product-line NRR (if multi-product).** The walk repeated per product line, each reconciling to the blended.
7. **Reconciliation to the cohort table.** GRR-at-TTM should equal the weighted average of layer-2 M12 retention across cohorts active at the start of the window; NRR-at-TTM should equal the weighted average of layer-4 M12 net dollar retention across the same cohorts. If they don't reconcile, name the discrepancy and its cause (data-quality gap, definition drift, timing issue).
8. **Expansion-decomposition analysis (max half a page).** Given the four channels, is the expansion diversified or concentrated? What is the risk if the largest expansion channel breaks?
9. **Benchmark comparison.** Cite the specific published benchmark for the segment (OpenView, Bessemer State of the Cloud, KeyBanc SaaS Survey) with the year, and compare the company's NRR and GRR to the band.
10. **Compounding-arithmetic scenario (max half a page).** Model the next 5 years' ARR trajectory under two scenarios: (a) the current NRR of X% held constant, (b) an NRR that is 10 percentage points higher or lower (depending on which is more diagnostic for the company). Report the ARR delta at year 5.
11. **CFO narrative (max one page).** The story a CFO tells a board: current NRR / GRR direction, the primary expansion driver, the primary churn driver, benchmark position, corrective actions if any.

## Starter guidance

- The MRR movement ledger is the single input; if it's incomplete, the walk will be wrong. Reconciliation is the first check.
- For "downgrade" vs. "churn" classification, use a specific rule: a customer whose MRR goes to zero is churned; anything else is a downgrade or expansion. A customer who downgrades then churns in a subsequent month is two events, not one.
- For the expansion decomposition, tag every expansion event with one of the four channels. If a single event is ambiguous (a customer added seats and upgraded to a higher tier in the same month), split it into two events.
- The reconciliation to the cohort table is the most important CFO-grade check. Both the walk and the cohort table are computed from the same underlying customer data; they should agree.
- For the compounding-arithmetic scenario, keep it simple — one input (NRR level), one arithmetic loop (5 years), one comparison. The point is to feel the magnitude, not to build a full model.
- The CFO narrative should be readable in 60 seconds and lead with the two headline stats (NRR at X%, GRR at Y%) before the walk.

## Acceptance criteria

- **The walk arithmetic ties end to end.** Starting ARR through every step to ending ARR, with no plug and no rounding hand-waves.
- **GRR is capped at 100% and NRR reflects expansion.** If GRR is above 100%, it's not GRR — it's NRR.
- **Expansion is decomposed into the four channels.** Total expansion equals the sum of channel-specific expansion. A "shared / other" bucket is acceptable if small and disclosed.
- **Reconciliation to the cohort table is either clean or discrepancy-named.** Two views of the same customer base should agree; discrepancy is a red flag worth naming.
- **Benchmark comparison cites a specific published source and year.** Not "typical NRR is 110%" but "OpenView 2024 SaaS Benchmarks for Series-B: median NRR 108%, top-quartile 118%; we are at 115%."
- **Compounding-arithmetic scenario shows a specific 5-year ARR delta.** A single number — "5-year ARR at 120% NRR is $62M; at 100% NRR is $33M" — is more communicative than a paragraph.
- **CFO narrative is one page maximum** and follows the direction / driver / benchmark / action structure.

## Deliverables

- Spreadsheet or notebook with the MRR ledger, the walk, the product-line breakdown, and the cohort-table reconciliation.
- Expansion-decomposition analysis (half a page).
- Compounding-arithmetic scenario (half a page).
- CFO narrative (one page).

## Extensions (optional)

- Produce the walk on a constant-currency basis if the company has material international revenue; report the constant-currency vs. reported NRR delta.
- Produce a *dollar* NRR and a *logo* NRR side by side; report the divergence and interpret.
- Model the NRR sensitivity: a 5-point improvement in seat-expansion rate translates to how many points of NRR? A 3-point reduction in downgrade rate translates to how many points?
- Author the slide that would go into the fundraise deck — headline stats, the walk in the middle, benchmark comparison at the bottom, narrative on the side.
