# Resources for mod-106 — Outcome Measurement and Executive Reporting

Primary sources first; secondary sources only where they add something a primary source does not cover. If a link is broken by the time you read this, search for the title on the issuer's site; URLs move more often than titles.

## Empirical AI productivity literature (methodology, not benchmark numbers)

These are the published studies that define *how* AI productivity can be measured credibly. Read for method — pre-registration, outcome specification, control construction, threats to validity — and reuse those methods in your own scorecard. Do not quote the headline effect sizes into your own measurement; see [Chapter 04](04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) on why the numbers do not travel.

- **Peng, Kalliamvakou, Cihon, Demirer — "The Impact of AI on Developer Productivity: Evidence from GitHub Copilot."** arXiv:2302.06590 — <https://arxiv.org/abs/2302.06590>. Randomized controlled experiment on an HTTP-server implementation task; the reference design for a pre-registered primary outcome with telemetry as secondary texture.
- **Ziegler, Kalliamvakou, Li, Rice, Rifkin, Simister, Sittampalam, Aftandilian — "Measuring GitHub Copilot's Impact on Productivity."** Communications of the ACM — <https://cacm.acm.org/research/measuring-github-copilots-impact-on-productivity/>. Measurement-validity companion to Peng et al., examining acceptance rate as a productivity proxy and the gap between perceived and measured productivity. The reference for construct-validity work between telemetry and outcome claims.
- **Noy & Zhang — "Experimental evidence on the productivity effects of generative artificial intelligence."** Science (14 July 2023) — <https://www.science.org/doi/10.1126/science.adh2586>. Randomized experiment on a mid-level professional writing task; the reference for two-dimensional outcome measurement (time plus quality) and heterogeneous treatment effects by skill level.
- **Brynjolfsson, Li, Raymond — "Generative AI at Work."** NBER working paper 31161 — <https://www.nber.org/papers/w31161>. Longitudinal field study of 5,179 customer-service agents; the reference for longitudinal measurement (treatment effects that evolve over months), heterogeneity by tenure, and secondary outcomes beyond productivity (customer satisfaction, agent retention).
- **Dell'Acqua, McFowland, Mollick, Lifshitz-Assaf, Kellogg, Rajendran, Krayer, Candelon, Lakhani — "Navigating the Jagged Technological Frontier."** Harvard Business School working paper 24-013 — <https://www.hbs.edu/faculty/Pages/item.aspx?num=64700>. Field experiment on 758 BCG consultants across 18 tasks; the reference for task-level capability heterogeneity (the "jagged frontier") and the finding that aggregate effects conceal large within-task-type variance.

Read these as a reading loop (see Chapter 04's "reading rhythm" section). Carry them into the methodology appendix of the quarterly review; cite them by title and by the specific method you borrowed.

## Standards and frameworks

- **NIST AI Risk Management Framework (AI RMF) 1.0.** Primary source: <https://www.nist.gov/itl/ai-risk-management-framework>. The Measure function in particular shapes what belongs in the measurement stack — read it alongside Chapter 01. The Govern function shapes the data-governance surface at the measurement interface ([Chapter 06](06-coordinating-with-the-analyst-and-the-team-manager.md)).
- **NIST Generative AI Profile (NIST AI 600-1).** Companion profile targeted at generative systems; reachable from the AI RMF page above. The risk taxonomy informs what the "risks" section of your monthly and quarterly cadences should surface at generative-tool rollouts.
- **ISO/IEC 42001:2023 — Information technology — Artificial intelligence — Management system.** Standard page: <https://www.iso.org/standard/81230.html>. The performance-evaluation and improvement clauses map onto the three-cadence scorecard structure from [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md); a scorecard structured along these clauses can be mapped to 42001 audit evidence without rework.
- **EU AI Act — Regulation (EU) 2024/1689.** Full consolidated text on EUR-Lex: <https://eur-lex.europa.eu/eli/reg/2024/1689/oj>. Article 50 (transparency and user information) and the Article 4 literacy obligations are the regulatory surfaces that the enablement scorecard evidences for EU-touching organizations; treat executive reporting on these obligations as a mandatory scorecard component for in-scope deployments.

## Reporting and financial-communication frameworks

These are the public reference frames for how organizations report material matters to boards and investors. The enablement lead borrows structure and vocabulary here — not accounting literally, but *the discipline of reporting with provenance* — for the quarterly review and the board update.

- **Financial Accounting Standards Board — SFAC No. 8, "Conceptual Framework for Financial Reporting."** FASB page: <https://www.fasb.org/jsp/FASB/Page/LandingPage&cid=1176168367774>. The qualitative characteristics of useful information (relevance, faithful representation, comparability, verifiability, timeliness, understandability) are the shape every executive-facing number should meet. Read the qualitative characteristics section once; it is short and durable.
- **CFA Institute — "Global Investment Performance Standards (GIPS)."** Primary source: <https://www.cfainstitute.org/standards/gips>. The GIPS discipline of reporting with construction methodology, time period, and composition is the reference for how a portfolio metric should be documented. Treat it as a shape to borrow, not a standard to comply with.
- **TCFD and ISSB (IFRS S1/S2) reporting structures.** ISSB page: <https://www.ifrs.org/issued-standards/ifrs-sustainability-standards-navigator/>. Sustainability-reporting frameworks have developed the clearest public treatment of reporting on non-financial metrics with confidence intervals, provenance, and scope boundaries — the problems the enablement lead faces on an AI scorecard. Read the governance and metrics-and-targets sections for structure.

## Writing for executives (craft references)

- **Barbara Minto — "The Pyramid Principle."** Publisher reference: <https://www.barbaraminto.com/>. The canonical reference for top-down, idea-structured executive writing — the BLUF discipline from [Chapter 03](03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) is an application of Minto's pyramid. Read the opening chapters for the SCQA (Situation, Complication, Question, Answer) structure; it is the shape of every useful strategic memo.
- **Amazon's PR/FAQ ("working backwards") document.** Amazon leadership principles reference: <https://www.aboutamazon.com/about-us/leadership-principles>. The six-page memo discipline — narrative-first, assumption-explicit, data-dense — is a working reference for how a program's quarterly review can be structured as a document rather than a slide deck. Search for the public summaries of the PR/FAQ format; the full internal format is proprietary but its outline is widely described.
- **Edward Tufte — "The Visual Display of Quantitative Information."** Publisher: <https://www.edwardtufte.com/tufte/books_vdqi>. Reference for how outcome rollups should be *shown* in the quarterly review — chart junk, data-ink ratio, small multiples for cross-rollout comparability. Read any one of Tufte's books end to end once; the vocabulary will land in every dashboard conversation you have with the analyst.

## Operational references for the measurement stack

- **CHI / ACM — "Measuring Software Developer Productivity."** Umbrella literature in the SPACE framework (Forsgren et al.) is reachable via the Microsoft Research page: <https://queue.acm.org/detail.cfm?id=3454124>. The SPACE framework (Satisfaction, Performance, Activity, Communication, Efficiency) is a reference multi-dimensional measurement structure that composes with the two-dimensional discipline from Noy & Zhang and the longitudinal discipline from Brynjolfsson et al.
- **DORA metrics — DevOps Research and Assessment.** State of DevOps report and framework: <https://dora.dev/>. Reference for team-level outcome measurement in software-engineering workflows; your coding-assistant rollouts should be measurable against a DORA-adjacent baseline where applicable. The "four key metrics" structure is the reference for a small, stable, defensible outcome set.
- **People Analytics bodies of knowledge — SIOP, i4cp, Bersin.** <https://www.siop.org/>, <https://www.i4cp.com/>, <https://www.bersinacademy.com/>. Reference material for operator-level measurement, change-management-health measurement, and the HR partnership that bounds what belongs on an enablement dashboard. The enablement lead reads these for vocabulary when coordinating with HR analytics on operator-level signals that overlap workforce measurement.

## Incident and workforce-impact reference

- **AI Incident Database (AIID).** Primary source: <https://incidentdatabase.ai/>. Public catalog of AI incidents; the reference pool for the *risks* section of the monthly deep-dive and the quarterly review. Scorecard risks named from AIID evidence are more credible than risks named from speculation.
- **OECD.AI Incidents Monitor.** Primary source: <https://oecd.ai/en/incidents-methodology>. Intergovernmental tracking of AI incidents and hazards; use alongside AIID when the risk being surfaced on the scorecard is international or regulatory in scope.
- **OECD — "AI and the Labour Market."** OECD employment outlook reports: <https://www.oecd.org/employment/employment-outlook/>. Reference for how workforce-impact findings from your workflow interviews should be framed in the quarterly review's strategic-risks section; the OECD is the most-cited public source for how AI adoption distributes across labour markets.

## Finance-partnership and ROI references

- **IFRS (International Financial Reporting Standards) treatment of intangible-asset measurement.** IFRS page: <https://www.ifrs.org/issued-standards/list-of-standards/ias-38-intangible-assets/>. Reference for how organizations already measure intangible investments; the vocabulary the Finance partner from [Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md) brings to the ROI methodology conversation.
- **Gartner research on AI ROI methodology.** Gartner publishes periodic research on AI business value frameworks; search their site for "AI ROI framework" or "AI business value measurement." <!-- needs-research: specific Gartner report numbers and publication dates relevant at the time of module publication --> Treat Gartner work as analyst reference, not as methodology authority; the published framings are useful as vocabulary but should not substitute for the methodology work with your own Finance partner.
- **MIT Sloan Management Review — AI research on measurement.** <https://sloanreview.mit.edu/topic/artificial-intelligence/>. Periodic practitioner articles on AI measurement in deployed organizations; useful for benchmarking your scorecard structure against published practice.

## Adjacent curricula in the AI Career Curriculum ecosystem

The other role tracks this module hands work to or consumes work from. Read the module READMEs rather than the full curricula.

- [`ai-augmented-analyst-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-analyst-learning) — level 20, AI Workforce family. The dashboard, pipeline, and metric-definition work this module's scorecard consumes ([Chapter 06](06-coordinating-with-the-analyst-and-the-team-manager.md)).
- [`ai-augmented-team-manager-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning) — level 40, AI Workforce family. The team-level outcome measurement this module aggregates ([Chapter 06](06-coordinating-with-the-analyst-and-the-team-manager.md)).
- [`ai-governance-analyst-learning`](https://github.com/ai-governance-curriculum/ai-governance-analyst-learning) — level 15, AI Governance family. The governance operational work that produces the risk signals for the quarterly review's Section 7.
- [`chief-ai-officer-learning`](https://github.com/ai-workforce-curriculum/chief-ai-officer-learning) — level 70, AI Workforce family. The CAIO is the typical co-author and co-signer of the board-ready quarterly review ([Chapter 03](03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md)); understand the altitude that artifact arrives into.
- [`head-of-ai-governance-learning`](https://github.com/ai-governance-curriculum/head-of-ai-governance-learning) — level 60, AI Governance family. Reviews the risk narrative in the quarterly review for regulated organizations.

## How to use these resources

- The empirical productivity papers are for method, not for numbers. Transplanting a published effect size into your own scorecard is the vendor-number-headline pattern from [Chapter 01](01-the-measurement-stack-at-org-scope.md). Cite method by title in your methodology appendix; measure your own numbers against your own cohort.
- The standards and frameworks section is read in primary source. The qualitative characteristics in the FASB conceptual framework, the Measure function in NIST AI RMF, and the performance-evaluation clauses in ISO 42001 are short, durable, and quoted back at you by auditors and the head of governance. Read them once; carry the vocabulary.
- The executive-writing craft references are for craft, not for ritual. Read Minto's pyramid once; after that, the BLUF discipline from Chapter 03 is the operating form. Read Tufte once per quarter; chart-junk is the single most pervasive failure in enablement-program dashboards.
- The Finance-partnership references bound the shared vocabulary with Finance. The Finance partner from Chapter 05 will have deeper fluency in these than the enablement lead; the enablement lead reads them for shared ground, not for sole authority.
- Adjacent curricula are read at README depth. Cross-track exercises require the interface contract; the depth of the adjacent role lives in that role's own track.
