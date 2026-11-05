# Exercise 01 — Commissioning Brief Drill

**Estimated effort:** 2 hours
**Format:** signed commissioning brief + stage-gate review summary + two-paragraph scope contract, Markdown
**Grounding chapters:** [01 — The Commissioner Stance — Not the Builder](../01-the-commissioner-stance-not-the-builder.md); [02 — The Commissioning Brief as the Load-Bearing Artifact](../02-the-commissioning-brief-as-the-load-bearing-artifact.md). Prior reading: [mod-102 Chapter 06](../../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md); [mod-107 Chapter 03](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md).

## Objective

Produce the signed commissioning brief that an `applied-ai-engineer` (or `agentic-ai-engineer` if the problem is multi-step) could begin building against on the day you submit it. The brief passes the seven-question stage-gate review from Chapter 02 in order. You carry the same chosen organisation and the same commission across Exercises 01, 02, 03, and 04 — so pick deliberately.

The output is the eight-section brief itself, a stage-gate review summary that walks the seven questions and names where each section landed, and a two-paragraph scope contract that distils what the three signatures are binding on.

## Prerequisites

- Chapters 01 and 02 read.
- [mod-102 Chapter 06](../../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md) read as the surface-level framing this exercise deepens.
- [mod-107 Chapter 03](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) read as the upstream decision — the brief is the deliverable of a Column 4 decision that has already been run.
- A chosen organisation and a chosen commission — **you will carry this across Exercises 01–04**. If you do not have one in mind, pick one of:
  - A 4,000-person professional-services consultancy commissioning an engagement-document triage agent that reads inbound engagement materials and routes them to the correct deal team with a preliminary engagement-type classification and a first-pass staffing note.
  - An 8,000-person regional health system commissioning a clinical-documentation prior-authorisation drafting agent that reads the physician's note plus payer policy and drafts a first-pass prior-auth narrative for a named list of specialties.
  - A 12,000-person bank commissioning a model-risk-management agent that reads the model-inventory and the challenger-model report, drafts a validation memo per SR 11-7, and routes to the model-risk-review council with a named severity tag.
  - A 2,500-person ed-tech vendor commissioning an internal customer-success agent that reads the account-health dashboard, the last 90 days of ticket history, and the customer's success plan, and drafts a quarterly business-review outline for the CSM to edit.

The chosen commission is the Column 4 decision that has already been made upstream; this exercise does not re-litigate the matrix.

## Problem statement

You are the enablement lead whose rollout artefact set has been running against vendor tools for a year. The mod-107 Chapter 03 matrix has landed on Column 4 for the commission you chose above. Your `ai-engineering-manager` has nominated an `applied-ai-engineer` (or `agentic-ai-engineer` for an agentic problem) who is available to begin kickoff on signature. Your job is the brief.

Treat the three signatures as live — the `ai-engineering-manager` will push back on architectural assumptions written into the brief, `head-of-ai-governance` will push back on under-scoped guardrails or a missing red-team ask, and the maintenance owner you name will push back if their Section 7 commitment is under-specified. Write the brief as if these signatures are being collected tomorrow.

## Requirements

### Part A — The eight-section brief

A single Markdown document with the eight sections from Chapter 02 at operational depth. Required:

- **Section 1 — Problem statement.** One paragraph. Function or role population; workflow step; quantitative baseline; one-sentence Column 4 justification from mod-107 Chapter 03. No AI technique in the problem statement.
- **Section 2 — Target task and user cohort.** User cohort (role, team, size, opt-in/mandated, pre-existing training reference); target task named from the operator's point of view; the current workflow around the task (what runs before, what runs after). For an agentic tool, the step boundary is named explicitly.
- **Section 3 — Success criterion.** Outcome metric (name, baseline, target, confidence-band shape); workflow metric; usage floor. For an agentic tool, a step-correctness metric alongside outcome and workflow.
- **Section 4 — Non-negotiable guardrails.** Data-class constraints, action constraints, surface constraints, escalation obligations. The red-team ask is attached as Appendix A — scope, threat-model inputs, success criteria for the red-team exercise itself, when evidence is needed (dated against the pilot-to-rollout gate), fold-back route for findings.
- **Section 5 — Budget.** Build cost (engineer-week cost with contingency); run cost at steady state (inference, infrastructure, maintenance); the source of both numbers (TCO shape from mod-107 Chapter 03, cost model from mod-107 Chapter 01).
- **Section 6 — Timeline.** Build calendar dates; pilot charter trigger date; pilot-to-rollout decision-gate date; acceptance date. Gates are dated, not month-granular.
- **Section 7 — Maintenance commitment.** Named owner (team or human); commitment shape (engineer-days per month at steady state); on-call expectation and SLA; scope of maintenance (what is in, what is explicitly out).
- **Section 8 — Rollout-artefact-set binding.** Each of the seven mod-102 Chapter 03 artefacts with a one-line reference to the specific instance this commission is binding to — use policy, data-handling SOP, access & offboarding playbook, training package, support & escalation path, champion list, kill-switch & rollback plan.

Appendices: Appendix A (red-team ask) and Appendix B (data-flow diagram reference — you may describe the data flow in prose rather than a diagram; name the data classes and surfaces).

### Part B — The stage-gate review summary

A one-page Markdown document that walks the seven stage-gate questions from Chapter 02 in order:

1. Is the problem statement one paragraph, named at the workflow step, with a quantitative baseline?
2. Does the success criterion name an outcome metric with baseline and target, not a usage metric dressed up as success?
3. Are the guardrails in testable form?
4. Is the red-team ask attached and dated before pilot-to-rollout?
5. Does the budget cite its source?
6. Is the maintenance owner named — a team or human, not a role abstraction?
7. Does the rollout-artefact-set binding reference each slot or explicitly waive it with governance sign-off?

For each question, name **pass**, **revise**, or **gate block**, and if revise or gate block, point to the section and specify the revision.

### Part C — The scope contract

Two paragraphs. The first paragraph is what the commissioner's signature binds to — problem, cohort, outcome, Section 8 slots. The second paragraph is what the brief is explicitly NOT a signature on — architecture decisions deferred to the engineer, policy decisions deferred to `head-of-ai-governance`, red-team methodology deferred to `ai-risk-engineer`. The scope contract is what the three signatories will read aloud at the brief-signing hand-off (Chapter 06).

## Starter guidance

- The hardest section is almost always Section 3. Spend the first thirty minutes just naming the outcome metric and its baseline and target against the mod-106 Chapter 01 framework. If you cannot name the metric, the commission is not ready — go back to Chapter 01's one-paragraph test.
- The most-often-missed section is Section 7. If the maintenance owner is TBD when you draft the brief, treat Section 7 as a stage-gate block (question 6) and name the specific conversation required to clear it. Do not sign a TBD.
- For the red-team ask, the scope is narrower than you think. Name the specific guardrails the red-team will exercise, not "all vulnerabilities." Date the evidence against the pilot-to-rollout gate from Section 6 explicitly.
- For an agentic-tool commission, the step boundary in Section 2 is the hardest part and the one the engineer will push back on if it is fuzzy. Make the brief sharp enough that the engineer can evaluate whether a candidate agent design respects the boundary.
- Where an organisational fact you need is unknown (specific role titles, specific policy document names, specific baseline numbers from mod-106 scorecards that do not yet exist), use `<!-- needs-research: ... -->` inline. Do not invent numbers.
- Do not write architecture into the brief. If you catch yourself naming a model, a retrieval pattern, or a vendor SDK, pull it out — the brief constrains behaviour, not means.

## Deliverables

- `brief.md` — the eight-section commissioning brief with Appendices A and B.
- `stage-gate-review.md` — the one-page review summary.
- `scope-contract.md` — the two-paragraph scope contract.
- A short cover note (3–5 sentences) summarising the section you found hardest to write and the one Chapter 01 posture (designer, product manager, apologist) you most actively guarded against while writing.

## Acceptance criteria

- The brief has all eight sections plus Appendices A and B; every section meets the Chapter 02 content requirements for its type.
- The success criterion is an outcome metric with baseline and target; usage appears only as a sanity-check floor.
- The guardrails are testable (behavioural, verifiable), not aspirational.
- The red-team ask is dated before the pilot-to-rollout gate in Section 6.
- The maintenance owner is a named team or human with a dated commitment and a co-signature line.
- The brief contains no architecture decisions — no model names, no retrieval-pattern names, no vendor SDKs. If an architecture term is absolutely necessary (say, "the tool must integrate with the organisation's SSO"), it is a constraint, not a design.
- The stage-gate review summary walks seven questions in order with a pass/revise/gate-block call on each.
- The scope contract's two paragraphs name what is bound and what is explicitly not.
- `<!-- needs-research: ... -->` is used wherever an organisational fact is missing.

## Stretch goals

- Add a **pilot cohort recruitment plan** as Appendix C — the specific operators who will participate in the pilot, how they were selected, and how their baseline is measured.
- Add a **retirement-criteria statement** to Section 3 — the specific target-miss pattern (e.g., three consecutive quarters below baseline on the outcome metric) that will trigger the Chapter 06 graduate-or-retire review's retire outcome. Pre-committing retirement criteria at commission time is the Chapter 01 apologist-posture prevention written into the brief.
- Draft a **"what the brief did not resolve"** memo — one page — naming the specific questions you flagged for the brief-signing hand-off meeting (Chapter 06) rather than resolving in the draft. These are the scope-contract-defining questions the three signatories will discuss before signing.

## Why this exercise matters

The brief is the single artefact this role's authority with the AI Engineering family runs through. An engineer whose brief is sharp builds the right tool on the first pass; an engineer whose brief is vague spends six weeks doing the commissioner's discovery work. The stage-gate review is the forcing function that makes the brief defensible before it is signed — and the scope contract is what the three signatures are collectively binding on, which is the one artefact a mid-build scope-creep conversation will live or die on. Producing all three under a two-hour budget is the calibration for producing them under live commission pressure, when the engineer's calendar and the business sponsor's patience set a tighter clock.
