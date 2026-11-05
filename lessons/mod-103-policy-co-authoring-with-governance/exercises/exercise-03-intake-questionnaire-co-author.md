# Exercise 03 — Intake Questionnaire Co-Author

**Estimated effort:** 3 hours
**Format:** completed questionnaire + 1-page memo, Markdown
**Grounding chapters:** [02 — The Governance Council Liaison Seat](../02-the-governance-council-liaison-seat.md), [06 — The Intake Questionnaire](../06-the-intake-questionnaire.md), [07 — What You Route Out](../07-what-you-route-out-counsel-soc-architect.md)

## Objective

Operate the intake questionnaire from the **runner** side for one specific tool request, then write the co-author memo proposing **two refinements** to the questionnaire schema — framed as evidence for `senior-ai-governance-architect` (L50), not as a redesign proposal. The exercise is where the schema-vs-runner distinction becomes real.

## Prerequisites

- Chapters 02, 06, and 07 read.
- The tool and organization you used in Exercises 01 and 02. Carrying the pairing forward produces a coherent artifact set (AUP + SOP + intake) you can present together.
- If you did not do Exercises 01 and 02, pick one of the three organization archetypes from Exercise 01 and sketch the AUP data classes and the SOP accident-path owner in a one-paragraph preamble.

## Problem statement

The BU sponsor from your Exercise 01 tool has formally submitted the tool for approval. You are running the enablement-side intake. You have just completed the 20-minute **pre-review session** with the sponsor and are now filling out the questionnaire on their behalf for submission to `senior-ai-governance-architect` and `head-of-ai-governance`.

You have also been operating intake for two cycles at this organization. You have noticed field evidence suggesting two refinements to the schema that could materially improve classification quality. You are writing the memo to the architect.

Important: the memo is **evidence for consideration**, not a redesign proposal. You are the runner; the architect is the designer. Confusing the two is the lateral drift [Chapter 07](../07-what-you-route-out-counsel-soc-architect.md) names.

## Requirements

### Deliverable A — completed intake questionnaire

Fill out the questionnaire for your tool and organization. Organize the submission under the field groupings from [Chapter 06](../06-the-intake-questionnaire.md):

- Tool identity (vendor, product, version, deployment model, hosting jurisdiction).
- Requester and business justification (BU, sponsor, target task, success criterion, alternatives considered).
- Data classes touched (inputs, outputs, training data, logging data — map to the Exercise 01 classification scheme).
- External disclosure (whether outputs reach customers, partners, public, regulators; whether inputs include third-party-confidential data).
- Cohort size and reach (named populations, sized, role mix, geography).
- Risk-classification prompt inputs (the questions whose answers feed the architect's schema — decision-making posture, human-review gating, regulated-domain context).
- Envelope check ([mod-102 Chapter 01 / Stage 2](../../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) approved-tooling envelope status).
- Policy touchpoints (which AUP sections and which data-handling SOP sections may need revision).

Include a **pre-review session summary** — a 3-sentence note at the top of the submission describing what the enablement-side pre-review surfaced that the raw requester submission would have missed.

Where an organization-specific fact is load-bearing and you do not know it, mark `<!-- needs-research: ... -->` with enough specificity that a partner can close the gap. You may *not* propose a risk classification in the submission — classification is governance's output, not yours.

### Deliverable B — co-author memo to `senior-ai-governance-architect`

A memo of one page maximum, addressed to `senior-ai-governance-architect` (L50) with `head-of-ai-governance` (L60) on cc. The memo proposes **two refinements** to the questionnaire schema with field evidence.

For each refinement:

- 1–2 sentences on the proposed change in general terms (not a redesigned field; a *shape* of change).
- 2–3 sentences of **field evidence** — specific submissions over the last two cycles where the current field set was insufficient, ambiguous, or systematically mis-filled. Named, with submission references (fabricated references are fine for the exercise — "INT-2026-087 and INT-2026-091" — but evidence shapes must be realistic).
- 1 sentence on costs and benefits — what would need to flow through if the refinement were adopted (training update, policy clause revision, re-classification of existing tools).

The memo must frame both refinements as **"evidence for the architect's consideration"** — not as a redesign to approve. The memo must *not* include a proposed field definition, a proposed value enumeration, or a proposed control mapping. Those are the architect's work.

## Starter guidance

- The pre-review session summary is the most load-bearing 3 sentences in the submission. Its purpose is to signal to the architect and the head of governance that this submission has been triaged with operator-side judgment, not rubber-stamped. Write it as "what we surfaced that the raw request did not say."
- **Do not propose a risk classification in the questionnaire.** You collect the inputs; the architect's schema produces the classification; `head-of-ai-governance` ratifies. If you catch yourself writing a classification, delete it and rewrite as risk-classification inputs.
- The **memo's framing is the exercise.** Resist the urge to write the redesigned field in the memo. If you find yourself drafting "here is the new field structure," cut it and rewrite as "here is the evidence that suggests a refinement; the architect's decision on what the refinement should be is what I am asking for."
- Pick refinements that are **realistic for a runner to have evidence on** — field systematically mis-filled, grouping that produces unstable classifications, prompt-input question that is read differently by different requesters. Do not pick refinements that would require architect-level knowledge of the taxonomy (control-library mapping, cross-framework alignment).
- The two refinements should be independent — do not propose two sides of the same change dressed up as two refinements.
- Carry forward: use the data classification scheme from Exercise 01's AUP and the accident-path routing from Exercise 02's SOP as context the questionnaire's "data classes touched" and "policy touchpoints" sections should reflect.

## Deliverables

- `intake-submission.md`: completed questionnaire, including the 3-sentence pre-review session summary and `<!-- needs-research: ... -->` marks where applicable.
- `intake-schema-refinement-memo.md`: 1-page memo to `senior-ai-governance-architect` with `head-of-ai-governance` on cc, containing two refinement proposals framed as evidence for consideration.

## Acceptance criteria

- Both artifacts present.
- Questionnaire covers all eight field groupings from Chapter 06.
- Pre-review session summary is exactly 3 sentences and names what the pre-review surfaced beyond the raw request.
- Questionnaire does not propose a risk classification.
- Memo is one page.
- Memo proposes exactly two refinements.
- Each refinement has: 1–2 sentences on the shape of change, 2–3 sentences of concrete field evidence with submission references, 1 sentence on costs and benefits.
- Memo frames the architect's decision authority explicitly ("evidence for your consideration," "for your call," or equivalent).
- Memo does **not** propose field definitions, value enumerations, or control mappings.
- Both refinements are independent.
- `<!-- needs-research: ... -->` used where organization-specific facts are missing. No invention.
- Data classes referenced match the scheme from Exercise 01's AUP (or the one-paragraph preamble if Exercise 01 was not completed).

## Stretch goals

- Draft the **Slack message** the runner sends to the requester after a stalled submission — the "nudge-upward" micro-artifact. 2–3 sentences, confirming what has stalled, what the next move is, and what the requester can do to unstall it.
- Write the **2-sentence summary** that would go onto the next council agenda for this particular intake (the pre-read format from [Chapter 02](../02-the-governance-council-liaison-seat.md), condensed to agenda-line length).
- Add a **status-tag history** at the top of the submission showing the transitions this item has gone through (`pre-intake` → `intake-in-progress` → `schema-complete` → `awaiting-council-decision`) with dates. Realistic for a running intake artifact.
- Draft the **report-back-to-champions** micro-artifact assuming the council approved the tool with conditions — what you tell champions in the field after the decision.

## Why this exercise matters

Intake is where the role's discipline becomes most visible to governance partners. A questionnaire filled out thoughtfully, with a pre-review summary that surfaces real judgment, and a memo that stays on the right side of the schema-vs-runner line, signals that the enablement seat can be trusted to feed the council well without drifting into architecture. That trust compounds: architects start to pull you into schema conversations earlier, heads of governance start to co-sign your policy drafts faster. The memo in particular is the recurring artifact you will write every cycle in the real role — this is the exercise where you build the muscle of staying on the runner side of the line under pressure.
