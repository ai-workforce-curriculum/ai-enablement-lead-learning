# Handoff Contracts — AI Risk Engineer, Head of Governance, SecOps and DFIR

> [Chapter 04](04-the-first-ten-minutes-to-the-first-hour.md) ended at T+60 with the enablement lead handing a packet to the downstream investigation. This chapter writes the three handoff contracts explicitly — what the enablement lead delivers to `ai-risk-engineer` (L25), to `head-of-ai-governance` (L60), and to security operations / DFIR; what each named owner delivers back; where the clocks sit; and what the role keeps in the supporting mode that follows. A contract makes the handoff a transfer of ownership rather than an informal continuation.

## Why three contracts, not one

The three downstream owners run different workstreams with different tooling, different clocks, and different external obligations. One packet-shape works for none of them perfectly. Writing three contracts — each lightweight, each named — makes the handoff legible and auditable.

- **`ai-risk-engineer` (L25)** runs the engineered forensics — model behaviour, prompt-and-output analysis, guardrail behaviour, root-cause attribution. Technical and vendor-coordination-heavy.
- **`head-of-ai-governance` (L60)** runs the program-level posture — severity classification, regulator-facing position, governance-council communication, close-the-loop authorisation. Program and compliance-heavy.
- **Security operations / DFIR** run the SOC-side investigation — forensic acquisition, log analysis, cross-system compromise assessment, vendor-side security coordination. Security and evidence-chain-heavy.

Each contract lists what the enablement side delivers, what the enablement side does *not* deliver (to stop the boundary collapsing in the first thirty minutes), what the downstream owner delivers back, and the clock on each delivery.

## Contract 1 — Enablement lead ↔ ai-risk-engineer (L25)

### What the enablement lead delivers

- **The preserved operator-side evidence.** The exact prompt (where available), the exact output (where available), the operator's description of what they were trying to do, the timestamp, the operator's role and function. Not the model's "intent" — the operator's.
- **The approved-use-case reference.** The use policy and the specific approved-use language that the operator was working under (from the mod-102 artifact 1 and mod-103 Chapter 04 AUP).
- **Vendor-side access context.** Which vendor, which tenant, which model variant (if known), which configuration flags (plugins, file upload, agentic behaviour) were on at the time of the event. The access context the ai-risk-engineer needs to pull vendor logs.
- **The usage-anomaly baseline (if the source was source type 2).** Dashboard baseline before and after the signal; the specific shift that triggered recognition.
- **The scope of affected operators.** Named count or estimated range; function and role distribution.
- **A named point of contact on the enablement side** who can answer operational questions during the investigation without the enablement lead being on every thread.

### What the enablement lead does **not** deliver

- A root-cause theory. Phrases like "I think the model was prompt-injected" or "this looks like a guardrail failure" belong to the ai-risk-engineer, not to the enablement lead. The hand-off packet says what was observed, not what caused it.
- A severity classification. "This is a S2 incident" is not the enablement lead's call.
- A vendor-engagement commitment. The enablement lead has not told the vendor anything substantive by this point; the ai-risk-engineer and governance decide what the vendor is told, by whom, and when.

### What the ai-risk-engineer delivers back

- **Engineered root-cause read**, flagged as provisional and refined on their own cadence.
- **Technical mitigation recommendations** — guardrail changes, prompt-template revisions, feature-toggle recommendations. The enablement lead carries these back to the artifact set in the close-the-loop ([Chapter 06](06-the-close-the-loop-discipline.md)).
- **Vendor-side evidence updates** — what the vendor retained, what was preserved, what the vendor's own incident team has produced.
- **Signals on parallel incident shapes.** If the ai-risk-engineer sees patterns across incidents the enablement lead did not connect, those patterns come back to the enablement side as rollout-envelope adjustments.

### Clocks

- Hand-off packet accepted by ai-risk-engineer: **within 90 minutes** of the signal, or the enablement lead escalates to the ladder's alternate and `head-of-ai-governance`.
- First provisional engineered read back to the enablement side: **within 24 hours** by default; shorter if the governance side's severity classification requires it.
- Final technical mitigation recommendations: **within the investigation's defined close window**, typically five to fifteen business days depending on complexity.

<!-- needs-research: the 24-hour and five-to-fifteen-day windows are reasonable defaults for a mid-sized organisation's AI-risk-engineering function; large organisations with mature risk engineering may run faster, smaller organisations may run slower. The runbook should localise these windows to the organisation's actual capacity. -->

## Contract 2 — Enablement lead ↔ head-of-ai-governance (L60)

### What the enablement lead delivers

- **The hand-off packet in full** (incident log, preserved primary signal, rollout artefact set, provisional read, access list).
- **The affected-operator-population read** — scope, functions, regions, any regulated-role sub-tier (clinician, registered representative, credit analyst, attorney) that is in scope.
- **The enablement-side communications state** — what has been said to champions, what has been said on the help channel, what has been said to the exec sponsor (informationally), what has not been said (externally).
- **The approved-tool envelope reference** — the tool's position in the envelope (approved, piloting, restricted) and any adjacent tools that may be affected.
- **A preliminary close-the-loop impact assessment** — which artefacts from the mod-102/103/104/105 stack are likely to need revision, flagged as preliminary. This is the enablement side's forward view, not the governance side's decision.

### What the enablement lead does **not** deliver

- A severity classification.
- A regulator-facing position statement.
- A notification-clock read for Article 73, GDPR Article 33, HIPAA Breach Notification Rule, or any other statutory clock. The clocks are governance- and legal-owned; the enablement lead's role is to preserve evidence so the clocks can be run accurately.
- An external communication draft. If external communication is required, `head-of-ai-governance` and general counsel author it.

### What head-of-ai-governance delivers back

- **The severity classification** and the authorising role for the kill-switch decision (if the authorising role is not already `head-of-ai-governance` themselves).
- **The approved champion-network message** to carry into the champion channel.
- **The governance-council communication plan** — when the council is briefed, what the brief covers, whether the enablement lead attends.
- **The close-the-loop authorisation** — which artefact revisions are authorised and in what window; see [Chapter 06](06-the-close-the-loop-discipline.md).
- **The posture on external communication** — who talks to whom, when, in what channel. The enablement lead's job is to not contradict this posture in internal channels.
- **For EU AI Act high-risk systems, the Article 73 reporting path** — whether the incident qualifies, who authors the submission, what evidence the enablement lead is preserving to support authoring. See [Chapter 07](07-briefing-the-governance-council-and-supporting-article-73-reporting.md).

### Clocks

- Hand-off packet accepted by `head-of-ai-governance`: **within 60 minutes** of the signal (this is the primary handoff; it is the first of the three).
- Severity classification back to the enablement side: **within 4 hours** by default; shorter for signals with external-stakeholder reach or confirmed regulated-data exposure.
- Approved champion-network message: **within 4 hours** for incidents affecting standing operator populations; the champion silent-brief from [Chapter 04](04-the-first-ten-minutes-to-the-first-hour.md) holds until the approved message arrives.
- Governance-council update: on the council's cadence or in a called-session, at the governance side's discretion.

## Contract 3 — Enablement lead ↔ SecOps / DFIR

### What the enablement lead delivers

- **The security-relevant subset of the hand-off packet** — operator-side evidence, the organisational log pipeline snapshot, any credential-exposure context, the user population at risk, the tool's SSO and identity configuration.
- **The access-list for SOC-relevant systems** — identity provider, licence pool, log pipeline, DLP alerts, egress logs. Where the SOC's investigation needs operational access, the enablement lead facilitates through IT identity.
- **The vendor DPA and vendor security contact.** The SOC owns the vendor-side security exchange; the enablement lead hands over the contract and contact information the SOC needs to open it.
- **Preservation-chain confirmation** — written confirmation that the enablement-side evidence has been preserved intact (no overwrites, no deletions, no retention-window-crossing lapses) up to the hand-off moment.

### What the enablement lead does **not** deliver

- A forensic finding on the tool's behaviour.
- A judgment on whether the incident involves malicious operator action.
- A commitment on data-breach notification. Even where the facts look clearly like a breach, the enablement lead does not pre-commit the organisation. That is `head-of-ai-governance`, general counsel, and the privacy officer.
- A vendor-side security exchange. The enablement lead does not open a conversation with the vendor's security team; the SOC does.

### What SecOps / DFIR delivers back

- **The forensic investigation finding** on security-relevant questions — whether data was exfiltrated, whether credentials were compromised, whether a cross-system incident is active.
- **Operational guidance** on continued use of the tool — whether the SOC supports the kill-switch state, whether the tool should be held offline pending security remediation, whether other tools in the envelope need equivalent treatment.
- **Evidence-chain formalisation** — the SOC takes custody of the evidence from the enablement side for the duration of the investigation.

### Clocks

- Security-relevant subset packet accepted by SOC: **within 90 minutes** for signals with any data-exfiltration or credential-exposure shape; otherwise within 4 hours.
- Initial SOC read: **within 4 hours** on the containment question (is the tool safe to continue, under what constraints).
- Full forensic finding: the SOC's own close window, typically days to weeks depending on scope.

<!-- needs-research: the SOC clocks depend heavily on the organisation's security operations maturity, the vendor's security responsiveness under the DPA, and the forensic-tooling available. Localise against the organisation. -->

## The shape of the packet

The packet is one or two documents — at most — plus the preserved evidence surface. One document is a "cover sheet" that lets each downstream owner find what they need; the other, if present, is the long-form evidence annex.

### Cover sheet template

A short Markdown or one-page PDF with named sections. One version for all three downstream owners; the sections each role needs are labelled.

- **Incident ID and timestamps.** Signal recognition time, packet assembly time, packet delivery time.
- **Source classification.** Which of the four signal sources.
- **Tool and vendor.** Name, version, tenant, configuration flags.
- **Affected scope.** Operators, functions, geographies, regulated-role sub-tiers.
- **Primary signal.** Link to preserved primary signal surface in the evidence store.
- **Rollout artifact set links.** Use policy, SOP, access playbook, training, support ladder, champion list, kill-switch runbook.
- **Current kill-switch state.** Pulled, partial-pulled, held. With timestamp and authorising role.
- **Enablement-side provisional read.** One short paragraph, flagged as provisional.
- **Enablement-side communications state.** What has been said on which channel, to whom, with timestamps.
- **Access list.** Named humans on the enablement side to contact for specific operational questions.
- **For the ai-risk-engineer.** Operator-side evidence, vendor access context, usage baseline.
- **For `head-of-ai-governance`.** Communications state, affected-operator-population read, preliminary close-the-loop impact assessment.
- **For SecOps / DFIR.** Organisational log pipeline snapshot, credential-exposure context, SSO configuration, vendor DPA reference and security contact.

The cover sheet's purpose is the handoff's purpose: a transfer of ownership that each downstream owner can act on without further briefing.

## The "shared, not transferred" boundary

One subtle thing worth naming: the enablement side does not *transfer* ownership of operator-facing communication and the champion network to the governance side; the enablement side continues to operate those surfaces under governance-authored content. The transfer is of the **investigation substance** — the thing the enablement side is not the owner of. The thing the enablement side *is* the owner of (the operational substance of the rollout) continues under incident governance.

This is why the three contracts above read as asymmetric. The downstream owners carry the substance; the enablement lead carries the operations. Both are live; neither is paused during an incident.

## The two-week horizon

Beyond the first-hour and first-day contracts, each investigation has its own close window. The enablement lead's horizon for supporting-mode is typically two weeks from the signal to a confirmed incident write-up, and then another two to four weeks to close the loop ([Chapter 06](06-the-close-the-loop-discipline.md)). Two-week supporting-mode responsibilities:

- Weekly check-in with each of the three downstream owners — what they need from the enablement side, what has changed in the investigation, what communications the governance side wants carried.
- Keeping the kill-switch state current with the investigation's needs — full pull, partial, or hold, revised as the investigation reads progress.
- Continuing the champion network's role as the first-line answer surface; feeding late-arriving field reports into the investigation as additional context.
- Not substituting for the investigation. The weekly check-in is a listening surface, not a status-demand from the enablement side.

## Three contract failures

- **The packet is delivered but the clock is not confirmed.** The enablement lead sends the hand-off; the downstream owner has not acknowledged receipt in the 60-to-90-minute window. The enablement lead does not re-send five times; they escalate to the alternate on the escalation ladder and to `head-of-ai-governance` simultaneously. **Prevention:** the escalation-ladder discipline from Chapter 02 Property 6.
- **The enablement lead keeps answering questions outside their contract.** The ai-risk-engineer asks "what do you think caused this at the model level?" and the enablement lead answers. The answer becomes part of the investigation's record. **Prevention:** the contracts above are **what you deliver** lists; questions outside the list go to the appropriate owner, not to the enablement lead.
- **The three downstream owners stop coordinating with each other.** The ai-risk-engineer works technical-root-cause; the SOC works forensic; `head-of-ai-governance` works severity — and they are not talking to each other. The enablement lead is often the only role with visibility across all three threads. **Prevention:** the weekly supporting-mode check-in is deliberately structured so the enablement lead can surface cross-thread information to all three owners in one pass; the enablement lead's role is convening the coordination, not substituting for it.

## Summary

- Three handoff contracts, not one. Each named owner runs a different workstream with different clocks and different external obligations.
- Each contract names: what the enablement side delivers, what the enablement side does not deliver, what the downstream owner delivers back, and the clocks on each delivery.
- The hand-off packet is one cover sheet (plus a preserved evidence annex). The cover sheet's purpose is to let each downstream owner find what they need and act without further briefing.
- The boundary is "shared, not transferred" — the investigation substance transfers to the downstream owner; the operational substance of the rollout continues under incident governance.
- Two-week supporting-mode horizon with weekly check-ins across the three downstream owners; the enablement lead is often the only role with cross-thread visibility and uses it to convene coordination, not to substitute for it.
- Three contract failures: unconfirmed clock on hand-off, scope-creep answering questions outside contract, cross-owner coordination breakdown. Each has a specific prevention.
