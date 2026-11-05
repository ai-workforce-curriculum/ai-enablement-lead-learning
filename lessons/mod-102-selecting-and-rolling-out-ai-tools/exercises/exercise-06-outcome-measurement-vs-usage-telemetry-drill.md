# Exercise 06 — Outcome Measurement vs. Usage Telemetry Drill

**Estimated effort:** 2 hours
**Format:** three short written rewrites plus diagnoses and owner notes, Markdown
**Grounding chapters:** [04 — Measuring Whether the Rollout Changed Anything](../04-measuring-whether-the-rollout-changed-anything.md), [05 — Failure Modes and the Pre-Mortem](../05-failure-modes-and-the-pre-mortem.md)

## Objective

Train the reflex of leading a rollout report with the *outcome* question and demoting usage telemetry to a sanity check. You will take three draft rollout reports that lean heavily on usage numbers, rewrite the lead paragraph of each so it starts from the outcome (or honestly names the fact that outcome is not yet instrumented), name the Chapter 05 failure mode the draft is sliding into, and write a three-sentence note to the rollout owner on what to change next week to produce real evidence.

The drill is short on purpose. The skill is noticing the swap *fast*, in a meeting, before the usage slide carries the room.

## Prerequisites

- Chapter 04 read, with the outcome-vs-telemetry distinction clear in your head.
- Chapter 05 read, with the named failure modes close enough to hand that you can pick one by its name rather than paraphrasing it.
- You have sat through at least one real rollout review in your working life, or can plausibly imagine one. If not, re-read Chapter 03 on the artifact set first so the scene is concrete.

## Problem statement

You are the AI Enablement Lead. Three different rollout owners from three different parts of the business have each sent you a draft one-paragraph update for the monthly steering committee. Each draft leans on usage telemetry — adoption percentages, seats, logins, prompts per day, satisfaction scores — and buries or omits the outcome question the pilot was supposed to answer. The steering committee meets in four days. You have time to send each owner a rewrite and a short note on what to change next week.

The three drafts follow. Treat them as *illustrative fictional drafts*, not sourced data; the numbers are plausible scene-setting, not real.

### Vignette A — professional-services firm, drafting assistant

> **Draft report from the Legal & Advisory Practice Lead:**
>
> "We rolled the drafting assistant out to 1,200 associates and partners across the firm in October. Adoption has been strong — 78% of licensed users logged in at least once in the first three weeks, and daily active usage has settled at around 540 people. Feedback in the internal channel has been broadly positive, with several partners calling it a step change. We recommend expanding the licence pool in Q1 to cover the remaining practice groups."

The original pilot charter named *time to first client-ready draft* as the target task. The draft report does not mention it.

### Vignette B — regional bank, meeting-notes tool

> **Draft report from the Retail Banking Operations Director:**
>
> "The meeting-notes tool is live for 900 seats across Retail Banking Operations. In the first month we saw 870 of those seats activated, an average of 2.3 logins per user per week, and roughly 14,000 prompts logged against the service. Usage is trending up week over week. On the strength of this engagement we are proposing to extend the tool to Commercial Banking in the next quarter."

The pilot was commissioned against a complaint that managers were spending too long writing up decisions after meetings and that follow-up actions were being lost. Neither of those is mentioned in the draft.

### Vignette C — software-vendor support operations, support copilot

> **Draft report from the Head of Customer Support Operations:**
>
> "Our support copilot pilot wrapped its first quarter with a user-satisfaction score of 4.6 out of 5 across the 220 agents in the pilot cohort. Agents told us in the survey that the tool is 'genuinely useful' and that they would be unhappy to lose it. We consider the pilot a clear success and are moving to full rollout across the 1,400-person support organisation next quarter."

The pilot charter named two outcome metrics: median *ticket resolution time* and a sampled *resolution quality* score from the QA team. Neither is reported in the draft.

## Requirements

For each of the three vignettes, produce the following three pieces:

1. **Rewrite (one paragraph, roughly the same length as the original).** Lead with the outcome metric the pilot was supposed to move, or — if the vignette gives you no evidence on it — lead with an honest acknowledgement that the outcome is not yet instrumented and that the usage numbers alone do not answer the question the pilot was asked. Demote the usage numbers to a sanity-check sentence. Do not invent specific outcome numbers the vignette has not given you; the point is to re-frame, not to fabricate.
2. **Diagnosis (two to four sentences).** Name the specific Chapter 05 failure mode the original draft is sliding into. Quote the failure mode by its chapter name. Explain in one or two sentences *why* the draft fits it. If more than one failure mode applies, pick the dominant one and say so.
3. **Note to the rollout owner (exactly three sentences).** Address the owner by role (not name). Tell them the single concrete thing to change *next week* to get real evidence on the outcome question. This is an instruction, not a lecture — write it as you would actually send it.

Across the three vignettes together, your diagnoses should cite at least two *different* failure modes from Chapter 05. If you end up naming the same failure mode three times, re-read the chapter and try again — you are missing distinctions.

## Starter guidance

- The rewrite is not a critique of the original. It is the paragraph the owner *should have sent*. Write it in their voice, not yours.
- "Outcome not yet instrumented" is a legitimate lead when the vignette gives you no outcome data. It is often the honest answer and it is almost always more useful to the steering committee than another adoption percentage. Do not dodge it.
- The usage numbers are not worthless — they are the sanity check that the tool is actually in use. Keep them. Demote them. One sentence, late in the paragraph, phrased as "on the usage side" or similar.
- The owner note is the hardest piece. It has to be specific enough that the owner knows what to do on Monday. "Instrument the outcome metric" is not specific enough. "Pull last week's ticket resolution times from the ticketing system for the pilot cohort and the matched control cohort, and bring the delta to Thursday's review" is.
- Chapter 05 names its failure modes in headings. Use those names verbatim in your diagnoses; do not paraphrase. The exercise is partly a vocabulary drill.

## Deliverables

- `outcome-vs-telemetry-drill.md` (or three short files, one per vignette): for each of A, B, C, a rewrite paragraph, a diagnosis, and a three-sentence owner note, in that order, under a clear heading per vignette.
- A short closing note (no more than four sentences) naming which of the three vignettes you found hardest to rewrite honestly and why. This is a self-check — the one that was hardest is usually the failure mode you are most prone to committing yourself.

## Acceptance criteria

- Each of the three rewrites leads with the outcome question or an honest acknowledgement that outcome is not yet instrumented. If a rewrite still opens with an adoption percentage, a seat count, or a satisfaction score, it has not landed — redo it.
- Each rewrite is roughly the same length as the original draft. No padding, no shrinking it down to a slogan.
- Each diagnosis cites a failure mode from Chapter 05 by its chapter-heading name. Across the three vignettes, at least two distinct failure modes appear.
- Each owner note is exactly three sentences, addresses the owner by role, and names a concrete action that can plausibly be done in one working week.
- No invented outcome numbers. If the vignette does not give you a number, the rewrite does not fabricate one.
- The closing self-check names one specific vignette and one specific reason. "They were all hard" does not count.

## Stretch goals

- Write a fourth vignette of your own, drawn from a rollout report you have actually seen (anonymise it). Put it through the same three-piece treatment. This is where the exercise starts to pay for itself — the drafts you catch in your own history are the ones you are most likely to send yourself.
- For Vignette B specifically, sketch — three bullets — the *pre-mortem* you would have run before launch that would have surfaced the missing outcome instrumentation before the first monthly review. Cross-reference Chapter 05.
- Pick one of your three owner notes and draft the *second* note you would send if, a week later, the owner came back with another usage-heavy update. The second note is almost always harder than the first and is where the role actually gets tested.

## Why this exercise matters

Usage telemetry is the easiest number to produce and the easiest number to defend. It is also the number that lets a rollout run for a year without anyone noticing that the thing the tool was bought to change has not changed. The AI Enablement Lead is the person in the room whose job it is to notice — out loud, in the meeting, before the deck moves on. That reflex is small, fast, and verbal; it is trained by drill, not by theory. This exercise is the drill.
