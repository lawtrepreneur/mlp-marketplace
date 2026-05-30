# LL Architecture Reference

## Business Context

**Lemonade Literacy (LL)** is a family subscription delivering two parallel
weekly curriculum streams. Content is published on Substack and stored in
Airtable.

---

## Streams

| Stream | Day | Applied mechanism (L4–5) |
|---|---|---|
| Life Skills | Tuesday | Real-world testing, synthesis, simulation. May or may not use AI tool. |
| AI Literacy | Thursday | Always uses AI tool. AI Interaction Mode required. |

---

## Age Tracks

| Track | Ages | Facilitation style |
|---|---|---|
| Lemonade Bubble | 6–8 | Parent-led. Concrete anchors. Read-aloud prompts. |
| Lemonade Stand | 9–12 | Shared exploration. **Default canonical track.** |
| Lemonade Labs | 12+ | Child-led. Greater conceptual depth. Optional extension. |

**Lemonade Ventures is retired. Do not use.**

Stand is canonical. Bubble and Labs are substantive adaptations of the
Stand core — not independent designs. Bubble: shorter runtime, higher
parental scaffolding, simplified language. Labs: self-direction, deeper
conceptual framing, optional extension challenge. Adaptations are design
changes, not tone adjustments.

---

## Cold-to-Hot Arc

Every pack is 5 lessons following this structure:

| Lessons | Type | Device required? |
|---|---|---|
| 1–3 | Conceptual, offline, pattern-based | No. Never. |
| 4–5 (Tuesday) | Applied — real-world testing or synthesis | Optional (Variant C if no tool; D-Applied if tool present) |
| 4–5 (Thursday) | AI-supplemented — direct AI tool interaction | Yes. Always. |

Lessons 1–3 must be completable with no device, no internet, no AI tool,
and no assumption of prior sessions. Every lesson runs cold.

---

## Paywall Arc

| Lesson | What's free | Airtable field value |
|---|---|---|
| 1 | Full activity (items 1–6) | Full Free |
| 2–3 | Opening hook only (items 1–5) | Hook Free |
| 4–5 | Pre-activity setup exercise only (items 1–5) | Pre-Activity Setup Free |

Items 1–4 (The Problem, Learning Objectives, The Concept, Arc Reminder)
are always free. Sections D–H are always paywalled. Item 5 and item 6
(Lesson 1 only) are the moving parts.

**Lesson 5 always appends a paywall signal** immediately after item 5:
"This week's full lesson — including [specific activity name] — is available
to paid subscribers."

---

## Contrarian Belief

> "Learning how to use AI has nothing to do with technology. It's about
> how you think about problems."

This governs all content — both streams, all age tracks, all five lessons.
The three skills being built:
- **Pattern recognition**
- **Context evaluation**
- **Asking precise questions**

Tuesday Life Skills builds these skills through real-world situations
without naming AI. Thursday AI Literacy names them explicitly in an AI
context. The two streams are parallel, not independent.

---

## Marcus — Primary Buyer

Analytical professional, 40s, two children aged 6–14, household income
$150K+. Evaluates on sophistication. Named concepts must appear before
asking for money. A lesson that does not name the cognitive skill it builds
fails his test regardless of activity quality.

Named concepts that satisfy Marcus: game theory, information asymmetry,
price elasticity, cognitive load theory, AI ethics, pattern recognition,
automation bias, evidence-based learning, desirable difficulty, source
triangulation, skill decomposition, problem-solution fit, iterative
planning, human-AI collaboration design.

---

## AI Interaction Modes

Used in Lessons 4–5 of both streams. Select one mode per lesson based on
the cognitive gap the lesson needs to create. The gap is the lesson.

### 1. Evaluation Gap (Wrong Bot)
**The gap:** AI sounds right but is wrong.
**AI's role:** Produces a designed, specific error.
**Child's job:** Catches the error and explains why it is wrong.
**Standard:** External and verifiable — there is a correct answer.
**Primary use:** Thursday AI stream.
**Debrief surfaces:** Error type, what it reveals about AI training,
the mechanism that produced it, age-specific notes for all three tracks.
**Variant:** D-Evaluation.

### 2. Perspective Gap
**The gap:** Same situation looks different from opposite framings.
**AI's role:** Argues one position, then argues the opposite.
**Child's job:** Experiences and evaluates each position.
**Primary use:** Pillars involving negotiation, empathy, pricing,
decision-making.
**Debrief surfaces:** Which perspective felt more convincing and why,
what information each perspective left out.
**Variant:** D-Applied.

### 3. Generation Gap
**The gap:** AI has breadth; child has context.
**AI's role:** Produces a large set of options, possibilities, or examples.
**Child's job:** Filters by relevance to their specific situation.
**Primary use:** Opportunity spotting, decision-making, research pillars.
**Debrief surfaces:** Difference between AI's breadth and child's context,
what filtering required that AI could not do.
**Variant:** D-Applied.

### 4. Mirror Gap
**The gap:** AI reflects the child's thinking back, slightly distorted.
**AI's role:** Reframes the child's input — extending or misrepresenting it.
**Child's job:** Evaluates the reflection, corrects where wrong, names
what was missed.
**Primary use:** Self-knowledge, goal-setting, planning pillars.
**Debrief surfaces:** Where AI's model of the child was right, where it
was wrong, what that reveals about inference from limited input.
**Variant:** D-Applied.

### 5. Stakes Gap
**The gap:** The other person in a real interaction has their own logic.
**AI's role:** Role-plays a customer, negotiating partner, sceptical
evaluator, or person with a problem.
**Child's job:** Navigates the interaction in real time, reads the room,
adjusts.
**Primary use:** Communication, pitching, pricing, persuasion pillars.
**Debrief surfaces:** What worked in the interaction, what the child
adjusted, what the AI's responses revealed about the other person's
perspective.
**Variant:** D-Applied.

### 6. Prediction Gap
**The gap:** What the child expected and what actually happened.
**AI's role:** Runs the scenario after the child has committed to a
prediction.
**Child's job:** Compares prediction to outcome and explains the gap.
**Primary use:** Cause and effect, market behaviour, system thinking,
consequence mapping.
**Debrief surfaces:** Why the prediction was right or wrong, what
information the child was missing, what they would predict differently.
**Variant:** D-Applied.

---

## Airtable Field List (lessonLibrary)

All Mode 2 content generation maps to these fields:

| Field | Notes |
|---|---|
| `lessonTitle` | Short, specific |
| `lessonObjectives` | 2–3 observable outcomes. Hard gate. No "understand" or "appreciate." |
| `lessonPrep` | Facilitator context before running |
| `lessonMaterials` | Max 5 items + time estimate |
| `lessonActivity` | Full runnable exercise — no facilitator guide required |
| `lessonReflection` | Closing questions + observable completion evidence |
| `lessonFamilyConnection` | Names cognitive skill in plain language. Parent-facing. |
| `lessonPaywallTier` | Full Free / Hook Free / Pre-Activity Setup Free |
| `lessonAIInteractionMode` | Lessons 4–5 only. Name mode, configure tool, write debrief for all three tracks. Replaces deprecated `lessonWrongBotFlag`. |
| `lessonMinutes` | Target under 60 |
| `lessonSynopsis` | 2–3 sentence internal description |
| `lessonCurriculumRef` | URL if provided; otherwise `[PENDING — curriculum mapping]` |
| `lessonTrackBubble` | Substantive adaptation for ages 6–8 |
| `lessonTrackLabs` | Substantive adaptation for ages 12+ |
| `literacyPackArcSignal` | Pack-level. Lesson 1 conversion hook. Under 100 words. Written last. |
| `literacyCurriculumSummary` | Pack-level. Ontario curriculum summary or `[PENDING]`. |

**Deprecated field:** `lessonWrongBotFlag` → replaced by
`lessonAIInteractionMode`. Flag any record still using the old field.

---

## Ontario Curriculum Codes (reference)

Do not invent codes. If not provided, mark `[PENDING — curriculum mapping]`.

Known mappings (from existing packs):
| Code | Area | LL Pack |
|---|---|---|
| A2.2 | Sci/Tech — AI impacts on everyday life | AI Revealed |
| C1.3 | Language — text patterns and importance | AI Decoded |
| C3.5 | Language — perspectives and bias | AI Ethics |
| D1.1 | Sci/Tech — automating systems | AI Amplified |

ICD2O (AI literacy) is optional, first available at Grade 10 (age 15).
Financial literacy is a 2023 cross-curricular expectation with no
structured delivery mechanism. LL starts at age 6. The Ontario curriculum
gap is LL's core acquisition argument.
