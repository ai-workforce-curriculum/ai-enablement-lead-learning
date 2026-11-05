# The Commissioning Brief as the Load-Bearing Artifact

> The brief is the only artefact in this module that an `applied-ai-engineer` cannot start without. Chapter 01 named the commissioner stance. This chapter writes the brief. Not a commissioning-brief checklist — the actual eight-section artefact, what each section answers, what engineers cannot work without, and the stage-gate review the brief passes through before a line of code is written.

## What the brief is for

The brief is a signed artefact with three audiences and three purposes:

- **The `applied-ai-engineer` (or `agentic-ai-engineer`) who builds the tool.** The brief is the specification they build against. It names the outcome, bounds the constraints, and leaves the architecture to them.
- **The `ai-engineering-manager` who co-signs on the engineering side.** The brief is the commitment their report is being asked to deliver against. It names the budget, the timeline, and the acceptance criteria that determine when the project is done.
- **The `head-of-ai-governance` (L60) who reads for program-level posture.** The brief is the artefact the governance council reviews when deciding whether the commission crosses into policy or risk thresholds. The guardrails section is the governance-facing read.

The brief is **signed before build**. Unsigned briefs are conversations. [mod-102 Chapter 06](../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md) named the signature discipline; this chapter names the content the signature is binding on.

## The eight sections

The brief has eight required sections. Order matters: each section is a precondition for the next, and the stage-gate review at the end of this chapter checks the sections in order.

### Section 1 — Problem statement

**One paragraph. The business problem, not the AI technique.** The paragraph names:

- The function or role population that has the problem.
- The specific workflow step where the problem bites.
- The current baseline — the time, cost, error rate, or quality shortfall today, as a number not an adjective.
- The reason a commercial tool from the approved envelope was not the answer (this is the Column 4 justification from [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md), summarised in one sentence).

**Smell test.** If the paragraph contains the words "AI agent," "LLM," "RAG," or "copilot" in the problem statement — as opposed to the technique section a few lines down — the paragraph is probably wrong. The problem statement names what is broken, not what will be built.

### Section 2 — Target task and user cohort

**Who uses the tool, to do what, as part of which workflow.** This section names:

- **The user cohort.** Role title, team, size (how many operators), whether this is the whole population or a pilot cohort, and whether participation is opt-in or mandated. Pre-existing training is named by reference to the [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md) curriculum.
- **The target task.** The workflow step the tool is replacing, augmenting, or inserting into — named from the operator's point of view, not the architect's. "Operator reads the inbound ticket and selects a routing queue" not "the agent performs intent classification over inbound ticket text." The engineer translates between the two; the brief holds the operator's framing.
- **The current workflow around the task.** What runs before the task today; what runs after. This is what the engineer's integration surface will have to respect. If the task is one step in a workflow of eight, the brief names all eight and marks the step the tool is entering.

### Section 3 — Success criterion

**A measurable statement of what "this worked" means.** The success criterion is the single most-contested section of the brief, and the one that most benefits from the discipline named in [mod-102 Chapter 02](../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md) and [mod-106 Chapter 01](../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md). The section names:

- **The outcome metric.** The business-outcome shift the tool is supposed to produce — first-contact resolution rate, documentation-quality score, time-to-triage, policy-compliance rate. Named with a baseline (the number today) and a target (the number after rollout), both with confidence bands where the scorecard framework uses them.
- **The workflow metric.** The leading indicator the outcome metric depends on — step completion time, error rate on the step the tool targets, downstream rework rate.
- **Usage as sanity check.** Minimum adoption below which the outcome metric cannot be interpreted — not a success criterion, a floor. [mod-102 Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md) named the three-layer priority; this section applies it.

A success criterion that reads "the tool is used by 80% of eligible operators within three months" is a usage metric and belongs in the sanity-check line, not the outcome line. The brief refuses this substitution. A commission whose success criterion is a usage number is a commission whose outcome was never specified.

### Section 4 — Non-negotiable guardrails

**The behaviours the tool must not exhibit, phrased in terms the engineer can test against.** This section is where the brief's connection to [mod-103](../mod-103-policy-co-authoring-with-governance/README.md) lands. Four classes of guardrail:

- **Data-class constraints.** Which data classes the tool must not read, write, retain, or emit. These come out of the data-handling SOP in [mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md).
- **Action constraints.** Which actions the tool must not take without a human in the loop — sending external communications, making financial commitments, modifying customer records, approving policy exceptions. For agentic tools, this is the step-boundary discipline named in [Chapter 01](01-the-commissioner-stance-not-the-builder.md).
- **Surface constraints.** Which deployment surfaces the tool may reach and which it may not — internal web, email, customer-facing channels, regulator-facing channels.
- **Escalation obligations.** When the tool must escalate to a named human (this is a *success criterion*, not a *failure* — an agent that escalates correctly is doing its job).

The guardrails section is co-reviewed with `head-of-ai-governance` (L60) and, for the red-team-ask-triggering guardrails, with `ai-risk-engineer` (L25). The red-team ask itself is attached to the brief as Appendix A; it names which guardrails the red-team will test and when the evidence is needed (before pilot-to-rollout, not after — this is the discipline from [mod-102 Chapter 06](../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md)).

### Section 5 — Budget

**Build and run, both numbers.** The budget section names:

- **Build cost.** The engineer-week cost projected by the `ai-engineering-manager`, plus a named contingency (20–30% is typical; the specific number is a conversation with the manager, not a default).
- **Run cost at steady state.** Inference cost, infrastructure cost, maintenance-owner cost — the full operating footprint after acceptance. A commissioned tool whose run cost is five times the comparable commercial tool is a Column 4 decision that should have been Column 2 or 3; the brief surfaces this at commission time, not at the first annual budget cycle.
- **The source of both numbers.** The TCO shape from [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) feeds the build number; the cost model from [mod-107 Chapter 01](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/01-the-enablement-cost-model-at-org-scope.md) feeds the run number. The brief cites the source so the numbers remain defensible under Finance audit.

### Section 6 — Timeline

**Pilot date, rollout date, decision gates in between.** The timeline section names:

- **The build calendar.** From signed brief to pilot-ready prototype — a dated range, not a sprint count.
- **The pilot charter trigger.** The point at which the mod-102 Chapter 02 pilot charter is authored; pilot charter authoring is **not a commissioning-side activity** — it is the standard pilot design the enablement lead runs on every rollout. The brief names the trigger point.
- **The pilot-to-rollout decision gate.** The date the rollout-vs-adopt-vs-kill call is made, which is also the date red-team evidence is due in the rollout artefact set.
- **The acceptance date.** The date the commissioner formally accepts the tool from the engineering team — the hand-off point to steady-state operation under the mod-102 rollout artefact set.

A timeline whose gates are month-granularity rather than date-granularity ("Q2 pilot, Q3 rollout") is a timeline that will drift. The brief refuses this; gates are dated.

### Section 7 — Maintenance commitment

**Who owns the tool after acceptance.** This is the section a commissioning brief most often short-changes, and the section whose weakness most often predicts tool-death at year one or two.

The maintenance commitment names:

- **The owner.** A specific team or named engineer who has committed to carrying the tool. Not "the AI Engineering team in general" — a named report or named manager. If the owner is not yet nameable at brief time, the brief flags this as a stage-gate blocker rather than signing with a TBD.
- **The commitment shape.** How much engineer-time per month at steady state the maintenance owner is committing. For a well-scoped point tool, this is often one to two engineer-days per month; for an agentic tool with multi-step evaluation surfaces, it is often higher.
- **The on-call expectation.** Who the tool pages when it breaks outside hours, and the SLA the maintenance owner is committing to.
- **The scope of maintenance.** What is in — bug fixes, prompt iteration, eval-harness updates, vendor-model changes (LLM-provider version bumps) — and what is explicitly out — feature expansion, new user cohorts, new target tasks. A new target task is a new commission, not a maintenance task.

The maintenance commitment is co-signed by the maintenance owner and by that owner's manager, independently of the `ai-engineering-manager`'s build sign-off. Build and maintenance can live in different organisations inside the engineering family; the brief requires both signatures.

### Section 8 — Rollout-artefact-set binding

**The specific instances of the mod-102 rollout artefacts this commission is responsible for populating.** This section is what prevents the commission from drifting away from the standing rollout framework:

- **Use policy** — references the mod-103 policy stack; the policy slot for this tool is co-authored with governance at the pilot-charter trigger.
- **Data-handling SOP** — references the mod-103 SOP; the tool's data-flow diagram is attached here as Appendix B for the governance co-author to redline against.
- **Access & offboarding playbook** — references the IT identity partnership from [mod-107 Chapter 04](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/04-partnering-with-procurement-finance-and-it.md).
- **Training package** — references the [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md) curriculum slot.
- **Support & escalation path** — references the [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) artefact 5 slot.
- **Champion list** — references the [mod-105](../mod-105-champion-networks-and-change-management/README.md) network.
- **Kill-switch & rollback plan** — references [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) artefact 7; the commissioning brief names the authoriser, the revocation sequence, and the evidence-preservation obligations in [mod-109 Chapter 02](../mod-109-ai-incident-response-and-enablement-side-rollback/02-the-kill-switch-as-an-operating-artifact.md).

Each slot is a reference, not a re-authoring. The brief points at where the rollout artefact will live and names the co-authors; it does not re-write the artefact set the preceding modules authored.

## The stage-gate review

A brief is **drafted** by the commissioner, **reviewed** against a stage-gate, and **signed** by the three signatories (commissioner, `ai-engineering-manager`, `head-of-ai-governance`). The stage-gate is a one-hour review the commissioner runs with a reader who was not part of the drafting — a peer enablement lead, an `ai-enablement-partner` who will embed with the user cohort, or the reviewer-role the organisation uses for CoE operating reviews (see [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md)).

The stage-gate checks seven questions in order:

1. **Is the problem statement one paragraph, named at the workflow step, with a quantitative baseline?** If the paragraph is three paragraphs, or if the baseline is an adjective ("slow," "expensive"), the brief goes back for Section 1.
2. **Does the success criterion name an outcome metric with baseline and target, not a usage metric dressed up as success?** If the criterion is "80% adoption," the brief goes back for Section 3.
3. **Are the guardrails in testable form?** "The tool must not disclose patient data" is testable; "the tool must respect patient privacy" is not. If the guardrails are unverifiable, Section 4 goes back.
4. **Is the red-team ask attached and dated before pilot-to-rollout?** If not, Section 4's Appendix A is incomplete.
5. **Does the budget cite its source (TCO shape, cost model)?** If the numbers float without provenance, Section 5 goes back.
6. **Is the maintenance owner named — a team or human, not a role abstraction?** If the owner is TBD, Section 7 is a stage-gate block.
7. **Does the rollout-artefact-set binding reference each slot or explicitly waive it with governance sign-off?** A commissioned tool that does not inherit the policy stack or the champion network is operating outside the enablement program, not inside it.

A brief that clears seven passes to the three signatures. A brief that fails any question returns to the commissioner for revision; the stage-gate is not a scoring exercise, it is a gate.

## What changes for agentic tools versus point tools

The eight sections are the same for an `applied-ai-engineer` brief and an `agentic-ai-engineer` brief. Three sections have agentic-specific expansions:

- **Section 2 (target task)** names the step boundary explicitly — the point in the workflow where the agent hands back to the human. For multi-step agents, the step boundary is often fuzzy by default; the brief sharpens it.
- **Section 3 (success criterion)** adds a **step-correctness metric** alongside the outcome and workflow metrics. A multi-step agent that gets the final answer right 80% of the time by taking three wrong steps and one correcting step is a brittle tool even though its outcome number looks good; the step-correctness metric exposes this.
- **Section 4 (guardrails)** adds **action-authorisation constraints** — the specific actions that require human review, and the escalation path when the agent cannot complete autonomously. The escalation is a success criterion (per Chapter 01), named here and tested in the eval harness (Chapter 05).

The architecture decisions that make these constraints hold — tool-use patterns, planner design, reflection loops — are the engineer's call. The brief constrains behaviour; the engineer builds the system.

## What the commissioning brief is not

Three mis-shapes the brief regularly drifts into. Each is a Chapter 01 posture failure landing on the brief:

- **A design document.** If the brief contains an architecture diagram, a model choice, a retrieval-pattern specification, or a vendor selection, the commissioner has drifted into designer posture. Pull the architecture out and send the brief back to Section 4.
- **A product-requirements document (PRD).** A PRD lists features. The brief does not. The brief names an outcome and constraints; the engineer decides which features achieve the outcome inside the constraints. If the brief has a feature list, the commissioner has drifted into product-manager posture. Pull the feature list out and replace with the success criterion the features were trying to satisfy.
- **A governance redline.** The guardrails section is the governance-facing read; the whole brief is not. If the brief has drifted into a policy document, the commissioner has done [mod-103](../mod-103-policy-co-authoring-with-governance/README.md)'s work in this chapter's space. Pull the policy content out, reference the mod-103 artefacts in Section 8, and restore the brief to its scope.

## Summary

- The brief is **the** load-bearing artefact of a commission. Unsigned briefs are conversations; signed briefs are commitments.
- Eight sections, in order: problem statement, target task & cohort, success criterion, non-negotiable guardrails, budget, timeline, maintenance commitment, rollout-artefact-set binding.
- The success criterion is an outcome metric with baseline and target; usage is a sanity-check floor, not a success. This is the mod-102 Chapter 04 and mod-106 discipline applied at commission time.
- The guardrails are testable, in behavioural terms, with a red-team ask attached and dated before pilot-to-rollout.
- The maintenance owner is a named team or human with a dated commitment and a co-signature from that owner's manager. TBD is a stage-gate block.
- The stage-gate review runs seven questions in order before the brief is signed; a brief that fails any question returns for revision.
- The brief is not a design document, a PRD, or a governance redline. When it drifts into any of those shapes, a Chapter 01 posture has collapsed and the brief is pulled back to its scope.
