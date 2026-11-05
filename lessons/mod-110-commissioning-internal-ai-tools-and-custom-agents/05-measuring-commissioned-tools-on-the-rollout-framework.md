# Measuring Commissioned Tools on the Rollout Framework

> The commissioned ticket-triage copilot has been in production for a quarter. The engineering team's eval harness is green — step correctness is 92%, model-level quality has not drifted. The mod-106 scorecard is red — first-contact resolution has moved sideways and workflow interviews report the same frustrations operators had before the tool. The engineer and the commissioner are both right about their respective numbers; the organisation's question is which number the governance council should believe. This chapter is the measurement discipline that keeps both numbers on the right surface and refuses to let an internal build hide behind its own scorecard.

## The frame is reused, not re-invented

Commissioned tools are measured on the same framework as every other rollout in the portfolio. The three-layer measurement stack from [mod-102 Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md) and [mod-106 Chapter 01](../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md) is the whole story:

1. **Outcome metrics on the target workflow.** The business-outcome shift the tool is supposed to produce — first-contact resolution, documentation-quality score, time-to-triage, policy-compliance rate — measured against the pre-rollout baseline, with confidence bands.
2. **Workflow interviews as qualitative ground truth.** Structured conversations with operators in the user cohort at a known cadence; the pattern-recognition surface that catches what the outcome metrics miss.
3. **Usage telemetry as sanity check.** Adoption, session frequency, prompt distribution — the floor below which the outcome metric cannot be interpreted. Not a success criterion, a floor.

The chapter's title — *measuring commissioned tools on the rollout framework* — is a deliberate refusal to treat internal builds as a different measurement category. The scorecard is the scorecard. A commissioned tool that moves a metric earns its budget; a commissioned tool that does not move its metric is retired or rebuilt, same as a vendor tool.

## The two temptations that collapse into an internal-build scorecard

Two patterns show up repeatedly on commissioned tools and together form the failure mode this chapter is named against: **the internal-build scorecard**. Each is seductive because it makes the commissioned tool look healthier than the portfolio scorecard says it is.

### Temptation 1 — Substituting the eval harness for the outcome metric

The engineer runs an eval harness as part of the build. The harness measures model-level quality against a curated test set: answer correctness, step correctness, response faithfulness to the retrieved context, latency, cost per query. The harness produces a number that is green.

The commissioner, under scorecard pressure, reports the eval-harness number to the governance council as the success measure. "The tool is at 92% step correctness on the eval harness" sits on the scorecard where "first-contact resolution shifted from 68% to 72% with a 95% confidence band of ±2%" used to sit.

**Why it is wrong.** The eval harness measures whether the tool does the thing the engineer scoped it to do. The outcome metric measures whether the thing the tool does moves the business outcome the commission was for. The two are not the same number. A tool can be eval-harness-perfect and outcome-neutral if the engineer scoped the wrong thing; a tool can be eval-harness-mediocre and outcome-positive if operators work around the model's weak spots in ways that still produce value. Substituting the harness for the outcome is the mod-102 Chapter 04 pattern of usage-as-success in a more sophisticated disguise.

**The discipline.** The eval harness is the **engineer's** measurement surface. The outcome metric is the **commissioner's** measurement surface. Both exist, both are reported, neither substitutes for the other. The scorecard slot for the commissioned tool reports the outcome metric; the eval-harness number appears as a supporting indicator in the monthly deep-dive, not as the headline.

### Temptation 2 — Building a bespoke dashboard for the internal tool

The commissioned tool is "different" from the vendor tools in the portfolio — it was built specifically for this cohort, it has access to telemetry a vendor tool would not expose, and the engineer is willing to instrument it in whatever way the commissioner wants. The commissioner, under the honest pressure of a scorecard whose outcome metric is noisy, builds a bespoke dashboard with ten custom metrics that tell a story about the tool.

Six months later the portfolio view has grown an extra scorecard panel, the governance council reads two sets of numbers for this one tool, and nobody can compare the commissioned tool's performance to the three vendor tools on the same workflow because the panels are different shapes.

**Why it is wrong.** The portfolio scorecard's value is comparability. A commissioned tool that reports on a bespoke dashboard is a commissioned tool that has quietly exited the portfolio view, and once it exits, the mod-107 tool-stack reconciliation ([Chapter 05 of mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/05-reconciling-the-tool-stack-across-bus.md)) cannot see it — "we have four ways to do ticket triage" becomes invisible because one of the four is reported on a different surface.

**The discipline.** The commissioned tool reports on the same scorecard surface as the rest of the portfolio. The engineer's observability surface exists in parallel, for the engineer's maintenance operations, not as the governance-facing read. If the portfolio scorecard needs a new metric to handle a commissioned-tool pattern, the metric is added to the whole scorecard and every tool is measured on it; the alternative is private metrics that nobody can benchmark.

## The two measurement surfaces and who owns each

The commissioned tool has two measurement surfaces. They live in different places, run on different cadences, and have different owners. Keeping them separate is what makes the measurement plan legible.

### Surface A — The eval harness (engineer-owned)

**What it measures.** Model-level quality: answer correctness against a labelled test set, step correctness for multi-step agents, faithfulness to retrieved context, refusal behaviour, guardrail-trigger accuracy, latency, cost per query, drift relative to a baseline eval run.

**Who owns it.** The `applied-ai-engineer` or `agentic-ai-engineer` who built the tool, maintained by the maintenance owner from [Chapter 02](02-the-commissioning-brief-as-the-load-bearing-artifact.md) Section 7.

**Who reads it.** The engineering team reads continuously (every model-version bump, every prompt change, every deployment). The commissioner reads at monthly cadence (does the eval surface look stable? is the maintenance owner's eval investment keeping pace with model-provider changes?). The `ai-risk-engineer` reads at red-team cadence (does the eval harness exercise the guardrails the red-team ask was dated against?).

**When it fires.** Continuously, as a CI-adjacent surface the engineer runs on every build.

**What the commissioner looks for.** Not the number — the trend. An eval harness that has drifted from 92% to 84% over a quarter is a tool whose maintenance is falling behind; the Chapter 02 Section 7 commitment is under-resourced and a conversation with the maintenance owner's manager is due.

### Surface B — The portfolio scorecard outcome metric (commissioner-owned)

**What it measures.** The business-outcome shift from the commissioning brief's Section 3. Named in the [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) vocabulary — outcome metric with baseline and target, workflow metric as leading indicator, usage as sanity-check floor.

**Who owns it.** The enablement lead, in partnership with the `ai-augmented-analyst` ([mod-106 Chapter 06](../mod-106-outcome-measurement-and-executive-reporting/06-coordinating-with-the-analyst-and-the-team-manager.md)) and the `ai-augmented-team-manager` who runs the team-level measurement.

**Who reads it.** The portfolio view is read weekly by the exec sponsor, monthly in the deep-dive, quarterly at the board-ready review. The maintenance owner reads to understand whether the tool's model-level numbers are translating into business impact.

**When it fires.** On the measurement cadence [mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) runs — weekly rollup, monthly deep-dive, quarterly board-ready.

**What the commissioner looks for.** The outcome shift against the Section 3 baseline and target, with confidence bands. A commissioned tool whose outcome has not moved after three months of post-pilot steady-state is a graduate-or-retire conversation; after six months it is a retirement conversation unless a named structural cause (concurrent process change, organisational re-org, data-input disruption) can be surfaced to the governance council.

## The eval-harness-to-outcome-metric gap and what it tells the commissioner

A specific pair of readings on the two surfaces is diagnostic. The table below names the four quadrants and the commissioner's move on each.

| Eval harness | Outcome metric | Diagnosis | Move |
|---|---|---|---|
| Green | Green | The commission is working. | Report in the misses-first scorecard discipline anyway — commissions whose outcome is green deserve the same auditable methodology as commissions whose outcome is red. |
| Green | Red | **Eval-harness success, business-outcome failure.** The tool does what the engineer scoped it to do; what the engineer scoped it to do is not moving the business outcome. | Workflow-interview round under [mod-106 Chapter 01](../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md)'s qualitative-ground-truth surface. The Section 1 or Section 3 of the brief is almost certainly wrong. Return to [Chapter 02](02-the-commissioning-brief-as-the-load-bearing-artifact.md) for a brief revision, not an engineering escalation. |
| Red | Green | **Eval harness regression against a still-green outcome.** The tool's model-level quality is falling but operators have adapted. Fragile posture: a further eval-harness drop may collapse the outcome. | Engineering escalation under the Chapter 02 Section 7 maintenance commitment. The maintenance owner's cadence is under-resourced; conversation with the engineering manager. |
| Red | Red | **Both surfaces regressing in parallel.** The tool is decaying. | Incident-path adjacency if the regression is sharp (see [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) for the outcome-regression signal source). Otherwise the graduate-or-retire conversation is immediate rather than deferred. |

The four-quadrant read is the commissioner's single most useful instrument. Reporting only one surface — the one that is greener today — is the Chapter 01 apologist posture arriving on the scorecard.

## The three cadences the measurement plan runs on

The measurement plan is not a document; it is a running cadence attached to the three scorecard cadences from [mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md). The commissioner authors the plan at commission time (as part of the brief's Section 8 binding) and runs it from pilot through steady-state.

### Weekly cadence

- The commissioned tool's outcome metric and workflow metric appear on the weekly rollup, same shape as every other rollout. Baseline, current reading, direction, confidence band.
- The eval-harness number appears **below the fold** as a supporting indicator, not as the headline. Engineering-side alerts (eval-harness drops, cost-per-query spikes, latency regressions) are the engineer's surface, surfaced to the commissioner weekly as a status line, not escalated into the scorecard unless they are crossing into the incident path.

### Monthly cadence

- The commissioned tool gets the same monthly deep-dive slot as every other rollout, with the [mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) seven-section structure.
- The eval-harness trend over the month appears as an addendum — a one-paragraph read of whether the model-level quality is stable, drifting, or improving, with the maintenance-owner's commentary.
- The four-quadrant read from the table above is run at monthly cadence; the commissioner's move is named in the deep-dive's misses section when a miss is in play.

### Quarterly cadence

- The commissioned tool's quarterly slot is read against the brief's Section 3 target, not against the previous quarter. The target is fixed at commission; moving the target to meet the current reading is the moving-goalpost pattern from [mod-106 Chapter 01](../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md) applied to internal builds.
- The quarterly read is the surface the graduate-or-retire conversation happens on. A commissioned tool that has missed its target for three consecutive quarters is a retirement candidate; the commissioner either (a) defends a specific named structural cause with evidence, (b) rebuilds the brief under [Chapter 03](03-inheriting-prototypes-and-the-honest-no-go.md)'s rebuild-from-brief recommendation, or (c) retires the tool and writes the retrospective.

## The red-team evidence surface at measurement time

Red-team evidence is not a one-shot artefact. The red-team ask authored in [Chapter 02](02-the-commissioning-brief-as-the-load-bearing-artifact.md)'s guardrails section lands evidence before pilot-to-rollout, but the measurement plan also carries a **re-run cadence**: at every model-provider major version change, at every data-source change the knowledge gateway exposes, and at every step-boundary change in an agentic tool, the red-team re-runs against the specific guardrails the change touches. The commissioner coordinates the re-run as part of the quarterly cadence; the `ai-risk-engineer` runs it.

A commissioned tool whose red-team evidence is more than two model-provider releases stale is a tool whose guardrails cannot be asserted to still hold. The commissioner either triggers a re-run or puts the tool on a pause until re-run evidence lands; a quietly-stale guardrail is a mod-109 incident waiting to happen.

## The retirement conversation

The honest no-go of [Chapter 03](03-inheriting-prototypes-and-the-honest-no-go.md) has a post-launch twin: the honest retirement. A commissioned tool whose quarterly reading has missed its target twice and whose four-quadrant diagnosis is persistent-red is on the retirement path. The retirement memo looks like the Chapter 03 no-go memo with one structural difference:

- Section 1 names what the tool did produce — the operators who used it, the specific outcomes that did shift even if the aggregate did not, the organisational learning the commission generated.
- Section 2 names the measurement evidence that triggered the retirement, with the quarterly readings in table form, the confidence bands, and the specific target the tool missed against.
- Section 3 names whether a rebuild from brief is being commissioned in the same space, or whether the problem has been re-routed to a different column of the [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) matrix (a commercial tool has emerged, a policy change has removed the problem, a process redesign has made the tool unnecessary).
- Section 4 names what happens to the commissioned stack — the eval harness, the retrieval index, the control-plane configuration — and whether any of it is reusable by the next commission in the space.
- Section 5 names the close-the-loop artefacts the retirement feeds back into [mod-103](../mod-103-policy-co-authoring-with-governance/README.md), [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md), and [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md).

Retirement memos are published in the same repository as the brief. A commissioning program that only publishes successes is a commissioning program whose scorecard is theatre.

## Summary

- Commissioned tools are measured on the same framework as vendor tools. The scorecard is the scorecard; no bespoke internal-build dashboard, no eval-harness-as-success substitution.
- Two temptations collapse into the internal-build scorecard: **substituting the eval harness for the outcome metric** and **building a bespoke dashboard**. The chapter's title is a refusal of both.
- Two measurement surfaces, two owners: the **eval harness** (engineer-owned, model-level quality) and the **portfolio scorecard outcome metric** (commissioner-owned, business outcome). Neither substitutes for the other; both appear in reporting, with the outcome as the headline.
- The four-quadrant read (eval × outcome, each green or red) is the commissioner's diagnostic instrument. Each quadrant has a specific move.
- Three cadences — weekly, monthly, quarterly — mirror the [mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) scorecard. Quarterly is the graduate-or-retire surface; the target from Section 3 of the brief is fixed, not slidable.
- Red-team evidence has a re-run cadence attached to model-provider changes, data-source changes, and step-boundary changes. Stale guardrails are an incident waiting to happen.
- Retirement is the measurement-side twin of Chapter 03's no-go. A commissioning program that only publishes successes is not auditable.
