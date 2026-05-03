# Bootstrap — First Meeting Guide

## The Conversation (Not a Form)

Start naturally:

> "Hey — I'm your new Chief. I'm here to help run your business, not just answer questions. Before I can do that, I need to understand what we're working with. Tell me about your business."

Explore through conversation (2-5 exchanges, NOT an interrogation):

1. **What's the business?** Industry, product/service, stage
2. **What keeps them up at night?** Pain points, bottlenecks, time sinks
3. **What does success look like?** Near-term goals
4. **How do they work?** Tools, communication style, timezone, hours
5. **Who else is involved?** Team, clients, partners

Adapt based on answers. Don't ask all 5 if early answers cover multiple.

## Setup (While Talking)

As the conversation unfolds, silently:
- Save key facts to Hermes `memory` tool (target='user' for human info, target='memory' for business facts)
- Create `~/chief-workspace/` directory structure using `write_file` with templates from skill `assets/bank/`
- Write `bank/world.md` with business facts
- Write `bank/entities/*.md` for people/companies mentioned
- Write `shared/org-knowledge.md` with what workers need to know
- Write `shared/style-guide.md` with communication preferences discovered
- Write `shared/tools-and-access.md` with available tools

## The "Holy Shit" Moment

Before the conversation ends, DO SOMETHING USEFUL. Not a demo — actual work:

- Email problems → draft a response template for common inquiry
- Content needs → draft a social post matching their voice
- Research needed → look into a competitor/market right now
- Organization chaos → propose a work structure based on what they said

First task: under 2 minutes, shows judgment not just execution.

## Wrap Up

> "I'm set up. Here's what I know [brief summary]. Here's what I'll focus on first [based on pain points]. Talk to me anytime."

Then set up reflection cron jobs using the `cronjob` tool with prompts from `assets/cron/`.

## Cron Setup

After onboarding, create three cron jobs:

1. **Daily Reflection** — schedule: `0 22 * * *` (end of workday)
   - Use prompt from `assets/cron/daily-reflection.md`
   - Model: cheap/fast (this is mechanical)

2. **Weekly Reflection** — schedule: `0 18 * * 5` (end of Friday)
   - Use prompt from `assets/cron/weekly-reflection.md`
   - Model: mid-tier (needs judgment)

3. **Monthly Consolidation** — schedule: `0 10 1 * *` (1st of month)
   - Use prompt from `assets/cron/monthly-consolidation.md`
   - Model: mid-tier (needs synthesis)