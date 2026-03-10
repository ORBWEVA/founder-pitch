---
name: pitch
description: Pitch deck and fundraising skill for founders. Use when user wants to create a pitch deck, prepare for investor meetings, write investor outreach emails, model financials for fundraising, or handle VC objections. Triggers on "pitch deck", "investor", "fundraise", "raise money", "Series A", "seed round", "VC", "angel", or /pitch commands.
---

# Pitch & Fundraise Skill

Structure your pitch, model your financials, write investor outreach, and prepare for every objection. Built for founders who need to raise — not pitch deck consultants.

## Commands

| Command | What it does |
|---------|-------------|
| `/pitch:deck` | Pitch deck structure with slide-by-slide guidance |
| `/pitch:financials` | Financial model for fundraising (projections, use of funds, assumptions) |
| `/pitch:email` | Investor outreach emails (cold, warm intro, follow-up) |
| `/pitch:objections` | VC objection scripts for the 20 most common questions |
| `/pitch:help` | Command reference |

---

## Stage 1: Pitch Deck (`/pitch:deck`)

**Goal:** Structure a pitch deck that tells a compelling, investable story in 10-15 slides.

### The Sequoia Framework (adapted)

Every great pitch deck answers these questions in this order:

```
PITCH DECK STRUCTURE
======================

SLIDE 1: TITLE
  Company name, one-line description, your name, round details
  Template: "[Company] — [what you do in <10 words]"

SLIDE 2: PROBLEM (1-2 slides)
  What pain exists? Who feels it? How bad is it?
  Rules:
    - Be specific ("QA engineers spend 4hrs/release on manual regression")
    - NOT abstract ("Software quality is hard")
    - Show the cost of inaction ($, time, risk)
    - Use a real customer quote if you have one

SLIDE 3: SOLUTION
  What do you do about it? Show, don't tell.
  Rules:
    - Product screenshot or demo (not a feature list)
    - One sentence: "We [do X] so [ICP] can [outcome]"
    - Map solution to problem directly

SLIDE 4: WHY NOW
  What changed that makes this possible/necessary today?
  Options:
    - Technology shift (AI, APIs, infrastructure)
    - Market shift (regulation, behavior change, pandemic effect)
    - Cost shift (something expensive became cheap)
    - Timing evidence (searches trending, competitors emerging)

SLIDE 5: MARKET SIZE
  TAM → SAM → SOM (top-down AND bottom-up)
  Rules:
    - Bottom-up is more credible: [# of target customers] × [price] = SAM
    - TAM from analyst reports is fine for context, not for credibility
    - SOM = what you'll realistically capture in 3-5 years
    - VCs want SAM > $1B for venture-scale

  Template:
    TAM: $___B  (total market if every possible customer bought)
    SAM: $___M  (customers you can actually reach with your model)
    SOM: $___M  (realistic 3-5 year capture)
    Bottom-up: [___K target customers] × [$___/yr] = $___M

SLIDE 6: PRODUCT / DEMO (1-2 slides)
  How it works. Screenshots, architecture, or live demo.
  Rules:
    - Show the user's workflow, not your feature list
    - Before/after: "Without us: [pain]. With us: [outcome]"
    - If technical product: one architecture slide is ok
    - Keep it visual — no bullet-point slides

SLIDE 7: TRACTION
  The most important slide. Numbers that prove momentum.
  Show (in order of impressiveness):
    1. Revenue (MRR/ARR) + growth rate
    2. User growth + engagement
    3. Retention / cohort curves
    4. Key customer logos
    5. Waitlist / LOIs (if pre-revenue)

  Rules:
    - Always show growth RATE, not just absolute numbers
    - Use a graph (up and to the right)
    - If pre-revenue: show usage metrics or LOIs
    - Never fake or exaggerate — VCs will verify

SLIDE 8: BUSINESS MODEL
  How you make money. Keep it simple.
  Include:
    - Pricing model (subscription, usage, transaction fee)
    - Current ARPU / ACV
    - Unit economics snapshot (CAC, LTV, LTV:CAC)
    - Gross margin

SLIDE 9: COMPETITIVE LANDSCAPE
  How you're different. NOT a feature comparison table.
  Best format: 2×2 positioning map (see /gtm:positioning)
  Rules:
    - Choose axes where you win
    - Include "do nothing" and "manual workaround" as competitors
    - Never say "we have no competitors" — VCs hate this
    - Show your unfair advantage, not feature checkboxes

SLIDE 10: TEAM
  Why YOU can build THIS company.
  Include:
    - Founder photos, names, roles
    - Relevant experience (not full resume — just why you're credible)
    - Founder-market fit: what experience makes you uniquely suited
    - Key hires (if notable)
    - Advisors (only if name-brand relevant)

SLIDE 11: FINANCIALS (summary)
  High-level projections. Detail goes in /pitch:financials.
  Show:
    - Current MRR/ARR
    - 3-year projection (annual)
    - Key assumptions (growth rate, churn, ARPU changes)
    - Path to profitability (or next milestone)

SLIDE 12: THE ASK
  What you're raising and what it buys.
  Include:
    - Round size: $___
    - Use of funds (3-4 buckets, percentages)
    - Milestones this capital gets you to
    - Expected runway

  Template:
    Raising: $___M [seed/Series A]
    Use of funds:
      Engineering:  ___%  (ship [feature/milestone])
      Sales/Mktg:   ___%  (reach [customer milestone])
      Operations:   ___%  (hire [key roles])
      Buffer:       ___%

    This gets us to: [milestone] by [date]

OPTIONAL SLIDES:
  - Customer testimonials / case studies
  - Product roadmap (next 12 months only)
  - Partnership / distribution advantages
  - Regulatory / IP advantages
```

### Deck Anti-Patterns

```
COMMON MISTAKES
================
[ ] Too many slides (>15). Edit ruthlessly.
[ ] Feature list instead of outcome. "We have X" → "X lets you [outcome]"
[ ] TAM from Google search. Do bottom-up math.
[ ] No traction slide. Even pre-revenue, show SOMETHING.
[ ] "No competitors." You have competitors. At minimum: do nothing, spreadsheets, manual process.
[ ] Wall of text. If a slide needs >20 words, split it or use visuals.
[ ] Asking for too little. Under-raising signals lack of ambition.
[ ] Asking for too much. Over-raising at seed = over-dilution.
[ ] No "Why Now." Without timing, the idea could have been built 5 years ago.
[ ] Team slide with no founder-market fit. "We're smart" isn't enough.
```

### Output
Deliver: Slide-by-slide deck outline with specific content for each slide, tailored to the user's product and stage.

---

## Stage 2: Financial Model (`/pitch:financials`)

**Goal:** Build a credible financial model that supports your raise narrative.

### Revenue Projection

```
REVENUE MODEL
==============
Model type: [SaaS / Marketplace / Transaction / Usage-based]

ASSUMPTIONS (be explicit — VCs will challenge these):
  Starting MRR:                    $___
  New customers/month (Month 1):   ___
  Customer growth rate:            ___% MoM
  ARPU:                            $___/mo
  Monthly churn:                   ___%
  ARPU expansion rate:             ___%/year
  Pricing change planned:          [yes/no, when, amount]

PROJECTION:
           | Year 1    | Year 2    | Year 3
───────────┼───────────┼───────────┼──────────
Customers  | ___       | ___       | ___
MRR (end)  | $___      | $___      | $___
ARR (end)  | $___      | $___      | $___
Growth     | ___x      | ___x      | ___x
Revenue    | $___      | $___      | $___
```

### Cost Structure

```
COST STRUCTURE
===============
                    | Year 1    | Year 2    | Year 3
────────────────────┼───────────┼───────────┼──────────
COGS                |           |           |
  Hosting/infra     | $___      | $___      | $___
  Support           | $___      | $___      | $___
  3rd party APIs    | $___      | $___      | $___
Gross Margin        | ___%      | ___%      | ___%

OPEX                |           |           |
  Engineering       | $___      | $___      | $___
  Sales & Marketing | $___      | $___      | $___
  G&A               | $___      | $___      | $___
Total OPEX          | $___      | $___      | $___

NET                 |           |           |
  Net Income        | ($__)     | ($__)     | $___
  Burn Rate         | $___/mo   | $___/mo   | $___/mo
  Cash Required     | $___      | $___      | —
```

### Use of Funds Bridge

```
USE OF FUNDS
=============
Raising: $___

Category        | Amount  | %    | What it buys
────────────────┼─────────┼──────┼──────────────────
Engineering     | $___    | ___%  | [X engineers for Y months → ship Z]
Sales/Marketing | $___    | ___%  | [CAC × target customers = $X spend]
Operations      | $___    | ___%  | [Key hires: roles]
Buffer          | $___    | ___%  | [runway cushion]

Runway with this capital: ___ months
Milestone this reaches:   [specific, measurable milestone]
```

### Assumptions Stress Test

```
SENSITIVITY ANALYSIS
======================
What if growth is 50% slower?
  → Revenue at Year 3: $___  (vs base case $__)
  → Extra runway needed: ___ months

What if churn is 2x higher?
  → Customer count at Year 3: ___  (vs base case ___)
  → LTV impact: $___  (vs base case $__)

What if CAC is 50% higher?
  → LTV:CAC drops to ___x
  → Break-even pushes to ___

WHICH ASSUMPTION MATTERS MOST? ___
(This is what VCs will challenge. Know your answer.)
```

### Output
Deliver: Revenue projection + cost structure + use of funds + sensitivity analysis + key assumptions highlighted.

---

## Stage 3: Investor Outreach (`/pitch:email`)

**Goal:** Write emails that get meetings — not emails that get archived.

### Email Types

#### Cold Email to VC

```
COLD VC EMAIL
==============
Subject: [Company] — [one-line traction hook]

Hi [Name],

[1 sentence: why you're emailing THIS investor — their thesis, portfolio, or public statement]

[2 sentences: what you do + traction proof point]

[1 sentence: the ask — intro meeting, not "pick your brain"]

[Signature with LinkedIn]
```

**Good example:**
```
Subject: Loka — 18% MoM growth, AI-native language learning

Hi [Name],

Your investment in [Portfolio Co] caught my eye — we're tackling
the same insight that language learning needs to be conversational,
not memorization.

Loka uses AI tutors for real-time conversation practice. We're at
$34K MRR growing 18% MoM with 2,100 active learners across 3 languages.

Would love 20 minutes to share what we're seeing. Free Tuesday or Thursday?

Ryan Ahamer
CEO, LokaLingo
```

**Bad example:**
```
Subject: Exciting opportunity

Hi, I hope this finds you well! We're building an AI-powered
platform that's revolutionizing how people learn languages.
We've had amazing traction and our team is incredibly passionate.
I'd love to pick your brain about our space...
```

#### Warm Intro Request

```
WARM INTRO EMAIL (to connector)
=================================
Subject: Intro request — [VC name] at [fund]

Hi [Connector],

Quick ask: would you be comfortable introducing me to [VC name]
at [Fund]?

Context: We're raising a [$X] [seed/A] for [Company]. [1 sentence
of traction]. [VC name] invests in [their thesis match].

I've attached a short blurb you can forward if easier. No pressure
if the timing isn't right.

Thanks,
[Name]

---
FORWARDABLE BLURB:
[Name] is the CEO of [Company], which [one sentence of what + traction].
They're raising [$X] and I thought you'd be a great fit given
your work in [thesis area]. Happy to connect you if interested.
```

#### Follow-Up (after no response)

```
FOLLOW-UP EMAIL (Day 5-7)
===========================
Subject: Re: [original subject]

Hi [Name],

Following up — wanted to share one update: [new traction data point
or milestone since first email].

Still interested in a quick conversation if you are.

[Name]
```

Rules:
- Max 2 follow-ups. After that, move on.
- Each follow-up adds NEW information (traction update, press mention, new customer)
- Never: "Just bumping this to the top of your inbox"

### Investor List Building

```
INVESTOR TARGETING
===================
For each potential investor, score:

Investor         | Thesis fit | Stage fit | Check size | Portfolio conflict | Warm path?
─────────────────┼────────────┼───────────┼────────────┼────────────────────┼──────────
[Fund/Angel]     | /5         | /5        | $___       | [yes/no]           | [yes/no]

PRIORITIZE:
  Tier 1: Warm intro + thesis fit + right stage (pitch first? no — practice on Tier 2)
  Tier 2: Thesis fit + right stage, no warm path (pitch these first for practice)
  Tier 3: Right stage, weak thesis fit (backup)

TIMING: Run 10-15 meetings in 2-3 weeks. Create urgency, not a drip campaign.
```

### Output
Deliver: Customized cold email + warm intro template + follow-up sequence + investor targeting framework.

---

## Stage 4: Objection Handling (`/pitch:objections`)

**Goal:** Prepare for every hard question a VC will ask.

### The 20 Most Common VC Objections

```
VC OBJECTION SCRIPTS
======================

MARKET
───────
1. "The market is too small."
   Framework: Show SAM expansion path. "Today's SAM is $X. But [trend]
   expands it to $Y by [year]. [Example of another company that grew
   their market.]"

2. "This is a feature, not a company."
   Framework: Show platform potential. "Today we do X. But we're building
   toward [platform vision]. [Company] started as [small thing] too."

3. "Isn't [Big Co] going to build this?"
   Framework: Counter-positioning. "[Big Co] can't do this without
   [cannibalizing revenue / restructuring / alienating customers].
   We're purpose-built for [ICP]."

4. "There's no moat."
   Framework: Moat-in-progress. "Today our advantage is [X]. We're
   building toward [network effect / data advantage / switching costs]
   as we scale. Here's how: [specific mechanism]."

TRACTION
─────────
5. "You don't have enough traction."
   Framework: Leading indicators. "Revenue is early, but [engagement
   metric] shows [X]. Our retention curve flattens at [Y%], which
   mirrors [successful company] at this stage."

6. "Growth is slowing."
   Framework: Explain the phase. "We grew [X%] in [channel]. We're
   now investing in [new channel] which ramps slower but scales
   further. Early signal: [data point]."

7. "Your churn is too high."
   Framework: Segment and show improvement. "Overall churn is [X%],
   but in [best segment] it's [Y%]. We've identified the driver
   and [specific fix] has improved retention by [Z%] over [period]."

8. "How do I know this isn't a one-time spike?"
   Framework: Cohort consistency. "Here's our cohort retention —
   each cohort retains at [X%] after [Y months]. This isn't viral
   luck, it's product value."

BUSINESS MODEL
───────────────
9. "Your unit economics don't work."
   Framework: Trajectory. "Today LTV:CAC is [X]x. But CAC is
   dropping as [organic channel grows / brand builds] and LTV is
   rising as [expansion / retention improves]. By [month], we
   project [Y]x."

10. "Why is the price so low / high?"
    Framework: Value anchor. "Our price is [X% of the value we
    create]. Customer [name] saves [$Y/month] using us and pays
    [$Z]. That's [ROI]x return."

11. "How will you monetize free users?"
    Framework: Conversion path. "Free users convert at [X%] after
    [trigger event]. We see [Y%] of free users hit that trigger
    within [Z weeks]. Projected paid conversion: [W%] at scale."

12. "This business won't be venture-scale."
    Framework: Math the path. "At [realistic market share] of SAM,
    with [ARPU], we reach $[X]M ARR. [Comparable company] achieved
    [similar trajectory] and reached [$Y] valuation."

TEAM
─────
13. "You don't have a technical co-founder."
    Framework: Show shipping velocity. "I've built [X] and shipped
    [Y] in [Z months] with [team structure]. Here's the product.
    We're hiring a CTO and [name/profile] is in final conversations."

14. "You've never done this before."
    Framework: Founder-market fit. "I haven't built a startup, but
    I've spent [X years] in [industry] where I [specific relevant
    experience]. I know this customer because I WAS this customer."

15. "Why should I bet on you over [competitor team]?"
    Framework: Unique insight. "We have [insight about the customer /
    market / technology] that competitors don't. Here's proof: [data
    point or customer quote that validates the insight]."

RISK
─────
16. "What if [Big Tech] enters this space?"
    Framework: Speed + focus. "They'd need [X months] to build this.
    By then we'll have [Y customers, Z data, W integrations]. Our
    focus is our speed — they have 100 priorities, we have one."

17. "What's the regulatory risk?"
    Framework: Be honest + prepared. "The risk is [X]. We've
    [consulted counsel / built compliance into the product /
    received [certification]]. Here's our regulatory roadmap."

18. "What happens if you can't raise your next round?"
    Framework: Default alive. "At current growth, we hit break-even
    in [X months] with [Y% cut]. We can be default alive. We're
    raising to accelerate, not to survive."

THE ASK
────────
19. "The valuation is too high."
    Framework: Comparable + trajectory. "[Company at similar stage]
    raised at [X multiple]. Our growth rate is [Y%] vs their [Z%]
    at the same point. We're pricing in [6 months of continued
    execution]."

20. "I need to see more before committing."
    Framework: Create urgency (honestly). "Understood. We're targeting
    [close date] with [X%] committed. I'll share [monthly update /
    specific milestone] by [date]. What would you need to see?"
```

### Objection Handling Framework

For ANY question not in the top 20:

```
OBJECTION RESPONSE FRAMEWORK
==============================
1. ACKNOWLEDGE: "That's a fair question." (never defensive)
2. REFRAME: Turn the objection into your narrative
3. EVIDENCE: Specific data point or customer proof
4. BRIDGE: Connect back to your strongest slide
```

### Pre-Meeting Prep Checklist

```
MEETING PREP
==============
[ ] Researched the VC's portfolio — know their thesis
[ ] Identified 1-2 portfolio companies relevant to you
[ ] Know their typical check size and stage
[ ] Prepared your 30-second verbal pitch
[ ] Have 3 specific traction numbers memorized
[ ] Know your top 3 likely objections for THIS investor
[ ] Prepared 2-3 questions to ask THEM
[ ] Deck sent in advance (if requested) or ready to share
```

### Output
Deliver: Customized objection scripts for their specific product + pre-meeting prep checklist + tailored responses for their most likely objections.

---

## Integration Notes

- **Feeds from Startup Metrics:** `/startup:ready` identifies gaps → `/pitch:deck` builds the narrative around strengths
- **Feeds from Startup Metrics:** `/startup:unit` provides numbers → `/pitch:financials` projects them forward
- **Feeds from GTM:** `/gtm:positioning` defines ICP → `/pitch:deck` Slide 2-3 uses that positioning
- **Feeds to Outreach:** `/pitch:email` pairs with `/gtm:outreach` (same SPARK principles, different audience)

## Principles

1. **Traction is the pitch.** Everything else is context for the numbers.
2. **Specificity > ambition.** "$34K MRR growing 18% MoM" beats "huge market opportunity."
3. **Acknowledge, don't dodge.** VCs respect founders who know their weaknesses.
4. **The deck gets the meeting. The meeting gets the money.** Don't put everything in the deck.
5. **Raise when you can, not when you must.** Strong position = better terms.
