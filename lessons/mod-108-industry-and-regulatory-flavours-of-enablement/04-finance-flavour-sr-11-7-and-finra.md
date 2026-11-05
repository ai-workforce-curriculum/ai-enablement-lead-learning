# Finance Flavour — SR 11-7, FINRA, and the Model-Governance Interface

> Three postings in the sample sit directly in finance: `p-014` Wells Fargo (AI Enablement Lending Lead, a national bank regulated under the Federal Reserve and OCC), `p-012` Dodge & Cox (AI Enablement Manager, SEC-registered investment adviser), and `p-022` Common Securitization Solutions (Director, Transformation & AI Enablement, GSE-adjacent mortgage infrastructure). The regulatory surface they share is wide — bank supervision, securities, consumer financial protection, anti-money-laundering, state financial supervisors — and the piece that most reshapes the enablement artifacts is model risk management under SR 11-7 and its sibling frameworks.

## The regulators and standards the enablement lead meets

### Model risk management

- **SR 11-7 — Supervisory Guidance on Model Risk Management.** Joint Federal Reserve / OCC supervisory letter from 2011 that established the US banking-regulator framework for model risk. Defines "model," establishes the three-lines-of-defense structure for model validation, and specifies ongoing monitoring, documentation, and inventory expectations. The reference document for bank-regulated AI enablement.
- **OCC Bulletin 2011-12** mirrors SR 11-7 for national banks; **FDIC FIL-22-2017** adopts SR 11-7 for state nonmember banks. Same substance, different issuing agency.
- **OCC Bulletin 2013-29 and updates (2017, 2020) on third-party risk management.** Composes with SR 11-7 when the model is vendor-provided; the enablement lead's vendor-vetting rubric meets this bulletin on the vendor side.
- **Interagency Guidance on Third-Party Relationships: Risk Management (June 2023).** The Federal Reserve / FDIC / OCC joint guidance that replaced parts of the prior third-party guidance; sets expectations across the entire third-party risk lifecycle and bites hard on AI/ML tool procurement.
- **SR 15-18 and SR 21-6** extend parts of SR 11-7 to specific use cases (operational-risk capital models, stress testing) that some bank enablement leads will encounter.
- **Model Risk Management expectations at non-bank entities.** SEC-registered investment advisers and broker-dealers operate under different specific frameworks but are expected to apply "appropriate" risk-management discipline to decision-support models used in investment management, trading, and client-facing advice. The specifics vary; the enablement lead reads with compliance.

### Securities and broker-dealer supervision

- **FINRA — the Financial Industry Regulatory Authority.** Self-regulatory organization for US broker-dealers; the rulebook includes Rule 3110 (supervision), Rule 3120 (supervisory control system), Rule 4511 (general recordkeeping), Rule 2210 (communications with the public), and Rule 2111 (suitability). AI-assisted customer communications produced by registered representatives engage every one of these rules.
- **FINRA Regulatory Notice 24-09 (June 2024) — Supervision of AI.** FINRA's reminder notice that firms' existing supervisory, recordkeeping, communications, and suitability obligations apply to AI use. The notice does not create new rules; it operationalizes the existing ones against AI-tool use. The enablement lead reads it as the FINRA-side reference on how the existing rulebook applies.
- **SEC — Securities and Exchange Commission.** For investment advisers, Rule 206(4)-7 (compliance), Rule 204-2 (books and records), and fiduciary-duty interpretations shape the compliance posture. For public companies, Regulation Fair Disclosure, Regulation S-K, and the 2023 cybersecurity disclosure rules (Item 106 of Reg S-K and Form 8-K Item 1.05) compose with AI-related disclosures.
- **SEC Marketing Rule (Rule 206(4)-1).** Governs adviser advertising and testimonials. AI-generated or AI-augmented marketing is in scope.

### Consumer financial protection and fair lending

- **ECOA — the Equal Credit Opportunity Act and Regulation B (12 CFR Part 1002).** Prohibits discrimination in credit transactions on prohibited bases. AI-assisted lending decisions must meet the same adverse-action-notice and non-discrimination standards as any other credit decision.
- **FCRA — the Fair Credit Reporting Act (15 USC 1681 et seq.).** Governs use of consumer reports in credit decisions; adverse-action-notice obligations apply.
- **UDAAP — Unfair, Deceptive, or Abusive Acts or Practices.** CFPB enforcement authority; AI-generated customer communications or AI-driven decisions that mislead or harm consumers engage UDAAP.
- **CFPB Circular 2022-03 and subsequent guidance on adverse-action notices from complex algorithms.** The CFPB has repeatedly stated that adverse-action notices must specify the actual reasons for the decision; a notice that cites "the model said so" does not satisfy ECOA.
- **State fair-lending and consumer-protection regimes.** Several states (notably New York's DFS, Colorado, California) have added AI-specific or AI-adjacent expectations around lending and underwriting. Coordinate with legal.

### Anti-money-laundering and bank operations

- **BSA / AML — Bank Secrecy Act and anti-money-laundering obligations.** AI-assisted transaction monitoring, customer due diligence, and SAR/CTR filings have regulatory expectations around model validation and explainability.
- **OFAC — Office of Foreign Assets Control sanctions obligations.** AI tools that touch payments, counterparty screening, or customer onboarding engage OFAC.

### Horizontal

- **NIST AI RMF 1.0 and the Generative AI Profile.** Non-industry, but increasingly referenced in bank-regulator examinations. See [mod-107 resources](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/resources.md).

<!-- needs-research: refresh SR 11-7 and third-party guidance status on the next content cycle. The 2023 interagency guidance is relatively new and supervisory interpretations are still developing. -->

## The data classes that attach

- **Customer non-public personal information (NPI).** Defined under Gramm-Leach-Bliley Act and Regulation P; the baseline customer-data class that attaches to any consumer-finance organization.
- **Material non-public information (MNPI).** Insider-trading-adjacent information; attaches to publicly-traded issuers, investment managers with inside-information access, and anyone else on the issuer's side of the fence.
- **Customer financial information under GLBA.** A broader set than NPI including non-personal customer records.
- **Payment card data under PCI-DSS.** Applies to any organization handling cardholder data.
- **Communications subject to FINRA recordkeeping.** Written customer communications produced by registered representatives — including AI-assisted communications — are subject to Rule 4511's retention requirements.
- **Books-and-records subject to SEC 17a-4 / 204-2.** Adviser- and broker-dealer-side recordkeeping obligations.
- **Credit-decision records.** ECOA, FCRA, and state fair-lending regimes impose specific retention and content requirements on credit-decision records.

## The artifact-level deltas

### AUP deltas

- **Approved uses must be split by whether the output is a *regulated decision* or a *regulated communication*.** A line permitting "generating draft customer emails" has very different compliance implications for a registered representative than for a back-office operator. The AUP names the distinction and defers the regulated cases to a gated process with supervisory review.
- **Prohibited uses.** Explicitly: no use of AI output as the sole basis for a credit decision; no use of AI to generate adverse-action notices without the model-generated reason-code substitution being verified against the actual decision logic; no insertion of MNPI into tools not isolated for MNPI; no use of AI-generated marketing without the supervisory-review process; no use of AI-assisted recommendations in the fiduciary flow without the suitability-review workflow.
- **Data classes allowed and forbidden.** Named explicitly: NPI, MNPI, credit-decision data, FINRA-communications data, PCI data.
- **Escalation path.** Must include the model risk team (SR 11-7-side), compliance (FINRA / SEC-side), and legal. The escalation path is a routing decision, not a single door.

### SOP deltas

- **MNPI handling.** The SOP has an MNPI-specific track with handling rules that are tighter than the general NPI track. Operators in roles that may touch MNPI (investment-side, deal teams, corporate-development) have a dedicated section.
- **Supervisory review.** Where AI-assisted output enters a FINRA-regulated communications channel, the SOP points to the supervisory-review process (not reproduces it). The enablement lead co-authors the hand-off with compliance.
- **Books-and-records retention.** The SOP names which outputs are books-and-records and which are not; which tools' audit logs are the records of record; and how long each class is retained. Coordinated with recordkeeping and compliance.
- **Adverse-action-notice generation.** If the tool generates draft adverse-action notices, the SOP specifies the review-and-substitute step that converts model-generated placeholder reasons into the actual-reason language required by ECOA.

### Intake questionnaire deltas

- **Model classification — Y/N/Unsure.** Is this candidate tool a "model" under SR 11-7 at the bank, or under the equivalent framework at the non-bank? Unsure routes to the model risk team for determination before intake progresses.
- **Regulated-decision touch.** Does the tool's output enter a regulated decision (credit, suitability, fair-lending-sensitive, trading, AML/BSA)?
- **Regulated-communication touch.** Does the tool's output enter a FINRA-regulated communication channel or an SEC-regulated marketing surface?
- **MNPI touch.**
- **PCI touch.**
- **NY DFS / state-regulator touch.** Fields for any state-level AI-specific regulator the organization is supervised by.

### Training curriculum deltas

- **Leadership.** The organization's model-risk posture and governance; the regulator-engagement cadence; the exam-year preparation; the enforcement history across peer banks; the FINRA Notice 24-09 reading and its implications.
- **Operator (default tier).** NPI handling in the operator's role; the escalation surface; the records-retention rule for AI-assisted work product.
- **Operator — regulated role sub-tier.** Operators in regulated-decision or regulated-communication roles (credit analysts, registered representatives, marketing producers, deal teams, trading support) have additional module content on the specific compliance obligations their role carries. This sub-tier is often where most of the industry-specific curriculum investment lands.
- **Specialist.** SR 11-7 model-validation framework at the depth their role touches it; the model-inventory discipline; the ongoing-monitoring expectations; the documentation standards.

### Vendor-vetting rubric deltas

- **The SR 11-7 flow-down.** For vendor-provided models that will be used in regulated decisions, the vendor contract must permit the model risk team's validation activities, ongoing monitoring access, and documentation access. Vendors that refuse are disqualified for model-regulated use even if they are approved for operator-level use.
- **The third-party-risk-management flow.** The 2023 interagency guidance's expectations are checked explicitly in the rubric.
- **Fourth-party risk.** Sub-processor exposure matters more in finance than in most industries because the ML vendor stack commonly chains multiple providers.
- **Explainability and reason codes.** For any tool that may feed an adverse-action notice, the rubric checks that the tool exposes the reason-code or feature-attribution surface the adverse-action process needs.

## The counterpart roles

The co-author surface in finance is wide. The enablement lead meets each of these on the signing surface for different artifacts.

- **Model Risk Management (MRM) lead.** Owns the SR 11-7 model-validation program; is the escalation point on the model classification question; is a co-author (often the lead author) on the specialist-tier content.
- **Chief Compliance Officer (CCO).** Owns the broader compliance program; the signer on the AUP's compliance section; the escalation point on FINRA / SEC obligations. At broker-dealers, the CCO is a named regulatory role.
- **Chief Risk Officer (CRO).** Owns enterprise risk management; the signer on the enterprise-risk aspects of the enablement artifacts.
- **Fair Lending Officer.** Owns the fair-lending compliance program; the escalation point on ECOA / FCRA and state-regulator fair-lending questions.
- **BSA Officer / AML Officer.** Owns the anti-money-laundering program; the escalation point on transaction-monitoring and customer-due-diligence tool evaluation.
- **General Counsel and specialized counsel.** Securities counsel, consumer-finance counsel, banking-regulatory counsel — each a different specialty.
- **Information Security Officer / CISO.** The security-side signer, with specific depth on financial-services-sector security frameworks (FFIEC, PCI).
- **Business line operations leaders.** The lending-ops lead, the trading-floor operations lead, the wealth-management operations lead. Each owns the operational layer the operators work inside; each is a co-author on their role's operator-tier content.

## The drifts to watch

- **"You own model governance."** You do not. Model risk management is a distinct function with its own hierarchy, three-lines-of-defense discipline, and regulator relationship. The enablement lead's job is to ensure the intake questionnaire catches candidate models, route them to MRM, and absorb MRM's output into the training content and the approved-use list. The drift is for the enablement lead to start making model-validity calls because MRM is slow or because the enablement lead is closer to the user; the move is to escalate up the bank's hierarchy to force MRM capacity, not to absorb MRM's job.
- **"You write the compliance program."** You do not. The CCO owns the compliance program. The enablement lead co-authors the AI-specific slices and ensures training and operator content reflect it; the program document itself is the CCO's.
- **"You decide whether a tool is suitable for a regulated role."** Compliance decides. The enablement lead surfaces the question, provides the operational context, and absorbs the decision; the regulated-role suitability call is not the enablement lead's.
- **"You handle exam prep."** Bank exams, SEC exams, FINRA exams — these are run by compliance, legal, and the business line leaders, with the CCO or an equivalent coordinating. The enablement lead provides evidence from the enablement surface (training rosters, AUP compliance, intake-queue status, approved-tool envelope documentation) and attends as a witness where the exam touches the enablement surface. Not as a primary.

## The "is it a model?" question

The single question the bank enablement lead will be asked most often by compliance counterparts, and the single question they are most expected to have a clear routing answer to:

> "Is the thing we are approving a *model* under SR 11-7?"

The answer is almost never the enablement lead's to give. The enablement lead's job is to ensure the question is *asked* on every intake and that the model-risk team is on the routing surface. SR 11-7 defines a model broadly as a "quantitative method, system, or approach that applies statistical, economic, financial, or mathematical theories, techniques, and assumptions to process input data into quantitative estimates." Generative AI tools and the workflows they enable sit uncomfortably across the edges of the definition; the determination is model-risk's call.

What the enablement lead can do is write the *question* into the intake questionnaire with enough structure that the model-risk team's answer is possible without a two-week debate every time. Three sub-questions that help:

- Does the tool's output affect a decision, estimate, or quantitative judgment?
- Does the output materially influence business or regulatory outcomes (credit, suitability, pricing, reserving, compliance)?
- Is the output used in any way that would need to be defended to a regulator?

An honest "yes" to any one opens the model-risk routing. The enablement lead carries the routing discipline; MRM makes the call.

## The exam-year posture

Every bank, every broker-dealer, every adviser has an exam cadence. In an exam year, the enablement lead's evidence surface is read directly. Three readinesses that matter:

- **The AUP, SOP, and intake questionnaire are co-signed, dated, versioned, and retrievable** by someone other than the enablement lead. Exam teams ask for these artifacts by name.
- **The training completion roster** for the tiers that cover regulated-role operators is current, with non-completer handling documented.
- **The approved-tool envelope** is reconciled with the BAA/MSA/DPA stack. Any tool in use but missing a required contract instrument is a finding waiting to happen.

Prepare for exam year like every year is an exam year. The organizations that do this are the organizations whose enablement lead is not surprised when the examiner's workbook arrives.

## Summary

- SR 11-7 (bank-side model risk management), FINRA Rule 3110 and 24-09 (broker-dealer supervision and AI-specific reminders), the SEC Marketing Rule and Rule 206(4)-7 (adviser-side), ECOA / FCRA / Reg B (consumer-finance), GLBA (customer data), and the interagency third-party-risk guidance together bound the US finance enablement surface.
- NPI, MNPI, credit-decision records, FINRA-communications data, and PCI data are the primary data classes.
- Artifacts take specific deltas: AUP splits approved uses by regulated-decision / regulated-communication status; SOP adds MNPI handling, supervisory review, and records retention; intake adds model-classification, regulated-decision-touch, MNPI, and PCI fields; training grows a regulated-role sub-tier; the vendor rubric adds SR 11-7 flow-down and reason-code explainability.
- The co-author surface includes MRM, CCO, CRO, fair-lending, BSA/AML, specialized counsel, CISO, and business-line operations leads.
- Drifts to resist: owning model governance, writing the compliance program, making regulated-role suitability calls, running exam prep.
- The single question the role meets most often is "is it a model?" — the enablement lead carries the routing discipline, not the determination.
