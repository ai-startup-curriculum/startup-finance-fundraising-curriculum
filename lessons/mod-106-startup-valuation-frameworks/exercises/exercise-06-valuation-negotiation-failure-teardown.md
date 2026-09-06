# Exercise 06 — Valuation-Negotiation Failure Teardown

**Estimated time:** ~5 hours
**Prerequisites:** Chapter 8 (valuation-negotiation failure modes and remediation); prior exercises 01-05 (the derivations that a proper valuation memo should have run).

## Problem statement

Tear down three fictional-but-realistic valuation negotiations that failed for each of the three canonical failure modes catalogued in chapter 8:

1. **Anchoring to the last round's post-money as this round's pre-money floor** without adjustment for market conditions.
2. **Chasing a public-comp multiple** that ignored the growth-and-margin band and the private-market discount.
3. **Ignoring the VC's fund math** and demanding a pre-money that the target lead's fund cannot underwrite.

For each failure, produce (a) the specific diagnosis with the arithmetic that identifies the mode, (b) the counterfactual — what the CFO should have done ahead of the negotiation, (c) the remediation with a rebuilt valuation memo, (d) a re-priced round proposal with a specific defensible pre-money, and (e) a "post-mortem to the board" memo that explains what went wrong and the corrected path forward.

The drill's goal is to build the diagnostic muscle for recognising each failure mode from an incoming pitch or a stuck negotiation, and the remediation muscle for producing the specific artefact that unblocks it.

## Scenarios — three cases to construct

Construct three fictional-but-realistic negotiation scenarios, each exhibiting one of the three failure modes. Each scenario needs enough detail to make the diagnosis and remediation concrete. Below are prompts; extend each with specifics you can defend.

### Scenario A — "The flat-round demand" (failure mode 1)

- Series-B target, fintech SaaS.
- Prior round: Series-A, closed 22 months ago at $60M post-money on a $12M raise (so $48M pre + $12M new).
- Current financial profile: $15M NTM revenue, 45% NTM growth (down from 80% at Series-A closing), 72% gross margin, -35% FCF margin.
- Founder demand: **$60M pre-money** (flat to the prior post-money) on a $20M new raise = $80M post-money.
- Market conditions: current-quarter median Series-B pre-money is materially below (say, 30-40% below) the last-round-based demand; the current-quarter fintech sector has compressed further than the SaaS median.
- Target lead: a $250M multi-stage fund that has offered $45M pre-money with market-standard terms.
- Founder's stated reasoning: "We're not doing a down round. The last-round investors won't accept it, and it damages the narrative with employees."

### Scenario B — "The 10x ARR headline pitch" (failure mode 2)

- Series-B target, vertical SaaS for healthcare-provider admin.
- $25M ARR (end-of-most-recent-month; NTM revenue projection roughly $22M given the recent ramp).
- 55% NTM growth, 76% gross margin, -25% FCF margin, Rule of 40 = 30.
- Founder demand: **$250M pre-money** on a $30M raise (implied 10× ARR or ~11× NTM revenue).
- Founder's stated reasoning: "The SaaS index is trading at 10× ARR, so we should be at 10× ARR. We're growing faster than the median public comp."
- Market conditions: the current filtered public-comp set for vertical SaaS at similar growth trades at a median EV/NTM of 8×; the private-market discount at Series-B is 35%; the target's applicable multiple is roughly 5.5×; the market-anchored pre-money is approximately $120M.
- Target lead: a growth-stage fund offering $110M pre-money with participating preferred (a reflection of the pricing gap).
- Meta-context: the founder is drawing the "10× ARR" number from a trade-press headline; has not filtered the comp set; has not applied a private-market discount; has not run the growth-adjusted regression.

### Scenario C — "The fund-math mismatch" (failure mode 3)

- Series-Seed target, developer-tools SaaS.
- $1.2M ARR, 20% MoM growth over the last six months, 82% gross margin, CAC payback 8 months.
- Founder demand: **$40M pre-money** on a $8M seed round = $48M post-money.
- Founder's stated reasoning: "Our comps just raised at these levels; the multiples framework supports this."
- Target lead: "Emerging Seed Partners" — a $50M seed fund, typical cheque $2-3M, target 5× fund-level MOIC, portfolio construction ~20 companies.
- Target lead's fund math at the demanded pre-money:
  - Their $3M cheque at $40M pre = 6.25% post-money ownership.
  - Assume a four-round dilution ladder (Series-A / B / C / D+) at 20% per round → retention roughly 41%.
  - Target exit value (base case, given the ARR and category): $500M.
  - Return math: $500M × 6.25% × 41% = $12.8M on a $3M cheque = **4.3× MOIC**.
  - Fund-returner multiple: $50M / $3M = 16.7× (the ceiling); realistic target multiple for the winners in this fund is 15-25×; 4.3× is 3-5× below the fund's target.
- Fund's counter-offer: $12M pre-money on $3M raise. Founder refuses.
- Two other target leads (a $200M multi-stage fund and a $30M "solo capitalist" fund) have different fund math and would produce different pre-money supports; the founder has not run the calculation for either.

## Requirements

Produce a workbook plus a "post-mortem to the board" memo for each of the three scenarios.

For each scenario:

1. **Scenario detail tab.**
   - Restate the scenario with any additional detail (financial projections, dilution schedule, exit-value hypothesis, comp-set constituents) you need to complete the diagnosis.
   - Cite specific market-conditions data (from exercise 05 or freshly pulled) that anchors the "market" side of the diagnosis.

2. **Diagnosis tab.**
   - Compute the specific arithmetic that identifies the failure mode:
     - **Scenario A:** derived pre-money from anchor / multiples / VC-method / market conditions vs. the flat-round demand. Quantify the gap.
     - **Scenario B:** derived multiple from the filtered comp set with growth adjustment and private-market discount vs. the demanded multiple. Quantify the gap.
     - **Scenario C:** the target lead's fund-math-implied pre-money vs. the demand. Quantify the gap. Also compute what the other two target leads' fund math would support.
   - Name the failure mode explicitly and the specific pattern in the founder's pre-negotiation memo that would have flagged it in a review.

3. **Counterfactual tab.**
   - Describe what the CFO should have done ahead of the negotiation to prevent the failure:
     - **Scenario A:** rebuild the pre-money from ground-up ignoring the prior post-money; produce the market-context down-round defence.
     - **Scenario B:** rebuild the multiples analysis with explicit filter, growth adjustment, private-market discount; produce the derivation walk-through.
     - **Scenario C:** build the target-investor list with each lead's fund-math pre-money; prioritise leads by which fund math clears the founder's minimum acceptable pre-money.
   - Specify the artefact (memo, workbook, slide) the CFO should have produced.

4. **Remediation tab.**
   - Produce the corrected valuation derivation for the target:
     - **Scenario A:** the ground-up derivation with the anchor bracket, VC method from the target lead's side, multiples framework, market-conditions read. Reach a corrected pre-money.
     - **Scenario B:** the filtered comp set, growth-adjusted regression, Rule-of-40 adjustment, private-market discount. Reach a corrected pre-money.
     - **Scenario C:** the VC method from each of the three target leads' sides. Prioritise the leads. Reach a corrected target investor list and a corrected pre-money that at least one lead's fund math supports.

5. **Re-price tab.**
   - Produce the specific re-priced round proposal:
     - Corrected pre-money.
     - Rationale walk-through.
     - Named specific-parameter arguments the CFO will defend.
     - Predicted counter-offer and negotiation posture.
     - Walk-away floor.

6. **Post-mortem memo tab (one per scenario).**
   Written to the board (1-2 pages each):
   - What happened (the founder's demand and the counterparty's response).
   - The specific diagnostic that identifies the failure mode.
   - What should have happened in the pre-negotiation preparation.
   - The corrected derivation and the corrected pre-money.
   - The specific process changes going forward (pre-negotiation checklist, memo-review discipline, cross-source triangulation, target-investor list construction).
   - The specific ask to the board (e.g., "adopt the pre-negotiation checklist below for every priced round going forward"; "engage a valuation advisor for the next round"; "revise the target-investor list per the corrected fund-math analysis").

7. **Meta-analysis tab.**
   Across the three scenarios:
   - The three failure modes as a taxonomy — what characterises each, what pattern in the pre-negotiation memo signals each, what the remediation stack is for each.
   - The one-page pre-negotiation checklist that would have caught all three failures in review.
   - The specific parameter each failure mode is most sensitive to — the parameter the CFO should stress-test hardest before signing off on the pre-negotiation memo.

## Starter guidance

- **Diagnose from the founder's memo, not from the counterparty's response.** The failure is in the derivation the founder walked in with, not in how the counterparty responded. Read the founder's pre-negotiation memo (or its absence) for the failure pattern.
- **Every failure mode has an artefact the CFO didn't produce.** Scenario A: no ground-up derivation with market-context down-round defence. Scenario B: no filtered-comp-set walk-through. Scenario C: no fund-math analysis from each target lead's side. The remediation is the specific missing artefact.
- **The remediation is not "insist on the original number harder."** The remediation is a different derivation that produces a defensible pre-money the market — or at least a specific target lead — will clear. In some scenarios the defensible pre-money is lower than the original demand; in others it's a repositioning to a different target lead pool.
- **The "market moved" defence is real for down-round pricing.** Scenario A's remediation includes preparing the specific chapter-6 / chapter-7 data on current-quarter down-round frequency, comparable-round pricing, and sector-specific compression. Cite specific data cuts.
- **Comp-set choice is where the negotiation concentrates for failure mode 2.** Scenario B's remediation is not just "apply a lower multiple" — it's "rebuild the comp set with a defensible filter and produce a derivation walk-through that the counterparty can debate at the parameter level."
- **Fund math is not the CFO's opinion; it's the lead's math run from public data.** Scenario C's remediation runs the VC method from each target lead using their disclosed fund size, cheque pattern, and portfolio construction. It's an arithmetic exercise, not a narrative one.
- **The post-mortem to the board should be corrective, not blame-allocating.** The purpose is to install the discipline going forward, not to litigate the past. Emphasise the process change.

## Acceptance criteria

- **All three scenarios are constructed with sufficient detail** to complete the diagnosis, counterfactual, and remediation.
- **The diagnosis for each scenario is quantitative** — the arithmetic that identifies the failure mode is explicit.
- **The counterfactual identifies the specific missing artefact** the CFO should have produced.
- **The remediation is a complete corrected derivation** — not a caveat on the original.
- **The re-priced round proposal is defensible** with named parameters and a walk-through the counterparty can debate.
- **Each post-mortem memo is 1-2 pages** and includes both the diagnosis and the process-change ask to the board.
- **The meta-analysis produces a one-page pre-negotiation checklist** covering all three failure modes.

## Deliverables

- The workbook with a scenario-detail / diagnosis / counterfactual / remediation / re-price tab for each of the three scenarios, plus the meta-analysis tab.
- The three post-mortem memos (Markdown or PDF).
- The one-page pre-negotiation checklist (Markdown, PDF, or a memo tab).

## Extensions (optional)

- **Add a fourth scenario for a fourth failure mode.** Author a fictional-but-realistic case where the failure is one not catalogued in chapter 8 — e.g., "the CFO underestimated the SAFE overhang and the priced-round pre-money the market would clear is materially higher than the demanded post-money net of the SAFE conversion," or "the CFO applied a DCF framework to a genuinely early-stage company where a DCF is not defensible and produced a valuation the lead rejected on methodology grounds." Diagnose and remediate.
- **Author the counterparty-side memo.** For one of the three scenarios, write the lead investor's internal partner-meeting memo that documents the pricing gap, the fund-math analysis, and the recommendation to counter-offer or walk. Compare the counterparty's memo against the founder's demand and use the comparison to teach the negotiation-posture lesson.
- **Add a "learning-from-postmortem" board-education pack.** A three-slide deck the CFO uses at the board meeting to install the discipline going forward, with a specific process change (mandatory pre-negotiation memo review, quarterly market-conditions refresh, target-investor list construction cadence) tied to each failure mode.
- **Run one scenario through a "successful negotiation" alternate branch.** Take the corrected pre-negotiation memo from the remediation tab and walk what a successful negotiation would look like — the counterparty's counter, the CFO's defensible-parameter response, the landing zone, the closed pre-money. Compare to the failed branch. Discuss what the corrected preparation bought the company.
- **Cross-reference with mod-108 (term sheets).** For scenario A (down-round pricing), extend the analysis to the term-sheet consequences: anti-dilution triggers on the prior round's preferred (broad-based weighted-average by default; see [mod-108](../../mod-108-term-sheets-and-preferred-stock-economics/)) and possible pay-to-play. For scenario B, extend to the participating-preferred term the lead offered as a reflection of the pricing gap. Discuss where the mod-106 fix ends and where the mod-108 fix begins.
