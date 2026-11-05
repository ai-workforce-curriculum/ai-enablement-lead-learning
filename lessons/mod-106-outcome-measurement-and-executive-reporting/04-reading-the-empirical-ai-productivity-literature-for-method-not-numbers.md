# Reading the Empirical AI Productivity Literature for Method, Not Numbers

> There is a small but genuine empirical literature on AI productivity gains — Peng et al. on GitHub Copilot, Ziegler et al. on the measurement validity of that same study, Noy & Zhang on writing tasks, Brynjolfsson/Li/Raymond on customer support, Dell'Acqua et al. on consulting. The enablement lead who cites the *headline numbers* from these studies to a board is doing exactly what [Chapter 01](01-the-measurement-stack-at-org-scope.md)'s vendor-number-headline pattern warns against. The enablement lead who reads them for *method* — how the studies constructed outcomes, what controls they used, what threats to validity they surfaced — is the one whose own measurement will survive a CFO's methodology challenge. This chapter is the reading guide.

## Why method travels and numbers don't

The reflex to pull a headline number from a published study — "GitHub's own research shows 55% faster task completion" — is irresistible when a scorecard needs a defensible-looking figure. Resist it anyway. The headline number travels badly because:

- **Different task.** The published task is not your task. Peng et al. measured an HTTP server implementation. Your developers are refactoring a monolith. Even in the same task family, outcome magnitudes shift by an order of magnitude with task shape.
- **Different population.** Published studies recruit volunteers. Your organization has a mandate population, a champion cohort, and a long tail of reluctant adopters. Treatment effect by population shape (the "jagged frontier" from Dell'Acqua et al.) is large enough to invert conclusions.
- **Different measurement cadence.** A 90-minute experimental session is not a quarterly rollout. Brynjolfsson et al. showed treatment effects that *change sign* over tenure; a 30-minute session cannot see that.
- **Different baseline.** Published studies instrument their own baselines. Your organization's pre-rollout baseline is almost always rougher. The denominator the published number is divided by is not the denominator you can produce.

The *methods* travel because they describe how to construct a defensible measurement — the choices, the trade-offs, the threats to validity — not what number those methods will produce on your organization.

A useful mental move: read these papers the way a civil engineer reads a published bridge design. The dimensions of the specific bridge do not transfer; the principles of load distribution do.

## What each paper teaches at this layer

### Peng et al. — "The Impact of AI on Developer Productivity: Evidence from GitHub Copilot" (arXiv:2302.06590)

**What it is.** A controlled experiment on 95 developers implementing an HTTP server in JavaScript, randomized to Copilot or no-Copilot conditions. Reported a 55.8% median reduction in task completion time for the treated group.

**What it teaches at this layer.**

- **Task selection discipline.** The study picked *one* bounded, concrete task with a clean start and a clean definition of done. The simplicity of the task is a feature, not a limitation — it is what makes the treatment comparison interpretable. Your pilot design should pick similarly bounded tasks, even when the "real" workflow is messier.
- **Pre-registration of the primary outcome.** The outcome metric (task completion time) was defined before the experiment ran. This is the pilot-charter discipline from [mod-102 Chapter 02](../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md) in experimental form. The moving-goalpost failure mode from [Chapter 01](01-the-measurement-stack-at-org-scope.md) is what pre-registration prevents.
- **Secondary outcomes as sanity checks.** The paper reports time spent in the coding editor vs. in the Copilot interaction as a texture measure, not as an outcome. Your telemetry should serve the same function — colour, not headline.

**What to watch for.** The paper's population was recruited volunteers who opted into a Copilot study. Self-selection into AI studies is a non-trivial source of effect inflation. Your organization's population is not self-selected in the same way; expect dampened effects.

### Ziegler et al. — "Measuring GitHub Copilot's Impact on Productivity" (Communications of the ACM, 2024)

**What it is.** A measurement-methodology paper by the authors of the Peng et al. study, published a year later, that examines the construct validity of productivity measurements for AI coding tools. Argues — using survey data correlating "perceived productivity" with telemetry — that acceptance rate of Copilot suggestions is a usable proxy for developer productivity gains.

**What it teaches at this layer.**

- **Measurement-validity work is its own thing.** Before you claim an outcome moved, you have to defend that the thing you measured is what you claim. The paper is a worked example of the methodology work that sits *between* the telemetry and the outcome claim.
- **Perceived productivity and measured productivity do not have to agree.** The paper openly treats the gap between what operators *report* and what telemetry *shows*. Your workflow interviews surface the perception side; your outcome metrics surface the measurement side. Divergence between them is a finding, not noise.
- **Acceptance rate as a proxy has an upstream dependency.** The claim that acceptance rate correlates with productivity gain depends on the design of acceptance rate itself. A proxy is only as defensible as the chain that connects it to the outcome. Borrow the structure, not the specific proxy; your tool's acceptance-rate equivalent may or may not carry the same relationship.

**What to watch for.** The paper is authored by employees of the tool's vendor. That does not disqualify it, but it does mean the methodology has an implicit interest in supporting proxy measures that make the tool look good. Read the construct-validity argument on its own merits.

### Noy & Zhang — "Experimental evidence on the productivity effects of generative artificial intelligence" (Science, 2023)

**What it is.** A randomized experiment on 453 professionals performing a mid-level writing task (grants, reports, memos). Treated participants used ChatGPT; controls did not. Measured time to completion and the quality of the output, scored by human raters.

**What it teaches at this layer.**

- **Two-dimensional outcome.** Time *and* quality, measured independently. This is the discipline that catches the faster-but-worse failure — a tool that speeds up a task while degrading its output. The paper's two-dimensional outcome is the shape your productivity-and-quality split from [Chapter 01](01-the-measurement-stack-at-org-scope.md) is modeled on.
- **Heterogeneous treatment effects.** Lower-skilled workers gained more than higher-skilled workers. This is a critical methodological finding: the aggregate effect is not evenly distributed across the population. Your scorecard should surface this when it is true — operators at different skill levels will see different gains, and the average obscures the distribution.
- **Human-rater quality scoring.** The paper did not trust a model-based quality score; it used human raters with inter-rater agreement measurement. Your quality outcomes should borrow this shape — a sampled human evaluation layered on top of telemetry.

**What to watch for.** The task was a stand-alone writing exercise, not embedded in a workflow. Real writing work at your organization is embedded in review cycles, client interactions, and multi-step coordination that the experiment stripped out. Effect sizes on embedded workflows will be lower; carry the shape of the measurement, not the size of the effect.

### Brynjolfsson, Li, Raymond — "Generative AI at Work" (NBER working paper 31161)

**What it is.** A longitudinal field study of 5,179 customer-service agents at a Fortune 500 firm, before and after rollout of an AI conversational assistant. Measured resolution time, first-contact resolution rate, customer satisfaction, and agent retention over months.

**What it teaches at this layer.**

- **Longitudinal measurement reveals shape.** The treatment effect was not constant over time; it grew as agents and the system learned together. A cross-sectional measurement (one month post-rollout) would have reported a different effect than the steady-state measurement at six months. The implication for your scorecard: a rollout's outcome at week 4 is not the rollout's outcome at week 24, and the quarterly review has to carry both.
- **Heterogeneous treatment by tenure.** Newer agents gained more than tenured ones. The pattern mirrors Noy & Zhang's skill-level finding — the assistance substitutes most for experience operators had not yet built. Your scorecard should be able to decompose outcomes by tenure or by role seniority when the data is there.
- **Secondary outcomes that matter.** The study reports customer satisfaction and agent retention alongside productivity. Your business-outcome family from [Chapter 01](01-the-measurement-stack-at-org-scope.md) is the shape; the paper is the worked example.
- **Realistic deployment conditions.** This is not a lab experiment; it is a rollout. The field conditions — selection into usage, variation in tool configuration, concurrent operational changes — are the conditions your organization will experience. The paper is the closest published analogue to a real rollout; borrow its measurement structure directly.

**What to watch for.** The paper's single firm, single tool, single task family limits generalizability. Reading for *method* is exactly right here; reading for the headline effect size and quoting it to your board would be the error.

### Dell'Acqua et al. — "Navigating the Jagged Technological Frontier" (HBS working paper 24-013)

**What it is.** A field experiment on 758 BCG consultants performing 18 different tasks, randomized to GPT-4 or control. Core finding: on tasks "inside the frontier" of AI capability, consultants with AI significantly outperformed; on tasks "outside the frontier," consultants with AI underperformed those without.

**What it teaches at this layer.**

- **Capability heterogeneity across tasks is the dominant signal.** The aggregate "AI makes consultants faster" story is wrong at the task level. Some tasks get better, some tasks get worse, and the magnitude of each is large enough that the aggregate conceals the operating reality. Your portfolio-level outcome rollups from [Chapter 01](01-the-measurement-stack-at-org-scope.md) will show this shape if you look for it.
- **The failure mode of AI on out-of-frontier tasks is not neutral.** The paper's "centaur vs. cyborg" framing — the way operators combine their work with AI output — produces specific failure shapes: anchoring on wrong AI output, under-editing, mistaking fluency for correctness. These are patterns your workflow interviews should surface, and your scorecard should name.
- **Expertise moderates the effect.** Lower performers gained more from AI; higher performers gained less or lost on out-of-frontier tasks. The pattern aligns with Noy & Zhang and Brynjolfsson et al.; read together, the three studies suggest a cross-study regularity about *who* AI helps and *when*, which is the shape your scorecard's role-level decomposition should carry.

**What to watch for.** The tasks in the study were curated; operators in your organization encounter a messier mix. The 18-task structure is your shape — pilot against multiple task types, do not aggregate across them without seeing the variance.

## The methodology patterns that transfer

Reading the five studies together surfaces a short list of methodology patterns that do travel. These are the moves you carry into your own measurement design.

### Pattern 1 — pre-registered primary outcome, with secondary outcomes as texture

The primary outcome is defined before the rollout starts, measured against a pre-rollout baseline, and reported with a confidence band. Secondary outcomes (telemetry, acceptance rates, usage patterns) provide texture but do not substitute for the primary. The Peng-and-Ziegler pair shows the shape — a pre-registered primary, with proxies worked out openly in a measurement-validity paper.

### Pattern 2 — two-dimensional outcome: productivity and quality

Noy & Zhang measured both; your scorecard should too. The one-dimensional outcome ("faster") is the failure that produces the faster-but-worse rollout. The quality dimension is often harder to measure — human raters, sampled QA, defect rates downstream — but is non-negotiable in the measurement stack.

### Pattern 3 — longitudinal observation, not cross-sectional

Brynjolfsson et al. showed treatment effects that evolve. A measurement at week 4 is not the measurement at week 24. Your scorecard carries the trajectory, not a snapshot — see the monthly deep-dive and quarterly review structure in [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md).

### Pattern 4 — heterogeneous treatment effects by sub-population

Noy & Zhang on skill level, Brynjolfsson et al. on tenure, Dell'Acqua et al. on task type. The aggregate average hides the distribution; the scorecard that reports only the mean is reporting less than what the measurement knows. Decompose by role, by seniority, by task family where the data supports it.

### Pattern 5 — field conditions over lab conditions, where possible

Lab experiments give clean treatment-vs-control comparisons; field experiments give conditions that resemble the rollout you are running. Where you can run against your real workflow, do. Lab-like pilots that do not generalize to field conditions are what the ghost-user rollout from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) looks like dressed up as research.

## The threats to validity the enablement lead carries

Every rollout's measurement faces the same short list of validity threats the published studies document. Name them before the CFO does.

- **Selection into use.** Operators who opt into the tool are not a random sample of operators. In mandatory rollouts the bias is smaller but not zero; usage intensity still self-selects. Report your results against the in-scope population, not the opted-in subset, where possible.
- **Concurrent operational change.** A rollout rarely happens in isolation. Process changes, staffing changes, workload changes, reorgs — any of these can produce an outcome movement that the measurement will attribute to the tool. Note the concurrent changes in the methodology appendix.
- **Novelty effects.** Early adoption often shows exaggerated effects — operators are paying attention, measurement is tight, the tool is novel. The effect dampens at steady state. Report longer trajectories; the six-month measurement is more credible than the one-month.
- **Measurement drift.** Operators change how they do a task in response to being measured. In a drafting rollout, if you measure time-to-first-draft, operators may shorten first drafts to preserve the metric at the cost of quality. Pair productivity with quality; read the pairing.
- **Attribution to AI specifically.** Even when outcomes move, the move may not be attributable to AI specifically. A champion network, a training program refresh, and a workflow redesign that happened to launch concurrently can account for an outcome movement independently. The attribution discipline is what [Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md) will treat; the methodology appendix in your quarterly review from [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) is where it lives.

Naming these threats in your own methodology appendix is defensive writing of the best kind. The CFO who sees "selection into use was addressed by comparing in-scope cohort means, not opted-in-subset means" is seeing a program that has read the literature. The CFO who sees a bare 22% number is seeing a program that has not.

## The reading rhythm

Carry the five papers above as a reading loop:

- **First read.** Scan for the headline result and the method section. Skip the discussion.
- **Second read.** Re-read the method section against your own measurement design. Mark places where your design differs, and decide whether the difference is defensible.
- **Third read.** Read the threats-to-validity section (or the equivalent, usually in the discussion) and map each threat onto your own program's exposure.
- **Annual re-read.** Pick one paper per quarter and re-read it. The literature is not that big; carrying it across the role is practical.

The methodology appendix in your quarterly review from [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) cites these papers by title and the methods you borrowed. Cite method, not numbers; see [Chapter 03](03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) on the vendor-voice failure for why.

## Where this chapter feeds

- [Chapter 01](01-the-measurement-stack-at-org-scope.md)'s outcome construction is grounded in the Pattern 1–Pattern 5 moves above.
- [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md)'s methodology appendix cites these studies as method references.
- [Chapter 03](03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md)'s confidence-band discipline is where the literature's uncertainty language lands in the executive artifact.
- [Chapter 05](05-partnering-with-finance-on-cost-model-and-roi.md)'s ROI attribution uses the attribution threat as its central methodology challenge.
- Exercise 05 walks the mapping from each paper to a specific metric choice in your scorecard.

## Summary

- Read the empirical AI productivity literature for method, not numbers; headline effect sizes do not transfer across task, population, cadence, or baseline.
- Peng et al. teaches pre-registered outcome with telemetry as texture; Ziegler et al. teaches measurement-validity work between telemetry and outcome claims; Noy & Zhang teaches two-dimensional outcome and heterogeneous effects by skill; Brynjolfsson et al. teaches longitudinal trajectories and heterogeneity by tenure; Dell'Acqua et al. teaches task-level capability heterogeneity and the jagged frontier.
- Five methodology patterns transfer: pre-registered primary outcome, two-dimensional productivity-and-quality, longitudinal observation, decomposition by sub-population, field over lab conditions.
- Carry five named threats to validity (selection into use, concurrent operational change, novelty effects, measurement drift, attribution to AI specifically) in the methodology appendix of the quarterly review.
- Cite method, not numbers, in every executive artifact. Vendor-number headlines are the failure this reading prevents.
