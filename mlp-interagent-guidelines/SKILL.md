---
name: mlp-interagent-guidelines
description: Behavioral guidelines for multi-agent systems to reduce token waste, prevent scope bleed, and maintain persistent context across heartbeats. Use this skill whenever you are operating as part of a multi-agent team, receiving delegated work from another agent, coordinating sub-agents, synthesizing agent reports, or building/hiring agents that will work in a team. Also apply when designing agent workflows, writing agent instructions (AGENTS.md), or reviewing agent behavior for correctness. These guidelines define how agents check context before acting, maintain minimum footprint, write durable memory, report clearly, and verify outcomes.
license: MIT
---

# Interagent Guidelines

Behavioral guidelines to reduce common failure modes in multi-agent systems. Adapted from Karpathy's coding guidelines for the interagent context.

**Tradeoff:** These guidelines bias toward caution over speed. For trivial single-heartbeat tasks, use judgment.

For memory file schemas and log/report formats, see `references/schemas.md`.
For the daily rhythm and CEO routine setup, see `references/daily-rhythm.md`.

---

## 1. Check Context Before Acting

**Don't rediscover what you already know. Don't trust what you can't verify.**

Before making any API call or starting work:

- Read `context.md` first. It is the CEO's synthesized view of current state, priorities, and known blockers. If it answers your question, stop there.
- Read your `<role>-summary.md` next. It tells you where you left off.
- Only reach for the network when context files are silent, stale, or the task requires live state (e.g. issue status, workspace URL).
- If `context.md` contradicts your issue thread, **the issue thread wins for tactical decisions**. Log the conflict explicitly — do not silently pick one.

The test: "Could I answer this from files I already have?" If yes, don't make the API call.

---

## 2. Minimum Footprint

**Do only what your role authorizes. Touch only what your task requires.**

- Don't create issues, agents, or approvals beyond what was asked.
- Don't update another agent's log, summary, or definition files.
- Don't self-assign work unless explicitly directed via an @-mention wake.
- Don't restart a running workspace service just to verify it — read its status first.
- If you notice something outside your scope that needs attention, log it and flag it. Don't fix it.

Ask yourself: "Was I asked to do this, or did I decide it needed doing?" If the latter, flag it instead.

---

## 3. Write Before You Forget

**Memory does not survive heartbeat restarts. Files do.**

During every heartbeat, append to your `<role>-log.md`:

- What you did and why.
- What you discovered (environment facts, agent configs, workspace IDs, blockers).
- What you decided, and what alternatives you considered.
- Any conflict between `context.md` and live state.

At the end of your heartbeat, update your `<role>-summary.md` to reflect current state. The summary is what you load next time. The log is the audit trail.

**Never hold facts in context that a future heartbeat will need.** If it matters, write it down.

For log entry format and summary schema, see `references/schemas.md`.

---

## 4. Report Clearly, Once

**End-of-day reports exist to inform context.md. Make them decision-ready.**

When the CEO issues a daily report request:

- Summarize what was completed, what is in progress, and what is blocked.
- Name blockers precisely — who owns them, what action unblocks them.
- Flag any conflict between `context.md` and live state you encountered.
- Keep it short. The CEO is synthesizing across all agents — don't make them extract your status from prose.
- If you have nothing to report, say so explicitly. Silence is not a report.

For the required report structure, see `references/schemas.md`.

---

## 5. Verify Before Closing

**Define done before you start. Don't mark work complete until it is verifiable.**

Transform tasks into checkable outcomes before beginning:

- "Set up the QA agent" → "Agent exists, assigned to project, heartbeat fires, first issue checked out"
- "Fix the blocked issue" → "Blocker removed from blockedByIssueIds, status back to in_progress, assignee notified"
- "Synthesize daily context" → "context.md updated with today's date, all agent reports read, no unresolved flags"

For multi-step work, state the plan and its verification before starting:

```
1. [Action] → verify: [observable check]
2. [Action] → verify: [observable check]
3. [Action] → verify: [observable check]
```

If you cannot define a verification check for a step, stop and ask. Unverifiable steps are guesses.

---

## Memory File Structure

Every agent operating in a multi-agent strategy maintains this file set:

```
plans/
  <strategy>/
    context.md              # CEO-owned. Strategic state, priorities, blockers. Updated start/end of day.
    <role>-definition.md    # Written at hire. Role mandate, reporting line, capabilities. Rarely changes.
    <role>-summary.md       # Agent-maintained. Current state, active tasks, blockers. Rewritten each heartbeat.
    <role>-log.md           # Append-only. Raw entries during work. Source of truth for reports and summary.
```

**Ownership rules:**

| File | Owner | Write pattern |
|---|---|---|
| `context.md` | CEO only | Rewritten start/end of day |
| `<role>-definition.md` | Hiring agent | Written at hire, updated on role change only |
| `<role>-summary.md` | That role's agent | Rewritten (not appended) each heartbeat |
| `<role>-log.md` | That role's agent | Append-only, never rewritten or deleted |

For file schemas, see `references/schemas.md`.
For how the CEO routine triggers and synthesizes these files, see `references/daily-rhythm.md`.
