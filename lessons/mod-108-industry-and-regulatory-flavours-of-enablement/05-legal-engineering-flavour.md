# Legal-Engineering Flavour — Privilege, Work Product, and the In-House Legal Function

> One posting in the sample sits squarely in the legal-engineering flavour: `p-021` The Walt Disney Company (Director, AI Enablement & Legal Engineering), an enablement role inside the legal function of a major media conglomerate. The role is not a general-counsel role or an outside-counsel role; it is an AI-enablement role whose primary user population is the legal department itself, and whose primary artifact set has to survive the legal-specific data classes — privileged communications, attorney work product, and client-confidence obligations — that outside counsel reviews would read before sign-off.

## What "legal engineering" means in this context

Legal engineering is the discipline of improving legal-work production through systems, data, and process — as distinct from the practice of law itself. It is adjacent to legal operations (which focuses on budget, panel management, metrics) but focuses on the *production surface* of legal work: template libraries, matter management, document automation, contract lifecycle management, due-diligence systems, and increasingly, AI-assisted drafting, review, and research.

The enablement lead in a legal-engineering role has three functions.

- **Enable the in-house legal function to use AI effectively.** Lawyers, paralegals, legal operations staff, legal technologists. The user population is small but senior and highly specialized; the content and the tool envelope look different from a general-workforce rollout.
- **Partner with outside counsel on tools and workflow.** Many legal workflows involve outside law firms. The AI tools and workflows the organization adopts have to compose with outside counsel's own tool stack and billing reality.
- **Partner with the general counsel's office on policy that governs AI use *across the whole enterprise*.** The general counsel is often the signer on the enterprise AUP's legal side (see [mod-103 Chapter 01](../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md)). The legal-engineering enablement lead is often the same person who co-authors that AUP from the legal side, not the enablement side.

The role is structurally closer to [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md) than to pure enablement — commissioning legal-specific tools is often a core part of the job. The flavour is in the data classes and the professional-responsibility obligations.

## The regulators and standards the enablement lead meets

Legal is regulated by professional responsibility rules rather than by a horizontal federal agency, but the obligations are concrete.

- **ABA Model Rules of Professional Conduct.** The model rules each state's bar adapts into its enforceable rules of professional conduct. The rules that engage most directly with AI use:
  - **Rule 1.1 — Competence.** The "technological competence" comment to Rule 1.1 (added 2012, adopted by most state bars) obligates lawyers to keep abreast of changes in relevant technology. AI tools used in legal work engage this.
  - **Rule 1.6 — Confidentiality of Information.** The baseline obligation not to reveal information relating to a client's representation without informed consent. AI tools that process client-confidential information engage this; the obligation is on the lawyer, who cannot delegate it to a tool.
  - **Rule 1.4 — Communication.** The obligation to keep the client reasonably informed. Material use of AI in the representation (especially in a way the client would want to know about) can require client disclosure.
  - **Rule 3.3 — Candor Toward the Tribunal.** AI-generated content filed with a tribunal that contains hallucinated citations or fabricated authorities engages Rule 3.3. The Mata v. Avianca line of cases (and the subsequent court-level standing orders) are the vivid illustrations.
  - **Rule 5.1 and 5.3 — Supervisory Obligations.** Lawyers have supervisory obligations over non-lawyer assistance, including tools. AI tool use in the firm or legal department engages 5.3.
- **ABA Formal Opinion 512 (July 2024) — Generative Artificial Intelligence Tools.** The ABA's own formal ethics opinion on generative AI. Practitioner guidance rather than binding rule; the state bars that have issued their own opinions typically echo or extend it.
- **State bar ethics opinions on AI.** California, New York, Florida, Texas, and most other state bars have issued AI-specific ethics opinions by the time of writing. The specifics vary; the legal-engineering enablement lead works with inside and outside counsel on which state's opinion binds which part of the work. <!-- needs-research: refresh the state-bar opinion list on the next content cycle; the pace of issuance has been continuous. -->
- **Attorney-client privilege and the work-product doctrine.** The common-law doctrines (and the federal Rule 26 work-product protection, and state-law equivalents) that protect certain legal communications and materials from discovery. AI tool use can waive privilege or work-product protection if the tool is a non-privileged third party or if the data leaves the privileged envelope in a way that cannot be defended. The specific tests are context-sensitive and jurisdiction-sensitive; the enablement lead does not render the opinion, but does ensure the tool envelope and the data-handling SOP are co-authored with counsel against the risk.
- **Court-level standing orders on AI.** Several federal and state judges have issued standing orders requiring certification, disclosure, or outright prohibition of AI-generated filings. When the organization litigates, the orders of the specific courts it appears in are binding. Litigation support knows the current list.
- **General data-protection obligations.** The underlying GDPR, CCPA, and state-privacy obligations continue to apply; privileged status does not override them.
- **Industry-overlap obligations.** The legal-engineering function inside a healthcare company handles PHI in a legal matter; inside a bank handles MNPI in a transaction; inside a media conglomerate handles production and talent contracts and personal-image rights. The legal data-handling discipline composes with the industry overlays on top.

## The data classes that attach

The legal-engineering AUP and SOP name the following classes explicitly. They do not reduce to the enterprise AUP's generic "confidential" class.

- **Attorney-client-privileged communications.** Communications between lawyer and client (and the lawyer's working team) made for the purpose of legal advice. Privilege can be waived by disclosure to a third party; AI tools that process the communication must be inside the privilege envelope.
- **Work product.** Material prepared in anticipation of litigation. Protected from discovery under the work-product doctrine; AI tools that process work product are in the same posture as privilege tools.
- **Client confidences (broader than privilege).** Information relating to a client's representation; the Rule 1.6 obligation covers more than strictly privileged communications.
- **Opposing-party confidential information.** Information received under protective order or confidentiality undertaking; AI tool use is constrained by the terms of the order or undertaking.
- **Settlement and negotiation materials.** Often mediation-privileged; often subject to specific confidentiality terms.
- **Regulatory communications.** Correspondence with regulators often has its own confidentiality posture.
- **Matter-management data.** The internal records of matters, budgets, staffing, outside-counsel fees. Not privileged but commercially sensitive.
- **Personal data in legal matters.** Personal data of employees, customers, witnesses, opposing parties — carried in legal matters and subject to the organization's general data-protection obligations and to the specific protective orders of the matter.

The data-class layering is more subtle than in other industries: a single document can carry multiple classes simultaneously (privileged *and* personal-data *and* opposing-party-confidential). The handling rule is the intersection of the applicable classes, not the maximum of them.

## The artifact-level deltas

### AUP deltas

- **Approved uses** are narrowly specified to the legal workflows that the organization has evaluated, with specific tools named. Open-ended "generate first drafts" approvals are too broad for the privilege envelope; approvals name the tool, the document type, and the data class the tool is permitted to touch.
- **Prohibited uses** must name explicitly: no privileged content into a tool not under privilege-protecting commercial terms; no opposing-party-confidential information into any tool; no court filings produced wholly by AI without the human-oversight and citation-verification workflow; no settlement or negotiation material into a shared tool without matter-level approval; no use of AI output as the basis for legal advice to a client without the attorney's professional-responsibility review.
- **Data classes allowed and forbidden** map to the privilege / work-product / client-confidence taxonomy with per-tool tables maintained alongside the AUP.
- **Escalation path** points to the general counsel's office, the managing counsel for the practice area, and (where applicable) the risk committee of the legal department.
- **Outside-counsel interoperability clause.** An explicit section on how the organization's AI tools interact with outside counsel's own AI tools and workflows — what tools the organization authorizes outside counsel to use on its work, what data classes outside counsel can process with those tools, what disclosure the organization expects back.

### SOP deltas

- **Matter-level classification.** The SOP has a matter-level rule: when a matter opens, it is classified for AI-use posture (approved tools, data classes, outside-counsel interoperability). The classification is a signed artifact on the matter file.
- **Privilege-preserving configurations.** Specific tool configurations (self-hosted model, dedicated tenant, no-training commitment, logging posture) that preserve privilege under the organization's legal theory. Not the theory itself — that is the general counsel's call — but the operational SOP.
- **Citation verification.** Specific workflow requirement for any AI output that cites authority: the citation must be verified against the primary source before the output is incorporated into a legal document.
- **Court standing-order compliance.** A reference check against the standing orders of the specific courts the organization appears in.
- **Billing and timekeeping.** AI-assisted work may have specific billing implications under the organization's rate structure, outside-counsel billing guidelines, or client-level engagement terms. The SOP references the billing policy; the billing policy itself is legal-operations-owned.

### Intake questionnaire deltas

- **Privilege touch — Y/N.**
- **Work-product touch — Y/N.**
- **Specific-matter restriction — Y/N (and matter list).** Some matters carry protective-order or confidentiality restrictions that limit tool use beyond the general rules.
- **Court-filing output — Y/N.** Routing to litigation support for standing-order and citation-verification review.
- **Outside-counsel sharing — Y/N.** Routing to outside-counsel-management for interoperability review.
- **Client-disclosure trigger — Y/N.** Rule 1.4 and matter-level engagement terms may require specific disclosure to clients; routing to the managing attorney for the matter.

### Training curriculum deltas

The user population is small, senior, and specialized; the training looks less like a mass-rollout and more like a professional-development program.

- **Leadership tier.** Chief legal officer, general counsel, deputy general counsels. The posture of the legal function on AI use, the professional-responsibility exposure, the outside-counsel-management surface, the standing-order landscape, the ABA opinion read, the enforcement history across peer legal departments.
- **Operator tier — lawyer sub-tier.** Attorneys. Rule 1.1 / 1.6 / 1.4 / 3.3 / 5.3 integration; the privilege-preserving tool envelope; the citation-verification workflow; the client-disclosure triggers; the court-specific standing orders. This content is professional-development-style, often with CLE credit available — coordinate with the state-bar CLE provider process.
- **Operator tier — non-attorney sub-tier.** Paralegals, legal operations staff, legal technologists. Same tool envelope and data-class discipline; different emphasis on their supervisory posture under Rule 5.3 (they are supervised, not supervising).
- **Specialist tier.** Legal engineers, legal technologists, legal-operations systems team. Deeper technical and risk material on the tools themselves.

### Vendor-vetting rubric deltas

- **Privilege-preserving commercial terms.** The vendor contract must support the legal theory under which the organization preserves privilege when using the tool. "We don't train on your data" is table stakes; more is often required (self-hosted or dedicated-tenant deployment, no-logging options, confidentiality terms strong enough that sharing a privileged document with the vendor does not constitute disclosure to a third party under the organization's jurisdiction's privilege law). The general counsel's office makes the privilege call; the enablement lead carries the commercial and operational requirements.
- **Jurisdictional coverage.** Legal engineering serves matters in multiple jurisdictions; the tool's data-handling must compose with the most-restrictive applicable jurisdiction on any given matter.
- **Hallucination posture.** Tools used in legal research or drafting have specific expectations on citation accuracy, retrieval grounding, and uncertainty surfacing. The rubric adds a hallucination-posture dimension.
- **Integration with matter management.** Tools that cannot flow data into the organization's matter-management system are expensive to operate in the privilege envelope.

## The counterpart roles

- **Chief Legal Officer / General Counsel.** The signer on everything legal. The enablement lead works through the general counsel's office rather than around it.
- **Deputy General Counsels / Managing Counsel by practice area.** The practice-area-specific counsel (litigation, M&A, IP, employment, regulatory, commercial) who own the professional-responsibility posture for their practice.
- **Outside Counsel Management lead.** The role (sometimes under legal operations, sometimes under legal) that manages outside-counsel relationships, billing guidelines, and AI-tool interoperability.
- **Legal Operations lead.** The role that owns the budget, metrics, technology, and process discipline of the legal department; often the enablement lead's direct counterpart or supervisor.
- **Chief Information Security Officer (CISO).** The security partner on tool configuration and data-handling implementation.
- **Chief Privacy Officer / Data Protection Officer.** The privacy partner on personal-data handling in legal matters.
- **Risk Committee of the legal department (if one exists).** The internal governance body for legal-function risk; the enablement lead reports to this committee on AI-tool status.
- **Bar Counsel (external).** For the organization's attorneys who are regulated by a state bar; occasionally consulted on professional-responsibility questions through formal or informal channels.

## The drifts to watch

- **"You advise on privilege."** You do not. Privilege is an attorney's call and the general counsel's office owns the theory. The enablement lead writes the *operational substance* that lets the attorneys' theory hold up; the theory itself is legal.
- **"You own citation verification."** You do not. Citation verification is the attorney's professional obligation under Rule 3.3 and Rule 1.1. The SOP routes the workflow; the attorney performs the verification.
- **"You negotiate outside-counsel AI policy."** Outside-counsel management, legal operations, and the general counsel negotiate this. The enablement lead surfaces operational requirements and ensures interoperability from the enablement side.
- **"You handle the standing-order disclosure."** The individual attorney filing in the court handles the disclosure. The enablement lead ensures the SOP points attorneys at the current standing-order list and the citation-verification workflow.

## The two-way flow with the enterprise AUP

A specific pattern worth naming: the legal-engineering enablement lead is often the same person (or on the same team) that co-authors the *enterprise-wide* AUP from the legal side. The enterprise AUP's legal signer is the general counsel; the drafter is often someone working inside legal-engineering or legal-operations. This produces two artifacts that must stay consistent:

- The **enterprise AUP** governing all workforce AI use.
- The **legal-function AUP** governing the legal department's own AI use — a specialized version with the legal data classes and the professional-responsibility overlay.

The two AUPs cannot drift. Changes to one trigger a review of the other. The enablement lead often operates both from the legal-engineering role, which means absorbing both perspectives (user of the legal AUP; co-author of the enterprise AUP) without conflating them. Write the version-coupling rule into the AUP metadata.

## Summary

- Legal engineering is the discipline of improving legal-work production through systems and data; the enablement lead's user population is the in-house legal function, the outside-counsel-interoperability surface, and the enterprise-wide AUP signed off by the general counsel.
- ABA Model Rules 1.1 / 1.6 / 1.4 / 3.3 / 5.3, Formal Opinion 512, state-bar ethics opinions, privilege and work-product doctrines, and court-level standing orders are the regulatory surface.
- The data classes are privileged communications, work product, client confidences, opposing-party-confidential information, settlement materials, regulatory communications, matter data, and personal data in matters — frequently layered on a single document.
- Artifacts take specific deltas: AUP narrows approved uses by tool and document type; SOP adds matter-level classification, privilege-preserving configurations, citation verification, and court-standing-order compliance; intake adds privilege / work-product / court-filing / outside-counsel / client-disclosure fields; training grows CLE-eligible attorney content; vendor rubric adds privilege-preserving commercial terms and hallucination posture.
- Counterpart roles include the general counsel, practice-area managing counsel, outside-counsel management, legal operations, CISO, CPO/DPO, and the risk committee.
- Drifts to resist: advising on privilege, owning citation verification, negotiating outside-counsel AI policy, handling standing-order disclosures.
- The legal-engineering lead often also co-authors the enterprise AUP from the legal side; the two AUPs stay coupled.
