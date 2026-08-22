# ASC 606 — The Five-Step Revenue Recognition Model for SaaS

## Why this matters

ASC 606, *Revenue from Contracts with Customers*, is the single accounting standard that decides *when* a SaaS startup's revenue hits the P&L. Before ASC 606 (issued 2014, effective for public companies in periods beginning after 15 December 2017 and private companies one year later), US GAAP revenue recognition was scattered across dozens of industry-specific standards under ASC 605 and SEC SAB 101/104. ASC 606 replaced them with one principles-based model — jointly converged with IFRS 15 by the FASB and the IASB — that applies to essentially every customer contract in every industry.

For a SaaS founder or CFO, ASC 606 is the reason an annual-prepaid $1.2M contract books $100K of revenue in each of twelve months, not $1.2M in the month of invoice. It is the reason implementation fees may need to be deferred and amortised over the expected customer life. It is the reason usage-based components have to be estimated and constrained. And it is the reason "we invoiced $X this month" is not a revenue statement.

## The scope of ASC 606

ASC 606 applies to all contracts with customers except leases (ASC 842), insurance contracts (ASC 944), financial instruments (ASC 815 et al.), guarantees (ASC 460), and non-monetary exchanges between entities in the same line of business. Every SaaS subscription, every on-premise software licence, every professional-services engagement, every marketplace commission, and every advertising placement falls inside the scope.

The core principle in ASC 606-10-05-3: *an entity recognises revenue to depict the transfer of promised goods or services to customers in an amount that reflects the consideration to which the entity expects to be entitled in exchange for those goods or services.* The five-step model operationalises that principle.

## Step 1 — Identify the contract with a customer (ASC 606-10-25-1 to 25-8)

A contract exists when all of these are true:

1. The parties have approved the contract (in writing, orally, or implicit by course of dealing).
2. Each party's rights regarding the goods or services are identifiable.
3. The payment terms are identifiable.
4. The contract has commercial substance.
5. Collection of the consideration is *probable* (a higher bar than "possible" — in practice, look at the customer's creditworthiness and payment history).

Contracts can be **combined** if they are entered into at or near the same time with the same customer and are economically linked. Contracts can be **modified**; modifications are treated as either a separate new contract, a prospective adjustment (if the remaining goods/services are distinct), or a cumulative catch-up (if the remaining goods/services are not distinct). Termination-for-convenience clauses reduce the enforceable contract term to the notice period.

For a SaaS startup, the practical questions in step 1 are: *do we have a signed order form or MSA, is the customer's payment probable, and what is the enforceable term* (annual with a 30-day out is a one-year contract; annual with a 30-day out plus a substantive termination penalty may be closer to a full-year contract).

## Step 2 — Identify the performance obligations in the contract (ASC 606-10-25-14 to 25-22)

A performance obligation is a promise to transfer a **distinct** good or service (or a series of substantially the same goods/services that are transferred in the same pattern). "Distinct" requires two things:

1. The good/service is *capable of being distinct* — the customer can benefit from it on its own or with other resources readily available.
2. The good/service is *distinct within the context of the contract* — it is separately identifiable from other promises.

For a typical SaaS contract, the analysis usually resolves as follows:

- **The SaaS subscription itself** is a single performance obligation — a series of substantially the same daily service delivered over the contract term. Ratable recognition over the term is standard.
- **Implementation, onboarding, or professional-services fees** may or may not be a separate performance obligation. If the implementation is substantive, distinct, and can be performed by other vendors, it is usually a separate PO recognised as the service is delivered. If the implementation is inseparable from the SaaS subscription (a customer cannot use the SaaS without it and only the vendor can perform it), the fee is combined with the subscription PO and deferred and amortised over the expected customer life.
- **Training** is often distinct and recognised as delivered.
- **Add-on modules or usage-based components** are usually separate performance obligations, with the usage-based portion recognised as consumed.

The judgement call — is implementation distinct or not — is the most common ASC 606 policy decision a SaaS company makes. It should be documented in a written revenue-recognition policy and applied consistently.

## Step 3 — Determine the transaction price (ASC 606-10-32-2 to 32-27)

The transaction price is the amount of consideration the entity expects to be entitled to in exchange for satisfying the performance obligations. It excludes amounts collected on behalf of third parties (sales tax, VAT — see chapter 5's discussion of agent vs. principal). It includes:

- **Fixed consideration** — the stated contract price.
- **Variable consideration** — usage-based fees, tiered discounts, service-level-agreement (SLA) credits, refunds, rebates, performance bonuses. Variable consideration is estimated using either the *expected-value method* (probability-weighted average of possible outcomes) or the *most-likely-amount method*, whichever better predicts the amount the entity will be entitled to.
- **Constraint on variable consideration** — the entity may only include variable consideration in the transaction price to the extent it is *probable* that a significant reversal will not occur when the uncertainty is resolved. For a new SaaS product with no usage history, this means variable-usage estimates are often heavily constrained.
- **Significant financing components** — if the timing of payment differs materially from the timing of delivery (typically more than one year), the transaction price is adjusted to reflect the time value of money. Annual-prepay SaaS is customarily below the one-year threshold and no financing adjustment is made; multi-year prepaid contracts may require the adjustment.
- **Non-cash consideration** measured at fair value.
- **Consideration payable to the customer** — payments a vendor makes to a customer (referral fees, MDF, rebates) are typically netted against revenue as contra-revenue, unless in exchange for a distinct good or service the vendor receives at fair value.

For a SaaS startup, the practical work in step 3 is decomposing the transaction price into fixed, variable, and contra-revenue components and applying the constraint to the variable portion.

## Step 4 — Allocate the transaction price to the performance obligations (ASC 606-10-32-28 to 32-41)

If a contract has multiple performance obligations, the transaction price is allocated to each PO based on **standalone selling price** (SSP). SSP is the price at which the entity would sell the good/service separately to a similar customer.

If SSP is directly observable — the entity actually sells the component separately at a listed price — that observable price is used. If SSP is not directly observable, it is estimated using an adjusted-market-assessment approach, an expected-cost-plus-margin approach, or a residual approach (only permitted in specific circumstances).

**Discounts** are typically allocated proportionally across performance obligations based on their relative SSP, unless observable evidence supports a specific allocation.

For a SaaS contract with a subscription PO and a distinct implementation PO, the practical work in step 4 is: compute SSP for each, allocate the transaction price proportionally, and be prepared to defend the SSP estimate in an audit.

## Step 5 — Recognise revenue when (or as) the entity satisfies a performance obligation (ASC 606-10-25-23 to 25-37)

Revenue is recognised when the entity transfers control of the promised good or service to the customer. Two patterns:

**Over-time recognition** — used when any of the following is true:
1. The customer simultaneously receives and consumes the benefits as the entity performs (SaaS subscription — the customer uses the service every day of the contract term).
2. The entity's performance creates or enhances an asset the customer controls.
3. The entity's performance does not create an asset with alternative use, and the entity has an enforceable right to payment for performance completed to date.

When over-time recognition applies, the entity measures progress using either an output method (units delivered, milestones achieved) or an input method (costs incurred, hours worked, time elapsed). For a subscription SaaS, **straight-line time-elapsed recognition** is the default — the value delivered is essentially uniform per day of the subscription.

**Point-in-time recognition** — used when the criteria for over-time are not met. Revenue is recognised at the moment control transfers. For a perpetual on-premise software licence, this is typically at delivery. For a distinct implementation deliverable that ships as a completed artefact, this is typically at customer acceptance.

## Working through a SaaS example — end-to-end

Consider a hypothetical customer signing on January 1:

- Annual SaaS subscription, $120,000 invoiced upfront
- $30,000 implementation fee, invoiced at signature, four-week engagement
- $10,000 training package, invoiced at signature, delivered in month 1
- 10% discount off list price for signing an annual (vs. monthly) contract
- SLA credit: if uptime falls below 99.9% in a month, credit up to $2,000 that month

Step 1 — Contract exists. Signed order form, credit review passed, one-year term with no termination-for-convenience clause. Enforceable term: 12 months.

Step 2 — Performance obligations. Analysis (hypothetical; the exact answer depends on the specific facts and the company's revenue-recognition policy):
- Subscription: 1 PO (series of substantially the same daily service, over-time).
- Implementation: assumed distinct (documented that other vendors can perform, customer has demonstrated ability to use SaaS on a peer without our implementation). 1 PO, recognised as delivered (four weeks, roughly ratable).
- Training: distinct. 1 PO, recognised in month 1 as delivered.

Step 3 — Transaction price. Fixed consideration: $160,000 ($120K + $30K + $10K). SLA credits are variable consideration; using expected value based on the vendor's historical uptime, the estimated annual credit exposure is (hypothetically) $500, constrained down to $500 (fully expected to be exposed). Transaction price: $159,500.

Step 4 — Allocation. SSP: assume list-price subscription is $133,333 (the 10% discount is applied to a list price of $148,148), implementation SSP is $30,000, training SSP is $10,000. Proportional allocation of the $159,500 transaction price across the three POs' SSPs (roughly $173,148 total SSP): subscription ~$122,721, implementation ~$27,614, training ~$9,205. (In practice, if the discount is contractually tied to the subscription — which is the more common facts — allocation would put the discount on the subscription only.)

Step 5 — Recognition. Assuming a July close on the illustrative allocation:
- Subscription: recognise $122,721 / 12 = $10,227/mo, straight-line, months 1-12.
- Implementation: recognise $27,614 over the four-week engagement, roughly $6,904/week.
- Training: recognise $9,205 in month 1.

January P&L revenue: $10,227 (subscription) + $27,614 (implementation, all delivered in Jan) + $9,205 (training) = $47,046. Cash collected in January: $160,000. Deferred revenue on the January 31 balance sheet: $160,000 − $47,046 = $112,954. That deferred revenue liability unwinds $10,227/mo from February through December. Chapter 4 walks the deferred-revenue mechanics in detail.

## Why annual prepay books monthly, not on invoice — the one-sentence answer

Annual prepay is a step-3 cash event (transaction price received) not a step-5 recognition event (performance obligation satisfied). The customer is paying for twelve months of service. Under ASC 606, revenue is recognised as the service is delivered, which is over-time on a straight-line basis for a subscription. Invoice date and cash-collection date are irrelevant to the P&L; they are balance-sheet and cash-flow-statement events.

## Common step-by-step failure modes

- **Skipping step 1.** Recognising revenue on a signed LOI without a substantive contract, or on a contract where collectibility is not probable. Both violate step 1 and lead to reversal.
- **Bundling everything into one PO.** A single-PO answer is often incorrect for a contract with distinct implementation or training and understates step-2 rigour. If challenged in audit, the vendor cannot show the SSP analysis.
- **Ignoring variable consideration.** Booking the stated contract price with no consideration of usage tiers, SLA credits, or performance bonuses. The transaction price is wrong, so the recognition is wrong.
- **Recognising on invoice date.** The single most common founder error. Invoice is a billings event, not a revenue event. Chapter 3 walks this distinction in detail.
- **Not documenting the policy.** ASC 606 permits judgement; the price of judgement is a written revenue-recognition policy that the vendor consistently applies. In audit, the first document requested is the revenue-recognition policy memo.

## Summary

- ASC 606 replaced ~all pre-2018 US GAAP revenue standards with one principles-based five-step model, converged with IFRS 15.
- The five steps: identify the contract, identify the performance obligations, determine the transaction price, allocate the price to obligations, recognise revenue as obligations are satisfied.
- For SaaS, subscription is typically a single over-time PO with straight-line recognition. Implementation, training, and add-ons may be separate POs.
- Annual-prepay contracts book revenue monthly because step 5 recognises as the service is delivered, not as cash is collected.
- The judgement calls in steps 2 and 3 (distinct PO test, variable-consideration constraint) should be documented in a written revenue-recognition policy applied consistently.

Chapter 3 walks the four SaaS numbers — bookings, billings, revenue, cash — that fall out of the ASC 606 framework and are consistently conflated by founders. Chapter 4 walks the deferred-revenue liability that carries the difference between billings and revenue.
