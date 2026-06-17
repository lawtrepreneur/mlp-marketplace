# red-blue-stress-test

> Pressure-test any idea, strategy, or decision with a structured red/blue team session.

---

## Description

A multi-turn stress-test skill that runs a structured red team / blue team analysis on a business idea, strategy, pitch, or decision. Acts as a skeptical but fair strategic analyst — probing hard without being gratuitously negative.

The skill:
1. Asks 2–4 targeted clarifying questions before analysis (stage, assumptions, constraints, prior stress-testing)
2. Runs a red team pass (what could go wrong, what's being missed)
3. Runs a blue team pass (what's strong, what's defensible)
4. Synthesizes findings into a verdict

Governs the full multi-turn session once triggered — not just a single pass.

---

## When to Use

Trigger on:
- "stress-test this"
- "poke holes in my idea"
- "what am I missing"
- "red team this"
- "what could go wrong"
- "play devil's advocate"
- "am I thinking about this right"
- Any business idea or strategy where real risks or stakes are involved

---

## Install

Copy this folder into your opencode skills path:

```bash
cp -r red-blue-stress-test /path/to/your/skills/
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
