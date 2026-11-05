# The Service Catalog as the CoE's Public Interface

> The organisation does not read the operating loop from Chapter 01. Operators, team managers, BU heads, the exec sponsor, and the governance side all read the same thing — the service catalog. The catalog is what the CoE can be *called on* to do, which is a very different thing from everything the CoE *could* do. This chapter authors the catalog as a signed-in interface — six slots, an intake form, service levels, and a deprecation discipline — so that the CoE's week can be defended and the organisation can know what it is entitled to ask for.

## Why "catalog" and not "menu"

A menu suggests optionality — pick what you want, we will do what we can. A catalog suggests a signed interface — these are the services we commit to, with the inputs we require, the time we take, and the output we return. The language matters because the catalog is the artefact that bounds Monday triage ([Chapter 01](01-the-coe-at-steady-state.md)). Without a catalog, Monday triage is a negotiation; with a catalog, Monday triage is a routing decision.

The catalog is also the artefact the CoE's budget is defended against ([mod-107 Chapter 02](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/02-the-enablement-cost-model.md)). Each slot has a staffing commitment underneath it — a service-level agreement supported by hours per slot per quarter per FTE. When Finance asks why the lead is asking for a second embedded enablement partner, the catalog is the line-item answer: *we are promising X on this slot; we are delivering Y; the gap is the staffing ask*. A CoE without a catalog defends budget on feelings; a CoE with a catalog defends it on queue depth and SLA misses.

## The six service-catalog slots

The six slots line up with the six most-cited themes in the role evidence (R1–R4 tooling and measurement, R5 policy, R7–R12 training, R8 champions, and the incident path from [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)) collapsed into a service interface. The slots are:

1. **Tool Selection.** Running the three-stage decision from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) on a requested tool or use case.
2. **Pilot Design and Operation.** Authoring the pilot charter, running the bounded pilot, applying the adopt / extend / kill decision from [mod-102 Chapter 02](../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md).
3. **Rollout and the Artefact Set.** Delivering the seven-piece rollout artefact set from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) against a confirmed adopt decision.
4. **Training and Enablement.** The audience-segmented curriculum and role-based playbooks from [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md); the delivery mix (workshops, office hours, bootcamps, spotlights).
5. **Outcome Measurement.** The three-cadence measurement framework from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) — the monthly scorecard, the quarterly deep-read, the ad-hoc read in support of a pilot-vs-rollout or build-vs-buy decision.
6. **Incident Support.** The enablement-side slice of the incident path from [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) — field-signal triage, communications, rollback coordination, post-incident fold-back into policy, training, and the champion priority list.

Six slots is deliberately a small catalog. A larger catalog looks more complete but is harder to staff, harder to measure, and easier to drift. If a seventh slot is being pulled for — "commissioning of internal tools" is the common candidate — check it against Chapter 01's three failure modes first. Commissioning ([mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md)) is a recurring but low-volume operation; it is better served as a workflow *inside* the Tool Selection slot (the three-stage decision's Column 4 outcome from [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md)) than as a seventh standalone slot that drags the operating loop.

## What a service-catalog slot specifies

Each slot in the catalog is a signed interface with the following six fields:

### Field 1 — Problem statement the slot accepts

Not "we help with AI." A one-sentence predicate that lets a requester determine whether their ask is in scope:

- *Tool Selection:* "We run the three-stage selection decision when a function has a bounded problem and no in-envelope approved tool fits."
- *Pilot Design and Operation:* "We design and run bounded pilots for a candidate tool that has already passed the three-stage selection's extend gate."
- *Rollout and the Artefact Set:* "We deliver the rollout artefact set for an adopt decision that has been signed by the AI council."
- *Training and Enablement:* "We deliver the foundational curriculum, the role-based playbooks for a named function, and the specialist-tier bootcamp for a named cohort."
- *Outcome Measurement:* "We evidence the exec scorecard and ad-hoc reads of a specific rollout's outcome, workflow, and usage surface against baselines agreed at pilot time."
- *Incident Support:* "We coordinate the enablement-side of an AI incident — field-signal triage, user communications, rollback, post-incident fold-back — from signal reception to hand-off closure with governance and SecOps."

A request that does not match any of the six predicates is routed out at Monday triage with the specific gap named, not quietly absorbed.

### Field 2 — Inputs the slot requires

Each slot has required inputs the requester must supply before the slot can begin work. The inputs are small but load-bearing. For Tool Selection, the input is: the function, the role population, the workflow step, the baseline evidence that a problem exists. For Pilot Design, the input is: the candidate tool, the signed extend decision, a named operator cohort, and a named sponsor who can evict a laggard pilot. For Rollout, the input is: the signed adopt decision and the maintenance owner. For Training, the input is: the function, the cohort size, and the named partnership with HR / L&D ([Chapter 05](05-the-quarterly-cross-functional-operating-ritual.md)). For Outcome Measurement, the input is: the tool, the baseline, the metric definition from mod-106. For Incident Support, the input is: the signal (field report, usage anomaly, outcome regression, external complaint) and the kill-switch name.

The inputs are what makes an intake form possible (next section). The service-catalog slot does not do the work of producing the inputs; that is the requester's half of the interface. If the requester cannot name the inputs, Monday triage returns the request with "here is what we need from you to accept this" — not a refusal, a precondition.

### Field 3 — Outputs the slot returns

The artefact bundle the slot ships. For Tool Selection, the output is the three-stage decision memo. For Pilot Design, the output is the pilot charter, the baseline, the pilot operating log, and the adopt / extend / kill decision at pilot close. For Rollout, the output is the seven-artefact bundle plus the go-live date. For Training, the output is the curriculum artefact, the delivered sessions, the fluency assessment data. For Outcome Measurement, the output is the scorecard row, the cadence of reads, and the quarterly deep-read memo. For Incident Support, the output is the incident timeline, the user comms log, the post-incident memo, and the fold-back checklist.

Outputs are not deliverables in the project-management sense — they are the specific artefacts that live in the governance evidence store ([mod-110 Chapter 06](../mod-110-commissioning-internal-ai-tools-and-custom-agents/06-signing-surfaces-maintenance-and-handoff-calendar.md) names the same store). The evidence store is the external memory of the CoE; the catalog is the surface that populates it.

### Field 4 — The service-level agreement

Each slot has an SLA — a time commitment for the CoE's response, not a time commitment for the slot's outcome. SLAs are short because they measure the CoE's own discipline, not the organisation's progress through the slot:

- *Tool Selection:* initial triage and three-stage decision within 15 business days of accepted intake.
- *Pilot Design and Operation:* pilot charter within 10 business days of accepted intake; pilot runs to its charter-committed duration.
- *Rollout and the Artefact Set:* artefact set delivered within 25 business days of accepted intake.
- *Training and Enablement:* standing curriculum available on the training surface at all times; cohort-specific session scheduled within 20 business days of the HR/L&D partnership intake.
- *Outcome Measurement:* scorecard refresh weekly; ad-hoc read within 10 business days of the ask.
- *Incident Support:* initial response within 2 business hours of signal reception; incident timeline posted within 24 hours of resolution.

SLAs are not promises the lead negotiates; they are the CoE's standing commitment. The SLA numbers above are indicative — the organisation sets its own on the first operating cycle and adjusts at the quarterly ritual (Chapter 05). What matters is that the numbers exist and are tracked.

### Field 5 — Escalation path

Each slot has a named escalation. If a Tool Selection runs past the SLA, it escalates to the exec sponsor. If a Pilot Design is blocked on a vendor response, it escalates to Procurement. If a Training delivery is blocked on HR partnership, it escalates to the AI council. If an Incident Support slot has crossed into program-level risk, it escalates to `head-of-ai-governance`. The escalation surface is the same surface the Chapter 03 status report routes to when the three questions have an at-risk item.

The escalation path is not a hierarchy; it is a routing rule. A slot without an escalation path is a slot that will stall silently. The lead's job at Monday triage includes naming the escalation path along with the slot assignment.

### Field 6 — Deprecation criterion

A slot that goes six months without a request, or a slot whose outcomes have consistently failed to move the scorecard, is a candidate for deprecation. The deprecation criterion is the specific signal the monthly deep dive ([Chapter 01](01-the-coe-at-steady-state.md)) watches for. Writing the deprecation criterion into the catalog *when the slot is launched* is the discipline that prevents a service catalog from accreting over three years into an unreadable list.

Default deprecation criteria to attach to each slot:

- **Zero demand for two consecutive quarters** → deprecate or absorb into another slot.
- **Two consecutive quarters below the scorecard's outcome target** → re-scope the slot or deprecate.
- **Escalation rate above 25% of routed items for two consecutive quarters** → the slot's scope is wrong; re-author.

## The intake form

The service catalog is read via an intake form. The form is short (12–15 fields) and lives on a channel every operator in the organisation can find — typically the enablement microsite plus a slack intake bot plus an ITSM intake form that mirrors into the CoE queue.

Required fields:

- **Requester** (name, team, BU, function).
- **Slot** the request is targeted at (dropdown of the six).
- **Problem statement** (free text, 300-character max — the form is deliberately not an essay).
- **Workflow step** (what in the current flow is the request targeting; free text).
- **Baseline** (what quantitative evidence do you have that the problem exists; free text or attach).
- **Named sponsor** (the manager who will own the decision-side handoff to the CoE).
- **Existing tool coverage** (has the approved-tool envelope been checked; yes/no plus details).
- **Timeline expectation** (what is the business-side date this needs to land by; free text).
- **Priority flag** (operator, manager, BU head — the signal of urgency the requester carries).
- **Attachments** (any prior analysis, prior pilot, prior memo).

The form's question order is deliberate. The slot dropdown comes second because it forces the requester to pick a scope boundary before writing the problem; this filters requests that are not actually catalog-shaped. The baseline question comes fifth because a request without a baseline usually dissolves on being asked — the requester did not actually have evidence; they had an intuition. Asking at the intake form moves the intuition-to-evidence conversation upstream of the CoE's queue.

An intake form that does not require the baseline field is a form that routes intuitions into the CoE's week. The baseline requirement is non-negotiable.

## How Monday triage reads the catalog

Monday triage ([Chapter 01](01-the-coe-at-steady-state.md)) is where new intake requests are routed. Each request passes through a three-step read:

1. **Does the request match the slot it was filed against?** If yes, accept and route to the slot owner. If the request is misfiled — "this is a selection request but you ticked pilot" — re-slot and accept.
2. **Does the request have all the inputs the slot requires?** If yes, accept with a target completion date. If no, return with a specific input gap named — "we need the baseline data to accept this; here is the template" — and log the return in the decision log (Chapter 03) so the request is not silently dropped.
3. **Is there capacity in the slot for the request this cycle?** If yes, accept. If no, queue with a visible position and target start date; escalate if the queue depth on that slot has crossed the staffing-conversation threshold.

The three-step read is short deliberately. Monday triage is a 30–60 minute meeting, not a working session. Requests that cannot be read in three steps are flagged for the Thursday block or escalated to the quarterly ritual as questions about catalog scope.

## Three catalog anti-patterns and their corrections

Three common anti-patterns are worth naming because they emerge *after* the catalog is published, not before.

### Anti-pattern 1 — "We also do X" accretion

A new ask comes in that doesn't fit any slot. The lead, wanting to be helpful, takes it on informally. Six months later there are eight informal slots the CoE is operating without catalog coverage, and the staffing shape has silently gone underwater.

Correction: Say the words. "That is not in our service catalog as it stands. Here is the path to request a catalog revision at the quarterly ritual; here is the person to talk to in the interim." The catalog's authority is strongest when the lead will defend its edges, not when the lead quietly expands it.

### Anti-pattern 2 — "Just a quick look" bypass

A senior exec slacks the lead directly asking for something that would normally be a Tool Selection slot. The lead, wanting to serve the exec, treats it as off-catalog work. The slot's queue continues to be worked while a shadow work stream runs on exec time.

Correction: Honour the request as a slot entry *and* flag the shadow pattern in the exec scorecard's misses column. The exec's right-to-ask is not in question; the catalog's job is to produce the artefact bundle the exec actually needs. A bypassed catalog produces a conversational answer that cannot be defended at the next council meeting; a honoured catalog produces an evidence artefact that can be.

### Anti-pattern 3 — The catalog page nobody reads

The catalog lives on an enablement microsite. Operators do not read microsites. They slack the lead directly or ask their manager. The catalog becomes CoE-internal documentation, not a public interface.

Correction: The catalog is published *where* the organisation already is — in the HR / L&D learning platform, in the IT self-service portal, in the slack bot that the champion community (Chapter 06) carries. The lead does not expect operators to discover the microsite; the lead ensures the catalog is routed through every surface the operator already uses. A catalog that cannot be found is a catalog that is not operating.

## The relationship to the budget line items

Each slot in the catalog maps to a specific budget line in the enablement cost model from [mod-107 Chapter 01](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/01-the-enablement-cost-model-at-org-scope.md). The mapping makes the catalog budget-defensible:

- Tool Selection, Pilot Design, Rollout → the CoE's own program-operations line (lead + operations analyst time).
- Training and Enablement → the training-production line (curriculum authoring) plus the delivery line (session hours).
- Outcome Measurement → the measurement-instrumentation line (analyst time for scorecard construction, dashboard operation).
- Incident Support → the incident-reserve line (planned slack in the staffing shape to absorb an incident without displacing the rest of the catalog).

When the catalog is re-sized at the quarterly re-read (Chapter 01), the budget line items re-size with it. A slot's demand doubling without the budget line doubling is a pre-committed SLA miss.

## The relationship to the chapters ahead

- [Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md) authors the decision log that records the routing calls the catalog produces, the status report that aggregates the week's slot activity, and the risk register that tracks the slot-level items at risk.
- [Chapter 04](04-vendor-and-external-partner-management.md) names how external vendors and partners (agencies, consultancies, external experts) plug *into* the catalog — slots the vendor can execute against, certification criteria that let the vendor's work meet the enablement bar.
- [Chapter 05](05-the-quarterly-cross-functional-operating-ritual.md) is where the catalog is re-read quarterly against the council, the exec review, and the BU reviews. Catalog revisions happen here, not in Monday triage.
- [Chapter 06](06-the-org-wide-champions-community-of-practice.md) is where the catalog's demand surface is amplified — the community of practice is the field channel that drives new requests into the right slots.

## Summary

- **The service catalog is the CoE's public interface.** It bounds Monday triage, defends the budget, and gives the organisation a durable statement of what the CoE commits to.
- **Six slots:** Tool Selection, Pilot Design and Operation, Rollout and the Artefact Set, Training and Enablement, Outcome Measurement, Incident Support. Each lines up with a prior-module framework; the catalog is the operating surface of the whole track.
- **Each slot specifies six fields:** problem statement the slot accepts, required inputs, returned outputs, SLA on CoE response, escalation path, and a deprecation criterion written at launch time.
- **The intake form is short and baseline-requiring.** The baseline field moves the intuition-to-evidence conversation upstream of the CoE's queue.
- **Monday triage reads each request in three steps:** slot match, input completeness, slot capacity. Queued requests are visible and dated; returned requests are logged in the decision register.
- **Three anti-patterns to catch:** "we also do X" accretion, "just a quick look" bypass, and the catalog-page nobody-reads. Each has a specific correction the lead can take within the operating loop.
