# The Intake Questionnaire

> The questionnaire is a schema the architect designs and a runner the enablement side operates. Confusing the two is the most common lateral drift in the role — the one where a well-intentioned enablement lead spends a quarter redesigning fields and controls that were not theirs to redesign, then realizes the taxonomy underneath has shifted and the audit story has to be rebuilt.

## What the intake questionnaire is

The intake questionnaire is the artifact every new AI-tool request fills in to enter the governance workflow. It converts "my BU wants a tool" into a structured decision packet the governance council can act on. In mod-103 it is artifact 3 of the enablement-side policy triad (acceptable-use policy, data-handling SOP, intake questionnaire). In [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md), the output of a completed intake is one of the inputs to the Stage 2 candidate-evaluation gate. In [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md), it is the intake for internally-commissioned agents, not only vendor tools.

The questionnaire has two separable layers — the **schema** and the **runner** — and the whole chapter hangs on keeping them separate.

## The schema vs. the runner

### Schema is architect territory

The **schema** of the questionnaire is:

- What fields exist.
- What values each field can take.
- How field values feed the organization's risk-classification scheme.
- How the classification output maps to controls in the control library.
- How evidence collected via the questionnaire maps to NIST AI RMF GOVERN categories, ISO/IEC 42001 clauses, and (in EU-touching orgs) EU AI Act obligations.

This is the work of `senior-ai-governance-architect` (L50), supported by `ai-risk-engineer` (L25) for engineered-risk content and `ai-governance-analyst` (L15) for the ongoing field maintenance. The schema is architecture — it survives personnel changes, it plugs into the audit story over years, it is the stable surface governance evidences against.

**You do not redesign the schema.** The temptation to do so is strong once you have run intake for a few quarters and you start noticing patterns. The right move for a pattern is to surface it as evidence (see "The co-authoring beat on schema" below) — not to rewrite the field.

### Runner is enablement territory

The **runner** role is the enablement lead's work:

- Standing up the submission interface operators actually fill out.
- Pre-filling what you already know (tool identity, vendor, envelope status) so requesters are not retyping what the operating model already has.
- Chasing laggards whose submissions have stalled in partial state.
- Flagging incomplete or incoherent submissions to governance.
- Routing completed submissions to the council agenda.
- Closing the loop with the requester after the council decides.

The runner role is operational — it keeps the schema's intent alive in day-to-day use.

Confusion between the two is the drift. A healthy enablement lead can operate the runner at scale without touching the schema; an unhealthy one begins to "fix" fields that are inconvenient to collect, and the audit story quietly breaks.

## Typical fields covered

These are the field groupings a well-designed intake questionnaire usually contains. Treat the list as **orientation** — the specific field set at your organization is schema (architect-owned) and will differ. The groupings themselves are relatively stable across organizations:

- **Tool identity.** Vendor, product name, product version, deployment model (SaaS multi-tenant, SaaS single-tenant, on-prem, hybrid), hosting jurisdiction.
- **Requester and business justification.** Who is asking (BU, function, named sponsor at `ai-augmented-team-manager` L40 level or above), for what target task, under what success criterion, with what alternatives already considered.
- **Data classes touched.** Inputs the tool receives, outputs the tool produces, training data the vendor uses or does not use, logging data the vendor retains. Map to the organization's classification scheme — the same scheme the AUP and data-handling SOP reference.
- **External disclosure.** Whether the tool's output reaches customers, partners, the public, regulators, or data subjects. Whether the tool's input includes data the organization received from those parties under confidentiality obligations.
- **Cohort size and reach.** Named populations, sized. Role mix. Geography (which matters for jurisdiction and for AI Act scope).
- **Risk-classification prompt inputs.** The questions whose answers feed the architect's risk schema — for example, whether the tool makes or supports a decision, whether a human reviews output before use, whether the task sits in a regulated domain. You collect the inputs; you do not propose the classification.
- **Envelope check.** Whether the tool is already in the approved-tooling envelope ([mod-102 Chapter 01 / Stage 2](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md)). If it is, much of the policy, DPA, SSO, and security review work has already been done; if it is not, the envelope-admission workstream runs in parallel with intake.
- **Policy touchpoints.** Which AUP sections and which data-handling SOP sections may need revision because of this tool. This is the field where the enablement-side reading shows up explicitly — often as "no new revisions required" and occasionally as "AUP section 3 may need an added approved use; propose at next walking redline."

Each grouping maps to one or more controls in the architect's library. The mapping is architect-owned.

## The pre-review session — the preempt against formality

The most common failure of an intake questionnaire is that it fills out as a formality instead of as a decision input. Fields get filled with "see attached" or "standard"; the risk-classification inputs get rubber-stamped; the resulting packet gives the council nothing to act on.

**Preempt with a 20-minute pre-review session.** Before the requester submits, sit with them for twenty minutes and walk the questionnaire. Your job during that session is:

- Reality-check the business justification — is this a real problem, or a budget line looking for a justification?
- Map the actual task and data classes, not the sanitized ones.
- Surface the policy touchpoints the requester would not notice on their own.
- Run the envelope check in the session, not as a follow-up.

The session is also the first opportunity to reshape the request if the current framing is going to land the tool in a classification that makes the rollout infeasible. Doing that reshaping *before* submission is cheap; doing it *after* council decline is expensive.

Pre-review sessions are a cost. They are the cost that makes intake useful.

## The feedback loop to the council

Completed questionnaires are what populate the AI governance council agenda — [Chapter 02](02-the-governance-council-liaison-seat.md)'s Job 1 (feed the intake workflow) is this chapter's output in the next week's council. Status tags move items through the pipeline:

- `pre-intake` → `intake-in-progress` → `schema-complete` → `awaiting-council-decision` → `council-approved` / `council-declined` / `council-deferred`.

Items that linger in any status for more than a cycle or two become your action item. Do not let the queue silently grow.

## The co-authoring beat on schema

Though you do not redesign the schema, you do contribute to it through a disciplined feedback cycle. Each cycle (quarter is typical), produce a short memo to `senior-ai-governance-architect` with:

- **Field evidence** — specific submissions where the current field set was insufficient, ambiguous, or systematically mis-filled. Named, with the submission references.
- **A proposed refinement** — framed as the architect's decision, not as a redesign. "Propose adding a sub-field for human-review gating, because over the last cycle, five of twelve submissions in regulated-domain tasks could not be classified without asking the requester for clarification." Not: "Here is the redesigned field."
- **Costs and benefits** — what changes would need to flow through if the refinement were adopted. Which training materials. Which policy clauses. Which existing classifications would be revisited.

The memo lands at the architect's door. The architect decides. If the refinement is accepted, the next schema version drops; the enablement side updates the runner side (submission interface, pre-review script, champion briefings) to match. Exercise 03 drills this memo.

## Where the chapter boundaries lie

- The questionnaire's **runner** operation is this role's. Chapter 02's Job 1 is where the output is used.
- The questionnaire's **schema** is `senior-ai-governance-architect`. [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) covers the discipline of routing architecture work out.
- The questionnaire's **classification output** is ratified by `head-of-ai-governance`; the engineered-risk inputs come from `ai-risk-engineer`. You collect inputs; you do not classify.

## Summary

- The intake questionnaire is a schema (architect-owned) and a runner (enablement-owned). Keep them separate; drifting into schema design is the most common lateral error in the role.
- Typical field groupings: tool identity, requester and business justification, data classes touched, external disclosure, cohort size and reach, risk-classification prompt inputs, envelope check, policy touchpoints. Specific fields are architect-defined; the groupings are relatively stable.
- The 20-minute pre-review session is the preempt against formality — do it before submission, not after decline.
- Status-tagged pipeline (`pre-intake` → `council-decided`) is what you bring to each council meeting. See [Chapter 02](02-the-governance-council-liaison-seat.md).
- The co-authoring beat on schema is a cyclic evidence memo to `senior-ai-governance-architect`, framed as architect-decides. Exercise 03 drills it.
- The questionnaire is a living artifact — update the runner side to match every schema revision in the same cycle, or the two drift and intake stops resolving cleanly.
