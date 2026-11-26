# Lab 01 — Author the Analyst-Ready Metric Specification (Specs, Not Names)

**Duration:** 60–75 minutes
**Format:** guided hands-on — specification authoring + red-team pass
**Grounding chapters:** [06 — Coordinating with the Analyst and the Team Manager](../06-coordinating-with-the-analyst-and-the-team-manager.md), [01 — The Measurement Stack at Org Scope](../01-the-measurement-stack-at-org-scope.md), [02 — Authoring the Executive Scorecard — Weekly, Monthly, Quarterly](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md)

## Objective

Produce the **metric-specification sheet** the `ai-augmented-analyst` (L20) can build a dashboard against for one rollout in your portfolio — the artifact Chapter 06 names as the first input the enablement lead owes the analyst. The sheet carries, in one document: the metric specification paragraph (not the metric name), the cohort definition, the baseline provenance, the confidence-band construction method, the three Chapter 02 annotations, the priority timeline, and the SQL-level pseudocode the analyst will turn into live queries. By the end of the lab, the sheet is specific enough that a competent analyst who has never spoken to you could build the dashboard from the document alone.

## Prerequisites

- [Chapter 06](../06-coordinating-with-the-analyst-and-the-team-manager.md) read, with particular attention to the four inputs the analyst needs (metric specifications, cohort definition, baseline provenance, priority stack) and the two things the enablement lead does not delegate (setting metric priorities, writing the narrative).
- [Chapter 01](../01-the-measurement-stack-at-org-scope.md) read; the Layer 1 outcome-metric discipline (confidence band, defensible denominator) is where the specification lives.
- [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) read; the three annotations (metric definitions, baseline provenance, confidence framing) are the fields this sheet will populate.
- One specific rollout chosen. Pick one task family — drafting, summarization, meeting-notes, support-ticket resolution, code review, retrieval, or analyst research — and one specific target workflow inside it. If you did Exercise 01, reuse the rollout from Part B.
- A blank working file — `metric-spec.md`.

## Why a lab, not an exercise

[Exercise 01](../exercises/exercise-01-outcome-vs-usage-metric-framework.md) builds the per-rollout *framework* — a one-page template the rollout owner fills in with the outcome metric, the workflow-interview commitment, the telemetry sanity check, and the theatre watchlist. [Exercise 02](../exercises/exercise-02-the-weekly-executive-scorecard.md) writes the weekly rollup that *reads* from the live metric; [Exercise 06](../exercises/exercise-06-roi-numerator-and-denominator-defence.md) writes the ROI narrative that *aggregates* over metrics. Neither builds the analyst-ready specification that sits between the framework and the dashboard. This lab is that specification — the layer where "time to first draft" stops being a name and becomes a defensible query the analyst can write and the Finance partner can audit. If you tried to run Exercise 02's Section 1 and felt you were making up numbers because the underlying specification was thin, this is the layer below that fills the gap.

## Setup

Open `metric-spec.md` and paste this skeleton. You will fill it in as you walk Steps 1–6.

```markdown
# Metric Specification — <rollout-slug> — v0.1 (draft)

**Owner (specification):** AI Enablement Lead — <your-name>
**Owner (build):** ai-augmented-analyst — <analyst-name>
**Owner (team-level measurement):** ai-augmented-team-manager — <tm-name>
**Status:** v0.1 draft, pre-first-build

## 1. Target workflow (one sentence)

## 2. Metric specification paragraph (the specification, not the name)

## 3. Cohort definition

## 4. Baseline

## 5. Confidence-band construction method

## 6. Annotations (Chapter 02 — metric definition, baseline provenance, confidence framing)

## 7. Priority and timeline

## 8. SQL-level pseudocode (analyst-facing)

## 9. Red-team notes
```

---

## Step 1 — Name the target workflow in one sentence (5 min)

Chapter 01's Layer 1 discipline begins with the target workflow, not the tool. In Section 1, write one sentence that names the workflow the rollout is intended to change, in the operator's own vocabulary. Three rules:

- The workflow is named, not the tool. "Legal associates drafting first-pass client advisories on cross-border matters" is a workflow. "Drafting AI rollout" is not; it is a tool-centric framing that will cause the dashboard to measure logins instead of drafts.
- The workflow is scoped tightly enough to have a measurable start and a measurable end. "Marketing content production" is too wide; "producing the first-pass product-launch announcement draft after the brief is accepted" has a start event and an end event the analyst can join on.
- The workflow does *not* include the AI tool's name. The specification should still make sense if the rollout switched vendors next quarter.

### Checkpoint 1 — before Step 2

- [ ] Section 1 contains one sentence, at most two.
- [ ] The sentence names a workflow, not a tool.
- [ ] The sentence contains a measurable start and end — events an analyst could point at in a source system.

---

## Step 2 — Write the specification paragraph (15 min)

This is the paragraph that makes "time to first draft" stop being a name. The Chapter 06 test is explicit: a metric name without a specification produces a dashboard that will not survive its first Finance challenge.

In Section 2, write a specification paragraph of 80–150 words that answers, in order, each of these six questions:

1. **What is measured?** The directly observed quantity — a duration, a count, a rate, a classification, a score. Name the unit (minutes, matters-per-week, defects-per-100-drafts, 1–5 rater score).
2. **On which events does the measurement start and stop?** Name the source-system events by their names in that system — "the `draft.started` event in the drafting tool" and "the `review.requested` event in the matter-management workflow system." If the events do not exist yet, the specification says so and routes to an upstream instrumentation ask.
3. **At what aggregation grain?** Operator-day, operator-week, matter, ticket, team-week. The grain determines the denominator; the denominator is the first thing a skeptical CFO will attack ([Chapter 01](../01-the-measurement-stack-at-org-scope.md)).
4. **With what inclusion filter?** Which work-shape is in scope — "retained-client advisory matters only," "tier-1 support tickets excluding escalations," "pull requests under 500 lines." Inclusion filters are where comparability lives; a specification without them aggregates across workflows that are not the same workflow.
5. **With what outlier handling?** Winsorize at the 99th percentile; drop operator-weeks with fewer than three matters; drop observations before the operator has used the tool twice. State the rule explicitly; "handled appropriately" is not a specification.
6. **Reported at what cadence?** The weekly rollup carries this as directional, the monthly deep-dive as a trajectory vs. quarterly target, the quarterly review as a portfolio rollup with confidence band ([Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md)). Specify the refresh cadence; the analyst builds against it.

A worked opening (fictional, drafting rollout):

> *Primary outcome: median elapsed business-minutes from the `draft.started` event in the drafting tool to the first `review.requested` event in the matter-management workflow system, aggregated at the operator-week grain. Inclusion filter: retained-client advisory matters only (matter-type codes RC-01 through RC-07). Outliers: operator-weeks with fewer than three matters are dropped; the top and bottom 1% of per-matter durations are winsorized within operator-week before the median is taken; the operator's first two matters post-tool-activation are excluded. Reported weekly as directional move vs. baseline; monthly as 90% CI trajectory vs. quarterly target; quarterly as portfolio rollup in the drafting-workflow category.*

The opening is 125 words. If yours is under 80, you have under-specified; if yours is over 200, you have put narrative in the specification. Narrative lives in the deep-dive, not the spec.

### Checkpoint 2 — before Step 3

- [ ] Section 2 answers each of the six questions explicitly; no question is skipped.
- [ ] Source-system events are named by their names in the source system, not paraphrased.
- [ ] The aggregation grain is stated and corresponds to a denominator you can defend.
- [ ] The inclusion filter is scoped to one work-shape; if the rollout spans two work-shapes (retained vs. new-matter advisory, tier-1 vs. tier-2 tickets), the specification says they are measured separately with linked but distinct specifications.

---

## Step 3 — Cohort, baseline, and confidence band (15 min)

Three fields the analyst needs that the specification paragraph does not carry on its own.

### Section 3 — Cohort definition

Which operators are in scope. State it as four items:

- **Role predicate.** The HR-system role codes or title patterns the cohort is pulled from. "Associates (roles ASSOC-1, ASSOC-2, ASSOC-3) in the Legal function (dept-code LEG-*)."
- **BU predicate.** Which business units. The cohort crosses the role × BU × tool coverage matrix from Chapter 01; name the cells.
- **Tool-activation predicate.** How the analyst detects "has the tool." Enterprise-seat allocation plus at least one authenticated session; *not* "logged in once ever."
- **Time-in-scope predicate.** The observation window — "week 5 through end of quarter," with the first four weeks excluded as the novelty-dampening period from [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md)'s threats-to-validity list.

### Section 4 — Baseline

Chapter 06 calls this *baseline provenance*. Three items:

- **Baseline value.** The pre-rollout number, with its denominator. "4.2 hours median time-to-first-draft, n=180 associates, 8-week pre-rollout window."
- **Baseline provenance.** Where the number came from. One of: the pilot charter (from [mod-102 Chapter 02](../../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md)); a prior measurement over a stated window; a sampled ground-truth exercise with named dates; a reconstruction from workflow-system logs with a named analyst. "To be measured" is not a provenance; if the baseline does not exist, the specification says so and the rollout cannot launch against this metric until the baseline is instrumented.
- **Baseline freshness.** When the baseline was taken; at what cadence it will be refreshed (if ever); the rule for when a baseline is retired (usually: never retired without a published scorecard event per Chapter 01's moving-goalpost discipline).

### Section 5 — Confidence-band construction method

Chapter 04 Pattern 1 and Chapter 02's confidence-framing annotation. Three items:

- **Band construction.** Name the method — bootstrap over operator-level deltas (preferred), parametric confidence interval, organizational standard. One sentence of justification.
- **Band width.** 90% by default; state it.
- **What the band *does not* include.** The band covers sampling variance in the outcome measurement. It does *not* cover attribution uncertainty (that lives in the Chapter 05 ROI sensitivity analysis), it does *not* cover measurement-definition drift (that lives in the scorecard event log), and it does *not* cover concurrent-operational-change bias (that is a methodology-appendix note). Say this explicitly; it is the single most common Finance methodology challenge.

### Checkpoint 3 — before Step 4

- [ ] Section 3 has all four predicates; the cohort can be reproduced from the predicates alone.
- [ ] Section 4 has a baseline value *and* a named provenance; "baseline TBD" fails and routes to an upstream ask.
- [ ] Section 5 names the construction method, the band width, and the three things the band does not cover.

---

## Step 4 — The three Chapter 02 annotations in one place (5 min)

Chapter 02 names three annotations as the quiet infrastructure that keeps the scorecard auditable six months later: *metric definitions*, *baseline provenance*, *confidence framing*. Sections 2, 4, and 5 above already carry them in substance; Section 6 pulls them into a single auditable block that will live in the quarterly review's methodology appendix.

In Section 6, produce three short sub-items:

- **6.1 Metric definition.** A one-paragraph version of Section 2 rewritten in auditor voice — a reader who has not seen the dashboard can reconstruct what is being measured. This is the paragraph that will be cited in the quarterly review by name.
- **6.2 Baseline provenance.** A one-sentence version of Section 4 — the baseline, its source, and the date it was taken. Published alongside every portfolio-level number that touches this metric.
- **6.3 Confidence framing.** A one-sentence statement of the confidence band and its construction — the "22% (90% CI: 14%–29%, bootstrap over operator-level deltas)" form from Chapter 02.

Section 6 is the field that ships verbatim into the methodology appendix. Keep it tight and auditor-ready.

### Checkpoint 4 — before Step 5

- [ ] Section 6 contains three sub-items 6.1, 6.2, 6.3 in order.
- [ ] 6.1 reads as auditor voice (no first person, no program-internal shorthand).
- [ ] 6.2 and 6.3 are each one sentence.

---

## Step 5 — Priority and timeline; analyst-facing pseudocode (15 min)

Two sections the analyst needs to schedule the build and start writing SQL.

### Section 7 — Priority and timeline

Chapter 06's fourth analyst input is the priority stack and timelines. Three items:

- **Priority tier.** Tier 1 (the scorecard front line; builds first), Tier 2 (the monthly-deep-dive back-up metric), Tier 3 (future-quarter aspirational). The enablement lead sets the tier; the analyst executes against it.
- **Build-by date.** When the dashboard is expected live for the first weekly rollup; when it is expected for the first monthly deep-dive; when the methodology appendix cell is expected for the next quarterly review.
- **Dependencies.** Upstream events, data-pipeline additions, source-system permissions, DPA review for vendor telemetry ([Chapter 06](../06-coordinating-with-the-analyst-and-the-team-manager.md) data-governance surfaces). Every dependency has a named owner.

### Section 8 — SQL-level pseudocode

The analyst will write the real SQL; the specification sheet carries the pseudocode so the analyst and the enablement lead agree on *what* the SQL is computing before the SQL exists. Pseudocode shape (fictional, drafting rollout):

```sql
-- Primary outcome: median elapsed business-minutes draft.started -> review.requested,
-- aggregated to operator-week, retained-client advisory matters only.

WITH tool_events AS (
    SELECT operator_id, matter_id, event_ts AS started_ts
    FROM drafting_tool.events
    WHERE event_type = 'draft.started'
      AND event_ts >= :observation_window_start
),
workflow_events AS (
    SELECT operator_id, matter_id, MIN(event_ts) AS reviewed_ts
    FROM mmws.events
    WHERE event_type = 'review.requested'
    GROUP BY operator_id, matter_id
),
joined AS (
    SELECT t.operator_id, t.matter_id,
           business_minutes_between(t.started_ts, w.reviewed_ts) AS elapsed_bmin
    FROM tool_events t
    JOIN workflow_events w USING (operator_id, matter_id)
    JOIN matters m ON m.matter_id = t.matter_id
    WHERE m.matter_type_code BETWEEN 'RC-01' AND 'RC-07'
),
winsorized AS (
    -- winsorize at 1st / 99th percentile within operator-week
    ...
)
SELECT operator_week, MEDIAN(elapsed_bmin) AS median_bmin
FROM winsorized
WHERE matters_in_operator_week >= 3
  AND operator_tool_matter_rank > 2  -- drop first two post-activation
GROUP BY operator_week;
```

The pseudocode is not production SQL; it is the shared mental model the analyst builds the real query against. The analyst will catch the edge cases (same-day drafting across time zones; multi-draft matters; operators who change roles mid-week); the pseudocode's job is to make sure both of you are building the same number.

### Checkpoint 5 — before Step 6

- [ ] Section 7 names a tier, a build-by date, and every dependency with an owner.
- [ ] Section 8 has pseudocode that a competent analyst could read and ask meaningful questions about.
- [ ] The pseudocode covers each of the six specification questions from Step 2 — if an inclusion filter lives in Section 2 but is missing from Section 8, the specification and the pseudocode will drift before the first build.

---

## Step 6 — Red-team against the four Chapter 01 theatre patterns and the two Chapter 06 role boundaries (10 min)

Read the full specification sheet aloud and check it against six failure modes. Anywhere the sheet fails a check, add a `<!-- fix: ... -->` note inline and fix before shipping to the analyst.

Four Chapter 01 patterns at the specification layer:

1. **The rollout-count scoreboard.** Does the specification measure the *workflow outcome*, or does it inadvertently measure "number of tool uses"? A specification that resolves to "count of sessions per operator-week" is this pattern in disguise. Outcomes measure work; counts measure activity.
2. **The cherry-picked rollout.** Does the inclusion filter in Section 2 narrow to the subset most likely to move? Scoping to retained-client advisory because new-matter drafting has a workflow-fit issue is defensible when the restriction is *named* ([mod-102 Chapter 02](../../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md)); silently narrowing to the subset with the strongest signal is the cherry-pick pattern. Say explicitly, in Section 2, which operators are *not* in scope and why.
3. **The moving goalpost.** Is the baseline the *pilot-charter* baseline, or a convenient replacement? If the baseline value in Section 4 differs from the pilot charter's baseline, Section 4 names the scorecard event (date, reason) that changed it. Chapter 01's discipline is: metric changes are published, not quiet.
4. **The vendor-number headline.** Is any number in Sections 4, 5, or 7 drawn from vendor telemetry or a vendor whitepaper? Vendor-reported productivity numbers do not sit in a specification; the specification is the organization's own measurement. Vendor telemetry may appear as a sanity-check line elsewhere in the dashboard, framed explicitly as vendor-reported.

Two Chapter 06 role boundaries at the specification layer:

5. **Did the analyst set the priority tier?** If so, you have inverted the interface. Section 7's tier is a program-decision the enablement lead owns; "the analyst had capacity so we built this first" is not a priority stack.
6. **Does the specification include narrative text (hits, risks, asks)?** If so, you are drafting the deep-dive inside the specification. Narrative lives in the deep-dive and is the enablement lead's output; the specification is a technical artifact. Cut the narrative.

Fix each `<!-- fix: ... -->` note before Step 7.

### Checkpoint 6 — before Step 7

- [ ] All six checks pass or carry a fix note.
- [ ] No field in the specification contains vendor-reported productivity numbers as the measured value.
- [ ] No field contains narrative sentences; the specification is technical throughout.

---

## Step 7 — Version the artifact and route to the analyst (5 min)

The specification is a versioned document. Chapter 06's versioning note: metric definitions change; when they do, the change is propagated with notice, not shipped silently.

Add a version footer to `metric-spec.md`:

```
Version: v0.1 — draft for ai-augmented-analyst review.
Next revision: after the analyst's build-walkthrough (expected within 2 weeks).
Changes between versions are logged below with date, author, and one-sentence reason.

## Change log

- v0.1 (YYYY-MM-DD) — <your-name> — initial specification.
```

Save the file. The deliverable is the specification sheet, not a write-up about it.

## Deliverables

- `metric-spec.md` — the analyst-ready metric specification sheet, with Sections 1 through 9 filled, pseudocode in Section 8, red-team fixes applied, versioned footer and change log.

## Checkpoint — self-evaluation

- [ ] A competent analyst who has never spoken to you could build the dashboard from Sections 2, 3, 7, and 8 alone.
- [ ] Section 6 (the three Chapter 02 annotations) is auditor-ready and can be lifted verbatim into the quarterly review's methodology appendix.
- [ ] The baseline in Section 4 carries a named provenance; "to be measured" does not appear anywhere in the sheet.
- [ ] The confidence band in Section 5 states what it covers *and* what it does not.
- [ ] The red-team pass caught at least one `<!-- fix: ... -->` the first time you read the sheet aloud; a spec that passes clean on first read was not red-teamed hard enough.
- [ ] The specification sheet contains no narrative sentences, no vendor-reported productivity numbers, and no field left as "TBD."

## What this lab prepares you for

Exercise 02's weekly rollup is a one-page document that *reads from* metrics specified at this depth; if the Section 1 outcome line in the rollup feels thin, this is the layer below that fills it. Exercise 03's quarterly review methodology appendix cites Section 6 of this sheet verbatim. Exercise 06's ROI narrative treats Section 5's confidence band as the outcome-side input to the ROI sensitivity analysis. The lab also exercises the Chapter 06 analyst interface: once this sheet exists, the standing weekly thirty-minute meeting with the analyst reads *this document*, not an ad-hoc request stack, which is the interface rhythm Chapter 06 names as the one that makes measurement defensible at steady state.
