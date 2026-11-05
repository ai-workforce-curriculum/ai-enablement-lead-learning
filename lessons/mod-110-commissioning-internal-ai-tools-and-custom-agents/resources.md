# Resources for mod-110 — Commissioning Internal AI Tools and Custom Agents

External references for the chapters and exercises. Primary documentation first; secondary sources where they give the commissioner specific operational calibration. The commissioner is a vocabulary-level reader on architectural references and a primary-source reader on policy, measurement, and governance references.

## Agent and LLM-application architecture — vocabulary reads

The commissioner reads these once per promotion cycle to keep the vocabulary current; depth belongs to the `agentic-systems-architect-learning` track.

- **Anthropic — "Building effective agents."** [https://www.anthropic.com/research/building-effective-agents](https://www.anthropic.com/research/building-effective-agents). The canonical short read on default patterns for agentic systems. Treats workflows (prompt chaining, routing, parallelisation, orchestrator-worker, evaluator-optimiser) and when to reach for an autonomous agent.
- **Anthropic — "Agent capabilities overview."** [https://docs.anthropic.com/en/docs/build-with-claude/agent-capabilities](https://docs.anthropic.com/en/docs/build-with-claude/agent-capabilities). Provider-side framing of tool use, extended thinking, and agentic patterns at the API surface.
- **OpenAI — "Agents guide."** [https://platform.openai.com/docs/guides/agents](https://platform.openai.com/docs/guides/agents). Implementation-leaning read on multi-step agent patterns.
- **LangChain / LangGraph documentation.** [https://langchain-ai.github.io/langgraph/](https://langchain-ai.github.io/langgraph/). Open-source framework vocabulary for stateful agent orchestration.
- **AWS Bedrock Agents.** [https://aws.amazon.com/bedrock/agents/](https://aws.amazon.com/bedrock/agents/). Vendor agent-platform surface commonly evaluated at enterprise scope.
- **Azure AI Foundry.** [https://azure.microsoft.com/en-us/products/ai-foundry](https://azure.microsoft.com/en-us/products/ai-foundry). Microsoft's agent-platform surface.
- **Google Vertex AI Agent Builder.** [https://cloud.google.com/products/agent-builder](https://cloud.google.com/products/agent-builder). Google's agent-platform surface.
- **Model Context Protocol (MCP).** [https://modelcontextprotocol.io/](https://modelcontextprotocol.io/). The emerging interoperability protocol between agent clients and tool/data servers; worth reading at vocabulary depth given its appearance in several agent-platform roadmaps.

## Retrieval-augmented generation and knowledge-gateway references

- **Lewis et al. (2020) — "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks."** [https://arxiv.org/abs/2005.11401](https://arxiv.org/abs/2005.11401). The canonical RAG paper; the commissioner reads to recognise the pattern and its trade-offs.
- **Gao et al. (2024) — "Retrieval-Augmented Generation for Large Language Models: A Survey."** [https://arxiv.org/abs/2312.10997](https://arxiv.org/abs/2312.10997). Survey covering the field's development since the Lewis paper.
- **Vendor documentation for the retrieval surfaces the organisation evaluates** (Pinecone, Weaviate, Elastic, Vertex AI Search, Azure AI Search, Amazon Kendra, etc.). The commissioner reads the data-posture and access-control sections, not the implementation sections.

## Policy and governance references for the guardrails section

- **NIST AI Risk Management Framework (AI RMF 1.0).** [https://www.nist.gov/itl/ai-risk-management-framework](https://www.nist.gov/itl/ai-risk-management-framework). The MAP and MEASURE functions carry commission-stage guidance; MANAGE is the operating counterpart treated in [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).
- **NIST AI RMF Generative AI Profile (NIST AI 600-1).** [https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf). Generative-AI-specific risks layered over the AI RMF.
- **ISO/IEC 42001 — AI management systems.** [https://www.iso.org/standard/81230.html](https://www.iso.org/standard/81230.html). AI-management-system standard; clauses 6.1 (risks and opportunities) and 8.1 (operational planning) are the commission-stage reads.
- **ISO/IEC 23894 — AI risk management.** [https://www.iso.org/standard/77304.html](https://www.iso.org/standard/77304.html). Risk-management companion to 42001.
- **Regulation (EU) 2024/1689 — the EU AI Act.** [https://eur-lex.europa.eu/eli/reg/2024/1689/oj](https://eur-lex.europa.eu/eli/reg/2024/1689/oj). High-risk AI system obligations (Articles 8–15) are the commission-stage reads for tools that may land in high-risk categories.
- **OECD AI principles.** [https://oecd.ai/en/ai-principles](https://oecd.ai/en/ai-principles). Policy-vocabulary ground truth.

## Red-team and evaluation references for Appendix A

- **MITRE ATLAS — Adversarial Threat Landscape for Artificial-Intelligence Systems.** [https://atlas.mitre.org/](https://atlas.mitre.org/). The attack taxonomy the red-team ask coordinates against. The commissioner reads the categories, not the mitigation depth.
- **OWASP Top 10 for LLM Applications.** [https://owasp.org/www-project-top-10-for-large-language-model-applications/](https://owasp.org/www-project-top-10-for-large-language-model-applications/). Application-side vulnerability framing.
- **OWASP AI Exchange.** [https://owaspai.org/](https://owaspai.org/). Broader OWASP guidance on AI security including threat modelling and controls.
- **NIST AI Safety Institute (AISI) materials** and the AI TEVV resources. [https://www.nist.gov/aisi](https://www.nist.gov/aisi). The commissioner reads for vocabulary; depth to the `ai-risk-engineer`.
- **Anthropic — "Responsible Scaling Policy" and model-card transparency reports.** [https://www.anthropic.com/responsible-scaling-policy](https://www.anthropic.com/responsible-scaling-policy). Example of a model-provider's standing safety posture; useful for reading what a provider commits to versus what the commissioner has to add.

## Measurement and eval references

- **Papers With Code — LLM evaluation benchmarks.** [https://paperswithcode.com/task/language-modelling](https://paperswithcode.com/task/language-modelling). Vocabulary surface for the eval-harness patterns the engineer uses.
- **HELM (Holistic Evaluation of Language Models).** [https://crfm.stanford.edu/helm/](https://crfm.stanford.edu/helm/). Stanford's broad evaluation framework; the commissioner reads for methodology, not for benchmark participation.
- **The empirical AI productivity literature cited in [mod-106 Chapter 04](../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md)** — Peng et al. (arXiv:2302.06590), Noy and Zhang (Science 2023), Brynjolfsson, Li and Raymond (NBER), Dell'Acqua et al. The commissioner reads for the methodology discipline that the outcome metric in the brief's Section 3 should honour.

## Commissioning and internal-build references

- **Build vs buy frameworks — vendor-neutral.** The commissioning decision inherits the mod-107 Chapter 03 matrix; the commissioner reads the general build-vs-buy literature (Christensen, Gartner's "Build vs. Buy Decision Matrix" category pages when current) for calibration. <!-- needs-research: specific Gartner / Forrester AI build-vs-buy research notes change annually; refresh citations on each content cycle. -->
- **ClearView Healthcare Partners** — a US-based healthcare-advisory consulting firm; cited in the role evidence (R16, p-019) as an example of an organisation whose senior-manager enablement roles name the productionisation-of-consultant-prototypes pattern. [https://www.clearviewhcp.com/](https://www.clearviewhcp.com/) — the commissioner reads the firm's public role descriptions for the shape of the pattern, not for methodology specifics.
- **DORA metrics (Accelerate: The Science of Lean Software and DevOps, Forsgren/Humble/Kim)** — the engineering-operations measurement vocabulary the maintenance owner uses; referenced in Chapter 06 as the vocabulary for engineer-maintenance resilience in the vendor-vetting rubric at graduation time. [https://dora.dev/](https://dora.dev/).

## Operational references for the hand-off calendar

- **The organisation's governance evidence store** — the same evidence repository the [mod-109 Chapter 02](../mod-109-ai-incident-response-and-enablement-side-rollback/02-the-kill-switch-as-an-operating-artifact.md) kill-switch runbook lives in. The brief, the pilot charter, the acceptance record, and the retirement memo live here; the commissioner does not maintain a separate commissioning-only store.
- **The CoE operating rhythm** named in [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md) — the commissioning pipeline view and the maintenance-owner portfolio view feed the CoE's standing cadences.

## How to use this list

- **Chapter 01 reading.** Anthropic's "Building effective agents" and the OpenAI agents guide are the vocabulary primer. The commissioner reads once and refreshes on each promotion cycle.
- **Chapter 02 reading.** The NIST AI RMF, the ISO/IEC 42001 clause 6.1 and 8.1 sections, and the EU AI Act Article 8–15 reads are the policy-stack references the brief's Section 4 cites.
- **Chapter 03 reading.** The ClearView reference is the pattern example; the commissioner's primary reading is their own organisation's consultant-engagement history and the prototypes currently resident in business-user tools.
- **Chapter 04 reading.** The agent-platform vendor documentation the organisation's architect is evaluating. Depth is defensive — enough to read the architect's proposal, not enough to design.
- **Chapter 05 reading.** The empirical productivity literature from mod-106 Chapter 04 and the HELM methodology reads are the measurement-methodology surfaces; the eval-harness vocabulary from Papers With Code is for coordinating with the engineering team.
- **Chapter 06 reading.** The organisation's governance evidence store documentation and the CoE operating rhythm from [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md).

<!-- needs-research: the agent-platform landscape is early and moves quickly. Verify URLs, product names, and availability on each content cycle. In particular: agent-platform products (Bedrock, Foundry, LangGraph Platform, Vertex AI Agent Builder) have changed branding multiple times; confirm current product names before citing. -->
