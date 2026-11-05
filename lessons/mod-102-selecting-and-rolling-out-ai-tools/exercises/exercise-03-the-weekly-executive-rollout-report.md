# Exercise 03 — The Weekly Executive Rollout Report

**Estimated effort:** 2 hours
**Format:** one-page executive report, Markdown
**Grounding chapters:** [04 — Measuring Whether the Rollout Changed Anything](../04-measuring-whether-the-rollout-changed-anything.md), [05 — Failure Modes and the Pre-Mortem](../05-failure-modes-and-the-pre-mortem.md)

## Objective

Write the one-page weekly report you would send to your executive sponsor on week 4 of a live AI tool rollout. The report must:

- *Lead with outcome*, not usage — headline a target-task metric, not a license count.
- *Carry workflow signal*, not just numbers — two or three paraphrased lines from this week's interviews.
- *Use adoption as a sanity check*, not a trophy — one quarter of the page at most.
- *Name a pre-mortem failure mode* this rollout is at risk of this week, if any.

If you did the work honestly, half of this exercise is resisting the urge to put the adoption chart at the top.

## Prerequisites

- Chapters 04 and 05 read.
- A chosen organization and a chosen rollout. Carry over the organization from Exercise 01 and the tool/use-policy context from Exercise 02 if you have them. If not, pick one of:
  - a 3,000-person US bank rolling out an AI coding assistant to its 180-person engineering org; target task is **pull-request cycle time on tier-2 service repos**
  - a 12,000-person global pharma rolling out a RAG-based regulatory-document drafting tool to its medical-affairs team; target task is **time to first reviewable draft of a response letter**
  - a 500-person SaaS company rolling out an AI meeting-notes tool to the go-to-market org; target task is **follow-up actions captured per customer meeting, tracked in the CRM**
- An honest view of where instrumentation is. If you do not have real numbers, generate plausible ones for the exercise and label them as simulated; or, write the report against the honest acknowledgment that outcome instrumentation is still being wired up.

## Problem statement

It is Friday of week 4 of the rollout. Your executive sponsor — the CIO, the Chief Medical Officer, the Chief Revenue Officer, whoever bought the rollout — asked for "a weekly one-pager, nothing fancy, so I know whether to keep writing the check." The first version you send sets the frame for every version after it. If you lead with license activations this week, you will be reporting on license activations in week 20.

## Requirements

Deliver a single page with these sections, in this order, with the stated relative weight:

1. **Outcome movement on the target task** — the largest section on the page.
   - One headline number: the movement (or non-movement) in the target-task metric this week, versus the pre-rollout baseline.
   - One paragraph (three or four sentences) interpreting it: what it means, what the confidence is, what confounds it.
   - If the outcome did not move, say so plainly: *"no measurable change on the target task this week; the hypothesis for why is X; here is what is changing next week."* Do not hide a flat week inside a usage chart.
2. **Workflow-interview signal from this week** — two or three bullets, paraphrased, specific.
   - Each bullet is a quote or paraphrase from a user interview or shadowing session this week. Name the role (not the person) and the task.
   - Prefer specific texture over generalities. *"Ryan — tier-2 backend engineer — now drafts the test harness with the tool first and hand-edits; says the first-draft of tests is where the time went"* beats *"engineers find the tool useful."*
3. **Usage sanity check** — no more than a quarter of the page. One line each on:
   - active users this week / weekly-active over licensed
   - cadence (median sessions per active user, or similar)
   - any sharp drop or spike worth flagging
4. **Risks and asks** — bulleted, each named with an owner and a date.
   - Risks: what could kill this rollout in the next two weeks. Named, not abstract.
   - Asks: what you need from the sponsor this week. Zero to two, not five.
5. **Pre-mortem check** — one line.
   - Pointer to the pre-mortem catalog in [Chapter 05](../05-failure-modes-and-the-pre-mortem.md).
   - Name which — if any — of the catalog's failure modes this rollout is sitting closest to this week, and why.
6. **Call to action for the sponsor** — one sentence, at the bottom. What you want them to do, or not do, before next Friday.

## Starter guidance

- The outcome section is where most learners fail. Two ways people fail it: they lead with usage because outcome is hard, or they bury a flat week in hedging language. Write the honest version first. The outcome number is either up, flat, or down, and you know which.
- The workflow bullets are the part the sponsor will actually remember. Three concrete paraphrased observations beat a paragraph of synthesis. The texture is the point.
- The usage sanity check should feel small on the page. If it's taking up a third of your document, you are still writing a usage report with outcome bolted on.
- The "risks and asks" section is where you prevent surprises. If there is a thing the sponsor will find out about from somebody else in the next two weeks, it belongs here, this week.
- The pre-mortem line is cheap to include and expensive to omit. Even "no failure mode from the catalog is close this week" is a useful line — it means you looked.
- Do not invent precise outcome numbers for drama. Either generate a plausible simulated set *and label it simulated*, or write the report against the honest state of instrumentation. Both are valid.
- This is the rollout-level weekly. In [mod-106](../../mod-106-outcome-measurement-and-executive-reporting/README.md) you will roll many of these up into the org-wide executive scorecard; the shape there is different, but the discipline — outcome first, usage as sanity check — is the same.

## Deliverables

- `weekly-rollout-report-wk04.md`: one page, six sections above, in the order above.
- A short appended note (no more than 3 sentences) naming which section you were most tempted to inflate or hedge, and what you did instead.

## Acceptance criteria

- The report fits on one page at normal body-text size. If it spills, cut from the usage section first.
- The outcome section comes first and is the largest section on the page.
- If the outcome did not move, the report says so in plain English with a hypothesis and a next-step — no burying.
- Workflow-signal bullets are specific: named role, named task, paraphrased observation. Generalities like "users like it" do not pass.
- The usage sanity check occupies no more than a quarter of the page and contains no claims about outcome.
- The pre-mortem line is present and either names a failure mode from Chapter 05 or explicitly states none is close this week.
- The call to action is a single sentence. If it is two sentences, cut.
- The appended note (temptation / what-you-did) is three sentences or fewer.

## Stretch goals

- Write a second version of the same week's report *as if you were leading with usage* — the version you were tempted to send. Put the two side by side. In three bullets, name what the sponsor would have asked you about in each case; this tells you what the frame produces.
- Draft the week-5 report in advance, with the outcome number left blank and the risks and asks filled in based on what you expect. On the actual Friday, see how close the pre-filled version was. This is the cheapest forecast-calibration exercise you will do.
- Extract the three or four lines from your report that would survive aggregation into a mod-106 org-wide scorecard (headline outcome, top risk, top ask). This previews the rollup you will do in mod-106.

## Why this exercise matters

Executive sponsors decide whether to keep paying for a rollout based on the frame you give them. Lead with usage and you will spend the rest of the rollout defending a license count. Lead with outcome, even when the outcome is flat, and you train the sponsor — and yourself — to ask the question that matters: *did the target task get better?* The weekly report is the smallest, highest-leverage artifact in the rollout. Getting the first one right costs two hours. Getting it wrong costs the rollout.
