# substack-launch-strategy

> Build, execute, and track a Substack publication launch strategy.

---

## Description

A session-aware Substack launch strategist built on the BRAWSA methodology. Combines strategy creation, execution tracking, and conversational direction into a single persistent system.

Three operating modes:

| Mode | Trigger | What Happens |
|---|---|---|
| **INIT** | No strategy file exists | Collect Input Block → build strategy → save as `[slug]-strategy.md` |
| **SESSION** | Strategy file exists | Load strategy + progress log → take direction |
| **LOG** | Explicit log request | Append session progress to log file |

Covers launch planning, content calendar, channel strategy, and growth tactics for any Substack publication.

---

## When to Use

Trigger on:
- "help me launch my Substack"
- "build a launch strategy"
- "I'm starting a newsletter"
- "how do I grow my Substack"
- "log my session", "where did we leave off"
- Any Substack publication planning or growth task

---

## Install

Copy this folder into your opencode skills path:

```bash
cp -r substack-launch-strategy /path/to/your/skills/
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

No license specified. All rights reserved.
