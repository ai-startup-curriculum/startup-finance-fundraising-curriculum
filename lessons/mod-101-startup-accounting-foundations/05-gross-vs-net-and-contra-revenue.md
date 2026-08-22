# Gross vs. Net Revenue, Contra-Revenue, and the Agent-vs.-Principal Analysis

## Why this matters

Two contracts with the same $10M of customer-collected cash can produce two very different revenue lines. A pure SaaS vendor collecting $10M in subscription fees books $10M of revenue. A marketplace processing $10M of transactions between third parties and keeping a 15% take-rate books $1.5M of revenue. The difference is not a matter of preference; ASC 606 has an explicit test — the **agent-vs.-principal** analysis — that dictates which of the two answers is correct.

Getting this wrong is expensive in three directions. Overstating revenue by booking gross when you should be booking net inflates every SaaS multiple applied to your top line — investors and auditors both catch this in diligence, and the restatement is embarrassing. Understating revenue by booking net when you should be booking gross deflates your comparable multiples and can drop you below the reporting thresholds SaaS investors screen on. Getting it right *and consistently* is the CFO's job; the revenue-recognition policy memo documents the analysis so the company applies it uniformly across contract types.

Alongside gross vs. net, ASC 606 also formalises the treatment of **contra-revenue** — discounts, credits, refunds, and rebates that reduce revenue rather than add to expenses.

## Gross vs. net — the core question

The core question in every revenue transaction that involves a third party: is the vendor acting as a **principal** (the vendor controls the good or service before it is transferred to the customer, and books the gross transaction as revenue with the third-party cost in COGS) or as an **agent** (the vendor arranges for another party to provide the good or service, and books only the commission or fee as revenue)?

ASC 606-10-55-36 through 55-40 provide the framework. The determinative question: does the vendor control the specified good or service before it is transferred to the customer? The standard offers three indicators that a vendor is a principal (all should be considered together; none is dispositive on its own):

1. **Primary responsibility** for fulfilling the promise to the customer, including responsibility for the good/service being acceptable.
2. **Inventory risk** — the vendor has risk of loss before the good/service is transferred to the customer, or after transfer (returns).
3. **Discretion in establishing the price** for the good/service — the vendor sets the price, not the third party.

If those indicators point to the vendor being an agent — the customer is really contracting with the third party through the vendor's platform, the third party sets its own prices and holds inventory risk, the vendor's obligation is to *arrange* the transaction rather than to *fulfil* it — then the vendor books only the net commission/take-rate as revenue.

## The SaaS-vs.-marketplace divergence

This is the standard illustration of the divergence.

**Pure SaaS vendor** — sells a software subscription for $10M/yr. The vendor develops the software, controls the delivery infrastructure, sets the price, bears the fulfilment risk, and is on the hook if the software fails. Principal. Revenue: $10M/yr. Hosting, third-party API pass-through, and cost-to-serve sit in COGS.

**Marketplace vendor** — a two-sided platform where suppliers list goods/services and buyers purchase them through the platform. The marketplace collects the buyer's payment, remits the supplier's share, and keeps a take-rate (say, 15%). Analysis:
- Primary responsibility: usually the supplier (the marketplace is not on the hook if the good is defective or the service is not performed — the supplier is).
- Inventory risk: usually the supplier (the marketplace does not hold inventory; unsold items remain the supplier's problem).
- Pricing discretion: usually the supplier sets prices (though the marketplace may set the take-rate percentage and require conformance to price ranges).

Agent conclusion: revenue is the $1.5M take-rate, not the $10M of gross merchandise volume (GMV). GMV is a supplementary operating metric disclosed alongside, not a revenue line.

The nuance: some marketplaces have hybrid characteristics. Managed marketplaces that provide QA, guarantees, and refund liability may be principals for some transactions. Marketplaces that begin as pure booking-and-remit and shift over time toward first-party fulfilment (private label, own delivery fleet, own inventory) shift from agent to principal for the transactions that flip. The classification is per performance obligation, not per company. A single company can be principal on some revenue lines and agent on others; the analysis is done per performance obligation.

## Reseller and hybrid patterns

**Value-added reseller (VAR).** A software vendor sells through a channel partner. Depending on the contractual structure — whether the reseller takes title, sets the customer price, holds any inventory (irrelevant for pure SaaS but relevant for on-premise licences), and bears fulfilment risk — the reseller may be a principal (books the full customer price as revenue, with the software vendor's revenue-share as COGS) or an agent (books only the margin as revenue). The vendor's own revenue is separately analysed against the same criteria.

**Payment processing pass-through.** A SaaS vendor collects payment on behalf of the customer's own downstream users (an embedded-payments pattern) and remits to a payment processor. The vendor is typically an agent for the payment-processing component (revenue is the interchange margin / take-rate, not the gross payment volume) and a principal for the SaaS-subscription component. Two separate performance obligations, two separate gross-vs.-net conclusions.

**Third-party hosting / API pass-through.** A SaaS vendor consumes third-party APIs (AI-model APIs, mapping APIs, SMS gateways) and passes the cost to the customer, sometimes as a straight pass-through with a small markup and sometimes as a value-added metered feature. If the vendor controls the specified service (the customer contracts with the vendor, the vendor bears fulfilment risk, the vendor sets the price with markup): principal. If the vendor is arranging the customer's access to the third party (the customer's contract terms flow to the third party, the third party sets the price, the vendor merely bills through): agent — only the arranging fee is revenue.

## Sales tax, VAT, and other amounts collected on behalf of third parties

ASC 606-10-32-2A provides an accounting policy election: an entity may exclude from the transaction price all sales, use, value-added, and similar taxes collected from customers and remitted to governmental authorities. Most SaaS companies elect this policy — sales tax collected passes through the P&L as neither revenue nor expense and sits on the balance sheet as a sales-tax-payable liability until remitted.

## Contra-revenue

ASC 606 treats certain economic events as reductions of the transaction price (contra-revenue) rather than as operating expenses. The result is a lower revenue line, not a higher expense line. Correctly classifying an item as contra-revenue vs. an operating expense changes gross margin and every downstream ratio.

The primary categories:

**Discounts and price concessions.** Volume discounts, tiered discounts, early-payment discounts (though early-payment discounts are frequently modelled as financing), and negotiated concessions all reduce the transaction price. Discounts are typically allocated across performance obligations proportionally to standalone selling prices unless observable evidence supports a specific allocation (ASC 606-10-32-37 through 32-41).

**Returns and refunds.** Estimated returns are a form of variable consideration; expected returns reduce the transaction price at recognition, with a refund liability recognised on the balance sheet for the expected amount to be returned to customers.

**Customer credits and service-level-agreement credits.** SLA credits (revenue credit for uptime misses) reduce the transaction price for the period the credit is issued. Historical credit rates factor into the variable-consideration estimate applied at the start of the contract; actual credits then true up against the estimate.

**Rebates and referral fees paid to customers.** ASC 606-10-32-25 through 32-27 govern consideration paid to a customer. Payments to a customer are typically netted against revenue *unless* the payment is in exchange for a distinct good or service that the vendor receives at fair value. A referral rebate paid to a customer who refers other customers is contra-revenue; a payment to a customer for legitimate marketing services rendered by that customer at fair market rates is an operating expense.

**Channel-partner MDF and rebates.** Market Development Funds paid to a channel partner in exchange for identifiable marketing activities at fair value are operating expense (S&M). MDF paid as a general rebate or price concession is contra-revenue.

The classification decision is fact-specific and material. Investors modelling gross margin off a public filing will compute a lower gross margin if $2M of rebates hit revenue vs. if the same $2M hit S&M expense; the P&L totals differ. Auditors focus on this line. The revenue-recognition policy memo should specify which economic events the company treats as contra-revenue and why.

## A worked example — the pass-through markup question

Consider a hypothetical vendor that resells third-party AI-model API calls to its customers alongside its own SaaS platform. The customer signs a $10K/mo subscription that includes $2K/mo of "AI-model access" — a metered pass-through of third-party API cost.

Analysis (hypothetical):
- The vendor is the party the customer contracts with for AI-model access; the customer never sees the underlying provider.
- The vendor sets the retail price for the customer ($0.10 per API call vs. the underlying $0.07 the vendor pays the provider — a 43% markup).
- The vendor bears fulfilment risk — if the model is unavailable, the vendor's SLA is triggered, not the underlying provider's.
- The vendor holds the customer relationship, invoices, and collects.

Conclusion: principal for the AI-model access performance obligation. Revenue: $10K/mo (both the SaaS subscription and the AI-model access). The $1.4K/mo the vendor pays the underlying provider sits in COGS. Gross margin on the AI-model access portion is lower than on the SaaS component; a defensible gross-margin bridge (mod-102 chapter 3) should decompose this.

Now change one fact — the customer's contract explicitly states that AI-model access is "billed through at cost as a pass-through, no markup" and the vendor's SLA excludes the underlying model:
- The vendor no longer bears meaningful fulfilment risk on the AI-model access.
- The vendor has no pricing discretion — the customer pays the underlying cost, invoiced through the vendor.
- The vendor is arranging access, not providing it.

Conclusion: agent for the AI-model access performance obligation. Revenue for AI-model access is zero (or a small arranging fee if one is separately charged). The $10K/mo total invoice is $10K of subscription revenue minus the $2K/mo netted-off pass-through, so revenue is $8K/mo on the P&L. Cash-in and cash-out are unchanged.

Same customer, same cash, two revenue outcomes, driven entirely by the contract terms and the control analysis.

## Why this matters for SaaS-vs.-marketplace comps

Investor comparability across SaaS and marketplace companies breaks if gross-vs.-net is treated inconsistently. A pure SaaS trading at 8× EV / NTM revenue looks cheap relative to a marketplace trading at 12× EV / NTM revenue — until you notice the marketplace's revenue is net take-rate and its GMV is 6× that. Meritech, Bessemer, and the standard SaaS-comp dashboards (see mod-106) all report revenue as reported under GAAP, so consistent gross-vs.-net treatment across the peer set is what makes the multiples comparable. Marketplaces disclose GMV alongside revenue precisely because the revenue line alone does not tell the full story.

## Common gross-vs.-net failure modes

- **Booking gross on a clear agent transaction.** Common in early-stage marketplaces that want to report bigger "revenue." Investors and auditors both catch it; the restatement is embarrassing and re-prices any equity raised in between.
- **Booking net on a clear principal transaction.** Rarer but happens with vendors that mis-analyse pass-through markups. Result: reported revenue is too low relative to the business's actual economics.
- **Inconsistent treatment across similar contracts.** A vendor books gross on some pass-through revenue and net on others with the same facts. The policy memo does not exist or is not followed.
- **Contra-revenue misclassified as opex.** Rebates and credits hit S&M rather than reducing revenue; gross margin is overstated.
- **Sales tax treated as revenue.** The company reports tax-inclusive top line; the ASC 606-10-32-2A policy election was never made or was made and inconsistently applied.

## Summary

- Gross-vs.-net revenue is decided by the ASC 606 agent-vs.-principal analysis: does the vendor control the specified good or service before it is transferred to the customer? Principals book gross; agents book net.
- SaaS vendors are typically principals for their subscription revenue; marketplaces are typically agents for GMV-based transactions; hybrids are analysed per performance obligation.
- Contra-revenue (discounts, refunds, SLA credits, referral rebates, customer-directed payments) reduces revenue rather than adding to expense. The classification changes gross margin.
- Sales tax and similar amounts collected on behalf of governments can be excluded from the transaction price via an ASC 606 policy election, and typically are.
- The revenue-recognition policy memo documents the analysis and drives consistent treatment across contract types; auditors and investors focus on this line.

Chapter 6 turns to the decision of *when* a startup must move from cash to accrual basis, and chapter 7 walks the authoritative guidance stack that sits behind every judgement call in this module.
