# Deliverable — Lead Magnet Specification: The Agency Profit Leak Scorecard

Skill deliverable "Lead Magnet: Scorecard Funnel Specification". Built for ScoreApp.com.
Derived from the demand driver selected in Dashboard 1.

---

## Scorecard Overview

| Element | Specification |
|---|---|
| Scorecard Name | The Agency Profit Leak Scorecard |
| Target ICP | ICP Level 1: owner-operator of a US life insurance telesales agency, 5 to 25 licensed producers, $10k to $60k per month in lead spend, final expense and mortgage protection weighted |
| Problem it Reveals | The owner cannot state their cost per issued policy per agent, so lead budget keeps flowing to producers who are below breakeven, and they find out weeks later, if at all |
| Immediate Value to User | A leak score out of 100, an estimated cost per issued policy for their agency, a comparison against the roughly $500 market cost per final expense close, and a named single biggest leak with what to do about it this week |
| Conversion Path to Flobase | Result page states the leak in dollars per month, then explains that producing the number continuously requires the lead invoice, the dial log and the policy record to sit in one ledger. High scorers get a direct walkthrough booking; medium scorers enter the four-email sequence; low scorers get the calculator and a nurture track |
| Completion target | Under 4 minutes, 7 questions, mobile-first, no email required to start |

---

## Questions

Seven questions. Scoring is a leak score where **higher means more leaking**, 0 to 100. Each question carries a maximum of 15 points except Q1 and Q7 which carry 10, totalling 85 raw, normalized to 100.

| # | Question | Answer Options | Scoring Logic | What It Reveals |
|---|---|---|---|---|
| 1 | How many licensed producers are actively working leads for you this month? | a) 1 to 4 (2) b) 5 to 9 (6) c) 10 to 19 (10) d) 20 or more (8) | Larger floors leak more in absolute terms, but 20+ agencies often already have an ops hire, so the curve peaks at 10 to 19 | ICP band and deal size. Routes 1 to 4 into a lighter nurture track |
| 2 | Roughly what does your agency spend on leads and calls in a typical month? | a) Under $5,000 (2) b) $5,000 to $15,000 (7) c) $15,000 to $40,000 (12) d) Over $40,000 (15) | Linear with spend; the exposure is the spend itself | The dollar size of the leak, and the tier they belong in |
| 3 | If I asked you right now what a single issued policy cost you in lead spend last month, how fast could you answer? | a) Off the top of my head, I track it (0) b) Within an hour from a spreadsheet (5) c) I would have to pull three reports and reconcile them (12) d) I genuinely could not tell you (15) | The core diagnostic question | Whether attribution exists at all. This is the question the whole scorecard is built around |
| 4 | Can you see cost per issued policy broken out per agent, not just for the agency overall? | a) Yes, per agent, updated continuously (0) b) Per agent, but only when I build it manually (8) c) Agency-wide only (13) d) No (15) | Blended CPA hides the actual leak, which is always agent-level dispersion | Whether the leak is even observable. Almost every ICP respondent lands on c or d |
| 5 | How do you control what an individual agent can spend on leads? | a) A per-agent budget enforced by the system (0) b) I approve each purchase myself (7) c) A monthly cap we track informally (11) d) Agents buy and I see it after the fact (15) | Measures whether spend can be stopped mid-month or only reviewed after | Whether a bad month can be interrupted. Directly maps to the agency wallet |
| 6 | How many separate vendors touch a lead between purchase and submitted policy? | a) One (0) b) Two (6) c) Three (11) d) Four or more (15) | Each handoff is a reconciliation point and a place attribution dies | Stack sprawl, and the size of the consolidation saving |
| 7 | Of the agents you recruited in the last 6 months, what share reached their first sale? | a) More than half (0) b) About a third (5) c) Fewer than one in five (9) d) I do not track it (10) | Industry baseline is roughly 30% gone within six months, so "do not track" scores near the worst outcome | Ramp leakage, and whether the onboarding tracker is a live pain or a future one |

**Derived output shown alongside the score:** estimated cost per issued policy, computed from the respondent's Q2 spend band midpoint divided by a stated close-rate assumption, presented explicitly as an estimate with the assumption visible. Never present it as measured fact.

---

## Results Tiers

| Score Range | Tier Name | Message | CTA |
|---|---|---|---|
| 0 to 39 | **Tight Ship** | "You are in the top slice of agencies for spend visibility. Your leak is small but it is not zero, and it will grow the moment you add agents faster than you add process. The number to watch is dispersion between your best and worst producer's cost per issued policy." | Soft. "Get the Cost Per Issued Policy Calculator" and enter the nurture track |
| 40 to 69 | **Leaking at the Seams** | "You know your blended numbers and you are flying blind below them. Based on your spend band, roughly `{calculated}` per month is going to producers you cannot currently identify as unprofitable, and you will not see it until the month closes. This is the most common and most expensive pattern in life telesales." | Medium. "See the 3 fixes for your biggest leak" then walkthrough offer in email 3 |
| 70 to 100 | **Bleeding** | "Your lead spend and your issued business are effectively in different universes. At your spend level that is roughly `{calculated}` per month you cannot attribute, and no amount of coaching fixes an attribution problem. This is fixable in weeks, not quarters, but not with the tools currently in your stack." | Strong. "Book a 30-minute walkthrough, we will rebuild your last 90 days live" |

**Tier logic notes:** the `{calculated}` figures come from the Q2 spend band midpoint multiplied by a leak percentage inferred from Q3 through Q5, with the assumptions shown on the result page. If the assumptions cannot be shown, drop the dollar figure and keep the score. A number this audience cannot audit will be dismissed, and the entire brand promise is about auditable numbers.

---

## Post-Scorecard Email Sequence

Four emails over eight days. Each has three variants, one per result tier. Copy below is the "Leaking at the Seams" variant, which is the majority path.

| Email # | Day | Subject Line | Content Focus | CTA |
|---|---|---|---|---|
| 1 | 0 | "Your leak score: `{score}` out of 100" | Deliver the result and interpret it. Restate their biggest leak in one sentence. Show the calculation assumptions openly. No product mention beyond a single footer line | "See how the score was calculated" |
| 2 | 2 | "Why your CRM cannot answer this question" | The structural reason: the lead invoice, the dial log and the policy record live in three systems that were never built to reconcile. Reference the stack teardown. Name the market benchmark of roughly $500 per final expense close | "Read the stack teardown" |
| 3 | 5 | "What it looks like when the three systems are one" | Introduce the mechanism, wallet to routed call to book to CPA, in three sentences. Offer the walkthrough where their own last 90 days get rebuilt live | "Book the 30-minute walkthrough" |
| 4 | 8 | "Last one on this" | One benchmark, one sentence on what they scored, an honest exit. Offer the calculator as the low-commitment alternative to a call | "Book a walkthrough" or "Just send the calculator" |

**Sequence rules**
- Plain text, no images, no more than 120 words per email. This audience reads on a phone between calls.
- No fabricated customer results in any email until a design partner result exists.
- Suppress the whole sequence on walkthrough booking.
- "Bleeding" tier variants compress the same arc into days 0, 1, 3 and 6, because the pain is acute and the window is short.
- "Tight Ship" tier variants extend to days 0, 4, 10 and 18, with the calculator rather than the walkthrough as the primary CTA.

---

## Build Specification for ScoreApp

| Item | Specification |
|---|---|
| Platform | ScoreApp.com |
| Question type | Single-select multiple choice throughout. No free text, no sliders |
| Email capture | After question 7, before the result. Never before question 1 |
| Fields captured | Email, first name, agency name. Nothing else |
| Result delivery | On-screen immediately, plus email 1 within 60 seconds |
| Mobile | Mobile-first. Test on a phone before launch, not after |
| Tracking | Per-channel UTMs preserved through to the CRM record, so completion rate can be read by channel and never blended |
| Integrations | ScoreApp to the ESP for the sequence, ScoreApp to the CRM for the lead record with score and tier as fields |
| Compliance | No collection of consumer PII, no health information, no carrier or product claims anywhere in the flow. The scorecard asks about the agency's operations only |
| QA gate before launch | Completion rate above 55% in a 20-person test, result page assumptions visible, all three tier paths verified, no `{TBD}` strings visible to a respondent |

## Success Metrics

| Metric | Target |
|---|---|
| Scorecard completion rate | Above 55% of starts |
| Cost per completion | `{TBD}`, set after first 2 weeks of paid traffic |
| Share of completions in ICP band (Q1 = b or c, Q2 = b, c or d) | Above 50% |
| Completion to walkthrough booking, Bleeding tier | Above 20% |
| Completion to walkthrough booking, all tiers blended | Above 8% |
| Email 1 open rate | Above 60%, it is a requested result, not a broadcast |
