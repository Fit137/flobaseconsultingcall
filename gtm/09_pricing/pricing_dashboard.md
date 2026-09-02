# Dashboard 9 — Pricing and Packaging (Flobase)

Skill steps 9.1 through 9.3.

**Status of this dashboard.** flobase.tech publishes no pricing, so this is a pricing *design*, not a description of what exists. Every price below is a proposal that needs willingness-to-pay validation against at least `{TBD}` design partner conversations before it is published. The structure is the durable output; the numbers are the testable part.

---

## Step 9.1: Value Metric Selection

| Denominator | Correlation to Value | Scalability | Ease of Measurement | Score (1-10) |
|---|---|---|---|---|
| /user | Low. A licensed agent who never dials costs Flobase almost nothing and produces nothing | Poor. Directly contradicts the "unlimited seats" promise already published on the site, and taxes the recruiting motion the product is built to encourage | High. Trivially countable | 3 |
| /seat | Low, and worse than /user. It is the metric every competitor uses, so it invites line-item comparison against Ricochet360 at $162 to $210 and AgencyBloc at $109, a comparison Flobase does not need to have | Poor. Same growth tax, plus it makes the downline expansion loop expensive for the customer | High | 2 |
| /usage (leads purchased and calls routed) | High. Usage is the real cost driver for Flobase and tracks the customer's own activity closely | Good, but volatile. Seasonal agencies would see swings that make budgeting hard, and pure usage pricing gives the owner no reason to consolidate their stack | High. The wallet already meters it | 7 |
| /outcome (issued policy or issued AP) | Highest correlation of any option. The customer pays when they get paid | Poor in practice. Requires carrier-confirmed issue data Flobase does not control, creates chargeback and lapse disputes, and drags Flobase into compensation territory that raises regulatory questions | Low. Issue and lapse confirmation is outside the platform | 4 |
| /capability | Medium. Hierarchy, sub-agencies and priority routing genuinely map to agency maturity | Excellent. Aligns price with the customer's structural stage rather than their headcount or their volume | High | 8 |
| **Active producing agent** (an agent who spends wallet or submits a policy in the month) | High. Only agents actually working cost anything or produce anything, so the metric moves with real value on both sides | Excellent. Preserves unlimited seats, so recruiting and inviting a downline stays free, and only converts to revenue when an agent goes live | High. Computable from wallet and book data Flobase already holds | 9 |

**Recommendation**

- **Primary value metric:** active producing agent, banded rather than charged per unit. An agent counts as active in a month if they spend wallet or submit a policy. Recruits, trainees and dormant agents are free, which keeps the published "unlimited seats" promise honest and keeps the recruiting loop frictionless.
- **Secondary usage metric:** wallet consumption on leads and routed calls, charged at pass-through cost with a published platform fee. Not a hidden take rate. The site already claims "no hidden fees", and the entire positioning is spend transparency, so a concealed margin on lead purchases would be the one pricing decision that could destroy the positioning.
- **Tertiary packaging lever:** capability, used to separate tiers (sub-agency hierarchy, priority routing, API) rather than to meter usage.
- **Rationale:** this is the only combination that prices in step with the customer's growth without taxing the two behaviors Flobase most wants (adding agents and running spend through the wallet), and it is the only one that lets Flobase publish a price at all, which is itself the differentiator in a category where Convoso, AgencyBloc and EverQuote all require a sales call to learn a number.

---

## Step 9.2: Pricing Tiers

Decoy, Hero, Hero+, Anchor.

| Plan | Price | Active Producing Agents | Wallet Terms | Position | Target % of Customers |
|---|---|---|---|---|---|
| **Launch** | $0 per month | Up to 3 | Pass-through cost + 12% platform fee, published | Decoy / Entry | 10 to 20% |
| **Agency** | $299 per month | Up to 15 | Pass-through cost + 6% platform fee, published | **Hero** | 60 to 80% |
| **Scale** | $799 per month | Up to 50 | Pass-through cost + 3% platform fee, published | Hero+ | 10 to 20% |
| **IMO** | Custom | Unlimited | Pass-through cost + negotiated fee, floor 1% | Anchor | 5 to 10% |

**What each tier includes**

| Capability | Launch | Agency | Scale | IMO |
|---|---|---|---|---|
| Unlimited seats and role-based access | ✓ | ✓ | ✓ | ✓ |
| Zero-delay dialer, drip SMS, book of business | ✓ | ✓ | ✓ | ✓ |
| Lead marketplace | ✓ | ✓ | ✓ | ✓ |
| Live inbound call routing | ✗ | ✓ | ✓ | ✓ |
| Agency wallet with per-agent allocation | Single balance only | ✓ | ✓ | ✓ |
| Team performance dashboard, CPA and ROI | Basic | ✓ | ✓ | ✓ |
| Hierarchy and live org graph | ✗ | Single level | Sub-agencies | Unlimited depth |
| Onboarding and licensing tracker | ✗ | ✓ | ✓ | ✓ |
| Referral links for downline recruiting | ✗ | ✓ | ✓ | ✓ |
| Priority routing pool | ✗ | ✗ | ✓ | ✓ |
| API and data export | Export only | Export only | ✓ | ✓ |
| White label | ✗ | ✗ | ✗ | ✓ |

**Design notes on the tiers**

- **Launch is a genuine decoy.** It is deliberately missing live inbound routing and per-agent allocation, which are the two things the buyer came for. It exists to make Agency look inevitable and to let a three-agent shop start without a decision, not to be a good long-term home.
- **The 12% to 6% to 3% platform fee gradient is the real upgrade pressure.** An agency spending $20,000 a month on leads saves $1,200 a month by moving from Launch to Agency, which pays the $299 four times over. The tier upgrade argues for itself arithmetically, which suits a buyer who thinks in CPA.
- **Publishing the platform fee is the whole point.** Every competitor complaint in the research is about not knowing what something costs. A published percentage on a published pass-through cost is the pricing expression of the positioning.
- **The Agency tier at $299 undercuts a comparable stack by roughly an order of magnitude** while sitting above the impulse-purchase line, which protects perceived value.

**Expansion levers**

1. **Active producing agents crossing a band.** The most common and most natural upgrade, and it happens as the customer succeeds.
2. **Platform fee gradient on wallet spend.** As lead spend grows, the fee saving alone justifies the next tier.
3. **Hierarchy depth.** Opening a second branch requires Scale. This is the lever that converts a Level 1 ICP into a Level 2 ICP inside the product.
4. **Priority routing pool.** Agencies that can staff more inbound will pay for first claim on it, and this is the only lever tied to a genuinely scarce resource.

---

## Step 9.3: ROI Anchoring

All external benchmarks are cited in `../00_inputs_and_research/research_findings.md`. All Flobase-side numbers are the proposed prices above. The customer-specific inputs are illustrative scenarios, not measured customer results.

### Anchor 1: Cost of Problem

| Problem Scenario | Cost Without Solution | Annual Subscription Cost | ROI Multiple |
|---|---|---|---|
| A 12-agent agency spends $25,000 per month on leads. 15% flows to agents whose cost per issued policy sits above their commission, invisible until month end | $3,750 per month, $45,000 per year | $3,588 (Agency) | 12.5x |
| One agent burns $4,500 of wallet across two months with no issued policy, discovered at the second month's reconciliation | $9,000 per occurrence | $3,588 (Agency) | 2.5x on a single occurrence |
| Three recruits stall between licensing exam and contracting and are lost, at industry recruiting value of $4,000 to $6,000 per agent hired | $12,000 to $18,000 per year | $3,588 (Agency) | 3.3x to 5.0x |
| Owner rebuilds the weekly production and spend reconciliation by hand, 5 hours per week at a conservative $100 per hour of owner time | $26,000 per year | $3,588 (Agency) | 7.2x |

### Anchor 2: Alternative Comparison

Comparable stack for a 10-seat life telesales agency, at published list prices as of 2026-09-02. Flobase Agency covers up to 15 active producing agents.

| Alternative | Their Cost (10 seats, per month) | Our Cost (per month) | Savings % |
|---|---|---|---|
| Ricochet360 (dialer + CRM) at $162 per user, plus the $585 minimum already absorbed | $1,620 | $299 | 82% |
| AgencyBloc AMS+ (book, commissions, reporting) at $109 per user, annual term | $1,090 | $299 | 73% |
| Agent CRM or HighLevel (automation, funnels, SMS) at $97 to $297 plus usage wallet fees | $300 to $600 realistic | $299 | 0% to 50% |
| Assembled stack: Ricochet360 + AgencyBloc + a lead vendor account + spreadsheets | $2,710+ before any lead spend | $299 | 89% |
| Status quo: dialer + CRM + separate lead vendor + owner's manual reconciliation | $2,710+ software, plus roughly $2,170 per month of owner time | $299 | 94% against the fully loaded figure |

Two honest caveats to keep in the sales conversation rather than hide: Flobase does not process commissions, so an agency that needs commission statements may retain AgencyBloc or another AMS, and the assembled-stack comparison assumes ten seats, so it weakens for very small agencies.

### Anchor 3: Breakeven Analysis

Assumes a final expense average issued annual premium of about $850 with roughly 100% first-year commission, and an IUL case at about $6,000 first-year annual premium. Both are illustrative, not guaranteed.

| Plan | Annual Cost | Value Needed to Break Even | Typical Customer Value | Payback Period |
|---|---|---|---|---|
| Agency, $299 per month | $3,588 | About 4.2 issued final expense policies per year | A 12-agent floor writing 30 to 60 policies per month | Under 3 days of production |
| Scale, $799 per month | $9,588 | About 11.3 issued final expense policies per year | A 40-agent operation writing 120 to 250 policies per month | Under 3 days of production |

### "One Issued Case Pays For X" Calculator

| One issued case value | Plan | Subscription covered |
|---|---|---|
| $850 final expense policy | Agency, $3,588 per year | 0.24 years, about 2.8 months |
| $2,400 mortgage protection case | Agency, $3,588 per year | 0.67 years, about 8 months |
| $6,000 IUL case | Agency, $3,588 per year | 1.67 years |
| $6,000 IUL case | Scale, $9,588 per year | 0.63 years, about 7.5 months |
| $12,000 IUL case | Scale, $9,588 per year | 1.25 years |

**Message:** "One IUL case at $6,000 first-year premium pays for 1.7 years of the Agency plan. One final expense policy pays for nearly three months."

---

## Pricing Risks and Open Questions

| Risk | Why it matters | What resolves it |
|---|---|---|
| The platform fee on wallet spend could be read as the "hidden fee" the site promises not to charge | It would invert the core positioning at the exact moment of purchase | Publish the fee as a headline number on the pricing page, show it as a line item in the wallet, and never change it without notice |
| $299 may be under-priced for a product replacing $2,700 of stack | Leaves margin on the table and can signal low value to a buyer used to $109 per user | Test $299, $449 and $599 across design partner conversations before publishing |
| "Active producing agent" is a novel metric buyers have not seen | Novel metrics need explaining, and explanation costs conversion | Show it as a simple counter in-product and state the definition on the pricing page in one sentence |
| Lead supply cost is variable and outside Flobase's control | A pass-through model exposes the customer to supply price swings | Publish cost-per-call ranges by lead type, the way the market already does, and never smooth them silently |
| No commission processing weakens the consolidation claim at the top of the range | ICP Level 2 will keep an AMS, so "one tab" is not literally true for them | Either build it, or position explicitly as the layer in front of the AMS rather than its replacement |
