# Exercise 07 — ISO vs. NSO vs. RSU vs. 83(b) Decision Matrix

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 7 (equity-comp toolkit — ISO, NSO, RSU, 83(b), early exercise, QSBS, secondary).

## Problem statement

For a set of six real-shaped hires at different stages of a company's lifecycle, produce the equity-comp instrument recommendation for each, with the full tax-outcome analysis for the employee at each of grant / vest / exercise / sale, and the ASC 718 / compensation-expense implication for the company. Then, for one of the hires, author a **grant explanation memo** that would go to the employee to explain their offer's equity structure in plain language.

The exercise proves that the instrument choice is not one-size-fits-all and installs the muscle memory for the CFO to make the choice per hire.

## The six hires

Design the specifics (name, exact numbers) to suit your scenario, but the archetypes are:

1. **Founder-equivalent early hire (Employee #4).** Joins the company at Month 3 post-formation. FMV per 409A: $0.05/share. Grant: 500,000 shares. Company culture: aggressive early-exercise. Employee can afford $25,000 up front.
2. **Series-A senior engineer.** Joins immediately after Series-A. FMV per 409A: $1.20/share. Grant: 40,000 shares. Total notional at grant FMV: $48K. Company allows early exercise; employee can afford up front but is undecided.
3. **Series-A GTM director.** Joins immediately after Series-A. FMV per 409A: $1.20/share. Grant: 30,000 shares. Employee cannot afford early exercise up front. Company grants a mix of ISO / NSO.
4. **Series-B mid-level engineer.** Joins post-Series-B. FMV per 409A: $2.60/share. Grant: 15,000 shares. Total notional: $39K. Company does not offer early exercise at this stage.
5. **Series-C VP of Sales.** Joins post-Series-C. FMV per 409A: $8.00/share. Grant: 200,000 shares. Total notional: $1.6M — well above the $100K ISO annual limit. Company issues a mix of options and RSUs at this level.
6. **Late-stage (pre-IPO) VP of Engineering.** Joins ~12 months pre-IPO. FMV per 409A: $18.00/share. Grant: 150,000 shares. Total notional: $2.7M. Company grants primarily RSUs with double-trigger settlement at IPO / acquisition. The offer includes participation in the pending secondary tender offer for prior grants.

## Requirements

Produce a single spreadsheet or notebook with the following:

1. **Per-hire equity instrument recommendation.** For each of the six hires, a row with:
   - Recommended instrument (Restricted Stock / ISO / NSO / RSU / mix — specify the split).
   - Vesting schedule (4-year / 1-year cliff / monthly is default; note any deviation).
   - Early-exercise availability and recommendation to the employee.
   - 83(b) election (yes if restricted stock or early-exercised options; NA otherwise).
   - QSBS eligibility (yes / no / partial; explain).
   - Acceleration (none / single-trigger / double-trigger; explain).
2. **Per-hire employee tax outcome analysis.** For each hire, walk through the four tax moments — grant, vest, exercise (if applicable), sale — and produce the expected federal tax under a plausible exit scenario (pick $200M exit at Year 6 or similar). For each moment, name:
   - Tax character (no tax / ordinary income / capital gain / AMT positive adjustment).
   - Estimated dollar amount at plausible federal rates (37% for ordinary income; 20% + 3.8% NIIT for LT cap gains; 28% AMT rate on AMT positive adjustments).
   - Whether the employee has cash to pay the tax at that moment or whether it's a "phantom income" problem.
   Also compute the **employee's net take-home** at the exit event, in dollars, after all federal tax.
3. **Per-hire company implications.** For each hire, name:
   - The ASC 718 compensation expense at grant (Black-Scholes fair value of options × shares; or FMV × shares for RSUs at grant), amortised over the vesting period. High-level; you don't need to compute Black-Scholes precisely, but note the order-of-magnitude expense per year.
   - The compensation-expense deduction the company gets (NSO exercise: deduction of the spread; ISO qualifying: no deduction; ISO disqualifying: deduction of the ordinary-income portion; RSU settlement: deduction of the FMV).
   - The Rule 701 consumption of this grant (from Chapter 6 / Exercise 06 mechanics).
   - Any 409A / diligence risk if the grant is misstructured.
4. **Comparative matrix.** A single table showing the six hires as columns and the key decisions as rows (instrument, vest, early exercise, 83(b), QSBS, acceleration, tax outcome for employee at exit). The matrix should read left-to-right as a lifecycle progression from Employee #4 through the late-stage VP, showing how the instrument choice evolves with stage.
5. **Grant-explanation memo (2-3 pages).** For **one** of the six hires (recommend Hire #2 or Hire #5 — the middle stages have the most decision content), author a memo the CFO / people team would give the employee alongside the offer letter. The memo:
   - Explains the specific instrument in plain language (no jargon; assume the employee has never encountered options / RSUs before).
   - Walks through the tax outcome at each of grant / vest / exercise / sale.
   - Explains the 83(b) election (if applicable) — what it is, why it matters, and the 30-day deadline.
   - Explains early exercise (if applicable) — the cost, the risk, and the tax benefit.
   - Explains QSBS at a high level (if applicable) — what it is and what the employee should do to preserve eligibility.
   - Names the company's specific policies that apply (early-exercise availability, acceleration terms, refresh policy at the company).
   - **Names three things the employee should do**: file the 83(b) if applicable, keep the option-grant agreement and 409A citation on file, and consult a personal tax advisor before any exercise decision.
   - Names three things the employee should NOT do: assume the offer letter is complete tax advice, delay the 83(b) election past 30 days, or exercise ISOs deep-in-the-money without AMT planning.
6. **Common mistake register (1 page).** A short list of the top 5-7 mistakes an employee or CFO typically makes with each instrument, and how to prevent them:
   - Missed 83(b) window.
   - ISO exercise triggering AMT without planning.
   - NSO exercise without cashless-exercise structure (employee owes ordinary-income tax and doesn't have cash).
   - Private-company RSU settlement at IPO creating unmanageable tax bill.
   - QSBS 5-year clock not tracked; sold too early.
   - Secondary tender participation that inadvertently terminates QSBS on unrelated shares.
   - Grant to a non-eligible person (e.g., a consultant LLC) that fails Rule 701.

## Starter guidance

- **Do not try to be a tax advisor.** Say things like "estimated at 37% federal ordinary rate assuming employee is in the top bracket" or "AMT at 28% on the positive adjustment" and note that state tax is separate. The point of the exercise is to show the *shape* of the outcome, not to produce filing-quality numbers.
- **For QSBS, name the specific requirements** each hire meets or doesn't. The Series-A senior engineer probably qualifies (C-corp, gross assets < $50M at grant, active business). The pre-IPO VP probably does not because gross assets exceeded $50M by the time of grant.
- **Early exercise + 83(b)** is the most tax-efficient path for hires who can afford it. Emphasise this in Hires #1 and #2. It's not available or not sensible for #4-6.
- **RSUs at late stage** are simpler and less tax-optimal but more understandable and less risky. This is the trade-off.
- **The grant-explanation memo is the deliverable that matters for the hire.** Write it in plain English. A real employee who reads it should be able to (a) file their 83(b) if applicable, (b) understand what tax they'll owe when, and (c) know what questions to ask their own advisor.
- **The comparative matrix is the artefact for the CFO.** It's the one-page cheat sheet that gets referenced for each new hire.

## Acceptance criteria

- **Six hires, six recommendations**, each with the six-line decision (instrument, vest, early exercise, 83(b), QSBS, acceleration).
- **Tax outcome analysis for each hire** at each of the four moments (grant, vest, exercise, sale), with dollar amounts at plausible rates.
- **Employee net take-home at exit** is computed for each hire in dollars.
- **Company implications** (ASC 718 expense, deduction, Rule 701 consumption) are noted for each hire.
- **The comparative matrix reads left-to-right** as a stage progression showing how the instrument choice evolves.
- **The grant-explanation memo is written in plain English** and covers all the required elements.
- **The common-mistake register names 5-7 real mistakes** with prevention guidance.

## Deliverables

- The workbook with the per-hire tables and the comparative matrix.
- The 2-3-page grant-explanation memo (Markdown or PDF).
- The 1-page common-mistake register.

## Extensions (optional)

- **Model an early-exercise + 83(b) outcome vs. no-early-exercise for Hire #2** with a common assumed exit at $8/share at Year 6. Compute the specific tax difference in dollars.
- **Model the ISO $100K limit calculation for Hire #5.** Given a $1.6M notional grant vesting monthly over 4 years, show the year-by-year ISO/NSO split.
- **Author the double-trigger RSU settlement analysis for Hire #6** at an IPO event: show the timing of income recognition, employer withholding options (sell-to-cover, net-share-settlement, cash-payment), and the tax cash-flow the employee faces.
- **Add a founder-refresh grant scenario** (a founder receiving an additional grant at Series-B). Analyse the tax and 83(b) treatment given the founder is already past the $100K ISO limit and the FMV is now much higher.
- **Interview a real employee (or CFO)** who has been through an exit at a private company and ask them what they wish they had known about their equity before the exit event. Compare to the chapter material.
