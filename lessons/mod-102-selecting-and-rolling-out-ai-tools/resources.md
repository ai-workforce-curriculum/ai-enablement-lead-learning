# Resources for mod-102 — Selecting and Rolling Out AI Tools at Organization Scale

Primary sources first; secondary sources only where they add something a primary source does not cover. If a link is broken by the time you read this, search for the title on the issuer's site; URLs move more often than titles.

## Standards and frameworks

- **NIST AI Risk Management Framework (AI RMF) 1.0.** Primary source: <https://www.nist.gov/itl/ai-risk-management-framework>. The Govern / Map / Measure / Manage functions structure the risk-screen you run during Stage 2 candidate evaluation, and the control vocabulary you reuse in the pre-rollout artifact set. Read the Map and Measure functions closely — they map one-to-one onto pilot design and the outcome / workflow / usage measurement frame in Chapter 04.
- **NIST Generative AI Profile (NIST AI 600-1).** Companion profile to AI RMF 1.0 targeted at generative systems, reachable from the AI RMF page above. The risk taxonomy here is what you borrow when you write the "what could go wrong" column of the Stage 2 decision memo for a generative tool.
- **ISO/IEC 42001:2023 — Information technology — Artificial intelligence — Management system.** Standard page: <https://www.iso.org/standard/81230.html>. The management-system clauses (context, leadership, planning, support, operation, performance evaluation, improvement) map onto the rollout artifact set this module teaches — use policy, data-handling SOP, access and offboarding, training package, support and escalation path, kill-switch and rollback plan. Read the clause structure so a rollout bundle you ship can be mapped onto 42001 later without rework.
- **EU AI Act — Regulation (EU) 2024/1689.** Full consolidated text on EUR-Lex: <https://eur-lex.europa.eu/eli/reg/2024/1689/oj>. For this module the deployer-side obligations are what touch rollout: transparency and user information (Article 50), human oversight for high-risk systems (Article 26), and the Article 4 AI-literacy obligation that your training package evidences. Read these before you draft the use policy and user-information notice for any EU-touching rollout.

## Empirical productivity literature (methodology references, not benchmark numbers)

These are the published patterns for *how* to measure AI-induced productivity change at the task level. Read for shape — study design, treatment / control construction, task granularity, outcome specification, threats to validity — and reuse that shape in your own pilot design. Do not cite specific numeric findings into your scorecard or executive narrative; those numbers were generated against different tools, cohorts, and tasks than yours.

- **Peng, Kalliamvakou, Cihon, Demirer — "The Impact of AI on Developer Productivity: Evidence from GitHub Copilot."** arXiv:2302.06590 — <https://arxiv.org/abs/2302.06590>. Randomized controlled trial on a single developer task; the reference design for a coding-assistant pilot with a pre-specified task outcome.
- **Noy & Zhang — "Experimental evidence on the productivity effects of generative artificial intelligence," Science 2023.** DOI entry: <https://www.science.org/doi/10.1126/science.adh2586>. Mid-level professional writing task; the reference design for generative-productivity pilots with knowledge-worker cohorts.
- **Dell'Acqua, McFowland, Mollick, Lifshitz-Assaf, Kellogg, Rajendran, Krayer, Candelon, Lakhani — "Navigating the Jagged Technological Frontier."** Harvard Business School working paper 24-013 — <https://www.hbs.edu/faculty/Pages/item.aspx?num=64700>. Field experiment on consulting work; the reference for how task-fit heterogeneity ("jagged frontier") shows up in pilot results and why aggregate averages can mislead.
- **Brynjolfsson, Li, Raymond — "Generative AI at Work."** NBER working paper 31161 — <https://www.nber.org/papers/w31161>. Customer-support deployment with longitudinal data; the reference for measurement over time, learning curves, and heterogeneous treatment effect by tenure.

Read these as methodology. The number your executive sees should be measured on your cohort, your tool, your tasks — not transplanted from a paper.

## Vendor documentation to read before a pilot

Point your pilot team at the admin / data-handling documentation root of each candidate tool *before* the Stage 2 decision memo is written — not after the contract is signed. The categories below cover the enterprise AI tools most learners will actually pilot. Link to documentation roots, not specific feature pages, so the link outlives feature renames.

- **Enterprise coding assistant category** — read the admin console, enterprise data-handling / privacy, and SSO / audit-log docs of whichever assistant you are piloting (GitHub Copilot, Cursor, Anthropic Claude Code, Windsurf, etc.). <!-- needs-research: verify current documentation roots for GitHub Copilot Business/Enterprise, Cursor Business, Claude Code enterprise admin, and Windsurf enterprise before each content cycle; vendor doc URLs reorganize frequently. -->
- **Enterprise productivity copilot category** — read the admin, data-residency, and compliance documentation of Microsoft 365 Copilot and Google Gemini for Workspace as the two most common pilots at this layer. <!-- needs-research: confirm the current enterprise admin / compliance documentation roots for Microsoft 365 Copilot and Google Gemini for Workspace. -->
- **Enterprise search / RAG category** — read the connectors, indexing boundary, and permission-mirroring docs of whichever enterprise-search or RAG product you are piloting (Glean, Microsoft Copilot with Graph grounding, etc.). The permission-mirroring behavior is the single most important thing to understand before Stage 2; it is the failure mode that produces "ghost-user access" to documents nobody intended to expose. <!-- needs-research: confirm current enterprise documentation roots for Glean and comparable enterprise-search / RAG platforms. -->
- **Enterprise meeting assistant category** — read the recording-consent, retention, and admin-control documentation of Zoom AI Companion, Microsoft Teams Premium meeting AI, and Google Meet AI features. Consent behavior is jurisdiction-sensitive and is the artifact most often missed in rollout. <!-- needs-research: confirm current admin / data-handling documentation roots for Zoom AI Companion, Microsoft Teams Premium AI, and Google Meet AI features. -->

For every pilot, read the vendor docs once end-to-end before Stage 2. Enterprise defaults differ from the consumer defaults the vendor's marketing site describes, and the differences are where rollouts get caught.

## Incident reference

- **AI Incident Database (AIID).** Primary source: <https://incidentdatabase.ai/>. Public catalog of AI incidents; this is the evidence pool for the Chapter 05 pre-mortem — swap speculative "what could go wrong" for recorded "what did go wrong" when you write the failure-mode narrative into the rollout artifact set.
- **OECD.AI Incidents Monitor.** Primary source: <https://oecd.ai/en/incidents-methodology>. Intergovernmental tracking of AI incidents and hazards; complements AIID with a broader methodology and more international coverage. Use both when sampling incidents for a specific industry or modality.

## Credential vocabulary (pointer, not depth)

This module uses credentials only as shared vocabulary with governance, L&D, and change-management partners. Depth lives in [mod-101](../mod-101-role-and-the-org-wide-enablement-operating-model/README.md) (positioning) and [mod-112](../mod-112-career-positioning-and-the-next-step-on-the-ladder/README.md) (which to actually sit).

- **IAPP AIGP — AI Governance Professional.** Program page: <https://iapp.org/certify/aigp/>. The vocabulary your governance partner brings to the Stage 2 risk-screen conversation.
- **Prosci Change Management Methodology and ADKAR model.** Primary source: <https://www.prosci.com/>. The vocabulary your change partner uses when you co-design the rollout communications plan inside the rollout artifact set.
- **ATD — Association for Talent Development.** Capability Model: <https://www.td.org/capability-model>. The vocabulary your L&D partner uses when you co-design the training package inside the rollout artifact set.

## Adjacent curricula in the AI Career Curriculum ecosystem

The other role tracks this module hands work to or consumes work from. Read the module READMEs rather than the full curricula.

- [`applied-ai-engineer-learning`](https://github.com/ai-engineering-curriculum/applied-ai-engineer-learning) — peer, level 30, AI Engineering family. The build of commissioned tools behind Stage 1 "buy-vs-build" and Chapter 06 commissioning handoffs.
- [`agentic-ai-engineer-learning`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning) — AI Engineering family. Multi-step agent build — what you commission when the Stage 1 decision lands on "build" and the solution shape is agentic.
- [`agentic-systems-architect-learning`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning) — AI Engineering family. Architectural depth for commissioned agent systems; your partner when the commissioned build crosses system boundaries.
- [`ai-risk-engineer-learning`](https://github.com/ai-governance-curriculum/ai-risk-engineer-learning) — peer, level 25, AI Governance family. Engineered risk and red-team evidence that feeds the Chapter 06 pre-rollout evidence bundle for generative tools.
- [`ai-governance-analyst-learning`](https://github.com/ai-governance-curriculum/ai-governance-analyst-learning) — level 15, AI Governance family. Operational governance legwork you consume into the Stage 2 risk-screen and the pre-rollout artifact set.
- [`ai-augmented-team-manager-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning) — level 40, AI Workforce family. Team-scope adoption this role hands rollout execution down to inside each BU.

## How to use these resources

- The regulation and standards section must be read in the primary source — paraphrases drift, and the exact wording of Article 4, Article 26, Article 50, and the NIST function definitions is what your governance and legal partners will quote back to you. Read EUR-Lex and the NIST pages themselves, not a vendor's summary.
- The empirical productivity papers are for *methodology*, not for numbers. The study designs tell you how to run a pilot that measures something real; the headline numbers from those studies were generated against a different tool, a different cohort, and different tasks than yours. Copying a published number into your scorecard is the metric-theatre failure mode Chapter 05 pre-mortems.
- The vendor documentation is read once per pilot *before* Stage 2 candidate evaluation closes. Enterprise admin behavior, data-handling defaults, and permission-mirroring semantics are where rollouts fail; a Stage 2 decision memo written without reading these is a decision memo making assumptions the vendor contract will not honor.
- The incident databases are evidence for the pre-mortem — use them to ground the failure-mode narrative in the rollout artifact set in recorded harm, not in speculation. Sample broadly before you write; the first three incidents you find are not representative.
- The credential section is for *vocabulary* at this module's layer. Treat the bodies of knowledge as glossaries you skim before cross-functional meetings; depth and the decision of whether to sit any specific exam belong to [mod-112](../mod-112-career-positioning-and-the-next-step-on-the-ladder/README.md).
