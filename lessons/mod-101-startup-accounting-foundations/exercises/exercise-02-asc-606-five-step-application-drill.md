# Exercise 02 — ASC 606 Five-Step Application Drill

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 2 (ASC 606 five-step model).

## Problem statement

Take three realistic SaaS customer contracts of varying complexity and apply the ASC 606 five-step revenue recognition model to each. Produce a per-contract revenue-recognition schedule showing dollar-of-transaction-price by month for the full contract term. Produce a written revenue-recognition policy memo that documents the judgement calls made and the rationale for each.

The goal is fluency in the standard: after this drill you should be able to look at any SaaS order form and produce a defensible ASC 606 recognition schedule within an hour.

## Scenario — three contracts

Construct or use three real contracts covering the following patterns. If constructing hypothetical contracts, write them at order-form-plus-key-terms detail — not just a summary. Include the full economic and delivery terms.

**Contract A — clean annual subscription.** Single product, annual contract, single billing, no implementation, no add-ons, no discounts, no variable consideration.

**Contract B — subscription + distinct implementation + training.** Annual SaaS subscription with a substantive four-week implementation engagement (billed separately at signature) and a two-day training package (billed separately). Include a signing discount that spans the whole contract.

**Contract C — subscription + variable usage-based add-on + SLA credit.** Annual base subscription with a metered API-call add-on billed monthly in arrears against a tiered price schedule. SLA credit of up to $X per month if uptime falls below 99.9%. Optionally, a one-time payment to the customer as a "sign-on rebate" — describe whether it is in exchange for something distinct.

## Requirements

For each of the three contracts, produce:

1. **Step 1 — Contract identification.** Confirm the five criteria (approval, identifiable rights, identifiable payment terms, commercial substance, collectibility probable) are met. Cite the fact for each. State the enforceable contract term (with attention to termination-for-convenience clauses if present).
2. **Step 2 — Performance obligation identification.** List every promise in the contract. Apply the "distinct" test to each. Combine or separate as the analysis requires. Document the rationale for any close calls (especially for implementation).
3. **Step 3 — Transaction price determination.** Compute fixed consideration, variable consideration (with expected-value or most-likely-amount method stated), any constraint on variable consideration, contra-revenue items, and any significant financing component. State any ASC 606-10-32-2A sales-tax policy election.
4. **Step 4 — Allocation to performance obligations.** Compute standalone selling price for each PO (with the SSP method — observable, market-assessment, cost-plus-margin, or residual). Allocate the transaction price to each PO based on SSP ratios. Show the arithmetic.
5. **Step 5 — Recognition schedule.** Produce a month-by-month recognition schedule for each PO from contract start through end of term. Distinguish over-time vs. point-in-time recognition per PO. Show the method (straight-line time-elapsed, units delivered, milestone-based, etc.).
6. **Consolidated monthly-revenue schedule.** For each contract, sum the per-PO schedules into one monthly total. Verify the total equals the total transaction price.

Then produce:

7. **Revenue-recognition policy memo (2-4 pages).** Document the company's policy positions supported by the three contracts. Sections: contract identification standard, performance-obligation identification for common patterns (subscription, implementation, training, add-ons, usage), transaction price (variable-consideration methods, constraint, sales-tax policy, treatment of consideration paid to customers), allocation (SSP methodology), recognition methods, contract modification handling. Cite the specific ASC 606 paragraphs for each position (e.g., "ASC 606-10-25-19 — distinct within the context of the contract"). Note any positions where more than one defensible answer exists and state which the company will apply.

## Starter guidance

- The three-contract set is deliberately chosen to force each step of the model to bite. Contract A is trivial; contract B forces the distinct-PO analysis and SSP-based allocation; contract C forces variable-consideration estimation and constraint.
- For the distinct-PO analysis on implementation, the two most-cited factors are (i) can other vendors perform the implementation (or does only the vendor's team have the specialised knowledge); and (ii) can the customer use the SaaS without our implementation. Write the answer for both factors.
- For SSP estimation, if you do not sell the component separately (implementation, for example), the residual method is only permitted in specific circumstances — read ASC 606-10-32-34 before using it. Default to a cost-plus-margin or market-assessment estimate.
- The revenue-recognition policy memo is the artefact an auditor asks for first. Write it as a document that will be handed to an external CPA firm.

## Acceptance criteria

- **Each contract has all five steps documented.** No skipping.
- **The recognition schedule totals equal the transaction price** for each contract, to the dollar.
- **Judgement calls are cited.** Every close call (distinct-PO, SSP method, variable-consideration method, constraint application) references the specific ASC 606 paragraph.
- **The policy memo covers every judgement made in the three contracts.** If contract B forced a distinct-implementation call, the memo has a "distinct implementation" section with the company's default position.
- **The memo is internally consistent.** The three contracts' individual analyses all conform to the general positions in the memo. If they don't, either the memo is wrong or one of the contracts was analysed differently from the policy — either way, reconcile.

## Deliverables

- Spreadsheet with per-contract five-step workpaper and per-month recognition schedule for each contract.
- Revenue-recognition policy memo (Markdown or PDF).

## Extensions (optional)

- Add a fourth contract with a multi-year term (three years, upfront prepay) to force the significant-financing-component analysis.
- Add a contract-modification event (customer upgrades mid-term with a partial-year credit) and walk the ASC 606 modification treatment.
- Produce the parallel IFRS 15 analysis for one of the contracts and identify any recognition differences (typically none for a straightforward SaaS subscription; differences may arise on variable-consideration constraint and licence-classification).
