# Contributing to MLP Marketplace

Thanks for contributing to MLP Marketplace — skills and tools for AI agents in modern legal practices.

---

## Skill Structure

Every skill must be a self-contained folder at the root of the repo. The minimum required file is `SKILL.md`.

```
my-skill-name/
├── SKILL.md          # required
├── README.md         # recommended
├── LICENSE           # required if not MIT
└── references/       # optional — supporting files loaded by SKILL.md
    └── example.md
```

### SKILL.md Frontmatter

The `SKILL.md` must begin with YAML frontmatter:

```yaml
---
name: my-skill-name
description: >
  One or two sentences describing what the skill does and when to use it.
  This is what agents use to decide whether to activate the skill.
license: MIT
---
```

Required fields: `name`, `description`
Recommended fields: `license`, `version`

---

## README.md

Each skill should include a `README.md` with:

- **Title** and one-line tagline
- **Description** — what it does
- **When to use** — trigger phrases or conditions
- **Install** — how to add it to opencode
- **License**

---

## PR Checklist

Before opening a pull request:

- [ ] Skill folder name matches the `name:` field in `SKILL.md`
- [ ] `SKILL.md` has a complete `description:` (used for agent activation)
- [ ] No hardcoded personal data, API keys, or credentials
- [ ] License is stated (in frontmatter or a `LICENSE` file)
- [ ] `README.md` exists and includes at minimum: description, when to use, install snippet

---

## Licensing

Skills in this repo use a mix of licenses. Your skill may use any open license (MIT, Apache 2.0, CC BY 4.0, etc.).

- **Commercial restriction**: If your skill is CC BY-NC or similar, state it clearly in both the `LICENSE` file and the `SKILL.md` frontmatter.
- **Proprietary skills**: Not accepted. All submissions must be openly licensed.

If your skill has no license field and no `LICENSE` file, it is assumed to be unlicensed (all rights reserved). Add a license before submitting.

---

## Submitting

1. Fork the repo
2. Add your skill folder to the root
3. Update `README.md` — add a row to the appropriate category table
4. Open a PR with a brief description of what the skill does and who it's for
