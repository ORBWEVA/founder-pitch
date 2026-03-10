# founder-pitch

Pitch deck and fundraising skill for Claude Code. Structure your deck, model financials, write investor emails, and handle every VC objection.

## What's inside

One skill set, 5 slash commands:

| Command | What it does |
|---------|-------------|
| `/pitch:deck` | Pitch deck structure with slide-by-slide guidance (Sequoia framework) |
| `/pitch:financials` | Financial model for fundraising — projections, use of funds, sensitivity analysis |
| `/pitch:email` | Investor outreach emails — cold VC, warm intro, follow-up sequences |
| `/pitch:objections` | VC objection scripts for the 20 most common investor questions |
| `/pitch:help` | Command reference |

## Install

```bash
npx skills add ORBWEVA/founder-pitch
```

Or manually copy:
- `skills/` -> `~/.claude/skills/`
- `commands/` -> `~/.claude/commands/`

## Example output

### `/pitch:deck` for a SaaS product

```
PITCH DECK OUTLINE
====================

SLIDE 1: TITLE
  Loka — AI-native language learning through real conversation
  Ryan Ahamer, CEO | Raising $2M Seed

SLIDE 2: PROBLEM
  Language learners spend 200+ hours on apps that teach vocabulary
  but can't hold a 5-minute conversation. 73% of Duolingo users
  quit within 30 days because memorization ≠ fluency.

SLIDE 3: SOLUTION
  Loka pairs learners with AI tutors for real-time conversation
  practice. Adaptive difficulty, instant correction, unlimited
  patience. "We do X so language learners can speak confidently
  in 90 days, not 900."

SLIDE 4: WHY NOW
  GPT-4 made real-time conversational AI possible at <$0.02/session.
  Two years ago this would cost $2/session — uneconomic for consumer.

SLIDE 5: MARKET SIZE
  TAM: $12.5B  (global language learning market)
  SAM: $890M   (online conversation-focused, 3 target languages)
  SOM: $45M    (2,100 users × $150/yr ARPU × growth trajectory)
  Bottom-up: 300K target learners × $150/yr = $45M

...

DECK SCORE: 8/12 slides strong. Gaps: Traction slide needs
cohort retention graph. Competitive slide needs 2×2 positioning map.
```

### `/pitch:email` for investor outreach

```
COLD VC EMAIL
==============
Subject: Loka — 18% MoM growth, AI-native language learning

Hi Sarah,

Your investment in TalkSpace caught my eye — we're tackling the same
insight that real conversation drives outcomes, not content consumption.

Loka uses AI tutors for real-time conversation practice. We're at
$34K MRR growing 18% MoM with 2,100 active learners across 3 languages.

Would love 20 minutes to share what we're seeing. Free Tuesday or Thursday?

Ryan Ahamer
CEO, LokaLingo

PERSONALIZATION: Level 4 (portfolio thesis match + specific reference)
```

## How the commands connect

```
STRUCTURE:  /pitch:deck        → build the narrative
MODEL:      /pitch:financials   → back it with numbers
OUTREACH:   /pitch:email        → get meetings
CLOSE:      /pitch:objections   → handle every hard question
```

1. **Structure** — deck builds the investable story slide by slide
2. **Model** — financials provide the numbers VCs will scrutinize
3. **Outreach** — emails get you in the room with the right investors
4. **Close** — objection scripts prepare you for every curveball

## Pairs with other ORBWEVA skills

| Skill | How it connects |
|-------|----------------|
| [dt-skill](https://github.com/ORBWEVA/dt-skill) | Design Thinking validates the problem before you pitch it |
| [gtm-skills](https://github.com/ORBWEVA/gtm-skills) | `/gtm:positioning` feeds deck slides 2-3, `/gtm:outreach` uses same SPARK principles |
| [founder-metrics](https://github.com/ORBWEVA/founder-metrics) | `/startup:ready` identifies gaps, `/startup:unit` feeds financials |

## Full founder stack

Install all four skill sets:

```bash
npx skills add ORBWEVA/dt-skill
npx skills add ORBWEVA/gtm-skills
npx skills add ORBWEVA/founder-metrics
npx skills add ORBWEVA/founder-pitch
```

## Security

Zero executable code. Pure markdown — structured prompts that guide Claude's thinking. No scripts, no dependencies, no API calls, no shell commands.

```
skills/pitch/SKILL.md          # Pitch methodology (4 stages)
commands/pitch/*.md            # 5 slash commands
package.json                   # metadata only
```

## License

MIT
