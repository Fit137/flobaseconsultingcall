# Dashboard 1 — Product Feature Matrix (Flobase)

Skill steps 1.2 through 1.7. Research input: `../00_inputs_and_research/research_findings.md`.

---

## Demand and Competitiveness

Demand scale: Wanted by one / Wanted by some / Wanted by most / Wanted by all.
Competitiveness scale: Commodity should be free / Most vendors can do this / A few others can do this / Unique to us.

| # | Feature | Demand | Competitiveness | Evidence |
|---|---|---|---|---|
| F1 | Live inbound call routing, sub-second, exclusive | Wanted by most | A few others can do this | EverQuote and other marketplaces sell live transfers, but routing is the marketplace's, not the agency's. No CRM in the set owns the routing layer |
| F2 | In-platform lead marketplace | Wanted by most | A few others can do this | Radius imports from lead vendors, it does not sell leads. Buying inside the CRM is rare |
| F3 | Agency wallet with per-agent budget allocation | Wanted by most | Unique to us | HighLevel has an agency wallet for comms usage only. Nothing in the set lets an owner allocate lead budget per agent and see spend against it live |
| F4 | Zero-delay dialer | Wanted by all | Most vendors can do this | Convoso, Ricochet360, Radius and Agent CRM all dial |
| F5 | Drip SMS campaigns | Wanted by all | Commodity should be free | Every platform in the set ships SMS drips; Agent CRM gives away prebuilt sequences |
| F6 | Book of business | Wanted by all | Most vendors can do this | AgencyBloc and Radius both hold policy records; AgencyBloc goes deeper |
| F7 | Team performance dashboard, spend, CPA, AP, close rate, ROI | Wanted by most | A few others can do this | Reporting exists everywhere, but spend-to-issued-AP attribution per agent is the gap reviewers name |
| F8 | Production heatmap | Wanted by some | Commodity should be free | Visualization layer, cheap to replicate, no buyer switches for it |
| F9 | Team and hierarchy management with live org graph | Wanted by most | Unique to us | AgencyBloc serves IMO/FMO through commissions and compliance. No competitor renders and manages a downline branch structure |
| F10 | Onboarding tracker, training to licensing to contracting | Wanted by some | Unique to us | Nothing in the set tracks recruit ramp. The category treats agents as users, not as an inventory that churns at 90% |
| F11 | Unlimited seats and role-based access | Wanted by most | Most vendors can do this | RBAC is standard. Unlimited seats is a pricing decision, not a capability |
| F12 | Referral links for downline recruitment | Wanted by one | Unique to us | Recruiting mechanics are absent from every competitor in the set |

## Entry Validation

Rules applied from skill step 1.5:

1. If "Wanted by some" then exclude "Most vendors can do this".
2. If "Wanted by all" then exclude "Unique to us: Only we can do it".
3. If "Wanted by one" then exclude "Commodity should be free".

| # | Feature | First-pass assignment | Rule violated | Corrected assignment |
|---|---|---|---|---|
| F11 | Unlimited seats and RBAC | Wanted by some / Most vendors can do this | Rule 1 | Wanted by most / Most vendors can do this — RBAC is genuinely wanted by every agency above five agents, so demand was understated |
| F6 | Book of business | Wanted by all / Unique to us | Rule 2 | Wanted by all / Most vendors can do this — AgencyBloc and Radius both hold the record, so the original claim was indefensible |
| F12 | Referral links | Wanted by one / Commodity should be free | Rule 3 | Wanted by one / Unique to us — no competitor ships it, so it cannot be a commodity |

All other rows passed validation on the first pass. The corrected table is the one shown above.

## Scatter Plot Scoring

Demand and Competitiveness on a -20 to +20 scale, distributed with decimals.

| Feature | Demand Score | Competitiveness Score |
|---|---|---|
| F1 Live inbound call routing | 14.6 | 11.8 |
| F2 In-platform lead marketplace | 13.2 | 9.4 |
| F3 Agency wallet | 11.7 | 16.3 |
| F4 Zero-delay dialer | 17.9 | -4.2 |
| F5 Drip SMS campaigns | 16.4 | -12.7 |
| F6 Book of business | 18.3 | -6.8 |
| F7 Team performance dashboard | 12.9 | 7.6 |
| F8 Production heatmap | -3.4 | -7.1 |
| F9 Hierarchy and live org graph | 9.8 | 15.1 |
| F10 Onboarding tracker | -5.7 | 17.4 |
| F11 Unlimited seats and RBAC | 10.3 | -8.9 |
| F12 Referral links | -11.2 | 13.6 |

## Quadrant Assignment

```
                    HIGH COMPETITIVENESS (+20)
                           |
         QUADRANT 2        |        QUADRANT 1
      "Differentiators"    |      "Hero Features"
      Low Demand,          |      High Demand,
      High Competitive     |      High Competitive
      Advantage            |      Advantage
                           |
LOW DEMAND -----------------+------------------- HIGH DEMAND
(-20)                      |                        (+20)
                           |
         QUADRANT 3        |        QUADRANT 4
        "Commodities"      |       "Table Stakes"
      Low Demand,          |      High Demand,
      Low Competitive      |      Low Competitive
      Advantage            |      Advantage
                           |
                    LOW COMPETITIVENESS (-20)
```

| Feature | Quadrant | Rationale |
|---|---|---|
| F3 Agency wallet | Q1 Hero | Highest competitive score of any high-demand feature. It is the mechanism behind the whole spend-to-sale story and nothing else in the category does it |
| F1 Live inbound call routing | Q1 Hero | High demand and defensible. Owning routing inside the agency's own tool is what marketplaces will not give up |
| F2 In-platform lead marketplace | Q1 Hero | Buying inside the CRM removes a vendor and a reconciliation step. Few can match it because it needs supply relationships plus software |
| F7 Team performance dashboard | Q1 Hero | Demand is high and the attribution the category cannot do is exactly the reviewer complaint. Only heroic because it is fed by F3 |
| F9 Hierarchy and live org graph | Q1 Hero | The feature that makes Flobase an agency product rather than an agent product. Unique in the set |
| F10 Onboarding tracker | Q2 Differentiator | Nobody asks for it, everybody bleeds from it. 90% first-year attrition makes this a wedge once demand is created through education |
| F12 Referral links | Q2 Differentiator | Narrow demand today, but it is the growth loop: agencies recruiting downline inside the product recruit new Flobase seats |
| F8 Production heatmap | Q3 Commodity | Low demand, easy to copy. Keep it as visual polish, never lead with it, never build more of it |
| F6 Book of business | Q4 Table Stakes | Wanted by everyone, held by AgencyBloc and Radius. Must exist and must be fast, will never win a deal |
| F4 Zero-delay dialer | Q4 Table Stakes | Universally required, and Convoso and Ricochet360 are better at raw dialing. Must be good enough, not best |
| F5 Drip SMS | Q4 Table Stakes | Commodity. Price it into the base plan and stop talking about it |
| F11 Unlimited seats and RBAC | Q4 Table Stakes | Expected. Its value is as a pricing weapon against per-seat competitors, not as a feature claim |

**Reading of the map:** five features sit in Q1, and four of the five (F3, F1, F2, F7) form a single closed loop — fund the wallet, buy or receive the lead, work it, see what it produced. That loop is the product. Q4 holds four features that must be defended but never sold. Q3 holds one, which tells you nothing needs to be cut from the current build.

## Demand Driver

One demand driver, chosen to sit at the top of the funnel, deliver value on contact, and expose a problem only Flobase resolves.

| Attribute | Description |
|---|---|
| What it is | The Agency Profit Leak Audit: a self-serve calculation of cost per issued policy, broken out per agent, from the owner's own lead spend and submitted-AP numbers |
| Immediate value | The owner sees, for the first time in one view, which agents are converting lead spend into issued annual premium and which are burning it. Most owners know their blended CPA and nothing below it |
| How it helps in problem identification | It converts a vague feeling that "leads are expensive" into a named number per agent. At $85 per live transfer and a 20% close rate the market cost per close is about $500; agents below that band are visible instantly |
| How it exposes the need to use Flobase | Producing the number by hand requires joining the lead vendor invoice, the dialer log and the policy record, which live in three systems that do not reconcile. The audit shows the answer is worth having and that their current stack cannot produce it on an ongoing basis. The agency wallet plus book of business does, natively |
| ICP fit | Aimed squarely at ICP Level 1, the owner-operator of a 5 to 25 agent life telesales agency spending $10k to $60k per month on leads |
| Leverage for conversion | The audit output is an agent-level ranked list. That list is a management decision the owner wants to act on this week, and acting on it means reallocating budget per agent, which is the wallet |
| Top-of-funnel use case | Ungated scorecard, run in under four minutes, no data upload. Feeds an email sequence and a booked walkthrough where the same numbers get rebuilt live inside Flobase |

## Demand Driver Variants

| Variant Name | Perceived Value | Ease of Delivery | Delivery Type | Description | TOFU Use Case |
|---|---|---|---|---|---|
| Agency Profit Leak Scorecard | High | Easy | Self-assessment scorecard on ScoreApp | Seven questions producing a leak score, a per-agent CPA band and a named biggest leak | Primary. Paid social, community posts, cold email and outbound all point here. Built in full in the Lead Magnet Specification |
| Cost Per Issued Policy Calculator | Medium | Easy | Light tool | Single-page calculator: lead spend, calls, close rate, average AP in, cost per issued policy out | Blog and SEO capture, retargeting offer, sales-call leave-behind |
| Lead Spend Teardown Call | High | Hard | Service, white glove | 45 minutes with an operator rebuilding the last 90 days of the agency's spend against its submitted AP | Reserved for accounts above $30k per month lead spend. Not scalable, high close rate |
| 14-Day Wallet Trial with Inbound Credit | High | Medium | Value using the software itself | A funded starter wallet and live inbound access, so the owner sees real routed calls and real cost-per-call before paying | Bottom of a TOFU sequence, converts the scorecard's high scorers |
| Downline Margin Map | Medium | Medium | Light tool | Visualizes override margin by branch against that branch's lead burn | For multi-branch ICP Level 2 owners; secondary |
| Agent Ramp Readiness Audit | Medium | Hard | Service, white glove | Review of the agency's recruit-to-first-sale process against licensing and contracting timelines | Recruiting-led agencies; secondary, ties to the onboarding tracker |

**Selected for build:** the Agency Profit Leak Scorecard. Highest perceived value at the lowest delivery cost, and it is the only variant whose output is a management decision the owner cannot execute in their current stack.
