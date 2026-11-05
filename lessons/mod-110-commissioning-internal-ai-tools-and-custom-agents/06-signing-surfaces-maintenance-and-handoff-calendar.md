# Signing Surfaces, Maintenance Commitments, and the Hand-Off Calendar

> A brief that isn't signed is a conversation. A maintenance owner who isn't named isn't committed. A hand-off calendar that lives in email isn't a calendar. The preceding chapters authored the brief, named the inheritance assessment, drew the architectural boundary, and specified the measurement. This chapter is the operational infrastructure that keeps the commission running after the signatures land — signing surfaces, maintenance commitments, hand-off cadence, and the question of when a commissioned tool stops being a commission and becomes something else.

## The three signatures the brief carries

[Chapter 02](02-the-commissioning-brief-as-the-load-bearing-artifact.md) named the signatories; this chapter names what each signature is binding on and what each signatory's veto applies to. Three signatures on a commissioning brief:

### Signature 1 — The commissioner (the enablement lead)

**What they bind to.**

- The problem statement in Section 1 — the business problem as named is the problem being solved, and will not be silently redefined after the brief is signed.
- The user cohort in Section 2 — the people receiving the tool are the people in the brief; expansion to other cohorts is a new brief, not a scope revision.
- The success criterion in Section 3 — the outcome metric with its baseline and target is the standard the commission is measured against, fixed at commission time.
- The rollout-artefact-set binding in Section 8 — every slot is honoured, every co-authoring commitment in the brief is the commissioner's to deliver through the pilot.

**What they can veto.** Scope changes. The commissioner's signature is the artefact a mid-build scope-creep conversation runs against. "We would also like the agent to handle tier-2 escalations" is a scope change that requires a brief revision and a re-signature; it is not a conversation the commissioner has in a slack channel.

### Signature 2 — The `ai-engineering-manager`

**What they bind to.**

- The build calendar in Section 6 — the dates named are the dates the engineering team will meet, with named contingency the commissioner has accepted.
- The budget in Section 5 — the engineer-week cost is the commitment, with the maintenance-owner commitment (Section 7) carried by the same organisational line.
- The acceptance criteria that determine when the build is complete — the brief is the specification; the build is done when the specification is met, not when the engineer thinks it is done.

**What they can veto.** The brief's architectural assumptions. If the brief implies an architecture the engineering team cannot build or cannot maintain, the manager sends the brief back with a specific list of assumptions to remove before re-signing. This is the Chapter 01 designer-posture prevention: the manager's veto surface is the discipline that keeps the commissioner from writing architecture into the brief.

### Signature 3 — The `head-of-ai-governance` (L60)

**What they bind to.**

- The guardrails section (Section 4) — the policy stack references are current, the red-team ask (Appendix A) is dated appropriately against the pilot-to-rollout gate, and the data-handling SOP from [mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md) is honoured.
- The rollout-artefact-set binding (Section 8) from the governance side — every slot that governance co-authors is accepted at the altitude of the signature.

**What they can veto.** Program-level risk posture. A brief whose guardrails do not meet the organisation's AI risk policy, or whose red-team ask is scoped too narrowly, is returned by `head-of-ai-governance` with a named gap. The governance veto is also the surface that catches commissions that should have been Column 2/3 (vendor tools with contract-level data protections) rather than Column 4 (internal builds where data protections live in the engineer's prompt discipline).

## The fourth signature — the maintenance owner

The brief's Section 7 is co-signed by the maintenance owner and that owner's manager, independently of the `ai-engineering-manager`'s build signature. The two signatures (build and maintenance) can live in different organisations; the brief requires both.

**What the maintenance owner binds to.**

- The commitment shape — engineer-days per month at steady state, on-call expectation, SLA.
- The scope — bug fixes, prompt iteration, eval-harness updates, vendor-model version bumps in scope; feature expansion, new user cohorts, new target tasks out of scope.
- The acceptance of the tool from the build team at the acceptance date named in Section 6.

**What the maintenance owner can veto.** A build that lands at acceptance without the runbook, eval harness, documentation, and observability surface the Chapter 02 Section 8 binding specifies. The maintenance owner is not obligated to accept a tool whose artefacts are missing; refusal returns the build to the engineering team for completion, not to the commissioner for acceptance under duress.

The maintenance owner's veto is the Chapter 01 apologist-posture prevention: when the build team wants to declare completion against an incomplete artefact, the maintenance owner is the surface that can refuse without putting the commissioner in a bind.

## The hand-off calendar

A commissioned tool has four hand-off moments that live on a calendar the commissioner owns. The calendar is not a sentimental artefact — it is the specific set of signed meetings that determine whether the commission is tracking.

### Hand-off 1 — Brief signing (T-0)

Three signatures (commissioner, `ai-engineering-manager`, `head-of-ai-governance`) plus the maintenance-owner co-signature. The brief is filed in the organisation's governance evidence store — the same store the [mod-109 Chapter 02](../mod-109-ai-incident-response-and-enablement-side-rollback/02-the-kill-switch-as-an-operating-artifact.md) kill-switch runbook lives in — not in the commissioner's local drive.

**What happens at this meeting.** The stage-gate questions from Chapter 02 are read aloud; each signatory confirms they are binding on the content they are signing for. The one-paragraph scope contract is read; each signatory confirms the scope they are committing to. The red-team ask (Appendix A) is dated against the pilot-to-rollout gate. The maintenance owner's commitment shape (Section 7) is confirmed.

### Hand-off 2 — Pilot charter review (pre-pilot)

The pilot charter from [mod-102 Chapter 02](../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md) is authored during the build. At the pilot charter review the commissioner, the engineering team, and (on the pilot's data-sensitivity surface) the governance co-author confirm that the pilot's cohort, duration, baseline, adopt/extend/kill criteria, and kill-switch match the brief's Section 2 and Section 3 constraints.

**What happens at this meeting.** The outcome metric from Section 3 is confirmed as the pilot's success criterion. The usage-as-sanity-check floor is set. The red-team evidence is confirmed as on-track for the pilot-to-rollout gate. The pilot cohort is confirmed as the brief's cohort or a defensible subset.

### Hand-off 3 — Acceptance (acceptance date)

The commissioner formally accepts the tool from the engineering team. Acceptance is the event; the maintenance owner's signature on acceptance is the operating consequence.

**What happens at this meeting.** The acceptance-criteria table from the brief is walked line by line. The eval harness is run and its baseline score recorded. The runbook, observability surface, and documentation are reviewed. The maintenance owner confirms the artefacts are complete and signs. The build budget's final accounting is closed with Finance ([mod-107 Chapter 04](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/04-partnering-with-procurement-finance-and-it.md)). The tool enters steady-state operation under the rollout artefact set.

An acceptance meeting that does not close with maintenance-owner signature is an incomplete acceptance. Treating it as complete is the hand-off failure the next six months will punish.

### Hand-off 4 — Graduate-or-retire review (every four quarters)

The commissioned tool has a standing graduate-or-retire review at a four-quarter cadence. The review is not an inquisition; it is the deliberate surface on which the tool's continued existence is affirmed or re-examined. The four-quadrant read from [Chapter 05](05-measuring-commissioned-tools-on-the-rollout-framework.md) is the input; three outcomes are possible:

- **Continue as a commissioned tool.** The outcome metric is tracking target; the maintenance commitment is being honoured. The next graduate-or-retire review is scheduled four quarters out.
- **Graduate to vendor-portfolio status.** The tool has stabilised sufficiently that it can be managed as a mature internal-build line item in the [mod-107 Chapter 06](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/06-the-vendor-vetting-rubric.md) vendor-portfolio view, with annual review rather than quarterly. The commissioner hands off program ownership to the CoE lead ([mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md)); the maintenance owner remains the maintenance owner.
- **Retire.** The retirement memo from [Chapter 05](05-measuring-commissioned-tools-on-the-rollout-framework.md) is authored. The tool is pulled under the [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) kill-switch and the [mod-109 Chapter 02](../mod-109-ai-incident-response-and-enablement-side-rollback/02-the-kill-switch-as-an-operating-artifact.md) runbook; the close-the-loop artefacts feed [mod-103](../mod-103-policy-co-authoring-with-governance/README.md), [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md), and [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md).

The graduate-or-retire review is the surface the commissioner's apologist-posture is most tested against. A tool that has missed its target twice and whose four-quadrant diagnosis is persistent-red is on the retire path; the commissioner's job is to run the review rather than defer it.

## The three tenure phases of a commissioned tool

Tying the hand-offs together, a commissioned tool has three tenure phases:

### Phase 1 — Build (T-0 to acceptance)

The tool is being built. The brief is the live specification. The engineering team runs scope conversations against the brief. The commissioner runs weekly against the build calendar from Section 6, attends the pilot charter review, and prepares the pilot cohort for first contact.

### Phase 2 — Pilot and early steady-state (acceptance to first graduate-or-retire review)

The tool is in operation. The rollout artefact set wraps it. The pilot-to-rollout decision happens on the gate from Section 6, with red-team evidence in hand. The portfolio scorecard carries the tool at the same cadence as every other rollout. The maintenance owner is running the Chapter 02 Section 7 commitment.

### Phase 3 — Steady state (after first graduate-or-retire review, if "continue" or "graduate")

The tool is a stable line item. If "continue," the quarterly cadence from [Chapter 05](05-measuring-commissioned-tools-on-the-rollout-framework.md) runs; the next graduate-or-retire review is four quarters out. If "graduate," the tool enters the vendor-portfolio view and the annual cadence; program ownership moves to the CoE lead; the maintenance owner continues the engineering responsibility.

A commissioned tool whose Phase 2 never cleanly transitions to Phase 3 is a commission the organisation has not decided about. The graduate-or-retire review is the forcing function that makes the decision happen.

## When a commissioned tool becomes a vendor-shaped tool

The graduation path from Phase 2 to the vendor-portfolio view is worth naming explicitly, because it is a quiet but structural shift in how the organisation holds the tool.

When a commissioned tool graduates:

- **Ownership moves from the commissioner to the CoE lead.** The commissioner continues to support the rollout, but the standing portfolio-management responsibility moves. See [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md) for the CoE operating rituals.
- **Measurement cadence shifts from quarterly to annual.** The tool continues on the scorecard but at the cadence commercial tools are read on.
- **The vendor-vetting rubric from [mod-107 Chapter 06](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/06-the-vendor-vetting-rubric.md) is applied.** The tool is now a line item in the vendor portfolio; the rubric reads the tool's capability trajectory, data posture, security and compliance, commercial resilience (for an internal tool this is maintenance resilience), operating surface, and switching posture.
- **The maintenance commitment is reaffirmed at annual cadence rather than quarterly.** The Chapter 02 Section 7 commitment is reviewed annually by the maintenance owner's manager and the CoE lead.
- **The rollout artefact set continues to wrap the tool, unchanged.** Graduation is a management-cadence shift, not a rollout-discipline shift. The policy, training, champion, support, and kill-switch artefacts are the same artefacts they were on day one; they are reviewed on the annual cadence, not the quarterly one.

Graduation is a success. A commissioned tool that reaches graduation is a tool that has justified its Column 4 decision, moved its outcome, honoured its maintenance commitment, and earned its line item. The commissioner's incentive is to run commissions whose shape makes graduation legible — not commissions that drift indefinitely in Phase 2.

## The retirement path, briefly

When the graduate-or-retire review concludes "retire," the retirement runs through the same kill-switch discipline as any other tool pull — the [mod-109 Chapter 02](../mod-109-ai-incident-response-and-enablement-side-rollback/02-the-kill-switch-as-an-operating-artifact.md) runbook is operated by the enablement lead, with the governance-side co-author on the communications. Three differences from an incident-driven kill:

- **The timeline is paced.** A retirement is not an incident; the operators have warning, the champions have a brief, the alternative path is named before the retirement date.
- **The retirement memo from [Chapter 05](05-measuring-commissioned-tools-on-the-rollout-framework.md) is the governance-council deliverable.** The memo makes the retirement auditable.
- **The engineering stack (eval harness, retrieval index, control-plane configuration) is handled under the maintenance owner's operational discipline.** Whether any of it is reused by the next commission in the space is the commissioner's call, with the architect consulted if the stack was built against platform surfaces the architect is still maintaining.

## The CoE-operations surface

The commissioning program has a standing CoE operating surface that [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md) treats in depth. From the commissioner's side of the interface, three artefacts live at the CoE cadence:

- **The commissioning pipeline view.** A standing one-page view of every brief in the system, its tenure phase, its next hand-off date, and its graduate-or-retire posture. Reviewed monthly with the CoE lead.
- **The maintenance-owner portfolio view.** The engineering teams that carry maintenance for commissioned tools, the specific tools each team owns, and the engineer-days-per-month each team is committed to. Reviewed quarterly with the engineering managers.
- **The co-owned CoE responsibility with the `applied-ai-engineer` manager.** R16 is a co-owned responsibility; the commissioning cadence is one of the recurring CoE rituals with the engineering manager on the other seat. The ritual is monthly, treats the pipeline view and the maintenance portfolio view together, and is the surface on which cross-commission patterns (platform constraints, policy updates, retirement decisions) are discussed.

## Summary

- Three signatures on the brief: the **commissioner** (binds to scope), the **`ai-engineering-manager`** (binds to build), the **`head-of-ai-governance`** (binds to program-level risk posture). A fourth signature from the **maintenance owner** and that owner's manager binds Section 7 independently.
- Each signatory has a specific veto surface. The signatures are the discipline that catches Chapter 01's designer, product-manager, and apologist postures before they collapse the commission.
- Four hand-offs: **brief signing (T-0)**, **pilot charter review (pre-pilot)**, **acceptance (acceptance date)**, **graduate-or-retire review (every four quarters)**. The hand-off calendar is an artefact the commissioner owns; informal cadence is an invitation to drift.
- Three tenure phases: **build**, **pilot and early steady-state**, **steady state**. Phase 3 is reached by continuing or graduating; phase 2 that never transitions is a commission the organisation has not decided about.
- Graduation moves ownership to the CoE lead and measurement to annual cadence; the rollout artefact set remains unchanged. Graduation is a success the commissioner designs for.
- Retirement runs through the kill-switch discipline with the Chapter 05 retirement memo as the auditable deliverable.
- The commissioning program has a standing CoE operating surface — pipeline view, maintenance-owner portfolio view, co-owned R16 ritual with the `applied-ai-engineer` manager — that [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md) treats in depth.
