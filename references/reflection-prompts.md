# Reflection Cycle Prompts

Use these as cron job prompts with the Hermes `cronjob` tool.

## Daily Reflection

Schedule: `0 22 * * *` (end of each working day)

```
Run daily reflection for the AI Workforce Chief. Today's date: use current date.

1. Read today's daily log (~/chief-workspace/memory/YYYY-MM-DD.md). If none exists, exit.
2. Extract key learnings → append to ~/chief-workspace/bank/experience.md (2-3 bullets max)
3. Update ~/chief-workspace/bank/opinions.md — confirm/contradict existing opinions, adjust confidence
4. Update ~/chief-workspace/bank/trust.md — log task outcomes, promote if 3+ consecutive successes
5. Update ~/chief-workspace/bank/entities/*.md — new people/projects? Update existing? Update bank/index.md
6. Update Hermes memory tool with any high-value cross-session facts
7. Prune Hermes memory if too many entries — keep only durable facts
8. Append ## Reflection section to today's daily log (3-5 sentences)

Rules: Don't fabricate events. Don't change trust without evidence. Be honest about mistakes.
```

## Weekly Reflection

Schedule: `0 18 * * 5` (end of Friday)

```
Run weekly reflection for the AI Workforce Chief.

1. Read past 7 days of daily logs (~/chief-workspace/memory/YYYY-MM-DD.md)
2. Write weekly summary → ~/chief-workspace/memory/weekly/YYYY-WXX.md
   Include: Highlights, Wins, Misses, Trust Changes, Patterns Noticed, Next Week Focus
3. Review trust progression in ~/chief-workspace/bank/trust.md — promote/demote based on full week evidence
4. Review ~/chief-workspace/bank/opinions.md — adjust confidence, remove stale low-confidence items
5. Check entity staleness in ~/chief-workspace/bank/entities/ — flag items not referenced in 30+ days
6. Review ~/chief-workspace/bank/processes.md — new SOPs from repeated tasks? Existing ones need updating?
7. Check if ~/chief-workspace/shared/ files still match reality — update if needed
8. Review worker delegation success rates — update patterns in bank/experience.md

Rules: Weekly summaries must be standalone. Be brutally honest about misses.
```

## Monthly Consolidation

Schedule: `0 10 1 * *` (1st of each month)

```
Run monthly consolidation for the AI Workforce Chief.

1. Read all weekly summaries from this month
2. Write monthly summary → ~/chief-workspace/memory/monthly/YYYY-MM.md
   Include: Summary (2-3 paragraphs), Key Achievements, Key Learnings, Trust State, Opinion Shifts, Entity Changes, Recommendations
3. Archive daily logs older than 60 days → ~/chief-workspace/memory/archive/YYYY/MM/
4. Deep prune Hermes memory — remove entries that are no longer relevant
5. Archive entities inactive 90+ days → ~/chief-workspace/bank/archive/
6. Review ~/chief-workspace/bank/processes.md — remove unused processes (60+ days)

Rules: Monthly summaries are historical record — be comprehensive. Archive, never delete.
```

## Capability Audit (Monthly, after consolidation)

```
Run monthly capability audit for the AI Workforce Chief.

1. Read ~/chief-workspace/bank/capabilities.md
2. List all currently available Hermes tools and skills
3. For each tool/skill, ask: "How could this help the business given what I know from bank/world.md?"
4. Update the Available table with any new entries
5. Review Gaps — any now solvable with current tools?
6. Review Proposed — any approved but not implemented? Set them up.
7. Add 1-2 Expansion Ideas based on recent work patterns from bank/experience.md
8. Propose new capability uses to the human (max 2 per month — don't overwhelm)
```