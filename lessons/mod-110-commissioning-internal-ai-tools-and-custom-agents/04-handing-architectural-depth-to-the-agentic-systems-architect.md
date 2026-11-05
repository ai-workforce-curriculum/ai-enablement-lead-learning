# Handing Architectural Depth to the Agentic Systems Architect

> The `applied-ai-engineer` is receiving the brief for the ticket-triage copilot. Halfway through kickoff they ask: "Do we build this against the agent platform the architect is standing up, or do we deploy it as a standalone service?" The right answer requires understanding what an agent platform is at the altitude the architect operates. The wrong answer — "whichever is faster" — silently commits the enablement program to a maintenance posture it will regret. This chapter is the vocabulary the commissioner needs for that conversation without pretending to design the platform.

## Why this chapter is short

R20 — agent-platform / architectural depth — is **below-threshold** in the enablement-lead role posture at 0.19 (five of twenty-six postings cite it). The role is consulted on the platform decision, does not design it, and does not own it. The right amount of content for this chapter is the vocabulary the commissioner needs to read an architect's proposal, ask the two or three right questions, and avoid the specific drift of commissioning point tools that are hostile to the platform decision the architect is making concurrently.

Everything deeper than that — control-plane topology, context-layer caching strategy, tool-router design, model-gateway versioning — is `agentic-systems-architect` work. The learner interested in going deeper reads the `agentic-systems-architect-learning` track.

## Three platform surfaces the commissioner meets

An agent platform at enterprise scope typically has three surfaces that the commissioner's briefs land on. The surfaces are vendor-neutral — the specific product chosen (AWS Bedrock Agents, Azure AI Foundry, LangGraph Platform, LangSmith, an in-house platform, or a hybrid) is the architect's call. The commissioner reads for the shape, not the product.

### Surface 1 — The agent control plane

**What it is.** The runtime that executes agents — orchestrates multi-step plans, calls tools, maintains session state, routes between models, handles retries and timeouts, emits observability signals. For point tools (single-LLM-call applications) the control plane is minimal, often just the vendor SDK. For agentic tools (multi-step) the control plane is the place every step runs through.

**Why the commissioner cares.** The commissioning brief's guardrails section (Chapter 02 Section 4) names which actions require human review. The control plane is the surface those constraints are enforced on. If the control plane does not support an approval-gate pattern, or does not support the specific escalation interface the brief names, the guardrails are unenforceable and the brief is signing against a constraint the engineer cannot build to.

**The question the commissioner asks the architect:** "Which guardrail shapes does the control plane support today, and which are roadmap?" A guardrail that is not on the platform's today list is a guardrail the point-tool commission has to implement itself, which adds build cost and maintenance cost the brief should name explicitly.

### Surface 2 — The knowledge gateway

**What it is.** The retrieval surface — vector indexes, document stores, search APIs, the metadata that routes a query to the right source — between the LLM and the organisation's content. In a mature platform, this is a managed service with ingestion pipelines, access-control integration, freshness SLAs, and an observability surface. In a less mature setup it is a hand-wired retrieval index built per tool.

**Why the commissioner cares.** The data posture of the commissioning brief depends on what the knowledge gateway enforces. If access control is at the gateway (every retrieval respects the requester's permissions on the underlying document), then the point-tool commission inherits a strong data-class guarantee from the platform. If access control is implemented per tool, then every commission reproduces the access-control logic, which is exactly the pattern [mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md) names as a policy-drift risk.

**The question the commissioner asks:** "Does the knowledge gateway enforce the data-class constraints my brief's Section 4 is going to carry, or does each commission have to reproduce them?" The answer is load-bearing for the commissioning cadence — if the platform enforces, the brief is lighter and the engineer is faster; if not, Section 4 grows and the build is more expensive.

### Surface 3 — The context layer

**What it is.** The layer that assembles the prompt — the system prompt, the retrieved context, the conversation history, the user's profile and permissions, the policy references the tool has to respect. In a mature platform, context assembly is a declarative pattern the engineer configures; in a less mature setup it is bespoke per tool.

**Why the commissioner cares.** The guardrails section's enforceability depends on context-layer discipline. A tool that is supposed to respect a data-handling policy only respects it if the policy's constraints are visible in the context the LLM reasons over. If the context layer is per-tool, then policy updates ripple through N tools and the enablement program's policy-stack-to-rollout coupling grows brittle (the specific brittleness [mod-103](../mod-103-policy-co-authoring-with-governance/README.md) names as policy-after-rollout drift at ingress).

**The question the commissioner asks:** "When [mod-103](../mod-103-policy-co-authoring-with-governance/README.md) revises the data-handling SOP, how does the change propagate through the context layer to every commissioned tool?" If the answer is "every tool is manually updated," the commissioning cadence will outrun the policy-propagation cadence and the policy stack will fall out of sync. If the answer is "the context layer references a central policy artefact and every tool picks up the update automatically," the platform is doing the enablement program a favour and the brief should lean into it.

## The three recurring consultation surfaces

The commissioner is pulled into platform decisions at three recurring moments. Each has a specific contribution to make without crossing into architectural design.

### Consultation 1 — Platform sizing

The architect is sizing the platform against projected workload. The commissioner contributes the **portfolio of commissioning briefs** the enablement program will produce over the next 12–24 months. Not the specific briefs — many will not have been written yet — but the aggregate shape: how many point tools, how many agentic tools, which user populations, which data classes, which outcome metrics.

**The contribution.** A portfolio projection that gives the architect real workload to size against, not a worst-case guess that over-builds the platform. [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md)'s three-stage selection pipeline and [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md)'s matrix produce the input; the commissioner translates them into a portfolio view for the architect.

**The discipline.** The commissioner does not tell the architect how to size the platform. The commissioner tells the architect what the platform will carry.

### Consultation 2 — Platform constraints feeding the brief

The architect publishes a platform roadmap. The roadmap includes a **constraint set** — "these things the platform will not do; commissions that need those things are out of platform scope." The commissioner reads the constraint set before writing new briefs and uses it to steer problem framing:

- If a candidate commission needs a capability the platform does not support, the commissioner either (a) moves the brief to a greenfield build off-platform, which is expensive and creates a maintenance orphan, (b) re-scopes the commission against what the platform does support, which keeps the brief inside the maintained surface, or (c) routes the capability request back to the architect as a platform roadmap input.
- Option (b) is usually the right default. The commissioner's job is often to find the version of the problem that fits the platform, not to commission capabilities the platform cannot maintain.

**The discipline.** The constraint set is not a negotiation surface at commission time. The commissioner negotiates on platform roadmap at platform-roadmap time; at commission time the constraint set is a fixed input.

### Consultation 3 — Platform-adjacent kill-switch coordination

The [mod-109 Chapter 02](../mod-109-ai-incident-response-and-enablement-side-rollback/02-the-kill-switch-as-an-operating-artifact.md) kill-switch runbook for a commissioned tool has two layers: the tool-level kill-switch (pulling this specific tool offline) and the platform-level kill-switch (pulling the agent platform offline, which pulls every tool on it). The commissioner co-authors the tool-level runbook with the engineer; the platform-level runbook is the architect's responsibility, co-signed with `head-of-ai-governance` (L60) and the IT identity lead.

**The contribution.** The commissioner ensures every commissioned tool's runbook names both layers — the tool-level pull and the platform-level pull — and that the escalation ladder from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) artefact 5 names the architect as the platform-level kill-switch operator.

**The discipline.** The commissioner does not author the platform-level runbook. The commissioner coordinates to ensure the two layers are both operable, drilled, and co-signed.

## The vocabulary trap

A specific drift happens to commissioners who spend too much time with the architect: the commissioner starts using architectural vocabulary with the user cohort, with Finance, and with the governance council. The business sponsors stop understanding the conversation; the governance council reads the commissioning brief as an architecture document and concludes the enablement lead has over-reached.

**The discipline.** The commissioner uses architectural vocabulary **only** with the architect and the engineering family. With the business sponsor, the governance council, the user cohort, and Finance, the commissioner uses the vocabulary of the mod-102 rollout artefact set and the mod-106 scorecard. The architectural vocabulary is a private language the commissioner reads but does not speak at the governance surface.

A test for whether the drift has happened: read the last three commissioning briefs you drafted and the last three communications you sent to the business sponsor. If an architecture term appears in the brief's Section 1 (problem statement) or in a business-sponsor communication, the drift is happening and the brief needs a Chapter 02 Section 1 revision.

## Agent-platform choice and mod-107's Column 2 reappearance

An architect's recommendation to adopt a commercial agent platform (AWS Bedrock Agents, Azure AI Foundry, LangGraph Platform, or equivalent) is a [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) **Column 2 (platform add-on) or Column 3 (industry-specific tool)** decision, not a Column 4 (internal build) decision. The architect runs the technical assessment; the commissioner and the `ai-engineering-manager` co-author the matrix run. The commissioner's contribution is the same as at any Column 2/3 decision: the vendor-vetting rubric from [mod-107 Chapter 06](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/06-the-vendor-vetting-rubric.md), the data-posture read against [mod-103](../mod-103-policy-co-authoring-with-governance/README.md), the operational-fit read against the enablement program.

When the platform is a Column 4 (internal build), the agent-platform build is itself a commission and has its own commissioning brief. The commissioner of the platform is often different from the commissioner of the point tools that run on it — the platform commission is typically signed by `head-of-ai-governance` or by a CoE lead (see [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md)), with the enablement lead contributing the portfolio sizing from Consultation 1 above.

## What the commissioner reads once, not continuously

A small, bounded set of references is the right reading surface for the commissioner on this topic. The vocabulary they produce is the vocabulary the commissioner needs; deeper reading is a signal of drift toward the designer posture from Chapter 01.

- **Anthropic's "Building effective agents" guidance.** A short, canonical read on the shape of agentic systems and the default decisions an agent builder makes. [https://www.anthropic.com/research/building-effective-agents](https://www.anthropic.com/research/building-effective-agents).
- **OpenAI's agents guide.** A parallel, implementation-leaning read on multi-step agent patterns. [https://platform.openai.com/docs/guides/agents](https://platform.openai.com/docs/guides/agents).
- **The agent-platform products the architect is evaluating.** AWS Bedrock Agents, Azure AI Foundry, LangGraph Platform, LangSmith, or the organisation's internal-platform documentation. Read enough to recognise the surface vocabulary; defer depth to the architect.
- **MITRE ATLAS** and **OWASP Top 10 for LLM Applications** as the attack-surface vocabulary. [atlas.mitre.org](https://atlas.mitre.org/) and [owasp.org/www-project-top-10-for-large-language-model-applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/). The commissioner does not design controls; the vocabulary is for coordinating with `ai-risk-engineer` on red-team asks.

The specific landing posture: read once per promotion cycle to keep the vocabulary current; do not read continuously.

## Summary

- R20 is below-threshold (0.19). The commissioner is consulted on platform decisions, does not design them, and does not own them. The chapter is short because the role depth is intentionally bounded.
- Three platform surfaces the commissioner meets: the **agent control plane** (runtime, orchestration, guardrail enforcement), the **knowledge gateway** (retrieval and access control), the **context layer** (prompt assembly and policy propagation). Each has one load-bearing question the commissioner asks the architect.
- Three recurring consultation surfaces: **platform sizing** (commissioner contributes portfolio projection, not architecture), **platform constraints feeding the brief** (commissioner steers problem framing to fit platform scope), **platform-adjacent kill-switch coordination** (two-layer runbook, both drilled).
- The vocabulary trap: using architectural language with business sponsors signals drift. The commissioner speaks the mod-102 rollout and mod-106 scorecard vocabulary at the governance surface; the architectural vocabulary is a private language with the engineering family.
- When the platform is a commercial product, it is a [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) Column 2/3 decision; when internally built, it is a commission whose brief is often signed by `head-of-ai-governance` or a CoE lead, with the enablement lead contributing portfolio sizing.
