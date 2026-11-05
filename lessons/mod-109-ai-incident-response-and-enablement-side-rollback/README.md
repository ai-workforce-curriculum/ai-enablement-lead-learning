# mod-109 — AI Incident Response and Enablement-Side Rollback

**Estimated effort:** 10 hours
**Role level:** 45 · **Family:** AI Workforce

This is the module where everything the preceding eight modules authored — the rollout artifact set from mod-102, the policy stack from mod-103, the training curriculum from mod-104, the champion network from mod-105, the scorecard from mod-106 — meets contact with harm. A rollout surfaces an incident. The enablement lead is often the first role on the signal, because the signal arrives through a champion field report, an outcome regression on the scorecard, a usage anomaly in the dashboard, or an external complaint that was routed to "the person running the AI rollout." The role's job at that moment is not to run the incident. The role's job is to **coordinate the enablement side** of the incident — preserve the signal, flip the kill-switch from the mod-102 artifact set, communicate to operators without pre-empting governance, hand off to `ai-risk-engineer` (L25) on engineered root cause, to `head-of-ai-governance` (L60) on program-level escalation, to security operations and DFIR on the SOC-side forensic workstream, and to fold the confirmed incident back into the artifact sets so the next rollout learns.

The hand-off discipline from [mod-103 Chapter 07](../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md) and the trigger-to-handoff shape from [mod-105 Chapter 08](../mod-105-champion-networks-and-change-management/08-the-handoff-to-the-governance-incident-path.md) set up the boundary. This module operates on the other side of that boundary — what happens once the signal has crossed into incident territory and the enablement lead is coordinating the first hour.

## Learning objectives

- Design the enablement-side incident path — what the enablement lead handles when a rollout surfaces harm, where the signal came from (champion field report, usage anomaly, outcome regression, external complaint), who gets paged, what the kill-switch looks like.
- Operate the rollback plan authored in [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) — flip the kill-switch, communicate to users, preserve evidence, hand to governance and SecOps — grounded in the AI Incident Database and the OECD.AI AI Incidents Monitor as precedents the enablement side has learned from.
- Hand off to `ai-risk-engineer` (peer, L25) on engineered root cause, to `head-of-ai-governance` (L60) on program-level escalation, and to security operations / DFIR on SOC-side investigation — the enablement lead coordinates, not conducts, the engineered forensics.
- Fold confirmed incidents back into the mod-102 rollout-artifact set, mod-103 policy, mod-104 training content, and mod-105 champion-network priorities — closing the loop so the next rollout learns.
- Brief the governance council and (for EU AI Act high-risk systems) support Article 73 serious-incident reporting without authoring it directly — authoring belongs to the governance / risk-engineering side.

## Lecture chapters

1. [The Enablement Side of the Incident Path](01-the-enablement-side-of-the-incident-path.md) — the boundary the role operates inside, the four signal sources, who gets paged, and the three postures that collapse the role on contact.
2. [The Kill-Switch as an Operating Artifact](02-the-kill-switch-as-an-operating-artifact.md) — operationalising the mod-102 Artifact 7 runbook, the five-field authorization criteria, the revocation sequence, user-visible state during rollback, and evidence preservation.
3. [Learning from the AI Incident Database and OECD.AI](03-learning-from-the-ai-incident-database-and-oecd-ai.md) — precedent at the right altitude; reading AIID and the OECD.AI AI Incidents Monitor for enablement-side lessons without catastrophising.
4. [The First Ten Minutes to the First Hour](04-the-first-ten-minutes-to-the-first-hour.md) — the enablement-side timeline: triage, preservation, paging, kill-switch decision, operator communications, the hand-off packet.
5. [Handoff Contracts — AI Risk Engineer, Head of Governance, SecOps and DFIR](05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md) — three named handoff contracts and the distinction between enablement-side coordination and engineered forensics.
6. [The Close-the-Loop Discipline](06-the-close-the-loop-discipline.md) — folding confirmed incidents back into the mod-102 artifact set, mod-103 policy, mod-104 training content, and mod-105 champion-network priorities.
7. [Briefing the Governance Council and Supporting Article 73 Reporting](07-briefing-the-governance-council-and-supporting-article-73-reporting.md) — the council brief the enablement lead delivers, and the Article 73 serious-incident reporting path the enablement lead supports but does not author.

## Exercises

Exercises 01 through 04 are a running thread against a single rollout the learner picks in Exercise 01. The artifact bundle produced across the four is coherent and worth keeping as a reference bundle.

1. [Enablement-Side Incident Triage Drill](exercises/exercise-01-enablement-side-incident-triage-drill.md) — walk four signals from the four source types through the triage-and-paging sequence; produce a triage log and a first-hour timeline.
2. [Kill-Switch and Rollback Dry Run](exercises/exercise-02-kill-switch-and-rollback-dry-run.md) — operationalise the mod-102 Artifact 7 against the same rollout; produce the runbook, the user-visible state plan, and the dry-run script.
3. [Handoff Contract with AI Risk Engineer and SecOps](exercises/exercise-03-handoff-contract-with-ai-risk-engineer-and-secops.md) — author the three handoff contracts (risk engineer, head of governance, SOC/DFIR) with the hand-off packet template and the clock-definition for each.
4. [Incident-to-Policy-and-Training Feedback Loop](exercises/exercise-04-incident-to-policy-training-feedback-loop.md) — take a plausible confirmed incident from Exercises 01–03 and author the close-the-loop artifacts into mod-102/103/104/105.

## Labs and quizzes

Lab and quiz prompts land in `labs/` and `quizzes/` on subsequent content cycles.

## Resources

External references: [`resources.md`](resources.md).

## How this module connects to the rest of the track

- Takes from [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md): the kill-switch and rollback plan from [Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) (artifact 7) and the support-and-escalation ladder (artifact 5) are the operating surfaces this module runs.
- Takes from [mod-103](../mod-103-policy-co-authoring-with-governance/README.md): the ten-minute accident path from [Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md) is the SOP the operator runs; the routing-out discipline from [Chapter 07](../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md) is the frame that holds the role in scope under incident pressure.
- Takes from [mod-105](../mod-105-champion-networks-and-change-management/README.md): the four-step handoff sequence from [Chapter 08](../mod-105-champion-networks-and-change-management/08-the-handoff-to-the-governance-incident-path.md) is the shape this module extends into the first hour and beyond.
- Feeds back into [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md): confirmed incidents revise the artifact set, the approved-tooling envelope, and the kill-switch runbook.
- Feeds back into [mod-103](../mod-103-policy-co-authoring-with-governance/README.md): confirmed incidents enter the walking-redline backlog as policy amendments.
- Feeds back into [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md): confirmed incidents enter the specialist-tier use-case library and update the operator-tier training where role-shaped lessons apply.
- Feeds back into [mod-105](../mod-105-champion-networks-and-change-management/README.md): confirmed incidents shift champion-network priorities — the function whose champion surfaced the signal gets recognition, the function whose rollout generated the incident gets a focused cadence slot.
- Feeds [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md): the incident-signal surface on the executive scorecard is populated from this module's close-the-loop output.
- Feeds [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md): commissioned internal tools and custom agents run the same incident path, with the enablement lead often closer to the engineering team on root cause.
- Feeds [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md): the incident-response cadence and the governance-council incident brief are recurring CoE operating rituals.
