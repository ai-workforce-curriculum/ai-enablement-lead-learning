# The Commissioner Stance — Not the Builder

> A product manager inside the organisation walks into your office with a Google Doc titled "AI Agent for Quarterly Business Reviews." Underneath the title is a hand-drawn boxes-and-arrows diagram. The PM wants to know whether your team can build it. You are not the build. You are the person whose brief is the difference between the engineer getting the problem on the first pass and the engineer spending six weeks discovering what the brief should have said. This chapter is the posture that distinction depends on.

## The uncomfortable truth about the commissioner's authority

Your authority with the AI Engineering family is not positional. You do not manage the engineers. You do not sign their performance reviews. You do not control their roadmap. If an `applied-ai-engineer` (peer, level 30), an `agentic-ai-engineer` (peer, AI Engineering family), or an `agentic-systems-architect` (peer, AI Engineering family) decides they have better uses of their time than building your tool, you have no positional lever to pull. The `ai-engineering-manager` on the other side of the brief can reassign them to a different project tomorrow.

What you have instead is **brief-shaped authority**. You get work out of these peers the same way: you hand them a problem that is specific enough to build against, named at the altitude they build at, scoped so they can finish inside a quarter, and defended against the committee drift that will try to re-scope the project after week two. If the brief is good, the engineer wants to build the tool, because building the tool means moving a visible outcome on the mod-106 scorecard. If the brief is vague, the engineer builds whatever is easiest to interpret from the vague brief, and the commissioner — not the engineer — owns the gap between what got built and what the business needed.

This inverts an instinct every enablement lead carries from the preceding modules. In [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md) the role picks the vendor and the vendor builds the tool to a spec the vendor controls. In mod-110 the role picks the problem and the engineer builds the tool to a spec the role controls. The failure mode is opposite in shape. With a vendor the role can under-specify and still get a usable product. With an engineer the role can under-specify and get nothing usable at all — the engineer builds the specific thing the under-specified brief pointed at, and that thing is almost never what the business needed.

The commissioner's craft is the quality of the brief, nothing else. The rest of the chapter unpacks what that craft looks like in practice.

## The four peers the commissioner coordinates

The AI Engineering family is not one role. The commissioning interface changes shape depending on which engineer is receiving the brief. [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) and [mod-102 Chapter 06](../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md) named the shape. This chapter sharpens it into a working map.

### `applied-ai-engineer` (peer, level 30, AI Engineering family)

The applied-ai-engineer is the default recipient of a commissioning brief for a **point tool** — a specific workflow step the tool is replacing, augmenting, or inserting into. A document-summarisation agent for a specific analyst population. A policy-grounded Q&A bot for a specific support team. A ticket-triage copilot for a specific inbound queue. The applied-ai-engineer is a full-stack builder who will scope the LLM, author the prompts, wire the retrieval, deploy the service, and write the eval harness.

**What the brief gives them:** the problem statement, the user cohort, the guardrails, the success criterion, the budget, the timeline, the maintenance owner.

**What they give back:** a working tool against the success criterion, an eval harness and a baseline score, a runbook the support path can operate, a named maintenance owner inside their team.

**What is out of scope for the brief:** the model choice, the prompt design, the retrieval strategy, the deployment platform. All of these are engineering decisions. The brief constrains the outcome; the applied-ai-engineer chooses the means.

### `agentic-ai-engineer` (peer, AI Engineering family)

The agentic-ai-engineer is the applied-ai-engineer's sibling specialising in **multi-step agent systems** — tools that plan across steps, call tools, maintain state, and surface outputs that are the composition of several LLM calls plus several non-LLM operations. A research agent that queries three databases and composes a memo. A procurement agent that reads a contract, flags clauses, and drafts redlines. A customer-success agent that ingests a call transcript, drafts a follow-up plan, and opens a ticket.

The brief shape is the same as for the applied-ai-engineer with three additions:

- **Step boundaries are part of the guardrails.** Non-negotiable constraints on which tools the agent may call, which data classes it may reach across, and which actions it may take without human review are brief-level guardrails. These are constraints on *behaviour*, not architecture; the engineer still picks the architecture.
- **Escalation to a human is a success criterion, not a failure.** An agent that correctly identifies that it cannot complete a step and routes to a named human is doing its job. The brief says this explicitly or the engineer will optimise for autonomous completion and the first production incident will be an escalation the agent should have made and did not.
- **The eval surface is larger.** Multi-step agent evaluation is a research-active area; the engineer chooses the eval harness, and the commissioner reviews the eval plan as part of the stage-gate (Chapter 02) but does not design it.

### `agentic-systems-architect` (peer, AI Engineering family)

The agentic-systems-architect is the role you do not usually commission a point tool from. They own the **platform surface** the point tools and agents are built against — the agent control plane, the knowledge gateway, the context layer, the eval infrastructure, the observability surface. R20 (agent-platform / architectural depth) is below-threshold at 0.19 in the enablement-lead role posture, which is saying: the enablement lead is consulted on the platform decision, does not design it, and does not own it. Chapter 04 of this module names the vocabulary and the three recurring consultation surfaces.

**What the commissioner sends them:** the portfolio of commissioning briefs the enablement program will produce over the next 12–24 months, so the platform can be sized against real workload, not against an architect's guess at future demand.

**What they send back:** a platform roadmap that the applied-ai-engineer and agentic-ai-engineer builds will target, and a constraint set — "these things the platform will not do; commissions that need those things are out of platform scope and have to be solved differently" — that the commissioner reads before writing briefs.

### `ai-risk-engineer` (peer, level 25, AI Governance family)

The ai-risk-engineer does not sit in the AI Engineering family; they sit on the governance side. [mod-102 Chapter 06](../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md) covered the red-team-ask interface. For a commissioned internal tool, the commissioner routes a red-team ask to the ai-risk-engineer **in parallel with** the build, not after. The red-team ask is dated against the pilot-to-rollout decision, not against the build completion, so that red-team evidence is in the rollout artefact set before anyone outside the pilot cohort sees the tool. Chapter 02 names the red-team ask as part of the brief's non-negotiable guardrails section.

## The three postures that collapse the role on contact with an engineering team

[mod-109 Chapter 01](../mod-109-ai-incident-response-and-enablement-side-rollback/01-the-enablement-side-of-the-incident-path.md) named three posture failures that collapse the role on contact with an incident. Commissioning has its own three. Each mirrors a drift already named in [mod-102 Chapter 06](../mod-102-selecting-and-rolling-out-ai-tools/06-partnering-with-peers-on-evidence-and-build.md); the specific context of a live engineering team is what makes them most likely.

### Posture 1 — The enablement lead becomes the designer

The PM walks in with the boxes-and-arrows diagram. The enablement lead, who has read widely on LLM applications and has opinions, re-draws the diagram and hands it to the engineer as "the design." The brief now contains an architectural choice (which model, which retrieval pattern, which deployment target) that the engineer did not make and will not defend when it breaks.

**Why it happens:** the enablement lead is the fastest-moving role in the room, has more AI-vocabulary exposure than the business-side requestor, and feels competent to sketch a design because the surfaces are familiar.

**What goes wrong:** the engineer has to build what the brief specifies rather than what the problem calls for. When the design misses, the engineer has no standing to redesign without a brief revision. The organisation has lost the engineer's judgement on the architecture — the specific thing the organisation hired the engineer to apply.

**The move that stops it:** the brief names the **outcome** and the **constraints**, not the **means**. The problem statement is one paragraph, not one diagram. The non-negotiable guardrails are behaviours the tool must not exhibit, not techniques the engineer must use to prevent them. Chapter 02 writes this discipline into the brief template.

### Posture 2 — The enablement lead becomes the product manager

The brief is signed. The build begins. The enablement lead, feeling responsible for the project, inserts themselves into the engineer's weekly standup, reviews code, arbitrates prompt-design decisions, and starts negotiating on behalf of the user cohort with the engineering team. The brief becomes a conversation; scope creeps in both directions.

**Why it happens:** the enablement lead feels accountable for the business outcome and wants to stay close. The engineering team has not been given a counterpart product-managing voice. The vacuum pulls the enablement lead into product-manager posture.

**What goes wrong:** the brief stops being the load-bearing artefact. Decisions get made in channel rather than in signed artefacts. The engineer's manager (`ai-engineering-manager`) does not have a clear surface to push back on, because scope drift is happening through informal exchanges the manager does not see. When the project misses, there is no artefact the enablement lead and the engineering manager can point to that holds the agreement they both signed against.

**The move that stops it:** the brief is the only decision surface. Weekly reviews happen against the brief. Scope changes are brief revisions co-signed by the enablement lead and the engineering manager; nothing less. A product-manager role, if one is needed, is named in the brief as an escalation partner, not improvised. Chapter 06 names the hand-off calendar that keeps the brief live without turning the commissioner into a product manager.

### Posture 3 — The enablement lead becomes the apologist

The tool is built. It does what the brief asked. The business outcome does not move. The enablement lead, over-invested in the project surviving, defends the tool against evidence that the mod-106 scorecard is not shifting. The failure is explained as "early days," "operator uptake lag," "attribution noise" — the exact three patterns of theatre mod-106 names as failure modes.

**Why it happens:** commissioning is scarcer and more visible than rolling out a vendor tool. A failed commission reads, inside the organisation, as a failed enablement decision. The sunk cost — the brief, the engineer's time, the pilot runway — makes retirement feel like personal loss.

**What goes wrong:** the scorecard begins to carry a line item the organisation cannot trust. Future commissions are harder to defend because the preceding commission is still on the books under a theatre narrative. The honest no-go call (Chapter 03) that should have been made six weeks ago is now twelve weeks overdue and more painful.

**The move that stops it:** the measurement plan (Chapter 05) and the signing surface (Chapter 06) carry pre-written retirement criteria. A commission that misses three consecutive outcome readings on the scorecard, or that is blocked at pilot after a named decision gate, transitions to a graduate-or-retire decision rather than drifting. The commissioner's authority is strongest when it can name its own retirements.

## The one-paragraph test a request has to pass before it becomes a commission

Not every AI request is a commission. Many are vendor-shaped and belong back in the [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) three-stage selection. Some are policy requests that belong in [mod-103](../mod-103-policy-co-authoring-with-governance/README.md). Some are measurement questions that belong in [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md). A rough but load-bearing test — the one-paragraph test — distinguishes a real commission from the others:

- **The problem is named at the workflow step.** Not "we want an AI thing"; "service agents spend forty percent of a ticket resolving which of four systems owns the answer." If the problem is not nameable at this altitude, go back to intake.
- **The commercial envelope has already been checked.** The three-stage selection decision has run; no tool in the approved-tool envelope and no reasonable commercial point tool satisfies the problem statement. If the envelope has not been checked, the brief is a short-circuit around the build-vs-buy matrix and it collapses on contact with Procurement.
- **A maintenance owner exists.** Not a maintenance commitment in the abstract; a named human or team that has committed to owning the tool after the engineer hands it off. If the maintenance owner cannot be named today, the tool is already dying.
- **The business outcome is measurable on the mod-106 framework.** Not a bespoke dashboard, not a usage-telemetry flourish; the same outcome / workflow / usage stack every other rollout in the portfolio is measured on. If the outcome is not measurable on that framework, the brief will be at odds with the scorecard the enablement program defends to the board.

A request that passes the one-paragraph test becomes a commission and moves to Chapter 02 for the full brief. A request that fails any one of the four lines returns to intake with the specific gap named. The commissioner's first discipline is to **not commission** more than it is to commission.

## The relationship to mod-107's Column 4

[mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) runs the four-column build-vs-buy matrix at enterprise scope. Column 4 is internal build. When Column 4 wins — because no commercial point tool exists, because the problem is organisation-specific, because the data posture makes a commercial tool unworkable — mod-107 hands off to mod-110. The commissioning brief in Chapter 02 is Column 4's deliverable.

Two implications of that hand-off worth naming here:

- **The commissioner inherits the TCO shape from mod-107.** The build and run costs projected in the Column 4 TCO shape are the budget section of the commissioning brief. If the brief revises those numbers upward, it triggers a return to the mod-107 matrix, not a quiet budget increase.
- **A Column 2 (platform add-on) or Column 3 (industry-specific tool) decision that gets re-litigated six months later as a commission is a build-vs-buy failure, not a commission failure.** The commissioner protects the matrix's decisions by refusing to accept a commissioning request that short-circuits it. "The vendor product does not do exactly what we want, so build us the custom version" is a conversation to have with the vendor's product manager first, not with an engineer.

## The Chapters ahead

- [Chapter 02](02-the-commissioning-brief-as-the-load-bearing-artifact.md) authors the eight-section commissioning brief at operational depth and names the stage-gate the brief passes through before a build starts.
- [Chapter 03](03-inheriting-prototypes-and-the-honest-no-go.md) treats the prototype-inheritance pattern — consultants, business users, hackathon demos — and the five-dimension productionize-worthiness assessment that produces the productionise / rebuild / no-go recommendation.
- [Chapter 04](04-handing-architectural-depth-to-the-agentic-systems-architect.md) names the vocabulary of the agent control plane, the knowledge gateway, and the context layer; the commissioner reads, consults, and does not design.
- [Chapter 05](05-measuring-commissioned-tools-on-the-rollout-framework.md) measures commissioned tools on the mod-102/mod-106 framework and refuses the internal-build scorecard.
- [Chapter 06](06-signing-surfaces-maintenance-and-handoff-calendar.md) names the signatures, the maintenance commitment, and the hand-off calendar.

## Summary

- The commissioner's authority with the AI Engineering family is **brief-shaped**, not positional. Quality of the brief is quality of the build.
- The four peers the commissioner coordinates are `applied-ai-engineer` (point tools), `agentic-ai-engineer` (multi-step agents), `agentic-systems-architect` (platform surface), and `ai-risk-engineer` (red-team evidence in parallel with the build).
- Three postures collapse the role on contact: **designer** (writes architecture into the brief), **product manager** (dissolves the brief into informal channel decisions), and **apologist** (defends a failed commission against the scorecard). Each has a specific prevention in the chapters ahead.
- The one-paragraph test distinguishes a real commission from a mis-routed request: workflow-step problem, envelope checked, maintenance owner named, outcome measurable on the mod-106 framework. Failing any of four lines returns the request to intake.
- Column 4 of [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) is the upstream decision; the commissioning brief in Chapter 02 is Column 4's downstream deliverable. The commissioner protects the matrix by refusing short-circuits.
