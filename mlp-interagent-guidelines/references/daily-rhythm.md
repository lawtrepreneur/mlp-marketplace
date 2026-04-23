# Daily Rhythm

The end-of-day synthesis cycle that keeps `context.md` current and agents oriented.

---

## Overview

```
CEO routine fires (cron, end of day)
  ↓
CEO creates one child report issue per sub-agent
  ↓
Each sub-agent wakes, appends to their log, posts structured report as issue comment
  ↓
CEO wakes on issue_children_completed (or timeout)
  ↓
CEO reads all <role>-summary.md files + report comments
  ↓
CEO rewrites context.md, marks report issues done
  ↓
Next heartbeat: each agent reads context.md + their own summary to orient
```

---

## CEO Routine Setup

Create this routine once during strategy initialization. Assign it to the CEO agent.

```json
{
  "title": "Daily agent synthesis",
  "assigneeAgentId": "<ceo-agent-id>",
  "projectId": "<project-id>",
  "status": "active",
  "concurrencyPolicy": "coalesce_if_active",
  "catchUpPolicy": "skip_missed"
}
```

Add a schedule trigger:

```json
{
  "kind": "schedule",
  "cronExpression": "0 17 * * 1-5",
  "timezone": "<company-timezone>"
}
```

Adjust `cronExpression` to match the team's end-of-day. Weekdays only shown above — adapt as needed.

---

## CEO Heartbeat: End-of-Day Synthesis

When the routine fires, the CEO agent follows this procedure:

### Step 1 — Create report issues

For each active sub-agent in the strategy, create a child issue:

```json
{
  "title": "<Role> daily report — YYYY-MM-DD",
  "assigneeAgentId": "<role-agent-id>",
  "parentId": "<ceo-routine-issue-id>",
  "goalId": "<strategy-goal-id>",
  "status": "todo",
  "priority": "high"
}
```

### Step 2 — Wait for completion

Rely on `issue_children_completed` wake. Do not poll.

**Timeout rule:** If the wake does not arrive within the configured window (recommend 30 minutes), synthesize regardless. Note missing reporters in `context.md` under Flags.

### Step 3 — Synthesize context.md

Read in this order:
1. Each `<role>-summary.md` — for current state per agent
2. Each report issue comment — for completed/blocked/flags delta
3. Previous `context.md` — for what changed vs. yesterday

Rewrite `context.md` using the schema in `references/schemas.md`. Do not append — rewrite the whole file. Always update the date at the top.

### Step 4 — Close report issues

Mark each child report issue `done` with a brief comment confirming synthesis complete.

---

## Sub-Agent Heartbeat: End-of-Day Report

When a report issue is assigned, the sub-agent follows this procedure:

### Step 1 — Append to log

Add a log entry to `<role>-log.md` covering the day's work. Use the log entry schema from `references/schemas.md`.

### Step 2 — Rewrite summary

Update `<role>-summary.md` to reflect current state. This is what loads next heartbeat — make it accurate.

### Step 3 — Post report comment

Post the structured end-of-day report as a comment on the report issue. Use the report schema from `references/schemas.md`.

### Step 4 — Close the issue

Mark the report issue `done`.

---

## Start-of-Day Orientation

There is no separate start-of-day routine. Agents orient themselves at the start of their first heartbeat each day by reading:

1. `context.md` — what changed overnight, current priorities
2. `<role>-summary.md` — where they personally left off
3. Their assigned issues — what is actionable now

This is covered by Guideline 1 (Check Context Before Acting). No extra API calls needed if these files are current.

---

## Strategy Initialization

When a new strategy is created, the initiating agent (typically CEO or manager) must:

1. Create `plans/<strategy>/context.md` with initial strategic intent
2. For each role being hired, create `plans/<strategy>/<role>-definition.md` at hire time
3. Create the CEO daily synthesis routine (see above)
4. Brief each agent on the file structure location so they know where to write

Agents create their own `<role>-summary.md` and `<role>-log.md` on their first heartbeat.

---

## File Location Convention

All strategy memory files live under `plans/` at the project root — outside personal agent memory — so all agents in the strategy can read them.

```
plans/
  <strategy-name>/
    context.md
    <role>-definition.md
    <role>-summary.md
    <role>-log.md
```

Use the strategy name consistently across all agents. If unsure of the strategy name, check `context.md` at the root of `plans/` or ask the CEO.
