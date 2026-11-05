# The CoE at Steady State — The Operating Loop That Keeps the Enablement Program Running

> Nine modules deep, the role has selected tools, co-authored policy, built a training curriculum, run a champion network, authored an executive scorecard, defended a budget, flavoured the program for an industry, run incident response, and commissioned an internal build. Each of those modules named one surface of the role. This module is the operating loop that runs all of them *at the same time*, week in and week out, without the lead burning out and without the program collapsing into theatre. The CoE is not a thing you built in mod-101 and then left running; it is the standing operating cadence this chapter formalises.

## Why "steady state" is the right word

The CoE pattern family was chosen in [mod-101 Chapter 02](../mod-101-role-and-the-org-wide-enablement-operating-model/02-the-ai-coe-pattern-family.md) — hub, hub-and-spoke, federated, or embedded. The operating model was authored in [mod-101 Chapter 03](../mod-101-role-and-the-org-wide-enablement-operating-model/03-authoring-the-enablement-operating-model.md) — intake path, decision rights, funding model, staffing shape, service catalog. Up until this point the material has focused on **standing up** each piece. Steady-state operation is the other half of the problem: how does the CoE keep running six months after launch, when the founding exec sponsor has moved to a new rotation, when the first cohort of champions is retiring, when three overlapping copilot pilots are in flight, when Finance is asking why the mid-year burn is above plan, and when a BU head wants to know why their rollout is behind the headline one?

Steady state is the state where the CoE is **not news**. The founding story is over. The service catalog is published. The intake queue has a queue depth. The scorecard is a running report, not a launch deck. R15 (0.35, cross-functional program management, prereq-level in the sample) is the shape of competence this state calls for: the lead is running a program, not launching one.

The failure mode at steady state is different from the failure mode at launch. Launch failures are visible — the training package doesn't ship, the pilot has no baseline, the champion network has no field signal. Steady-state failures are quiet. The intake queue grows faster than the CoE can triage. The decision log falls behind and decisions are being made in slack. The risk register has the same six items as six months ago. The exec scorecard loses credibility because last quarter's miss has no owner this quarter. The CoE is still there, but it is no longer *operating* — it is reacting.

This chapter is the operating loop that prevents that drift. The remaining chapters of the module name the specific instruments the loop runs on.

## The three questions a CoE at steady state has to answer every week

Three questions make the CoE legible to the executives funding it and to the BU leaders consuming its services:

1. **What is in flight?** The portfolio of tool selections, pilots, rollouts, incidents, commissions, and policy edits under active CoE work this week.
2. **What is blocked?** The items that cannot move without a decision, a resource, a vendor response, or a cross-functional alignment call.
3. **What is at risk?** The items on the scorecard, the risk register, or the incident queue whose current trajectory does not get to the expected outcome without intervention.

The three questions are the skeleton of the weekly status report (Chapter 03) and of the monthly rollup that feeds the exec scorecard ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md)). A CoE that cannot answer all three in writing by Friday afternoon has stopped operating and started firefighting.

The questions are deliberately scoped to the CoE's operating surface, not to the enterprise AI story. *What is the enterprise doing with AI* is the chief-ai-officer's question (level 70, deferred up in [`CURRICULUM.md`](../../CURRICULUM.md)). *What is the governance program covering* is the head-of-ai-governance's question (level 60, co-owned at the council in Chapter 05). *What is the engineering team shipping* is the ai-engineering-manager's question. The lead's three questions are specific to the enablement operating system — the intake, the service catalog, the decision log, the scorecard, the vendor portfolio, the champion community.

## The weekly operating loop

The CoE runs on a weekly loop regardless of the pattern family chosen in [mod-101 Chapter 02](../mod-101-role-and-the-org-wide-enablement-operating-model/02-the-ai-coe-pattern-family.md). The loop's cadence does not change with the pattern; what changes is who sits in which meeting. The loop:

### Monday — Intake triage (30–60 minutes)

The intake queue (Chapter 02, the service catalog) is reviewed in a standing 30–60 minute meeting. Every new request in the queue gets routed to one of six service-catalog slots or is returned to the requester with a specific gap named. The decision log (Chapter 03) records the routing. The service catalog does not grow on Monday — Monday is where incoming demand is bounded against standing capacity. The outcomes of Monday:

- Requests routed to a service-catalog slot with a named owner and an expected next touch date.
- Requests returned to the requester with a specific gap named, filed in the decision log so the request is not silently dropped.
- Requests escalated to the AI council (Chapter 05) because they cross a threshold the CoE cannot decide alone — a budget ask above the delegated ceiling, a policy question the governance side has to rule on, a BU-level scope conflict.

### Tuesday–Wednesday — Service delivery

The bulk of the CoE's working time. The lead is holding the discipline across the service catalog slots; the CoE team members (`ai-governance-analyst` partnerships at [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md), embedded enablement partners if the funding model supports them) are executing against the routed work.

Standing Tuesday–Wednesday surfaces:

- **Office hours for operators.** A recurring block on the CoE calendar that operators can walk into without an appointment. Field signal flows from this block into the champion community (Chapter 06) and into the field-report pipeline from [mod-105 Chapter 03](../mod-105-champion-networks-and-change-management/03-routing-field-signal-back-to-policy-tooling-and-training.md).
- **Partner stand-ups.** Short co-working sessions with the functional partnerships named in Chapter 05 (HR, L&D, IT, legal, security, procurement, finance) — the specific partner on the agenda rotates week-to-week.
- **Pilot and rollout check-ins.** The gate-forward reviews on in-flight tool selections from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md), scored on the three-cadence measurement plan ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md)).

### Thursday — Status writing and risk-register review

The lead is at the desk writing. The three questions (what is in flight / blocked / at risk) are answered against the week's evidence. The risk register (Chapter 03) is updated — closed items closed, new items opened, open items re-aged. The scorecard misses-first discipline from [mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) is applied to the status report before the report leaves the lead's hands.

Thursday is also where the lead re-reads the previous week's decision log and confirms the decisions that were due for a follow-up have had one. A decision made on Monday and never re-touched is the shape of the quiet failure mode named above.

### Friday — External face

Status report ships to the exec sponsor, the AI council chair (`head-of-ai-governance`), and the CAIO if one is in place. The service-catalog view updates for the organisation. The champion community (Chapter 06) gets the week's cross-team lesson post. The CoE goes dark for the weekend.

The "external face" is the deliberate boundary between the operating loop and the people the operating loop serves. If the lead is answering slack messages into Friday evening, the operating loop has broken and Monday's intake triage will be reacting to leakage from the week it was supposed to close.

## The monthly, quarterly, and semi-annual overlays

The weekly loop is the base layer. Four overlays run against it:

### Monthly — Deep dive on one service-catalog slot

Each month, one of the six service-catalog slots (selection, pilot, rollout, training, measurement, incident support) gets a deep review. In a six-month rotation, every slot has been reviewed inside a half year. The deep review looks at:

- **Demand shape.** How many requests landed in this slot in the last six months? What is the trend?
- **Throughput.** Of the requests routed into the slot, how many closed, how many are still open, how long have the open ones been open?
- **Outcome.** For closed items, what did the scorecard record? Are the outcome metrics (mod-106 framework) moving in the direction the service was supposed to move them?
- **Escalation pattern.** Where did items leave this slot for a different surface (council, exec review, incident path)? Is the escalation pattern stable, trending up, trending down?

The monthly deep dive is what prevents a service-catalog slot from quietly rotting. A slot with zero demand for three months is a signal to deprecate, not a signal to wait. A slot with growing demand and flat throughput is a signal to staff, not a signal to apologise.

### Quarterly — The cross-functional operating ritual

Chapter 05 is the full treatment. At cadence level: once a quarter, the AI council convenes with the governance side (`head-of-ai-governance`, `senior-ai-governance-architect`), the executive leadership team reviews the program (the CAIO if present, the exec sponsor otherwise), the BU leaders review their slice of the portfolio, and the functional partnerships (HR, L&D, IT, legal, security, procurement, finance) renew their partnership contracts for the next quarter. The quarterly ritual is where the operating loop becomes defensible to the wider organisation.

### Quarterly — The budget and build-vs-buy re-read

[mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md) is the full treatment. At cadence level: once a quarter, the lead walks the cost model and the four-column build-vs-buy matrix against the last quarter's evidence. New vendor products that have entered the market, vendor products that have been repriced, internal commissions ([mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md)) that have landed in acceptance or retirement, and shifts in the rollout evidence that change which column a given use case belongs in.

### Semi-annual — Champion network intake and retirement

[mod-105 Chapter 02](../mod-105-champion-networks-and-change-management/02-the-four-phase-lifecycle-recruit-train-recognise-retire.md) names the four-phase lifecycle at team and function level. At CoE level, the semi-annual cadence is where the aggregate champion network is re-sized — intake class sized against the quarterly rollout plan, retirement cohort released on schedule, community-of-practice membership refreshed (Chapter 06).

## The shape of the CoE team at steady state

The staffing shape named in [mod-101 Chapter 03](../mod-101-role-and-the-org-wide-enablement-operating-model/03-authoring-the-enablement-operating-model.md) runs the operating loop above. At steady state the shape stabilises on a small team with a defined boundary:

- **The enablement lead (this role, level 45).** Owns the three weekly questions. Writes the status report. Chairs the quarterly ritual. Holds the service catalog's shape.
- **An operations analyst** (often an `ai-governance-analyst` on the governance side with a dotted line to the CoE at level 15 per [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md)). Runs the intake queue, maintains the decision log, instruments the service-catalog throughput dashboard, keeps the risk register current.
- **Embedded enablement partners** if the pattern family is hub-and-spoke or federated. One per large BU, with a matrixed reporting line into the BU's leadership and a dotted line into the CoE. They run the local rollout, train the local champions, feed BU-specific field signal back into the hub.
- **Shared service contracts with HR / L&D, IT, legal / security / privacy, procurement / finance.** Not CoE headcount, but named counterparts whose partnership contract (Chapter 05) obligates specific service against the operating loop.

The shape is lean deliberately. A CoE that staffs to its peak demand in the first year is over-scoped at steady state and under-scoped during incidents. The right discipline is the opposite: staff to the steady state, surge to the peaks with vendors ([Chapter 04](04-vendor-and-external-partner-management.md)) and with champion-community pull (Chapter 06).

## When the loop breaks — the three diagnosable failure modes

Three failure modes are the most common at steady state. Each is diagnosable from the operating loop itself, not from a satisfaction survey:

### Failure mode 1 — The intake queue grows faster than Monday triage

Symptom: Monday triage keeps being deferred to Tuesday, then Wednesday, then not held at all. The queue grows. The lead's week starts with a backlog of two-week-old requests.

Diagnosis: Demand has exceeded capacity, or the service catalog has silently expanded past the staffing shape. A service catalog slot has been added without a corresponding owner. An existing slot is receiving requests it was never scoped for.

Correction: Either bound demand (return requests that do not fit the catalog's scope with a specific gap named) or expand capacity (add an embedded enablement partner for the BU driving most of the demand). Do not expand the catalog without expanding the staffing. The surface for this correction is the monthly deep dive.

### Failure mode 2 — The decision log stops being written

Symptom: Decisions are being made, but they are being made in slack, in hallway conversations, in exec one-on-ones. The log file has not been updated in two weeks. When a BU head asks "why did the CoE choose that vendor for the triage rollout?" the lead has to remember instead of citing.

Diagnosis: The lead is firefighting. The Thursday status-writing block has been eaten by Monday–Wednesday reactions.

Correction: Protect Thursday. If the Thursday block cannot survive the week, something earlier in the week is wrong — probably an under-scoped service-catalog slot or an unstaffed BU demand. The log is the forcing function; losing the log is the leading indicator that the operating loop is failing.

### Failure mode 3 — The risk register has the same items it had six months ago

Symptom: The risk register is updated weekly, but the open items are the same six or eight items. None of them have moved to mitigation, none have been closed, none have been escalated. The register has become wallpaper.

Diagnosis: The risk register's role in the operating loop has drifted from *tracking* to *performing*. The items on it are no longer live; they are inherited from a prior cycle.

Correction: Rebase the register. In a single Thursday block, close every item that is no longer live, escalate every item that has been standing for a quarter without progress, and name two new items from the current evidence. A register that does not change is not a risk register; it is a trophy case.

## The relationship to the chapters ahead

The weekly loop above is the frame. The rest of this module fills in the instruments:

- [Chapter 02](02-the-service-catalog-as-the-coes-public-interface.md) authors the service catalog in operational depth — the six slots, the intake form, the SLA per slot, and the deprecation discipline.
- [Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md) names the three instruments the operating loop runs on in writing — decision log, status report, risk register — and the formats that keep them defensible.
- [Chapter 04](04-vendor-and-external-partner-management.md) treats the vendor and external-partner surface — screening, training, certification, and the quarterly vendor review that keeps the external portfolio honest.
- [Chapter 05](05-the-quarterly-cross-functional-operating-ritual.md) authors the quarterly ritual — AI council, exec review, BU reviews, functional partnerships.
- [Chapter 06](06-the-org-wide-champions-community-of-practice.md) names the community-of-practice layer that sits above the per-team champion networks owned by `ai-augmented-team-manager` (level 40).
- [Chapter 07](07-the-credentials-portfolio-as-shared-vocabulary.md) positions the credentials portfolio that is the role's shared vocabulary across all of the above.

## Summary

- **Steady state is the state where the CoE is not news.** The founding story is over; the service catalog is published; the lead is running a program, not launching one. R15's program-management posture is what the shape calls for.
- **Three weekly questions anchor the operating loop:** what is in flight, what is blocked, what is at risk. A CoE that cannot answer all three in writing by Friday afternoon has stopped operating.
- **The weekly loop is Monday intake, Tuesday–Wednesday delivery, Thursday writing, Friday external face.** Overlays run monthly (deep dive on one service-catalog slot), quarterly (cross-functional ritual, budget re-read), and semi-annually (champion network intake and retirement).
- **The CoE team is lean deliberately.** Lead, operations analyst, embedded BU partners where the pattern calls for them, and shared-service contracts with the functional partners. Surge capacity comes from vendors and the champion community, not from headcount.
- **Three failure modes signal that the operating loop has broken:** the intake queue grows faster than Monday triage can close; the decision log stops being written; the risk register ossifies. Each has a specific correction in the operating loop itself, not in a reorg.
