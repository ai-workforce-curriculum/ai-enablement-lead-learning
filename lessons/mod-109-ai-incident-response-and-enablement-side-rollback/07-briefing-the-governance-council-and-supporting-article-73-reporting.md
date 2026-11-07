# Briefing the Governance Council and Supporting Article 73 Reporting

> The enablement lead attends the AI governance council from [mod-103 Chapter 02](../mod-103-policy-co-authoring-with-governance/02-the-governance-council-liaison-seat.md). On an incident cycle, the council brief shifts shape. The read-ahead has an incident slot; the enablement lead speaks to the enablement-side substance; the governance side speaks to the program-level posture and the regulator-facing position. For EU AI Act high-risk systems, one specific reporting obligation — Article 73 — sits across this surface and is the single most time-sensitive external obligation the enablement side supports. This chapter writes both roles: the council brief the enablement lead delivers, and the Article 73 support posture the enablement lead holds. Neither is authoring; both are co-authorial-support postures with specific deliverables.

## The council brief on an incident cycle

The standing council cadence from [mod-103 Chapter 02](../mod-103-policy-co-authoring-with-governance/02-the-governance-council-liaison-seat.md) runs independently of incidents. On a cycle where a confirmed incident sits on the agenda, the brief adds one slot — the incident slot — and the enablement lead's contribution is specific.

### The enablement-side content of the incident brief

The enablement lead's section of the incident read-ahead has four parts.

- **Signal and recognition.** Which of the four signal sources ([Chapter 01](01-the-enablement-side-of-the-incident-path.md)) surfaced the signal; the latency from the underlying event to recognition; a one-sentence read on whether the recognition was fast or slow against the organisation's expectations.
- **First-hour operations.** The kill-switch state (pulled, partial, held, with the authorising role); the preservation state; the communications state (what has gone out on which internal channel, with the governance-approved framing). This is the enablement-side record of the first hour, not the investigation's findings.
- **Close-the-loop status.** Which of the five surfaces from [Chapter 06](06-the-close-the-loop-discipline.md) are revising; which revisions are drafted, co-signed, or live; the three-month verification check-in schedule.
- **Enablement-side lessons for the next rollout.** Not forensic root-cause (that is `ai-risk-engineer`'s) and not severity classification (that is `head-of-ai-governance`'s). Specifically: what the enablement side's artefact set did well, what it did not, and what the artefact-set revisions will teach the next rollout.

### What the enablement lead does **not** cover in the brief

- Forensic root-cause. The ai-risk-engineer covers the engineered finding.
- Severity classification and the regulator-facing posture. The governance side covers both.
- The Article 73 submission substance (below). The governance side authors; the enablement lead supports.
- External communications posture. Legal and governance co-author; the enablement lead does not characterise.

The enablement side's section is tight — typically one page in the read-ahead and five to seven minutes in the council session. The rest of the time belongs to the roles with the primary substance.

### The council's reading surface

The council is not re-litigating the incident in the brief. The council is reading whether the organisation's AI program learned from the incident, whether the program is ready for the next rollout, and whether governance leadership is comfortable attesting that the organisation's posture is defensible. The enablement-side section contributes to the third reading — the artefact-set is what the organisation uses to attest to posture. A clean enablement-side record in the incident brief is what makes the attestation unremarkable; a weak record forces the council to spend attention on remediation rather than on strategic calls.

## Article 73 — the EU AI Act serious-incident reporting obligation

For organisations that deploy or provide a high-risk AI system (as defined under the EU AI Act) and whose deployment touches the EU market, Article 73 of Regulation (EU) 2024/1689 ([the EU AI Act](https://eur-lex.europa.eu/eli/reg/2024/1689/oj)) imposes a specific serious-incident reporting obligation. This section writes the enablement lead's support posture; it does not write the submission, because the submission is not the enablement lead's artefact.

The Article 73 text, the serious-incident definition, the tiered reporting clocks (with a default outer bound of fifteen days, shortened in critical-infrastructure and loss-of-life scenarios), and the member-state market-surveillance authority identities are governed by the Act itself and by the implementing guidance of the EU AI Office and member-state authorities, both of which continue to develop; the enablement lead re-reads the primary text and current guidance on each content cycle. See [Article 73 in EUR-Lex](https://eur-lex.europa.eu/eli/reg/2024/1689/oj).

### What Article 73 broadly requires

Article 73 of the AI Act requires providers of high-risk AI systems placed on the EU market to report **serious incidents** to the **market-surveillance authorities** of the affected member state(s), within a defined short window from the moment the provider becomes aware of the incident. The Act defines "serious incident" and sets the reporting clock, which is tight; the specific window and the precise authority routing are governed by the Act's text and the implementing guidance from the EU AI Office and member-state authorities, which continue to develop.

The Article's obligation sits with the **provider** (and, under specific conditions, the deployer). Reading the provider/deployer distinction correctly for each organisation's situation is a legal question that general counsel and `head-of-ai-governance` co-answer; the enablement lead does not read the distinction independently.

### The enablement side's role in an Article 73-eligible incident

The enablement lead is the operational role that preserves evidence and runs the internal operations that make the submission authorable. The specific supporting responsibilities:

- **Preservation sufficient for the submission.** The enablement-side evidence — operator-side observations, usage context, user-facing output, communication records — is preserved to the standard the submission requires. [Chapter 02](02-the-kill-switch-as-an-operating-artifact.md) Property 4 names the preservation sequencing; for Article 73-eligible incidents, the preservation standard is not the organisation's choice. The governance and legal side specify the standard; the enablement lead executes.
- **Timeline documentation sufficient for the submission.** The incident log from [Chapter 04](04-the-first-ten-minutes-to-the-first-hour.md) — timestamped, append-only, observation-based — is directly usable in the submission's timeline reconstruction. The log's observation-only discipline matters especially here: the Article 73 submission is read by a regulator, and the enablement side's log should not contain speculation or opinion that the regulator reads as organisational position.
- **Deployment-side context to the submission author.** The submission needs the deployment context: the affected operator population, the geographic distribution (specifically, which EU member states were affected), the use case the tool was deployed for, the training and policy the operators were under. The enablement lead supplies this context to the author in a structured form.
- **Post-submission artifact coordination.** The submission names (sometimes in detail) the organisation's planned mitigations. Those mitigations run through the close-the-loop process from [Chapter 06](06-the-close-the-loop-discipline.md); the enablement lead's close-the-loop plan is what the submission's mitigation section commits to. Writing the submission before the close-the-loop plan is a specific sequencing problem; the enablement lead's early draft of the close-the-loop plan during the investigation is the input the submission author needs.

### What the enablement lead specifically does **not** do on Article 73

- Author the submission. The submission is authored by the governance and legal side, under `head-of-ai-governance`'s program leadership. The enablement lead does not sign.
- Communicate with the market-surveillance authority. The organisation's counsel and `head-of-ai-governance` communicate.
- Classify the incident as "serious" under the Act's definition. The classification is a legal and governance call; the enablement lead supports the preservation and context work that lets the classification be made correctly.
- Run the reporting clock. The clock is owned on the governance and legal side. The enablement lead's discipline is to not accidentally *stop* the clock by communicating substantively with the regulator or externally characterising the incident in a way that moots the submission.

### The provider-vs-deployer distinction for the enablement seat

Most organisations the enablement lead works at are **deployers** under the AI Act, not **providers**. Deployer obligations under Article 73 are narrower than provider obligations but not zero — specifically, deployers have a duty to inform the provider of a serious incident, and in some fact patterns deployers' own reporting duties attach.

For the enablement lead, this means: when an EU-touching incident arises on a tool the organisation uses but did not build, the governance side runs two parallel threads — the organisation's own deployer obligations, and the organisation's duty to inform the provider (vendor). The enablement lead supports both. The provider's own Article 73 submission is the vendor's work, but the enablement lead's hand-off packet to the ai-risk-engineer and to `head-of-ai-governance` is often used to inform the vendor; the enablement lead's packet discipline from [Chapter 05](05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md) is therefore load-bearing in the Article 73 chain, even without the enablement lead authoring a submission.

For organisations that **are** providers of a high-risk system (including organisations with an in-house custom tool that qualifies as high-risk under the Act), the provider obligations attach directly and the enablement lead's preservation and context work is input to the organisation's own submission. [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md) treats the commissioning of internal tools; the Article 73 consideration intensifies in that context.

### Parallel reporting obligations across jurisdictions

Article 73 is the most prominent AI-specific serious-incident reporting regime but not the only one. Other obligations the enablement lead supports without authoring:

- **GDPR Article 33.** Personal-data-breach notification to the supervisory authority within 72 hours. Runs in parallel to Article 73 when both apply.
- **HIPAA Breach Notification Rule (US healthcare).** Separate clock, separate authority (HHS OCR), separate affected-individual notification obligations.
- **State breach-notification laws (US).** Vary by state; California, New York, and others carry specific obligations.
- **Sector-specific obligations.** SR 11-7 in banking (for model-risk-adjacent events); FINRA for securities firms; FDA for medical-device software functions.
- **Member-state-specific obligations under the AI Act.** Member states may implement supplementary obligations beyond Article 73.

The enablement lead does not run any of these clocks. The enablement lead's specific contribution across all of them is the same: preservation sufficient for the submission, timeline documentation, deployment context, and non-interference with the clock. The governance and legal side runs the clocks and authors the submissions.

## The council-level posture on the clock

One subtle point worth naming at the council level: the enablement lead's **speed of signal-recognition** is the organisation's primary constraint on meeting the Article 73 and parallel clocks. The clocks start when the organisation becomes aware; the enablement side's recognition speed is often the moment of awareness. A slow signal-recognition surface is not an engineering-side problem; it is an enablement-side problem, and the council reads it as such.

The specific council-level ask the enablement lead should be able to answer is: "On this incident, how long was it between the underlying event and the moment the enablement side recognised the signal?" The answer is in the incident log. If the answer is uncomfortably long, the close-the-loop surfaces include the signal-recognition surfaces themselves — the dashboard thresholds, the champion-network briefing content, the help-channel escalation criteria. Fixing the signal-recognition surface is a recurring close-the-loop output.

## Three governance-council brief failures

- **The enablement lead over-briefs on substance.** The council's time belongs to the roles with the primary substance (governance for posture, ai-risk-engineer for root-cause). The enablement lead speaking beyond the enablement-side content above crowds out the primary voices. **Prevention:** the four-part read-ahead above is tight; prepare to the four parts.
- **The enablement lead under-briefs on operations.** The council reads the operational-substance section as light because the enablement lead is treating it as support rather than substance. The operational substance *is* substance — the artefact set, the first-hour operations, the close-the-loop. The council needs these to attest to posture. **Prevention:** treat the four-part read-ahead as the enablement lead's primary council content, authored carefully.
- **The enablement lead takes a question that is not theirs.** A council member asks "what caused this at the model level" or "what is the regulator-facing posture." Both are redirect-to-named-owner questions. **Prevention:** have the redirects named and ready; the enablement lead redirects to the correct owner without substituting.

## A short checklist for the enablement lead before an incident-cycle council session

- Incident log ready in its final enablement-side state.
- Four-part read-ahead drafted; reviewed by `head-of-ai-governance` the day before.
- Close-the-loop plan drafted (even if not yet executed); ready to show as evidence of learning.
- Kill-switch runbook revision drafted if the incident surfaced a runbook weakness.
- Three-month verification date in the calendar.
- Rehearsed answer to "how long was it between the event and signal-recognition?"
- Redirects named for the three questions that are not the enablement lead's.

## Summary

- On an incident cycle, the council brief has an incident slot. The enablement lead's contribution is a four-part read-ahead: signal and recognition, first-hour operations, close-the-loop status, and enablement-side lessons for the next rollout.
- The enablement lead does not cover forensic root-cause, severity classification, regulator-facing posture, Article 73 submission substance, or external communications. Named owners cover each.
- Article 73 of the EU AI Act imposes a serious-incident reporting obligation on providers of high-risk AI systems. The enablement lead supports — preservation to the submission standard, timeline documentation, deployment context, non-interference with the clock — but does not author.
- For deployers (most organisations), the obligations are narrower but non-zero; the enablement lead's packet discipline from [Chapter 05](05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md) is the input the governance side uses to inform the vendor and run the organisation's own deployer obligations.
- Parallel obligations across jurisdictions (GDPR Article 33, HIPAA Breach Notification Rule, state laws, sector-specific regimes) attach the same supporting-not-authoring posture. The enablement lead does not run the clocks; the governance and legal side does.
- The enablement side's signal-recognition speed is the organisation's primary constraint on the clocks. A slow recognition surface is an enablement-side problem and a recurring close-the-loop target.
- Three brief failures: over-briefing on substance, under-briefing on operations, taking questions that are not the enablement lead's. Each has a specific prevention.
