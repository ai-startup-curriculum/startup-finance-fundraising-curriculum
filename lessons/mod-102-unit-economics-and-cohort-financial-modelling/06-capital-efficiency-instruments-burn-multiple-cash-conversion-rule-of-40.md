# Capital-Efficiency Instruments — Burn Multiple, Cash Conversion Score, Rule of 40

## Why this matters

Unit economics (CAC, LTV, payback) tell you whether a single customer is profitable to acquire and serve. NRR / GRR (chapter 5) tell you whether the base is sticky and expanding. Neither of those tells you *how efficiently a startup as a whole is converting invested capital into revenue*. That is what the modern capital-efficiency instruments — **burn multiple**, **cash conversion score**, and **Rule of 40** — are built to measure. Together they form the diagnostic scorecard that a Series-B or later CFO uses to answer the specific question a board member will ask: *"we've raised $80M and we're at $18M ARR — is that good or bad?"*

The three instruments are different because they answer different questions. Burn multiple asks *"per dollar of net-new ARR added, how many dollars of cash did we burn?"* — a period metric that grades marginal efficiency. Cash conversion score asks *"across the company's life, how many dollars of ARR did we produce per dollar of capital raised?"* — a lifetime metric that grades cumulative efficiency. Rule of 40 asks *"is the growth rate plus the FCF margin a healthy number?"* — a balance metric that says whether the growth-vs-profitability trade-off is at an acceptable point. All three are pattern-matched by growth investors against known-good bands published by OpenView, Bessemer, Emergence, SaaStr, and a16z. A CFO who cannot compute all three, benchmark them against the current-year data, and diagnose which lever is failing does not have a credible board seat at Series-B and beyond.

This chapter installs each metric, its formula and the specific edge cases in the formula, the current benchmark bands, and the diagnostic procedure a CFO runs when the number falls outside the band.

## Burn multiple — the David Sacks metric

Burn multiple was formalised by [David Sacks in a 2020 Craft Ventures essay](https://sacks.substack.com/) and rapidly became the standard efficiency metric that Series-A and Series-B investors ask about. It answers: *for every dollar of net-new ARR we added this period, how many dollars of cash did we burn?*

$$
\text{Burn Multiple} = \frac{\text{Net Burn}}{\text{Net-New ARR}}
$$

- **Net burn** = cash outflow from operations plus cash outflow from investing (excluding cash from financing) over the period. Typically measured over the trailing 12 months or by-quarter.
- **Net-new ARR** = ending ARR minus starting ARR. Includes new logos, expansion, downgrade, and churn — the whole net movement.

A burn multiple of 1× means the company burned $1 for every $1 of net-new ARR added. Interpret in the band:

| Burn multiple | Sacks' interpretive label | Interpretation |
|---|---|---|
| Below 1× | Amazing | Extraordinary capital efficiency; typical of best-in-class PLG or capital-efficient AI-native companies |
| 1× to 1.5× | Great | Healthy for most SaaS at Series-A/B |
| 1.5× to 2× | Good | Acceptable at growth stages with strong unit economics |
| 2× to 3× | Suspect | Investors will probe for the reason |
| Above 3× | Bad | Serious capital-efficiency problem; typically triggers a "fix the burn" board conversation |

<!-- needs-research: verify the specific interpretive bands against the current-year Sacks Craft essay and against the SaaStr / OpenView benchmark data; bands have shifted since the original 2020 post -->

The elegance of burn multiple is that it collapses the growth-vs-profitability trade-off into a single number. A company burning $10M/year and adding $10M of net-new ARR has a 1× burn multiple — capital-efficient regardless of whether it's operating at $2M ARR or $50M ARR. A company burning $10M/year and adding $2M of net-new ARR has a 5× burn multiple — inefficient regardless of the absolute scale.

Two mechanical subtleties:

**Signed vs. absolute net-new ARR.** If a company loses more ARR (churn + downgrade) than it adds (new + expansion), net-new ARR is negative. Burn multiple with a negative denominator is undefined (or produces a misleading negative number). The convention: when net-new ARR is negative, report the *dollar burn* and the *dollar ARR contraction* directly and do not compute burn multiple — the company is in a distinct diagnostic state (see chapter on runway management in [`mod-109`](../mod-109-runway-management-and-bridge-financing/)).

**Non-cash items and unusual items.** Net burn should exclude one-time cash movements (a security deposit refund, a legal settlement, a large tax refund) that would distort the ratio. The convention is to compute burn multiple on a "normalised" basis and disclose the normalisation.

## Cash conversion score — the Bessemer lifetime metric

Cash conversion score (CCS) — sometimes called capital efficiency ratio — was formalised by [Bessemer Venture Partners in their SaaS-metrics work](https://www.bvp.com/atlas/state-of-the-cloud) as a lifetime metric complementing the burn multiple's period metric. It answers: *across our company's life, how much ARR have we produced per dollar of net capital raised?*

$$
\text{Cash Conversion Score} = \frac{\text{Current ARR}}{\text{Total capital raised} - \text{Current cash}}
$$

The denominator is "net capital deployed" — the total equity and debt raised, minus the cash still on the balance sheet. This isolates the capital actually consumed to reach the current ARR. Interpret in the band:

| Cash conversion score | Interpretation |
|---|---|
| Above 1.0 | Best-in-class; every dollar of capital deployed produced a dollar of ARR |
| 0.5-1.0 | Healthy; typical of well-run SaaS companies at Series-B and beyond |
| 0.3-0.5 | Standard; the mid-band for growth-stage SaaS |
| Below 0.3 | Capital-intensive; requires a story about future capital efficiency |

<!-- needs-research: cite the Bessemer *State of the Cloud* current-year data on cash conversion score bands by ARR stage -->

CCS is a useful complement to burn multiple because it captures cumulative history that burn multiple ignores. A company with a 1× burn multiple this quarter but a 0.2 CCS lifetime is a company that has recently gotten efficient — investors will note the recent improvement but also note that $80M was already spent to reach $16M ARR. Both metrics belong on the same slide.

A subtlety: the denominator should net out cash that came from *operations* over the company's life (rare — most startups burn every dollar of equity they raise) but should not net out cash that came from *primary equity or debt financing*. In practice for most venture-backed startups this is: capital raised = total equity issuance across all rounds + total debt drawn - debt repaid. Verify against the cap table and the historical cash-flow statements.

## Rule of 40 — the balance metric

Rule of 40 is the classic SaaS efficiency benchmark, popularised by Brad Feld and adopted broadly across public SaaS analysis. It states that a healthy SaaS company's growth rate plus FCF margin should sum to at least 40%:

$$
\text{Rule of 40 Score} = \text{Growth Rate (\%)} + \text{FCF Margin (\%)}
$$

- **Growth rate** = YoY ARR growth rate (or YoY revenue growth rate for public-company comparisons where ARR is not disclosed).
- **FCF margin** = free cash flow divided by revenue, on a trailing-twelve-months basis.

Interpretation:

| Rule of 40 score | Interpretation |
|---|---|
| Above 60% | Elite; typical of top-decile public SaaS |
| 40-60% | Best-in-class; the target band for growth-stage SaaS |
| 20-40% | Acceptable, especially at earlier stages or in expansion phases |
| Below 20% | Poor; the trade-off between growth and profitability is not being managed well |

The intuition: the acceptable balance between growth and profitability shifts along a frontier. A company growing 80% year-on-year at -40% FCF margin scores 40% (acceptable — investing hard into an obvious opportunity). A company growing 25% year-on-year at 15% FCF margin scores 40% (also acceptable — modest growth at healthy profitability). A company growing 50% at -30% FCF margin scores 20% (below the line — burning cash without capturing enough growth to justify it).

Rule of 40 is *most* relevant at Series-C and beyond, where FCF becomes a meaningful measurable quantity and investors expect a credible path to profitability. At Series-A and early Series-B, growth rates are usually well above 40% and FCF margins are deeply negative; the Rule of 40 arithmetic still holds but is dominated by the growth-rate term. The metric becomes diagnostic once FCF margins start to matter — typically once ARR exceeds $30-50M.

## The combined scorecard — a CFO's diagnostic worksheet

The three metrics used together form a diagnostic scorecard. A worked example for a hypothetical Series-B SaaS company:

| Metric | Value | Benchmark band | Diagnosis |
|---|---|---|---|
| ARR | $22M | — | Series-B stage |
| YoY growth rate | 80% | 60-100% (median for stage) | Healthy |
| Burn multiple (TTM) | 2.4× | Target ≤ 2× | Slightly weak — inefficient marginal spend |
| Cash conversion score | 0.35 | Target ≥ 0.5 | Weak — cumulative capital efficiency below best-in-class |
| Rule of 40 score | 15% (80% - 65% FCF margin) | Target ≥ 40% | Poor — trade-off is skewed too heavily to burn |
| NRR (TTM) | 105% | Target ≥ 115% | Weak — expansion motion needs work |
| GRR (TTM) | 88% | Target ≥ 90% | Acceptable but not best-in-class |
| Payback (cohort-based, median) | 22 months | Target ≤ 18 months | Weak — CAC recovery too slow |

The scorecard tells a specific story: a company growing well but doing so with weak marginal efficiency, weak retention on the base, and slow payback. The diagnosis is not "the company is failing" — 80% growth at $22M ARR is a real business — but "the growth engine is expensive and the customer engine isn't compounding." The corrective actions map to specific chapters of this module: chapter 1 (CAC discipline per channel), chapter 3 (gross-margin decomposition — is the margin holding?), chapter 5 (NRR / GRR expansion motion).

The scorecard also names the *sequence* of the fix. Fixing NRR is typically the highest-leverage move because it compounds; fixing burn multiple is second because it produces immediate cash conservation; fixing payback is third because payback improvements take a full cycle to appear in the numbers.

## Benchmarking against published data — where to get the numbers

Every benchmark band in this chapter is based on published data from a small number of authoritative providers. When you cite benchmarks in a board pack or a fundraise deck, cite the specific report, its year, and the specific segment or ARR band it references.

**OpenView SaaS Benchmarks** — [openviewpartners.com](https://openviewpartners.com/) publishes an annual report drawn from hundreds of SaaS companies, segmented by ARR band, motion (PLG vs. sales-led), and industry. The most useful single reference for burn multiple, CAC payback, and gross-margin benchmarks by ARR stage.

**Bessemer Venture Partners State of the Cloud** — [bvp.com/atlas](https://www.bvp.com/atlas/state-of-the-cloud) publishes annual analysis with a strong late-stage and public-SaaS focus. Cash conversion score and the "Best Cloud Companies" NRR data live here.

**Bessemer Cloud Index (EMCLOUD)** — [cloudindex.bvp.com](https://cloudindex.bvp.com/) tracks a basket of public SaaS companies with real-time multiple, growth, and Rule of 40 data.

**Meritech Capital SaaS Comps** — [meritechcapital.com/saas-comps-table](https://www.meritechcapital.com/saas-comps-table) provides current-quarter public-SaaS metrics, including revenue multiples correlated with Rule of 40 and NRR. The most useful reference for revenue-multiple-based benchmarking against comparable public companies.

**SaaStr Annual State of SaaS** — [saastr.com](https://www.saastr.com/) publishes practitioner-oriented benchmarks focused on the operator community; useful for CAC, sales-efficiency, and stage-transition data.

**a16z SaaS metrics essays** — [a16z.com/tag/saas/](https://a16z.com/) publishes stage-specific benchmark essays; useful for the operator's-view framing of the same numbers.

**KeyBanc Capital Markets Annual SaaS Survey** — [key.com/kbcm](https://www.key.com/businesses-institutions/industry-expertise/technology.html) publishes an annual survey of private SaaS companies with detailed unit-economics and expense-ratio benchmarks; a strong reference for the private-company side that OpenView complements.

<!-- needs-research: verify the current URLs and current publication cadence for each of the above providers; update citations to the most recent report year -->

The convention: pick two providers whose methodology you understand, cite specific years, and present the benchmark bands in a footnote or an appendix slide of the board pack. Cross-source benchmarking is more defensible than single-source; if OpenView and Bessemer disagree on a band, the disagreement itself is worth surfacing.

## Diagnosing which lever is failing — the four decompositions

When a company's capital-efficiency scorecard is below benchmark, the CFO's diagnostic job is to identify which of four levers is the actual cause. The four levers, in the order they typically dominate:

**Lever 1 — Top-line growth rate.** If growth is below-benchmark, no burn discipline will produce a healthy Rule of 40. The question becomes: is the growth-rate deceleration a demand problem (TAM saturation, competitive pressure) or a supply problem (S&M capacity, product gaps)? The unit-economics diagnostic: is CAC (chapter 1) inflating over time? Are cohorts shrinking (chapter 4)? Is NRR (chapter 5) below-benchmark and constraining the compounding effect?

**Lever 2 — Gross margin.** If gross margin is below the 70% SaaS floor or the 20% marketplace take-rate floor (chapter 3), every dollar of revenue produces less contribution and every capital-efficiency metric worsens. The question: is the gross margin structurally low (business model issue) or contingently low (cost-to-serve inflation, mix shift)? The corrective: chapter 3's decomposition names the failing bucket (hosting inefficiency, third-party COGS growth, over-staffed support) and directs the fix.

**Lever 3 — S&M efficiency.** If CAC is inflating or payback is extending (chapter 1), S&M spend is producing weaker economics per dollar. The question: is a specific channel becoming inefficient (paid search saturating, outbound team under-performing) or is the whole mix drifting? The per-channel per-cohort CAC view names the failing channel and directs the reallocation decision.

**Lever 4 — R&D allocation.** If R&D as a percentage of revenue is above benchmark (typically 30-45% at Series-B, 20-30% at Series-C+) without a clear product outcome to justify it, R&D dollars are consuming burn without proportional revenue return. The question: is the R&D headcount aligned to the growth priorities the CFO's model implies? R&D over-investment is one of the two most common contributors to a high burn multiple (the other being an oversized S&M team that isn't producing).

The corollary for the CFO: the scorecard doesn't just report the number; it names the failing lever. A one-page CFO memo for the board on capital efficiency should have the format: (1) headline metrics with benchmark comparisons, (2) diagnosis — which lever(s) are failing and why, (3) the operational actions being taken and the expected timeline for the metrics to reflect them. Chapter 7 covers how this feeds into the fundraise narrative and board governance.

## The rule-of-thumb reference table by ARR band

For quick reference, the approximate benchmark ranges by ARR stage (subject to the caveats above — verify against current-year data):

| Metric | Series-A ($1-5M ARR) | Series-B ($5-25M ARR) | Series-C ($25-75M ARR) | Late/growth ($75M+ ARR) |
|---|---|---|---|---|
| Growth rate (YoY) | 200%+ | 100-150% | 60-100% | 40-70% |
| Gross margin | 70%+ | 72-78% | 74-80% | 76-82% |
| Burn multiple | Highly variable | 1-2× | 1-1.5× | Approaching 1× |
| CAC payback (mo) | Not yet stable | 12-18 | 12-24 | 15-24 |
| NRR | Emerging | 110-120% | 115-130% | 120-135% |
| GRR | Emerging | 85-92% | 90-95% | 92-96% |
| Rule of 40 | N/A (growth dominates) | 40-80% (growth-heavy) | 40-60% | 40-50% |
| Cash conversion score | N/A (too early) | 0.4-0.7 | 0.5-0.9 | 0.7-1.2+ |

<!-- needs-research: replace this table with values traceable to the current-year OpenView / Bessemer / KeyBanc data, with citations per row -->

Bands are directional. Investors will accept a metric outside the band if the CFO can name the reason and the corrective plan. What they will not accept is a metric outside the band that the CFO cannot explain, or worse, hadn't noticed.

## Common capital-efficiency mistakes

Pre-diligence checklist:

- **Burn multiple computed on gross burn instead of net burn.** Gross burn is spend without any offset; net burn is spend minus revenue collection. The industry-standard convention is net burn.
- **CCS computed with gross capital raised, not net.** Total capital raised minus current cash isolates the capital *actually consumed*. Companies that recently raised a large round have inflated CCS numerators if they don't subtract cash.
- **Rule of 40 with billings growth instead of revenue / ARR growth.** ARR growth is the canonical numerator for private-company Rule of 40. Billings growth is a different (bookings-based) metric and is not comparable.
- **Comparing burn multiple across companies without normalising for non-recurring items.** Financing cash flows, one-time gains, and unusual items distort the ratio; disclose the normalisation.
- **Benchmarking against old data.** Venture-benchmark bands shift year to year — 2021-vintage numbers are not defensible in 2025. Always cite the year of the benchmark report.
- **Reporting metrics without diagnosis.** A scorecard that says "burn multiple 3.2×, target ≤2×" is incomplete without naming *why*. Investors read the diagnosis, not just the numbers.

## Summary

- Burn multiple = net burn ÷ net-new ARR; a period metric of marginal capital efficiency. Below 1× is "amazing"; above 3× is a problem.
- Cash conversion score = current ARR ÷ (total capital raised − current cash); a lifetime metric of cumulative capital efficiency. Above 0.5 is healthy; above 1.0 is best-in-class.
- Rule of 40 = growth rate + FCF margin; a balance metric. 40%+ is healthy; the metric matters most at Series-C and beyond.
- All three are pattern-matched against benchmark data from OpenView, Bessemer, Meritech, SaaStr, a16z, and KeyBanc. Cite the year.
- The scorecard's diagnostic value is naming which of four levers — top-line growth, gross margin, S&M efficiency, R&D allocation — is failing.
- The CFO's board memo on capital efficiency has three sections: metrics with benchmarks, diagnosis, corrective actions with timelines.

Chapter 7 places the entire unit-economics-and-capital-efficiency stack against the sideways boundary with GTM and turns to the specific fundraising narrative that the pack supports.
