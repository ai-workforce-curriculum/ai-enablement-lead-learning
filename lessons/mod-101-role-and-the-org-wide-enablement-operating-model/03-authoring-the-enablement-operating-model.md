# Authoring the Enablement Operating Model

> The operating model is the plumbing of the role. Most of the public artifacts — the service catalog, the training calendar, the scorecard — are visible and discussed. The plumbing underneath — intake path, decision rights, funding, staffing shape — is usually invisible and therefore undesigned. Design it on purpose.

## What "operating model" means here

An operating model is the set of recurring mechanisms that turn a strategy into a weekly routine. For AI enablement, four things have to be designed and written down:

1. **Intake path** — how a request moves from an employee or a team into the CoE and out again.
2. **Decision rights** — who decides what, when CoE / BU / governance / security all touch the same request.
3. **Funding model** — how the work is paid for and what that signals.
4. **Staffing shape and service catalog** — the roles inside the CoE and the services they publish.

If any of these four is undefined, you will spend your week refereeing requests instead of running the program. The point of writing them down is not bureaucracy; it is to stop re-deciding.

## Intake path

Intake is the single biggest determinant of whether the CoE feels useful or obstructive. Three paths need design:

### The employee intake (the long tail)

A single employee has an AI question or a use-case idea. They should hit one front door — a form, a chatbot, a dedicated channel — not six. The front door routes to one of a small set of outcomes:

- **Self-serve.** "You can do that with the approved tool at this link, here is the one-page playbook."
- **Office hours.** "Bring it to Thursday office hours; we'll pair with you."
- **Training.** "This is covered in the Level 1 literacy curriculum; here is the next cohort."
- **Champion routing.** "The champion for your BU is X; they handle this."
- **New-use-case intake.** "This is a new use case; we're opening an intake ticket and the rollout process starts here."

The design goal: 80%+ of the long-tail traffic resolves at the first four outcomes and never becomes an intake ticket. If every request becomes a ticket, you will drown.

### The new-use-case intake (the pilot pipeline)

A team wants to pilot a new use case or new tool. This is heavier. It has steps — problem framing, data-handling check with governance, security review, pilot design, decision criteria, pilot run, decision — that correspond to [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md). The operating-model piece is the *cadence*: a weekly intake triage where the CoE lead and the governance partner review new tickets, say yes / no / wait, and assign the next step to a named owner.

### The incident intake (the fast lane)

Something a rollout surfaced is harming people. This is a different queue with a different SLA — same-day triage, kill-switch authority on the CoE lead, parallel notification to governance and security. The incident path is covered in [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md); here, the operating-model piece is making sure the fast lane exists and is visibly separate from the pilot pipeline, so nothing waits in a weekly queue when it should not.

## Decision rights — the four-way intersection

Four parties routinely touch an AI request: the CoE (you), the BU (the requester or their leader), governance (program, policy), and security (data, DLP, access). Without written decision rights, every non-trivial decision becomes a meeting with eight people.

Write a short decision-rights table. One row per recurring decision. Columns for CoE / BU / Governance / Security, each marked **Decide** (D), **Approve** (A), **Consult** (C), or **Inform** (I). Keep it short — ten to fifteen rows covers 95% of the real decisions.

A rough starting set:

| Decision | CoE | BU | Governance | Security |
|---|---|---|---|---|
| Add tool to approved-tool envelope for pilot | D | C | A | A |
| Add tool to approved-tool envelope for general use | C | I | D | A |
| Approve a pilot use case | D | C | C | C |
| Approve rollout of a piloted use case | D | A | C | C |
| Pull kill switch on a rollout | D | I | I | I |
| Revise acceptable-use policy | C | I | D | C |
| Revise data-handling SOP for AI | C | I | D | C |
| Approve a new champion | D | A | I | I |
| Revise the training curriculum | D | C | I | I |
| Publish the executive scorecard | D | I | C | C |
| Open an AI incident ticket | D | I | A | A |
| Escalate an incident to legal / regulator | C | I | D | C |

This is a starting set, not the right set for your organization. The goal is to have *a* table that is signed by all four parties before the first real decision tests it. Updating the table after the first hard case is normal; discovering that the table doesn't exist in the middle of the first hard case is bad.

## Funding model

Who pays for the CoE signals what the CoE is. Three options, in order of market prevalence:

**Central funding (corporate or CIO/CAIO budget).** The CoE is free at point of use. Demand is unbounded. Teams do not have to prioritize. Advantage: no friction in adoption. Disadvantage: no demand-side signal, and the CoE can be cut in the next cycle because nobody paid for it.

**BU charge-back.** BUs are billed for the CoE services they consume. Advantage: BUs prioritize; the CoE can prove revenue and defend its headcount. Disadvantage: the overhead of charge-back usually exceeds the demand-signal benefit for the first two years; also, the services most important to the organization (policy, training, incident response) are the hardest to bill for.

**Hybrid.** Central funding for the shared infrastructure (policy, training production, measurement, incident response, champion network). BU funding for spokes and for commissioned builds. This is the most common structure at mature hub-and-spoke programs.

Pick the funding model deliberately, write it in the operating-model doc, and revisit it annually. An unfunded CoE is a hobby; an over-metered CoE will not get the pilot traffic it needs to be useful.

## Staffing shape

The staffing shape follows the CoE pattern choice from Chapter 02. For a mid-size enterprise running hub-and-spoke, a realistic starting shape:

- **AI Enablement Lead (you)** — level 45. Operating-model design, exec reporting, policy co-authoring, service-catalog ownership.
- **Training & Curriculum Lead** — owns the AI literacy curriculum, role-based playbooks, cohort delivery. Often a senior L&D person with AI fluency.
- **Change & Champion Network Lead** — owns the champion program, change communications, adoption measurement. Often a senior change management person (Prosci-certified is a market signal).
- **Embedded Enablement Partners (one per BU)** — the spokes. Run their BU's local adoption, feed field signal upward, surface shadow AI.
- **Operations Analyst** — runs the scorecard, maintains the service catalog, triages intake, handles the vendor-management touchpoints that don't need the lead.
- **(Optional) Internal Tool Commissioner** — covered in [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md). Owns commissioning briefs for internal agents. Often started as a fractional role, graduated to a dedicated role as the commissioned portfolio grows.

For a hub shape, same roles without the spokes. For a federated shape, the lead and the operations analyst plus a vendor-management partner, and the training / change / champion work sits inside BUs instead of at the center.

Do not staff all of this in the first quarter. The first-quarter shape is usually you, one training person (part-time or borrowed from L&D), and one operations analyst. The rest is sequenced over the first year.

## The service catalog

The service catalog is the external-facing menu of what the CoE offers. Most of the organization never reads the operating model; they read the service catalog. Keep it short and specific:

- **For individuals:** approved-tool list and access, Level 1 literacy curriculum (self-paced), role-based playbooks (by function), office hours, prompt-coaching clinic.
- **For teams:** team-adoption kit, team-manager playbook, use-case workshop, champion nomination path.
- **For BUs:** embedded enablement partner (if hub-and-spoke), BU-level rollout planning, BU-level scorecard template, executive-briefing template.
- **For functions (legal, security, privacy, finance, HR):** co-authored policy artifacts, intake-questionnaire support, policy-change notification cadence.
- **For the executive office:** monthly executive scorecard, quarterly board-ready review, budget & ROI narrative, incident briefings.

Version the catalog. When something is added, mark it *new*. When something is retired (the half-run program nobody uses), mark it *sunset: 2027-Q1* three months before pulling it. A catalog that only grows is a catalog that will collapse under its own weight.

## Writing the operating-model document

The operating-model document is one artifact — usually four to eight pages — that ties the four pieces together: intake path, decision rights, funding, staffing + catalog. It should be the sort of document a new hire into the CoE reads on day one and has a workable mental model of the whole job by lunch.

It is not the *public* artifact — the scope contract (Chapter 01), the service catalog, and the scorecard face outward. The operating-model doc is for the CoE itself and for the executives funding it.

## Summary

- Design four things on purpose: intake path, decision rights, funding model, staffing + service catalog.
- Intake has three queues: long-tail employee, new-use-case pilot, incident. Each has a different cadence and SLA.
- Decision rights are a short written table against four parties — CoE / BU / Governance / Security — signed before the first hard decision tests it.
- Funding is deliberate: central, charge-back, or hybrid — and you choose with your eyes open.
- Staffing shape follows the CoE pattern from Chapter 02 and is sequenced over the first year, not hired in the first quarter.
- The service catalog is the organization-facing summary of everything above; version it and retire what nobody uses.
