# The Measurement Stack at Org Scope — Outcomes, Workflow Interviews, Usage Telemetry

> [mod-102 Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md) taught the three-layer measurement frame — outcome metrics on the target task, workflow interviews as qualitative ground truth, usage telemetry as sanity check — for a single rollout. This chapter extends that frame into an *org-wide portfolio*: what you measure across every rollout the enablement program owns, how you aggregate without washing the signal out, and the AI-theatre patterns that get louder as the portfolio gets bigger.

## Why the per-rollout frame needs extension at org scope

Measuring one rollout well is a Chapter 04 problem. Measuring twenty rollouts, across six business units, with three different vendor tools in one task category and two internal builds in another, is a different problem. The Chapter 04 discipline does not change — outcomes first, interviews second, telemetry third — but three things get harder:

- **Aggregation pressure.** A board that will read one line about "AI" wants one number. If you hand them an unweighted average across twenty rollouts, the laggards disappear into the mean and the leaders carry the story; if you hand them the sum, a widely-deployed low-impact tool dominates. Aggregation is a methodology question, not a slide-deck question.
- **Portfolio-level theatre.** At one rollout, metric theatre looks like adoption-up / outcome-missing. At twenty, it looks like *rollout-count-up* — a chart counting how many tools are in production as if that were the outcome. The failure mode gets a new shape at scale.
- **Cross-rollout comparability.** Outcome metrics are task-specific by design. Comparing "time to first client-ready draft" in legal to "first-contact resolution rate" in support is a category error. You either stop reporting them together, or you define a comparability frame on purpose.

These three pressures shape the rest of the chapter.

## The three measurement layers, at org scope

The priority order is unchanged from [mod-102 Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md):

1. **Outcome metrics on the target workflow.** For every rollout in the portfolio, one named outcome metric, baselined pre-rollout on comparable work, reported post-rollout against that baseline.
2. **Workflow interviews.** A quarterly interview cadence across role × business unit × tool cells, structured and transcribed, read for patterns the aggregated numbers cannot see.
3. **Usage telemetry.** Seat, login, active-use, prompt-volume data. Sanity check only. Never an outcome, never a leading metric on the exec scorecard.

Three things change when the frame scales.

### What changes in Layer 1 — outcome metrics

At the portfolio level, outcome metrics acquire two attributes they did not carry at rollout level:

- **A confidence band.** A single rollout can report a point estimate against the pre-rollout baseline because the comparison is tight. A portfolio metric that averages across rollouts has sampling and attribution variance; report it with a band, not a point. "Median time-to-first-draft across drafting rollouts fell 22% (90% CI: 14%–29%)" is honest; "drafting workflows are 22% faster" is not. The literature in [Chapter 04](04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) is where you learn to construct the band.
- **A denominator you can defend.** "Time saved per week per operator × operators using it × weeks measured" is a credible aggregation; "time saved × total licensed seats" is not — unused seats do not save time. The denominator is the first thing a skeptical CFO or auditor will attack.

Outcome metrics at the portfolio level fall into three families. Keep them separated on the scorecard:

- **Productivity outcomes.** Time per task, throughput per operator, cycle time reductions. Measured against pre-rollout baselines on comparable work.
- **Quality outcomes.** Defect rate, rework rate, acceptance-on-first-pass rate, error rate caught downstream. Easier to measure; harder to attribute. Hold them and productivity side by side because the common failure is faster-but-worse.
- **Business outcomes.** Revenue influenced, cost avoided, customer-satisfaction delta, retention delta. The hardest to attribute to AI specifically; demand the most methodology discipline. Not every rollout has one; the ones that do are the ones the board most wants to hear about.

### What changes in Layer 2 — workflow interviews

At the rollout level, you interview the roles that use the tool. At the portfolio level, you need a *coverage matrix* so no family-of-rollouts goes a quarter without a qualitative read:

```
                  | Business Unit A | Business Unit B | Business Unit C |
------------------+-----------------+-----------------+-----------------+
Drafting tools    | monthly         | quarterly       | quarterly       |
Meeting-notes     | quarterly       | monthly         | —               |
Support copilot   | —               | —               | monthly         |
Search / RAG      | quarterly       | quarterly       | quarterly       |
```

The matrix is read as: for each live rollout family in each BU, what cadence of interview is active. Blank cells are known gaps. A rollout live for 90 days without a cell on the matrix is a flagged risk, not a quiet success.

The interview itself is the same four questions from mod-102 Chapter 04:

- What did you use the tool for this week?
- What did it replace?
- What did it add that wasn't there before?
- Where did it misbehave or where did you stop trusting it?

The point of carrying the same four questions at org scope is longitudinal comparability. Quarterly aggregates of question 4 responses, read in sequence, show the shape of a workflow's trust curve — which is a signal the dashboard cannot generate.

### What changes in Layer 3 — usage telemetry

Usage telemetry at org scope has two legitimate uses and a lot of illegitimate ones.

Legitimate:

- **Floor check.** DAU and active-use curves tell you whether a rollout is alive. Collapsing DAU in month six is a signal — go find out what.
- **Dark-matter detection.** Business units with licenses and near-zero usage are workflow-interview targets, not scorecard content.

Illegitimate:

- Adoption percentage as an org-level KPI. "68% of the company has used an AI tool this quarter" is a sentence that does not answer any executive question worth asking. Operators logging in without changing a workflow is noise.
- Prompt volume as a productivity proxy. Prompt volume is correlated with *using the tool*, not with *producing better outcomes*; a tool that needs twenty prompts per task is often a tool with a workflow-fit problem.
- Vendor-reported productivity numbers imported into your scorecard. Vendor dashboards report telemetry against vendor-chosen denominators. They are vendor marketing with an admin panel; the methodology is not auditable, and borrowed vendor numbers are indefensible in front of a CFO who has seen the pattern before.

If a stakeholder keeps asking for a usage headline, that stakeholder is confusing attention with impact. The remediation is editorial — rebuild the scorecard with outcome in the lead; the usage number lives three sections down as a sanity check with explicit framing. See [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) for the template.

## Distinguishing AI-induced gain from AI theatre at org scope

Four theatre patterns show up at portfolio scale. Each has a specific tell and a specific remediation. Name them out loud; the names are the vocabulary the role needs in a steering meeting.

### Pattern 1 — the rollout-count scoreboard

**Tell.** The headline on the AI slide is the number of tools in production or the number of business units with an AI rollout. The number goes up every quarter because rollouts accumulate; it would also go up in a program producing no business value at all.

**Why it survives.** Count is easy to produce, hard to argue against, and feels like progress. It is the portfolio-scale equivalent of "95% of licensed users logged in" from mod-102 Chapter 04.

**Remediation.** The headline is an outcome metric aggregated across the portfolio with a confidence band. The rollout count moves to the operational appendix if it moves anywhere.

### Pattern 2 — the cherry-picked rollout

**Tell.** The exec readout features the same one or two rollouts every month — the ones with the strongest numbers. The portfolio contains fifteen others that have not appeared in an exec surface for three quarters.

**Why it survives.** Rolling up fifteen rollouts is work; promoting one is easy. The two cherry-picked rollouts are usually genuine wins, which makes the editorial dishonesty hard to see.

**Remediation.** The scorecard has a fixed roster of rollouts that appear every cycle, chosen by business-impact weight not by metric strength. A rollout on the scorecard that is missing its outcome for two cycles running triggers an investigation, not a quiet removal.

### Pattern 3 — the moving goalpost

**Tell.** The target metric for a rollout changed mid-flight. "We are measuring time per draft" became "we are measuring satisfaction" when time per draft did not move. The new metric was not the pilot charter's metric.

**Why it survives.** Nobody remembers the pilot charter after the rollout ships. The owner is under pressure to show progress; satisfaction is easier to move than time-per-draft.

**Remediation.** The scorecard carries the *original* pilot-charter outcome metric for the life of the rollout. A metric change is a scorecard event with a line: *target metric changed from X to Y at date D, reason R*. Published, not quiet.

### Pattern 4 — the vendor-number headline

**Tell.** An exec readout opens with a number from a vendor whitepaper — "55% faster coding," "40% time saved on summarization" — presented as if it were *the organization's* measurement.

**Why it survives.** The vendor number is big, concrete, and already written. The organization's own measurement produces a smaller number, later, with more caveats. The borrowed number wins the slide.

**Remediation.** The scorecard reports only measurements taken on the organization's cohort, tasks, and baselines. Vendor numbers may appear as context in a methodology appendix, framed explicitly as "vendor-reported, not our measurement."

## Aggregating without washing the signal out

Two aggregation disciplines keep the portfolio metric honest.

### Discipline 1 — aggregate within category, not across

Time per task across drafting rollouts aggregates cleanly. Time per task across drafting *and* support-ticket resolution does not. The categories were different workflows; the common statistic is a category error.

Report four to six category rollups rather than one grand total:

- Drafting workflows.
- Summarization and meeting-notes workflows.
- Retrieval and internal-search workflows.
- Support-ticket resolution workflows.
- Code-review and software-engineering workflows.
- Analyst and research workflows.

The grand total, if one appears, is a weighted composite with the weights published alongside it. The weighting is a methodology choice the Finance partner from [Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md) will have an opinion about; do not do it alone.

### Discipline 2 — publish the denominator with the ratio

Every portfolio-level outcome ratio appears with its denominator stated. "22% faster across drafting workflows (n=842 operators, 14 weeks post-rollout)" is defensible; "22% faster across drafting" is not. The denominator is the first thing an auditor, a CFO, or a board member who has seen this pattern before will ask for; publishing it preempts the challenge and builds credibility over cycles.

## What belongs on the dashboard versus the scorecard

Two surfaces are easy to confuse.

- The [mod-105 Chapter 07](../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md) **change-management health dashboard** is a *leading indicator*. It measures the health of the change effort — adoption curve shape, champion retention, communications reach, resistance survey. It belongs to the enablement function and informs internal operating decisions.
- The **executive scorecard** from [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) is a *trailing indicator*. It measures business outcomes — productivity, quality, business impact — that result from a healthy change effort. It belongs to the exec sponsor and shapes investment decisions.

A healthy change dashboard with a flat scorecard is a timing problem, not a program problem — the behaviour change has not yet produced the outcome. A deteriorating dashboard with a bright scorecard is the silent-compliance risk from [mod-105 Chapter 06](../mod-105-champion-networks-and-change-management/06-ai-specific-resistance-patterns-adkar-and-kotter.md); the scorecard is about to turn. Reading them together is the enablement lead's practice.

## The qualitative ground-truth discipline

The single most useful hour on the enablement lead's week is the one spent *reading transcribed workflow interviews*, not reading dashboards. The dashboard tells you what moved; the transcript tells you what is actually happening at the operator level — the shadow spreadsheet, the dropped tool, the quiet workaround, the trust collapse.

Three rules for keeping the qualitative layer honest:

- **The enablement lead reads the transcripts personally.** This is not delegable to the analyst. An aggregated interview summary loses the texture that makes the qualitative layer diagnostic.
- **Anonymize at ingest.** Operators will not speak to specifics if their names are on the transcript at review time. Anonymization also is the floor the HR partner will require.
- **Quote in the scorecard, carefully.** An anonymized operator quote that cuts against the aggregate number is more credible than ten quotes that confirm it. Use quotes to show the role is reading its own transcripts, not to decorate the deck.

## Where this chapter feeds

- [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) uses this measurement stack as the *inputs* to the executive scorecard across all three cadences.
- [Chapter 03](03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) treats how the measurements become an executive-ready narrative.
- [Chapter 04](04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) grounds Layer 1 outcome construction in the published method.
- [Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md) composes Layer 1 outcomes with cost attribution into ROI.
- [Chapter 06](06-coordinating-with-the-analyst-and-the-team-manager.md) specifies who produces each layer — team manager, analyst, enablement lead.

## Summary

- Extend the Chapter 04 three-layer frame to a portfolio: outcome metrics per rollout with confidence bands and defensible denominators, workflow interviews on a role × BU × tool coverage matrix, usage telemetry restricted to floor-check and dark-matter detection.
- Four named org-scale theatre patterns — rollout-count scoreboard, cherry-picked rollout, moving goalpost, vendor-number headline — each with a specific tell and remediation. Name them out loud; the vocabulary is the defence.
- Aggregate within category, not across; publish the denominator with every ratio.
- The dashboard is leading; the scorecard is trailing. Reading them together is the practice.
- The enablement lead reads transcribed workflow interviews personally; the qualitative layer is not delegable without losing diagnostic texture.
