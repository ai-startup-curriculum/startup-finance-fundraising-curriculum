# Exercise 02 — Bridge Round Structure Decision

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 2 (Bridge Round Structures — Extension, Insider SAFE, and Bridge Convertible Note). Familiarity with mod-105 (Convertible Instruments) and mod-108 (Term Sheets and Preferred-Stock Economics).

## Problem statement

For a specified stressed-runway scenario, choose the appropriate bridge structure — extension of existing preferred, insider-led bridge SAFE, or bridge convertible note — apply the decision framework from chapter 2, model the pro-forma cap-table impact under multiple next-round-price scenarios, and author the founder / lead-investor memo defending the choice. The point of the drill is to develop the muscle for making the structural decision deliberately (as opposed to defaulting to the instrument that was easiest to close last time) and to build the artifact set that a real bridge close requires.

## Scenario — the situation

Use this specific scenario for the drill. (For extra depth, run the same drill against two additional scenarios of your own construction with different KPI trajectories.)

**Company:** Series-A B2B SaaS company, 60 employees, closed a $15M Series-A 14 months ago at $45M post-money. Series-A lead was a well-regarded early-stage fund with $500M under management and standard-market pro-rata rights. Two co-investors participated in the Series-A for smaller cheques.

**KPI trajectory since Series-A close:**
- ARR grew from $3M to $7.5M (roughly on the plan the Series-A underwrote against $8M ARR at month 15).
- Net-new-ARR pace slowed noticeably in the last four months (from $200K/month average to $130K/month), attributable to a slower enterprise-sales ramp than modelled.
- NRR is 118% (strong), gross margin 78% (strong), CAC payback 22 months (weak vs. the 15-month plan).
- Founders and executive team all intact. Product roadmap on schedule.

**Current cash and burn:** $4M cash, $650K/month current burn. Actuals-forward cash-out date is 6 months.

**The task:** the company needs a bridge to buy time to close a Series-B at a defensible price. The company's own view is that a Series-B in 6-9 months at $60-80M post-money is achievable if net-new-ARR reaccelerates back to the $200K/month range and if the CAC payback improves to 18 months.

## Requirements

Produce a single deliverable pack containing the following.

### Part A — apply the decision framework

1. **Decision-framework memo.** In a two-page memo, walk the five-step decision framework from chapter 2:
   - Step 1 — is the last-round price defensible? Justify.
   - Step 2 — is the landing event specific? What is it?
   - Step 3 — is the insider set (specifically, the Series-A lead) available? Assume they have $12M of dry powder in the fund for follow-on but only one other portfolio company currently in bridge conversations.
   - Step 4 — is the speed constraint binding? Assume a normal 6-8 week timeline is workable.
   - Step 5 — is the size reasonable relative to the last round? Target bridge size 25-35% of the Series-A ($4-5M).
   Conclude with a specific structure recommendation (extension, SAFE, or note) and the reasoning.

### Part B — model the pro-forma cap table under three scenarios

2. **Pro-forma cap-table workbook.** Build the pre-bridge cap table (Series-A preferred, founder common, option pool, any prior SAFEs — assume there is one prior seed-stage SAFE with $500K principal at a $10M post-money cap that has not yet converted).
3. Model the bridge under the recommended structure. Then compute the pro-forma cap table under three next-round-price scenarios:
   - **Base case:** Series-B closes at $70M post-money in 8 months.
   - **Upside:** Series-B closes at $100M post-money in 10 months (net-new-ARR reaccelerates strongly).
   - **Downside:** Series-B closes at $50M post-money in 12 months (net-new-ARR does not reaccelerate; a modest down-round from the "flat-to-up" expectation).
4. For each scenario, produce the post-Series-B cap table, the founder ownership, the Series-A lead ownership, and the bridge participants' ownership. Also compute the same three scenarios under **each of the two alternative bridge structures** you did not recommend, so the comparison is on the same basis.

### Part C — author the memo the CFO delivers

5. **Founder / CEO memo (2 pages).** Explains the recommendation, walks the framework, shows the pro-forma cap-table results under the three scenarios, and answers the question: "why this structure and not one of the other two?" The memo should be readable by a CEO who is not an expert in convertible mechanics — jargon defined where used.
6. **Lead-investor talking points (1 page).** The specific ask to the Series-A lead. Includes: bridge size, structure, target close date, participation ask (target dollar amount from the Series-A lead), pro-rata offer to other investors, key term parameters (cap if SAFE; conversion mechanics if note; per-share price if extension). Written in the voice of the CFO or CEO asking the lead partner to commit.
7. **Board consent draft.** A one-page draft consent authorising the bridge (specific to the chosen structure). Includes signature block.

### Part D — the updated capital plan

8. **Updated capital plan memo.** Slot the bridge into the chapter 1 capital-plan framework. Post-bridge cash-out date, updated distance to the trigger points, updated primary path (Series-B) with the updated milestone gates.

## Starter guidance

- **Do not skip step 1 of the framework.** The most common failure is defaulting to the SAFE (fastest to close) when an extension would have been signal-appropriate.
- **The insider set constraint (step 3) usually determines the answer.** If the Series-A lead cannot lead the extension, the SAFE / note options are what remain.
- **The pro-rata rights of the other Series-A co-investors matter.** Do not skip offering pro-rata; the exercise should reflect that offering.
- **Under the downside scenario, model the anti-dilution recalculation on the Series-A preferred** — the down-cap or down-priced next round triggers the anti-dilution formula from mod-108 chapter 4. Broad-based weighted-average is standard.
- **When you compare structures across the three scenarios, note the specific structure that beats each of the others in each scenario, and why.** The narrative should be: "our recommended structure is X because it beats the alternatives in the base case and is only slightly worse in the downside; under the upside it is comparable to alternatives; combined with the signalling benefit, it is the choice."

## Acceptance criteria

- **The decision-framework memo walks all five steps and reaches a specific structural recommendation** with defensible reasoning.
- **The pro-forma cap table is computed correctly for the recommended structure and for both alternative structures across all three next-round-price scenarios**, and reconciles to the pre-bridge cap table.
- **The founder memo is understandable to a non-expert reader** and answers "why this and not the alternatives" with specific numbers.
- **The lead-investor talking points include specific participation asks with dollar amounts.**
- **The board consent authorises the specific chosen structure** with the specific parameters (cap, size, per-share price, or note terms as applicable).
- **The updated capital plan shows the post-bridge cash-out date and updated trigger distances.**

## Deliverables

- The pro-forma cap-table workbook (spreadsheet).
- The decision-framework memo (Markdown or PDF).
- The founder / CEO memo (Markdown or PDF).
- The lead-investor talking points (Markdown or PDF).
- The board consent draft (Markdown or PDF).
- The updated capital plan memo (Markdown or PDF).

## Extensions (optional)

- **Second scenario:** the Series-A lead's fund does not have follow-on dry powder for the bridge. Rerun the framework — the extension is now off the menu because the lead cannot lead it. Which structure wins now, and what is the signalling cost?
- **Third scenario:** the KPIs are meaningfully worse than in the base scenario (ARR at $5M not $7.5M; net-new-ARR at $80K/month). The bridge is now bridging into what may be a down round. Rerun the framework and consider whether the answer shifts toward the note (with the maturity clock being a feature, not a bug, if the situation deteriorates further).
- **Model a "bridge with warrants" package** where the bridge SAFE or note is accompanied by warrant coverage for the participating investors. Quantify the incremental dilution.
- **Author the retrospective memo** the CFO would write 12 months from now under each of the three next-round scenarios. The memo answers: "did the structure choice hold up?"
