# Exercise 04 — Commissioned Tool Measurement Plan

**Estimated effort:** 2 hours
**Format:** measurement plan + eval-vs-outcome split spec + three-cadence running plan + portfolio-scorecard slot mock-up, Markdown
**Grounding chapters:** [05 — Measuring Commissioned Tools on the Rollout Framework](../05-measuring-commissioned-tools-on-the-rollout-framework.md); [02 — The Commissioning Brief as the Load-Bearing Artifact](../02-the-commissioning-brief-as-the-load-bearing-artifact.md); [06 — Signing Surfaces, Maintenance Commitments, and the Hand-Off Calendar](../06-signing-surfaces-maintenance-and-handoff-calendar.md). Prior reading: [mod-102 Chapter 04](../../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md); [mod-106 Chapters 01 and 02](../../mod-106-outcome-measurement-and-executive-reporting/README.md).

## Objective

Author the measurement plan for the commissioned tool from Exercise 01, respecting the two-temptation refusal from Chapter 05. The plan names the two measurement surfaces (eval harness, portfolio-scorecard outcome) and their owners, the three cadences (weekly, monthly, quarterly), the four-quadrant diagnostic the commissioner runs on, and the specific scorecard slot the commissioned tool occupies inside the mod-106 portfolio view. The plan is the artefact the Chapter 06 Hand-Off 3 acceptance meeting verifies alongside the tool itself, and the artefact the first graduate-or-retire review (Hand-Off 4) runs against.

The deliverable is the plan itself, the eval-vs-outcome split spec (who owns what, read at what cadence), the three-cadence running plan (what happens weekly, monthly, quarterly), and a one-page mock-up of the portfolio-scorecard slot.

## Prerequisites

- Chapters 05, 02, and 06 read.
- Exercises 01 and 03 complete (the brief and the handoff contract are in hand; the eval-harness and outcome-metric commitments are specified there).
- [mod-102 Chapter 04](../../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md) re-read as the three-layer measurement stack.
- [mod-106 Chapters 01 and 02](../../mod-106-outcome-measurement-and-executive-reporting/README.md) re-read as the portfolio-scorecard framework. In particular [mod-106 Chapter 02](../../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) names the three-cadence structure this plan attaches to.

## Problem statement

Your commissioned tool is approaching acceptance. The brief's Section 3 named the outcome metric with baseline and target; the handoff contract named the eval-harness commitments. Now you need the measurement plan that makes both surfaces operable from acceptance through the first graduate-or-retire review at T+4 quarters. The plan is read by the commissioner, by the maintenance owner, by the `ai-augmented-analyst` building the scorecard pipeline, and by the exec sponsor who reads the weekly rollup.

Specifically: the plan has to defend against the two temptations from Chapter 05 — substituting the eval harness for the outcome metric, and building a bespoke dashboard — both of which land easily when a commissioned tool is a visible and politically defensible line item. The plan's shape is what keeps the commissioned tool legible in the portfolio view.

## Requirements

### Part A — The measurement plan

A single Markdown document with the following sections:

- **Section 1 — The two surfaces.** Name the eval harness (engineer-owned, model-level quality) and the portfolio-scorecard outcome metric (commissioner-owned, business outcome). One paragraph per surface naming what it measures, who owns it, and who reads it.
- **Section 2 — The three-layer outcome stack.** The outcome metric, the workflow metric, the usage-as-sanity-check floor — all three from the brief's Section 3, re-stated with the specific scorecard surfaces each lives on.
- **Section 3 — The four-quadrant diagnostic.** A table reproducing Chapter 05's four quadrants (eval green/outcome green, eval green/outcome red, eval red/outcome green, eval red/outcome red), with the diagnosis and move named for your specific commission. The moves reference the specific brief sections, maintenance-owner contacts, or Chapter 03 rebuild-or-retire paths.
- **Section 4 — Red-team re-run cadence.** The specific triggers (model-provider major version, data-source change, step-boundary change for agentic tools) and the coordination with `ai-risk-engineer`. The plan names the two-model-provider-release staleness threshold as a pause-until-re-run trigger.
- **Section 5 — The portfolio-scorecard slot.** How this commissioned tool appears on the mod-106 portfolio scorecard — baseline, target, confidence-band shape, misses-first discipline from [mod-106 Chapter 02](../../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md). Explicit refusal of the bespoke-dashboard temptation — no new metric panels are added for this tool unless the panel is added to every tool in the portfolio.
- **Section 6 — Retirement criteria.** The specific target-miss pattern (name the exact rule — e.g., three consecutive quarterly readings below baseline on the outcome metric) that triggers the Chapter 06 Hand-Off 4 graduate-or-retire review's retire outcome. Pre-committed at measurement-plan authoring time, not at retirement-decision time.

### Part B — The eval-vs-outcome split spec

A one-page Markdown document with a table. Columns: **Surface**, **What it measures**, **Owner**, **Who else reads**, **Cadence**, **Where it lives**. Rows cover the eval harness and the portfolio-scorecard outcome metric; optionally, a third row covers a workflow-interview surface (qualitative ground truth from mod-106 Chapter 01).

Each row's **Cadence** entry is specific — "continuous CI-adjacent" for the eval harness, "weekly rollup / monthly deep-dive / quarterly review" for the portfolio-scorecard outcome. Each row's **Where it lives** entry names the specific store — the eval harness in the engineering team's observability stack, the portfolio-scorecard in the mod-106 evidence store, the workflow interviews in the mod-105 champion-network surface.

### Part C — The three-cadence running plan

A one-page Markdown document for each of the three cadences:

- **Weekly.** What appears on the weekly rollup for this commissioned tool. The outcome and workflow metrics with baseline, current, direction, confidence band. The eval-harness number below-the-fold as a supporting indicator. Engineering-side alerts surfaced as a status line, not as a scorecard item.
- **Monthly.** The monthly deep-dive slot. The seven-section structure from [mod-106 Chapter 02](../../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) applied to this commissioned tool, plus the eval-harness trend addendum, plus the four-quadrant read run against the month's readings.
- **Quarterly.** The quarterly slot. The reading against Section 3's fixed target (not against the previous quarter). The graduate-or-retire posture update. The red-team re-run status check.

For each cadence, name the specific agenda and the specific participants.

### Part D — The portfolio-scorecard slot mock-up

A one-page Markdown mock-up showing how the commissioned tool appears on the portfolio scorecard. Use the mod-106 Chapter 02 weekly-rollup five-section structure; populate with the commission's specific numbers (name them as `[placeholder]` if you do not yet have them from Exercise 01's Section 3 — do not invent). Specifically ensure:

- The outcome metric is the headline.
- The workflow metric is a leading indicator paragraph beneath.
- Usage telemetry appears only as a sanity-check line.
- The eval-harness number appears below-the-fold, as a supporting indicator with a one-sentence trend read.
- The tool's panel is the same shape as every other tool's panel in the portfolio. No bespoke panels.

The mock-up is what the exec sponsor sees on the weekly rollup. If it looks different from the other rollouts' panels in your portfolio, it is the bespoke-dashboard temptation landing; fix it.

## Starter guidance

- Section 3's four-quadrant diagnostic is the plan's most useful instrument. Spend the first thirty minutes populating the four quadrants with your commission's specific numbers and moves. Vague quadrant moves ("investigate further") collapse the diagnostic; specific moves ("workflow-interview round with the pilot cohort to test whether Section 1's problem framing is wrong") are what the plan is for.
- Section 6's retirement criteria are the most politically difficult section to write. If you find yourself softening the criteria at authoring time ("two consecutive quarters below baseline with a named structural cause," where the structural-cause carveout is left undefined), you are rehearsing the apologist posture at plan-authoring time. Name the criteria sharp. The Chapter 06 Hand-Off 4 review is where structural causes are weighed; the plan sets the criteria that trigger the review.
- The portfolio-scorecard slot mock-up is the discipline test. If your mock-up has a panel shape that no other tool in your portfolio has, the plan is already inside the bespoke-dashboard temptation. Rewrite the slot to the shape of every other panel.
- For an agentic-tool commission, the eval-harness surface in Part B expands. In addition to answer correctness and step correctness, name the escalation-correctness metric and the guardrail-trigger-accuracy metric. These are agent-specific and should be visible in the eval-harness row.
- The red-team re-run cadence in Section 4 interacts with the maintenance-owner commitment in Chapter 02 Section 7. If the maintenance owner's engineer-days-per-month is not sized to accommodate the re-run cadence, the plan's Section 4 cannot be delivered. Name the interaction explicitly; if the sizing is off, flag it as a brief-revision trigger.
- Where an organisational fact you need is unknown, use `<!-- needs-research: ... -->` inline.

## Deliverables

- `measurement-plan.md` — Part A, the six-section plan.
- `eval-vs-outcome-split-spec.md` — Part B, the table.
- `three-cadence-running-plan.md` — Part C, the weekly/monthly/quarterly agendas.
- `portfolio-scorecard-slot-mockup.md` — Part D, the weekly-rollup slot in the same shape as every other panel.
- A short cover note (3–5 sentences) summarising the specific temptation (eval-harness substitution or bespoke dashboard) you found hardest to resist in the plan's authoring and the structural discipline you applied to resist it.

## Acceptance criteria

- The measurement plan has all six sections. The two surfaces are named with owners and readers; the three-layer outcome stack is re-stated from the brief; the four-quadrant diagnostic is populated with specific moves.
- The red-team re-run cadence is named with specific triggers and a staleness threshold.
- The retirement criteria in Section 6 are pre-committed, sharp, and defensible.
- The eval-vs-outcome split spec table has all six columns with specific entries, not placeholders (except where organisational facts are flagged).
- The three-cadence running plan names the specific agenda and participants for each cadence.
- The portfolio-scorecard slot mock-up has the outcome metric as the headline, the workflow metric beneath, usage as sanity-check only, the eval-harness number below-the-fold — and is the same panel shape as the other rollouts in the portfolio.
- `<!-- needs-research: ... -->` is used wherever an organisational fact is missing.
- Nothing in the plan substitutes the eval harness for the outcome metric; nothing in the plan creates a bespoke dashboard.

## Stretch goals

- Author a **retrospective companion** — a one-page retrospective-template that the Chapter 06 Hand-Off 4 graduate-or-retire review will fill in, including the four-quadrant readings over the four preceding quarters, the maintenance-owner commentary, and the graduate / continue / retire recommendation with its evidence. Pre-authoring the template at measurement-plan time makes the hand-off meeting procedural rather than improvised.
- Draft a **scorecard-coordination contract** with the `ai-augmented-analyst` — one page — naming the specific data pipelines the analyst maintains, the refresh cadences, and the data-governance surface ([mod-106 Chapter 06](../../mod-106-outcome-measurement-and-executive-reporting/06-coordinating-with-the-analyst-and-the-team-manager.md)). This is the dependency the plan's weekly cadence rests on.
- Draft a **"what moves this tool off the scorecard"** memo — one page — naming the three paths the tool exits the scorecard on (graduation to annual-cadence portfolio view, retirement, replacement by a commercial tool that emerged in the mod-107 Chapter 05 consolidation cadence). Each path is named with the artefact that triggers it and the close-the-loop feedback into mod-103/104/106.

## Why this exercise matters

A commissioned tool whose measurement plan is weak is a tool whose budget defense collapses at the first mod-107 Chapter 04 Finance review and whose retirement is deferred until the fourth consecutive miss when it should have been retired at the third. The plan is the surface on which the commissioner's authority to retire, graduate, or defend the tool rests — and it is the surface the governance council reads when deciding whether the enablement program's internal-build line items are earning their place in the portfolio. Producing all four parts under a two-hour budget is calibration for producing them under live portfolio pressure, when the quarterly review is on the calendar and the scorecard is red.
