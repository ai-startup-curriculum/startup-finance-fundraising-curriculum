# NRR and GRR as Compounding Capital-Efficiency Levers

## Why this matters

If a startup could pick one metric to move to the top of a Series-A deck, it would be net revenue retention. Growth-at-any-cost startups that can't defend their unit economics all show high growth rates; capital-efficient startups that get through fundraising markets show high NRR. Bessemer's *State of the Cloud* reports and Meritech's SaaS-comps analysis consistently identify NRR as one of the two or three variables most correlated with revenue-multiple valuations for public SaaS companies. On the fundraising side, a startup with 120% NRR at $10M ARR is quantitatively a different capital story than a startup with 90% NRR at $10M ARR — the former can hit $50M ARR with less new-customer acquisition, less S&M spend, and less dilutive capital than the latter.

The failure mode: a founder reports NRR and GRR from the CRM's "renewal report" without checking that the two reconcile to each other, to the cohort table, and to the accrual P&L. In diligence, the numbers don't tie, and the CFO spends the diligence cycle rebuilding retention math instead of defending the business. This chapter installs the CFO-grade definitions, the walk from GRR to NRR to gross bookings that a board pack needs, and the specific way NRR compounds into capital efficiency.

## The two definitions, precisely

Net revenue retention (NRR) and gross revenue retention (GRR) both measure how much revenue from a starting-period cohort of customers is *retained and expanded* (NRR) or *retained only* (GRR) in a later period. Both are typically reported over trailing-12-month windows.

**Gross revenue retention (GRR)** — the fraction of a starting cohort's revenue that survives through a measurement period, counting only downgrades and churn as negatives, *not* counting expansion. Capped at 100%.

Formally, for a starting cohort of customers with revenue $R_0$ at the start of the period:

$$
\text{GRR} = \frac{R_0 - \text{Downgrades} - \text{Churn}}{R_0}
$$

GRR isolates the "stickiness" of the customer base — the retention side of the story. A GRR of 92% says 8% of the starting revenue was lost to churn or downgrades regardless of what expansion did. Best-in-class SaaS GRR is typically 90-95%; anything below 85% signals a material churn problem.

**Net revenue retention (NRR)** — the same cohort's revenue at the end of the period *including expansion*, divided by the starting revenue. Can exceed 100%.

$$
\text{NRR} = \frac{R_0 - \text{Downgrades} - \text{Churn} + \text{Expansion}}{R_0}
$$

NRR captures the "growth from the existing base" story. An NRR of 120% says the same cohort of customers, one year later, is producing 20% more revenue than they were a year ago even after accounting for whoever left. Best-in-class SaaS NRR is typically 115-130%; the elite public-SaaS band reaches 135-150%.

The critical property: NRR *excludes new-customer revenue*. If a startup added $2M of new-customer revenue in the trailing 12 months, that $2M is not in the NRR numerator. NRR measures only what the *existing customer base at the start of the period* produced by the end of it.

## The NRR / GRR walk — what a board pack shows

A board pack presents a walk that reconciles starting ARR to ending ARR by naming the retention drivers. The canonical presentation:

```
Starting ARR (Jan 1)                                    $10.00M

    - Churn (customers lost)                            ($0.60M)
    - Downgrades (customers who reduced spend)          ($0.20M)
    ───────────────────────────
    = Retained ARR                                       $9.20M
      → GRR = 9.20 / 10.00 = 92.0%

    + Expansion (existing customers who added spend)    $1.80M
    ───────────────────────────
    = Ending ARR from starting cohort                   $11.00M
      → NRR = 11.00 / 10.00 = 110.0%

    + New logos (customers who signed up in period)      $3.00M
    ───────────────────────────
    = Total ending ARR (Dec 31)                         $14.00M
      → Growth = 14.00 / 10.00 = 40.0% (net-new ARR growth)
```

This walk is the artefact that lives on the KPI slide of a board pack and on the cohort-retention slide of a fundraise deck. Every arithmetic step is a real business event that can be tied back to a customer-level ledger — a specific customer churn, a specific downgrade, a specific expansion, a specific new-logo close. The walk also reconciles into the accrual P&L: ending ARR should match the run-rate revenue implied by the last month of the period, adjusted for one-time revenue.

The four buckets on the walk — churn, downgrade, expansion, new — should each have a *customer-count* view and an *ARR-dollar* view. A company with a churn dollar of $600K might have churned 12 customers (a small number of large accounts) or 150 customers (many small accounts); the two situations have very different diagnostic implications. Both views should appear.

## Why NRR compounds and how it changes the capital story

The reason NRR is treated as one of the most important metrics in SaaS is that it operates on the *existing revenue base*, and the base compounds. To make the effect concrete:

Consider two hypothetical startups, both at $10M ARR entering Year 1. Both add $5M of new-logo ARR each year. Startup A has 90% NRR; Startup B has 120% NRR.

**Startup A (90% NRR, $5M new logos per year):**
- End of Year 1: $10M × 90% + $5M = $14.0M ARR
- End of Year 2: $14.0M × 90% + $5M = $17.6M ARR
- End of Year 3: $17.6M × 90% + $5M = $20.8M ARR
- End of Year 4: $20.8M × 90% + $5M = $23.7M ARR
- End of Year 5: $23.7M × 90% + $5M = $26.4M ARR

**Startup B (120% NRR, $5M new logos per year):**
- End of Year 1: $10M × 120% + $5M = $17.0M ARR
- End of Year 2: $17.0M × 120% + $5M = $25.4M ARR
- End of Year 3: $25.4M × 120% + $5M = $35.5M ARR
- End of Year 4: $35.5M × 120% + $5M = $47.6M ARR
- End of Year 5: $47.6M × 120% + $5M = $62.1M ARR

Same new-logo pace, same starting point, radically different outcomes. Startup B reaches $62M ARR while Startup A reaches $26M ARR. Startup B's growth compounds; Startup A's growth is arithmetic (each year layers ~$3M of net-new ARR on the base, held back by the 10% base erosion).

Reframed as a capital-efficiency question: to reach the same ending ARR, Startup A has to spend far more S&M dollars acquiring far more customers. If it costs $8K to acquire a new-logo dollar of ARR at Startup A's blended CAC, and each of the 5 years buys $5M of new logo ARR, Startup A spent $200M on S&M to reach $26M ARR while Startup B — same S&M spend — reached $62M ARR. Or, in the flipped framing, Startup B could have reached $26M ARR with less than half the S&M spend Startup A required.

The 120% NRR startup effectively halves its CAC-payback-adjusted growth requirement compared to the 90% NRR startup. This is not marketing hyperbole; it is a compounding-arithmetic property that every serious growth investor spreadsheets when they see the NRR number on a deck.

## Where expansion revenue actually comes from — the four channels

For NRR to be defensible, the CFO must be able to point to the operational mechanisms by which existing customers expand. The four canonical expansion channels in SaaS:

**1. Seat expansion.** Customer buys more licenses within the same product. The classic per-seat SaaS model — Slack, Zoom, Figma — where the customer expands as they hire more people or roll the product out to more teams. Seat expansion is the most predictable expansion channel because it correlates with the customer's own headcount growth.

**2. Usage expansion.** For usage-based-priced products (Snowflake, DataDog, Twilio, most infrastructure), the customer's own workload growth drives expansion. This channel produces the highest NRR figures in the public SaaS index — Snowflake and DataDog have reported NRR above 150% at various points during their high-growth phases.

**3. Cross-sell (multi-product expansion).** Customer adopts a second product from the same vendor. HubSpot's motion of selling Sales Hub into customers who bought Marketing Hub, or Salesforce's sale of Service Cloud into Sales Cloud customers, or Datadog's expansion from monitoring into logs, APM, and security. Cross-sell requires a multi-product portfolio and a sales motion that is capable of expansion selling.

**4. Tier upgrade.** Customer moves from a lower-tier plan to a higher-tier plan (Basic → Pro → Enterprise). Common in PLG motions where product usage naturally graduates a customer into higher tiers.

A CFO-authored NRR walk decomposes expansion into these four channels. A total NRR of 120% might be 5 points seat expansion + 8 points usage + 5 points cross-sell + 2 points tier upgrade, netting 20% expansion against ~10% churn+downgrade to reach 110% GRR-net-of-expansion of… wait, this doesn't add up — because a 120% NRR contains, by definition, both the *retained-and-expanded* contribution and the *retained-only* contribution. The correct decomposition is:

```
Starting ARR                    $10.0M     100%
- Churn                         ($0.6M)    (6%)
- Downgrade                     ($0.2M)    (2%)
= GRR                            $9.2M     92%

+ Seat expansion                +$0.5M     +5%
+ Usage expansion               +$0.8M     +8%
+ Cross-sell                    +$0.4M     +4%
+ Tier upgrade                  +$0.1M     +1%
= Total expansion               +$1.8M     +18%

= NRR                           $11.0M     110%
```

This decomposition reveals whether the NRR number is diversified (multiple channels contributing) or concentrated (one channel doing all the work). A concentration in one channel is a risk — if usage-based pricing hits a customer's usage ceiling, or if a single cross-sell campaign was the source of the year's expansion, the NRR number is more fragile than it looks.

## GRR — the churn story on its own

GRR is the more conservative retention metric because it caps expansion out and only measures the losses. A company reporting 130% NRR and 85% GRR is a company where the expansion is masking a real churn problem: 15% of the starting cohort's revenue was lost, and the growth-from-existing story is entirely dependent on the 30-45% expansion coming in to compensate. If the expansion motion breaks — a competitive product ships that satisfies the same expansion need, a customer segment reaches a natural usage ceiling, a macro downturn compresses IT budgets — the 85% GRR is what remains.

Best-in-class GRR by segment (based on the SaaS-benchmark data from OpenView, Bessemer, and public-SaaS 10-K disclosures):

| Segment | Best-in-class GRR | Notes |
|---|---|---|
| Enterprise SaaS | 92-97% | Multi-year contracts, high switching cost |
| Mid-market SaaS | 85-92% | Annual contracts, moderate switching cost |
| SMB SaaS | 75-85% | Monthly billing common, high SMB mortality drives some churn |
| PLG / self-serve | Highly variable | Depends on activation and monetisation motion |

<!-- needs-research: cite the current-year OpenView SaaS Benchmarks and Bessemer State of the Cloud data on GRR by segment; verify the specific bands quoted here against the most recent survey -->

The pairing of NRR and GRR gives two independent readings: how healthy is the base (GRR), and how much of the base's growth is being manufactured by expansion (NRR - GRR). Investors read both.

## Logo retention vs. dollar retention — the same story at two units

There's a parallel pair of metrics: gross logo retention and net logo retention. Logo retention counts customers, not dollars.

- **Gross logo retention** = (customers retained at end of period) ÷ (customers at start of period). Capped at 100%.
- **Net logo retention** is rarely reported separately because "expanding a logo" doesn't have a clear meaning — a customer either retained or didn't. Some companies report a "logo NDR" as an ARPU-adjusted signal, but it's not standard.

The interesting comparison is dollar retention vs. logo retention. A company with 92% dollar GRR but 78% logo GRR is losing a lot of small customers while retaining the large ones — 22% of customers churned but only 8% of revenue did. This is a normal enterprise-SaaS pattern (small-customer mortality is high; the enterprise base is sticky). A company with the reverse — 78% dollar GRR but 92% logo GRR — is losing a lot of revenue from customers who technically retained (downgrades from enterprise to mid-market plans). The reverse pattern is a red flag and usually signals a pricing or product-value problem.

Both views appear in a well-authored board pack.

## The measurement window — trailing-12-months is standard

NRR and GRR are typically reported over a trailing-12-month window because it smooths out seasonal and one-off effects. The mechanics:

- Take the set of customers who were active at the *start* of the period (12 months ago).
- Track that specific cohort's revenue at the end of the period.
- Ratio.

Some companies report NRR / GRR at shorter windows (quarterly or monthly annualised); these are noisier and mostly used for internal management. External reporting is trailing-twelve-months.

For companies with lumpy renewal cycles (e.g., annual-contract enterprise SaaS where 30% of the base renews in a single month), the TTM window smooths across the whole renewal calendar. Reporting a monthly-annualised NRR right after a big renewal month over-states NRR; right before it, understates. TTM avoids the issue.

## NRR / GRR and their relationship to the cohort table

NRR and GRR are company-level aggregates; the cohort table (chapter 4) is the customer-level substrate. The two must reconcile:

- **GRR at TTM** should equal the weighted average of layer-2 M12 retention across all cohorts that were active at the start of the period.
- **NRR at TTM** should equal the weighted average of layer-4 M12 net dollar retention across the same cohorts.

If they don't reconcile, one of two things is wrong: either the cohort table's per-customer ARR data doesn't match the finance-system-of-record ARR data, or the NRR calculation is counting customers or dollars that don't belong. Both are common failure modes and both are diligence-week traps. The reconciliation is a specific piece of the pre-diligence unit-economics review.

## Common NRR / GRR mistakes

- **Including new logos in the numerator.** The definition specifically excludes new-logo revenue. Some CRM reports blend the two; the resulting "retention" number is really total growth divided by starting ARR and is not comparable to what other companies report.
- **Netting expansion against churn in GRR.** GRR is *gross* — it does not net expansion. If your GRR is above 100% you're computing NRR.
- **Not caring about currency.** For companies with material international revenue, exchange-rate movements over a TTM window can move NRR and GRR by 1-3 points. Report constant-currency retention alongside actuals for international companies.
- **Renewal-window versus period-window confusion.** For enterprise-SaaS companies with annual renewal cycles, the definition of "expansion" (upsell at renewal) and the definition of "churn" (customer chose not to renew) can be scoped to the renewal event or to the calendar month. Companies usually report renewal-based NRR for detailed reporting and calendar-window NRR for the top-line number. Disclose which.
- **Reporting NRR without the walk.** A single NRR number without the churn / downgrade / expansion decomposition is a top-line summary that hides diagnostic content. Investors will always ask for the walk; produce it upfront.
- **Using the wrong denominator.** NRR uses starting-cohort ARR as the denominator. Some founders use ending ARR as the denominator, which is arithmetically wrong and inflates the ratio.

## Summary

- GRR measures the fraction of starting revenue that survives churn and downgrades; capped at 100%; best-in-class SaaS is 90-95%.
- NRR adds expansion to the GRR numerator; can exceed 100%; best-in-class SaaS is 115-130%.
- The NRR / GRR walk — starting ARR → churn → downgrade → GRR → expansion → NRR → new logos → ending ARR — is the board-pack presentation.
- NRR compounds on the existing base; a 120% NRR startup can reach much higher ARR at the same S&M spend as a 90% NRR startup, because the base grows without new-logo cost.
- Expansion decomposes into four channels: seat, usage, cross-sell, tier upgrade. Concentration in one channel is a risk.
- GRR and NRR should be reported paired; a high NRR masking a low GRR is a specific fragility.
- Dollar retention vs. logo retention gives two independent views; enterprise SaaS often has high dollar / lower logo retention (small-customer mortality); the reverse is a red flag.
- Both metrics reconcile to the cohort table; the reconciliation is a diligence-artefact.

Chapter 6 turns to the capital-efficiency instruments that pair with unit economics in the CFO's scorecard — burn multiple, cash-conversion score, Rule of 40 — benchmarked against the public data providers.
