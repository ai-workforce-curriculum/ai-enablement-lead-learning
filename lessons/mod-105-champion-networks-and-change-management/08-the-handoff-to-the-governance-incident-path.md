# The Handoff to the Governance-Owned Incident Path

> The enablement side of the house is where signals that will become incidents first become visible. The enablement side is *not* where incidents get run. This chapter is the short, load-bearing one on how the enablement lead coordinates the handoff — when a signal from the champion network, the resistance survey, or the operations dashboard crosses into incident territory and must leave the change-management operating surface and enter the governance-owned incident path.

## Why this chapter is short

The full incident-response treatment lives in [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md). That module owns the forensic depth, the regulator-notification clock, the serious-incident reporting path, the hand-off to `ai-risk-engineer` L25 for engineered root-cause. This chapter owns one specific question: **how does the change-management surface recognise that a signal needs to leave this module and move to that one, and what does the handoff look like?**

Four points to make, and no more. Length is a correctness discipline here — a long chapter would start duplicating mod-109's content.

## Point 1 — Three triggers from the change-management surface

An incident-path handoff is triggered when the enablement-side surface produces one of three specific signals:

- **A field report tagged `incident-shaped`.** The champion's field-report schema from [Chapter 03](03-routing-field-signal-back-to-policy-tooling-and-training.md) has an `incident-shaped` option in the signal-type field. The tag is explicitly named so champions can use it without diagnosis — the champion does not need to decide *whether* it is an incident; they only need to recognise that it looks like one.
- **A dashboard combined-signal read from [Chapter 07](07-measuring-change-management-health.md).** The adoption-up / quality-skepticism-rising combination is the most common; the quality-skepticism-high / specific-tool-failing read on the survey is another. The dashboard itself does not escalate; the enablement lead reviewing the dashboard escalates based on the signal shape.
- **An external surface** — a customer complaint, a regulator query, a press mention, a legal hold notice — arriving at the enablement lead because the tool is enablement-rolled-out, even though the incident surface is not an internal field report. These get the same handoff; the signal shape is just upstream.

The three triggers share a property: they are all on *the enablement lead's* reading surface. The job is to recognise the trigger quickly and hand off cleanly, not to investigate.

## Point 2 — What "handoff" means operationally

Handoff is a specific sequence, not a notification. It has four steps, in order.

### Step 1 — Preserve the signal

Before the enablement lead passes anything to governance, the signal gets preserved — the field report is captured with its full narrative, the dashboard snapshot is saved, the external surface (email, screenshot, ticket) is recorded with timestamps. [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) treats the preservation surface in depth; the slice here is that *the enablement lead does not wait* for governance to run preservation — the primary signal is captured inside the enablement side's own systems first.

### Step 2 — Notify the named path

A named human on the governance side is notified. Depending on signal shape:

- **`head-of-ai-governance` L60** for program-level incidents, policy-triggered incidents, and anything reaching external-stakeholder surface.
- **`ai-risk-engineer` L25** for engineered-root-cause signals — unexpected model behaviour, prompt-injection-shaped outputs, guardrail failure.
- **Security operations** (SOC) for data-exfiltration-shaped signal, credential exposure, or incidents where the operator action appears malicious.
- **Privacy** for personal-data-handling incidents.

The notification uses the escalation ladder from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) — the one with names, not role titles. If the ladder has gone stale since the rollout, the enablement lead has a stale-ladder problem, which is itself a point of failure.

### Step 3 — Transfer the facts, not the ownership

The enablement lead provides the governance-side owner with:

- The signal in full — the field report, the dashboard snapshot, the external surface.
- The context — which tool, which function, which rollout version, which champion.
- The enablement-side provisional read — what the enablement lead thinks the signal is, flagged as provisional.
- The access — to the rollout artifact set, the champion, the affected operator (through the champion).

The enablement lead *does not*:

- Conduct the forensic investigation.
- Communicate with the operator about the incident substance (the governance side decides when and how to engage the operator directly).
- Issue public statements or send cadence content about the incident ahead of the governance-side communications decision.
- Brief the exec sponsor on the substance of the incident ahead of the governance side; informational notification is fine, substantive briefing is not.

The co-author posture from [mod-103 Chapter 01](../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md) matters here — the enablement lead co-authors policy, but does not co-conduct incidents. The handoff is a transfer of ownership, not a shared ownership.

### Step 4 — Enter the enablement-side supporting mode

Once the incident is in the governance-owned path, the enablement lead moves into a supporting role. Three things the enablement side does well and should do while the incident is live:

- **Coordinate the champion network's response.** If the incident is specific to one function, the champion for that function is briefed with what the governance side has approved for communication. If the incident is organization-wide, the champion network becomes the first-line answer surface for operator questions.
- **Operate the kill-switch and rollback plan** from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) if the incident requires rollback. The mod-102 artifact names *who authorises*; the enablement lead executes with IT identity.
- **Protect the communications cadence.** The incident may require a specific cadence send; the communications discipline from [Chapter 04](04-the-rollout-communications-cadence.md) is the surface. Internal comms is in the room.

What the enablement lead does *not* do: engineer the root cause, author the regulator-facing notification, decide the severity classification, run the forensic depth. Those live in mod-109.

## Point 3 — Close-the-loop back to the change-management surface

An incident that goes through mod-109 produces a post-incident report. The enablement side is a primary audience for that report; the content comes back into this module's operating surface in specific ways.

- **Policy backlog.** Confirmed incidents often produce policy changes; these flow through the walking-redline backlog from [mod-103 Chapter 01](../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md). The champion whose report triggered the escalation is credited in the redline log.
- **Tooling backlog.** If the incident surfaced a tool-level problem, the tool's position in the approved-tool envelope ([mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md)) may change — demoted, restricted, or removed.
- **Training content.** The incident becomes a case in the use-case library — not for operators generally, but for the specialist and champion curricula. [mod-104 Chapter 04](../mod-104-training-programs-and-ai-literacy-curriculum/04-role-based-playbooks-and-use-case-libraries.md) treats the library; the specific incident content lives in the specialist-tier content, not operator-tier.
- **Cadence Slot 3.** A redacted, consent-reviewed version of the incident goes into the "what is working *and* what is not" slot of the quarterly cadence — the honest cadence discipline from [Chapter 04](04-the-rollout-communications-cadence.md). Not all incidents are communicated externally; the ones that are, are reported honestly.
- **Dashboard baseline.** The incident often produces a shift in one of the four health signals from [Chapter 07](07-measuring-change-management-health.md). The dashboard baselines are reset where appropriate.

The through-line: every incident the enablement side handed off should be visible in the change-management surface three months later as something that changed. If not — if the loop did not close — the organization did not learn.

## Point 4 — The three failure modes at the boundary

Three ways the handoff goes wrong, each with a specific cause.

- **The enablement lead holds the incident.** The signal came in; the enablement lead investigated, issued a fix, and did not escalate. Cause: either the trigger definition was unclear or the enablement lead did not recognise the signal shape. Impact: governance did not see the incident; the organizational posture became "the enablement team handles AI issues," which the governance side cannot defend to the regulator. **Prevention:** the field-report `incident-shaped` tag is *the champion's call*, not the enablement lead's; the enablement lead's filter is biased toward escalation, not toward containment.
- **The handoff is a notification, not a transfer.** The enablement lead emails `head-of-ai-governance`, moves on, does not preserve the signal or transfer the facts. The governance side starts cold. Impact: slower response, missing context, often re-interviewed champions. **Prevention:** the four-step sequence above is a procedure, not an email template.
- **The enablement side becomes mute during the incident.** The handoff happens cleanly, then the enablement lead goes silent — no champion briefing, no cadence update, no kill-switch readiness. The operators who need information do not get it. Impact: narrative vacuum fills with speculation. **Prevention:** step 4 (supporting mode) is explicit; the enablement side continues to run its standing operations, with content governed by the incident owner.

Each of the three has a mirror in the resistance patterns from [Chapter 06](06-ai-specific-resistance-patterns-adkar-and-kotter.md). A handoff failure is also a change-management failure — it shows up in the next quarter's resistance survey as "the program was not honest about X."

## A short decision table

| You see | Who gets it first | What you do in the first 30 minutes |
|---|---|---|
| Field report tagged `incident-shaped` | `head-of-ai-governance` (plus `ai-risk-engineer` if engineered-root-cause shape) | Preserve the report; notify named; transfer facts; coordinate champion silence pending guidance |
| Dashboard adoption-up / skepticism-rising | `ai-risk-engineer`, as a watch-item; `head-of-ai-governance` informational | Investigate on the change-management surface; escalate if a specific incident shape emerges |
| External surface (customer complaint, regulator query) | `head-of-ai-governance` (always); legal (usually); SOC (if data-shaped) | Preserve the surface; notify; do not respond externally until governance approves |
| Champion reports operator pasted customer data into off-envelope tool | `head-of-ai-governance` and SOC; privacy if PII | Preserve; notify; trigger ten-minute accident path from [mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md) |
| Confirmed harm to a specific person surfaces | `head-of-ai-governance` (always and immediately); legal | Preserve; notify; move to supporting mode immediately |

The table is a starting shape, not the final word. [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) treats the full taxonomy.

## Where this chapter feeds

- [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) is where this chapter hands off completely; read it next in the track order.
- [mod-103 Chapter 07](../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md) treats the broader routing-out discipline of which this handoff is a specific case.
- [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) is where the kill-switch and escalation ladder this chapter uses were authored.
- Exercise 06's change-management health dashboard includes the incident-signal surface as part of the dashboard design.

## Summary

- Three triggers on the change-management surface: `incident-shaped` field report, combined-signal dashboard read, external surface arriving at the enablement lead.
- Handoff is a four-step sequence: preserve the signal, notify the named governance-side owner, transfer the facts, enter the enablement-side supporting mode. It is not an email.
- The enablement lead does not conduct the investigation, communicate substance to the operator, brief the exec sponsor on substance ahead of governance, or author external notifications. All of that is mod-109.
- Close the loop back into the change-management surface: policy backlog, tooling backlog, training content, cadence Slot 3, dashboard baselines. If none of these changed three months on, the organization did not learn.
- Three failure modes at the boundary — enablement holds the incident, handoff is a notification not a transfer, enablement goes mute — each have a specific prevention in the procedure.
