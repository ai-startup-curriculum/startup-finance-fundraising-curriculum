# Exercise 05 — Data Room Architecture Drill

**Estimated time:** ~4-6 hours (setting up the folder architecture and populating it with representative or placeholder artifacts).
**Prerequisites:** Chapter 5 (seven canonical sections, read order, access-tiering), plus prior familiarity with the cap table (mod-104), the financial model (mod-103), and the accounting stack (mod-101).

## Problem statement

Construct a full data-room folder architecture for a Series-A B2B SaaS raise. Populate it with either real artifacts (from a hypothetical company you're building for the module) or placeholder artifacts with clear "what belongs here" descriptions. Layer on a diligence-request checklist, an access-tier map, and an investor-facing README describing the recommended read order. This is what a CFO hands to counsel and to the fund's diligence lead in the first week of a Series-A process.

The point of the exercise is to install the specific data-room *architecture* — the seven canonical sections, the sub-folder structure within each, the audit-trail and access-tiering mechanics — so that when a real raise starts, the CFO is not building the room from scratch under deadline pressure.

## Scenario — build your own

Use the target company from exercise 01 / 02 / 04, or build a fresh one meeting this shape:

- Series-A B2B SaaS.
- Current ARR $1.5M-$3M with 15-30 team members.
- Delaware C-corp, 3-5 years old.
- Prior seed round (priced or SAFEs — some conversion mechanics live here).
- 10-40 customers on annual or multi-year contracts, at least one enterprise anchor deal.
- SOC2 in progress or complete; standard security posture.

Document the company profile on a "company context" tab or as a data-room README section.

## Requirements

### The folder architecture

Structured per chapter 5's seven canonical sections. For each section, produce sub-folders and a `README.md` at the section level describing what belongs and (for placeholders) what the file would contain.

**Section 1 — Corporate documents.** Certificate of incorporation, bylaws, board consents and minutes, stockholder consents, prior-round financing docs, IP-assignment agreements, employment agreements for key hires, contractor agreements, foreign-subsidiary docs (if any), material contracts (top vendor contracts, key strategic partnerships).

**Section 2 — Financials.** Historical financials (last 24-36 months of monthly P&L, balance sheet, cash-flow statement), forecast model (from exercise 01 sizing), reconciliation of ARR / MRR to GAAP revenue (mod-101 chapter 3), gross-margin bridge (mod-102 chapter 3), audit files (if any), tax returns (last 3 years), R&D tax-credit filings (if any).

**Section 3 — Cap table and equity.** Current cap table (mod-104), option-pool documents, RSU documents (if any), 409A valuation report (most recent), option-grant history, prior-round conversion mechanics (SAFEs / notes from mod-105), pool-shuffle math for the current round.

**Section 4 — Customer and revenue.** Top-10 customer contracts, customer list (name, ACV, contract term, renewal date, expansion history), cohort table (mod-102 chapter 4), NRR / GRR analysis, customer-concentration analysis, churned-customer log, sales-pipeline snapshot, sales-cycle-length analysis, win-rate data by segment.

**Section 5 — Product and IP.** Product roadmap (12-18 months forward), technical architecture summary, IP assignments (from section 1 cross-referenced), open-source-license inventory, security-and-compliance documentation (SOC2 report or in-progress evidence, privacy documentation, DPAs), integration inventory.

**Section 6 — Team and organisational.** Org chart, hiring plan (12-18 months forward — from exercise 01), key-hire bios and references, compensation philosophy, benefits summary, DEI policy (if any), employee-satisfaction data (if any), turnover data.

**Section 7 — Legal and other.** Litigation log (open and closed), regulatory correspondence, insurance policies, real-estate leases, references list (customers, employees, prior investors), any specific consent-or-approval items the round will need.

### The diligence-request checklist

A single tracker (spreadsheet or Markdown table) with one row per anticipated diligence request. Columns:

- Request category (which of the seven sections).
- Specific artifact requested.
- Whether the artifact is already in the data room (yes / no / placeholder).
- Data-room location (folder path).
- Access tier required (see below).
- Owner (who prepares / provides).
- Estimated preparation time (if not yet ready).
- Status (Ready / In progress / Blocked / Not applicable).

The checklist should anticipate at least 30-50 specific diligence requests. Use chapter 5's chapter and the practitioner references (Feld & Mendelson's *Venture Deals* diligence chapters, standard VC-diligence templates from Sequoia / a16z / etc.) as sources.

### The access-tier map

A one-page document mapping each folder and file to an access tier. Chapter 5's staged-access pattern suggests:

- **Tier 1 (immediate share on partner interest, before term sheet).** Deck, high-level financials, high-level cap table, product overview, team, market summary, references list.
- **Tier 2 (share after partner meeting or verbal indication of interest).** Detailed financials with monthly breakouts, detailed cap table with individual holdings, cohort table, top-N customer list without contracts, product roadmap, hiring plan, standard corporate documents.
- **Tier 3 (share after term sheet or in deep-diligence).** Individual customer contracts, individual employment agreements, litigation logs, sensitive IP, security audit reports, tax returns, board consent history.

Map every folder / file to a specific tier. If a document has multiple versions (e.g., a redacted vs. unredacted customer contract), map each version to its tier.

### The investor-facing README

A single Markdown README at the data-room root, ~1 page, containing:

- One-paragraph company summary.
- The recommended read order (chapter 5 section — the specific sequence a diligence associate would benefit from reading in).
- Naming conventions used in the room.
- Points of contact for follow-up questions (CFO for financial / cap-table questions, CEO for team / vision, counsel for legal).
- Update / version-control conventions (e.g., "financial-model has month-of-update tag in filename").
- Access-tier disclosure — what the fund is granted at each stage of the process.
- Confidentiality note referencing the data-room platform's audit trail.

### The audit-trail plan

A half-page plan describing:

- Which data-room platform is being used (chapter 5 discusses DocSend Spaces, Google Drive with granular sharing, dedicated tools like Digify / DealRoom / Datasite).
- What the audit trail captures (per-user views, per-file views, download log, forwarding log).
- Weekly review cadence — which team member reviews the audit trail weekly and looks for signal.
- Signal-reading rules — what a spike in views of the cap-table file (or a specific contract) might mean and how to interpret it.

## Starter guidance

- **Build the empty folder structure first.** Create all seven sections and their sub-folders before placing any files. Naming discipline matters — use consistent conventions (e.g., `01-corporate-docs/`, `02-financials/`).
- **Use placeholders liberally.** Real customer contracts and 409A reports are not the point — the folder architecture and the `README.md` describing what belongs is. A placeholder `.md` file per artifact with a "this-file-would-contain" description is fine.
- **Cross-reference between sections.** IP assignments live in section 1 (corporate); they are referenced from section 5 (product / IP). Cap table math (section 3) references the SAFEs from section 1 (financing docs). Make the cross-references explicit.
- **Do not over-share in tier 1.** Chapter 5's staging is deliberate — the point is to give diligence partners just enough to advance the conversation without exposing sensitive detail before there is a real interest signal.
- **Version-control convention.** Use a `-vYYYYMMDD` or `-vX.Y` suffix on files that get updated during the raise. The current version is always the highest-versioned; older versions live in an `archive/` sub-folder.
- **The diligence-request checklist is a live document.** It gets updated as new requests come in during the raise. Structure it so it can absorb the additions.
- **Access-tier assignments should be defensible.** A file assigned to tier 1 that a peer CFO would say "why is that in tier 1?" is a signal you have not thought about the sensitivity carefully. Err toward tighter tiers early in the process.
- **Include one or two artifacts you would not include** and note why (e.g., legal-hold documents from a resolved dispute, internal HR complaints — some things are diligence-relevant only under specific circumstances and require explicit lead-fund pre-agreement to share).

## Acceptance criteria

- **Seven canonical sections** each with sub-folders and a section-level `README.md`.
- **At least 30-50 placeholder artifacts** across the sections, covering the standard diligence requests.
- **A diligence-request checklist** with 30-50 rows, each mapped to a specific folder and access tier.
- **A full access-tier map** — every folder and file mapped to a specific tier with the tier-1 / tier-2 / tier-3 pattern.
- **An investor-facing README** at the data-room root covering the required sections.
- **An audit-trail plan** covering platform choice, capture, and review cadence.
- **Cross-references between sections** explicit — IP assignments cross-referenced between corporate and product/IP, financing docs cross-referenced between corporate and cap table, etc.
- **Version-control convention documented** and applied to the placeholder artifacts.
- **The read order is specific** — a diligence associate could follow it start to finish and know exactly which file to open next.
- **The data room is stage-appropriate for Series-A** — chapter 9's Series-A specifics (formal room, cohort data, monthly financials, top-10 customer contracts) are represented.

## Deliverables

- The data-room folder tree (as a directory of files, or as a Google Drive / Notion / dedicated-tool link).
- The diligence-request checklist (.xlsx, Google Sheets, or a Markdown table).
- The access-tier map (Markdown or spreadsheet).
- The investor-facing README (Markdown, ~1 page).
- The audit-trail plan (Markdown, half page).

## Extensions (optional)

- **Build a Series-B version.** Layer on the Series-B-specific artifacts (chapter 9): QoE-ready books, sales-productivity pack (rep-level ramp curves, quota attainment), customer-segmentation pack, last 6-12 board packs. Note which sections expand materially.
- **Run a mock diligence request set** — have a peer generate 15-20 diligence questions typical of a Series-A associate, and produce responses that either point to a specific file in the room or note that the artifact needs to be built. Log any gaps discovered.
- **Add a redaction workflow** for tier-2 artifacts that need customer-name or contract-detail redaction. Document the redaction convention and produce redacted vs. unredacted copies of at least two artifacts.
- **Data-room security walk-through.** Document the specific access-management flow (invitation with expiry, single-sign-on where the platform supports it, watermarking on downloads, revocation).
- **Post-diligence archival plan.** After the round closes, what happens to the data room? Which artifacts move to a post-close ongoing-investor-updates cadence, which get archived, and which retain shared access for the incoming investor's ongoing reporting rights.
