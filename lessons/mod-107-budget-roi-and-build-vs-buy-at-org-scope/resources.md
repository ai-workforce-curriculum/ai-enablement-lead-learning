# Resources for mod-107 — Budget, ROI, and Build-vs-Buy at Organization Scope

Primary sources first; secondary sources where they add something a primary source does not cover. If a link is broken by the time you read this, search for the title on the issuer's site; URLs move more often than titles. Use these for vocabulary and method — not to transplant specific numbers or benchmarks into your own cost model or ROI projection.

## Standards and frameworks the partnerships operate under

### AI-specific governance frameworks

- **NIST AI Risk Management Framework (AI RMF) 1.0.** Primary source: <https://www.nist.gov/itl/ai-risk-management-framework>. The Manage and Govern functions shape vendor oversight; the Measure function shapes the cost-attribution discipline. Read alongside [Chapter 06](06-the-vendor-vetting-rubric.md). Carried forward from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/resources.md).
- **NIST Generative AI Profile (NIST AI 600-1).** Companion to the AI RMF, reachable from the AI RMF page above. The risk taxonomy for generative systems informs the vendor-vetting rubric's data-and-model-posture dimension.
- **ISO/IEC 42001:2023 — Information technology — Artificial intelligence — Management system.** Standard page: <https://www.iso.org/standard/81230.html>. The leadership and support clauses map onto the budget and resourcing discipline from [Chapter 01](01-the-enablement-cost-model-at-org-scope.md); the operation clause composes with the three-way partnership contract from [Chapter 04](04-partnering-with-procurement-finance-and-it.md).
- **EU AI Act — Regulation (EU) 2024/1689.** Full consolidated text on EUR-Lex: <https://eur-lex.europa.eu/eli/reg/2024/1689/oj>. Article 50 (transparency and user information), the risk-tier classification in Articles 6-29, and the general-purpose AI obligations in Chapter V bound what compliance posture the vendor-vetting rubric must verify for EU-touching deployments.
- **ISO/IEC 23894:2023 — Information technology — Artificial intelligence — Guidance on risk management.** Standard page: <https://www.iso.org/standard/77304.html>. Companion to ISO 42001 at a more technical level; the risk-treatment vocabulary composes with the vendor-vetting rubric.

### Security and data-protection frameworks

- **AICPA SOC 2 — Trust Services Criteria.** Primary source: <https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services>. The reference for what a SOC 2 Type II report actually attests to. Learn the distinction between Type I (design-only) and Type II (operating effectiveness over a period) and the difference between the five Trust Services Criteria (Security, Availability, Processing Integrity, Confidentiality, Privacy).
- **ISO/IEC 27001:2022 — Information security management.** Standard page: <https://www.iso.org/standard/27001>. The international equivalent of SOC 2 at a different control depth; frequently required alongside SOC 2 in cross-border contracts.
- **ISO/IEC 27701:2019 — Privacy information management.** Extension to ISO 27001 for privacy; relevant when the vendor contract touches personal data under GDPR, CCPA, or equivalent.
- **GDPR — Regulation (EU) 2016/679.** Consolidated text on EUR-Lex: <https://eur-lex.europa.eu/eli/reg/2016/679/oj>. Article 28 defines the controller / processor relationship that every enterprise AI contract's DPA structures itself against; Articles 44-50 define the cross-border data-transfer rules that data-residency terms address.
- **EU Standard Contractual Clauses (2021/914).** Commission implementing decision: <https://eur-lex.europa.eu/eli/dec_impl/2021/914/oj>. The standard clauses most cross-border DPAs incorporate for data transfers out of the EEA. Read module 2 (controller-to-processor) as the baseline vendor relationship.
- **FedRAMP — Federal Risk and Authorization Management Program.** Primary source: <https://www.fedramp.gov/>. The U.S. federal cloud-security authorization framework; required for most AI tool deployments touching U.S. federal data. Three impact levels (Low, Moderate, High).
- **HIPAA Security Rule and the Business Associate Agreement.** HHS reference: <https://www.hhs.gov/hipaa/for-professionals/security/index.html>. The baseline for AI tools processing U.S. protected health information; the BAA is the specific contract instrument.
- **PCI-DSS v4.0.** PCI SSC reference: <https://www.pcisecuritystandards.org/document_library/>. The baseline for AI tools handling payment-card data.

### Emerging AI-specific attestations and supply-chain standards

- **ISO/IEC 42005 — AI system impact assessment** and **ISO/IEC 42006 — AI management system audit requirements.** Published and in-progress in the ISO/IEC JTC 1/SC 42 pipeline. <!-- needs-research: specific publication status and dates relevant at time of module publication -->. Emerging references for what a formal AI-system audit will look like; relevant for the vendor-vetting rubric as the industry matures.
- **US NIST AI Safety Institute and the UK AI Safety Institute evaluations.** <https://www.nist.gov/aisi> and <https://www.aisi.gov.uk/>. Government-run evaluation programs for frontier models; relevant for the model-provenance dimension of the vendor-vetting rubric when the vendor's underlying models have participated.
- **Model Cards (Mitchell et al., FAT* 2019).** Reference: <https://arxiv.org/abs/1810.03993>. The academic reference for structured model documentation; some vendors provide model cards or equivalent model-provenance artifacts that the vetting rubric evaluates against.

## Finance and budgeting frameworks

The enablement lead reads these for vocabulary; the Finance partner from [Chapter 04](04-partnering-with-procurement-finance-and-it.md) has deeper fluency. Carrying the vocabulary is what makes the partnership functional.

- **Financial Accounting Standards Board — SFAC No. 8, "Conceptual Framework for Financial Reporting."** FASB page: <https://www.fasb.org/>. The qualitative characteristics of useful information (relevance, faithful representation, comparability, verifiability, timeliness, understandability) are what every executive-facing cost or ROI number should meet. Carried forward from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/resources.md).
- **IFRS — IAS 38 Intangible Assets.** IFRS page: <https://www.ifrs.org/issued-standards/list-of-standards/ias-38-intangible-assets/>. The framework for measuring intangible investments; the vocabulary the Finance partner brings to the ROI methodology conversation when the AI tool capability is an intangible asset.
- **ISO 31000:2018 — Risk management guidelines.** Standard page: <https://www.iso.org/iso-31000-risk-management.html>. The generic risk-management framework; useful for the vendor-concentration and commercial-resilience dimensions of the vetting rubric.
- **COSO Enterprise Risk Management — Integrating with Strategy and Performance (2017).** Reference page: <https://www.coso.org/>. The U.S.-origin enterprise risk-management framework; frequently the organization's standard for how risk is articulated to the board. The enablement-program risks (vendor concentration, model provenance, data boundary) are often reported in this framework's shape.
- **Gartner research on AI business value and ROI methodology.** Gartner publishes periodic research on AI business value frameworks; search their site for "AI ROI framework," "AI business value measurement," "generative AI business case," or "AI center of excellence." <!-- needs-research: specific Gartner report numbers and publication dates relevant at time of module publication -->. Treat Gartner work as analyst reference, not methodology authority.
- **Forrester Total Economic Impact (TEI) methodology.** Forrester reference: <https://www.forrester.com/bold/total-economic-impact/>. Common industry framework for vendor-funded ROI analyses. Useful to read for the method; vendor-commissioned TEI studies are structurally the vendor-number-headline pattern from [mod-106 Chapter 01](../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md) and should be read as marketing, not measurement.
- **MIT Sloan Management Review and MIT CISR — Research on IT value and AI investment.** <https://sloanreview.mit.edu/topic/artificial-intelligence/> and <https://cisr.mit.edu/>. Practitioner-oriented research on how organizations measure and communicate IT and AI investments; useful for benchmarking the cost-model and ROI structures against published practice.

## Procurement and contract-term references

- **International Association for Contract and Commercial Management (World Commerce & Contracting, WorldCC).** <https://www.worldcc.com/>. The professional body for commercial contracting; publishes contracting principles and term benchmarks that the Procurement partner will reference.
- **AI Procurement Toolkit — OECD / UK Government Digital Service.** OECD AI policy observatory: <https://oecd.ai/en/>. UK GDS and the OECD have published AI procurement guidelines for public-sector organizations; useful reference even in private sector for the questions a careful procurement process asks.
- **GSA — Artificial Intelligence Guide for Government.** U.S. GSA AI procurement reference: <https://coe.gsa.gov/coe/ai-guide-for-government/>. Public-sector AI procurement guidance; the model-provenance and sub-processor flow-down questions are explicit.
- **MITRE — Procuring Artificial Intelligence resources.** <https://www.mitre.org/>. MITRE has published AI procurement guidance and acquisition-risk frameworks. <!-- needs-research: specific publication titles and IDs relevant at time of module publication -->.

## Build-vs-buy and capability reference

- **McKinsey, BCG, Deloitte, and Accenture — AI build-vs-buy practitioner research.** These firms publish periodic practitioner research on AI build-vs-buy decisions. <!-- needs-research: specific publication titles, dates, and URLs relevant at time of module publication -->. Treat as practitioner reference, not as methodology authority; the analyses are often vendor-adjacent.
- **Harvard Business Review — AI strategy and build-vs-buy articles.** <https://hbr.org/topic/artificial-intelligence>. Periodic practitioner-oriented articles on AI build-vs-buy; useful for executive-communication framing.
- **CIO.com, InfoWorld, and TechCrunch Enterprise coverage of enterprise AI tool adoption.** Useful for keeping the Column 1-3 tool market picture current as the market evolves. Treat as market intelligence, not as methodology.

## Vendor-specific trust and compliance surfaces (illustrative, not endorsements)

The vendor-vetting rubric's data-and-posture and compliance dimensions check vendor trust pages. Linking the major vendors' trust pages is practical reference; the specific attestations change over time, so read the current page at decision time.

- **OpenAI Trust Portal.** <https://trust.openai.com/>.
- **Anthropic Trust Center.** <https://trust.anthropic.com/>.
- **Microsoft Trust Center.** <https://www.microsoft.com/en-us/trust-center>.
- **Google Cloud Compliance Resource Center.** <https://cloud.google.com/security/compliance>.
- **GitHub Trust Center.** <https://github.com/trust-center>.
- **AWS Artifact and AWS Compliance.** <https://aws.amazon.com/compliance/>.
- **Salesforce Trust.** <https://trust.salesforce.com/>.
- **Atlassian Trust Center.** <https://www.atlassian.com/trust>.
- **Cursor, Windsurf (Codeium), Glean, Harvey.** Vendor trust/security pages are on each vendor's primary site; locate per decision.

Reading these pages well means checking (a) the specific service in scope — SOC 2 Type II on the base platform does not cover the AI add-on automatically, (b) the report date — attestations expire, (c) the sub-processor list — the model provider matters, (d) the data-residency commitments — region availability versus residency guarantee are different, (e) the training-use language — "we do not train on your data" should be a contractual term, not a blog post.

## Change-management and consolidation reference

- **Prosci ADKAR and Research Hub.** <https://www.prosci.com/methodology/adkar>. The change-management framework from [mod-105](../mod-105-champion-networks-and-change-management/README.md); the surfacing-without-stripping discipline in [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) composes with ADKAR's awareness / desire / knowledge / ability / reinforcement stages at each transition step.
- **Kotter — Leading Change (8-step process).** Kotter Inc.: <https://www.kotterinc.com/methodology/>. The organizational-change framework; the tool-consolidation case is structurally a change initiative and benefits from Kotter's shape.

## Adjacent curricula in the AI Career Curriculum ecosystem

The role tracks this module composes with. Read the module READMEs rather than the full curricula.

- [`ai-augmented-team-manager-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning) — level 40, AI Workforce family. The BU-level enablement partner; often the attestation source for Family 4 lines in the cost model and the consolidation-case workflow-interview source.
- [`ai-governance-analyst-learning`](https://github.com/ai-governance-curriculum/ai-governance-analyst-learning) — level 15, AI Governance family. Governance operational work that produces inputs to the vendor-vetting rubric's compliance dimension.
- [`head-of-ai-governance-learning`](https://github.com/ai-governance-curriculum/head-of-ai-governance-learning) — level 60, AI Governance family. The sign-off partner on risk aspects of vendor decisions in regulated contexts.
- [`chief-ai-officer-learning`](https://github.com/ai-workforce-curriculum/chief-ai-officer-learning) — level 70, AI Workforce family. The executive sponsor for enterprise-scope budget and build-vs-buy decisions; understand the altitude the writeups land at.
- [`applied-ai-engineer-learning`](https://github.com/ai-engineering-curriculum/applied-ai-engineer-learning) — level 30, AI Engineering family. The engineering bench a Column 4 (internal build) decision depends on; the build-cost scoping in [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) is read against this role's altitude.
- [`ai-risk-engineer-learning`](https://github.com/ai-engineering-curriculum/ai-risk-engineer-learning) — level 25, AI Engineering family. The technical risk partner on vendor data-boundary and model-provenance review.

## How to use these resources

- **Standards and frameworks are read in primary source.** The NIST AI RMF, ISO 42001, SOC 2 Trust Services Criteria, GDPR Article 28, FASB Conceptual Framework — these are short, durable, and quoted back at you by auditors, Finance, and the head of governance. Read them once; carry the vocabulary into the partnership conversations from [Chapter 04](04-partnering-with-procurement-finance-and-it.md).
- **Vendor trust pages are read at decision time, not once.** Attestations, sub-processors, data-residency terms, and training-use language change. The vendor-vetting rubric from [Chapter 06](06-the-vendor-vetting-rubric.md) is refreshed at the triggers listed there; the vendor trust pages are read fresh at each refresh.
- **Analyst work (Gartner, Forrester, McKinsey, BCG) is read for vocabulary, not for authority.** The frameworks are often useful; the specific numbers are usually vendor-adjacent. Use the structures in your own writeups; produce your own numbers against your own cohort and cost model.
- **Build-vs-buy market intelligence (tool lists, vendor comparisons) changes continuously.** The current-market tool names in [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) and [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) will date; the matrix shape, the ten dimensions, the four columns will not. Use the lecture chapters for method; use trade press for current tool lists.
- **The empirical literature from [mod-106 Chapter 04](../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) carries forward.** The ROI projection method in [Chapter 02](02-projecting-roi-with-confidence-bands.md) grounds its magnitude bands in the Peng, Ziegler, Noy & Zhang, Brynjolfsson/Li/Raymond, and Dell'Acqua papers; those references are not duplicated here but are the primary literature for the projection work.
