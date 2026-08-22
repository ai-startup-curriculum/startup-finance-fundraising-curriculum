# mod-102 — Unit Economics & Cohort Financial Modeling

**CAC, LTV, Payback, and Burn Multiple at CFO Grade**

**Track:** [Startup Finance & Fundraising](../../CURRICULUM.md)
**Stage:** PRE-SEED / SEED
**Hours:** 24 (7 chapters + 6 exercises + 1 lab + 1 quiz)

## What this module installs

The cohort-based, discount-rate-adjusted, board-defensible modelling vocabulary a CFO needs the moment a Series-A investor opens a diligence conversation with *"walk me through your unit economics."* The GTM-operator view of the same numbers — magic number, sales-efficiency ratios, funnel-stage conversion — is owned by [`startup-product-gtm-curriculum`](https://github.com/ai-startup-curriculum/startup-product-gtm-curriculum). This module is what a CFO layers on top so the numbers survive an investor's model. Specifically:

- **Fully-loaded CAC** per acquisition channel per monthly cohort — every dollar of S&M spend, plus the cost-to-serve that produced the signup, allocated to the customers that channel produced in that month.
- **Cohort-based LTV** — the present value of a cohort's gross-profit stream, discounted at a venture-appropriate rate — not the ARPU × gross-margin ÷ churn shorthand that appears on early-stage decks.
- **Payback period** measured off the cohort table itself, in months, not the arithmetic CAC ÷ (ARPU × gross margin) ratio.
- **Gross-margin bridge** decomposing GAAP gross margin into hosting / third-party COGS / support / customer-success / delivery, with the SaaS and marketplace bands that trigger investor scepticism.
- **The cohort table** — monthly signups → retained → revenue → cost-to-serve → gross profit — as the single artefact from which retention, expansion, and churn are read directly.
- **NRR and GRR** as compounding capital-efficiency levers, and the walk that reconciles the two in a board pack.
- **Burn multiple, cash-conversion score, and Rule of 40** — the modern capital-efficiency instruments benchmarked against OpenView, Bessemer, and SaaStr data and used to diagnose which lever a specific startup is failing.
- **The ownership boundary and the fundraising narrative** — where GTM's operator view ends and where the CFO's board-defensible framing begins, and how the module's outputs feed the deck, the model, and the data room.

## Chapters

1. [`01-fully-loaded-cac-per-channel-and-cohort.md`](01-fully-loaded-cac-per-channel-and-cohort.md) — what "fully loaded" and "per channel per cohort" actually mean, and why blended CAC is lagging and lossy.
2. [`02-cohort-ltv-and-the-discount-rate.md`](02-cohort-ltv-and-the-discount-rate.md) — cohort LTV as a discounted gross-profit stream, choosing a venture-appropriate discount rate, and the failure mode of an undiscounted 5-year LTV.
3. [`03-gross-margin-decomposition-and-bridge.md`](03-gross-margin-decomposition-and-bridge.md) — cost-of-revenue buckets, SaaS-vs.-marketplace gross-margin bands, and a defensible gross-margin bridge.
4. [`04-cohort-table-construction-and-reading.md`](04-cohort-table-construction-and-reading.md) — building the cohort table and reading retention / expansion / churn directly off it.
5. [`05-nrr-and-grr-as-capital-efficiency-levers.md`](05-nrr-and-grr-as-capital-efficiency-levers.md) — the two retention metrics, the compounding capital-efficiency effect, and the walk a board pack needs.
6. [`06-capital-efficiency-instruments-burn-multiple-cash-conversion-rule-of-40.md`](06-capital-efficiency-instruments-burn-multiple-cash-conversion-rule-of-40.md) — burn multiple, cash-conversion score, Rule of 40 benchmarked by ARR band and used as a diagnostic.
7. [`07-ownership-boundary-with-gtm-and-the-fundraising-narrative.md`](07-ownership-boundary-with-gtm-and-the-fundraising-narrative.md) — where the GTM-operator view ends, where the CFO view begins, and how the unit-economics pack feeds the fundraise.

## Exercises

1. [`exercises/exercise-01-fully-loaded-cac-per-channel-derivation.md`](exercises/exercise-01-fully-loaded-cac-per-channel-derivation.md) — build a fully-loaded per-channel per-cohort CAC schedule from an S&M ledger (~3h).
2. [`exercises/exercise-02-cohort-ltv-with-discount-rate-derivation.md`](exercises/exercise-02-cohort-ltv-with-discount-rate-derivation.md) — compute cohort LTV three ways (undiscounted, discounted, capped) and defend a discount-rate choice (~3h).
3. [`exercises/exercise-03-gross-margin-bridge-authoring.md`](exercises/exercise-03-gross-margin-bridge-authoring.md) — decompose a P&L into a defensible gross-margin bridge and benchmark against Meritech / Bessemer bands (~3h).
4. [`exercises/exercise-04-cohort-table-build-and-read.md`](exercises/exercise-04-cohort-table-build-and-read.md) — build the full cohort table for 12 months of signups and read the retention / expansion / churn signals (~4h).
5. [`exercises/exercise-05-nrr-and-grr-walk-authoring.md`](exercises/exercise-05-nrr-and-grr-walk-authoring.md) — produce the NRR / GRR walk with a base / expansion / contraction / churn / new bridge (~3h).
6. [`exercises/exercise-06-burn-multiple-and-rule-of-40-diagnosis.md`](exercises/exercise-06-burn-multiple-and-rule-of-40-diagnosis.md) — compute burn multiple, cash-conversion score, and Rule of 40 for one startup and diagnose the failing lever (~3h).

## Lab

- `lab-01-publish-a-unit-economics-pack-for-one-startup` — planned; produces the end-to-end unit-economics pack (fully-loaded CAC by channel, cohort LTV with discount rate, cohort table, gross-margin bridge, NRR/GRR walk, capital-efficiency scorecard) for one hypothetical or real startup, in the shape a Series-A data room expects. Placeholder to be authored in a subsequent content cycle.

## Quiz

- `quiz-01` — planned; 12-15 questions covering the seven chapter objectives. Placeholder to be authored in a subsequent content cycle.

## Reference

- [`resources.md`](resources.md) — the citable SaaS-metrics canon, venture-benchmark data providers, and academic references behind the module.

## How this module fits

The module sits on the accrual-basis financial vocabulary from [`mod-101`](../mod-101-startup-accounting-foundations/README.md) — revenue, gross margin, deferred revenue, and the four SaaS numbers are prerequisites, not re-taught here. The cohort table this module builds is a direct input to [`mod-103`](../mod-103-three-statement-model-and-driver-based-forecasting/) (the retention curve becomes a driver in the three-statement model), to [`mod-106`](../mod-106-startup-valuation-frameworks/) (the growth-adjusted revenue multiple is bounded by the Rule-of-40 diagnostic and the NRR level), to [`mod-107`](../mod-107-fundraising-strategy-and-investor-targeting/) (the unit-economics pack is a data-room artefact), to [`mod-108`](../mod-108-term-sheets-and-preferred-stock-economics/) (the valuation the term sheet reflects is anchored to the unit-economics narrative), and to [`mod-110`](../mod-110-board-and-investor-governance-for-the-cfo/) (the KPI dashboard reconciled to the cohort table is a board-pack staple).

The module *does not* teach: GTM funnel mechanics, sales-motion design, pricing-page architecture, or channel-selection strategy (those are `startup-product-gtm-curriculum`). It does not teach three-statement model construction (that is [`mod-103`](../mod-103-three-statement-model-and-driver-based-forecasting/)) or the valuation methods that consume the outputs (that is [`mod-106`](../mod-106-startup-valuation-frameworks/)). It teaches the CFO's view of the numbers: fully loaded, cohort based, discounted where it should be, benchmarked against real venture data, and packaged for a board and a lead-investor audience.
