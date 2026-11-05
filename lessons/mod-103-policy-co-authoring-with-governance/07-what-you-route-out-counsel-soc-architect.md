# What You Route Out — Counsel, SOC, Architect

> You are the convener. The convener often writes the first draft of everything. If you are not careful, you end up treated as the owner of everything — legal opinions, forensic findings, control architecture. The drifts feel like upgrade and read like competence. They are not; they are quiet role collapse. This chapter is the correction.

## Why the drifts happen

An enablement lead six months into a role has usually written more co-authored drafts than any single partner in the room. You have been inside the walking redline on acceptable-use policy ([Chapter 04](04-the-one-page-acceptable-use-policy.md)), the data-handling SOP ([Chapter 05](05-the-data-handling-sop.md)), the intake questionnaire ([Chapter 06](06-the-intake-questionnaire.md)). You have attended the AI governance council ([Chapter 02](02-the-governance-council-liaison-seat.md)) and surfaced field signal from champions that shaped three policy decisions. You have read NIST AI RMF GOVERN and ISO/IEC 42001 clauses ([Chapter 03](03-nist-ai-rmf-govern-and-iso-iec-42001-for-the-enablement-seat.md)) at enough depth to speak the standards vocabulary.

This is the point in the role where three drifts become most likely — not out of overreach, but out of the pattern-matching of a competent operator who has accumulated more context than any single counterparty.

The three drifts, in order of frequency:

1. **Legal opinion → counsel.** Writing legal readings instead of legal hooks.
2. **SOC-side incident handling → security operations.** Running forensic workstreams instead of convening them.
3. **Control-library architecture → `senior-ai-governance-architect` (L50).** Redesigning the taxonomy instead of surfacing evidence.

## Drift 1 — Legal opinion stays with counsel

### The distinction between a legal hook and a legal opinion

A **legal hook** is a statement in your draft that gives counsel somewhere to attach an obligation. You write it; counsel attaches language to it.

- "Users must not paste customer PII into prompts." (Hook — names a data class.)
- "This tool processes data in the US East region." (Hook — names a jurisdiction.)
- "Vendor retains inputs for 30 days per the DPA." (Hook — names a counterparty relationship and a contractual term.)

A **legal opinion** is a statement of what the law requires or permits, or of what the organization's legal position is. You do not write these; counsel does.

- "This would violate GDPR Article X." (Opinion.)
- "This is acceptable under our EU AI Act deployer obligations." (Opinion.)
- "This exceeds the DPA's authorized processing." (Opinion.)

The test for any sentence in a draft: does it describe a fact the operator should know about (hook), or does it assert what the law or the contract says (opinion)? If the latter, cut it and leave the legal attachment to counsel.

### The handoff mechanics

- A weekly or per-cycle **legal review slot** with counsel. Thirty minutes. Walk the current drafts; capture every legal-written line in the redline log ([Chapter 01](01-the-co-author-posture-and-the-redline-log.md)).
- **Counsel named in the co-author tag** on every section where a legal reading has been attached.
- An **explicit question queue** for counsel between cycles. When a draft needs a legal reading before the next cycle, open the question explicitly ("is the vendor retention term compatible with our data-subject-rights obligations for EU employees?") rather than guessing at the answer.

### What you keep

You keep the ability to ask hard legal questions. You keep the operational knowledge that lets you draft sentences counsel can productively respond to. You give up the responsibility for the opinion itself.

## Drift 2 — SOC-side incident handling stays with security operations

### The distinction between enablement-side and SOC-side

**Enablement-side incident handling** is the first ten minutes and the convening that follows:

- The data-handling SOP accident path ([Chapter 05](05-the-data-handling-sop.md) section 4) — what the user does, who they contact, what evidence to preserve.
- First-line triage — recognizing the shape of the accident (paste-mistake, subtly-wrong-output, tool-malfunction) and routing accordingly.
- The pause-rollout decision — when to pull the kill switch on a specific tool ([mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) artifact 7).
- Champion-network communication — what to tell operators so they do not compound the incident by continuing to run into it.
- Convening the right security and legal partners for the handoff.

**SOC-side incident handling** is the forensic workstream that picks up at the handoff:

- Forensic acquisition and preservation.
- Log analysis and model-forensics (what the tool actually did, what persisted, where).
- Vendor coordination — what the vendor retained, what they can preserve, what they can delete.
- Regulator-notification-clock management — if a clock is tripped, `head-of-ai-governance` and counsel run the external communications.
- External coordination with data subjects where obligations attach.

The enablement lead **convenes**, **triages**, and **hands off**. Does not run the forensic workstream. Does not decide notification clocks. Does not speak to regulators.

### The handoff mechanics

- A named SOC point of contact and a named `ai-risk-engineer` (L25) in the escalation path section of the AUP and the SOP.
- An "enablement-side evidence pack" discipline — the operator-side evidence (the accident path's preserved prompt text, output, timestamp, user context) packaged and handed to the SOC within a defined SLA, not drip-fed as questions arise.
- Explicit clock on when enablement-side handling ends and SOC-side handling begins. Often the moment the SOC accepts the evidence pack, or the moment a notification obligation becomes a live question — whichever comes first.

### What you keep

You keep the convening role. You keep the operational knowledge that lets you brief the SOC quickly and accurately. You give up the responsibility for the forensic finding and the external posture. [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) runs this handoff end-to-end.

## Drift 3 — Control-library architecture stays with `senior-ai-governance-architect`

This is the most insidious drift because it feels like upgrade.

### The shape of the drift

You have been running intake for months. Patterns are visible: field X is systematically mis-filled; classification tier Y is never evidenced in practice; control Z maps to a policy clause operators ignore. You start to want to redesign the intake schema, restructure the risk-classification taxonomy, or rewrite the mapping between policies and controls.

**Stop.** The taxonomy is the architect's accountability. The architect is responsible for it surviving audit, evolving across regulations, and plugging into the governance program over years. Enablement-side revisions, made in good faith to "fix" what seems broken from the operating-model view, tend to destabilize the audit story in ways you will not see from inside the operating model.

### The move that is yours

You surface the field evidence. You do not propose the redesign.

- Collect the cases where the current taxonomy produces a wrong or unstable classification.
- Collect the controls that are never evidenced in practice.
- Collect the policy categories that never see use, or see use for something other than their intent.
- Write the memo to the architect, per the co-authoring beat on schema in [Chapter 06](06-the-intake-questionnaire.md). Frame it as evidence for the architect's consideration. Do not include the proposed field redesign.
- The architect decides what, if anything, to redesign. If the architect decides to proceed, the architect leads the redesign and you run the enablement-side update (training, policy revision, champion briefings).

### The handoff mechanics

- Quarterly or per-cycle evidence memo to `senior-ai-governance-architect`, with `head-of-ai-governance` (L60) on cc.
- A standing 30-minute monthly bilateral with the architect, where the two of you walk the evidence and the architect decides priority.
- A disciplined "no redesign proposals from this seat" rule, held even under pressure from the council to "just fix it."

### What you keep

You keep the operational knowledge that makes you the person surfacing the sharpest evidence. You keep the ability to say the current design is not working. You give up the responsibility for the next design.

## The discipline that stops all three drifts

The pattern is the same across the three. You write **observations**, not **opinions**. You name **owners**, not **outcomes**. You **convene**, you do not **absorb**.

- For legal: write hooks, not readings. Named counsel in the tag.
- For security: write what you observed, not what was forensically true. Named SOC contact in the escalation path.
- For architecture: write evidence, not redesigns. Named architect in the quarterly memo.

Each handoff has a **named owner**, a **named trigger**, and a **thing you keep** (the observation, the convening, the operational knowledge). The thing you keep is what makes you the strongest possible partner to each of the three — and what stops the partner relationship from collapsing into a one-person job.

## A closing note on why this is worth getting right

These three drifts are a sign of strong operators, not weak ones. You drift because you are the person with the most context in the room. The discipline is to spend that context by convening the right owners — not by absorbing their jobs. A role that absorbs becomes the choke-point when the absorbed owner is needed in parallel; a role that convenes scales to any number of parallel threads because each owner is pulling their own weight.

[mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) drew the handoff map. This chapter is what keeps the four arrows live when they are under pressure.

## Summary

- Three drifts the enablement seat most commonly makes: legal opinion, SOC-side incident handling, control-library architecture.
- Legal: write hooks (facts the operator should know) not opinions (what the law says). Counsel attaches the opinion. Weekly review slot and co-author tag on every section counsel touches.
- SOC: convene and triage the first ten minutes; hand off the evidence pack; let security operations and `ai-risk-engineer` (L25) run the forensic workstream. See [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).
- Architecture: surface field evidence to `senior-ai-governance-architect` (L50) as a quarterly memo. Do not propose redesigns from this seat. The architect decides; you update the runner side.
- The shared discipline: observations not opinions; named owners not outcomes; convene, do not absorb.
- The thing you keep in each handoff — the convening role, the operational knowledge — is what makes you the strongest possible partner to each of the three owners.
