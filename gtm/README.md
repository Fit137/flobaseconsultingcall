# Flobase Go-To-Market Strategy

Produced by running the `gtm-builder` skill (v3.1.0, B2B SaaS Go-To-Market Builder) against `../Flobase_Project_Brief.md`.
Run date: 2026-09-02.

Every dashboard exists as a markdown file (the readable source of truth, reviewable in a diff) and as the office file format the skill specifies. The markdown is authoritative; the XLSX and DOCX are generated from it by `../tools/md_to_xlsx.py` and `../tools/md_to_docx.py`, so edit the markdown and regenerate rather than editing the office files directly.

---

## Deliverables

| # | Dashboard | Markdown | Generated output |
|---|---|---|---|
| 0 | Inputs, assumptions and research | [00_inputs_and_assumptions.md](00_inputs_and_research/00_inputs_and_assumptions.md), [research_findings.md](00_inputs_and_research/research_findings.md) | — |
| 1 | Product Feature Matrix | [product_feature_matrix.md](01_product_feature_matrix/product_feature_matrix.md) | `product_feature_matrix.xlsx` (7 sheets) |
| 2 | Competitive Market Analysis | [competitive_analysis.md](02_competitive_analysis/competitive_analysis.md) | `competitive_analysis.xlsx` (14 sheets), `positioning_summary.docx` |
| 3 | Positioning | [positioning_statements.md](03_positioning/positioning_statements.md) | `positioning_statements.docx` |
| 4 | ICP | [icp_dashboard.md](04_icp/icp_dashboard.md) | `icp_dashboard.xlsx` |
| 5 | Buying Committee | [buying_committee.md](05_buying_committee/buying_committee.md) | `buying_committee.xlsx` |
| 6 | Value Proposition | [value_proposition.md](06_value_proposition/value_proposition.md) | `value_proposition.docx` (pillars + 9 copy drills) |
| 7 | Customer Journey Funnel | [customer_journey.md](07_customer_journey/customer_journey.md) | `customer_journey.xlsx` |
| 8 | Assets and Collaterals Library | [assets_library.md](08_assets_library/assets_library.md) | `assets_library.xlsx` (22 assets) |
| 9 | Pricing and Packaging | [pricing_dashboard.md](09_pricing/pricing_dashboard.md) | `pricing_dashboard.xlsx` |
| — | Lead Magnet Specification | [lead_magnet_spec.md](10_lead_magnet/lead_magnet_spec.md) | `lead_magnet_spec.xlsx`, `scorecard_spec.docx` |
| — | 10-Slide GTM Walkthrough Deck | [gtm_walkthrough.md](gtm_walkthrough.md) | Paste directly into Gamma AI |

## Execution Checklist

```
□ PHASE 1: Product Feature Matrix Dashboard
  ✔ 1.1 Research scope        (executed in-session, see research_findings.md)
  ✔ 1.2 Demand & Competitiveness analysis
  ✔ 1.3 Scatter plot scoring (with decimals)
  ✔ 1.4 Quadrant assignment (two tables)
  ✔ 1.5 Entry validation rules (3 violations found and corrected)
  ✔ 1.6 Demand driver identification
  ✔ 1.7 Demand driver variants (6)
□ PHASE 2: Competitive Market Analysis Dashboard
  ✔ 2.1 Research scope        (executed in-session)
  ✔ 2.2 Competitor summary table (6 competitors)
  ✔ 2.3 Core offering vectors (one-word bullets)
  ✔ 2.4 Target audience extraction
  ✔ 2.5 Value proposition extraction (3 levels)
  ✔ 2.6 Feature extraction (per company)
  ✔ 2.7 G2 reviews analysis    (executed in-session; per-theme counts left {TBD})
  ✔ 2.8 Positioning vectors (4 vectors, scored 0-10)
  ✔ 2.9 Feature consolidation (20 consolidated features)
  ✔ 2.10 Feature presence table (✓/✗)
  ✔ 2.11 Features to benefits
  ✔ 2.12 Benefits potency (1-5 stars)
  ✔ 2.13 Competitive advantage (3-4 words)
  ✔ 2.14 Competitive advantage explanation
  ✔ 2.15 Category summary (4 blocks)
  ✔ 2.16 Positioning summary (2 paragraphs)
□ PHASE 3: ✔ 3.1 Positioning statements (3)
□ PHASE 4: ✔ 4.1 Two-level ICP definition
□ PHASE 5: ✔ 5.1 Committee personas (2 ICPs x 3)  ✔ 5.2 Design partner profile
□ PHASE 6: ✔ 6.1 Brand promise  ✔ 6.2 VP pillars  ✔ 6.3 Copy drills (9)
□ PHASE 7: ✔ 7.1 Funnel mapping (7 stages)  ✔ 7.2 Key journey insights
□ PHASE 8: ✔ 8.1 Full-funnel asset mapping (3 mandated channels + 1 recommended)
□ PHASE 9: ✔ 9.1 Value metric  ✔ 9.2 Pricing tiers  ✔ 9.3 ROI anchoring
□ LEAD MAGNET: ✔ Overview  ✔ 7 questions  ✔ 3 result tiers  ✔ 4-email sequence
□ FINAL DECK: ✔ 10 slides, no tables, no em dashes, "So what" bullet on every slide
```

## What the Strategy Concludes

1. **Lead with the money loop, not the dialer.** The wallet, the marketplace, live inbound routing and CPA attribution form one closed loop no competitor holds end to end. Convoso and Ricochet360 win any argument about raw dialing throughput, so do not have that argument.
2. **Enter at 5 to 25 agent agencies.** Ricochet360's $585 monthly minimum, Convoso's ~20 seat viability floor and AgencyBloc's annual term at $109 per user leave that band structurally undefended.
3. **Publish the price.** Every recurring complaint in competitor reviews is about not knowing what something costs. Publishing pricing and the wallet platform fee is the pricing expression of the positioning, and it unblocks five marketing assets.
4. **The scorecard is the whole top of funnel.** One demand driver, reformatted per channel, returning a number the owner does not currently have.
5. **The design partner program is on the critical path for marketing, not just product.** The entire bottom of funnel depends on peer proof that does not exist yet.

## Known Gaps

Carried forward honestly rather than filled with invented numbers:

- **No business context was supplied** (team, burn, runway, channels tried). Marked `{TBD}` throughout.
- **No customer proof exists.** All nine social-proof headlines in Dashboard 6 ship with `{TBD}` slots and must not run until a real result fills them.
- **G2 per-theme review counts** are qualitative, not counted. A G2 seat would close this.
- **All pricing is proposed, not validated.** Needs willingness-to-pay testing against design partners before publication.
- **The "under 1 second" routing claim and the "#1" superiority claim** both need substantiation before they appear in paid channels.
- **The competitor set is an assumption.** Replace any name and re-run Phases 1 and 2.

## Regenerating the Office Files

```bash
python3 tools/md_to_xlsx.py gtm/09_pricing/pricing_dashboard.md gtm/09_pricing/pricing_dashboard.xlsx
python3 tools/md_to_docx.py gtm/03_positioning/positioning_statements.md gtm/03_positioning/positioning_statements.docx
```

Requires `openpyxl` and `python-docx`.
