# GTM Discovery Inputs and Assumptions — Flobase

Skill: `gtm-builder` v3.1.0 (B2B SaaS Go-To-Market Builder)
Run date: 2026-09-02
Source of truth for product facts: `Flobase_Project_Brief.md` (flobase.tech homepage content as published)

---

## 1. Project Information

| Field | Value | Source |
|---|---|---|
| Project name | Flobase | Brief |
| Project website | flobase.tech | Brief |
| Category name | Insurance Agency Operating System (life insurance agency CRM + lead acquisition + dialer) | Derived |
| Niche focus | US life insurance agency owners running remote telesales teams with a downline hierarchy (final expense, mortgage protection, term, IUL) | Derived from brief language: "agency owners", "downline", "sub-agencies", "closers", "100k AP in a single month" |
| One-liner | "Your entire agency in one tab. Take live inbound calls, buy and dial leads, drip SMS, submit sales, and track your book, all in one place." | Brief (verbatim site copy) |
| Positioning claim on site | "The #1 All-In-One CRM for Life Insurance Agents", "Built by closers, for closers." | Brief (verbatim site copy) |

## 2. Competitor Set (6)

The brief does not name competitors, so the set below was selected from market research and is an **assumption**. It is built to cover the four budget lines a Flobase buyer already pays for, because Flobase's core claim is stack consolidation. Swap any row and re-run Phases 1 and 2 if the real evaluation set differs.

| # | Competitor | Website | Bucket it represents | Why it is in the set |
|---|---|---|---|---|
| 1 | Radius (formerly Radiusbob) | radiusbob.com | Insurance-specific CRM + dialer | The default CRM for independent life agents; direct feature overlap on CRM, telephony, lead import |
| 2 | AgencyBloc AMS+ | agencybloc.com | Agency management system for life, health and senior | Explicitly sells to IMO/FMO and call centers; owns the book-of-business and commission budget line |
| 3 | Convoso | convoso.com | Outbound contact-center dialer | 47% of its reviewers are in insurance; owns the dialer budget line for high-volume telesales rooms |
| 4 | Ricochet360 | ricochet360.com | Speed-to-lead dialer + CRM + marketing automation | 75% of its reviewers are insurance; the closest "all-in-one dialer + CRM" pitch |
| 5 | Agent CRM | agent-crm.com | All-in-one marketing CRM built for insurance agents (HighLevel-based) | Direct all-in-one competitor at a low price point with an insurance-agent community motion |
| 6 | EverQuote (Agent / LCS) | everquote.com | Lead and live-transfer marketplace | Owns the lead acquisition budget line that Flobase's marketplace and inbound routing target |

Adjacent but excluded, with reasons: GoHighLevel (covered through Agent CRM, which is the insurance-packaged form of it), InsuredMine and EZLynx (P&C-weighted), Sunfire / Integrity LeadCENTER (Medicare-weighted), Salesforce FSC and HubSpot (enterprise, not the SMB agency-owner budget).

## 3. Product Features List (12, taken verbatim in substance from the brief)

| # | Feature | Brief wording |
|---|---|---|
| F1 | Live inbound call routing | Consumer-initiated calls from insurance ads routed to the next available closer in under 1 second, exclusive to one agent per interaction |
| F2 | In-platform lead marketplace | Agents buy exclusive leads inside the platform |
| F3 | Agency wallet | Owners fund a central wallet and allocate budget to agents; real-time spend, cost-per-call and balance; "no hidden fees" |
| F4 | Zero-delay dialer | Outbound dialing with no connect delay |
| F5 | Drip SMS campaigns | SMS nurture sequences for bought leads |
| F6 | Book of business | Centralized searchable record of every submitted sale, policy and client |
| F7 | Team performance dashboard | Spend, CPA, AP, close rate and ROI at agent and campaign level |
| F8 | Production heatmap | Visualization of performance trends |
| F9 | Team and hierarchy management | Single table for agents, sub-agencies, admins, invites, plus a live org graph of branch structure |
| F10 | Onboarding tracker | Training course to licensing exam to contracting, plus bookable onboarding-call slots |
| F11 | Unlimited seats and role-based access | Unlimited seats, role-based access control across the hierarchy |
| F12 | Referral links for downline recruitment | Referral links to support downline recruiting |

## 4. Business Context

Not supplied in the brief. Treated as `{TBD}` throughout and never invented.

| Field | Status |
|---|---|
| Current team structure | {TBD} |
| Monthly burn rate | {TBD} |
| Runway remaining | {TBD} |
| Channels tried and results | {TBD} |
| Current customer count / AP under management | {TBD} |
| Current pricing | {TBD} — the homepage publishes no pricing, so Phase 9 designs pricing rather than documenting it |

## 5. Assumptions Register

Every assumption below changes the output if it is wrong. Correct any of these and re-run the phase named.

| # | Assumption | Affects | Confidence |
|---|---|---|---|
| A1 | The competitor set in section 2 is the real evaluation set | Phases 1, 2, 3 | Medium |
| A2 | Flobase's economic buyer is the agency owner, not the individual producer, because the wallet, hierarchy and ROI reporting are owner-facing | Phases 4, 5, 9 | High |
| A3 | The niche is life telesales (final expense weighted), not P&C or Medicare | All phases | High |
| A4 | Every module badged "Live" on the site is genuinely shipped | Phases 1, 2, 8 | High (site states it) |
| A5 | Pricing is unpublished because it is still being set, so Phase 9 is a design, not a description | Phase 9 | Medium |
| A6 | The lead marketplace and inbound routing carry real per-unit cost to Flobase, so the wallet is a pass-through plus platform fee, not pure margin | Phase 9 | Medium |
| A7 | The brief captures the full public feature set; no unreleased roadmap is included | Phases 1, 2 | High |

## 6. Deviations from the Skill Script

| Skill instruction | What was done | Why |
|---|---|---|
| Steps 1.1, 2.1, 2.7 are "user executes externally" | Executed in-session via web research; findings and sources are in `research_findings.md` | The run was requested end to end; blocking on external research would have delivered nothing |
| Step 2.7 asks for exact G2 review counts per theme | Themes are captured with qualitative frequency labels, not counts | Per-review counts are not retrievable without a G2 seat; counts are marked `{TBD}` rather than invented |
| Skill assumes 5 competitors | 6 used | The category splits across four budget lines, which needs six names to cover |
| Phase 8 mandates LinkedIn Outreach, Cold Email and LinkedIn Ads | Delivered as specified, plus a channel-fit note | This ICP concentrates in Facebook groups, YouTube and IMO communities, so the mandated channels are delivered but the note flags where budget should actually land |
