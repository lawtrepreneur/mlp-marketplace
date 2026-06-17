# paperclip-copilot

> Co-pilot for managing AI CEOs and sub-agents across multiple businesses.

---

## Description

A co-pilot skill for interfacing with AI CEOs and sub-agents across multiple Paperclip businesses. Produces three output types:

- **CEO Session Briefs** — context packages for kicking off a CEO agent session
- **Agent Task Briefs** — atomic task instructions for sub-agents
- **Proposal Reviews** — structured review of agent proposals for board approval

Use when you need to brief a CEO, assign a task to a sub-agent, or review agent output.

---

## When to Use

Trigger on:
- "brief the CEO"
- "assign this to a sub-agent"
- "review this proposal"
- "I need a task brief for..."
- Any Paperclip session management task across businesses

---

## Install

Copy this folder into your opencode skills path:

```bash
cp -r paperclip-copilot /path/to/your/skills/
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
