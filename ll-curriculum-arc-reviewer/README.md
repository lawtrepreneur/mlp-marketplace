# ll-curriculum-arc-reviewer

> Review, generate, and QA Lemonade Literacy lesson arc content.

---

## Description

A three-mode skill for producing and auditing Lemonade Literacy (LL) lesson arcs for Substack publication.

| Mode | What it does |
|---|---|
| **Mode 1 — Template Review** | Audit the Airtable lessonLibrary schema against LL curriculum architecture |
| **Mode 2 — Content Generation** | Generate a new 5-lesson pack arc from scratch |
| **Mode 3 — Arc Review** | Review existing lesson markdown files for quality and template compliance |

Loads two reference files automatically: `ll-architecture.md` (streams, age tracks, Cold-to-Hot arc, AI Interaction Modes) and `ll-substack-template.md` (template variants A, B, C, D-Evaluation, D-Applied with compliance checklist).

---

## When to Use

Trigger on:
- "review this arc / lesson / pack"
- "check this lesson against the template"
- "generate a lesson arc for [pillar/theme]"
- "does this pass the Marcus test"
- Uploading LL lesson markdown files for review
- Any mention of: Wrong Bot, AI Interaction Mode, Cold-to-Hot arc, Lemonade Bubble/Stand/Labs, lessonAIInteractionMode

---

## Install

Copy this folder into your opencode skills path:

```bash
cp -r ll-curriculum-arc-reviewer /path/to/your/skills/
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
