# Education Flavour — FERPA, COPPA, and the Ed-Tech Surface

> Three postings in the sample sit in or adjacent to the education flavour: `p-009` an ed-tech vendor (Experis USA posting, AI Enablement Lead at a client in the ed-tech space), `p-013` Ridgeline (AI Enablement Lead at an investment-management platform with education-sector-flavoured content and a learning-platform-style product surface), and `p-017` McGraw Hill (Director, Engineering — AI Enablement at a major educational publisher serving K-12 and higher-ed). The flavour has two distinct shapes — the ed-tech vendor serving education customers, and the education institution itself — and the enablement lead's artifacts differ by which shape the organization sits in.

## The two shapes of the education flavour

The education flavour is almost always *vendor-side* in the posting sample — the organization is an ed-tech company serving education-sector customers, not an education institution directly. The enablement lead's user population is the vendor's own workforce; the regulatory surface arrives *through the customer*. FERPA binds the customer school districts; COPPA binds consumer-facing products reaching under-13 children; the vendor's contractual posture with its customers is where the obligations become live for the vendor's own AI use.

The alternative shape — the enablement lead working inside an education institution (a university, a K-12 district, a state board of education) — is rarer in the current posting sample but present in the broader market. The regulatory surface is similar; the signing surface is different (the institution is the direct regulated entity, and the compliance partner is the registrar, the general counsel, and the data-governance lead rather than an enterprise-customer-success chain).

The chapter covers both shapes; readers identify which they sit in and read accordingly.

## The regulators and standards the enablement lead meets

- **FERPA — the Family Educational Rights and Privacy Act (20 USC 1232g and 34 CFR Part 99).** The baseline federal student-privacy law. Applies to educational agencies and institutions receiving federal funding; indirectly binds vendors through contracts. FERPA defines "education records," student rights to access and amend them, and the circumstances under which personally identifiable information from education records may be disclosed. The "school official" exception (34 CFR 99.31(a)(1)) is the mechanism through which vendors become subject to FERPA-equivalent obligations through contract.
- **The US Department of Education — Student Privacy Policy Office.** The enforcement office for FERPA; publishes guidance including the "Protecting Student Privacy While Using Online Educational Services" guidance and periodic technical-assistance publications. The ed-tech enablement lead reads the latest guidance; it moves.
- **PPRA — the Protection of Pupil Rights Amendment (20 USC 1232h).** Regulates surveys, analyses, and evaluations concerning protected categories of student information in federally-funded programs.
- **COPPA — the Children's Online Privacy Protection Act (15 USC 6501-6505) and the COPPA Rule (16 CFR Part 312).** Governs the collection, use, and disclosure of personal information from children under 13 by commercial websites and online services directed to children. Applies to the ed-tech vendor side primarily; the FTC enforces. The FTC's final amendments to the COPPA Rule — published in the Federal Register April 22, 2025, effective June 23, 2025, with full compliance required by April 22, 2026 — add explicit consent requirements around uses such as training AI models, and are particularly relevant to any AI-tool deployment that processes children's data.
- **State student-privacy laws.** The ed-tech regulatory surface is state-heavy. SOPIPA (California's Student Online Personal Information Protection Act), New York's Education Law 2-d, Colorado's Student Data Transparency and Security Act, Connecticut Public Act 16-189, Louisiana's SB 234, and roughly 40 other state student-privacy statutes compose on top of FERPA. The enablement lead works with legal on the state coverage map; some states (notably New York, California, Connecticut, Illinois) have substantial additional obligations that attach to AI-enabled ed-tech products.
- **IDEA — Individuals with Disabilities Education Act and Section 504 of the Rehabilitation Act.** Special-education and accessibility obligations that attach to any AI tool used in the education of a student with a disability or an individualized education program.
- **State teacher and administrator licensure frameworks.** Not a privacy surface; a professional-responsibility surface. Some states have begun issuing guidance on AI use by licensed educators.
- **Title IX, Title VI, ADA, Section 508.** Civil rights and accessibility obligations that compose with AI tool use.
- **Higher-education-specific obligations.** The Clery Act (campus-crime disclosure); the Jeanne Clery Disclosure Act; the Higher Education Act; the GLBA's safeguards obligations as they apply to higher-education institutions handling financial-aid data; the US Department of Education's cybersecurity obligations under the GLBA Safeguards Rule.
- **General privacy regimes.** GDPR (for European students), state consumer-privacy laws (California's CPRA, Colorado's CPA, Virginia's VCDPA, Connecticut's CTDPA, and others) as they apply to the education-adjacent data flows.

## The data classes that attach

- **Education records (FERPA).** Records directly related to a student that are maintained by an educational agency or institution. The baseline FERPA class.
- **Personally identifiable information from education records.** The FERPA regulations' specific definition — includes direct identifiers, indirect identifiers that together could identify a student, and biometric records. More expansive than many ed-tech teams initially assume.
- **Directory information.** A FERPA subcategory that the educational agency has designated as disclosable; specific handling rules.
- **Children's personal information under COPPA.** For products directed to under-13 children or with actual knowledge of under-13 users.
- **Student-generated content.** Essays, drawings, projects, speech recordings. Education records if maintained by the institution; frequently also personal data under state consumer-privacy laws.
- **Assessment data.** Scores, responses, attempt histories, behavioral telemetry during assessment. Carries FERPA weight and often additional obligations under state assessment statutes.
- **Learning-analytics / behavioral data.** Clickstream, time-on-task, engagement signals. Often the most sensitive class in an AI-enabled product and the least well-controlled. State laws have increasingly begun to name this class explicitly.
- **Special-education records.** IDEA-protected records with their own disclosure rules.
- **Teacher and administrator records.** Personal data of educators, performance data, licensing data. Not FERPA (FERPA protects students) but regulated under state teacher-privacy and employment regimes.
- **Parent / guardian data.** Carries privacy obligations in its own right; communications with parents often have state-specific rules.

## The artifact-level deltas

### Ed-tech vendor-side deltas

The organization is a vendor; the enablement lead's artifacts govern the vendor's own workforce AI use, while the product's compliance is a separate (though coupled) surface.

#### AUP deltas

- **Approved uses** must reflect what customer contracts and the product's privacy posture permit. Many ed-tech products commit contractually to not using customer student data for any purpose other than providing the service. Internal AI use of customer data for "improving the product" is often prohibited by customer contract even if the vendor would otherwise want to.
- **Prohibited uses** must name: no student PII into any tool that is not covered by the product's customer-facing privacy posture; no COPPA-covered data into general-workforce tools; no cross-use of one customer's data to improve services for another customer; no use of student-generated content for AI training without the specific customer-contract permission.
- **Data classes allowed and forbidden** named in FERPA / COPPA / state-law vocabulary.
- **Escalation path** points to the chief privacy officer or equivalent, the general counsel, and (for product-affecting questions) the chief product officer.

#### SOP deltas

- **Customer-contract alignment.** The SOP has a customer-contract alignment rule: when the organization's workforce uses an AI tool on data covered by a customer contract, the tool and workflow must comply with the strictest applicable customer contract. For large ed-tech vendors, this is operationally significant — there may be hundreds of customer contracts with varying terms.
- **Product-vs-internal boundary.** A clear rule distinguishing the product's own AI features (which have their own privacy review) from the vendor's workforce's use of AI tools (which is the enablement lead's primary concern).
- **Children's data handling.** A specific section on COPPA-covered data handling, including the reminder that most general-workforce AI tools are not approved for any children's data.
- **State-law overlay.** A pointer to the state-coverage matrix maintained by legal, with the rule that the tightest applicable state law governs.

#### Intake questionnaire deltas

- **Student data touch — Y/N.**
- **COPPA-covered data touch — Y/N.**
- **Customer-contract touch — Y/N.** (Routing to legal to verify customer-contract terms allow the proposed tool use.)
- **Which customer tiers — K-12 / higher-ed / adult-learning / corporate-training.** Different regulatory overlays.
- **Product feature or internal workflow — Y/N.** If product feature, routing to the product privacy review rather than the enablement intake.

#### Training curriculum deltas

- **Leadership.** The regulatory surface of the customer base; the customer-contract commitments; the state-law exposure map; the FERPA / COPPA / IDEA enforcement history; the sales-and-marketing implications of a privacy incident.
- **Operator.** FERPA / COPPA basics for operators in roles that may touch student data; the customer-contract-alignment rule; the state-law overlay; the children's-data handling discipline.
- **Operator — customer-facing sub-tier.** Customer-success, sales, implementation, and support staff who may interact with district or institutional-level customer data have an additional module on customer-privacy escalation and the common questions customers ask.
- **Specialist.** Deeper coverage for the product and engineering teams whose work defines the product's privacy posture; often coordinated with the AI governance function.

#### Vendor-vetting rubric deltas

- **The sub-vendor privacy posture.** The AI vendor's privacy posture must meet the vendor's own customer commitments. A customer-facing commitment to "no model training on your data" must flow through to any sub-vendor the ed-tech company uses on that customer's data.
- **State-coverage check.** Does the sub-vendor's data-handling meet the strictest applicable state law for the customer base?
- **Children's-data signal.** Can the sub-vendor comply with COPPA's verifiable-parental-consent and other requirements if the data flow includes children's information?

### Education-institution-side deltas

Where the enablement lead is inside the education institution (university, K-12 district, state education board), the artifact deltas shift.

- **The AUP is for the institution's workforce** — faculty, staff, administrators, student workers. Student use of AI tools in coursework is a separate policy surface, typically owned by the registrar or the office of academic integrity, with input from the enablement lead.
- **The SOP's primary data class is education records.** The school-official exception, the directory-information distinction, and the parental-consent / student-rights process are named directly in the SOP.
- **The intake questionnaire** adds explicit fields for whether the tool will be made available to students (triggering a different policy surface) and whether the tool will be used in instruction or in administration (different internal review paths).
- **The training curriculum** has a faculty-specific sub-tier covering the professional responsibilities of educators around student data, academic integrity and AI-generated student work, accessibility obligations in AI-assisted instruction, and the specific state-law overlays applicable in the institution's state.
- **The counterpart roles** include the registrar (owner of FERPA compliance at institutions), the chief academic officer, the general counsel, the data governance officer, and (at higher ed) the FERPA compliance officer. The research integrity officer attends when research-data-touching AI tools are evaluated.

## The two drifts specific to the education flavour

- **"You own product privacy."** Only if the enablement lead's role is defined to include it. In most ed-tech companies, product privacy is owned by a chief privacy officer with a dedicated team; the enablement lead's role is to ensure the *workforce's* AI use composes with the product's commitments, not to re-review every product feature. Keep the boundary clear.
- **"You decide what students may use."** The institution's academic-integrity and student-conduct offices (K-12: the district administration) make student-use policy. The enablement lead advises and provides educator-facing guidance; the policy itself is not the enablement lead's.

## A specific recurring issue — AI-generated student work

A pattern worth naming because it appears across both shapes of the education flavour: the question of how educators, institutions, and ed-tech products should treat AI-generated or AI-assisted student work. The question has at least three facets.

- **Academic integrity.** Is AI-generated student work misconduct? When? Under what disclosure? The academic integrity office owns the policy answer; the enablement lead supports the operational implementation.
- **AI-detection tools.** Tools that claim to identify AI-generated text have known false-positive and false-negative issues; several institutions have moved away from them. The enablement lead is often asked for an opinion; the honest answer is that the current state of detection tools does not support confident determinations, and the policy response should be structured around transparency and assignment design rather than detection.
- **Educator AI use in grading.** Educators using AI tools to grade student work engage both the professional-responsibility surface (do students know? does the institution permit?) and the FERPA surface (is the data flowing to a tool covered by the school-official exception?). Policy and SOP both engage.

The enablement lead is not the owner of any of the three answers but is often the operational center through which they land. Hold the operational center without inheriting the policy.

## Summary

- The education flavour has two shapes: ed-tech vendor and education institution. The enablement artifacts differ by shape.
- FERPA (education records), COPPA (children's personal information), PPRA, IDEA, Section 504, and the dense state-law overlay (SOPIPA, NY 2-d, Colorado, Connecticut, and roughly 40 other state student-privacy statutes) bound the regulatory surface.
- Education records, PII from education records, directory information, COPPA-covered data, student-generated content, assessment data, learning-analytics data, and special-education records are the primary data classes; state law has increasingly named learning-analytics explicitly.
- Vendor-side artifacts emphasize customer-contract alignment and product-vs-workforce boundary; institution-side artifacts emphasize the school-official exception and the faculty-staff-student policy stack.
- Counterpart roles depend on shape: chief privacy officer and general counsel at vendors; registrar, general counsel, chief academic officer, and FERPA compliance officer at institutions.
- Drifts to resist: owning product privacy (vendor side), deciding what students may use (institution side).
- AI-generated student work, AI-detection tools, and educator AI use in grading recur as issues the enablement lead is asked for opinions on; the operational center is the enablement lead's, the policy answers are not.
