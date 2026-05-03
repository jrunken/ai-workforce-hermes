# Operational Patterns

## Worker Specialization

Track what works. Over time, worker configurations develop profiles in `bank/experience.md`:

```
## Worker Patterns That Work
- Research tasks: delegate_task with web toolset + "cite all sources" → 90% usable first try
- Content drafts: delegate_task with org-knowledge + style-guide context → needs tone fixes 40% of time
- Data extraction: delegate_task with specific format instructions → 95% accurate
- Competitor analysis: parallel delegate_task with web toolset → good but consider parallel

## Worker Patterns That Don't Work
- Vague research prompts → hallucinations
- Long content tasks without style-guide context → always needs rewrite
- Multiple questions in one worker task → misses later items
```

Use these patterns to improve future delegations. During weekly reflection, review worker success rates and update patterns.

## Memory Decay Rules

Not all memories age equally. During reflection, apply decay:

- **Referenced this week** → keep, full relevance
- **Referenced this month** → keep, review during monthly consolidation
- **Not referenced in 30+ days** → flag as stale in bank/index.md
- **Not referenced in 60+ days** → archive to memory/archive/ (daily logs) or bank/archive/ (entities)
- **Not referenced in 90+ days** → aggressive pruning from Hermes memory tool

**Exceptions (never decay):**
- Business rules and constraints (bank/world.md)
- Trust history (bank/trust.md)
- Human preferences and personal context (Hermes memory tool, target='user')
- Active processes (bank/processes.md entries used in last 60 days)

**Confidence-weighted:** Opinions in bank/opinions.md with confidence < 0.3 that haven't been updated in 30+ days → remove. The Chief should hold fewer, higher-confidence opinions over time.

## Audit Trail Format

Log significant actions in `memory/YYYY-MM-DD.md` with accountability context:

```
## 14:30 — Sent competitor analysis to human
- Trust level: notify (research tasks)
- Workers used: delegate_task, 2 parallel web research subagents
- Reviewed: yes, rewrote summary for brevity
- Cost: ~$0.15

## 15:45 — Proposed email draft to Client X
- Trust level: propose (external communications)
- Awaiting human approval
- Flagged because: first contact with this client
```

When trust is earned through track record, the track record needs to be auditable. During reflection, these logs feed trust progression decisions.