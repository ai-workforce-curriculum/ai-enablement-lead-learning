# Coordinating with the Analyst and the Team Manager

> The scorecard the enablement lead signs is not produced by the enablement lead alone. Two adjacent roles do most of the measurement work that the scorecard aggregates: `ai-augmented-analyst` (level 20) builds and maintains the dashboards, pipelines, and metric definitions the scorecard draws from; `ai-augmented-team-manager` (level 40) runs team-level outcome measurement in each business unit that the enablement lead rolls up into the portfolio view. Without clean interfaces to both, the scorecard becomes either a vanity artifact (if the enablement lead invents metrics the analyst can't produce or the team manager doesn't recognise) or an inconsistent one (if each BU measures differently and the aggregation is a category error). This chapter is the operating contract with each.

## The three-tier measurement stack

Measurement at this layer is explicitly a three-tier stack. Each tier produces work for the one above; each tier consumes definitions from the one above.

```
Enablement lead (L45) — portfolio rollup, executive scorecard, ROI narrative
        ^
        | aggregates team-level outcomes; consumes dashboards
        |
Team manager (L40) — team-level outcome measurement, rollout execution
        ^
        | consumes dashboards; feeds operator-level signal
        |
Analyst (L20) — dashboards, pipelines, metric definitions, data quality
```

The enablement lead does not produce dashboards; the team manager does not aggregate across BUs; the analyst does not set strategic metric priorities. Role confusion at any tier is the single most common cause of scorecard failure at this layer.

## The interface with `ai-augmented-analyst` (L20)

### What the analyst produces

The analyst produces four categories of output that the scorecard depends on:

- **Dashboards.** The live, queryable views of outcome metrics, usage telemetry, and change-management health per rollout. The dashboard is not the scorecard; it is the raw material the scorecard draws from. Dashboards are built once per metric family and maintained over time.
- **Metric definitions and SQL.** The analytical definition of each metric — what is counted, what is excluded, how joins work across source systems — plus the SQL or equivalent query logic. Metric definitions are versioned; changes are propagated with notice.
- **Data pipelines and quality monitoring.** The ETL (or ELT) from source systems — vendor APIs, workflow systems, HR system, ticketing — into the measurement warehouse. Data-quality monitoring runs against each pipeline so measurement failures are visible, not silent.
- **Ad-hoc analyses.** Investigations into outcome movements, cohort decomposition for the miss narrative, attribution analyses for the ROI numerator. The analyst's hours on ad-hoc work expand around the quarterly review.

### What the enablement lead supplies

The analyst needs four inputs from the enablement lead to produce credible measurement:

- **Metric specifications, not just metric names.** "Time to first draft" is a name. "Median elapsed time in minutes, from the draft-started event in the drafting tool to the first-review-requested event in the workflow system, computed per operator per week, filtered to retained-client advisory matter types, with outliers above the 99th percentile excluded" is a specification. The analyst builds against specifications; a metric name without a specification produces a dashboard that will not survive its first Finance challenge.
- **The cohort definition for each measurement.** Which operators are in scope. Which BUs. What time window. The cohort is often the first thing a dashboard gets wrong when the specification is thin.
- **Baseline provenance.** Where the pre-rollout baseline came from, whether the analyst needs to compute a historical baseline, and if so, over what period. Baselines without provenance are the vanity-number risk from [mod-102 Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md).
- **Priority stack and timelines.** What the analyst should work on this cycle, and against which deadlines. The enablement lead who gives the analyst nothing but a stack of requests without priorities will get work in an order that does not match the scorecard cadence.

### The standing interface — a working rhythm

A durable rhythm with the analyst:

- **Weekly, thirty minutes.** Review this week's dashboard refreshes, anomalies flagged by data-quality monitoring, and any ad-hoc requests queued for the next two weeks. The enablement lead treats this as an operating meeting, not a status meeting.
- **Monthly, sixty minutes, before the monthly deep-dive drafts.** Walk the metrics the deep-dive will carry, confirm the numbers, align on any methodology changes. The analyst catches the cases where a reported number is driven by a data-pipeline change rather than a program change; the enablement lead catches the cases where a metric is arithmetically correct but narratively misleading.
- **Quarterly, two to three hours, before the quarterly review drafts.** Full walk of the portfolio-level outcome rollups, the attribution analyses for ROI, the confidence bands. This is where the analyst's deepest work lands in the scorecard; book it long enough.

### What the enablement lead does not ask the analyst to do

Two things the enablement lead must not delegate downward to the analyst, because the analyst does not own them:

- **Setting metric priorities.** Which metrics make the scorecard is a program decision. The analyst builds what is specified; the enablement lead specifies.
- **Writing the narrative.** The scorecard narrative — hits, misses, risks, asks — is the enablement lead's output. The analyst provides the numbers and the texture; the lead writes the story. Analysts who are asked to write narratives produce reports that read as data-descriptive rather than decision-forcing; reports that will not shape investment.

Depth on the analyst role lives in [`ai-augmented-analyst-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-analyst-learning); at this chapter's altitude, carry the interface.

## The interface with `ai-augmented-team-manager` (L40)

### What the team manager produces

The team manager owns measurement *inside* the business unit, for the operators on their team. They produce three categories of output the enablement lead aggregates:

- **Team-level outcome measurement for each rollout the team operates.** The outcome metric specified by the enablement lead, measured against the team's pre-rollout baseline, reported on the cadence the enablement lead specifies. The team manager is where the measurement happens in the real workflow, not in the abstract.
- **Qualitative texture from the team.** The team manager sees the operator-level reality the aggregated interviews cannot see — who is silently abandoning the tool, which workflows the tool fits and which it doesn't, which operators are becoming informal experts. This texture is a running qualitative input to the portfolio rollup from [Chapter 01](01-the-measurement-stack-at-org-scope.md).
- **Change-management health at the team level.** Per [mod-105 Chapter 07](../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md), the team manager observes adoption curve, champion activity, communications reach, and resistance patterns at the team level. These team-level signals aggregate into the enablement lead's dashboard (not the executive scorecard).

### What the enablement lead supplies

The team manager needs four things from the enablement lead to produce credible team-level measurement:

- **The portfolio context.** What rollouts the team is operating, what the organization expects from each, what the team-level outcome targets are against the portfolio plan.
- **The metric specification, pre-translated.** The analyst's specification stated in terms the team manager can operate — not "median elapsed time between draft-started and first-review-requested events" but "the time, in business minutes, between an associate starting a draft and sending it for review, measured on retained-client advisory matters."
- **Dashboard access, with permission scope.** The team manager needs to see the team's own measurement in real time; the enablement lead works with the analyst and IT to make sure the dashboard has the correct permission scoping so team managers see their own BU, not the whole portfolio.
- **The feedback loop back to the team.** When the team's measurement moves the portfolio view — good or bad — the team manager hears about it quickly. A team manager who learns from the quarterly board readout that their team was the quarter's miss is a team manager who will disengage from the measurement loop.

### The standing interface — a working rhythm

A durable rhythm with team managers (plural; the enablement lead will have several):

- **Monthly, thirty to forty-five minutes per team manager, individually.** Review the team's outcomes against target, texture from the workflow, change-management health. The enablement lead carries forward issues that will land in the next deep-dive; the team manager carries back program-level decisions that affect the team.
- **Quarterly, a working group with all team managers together.** Two to three hours. Review the portfolio rollup before it goes to the board, hear each team manager's pattern findings, align on next quarter's targets. The group format is where cross-BU pattern finding happens; a shark-fin adoption curve in BU A that the team manager in BU B recognises as a pattern they are also seeing is a finding that will not surface in one-on-ones.

### What the enablement lead does not ask the team manager to do

Three things:

- **Aggregating across teams.** The team manager measures their own team. Cross-team aggregation is the enablement lead's job (with the analyst's infrastructure). A team manager who is cross-aggregating is drifting out of role scope.
- **Public miss narratives in the exec scorecard.** When a team's rollout misses, the miss narrative in the exec scorecard is the enablement lead's writing. The team manager is the source of the diagnosis; the lead is the author of the narrative. Team managers who are asked to write the exec-facing miss narrative are being asked to do executive communication without the skill or the sponsor relationship — a failure shape.
- **Direct interface with Finance on ROI.** The team manager contributes team-level cost and value inputs when asked, but the ROI narrative with Finance ([Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md)) is the enablement lead's interface. A team manager pulled into Finance conversations on ROI will produce inconsistencies across teams.

Depth on the team-manager role lives in [`ai-augmented-team-manager-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning); at this chapter's altitude, carry the interface.

## The handoff cadences, in one place

| Cadence | Who | Purpose |
|---|---|---|
| Weekly 30 min | Enablement lead + analyst | Dashboard anomalies, ad-hoc queue |
| Monthly 30-45 min each | Enablement lead + each team manager | Team outcomes vs. target, qualitative texture |
| Monthly 60 min | Enablement lead + analyst | Deep-dive draft numbers |
| Quarterly 2-3 hr | Enablement lead + analyst | Portfolio rollups, attribution, confidence bands |
| Quarterly 2-3 hr | Enablement lead + all team managers | Cross-team pattern finding, next-quarter targets |
| Quarterly 30-60 min | Enablement lead + Finance ([Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md)) | ROI narrative co-authoring |

The combined time is non-trivial. Protect it as calendar; the scorecard that lands without these meetings has had its methodology compressed into the enablement lead's assumptions, which is not what a defensible scorecard is.

## The data governance surface the enablement lead carries

Three data-governance concerns sit at the interface with the analyst and will land on the enablement lead if they go wrong.

### Personal data and operator identification

Measurement at the operator level is personal data in most jurisdictions. The enablement lead and the analyst operate under the organization's data-governance policies (which are often consequences of the [mod-103](../mod-103-policy-co-authoring-with-governance/README.md) policy stack), including:

- Data minimisation on dashboards exposed to non-HR audiences.
- Aggregation thresholds — team-level metrics do not appear below a cell size that would re-identify individuals.
- Retention policies on workflow-interview transcripts and resistance-survey responses.

A dashboard that violates these is not a scorecard input problem; it is a governance incident. See [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) for the incident path.

### Cross-BU access to measurement

Team managers see their own team; the enablement lead sees the portfolio; VPs see their BU; the board sees the portfolio. Setting up permission scoping correctly is a shared responsibility with IT and the analyst. The common failure is over-permissive dashboards — a VP who can see another VP's BU — which is a political event in most organizations.

### Vendor data and the measurement loop

Vendor-supplied telemetry (per-tool usage data from the AI tool's admin console) is a data source. The data-processing-agreement terms the organization signed with the vendor constrain what can be done with that data; the analyst and the enablement lead operate under those terms. A dashboard that mixes vendor telemetry with HR data in ways the DPA does not permit is a compliance exposure.

The enablement lead does not have to be the authority on these questions; they do have to know they exist and route them into the governance partnership from [mod-103](../mod-103-policy-co-authoring-with-governance/README.md).

## What this chapter does not try to cover

Intentionally out of scope at this altitude:

- **The craft of dashboard construction.** That lives in the analyst track. The enablement lead specifies what the dashboard should show; they do not build it.
- **The craft of team-level outcome measurement in each workflow.** That lives in the team-manager track. The enablement lead specifies the metric and the cadence; the team manager runs the measurement in the workflow.
- **The HR partnership on operator-level sentiment.** Operator-level sentiment is HR's work. The enablement lead reads aggregated resistance-survey outputs; they do not run operator sentiment themselves.

Carrying these distinctions is what keeps the enablement lead's role at level 45 rather than drifting into the level-20 or level-40 work below.

## Where this chapter feeds

- [Chapter 01](01-the-measurement-stack-at-org-scope.md) measurement stack specifies what each of the three tiers is producing.
- [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) cadences are produced by this chapter's interface rhythms.
- [Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md) adds the Finance interface alongside the analyst and team-manager interfaces here; the three interfaces together are the enablement lead's measurement operating model.
- Exercise 06 walks the ROI defence against the three interfaces together.

## Summary

- Measurement at this layer is a three-tier stack: analyst (L20) produces dashboards and pipelines; team manager (L40) measures team-level outcomes; enablement lead (L45) aggregates into portfolio rollup and scorecard.
- The analyst interface is specification-driven: the enablement lead supplies metric specifications, cohort definitions, baseline provenance, and priorities; the analyst produces dashboards, SQL, data-quality monitoring, and ad-hoc analyses. Do not ask the analyst to set priorities or write narratives.
- The team manager interface is portfolio-context-driven: the enablement lead supplies context, pre-translated metric specifications, dashboard access, and a feedback loop; the team manager produces team-level outcomes, qualitative texture, and change-management health signals. Do not ask the team manager to aggregate, to write exec-facing narratives, or to interface directly with Finance.
- A working calendar carries six recurring interfaces — weekly and monthly with the analyst, monthly and quarterly with each team manager, quarterly with the whole team-manager group, quarterly with Finance. Protect the time; a scorecard without these interfaces has had its methodology compressed into assumptions.
- Three data governance surfaces — personal data, cross-BU access, vendor data terms — sit at this interface and route into [mod-103](../mod-103-policy-co-authoring-with-governance/README.md) and [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) when they go wrong.
- The enablement lead specifies metrics but does not build dashboards; specifies cadences but does not run team-level measurement; reads aggregated texture but does not run operator-level sentiment. Role-boundary discipline is what keeps the scorecard honest and the role at level 45.
