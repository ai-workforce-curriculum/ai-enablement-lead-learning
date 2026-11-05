# Exercise 03 — Org-Scope Build-vs-Buy Matrix

**Estimated effort:** 3 hours
**Format:** scored matrix (Markdown table), signed-artifact writeup, and a one-paragraph decision recommendation
**Grounding chapters:** [03 — The Build-vs-Buy Matrix at Enterprise Scope](../03-the-build-vs-buy-matrix-at-enterprise-scope.md), [01 — The Enablement Cost Model at Org Scope](../01-the-enablement-cost-model-at-org-scope.md), [02 — Projecting ROI with Confidence Bands](../02-projecting-roi-with-confidence-bands.md), [04 — Partnering with Procurement, Finance, and IT](../04-partnering-with-procurement-finance-and-it.md), [06 — The Vendor Vetting Rubric](../06-the-vendor-vetting-rubric.md)

## Objective

Run the four-column build-vs-buy matrix on one concrete target task: compare candidates from coding / knowledge-work copilots (Column 1), platform add-ons (Column 2), industry-specific tools (Column 3), and internal build (Column 4) using the ten-dimension comparison frame from [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md). Produce the signed artifact that would land at the Stage 2 gate from [mod-102 Chapter 01](../../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md), with weights published, scores filled, TCO shapes derived from [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md), projected ROI bands from [Chapter 02](../02-projecting-roi-with-confidence-bands.md), and the recommendation defended.

## Prerequisites

- [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md) read; the four columns, the ten dimensions, the TCO shapes per column, and the three failure modes close enough to cite without the chapter open.
- [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md) read; TCO for each candidate uses the six-family cost model structure.
- [Chapter 02](../02-projecting-roi-with-confidence-bands.md) read; projected ROI for each candidate carries a composed band.
- [Chapter 04](../04-partnering-with-procurement-finance-and-it.md) read; the contract-term vocabulary shapes the data-boundary, compliance, and switching-cost dimensions.
- [Chapter 06](../06-the-vendor-vetting-rubric.md) read; vendor-concentration and capability-ceiling dimensions use the vetting rubric.
- One concrete target task — not a function, a *task*. "Drafting first-pass responses to tier-one support tickets," not "customer support." Candidates include an engineering-copilot task, a knowledge-work drafting task, a meeting-summary task, a support-copilot task, a legal-research task, or a clinical-documentation task. Carrying the task from Exercise 02 if applicable is efficient.

## Problem statement

The organization is at Stage 2 of [mod-102 Chapter 01](../../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md)'s selection decision for your chosen target task. The Stage 1 problem is well-named. Three BUs have independently surfaced the same task as a priority. Procurement has flagged that any single purchase above $250K annualized requires a formal build-vs-buy writeup. The executive sponsor has asked for a signed four-column artifact before the Stage 2 gate review in two weeks.

Your job is to produce the signed writeup — the matrix scored across all four columns, the recommendation defended, the disqualifiers acknowledged, the dependencies named — in a form that Procurement, Finance, Security, and the executive sponsor can co-sign.

## Requirements

### Part A — the matrix

Produce a scored matrix with four columns and ten rows.

Rows (dimensions from [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md)):

1. Capability fit for the target task.
2. Total cost of ownership over the three-year horizon.
3. Projected ROI with band.
4. Data boundary.
5. Data residency.
6. Security and compliance posture.
7. Switching cost.
8. Vendor concentration and resilience.
9. Capability ceiling and roadmap.
10. Operating complexity.

Columns (candidates from [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md)):

- **Column 1 — coding / knowledge-work copilot.** Name a specific current-market tool appropriate to the task (e.g., for coding tasks: GitHub Copilot, Cursor, Claude Code, Windsurf; for knowledge work: ChatGPT Enterprise, Claude for Enterprise).
- **Column 2 — platform add-on.** Name a specific add-on on a SaaS the organization already runs (Microsoft Copilot across M365, Google Gemini for Workspace, Zoom AI Companion, Salesforce Einstein, ServiceNow Now Assist, Atlassian Rovo).
- **Column 3 — industry-specific tool.** Name a specific domain tool relevant to the task if applicable (clinical: Nuance DAX, Abridge; legal: Harvey, Spellbook; support: Ada, Decagon; sales: Gong, Chorus). If no industry tool is relevant, mark the column "not applicable because …" with a one-sentence reason.
- **Column 4 — internal build.** Describe the build scope honestly — thin wrapper, RAG-grounded assistant, agentic workflow. Scope it to the ambition and the engineering bench.

Each cell contains: a score (1-5), a one-to-two-sentence note. Scoring criteria are stated once above the matrix (1 = severe concern or weak fit; 5 = strong fit or minimal concern).

Weights (summing to 100) are published above the matrix with rationale. Non-capability dimensions (TCO, ROI, data boundary, compliance, switching cost, vendor concentration, operating complexity) sum to at least 40% per [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md).

### Part B — TCO shapes

For each candidate, a one-paragraph TCO walk over the three-year horizon:

- Column 1: front-loaded enablement (year one Family 2, 3, 4), back-loaded license (years two-three Family 1), annual uplift modeled, add-on / tier creep modeled.
- Column 2: license-dominant TCO at scale, coupled to parent-SaaS contract.
- Column 3: higher per-seat cost, embedded compliance posture, narrower addressable surface.
- Column 4: front-loaded build cost (year zero/one engineering), ongoing operating cost (model hosting/API, maintenance, iteration, incident response), with the maintenance commitment explicit.

Each TCO walk produces a three-year total and a stated band.

### Part C — projected ROI per candidate

For each candidate, the projected three-year ROI from [Chapter 02](../02-projecting-roi-with-confidence-bands.md)'s method — central estimate and composed band. The numerator inputs are the same across candidates (the target task's value realisation is task-shaped, not tool-shaped); the denominator varies per candidate TCO; the ramp and crossover differ by candidate (platform add-ons typically have the fastest crossover; internal builds the slowest). State explicitly.

### Part D — the signed artifact

The writeup, structured per the [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md) template:

```
Build-vs-Buy Decision — <target task name>

Stage 1 problem statement: <one sentence>
Target task and cohort: <summary>

Candidates considered
  Column 1 (copilot): <specific tool>
  Column 2 (add-on):  <specific add-on>
  Column 3 (industry): <specific tool or "not applicable because …">
  Column 4 (build):   <build scope>

Comparison (ten dimensions, weighted)
  Weights (summing to 100): <published, with rationale>
  Scores: <table across candidates>

TCO (three-year horizon)
  Candidate A: $X.X M, with band
  Candidate B: ...
  ...

Projected ROI (three-year horizon, Chapter 02 method)
  Candidate A: central Yx, 90% band Z-W
  ...

Recommendation: <candidate, with reasoning paragraph>
Disqualifiers acknowledged: <non-winning candidates' failure modes>
Dependencies: <what has to be true for the recommendation to hold>
Decision owner: <sponsor / Stage 3 attendee>
```

### Part E — the failure-mode self-check

A short paragraph (3-5 sentences) stating whether each of the three failure modes from [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md) appears in your writeup:

1. Vendor capture (three columns effectively empty).
2. Build hubris (year-three internal-build TCO lower than any vendor's, with thin maintenance line).
3. Capability-only scoring (non-capability weights sum to less than 40%).

For any pattern present, revise before finalizing.

## Starter guidance

- Name specific current-market tools in the columns, even if the market will change. A writeup with "Tool A, Tool B" labels is not readable in a steering meeting; a writeup with "Claude Code vs. Microsoft Copilot vs. internal RAG build" is. Readers will mentally substitute the tools that are current at their reading time; keep the names current enough to be useful.
- The hardest column to score honestly is Column 4 (internal build). The build hubris pattern lives there. Internal-build TCO for a non-trivial tool is typically 4-8 FTE for 6-9 months plus 1-3 FTE ongoing; honest scope is almost always larger than the engineering-lead's first estimate. Peer-review the Column 4 TCO with an engineering lead who would inherit the maintenance before finalizing.
- If Column 3 genuinely has no candidate (the target task has no industry-specific tool), mark it "not applicable because …" with a one-sentence reason and do not score it. The matrix should not be padded; an honest "not applicable" is preferable to a hollow score.
- Weights are a methodology choice. For regulated workflows, compliance and data-boundary weights are typically 15-20% each. For high-volume commodity workflows, TCO weight dominates. For frontier-capability workflows, capability fit and capability ceiling dominate. State the rationale.
- The disqualifiers section is the one most often left blank. Non-winning candidates have specific reasons they lost; naming the reasons shows the matrix was run honestly. "Column 2 lost on capability-ceiling: the add-on lags Column 1 by 12-18 months on the task's complexity frontier" is a specific disqualifier; "Column 2 scored lower" is not.
- The dependencies section is where the recommendation's fragility shows. "Recommendation holds if the vendor's SOC 2 Type II renews on schedule in Q3; if it does not, re-open with Column 4 as the fallback" is honest and makes the recommendation reviewable.
- The vendor-concentration dimension scores against the existing portfolio from [Chapter 06](../06-the-vendor-vetting-rubric.md). A recommendation that further concentrates spend on an already-dominant vendor is not disqualified but is a line the writeup owes.

## Deliverables

- `build-vs-buy-matrix.md` containing Parts A through E.

## Acceptance criteria

- All four columns are populated with a specific tool or a specific "not applicable because …" explanation; no column is a blank placeholder.
- All ten dimensions are scored for each in-scope column; scoring criteria are stated once above the matrix.
- Weights sum to 100; non-capability weights sum to at least 40%; rationale is published.
- TCO is reported per candidate as a three-year total with a stated band; the Column 4 TCO carries an explicit ongoing-maintenance line.
- Projected ROI per candidate uses Chapter 02's method: central estimate and composed band.
- The recommendation paragraph names the winning candidate and defends the recommendation on at least three of the ten dimensions.
- The disqualifiers section names specific reasons the non-winning candidates lost (not just "scored lower").
- The dependencies section states at least two conditions under which the recommendation could change.
- The failure-mode self-check addresses each of the three patterns from [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md); where any pattern is present, the writeup has been revised.
- The writeup is in a form the four co-signers (sponsor, Finance, Procurement, Security) could reasonably sign.

## Stretch goals

- Run the matrix for the same target task two more times — once under the weights that a regulated-industry organization would use (compliance and data-boundary heavy), once under the weights that a cost-sensitive mid-market organization would use (TCO heavy). Compare the three recommendations; the exercise is in seeing how weight choices shift winners.
- Extend Column 4 into a mini-commissioning brief — the scope, the engineering plan, the maintenance plan, the handoff to [mod-110](../../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md). The brief is what mod-110 picks up if Column 4 wins; writing it now makes the Column 4 scoring honest.
- Produce the one-page executive summary of the matrix: BLUF with the recommendation, the two load-bearing dimensions, the composed ROI band, and the dependencies. The summary is what the sponsor reads before the Stage 2 gate.

## Why this exercise matters

Build-vs-buy decisions at enterprise scope commit the organization for years on contracts that reshape the tool stack, the champion network, the training program, and the scorecard. A decision made in a single-column writeup — because a vendor was already in the room — produces lock-in the organization did not deliberately choose. The four-column matrix is the shape of the decision at the altitude the role operates at; running it honestly across four columns, ten dimensions, and three year-horizon TCOs is the discipline that distinguishes the enablement lead's writeup from a vendor pitch deck. This exercise is the first draft of that writeup for your chosen task.
