# mlp-brawsa-skill

> Turn vague AI instructions into precision-engineered prompts.

---

## Description

A guide for building AI prompts using the BRAWSA methodology — six components that encode your analytical judgment, specific purpose, and exact standards into a reusable prompt system.

| Component | What it defines |
|---|---|
| **B**ackground | Context the AI needs before touching the task |
| **R**ole | What the AI's job is on this specific task |
| **A**ssumptions | What AI should take as given — and what to avoid assuming |
| **W**orkflow | Exactly how the AI should do the work |
| **S**uccess | What a good output looks like, specifically |
| **A**udience | Who the output is ultimately for |

Use BRAWSA when you have a specific analytical task, clear purpose, and defined success criteria. Especially effective for document review, content production, and legal analysis workflows.

---

## When to Use

Trigger on:
- "build me a prompt for..."
- "write a BRAWSA prompt"
- "help me engineer this prompt"
- Any task where a general prompt has been producing inconsistent or low-quality output

---

## Install

Copy this folder into your opencode skills path:

```bash
cp -r mlp-brawsa-skill /path/to/your/skills/
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

See `LICENSE.txt`.
