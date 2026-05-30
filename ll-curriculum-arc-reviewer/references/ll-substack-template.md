# LL Substack Template Reference

## Variant Selection

| Lesson | Stream | Variant |
|---|---|---|
| Lesson 1 | Either | **A** |
| Lessons 2–3 | Either | **B** |
| Lessons 4–5 | Tuesday, no AI tool | **C** |
| Lessons 4–5 | Evaluation Gap (Wrong Bot) | **D-Evaluation** |
| Lessons 4–5 | Any other AI Interaction Mode | **D-Applied** |

**Decision tree:**
```
Lesson 1? → Variant A
Lesson 2 or 3? → Variant B
Lesson 4 or 5?
  └─ No AI tool? → Variant C (Tuesday only)
  └─ AI tool present?
       └─ Evaluation Gap (Wrong Bot)? → Variant D-Evaluation
       └─ Any other mode? → Variant D-Applied
```

---

## Fixed Structure (all variants)

**Always free — items 1–4:**
1. The Problem
2. Learning Objectives
3. The Concept
4. Arc Reminder

**Always paywalled — Sections D–H:**
- D. Age-Specific Scaffolding
- E. Conversation Starters
- F. What Success Looks Like
- G. If It Goes Sideways
- H. AI Interaction Mode — Debrief Notes *(Lessons 4–5 only)*

**What moves:** Item 5 only (and item 6 in Lesson 1).

---

## Eyebrow Format

```
[LIFE SKILLS or AI] · [BUBBLE / STAND / LABS] · PACK [X] · LESSON [Y] OF 5
```

Unified post: `[LIFE SKILLS or AI] · ALL TRACKS · PACK [X] · LESSON [Y] OF 5`

---

## Pack Arc Signal (Lesson 1, item 4)

Write last. Under 100 words. Formula:
> "[Pack name] is a 5-lesson sequence. By Lesson 5, your child will
> [specific observable capability — not an activity description].
> Lessons 4 and 5 use a purpose-built AI activity available to paid
> subscribers."

**Test:** Can Marcus witness the promised capability in his child?
If not, rewrite. "Will design a workflow" is an activity. "Will hand
you a written workflow and identify its dependency risks" is a
capability.

---

## Arc Reminder (items 4, Lessons 2–5)

One sentence only: "Last week: [X]. This week: [Y]. Next: [Z]."
Lesson 5 variant: "Last week: [X]. This week: the final lesson."

---

## Length Targets

| Lesson | Free section | Paid section |
|---|---|---|
| Lesson 1 | 450–600 words | 400–600 words |
| Lessons 2–3 | 150–200 words | 600–800 words |
| Lessons 4–5 | 150–200 words | 700–900 words |

---

## Variant A — Lesson 1 (Full Free)

Item 5 (What You Need) and item 6 (The Activity) are above the paywall.
Paid section begins at Section D (Age-Specific Scaffolding).

**Item 6 — The Activity structure:**
- Opening hook: 1–2 sentences. The ignition moment.
- Main activity: step by step, 200–300 words. Runs without facilitator
  guide. No step assumes prior sessions or unlisted materials.
- Connection-making: ~100 words. Names the cognitive skill explicitly.

**Paid section note:** Section B (The Activity) is omitted in Lesson 1
paid section — the full activity was free. Proceed directly to Section D.

---

## Variant B — Lessons 2–3 (Hook Free)

Item 5 (The Opening Hook) is above the paywall. Everything else paywalled.

**Item 5 requirements:**
- The ignition moment only
- Must run cold — no prior session required
- Executable in under 5 minutes
- 50–80 words

**Paid section adds:** Section A (What You Need) and Section B (The
Activity) before Section D.

---

## Variant C — Lessons 4–5, Tuesday, No AI Tool

Item 5 (Pre-Activity Setup Exercise) is above the paywall.

**Item 5 requirements:**
- Activates prior learning without a device
- Must run cold
- Executable in under 5 minutes
- 50–80 words
- **Lesson 5 only:** append paywall signal immediately after item 5:
  "This week's full lesson — including [name the specific applied
  activity] — is available to paid subscribers."

**No Section H.** This variant has no AI Interaction Mode debrief.

---

## Variant D-Evaluation — Lessons 4–5, Evaluation Gap (Wrong Bot)

Item 5 (Pre-Activity Setup Exercise) is above the paywall. The child
forms a hypothesis that Wrong Bot will test.

**Item 5 requirements:**
- Predictive exercise — child commits to a hypothesis before tool opens
- Must run cold
- 50–80 words
- **Lesson 5 only:** append paywall signal

**Paid section structure:**
- A. What You Need (Wrong Bot link required as first item)
- B. The Activity (sequence: hypothesis → Wrong Bot → identification →
  explanation. Explanation is the skill; identification is the warm-up.)
- C. How to Use the Wrong Bot (error category only — do not reveal
  the specific error)
- D. Age-Specific Scaffolding
- E. Conversation Starters (must ask child to *explain* the error,
  not just find it)
- F. What Success Looks Like
- G. If It Goes Sideways
- H. AI Interaction Mode — Debrief Notes (see Section H spec below)

**Labs extension for D-Evaluation:** Child designs the prompt that
produces the Wrong Bot behaviour — "build the trap, then catch it."
This is the metacognitive layer.

---

## Variant D-Applied — Lessons 4–5, All Other Modes

Item 5 (Pre-Activity Setup Exercise) is above the paywall. The child
creates a stake before the AI interaction opens.

**Item 5 — mode-specific setup:**
| Mode | What child does above paywall |
|---|---|
| Perspective Gap | States their position before AI argues both sides |
| Generation Gap | Lists what they already know before AI generates options |
| Mirror Gap | Writes their own description before AI reflects it back |
| Stakes Gap | Prepares their pitch / argument before AI plays the other person |
| Prediction Gap | Writes their prediction before AI runs the scenario |

**Lesson 5 only:** append paywall signal after item 5.

**Paid section structure:**
- A. What You Need (AI tool link or name; max 4 additional items)
- B. The Activity (sequence varies by mode — see mode specs in
  ll-architecture.md)
- C. How to Use the AI Tool (mode-specific; do not over-explain —
  the interaction is the lesson)
- D. Age-Specific Scaffolding
- E. Conversation Starters (must surface the gap the AI created,
  not just what the AI said)
- F. What Success Looks Like (mode-specific — see spec below)
- G. If It Goes Sideways (mode-specific recovery)
- H. AI Interaction Mode — Debrief Notes (see Section H spec below)

**Labs extension for D-Applied:** Child modifies the AI prompt and
evaluates how the change affected the output. This is the metacognitive
layer.

---

## Section H — AI Interaction Mode Debrief Notes

### For Variant D-Evaluation (Evaluation Gap)

```
H. AI INTERACTION MODE — DEBRIEF NOTES
   Mode: Evaluation Gap

   Error type: [factual fabrication / pattern over-application /
   context collapse / confidence without basis / other]

   What it reveals: [What does this error type reveal about how AI
   models are trained? 2–3 sentences. Parent-facing. No jargon.]

   How it connects to AI training: [The mechanism. Why does a
   well-trained AI produce this error? 1–2 sentences.]

   Age-specific debrief notes:
   BUBBLE: [One idea. Simple. Concrete comparison if needed.]
   STAND:  [One mechanism. The why, not just the what.]
   LABS:   [The formal concept if one applies. Connection to
            broader skill across the arc.]
```

### For Variant D-Applied (all other modes)

```
H. AI INTERACTION MODE — DEBRIEF NOTES
   Mode: [Perspective Gap / Generation Gap / Mirror Gap /
          Stakes Gap / Prediction Gap]

   The gap this mode creates: [One sentence — what experiential gap
   does this mode produce between what the child expected and what
   they got?]

   What it reveals: [What does this gap reveal about either the AI's
   limits or the child's thinking? 2–3 sentences. Parent-facing.
   No jargon.]

   How the child should narrate it: [Complete the sentence:
   "I expected [X]. The AI [Y]. That gap showed me [Z]."
   This is the transferable insight.]

   Age-specific debrief notes:
   BUBBLE: [One idea. Simple. Concrete comparison if needed.]
   STAND:  [One mechanism. The why, not just the what.]
   LABS:   [The formal concept if one applies. Connection to
            broader skill across the arc.]
```

---

## Section F — What Success Looks Like (mode-specific)

| Mode | Observable success |
|---|---|
| Evaluation Gap | Child names the error AND explains why it occurred, connecting to AI training |
| Perspective Gap | Child argues the position they initially disagreed with and explains what changed |
| Generation Gap | Child explains why they kept what they kept and cut what they cut |
| Mirror Gap | Child identifies specifically where the AI's reflection was wrong and what it missed |
| Stakes Gap | Child describes one adjustment they made mid-interaction and why |
| Prediction Gap | Child explains the gap using a cause, not just a description |

---

## Compliance Checklist

Run before publishing any post.

**All lessons:**
- [ ] Eyebrow correct: stream · age track · pack · lesson number
- [ ] Items 1–4 above paywall
- [ ] Paywall marker in correct position for this lesson number
- [ ] Sections D–H below paywall
- [ ] Learning Objectives: observable outcomes only — no "understand,"
      "appreciate," "be aware of"
- [ ] Concept section names cognitive skill in plain language
- [ ] No step in free section assumes prior session or unlisted material

**Lesson 1 only:**
- [ ] Pack Arc Signal present in item 4
- [ ] Pack Arc Signal names specific observable capability (not activity)
- [ ] Pack Arc Signal signals paid L4–5 without describing mechanics
- [ ] Pack Arc Signal under 100 words

**Lessons 2–5:**
- [ ] Arc Reminder is one sentence: "Last week / This week / Next"

**Lessons 4–5 with AI tool (Variants D-Evaluation and D-Applied):**
- [ ] Pre-activity setup exercise above paywall
- [ ] Item 5 creates a stake — position, prediction, or question
- [ ] Lesson 5: paywall signal appended after item 5
- [ ] AI Interaction Mode named in Section H
- [ ] Section H complete: gap + what it reveals + how child narrates it
      + age-specific debrief for all three tracks (Bubble, Stand, Labs)

**Variant D-Evaluation (Wrong Bot) only:**
- [ ] Wrong Bot listed first in materials (Section A)
- [ ] Section C present (How to Use the Wrong Bot)
- [ ] Section H names error type
- [ ] Section H explains connection to AI training
- [ ] Conversation Starters ask child to explain error, not just find it
- [ ] Labs scaffolding includes "build the trap, then catch it" where
      appropriate

**Variant D-Applied only:**
- [ ] Section C present and mode-specific (How to Use the AI Tool)
- [ ] Section H gap statement: "I expected [X]. The AI [Y]. That gap
      showed me [Z]."
- [ ] What Success Looks Like is mode-specific
- [ ] Labs scaffolding includes prompt-modification extension where
      appropriate

**Age-specific scaffolding (all lessons):**
- [ ] Bubble: parent-led language, concrete anchor, guided prompts in
      quotes, shorter runtime
- [ ] Stand: shared exploration, child invited to lead
- [ ] Labs: child-led, extension challenge named, formal concept named
      if applicable
