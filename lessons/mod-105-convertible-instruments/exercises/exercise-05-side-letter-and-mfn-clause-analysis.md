# Exercise 05 — Side Letter and MFN Clause Analysis

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 5 (side letters and MFN amendments). Also uses chapter 1 (post-money SAFE anatomy) and chapter 4 (stacked-convertibles priced-round pro-forma).

## Problem statement

Take a three-closing seed programme in which every SAFE carries a different side-letter posture — one with elective MFN and pro-rata rights, one with an "automatic" pull-through MFN and no pro-rata, one with pro-rata rights only and no MFN — and drive the MFN cascade forward through each subsequent closing. Quantify what each MFN election costs the founder in percentage points and in dollars at the Series-A closing. Then take a real problem side letter (constructed in the scenario below), redline the hazardous clauses, and produce a clean counter-draft plus a memo to the founder explaining what changed and why.

The drill has three purposes. First, to build the reading habit of "which side-letter clauses reshape the cap table vs. which shape the operational relationship." Second, to make the MFN back-propagation arithmetic concrete rather than abstract. Third, to develop the drafting instinct — knowing which clauses to refuse, which to accept with a threshold, and which to reshape rather than reject outright.

## Scenario — the three closings

Construct a hypothetical Delaware C-corp with a standard two-founder starting cap table (8,000,000 founder common; 1,000,000 unissued option pool; no other securities). Run the following three SAFE closings, in the order given, with the side-letter postures described:

- **Closing 1 (T+0 months) — SAFE 1.** $500,000 investment on a $10,000,000 post-money cap, no discount. YC post-money Valuation-Cap-only form (variant 1 from chapter 1). Side letter attached with:
  - **Elective MFN** covering "any subsequent SAFE, convertible security, or similar instrument" issued before the equity financing that triggers conversion.
  - **Pro-rata rights** on the next priced round, with a $250,000 major-investor threshold (which SAFE 1 clears).
  - **Information rights** — annual audited financials, quarterly unaudited financials, an annual investor letter.
  Investor: institutional seed lead.

- **Closing 2 (T+6 months) — SAFE 2.** $250,000 investment on an $8,000,000 post-money cap, no discount. YC post-money Valuation-Cap-only form. Side letter attached with:
  - **"Automatic" pull-through MFN** — amends SAFE 2 to any better subsequent terms without requiring notice from the holder.
  - No pro-rata rights.
  - No information rights.
  Investor: angel with an aggressive counsel.

- **Closing 3 (T+12 months) — SAFE 3.** $750,000 investment on a $5,000,000 post-money cap with a 20% discount. YC post-money Valuation-Cap-and-Discount form (variant 4). Side letter attached with:
  - **No MFN** (this is a later-in-time SAFE and the terms are already the best on the table).
  - **Pro-rata rights** on the next priced round, no major-investor threshold.
  - Information rights matching SAFE 1's.
  Investor: strategic corporate investor writing at a favourable cap because the raise was needed for a specific milestone.

**Priced round (T+18 months) — Series A.** $8,000,000 raised on $20,000,000 pre-money / $28,000,000 post-money, with a 10% post-close option pool placed pre-money per the term-sheet default.

## Requirements

Produce a single workbook (Excel or Google Sheets) plus two written artefacts (the redline memo and the founder memo):

1. **Instrument register.** One row per SAFE with: investor, variant, investment, cap, discount, closing date, corporate-record reference (fictional IDs — SAFE-01, SAFE-02, SAFE-03).
2. **Side-letter register.** One row per SAFE mirroring the instrument register with columns for: MFN present (Y/N), MFN mechanic (elective / automatic / none), MFN scope (SAFE-only / any convertible / any security), pro-rata rights (Y/N), pro-rata threshold, pro-rata expiry, information rights (Y/N with content list), board observer rights (Y/N), other custom clauses.
3. **MFN cascade timeline.** Walk each closing forward in time. At each closing, for each earlier SAFE with an active MFN:
   - Compare the new SAFE's terms against the earlier SAFE's current terms (which may already have been amended by an earlier MFN).
   - Determine whether adopting any subset of the new terms is more favourable to the earlier holder.
   - For elective MFNs, record the specific election the holder would rationally make and produce the amended terms.
   - For automatic MFNs, record the amendment as executed at the moment of the new SAFE's signing without requiring an election.
   - Produce the "current effective terms" for each SAFE after each closing.
4. **Pre-cascade vs. post-cascade pro-forma.** Two Series-A pro-forma cap tables:
   - **Naïve pro-forma**: each SAFE converts at its original signed terms (no MFN elections modelled). This is the number a founder who did not track the side letters would produce.
   - **Correct pro-forma**: each SAFE converts at its post-cascade effective terms. This is the number that the diligence firm will produce.
   Both use the four-share-count header (mod-104 chapter 1) and reconcile to the priced-round term sheet.
5. **The MFN cost table.** For each SAFE with an active MFN, quantify:
   - The original post-conversion percentage of pre-new-money FD (from the naïve pro-forma).
   - The post-cascade post-conversion percentage (from the correct pro-forma).
   - The delta in percentage points.
   - The dollar value of the delta at the $28M post-money valuation.
   - The specific closing event that caused each amendment.
   Sum the MFN cost across the three SAFEs. Attribute the total cost to the founder (i.e., the dilution the founder took that would not have happened absent the MFN elections).
6. **Pro-rata absorption analysis.** For the correct pro-forma, compute:
   - The pro-rata cheque each pro-rata-holding SAFE holder is entitled to write at the Series A, expressed as a dollar amount (their post-conversion percentage of the $8M new-money raise).
   - The aggregate pro-rata allocation across all SAFE holders with pro-rata rights.
   - The residual allocation left for the new Series-A lead after pro-rata cheques.
   - Whether the residual is enough for the lead's target 25% post-money ownership, and if not, what adjustment (larger raise, waived pro-rata, expanded pool) is needed.
7. **Side-letter redline.** The scenario side letters are all serviceable, but suppose the founder is presented with a **fourth SAFE (SAFE 4)** at T+15 months (three months before the Series A) whose proposed side letter contains the following clauses. Redline the draft — accept, revise, or refuse each — and explain the reasoning in one to two sentences per clause. Then produce a clean counter-draft with only the clauses the founder should accept as drafted.
   - **Clause A**: "Investor shall have the right to elect the terms of any subsequent SAFE, convertible security, or similar instrument issued by the Company at any time, whether prior to or following the Equity Financing."
   - **Clause B**: "Company shall grant Investor a broad-based weighted-average anti-dilution adjustment upon issuance of any subsequent SAFE at a valuation cap lower than the cap in this SAFE."
   - **Clause C**: "Investor shall have the right to require the Company to redeem this SAFE at the greater of the invested amount and the fair market value of the underlying shares upon the fifth anniversary of the closing date if no Equity Financing has occurred."
   - **Clause D**: "Investor shall have pro-rata rights on all future financings for the life of Investor's ownership of any securities of the Company, without any major-investor threshold and without any expiration."
   - **Clause E**: "Founders shall not, without Investor's prior written consent, transfer, encumber, or pledge more than 5% of their common stock during the three-year period following the closing date."
   - **Clause F**: "Company shall deliver to Investor, within 15 business days of the end of each calendar month, unaudited financial statements, cash-flow forecasts, hiring plans, and any board materials distributed since the prior report."
   - **Clause G**: "Investor shall have the right to appoint one board observer, who shall have the right to attend all board meetings including executive sessions and to receive all board materials."
   - **Clause H**: "This SAFE and the associated side letter shall be freely assignable by Investor to any third party without the Company's consent."
8. **Founder memo (two pages).** Written to the founder ahead of the Series-A signing. Contents:
   - The bottom-line MFN cost from step 5, expressed in percentage points of founder ownership and in dollars at the $28M post-money valuation.
   - A summary of the pro-rata absorption from step 6 and its effect on the Series-A lead's allocation.
   - Two or three specific side-letter drafting rules the founder should adopt going forward, based on the redline in step 7 (e.g., "elective MFN only, scoped to SAFE-shaped instruments"; "no redemption rights in a SAFE"; "pro-rata threshold and expiry always").
   - A "no undisclosed side letters" representation the founder can honestly make at the Series-A closing, referencing the side-letter register from step 2.

## Starter guidance

- **Build the side-letter register before the MFN cascade.** The cascade arithmetic is trivial once the register is complete; without the register, it's easy to miss which SAFEs carry MFN in the first place.
- **Walk the timeline forward, not backward.** At each closing, evaluate each earlier SAFE's MFN against the new SAFE. Do not try to compute all cascades at once — the intermediate state after each closing is what carries into the next.
- **For the SAFE 1 MFN at the SAFE 2 closing.** SAFE 2's terms are $8M cap. SAFE 1's original terms are $10M cap. Adopting SAFE 2's cap gives SAFE 1 holder more shares per dollar (`$500K / $8M = 6.25%` vs. `$500K / $10M = 5.00%`). SAFE 1 holder rationally elects. SAFE 1's effective cap is now $8M.
- **For the SAFE 1 and SAFE 2 MFNs at the SAFE 3 closing.** SAFE 3's terms are $5M cap with 20% discount. Both SAFE 1 (currently $8M cap after the earlier election) and SAFE 2 (automatic; already amends without election) will adopt the more-favourable terms. SAFE 2 amends automatically upon SAFE 3's signing. SAFE 1's holder elects. Both end at $5M cap with 20% discount.
- **The MFN election can cherry-pick.** The elective MFN in SAFE 1 lets the holder pick "any subset" of SAFE 3's terms. At the SAFE 3 closing, the holder will adopt the $5M cap and the 20% discount. If SAFE 3 had also carried a term unfavourable to SAFE 1 (say, a shorter dissolution priority), the holder would refuse that.
- **The automatic MFN gives no negotiation gap.** SAFE 2's holder does not need to send notice; the amendment fires the moment SAFE 3 is signed. This is why the automatic mechanic is more dangerous to the founder: there is no window in which the founder can go back to SAFE 2's holder and negotiate an alternative before the amendment takes effect.
- **Compute the pro-forma with iterative calculation enabled.** The three SAFEs plus the pool top-up plus the priced round produce a coupled system; solve iteratively per chapter 4.
- **For the pro-rata absorption**, do not assume every pro-rata-holding investor will actually write their cheque. The requirement in the pro-forma is to compute the *entitlement*; the memo can discuss expected behaviour (institutional seed leads almost always exercise; smaller investors sometimes waive).
- **For the redline in step 7**, use the "what good drafting looks like" list at the end of chapter 5 as your checklist. Every clause failing that checklist gets a redline; the memo explains why in the founder's language, not the lawyer's.
- **The cost of a redline is not always founder-favourable.** Some clauses (e.g., pro-rata rights within reason) are the price of doing business with institutional investors. The redline should be surgical — refuse the genuinely hazardous clauses, revise the salvageable ones, accept the ones that are standard.

## Acceptance criteria

- **The side-letter register captures all clauses** across the three SAFEs, with the MFN mechanic (elective vs. automatic) correctly identified.
- **The MFN cascade timeline produces the correct amended terms** at each closing. SAFE 1 ends the seed programme at $5M cap with 20% discount (post two elections). SAFE 2 ends at $5M cap with 20% discount (post one automatic amendment). SAFE 3 is unchanged.
- **The naïve vs. correct pro-forma comparison quantifies the total MFN cost** in percentage points and in dollars. Expect a founder-dilution delta of several percentage points once both SAFE 1 and SAFE 2's caps drop to $5M with a discount.
- **Each SAFE's post-cascade `investment / post-money cap` identity holds** in the correct pro-forma (with discount adjusting the effective price as needed).
- **The pro-rata absorption analysis** correctly computes each pro-rata holder's dollar entitlement and identifies whether the Series-A lead's residual allocation meets their target.
- **The redline classifies each of the eight clauses** (A-H) as accept / revise / refuse with specific reasoning tied to the chapter 5 hazards list.
  - Clause A: refuse (MFN should not extend past the Equity Financing; sweeps in future preferred).
  - Clause B: refuse or heavily revise (functional MFN-plus; over-scoped anti-dilution).
  - Clause C: refuse (redemption right turns the SAFE into a debt instrument with soft maturity).
  - Clause D: revise (add major-investor threshold; add expiration after N rounds).
  - Clause E: refuse (founder vesting and personal share transfer is founder business, not investor business at seed).
  - Clause F: revise (monthly board-material delivery is invasive at seed; scale back to quarterly financials + annual investor letter).
  - Clause G: revise (observer rights should be subject to confidentiality and executive-session exclusion, per chapter 5 drafting guidance).
  - Clause H: refuse (free assignability without company consent lets the SAFE walk to a downstream investor uncontrolled).
- **The clean counter-draft** contains only clauses the founder should accept, with the revisions from the redline incorporated.
- **The founder memo makes a specific "no undisclosed side letters" representation** the founder can honestly sign at the Series A, backed by the side-letter register.

## Deliverables

- The workbook with the instrument register, side-letter register, MFN cascade timeline, naïve pro-forma, correct pro-forma, MFN cost table, and pro-rata absorption tabs.
- The redline memo (Markdown or PDF) with the eight-clause analysis and the clean counter-draft.
- The two-page founder memo (Markdown or PDF).

## Extensions (optional)

- **Add a fourth SAFE** at T+9 months with an elective MFN and a $9,000,000 cap. Re-run the cascade. Show how introducing an intermediate-cap SAFE with MFN in the middle of the sequence changes the cascade path (specifically, at the SAFE 3 closing all three earlier SAFEs elect and end at the same terms).
- **Model a "MFN removal amendment"** in which the founder, before signing SAFE 3, offers SAFE 1's holder a $9,000,000 amended cap (better than SAFE 1's original $10M but worse than what the MFN would produce at SAFE 3's signing) in exchange for striking the MFN from SAFE 1's side letter. Compare the founder's post-SAFE-3 dilution under: (a) no amendment, MFN fires at SAFE 3; (b) MFN removal at $9M cap; (c) MFN removal at $8M cap. Which trade is founder-optimal, and how does that depend on whether SAFE 3 actually closes at $5M?
- **Trace an integration-adjacent scenario** in which the pro-rata rights on SAFE 1 and SAFE 3 are triggered but the Series-A lead demands the pro-rata cheques be treated as part of a single 506(b) offering under Reg D. Cross-reference with chapter 6 and identify whether pro-rata exercise by the SAFE holders alters the exemption analysis.
- **Interview a startup lawyer** (or use a public conference talk transcript from Cooley, Wilson Sonsini, or Gunderson Dettmer) and add to the redline any additional hazardous side-letter clauses they flag in current-market drafts. Cite the source in the memo.
