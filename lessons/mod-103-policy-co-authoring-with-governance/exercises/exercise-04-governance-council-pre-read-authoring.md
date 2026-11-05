# Exercise 04 — Governance Council Pre-Read Authoring

**Estimated effort:** 2 hours
**Format:** 1-page pre-read, Markdown
**Grounding chapters:** [02 — The Governance Council Liaison Seat](../02-the-governance-council-liaison-seat.md)

## Objective

Write the 1-page pre-read you send 48 hours before the next AI governance council meeting. The pre-read must cover **three in-flight items**, one for each of the three jobs the enablement lead does at council: feed the intake workflow, provide risk-classification input, surface field signal from champions. The exercise's constraint — one page, three sections, named ask per item — is the exercise.

## Prerequisites

- Chapter 02 read.
- The organization you used in Exercises 01–03 (or one of the three archetypes from Exercise 01) is your council context.
- Optional: the completed intake questionnaire from Exercise 03 gives you a ready-made Section 1 ("Intake pipeline update") item. Carrying it forward produces a coherent set.

## Problem statement

The AI governance council meets on Tuesday. It is Friday afternoon. The council chair, `head-of-ai-governance` (L60), has asked for pre-reads to land in the shared drive by Monday morning. The enablement seat's pre-read is one of five going into the packet; the others come from counsel, the CISO, the DPO, and the `senior-ai-governance-architect`.

Your pre-read is the operating-model view of what is happening in the field. It must be tight enough to read in five minutes and specific enough that each item has a decision or discussion ask the council can act on.

## Requirements

A single-page pre-read with a short header and three sections, in this order.

### Header

- Council date.
- Chair: `head-of-ai-governance` (L60).
- Attendee roles (role names, not people names).
- Author: this role.

### Section 1 — Intake pipeline update

Two to four lines on tools and requests currently in flight through the intake workflow ([Chapter 06](../06-the-intake-questionnaire.md)). Each item carries a **status tag**:

- `pre-intake`
- `intake-in-progress`
- `schema-complete`
- `awaiting-council-decision`
- `council-deferred-from-last-cycle`

Items awaiting a decision this cycle must be flagged with the decision ask (approve / decline / defer).

### Section 2 — Risk-classification input

**One named tool** whose field-level usage over the last cycle changes what classification it should receive, with **three bullets** of field evidence:

- The cohort that is actually using the tool (size, role mix, geography).
- The task mix observed (via workflow interviews or champion reports).
- The data classes observed in operator practice.

**Do not propose a classification.** You provide inputs; classification is the architect-and-head-of-governance output. Frame the section as "classification inputs for council review" with a named ask of *discussion* or *decision*.

### Section 3 — Field signal from champions

**One trend or pattern** the champion network has surfaced since the last council — not a single-user anecdote. Minimum threshold: at least three champions reporting the same pattern, or the same pattern observed across at least two business units. Include:

- A one-sentence description of the pattern.
- A one-sentence description of the evidence that confirms it is a trend (how many champions, over what window, across which BUs).
- A one-sentence recommended action **framed as input** — "Recommend the council consider whether AUP Section 3 should add approved use X" — not as a decision to ratify.

### Named ask per section

Every section ends with its **named ask**: `decision`, `discussion`, or `informational`. "Informational" is a legitimate ask; if all three sections are informational, the pre-read is not using the seat.

### Length constraint

The whole pre-read must fit on one page at normal body-text size. No section may exceed six lines of body text. The constraint is the exercise.

## Starter guidance

- The hardest section is **Section 3 (field signal)**. The failure mode is dressing up a single champion's complaint as a trend. Hold yourself to the "at least three champions or at least two BUs" threshold even for an exercise — the discipline is what makes the field-signal job useful to the council.
- **Status tags in Section 1** are not optional. The point of this section is for the council to see the state of the pipeline in one glance. Items without status tags force the chair to ask, which wastes meeting time.
- **Section 2 must not propose a classification.** If you catch yourself writing a classification, rewrite as classification inputs. The architect and head of governance produce the classification; your value is the field evidence they classify against.
- The **named ask** is what makes the pre-read usable. If a section has no ask, the council does not know what to do with it. "Informational" is a legitimate ask only if that section genuinely does not need a council decision this cycle.
- **Role names, not people names.** Role names survive personnel changes; people names do not. If you find yourself writing "Sarah from the CISO's office," rewrite as "CISO delegate."
- Do not invent organization-specific facts. Mark `<!-- needs-research: ... -->` inline where you would need a real cohort size, a real champion count, a real BU list.
- If you carried forward the Exercise 03 intake submission, Section 1 should name that submission explicitly with its status tag. Coherence across exercises is the point.

## Deliverables

- `council-pre-read.md`: one page, header plus three sections in the required order, named ask per section.

## Acceptance criteria

- Fits on one page at normal body-text size. If it spills, cut.
- Header present with council date, chair, attendee roles, author.
- Three sections present in the required order (intake pipeline, risk-classification input, field signal).
- Section 1: at least two in-flight items, each with a status tag.
- Section 2: one named tool, three bullets of field evidence, no proposed classification.
- Section 3: one trend (not an anecdote), explicit evidence that it crosses the "three champions or two BUs" threshold, recommended action framed as input.
- Each section ends with an explicit named ask (`decision`, `discussion`, or `informational`).
- No section exceeds six lines of body text.
- Role names used throughout (no people names).
- `<!-- needs-research: ... -->` used where organization-specific facts are missing. No invention.

## Stretch goals

- Write the **3-sentence Slack message to `head-of-ai-governance`** that accompanies the pre-read, naming the two items you expect to be most contested and why.
- Draft the **report-back-to-champions template** you would send 2–3 business days after the council, assuming the council acted on your Section 3 field signal.
- Add a **"watch next cycle" footer** of 1–2 lines on a trend you expect to surface at the *following* council but that is not yet mature enough to include this time.
- Sketch the **bilateral agenda** for the 30-minute meeting with `head-of-ai-governance` the day before the council, prioritizing which items need pre-alignment on house position.

## Why this exercise matters

The pre-read is the recurring artifact the enablement seat produces every council cycle. Its quality shapes how the council treats the enablement voice over time: a tight, specific, named-ask pre-read earns the seat weight; a vague, informational-only pre-read loses it. The one-page constraint and the three-section structure force the discipline the chapter describes, and the muscle you build in this exercise is the one you use every month in the real role.
