# Exercise 02 — VC Method Target-Return Back-Solve

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 2 (VC method); familiarity with [mod-104 chapter 2](../../mod-104-cap-tables-and-equity-compensation/02-pre-vs-post-money-math-and-the-option-pool-shuffle.md) on the pre-vs.-post-money math and pool shuffle.

## Problem statement

Build a VC-method back-solve model for a hypothetical Series-Seed round. Work through a plausible Series-A / B / C dilution ladder to a defined exit; sensitise across target-return, dilution schedule, and exit-value assumptions; produce the pre-money the VC's fund math supports; and then run the same calculation from *two different target-lead funds' sides* (a small pre-seed fund and a large multi-stage fund) to see how the fund-math pre-money differs for the same company depending on who the lead is.

The drill's goal is to install the discipline of running the VC method from the specific target lead's perspective, and to make the four inputs (exit value, target multiple, dilution schedule, investment amount) explicit and negotiable in the CFO's model.

## Scenario — build your own

Construct a hypothetical Series-Seed target and two target lead funds.

**Target company:**

- Delaware C-corp, incorporated 18 months ago.
- Founders + early hires at 100% of common (5,000,000 shares outstanding).
- No prior SAFEs / notes (clean cap table for simplicity — extend later if desired).
- 12 months of revenue history: $500K ARR at end of most recent month, growing ~15% MoM, gross margin 75%, CAC payback ~12 months (rough but modelable).
- Fundraising target: **$4M seed round** on a pre-money to be determined.
- Assumed exit: acquisition in year 5-6 by a strategic acquirer.

**Target lead fund A — "Pre-Seed Partners":**

- Fund size: $40M.
- Target return: 3× net-to-LPs.
- Typical cheque size at seed: $2M-$4M (leading a $4-6M round).
- Portfolio construction: ~25 companies per fund.
- Fund vintage: current (year 1-2 of investment period).

**Target lead fund B — "Multi-Stage Ventures":**

- Fund size: $500M.
- Target return: 3× net-to-LPs.
- Typical cheque size at seed: $5M-$8M (leading a $6-10M round, willing to lead this specific $4M round at $4M).
- Portfolio construction: ~30 companies across seed / Series-A / Series-B in the same fund.
- Fund vintage: current (year 1-2).

## Requirements

Produce a single workbook (Excel or Google Sheets) with the following:

1. **Assumptions tab.**
   - All the scenario inputs above, plus explicit values for: exit-value hypothesis (base / bull / bear cases), target-return-multiple assumptions per fund, dilution schedule per round (Series-A dilution %, Series-B dilution %, Series-C dilution %), and the investment amount for each target lead.

2. **Dilution ladder tab.**
   - Round-by-round dilution schedule from Series-Seed through Series-C (or through exit if fewer rounds).
   - For each round: assumed pre-money, assumed raise, resulting dilution to prior shareholders, resulting retention.
   - Anchor the per-round dilution assumptions against Carta State of Private Markets (chapter 7) median dilution by stage. Cite the specific Carta cut and date.
   - Produce the aggregate retention through the ladder — the fraction of today's ownership that remains at exit after all future dilution.

3. **Fund-A VC method tab.**
   - Compute the fund-returner multiple: fund size / typical cheque size = the number of times this cheque has to return the fund. This is the *upper-bound* target multiple.
   - Compute a realistic per-deal target multiple: fund's target-return × the multiplier a "winner" has to hit given the portfolio's expected loss distribution. Show the arithmetic.
   - Run the VC method: `post-money today = (target exit value × retention) / target multiple`; `pre-money today = post-money - investment`.
   - Sensitise across three exit-value cases (base / bull / bear), three target-multiple cases (10× / 20× / 30×), and two dilution-schedule cases (aggressive / conservative).
   - Produce the pre-money range Fund A's math supports.

4. **Fund-B VC method tab.**
   - Same structure as Fund-A tab but with Fund-B's inputs.
   - Fund B is larger with more companies per fund; its target multiple per deal is typically lower than Fund A's. The pre-money Fund B supports should be different from what Fund A supports on the same company.

5. **Comparison tab.**
   - Side-by-side of the pre-money ranges each fund's math supports.
   - Notes on where the two funds overlap and where they diverge.
   - A ranking of the two funds by which one's math clears the founder's minimum acceptable pre-money.

6. **Cross-check tab.**
   - Run a **multiples framework** cross-check (chapter 3): what pre-money does a comp-set multiple applied to NTM revenue produce? Even at seed, the company has some revenue, so a rough multiples check is possible.
   - Run an **anchor-method cross-check** (chapter 1): where does the target sit against a Berkus / Payne / risk-factor bracket?
   - Run a **market-conditions cross-check** (chapters 6-7): current-quarter seed median pre-money from Fenwick / Wilson Sonsini / Carta.
   - Produce a comparison table across all four lenses (Fund A VC method, Fund B VC method, multiples, anchor, market conditions).

7. **Founder-facing memo.**
   - The pre-money range each fund's math supports.
   - The founder's minimum acceptable pre-money and whether either fund's math clears it.
   - Recommended target-lead priority order.
   - The specific-parameter arguments the CFO is prepared to defend (exit-value hypothesis, dilution schedule assumptions).
   - The walk-away floor and the specific-conditions logic for taking it.

## Starter guidance

- **The fund-returner multiple is not the target multiple.** A $40M fund into a $2M cheque needs a 20× MOIC on the cheque to return the fund. That is the ceiling. The realistic target multiple is somewhat lower, because most VCs expect a small number of winners to carry the fund rather than every deal to return the fund. Use 15-25× as the realistic target for a $40M seed fund's lead deals.
- **Larger funds have lower per-deal target multiples.** A $500M multi-stage fund can accept 8-15× on a specific deal because more deals are contributing to the fund return. Use that in Fund B's calculation.
- **The exit-value hypothesis is the single most-sensitised input.** Base case might be $250M; bull case $750M; bear case $75M. Run the calculation across all three and note how the pre-money moves.
- **The dilution schedule matters.** A four-round path (Series-A / B / C / D + exit) with 20% dilution per round produces ~41% retention. A three-round path with 20% per round produces ~51%. The difference materially affects the calculated pre-money.
- **Cite specific Carta data cuts** for the dilution assumptions. Do not use generic "20% per round" numbers.
- **Cross-check ALL FOUR lenses.** The point of the exercise is to show that VC-method pre-moneys can diverge from multiples / anchor / market-conditions pre-moneys, and to make the CFO explicit about which one is dominating the negotiation.

## Acceptance criteria

- **Fund-A and Fund-B VC-method calculations are complete** with sensitised outputs across exit-value, target-multiple, and dilution-schedule cases.
- **The dilution ladder is anchored to real Carta or PitchBook data** with citation and date.
- **The comparison tab makes explicit** which fund's math clears the founder's minimum and which doesn't.
- **The cross-check tab reconciles the VC method against multiples, anchor bracket, and market-conditions.** Any divergence >25% is discussed with a hypothesis for the divergence.
- **The founder-facing memo produces a specific target-lead priority order** with a specific defended pre-money target and a specific walk-away floor.
- **The retention calculation is explicit** — the model shows the founder how much of today's ownership survives to exit under each dilution-schedule case.

## Deliverables

- The workbook with all seven tabs.
- The founder-facing memo (Markdown, PDF, or a memo tab).
- A one-slide summary suitable for a board deck showing the two funds' pre-money ranges alongside the multiples / anchor / market-conditions cross-checks.

## Extensions (optional)

- **Add a third target lead fund** — a $150M "graduated Series-A" fund that leads seed rounds as a portfolio-building exercise but underwrites at Series-A economics. Compare its supported pre-money to Fund A and Fund B.
- **Add a partner-meeting deck slide** that walks the fund math from the lead's perspective, showing the return math at the target pre-money against the lead's fund-level target. Framed to pre-empt the fund-math objection.
- **Sensitise across MFN and pro-rata scenarios** — if this seed round has an MFN clause on the SAFE or if the lead demands pro-rata rights, how does that affect the dilution ladder and therefore the required pre-money today? Cross-reference [mod-105 chapters 1 and 5](../../mod-105-convertible-instruments/).
- **Rerun the exercise for a Series-A** — same company, 18 months later, $8M ARR, raising $15M at a target Series-A pre-money. Compare how the VC method behaves at a stage with more revenue data and shorter distance to exit.
