# paperclip-task-brief

> Atomic task instruction template for Paperclip sub-agents.

---

## Description

A template for Agent Task Briefs — precise, single-task instructions sent to specific Paperclip sub-agents. Sub-agents read only the files relevant to their task. One task per brief.

Use for any sub-agent execution work: content, development, distribution, analytics, or QA.

---

## When to Use

Trigger on:
- "write a task brief for..."
- "assign this task to [sub-agent]"
- "create an agent brief"
- Any time you need to delegate a specific task to a sub-agent with a clean, scoped instruction set

---

## Install

Copy this folder into your opencode skills path:

```bash
cp -r paperclip-task-brief /path/to/your/skills/
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
