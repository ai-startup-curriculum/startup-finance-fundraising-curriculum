# Exercise 04 — Board Consent and Action-Item Register Drill

**Estimated time:** ~4 hours
**Prerequisites:** Chapter 4 (board consents, action items, and the CFO-owned register). Familiarity with the DGCL §141(f) and §228 mechanics from the chapter is required. This exercise pairs well with exercise 02 (the pack) and exercise 03 (the meeting the consents come out of), but does not require them.

## Problem statement

For a specified quarter's worth of board activity at a Series-B Delaware-incorporated C-corporation, draft the written consents for every consent-required item, maintain the running action-item register across the quarter, and produce the corporate-minute-book table of contents that records the quarter's governance activity. The consents must follow DGCL §141(f) and §228 mechanics correctly, be organised as board-only vs. board-and-stockholder items, and be presented in the format an outside law firm's associate could file into the minute book without rewriting.

The exercise trains the specific legal-mechanics discipline that separates a well-run corporate minute book from a minute book the next fundraise's diligence team will flag as disorganised. Consents are load-bearing but unglamorous; a CFO who cannot draft one cleanly is a CFO who will spend the next raise's diligence phase producing after-the-fact consents that should have been signed contemporaneously — a specific diligence red flag.

## Scenario — the quarter's board activity

You are the CFO of a Series-B Delaware C-corporation ($15M ARR, 90 employees, $220M post-money at Series-B close 12 months ago, six directors including two founders, one Series-A lead, one Series-B lead, one independent, plus a Series-B board observer). Over Q3, the following governance events occur.

**Quarterly board meeting (September 15).** At the meeting, the board:

- Approved the prior meeting's minutes (Q2 minutes).
- Approved the annual 409A refresh (a new common-stock fair-market-value of $2.14 per share, effective as of the meeting date).
- Approved four option grants: (a) 25,000 ISOs to a newly-hired Director of Engineering (start date September 5); (b) 15,000 ISOs to a newly-hired Senior PM (start date September 20); (c) 60,000 RSUs to the newly-appointed VP Sales (start date October 1); (d) 5,000 RSUs to a senior advisor (previously approved as an advisor but not yet granted).
- Ratified a previously-approved venture-debt facility with a specific bank ($10M facility, drawable in tranches; the specific term sheet had been circulated in the pack).
- Approved a new sales-and-marketing office lease (24-month term, aggregate rent obligation of $840K, above the $500K aggregate-obligation threshold in the bylaws).
- Voted to defer a decision on a specific strategic-partnership term sheet pending additional analysis (no consent adopted; the deferred decision goes back on the next meeting's agenda).

**Between-meeting activity (September 15 through October 30).** Between the quarterly meeting and the next quarterly meeting, the following consent-required items arise:

- A specific engineering-hire compensation package needs board-committee approval before an offer letter can be signed (the candidate is a VP Engineering; the offer package exceeds the compensation-committee-approved thresholds and requires full-board sign-off).
- A term sheet from a specific enterprise customer includes an unusually broad most-favoured-nation clause; the sales leadership wants to sign it and the CFO believes it warrants a specific consent from the board given the potential impact on future customer pricing (this is a judgement call; document it as such).
- The company decides to grant 8,000 additional RSUs to the new VP Sales as a make-whole for unvested equity at their prior employer; the make-whole was not part of the original comp package approved at the quarterly meeting.
- The company receives a Series-B pro-rata exercise notice from the Series-A lead for a small secondary purchase (buying $500K of common shares from an early employee at the current 409A fair-market-value); the transaction requires board approval under the ROFR and Co-Sale Agreement.

**Stockholder-level consent items.** Also during the quarter:

- The board approves (and stockholders subsequently approve by DGCL §228 written consent) a stock plan amendment increasing the pool size by 500,000 shares.
- The board approves (and stockholders subsequently approve by DGCL §228 written consent) an amendment to the Amended and Restated Certificate of Incorporation reflecting an additional Series-B share issuance from an authorised-but-unissued Series-B tranche closing.

**Committee-level activity (assume the company has a compensation committee formed at Series-B close).** The compensation committee approves individual grants below the full-board threshold for four other rank-and-file hires during the quarter.

## Requirements

Produce a submission directory containing the following.

1. **The consent-categorisation matrix** (`00-consent-matrix.md`). One-to-two pages. A table listing every governance event above, categorised as:
   - **Meeting-vote consent** (approved by vote at the September 15 meeting; the meeting minutes document the vote; no separate written consent required).
   - **Between-meeting board written consent (DGCL §141(f))** — the between-meeting items requiring unanimous board written consent.
   - **Stockholder written consent (DGCL §228)** — the items also requiring stockholder approval.
   - **Compensation-committee consent** — the items delegated to the compensation committee.
   - **Not requiring a consent** — items that were discussed but did not require a formal action.
   - Justify each categorisation with a one-line rationale citing the specific corporate document (bylaws, charter, IRA, stock plan) or DGCL section that governs.

2. **The meeting-vote consents drafted as resolutions in the meeting minutes** (`01-meeting-resolutions.md`). Two-to-four pages. For each meeting-vote consent (409A refresh, four option grants, venture-debt ratification, office lease approval), draft the specific resolution text in the format that appears in the meeting minutes: "RESOLVED, that ..." with the specific action, the specific date, the specific approvals granted, and the specific delegations of officer authority to execute follow-on documents. The resolution text is what gets filed into the minute book alongside the meeting minutes.

3. **The between-meeting board written consents** (`02-board-written-consents/`). One file per consent (four consents). Each consent is drafted per the DGCL §141(f) format:
   - Header: "Action by Unanimous Written Consent of the Board of Directors of [Company Name]."
   - Recitals: the "WHEREAS" preamble establishing the context and the specific authority under DGCL §141(f) and the company's bylaws.
   - Resolutions: the specific "RESOLVED, that ..." action.
   - Signature block for every director entitled to vote; date-of-effectiveness clause ("This consent shall be effective as of the date the last director signs, unless otherwise stated").
   - Distribution note (typically the CFO's cover email accompanying the consent for signature).
   - The four consents:
     - `01-vp-eng-comp-approval.md`
     - `02-enterprise-customer-mfn-consent.md`
     - `03-vp-sales-makewhole-rsu-grant.md`
     - `04-series-a-lead-secondary-purchase-approval.md`

4. **The stockholder written consents** (`03-stockholder-written-consents/`). One file per consent (two consents). Each consent is drafted per the DGCL §228 format:
   - Header: "Action by Written Consent of the Stockholders of [Company Name]."
   - Recitals: DGCL §228 authority, the specific charter provision, the specific stockholder-vote threshold required (which class or classes of stock must approve, and at what percentage).
   - Resolutions: the specific action being approved.
   - Signature block: sufficient stockholders (typically pre-solicited) to reach the required threshold; date-of-effectiveness.
   - Notice-to-non-signing-stockholders clause (per DGCL §228(e), non-signing stockholders must receive prompt notice of the action).
   - The two consents:
     - `01-stock-plan-pool-increase.md`
     - `02-charter-amendment-series-b-additional-issuance.md`

5. **The consent-tracking log** (`04-consent-tracking-log.md`). One page. A running log for the quarter that the CFO maintains as the source-of-truth for what consents are in flight, when they were circulated, when they were fully executed, and where they are filed in the minute book. Columns: consent ID, description, DGCL basis, circulation date, target-signed-by date, actual-fully-executed date, minute-book location, notes.

6. **The action-item register — full-quarter view** (`05-action-item-register.md`). One-to-two pages. The running register the CFO owns across the quarter. Starts with two carried-forward items from the prior quarter (invent plausible items); adds the action items generated at the September 15 meeting (a customer-executive-conversation follow-up for a slipped enterprise deal; a compensation-benchmarking refresh; a strategic-partnership analysis for the deferred decision); adds any action items generated by the between-meeting consents (e.g., "circulate the executed VP Sales make-whole consent to counsel for filing"). Columns: item, owner, opened date, due date, status (open / in-progress / closed / deferred), related decision or consent reference, comments.

7. **The corporate-minute-book table of contents** (`06-minute-book-toc.md`). One page. For Q3, the entries to be filed in the corporate minute book in chronological order: the Q2 meeting minutes (approved at Q3 meeting), the Q3 meeting minutes, the meeting-vote resolutions (appended to the Q3 minutes), the four between-meeting board written consents, the two stockholder written consents, the compensation-committee minutes for the four rank-and-file grants, and any officer-certificate or related-document filings. Each entry: date, document type, document title, brief description, filing location reference.

8. **The counsel-facing cover memo** (`07-counsel-cover-memo.md`). One page. A short cover memo to the company's outside corporate counsel accompanying the quarter's consent pack. Names the consents attached, flags the two judgement-call items (the enterprise-customer MFN consent and the VP Sales make-whole grant), asks counsel to confirm the DGCL basis and the specific charter references, and requests any redlines to the drafted resolutions before final signature circulation.

## Starter guidance

- **Read chapter 4 and the DGCL §141(f) and §228 statutory text before drafting.** The specific DGCL sections are short and well-drafted; a CFO who has not read the statutes cannot draft correctly against them. Both are linked in `resources.md`.
- **Categorise before drafting.** The consent-categorisation matrix is the first deliverable for a reason: the wrong categorisation (drafting a between-meeting board consent when the action was voted at the meeting) produces double-counted authorisation, which reads as sloppy to counsel and to future diligence teams. Get the categorisation right first.
- **The meeting-vote resolutions are the shortest to draft** but the easiest to fail: they must be in the "RESOLVED, that ..." format that matches what a real minute book contains. Look at a sample resolution from Cooley GO or Orrick's founder-content library if unsure.
- **The board written consents use the specific §141(f) preamble.** The "WHEREAS the Board deems it in the best interest of the Corporation ..." preamble followed by "NOW THEREFORE, BE IT RESOLVED ..." is the reference. Non-Delaware companies use the equivalent language for their state; specify the DGCL basis for a Delaware-incorporated company.
- **Unanimous means unanimous.** Every director entitled to vote must sign, or the consent fails as a §141(f) action. Draft the signature blocks for all six directors even if you assume all six will sign in the exercise. If a director might reasonably not sign (a specific conflict-of-interest scenario), draft a separate meeting-vote path for that item and note the alternative.
- **The stockholder consents are trickier.** DGCL §228 requires only a majority (or a higher threshold per the charter) rather than unanimous, but the specific classes of stock that must approve and at what percentage depends on the charter. For the pool increase, common-plus-preferred-voting-together is typical; for a charter amendment affecting the Series-B, a Series-B-only class vote is typically required in addition. Cite the specific charter provision (or a placeholder reference to it) in the consent's recitals.
- **The consent-tracking log is a real operational artefact.** Do not treat it as ceremonial. In a real company, the log answers "have we filed the executed VP Engineering consent yet, or is it still out for signature" without a search. Include the log fields that make that answer easy to retrieve.
- **The action-item register carries forward.** The Q3 register includes at least one item carried from Q2, plus new items from Q3, plus explicit closures of items that completed in Q3. This is the discipline that makes the register a real governance tool rather than a stack of unresolved items.
- **The counsel-facing cover memo respects counsel's role.** The CFO drafts; counsel confirms. Do not draft as if the consents are final; explicitly ask counsel to redline. This is a chapter-4 discipline that keeps the CFO within the CFO's own scope (economic and governance drafting) rather than practising law.
- **No fabricated legal citations.** If a specific DGCL section, charter provision, or bylaw threshold is referenced, cite the section number correctly or mark `<!-- needs-research: verify DGCL §XXX applicability -->`.

## Acceptance criteria

- **All eight deliverables present.** Categorisation matrix, meeting-vote resolutions, four between-meeting board consents, two stockholder consents, tracking log, action-item register, minute-book table of contents, counsel-facing cover memo.
- **The consent-categorisation matrix is complete and defensible.** Every governance event is categorised, with a one-line rationale citing the specific authority.
- **The meeting-vote resolutions are in the "RESOLVED, that ..." format** and would be appended verbatim to a Q3 meeting-minutes document.
- **The board written consents follow DGCL §141(f) mechanics.** Correct preamble, correct resolution text, correct unanimous-signature-block, correct effective-date clause.
- **The stockholder written consents follow DGCL §228 mechanics.** Correct authority citation, correct class-vote threshold reference, correct notice-to-non-signing-stockholders clause.
- **The consent-tracking log is complete and includes the operational fields** (circulation, signature completion, minute-book filing location).
- **The action-item register carries forward at least one prior item, adds the meeting-generated items, and adds any consent-generated items.** No item is orphaned.
- **The minute-book table of contents lists every filed document from the quarter in chronological order.**
- **The counsel-cover memo respects the CFO-drafts / counsel-confirms boundary** and explicitly asks for redlines.
- **No fabricated legal citations.** Any specific DGCL or charter reference is correct or marked `needs-research`.

## Deliverables

- `00-consent-matrix.md`
- `01-meeting-resolutions.md`
- `02-board-written-consents/` (with four files)
- `03-stockholder-written-consents/` (with two files)
- `04-consent-tracking-log.md`
- `05-action-item-register.md`
- `06-minute-book-toc.md`
- `07-counsel-cover-memo.md`

## Extensions (optional)

- **The audit-committee consent stream.** For a company that has an audit committee (per chapter 6), draft the Q3 audit-committee consents: audit-plan approval for the annual audit, approval of a specific non-audit service (a tax-provision study by the same firm), and the audit-committee-only recommendation to the full board on the annual financial statements.
- **The stakeholder-consent notice.** DGCL §228(e) requires prompt notice to non-signing stockholders of any action taken by written consent. Draft the specific notice letter for the two stockholder consents, with the required content and timing. Include the CFO's tracking for delivery confirmation.
- **The related-party consent.** Assume the Series-A lead's fund is buying a small secondary tranche from an employee (the September consent). Draft the specific related-party-transaction consent that includes the independent-director approval mechanic (the vote of the disinterested directors, per DGCL §144 and the company's related-party policy). This is a more complex consent than the base scenario and trains the independent-director-approval mechanic.
- **The retrospective diligence view.** Assume the company is now 12 months into a Series-C diligence, and the Series-C lead's counsel has asked for a complete minute-book audit for Q3 (the quarter above). Draft the CFO's response: the summary of the quarter's governance, the specific documents provided, and the specific documents flagged as potentially requiring a ratifying consent (if any). Practice the retrospective-diligence mechanic and demonstrate why contemporaneous consent-authoring saves time later.
- **The state-of-incorporation variant.** Redraft the four between-meeting board consents assuming the company is incorporated in California rather than Delaware. Cite the specific California Corporations Code sections (Cal. Corp. Code §307(b) for the equivalent-of-§141(f) mechanic) and note the specific differences from the Delaware mechanics. Trains the state-specific-legal-frame reading skill.
- **The consent-training pack for the finance team.** Draft a one-page reference for the finance-team member who will maintain the consent-tracking log and the action-item register going forward. Includes the specific fields, the specific circulation cadence, and the specific escalation criteria (e.g., "any consent still unsigned 14 days after circulation escalates to the CFO").
