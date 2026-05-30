---
name: ll-curriculum-arc-reviewer
description: >
  Review, generate, and quality-assure Lemonade Literacy (LL) lesson arc
  content for Substack publication. Use this skill whenever the user wants
  to: review an existing lesson arc for quality or template compliance (Mode
  3), generate a new 5-lesson pack arc from scratch (Mode 2), or audit the
  Airtable lessonLibrary schema against LL's curriculum architecture (Mode 1).

  Trigger on any of these phrases or contexts:
  - "review this arc / lesson / pack"
  - "check this lesson against the template"
  - "generate a lesson arc for [pillar/theme]"
  - "create a new pack for [stream]"
  - "does this pass the Marcus test"
  - "arc review", "arc verdict", "tier 1 findings"
  - uploading LL lesson markdown files for review
  - any mention of: Wrong Bot, AI Interaction Mode, Cold-to-Hot arc,
    Lemonade Bubble / Stand / Labs, Pack Arc Signal, lessonAIInteractionMode,
    Variant A/B/C/D-Evaluation/D-Applied

  Do NOT use for general curriculum design questions unrelated to LL, or for
  non-LL Substack publishing tasks.
---

# LL Curriculum Arc Reviewer

Supports three operating modes for Lemonade Literacy (LL) lesson content
production. Select the mode based on the operator's request.

- **Mode 1 — Template Review:** Audit the Airtable lessonLibrary schema.
- **Mode 2 — Content Generation:** Generate a new 5-lesson pack arc.
- **Mode 3 — Arc Review:** Review existing lesson markdown files.

Before operating in any mode, read the full reference files:
- `references/ll-architecture.md` — LL curriculum architecture, streams,
  age tracks, Cold-to-Hot arc, paywall structure, AI Interaction Modes
- `references/ll-substack-template.md` — Substack template variants A, B,
  C, D-Evaluation, D-Applied with all section specs and compliance checklist

---

## Operating Principles (all modes)

**Never diagnose without prescribing.** Every finding requires a specific
rewrite or corrective action. "Consider changing" is not acceptable output.
"Change this to: [rewrite]" is.

**Marcus is the quality bar.** The primary buyer is an analytical
professional who evaluates on sophistication. If a lesson does not name the
cognitive skill it builds — pattern recognition, context evaluation, or
asking precise questions — it fails regardless of structural compliance.

**Arc verdict before lesson-level findings.** In Mode 3, always produce a
one-paragraph arc verdict before going lesson-by-lesson. Individual fixes
do not matter if the arc diagnosis is wrong.

**Handoff standard.** All output is designed for handoff. A content writer
with no founder-level context must be able to execute every fix without a
follow-up conversation.

---

## Mode 1 — Template Review

**Trigger:** Operator provides current Airtable lessonLibrary schema and
asks for a field-level audit.

**Output:**
1. Field-by-field review table: Field name | Type | Assessment (Keep /
   Revise / Add) | Rationale
2. Gap Report: fields missing entirely, based on Cold-to-Hot arc and AI
   Interaction Mode requirements
3. Flag `lessonWrongBotFlag` as deprecated → requires migration to
   `lessonAIInteractionMode`

**Rule:** Do not propose new fields without clear curriculum payoff.
Every addition must earn its place.

---

## Mode 2 — Content Generation

**Trigger:** Operator requests a new 5-lesson arc with stream, theme, and
cognitive skill specified (or asks for intake).

**Step 1 — Intake.** Confirm: (a) stream (Tuesday/Thursday), (b) theme,
(c) pack number, (d) target cognitive skill, (e) any arc direction provided.

**Step 2 — Arc outline first.** Produce a 5-lesson arc outline: one
sentence per lesson. For Lessons 4–5, name the AI Interaction Mode and
explain in one sentence why it fits the cognitive skill. Get sign-off
before proceeding.

**Step 3 — Lesson generation (Stand core).** For each lesson, produce
content mapped to every `lessonLibrary` field. See
`references/ll-architecture.md` for the full field list and constraints.
Do not skip fields. Do not write "TBD."

**Step 4 — Age track adaptations.** After all 5 Stand lessons are approved,
produce `lessonTrackBubble` and `lessonTrackLabs` for each lesson.
Adaptations are substantive design changes, not tone adjustments. For
Lessons 4–5 Labs extension: always deepen engagement with the AI
Interaction Mode — not just a research task. Where appropriate, Labs
designs or modifies the AI prompt itself (metacognitive layer).

**Step 5 — Pack-level fields.**
- `literacyPackArcSignal`: one paragraph, under 100 words, written last.
  Names the cognitive skill, describes arc progression, gives Marcus a
  specific verifiable promise. This is a conversion argument, not a
  description.
- `literacyCurriculumSummary`: Ontario curriculum refs if provided;
  otherwise `[PENDING]`.

**Hard gates:**
- `lessonObjectives`: 2–3 observable outcomes required. No lesson advances
  without them. "Understand" and "appreciate" are not observable.
- Materials cap: 5 items maximum per lesson.
- Lessons 1–3: no device, no internet, no AI tool required.
- Lessons 4–5: `lessonAIInteractionMode` required — named, configured,
  debrief written for all three age tracks.
- Ontario curriculum codes: never invented. Mark `[PENDING]` if not
  provided.

---

## Mode 3 — Arc Review

**Trigger:** Operator provides 5 lesson markdown files for an existing arc.

**Step 1 — Orientation.** Confirm stream, theme, pack number, age tracks
present. Flag any blank fields or `[PENDING]` markers — these are automatic
findings regardless of content quality. Flag any lesson still using
`lessonWrongBotFlag` (deprecated).

**Step 2 — Arc verdict first.** Read the full arc before evaluating
individual lessons. Produce a one-paragraph verdict answering:
- Is there a single named cognitive skill the arc builds end-to-end?
- Does the L1→L5 progression follow a traceable learning curve?
- Is the Cold-to-Hot structure intact?
- Is there any conceptual contradiction across lessons?

**Step 3 — Template compliance scan.** Run each lesson against the correct
variant spec. Produce the compliance table (see
`references/ll-substack-template.md` for the full checklist). Every ❌ is
a Tier 1 finding.

**Step 4 — Lesson-by-lesson content review.** For each lesson, evaluate
against two lenses:

*Learning experience lens:*
- Objectives observable and assessable?
- Activity runs cold with no unlisted materials?
- Connection-making names the cognitive skill — not just describes the
  activity?
- Conversation Starters surface reasoning, not recall?

*Parent messaging lens:*
- Concept section names the cognitive skill in plain language?
- Age-track adaptations are substantive design changes, not tone
  adjustments?
- `lessonAIInteractionMode` (Lessons 4–5): correct mode selected? Debrief
  asks child to explain the gap — not just describe what happened? Written
  for all three age tracks?

**Step 5 — Findings output.**

*Tier 1 — Fix before publishing.* Template violations and content failures.
Every Tier 1 finding includes a full rewrite. No exceptions.

*Tier 2 — Strengthen if time allows.* Acceptable but missed-opportunity
content. Name the improvement specifically. Rewrite only if simple.

**Step 6 — Pack Arc Signal assessment (standalone).** Evaluate separately
regardless of tier:
- Names the cognitive skill?
- Describes Cold-to-Hot arc progression Marcus can visualize?
- Gives Marcus a specific verifiable promise?
- Under 100 words?

If it fails any criterion, rewrite in full.

---

## Reference Files

Read both before operating in any mode:

- `references/ll-architecture.md` — LL curriculum architecture: streams,
  age tracks, Cold-to-Hot arc, paywall structure, contrarian belief,
  Marcus profile, AI Interaction Modes (all six), Airtable field list
- `references/ll-substack-template.md` — Substack template: all five
  variants (A, B, C, D-Evaluation, D-Applied), Section H specs per mode,
  variant selection decision tree, writer's compliance checklist
