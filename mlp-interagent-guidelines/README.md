# mlp-interagent-guidelines

> Behavioral guidelines for AI agents working in multi-agent teams.

---

## Description

A set of operational guidelines that reduce common failure modes in multi-agent systems: token waste, scope bleed, lost context, and unverified outcomes. Adapted from Karpathy's coding guidelines for the interagent context.

Covers:
- Checking context before acting (read files before making API calls)
- Maintaining minimum footprint (don't acquire resources beyond the task)
- Writing durable memory (summaries, not logs)
- Reporting clearly (structured handoffs and status updates)
- Verifying outcomes (don't assume success)

Includes two reference files: `schemas.md` (memory file schemas, log/report formats) and `daily-rhythm.md` (CEO daily routine and session cadence).

---

## When to Use

Apply this skill whenever you are:
- Operating as part of a multi-agent team
- Receiving delegated work from another agent
- Coordinating sub-agents or synthesizing agent reports
- Designing agent workflows or writing agent instructions (`AGENTS.md`)
- Reviewing agent behavior for correctness

---

## Install

Copy this folder into your opencode skills path:

```bash
cp -r mlp-interagent-guidelines /path/to/your/skills/
```

Then ensure your `opencode.json` points to that path:

```json
{
  "skills": {
    "paths": ["/path/to/your/skills"]
  }
}
```

---

## License

MIT
