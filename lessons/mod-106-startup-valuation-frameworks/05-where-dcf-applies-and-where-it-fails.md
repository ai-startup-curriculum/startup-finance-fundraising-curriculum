# Where DCF Applies and Where It Fails

## Why this matters

Discounted cash flow is the standard equity-valuation framework taught in every finance MBA and used by every equity analyst on a mature public company. It has one core property: it produces a valuation from **the company's own forecast cash flows**, not from a comp-set derivation or an anchor-method bracket. That property is exactly what makes it powerful for a mature company with predictable cash flows and exactly what makes it dangerous for an early-stage startup whose cash-flow projections are inherently unreliable.

A CFO working across the startup life cycle needs to know precisely **when the DCF framework crosses from unreliable to useful**. Running a DCF on a Series-Seed company produces a number that gives the founder false confidence in an answer the model cannot support. Not running a DCF on a Series-C growth-stage company with a modelable breakeven and stable unit economics leaves a defensible triangulating anchor on the table.

This chapter installs the DCF-applicability boundary. It walks the DCF as a valuation framework, walks why the framework breaks at early stage, walks where the framework re-enters the toolkit as the company matures, and walks how to present DCF outputs as a triangulating third lens alongside the multiples framework (chapters 3-4) rather than as a stand-alone valuation.

Aswath Damodaran's academic-practitioner work on the valuation of young companies (see [`resources.md`](resources.md)) is the authoritative reference on this boundary and the primary source for the framing this chapter uses.

## The DCF framework in brief

Standard DCF for an equity valuation:

```
Enterprise value = Σ (free cash flow_t / (1 + WACC)^t)  for t = 1..N
                 + terminal value / (1 + WACC)^N
Equity value    = Enterprise value + cash - debt
Per-share value = Equity value / diluted shares outstanding
```

Where:

- **Free cash flow** = after-tax operating income + depreciation and amortisation - working-capital investment - capital expenditure. (Sometimes computed as EBITDA - taxes - working-capital investment - capital expenditure.)
- **WACC** = weighted average cost of capital, blending the after-tax cost of debt and the equity cost of capital by their respective weights in the capital structure.
- **Terminal value** = the present value of cash flows beyond the explicit forecast period. Typically computed either as (a) a Gordon growth model — `FCF_N × (1 + g) / (WACC - g)` — or as (b) an exit-multiple approach — `EBITDA_N × terminal EBITDA multiple`.
- **N** = the length of the explicit forecast period, typically 5-10 years.

The four moving parts are the free-cash-flow projection, the WACC, the terminal value, and the forecast period. Every one of them has a specific role, and every one of them behaves differently at different stages of company maturity.

For a mature public company (utility, consumer staples, mature enterprise software), all four are relatively stable and the DCF produces a defensible enterprise value. For an early-stage startup, one or more of them is fundamentally unreliable.

## Why DCF fails at early stage

Four failures compound at early stage. Any one of them is enough to make the DCF output non-informative; all four together make the exercise mostly noise.

### Failure 1 — the free-cash-flow projection is not defensible

A DCF requires a forecast of annual free cash flow for at least 5-10 years. Early-stage companies:

- Do not have a stable enough revenue trajectory to project year-1 revenue with confidence, let alone year-5.
- Do not have a stable enough operating expense base to project margin evolution over the forecast period.
- Have not converged on a repeatable customer-acquisition motion, so CAC and payback (mod-102) are moving targets.
- Are likely to pivot at least partially in the forecast period, invalidating the forecast entirely.

Small errors in year-1 revenue compound exponentially over the forecast period. A 5%/year error in year-1 growth compounded over 5 years is a 27% deviation in year-5 revenue; a 15%/year error compounds to a 200%+ deviation. Given that early-stage revenue forecasts routinely miss by 30-50% in year 1, the year-5 forecast has essentially unbounded uncertainty.

### Failure 2 — the WACC is unknowable at early stage

WACC has two components: cost of debt and cost of equity. For an early-stage startup:

- **Cost of debt** is often meaningless because the company has no debt (venture debt at seed is uncommon; when present, the effective cost — including warrants — is difficult to compute).
- **Cost of equity** is theoretically derived via CAPM (`risk-free rate + beta × equity risk premium`). Beta requires a comparable set of publicly-traded equities and a historical regression. Early-stage private companies have no beta of their own; using a comparable public-SaaS beta is a plug rather than a measurement.
- **The cost of equity for a private early-stage company is dominated by illiquidity and stage risk**, neither of which CAPM captures. Damodaran's work uses adjusted cost-of-equity estimates for private companies that add substantial risk premia; the resulting "cost of equity" is in the 20-40% range for early-stage companies, but the specific number is itself an estimate rather than a measurement.

WACC estimates for early-stage private companies span a wide range depending on the assumptions used, and the DCF output is highly sensitive to WACC. A DCF that produces $50M enterprise value at 25% WACC and $150M enterprise value at 15% WACC is not a defensible valuation of anything.

### Failure 3 — the terminal value dominates

For an early-stage company with negative free cash flow in the explicit forecast period and positive free cash flow only in the terminal phase, the DCF's enterprise value is dominated by the terminal value — often 80-95% of the total.

That means the DCF is really a valuation of the terminal-value assumption, not of the explicit-forecast cash flows. And the terminal-value assumption reduces to one of:

- **A terminal growth rate** (Gordon growth). For a startup that hasn't achieved product-market fit, an assumed 3%-in-perpetuity growth rate 5-10 years from now is a plug, not a measurement.
- **A terminal exit multiple.** Applied to year-N EBITDA. But year-N EBITDA is itself a highly-uncertain projection, and the "terminal exit multiple" is a comparable-driven number that already exists in the multiples framework (chapters 3-4). The DCF becomes an over-elaborated way to run the multiples calculation.

Either way, the DCF's answer is set by the terminal value, and the terminal value is set by inputs that are more directly modelled outside the DCF.

### Failure 4 — the framework gives false precision

The most damaging failure mode is presentational. A DCF produces a specific dollar valuation. That valuation carries the analytical weight of "we ran the equity-analyst framework, and this is what fell out." In a room full of people who defer to that framework, the false precision can move the conversation past questions like "is this trajectory even plausible?" that would otherwise stop the conversation.

Sophisticated investors are not fooled — most will ask which line items in the DCF are load-bearing and pull those apart. But the founder who has been convinced by their own DCF that the company is worth $200M is going into that conversation with a mismatched anchor.

## When DCF re-enters the toolkit

DCF becomes useful for a startup when the four failure modes are meaningfully mitigated. Roughly:

- **Failure 1 fix — defensible FCF projection.** The company has enough revenue history (typically 3-5 years) that year-1 revenue can be projected to within ±10-15%, and the operating-expense base is stable enough that year-3 margin evolution can be modelled with an unlevered-margin trajectory tied to specific cohort-based unit economics. This is usually mid-to-late Series-B onwards for a well-instrumented SaaS company, sometimes earlier for a highly capital-efficient one.
- **Failure 2 fix — WACC estimable.** The company has a large enough set of public-SaaS comparables with computable levered betas, an established relationship with venture-debt providers that produces a real cost-of-debt observation, and a broadly-agreed illiquidity-and-stage-risk premium against Damodaran's private-company adjustments. Still not perfect at Series-B; usable by Series-C / D.
- **Failure 3 fix — terminal value not dominant.** The explicit-forecast cash flows are positive in at least the last 3-5 years of the explicit period, so the terminal value is a meaningful minority of enterprise value (typically 40-60% for a growth-stage software company, not 90%+).
- **Failure 4 fix — presented as a triangulation, not a stand-alone.** The DCF output is one of three or four lenses being triangulated against the multiples framework, the recent transaction-comps, and the VC-method calculation — not a stand-alone number defended in isolation.

For most SaaS companies, that combination arrives at growth stage — post-Series-B, into Series-C / D / pre-IPO. Before that, the DCF is a diagnostic tool at best, not a valuation.

**A cleaner heuristic.** DCF is defensible when:

- The company has a modelable path to positive free cash flow within the explicit forecast period.
- The unit economics (mod-102) are stable enough that gross margin, CAC, and payback are predictable within a defensible range for the forecast period.
- The public-comp set is broad enough to derive a defensible WACC and a defensible terminal multiple.
- The DCF is being run as a check on the multiples framework, not as a substitute for it.

## The DCF at growth stage — worked outline

For a growth-stage software company (say, Series-C, $150M ARR, 45% NTM growth, modelable breakeven in year 3), the DCF walk:

**Step 1. Build the explicit-forecast cash flows.**

- Year 1: NTM revenue $150M × (1 + 45%) growth = $217M. Operating margin -15% (still investing in growth). Operating income = -$32M. Add-back D&A ~$5M, working-capital change ~-$15M (deferred revenue less receivables growth), capex ~$3M. **FCF ≈ -$45M.**
- Year 2: revenue $217M × (1 + 40%) = $304M. Margin -5%. FCF ≈ -$20M.
- Year 3: revenue $304M × (1 + 35%) = $410M. Margin +5%. FCF ≈ +$15M. **Breakeven year.**
- Year 4: revenue $410M × (1 + 30%) = $533M. Margin +12%. FCF ≈ +$60M.
- Year 5: revenue $533M × (1 + 25%) = $666M. Margin +18%. FCF ≈ +$115M.

**Step 2. WACC.**

- Cost of equity from a public-comp beta of, say, 1.4 against a 4.5% risk-free rate and a 5.5% equity risk premium: `4.5% + 1.4 × 5.5% = 12.2%`.
- Illiquidity/stage adjustment for a Series-C: add 300-500 bps. Use 400 bps. Adjusted cost of equity: **16.2%**.
- Assume 90% equity / 10% debt at effective 8% (venture debt, after tax): `0.9 × 16.2% + 0.1 × 8% × (1 - 21%) = 14.6% + 0.63% ≈ 15.2%`.
- **WACC = 15.2%.**

**Step 3. Terminal value.**

- Use exit-multiple approach: assume year-5 EBITDA multiple of 20× (a defensible growth-SaaS multiple for a Rule-of-40 passing company at year 5).
- Year-5 EBITDA ≈ FCF + capex + working-capital investment + taxes ≈ $115M + $10M + $30M + $20M ≈ $175M. (Rough; the point is the shape.)
- Terminal value = 20 × $175M = **$3,500M**.
- Present value of terminal value = $3,500M / (1.152)^5 ≈ $1,725M.

**Step 4. Present value of explicit-forecast FCFs.**

- PV of year-1 FCF: -$45M / 1.152 = -$39M
- PV of year-2 FCF: -$20M / 1.152^2 = -$15M
- PV of year-3 FCF: $15M / 1.152^3 = $10M
- PV of year-4 FCF: $60M / 1.152^4 = $34M
- PV of year-5 FCF: $115M / 1.152^5 = $57M
- Sum: **$47M** (rough; a small positive).

**Step 5. Enterprise value.**

- EV = PV(FCFs) + PV(terminal value) = $47M + $1,725M = **$1,772M**.

**Step 6. Equity value.**

- Add cash ($200M assumed), subtract debt ($40M assumed).
- Equity value = $1,772M + $200M - $40M = **$1,932M**.

**Cross-check to the multiples anchor.** Chapter 3's multiples framework on the same company: NTM revenue $217M × (say) 10× public-comp multiple × (1 - 20%) private-market discount = **$1,736M**. The DCF anchor ($1.77B enterprise value) triangulates within 3% of the multiples anchor ($1.74B). That agreement is the load-bearing evidence that both lenses are producing consistent answers.

Where the DCF adds value at this stage:

- **It surfaces the assumptions.** The multiples framework hides the growth assumption in the choice of multiple; the DCF exposes it as a specific-year revenue projection.
- **It supports sensitivity analysis.** Sensitising the DCF across (growth rate × terminal multiple × WACC) produces a defensible range that the multiples framework alone does not.
- **It stress-tests the exit hypothesis** in the VC method (chapter 2). The DCF's terminal value is a bottom-up construction of the exit value that the VC method uses as an input.

**Where the DCF still has to be presented carefully.** Even at growth stage, ~80% of the DCF enterprise value in this example is terminal value. Sensitising the terminal multiple from 15× to 25× moves enterprise value from $1.3B to $2.2B — a 70% range. The DCF is a lens, not a precision tool, and the memo should present the range, not the point.

## The DCF sensitivity table

A defensible growth-stage DCF is presented as a **sensitivity table**, not as a single point. The standard sensitivity is two-variable across:

- Terminal exit multiple (rows: 12×, 16×, 20×, 24×, 28×).
- WACC (columns: 12%, 14%, 16%, 18%, 20%).

The cell values are enterprise value. The table shows the DCF's answer across the plausible range of both variables and lets the reader see how sensitive the number is to each. A well-instrumented sensitivity table often shows a 3-4× range across the corners of the table, which is exactly the point — the DCF has that much uncertainty, and hiding it in a single point is analytical malpractice.

## The DCF as a triangulating anchor, not a stand-alone

Even where DCF applies (growth-stage, modelable breakeven, stable unit economics), it is best presented as a **third lens** alongside:

- **Multiples framework** (chapters 3-4) — public-comp multiple applied to NTM revenue with growth-adjustment.
- **VC method** (chapter 2) — target-return back-solve for lead-investor negotiation.
- **DCF** — bottom-up cash-flow triangulation.

If all three lenses converge on a similar valuation, the number is defensible. If they diverge materially, the divergence itself is the diagnostic — one of the lenses is picking up something the others are missing, and the memo should name what it is.

At Series-C and later, the multiples framework and the DCF should generally agree within 20-25%. Larger divergences typically indicate:

- The comp set is not right (chapter 3).
- The growth-adjustment is off (chapter 4).
- The DCF's terminal multiple or WACC assumption is off.
- The company is at an inflection point that neither framework captures cleanly.

## Common founder traps

- **Running a DCF at seed.** Produces a number, gives false confidence, distracts from the anchor-method bracket and the VC-method calculation that are the actually-defensible frameworks at that stage.
- **Presenting a DCF as a single point.** The DCF's uncertainty range is wide even at growth stage. A single point overstates the precision.
- **Terminal value >90% of enterprise value with no comment.** The memo should quantify the terminal-value share and defend the terminal assumption.
- **Cost of equity plugged in without disclosure.** WACC is one of the two levers with the largest sensitivity. Whichever number is used has to be defended.
- **Using a public-comp beta without adjustment.** A private company at growth stage is not the same as a public-comp company; the beta needs an illiquidity / stage-risk adjustment.
- **Substituting DCF for the multiples framework.** DCF triangulates the multiples framework; it does not replace it. A DCF that produces a very different number than the multiples framework indicates a problem, not a superior analytical result.
- **Skipping the sensitivity table.** A DCF with no sensitivity table is a DCF that has not been diligenced.

## What good looks like

A finance leader considering DCF for a valuation memo:

- **Applies the boundary test first.** Is the company past the point where the four failure modes are meaningfully mitigated? If not, run the anchor methods (chapter 1) and the VC method (chapter 2), and skip the DCF.
- **If yes, presents the DCF as a triangulating third lens** alongside the multiples framework (chapters 3-4) and the VC method (chapter 2).
- **Builds the explicit-forecast FCFs** off the driver-based three-statement model (mod-103) and the cohort-based unit economics (mod-102), tied to specific-year revenue, gross margin, opex, working capital, and capex projections.
- **Defends the WACC estimate** with an explicit source for the public-comp beta and an explicit illiquidity-and-stage-risk adjustment.
- **Presents a two-variable sensitivity table** across terminal multiple and WACC, and quantifies the share of enterprise value coming from the terminal.
- **Cross-checks against the multiples anchor** and names any material divergence, with a specific hypothesis for what is causing it.
- **Notes explicitly where DCF adds value** and where it is dominated by the multiples framework.

## Summary

- DCF is the standard equity-valuation framework for mature companies but fails at early stage for four reasons: unreliable FCF projections, unknowable WACC, terminal-value dominance, and false analytical precision.
- The framework becomes usable when the company has a defensible year-1-to-year-5 FCF trajectory, an estimable WACC anchored to a real public-comp set, an explicit-forecast period that is a meaningful share of enterprise value, and the discipline to present the output as a triangulating lens rather than a stand-alone number.
- For most SaaS companies, DCF is applicable from mid-to-late Series-B onwards. Before that, run the anchor methods (chapter 1) and the VC method (chapter 2).
- At growth stage, DCF is best presented as a triangulating third lens alongside the multiples framework and the VC method, with an explicit sensitivity table across terminal multiple and WACC, and a specific comparison to the multiples anchor.
- Damodaran's work on young-company valuation is the authoritative reference on the boundary; his practitioner writing on the adjustments to standard DCF for private and early-stage companies is required reading before running one in a real memo.
- Common failure modes: running DCF at the wrong stage, presenting a single point instead of a range, terminal value dominating without disclosure, plugging in WACC without source, using DCF as a substitute for rather than triangulation of the multiples framework.

Chapter 6 turns to the quarterly market-conditions reports (Fenwick, WSGR, PitchBook-NVCA) that establish the current-quarter context for any valuation the CFO derives from the anchor methods, VC method, multiples framework, and DCF.
