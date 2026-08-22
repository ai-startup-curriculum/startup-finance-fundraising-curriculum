# 409A Methodology, FMV, and Refresh Cadence

## Why this matters

Every option granted by a private company has a **strike price**, and that strike price cannot be lower than the **fair market value (FMV)** of the underlying stock on the grant date. Set the strike below FMV and the option is issued "in the money," which under Internal Revenue Code Section 409A treats the entire spread as deferred compensation subject to immediate income inclusion, a 20% additional tax on the recipient, plus interest — a punitive outcome that lands on the *option-holder*, not the company that mispriced the grant.

The FMV of a private company's common stock is not observable from a market price the way public-company FMV is. It has to be **appraised**. The appraisal — usually done by an independent third party — is what the industry calls a "409A valuation" or a "409A report," and its output is a per-share FMV number the board uses to set option strike prices for the following period.

The 409A regime creates two things a CFO must manage:

1. **The valuation itself** — engaging an appraiser, providing them with the inputs, understanding the methodology they'll use, and reading the output critically.
2. **The refresh cadence** — knowing when the existing 409A is still safe to grant against and when a fresh appraisal is required.

Get the cadence wrong and the safe-harbor protection of a prior 409A doesn't apply to a grant that was issued after a material event. Get the methodology wrong (or accept a bad appraisal without questioning it) and the FMV is defensible for tax purposes but not for common-vs.-preferred pricing, which affects both employee-grant economics and later-round negotiations.

This chapter installs the methodology, the cadence rules, and the safe-harbor framework. The equity-comp instruments that reference the 409A output (ISOs, NSOs, RSUs) are the subject of chapter 7.

## Where 409A comes from

Internal Revenue Code Section 409A was enacted in 2004 (as part of the American Jobs Creation Act) in response to abuses in the deferred-compensation space — most visibly the Enron executives who had backdated compensation arrangements to shield income from tax. Treasury issued final regulations in 2007 (Treas. Reg. §§1.409A-1 through 1.409A-6).

Section 409A defines a **stock right** (options and stock appreciation rights) as a form of nonqualified deferred compensation. The regulations then carve out an **exemption** for stock rights that meet specific conditions — the most important being that the exercise price is not less than the FMV of the underlying stock on the grant date. If the exemption applies, the stock right is outside 409A. If not, the entire spread between FMV and strike, at grant, is subject to 409A's punitive consequences on the option-holder.

The consequences (Treas. Reg. §1.409A-3, §1.409A-6):

- **Immediate income inclusion** of the vested spread at grant (and each vesting date for unvested portions).
- **Additional 20% federal tax** on that income (plus state 409A equivalents in California, for example).
- **Underpayment interest** at the underpayment rate plus 1%.

These consequences fall on the option-holder (the employee), not the company. But the reputational and litigation risk to the company for having issued options that trigger 409A on employees is severe, and every venture-backed startup treats 409A compliance as non-negotiable.

## The safe-harbor framework

The regulations (Treas. Reg. §1.409A-1(b)(5)(iv)(B)) create a **presumption of reasonableness** for FMV determinations that meet one of three safe harbors. If the company grants at a price that meets a safe harbor's presumption, the IRS bears the burden of proving the FMV was unreasonable (a high bar); if the company grants outside the safe harbors, the company bears the burden of proving the FMV was reasonable (also a high bar, and one that is worse to lose).

**Safe harbor 1: Independent appraisal.** An appraisal by a qualified independent appraiser using a valuation methodology consistent with the regulations. The presumption applies if the appraisal is no more than 12 months old and no "material event" has occurred since. This is the safe harbor almost every venture-backed startup uses.

**Safe harbor 2: Illiquid startup safe harbor.** For companies less than 10 years old, with no public market, and a valuation performed by a person with "significant knowledge and experience or training in performing similar valuations." This is a lower bar than a full independent appraisal, but it requires documented methodology and the same 12-month freshness rule. In practice, this safe harbor is used for very early stage companies where an outside appraiser isn't yet engaged.

**Safe harbor 3: Formula method.** A valuation based on a formula in a written binding agreement (e.g., book value plus a multiple). Very rarely used in venture-backed startups because formula-based FMVs don't hold up as the company grows.

The industry-standard practice: safe harbor 1, from an independent appraiser, refreshed every 12 months or on a material event, whichever comes first. This is the "12-month rule" every early-stage CFO learns.

## Who does the appraisal

Appraisers who serve the venture-backed startup market:

- **Full-service 409A appraisal firms** — Aranca, Preferred Return, Scalar (formerly ValuatePro), VRC, Kroll Duff & Phelps (now Kroll), Marcum, Andersen Tax's valuation practice. Cost typically $2K-$5K per report at Series-Seed / Series-A, rising to $5K-$15K at Series-B and above depending on complexity.
- **Cap-table-platform embedded appraisals** — Carta 409A, Pulley 409A, LTSE Equity 409A. Bundled as an add-on to the cap-table service. Historically the fastest and least expensive option; historically also criticised for being production-line rather than deeply analytical, though methodology has professionalised significantly.
- **Boutique / independent appraisers** — smaller firms serving startups at cost roughly comparable to the cap-table platforms but with more analyst attention per report.

The CFO's choice among these depends on complexity (a Series-D company with international operations, multiple preferred series, warrants outstanding, and secondary tender offers is a different appraisal problem than a Seed company with one preferred series), cost sensitivity, and any diligence-firm-requested independence (some Series-B+ diligence firms want to see a full-service firm's report rather than a platform-embedded one).

## The valuation methodologies

The appraiser produces a per-share common FMV using one or a combination of the following methods, drawn from the AICPA Accounting and Valuation Guide *Valuation of Privately-Held-Company Equity Securities Issued as Compensation* (the "AICPA Practice Aid," originally published 2004, updated several times):

**1. Backsolve from the recent priced round.** If the company recently raised a priced round (typically within the last 6 months), the round's preferred-share price implies a total-equity value that the appraiser walks *backward* to common. The backsolve uses an option-pricing model (usually Black-Scholes) to solve for the total-equity value that, when distributed through the preference waterfall and volatility, produces the observed preferred-share price. Then the same OPM is used to allocate that total value between preferred and common at grant date. Preferred trades at a premium to common because of its liquidation preference and (if any) participation right; common's implied FMV is typically 20-40% of the preferred price for a Series-A company, 50-70% for a Series-B, higher as the company matures.

This is the dominant methodology for post-priced-round appraisals. When the priced round is fresh, this is the most defensible per-share FMV number available.

**2. Comparable public companies analysis (market approach).** The appraiser identifies public companies in the same industry with similar business models, computes trading multiples (EV / Revenue, EV / ARR, EV / EBITDA), applies those multiples to the subject company's financials to derive an enterprise value, then walks that to a per-share common FMV through the waterfall + OPM.

This method is more common when there is no recent priced round to backsolve from. It requires public comparables — challenging for very early stage or unusual businesses.

**3. Discounted cash flow (income approach).** The appraiser builds a DCF against the company's financial model, terminal-value-anchored to some multiple, discounts back at a rate reflecting the company's cost of capital.

DCF for a pre-profitability startup is heroic; the appraiser typically uses it as a sanity check rather than a primary method, unless the company has real free cash flow (unusual before Series-C for most SaaS businesses).

**4. Asset-based approach.** Book value or liquidation value. Almost never applicable to a going-concern software business; used for asset-heavy businesses or distressed situations.

The appraiser typically produces the FMV using a **weighted combination of methods** (e.g., 60% backsolve, 30% comparable-companies, 10% DCF) with the weighting justified in the report. The report also includes a **discount for lack of marketability (DLOM)** — a further downward adjustment on common because private-company stock cannot be freely sold. DLOMs are typically 15-30% depending on stage and expected time-to-liquidity.

## The refresh cadence — the 12-month rule and material events

The safe harbor's presumption of reasonableness lasts **12 months from the appraisal date** *or* **until a material event occurs** — whichever comes first.

**The 12-month clock.** A 409A report dated 15 March 2026 provides safe-harbor protection for grants issued through 14 March 2027. Grants issued on or after 15 March 2027 need a fresh 409A. This is the annual refresh cadence.

**Material events.** Regulations enumerate examples but the concept is broader: any event that would meaningfully change the FMV of the common stock. In practice:

- **A new priced round of preferred stock.** Almost always a material event. Even a small extension of the last series can qualify. The rule of thumb: any priced round triggers a fresh 409A.
- **A tender offer or secondary transaction at a price different from the last 409A.** Yes, always. If secondary buyers pay a per-share price meaningfully different from the last 409A, the transaction data is new information about market value.
- **A material acquisition or divestiture.** Yes.
- **A material change in financial projections or actual performance.** Judgment call. A 30% revenue miss vs. plan is probably material; a 5% miss usually isn't. A large customer contract signing (e.g., 3x the largest existing customer) might qualify.
- **A change in the capital structure** (e.g., a recapitalisation, a large debt facility).
- **A pending exit event** — a term sheet from a potential acquirer, a signed LOI, a filed S-1.

**When in doubt, refresh.** The cost of an unnecessary fresh 409A is $2K-$15K; the cost of granting options at a stale FMV that later proves inadequate is 409A penalties on the option-holder plus loss of the ISO qualification (chapter 7) plus a diligence problem at the next round. The asymmetric cost pushes CFOs toward refreshing more often than strictly required.

## When the CFO orders a fresh 409A

**Immediately after a priced round closes.** The round's share price is the strongest input for a backsolve. The CFO orders the 409A within days of the closing memo being finalised. Grants issued between the closing and the receipt of the new report should be avoided; if urgent grants are needed (e.g., a pending offer letter to a critical hire), the option is to wait for the report or to issue at a temporarily conservative strike that's guaranteed to be at or above the eventual FMV.

**Approximately 12 months after the last report** if no priced round or material event has occurred. Many CFOs schedule the appraisal for month 11 to have the report in hand before the 12-month clock expires and grants become exposed.

**On any of the material events listed above.**

**Before a tender offer / secondary transaction.** The pricing of a secondary transaction is *itself* new market information, and if the secondary price differs meaningfully from the current 409A, the current 409A is stale as of the closing of the secondary. Some CFOs order a fresh 409A after the secondary to reset the baseline; some hold the position that the secondary price is a *transaction-specific* premium or discount that doesn't affect the ongoing 409A. The 2022 AICPA Practice Aid update tightened the guidance here; the current default is to treat any priced secondary transaction as at least presumptively material.

<!-- needs-research: verify the current AICPA Practice Aid's specific language on tender-offer / secondary treatment; the guidance has been updated several times since 2014. -->

## Reading a 409A report critically

The CFO who receives a 409A report should not just accept the number. The reasonable checks:

- **Methodology consistency with prior reports.** If the last report was 60% backsolve / 40% comps and this one is 20% backsolve / 80% comps without a material change in the company, ask why. Methodology drift is a warning sign.
- **The DLOM.** A 15% DLOM on a Series-C company with an active secondary market is aggressive (low); a 40% DLOM on a Series-Seed company with no near-term liquidity is defensible (high). Ask the appraiser to justify the DLOM range and the specific number chosen.
- **The backsolve inputs.** If the appraiser is backsolving from a stale round (e.g., the last priced round was 15 months ago and the company has since 3x'd), the backsolve is not the appropriate primary method. Push the appraiser to weight comps / DCF more heavily.
- **The relationship between common FMV and preferred price.** The ratio of common FMV to the most recent preferred price is a defensibility check. At Series-A the ratio is typically 20-40%. At Series-B 40-60%. At Series-C 60-80%. Ratios substantially outside these ranges without explanation are a warning.
- **The volatility assumption in the OPM.** The Black-Scholes-Merton allocation uses a volatility input. Higher volatility → more value allocated to common (because common has higher optionality against the preference stack). Appraisers can play games here to move the answer; ask for the sensitivity of the answer to volatility.

The CFO who reads the report critically and asks these questions gets a more defensible number and a better relationship with the appraiser for future reports.

## When strike prices are set

The 409A is used to set option strike prices via a **board consent** that (i) grants the specified options and (ii) sets the strike price at the current FMV per the 409A. The board consent references the 409A report by name and date. This paper trail is what the diligence firm will follow.

The failure mode: board consents that set strike prices without referencing the 409A, or that reference an out-of-date 409A because no one caught the 12-month rollover. Both are common enough at diligence to be a regular fix-in-diligence item.

## The interaction with equity-comp instruments

The 409A is a prerequisite for:

- **ISOs and NSOs.** Both require a strike price at or above FMV to avoid 409A. ISOs have additional requirements (chapter 7).
- **Stock appreciation rights (SARs).** Same — SARs are stock rights within the 409A framework.
- **RSUs.** RSUs are treated differently — RSUs don't have a "strike price" but the settlement structure has to comply with 409A's timing rules (settle upon a permissible payment event, typically a fixed date, a change of control, or death / disability; no elective deferral of settlement). Private-company RSUs (chapter 7) typically require a liquidity event trigger to avoid FICA / income-inclusion issues.

The 409A is not a prerequisite for restricted stock (RS) — a direct purchase of common at a nominal price, usually by founders — because restricted stock is not a "stock right"; it is stock. But the purchase price for restricted stock still needs to be FMV to avoid compensation-income issues.

## Refresh in a rising vs. falling market

**Rising market (company doing well).** A fresh 409A is more expensive for future grantees (higher strike), but it protects the existing grants (issued at the lower prior FMV) and it's a positive-signal event for the company. Some CFOs delay ordering the fresh 409A near the 12-month deadline to squeeze in a batch of grants at the lower FMV — this is technically compliant if the material-event condition hasn't been triggered, but it's aggressive and diligence firms are increasingly attentive to it.

**Falling market (company underperforming, or the broader market has repriced).** A fresh 409A is *cheaper* for future grantees (lower strike) but requires the CFO to explain to employees why the new FMV is lower. Often accompanied by an **option repricing** — a formal action to reduce the strike price on already-outstanding options to the new FMV. Repricing is legally straightforward (board consent + optionee agreement) but has accounting consequences under ASC 718 (a modification, typically a new fair-value measurement and an incremental compensation expense) and cultural consequences (repricing is a signal that the company thinks the old strikes are underwater; some employees like it, some see it as a bailout of poor prior grants).

Repricings became common in the 2022-2023 SaaS reset and the 2001-2003 dot-com reset. They are one of the more visible interactions between the 409A refresh cycle and the operating reality of the company.

## Summary

- IRC Section 409A requires options to be granted at or above the FMV of the underlying stock; grants below FMV trigger immediate income inclusion, a 20% additional tax, and interest on the option-holder.
- FMV of private-company common is determined by appraisal. Safe harbor 1 (independent appraisal by a qualified firm) is the industry-standard mechanism; safe harbor 2 (illiquid-startup) applies to earliest-stage companies; safe harbor 3 (formula) is rare.
- The 409A appraisal typically combines backsolve from the recent priced round, comparable-companies analysis, and (occasionally) DCF, with a discount for lack of marketability applied to common.
- The refresh cadence: every 12 months, or on any material event — priced round, secondary transaction, material projection change, pending exit, recapitalisation, large financing. When in doubt, refresh.
- Reading the report critically — methodology consistency, DLOM, backsolve staleness, common-to-preferred ratio, volatility input — produces a better number and a better appraiser relationship. Accepting the number without scrutiny is common and avoidable.
- Board consents that grant options must reference the current 409A report by name and date; missing this reference is a common diligence fix-item.
- Restricted stock (founder grants) is not a stock right and doesn't require a 409A per se, but the purchase price still needs to be FMV. RSUs are outside the "strike price" question but subject to 409A settlement-timing rules.
- Repricings and secondary transactions each interact with the 409A cycle — repricings reset outstanding strikes downward with ASC 718 consequences; secondaries are themselves a data point for the next 409A.

Chapter 6 turns to Rule 701 — the securities-law regime that caps the aggregate value of unregistered option grants a private company can make in a rolling 12-month period without triggering registration or a Form S-8.
