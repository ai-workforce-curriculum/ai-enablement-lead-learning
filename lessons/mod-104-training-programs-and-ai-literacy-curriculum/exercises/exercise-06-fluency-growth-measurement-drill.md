# Exercise 06 — Fluency Growth Measurement Drill

**Estimated effort:** 3 hours
**Format:** a measurement artifact set of 3–5 pages, Markdown or docx
**Grounding chapters:** [07 — Measuring Fluency Growth](../07-measuring-fluency-growth.md), [02 — Audience Segmentation and Fluency Targets](../02-audience-segmentation-and-fluency-targets.md)

## Objective

Produce the three measurement artifacts a literacy program needs to defend itself in an exec review and an auditor walk-through: a **pre/post assessment design**, **one complete task-level rubric**, and a **fluency scorecard template**. These are the artifacts that separate a literacy program from an attendance program.

## Prerequisites

- Chapter 07 read; Chapter 02 revisited.
- Fluency target map from Exercise 01 in hand (the named tasks are the inputs to the rubric).
- Role-based playbook from Exercise 03 in hand (one of its use cases is the rubric's subject).

## Problem statement

Your exec sponsor has asked for "the proof the program is working" at the next quarterly review — four weeks away. The scorecard you have today reports completion rates and satisfaction scores; those numbers are not going to carry the review. You need the measurement stack from Chapter 07 operationalized to the point that at the Q+1 review you can show *fluency growth*, not attendance.

## Requirements

Deliver three artifacts in one document.

### Artifact A — Pre/post assessment design (1 page)

Specify:

#### 1. Assessment scope

- Which tier and which cohort are being assessed (match your fluency target map from Exercise 01).
- The in-scope population size.
- The windows: pre-assessment at onboarding or at cohort start; post-assessment at curriculum-completion + 30 days (so behavior change has started to land).

#### 2. The two layers of items

- **Knowledge check:** item bank design — total pool size, items per attempt, item-rotation policy, pass bar. Specify at least one example item in full (scenario, choices, correct answer, source document).
- **Artifact production:** the task operators produce at post-assessment. Specify the prompt, the data they receive, the time budget, the submission format.

#### 3. Scoring and comparison

- Who scores what (LMS auto-grades knowledge; specialist-tier contributor or manager grades the artifact against the rubric from Artifact B).
- How pre and post are made comparable (rotated items from the same bank; same rubric version).
- The anti-inflation move you take against self-report bias.

### Artifact B — One complete task-level rubric (1–2 pages)

Pick one task from the role-based playbook you authored in Exercise 03. Build its rubric in full, matching the shape from Chapter 07:

#### Rubric header

- Task name.
- Rubric version and date.
- Author trio (function senior IC, specialist contributor, enablement lead with governance co-signer).

#### Rubric body

A table with:

- 4–7 rows of named criteria.
- A 1–4 scale (or 1–5 if you prefer and defend the choice).
- Descriptors for each cell — what distinguishes a "3 — meets" from a "4 — exceeds" is a specific, observable difference, not a vibe.
- A "quality bar" specification — which rows have to hit which score for a submission to count as proficient.

#### Rubric use

A short section (3–5 sentences) specifying:

- Who scores (manager, peer, specialist, or AI-assisted with sample validation).
- How often.
- What happens with a sub-bar score — coaching routing, not punishment.

### Artifact C — Fluency scorecard template (1 page)

The one-page artifact the operations analyst maintains monthly. Build the template; do not fill it with real numbers.

#### Rows

- One per tier (leadership, operators, specialists, builders).
- One per major function.

#### Columns

- Completion rate (L1), split by tier / function.
- Average knowledge-check score (L2).
- Share of operators meeting the rubric quality bar on named tasks (L3) — reference the rubric from Artifact B.
- Headline business-outcome delta, sourced from the function's system of record (L4) — reference [mod-106](../../mod-106-outcome-measurement-and-executive-reporting/README.md).
- Open issues: lapsed records, failed rubric cohorts, incident signals.

#### Freshness and ownership

- Who maintains, how often.
- The monthly CoE review cadence; the quarterly exec extract.

## Starter guidance

- The scenario-based knowledge item is the single most-skipped detail. Write *one* in full — a scenario, four choices, the correct answer with its policy citation, the common distractor and why it is wrong. That one item is the template for the next 50; without it, the item bank is vapor.
- The rubric descriptors are the hardest part. Resist adjectives ("good," "clear," "effective"). Write observable features: "Every number named in the draft is cross-referenced to the source document" is a descriptor; "Writing is clear" is not. If a descriptor can't be scored by two different graders arriving at the same score, rewrite it.
- The anti-inflation move in Artifact A is specific and worth investing in. Options: (a) comparable-but-different items pre and post, (b) a hidden anchor item that is identical at pre and post to measure test-taking skill drift, (c) a rubric-graded artifact at both windows instead of a self-report survey. Pick one; defend the choice.
- Scorecard numbers do not go in this exercise. The deliverable is the *template* — the thing the operations analyst fills every month. If you write fake numbers, you are over-building the exercise.
- Refer to Josh Bersin AI-in-L&D and Microsoft Work Trend Index framing in Chapter 07 as *context*, not as targets. Do not put a "beat the Microsoft benchmark" row in the scorecard — the denominators are not comparable.

## Deliverables

- `fluency-measurement-stack.md` (or `.docx`): the three artifacts above in one document.
- A short *audit-walkthrough script* (5–8 sentences) summarizing how you would use these three artifacts to answer an auditor asking "show me that the program is working."

## Acceptance criteria

- Pre/post assessment design specifies population, timing, item design, and anti-inflation moves.
- At least one full example knowledge-check item is included.
- The rubric covers one task from the Exercise 03 playbook with 4–7 criteria, a defensible scale, and observable descriptors.
- The scorecard template has at least four L1–L4 columns and is organized by tier and function.
- The author trio for the rubric is named; the scorecard owner is named; the ownership and cadence sections are specific.
- The audit-walkthrough script connects the three artifacts into a defensible story.

## Stretch goals

- Author the full 10-item knowledge-check bank for one module of your foundational curriculum (from Exercise 02). Each item grounded in a specific policy text.
- Run the Exercise 03 playbook's recommended prompt pattern on a synthetic input, score the output against the rubric you just built, and note two revisions to the rubric that would make scoring more reliable.
- Design the dashboard that aggregates the scorecard across tiers into the exec-scorecard view in [mod-106](../../mod-106-outcome-measurement-and-executive-reporting/README.md). One page, visual, readable in 60 seconds by a non-technical executive.
- Draft the lapse-handling SOP — the process when a completion record falls past the refresh cadence. This is the operations piece that keeps the scorecard honest.

## Why this exercise matters

Most AI literacy programs cannot survive an exec review beyond year one because they do not have the measurement stack to prove growth. Programs that operationalize the stack get budget compounding year over year; programs that do not get cut. Building the three artifacts here produces the substrate the next three years of program budgeting defend themselves on.
