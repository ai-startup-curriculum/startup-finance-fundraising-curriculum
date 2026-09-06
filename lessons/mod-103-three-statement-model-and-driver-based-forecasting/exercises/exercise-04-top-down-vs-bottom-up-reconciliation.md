# Exercise 04 — Top-Down vs. Bottom-Up Reconciliation

**Estimated time:** ~3 hours
**Prerequisites:** Chapter 5 (top-down vs. bottom-up reconciliation). Exercises 01-03 (the driver architecture, the hiring plan, and the funnel-driven bottom-up revenue trajectory).

## Problem statement

For the same company you modelled in exercises 01-03, author both a *top-down* TAM / SAM / SOM view and a *bottom-up* funnel / cohort view of year-3 ARR, tie the two together at the same forecast horizon, and write the one-page reconciliation memo a CFO puts in front of a Series-A lead investor.

The point of the exercise is not to make the two views agree by adjusting numbers until they do. It is to build both views honestly, observe where they agree and where they diverge, and produce the CFO-narrative that names the disagreement, its cause, and the action it drives. If the two views converge cleanly, the exercise is trivial. If they diverge — which is the more common case — the disagreement is the most useful diagnostic the model produces this cycle.

## Scenario — build both views for the same company

Use the company from exercises 01-03. The bottom-up view already exists (the cohort revenue schedule from exercise 03 produces the year-1, year-2, year-3 ARR trajectory). The top-down view is what you author here.

For the top-down side, you will need:

- A defined *category* the product sells into — the noun a market-research firm would recognise (e.g., "workflow automation for marketing teams", "observability for cloud-native infrastructure", "revenue-intelligence for B2B sales orgs").
- A defined *ICP* — the buyer segment the sales motion targets, described specifically enough to be counted (industry, company-size band, geography, seniority of the buyer, tech-stack signals).
- A defined list-price anchor — the ACV band the sales motion actually sells at today (from exercise 03's ACV assumption).
- A geographic scope reflective of the current sales motion (US-only, US + EMEA, global English-speaking, etc.).

## Requirements

Add the following to the workbook and produce the accompanying memo.

1. **TAM tab.** Author all three TAM-construction methods from chapter 5 and reconcile the three numbers:
   - **Top-down from industry research.** Cite a specific published industry-report number (Gartner, IDC, Forrester, Statista, or a comparable analyst source; a public company's 10-K "market opportunity" section is acceptable). Apply the filter cascade to get from the raw industry number to SAM: geography filter, segment filter, use-case filter, price-band filter. Every filter's percentage is documented with a source or a stated assumption.
   - **Bottom-up count × price × attach rate.** Count the target buyers in the ICP from a source (Crunchbase, ZoomInfo, LinkedIn Sales Navigator, government/trade-association census, SEC filings for public buyers). Multiply by the list-price anchor. Apply an attach-rate assumption (fraction of buyers who would use a product in this category at all). This is the most auditable TAM number.
   - **Analog from a comparable company.** Identify a public or well-covered private company that has sold into a comparable market at a comparable stage. Cite the ARR they reached at maturity (from their 10-K / S-1 / a credible analyst report). Treat this as a floor on the TAM.
   - **SAM.** Filter TAM to the specific geography, segment, and motion the company plays in.
   - **SOM.** The realistic slice of SAM the company could win within 5 years, given competitive dynamics. Named-competitor list, current share breakdown if known, and a defended share estimate for year 5.
2. **Bottom-up view — extract from exercise 03.** On a summary tab, pull the bottom-up ARR trajectory from the cohort schedule: year-1, year-2, year-3 ARR under the base case (base scenario, from the scenario switch). Show the ARR at year-end for each of the three years.
3. **Penetration table.** Compute implied year-3 penetration = `bottom-up year-3 ARR ÷ SAM`, using each of the three TAM methods separately. Three penetration numbers, one per method.
4. **Capacity check.** From the hiring plan (exercise 02) and the funnel assumptions (exercise 03), verify that the year-3 bottom-up ARR is producible by the modelled S&M organisation. Specifically:
   - Required new logos in year 3 = `year-3 new ARR ÷ year-3 average ACV`.
   - Required SQL volume = `required new logos ÷ close rate`.
   - Required SDR headcount = `required SQL volume ÷ SDR productivity ÷ 12`.
   - Modelled SDR headcount at year 3 = from the hiring plan.
   - Gap = required − modelled. Zero or negative gap means the plan is producible; positive gap means the hiring plan cannot support the assumed ARR.
5. **Growth-rate ceiling check.** From the top-down view, estimate the market's own growth rate (industry-report CAGR, or an analog-based estimate). Compare to the bottom-up implied ARR growth rate at year 3. If the company's growth rate exceeds the market's by 5-10× at year 3, name the source of the excess growth (share-take from a named competitor, category expansion, geography expansion, etc.).
6. **Reconciliation memo (one page).** The output the CFO puts in front of the board and lead investor, structured per chapter 5:
   - Bottom-up ARR trajectory with base / upside / downside numbers (from the scenario switch in exercise 05 if built; if not, base only).
   - TAM decomposition — the three method numbers side by side, with the SAM/SOM cascade.
   - Implied penetration — the three numbers from the penetration table.
   - The gap — where the two views agree, where they disagree, and the shape of the disagreement (one of the four shapes from chapter 5, or a named alternative).
   - The action — what the disagreement implies for the plan (grow the hiring plan, expand the SAM decomposition, revise the bottom-up plan downward, or "both views agree — no action required").
   - Any market-creating adjustments (if the product is in a greenfield category, the adjacent-market or adoption-curve construction).
7. **Optional: a chart on the TAM tab** showing the funnel from TAM → SAM → SOM → bottom-up year-3 ARR as a waterfall. Useful for the memo appendix.

## Starter guidance

- **Do the top-down build before writing the memo.** The memo's shape depends on which of the four disagreement patterns emerges. Writing the memo first commits you to a story before the numbers can tell you which story is real.
- **Cite every top-down number to a source.** "$50B market" with no citation is worse than no top-down number at all — investors will discount an uncited TAM to zero. If you cannot find a source, mark it `<!-- needs-research: source for [claim] -->` in the memo rather than typing a plausible-looking number.
- **The bottom-up count × price is the most-defensible TAM method.** Even if the number is smaller than the top-down industry-report number, an auditable smaller TAM is worth more in diligence than a large uncited one.
- **The capacity check is the most-neglected part of the reconciliation.** Chapter 5's shape 3 (fine ARR but hiring can't produce it) is the most common real-world failure. Do the capacity check even if the ARR-vs-SAM penetration looks fine.
- **The memo is one page. Not "one page front and back." Not "one page plus appendix." One page.** Every additional page is a diligence question the CFO didn't compress into an answer.
- **Do not adjust the bottom-up ARR to match the top-down ceiling.** The reconciliation is honest reporting of a disagreement, not manufactured consistency. Adjusting the bottom-up to match the TAM view is what produces the "the plan matches the market" answer that investors know is fake.

## Acceptance criteria

- **All three TAM-construction methods are authored** with sources for every input. Every filter percentage in the top-down cascade is cited or marked as an assumption.
- **The penetration table produces three numbers**, one per TAM method, all sourced correctly from the bottom-up year-3 ARR ÷ the respective SAM number.
- **The capacity check computes required SDR headcount and compares it to modelled headcount** from the hiring plan. The gap (positive or negative) is named.
- **The growth-rate ceiling check compares bottom-up year-3 growth to market growth** and, if the bottom-up exceeds the market, names the source of excess growth.
- **The one-page reconciliation memo covers all five sections** — bottom-up trajectory, TAM decomposition, implied penetration, the gap, the action.
- **The memo names one of the four disagreement shapes** from chapter 5 (or "both views agree") and defends the naming.
- **Sources are auditable.** Every citation is a live URL or a document/report the reviewer can locate. `<!-- needs-research -->` markers are used where a source could not be verified rather than manufactured citations.

## Deliverables

- The updated workbook with the TAM tab, penetration table, capacity check, and growth-rate ceiling check.
- The one-page reconciliation memo (Markdown or PDF).
- A short (max half-page) sources memo listing every top-down source cited, with URL and access date.

## Extensions (optional)

- Build the TAM view for a second geography (e.g., current is US-only; extend to US + EMEA) and produce the incremental SAM and the incremental hiring-plan implication. This is the "should we expand to EMEA next year" analysis in condensed form.
- For a market-creating product (if applicable), author both the adjacent-market anchor and the adoption-curve construction described in chapter 5, and produce a range of year-5 ARR ceilings from the two methods.
- Run the top-down build for one direct competitor using their public information (S-1, 10-K, press releases). Compare their penetration trajectory to yours and note where the two diverge.
- Author a second version of the capacity check using productivity ranges from a published benchmark (OpenView SaaS Benchmarks or Bridge Group SDR reports) rather than your own historical productivity. Report where your assumption sits inside the published band.
