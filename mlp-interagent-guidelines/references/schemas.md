# Schemas

Canonical formats for all memory files and structured outputs defined in the interagent guidelines.

---

## context.md

Owned by the CEO. Rewritten at start and end of each day after synthesizing all agent reports.

```markdown
# Context — YYYY-MM-DD

## Strategy
[One paragraph. What we are trying to achieve and why. Stable unless strategy changes.]

## Current Priorities
1. [Highest priority item — who owns it, what state it's in]
2. [Second priority]
3. [...]

## Active Blockers
- [Blocker description] — Owner: [role/agent] — Unblock: [specific action needed]

## Decisions Made Today
- [Decision] — Rationale: [why]

## Flags from Agents
- [Role]: [conflict or anomaly flagged, with issue ref if applicable]

## What Changed Since Last Context
[Brief delta from previous context.md — what shifted, what resolved, what is new]
```

---

## `<role>-definition.md`

Written at hire by the hiring agent. Updated only on role change. Read by the agent on first heartbeat or when role is unclear.

```markdown
# <Role> Definition

## Role
[Title and one-sentence mandate]

## Reporting Line
Reports to: [manager role/agent name]
Manages: [direct reports if any]

## Capabilities
[What this agent is authorized to do — issue creation, hiring, approvals, external calls, etc.]

## Out of Scope
[What this agent must not do — explicit boundaries]

## Key Relationships
- [Other role]: [nature of relationship — delegates to, reviews output of, blocked by, etc.]

## Hiring Notes
[Date hired, hiring agent, any context about why this role was created]
```

---

## `<role>-summary.md`

Owned and maintained by that role's agent. Rewritten (not appended) at the end of each heartbeat. This is the primary orientation file loaded at the start of every heartbeat.

```markdown
# <Role> Summary — last updated YYYY-MM-DD

## Current State
[One paragraph. What I am working on right now and what state it's in.]

## Active Tasks
- [Issue ref + title] — status: [in_progress/blocked/in_review]
- [...]

## Known Blockers
- [Blocker] — waiting on: [who/what]

## Next Action
[The single most important thing I will do in my next heartbeat]

## Recent Discoveries
[Facts learned in last 1-3 heartbeats that are worth loading quickly — workspace IDs, agent configs, env facts]
```

---

## `<role>-log.md`

Owned by that role's agent. Append-only. Never rewritten or deleted. Each entry is timestamped. This is the source of truth for end-of-day reports and summary rewrites.

```markdown
# <Role> Log

---
## YYYY-MM-DD HH:MM

**Did:** [What was done this heartbeat]
**Discovered:** [Any environment facts, IDs, configs worth preserving]
**Decided:** [Any decisions made, with alternatives considered]
**Conflict:** [Any mismatch between context.md and live state — optional, only when present]
**Next:** [What happens next and who owns it]

---
## YYYY-MM-DD HH:MM

[next entry...]
```

---

## End-of-Day Report

Posted as a comment on the CEO's daily report issue. Drawn from the log. Must be structured consistently so the CEO can synthesize without parsing prose.

```markdown
## <Role> Report — YYYY-MM-DD

**Completed:** [What finished this cycle — issue refs preferred]
**In Progress:** [Actively being worked — issue refs + current state]
**Blocked:** [What is stuck — blocker description + who owns the unblock]
**Flags:** [Conflicts, anomalies, or things CEO should know — be specific]
```

**Rules:**
- One report per agent per day.
- If nothing to report, post: `## <Role> Report — YYYY-MM-DD — Nothing to report.`
- Never post silence. Silence is not a report.
- Keep it short. The CEO reads all agents' reports before synthesizing.

---

## Log Entry — Conflict Flag

When `context.md` contradicts live state, the log entry must name both sides explicitly:

```
**Conflict:** context.md says [X]. Issue thread / API says [Y]. Proceeding with [Y] for tactical decision. Flagged for CEO.
```

This becomes a **Flag** in the end-of-day report so the CEO can resolve it in the next `context.md` rewrite.
