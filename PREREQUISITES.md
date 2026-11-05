# Prerequisites — AI Enablement Lead track

**Role level:** 45 (org-wide enablement scope — AI Workforce family)
**Track:** `ai-enablement-lead-learning`

This is a leadership track that assumes a solid foundation in both operational AI-adoption at the team scope and general program / people management. Fundamentals are **not** re-taught here — the modules step directly onto org-wide operating model, tool selection and rollout at scale, policy co-authoring, training programs, champion networks, change management, outcome measurement, executive reporting, budget / ROI, industry flavours, incident response, agent commissioning, and AI CoE operations.

## Assumed lower-level curriculum

Complete or be practically fluent in the equivalent of these lower-level tracks before starting:

- **[`ai-augmented-team-manager-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning) — level 40** (AI Workforce family) — the team-scale operating system for AI-augmented work: team adoption roadmap and workflow redesign, review norms and eval commissioning, team productivity and AI-ROI measurement, team-scope enablement programs, agent-delegation at team scope, hiring / performance / feedback with AI in play, team-scope governance and policy translation, vendor / budget / tool selection at team scope. This role runs the org-scope version of the same operating system; team-scope delivery is routinely handed down to this peer-below.
- **[`ai-augmented-analyst-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-analyst-learning) — level 20** (AI Workforce family) — IC-scope AI-augmented analyst work and dashboard construction. This role *commissions* and *reads* dashboards, it does not build them — the analyst track owns the mechanics.
- **[`ai-assisted-software-engineer-learning`](https://github.com/ai-engineering-curriculum/ai-assisted-software-engineer-learning) — level 20** (AI Engineering family) — IC-scope AI-assisted engineering, prompt craft, and agent-authoring mechanics. This role coaches prompt engineering at the *coaching* framing (see [mod-104](.aicg/curriculum-plan.json)); IC-level craft defers down.
- **[`ai-governance-analyst-learning`](https://github.com/ai-governance-curriculum/ai-governance-analyst-learning) — level 15** (AI Governance family) — operational analyst work: AI use-case intake and triage, model / AI-system inventory maintenance, NIST AI RMF / ISO/IEC 42001 / EU AI Act framework crosswalks, first-draft impact assessments, model / system / dataset card authoring at the analyst tier, jurisdictional regulatory tracking, reading eval / red-team / audit evidence into governance records. This role co-authors policy with and consumes artifacts from the governance analyst — the track does not re-teach the intake questionnaire or the analyst-tier model-card walkthrough.

## Assumed working knowledge

Even without holding the equivalent role formally, you should be practically fluent in:

- **General program management** — status reporting, risk registers, decision logs, portfolio coordination across workstreams; Kerzner / Larson at the baseline level, PMP / PgMP vocabulary. This track does not re-teach program management — it layers AI-CoE-specific framing on top.
- **General people management** — 1:1s, feedback, hiring, performance management, budgeting at the baseline level (Grove, Fournier, Larson, Zhuo). This track does not re-teach management fundamentals.
- **Change management** — Prosci ADKAR and Kotter 8-step at the frame level; this track adapts them to AI-specific resistance in [mod-105](.aicg/curriculum-plan.json), but does not teach the underlying change-management discipline from scratch.
- **Working AI-tool fluency** — comfortable using Cursor / Copilot / Claude Code / ChatGPT / Gemini / Claude at the daily-user level; comfortable reading a model card, a system prompt, an eval report, and a red-team summary. This role is the senior customer of AI tools, not the builder — but the role cannot credibly commission, roll out, or coach the use of tools the holder cannot use themselves.
- **Working financial literacy** — reading a cost model, defending a budget, projecting ROI on a bounded initiative, partnering with Finance without being Finance. [mod-107](.aicg/curriculum-plan.json) layers AI-CoE economics on top of this baseline.
- **Executive communication** — writing a one-page memo, an exec pre-read, a board update, a strategic briefing; speaking to a C-suite audience without over-claiming. [mod-106](.aicg/curriculum-plan.json) and [mod-112](.aicg/curriculum-plan.json) add AI-specific framing.
- **Basic AI / ML literacy** — distinguishing a foundation model from a fine-tune, an LLM from a classifier, a retrieval system from a trained model; familiar with the OWASP Top 10 for LLM Applications and the NIST AI RMF at the vocabulary level. The track names each framework but does not teach them from scratch.

## Not assumed, taught here

You do **not** need prior experience with:

- The AI CoE pattern family (hub, hub-and-spoke, federated, embedded). [mod-101](.aicg/curriculum-plan.json) covers the operating-model shapes.
- The three-stage AI tool selection or the full rollout artifact set. [mod-102](.aicg/curriculum-plan.json) covers each stage and artifact.
- The audience-segmented AI literacy curriculum or the role-based playbook. [mod-104](.aicg/curriculum-plan.json) covers audience segmentation, foundational-to-advanced curriculum design, and role-based playbook authoring.
- The champion-network full lifecycle (recruit, train, recognise, retire, two-way feedback). [mod-105](.aicg/curriculum-plan.json) covers the champion network as operating system, not just as an org-chart row.
- The executive AI scorecard. [mod-106](.aicg/curriculum-plan.json) covers weekly rollup, monthly deep-dive, quarterly board-ready review, and the metric-miss narrative.
- The enablement-side AI incident path. [mod-109](.aicg/curriculum-plan.json) covers kill-switch design, rollback, hand-off, and incident-to-policy feedback.
- The commissioning brief for internal AI tools. [mod-110](.aicg/curriculum-plan.json) covers the commissioner framing and prototype-inheritance decision.

## Recommended reading before starting

- [NIST AI Risk Management Framework 1.0 (AI 100-1)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) — front-to-back once, focused on the GOVERN function this role operationalises.
- [EU AI Act, Articles 4 (AI literacy), 14 (human oversight), 50 (transparency)](https://eur-lex.europa.eu/eli/reg/2024/1689/oj) — the deployer obligations the enablement lead implements.
- [OWASP Top 10 for LLM Applications (2025)](https://owasp.org/www-project-top-10-for-large-language-model-applications/) — vocabulary for the risks enablement policy must name.
- [Microsoft Responsible AI Standard](https://www.microsoft.com/en-us/ai/responsible-ai) and [Google AI Principles](https://ai.google/responsibility/principles/) — two public enterprise operating templates.
- [Dell'Acqua et al., "Navigating the Jagged Technological Frontier" (HBS Working Paper 24-013)](https://www.hbs.edu/faculty/Pages/item.aspx?num=64700) — the research foundation for mod-104 / mod-106 framing.
- [Microsoft Work Trend Index — most recent edition](https://www.microsoft.com/en-us/worklab/work-trend-index) and [McKinsey State of AI](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai) — the industry-survey layer this role reads as market context, not as plan.
- A current public system card (Claude, GPT, or Gemini family) — read as an enablement lead would, tracing what you can and cannot promise users.

## Not required, useful to have

- **[IAPP AIGP](https://iapp.org/certify/aigp/)** — AI Governance Professional certification; the most-cited certification in senior AI enablement and governance postings. Not required, treated as a strong signal.
- **[ATD CPTD / APTD](https://www.td.org/credentials)** — Association for Talent Development professional credentials; signal for the training-program side of the role.
- **[Prosci Change Management Certification](https://www.prosci.com/solutions/training-programs/change-management-certification-program)** — signal for the change-management side of the role.
- **[ISO/IEC 42001 Lead Auditor / Lead Implementer](https://www.iso.org/standard/81230.html)** — AI management system implementation; signal for enablement leads working inside ISO-certified organizations.
- **[PMP / PgMP](https://www.pmi.org/certifications)** — signal for the program-management shape of the role at the Director / VP tier.
- Prior experience as a team manager with AI in the delivery stack ([`ai-augmented-team-manager-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning) level 40 is the most common entry path).
- Prior experience in enterprise L&D, change management, or internal consulting is a strong signal — the enablement lead integrates these disciplines rather than inventing them.

## Not in scope for this track (linked out)

- **Engineered risk / red-team / guardrail depth** — harm model authoring, LLM red-team engineering, adversarial-ML, guardrail code, privacy-risk engineering — owned by [`ai-risk-engineer-learning`](https://github.com/ai-governance-curriculum/ai-risk-engineer-learning) (peer, level 25, AI Governance family).
- **Control-library architecture, policy taxonomy, cross-jurisdiction reconciliation** — owned by [`senior-ai-governance-architect-learning`](https://github.com/ai-governance-curriculum/senior-ai-governance-architect-learning) (level 50).
- **AI governance program leadership, board-level reporting, regulator engagement** — owned by [`head-of-ai-governance-learning`](https://github.com/ai-governance-curriculum/head-of-ai-governance-learning) (level 60).
- **Enterprise AI strategy, portfolio P&L, M&A, executive external positioning** — owned by [`chief-ai-officer-learning`](https://github.com/ai-governance-curriculum/chief-ai-officer-learning) (level 70).
- **Build of internal agents, custom AI tools, agent platforms** — owned by [`applied-ai-engineer-learning`](https://github.com/ai-engineering-curriculum/applied-ai-engineer-learning) (peer, level 30), [`agentic-ai-engineer-learning`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning), and [`agentic-systems-architect-learning`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning).
- **IC-level dashboard construction / pipeline building** — owned by [`ai-augmented-analyst-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-analyst-learning) (level 20).
- **IC-level prompt craft, agent authoring mechanics** — owned by [`ai-assisted-software-engineer-learning`](https://github.com/ai-engineering-curriculum/ai-assisted-software-engineer-learning) (level 20).
- **Team-scope AI adoption and team-level enablement** — owned by [`ai-augmented-team-manager-learning`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning) (level 40).
- **Legal opinion** — out of scope; routed to counsel.
- **Contract execution, billing mechanics** — out of scope; routed to procurement and finance.
- **SSO / IAM implementation** — out of scope; routed to IT identity teams.
- **SOC-side incident handling** — out of scope; this role feeds AI-specific signal to SecOps.
