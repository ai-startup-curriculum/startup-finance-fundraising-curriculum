# Three-Statement Financials on Cash and Accrual Basis

## Why this matters

Every substantive question a founder or CFO answers about a startup — *how much runway do we have, what did we actually earn last quarter, can we make payroll in March* — is answered by pointing at one of three numbers on one of three statements. A "financials pack" is not a spreadsheet; it is the P&L, the balance sheet, and the cash-flow statement, produced together, reconciled to each other, and produced on a chosen accounting basis (cash or accrual).

The founder-first instinct — "just look at the bank balance" — is a cash-basis P&L with no balance sheet and no cash-flow statement. It is directionally right at IDEA-stage, quietly wrong at PRE-SEED (once the first customer prepays a year), and structurally wrong from SEED forward. Every investor pack from Series-A on is accrual-basis. If you cannot read and produce the three statements on both bases, you cannot answer the question "what is our revenue this quarter" in a way any two people will agree on.

## The three statements — a working definition

The three statements are the standard GAAP presentation of a company's financial position and performance across a period.

**Profit & loss statement (P&L / income statement)** — for a period (a month, quarter, or year):

```
Revenue
  − Cost of revenue                         (COGS)
= Gross profit
  − Sales & marketing
  − Research & development
  − General & administrative
= Operating income (loss)
  ± Interest / other income / expense
  − Taxes
= Net income (loss)
```

The P&L answers *did we make money this period?*

**Balance sheet** — a snapshot at a point in time (end of month, quarter, year). The accounting identity:

```
Assets = Liabilities + Stockholders' equity
```

For a startup, the recurring line items are typically:

- Assets: cash & cash equivalents, accounts receivable (AR), prepaid expenses, property & equipment (net of depreciation), intangibles, deferred contract costs
- Liabilities: accounts payable (AP), accrued liabilities, deferred revenue (contract liability), debt, other long-term obligations
- Stockholders' equity: common stock, preferred stock (by series), additional paid-in capital (APIC), accumulated deficit

The balance sheet answers *what do we own and what do we owe, right now?*

**Cash-flow statement** — for a period. Three sections:

```
Cash from operating activities        (CFO)
  Net income
  + Non-cash items (depreciation, stock-based comp)
  ± Changes in working capital
    - increase in AR (customer hasn't paid yet)
    + increase in deferred revenue (customer prepaid)
    + increase in AP (we haven't paid vendors yet)
= Net cash from operations

Cash from investing activities        (CFI)
  ± Capex, acquisitions, investments in securities

Cash from financing activities        (CFF)
  ± Equity issuances, debt draws / repayments, dividends

= Net change in cash
+ Beginning cash
= Ending cash                          (must tie to balance-sheet cash line)
```

The cash-flow statement answers *where did the cash actually go?* It is the arbitration layer between the P&L (which is on accrual basis in almost all published financials) and the balance sheet (which is a snapshot). The three statements are not independent — the cash line on the balance sheet must match the ending-cash line on the cash-flow statement, and net income on the P&L must roll into retained earnings / accumulated deficit on the balance sheet.

Cash from operations is typically presented using the **indirect method** (start with net income, add back non-cash items, adjust for working-capital changes). The **direct method** — sum the actual cash receipts and payments by category — is permitted under US GAAP and IFRS but rarely used in practice because indirect is easier to reconcile back to net income. FASB ASC 230 governs the cash-flow statement.

## Cash basis vs. accrual basis — the mechanical difference

Two different clocks decide *when* revenue and expenses hit the P&L.

**Cash basis.** Revenue is recognised when cash is received. Expense is recognised when cash is paid. There is no AR line, no AP line, no deferred revenue, no matching principle. The P&L collapses toward the checkbook — what came in, what went out. Cash-basis accounting is permitted for US federal income-tax purposes for certain small taxpayers under the Internal Revenue Code and is described in IRS Publication 538, *Accounting Periods and Methods*.

**Accrual basis.** Revenue is recognised when *earned* (a performance obligation is satisfied under ASC 606). Expense is recognised when *incurred* (the matching principle — the cost of producing a period's revenue is booked in that period). Accrual introduces four line items that never appear on a cash-basis P&L: accounts receivable (revenue earned, cash not yet received), accounts payable (expense incurred, cash not yet paid), deferred revenue (cash received, revenue not yet earned), and prepaid expenses (cash paid, expense not yet incurred).

Accrual is US GAAP. Every audited financial statement, every S-1, every institutional investor pack is accrual. The FASB's Conceptual Framework and the specific accounting standards (including ASC 606 for revenue) presume accrual.

## Why a cash-basis SaaS company's headline revenue can differ meaningfully from its accrual-basis revenue

Consider a hypothetical annual-prepay SaaS company. In January it signs and collects $1.2M on a single annual contract that runs 12 months at $100K per month of service delivered. Continue for illustration only.

- On cash basis, January revenue is **$1.2M**. February revenue is $0.
- On accrual basis (ASC 606, straight-line ratable delivery), January revenue is **$100K**. February revenue is $100K. So is every month through December.
- The **$1.1M gap** on the January P&L is the deferred-revenue liability on the January 31 balance sheet — cash the company holds but has not yet earned.

Stack this pattern across a year of contracts and the effect grows. A company with $5M of ARR (contracts in force) that grew fast in the first half of the year, with heavy annual-prepay concentration, can report cash-basis "revenue" for the year that is meaningfully higher or lower than its accrual-basis revenue — higher if bookings pulled forward, lower if bookings back-loaded. The direction depends on the shape of the year; the magnitude depends on annual-prepay concentration. It is not unusual for the two bases to diverge by a material fraction of headline revenue in a growing SaaS company.

The corollary — the failure mode a founder falls into — is *quoting cash-basis revenue as "revenue"* to an investor who assumes accrual. The investor will build a multiple off the number, discover the divergence in diligence, and re-price. The CFO's job at Series-A onwards is that the number on the deck matches the number in the accrual-basis financials, and that both match the number in the model.

## How the three statements interlock

The three statements are one integrated model of the business. The links you must be able to trace:

1. **Net income → retained earnings.** Net income (or loss) for the period flows from the P&L into the "accumulated deficit" (or retained earnings) line on the balance sheet.
2. **Balance-sheet cash → cash-flow ending cash.** The cash line on the balance sheet must equal the ending-cash line on the cash-flow statement.
3. **Working-capital deltas → cash from operations.** Changes in AR, AP, deferred revenue, prepaid expenses, and accrued liabilities on the balance sheet are the adjustments in the operating-activities section of the cash-flow statement.
4. **Capex → PP&E.** Investing-activity cash outflows for property and equipment build the gross PP&E line on the balance sheet.
5. **Financing activities → equity and debt.** Equity issuances build common / preferred stock and APIC; debt draws build the debt line; the movements appear as cash inflows in the financing section.

If any of these links breaks — retained earnings drifts from cumulative net income, balance-sheet cash disagrees with ending cash, working-capital deltas don't match the cash-flow adjustment — the model is broken. This is the "the balance sheet doesn't balance" moment, and it is the single most common failure in a founder-authored financial model. Chapter 3 of mod-103 walks the failure modes in detail; this chapter's job is to install the mental model.

## When cash basis is *fine* and when it isn't

Cash basis is fine at IDEA-stage and often at PRE-SEED — no or few customers, no or trivial deferred revenue, no auditor asking questions. You can run the bookkeeping in QuickBooks Online (QBO) or Xero on cash basis, produce a cash-basis P&L for internal use, and pay estimated taxes on cash basis if you qualify under IRC §448 (see chapter 6).

Cash basis stops being fine as soon as any of the following is true:

- The company has annual-prepay contracts (or any material timing mismatch between cash and service delivery)
- The company is preparing for a priced round where the investor pack is expected to be accrual
- The company is preparing for its first outsourced audit (see mod-111)
- The company has crossed the IRC §448 gross-receipts threshold and is required to accrual for tax purposes <!-- needs-research: cite current inflation-adjusted §448(c) threshold and effective year -->
- The company has a board or lead investor requesting accrual-basis reporting

The mechanics of the cash-to-accrual transition — the memo, the retained-earnings adjustment, the two-year restatement, the auditor letter — are chapter 6. This chapter is only about the definitions and the mental model.

## Summary

- The three statements are the P&L (period), the balance sheet (snapshot), and the cash-flow statement (period). They are one model, reconciled to each other.
- Cash basis recognises revenue and expense when cash moves. Accrual recognises revenue when *earned* and expense when *incurred*, introducing AR, AP, deferred revenue, and prepaid expenses.
- Accrual is US GAAP and the assumed basis for every institutional investor pack.
- A SaaS company with annual-prepay concentration can report headline revenue that differs meaningfully between the two bases; the delta lives on the balance sheet as deferred revenue.
- The three statements interlock through five specific links; a break in any of them is a broken model.

The rest of this module is about the mechanics on the accrual side — ASC 606 (chapter 2), bookings/billings/revenue/cash (chapter 3), deferred revenue (chapter 4), gross vs. net (chapter 5) — and about the decision to transition (chapter 6) and the guidance stack behind it (chapter 7).
