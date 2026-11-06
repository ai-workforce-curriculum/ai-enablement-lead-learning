# Healthcare Flavour — HIPAA, PHI, and the BAA Surface

> Two postings in the sample sit directly in healthcare: `p-018` Navitus Health Solutions (Lead AI Governance & Enablement at a pharmacy benefits manager with direct PHI exposure) and `p-008` WelbeHealth (AI Adoption & Enablement Lead at a PACE-model care provider for frail seniors). Both roles sit on top of an operating model that would be recognizable at any 2,000-to-10,000-person organization, with one addition that reshapes almost every artifact: the organization is a HIPAA covered entity or business associate, the primary data class is protected health information (PHI), and the vendor-vetting rubric cannot approve a tool without a business associate agreement (BAA).

## The regulators and standards the enablement lead meets

- **HIPAA — the Health Insurance Portability and Accountability Act of 1996.** The three operative rules are the Privacy Rule (45 CFR Parts 160 and 164 Subparts A and E), the Security Rule (45 CFR Parts 160 and 164 Subparts A and C), and the Breach Notification Rule (45 CFR Part 164 Subpart D). The US Department of Health and Human Services' Office for Civil Rights (OCR) enforces. HIPAA sorts organizations into covered entities (health plans, health-care clearinghouses, most health-care providers who transmit any health information electronically) and business associates (any entity that creates, receives, maintains, or transmits PHI on behalf of a covered entity). Almost every AI vendor serving a healthcare organization is a business associate under the Act.
- **The HIPAA Business Associate Agreement (BAA).** The specific contract instrument that extends HIPAA obligations to a business associate. No BAA, no PHI; any AI tool that will touch PHI must have a signed BAA with the vendor before PHI enters the tool. This is the single most important gate in the healthcare approved-tool envelope.
- **HITECH — the Health Information Technology for Economic and Clinical Health Act of 2009.** Strengthened HIPAA enforcement, extended direct liability to business associates, and tightened breach notification.
- **42 CFR Part 2 — Confidentiality of Substance Use Disorder Patient Records.** A stricter-than-HIPAA federal regime for patients receiving substance-use-disorder treatment. If any part of the organization's AI surface touches Part 2 data, the handling rules are tighter than HIPAA alone.
- **State medical-privacy laws.** Several states (California's CMIA, New York's SHIELD Act, Texas's HB 300 among others) add on top of HIPAA. When the organization operates across states, the enablement lead coordinates with legal on which state's floor applies where.
- **FDA regulation of Software as a Medical Device (SaMD) and Clinical Decision Support (CDS).** When an AI tool produces output that is used in a clinical decision, FDA regulation may attach. The FDA's AI/ML-based SaMD action plan and the subsequent guidance documents (the 2021 action plan; the October 2021 Good Machine Learning Practice (GMLP) guiding principles jointly issued with Health Canada and the UK MHRA; and the January 2025 draft guidance "Artificial Intelligence-Enabled Device Software Functions: Lifecycle Management and Marketing Submission Recommendations," docket FDA-2024-D-4488) shape what is and is not permitted inside a covered entity's clinical workflow. The enablement lead does not make the SaMD determination; the enablement lead *intakes the question to governance and routes the answer back into the training content and the approved-use list*.
- **The NIST AI RMF 1.0 Generative AI Profile (NIST AI 600-1).** Horizontal, non-industry; carried in alongside HIPAA because US healthcare regulators have begun referencing NIST frameworks in enforcement and guidance. See the resources page.

## The data classes that attach

The HIPAA data taxonomy must be named in the enablement artifacts explicitly. PHI is not "confidential information"; it is PHI, with its own handling rule. A healthcare enablement lead's acceptable-use policy and data-handling SOP name, at minimum, these classes.

- **Protected Health Information (PHI).** Any individually identifiable health information held or transmitted by a covered entity or business associate. Includes clinical data, billing data, insurance information, and the eighteen specific identifiers listed in the Privacy Rule when combined with health information.
- **Electronic PHI (ePHI).** PHI in electronic form; the specific focus of the Security Rule. Nearly all AI-tool-handled PHI is ePHI.
- **De-identified health information.** Information that has been de-identified per the Safe Harbor method (removal of the eighteen identifiers plus the covered entity's actual-knowledge check) or the Expert Determination method (a qualified statistician certifies very small re-identification risk). De-identified information is not PHI; the AUP should still name it and state the rules around re-identification attempts.
- **Limited Data Set (LDS).** A partially-de-identified subset usable for research, public health, or health-care operations under a Data Use Agreement. Has its own handling rule.
- **42 CFR Part 2 data.** Substance-use-disorder treatment records; tighter handling than general PHI.
- **Non-PHI operational data.** HR data, financial data, non-clinical operational data. Handled under the organization's general data classification scheme; the AUP names it so operators know which bucket their work sits in.

## The artifact-level deltas

### AUP deltas

The seven sections of the AUP ([mod-103 Chapter 04](../mod-103-policy-co-authoring-with-governance/04-the-one-page-acceptable-use-policy.md)) all survive the port; four take direct content changes.

- **Approved uses.** Named uses must exclude PHI by default. A line that says "summarize clinical notes you captured yourself" has to be gated on *whether the tool has a BAA*. If no BAA, the line is prohibited regardless of operator intent.
- **Prohibited uses.** Explicitly: no PHI into any AI tool that lacks a BAA; no re-identification attempts against de-identified data; no PHI in prompts to chat tools that log inputs beyond the HIPAA-required retention; no use of AI output as the final step in clinical decisions covered by an FDA SaMD framing without the governance-approved human-oversight pattern.
- **Data classes allowed and forbidden.** Named explicitly in HIPAA language (PHI / ePHI / de-identified / LDS / Part 2 / non-PHI operational), with the specific tools-per-class table maintained alongside the AUP.
- **Escalation path.** Named to include the privacy officer (required role under HIPAA) and the security officer (required role under the Security Rule) in addition to the general escalation surface.

### SOP deltas

The data-handling SOP ([mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md)) takes the heaviest industry overlay.

- **The ten-minute accident path becomes the breach-notification clock entry.** HIPAA Breach Notification requires notice to affected individuals without unreasonable delay and in no case later than 60 days from discovery; notice to HHS within 60 days for breaches affecting 500 or more individuals; notice to prominent media where applicable. The operator-level ten-minute accident path hands off to the breach-assessment workflow run by the privacy officer; the operator needs to know which first step counts as "discovery" for the regulatory clock. Co-author with privacy and legal.
- **Minimum necessary.** HIPAA's "minimum necessary" standard shapes how much PHI operators are permitted to put into a prompt. The SOP names the standard and gives concrete examples of over-inclusion.
- **BAA verification.** The SOP includes the operator's role in verifying that a tool has a BAA before PHI enters it. The approved-tool envelope ([mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md)) does the heavy lifting; the SOP is the last-mile reminder.
- **Audit logging.** The Security Rule's audit-controls standard (164.312(b)) requires covered entities to implement hardware, software, and procedural mechanisms that record and examine activity in systems containing ePHI. The SOP points operators at which tools have audit logs that will be read if something goes wrong.

### Intake questionnaire deltas

The intake questionnaire ([mod-103 Chapter 06](../mod-103-policy-co-authoring-with-governance/06-the-intake-questionnaire.md)) adds required fields.

- **PHI touch — Y/N/Unsure.** With a hard rule: Unsure routes to privacy officer review before progressing.
- **Clinical decision support — Y/N.** Routing to the clinical-informatics lead and the compliance team to assess FDA SaMD implications.
- **BAA status — not-executed / requested / executed.** Not-executed is a hard stop for PHI.
- **De-identification method, if the tool runs on de-identified data.** Safe Harbor or Expert Determination, with the determination record.
- **Part 2 touch — Y/N.** Routing to the Part 2 specialist.

### Training curriculum deltas

The three-tier curriculum from Chapter 02 picks up HIPAA content at each tier.

- Leadership: the HIPAA compliance posture of the organization, the breach-notification process, the enforcement history at peer organizations, the FDA SaMD framing of clinical AI.
- Operator: PHI and minimum necessary in the operator's own role; the BAA-before-PHI gate; the breach-assessment first-step; the escalation to the privacy officer.
- Specialist: deeper Security Rule content (access controls, audit controls, transmission security); the de-identification standards and the re-identification risk-assessment expectations; the FDA SaMD lifecycle where the specialist's role touches it.

### Vendor-vetting rubric deltas

The vendor-vetting rubric ([mod-107 Chapter 06](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/06-the-vendor-vetting-rubric.md)) has a hard gate.

- **BAA availability is a disqualifier.** A vendor that will not sign a BAA is not an approved tool for any PHI-touching use, regardless of how strong the rest of its surface looks.
- **Sub-processor flow-down.** The BAA must flow HIPAA obligations down to sub-processors (the model provider, the hosting infrastructure). Vendors that aggregate many sub-processors need their sub-processor list reviewed.
- **Data residency.** HIPAA itself does not require US-only storage, but many covered entities have contractual commitments that do. Verify.
- **Training-use language.** "We do not train on your data" is table stakes in healthcare; needs to be contractual, not a blog post.

## The counterpart roles

The co-author surface in healthcare has a specific shape. Add these roles to the handoff map from [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md).

- **Privacy Officer.** A named role required under the HIPAA Privacy Rule. Owns the HIPAA privacy program; is the signer on the privacy side of the data-handling SOP; is the escalation point on breach assessment.
- **Security Officer.** A named role required under the HIPAA Security Rule. Owns the ePHI security program; is the signer on the security side of the SOP; the escalation point on ePHI security incidents.
- **Compliance Officer / Chief Compliance Officer.** The organization-level compliance lead, often distinct from the privacy officer. Owns the broader regulatory-compliance program; the signer on the AUP.
- **Clinical informatics lead.** The role that owns the clinical workflow integration and the intersection with electronic health records (EHR). Is a co-author on operator-tier content for clinical roles; a co-author on the intake-questionnaire clinical-decision-support field.
- **General counsel or health-law counsel.** External or internal counsel with healthcare-regulatory depth. The legal signer on the AUP; the escalation point on FDA SaMD framing and Part 2 scope.
- **The medical staff / clinical leadership.** For organizations with direct clinical care, the medical staff (chief medical officer, department chairs) has governance authority over clinical practice that intersects with any AI-assisted clinical workflow. Not a regulatory counterpart, but a required partner.

## The drifts to watch

Three drifts the healthcare-industry enablement lead most often gets pulled into, and the move that keeps the role in scope.

- **"You're the HIPAA trainer."** HIPAA has a workforce-training obligation under the Privacy Rule (164.530(b)) and the Security Rule (164.308(a)(5)). Many organizations have an existing HIPAA training program that long predates any AI work. The drift is for the enablement lead to inherit the organization's entire HIPAA training program because *AI training is near HIPAA training*. The move: the HIPAA training program is the privacy officer's or compliance officer's; the AI literacy program *integrates with* it (shared roster, aligned refresh cadence, coupled triggers) but is not absorbed into it. Write the integration in the training governance note.
- **"You're the BAA negotiator."** Procurement and legal negotiate BAAs. The enablement lead's role is to ensure the BAA gate is in the intake questionnaire and the approved-tool envelope, not to negotiate the BAA. Pull the BAA conversation back to legal every time.
- **"You own the SaMD determination."** The determination of whether a given AI deployment constitutes a medical device under FDA regulation is a regulatory call. Legal and regulatory affairs own it. The enablement lead surfaces the question in the intake questionnaire and incorporates the answer into the AUP's approved-use list; the determination itself is not the enablement lead's.

## The posture when the organization is a business associate, not a covered entity

Some of the healthcare-adjacent organizations in the sample (pharmacy benefits management, PACE-model care coordination) sit as business associates under HIPAA rather than covered entities. The obligations are substantially similar — HITECH extended direct liability to business associates — with three differences worth noting.

- **The BAA is where the organization *signs* as well as the gate it requires of vendors.** The organization has upstream BAAs with its covered-entity customers and downstream BAAs with its own sub-processors (including AI vendors). The downstream obligations must flow through; this is the enablement lead's concern on tool selection.
- **The breach-notification obligations run through the covered entity.** Business associates must notify the covered entity of a breach within the time stipulated in the BAA (default without unreasonable delay and no later than 60 days). The SOP's ten-minute accident path hands off to the covered-entity-notification workflow.
- **The clinical decision support question is often *about* the customer's workflow.** The business associate's tool is used inside the covered entity's clinical workflow. The SaMD determination may attach to the business associate's tool regardless of where the end-use happens. Legal sorts this; the enablement lead carries the intake field.

## Summary

- HIPAA (Privacy Rule, Security Rule, Breach Notification Rule), HITECH, 42 CFR Part 2, state medical-privacy laws, and FDA SaMD / CDS guidance are the regulatory surface the healthcare enablement lead meets.
- PHI is the primary data class; named explicitly in AUP and SOP, mapped to tool-level rules through the approved-tool envelope.
- The BAA is the gate — no BAA, no PHI, period. Named in the intake questionnaire, enforced by the vendor-vetting rubric.
- Artifacts take specific deltas: AUP and SOP absorb the PHI vocabulary; intake adds PHI-touch, CDS, BAA-status, de-identification, and Part 2 fields; training layers HIPAA content on each of the three Article 4 tiers.
- The co-author surface expands to include the privacy officer, the security officer, the compliance officer, the clinical informatics lead, health-law counsel, and (for direct-care organizations) clinical leadership.
- Three drifts to resist: owning the whole HIPAA training program, negotiating BAAs, making the SaMD determination. Each belongs to a named counterpart.
