# MLP Marketplace

> Skills and tools for AI agents in modern legal practices.

A curated collection of skills for [opencode](https://opencode.ai)-compatible AI agents. Each skill is a self-contained folder with a `SKILL.md` that loads directly into your agent's context.

---

## Install a Skill

1. Clone or download the skill folder into your skills directory
2. Point opencode at that directory in `opencode.json`:

```json
{
  "skills": {
    "paths": ["/path/to/your/skills"]
  }
}
```

3. The agent loads all skills in that path automatically on the next session

---

## Skills

### Agent Infrastructure

| Skill | Description | License |
|---|---|---|
| [mlp-interagent-guidelines](./mlp-interagent-guidelines) | Behavioral guidelines for multi-agent systems — reduce token waste, prevent scope bleed, maintain context across heartbeats | MIT |

### Prompt Engineering

| Skill | Description | License |
|---|---|---|
| [mlp-brawsa-skill](./mlp-brawsa-skill) | Build precision AI prompts using the BRAWSA methodology (Background, Role, Assumptions, Workflow, Success, Audience) | See LICENSE |

### Legal & Document Generation

| Skill | Description | License |
|---|---|---|
| [mlp-docgen-ontario-affidavit](./mlp-docgen-ontario-affidavit) | Generate court-ready Ontario affidavits from fact summaries with automatic AI writing pattern detection | CC BY-NC 4.0 |

### Content & Publishing

| Skill | Description | License |
|---|---|---|
| [rhh-content-planner](./rhh-content-planner) | Plan, draft, and assess Substack posts using the BRAWSA methodology and a two-format post template | — |
| [substack-launch-strategy](./substack-launch-strategy) | Build, execute, and track a Substack launch strategy with a session-aware, file-backed system | — |
| [ll-curriculum-arc-reviewer](./ll-curriculum-arc-reviewer) | Review, generate, and QA Lemonade Literacy lesson arc content for Substack publication | — |

### Business Operations

| Skill | Description | License |
|---|---|---|
| [paperclip-ceo-brief](./paperclip-ceo-brief) | Structured CEO Session Brief template for kicking off an AI CEO agent session | — |
| [paperclip-copilot](./paperclip-copilot) | Co-pilot for interfacing with AI CEOs and sub-agents across multiple businesses | — |
| [paperclip-task-brief](./paperclip-task-brief) | Atomic task instruction template for Paperclip sub-agents | — |

### Strategy & Analysis

| Skill | Description | License |
|---|---|---|
| [red-blue-stress-test](./red-blue-stress-test) | Structured red/blue team pressure test on any business idea, strategy, or decision | — |

---

## Community Tools

> Know a skill or tool that belongs here? [Open a PR](./CONTRIBUTING.md).

*This section is for community-contributed and third-party skills. None listed yet — be the first.*

---

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for skill structure requirements and PR guidelines.

---

Built by [Lawtrepreneur](https://github.com/lawtrepreneur).
