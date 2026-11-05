# The Enablement Side of the Incident Path

> An AI rollout surfaces harm. A customer sees an output that should not have been produced. A champion reports an operator who pasted something they should not have pasted. The outcome scorecard turns red on a metric that was trending green last week. A regulator sends an email. In every one of those openings, the enablement lead is often the first role on the signal — not because the role is the incident owner, but because the signal arrived on surfaces the role runs. This chapter draws the boundary the role operates inside: what the enablement side of the incident path is, what it is not, where the signal comes from, who gets paged, and what the role drifts into if the boundary is not held.

## Where the role stands at the moment of the signal

The industry-neutral boundary from [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) and the routing-out discipline from [mod-103 Chapter 07](../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md) already named the shape. The enablement lead **convenes**, **triages**, and **hands off**. The forensic workstream — model forensics, log analysis, vendor-side evidence coordination, regulator-notification-clock management — runs on the governance and security-operations side. [mod-105 Chapter 08](../mod-105-champion-networks-and-change-management/08-the-handoff-to-the-governance-incident-path.md) drew the handoff sequence for signals arriving on the change-management surface. This module picks up the moment after the handoff is initiated and runs the enablement-side thread through the first hour, the rollback, the governance-council brief, and the close-the-loop back into the artifact sets.

The role's authority on the incident path is not investigative. It is three specific things:

- **Convening.** Pulling the named humans from the escalation ladder ([mod-102 Chapter 03, artifact 5](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md)) into a thread inside an SLA.
- **Operational control of the kill-switch.** Executing the rollback runbook authored in [mod-102 Chapter 03, artifact 7](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md), under the authorization criteria that runbook defines. Chapter 02 of this module operationalises the kill-switch.
- **Communication to operators and the champion network** — within the frame the governance-side owner approves. The role is not the external communicator; it is the internal one.

Everything else — root-cause analysis, severity classification, regulator-facing posture, notification-clock management, legal position — belongs to the named owners. The role supports.

## The four signal sources

An enablement-side incident signal arrives through one of four channels. Each has a different shape, a different latency, a different confidence level, and a different first-move.

### 1. Champion field report

A champion from [mod-105 Chapter 03](../mod-105-champion-networks-and-change-management/03-routing-field-signal-back-to-policy-tooling-and-training.md) files a report tagged `incident-shaped`. The six-field schema is live; the tag is the champion's call, not the enablement lead's. The champion has not diagnosed the incident — the tag says *this looks like one*.

**Shape:** a specific, often operator-level event. A paste-mistake. An output that embarrassed the user. A hallucinated recommendation delivered to an external party. A tool answer that contradicts the organisation's policy on something sensitive.

**Latency:** fastest. The champion is the operator's peer; the report lands within hours of the event.

**Confidence:** uneven. The champion is trained to recognise shape, not to adjudicate severity. The report is reliable about *what happened on the floor*, less reliable about *what it means at the program level*.

**First-move:** preserve the full report, confirm the shape with the champion in one short exchange, page the named governance-side owner from the escalation ladder before doing anything else.

### 2. Usage anomaly

The dashboard surfaces from [mod-105 Chapter 07](../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md) or the outcome scorecard from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) show a reading that is not explained by the rollout's steady-state behaviour. Volume spikes in a tool that is approved only for narrow tasks. A sudden surge in sessions outside business hours. Prompt-length distribution shifting in a direction that suggests the tool is being asked to do something it was not pilot-scoped for.

**Shape:** aggregate, inferential. The dashboard is pointing; it has not produced a specific event the enablement side can point to.

**Latency:** slow by comparison. Aggregate signals need a window to emerge; by the time the dashboard shows the shift, operators have already been running into the pattern for days or weeks.

**Confidence:** uneven in the opposite direction. The aggregate shape is reliable; the attribution to a specific *incident* needs evidence that is not yet collected.

**First-move:** do not escalate as an incident yet; open a short investigation on the change-management surface ([mod-105 Chapter 08, point 1](../mod-105-champion-networks-and-change-management/08-the-handoff-to-the-governance-incident-path.md)). Pair with the appropriate champion to pull specific examples. If the specific examples look like incidents, escalate as champion field reports. If they do not, close the investigation as a tooling or training backlog item.

### 3. Outcome regression

The outcome scorecard from mod-106 shows a regression in a metric the rollout is supposed to move — a quality measure, a customer-satisfaction score, a compliance-rate reading — that cannot be explained by seasonality or by a confounding change.

**Shape:** business-outcome shape. The scorecard is saying the rollout is making something worse, not the same or better.

**Latency:** slowest. Outcome metrics have the longest cycle time in the measurement stack; a regression visible on the scorecard has been emerging for one to three reporting periods.

**Confidence:** high on the regression itself, lower on causation. The scorecard owner and the enablement lead run the causation question together.

**First-move:** notify the exec sponsor informationally (not substantively — the regression is not yet an incident), open a causal-investigation thread with the function whose outcome is regressing, pull the ai-risk-engineer (L25) in for a technical-root-cause read, and *then* classify. Some regressions turn out to be change-management problems; some turn out to be incident-shaped (the tool is systematically producing a class of harm) and transition to the full incident path.

### 4. External complaint

A customer, a regulator, a journalist, a counterparty, or a member of the public contacts the organisation with a complaint about the AI tool or its output. The complaint lands at the enablement lead because the tool is enablement-rolled-out and the organisation's routing defaults to "the person who runs the AI program."

**Shape:** external surface. The organisation's position is being read from outside.

**Latency:** varies. A customer complaint arrives within days of the customer-facing event. A regulator query may arrive weeks or months after the underlying event. A journalist may be writing against a deadline.

**Confidence:** complete on the fact that an external party is complaining; unknown on the substance until the organisation investigates.

**First-move:** do not respond externally. Preserve the complaint (full text, timestamps, sender, channel). Page `head-of-ai-governance` (L60) and legal before any substantive exchange. If the complaint is from a regulator, the clock on notification obligations may have started; the enablement lead does not manage that clock but is responsible for not accidentally stopping it with a premature response.

### A summary table of the four

| Source | Shape | Latency | First-move |
|---|---|---|---|
| Champion field report | Specific event | Hours | Preserve, confirm, page escalation ladder |
| Usage anomaly | Aggregate, inferential | Days–weeks | Investigate on change-management surface; escalate if specific events emerge |
| Outcome regression | Business-outcome | 1–3 reporting periods | Notify exec sponsor informationally; open causal investigation; classify |
| External complaint | External, position-reading | Varies | Preserve; do not respond externally; page governance + legal |

## Who gets paged — the escalation ladder refresher

The named humans on the escalation ladder from [mod-102 Chapter 03, artifact 5](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md). This module uses the ladder; it does not re-author it.

- **Tier 1 — the help channel.** Operator-facing. This is where most signals surface in the first place.
- **Tier 2 — enablement.** The enablement lead's team or delegate. Triages the signal into one of the four shapes above.
- **Tier 3 — forks by incident shape:**
  - `head-of-ai-governance` (L60) for program-level incidents, policy-triggered incidents, and anything reaching external-stakeholder surface.
  - `ai-risk-engineer` (L25) for engineered-root-cause signals — unexpected model behaviour, prompt-injection-shaped outputs, guardrail failure, output quality regression attributable to the model or its wrappers.
  - **Security operations (SOC) and DFIR** for data-exfiltration-shaped signals, credential exposure, incidents where operator action appears malicious, or any cross-system compromise.
  - **Privacy officer or DPO** for personal-data-handling incidents — GDPR, HIPAA, FERPA, state privacy law.
  - **General counsel** for anything with external-communication implications, regulator-contact implications, or litigation-adjacent posture.
- **Vendor** — the vendor-side incident contact in the DPA or vendor incident SLA, pulled in by `head-of-ai-governance` or the ai-risk-engineer, not by the enablement lead unilaterally.

The ladder's correctness is what makes the enablement side's paging move fast. A stale ladder on the day of an incident is itself a sub-incident. [Chapter 02](02-the-kill-switch-as-an-operating-artifact.md) treats ladder-freshness as part of the kill-switch runbook's standing obligations.

## The three postures that collapse the role on contact

Under incident pressure, three specific posture failures cause the role to collapse the boundary. Each is a mirror of a drift already named in [mod-103 Chapter 07](../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md); the pressure of a live incident is what makes them most likely.

### Posture 1 — The enablement lead becomes the investigator

The signal arrives. The enablement lead begins pulling logs, asking operators questions about what they did, forming a theory about what went wrong at the model level, and writing a draft root-cause narrative. The governance side gets a briefing that reads as a finished finding.

**Why it happens:** the enablement lead is the fastest-moving role in the room, has the most context from running the rollout, and feels competent to investigate because the surfaces are familiar.

**What goes wrong:** the ai-risk-engineer and the SOC see a case that has been pre-committed to a narrative. Evidence that contradicts the narrative gets quietly discarded. The regulator-facing position is now constrained by what the enablement lead wrote first. The organisational posture becomes "the enablement team handles AI issues," which cannot be defended to a regulator who asks why the ai-risk-engineer or the SOC did not run the investigation.

**The move that stops it:** write **observations**, not **findings**. Describe what the operator did, what the tool produced, what the champion observed. Do not describe what the model "was doing" or why. That belongs to the ai-risk-engineer. The hand-off packet in [Chapter 04](04-the-first-ten-minutes-to-the-first-hour.md) is the artefact that holds this discipline.

### Posture 2 — The enablement lead becomes mute

The signal arrives. The enablement lead escalates cleanly, then goes silent — no champion-network briefing, no cadence update, no kill-switch readiness, no coordination on operator communication. The operators who need information do not get it. The incident narrative is filled by speculation across Slack.

**Why it happens:** the enablement lead reads "hand-off" as "step back," and the governance side has not yet produced approved communications.

**What goes wrong:** the enablement side's standing operating responsibilities — the champion network, the rollout communications cadence — drift during the incident. When the governance side does produce an approved message, there is no primed channel to carry it. The organisation looks disorganised; the operators who matter most do not get the message.

**The move that stops it:** [Chapter 04](04-the-first-ten-minutes-to-the-first-hour.md) names the enablement-side supporting mode explicitly. The role continues to run its standing operations under incident governance; silence is not an option.

### Posture 3 — The enablement lead becomes the spokesperson

The signal arrives, often from the external channel (source type 4). The enablement lead, as the most senior enablement-side role, responds — to the customer, to the regulator, to the journalist, to the exec sponsor asking for a readout. The response contains substantive characterisations of the incident.

**Why it happens:** the external surface is impatient. The enablement lead has access to the information. Someone needs to respond.

**What goes wrong:** every substantive sentence the enablement lead writes to an external party becomes part of the organisation's position on the incident — a position that ought to be authored by general counsel and `head-of-ai-governance` after investigation. The regulator-notification clock may be constrained. The legal posture is compromised. The organisational position is now also owned by a role that does not have the standing to own it.

**The move that stops it:** route external surfaces to general counsel and `head-of-ai-governance` without substantive response. An acknowledgement that the message has been received and routed is not a substantive response; a characterisation of the incident is. Chapter 07 of this module names the governance-council brief shape the enablement lead *does* deliver; external voice belongs to the governance side.

## The signal-to-incident distinction

Not every signal is an incident. A signal may be a change-management problem, a training gap, a tool-fit mismatch, or an operator mistake handled by the ten-minute accident path in [mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md) without rising to the incident surface. The enablement lead's filter at this stage is deliberately biased toward escalation, for two reasons:

- **The cost of a mis-classified incident is asymmetric.** Treating a change-management problem as an incident costs the governance side a few hours of triage. Treating an incident as a change-management problem costs the organisation its regulator relationship if the clock on notification obligations slipped.
- **The filter is not the enablement lead's call alone.** The champion's `incident-shaped` tag, the ai-risk-engineer's technical-root-cause read, the privacy officer's data-class classification, and `head-of-ai-governance`'s program-level read are the roles that collectively decide *this is an incident*. The enablement lead escalates the shape; the escalation surface decides the classification.

What the enablement side is responsible for is the *recognition speed* — spotting the signal early and getting it to the ladder. Over-escalation is cheaper than under-escalation. The role's filter is set accordingly.

## The Chapters ahead

- [Chapter 02](02-the-kill-switch-as-an-operating-artifact.md) operationalises the kill-switch — the mod-102 Artifact 7 runbook as a live piece of machinery, not a paper document.
- [Chapter 03](03-learning-from-the-ai-incident-database-and-oecd-ai.md) grounds the incident-path content in two external precedent surfaces — the AI Incident Database and the OECD.AI AI Incidents Monitor. Reading precedent before the incident is cheaper than reading precedent during one.
- [Chapter 04](04-the-first-ten-minutes-to-the-first-hour.md) walks the first-hour timeline — triage, preservation, paging, kill-switch decision, operator comms, hand-off packet.
- [Chapter 05](05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md) writes the three handoff contracts explicitly — what the enablement lead delivers to each named owner, what each owner delivers back.
- [Chapter 06](06-the-close-the-loop-discipline.md) is the folding-back phase — the confirmed incident becoming policy, training, champion-network, and artifact-set revisions.
- [Chapter 07](07-briefing-the-governance-council-and-supporting-article-73-reporting.md) covers the governance-council brief and the Article 73 serious-incident reporting support posture the enablement lead holds.

## Summary

- The enablement lead stands in the incident path as **convener**, **operational kill-switch controller**, and **internal communicator** — not as investigator, severity-classifier, or external spokesperson.
- Four signal sources land on the enablement side: champion field reports (fastest, specific), usage anomalies (inferential, slow), outcome regressions (business-outcome, slowest), and external complaints (position-reading). Each has a different first-move.
- The escalation ladder from [mod-102 Chapter 03 artifact 5](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) is the paging surface; ladder-freshness is a standing obligation treated in Chapter 02.
- Three posture failures collapse the role under incident pressure: becoming the investigator, becoming mute, becoming the spokesperson. Each has a specific prevention.
- The enablement side's filter at the signal stage is biased toward escalation, because the cost of under-escalation is asymmetric with the cost of over-escalation and because the classification is not the enablement lead's alone to make.
