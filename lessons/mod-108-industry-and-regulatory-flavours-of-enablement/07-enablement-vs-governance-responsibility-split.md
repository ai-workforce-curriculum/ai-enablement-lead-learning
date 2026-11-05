# Enablement vs. Governance — The Industry-Specific Responsibility Split

> [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) drew the industry-neutral handoff map: the enablement lead (level 45) co-owns artifacts with `head-of-ai-governance` (level 60) and routes control-library architecture to `senior-ai-governance-architect` (level 50). That map survives contact with regulated industries, but the *content* on either side of each arrow changes. This chapter writes the industry-specific split explicitly. The enablement lead owns the operational substance of training, policy co-authoring, and the user-facing envelope; governance owns the regulator-facing control inventory, the risk program architecture, and the certifications that compose with it. A role that confuses the two becomes either the de-facto head of governance (no title, no authority, same accountability) or the de-facto training manager at an organization whose regulators are reading everything else.

## The industry-neutral split, restated

Before the industry-specific overlays, the generic split from mod-101 Chapter 04 and mod-103 Chapter 07:

- **The enablement lead owns the operational substance.** Policy drafts and the redline log; the training curriculum; the approved-tool envelope; the intake questionnaire and its runner; the champion network; the scorecard's adoption and velocity surfaces; the operator and leadership literacy content.
- **`head-of-ai-governance` (L60) owns the regulator-facing posture.** The control inventory; the regulator-engagement cadence; the risk appetite statement; the enterprise-level AI policy; the final approver on high-risk tool deployments; the signer on regulatory submissions.
- **`senior-ai-governance-architect` (L50) owns the control library's architecture.** The intake questionnaire's schema; the risk taxonomy; the control-mapping of controls to standards; the structure of the enterprise AI policy's control references.
- **`ai-governance-analyst` (L15) runs operational governance work.** Control testing, control evidence collection, intake-queue triage inside the governance program.
- **`ai-risk-engineer` (L25, engineering family) owns the technical AI-risk discipline.** Red-teaming, evaluation, model-risk technical work.

The split's purpose is to produce distinct accountabilities rather than overlapping responsibilities. In regulated industries, the overlap pressure is high — regulators want a single named owner for each obligation, and the role closest to the obligation is often pulled toward owning it.

## The industry-specific overlay — healthcare

The HIPAA regulatory posture has been built in healthcare organizations for decades before AI arrived. The governance and privacy teams are mature; the AI enablement lead is the new entrant to a long-standing compliance surface.

- **Enablement lead owns:** The AI-literacy content inside the HIPAA training program (not the whole HIPAA training program). The AI-specific sections of the AUP and the SOP. The intake-questionnaire fields that classify PHI touch and BAA status. The approved-tool envelope's day-to-day composition. The scorecard's adoption surface.
- **Governance (`head-of-ai-governance`, plus privacy officer and security officer) owns:** The HIPAA compliance program. The BAA-signing process with vendors (procurement and legal execute; privacy and security sign off). The breach-assessment workflow and the regulator-notification process. The FDA SaMD determination. The organization's position on the FDA AI/ML-enabled device software functions guidance. The regulatory-engagement cadence with HHS OCR.
- **Senior AI governance architect owns:** The intake-questionnaire's schema including the PHI-and-BAA structure. The control mapping of HIPAA Security Rule standards to AI-tool-specific control statements. The risk taxonomy that distinguishes PHI data flows from non-PHI data flows.

The failure mode in healthcare: the enablement lead inherits the HIPAA training program because the privacy officer's team is small and the enablement lead's team is building training infrastructure anyway. The merged training program drifts because it is run by someone without the professional-responsibility hooks a privacy officer has; the privacy officer loses visibility; a breach-adjacent incident surfaces evidence gaps. The move: integrate the AI-literacy content into the HIPAA training program while leaving the HIPAA training program under the privacy officer; co-sign the integration explicitly.

## The industry-specific overlay — finance

The bank's model risk management function is a distinct governance apparatus with its own hierarchy, reporting line, regulator relationship, and independence expectations under SR 11-7. The AI enablement lead meets this function on tool intake; the split is specific.

- **Enablement lead owns:** The intake-questionnaire fields that flag candidate models for MRM routing. The AUP and SOP as they apply to AI-tool use across the workforce. The training content on model-awareness for non-specialist roles. The regulated-role sub-tier content in coordination with compliance.
- **Governance (`head-of-ai-governance`, MRM, compliance) owns:** The SR 11-7 model risk management program itself. The model inventory. The model validation activities. The ongoing monitoring regime. The regulator-engagement during exam. The FINRA supervision program. The SEC compliance program under 206(4)-7. The CFPB-facing posture on adverse action and UDAAP. The fair-lending compliance program. The AML program.
- **Senior AI governance architect owns:** The intake questionnaire's model-classification schema, co-authored with MRM. The control mapping of SR 11-7 expectations to AI-tool-specific controls. The risk taxonomy aligned with the bank's enterprise-risk framework.

The failure mode in finance: the enablement lead begins making "is it a model?" calls on the fly because MRM is slow and the rollout has momentum. The organization accumulates deployed tools that have not been through MRM; an exam finding results. The move: when MRM is slow, escalate to the CRO or the head of governance — do not substitute enablement judgment for MRM determination. The scorecard should surface the MRM-queue latency explicitly; the latency is a governance-team load issue, not an enablement-side authority issue.

## The industry-specific overlay — legal engineering

Legal engineering is unusual in that the enablement lead and the general counsel's office are often co-located, and the general counsel is a regulator-adjacent role (in their state bar) as well as a signer. The split looks slightly different.

- **Enablement lead owns:** The operational substance of the legal function's AI tool use — approved tools, configurations, SOP, matter-level classification runner, training. For organizations where the legal-engineering lead also co-authors the enterprise AUP, that drafting role is still an enablement role; the signer is the general counsel.
- **Governance (`head-of-ai-governance`, general counsel) owns:** The organization-level AI posture. The professional-responsibility posture of the legal function (the GC's own call, in consultation with practice-area managing counsel). The privilege theory the organization operates under. The state-bar-facing posture. The court-standing-order compliance strategy. The outside-counsel-management AI policy.
- **Senior AI governance architect owns:** The schema of the matter-level AI-use classification. The control mapping of privilege-preserving configurations to specific tool deployments.

The failure mode in legal engineering: the enablement lead begins making professional-responsibility calls because the legal-engineering role sits inside the legal department and the enablement lead is often an attorney themselves. The calls accumulate; the general counsel loses visibility of the professional-responsibility exposure. The move: when wearing the enablement hat, route professional-responsibility questions to the GC or managing counsel, even when the enablement lead has the credential to answer them personally.

## The industry-specific overlay — education

The split in education depends on which shape the organization sits in.

### At the ed-tech vendor

- **Enablement lead owns:** The workforce-side AI-tool envelope and training. The customer-contract-alignment rule inside the SOP. The state-coverage navigation for workforce use.
- **Governance (chief privacy officer, general counsel, `head-of-ai-governance`) owns:** The product's privacy posture. The customer-contract obligations themselves. The state-coverage navigation for the product. The FTC-facing posture on COPPA. The regulator engagement with state attorneys general.
- **Senior AI governance architect owns:** The schema of the student-data classification system (if the organization builds one). The control library for FERPA / COPPA / state-law obligations.

### At the education institution

- **Enablement lead owns:** The institution-workforce AI-tool envelope and training; coordination with the academic-integrity office on operational training for educators.
- **Governance (registrar as FERPA compliance officer, general counsel, `head-of-ai-governance` where it exists) owns:** The FERPA compliance program. The academic-integrity policy on AI-generated student work. The special-education compliance program. The Title IX / ADA / Section 508 compliance programs.
- **Senior AI governance architect owns:** The institutional control library for student-data handling in AI tools.

The failure mode on the vendor side: the enablement lead gets pulled into product-privacy review because the product and workforce AI surfaces overlap. The move: surface the overlap to the chief privacy officer and request a formal boundary rather than quietly absorbing both.

The failure mode on the institution side: the enablement lead drafts the academic-integrity policy on student AI use because the academic-integrity office asks. The move: support the drafting operationally, but the policy signer is the academic-integrity office, not the enablement lead.

## The EU AI Act Article 4 split, revisited

Article 4 is in this module but belongs across the split just like every other obligation. The clean version:

- **Enablement lead owns:** The literacy curriculum content for every tier. The content-update trigger matrix and its running operation. The scope-definition record as co-signed artifact.
- **Governance (`head-of-ai-governance`) owns:** The AI Act compliance program at the organization level. The classification of specific systems under the AI Act's risk tiers. The regulator-engagement with EU member-state market-surveillance authorities. The organizational commitment to Article 4 itself as a compliance posture.
- **Senior AI governance architect owns:** The control mapping of Article 4 and the broader AI Act obligations to internal control statements. The schema of the training evidence catalog.

The specific question an EU member-state authority might ask that illustrates the split: *"Who in your organization is accountable for Article 4 compliance?"* The honest answer is a *two-named* answer: the head of AI governance is accountable for the compliance posture; the enablement lead is accountable for the operational substance that makes the posture defensible. A single-named answer is either wrong (enablement lead isolation) or incomplete (governance lead isolation).

## The four tests the role runs when the split is stressed

When a regulated-industry conversation puts pressure on the enablement lead to absorb a governance obligation, four tests keep the role in scope.

- **The signing-surface test.** Who signs the artifact at the end? If the enablement lead is the drafter but not a signer, the artifact is co-authored; if the enablement lead is both drafter and signer and the artifact is regulator-facing, the role has drifted.
- **The regulator-communication test.** When this obligation comes up in a regulator exam or inquiry, who communicates with the regulator? That role owns the obligation; the enablement lead supports.
- **The professional-responsibility test.** Does this call engage a professional-responsibility surface (medical professional, legal professional, licensed financial professional, licensed educator) that the enablement lead does not hold the license for? If yes, the enablement lead supports; the licensed professional decides.
- **The three-lines-of-defense test.** In regulated industries with a formal three-lines-of-defense structure, which line owns this? Enablement generally sits in first-line operations support; governance in second-line oversight; internal audit in third-line assurance. A first-line role that is making second-line calls has drifted; a second-line role whose operational substance is handled by first-line needs to coordinate.

## What the enablement lead *does not* do, written as a short list

A short, memorable list for when the role is pressured.

- Sign the organization's regulator-facing attestations.
- Make FDA SaMD determinations, SR 11-7 model classifications, privilege waiver assessments, FERPA school-official-exception determinations, or any other regulator-recognized determination of the organization's regulatory status.
- Negotiate BAAs, data processing agreements, or outside-counsel engagement letters.
- Serve as the breach-notification officer or the regulatory-incident-reporting officer.
- Hold a seat on the audit committee as the primary AI-risk reporting role.
- Respond to regulator inquiries or subpoenas without legal counsel on the thread.
- Build the enterprise control inventory or the control library's taxonomy.
- Make the model-validation call or the suitability call on regulated decisions.

The enablement lead's job is to make each of these roles' work easier through operational substance — not to absorb them.

## The two directions the boundary fails

The boundary fails in both directions.

- **Enablement absorbs governance.** The common failure in organizations where the governance function is immature, under-staffed, or recently formed. The enablement lead has momentum, a visible rollout, and an executive relationship; the governance function does not yet. Work flows to the enablement lead. The organization appears to be making progress; the regulatory exposure accumulates behind the scenes. Governance belongs to the governance role regardless of whose desk the work would otherwise fall on; the fix is to escalate the capacity gap, not to backfill it quietly.
- **Governance absorbs enablement.** The common failure in organizations where the governance function is mature, regulator-facing, and risk-averse; a new enablement role lands and governance keeps authoring the user-facing content "until the enablement role is up to speed." A year later the enablement role still does not own the operator-facing surface and is drifting out of the organization. The fix is a clear handoff cadence; governance holds for the first 90 days, then hands off on schedule.

The shape of the boundary is not the problem; the discipline of running it is. Chapters 01 through 06 of this module gave the enablement lead the content on the enablement side of the boundary; this chapter is the frame that keeps the content on its side.

## Summary

- The industry-neutral split from [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) survives contact with regulated industries; the content on each side of the arrows changes per industry.
- Healthcare: enablement owns the AI-literacy slice of the HIPAA training program and the AUP/SOP's AI content; governance (privacy officer, security officer, compliance officer, `head-of-ai-governance`) owns the HIPAA program, BAA signing, breach notification, and FDA SaMD determination.
- Finance: enablement owns the intake-questionnaire fields that route candidate models; governance (MRM, CCO, CRO, `head-of-ai-governance`) owns the SR 11-7 program, the model inventory, FINRA / SEC compliance, fair-lending, AML, and regulator exam response.
- Legal engineering: enablement owns the operational substance of the legal function's AI use; governance (general counsel, practice-area managing counsel, `head-of-ai-governance`) owns the professional-responsibility posture, the privilege theory, and the state-bar and court-standing-order compliance.
- Education: the split varies by shape (vendor vs. institution). Enablement owns the workforce surface; governance owns the product-privacy / FERPA-compliance surface.
- EU AI Act Article 4: enablement owns the curriculum content, trigger matrix, and scope-definition record; governance owns the AI Act compliance posture and regulator engagement.
- Four tests keep the split from drifting: the signing-surface test, the regulator-communication test, the professional-responsibility test, the three-lines-of-defense test.
- The boundary fails in both directions; the discipline of running it is the fix.
