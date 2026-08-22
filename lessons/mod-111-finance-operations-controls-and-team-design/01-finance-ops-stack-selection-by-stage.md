# Finance-Ops Stack Selection by Stage

## Why this matters

The finance-ops stack is the CFO's plant and equipment. It is the software that produces every invoice the company sends, every dollar the company pays out, every payroll run, every ledger entry, every accrual, every close pack, every board pack. Choose it well and the finance team runs a five-business-day close and produces audit-ready financials in the background while doing higher-leverage work. Choose it badly — either by staying on a founder-tier stack past the point of failure, or by over-buying the enterprise stack years before the company can use it — and the finance team spends its calendar reconciling around the stack rather than closing the books.

The CFO decision is not "which vendor is best." It is *which stack the company graduates onto next, and when to graduate*. Every stack tier has a set of graduation events — first audit, first NetSuite migration, first Coupa procurement rollout — that dictate when the current tier stops being fit-for-purpose. Missing a graduation event by six months costs one bad close cycle. Missing it by 18 months costs a fundraise slip.

## The five layers

The stack decomposes into five layers. Each layer has a distinct set of vendors at each stage. Naming the layers first — and separating the vendor choice inside a layer from the layer's stage-appropriate tier — is the discipline that keeps the stack coherent.

1. **Banking and ops** — where cash lives, where corporate cards live, where treasury and FX and wires and bill-pay happen.
2. **General ledger (GL) / accounting** — where journal entries land, where the trial balance is produced, where the financial statements are generated.
3. **Payroll and HRIS** — where employees are onboarded, where W-2 / 1099 / international contractor pay is run, where benefits are administered.
4. **Accounts payable (AP) / spend / procurement** — where vendor bills flow, where they are approved, where purchase orders originate, where corporate spend is managed.
5. **FP&A / planning / consolidation** — where the model lives, where actuals are pulled against plan, where consolidation and multi-entity roll-up happens.

There are adjacent layers — billing / subscription management (Stripe / Chargebee / Zuora / Maxio), revenue recognition (RightRev / Ordway / Sage Intacct's rev-rec module), tax (Avalara / TaxJar / Anrok — covered in chapter 7), audit / controls tooling (AuditBoard / Workiva at growth-stage) — but the five above are the load-bearing structure.

## The tiers by stage

### PRE-SEED / SEED — the founder-bookkeeping tier

At pre-seed and early seed, the company has a founder or COO doing the bookkeeping, plus an outsourced accountant or bookkeeping service reviewing monthly (Kruze, Pilot, Bench, Zeni). The stack is chosen for *low setup cost, minimal ongoing admin, and easy handoff to an outsourced provider*.

- **Banking / ops.** Mercury or Brex or SVB (post-2023 acquisition by First Citizens Bank) or a traditional bank (Chase, Wells) with corporate cards. Ramp and Brex both offer combined banking + corporate cards + bill-pay. The choice is largely aesthetic at this stage; graduation to a dedicated treasury workflow does not come until Series-B+.
- **GL.** QuickBooks Online (QBO) or Xero. Both are cloud-native, both integrate with every early-stage banking / AP / payroll product. QBO has larger US market share; Xero has stronger multi-currency handling.
- **Payroll.** Gusto or Rippling. Gusto is simpler and cheaper; Rippling combines payroll with HRIS and IT device management (a stronger fit once headcount crosses ~20). Justworks and TriNet are PEO alternatives that offer better benefits pricing but restrict some entity-structuring flexibility.
- **AP / spend.** Ramp or Brex bill-pay; Bill.com for vendor-heavy workflows. Corporate cards on Ramp / Brex feed the AP flow automatically.
- **FP&A.** Excel or Google Sheets. Buying an FP&A platform at this stage is over-buying.

The whole stack at this tier costs $500-$2,000 / month depending on headcount and card-spend volume. The outsourced-accounting service on top adds $2,000-$8,000 / month. The full finance-ops line-item runs $3,000-$10,000 / month and the CFO decision at this stage is "which outsourced provider to run this on" more than "which vendors to string together."

### SERIES-A — the first-controller tier

At Series-A, the company hires a controller (or a Head of Finance who is functionally the controller — chapter 2 covers the title question). The stack is chosen to *give the controller enough leverage to run a clean close without breaking the pre-seed / seed stack yet*.

- **Banking / ops.** Same as prior stage, plus the treasury workflow starts to matter — where does excess cash sit (money-market fund at the primary bank, or a treasury product like Meow / Arc / Treasure), what is the FX policy for the first international entity if applicable.
- **GL.** Usually still QBO or Xero, but with the accounting team's discipline now installed on top — clean chart of accounts, proper multi-class or department tagging, deferred-revenue subledger. Some Series-A companies migrate to Sage Intacct here as a middle step between QBO / Xero and NetSuite; the CFO decision is whether the migration effort is worth avoiding a bigger migration later. The most common answer at Series-A is "stay on QBO, plan for NetSuite at Series-B."
- **Payroll.** Same as prior stage; Rippling more common as headcount and IT-device management grow.
- **AP / spend.** Ramp or Brex, with approval routing now configured (chapter 5 on controls covers the approval-hierarchy design). Bill.com used for vendor invoices that arrive as PDFs.
- **FP&A.** Excel / Google Sheets remains standard. Some Series-A companies adopt Causal, Runway, Mosaic, or Pry here to graduate the founder-authored spreadsheet model onto a purpose-built FP&A tool. The decision is whether the FP&A hire (chapter 2) will maintain a spreadsheet model or a platform model.
- **Adjacent — billing.** For SaaS: Stripe Billing is the default; Chargebee / Maxio / Recurly are alternatives with stronger dunning / lifecycle features. For usage-based / consumption pricing: Metronome / Orb / m3ter. Getting the billing choice right at Series-A saves a large migration project at Series-B when revenue-recognition volume grows.

Whole-stack cost at Series-A typically runs $5,000-$25,000 / month.

### SERIES-B — the NetSuite-migration tier

Series-B is the graduation event for the general-ledger layer. The QBO / Xero ledger, however clean, starts to fail on three axes: multi-entity consolidation (international subsidiaries, holding-company structure), audit-scale transaction volume (the first outsourced audit — chapter 4 — is often a Series-B event), and the depth of the deferred-revenue and revenue-recognition subledger that ASC 606 compliance requires at scale.

- **Banking / ops.** Now firmly separated by function: primary operating cash at Bank A, treasury / MMF at Bank B or a dedicated treasury platform, FX / international at a third provider (Wise, Airwallex, Nium). Corporate cards standardised on one issuer (Ramp / Brex / Airbase — see AP layer).
- **GL — the migration.** NetSuite is the market default for the Series-B to pre-IPO segment. Sage Intacct is a common alternative especially for services-heavy or non-SaaS businesses. Both migrations are 3-6 month projects with an implementation partner; the CFO owns scoping (chart-of-accounts design, subsidiary structure, subledger configuration, revenue-recognition automation) even if a systems integrator runs the build. NetSuite implementations that fail almost always fail on chart-of-accounts / entity-structure decisions made in month 1, not on data-migration in month 5.
- **Payroll / HRIS.** Rippling or Gusto for smaller Series-B; larger and more-international Series-B companies migrate to Deel / Remote for the international-entity coverage or start planning a Workday HCM migration in anticipation of Series-C+.
- **AP / spend.** Ramp, Brex, or Airbase, with formal approval hierarchies, procurement policy enforcement, and the audit-trail depth the auditor will need. Concur remains the reference at the enterprise end but is over-buying at Series-B.
- **FP&A.** Purpose-built FP&A platform is the norm — Workday Adaptive Planning (formerly Adaptive Insights), Anaplan, Vena, Mosaic, Causal, or Cube. The choice depends on model complexity, the FP&A team's platform familiarity, and integration with the new NetSuite GL. Consolidation is often handled inside the FP&A platform or via a dedicated consolidation tool (OneStream, Fluence, Prophix) at the upper end.

Whole-stack cost at Series-B typically runs $25,000-$100,000 / month.

### SERIES-C+ AND PRE-IPO — the enterprise-controls tier

Series-C and later — especially any company on a dual-track (chapter 8) — layers a controls-and-procurement tier on top of the Series-B stack.

- **Procurement.** Coupa is the enterprise reference; Zip is the modern lightweight alternative with a strong SaaS-vendor focus; SAP Ariba is common in industries with heavy supplier compliance. Purchase-order requisition, three-way match (PO / receipt / invoice), vendor onboarding with W-9 / W-8 collection and OFAC screening.
- **Close automation.** Blackline (or FloQast, or the newer Numeric) for close-task management, account reconciliation automation, and audit-trail preservation. The 5-business-day close (chapter 3) at scale is very hard without one of these.
- **FP&A / consolidation.** Workday Adaptive Planning or Anaplan at scale; Oracle EPM / Hyperion at the very high end. Consolidation via OneStream / Fluence / Workday for multi-entity roll-ups with FX translation.
- **Contract / revenue.** RightRev, Ordway, or NetSuite's own revenue-recognition module for automated ASC 606 revenue-recognition at contract volume the manual subledger can no longer handle.
- **Treasury.** Kyriba, GTreasury, or Trovata for cash-visibility, FX exposure, and debt-covenant monitoring across many accounts and many entities.
- **Audit / controls tooling.** AuditBoard or Workiva at the pre-IPO stage for SOX-404 control documentation, test-of-controls tracking, and the S-1 workflow (chapter 8).

Whole-stack cost at Series-C+ typically runs $75,000-$400,000+ / month depending on scale, entity count, and international footprint.

## The graduation events

Each layer has a small number of specific events that trigger the migration. Naming the events, and tracking whether they have occurred, is the CFO discipline that avoids either premature migration or a missed one.

**GL graduation (QBO / Xero → NetSuite / Intacct):**
- First outsourced audit is committed (or planned within 12 months).
- Second operating entity added (international sub, holding company, spin-out).
- Deferred-revenue schedule crosses ~500 active contract-months tracked and the spreadsheet subledger starts producing errors.
- Multi-currency operations begin.
- Monthly transaction volume crosses the point QBO / Xero begin degrading (rough benchmark: 5,000+ monthly transactions; verify against current vendor scale guidance <!-- needs-research: current QBO / Xero recommended transaction-volume ceilings from vendor documentation -->).

**AP / procurement graduation (Ramp / Brex → Coupa / Zip):**
- PO / requisition workflow required by the auditor as a control (Series-B / C).
- Vendor count crosses ~200 active vendors and vendor onboarding becomes a bottleneck.
- Three-way-match required by internal controls program.

**FP&A graduation (spreadsheet → Adaptive / Anaplan):**
- Consolidated model spans multiple entities with FX translation.
- Two or more full-time FP&A analysts collaborating on the model produce merge-conflicts and version drift.
- Board pack requires actuals-vs.-plan variance analysis at a cadence the manual spreadsheet cannot support.

**Payroll / HRIS graduation (Gusto → Rippling → Workday):**
- Headcount crosses ~200 (Rippling begins to strain at the upper end for complex org designs).
- International employee count exceeds ~30-50 across three or more countries.
- Compensation-planning cycle needs to sit inside the HRIS rather than in a separate spreadsheet.

**Close-automation graduation (spreadsheet checklist → FloQast / Blackline / Numeric):**
- 5-business-day close target is committed and the manual checklist starts to slip.
- Auditor requests documented control activities and reviewer sign-off per account.

## The two failure modes

**Failure mode 1 — staying too long.** The most common. Company at late Series-B still on QBO, deferred-revenue schedule maintained in a Google Sheet with ~2,000 active contract-months, and the year-end audit turns into a five-month project instead of a six-week project because the auditor requests reconciliations that require rebuilding the subledger. Cost: one delayed audit, one delayed fundraise, one very unhappy audit committee. The CFO owns the graduation call; delaying it to save $50K in migration cost against a fundraise slip that costs multiple millions in dilution is a false economy.

**Failure mode 2 — jumping too early.** Less common but very expensive. Company at Series-A commits to NetSuite before hiring a controller, before having a coherent chart of accounts, before knowing what the entity structure will look like at Series-B. The implementation goes 6 months and $300K, the resulting NetSuite instance is a mess of misconfigured segments and subledgers, and the company spends the next year fighting the tool. The rule: **hire the controller first; let the controller own the migration choice**. The controller-first sequencing is chapter 2.

## The "graduates onto next" framing

Every stack choice at every stage should be evaluated on two axes: *does it work now* and *does it graduate cleanly to the next tier*. A QBO instance with a clean chart of accounts, proper subledgers, and reconciled monthly balances migrates to NetSuite in six weeks; a QBO instance with a chart of accounts drifting since 2019 migrates in six months. The forward-compatibility discipline is the difference.

At the vendor level, the same discipline applies. Choose Rippling over Justworks at seed if the Series-A trajectory takes headcount past the point where Rippling's HRIS depth becomes load-bearing. Choose Stripe Billing over Recurly at seed if the roadmap includes usage-based pricing where Stripe's metering will simplify the eventual Orb / Metronome integration. The CFO who evaluates each vendor choice against the next two stages, not just the current one, avoids the mid-Series-B rebuild.

## Summary

- The finance-ops stack decomposes into five layers: banking / ops, GL, payroll / HRIS, AP / spend, FP&A / planning.
- Each layer has a distinct set of vendors by stage: pre-seed / seed founder-bookkeeping tier, Series-A first-controller tier, Series-B NetSuite-migration tier, Series-C+ enterprise-controls tier.
- Graduation events (first audit, second entity, contract-volume threshold, headcount threshold, close-cadence target) trigger the migration from one tier to the next.
- The two failure modes are staying too long (audit delay, fundraise slip) and jumping too early (misconfigured enterprise stack the company cannot use).
- The forward-compatibility discipline — choose each vendor against the next two stages, not just the current one — is the CFO practice that keeps the stack coherent.

The next chapter turns to the team that operates the stack.
