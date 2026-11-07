# Resources for mod-109 — AI Incident Response and Enablement-Side Rollback

External references for the chapters and exercises. Primary documentation first; secondary sources where they give the enablement side specific operational calibration.

## AI incident precedent surfaces

- **AI Incident Database (AIID)** — the Responsible AI Collaborative's public repository of reported AI incidents, with incident-level entries composed of multiple source reports. The enablement lead reads for incident shapes, policy-coupling weaknesses, communication postures, and regulator-visibility. [incidentdatabase.ai](https://incidentdatabase.ai/)
- **OECD.AI AI Incidents Monitor (AIM)** — the OECD.AI Policy Observatory's incidents tracker, with OECD-jurisdiction-weighted coverage and tags against OECD AI principles. [oecd.ai/en/incidents](https://oecd.ai/en/incidents) and the broader [OECD.AI Policy Observatory](https://oecd.ai/en/).
- **Responsible AI Collaborative** — the maintainer of the AIID; context on the database's methodology and taxonomy. [responsible.ai](https://www.responsible.ai/)

## The EU AI Act — primary text and supporting documents

- **Regulation (EU) 2024/1689 — the EU AI Act.** The primary text, including Article 73 (reporting of serious incidents) and the serious-incident definitions. [EUR-Lex](https://eur-lex.europa.eu/eli/reg/2024/1689/oj).
- **European Commission — AI Office.** The Commission office coordinating AI Act implementation, including serious-incident reporting guidance as it develops. [European Commission AI Office](https://digital-strategy.ec.europa.eu/en/policies/ai-office).
- **European AI Board** — the member-state coordination body under the AI Act; its guidance under Article 73 continues to develop and should be re-read on each content cycle.

## Parallel incident-reporting obligations

- **GDPR Article 33 — Notification of personal data breach to the supervisory authority.** [Article 33, Regulation (EU) 2016/679](https://gdpr-info.eu/art-33-gdpr/); EDPB guidance on breach notification.
- **European Data Protection Board (EDPB)** — guidance on breach notification and, as issued, on AI-specific personal-data obligations. [edpb.europa.eu](https://edpb.europa.eu/).
- **HIPAA Breach Notification Rule.** [45 CFR §§ 164.400–164.414 via the HHS Office for Civil Rights](https://www.hhs.gov/hipaa/for-professionals/breach-notification/index.html).
- **State breach-notification laws (US).** State-by-state references vary; the National Conference of State Legislatures maintains a tracker at [ncsl.org](https://www.ncsl.org/technology-and-communication/security-breach-notification-laws).
- **SR 11-7 — Supervisory Guidance on Model Risk Management.** [Federal Reserve Board](https://www.federalreserve.gov/supervisionreg/srletters/sr1107.htm); joint guidance with the OCC. The incident-adjacent obligations (model-event notification, model-inventory updates) are co-authored between the enablement lead and MRM.
- **FINRA supervision and recordkeeping.** [finra.org](https://www.finra.org/); specific rules depend on the firm's registration and products.
- **FDA — AI/ML-Enabled Medical Device Software Functions.** [FDA Software as a Medical Device (SaMD) guidance](https://www.fda.gov/medical-devices/software-medical-device-samd); incident-reporting obligations attach under MDR where applicable.

## NIST and ISO standards

- **NIST AI Risk Management Framework (AI RMF 1.0).** [NIST AI RMF 1.0](https://www.nist.gov/itl/ai-risk-management-framework). The MANAGE function covers incident response; GOVERN covers the program-level posture the council reads.
- **NIST AI RMF Generative AI Profile (NIST AI 600-1).** [Generative AI Profile](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) as a layer over the RMF for generative-AI-specific risks.
- **ISO/IEC 42001 — AI management systems.** [ISO/IEC 42001](https://www.iso.org/standard/81230.html); nonconformity and incident-handling clauses align with the enablement-side close-the-loop discipline.
- **ISO/IEC 23894 — AI risk management.** [ISO/IEC 23894](https://www.iso.org/standard/77304.html) for the risk-management shape the AI RMF aligns with.
- **NIST SP 800-61 Rev. 2 — Computer Security Incident Handling Guide.** [NIST SP 800-61](https://csrc.nist.gov/pubs/sp/800/61/r2/final). The SOC-side incident-handling discipline the enablement lead's handoff feeds; not an AI-specific document but the baseline SecOps vocabulary.

## Technical reference surfaces for the ai-risk-engineer handoff

These are reading the enablement lead points the ai-risk-engineer and the SOC at, rather than reads directly.

- **MITRE ATLAS — Adversarial Threat Landscape for Artificial-Intelligence Systems.** [atlas.mitre.org](https://atlas.mitre.org/). The ML-adversarial attack taxonomy; essential for prompt-injection, model-extraction, and model-poisoning incident shapes.
- **OWASP Top 10 for LLM Applications.** [owasp.org/www-project-top-10-for-large-language-model-applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/). Developer-facing LLM-specific vulnerability guidance; frames the shape of application-side incidents.
- **OWASP AI Exchange.** [owaspai.org](https://owaspai.org/). Broader OWASP guidance on AI security including threat modelling and controls.
- **NIST AI Testing, Evaluation, Verification, and Validation (TEVV) resources** and the NIST AI Safety Institute materials. [NIST AISI](https://www.nist.gov/aisi).

## Operational references

- **SANS Incident Handler's Handbook.** [SANS reading room](https://www.sans.org/reading-room/). Not AI-specific; useful for the enablement lead on the SOC-side vocabulary they coordinate with.
- **NIST SP 800-150 — Guide to Cyber Threat Information Sharing.** [NIST SP 800-150](https://csrc.nist.gov/pubs/sp/800/150/final). Useful for vendor-coordination patterns during incident response.
- **OECD AI principles.** [oecd.ai/en/ai-principles](https://oecd.ai/en/ai-principles). The policy vocabulary the OECD.AI AIM tags against.

## Tooling

- **Incident-management platforms.** Any organisational IR platform the SOC uses is the primary tool; the enablement lead's log and packet live in the same system or in the organisation's governance evidence store, not in a separate enablement-side tool.
- **Evidence stores.** The organisation's governance-approved evidence repository (often a secure document-management system with retention controls). The enablement lead uses whatever the governance side has approved; the runbook names the specific location.

## How to use this list

- **Chapter 03 reading cadence.** The two precedent surfaces (AIID and AIM) are the primary reading. Set a calendar entry for the monthly scan and the quarterly deep-read.
- **Chapter 05 handoff contracts.** The parallel-obligation references (GDPR Article 33, HIPAA Breach Notification Rule, SR 11-7, FDA) are what the governance-side owner needs to run their clocks; the enablement lead reads once to know the shape and defers the clock-running to governance.
- **Chapter 07 council brief.** The EU AI Act (Article 73), the AI RMF MANAGE function, and the ISO/IEC 42001 nonconformity clauses frame the council's reading of the organisation's incident posture.
- **Exercises 02 and 03.** The MITRE ATLAS and OWASP LLM Top 10 references are the technical ground the ai-risk-engineer-side contract hands off to; the enablement lead does not read at forensic depth but reads to know the vocabulary.

The incident-response regulatory landscape evolves quickly; the enablement lead re-verifies the URLs, the active guidance versions, and the applicability of each reference to the organisation's specific deployment context on each content cycle.
