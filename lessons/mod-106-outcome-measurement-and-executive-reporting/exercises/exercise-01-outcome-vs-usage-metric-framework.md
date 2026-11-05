# Exercise 01 — Outcome vs. Usage Metric Framework

**Estimated effort:** 2 hours
**Format:** written framework document plus a worked example, Markdown
**Grounding chapters:** [01 — The Measurement Stack at Org Scope](../01-the-measurement-stack-at-org-scope.md), [04 — Reading the Empirical AI Productivity Literature for Method, Not Numbers](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md)

## Objective

Build the one-document framework you will carry into every rollout to decide, in advance, how it will be measured — one outcome metric with its baseline and confidence framing, one workflow-interview coverage commitment, one explicit telemetry-as-sanity-check line. The framework is the thing you point at when someone asks why the scorecard does not open with adoption percentage. Then apply the framework to one worked rollout so a reader can see it operating, not just described.

## Prerequisites

- [Chapter 01](../01-the-measurement-stack-at-org-scope.md) read, with the three layers and the four named theatre patterns (rollout-count scoreboard, cherry-picked rollout, moving goalpost, vendor-number headline) close enough to name without the chapter in hand.
- [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) read, with the five methodology patterns (pre-registered outcome, two-dimensional outcome, longitudinal observation, decomposition by sub-population, field over lab) available for citation.
- One specific organization and one specific rollout picked — real or realistic. The rollout should have a clearly identifiable target workflow (drafting, summarization, support-ticket resolution, code review, retrieval, meeting notes, or analyst research).

## Problem statement

You are the AI Enablement Lead and your CoE runs a portfolio of AI rollouts. Each rollout today is being measured inconsistently — some with outcome metrics, most with usage percentages, a few with vendor-reported numbers. Your sponsor has asked for a "measurement framework" every rollout owner can apply. The deliverable is the framework itself (a reusable one-document template) *and* a worked example on one rollout that shows the framework operating.

The framework you produce will later feed the executive scorecard (Exercise 02), the quarterly board-ready review (Exercise 03), and the ROI defence (Exercise 06). Carry the same organization and ideally the same rollout through those exercises for a coherent bundle.

## Requirements

### Part A — the framework template

Produce a one-page reusable framework document that every future rollout owner will fill in before launch. It must contain, in this order:

1. **Target workflow.** The specific workflow the rollout is intended to change, stated in one or two sentences — not the tool name, not the function name. "Legal associates drafting first-pass client advisories on cross-border matters" is a workflow; "Legal AI rollout" is not.
2. **Outcome metric specification.** One primary outcome metric with: name, specification (what is measured, on which cohort, at what cadence, with what denominator), unit, pre-rollout baseline value and provenance, target value with target date, confidence-band construction method. Optionally one secondary outcome on the *other* dimension (if the primary is productivity, the secondary is quality or vice versa — per the Noy & Zhang two-dimensional discipline from Chapter 04).
3. **Workflow-interview commitment.** Cadence (monthly / quarterly), coverage (which roles × BUs in the role × BU × tool coverage matrix from Chapter 01), the four questions carried from mod-102 Chapter 04, and the owner of the interview cadence.
4. **Telemetry sanity-check.** One line stating what telemetry is being collected, framed explicitly as sanity check only. The framework must call out — in the template itself, not just in guidance — that telemetry does not appear on executive surfaces as the headline.
5. **Theatre watchlist.** Each of the four named Chapter 01 theatre patterns listed with a one-line note on how *this specific rollout* is at risk of each, and what the rollout owner will do to avoid it.
6. **Review schedule.** When the framework will be revisited — baseline re-check, interim review, retire-or-renew decision — with named owner and dates.

The template is a *template*, not the filled-in form. Keep it blank in the appropriate sections so a future rollout owner can fill it in for their rollout. The structure, the field names, and the guidance notes are what make it operational.

### Part B — a worked example on one rollout

Apply the framework to the rollout you picked. Fill in every section with realistic (but not necessarily sourced-from-production) content. The worked example must be long enough to show that each section lands with specific content — not "TBD," not "to be measured" — but short enough that it fits on three pages including the framework.

### Part C — a one-paragraph defence

Three to five sentences at the end of the worked example, addressed to the rollout owner, naming the single most important reason the usage-only alternative would have failed for this rollout. Cite one of the four Chapter 01 theatre patterns by name and explain, in one sentence, why *this specific rollout* was vulnerable to it.

## Starter guidance

- The hardest field is the outcome metric specification. Spec, don't name. "Time saved" is not a specification; "median elapsed business-minutes, from X event to Y event, measured on operator-week, filtered to work-shape Z, with provenance P" is. If your spec is under a hundred words, you have not yet pinned it down.
- The pre-rollout baseline is non-negotiable. If the baseline does not exist, the framework says so explicitly and requires a baseline-measurement activity before the rollout launches. "We will measure the baseline after launch" is not a framework entry; it is a Chapter 01 moving-goalpost in disguise.
- The workflow-interview coverage commitment is not optional. A framework without a qualitative layer is a framework that has not read the chapter. Even a quarterly 3-interview cadence counts; zero does not.
- Confidence-band construction — see Chapter 04 Pattern 1 — can be a bootstrap over operator-level deltas, a simple parametric interval, or an organizational standard; pick one and state it. The methodology matters less than making the choice explicit.
- For the theatre watchlist, pick the Chapter 01 pattern most likely to appear for *this specific rollout* given its scope, visibility, and vendor relationships. Honest diagnosis of your own program's vulnerabilities is the signal that this exercise landed.
- Avoid inventing specific published statistics (Peng 55%, Noy 37%, Brynjolfsson 14%) into the target. The Chapter 01 vendor-number-headline pattern is exactly this failure. Targets are set on the organization's own cohort, drawing on published *methodology*.

## Deliverables

- `outcome-metric-framework.md` containing:
  - Part A — the framework template (reusable, blank in the content fields).
  - Part B — the worked example on your chosen rollout.
  - Part C — the one-paragraph defence.
- A short reading list at the end: which Chapter 04 papers (one or more) informed your choice of methodology, and in one sentence per paper, how.

## Acceptance criteria

- The framework template has all six sections in the order specified, with each section labeled and with inline guidance a future rollout owner can use.
- The outcome metric specification in the worked example is a specification, not a name. A reader who has never seen the rollout can reconstruct what would be measured from the specification alone.
- The pre-rollout baseline in the worked example has a stated provenance (where the baseline came from, or how it will be produced before launch). "Baseline TBD" fails this criterion.
- The workflow-interview coverage is stated as a cadence and a coverage commitment (which roles × BUs), not as "we'll interview some users."
- The telemetry sanity-check line explicitly disclaims usage as a headline metric. The exact word "headline" does not need to appear, but the discipline does.
- The theatre watchlist cites all four Chapter 01 patterns by name.
- The defence paragraph cites exactly one theatre pattern by name and explains why this rollout was vulnerable to it in one specific sentence.
- No invented vendor-reported numbers used as targets. Published numbers may be cited as methodology references but not transplanted as targets.

## Stretch goals

- Extend the framework template with a "measurement graduation" section — how the framework evolves as a rollout moves from pilot (where measurement is tight and operator-level) to rollout (where measurement is portfolio-level and aggregated). The two measurement regimes are different, and the framework can document the transition explicitly.
- Produce a second worked example on a rollout from a different task family (if you did drafting, pick summarization or support). The second example tests whether your framework actually travels across task families or whether it over-fit to the first one.
- Write a one-page objection-handling sheet: the three most likely pushbacks from rollout owners against using this framework ("too much work," "we don't have a baseline," "the vendor dashboard already shows it"), each with a two-sentence response.

## Why this exercise matters

The scorecard's credibility compounds across rollouts; a single rollout measured as usage percentage poisons the portfolio rollup. The framework is what makes "outcomes first" the default for every rollout owner, not a per-rollout argument the enablement lead has to win repeatedly. The exercise trains the reflex of pinning down the specification *before* launch, when the baseline can still be measured and the theatre patterns can still be preempted. This is the paper discipline that makes the rest of the module's work possible.
