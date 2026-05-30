---
name: paperclip-ceo-brief
description: Template for CEO Session Briefs — structured briefings Romesh sends to an AI CEO agent to kick off a Paperclip session. CEO reads all 6 business files. Output is a proposal (org structure, task breakdown, hiring request) for board review. Use this template for every CEO session, first or returning.
---

# CEO Session Brief — Template

## Template

```
COMPANY: [lemonade | romeshx | signallawyers | legalx]
READ: ~/paperclip/[business]/ — all 6 files
SINCE LAST SESSION: [completed tasks, resolved blockers, new approvals — or "first session"]
PRIORITY: [one initiative name from initiatives.md]
BOARD HAS APPROVED: [specific items CEO can act on immediately — or "none yet"]
PRODUCE: [proposal | task breakdown | hiring request | status update]
DONE WHEN: [specific, observable output — one thing]
ESCALATE TO BOARD IF: [what triggers a decision this session]
```

---

## Field Reference

| Field | Purpose | Token role |
|-------|---------|-----------|
| `COMPANY` | Scopes context to one business | Prevents cross-business drift |
| `READ` | CEO always reads all 6 files | Full strategic context in one instruction |
| `SINCE LAST SESSION` | State update from board | CEO skips history reconstruction — starts from now |
| `PRIORITY` | One initiative only | CEO doesn't try to advance all initiatives at once |
| `BOARD HAS APPROVED` | What CEO can act on | CEO doesn't propose what's already decided; doesn't stall on what's approved |
| `PRODUCE` | Output type | CEO knows whether to write a proposal, create tasks, or report |
| `DONE WHEN` | Binary done condition | CEO stops when this is met — not when it feels complete |
| `ESCALATE TO BOARD IF` | Decision trigger | CEO surfaces decisions instead of making them |

---

## First Session Template

```
COMPANY: [business]
READ: ~/paperclip/[business]/ — all 6 files
SINCE LAST SESSION: first session
PRIORITY: [Initiative 1 name from initiatives.md]
BOARD HAS APPROVED: none yet
PRODUCE: hiring proposal — agents needed, roles, adapter types, estimated budget
DONE WHEN: hiring proposal formatted as board approval request, ready for review
ESCALATE TO BOARD IF: any budget value is required before proceeding
```

## Returning Session Template

```
COMPANY: [business]
READ: ~/paperclip/[business]/ — all 6 files
SINCE LAST SESSION: [TASK-00X complete — one line description]; [agent X approved and hired]
PRIORITY: [current active initiative]
BOARD HAS APPROVED: [agent names hired]; [budget set at $X/month]
PRODUCE: [task breakdown | next hiring proposal | status update]
DONE WHEN: [specific output]
ESCALATE TO BOARD IF: [decision type]
```

---

## Rules

- One PRIORITY per session — never list two initiatives
- DONE WHEN must be something Romesh can look at and say yes/no in under 10 seconds
- ESCALATE TO BOARD IF must name a decision type, not a vague trigger ("any uncertainty" is not a trigger)
- CEO proposes — board approves — never the reverse
