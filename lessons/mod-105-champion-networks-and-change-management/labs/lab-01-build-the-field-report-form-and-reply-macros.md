# Lab 01 — Build the Field-Report Form and the 24-Hour Reply Macros

**Duration:** 60–75 minutes
**Format:** guided hands-on — form design + macro authoring + red-team pass
**Grounding chapters:** [03 — Routing Field Signal Back to Policy, Tooling, and Training](../03-routing-field-signal-back-to-policy-tooling-and-training.md), [02 — The Four-Phase Lifecycle](../02-the-four-phase-lifecycle-recruit-train-recognise-retire.md)

## Objective

Produce two production-ready artifacts the operations analyst uses the Monday of every weekly triage: a **field-report intake form** (the six-field schema wired for a specific intake surface) and a **reply macro set** — one short, record-level boilerplate per route (policy, tooling, training, incident-shaped) that closes the loop within 24 hours. Together they are the plumbing that turns Chapter 03's design into a real operating surface.

## Prerequisites

- Chapter 03 read, with particular attention to the six-field schema, the 24-hour reply commitment, and the "closing the loop at the record level" discipline.
- Chapter 02 read (the lifecycle naming matters — macros reference the champion's filing cadence).
- A chosen intake surface. Pick one and stay with it: a Slack slash-command form, a short web form fronting a ticketing system, or a Notion / Airtable database. The lab works for all three.
- A blank working file — `field-report-form.md` for the schema and `reply-macros.md` for the macros.

## Why a lab, not an exercise

[Exercise 02](../exercises/exercise-02-two-way-feedback-loop-drill.md) asks you to *run* the Monday-morning triage against six pre-written field reports and produce routing decisions. The exercise assumes the intake form exists, the destination-ticket templates exist, and the 24-hour reply macros exist — none of which do when you start the role. This lab builds exactly those three artifacts, so the exercise's triage becomes runnable in the 30-minute cap Chapter 03 mandates. If you find Exercise 02's reply column feels hand-wavy, that's because the macros have not been written yet; this is the layer below.

## Setup

Open `field-report-form.md` and paste this skeleton. You will fill it in as you walk Step 1.

```markdown
# Field-Report Intake Form — v0.1 (draft)

**Intake surface:** <Slack slash-command | web form | Notion/Airtable>
**Owner:** operations analyst
**Review cadence:** Monday 09:30, 30-minute weekly triage
**Target reply time:** 24 hours to filing champion

## Field schema

| # | Field | Type | Required? | Default | Help text (champion-facing) |
|---|-------|------|-----------|---------|------------------------------|
| 1 | | | | | |
```

Open `reply-macros.md` and paste this skeleton:

```markdown
# Reply Macros — v0.1 (draft)

Macros replace ad-hoc replies to field-report filings. Each is short, names a route, names a destination ticket ID, names a resolution date, and closes with how the champion will see the outcome.

- [ ] POL — policy route
- [ ] TOOL — tooling route
- [ ] TRAIN — training route
- [ ] INC — incident-shaped (fast path to governance)
- [ ] NEEDS-CLARIFY — triage could not route; champion input requested
```

---

## Step 1 — Specify the six-field schema (15 min)

Chapter 03 lists six fields. Transcribe them into the table in `field-report-form.md`, one row each, filling the five columns. The champion-facing help text is the row that does the most work — it is what the champion reads while filing between two operator conversations, and it is what makes or breaks the ten-minute filing time Chapter 03 names.

Use the schema below as the row set. Fill the **Help text** column in your own words — a complete sentence per field, written for a champion in their third month.

| # | Field (from Ch 03) | Type | Required? | Default |
|---|---|---|---|---|
| 1 | Date and function | auto | yes | filer's identity |
| 2 | Tool(s) involved | multi-select over approved-tool envelope + "off-envelope" | yes | — |
| 3 | Signal type | single-select: use-case pattern / policy question / operator friction / **incident-shaped observation** / training gap / tool limitation | yes | — |
| 4 | Narrative (2–4 sentences) | free text | yes | — |
| 5 | Operator identity | choice: anonymous / operator-opted-in to be named | yes | **anonymous** |
| 6 | Recommended next step | free text, short | yes | "raising; no action proposed" acceptable |

Three design notes you encode while writing the help text:

- **Field 3's `incident-shaped observation` option is the tag** that triggers the Chapter 08 fast path. The help text should tell the champion they do not need to diagnose severity — if it *looks* incident-shaped, tag it that way. The chapter is explicit: the tag is the champion's call, not the enablement lead's.
- **Field 5 defaults to anonymous** for a specific reason named in Chapter 03 — an operator worried about attribution does not give the champion the real story. The help text says this in a line.
- **Field 4 is deliberately short.** Two to four sentences, operator language. Longer than that and the field becomes a compliance surface, which is the first failure mode of intake forms.

### Checkpoint 1 — before Step 2

- [ ] All six rows are filled; the schema has exactly six fields and no more.
- [ ] Field 3's enumeration includes the `incident-shaped observation` option verbatim.
- [ ] Field 5 defaults to anonymous and the help text names why.
- [ ] Help text on every field is written in a complete sentence, from the champion's point of view.
- [ ] You can state in one sentence what you would cut if the schema grew to seven fields (hint: whichever one the champion would skip).

---

## Step 2 — Write the four route-reply macros (25 min)

Open `reply-macros.md`. Write one macro per route — POL, TOOL, TRAIN, INC. Each macro is a short paragraph the operations analyst pastes into the reply within 24 hours of filing. Each must:

- Thank the champion by first name (the macro includes a `{champion_first_name}` token).
- Name the route chosen.
- Reference the destination ticket by its ID (the macro includes a `{ticket_id}` token).
- State the resolution date or the next milestone (policy and training default to 30 days per Ch 03; tooling is variable — the macro has a `{resolution_horizon}` token with a comment).
- Say how the champion will see the outcome — the ticket update will post back to the source report (Ch 03's record-level loop-close).

Use the seed text below for POL; write the other three yourself matching the shape.

### POL — policy route (seed)

```
Hi {champion_first_name} — thanks for the field report {report_id}.

Routing: this is going into the policy backlog as {ticket_id}. The signal
is that the {brief_restatement_of_issue}; it will be worked with the
head of AI governance in the walking-redline cadence.

Timeline: expect a resolution update by {resolution_date_30_days}. If the
redline ships inside that window you will see the diff; if the backlog
decides this does not need a change, you will see the reasoning.

How you will see it: the update to {ticket_id} will post back to the
record of {report_id}. You do not need to click through to policy
tooling to track it.

— {ops_analyst_name}
```

Now write the equivalent for:

- **TOOL** — note that resolution horizon is "pilot cycle" or "next quarterly envelope review," not 30 days.
- **TRAIN** — note that the playbook rev cycle is quarterly; the use-case library is near-continuous, so the horizon depends on which it is.
- **INC** — the macro is different in shape. It confirms the fast-path handoff has started, names the governance-side owner the field report has been routed to, and explicitly tells the champion to **pause further outbound communication to the operator about the substance of the incident until governance-side guidance arrives**. The macro does *not* include a resolution date; Chapter 08 is explicit that substantive communication is not the enablement lead's call once an incident is live.

### The NEEDS-CLARIFY macro — the one most programs skip

Add a fifth macro for the triage case where the report can't be routed cleanly — the narrative is short, the tool field says "off-envelope" without naming the tool, or the signal type doesn't obviously match. The macro asks one specific clarifying question (not three — one), names the standing triage next Monday as the fallback, and commits to replying again inside 24 hours of the champion's answer. The macro exists because without it, ambiguous reports pile up unrouted and the loop breaks.

### Checkpoint 2 — before Step 3

- [ ] Four macros plus NEEDS-CLARIFY, in `reply-macros.md`.
- [ ] Each of POL / TOOL / TRAIN names a route, a ticket token, a resolution horizon, and the record-level loop-back.
- [ ] INC pauses outbound champion communication to the operator and names the governance-side owner; INC does **not** give a resolution date.
- [ ] Every macro is under 120 words. If one is longer, it is trying to do investigation; cut.
- [ ] Token placeholders are consistent across all macros — `{champion_first_name}`, `{report_id}`, `{ticket_id}`, `{resolution_date_30_days}`, `{ops_analyst_name}`.

---

## Step 3 — Red-team against the Chapter 03 anti-patterns (15 min)

Read every macro aloud and check it against the three anti-patterns Chapter 03 names. Any macro that fails one of the checks gets a `<!-- fix: ... -->` comment inline.

1. **The "thanks, we've noted it" anti-pattern.** Does the macro open a specific destination ticket with a specific ID, or does it acknowledge without routing? A macro that says "we'll review" without a route is the anti-pattern in disguise.
2. **The record-level loop-close check.** Does the macro tell the champion they will see the outcome *in the record of the report they filed* — not through a separate system, not by DM, not by the operations analyst remembering to update them? Chapter 03 names this as "the single most important design decision in the chapter."
3. **The attribution check.** Does the macro leave room for the attribution surface — specifically, does it respect Field 5's anonymous default and *not* name the operator in the reply? A macro that paraphrases the narrative in a way that identifies the operator breaks the attribution promise.

Fix any `<!-- fix: ... -->` items before Step 4.

### Checkpoint 3 — before Step 4

- [ ] Every macro passes all three checks or carries an explicit fix note.
- [ ] No macro names an operator by implication (narrative paraphrase is scrubbed of identifying detail).

---

## Step 4 — Walk one real report through the plumbing (10 min)

Pick one of the six reports from [Exercise 02](../exercises/exercise-02-two-way-feedback-loop-drill.md) — Report B (Marcus, Legal Operations, the "materially" clause) works well because it is a clean training-and-tooling candidate without incident-shape.

Do three things:

1. **Fill the intake form as if you were Marcus.** Open `field-report-form.md`, pretend you are the champion, and write a filing that matches the six-field schema. Field 4 should be two to four sentences, operator language. Field 5 — anonymous or named? Make the choice and note why in a comment.
2. **Triage the report in 60 seconds.** Which route? Any cross-routing? Would you flag it as attribution-candidate for the quarterly recognition surface?
3. **Paste the appropriate macro and fill the tokens.** If you chose TRAIN as the route, instantiate the TRAIN macro with `{report_id}`, `{ticket_id}`, resolution horizon, and your name as `{ops_analyst_name}`. Read it as Marcus would receive it. If it reads as thanks-but-filed-away rather than routed-with-a-date, you have found the gap in the macro.

### Checkpoint 4 — self-evaluation

- [ ] The filled filing fits the six-field schema cleanly; no field was skipped.
- [ ] The triage took under a minute; if it took longer, the schema is not helping the triage move at Chapter 03's 30-minute cap.
- [ ] The filled macro reads as a route-with-a-date, not an acknowledgment.
- [ ] The response you would send Marcus is under 120 words.

---

## Step 5 — Version the artifacts (5 min)

Both artifacts need a version header and a change-log footer so they survive the first real iteration.

For `field-report-form.md`, add at the top:

```
Version: v0.1 — draft for ops analyst review. Next revision: after
first full triage cycle (expected week 3 of standing operations).
```

For `reply-macros.md`, add at the top:

```
Version: v0.1 — draft for ops analyst review. Macros are reviewed
after the first ten real filings; token set is locked after that.
```

Save both files. The deliverables are the two artifacts, not a write-up about them.

## Deliverables

- `field-report-form.md` — six-field schema with champion-facing help text, versioned header.
- `reply-macros.md` — five macros (POL / TOOL / TRAIN / INC / NEEDS-CLARIFY) with tokens, versioned header.

## Checkpoint — self-evaluation

- [ ] Exactly six fields in the schema; the `incident-shaped observation` enumeration is present verbatim and routes to the Chapter 08 fast path via the INC macro.
- [ ] Field 5 defaults to anonymous; the help text names the Chapter 03 reasoning in one sentence.
- [ ] Four route macros plus NEEDS-CLARIFY; INC omits a resolution date; each macro loops the champion back at the record level.
- [ ] Token set is consistent across all five macros.
- [ ] You walked one Exercise 02 report through the form and macros in under three minutes and the output read as a routed, dated reply.

## What this lab prepares you for

Exercise 02 is runnable in 30 minutes because this lab's artifacts exist. The macros also feed the operations analyst's day-one onboarding — a new analyst can run the triage from the macro file plus Chapter 03 without shadowing a cycle first. The field-report form is the specific instrument Chapter 07's "filings per champion per quarter" metric reads from; building it carefully here is cheaper than rebuilding it after the first quarter's data is unusable because the schema was ambiguous.
