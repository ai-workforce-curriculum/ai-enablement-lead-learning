# Exercise 01 — CoE Service Catalog and Intake Cadence

**Estimated effort:** 2 hours
**Format:** service catalog document + intake form specification + Monday-triage routing rules, Markdown
**Grounding chapters:** [01 — The CoE at Steady State](../01-the-coe-at-steady-state.md); [02 — The Service Catalog as the CoE's Public Interface](../02-the-service-catalog-as-the-coes-public-interface.md). Prior reading: [mod-101 Chapter 03](../../mod-101-role-and-the-org-wide-enablement-operating-model/03-authoring-the-enablement-operating-model.md); [mod-102 Chapter 03](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md); [mod-107 Chapter 01](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/01-the-enablement-cost-model-at-org-scope.md).

## Objective

Author the service catalog, the baseline-requiring intake form, and the Monday-triage routing rules that let a CoE operate the weekly loop from Chapter 01. The output is a bundle a new embedded enablement partner could pick up on their first day and use to accept, route, or return intake requests without ambiguity.

You will carry one chosen organisation across Exercises 01–04 — so pick deliberately. Exercise 05 is personal and runs against your own trajectory, not the organisation's.

## Prerequisites

- Chapters 01 and 02 read.
- [mod-101 Chapter 03](../../mod-101-role-and-the-org-wide-enablement-operating-model/03-authoring-the-enablement-operating-model.md) read as the upstream operating-model authoring.
- [mod-102 Chapter 03](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) read as the artefact bundle the Rollout slot delivers.
- [mod-107 Chapter 01](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/01-the-enablement-cost-model-at-org-scope.md) read as the cost model the catalog slots map to.
- A chosen organisation — **you will carry this across Exercises 01–04**. If you do not have one in mind, pick one of:
  - A 4,000-person professional-services consultancy running a federated CoE pattern — one hub team at HQ plus embedded enablement partners in the four largest practice areas, with high consultant / contractor density.
  - An 8,000-person regional health system running a hub-and-spoke CoE pattern — one central CoE serving the hospital-group corporate centre plus five regional spoke leads embedded in large hospitals, all under HIPAA.
  - A 12,000-person bank running a federated CoE pattern — enterprise CoE at corporate plus BU-embedded leads in retail banking, commercial lending, wealth management, and risk, all under SR 11-7 model-risk-management framing.
  - A 2,500-person ed-tech vendor running a hub CoE pattern — one central team serving all functions, with K-12 regulation (FERPA, COPPA) framing the data-handling posture.

## Problem statement

The CoE's founding story has closed. The service catalog is ready for first publication. Your three weekly questions ([Chapter 01](../01-the-coe-at-steady-state.md)) have to answer themselves against the catalog you are about to author. If an operator submits an intake request on Monday morning, Monday triage has to be able to route, return, or queue the request in under 15 minutes.

Write the catalog as if it ships to the whole organisation this Friday. Treat the embedded enablement partners (if the pattern family carries them) as readers who will operate the catalog from Monday onwards with no additional conversation from you.

## Requirements

### Part A — The service catalog document

A single Markdown document with the six catalog slots at operating depth. For each of the six slots:

1. **Problem statement the slot accepts** — one sentence predicate, written at the altitude from [Chapter 02](../02-the-service-catalog-as-the-coes-public-interface.md). Specific enough that a requester can self-assess whether their ask is in scope.
2. **Inputs the slot requires** — the specific precondition artefacts the requester must supply.
3. **Outputs the slot returns** — the specific artefact bundle, named at the altitude of the governance evidence store.
4. **SLA on CoE response** — the business-day commitment. Calibrate against the organisation's size and staffing shape; do not import the chapter's defaults uncritically.
5. **Escalation path** — the specific named surface (exec sponsor, AI council, Procurement, `head-of-ai-governance`) a slipping item routes to.
6. **Deprecation criterion** — the specific signal that would trigger deprecation review at the monthly deep dive.

Open the catalog document with a one-paragraph preface naming:

- The CoE pattern family in use (from mod-101 Chapter 02).
- The current staffing shape (lead + operations analyst + any embedded partners).
- The budget line each slot maps to (from mod-107 Chapter 01).
- The governance evidence store the catalog's output artefacts land in.

### Part B — The intake form specification

A Markdown specification for the intake form the organisation reads the catalog through. Required:

- **The 12–15 required fields.** For each field, name the field label, the field type (text, dropdown, numeric, attachment), the character limit if any, and the validation rule.
- **The dropdown value lists.** For "slot targeted at," list the six values. For "named sponsor," specify the field requires a role that can be looked up in the HR directory.
- **The baseline-requiring field.** Specifically name the baseline field, its required inputs, and its validation. A form that accepts an empty baseline is a form that routes intuitions into the CoE's queue — this field is non-negotiable.
- **The surface(s) the form is published on** — HR / L&D platform, IT self-service portal, enablement microsite, slack intake bot. Name the specific surfaces the chosen organisation would use.
- **A sample completed form.** Three example submissions — one well-formed and in-catalog; one well-formed but that should be returned at Monday triage with a specific input gap; one misfiled against the wrong slot that should be re-slotted and accepted.

### Part C — The Monday-triage routing rules

A one-page decision tree that an embedded enablement partner (or the operations analyst in the lead's absence) can follow to triage each request. Required:

- **The three-step read** from [Chapter 02](../02-the-service-catalog-as-the-coes-public-interface.md) made explicit as sequential if-then branches.
- **The decision-log entry template** that each triage decision produces — slot assigned, owner named, next-touch date, review date if time-sensitive.
- **The specific wording for a return-with-gap-named response** when the request lacks an input. Boilerplate the requester receives via the intake form's reply; three variants, one each for missing baseline, missing named sponsor, missing existing-tool-coverage check.
- **The escalation rules** for a request that does not fit any slot — who the triage operator contacts, how the escalation is logged.

## Starter guidance

- The hardest part is the Section 3 Rollout and the Artefact Set slot's deprecation criterion. Deprecating a rollout slot sounds wrong at first — rollouts are perennial. But a rollout *of a specific tool* can be deprecated when the tool is retired. Think about the deprecation criterion at the slot-shape level, not the tool-shape level.
- The baseline field in the intake form is where you will get pushback. Requesters will want to submit without a baseline. The field is non-negotiable; attach a short "how to produce a baseline" one-pager as a linked resource in the form itself, so the requester has a path forward rather than a closed door.
- The embedded enablement partner reader is the persona to write to. If the chosen organisation's pattern family does not carry embedded partners, substitute "the operations analyst on their first week" — same discipline, same clarity requirement.
- For the consultancy and bank options, an unusually dense consultant / contractor layer complicates Field 7 of the intake form (existing tool coverage). Read the question in those scenarios as "has the approved-tool envelope been checked *for internal staff*, and separately for consultant / contractor use."
- Where an organisational fact you need is unknown (specific budget-line numbers, specific role-title names, specific baseline data), use `<!-- needs-research: ... -->` inline. Do not invent numbers.

## Deliverables

- `service-catalog.md` — the six-slot catalog with preface and per-slot six-field specifications.
- `intake-form.md` — the field specification, dropdown lists, surface list, and three sample submissions.
- `monday-triage-rules.md` — the three-step routing decision tree, the decision-log entry template, the return-with-gap boilerplate variants, and the escalation rules.
- A short cover note (3–5 sentences) summarising the slot you found hardest to specify and the one you expect to produce the most intake volume in year one.

## Acceptance criteria

- All six slots are specified across all six fields; no field is TBD.
- The intake form requires a baseline field with explicit validation rules.
- Each slot's SLA is dated in business days (not "a few days" or "roughly a week"); each slot's escalation path names a specific role or named surface.
- Each slot's deprecation criterion is a specific, measurable signal — zero demand for N quarters, or N consecutive quarters below target, or escalation rate above N%.
- The Monday-triage decision tree produces a decision-log entry for every input request, including requests that are returned.
- The three sample submissions cover one accepted, one returned-with-gap, and one re-slotted. Each submission includes the triage operator's reasoning in a comment.
- `<!-- needs-research: ... -->` is used wherever an organisational fact is missing. No invented numbers.
- The cover note names the hardest slot and the highest-volume slot with one sentence of reasoning each.

## Stretch goals

- **Add a slot-level staffing worksheet** showing, for each slot, the FTE hours per quarter the SLA commits to, mapped to the staffing shape. The worksheet is the answer to "can the CoE actually deliver what the catalog promises."
- **Author a deprecation case** — pick one slot and walk the deprecation path from signal detection through AI council sign-off through catalog revision. Three pages. This is the stretch work that turns the deprecation criterion from a promise into an operating artefact.
- **Produce a sixty-second pitch** — a two-paragraph text the enablement lead can use when an exec sponsor asks "what is the CoE for" at a corridor conversation. The pitch cites the catalog as the answer, not the lead's role.

## Why this exercise matters

The catalog is the interface the organisation reads the CoE through. Everything in the mod-101 operating-model authoring either shows up on the catalog or does not exist in the organisation's lived experience. The quality of the catalog determines whether Monday triage is a routing decision or a negotiation, whether the weekly status report has shape, and whether the CoE's budget is defensible against the enablement cost model. Producing the catalog, the intake form, and the triage rules under a two-hour budget is calibration for producing them under live-launch pressure, when the organisation's first intake requests are landing in real time.
