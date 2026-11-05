# The First Ten Minutes to the First Hour

> The incident has crossed into incident territory. The enablement lead has read the signal, confirmed the shape, and is now standing at the beginning of the timeline that produces either a well-handled incident or an incident that reads badly a week later. This chapter is the timeline — the first ten minutes, the first hour, and the first day — of what the enablement side does, and what it hands off. The discipline is not heroic; it is procedural. A hero in the first ten minutes of an AI incident is almost always a role that is about to collapse the boundary.

## The anchor — the enablement lead's three jobs on the clock

Before the timeline, the three jobs ([Chapter 01](01-the-enablement-side-of-the-incident-path.md)) repeated as a clock-side mantra:

- **Convene** the named humans on the escalation ladder.
- **Operate** the kill-switch on authorised call.
- **Communicate** internally within the approved frame.

Every action in the first hour maps to one of the three. If an action does not, it is probably outside the enablement side's scope — pause and check.

## The timeline

### T+0 to T+10 minutes — recognise, preserve, page

The signal has arrived. The enablement lead is often the first operational role on the surface.

**T+0 — recognise the signal shape.**

Confirm which of the four signal sources ([Chapter 01](01-the-enablement-side-of-the-incident-path.md)) the signal is:

- Champion field report tagged `incident-shaped`.
- Usage anomaly on the dashboard.
- Outcome regression on the scorecard.
- External complaint.

The source determines the first-move. In the first ten minutes, the enablement lead should not be classifying *severity*; the classification is the governance side's call. The enablement lead is classifying *source* — a different, faster call.

**T+2 — preserve the primary signal surface.**

Before any communication, capture the signal in its current state:

- The field report with its full narrative, timestamps, and champion identity.
- The dashboard snapshot (screenshot or exported data at the moment of reading).
- The scorecard regression view.
- The external complaint in full (email body with headers, ticket with full thread, letter scanned, public post preserved).

Save to the enablement-side evidence store — a specific location named in the runbook, not an improvised folder. If the organisation has not set up an evidence store, fix that today; this is what was supposed to be on the pre-launch gate.

**T+5 — brief yourself in writing.**

Open the incident log — a timestamped, append-only document owned by the enablement side for the duration of the incident. Write:

- One sentence on what the signal says.
- Which of the four sources it came from.
- The provisional severity read (clearly flagged as provisional).
- The governance-side owner about to be paged.

The incident log is a working artefact, not a finished document. Its purpose is to keep the enablement side's thread clean under pressure and to feed the hand-off packet at the end of the first hour.

**T+7 — page the named governance-side owner.**

From the escalation ladder ([mod-102 Chapter 03 artifact 5](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md)):

- **`head-of-ai-governance` (L60)** is the default primary for program-level, policy-triggered, and external-reaching signals.
- **`ai-risk-engineer` (L25)** is the default primary for engineered-root-cause-shaped signals.
- **SOC** is the default primary for data-exfiltration-shaped signals, credential exposure, or operator-looks-malicious signals.
- **Privacy officer / DPO** is paged in parallel for personal-data signals.
- **General counsel** is paged in parallel for external-surface signals.

The paging uses the channel named on the ladder (phone, dedicated Slack channel, named on-call rotation). The paging message is short: "Signal of shape X has arrived on surface Y. I am preserving evidence. Need you on the thread." Not a pre-committed narrative; a request.

### T+10 to T+30 — confirm the thread, pause the rollout, brief the champion network silently

**T+10 to T+15 — confirm the thread.**

The governance-side owner is on. The enablement lead briefs them with the incident log's four bullet points, hands over the preserved primary signal, and asks two questions:

- Does the governance-side owner want the enablement lead to **operate the kill-switch** (Chapter 02), **hold** (do nothing to the tool while investigation begins), or **take a partial-pull shape** (scope-narrow, feature-disable, rate-limit)?
- Does the governance-side owner want the enablement lead to **brief the champion network silently** (ask champions to pause operator-facing cadence pending guidance) or to **send a specific message** (approved by the governance side) to the champion network?

The enablement lead's provisional read goes in; the governance-side owner decides. The decision and the authorising role are written into the incident log.

**T+15 to T+20 — operate the kill-switch (or do not).**

If the authorising role has called for a pull, execute the runbook from Chapter 02. If a partial pull, execute the specific partial shape. If a hold, do not touch the tool.

Preservation sequencing is a hard rule: vendor-side audit logs, organisational log pipeline, operator-side evidence, and communication surfaces are preserved *before* revocation per Chapter 02 Property 4. If the preservation step blocks the pull by more than a few minutes, the authorising role decides the trade-off; do not improvise.

**T+20 to T+30 — brief the champion network silently.**

Default move for any incident whose scope is not yet known: send a short message to every affected-function champion via the dedicated champion channel.

- "A signal has reached the enablement team on tool X. We are coordinating with governance. **Please pause operator-facing comms on this tool until further notice.** Do not engage substantively with operator questions; direct operators to the help channel. We will update within the next 60 minutes."

The message does not describe the incident. The message does not characterise severity. The message does not promise a timeline. It pauses the standing cadence and buys the governance side time to produce an approved external frame.

If the governance-side owner has approved a specific operator-facing message, that message goes out instead or in addition. The silent-brief is the default; the specific message is the escalation.

### T+30 to T+60 — hand-off packet, exec informational notification, support the investigation

**T+30 to T+45 — assemble the hand-off packet.**

The hand-off packet is the enablement side's finished first-hour product. [Chapter 05](05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md) specifies the contents per downstream role. The packet contains:

- The incident log (append-only, timestamped).
- The preserved primary signal surface.
- The rollout artefact set for the affected tool (use policy, SOP, access playbook, training package, support ladder, champion list, kill-switch runbook — the mod-102 Chapter 03 set).
- The enablement-side evidence pack (operator-side observations, champion context, user population at risk, dashboard baseline before and after the signal).
- The enablement side's **provisional read** — what the enablement lead thinks the signal is, explicitly flagged as provisional and not as a finding.
- The access-list — who on the enablement side has information the downstream investigator may need, with contact details.

The packet is one or two documents, not a scattered set of emails. One place to find everything.

**T+45 — send the exec informational notification.**

Not a substantive briefing; an informational one. The message to the exec sponsor named in [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) is short:

- One sentence: a signal has crossed into incident territory on tool X.
- One sentence: `head-of-ai-governance` is leading the investigation; the enablement side is supporting.
- One sentence: internal operator-facing communications are on pause; the governance side will author the approved message.
- One sentence: the enablement lead will send the first substantive update at a stated time (set by the governance side, not the enablement side).

The exec sponsor's role is sponsorship; they do not run the incident, and they do not need substantive detail before the governance side has produced it. Over-briefing the exec sponsor at T+45 is a specific failure mode — it generates informal expectations (that the exec will be kept current moment-by-moment) that are expensive to meet and that pull the enablement side into a substantive-communications role it does not have.

**T+60 — the handover.**

At T+60, the enablement lead hands the investigation substance to the downstream owners:

- The investigation thread belongs to `head-of-ai-governance` (and, as applicable, the ai-risk-engineer, the SOC, privacy, legal).
- The enablement lead moves into **supporting mode** — standing operations continue under incident governance.

If the ninety-minute mark arrives without a clean handover — the governance-side owner has not accepted the packet, the investigation thread has not been constituted — the enablement lead escalates to the alternate on the escalation ladder. The enablement lead does not absorb the investigation by default.

## Supporting mode — hours 1 to 24

The enablement lead's supporting-mode responsibilities for the first day are the standing operations, now under incident governance.

- **Champion network coordination.** When the governance side produces an approved message, the enablement lead routes it through the champion network. The champion network also surfaces late-arriving field reports; those get preserved and handed to the investigation on the same packet-shaped basis.
- **Help channel operation.** Tier 1 support is running; the operator-facing script is the approved one. Operators asking "is it true that X happened" are told the team is coordinating with governance and will provide an approved update on the stated cadence.
- **Kill-switch readiness** (if a partial pull or a hold was called at T+15). The runbook stays warm for a subsequent full pull if the investigation requires it.
- **Communications-cadence protection.** Any standing rollout cadence slot ([mod-105 Chapter 04](../mod-105-champion-networks-and-change-management/04-the-rollout-communications-cadence.md)) touching the affected tool is paused or revised; the governance side approves the revised content.
- **Preservation of late signals.** New field reports, dashboard shifts, external surfaces that arrive in the first day go through the same T+0 to T+30 sequence, scoped to "this is additional context on the open incident."

The role does **not** start running its own parallel investigation. The temptation is highest at the 24-hour mark, when the governance side has been slow and operators are asking harder questions. The discipline: push the governance side harder on the cadence of their update, do not substitute for it.

## The incident-log discipline

The incident log is the single most important enablement-side artefact in the first hour, and the one most often done poorly. Four rules:

- **Append-only.** A log that gets rewritten to reflect what the enablement lead "now thinks" the signal was is useless to the investigation and dangerous under subsequent legal or regulatory scrutiny. Add new entries; do not revise old ones.
- **Timestamped.** Every entry has a timestamp. Clock skew matters later — use the same source for all entries (either the organisation's authoritative clock or a chosen single device).
- **Observations, not findings.** The log records what the enablement lead saw, what the champion said, what the dashboard showed, what time the governance-side owner was paged. The log does not record what "was happening in the model." That belongs to the ai-risk-engineer.
- **Readable by the investigation.** Written so that the ai-risk-engineer or SOC investigator can pick up the log cold and reconstruct the enablement-side timeline without the enablement lead in the room.

The log ends when the investigation accepts the hand-off packet. The investigation picks up its own log from that point.

## Three common first-hour failures

- **The champion network is spun up too loudly.** The enablement lead broadcasts to all champions with a substantive characterisation of the incident. Champions, trained to be the trusted operator-facing voice, carry the characterisation to operators before the governance side has an approved frame. The organisation's position is now partly authored by champions. **Prevention:** the silent-brief default at T+20 to T+30, with no substantive characterisation.
- **The kill-switch is pulled by the enablement lead unilaterally under self-perceived urgency.** The enablement lead judges the signal severity as high and executes the runbook without the authorising role's call. Property 1 from Chapter 02 is specifically designed to prevent this; the pressure of a live incident tests the discipline. **Prevention:** the role separation is non-negotiable except where the runbook pre-delegates specific criteria in writing.
- **The hand-off packet is not assembled, and the investigation starts from an email thread.** The enablement lead pages the governance-side owner, enters a Slack thread, answers questions ad hoc for an hour, and never consolidates into a packet. The investigation picks up a scattered record; context is lost; the enablement lead becomes the live knowledge carrier and cannot step out of the thread. **Prevention:** the T+30 to T+45 packet assembly is a procedural step, not optional.

## A short decision table for the first hour

| Decision | Who decides | When | Source of truth |
|---|---|---|---|
| Is this a signal or an incident? | Enablement lead (source classification); governance side (severity classification) | T+0 recognition; T+15 confirmation | Signal shape; [Chapter 01](01-the-enablement-side-of-the-incident-path.md) |
| Pull the tool, partial pull, or hold? | Authorising role (per runbook) | T+15 | Kill-switch runbook (Chapter 02) |
| Silent brief or approved message to champions? | Governance-side owner | T+20 | Approved message from governance |
| Notify the exec sponsor? | Enablement lead (informational only) | T+45 | Pre-approved template |
| Who owns the investigation at T+60? | Governance-side primary + specialist peers | T+60 | Escalation ladder |
| Who talks to the external party? | Governance-side owner + legal | Always | Never the enablement lead |

## Summary

- The first hour is procedural, not heroic. Three jobs: convene, operate the kill-switch, communicate internally within the approved frame.
- T+0 to T+10 — recognise, preserve, page. Classify the source (not the severity); preserve the primary signal surface before communication; page the named governance-side owner.
- T+10 to T+30 — confirm the thread, operate the kill-switch (or not), brief the champion network silently.
- T+30 to T+60 — assemble the hand-off packet, send the exec informational notification, hand over the investigation at T+60.
- Supporting mode runs for the first day: champion coordination, help channel, kill-switch readiness, communications-cadence protection, late-signal preservation.
- The incident log is append-only, timestamped, observation-only, and readable by the investigation cold.
- Three common failures: loud champion broadcast, unilateral kill-switch pull, scattered hand-off. Each has a procedural prevention in the timeline.
