# mod-106 — Outcome Measurement and Executive Reporting

**Estimated effort:** 18 hours
**Role level:** 45 · **Family:** AI Workforce

This is the module where the enablement program becomes legible to the organization that funds it. Before the budget defense (mod-107), before industry-specific flavouring (mod-108), before the incident path (mod-109), the role has to be able to *measure what the program has actually changed at org scope*, *assemble that measurement into a scorecard a board can act on*, and *defend the ROI narrative on methodology rather than on outcomes alone*. The rollout-level measurement from mod-102 Chapter 04 is the input; the aggregated scorecard, the quarterly board-ready review, the methodology appendix, the ROI narrative co-authored with Finance, and the running interfaces with the analyst and team manager are the operating output. Six chapters, six exercises.

## Learning objectives

- Choose adoption / productivity / ROI metrics that distinguish AI-induced gain from AI theatre at org scope — outcome metrics on the target workflow, workflow interviews as qualitative ground truth, usage telemetry only as sanity check — extending R4 (0.77) measurement depth from mod-102 into the org-wide scorecard.
- Author the executive scorecard — weekly rollup, monthly deep-dive, quarterly board-ready review — that frames AI progress, risks, investment asks, and metric misses; publish the targets that missed with the reason, not just the hits, grounded in R6 (0.58, 15/26 postings).
- Produce executive-ready communications — board updates, LT briefings, strategic memos — that a VP can sign and a board can act on; translate technical progress for executive leadership without theatre.
- Read the empirical literature on AI productivity gains (Peng arXiv:2302.06590, Ziegler ACM, Noy & Zhang Science 2023, Brynjolfsson/Li/Raymond NBER, Dell'Acqua et al.) as evidence for metric choice; defend the ROI narrative on methodology, not only outcomes.
- Partner with Finance on cost-model attribution — tool licenses, enablement program spend, FTE time — so the ROI numerator and denominator are both defensible.
- Coordinate with `ai-augmented-analyst` (level 20) on dashboard construction and with `ai-augmented-team-manager` (level 40) on team-level measurement which this role aggregates.

## Lecture chapters

1. [The Measurement Stack at Org Scope — Outcomes, Workflow Interviews, Usage Telemetry](01-the-measurement-stack-at-org-scope.md) — the three-layer frame from mod-102 Chapter 04 extended to a portfolio: confidence bands, defensible denominators, the role × BU × tool coverage matrix, four named theatre patterns at org scope (rollout-count scoreboard, cherry-picked rollout, moving goalpost, vendor-number headline), and the aggregate-within-category discipline.
2. [Authoring the Executive Scorecard — Weekly, Monthly, Quarterly](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) — three cadences, three audiences, three templates; the five-section weekly rollup, the seven-section monthly deep-dive, the eight-section quarterly board-ready review, the misses-first discipline, and the five-part miss narrative structure.
3. [Writing for Executives — Board Updates, LT Briefings, Strategic Memos](03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) — the three executive artifacts, the three structural moves (BLUF, misses-in-the-lead, confidence bands), the three named theatre failure modes in executive communication, the co-authoring rhythm with the sponsor, and the discipline of translation without theatre.
4. [Reading the Empirical AI Productivity Literature for Method, Not Numbers](04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) — Peng, Ziegler, Noy & Zhang, Brynjolfsson/Li/Raymond, Dell'Acqua; the five transferable methodology patterns and the five threats to validity the enablement lead carries.
5. [Partnering with Finance on the Cost Model and ROI](05-partnering-with-finance-on-cost-model-and-roi.md) — the ROI equation at this layer, three numerator components, four denominator components, three attribution frames (fraction, cohort comparison, staggered rollout), the confidence-band discipline at ROI altitude, the standing Finance partnership contract.
6. [Coordinating with the Analyst and the Team Manager](06-coordinating-with-the-analyst-and-the-team-manager.md) — the three-tier measurement stack, the specification-driven interface with the analyst, the portfolio-context-driven interface with the team manager, the handoff calendar, and the three data-governance surfaces at the measurement interface.

## Exercises

Carrying one chosen organization and one chosen portfolio across Exercises 01, 02, 03, 05, and 06 will produce a coherent measurement-and-reporting bundle worth keeping. Exercise 04 is a sharper, self-contained drill that can be done against any portfolio shape.

1. [Outcome vs. Usage Metric Framework](exercises/exercise-01-outcome-vs-usage-metric-framework.md) — the reusable framework template, a worked example on one rollout, and a defence paragraph against the Chapter 01 theatre patterns.
2. [The Weekly Executive Scorecard](exercises/exercise-02-the-weekly-executive-scorecard.md) — the one-page weekly rollup for a portfolio of four to six rollouts, in five fixed sections, with an authoring note.
3. [Quarterly Board-Ready Review Outline](exercises/exercise-03-quarterly-board-ready-review-outline.md) — the eight-section outline plus the fully-drafted one-page executive summary.
4. [Metric Miss Narrative Drill](exercises/exercise-04-metric-miss-narrative-drill.md) — three miss narratives (workflow-fit miss, measurement-issue miss, change-management-lag miss) each in the five-part Chapter 02 structure.
5. [AI Productivity Literature to Metric Choice Map](exercises/exercise-05-ai-productivity-literature-to-metric-choice-map.md) — the paper-to-scorecard mapping table, per-paper methodology notes, and the five-pattern inventory with commitments by quarter.
6. [ROI Numerator and Denominator Defence](exercises/exercise-06-roi-numerator-and-denominator-defence.md) — the Section 6 ROI narrative plus a simulated six-challenge Finance Q&A.

## Labs and quizzes

Lab and quiz prompts land in `labs/` and `quizzes/` on subsequent content cycles.

## Resources

External references: [`resources.md`](resources.md).

## How this module connects to the rest of the track

- Takes from [mod-101](../mod-101-role-and-the-org-wide-enablement-operating-model/README.md): the scope contract (Chapter 01) and handoff map (Chapter 04) define the audience for the scorecard and the roles the enablement lead coordinates with across measurement.
- Takes from [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md): the rollout-level outcome measurement from [mod-102 Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md) is the per-rollout input this module aggregates into the portfolio view; the pilot charter from [mod-102 Chapter 02](../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md) is the source of the pre-rollout baseline and the pilot-charter target that the moving-goalpost discipline protects.
- Takes from [mod-103](../mod-103-policy-co-authoring-with-governance/README.md): the data-handling policy stack bounds what can appear on the measurement dashboards and in the scorecard — the data-governance surface treated in [Chapter 06](06-coordinating-with-the-analyst-and-the-team-manager.md).
- Takes from [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md): training-program effects are a potential concurrent cause when AI-attribution is measured; the attribution discipline in [Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md) composes training effects with AI effects.
- Takes from [mod-105](../mod-105-champion-networks-and-change-management/README.md): the change-management health dashboard from [mod-105 Chapter 07](../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md) is the leading indicator that pairs with this module's trailing-indicator scorecard; the five resistance-pattern signals from [mod-105 Chapter 06](../mod-105-champion-networks-and-change-management/06-ai-specific-resistance-patterns-adkar-and-kotter.md) feed the qualitative-ground-truth section of the monthly deep-dive and the quarterly review.
- Feeds [mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md): the ROI methodology, the cost model, and the Finance-partnership contract at scorecard depth are inputs to the deeper budget and build-vs-buy work in mod-107; [Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md) is the scorecard-facing slice of what mod-107 treats at depth.
- Feeds [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md): a dashboard signal that crosses into harm territory routes into the incident-path; the data-governance surface at the measurement interface is an incident surface when it goes wrong.
- Feeds [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md): the three-cadence scorecard and the running Finance, analyst, and team-manager interfaces are among the recurring operating-model rituals at CoE steady state.
- Feeds [mod-112](../mod-112-career-positioning-and-the-next-step-on-the-ladder/README.md): the executive-communication craft from [Chapter 03](03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) and the methodology discipline from [Chapter 04](04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) are among the capabilities that distinguish the enablement lead at level 45 from the next-step-up roles.
