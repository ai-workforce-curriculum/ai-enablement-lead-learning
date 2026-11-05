# The Close-the-Loop Discipline

> A confirmed incident produces a write-up. The write-up names what happened, what caused it, and what should change. The write-up is governance-owned. The *changes it produces* flow back through the enablement side's artefact set — the mod-102 rollout artifact set, the mod-103 policy stack, the mod-104 training curriculum, the mod-105 champion network. This chapter is the discipline for making the loop close. An incident that does not revise an artifact three months later was not learned from; it was survived.

## Why the loop so often does not close

The incident is over. The downstream owners have produced their findings. The governance council has been briefed. Operators are back on the tool (or not). The enablement lead's inbox is full of other work.

Three forces pull against closing the loop:

- **Incident-fatigue.** The enablement lead ran the first hour, the first day, the two-week supporting mode. The appetite for picking up the write-up on day 15 is low.
- **Ownership-fog.** The downstream owners' write-up may not specify which artefacts the enablement side should revise. The governance side authorises revision but does not author it; the enablement side is responsible for authoring but has not been given a specific scope.
- **Prioritisation-pressure.** The next rollout is already running; the next policy redline cycle is already queued. Revising the artefact set for a closed incident feels like retrospective work in a forward-only role.

The close-the-loop discipline is specifically designed to fight the three forces. It is a procedure, scheduled on a cadence, with a named owner (the enablement lead) and named deliverables (per-artefact revisions). The procedure does not depend on the enablement lead's continuing interest in the incident.

## The five surfaces to fold back into

An incident touches, at most, five surfaces the enablement side owns. Not all five on every incident. The enablement lead reads the incident write-up against each surface, decides whether the surface needs revision, and names the revision.

### Surface 1 — The mod-102 rollout artifact set

The seven artefacts from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md):

- **Use policy.** If the incident exposed a use case that was ambiguous, under-specified, or missing from the policy, the policy revises.
- **Data-handling SOP.** If the incident involved a data class the SOP did not name or a procedural gap in the ten-minute accident path, the SOP revises.
- **Access & offboarding playbook.** If the incident involved a leaver or a transfer whose access should have been revoked and was not, the playbook revises.
- **Training package.** Covered under Surface 4 below.
- **Support & escalation path.** If the escalation ladder was slow, stale, or missing a named contact, the ladder revises.
- **Champion list.** Covered under Surface 5 below.
- **Kill-switch & rollback plan.** If the runbook failed on contact — stale ladder, undiscovered order dependency, destroyed evidence — the runbook revises. [Chapter 02](02-the-kill-switch-as-an-operating-artifact.md) Property 6 names the per-incident revision as a standing cadence trigger.

The approved-tooling envelope position may also shift — the tool may be demoted, restricted, removed, or kept with new conditions. The envelope-position change is itself an artefact revision that routes through governance co-sign.

### Surface 2 — The mod-103 policy stack

The one-page AUP, the data-handling SOP, and the intake questionnaire from [mod-103](../mod-103-policy-co-authoring-with-governance/README.md). Overlaps with Surface 1 but is treated separately because the policy revisions flow through the walking-redline cycle with the governance co-author ([mod-103 Chapter 01](../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md)). Specifically:

- The AUP's approved-use list may narrow (removing the use case the incident exposed) or expand (adding a specific prohibition the operator's action revealed as needed).
- The SOP's data-class list may add a class, revise a handling rule, or add a step to the accident path.
- The intake questionnaire's schema may surface an evidence gap — a question the questionnaire should have asked and did not. Evidence-shaped memos go to `senior-ai-governance-architect` (L50) per [mod-103 Chapter 06](../mod-103-policy-co-authoring-with-governance/06-the-intake-questionnaire.md); the enablement lead does not propose schema redesigns, only surfaces the evidence.

### Surface 3 — The mod-104 training content

Training content is the operator's pre-incident relationship with the policy. An incident whose root cause includes "the operator did not know the policy" is not only a policy problem — it is also a training problem. From [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md):

- **Operator-tier content** revises if the incident surfaced a lesson that all operators of the tool should know. The revision is small — adding or revising a specific module, scenario, or attestation item.
- **Specialist-tier content and use-case library** revises more extensively. Specialists and champions should know the incident at a detailed level, so they can recognise the shape when it recurs on their function.
- **Role-based sub-tiers** in regulated industries may need regulated-role-specific revisions (a clinician-tier revision if the incident involved PHI; a registered-representative-tier revision if the incident involved a FINRA-governed communication).

Not all incidents become training content. The filter: the incident is included when the lesson generalises (the next operator in this role, under similar conditions, might make the same mistake). Not when the lesson is operator-specific (a known-individual failure that is a performance-management matter).

### Surface 4 — The mod-105 champion-network priorities

The champion network is the organisation's distributed sensing surface for AI incidents. An incident reshapes champion priorities:

- **Recognition of the champion whose report surfaced the incident.** From [mod-105 Chapter 02](../mod-105-champion-networks-and-change-management/02-the-four-phase-lifecycle-recruit-train-recognise-retire.md). The champion takes an operational hit in surfacing an incident; the recognition is explicit and visible.
- **Focused briefing for the function whose rollout generated the incident.** The function's champion gets a direct brief; the function's cadence slot is populated with the honest treatment from [mod-105 Chapter 04 Slot 3](../mod-105-champion-networks-and-change-management/04-the-rollout-communications-cadence.md).
- **Champion-training content update.** The champion bootcamp's case library adds the incident at the specialist-tier depth; new champions learn the incident as part of onboarding.
- **Cross-function awareness message.** Where the incident has lessons for other functions (another function uses the same tool differently and should be warned), champions across those functions get a brief through the champion channel.

The champion network is not an investigative surface. The enablement lead does not direct champions to go find more instances of the incident — that is the ai-risk-engineer's or the SOC's call. Champions are given the recognition and the training; they surface additional evidence organically.

### Surface 5 — The mod-106 executive scorecard

The outcome scorecard from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) has a slot — often small, sometimes a dedicated surface — for incident signals. The close-the-loop output populates that slot: confirmed incidents in the reporting period, revisions the incidents produced, close-the-loop-completion status.

The scorecard reporting is governance-authored (the honest treatment is governance's voice, not the enablement side's) and enablement-supported. The enablement lead provides the evidence; `head-of-ai-governance` decides the framing.

## The close-the-loop cadence

The procedure that makes the five surfaces revise on schedule.

### Step 1 — Post-incident review, enablement-side slice

Within one week of the incident write-up being finalised, the enablement lead runs a 60-minute post-incident review focused on the enablement-side slice. Attendees: enablement lead, `head-of-ai-governance`, `ai-risk-engineer`, SOC liaison (as applicable), privacy officer (as applicable), general counsel (as applicable), the IT identity lead (if the kill-switch ran).

The agenda has four items:

- Walk the incident timeline from the enablement-side log. What worked; what did not.
- Walk each of the five surfaces above. Which revise; which do not.
- Name the revision owner for each surface that revises. Default owner is the enablement lead; some revisions co-own.
- Set the revision window for each revision — short (within two weeks), standard (within four weeks), long (next scheduled artefact cycle).

Exit the meeting with a one-page revision plan.

### Step 2 — Draft the revisions

The enablement lead drafts the artefact revisions in the revision window. Each revision follows the usual co-authoring surface for its artefact:

- AUP and SOP revisions go through the walking-redline cycle from [mod-103 Chapter 01](../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md).
- Training content revisions go through the L&D partnership from [mod-104 Chapter 08](../mod-104-training-programs-and-ai-literacy-curriculum/08-partnering-with-hr-ld-and-internal-comms.md).
- Champion-network changes go through the standing champion cadence from [mod-105](../mod-105-champion-networks-and-change-management/README.md).
- Kill-switch runbook revisions are signed by the enablement lead, `head-of-ai-governance`, and IT identity.

The redline log from mod-103 Chapter 01 is the audit trail. Each revision is tagged to the incident ID; a reader three years later can trace from an AUP clause back to the specific incident that produced it.

### Step 3 — Ratify the revisions

Ratification runs through the co-author surfaces named above. The enablement lead does not sign the revisions alone; the co-signing surfaces apply.

### Step 4 — Communicate the revisions

Operators learn the revised policy through the standing cadence from [mod-105 Chapter 04](../mod-105-champion-networks-and-change-management/04-the-rollout-communications-cadence.md); specialists learn through the specialist-tier curriculum update; champions learn through the champion channel; the governance council sees the revisions on the next council read-ahead.

Do not pretend the revisions are disconnected from the incident. The honest-slot from mod-105 Chapter 04 is the surface where the organisation says "here is what happened, here is what we revised, here is why." A revision that is unexplained reads as an arbitrary rule and is less likely to stick.

### Step 5 — Verify the revisions three months on

At the three-month mark, the enablement lead verifies that each revision is live:

- The AUP revision is in the published policy and operators are being trained on it.
- The SOP revision is in the published SOP.
- The training module is in the curriculum and completion is being tracked.
- The champion network has the revised brief.
- The scorecard reflects the incident and the revisions.
- The kill-switch runbook is updated and the ladder is current.

If any revision is not live, the enablement lead investigates why — authoring delay, co-signing delay, delivery delay — and escalates on the appropriate cadence. The three-month check is a specific anti-drift mechanism; without it, revisions silently decay.

## When the loop does not call for a revision

Not every incident revises every surface. Four shapes of incident that typically do not touch all five surfaces:

- **An operator-specific incident with no generalisable lesson.** A known-individual failure, handled through performance management. Training may not revise. Policy may not revise.
- **A vendor-caused incident where the vendor has remediated and the deploying organisation's artefacts were correct.** The organisation may add a vendor-coordination note to the runbook; other artefacts may not revise. The decision on whether to keep the vendor in the approved envelope is governance's.
- **An external complaint that was investigated and found to be unsupported.** No artefact revision; the incident log is closed with the finding, and the external communication (if any) is governance-authored.
- **A dashboard anomaly that resolved on its own with no specific operator event.** The dashboard baselines may reset; artefacts generally do not revise.

The post-incident review's agenda item 2 ("walk each of the five surfaces; which revise; which do not") is where these calls happen. Deciding *not* to revise is a legitimate outcome; the review documents it and the loop still closes.

## The loop-closure audit trail

One subtle discipline: the close-the-loop artifact trail is often the primary evidence a regulator or auditor reads when asking "what has your organisation learned from its AI incidents?" The trail has three components:

- **The post-incident review record.** One page per incident, with the five-surface walk and the revision plan.
- **The redline log tags.** Every AUP, SOP, training, and runbook revision carries the incident ID that produced it.
- **The three-month verification record.** One line per revision, with a date and a current-state note.

The trail is governance-authored or governance-co-authored (the post-incident review record and the verification record), and the enablement side maintains the operational substance (the redline log). An auditor reading the trail sees a specific chain: signal → investigation → finding → revision → verification. The discipline of producing the chain is what makes the organisation's learning auditable.

## Three loop-closure failures

- **The post-incident review happens but does not produce a revision plan.** Attendees walk the incident and go back to work. **Prevention:** the exit artefact from the review is a one-page revision plan with named owners and windows. Without the plan, the meeting did not happen.
- **The revision drafts but does not co-sign.** The enablement lead drafts the AUP revision; the governance co-author does not redline on cadence; the revision sits in draft for weeks. **Prevention:** the walking-redline cycle from [mod-103 Chapter 01](../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md) has a cadence; incident-driven revisions enter that cadence with a priority tag.
- **The revision is live but the training never updates.** The policy says one thing; the training says the old thing; the operator learns the old thing. **Prevention:** the policy-and-training coupling discipline from [mod-103 Chapter 01](../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md) and [mod-104 Chapter 08](../mod-104-training-programs-and-ai-literacy-curriculum/08-partnering-with-hr-ld-and-internal-comms.md); a policy revision triggers a training revision as a standing rule.

## Summary

- An incident that does not revise an artefact three months later was survived, not learned from. The close-the-loop discipline is a specific procedure to make the revision happen.
- Five surfaces to fold back into: the mod-102 rollout artifact set, the mod-103 policy stack, the mod-104 training content, the mod-105 champion-network priorities, the mod-106 executive scorecard.
- Five-step cadence: post-incident review (enablement slice), draft revisions, ratify, communicate, verify at three months.
- Not every incident revises every surface. Deciding not to revise is a legitimate outcome, documented in the review record.
- The loop-closure audit trail (review record, redline log tags, verification record) is the regulator-readable evidence that the organisation has learned from its incidents.
- Three loop-closure failures: review without plan, revision without co-sign, revision without training update. Each has a specific prevention in the procedure.
