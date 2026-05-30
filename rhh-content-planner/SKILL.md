---
name: rhh-content-planner
description: >
  Plan, draft, and assess Clarity > Complexity (romeshh.com) Substack posts
  using the BRAWSA methodology and a two-format post template (short ~400 words,
  long ~1,000+ words) built for the RHH brand. Use this skill whenever Romesh
  asks to draft a post, assess a draft, plan a content piece, assign a topic to
  a pillar, or generate a BRAWSA prompt for the Clarity > Complexity publication.
  Also trigger when the user says "write a post", "draft this", "which pillar
  does this belong to", "assess this draft", "content plan", or references any
  of the three pillars (The Stakes, In Practice, Mental & Digital Models) or
  any avatar (CREDPRO, EXEC-DEV). Always use this skill before writing any
  Clarity > Complexity content — do not attempt to draft from general knowledge.
---

# RHH Content Planner

Skill for planning and drafting *Clarity > Complexity* Substack posts
(romeshh.com). Covers pillar assignment, pre-draft intake, format selection,
full draft generation, and draft assessment — all governed by the BRAWSA
prompt and two-format post template built in session.

---

## Quick Reference

**Three pillars:**
- **The Stakes** — what's changing and why the gap has a specific cost
- **In Practice** — real builds, real failures, real tools; the proof layer
- **Mental & Digital Models** — the thinking underneath the tools

**Two formats:**
- **Short (~400 words)** — 6 sections: Hook → Tension → Turn → Model → Close → CTA
- **Long (~1,000+ words)** — 7 sections: adds Implication between Model and Close

**Two avatars:**
- **CREDPRO** — credentialed professional; liability objector
- **EXEC-DEV** — executive; intellectual objector ("frameworks don't stick")

**One CTA (always):**
> *"If you want to see where your gap is: Assess Your Delegation Gap — 5 minutes, free."*

---

## Mode Selection

Identify which mode applies from the user's request, then follow
the relevant section below.

| User request | Mode |
|---|---|
| "Draft a post on X" / "Write X" | → Mode 1: Full Draft |
| "Which pillar does X belong to?" | → Mode 2: Pillar Assignment |
| "Assess this draft" / "Review this" | → Mode 3: Draft Assessment |
| "Build a BRAWSA prompt for X" | → Mode 4: BRAWSA Prompt Output |

---

## Mode 1 — Full Draft

### Step 1: Intake gate

Collect all four before proceeding. If any are missing, ask for them.
Do not infer silently.

```
TITLE:         post title or topic
PILLAR:        The Stakes / In Practice / Mental & Digital Models
FORMAT:        Short (~400 words) / Long (~1,000+ words)
READER STATE:  one sentence — specific emotional state, not just avatar label
TRIGGER:       the near-miss or borrowed pain moment that surfaces this post
```

If PILLAR or FORMAT are not supplied, run Mode 2 first, then confirm
format with the user before drafting.

### Step 2: Pre-draft checks

Before writing the hook, confirm internally:

- **Pillar locked.** If the topic fits two pillars, name the primary
  and state in one sentence why the other was set aside.
- **Post type named.**
  Diagnostic / Contrarian / Build Log / Case Narrative / Model / Founder Note
- **Reader state is specific.** Not "CREDPRO" — the emotional position
  this reader is in right now. See reference file for examples.
- **Trigger is a near-miss, not a crisis.** Reactive readers don't read
  Substack. If the trigger is a full crisis, pull back to the moment before.

### Step 3: Draft using the template

Follow the section sequence exactly. Apply word budgets.
Run internal FAIL checks at each section before proceeding.

Read `references/post-template.md` for full section specs,
word budgets, and FAIL conditions.

### Step 4: Quality check

Before outputting, run every item in the quality checklist
(bottom of `references/post-template.md`). If any fail, revise first.

---

## Mode 2 — Pillar Assignment

Given a topic or title, assign it to the correct pillar and
recommend a format. Output:

```
PILLAR:      [The Stakes / In Practice / Mental & Digital Models]
FORMAT:      [Short / Long] — reason in one sentence
POST TYPE:   [Diagnostic / Contrarian / Build Log / Case Narrative / Model / Founder Note]
ANGLE:       one sentence — what makes this fit this pillar, not another
```

**Assignment logic:**

- Is the post about *what's changing economically or professionally*
  and why the reader's current position has a specific cost?
  → **The Stakes**

- Is the post about *a specific build, tool decision, or workflow*
  inside a regulated practice — including what failed?
  → **In Practice**

- Is the post about *a thinking framework, mental model, or decision
  principle* that is portable across tools and situations?
  → **Mental & Digital Models**

- Does it fit two pillars? Choose the one where the *model or evidence*
  primarily lives — not the framing around it.

**Format logic:**

- Short if: the insight lands in one scenario, one turn, one model.
  The Stakes and Mental & Digital Models default here.
- Long if: the build requires showing failure, or the framework requires
  a full professional situation to land. In Practice defaults here.
- A post that needs an Implication section to be complete is a long post.
  A post that doesn't earn an Implication section is a short post.

---

## Mode 3 — Draft Assessment

Assess a supplied draft against the template and voice rules.
Output a structured verdict with specific line-level notes.

**Assessment structure:**

```
PILLAR FIT:     [Clean / Unclear — reason]
FORMAT:         [Short / Long / Mixed — note if Implication present in short]
HOOK:           [Pass / Fail — specific note]
TENSION:        [Pass / Fail — near-miss or crisis? specific enough?]
TURN:           [Pass / Fail — reframe or solution?]
MODEL:          [Pass / Fail — capability test: category or instance?]
IMPLICATION:    [Pass / Fail / N/A — earned or asserted?]
CLOSE:          [Pass / Fail — summarises or lands?]
CTA:            [Pass / Fail — once, earned, final?]
VOICE:          [Pass / Fail — specific lines that violate voice rules]
VERDICT:        [Ready / Needs revision]
PRIORITY FIX:   [The one section to fix first if revision needed]
```

For each FAIL, quote the specific sentence or phrase and state
the precise violation — do not give general notes.

---

## Mode 4 — BRAWSA Prompt Output

Output the full BRAWSA prompt from `references/brawsa-prompt.md`
with the intake fields pre-filled if the user has supplied them.

If intake fields are missing, output the prompt with blank fields
and instruct the user to complete them before running.

---

## Voice Rules (apply to all modes)

```
DO:
→ Short sentences. Blunter than the brand documents suggest.
→ Name the cost before naming the fix.
→ Earned authority — the practitioner who lived the problem.
→ Specific scenarios over general observations.
→ Plain language throughout.

DO NOT:
→ AI consultant register. No productivity pitch.
→ Performance. No warmup. No rhetorical questions.
→ Assertions without demonstration.
→ Summarising in the close.
→ Repeating the CTA.
→ Any sentence that could appear on any other
   professional services website.
```

---

## Reference Files

| File | When to read |
|---|---|
| `references/post-template.md` | Mode 1 drafting — full section specs, word budgets, FAIL conditions, quality checklist |
| `references/brawsa-prompt.md` | Mode 4 — full BRAWSA prompt for post generation |

Load the relevant reference file before executing the mode.
Do not draft from memory.
