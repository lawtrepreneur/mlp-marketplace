---
name: paperclip-task-brief
description: Template for Agent Task Briefs — atomic task instructions Romesh sends to specific Paperclip sub-agents. Sub-agents read only the files relevant to their task. One task per brief. Use for any sub-agent execution work (content, dev, distribution, analytics, QA).
---

# Agent Task Brief — Template

## Template

```
BUSINESS: [lemonade | romeshx | signallawyers | legalx]
AGENT: [agent name from agents.md]
READ: ~/paperclip/[business]/[file.md], [file.md]
TASK: [one action verb + one output]
DONE WHEN: [specific, binary — yes/no in under 10 seconds]
SCOPE: [what files or areas are in play]
DO NOT: [the one constraint most likely to cause drift]
IF BLOCKED: mark blocked, state the blocker in one sentence, stop
```

---

## Field Reference

| Field | Purpose | Token role |
|-------|---------|-----------|
| `BUSINESS` | Scopes to one company | No cross-business context loaded |
| `AGENT` | Names the receiving agent | Agent confirms it is the right recipient |
| `READ` | Specific files only — not all 6 | Cuts context load 60–70% vs full folder read |
| `TASK` | One verb + one output | Agent doesn't interpret scope from vague instructions |
| `DONE WHEN` | Binary done condition | Agent stops generating when output exists — not when it feels complete |
| `SCOPE` | What's in bounds | Agent doesn't touch adjacent files or tasks |
| `DO NOT` | Single hardest constraint | Prevents the most common drift for this task type |
| `IF BLOCKED` | Explicit escalation path | Agent surfaces problems instead of spinning silently |

---

## Example — content task

```
BUSINESS: lemonade
AGENT: ll-content
READ: ~/paperclip/lemonade/company.md, initiatives.md
TASK: Write Substack About page copy for Lemonade Literacy
DONE WHEN: Markdown file, max 300 words, includes founding scene + 
           contrarian belief + curriculum gap argument
SCOPE: About page copy only
DO NOT: Use "fun", "engaging", or warm-and-fuzzy language
IF BLOCKED: mark blocked, state the blocker, stop
```

## Example — dev task

```
BUSINESS: signallawyers
AGENT: sl-dev
READ: ~/paperclip/signallawyers/company.md, constraints.md
TASK: Create lib/config/aboutConfig.js for the Signal Lawyers About page
DONE WHEN: aboutConfig.js exists in lib/config/ with all copy sections 
           populated and no hardcoded strings in components
SCOPE: lib/config/aboutConfig.js only — no other files
DO NOT: Add output: 'export' to next.config.js under any circumstances
IF BLOCKED: mark blocked, state the blocker, stop
```

---

## Rules

- One task per brief — if you need two things done, send two briefs
- READ should list 2 files maximum — if you need more, the task is probably too large
- DONE WHEN must be something Romesh can verify without running the agent again
- DO NOT should be the single most likely failure mode for this specific agent and task
- Agents communicate via tasks only — never instruct an agent to "tell agent X" anything
