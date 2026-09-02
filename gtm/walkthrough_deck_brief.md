# Flobase — GTM Walkthrough, Interactive Deck Brief

**Audience:** the Flobase founder and whoever signs off on lead budget, across a table on a consulting call.
**Runtime:** 14 slides · ~13 minutes, or a 7-slide / ~7-minute cut (marked below)
**Ask:** approve the two unblocking decisions, publish pricing and open the design partner program, this week.
**Deliverable:** slide copy plus a design brief per slide, written to be handed straight to Claude to build as a single interactive HTML file.

Every claim on these slides traces to the nine GTM dashboards in this repo, and through those to the 29 cited sources in `00_inputs_and_research/research_findings.md`. Competitor prices are published list prices captured 2026-09-02. What is not verified is named individually in Part 4, and it is not a short list.

**A note on design ownership.** This brief deliberately specifies no palette, no type scale and no colour values. Claude Design carries its own design system and this deck inherits it whole. What follows governs geometry, construction, motion and hover behaviour only. Where a colour is named it is named by role, never by value. See Part 6 for where the deck-builder method had to bend to make that true.

---

## Part 0 — Deck spec at a glance

| | |
|---|---|
| Format | 16:9, one self-contained HTML file, arrow / click / swipe navigation |
| Slides | 14 (7-minute cut: 1, 3, 6, 7, 9, 13, 14) |
| Palette | **Inherited.** Host design system tokens, referenced by role only. This brief sets no values |
| Type | **Inherited.** One exception, tabular figures on every numeral, non-negotiable |
| Motion | CSS 3D transforms plus one shared requestAnimationFrame loop. No libraries, no WebGL |
| Register | Commercial. Objects **land**. Weight, settle, impact. This is a room where someone signs, so precision beats spectacle throughout |
| Spine | Flobase does not win by dialing faster. It wins because it is the only product that can tell an owner what a policy cost to issue, and the go-to-market is the act of publishing that number |

**The arc:** *the question you cannot answer → why the category cannot answer it → what that costs you → what you actually own → the loop → the objection → who to sell it to → how they buy → the offer → the ask*

**The number that carries the deck:** **$2,710 a month of stack, $299 to replace it, and not one competitor will publish either figure.**

**The recurring motif:** the ledger tick, three segments standing for invoice, call and policy. It appears on slides 1, 6, 13 and 14, unlit then progressively lit, and is never explained on screen. Geometry specified once in Part 2.

---

## Part 1 — The slides

### Slide 1 · The question

**On screen**

> **Eyebrow:** Flobase GTM
> **Headline:** What did that policy cost you?
> **Sub:** The answer lives in three systems that were never built to talk to each other.
> **Three plates:** Lead invoice · Dial log · Policy record
> **Kicker / bottom rail:** Nobody in this category can join them. That is the whole opportunity.

**Say it (~55 s)**

> "I want to start with the question your buyer cannot answer, because everything I'm about to show you comes out of it. An agency owner spends forty thousand dollars a month on leads. Ask them what one issued policy cost, and you'll get a blended number, if that. Ask which agent's policies cost more than the commission they paid out, and you get silence. Not because they're careless, these are sharp operators. Because the invoice sits with the lead vendor, the call sits in the dialer, and the policy sits in the CRM, and those three were never built to reconcile. So the owner becomes the integration layer, on a Sunday night, in a spreadsheet. I spent the whole research phase looking for someone who'd solved this. I want to show you who I found."

**Design brief**

- **Stage:** the host system's deepest background surface. Dark. Single light source from upper-left, raking, so the plates catch an edge highlight and cast soft shadow onto each other. This is the darkest slide in the deck and slide 14 returns to it.
- **Hero object — the three ledgers:** three flat planes, 420×260px, floating at `translateZ` of -180, 0 and +180, yawed 8° / 0° / -8°, arranged so they read as three pages that ought to stack but do not align. Each plane carries three or four ruled lines drawn in CSS, no real text, suggesting a document. Between them, six connector lines attempt to run plane to plane. **Every connector stops 24px short of its target and terminates in a small open circle.** The failure to connect is the entire argument of this slide, so it must be visible from the back of the room, not a subtlety.
- **Entry motion:** plates fade and rise from `translateY(40px)` staggered 140ms apart, 700ms each. Connectors draw last, 900ms after the third plate, using `stroke-dashoffset` over 500ms, and each one visibly decelerates and stops short rather than being clipped. The stopping is animated, not static.
- **Ambient:** the three plates drift out of alignment and back on an 11s loop, ±0.4° yaw, each on a different phase offset so they never re-align cleanly. The open circles at the connector ends pulse opacity 0.5 to 1.0 on a 3.5s loop.
- **Interaction:** pointer parallax across the whole rig, ±6° yaw and ±4° pitch, damped. **Hover any plate** and it lifts 20px toward the viewer over 180ms while the other two recede 10px and drop to 55% opacity, so the hovered record is isolated the way it is isolated in real life. **Keyboard:** `1` `2` `3` isolate the corresponding plate, `0` returns to rest.
- **Restraint:** do not animate the connectors reaching and retreating repeatedly. They draw once, stop short, and stay stopped. A connector that keeps trying reads as a loading state and the audience waits for it to succeed.
- **Reduced motion:** all three plates present at final position, connectors drawn to their short-stop state, no drift. Hover isolation still applies as an instant opacity change with no transform.

---

### Slide 2 · The category is fragmented by design

**On screen**

> **Eyebrow:** Competitive map
> **Headline:** Six competitors. Four budget lines. No overlap where it matters.
> **Four columns:** Dialer · CRM and book · Lead supply · Reconciliation
> **Column tenants:** Convoso, Ricochet360 / Radius, AgencyBloc / EverQuote / *nobody*
> **Kicker / bottom rail:** The fourth column is a spreadsheet the owner rebuilds every Monday.

**Say it (~50 s)**

> "So I mapped who's actually taking their money today. Six names, and they sort cleanly into four budget lines. Convoso and Ricochet360 sell you conversations, and they're genuinely good at it. Radius and AgencyBloc hold the record after the sale. EverQuote sells you the prospect before it. Three real businesses solving three real problems, and I'm not going to stand here and pretend otherwise, because your reps will lose credibility fast if they do. But look at the fourth column. Reconciliation. Nobody's standing in it. And that's not an oversight anyone's about to fix, it's structural, because none of those four can see the other three columns' data. They can't join what they can't see. So the owner does it by hand. Let me show you what that costs."

**Design brief**

- **Stage:** same dark surface as slide 1, lighting rotated to overhead so the blocks read as objects on a floor rather than pages in space. A subtle floor plane at `rotateX(72deg)` catches the block shadows.
- **Hero object — sorting blocks:** six extruded blocks, 130×90×34px, built with the face / edge / side construction in Part 2. They arrive scattered and unsorted, then physically travel into four labelled columns. Column four receives nothing, and an empty socket outline stays visible in it. **The empty column is the point.** Give it the same footprint and lighting as the occupied ones so its emptiness reads as absence rather than as layout.
- **Entry motion:** blocks fade in scattered at randomised positions over 500ms, hold 400ms so the disorder registers, then travel to their columns on staggered 620ms tweens, 90ms apart, each landing with a 100ms scale-punch to 1.03 and settling. Column labels fade up after the last block lands. The empty socket in column four draws its outline last, 400ms after everything else has stopped, which is what makes the room notice it.
- **Ambient:** blocks breathe on a 9s loop, ±0.3° yaw, phase-offset per column. The empty socket outline pulses opacity 0.35 to 0.7 on a 4s loop, slightly out of sync with the blocks, so it feels unresolved.
- **Interaction:** **hover a block** and it lifts 16px with a 180ms ease, its side faces brighten via the shared lighting model, and a small caption plate slides up from beneath it carrying that vendor's one-line weakness from the competitive dashboard, for example Convoso's *"no published price, not viable under twenty agents."* Hovering the empty socket surfaces *"this is the spreadsheet."* **Keyboard:** `1` to `4` step the columns, `Enter` on a focused column cycles its blocks.
- **Reduced motion:** blocks present in final sorted position, empty socket drawn, no travel and no breathe. Hover captions appear instantly.

---

### Slide 3 · What the stack costs

**On screen**

> **Eyebrow:** The teardown · 10 seats
> **Headline:** $2,710 a month, before you buy a single lead.
> **Printed lines:** Ricochet360, 10 seats · $1,620 — AgencyBloc AMS+, 10 seats · $1,090 — lead vendor account · billed separately — reconciliation · the owner's Sunday
> **Total plate:** $2,710 / month
> **Last line:** Cost per issued policy, per agent · **unknown**
> **Kicker / bottom rail:** Published list prices, 2026-09-02. The last line has no price because it is not for sale.

**Say it (~65 s)**

> "Here's the arithmetic, and I want to be clear these are published list prices, not my estimates, and you can hover any line and see the source. Ricochet360 is a hundred and sixty-two dollars a user, and they hold you to a five hundred and eighty-five dollar monthly minimum on top of that. AgencyBloc is a hundred and nine a user, on an annual term. Ten seats, that's twenty-seven hundred a month, and you haven't bought a single lead yet. That's before media. Now watch the last line, because this is the one I care about. Cost per issued policy, per agent. There's no figure next to it. And there's no figure because nobody sells it. You cannot buy that line from anyone on this list at any price. That's the line I think you should be selling, and it's the reason I'm going to push you to put your price on the website, which I'll come back to at the end."

**Design brief**

- **Stage:** lift the surface one step lighter than slides 1 and 2. This slide is a document, not a space, so flatten the perspective to `perspective: 2400px` and reduce parallax to ±2°. It should feel like paper on a desk under a lamp.
- **Hero object — the invoice:** a single tall plane, 560px wide, tilted `rotateX(6deg)`, with line items printing onto it top to bottom. A running subtotal in the upper right increments as each line lands. Numerals tabular, always, or the subtotal will reflow while it counts and the room will stop trusting it.
- **Entry motion:** each line item types on over 260ms with a 180ms gap, and the subtotal counts up to the new running figure over 300ms as the line settles. After the fourth line, **hold for 1.2 seconds with nothing moving.** Then the total plate lands beneath the rule with a 110ms impact, scale 1.04 to 1.0, and a faint dust ring. Then, 800ms later, the final line prints, and where a figure should be it carries the word `unknown` in the same tabular treatment the numbers used, so it occupies a number's slot and reads as a missing value rather than as a caption.
- **Ambient:** the paper plane drifts ±0.25° yaw on a 13s loop, nothing else. The lamp highlight sweeps across it once every 14s, 2.5s duration, left to right.
- **Interaction:** **hover any line item** and a small source chit slides out to the right carrying the citation, for example *"Capterra, list price, 2026-09-02"*, over 180ms. This slide is where the founder will push back, so every number must be defensible under a cursor without leaving the slide. **Keyboard:** `↑` `↓` walk the line items, source chit follows focus.
- **Restraint:** **do not animate the `unknown` line.** No pulse, no glow, no colour shift, no shake. It prints once in the same weight as every other line and then holds absolutely still while the presenter talks over it. The stillness is what makes it land. Any emphasis added here converts an argument into a gimmick and the room will feel sold to.
- **Reduced motion:** the full invoice rendered complete, total plate in place, `unknown` present, no printing sequence and no sweep. Source chits render permanently inline beneath each line rather than on hover, which is also the print state.

---

### Slide 4 · What you actually own

**On screen**

> **Eyebrow:** Feature matrix · 12 shipped features scored
> **Headline:** Five features carry the company. Four you must defend and never sell.
> **Quadrants:** Hero, 5 · Differentiator, 2 · Table stakes, 4 · Commodity, 1
> **Named heroes:** Agency wallet · Live inbound routing · Lead marketplace · CPA attribution · Hierarchy and org graph
> **Kicker / bottom rail:** Nothing sits in the cut quadrant. There is nothing here to remove.

**Say it (~55 s)**

> "So I scored all twelve of your shipped features on two axes, how much the market wants it and how hard it is to copy, and plotted them. Five land in the hero quadrant. The dialer isn't one of them. Neither is drip SMS. And I want to be blunt that this is good news, not bad news. Convoso and Ricochet360 will beat you on raw dialing forever, they've spent years on caller ID reputation, so the worst thing your reps can do is spend a call arguing about it. Those are table stakes. They have to be good enough and then you stop talking about them. One feature landed down in the commodity corner, the production heatmap, and even that one I'd keep. There's nothing in this build I'd cut. But four of those five heroes have something in common."

**Design brief**

- **Stage:** dark surface, single overhead source. This slide is a field, so establish a floor plane at `rotateX(68deg)` with a faint grid marking the two axes. Grid lines use the host system's most muted border token.
- **Hero object — the quadrant field:** twelve small extruded markers standing on the floor plane at their real scored coordinates from the feature matrix dashboard, height scaled to demand score so the field reads as a physical relief map rather than a scatter chart. The five hero markers stand tallest and take the host system's accent role. The rest take the muted role. **Positions must come from the actual scores in `01_product_feature_matrix`, not from an eyeballed layout**, because the founder may recognise a feature sitting somewhere they disagree with, and that is a conversation worth having.
- **Entry motion:** the floor grid draws first, 500ms, axis lines from origin outward. Markers then rise from the floor to their heights, staggered 70ms, 550ms each, in ascending score order so the field builds from commodity up to hero and the eye finishes on the tall cluster. Quadrant labels fade in last.
- **Ambient:** the five hero markers breathe ±0.4° and gain a 6% height oscillation on an 8s loop, phase-offset. The other seven are still. Life is allocated to the argument, not distributed evenly.
- **Interaction:** **hover a marker** and it rises a further 18px over 180ms while a label plate rotates up from its base carrying the feature name and both scores. Simultaneously the other eleven drop to 40% opacity. **Hover a quadrant label** and all markers in that quadrant lift together, which is how the presenter shows "these four are table stakes" in one gesture. **Keyboard:** `Q` cycles quadrants, `↑` `↓` walk markers within the focused quadrant.
- **Reduced motion:** full field at final heights, no rise, no breathe. Hover lift becomes an instant opacity and outline change.

---

### Slide 5 · Quiet slide

**On screen**

> **Headline:** Four of those five are the same loop.
> *(nothing else on this slide)*

**Say it (~25 s)**

> "Before I show you the next slide, I want you to notice something I didn't see myself until about the third pass through this material. Four of those five hero features aren't five separate advantages that happen to sit next to each other. They're one thing, described four different ways. It took me longer than it should have to spot it. Here it is."

**Design brief**

- **Stage:** **invert to the host system's lightest surface.** This is the only light slide in the deck and it exists purely to make slide 6 land. The contrast is doing the work, so do not decorate it.
- **Hero object:** none. One line of type, optically centred, sitting slightly above true centre. That is the entire slide.
- **Entry motion:** the line fades up from `translateY(12px)` over 600ms. Nothing else happens. Do not stagger the words. Do not animate per-character.
- **Ambient:** a single ledger-tick motif, unlit, small, bottom-left at the deck's standard motif position, drifting ±0.2° on a 14s loop. This is the motif's second appearance and it is at its quietest here, which is what earns its third appearance on slide 6.
- **Interaction:** none. Deliberately. The presenter is speaking and there is nothing to grab.
- **Restraint:** **this slide gets no hero object, no parallax, no light sweep and no hover state at all.** A builder's instinct will be to fill it, because it will look unfinished next to its neighbours in a review. It is not unfinished. A deck at constant intensity has no peak, and slide 6 is the peak. Reject any addition here.
- **Reduced motion:** identical, minus the fade and the motif drift.

---

### Slide 6 · The loop · CENTREPIECE

**On screen**

> **Eyebrow:** The mechanism
> **Headline:** Fund it. Buy the lead. Work it. See what it produced.
> **Four stations:** Agency wallet → Lead marketplace and live inbound → Zero-delay dialer and SMS → Book of business
> **Return path:** cost per issued policy, per agent
> **Kicker / bottom rail:** One ledger. That is the product.

**Say it (~70 s)**

> "This is the whole thing, and if you take one slide out of today, take this one. Money goes into the wallet. The owner allocates it per agent, so every dollar has a name on it before it's spent. That budget buys a lead, or it receives a routed inbound call. The agent works it, submits the sale, and the policy lands in the book still attached to the dollars that bought it. And then it closes. That return path underneath is what makes the number computable. Not a better report, not a smarter dashboard. You can compute it because you own every single step, and nobody else owns more than one. Now think back to the first slide for a second. Same three records. Invoice, call, policy. There, they couldn't join no matter how hard anyone tried. Here, they never had to join, because they were never apart in the first place. That's your company in one sentence, and honestly I'd put it on the homepage above everything that's up there now."

**Design brief**

- **Stage:** return to the deep dark of slides 1 and 2, but raise the light. This is the brightest-lit dark slide in the deck. Key from upper-left, plus a soft fill from below so the loop's underside is legible, because the return path runs beneath the stations.
- **Hero object — the closed circuit:** four station objects arranged on an ellipse in 3D, each a small extruded block with a distinct silhouette, positioned so the ellipse is seen at roughly `rotateX(52deg)`, giving depth without becoming a flat ring. Between stations, a track segment. Beneath the ellipse, running back from station four to station one, a **return path drawn on a lower Z plane** so it visibly passes under the stations rather than through them.
- **Entry motion:** stations rise in sequence, 1 through 4, 600ms each with a 240ms overlap, each landing with a 90ms settle. As each lands, the track segment to the next station draws over 380ms. When station four lands, hold 600ms with the loop still open. **Then the return path draws beneath, right to left, over 900ms, and on connection the entire circuit lights in a single 220ms pass and the ledger-tick motif in the corner lights all three segments for the first time in the deck.** That single moment is the centrepiece. Everything before it in the deck is setup for it.
- **Ambient:** once lit, a pulse travels the circuit continuously, one full lap every 11s, brightening each segment as it passes by roughly 18% and decaying behind it. The stations themselves breathe ±0.3° on a 9s loop. **The loop must never stop moving while the presenter is on this slide**, because a stalled circuit reads as a broken product.
- **Interaction:** **hover a station** and it lifts 22px over 180ms, the pulse slows to half speed while hovered, and a detail plate unfurls carrying that station's real capability line from the feature matrix. Hovering does not break the circuit. **Hover the return path** and it thickens and brightens over 180ms while the four stations dim to 50%, isolating the thing that makes the product defensible. **Click any station** to latch it, so the presenter can leave it open and talk with both hands. **Keyboard:** `1` to `4` latch stations, `R` isolates the return path, `0` clears.
- **Restraint:** do not add particles, sparks or trails to the pulse. One clean travelling brightness. The temptation here is enormous because this is the money slide, and every effect added past the light pass makes it read as a product video rather than as an argument.
- **Reduced motion:** full circuit rendered lit and closed, return path drawn, ledger tick fully lit, no travelling pulse and no breathe. Hover isolation retained as instant opacity change.

---

### Slide 7 · The objection

**On screen**

> **Eyebrow:** The thing they will say back
> **Headline:** "Convoso dials faster."
> **Left plane:** Raw throughput — Convoso 9.6, Flobase 7.4
> **Right plane:** Spend-to-sale transparency — Flobase 9.3, best competitor 5.8
> **Kicker / bottom rail:** Both are true. Only one of them is a fight you can win.

**Say it (~65 s)**

> "Somebody in an evaluation is going to say this to your rep, probably in the first ten minutes, and I'd much rather we answer it here than have someone improvise it badly on a call. Yes. Convoso dials faster. I scored them at nine-six against your seven-four and I'd defend both numbers in front of them. They've spent years on caller ID reputation and it genuinely shows in their contact rates. So if the deal turns into a dialing bake-off, you lose it. And you should lose it, because that's a fight where the other guy is simply better. Don't take it. Now look at the second axis. You're at nine-three, the closest competitor is under six, and that's the axis where you're the only credible answer in the room. The discipline this needs is that your reps concede the first one immediately and move, every single time, without exception. Conceding is what buys you the right to make the second claim."

**Design brief**

- **Stage:** dark, lighting split so the left half of the stage is cooler and flatter and the right half is keyed. The stage itself takes a side before the copy does.
- **Hero object — the hinge:** two planes, 400×300px, joined on a shared vertical axis at centre, each rotated to face the pointer while the other recedes, per the standard hinge construction. Each plane carries its axis name and its two scores as a small bar pair, tabular figures.
- **Entry motion:** the hinge arrives closed, edge-on, at 900ms, then opens to 42° over 700ms so both planes are legible. Score bars fill left to right over 500ms staggered 120ms. Both planes are equally lit at rest, which matters, because the slide's credibility depends on conceding the first axis honestly before winning the second.
- **Ambient:** the hinge oscillates ±1.5° around its axis on a 10s loop, so both planes are alive and neither is favoured until the presenter acts.
- **Interaction:** **hover either plane** and it rotates to face the viewer over 220ms while the other recedes toward edge-on and drops to 45% opacity. **Click the left plane** to concede it: it rotates a full 90° to edge-on and stays there, leaving the right plane alone and square to the viewer. That gesture is the argument, and it is the one interaction in the deck the presenter should rehearse. Do not fade the conceded plane out. It stays present, edge-on, visible, because the claim is *"that's true and I'm not taking that fight"*, not *"that doesn't exist."* **Keyboard:** `←` `→` to face a plane, `Enter` to concede the focused one, `0` to reopen.
- **Restraint:** **do not animate the two score bars competitively.** No racing, no overtaking, no colour change on the losing figure. They fill once, at the same rate, and stop. Anything that dramatises the comparison undercuts the concession, and the concession is what buys the presenter the right to make the second claim.
- **Reduced motion:** hinge open at 42°, both planes legible, bars filled. Concede becomes an instant 90° state change with no tween.

---

### Slide 8 · Positioning

**On screen**

> **Eyebrow:** Four vectors, scored 0 to 10
> **Headline:** Two the incumbents own. Two nobody has claimed.
> **Theirs:** Outbound dialing throughput, Convoso 9.6 · Policy and commission depth, AgencyBloc 9.5
> **Ours:** Spend-to-sale transparency, 9.3 · Single-tab agency operations, 9.1
> **Kicker / bottom rail:** Both of ours are reversals of their own reviewers' complaints. We did not choose them. The reviews did.

**Say it (~55 s)**

> "The two vectors we lead on didn't come out of a positioning workshop, and I think that's the single most useful thing about them. I read the one, two and three star reviews across the whole competitor set and pulled out what people complain about over and over. Opaque pricing. Costs that show up after signature. Minimum spends. Four vendors that don't talk to each other. Turn those complaints over and you get exactly two vectors, and they happen to be the two nobody's standing on. So when a prospect asks why you're claiming these, the answer isn't that you think you're good at them, which is what every vendor says. It's that their own customers said it, on their own review pages, and you can quote it back. That's a much stronger position than an opinion."

**Design brief**

- **Stage:** dark, overhead key. Establish a floor plane so the four vectors read as standing on ground rather than floating.
- **Hero object — four standing vectors:** four vertical extruded columns arranged front to back in Z, not side by side, so depth carries the ranking and the two rear columns are genuinely further away. Each column's height is its Flobase score and each carries a smaller ghost column beside it at the leading competitor's score. The two we lead take the host accent role, the two we do not take the muted role.
- **Entry motion:** the two incumbent-led vectors rise first, 700ms, with their competitor ghosts rising taller alongside them, so the room sees us losing those two before we claim anything. Hold 700ms. Then the two we lead rise, 800ms, overtaking their ghosts, and their ghosts settle visibly short. The order is the argument. Concede, then claim.
- **Ambient:** all four breathe ±0.35° on a 10s loop. A slow light sweep crosses the field every 13s, 3s duration, front to back, so the rear columns are periodically legible.
- **Interaction:** **hover a column** and it and its ghost both lift 18px while the other three pairs drop to 45%, and a plate unfurls carrying the derivation, for example *"reversal of: no published price, hidden costs after signing, minimum spends."* This is the slide where the founder asks "says who", so the source must be one hover away. **Keyboard:** `1` to `4` walk vectors front to back.
- **Reduced motion:** all four at final height with ghosts, no rise sequence, no sweep. Derivation plates render inline beneath each column permanently.

---

### Slide 9 · Who to sell to first

**On screen**

> **Eyebrow:** ICP Level 1
> **Headline:** Five to twenty-five agents. Structurally undefended.
> **Three gates:** Ricochet360 · $585/mo minimum — Convoso · not viable under ~20 seats — AgencyBloc · $109/user, annual term
> **The band:** 5 to 25 producers · $10k to $60k monthly lead spend · owner is the entire approval chain
> **Kicker / bottom rail:** Every direct competitor has priced themselves out of this band. That is not a gap we found. It is one they left.

**Say it (~60 s)**

> "This is the segment I'd start with, and I want to show you why rather than just assert it. Three gates. Ricochet360 holds you to five hundred and eighty-five a month whatever your size, so a small agency pays for capacity it can't use. Convoso isn't practical under about twenty seats, and their own reviewers are the ones who say so, not me. AgencyBloc wants a hundred and nine a user on a twelve-month commitment. Now put a twelve-agent agency in front of those three. Every one of them is either too expensive, too big, or won't take the meeting. So that band is sitting there underserved, and the owner is the entire approval chain, which means one conversation, one signature, no committee. That's the cheapest customer acquisition available to you anywhere in this market, and it's available because three competitors walked away from it on purpose."

**Design brief**

- **Stage:** dark, key from directly above so the gates cast hard vertical shadows across the floor and the lit band between them is unmistakable.
- **Hero object — the gates:** three tall thin slabs standing across the stage in Z, each carrying a competitor's price floor. Between and beyond them, a floor band lit in the host accent role, marked 5 to 25. **Scarcity here is structurally true, so render it truthfully:** the gates are not blocking a door, they are standing where those competitors' economics genuinely stop. Do not draw the band as a prize with rays or a spotlight cone. It is simply the only lit ground.
- **Entry motion:** floor draws first, unlit, 500ms. Gates drop in from above in sequence, 1 to 3, each falling 300px over 500ms and landing with a 110ms impact and a short dust ring, staggered 260ms. Each landing darkens the floor either side of it. After the third lands, hold 500ms, then the remaining band lights over 700ms from centre outward. The band lights because the gates have finished falling, not on its own cue.
- **Ambient:** dust motes drift slowly in the key light, 5 to 7 particles, 14s loop, extremely subtle. The lit band's intensity oscillates ±6% on a 9s loop.
- **Interaction:** **hover a gate** and it lifts slightly and its full constraint plate unfurls with the citation. **Hover the lit band** and the three ICP qualifiers rise from the floor as small standing labels, and the gates dim to 40%. **Keyboard:** `1` `2` `3` for gates, `B` for the band.
- **Reduced motion:** gates standing at final position, band lit, no fall, no impact, no motes. Constraint plates inline.

---

### Slide 10 · How they buy

**On screen**

> **Eyebrow:** Customer journey · seven stages
> **Headline:** Stages three and four collapse into one call.
> **The road:** Problem awareness → Solution discovery → **Vendor evaluation** → **Trial and purchase** → Value realisation → Expansion → Renewal
> **The compression:** the walkthrough rebuilds their own last ninety days, and the funded wallet starts in the same session
> **Kicker / bottom rail:** No data migration is required to start, so nothing has to wait.

**Say it (~55 s)**

> "Seven stages, and I've written the buyer's actual words at each one so your team can hear them. But the part I'd change your calendar over is sitting in the middle. In a normal software sale, evaluation and trial are weeks apart, because trial means migration, and migration means somebody has to move their data before they can see anything. Here it doesn't. You can rebuild their last ninety days live on the walkthrough call, from numbers they already know by heart, and then fund a wallet and route a real call before you hang up. Those two stages become one session. Not one of the six competitors can do that, because every one of them needs your data moved first. That's a cycle-time advantage, and I'd argue it's worth more to you than any single feature on the matrix slide."

**Design brief**

- **Stage:** dark. Deep perspective, `perspective: 1100px`, because this slide is about distance and the far end of the road should genuinely feel far.
- **Hero object — the ribbon:** the seven stages as a road receding into Z, not a horizontal bar. Each stage is a marker standing on the road surface. Near stages are large and legible, far stages small. Stages 3 and 4 sit at the point where the road is still readable, which is where the eye naturally rests.
- **Entry motion:** the road draws from the viewer outward over 900ms, easing out so it appears to accelerate away. Markers rise in order 1 to 7, staggered 90ms, 450ms each. After stage 7 lands, hold 800ms. **Then markers 3 and 4 slide toward each other and merge into a single wider marker over 600ms**, the road between them closing up, and the total road length visibly shortens. The compression is the claim and it must be the last thing that happens.
- **Ambient:** a light travels the road from near to far every 12s, 4s duration, passing over each marker in turn. Markers breathe ±0.3° on staggered 10s loops.
- **Interaction:** **hover a marker** and it grows, rotates to face the viewer regardless of its depth, and unfurls the buyer's quoted mindset and that stage's internal KPI. Far markers must become fully legible on hover, which is the only reason a seven-item list works in perspective at all. **Click the merged 3-4 marker** to split it back apart and replay the merge, because the presenter will want to show it twice. **Keyboard:** `↑` `↓` walk stages, `M` replays the merge.
- **Reduced motion:** road drawn, all markers placed, stages 3 and 4 already merged. No travel light, no merge animation. `M` performs an instant split and re-merge.

---

### Slide 11 · The scorecard

**On screen**

> **Eyebrow:** Demand driver · the top of the funnel, all channels
> **Headline:** Seven questions. Under four minutes. One number they do not have.
> **What it returns:** a leak score, an estimated cost per issued policy, their single biggest leak
> **Why it converts:** producing that number by hand means joining three systems that do not reconcile
> **Kicker / bottom rail:** The result is a management decision they will want to act on this week.

**Say it (~60 s)**

> "One lead magnet, not five, and it's the same asset in every channel with different entry copy on top. Seven questions, four minutes, and no email address until after the last one, which matters more than people think. What comes back is a leak score and an estimate of what a policy is actually costing them. But here's why it converts, and it isn't the score. It's what happens when they try to check the number. To verify it, they'd have to join the lead invoice, the dial log and the policy record, and now we're right back on slide one. So the scorecard hands them a decision they genuinely want to make on Monday morning, and the only way to act on it is to reallocate budget per agent. Which is the wallet. The lead magnet and the product are the same argument."

**Design brief**

- **Stage:** mid-tone, one step lighter than the dark slides. This is an artifact slide, so the object should feel handled rather than staged.
- **Hero object — the scorecard:** a single card, 340×460px, standing at a slight tilt, built with real depth on its edge so it reads as a physical card rather than a rectangle. Its face carries seven ruled question rows. **On its reverse is the result**, a single large tabular number.
- **Entry motion:** card rises and settles over 700ms. The seven question rows tick on, 110ms apart, each a short 160ms draw. After the last row, hold 900ms. Then the card flips 180° on its vertical axis over 420ms, and the result number counts up on the reverse over 500ms as the flip completes, so the number is already moving when the face arrives. **The flip is the argument**, per the standard flip mechanic.
- **Ambient:** the card drifts ±0.4° yaw and ±0.25° pitch on an 11s loop. A sheen tracks slowly across its face on a 10s cycle independent of the pointer, so it is alive before anyone touches it.
- **Interaction:** **hover the card** and the sheen leaves its ambient path and tracks the pointer directly, over 180ms, and the card tilts up to 10° toward the cursor. This is the deck's most tactile hover and it should feel like picking something up. **Click** to flip between question face and result face; the presenter will flip it repeatedly while talking. **Hover a question row** on the face side and its answer options and what it reveals unfurl to the side. **Keyboard:** `Space` flips, `↑` `↓` walk the seven rows.
- **Reduced motion:** card at rest showing the question face, result face reachable by click as an instant swap, no flip tween, no drift, sheen static.

---

### Slide 12 · The assets

**On screen**

> **Eyebrow:** Assets and collaterals · 22 pieces
> **Headline:** Twenty-two assets. Five of them are blocked on one decision.
> **Channels:** Cold email, full weight · LinkedIn, test weight · LinkedIn ads, test weight · Facebook and YouTube, **recommended, not in the original scope**
> **The block:** publish pricing → unblocks 5 · first design partner result → unblocks the entire bottom of funnel
> **Kicker / bottom rail:** The library is built. Two decisions release it.

**Say it (~55 s)**

> "Twenty-two assets, mapped top to bottom across the channels. Two things I want to flag rather than bury in an appendix. First, the brief specified LinkedIn, and I've built LinkedIn in full, but your buyer lives in Facebook groups and on YouTube and a lot of them barely open LinkedIn. So I've added a fourth channel outside the original scope, and I'd put real budget behind it. Second, and this one matters more. Five of these assets can't ship until you publish a price. And every single bottom-of-funnel asset is blocked until one design partner gives you a real before-and-after number. So the library isn't your bottleneck. The library's finished. What's holding it is two things only you can sign off, and I'm going to ask you for both of them at the end."

**Design brief**

- **Stage:** dark, even lighting, because this slide is inventory and clarity beats drama.
- **Hero object — depth repetition:** the 22 assets as small plates arranged in four channel lanes running back into Z, three depth ranks per lane for top, middle and bottom of funnel. **Blocked assets render as wireframe outlines with no fill**, unbuilt things rendering as unbuilt, never as existing. The fourth lane, the recommended channel, renders in the same fill as the others but with a dotted lane floor, marking it as outside the original scope without demoting it.
- **Entry motion:** lanes draw back to front, 400ms each, 150ms apart. Plates populate within each lane in funnel order, staggered 45ms, 300ms each. The wireframe blocked plates arrive last, after every solid plate has landed, and arrive at 60% opacity so their absence registers as the final beat.
- **Ambient:** plates breathe ±0.25° on staggered 12s loops. The wireframe outlines pulse opacity 0.4 to 0.7 on a 5s loop, unresolved, matching the empty socket on slide 2 so the two read as the same visual idea.
- **Interaction:** **hover a lane** and it slides forward in Z while the other three recede and dim, with the lane's asset count and weight recommendation surfacing. **Hover a wireframe plate** and it surfaces exactly what unblocks it. **Press `U`** to fill every wireframe plate simultaneously over 500ms, showing the library complete, which is the gesture that makes the ask on slide 14 concrete. **Keyboard:** `1` to `4` for lanes, `U` to toggle the unblocked state.
- **Reduced motion:** all lanes and plates at final position, wireframes static at 60%, no breathe or pulse. `U` performs an instant fill.

---

### Slide 13 · The offer

**On screen**

> **Eyebrow:** Pricing and packaging · proposed, not validated
> **Headline:** $299, published on the page, with the platform fee printed next to it.
> **The metric:** the active producing agent — spends wallet or submits a policy this month. Recruits and dormant agents are free
> **The tiers:** Launch $0 · **Agency $299** · Scale $799 · IMO custom
> **The gradient:** 12% → 6% → 3% platform fee on wallet spend, published
> **Kicker / bottom rail:** $2,710 of stack. $299 to replace it. One IUL case pays for 1.7 years.

**Say it (~55 s)**

> "Here's the offer, and I want to be honest up front that these numbers are a design, not a validated price, because you've never published one to test against. The structure I'd defend hard. Charge per active producing agent, meaning somebody who spent wallet money or wrote a policy that month. Recruits are free. Dormant agents are free. So your unlimited seats promise stays literally true, and recruiting stays frictionless, which matters because recruiting is how these accounts grow. Then publish the platform fee on wallet spend, twelve percent down to three as they scale, printed right there next to the price. Every recurring complaint in this category is about not knowing what something costs until after you've signed. Publishing that number is the strategy. It is not a disclosure risk. It's the cheapest differentiator you own, and it's sitting there unclaimed."

**Design brief**

- **Stage:** dark, key from upper-left, with enough fill from beneath that the price card's underside edge is legible when the stack settles onto it.
- **Hero object — the stack:** value slabs stacking upward, one per click or auto-advance, each slab's depth scaled to its replacement value, with a running total counting up in tabular figures beside the stack. **Then the price card lands beneath the stack**, and the whole stack settles onto it by 6px with a 100ms impact. The stack resting on the price is the argument that the price is carrying the value, and it only works if the settle is visible, so hold the camera still through it.
- **Entry motion:** slabs arrive from above, 520ms each, 140ms apart, each landing with a 90ms settle. Running total increments as each lands. After the last slab, hold 1.0s. Price card slides in beneath over 600ms, then the settle. **Then, 700ms later, the fee gradient appears beside the stack as three figures, 12, 6, 3, and the ledger-tick motif lights for its third appearance.**
- **Ambient:** the settled stack breathes as a single body, ±0.25° on a 12s loop, so it reads as one mass resting on the card rather than as separate slabs. A slow highlight passes down the stack's front face every 13s.
- **Interaction:** **hover a slab** and it slides out 30px to the right, revealing its replacement-cost basis and citation, then returns on exit. Every slab must be auditable this way, because a single indefensible line here discounts the whole stack. **Hover the price card** and the four tiers unfurl beneath it. **Hover a fee percentage** and it shows the annual saving at a worked lead-spend example. **Keyboard:** `↑` `↓` walk slabs, `T` opens the tier set, `F` cycles the fee gradient.
- **Reduced motion:** stack complete and settled on the price card, total shown, gradient present, motif lit. No arrival, no settle, no highlight. Slab bases render inline permanently, which is also the print state.

---

### Slide 14 · The ask

**On screen**

> **Eyebrow:** What I need from you
> **Headline:** Two decisions this week.
> **One:** Publish pricing, including the platform fee. Unblocks five assets and the biggest evaluation-stage blocker
> **Two:** Open the design partner program. Five to eight owners. Unblocks every bottom-of-funnel asset you have
> **Still open:** no measured routing latency · no basis for the "#1" claim · no commission processing · pricing unvalidated
> **Kicker / bottom rail:** What did that policy cost you? Now you can answer it.

**Say it (~60 s)**

> "Two decisions, and neither one is a build. Publish the price, including the fee, this week. And open the design partner program, five to eight owners who are already running a version of this in spreadsheets, because until one of them gives you a real before-and-after, every proof point in this strategy is a blank space. I've left those blanks visible rather than filling them with something plausible, and there are four more listed there I'd want settled before any of this goes in front of a customer. You'll notice I haven't put a single customer number on any slide today, and that is exactly why. But look at what's behind me. Same three records I opened with. They join now. That's the company. Everything I've shown you today is just the work of saying that out loud, in public, with a price attached."

**Design brief**

- **Stage:** **return exactly to slide 1.** Same deepest surface, same raking key from upper-left, same camera position. The loop closes visually or it does not close.
- **Hero object — the three ledgers, joined:** the identical three-plane rig from slide 1, same dimensions, same positions. **The state is what changed.** The six connectors now complete: they run plane to plane, terminate in closed filled nodes rather than open circles, and the three planes have rotated into alignment at 0° yaw. The ledger tick sits at its standard corner position, fully lit for its fourth and final appearance.
- **Entry motion:** the three plates arrive already aligned, 600ms fade and rise, no stagger, because the disorder of slide 1 is over. Connectors then draw plane to plane over 700ms and each one **completes**, the closing node snapping shut with a 90ms scale-punch. Then the two ask lines fade up, 500ms, 200ms apart. The open items fade up last, at 70% opacity, deliberately quieter than the ask.
- **Ambient:** the joined rig drifts as one body, ±0.3° on a 12s loop, all three planes in phase, which is the visual opposite of slide 1's out-of-phase drift. A pulse runs the connector network every 10s.
- **Interaction:** **hover either ask line** and it lifts with its detail. **Hover the open-items block** and each item expands to state what breaks if it goes the other way, because the founder will ask and the honest answer should be one hover away rather than a slide the presenter skipped. **Press `1`** to snap back to slide 1's broken state for a two-second A/B, then release. That comparison is the deck's closing gesture and it should be on a key, not a cursor. **Keyboard:** `1` holds the before-state, `↑` `↓` walk asks and open items.
- **Restraint:** **do not animate the open-items list.** No pulse, no accent colour, no attention treatment of any kind. It sits quiet at 70% opacity while the ask sits at full. The gaps are stated plainly because that is what makes the rest of the deck credible, and dramatising them turns honesty into a performance.
- **Reduced motion:** joined rig at final aligned state, connectors complete, motif lit, all copy present. No drift, no pulse. `1` performs an instant state swap.

---

## Part 2 — Design system

This part governs **construction, motion and hover only.** Colour, type, spacing and radii are inherited from the host design system in full. That is a deliberate constraint, not an omission, and Part 6 explains why.

### Palette — inherited, referenced by role

Do not introduce colour values. Use the host system's existing tokens, and map them to these five deck roles once, at the top of the stylesheet, so every slide references the role rather than the token:

```css
:root {
  /* Map each of these to an EXISTING host token. Do not invent values. */
  --deck-stage:      /* deepest background surface        */ ;
  --deck-stage-lift: /* one step lighter, slides 3 and 11 */ ;
  --deck-stage-inv:  /* lightest surface, slide 5 only    */ ;
  --deck-ink:        /* primary foreground                */ ;
  --deck-muted:      /* secondary foreground and borders  */ ;
  --deck-accent:     /* the system's emphasis colour      */ ;
}
```

**What each role means in this deck**, so the argument stays legible if the file is forwarded without the presenter:

| Role | Carries |
|---|---|
| `--deck-accent` | Only what Flobase uniquely owns. The five hero features, the two vectors we lead, the lit ICP band, the price. Nothing else, ever |
| `--deck-ink` | The argument. Headlines, figures, anything the presenter is speaking to |
| `--deck-muted` | Everything conceded, absent, blocked or unbuilt. The competitors' ghost columns, the wireframe assets, the empty socket, the open items on slide 14 |
| `--deck-stage` | Depth. Three surface steps only, and slide 5 is the sole inversion |

The single discipline that matters: **accent is scarce.** If the accent appears on more than one idea per slide, the slide has stopped arguing.

### Type — inherited, with one non-negotiable

Faces, weights and scale come from the host system. One override:

```css
.deck [data-numeral], .deck .fig { font-variant-numeric: tabular-nums; }
```

**Tabular figures on every numeral in the deck, without exception.** Six slides count numbers up on entry. A figure whose glyph widths change while it counts makes the number look like it is being decided rather than reported, and this is a deck about trusting numbers.

Headline scale sits at the commercial register, which in the host system's terms means the step below its largest display size. Objects land in this deck; they do not shout.

### The 3D technique

There is no shipping Flobase component to quote, so this construction is specified new. It is the standard stage / rig / face / edge / side pattern and it builds every object in the deck, from the ledger plates on slide 1 to the value slabs on slide 13.

```css
/* STAGE — one per slide. Perspective lives here, never on the moving element. */
.stage {
  perspective: 1400px;          /* 1100px on slide 10, 2400px on slide 3 */
  perspective-origin: 50% 42%;  /* slightly high: objects sit below eyeline */
  transform-style: preserve-3d;
}

/* RIG — the only element the pointer drives. One rig per slide. */
.rig {
  transform-style: preserve-3d;
  transform:
    rotateX(var(--rig-x, 0deg))
    rotateY(var(--rig-y, 0deg))
    translateZ(var(--rig-z, 0px));
  will-change: transform;        /* set on pointerenter, REMOVE on pointerleave */
}

/* SOLID — an extruded block. Five faces; the back is never seen, so never built. */
.solid { position: relative; transform-style: preserve-3d; }
.solid > .face  { transform: translateZ(calc(var(--d) / 2)); }
.solid > .back  { transform: translateZ(calc(var(--d) / -2)); }
.solid > .side-l{ transform: rotateY(-90deg) translateZ(calc(var(--w) / 2)); }
.solid > .side-r{ transform: rotateY( 90deg) translateZ(calc(var(--w) / 2)); }
.solid > .top   { transform: rotateX( 90deg) translateZ(calc(var(--h) / 2)); }

/* LIGHTING — fake it with static brightness per face. One key, upper-left.
   Never recompute lighting per frame; the constancy is what makes it read as solid. */
.face   { filter: brightness(1.00); }
.top    { filter: brightness(1.14); }
.side-l { filter: brightness(0.88); }
.side-r { filter: brightness(0.74); }
```

**Pointer parallax.** One damped loop for the entire deck. Never drive a transform from a raw pointer event.

```js
/* Targets updated by pointermove; current values chase them in ONE rAF loop.
   0.085 is the damping constant. Higher snaps, lower floats.
   Commercial register wants a slightly firm chase, so 0.085 not 0.04. */
let tx = 0, ty = 0, cx = 0, cy = 0, raf = null;

function onMove(e) {
  const r = stage.getBoundingClientRect();
  tx = ((e.clientX - r.left) / r.width  - 0.5) *  MAX_Y; // MAX_Y = 6deg
  ty = ((e.clientY - r.top ) / r.height - 0.5) * -MAX_X; // MAX_X = 4deg, inverted
  if (!raf) raf = requestAnimationFrame(tick);
}

function tick() {
  cx += (tx - cx) * 0.085;
  cy += (ty - cy) * 0.085;
  rig.style.setProperty('--rig-y', cx.toFixed(3) + 'deg');
  rig.style.setProperty('--rig-x', cy.toFixed(3) + 'deg');
  raf = (Math.abs(tx - cx) > 0.01 || Math.abs(ty - cy) > 0.01)
      ? requestAnimationFrame(tick)
      : (rig.style.willChange = 'auto', null);   // release, do not hold
}
```

**Hover, which is where this deck lives.** Every hero object uses the same three-part response, and the consistency is what makes fourteen different objects feel like one system:

1. **Lift.** The hovered element translates toward the viewer, 16 to 22px, over **180ms**. Never scale to imply lift; scale reads as a button, translate reads as an object.
2. **Recede.** Every sibling drops 10px in Z and to 40 to 55% opacity over the same 180ms. **The isolation is the information.** A hover that only affects the hovered thing tells the room nothing.
3. **Unfurl.** A detail plate rotates up from the object's base on its own X axis, `rotateX(-90deg)` to `0deg` over 220ms, 60ms after the lift begins. It rotates up from the object because it belongs to the object. It never fades in from nowhere.

On `pointerleave`, everything reverses at **140ms**, slightly faster than it arrived. Objects should settle back a little more eagerly than they lift.

### The ledger tick

Specified once here, referenced from slides 1, 6, 13 and 14, and **never explained on screen.**

Three segments in a row, each 14×4px, 3px gap, total 46×4px. Bottom-left of the stage at the deck's standard motif position, 48px from each edge. Each segment stands for one of the three records: invoice, call, policy. Unlit segments render at `--deck-muted` at 30% opacity. Lit segments render at `--deck-accent` at full.

| Slide | State | Why |
|---|---|---|
| 1 | All three unlit | The records exist and do not connect |
| 5 | All three unlit, at its quietest | Holding, so slide 6 can pay it off |
| 6 | All three light in one 220ms pass as the circuit closes | The payoff, and the centrepiece's final beat |
| 13 | All three lit, steady | The number the price is charging for |
| 14 | All three lit, with a pulse crossing them every 10s | Resolved and running |

By slide 13 the room reads it without a legend. That is the entire purpose of a motif, and it is why it must never be captioned.

### Motion principles

1. **One easing curve, everywhere:** `cubic-bezier(.22,1,.36,1)`. What varies between slides is duration and settle weight, never the curve.
2. **Durations:** entry 500 to 900ms · hover 180ms in, 140ms out · flip 420ms · impact 90 to 120ms · ambient loops 8 to 14s.
3. **Stagger between siblings: 60 to 140ms.** Below 60 reads as simultaneous, above 140 reads as slow.
4. **Ambient amplitude: ±0.25° to ±0.5° yaw.** Larger reads as broken, not alive.
5. **Nothing is ever frozen while the presenter is talking.** Every slide has an ambient state, and slide 5's ambient is deliberately the smallest in the deck rather than absent.
6. **Objects land.** This is the commercial register. Every arrival ends in a settle, not a float. Where something must feel weighty, add a 90 to 110ms scale-punch to 1.03 and let it resolve.
7. **Hold before the payoff.** Slides 3, 6, 9, 10, 11 and 13 all pause 600ms to 1.2s before their final beat. Those holds are load-bearing. A builder optimising them out will remove the deck's timing.
8. **Reduced motion ships the resolved end state,** never a degraded animation. Every slide's final frame is a complete argument on its own, which is also why the print path works.

### Build constraints

- **One self-contained HTML file.** All CSS and JS inline. Every graphic drawn in SVG or CSS. No external requests of any kind.
- **No 3D libraries and no WebGL.** CSS 3D transforms plus one `rAF` loop build every object above. A WebGL context costs crisp type, and type is what this deck is carrying.
- **Navigation:** arrow keys, click, swipe. `P` toggles presenter notes, `F` fullscreen, number keys jump to a slide, slide number bottom-right. Per-slide interaction keys are listed in each design brief and must not collide with these.
- **Performance:** hold 60fps during entry animations. Never promote more than a handful of layers with `will-change` simultaneously, and release after animating.
- **Projector safety:** minimum 22px body text, 4.5:1 contrast against the stage in the host system's terms, and nothing placed within 5% of any edge. Venue projectors crop.

### The print path

**Mandatory for this deck.** It is going to be forwarded to whoever was not in the room, and that is where the decision actually gets made.

`@media print` renders each slide as one page, 3D flattened to its resolved state, and **every hover-only detail printed inline**: the source citations on slide 3, the vector derivations on slide 8, the slab bases on slide 13, the open-item consequences on slide 14. A forwarded copy that loses its citations loses the argument, because the citations are the argument.

### Illustration direction

Everything is drawn, nothing is photographed or rendered. Line weight consistent across the deck at the host system's border width, scaled up one step for object edges so silhouettes hold at projector distance. Objects read as machined rather than sketched, which matches the commercial register and matches a product about ledgers.

**The Flobase mark appears exactly twice, on slide 1 and slide 14.** Scarcity is what makes it a mark rather than wallpaper, and here it also reinforces the loop closing.

---

## Part 3 — Master prompt

> Build a single self-contained HTML file: a 14-slide interactive presentation deck for Flobase, a life insurance agency operating system. The audience is the Flobase founder across a table on a consulting call, and the deck walks them through a completed go-to-market strategy and ends in a two-decision ask.
>
> **Register:** commercial. Objects land. Weight, settle, impact. Precision over spectacle, because this is a room where someone signs.
>
> **Inherit the design system.** Use the existing design system's colour tokens, type faces, scale, spacing and radii exactly as they are. Do not introduce new colour values, do not define a new type scale, do not restyle components that already have a style. Map the host tokens to the six deck roles declared at the top of Part 2 and reference those roles throughout. The one typographic override is `font-variant-numeric: tabular-nums` on every numeral in the deck, which is non-negotiable because six slides count numbers up on entry.
>
> **The non-negotiables:**
> - **Real 3D.** CSS 3D transforms only, using the stage / rig / face / edge / side construction and the single damped `requestAnimationFrame` pointer loop given in Part 2. No 3D libraries, no WebGL, no CDN, no external requests.
> - **Alive at rest.** Every slide has an ambient state. Nothing is frozen while the presenter is talking. Amplitudes stay at ±0.25° to ±0.5°.
> - **Hover is the interaction model.** Every hero object uses the same three-part hover: lift 16 to 22px in 180ms, siblings recede and dim, detail plate unfurls by rotating up from the object's base. Reverse at 140ms. The consistency across fourteen different objects is what makes them one system.
> - **Illustrative, never decorative.** Every graphic carries its slide's argument. On the strongest slides the motion *is* the claim: connectors that stop short on slide 1, a circuit that closes on slide 6, a plane conceded to 90° edge-on on slide 7, two journey stages merging on slide 10, a stack settling onto a price on slide 13.
> - **Respect the restraint notes.** Slides 3, 5, 7, 12 and 14 carry explicit do-not-animate instructions. They exist because the instinct to add motion there is strong and wrong. Slide 5 in particular will look unfinished next to its neighbours. It is not.
> - **Respect the holds.** Slides 3, 6, 9, 10, 11 and 13 pause before their final beat. Those pauses are the deck's timing.
> - **Reduced motion is a first-class state**, shipping the resolved end state of every animation, not a degraded version.
> - **Print path required.** `@media print` renders each slide as a page with 3D flattened and every hover-only detail inline, including all source citations.
> - **Presenter mode:** `P` for notes, `F` fullscreen, arrows and number keys to navigate, plus the per-slide interaction keys listed in each design brief.
>
> **The centrepieces to build first, because everything else is calibrated against them:** slide 6, the closing circuit, which is the deck's peak and the moment the recurring motif pays off; slide 3, the printing invoice that ends in the word `unknown` where a figure should be; and slide 14, which must return to slide 1's exact camera and stage with only the state changed, because the loop closes visually or it does not close.
>
> Use the construction pattern and the hover model in Part 2 verbatim. Take everything else, colour, type, spacing, radii, from the design system that already exists, so the deck looks like it came from the same hand as the product it is about.

---

## Part 4 — Before you present

### What's verified

- **Every competitor price on slide 3 and slide 9** is a published list price captured 2026-09-02, cited per-line in the hover state: Ricochet360 at $162 to $210 per user per month with a $585 monthly minimum, AgencyBloc AMS+ from $109 per user per month on an annual term, Agent CRM at $97 per month, EverQuote live transfers at $50 to $100+ per call.
- **Slide 7's concession is real.** Convoso's contact-rate leadership and its 47% insurance reviewer base are documented, as is Ricochet360's 75%. The deck concedes the dialing axis because the research supports conceding it.
- **Slide 8's two vectors are derived, not chosen.** Both come from repeated 1 to 3 star complaint themes across the competitor set. The derivation is one hover away on the slide itself.
- **Slide 9's three gates are the competitors' own published constraints**, not characterisations of them.
- **Every Flobase feature named** traces to `Flobase_Project_Brief.md`, which is flobase.tech's homepage as published, and every module there carries a "Live" badge.
- **The industry benchmarks** on slides 3, 11 and 13 are cited: roughly $500 cost per final expense close at an $85 transfer and 20% close, over 90% first-year agent attrition, $4,000 to $6,000 recruiting value per agent hired.

The deck does **not** claim a customer, a result, a growth rate or a retention figure, because there are none to claim.

### Six things to settle

1. **Pricing is a design, not a validated price.** If real cost-to-serve per active producing agent comes in above roughly $60 per month, the $299 Agency tier breaks its margin and slide 13's entire stack has to be rebuilt. Get the cost-to-serve number before this deck is presented to anyone but the founder.
2. **The platform fee could read as the hidden fee the site promises not to charge.** flobase.tech says "no hidden fees". A 12% fee on wallet spend is either the most credible thing on slide 13 or a direct contradiction of the homepage, and which one it is depends entirely on it being printed next to the price rather than discovered later. If the founder will not publish it, cut the fee gradient from slide 13 and reprice.
3. **"Under 1 second" routing has no measured basis.** It is on the homepage and it is not on any slide in this deck, deliberately. Before it appears in any paid channel, measure it and publish the methodology. This audience has been burned by routing claims and will test it live on a demo.
4. **"The #1 All-In-One CRM for Life Insurance Agents" has no substantiation.** It is a superiority claim to a regulated, litigious audience. It appears nowhere in this deck. Decide whether it survives in market at all.
5. **No commission processing weakens the single-tab claim at the top of the range.** ICP Level 2 will keep AgencyBloc or another AMS regardless, so "one tab" is not literally true for them. Either build it, or reposition explicitly as the layer in front of the AMS. Slide 6 currently implies the former.
6. **The competitor set was selected, not supplied.** Radius, AgencyBloc, Convoso, Ricochet360, Agent CRM and EverQuote were chosen from research to cover four budget lines. If the real evaluation set differs, slides 2, 3, 7, 8 and 9 all move.

### What was invented

Named individually, because this is the section that makes the rest of the document trustworthy.

| Invented | Where | Why it is there | What committing to it costs |
|---|---|---|---|
| The `$2,710` stack figure | Slide 3, and it is the deck's carrying number | Built by summing real list prices at a 10-seat configuration | A 10-seat assumption. It weakens below about 6 seats and the founder must not quote it for a small agency |
| The four-column category map | Slide 2 | A framing device for organising six real competitors | It is my structure, not an industry taxonomy. Nobody else describes the category this way |
| "Active producing agent" as the value metric | Slide 13 | Preserves the unlimited-seats promise while pricing on value | A metric no buyer has seen before. It needs one sentence of explanation on the pricing page forever |
| The $299 / $799 tier points and the 12-6-3 fee gradient | Slide 13 | Derived from the stack teardown and the expansion logic, not from willingness-to-pay research | Publishing a price is very hard to walk back upward. Test before you publish |
| "Five to eight design partners" | Slide 14 | A workable cohort size for the ask | An operational commitment. Someone has to run weekly calls for 90 days |
| The two-decision framing of the ask | Slide 14 | Reduces a nine-dashboard strategy to something actionable in a week | It implies everything else is ready, which is true of the assets and not yet true of the product |
| The claim that stages 3 and 4 collapse into one call | Slide 10 | Follows logically from the trial requiring no migration | Nobody has run that call yet. The first one will reveal whether it holds |

**Decide these before you say them, because this room will hold you to them.**

---

## Part 5 — The pricing model behind slide 13

Slide 13 carries tiers, so the commercial module applies. Dashboard 9 already holds the value metric analysis, the tier table and three ROI anchors. What it does **not** contain, and what slide 13 needs before it can be defended in a room, is the floor / band / ceiling derivation that produces $299 rather than asserting it.

```
FLOOR      cost_to_serve per active producing agent, fully loaded = {TBD}
           Must include: routing infrastructure, telephony minutes, lead
           marketplace supply cost, support load, payment processing.
           floor_price = cost_to_serve / (1 - target_gross_margin)

           Margin target by business shape: Flobase is NOT pure software.
           The wallet is pass-through and the marketplace carries real
           supply cost, so a blended 80% software target is wrong here.
           Use 78-82% on the platform fee and 8-14% on wallet throughput,
           and model them separately. A single blended target will
           systematically overprice the platform or underprice the wallet.

BAND       Ricochet360   $162-210/user/mo  + $585/mo minimum
           AgencyBloc    $109/user/mo       annual term
           Agent CRM     $97/mo             flat, all unlocked
           GoHighLevel   $97-497/mo         + usage wallet
           Normalized to a 10-active-agent agency:
             low $97  ·  median ~$300  ·  high $1,620

CEILING    Quantified annual value per agency (Dashboard 9, Anchor 1):
             $45,000  unattributed spend on below-breakeven producers
           x capture_fraction 0.10-0.30
           = $4,500 to $13,500/yr  =  $375 to $1,125/mo

HERO       Range = [max(floor, 97), max(1125, 1620)]
           $299/mo sits just above the normalized band median and at the
           low end of the value ceiling. That is a deliberate land-and-
           expand placement, not a value-maximising one.

DERIVED    decoy   Launch $0        (below the band, as an attraction offer)
           hero    Agency $299      (1.00x)
           hero+   Scale $799       (2.67x hero)
           anchor  IMO custom       (4.0x+ hero)
```

**Which layer governs, and why it matters.** Direct comparables exist for the CRM and dialer portion, so **the market band governs the platform fee** and the value ceiling is a footnote. No comparable exists for per-agent spend attribution, so **the value ceiling governs the wallet fee gradient** and the band is a footnote. These invert between the two halves of the same product, which is unusual and worth stating out loud on the call, because it is the reason a single per-seat price cannot express this product.

**The honest read on $299:** it is under-priced against the ceiling. It captures roughly 8% of the quantified annual value, below the 10 to 30% band. That is defensible as a deliberate entry price into a segment three competitors abandoned, and indefensible as a permanent position. Recommend testing $299, $449 and $599 across design partner conversations, and say plainly on the call that the first cohort is buying at a founding rate that will not last.

**Cash check.** At $299 with a 12-month prepay and a waived activation fee, revenue collected on signature is $3,588 against a cost to serve of `{TBD}`. This line cannot be completed without the floor number, which is why item 1 in Part 4 is item 1.

---

## Part 6 — Where the method had to bend

Two deviations from the deck-builder method, both deliberate, both requested or forced.

**1. Phase 1 excavation found no design system, and was instructed not to invent one.**

The method's highest-leverage move is lifting real palette hex values, real font stacks and a shipping 3D component's actual CSS out of the codebase, so the deck inherits the product's physics. This repo contains markdown and generated office files. There is no `globals.css`, no component library, no shipping 3D anything, and flobase.tech is not reachable from this environment to excavate its live tokens.

Independently, the instruction for this run was explicit: **do not enforce design specs, because Claude Design carries its own design system and a competing spec would create conflict.**

Those two facts point the same direction, so Part 2 inverts the method's normal behaviour. It declares no palette and no type scale, maps host tokens to six semantic deck roles instead, and spends its full weight on the two things a design system does not own and cannot supply: **the 3D construction and the motion.** Colour appears only as a role with a stated meaning, which is the minimum needed to keep the deck legible when it is forwarded without a presenter.

**What this costs:** the method's QC checklist item "palette is real hex from the codebase with real variable names" cannot pass and is not claimed. The compensating discipline is the accent-scarcity rule in Part 2, which does the job colour-mapping normally does, without setting a single value.

**2. The commercial module was invoked partially.**

Slide 13 carries pricing and tiers, which triggers the module. But the pricing strategy already exists in full in Dashboard 9, so reproducing it as Part 5 would duplicate rather than add. Part 5 therefore contains only the layer Dashboard 9 is missing, the floor / band / ceiling arithmetic that derives $299 instead of asserting it, and it stops at the cash check because the cost-to-serve floor is genuinely unknown.

**Where the module's own guidance bent:** its default margin targets assume a single business shape. Flobase is two, a software platform and a pass-through marketplace, and applying one blended margin target across both would systematically misprice one of them. Part 5 splits the target and says so, which is a departure from the module as written and, I think, the right call for this business.
