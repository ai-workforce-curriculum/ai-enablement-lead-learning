# Literacy is the Frame; Training is the Vehicle

> Most enterprise AI training programs are failing at the *framing* level, not the delivery level. They are planned as "AI training" — a catalog of courses to push into an LMS — when the job is to build *literacy* — a durable capability the workforce carries into every tool and every task. The two framings produce very different programs, very different budgets, and very different defenses when the CFO asks what the program is for. This chapter is the framing the rest of the module rests on.

## Why the word "literacy" earns its place

Pick either framing and the shape of the program follows automatically.

- **Training.** Decisions in the program are about courses: which courses to buy, which to build, which to require, which to retire. The success metric is *completion*. The audience grows by LMS enrollment. The budget is a negotiation with L&D on seat licenses. When the toolset changes, the course catalog is rebuilt behind it.
- **Literacy.** Decisions are about capabilities: what a role can *do* fluently with AI, what they will notice as risky, what they will escalate. The success metric is *task-level fluency* ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) treats the broader outcome measurement). The audience is segmented by role. The budget is a negotiation with the exec sponsor on business outcomes. When the toolset changes, the literacy is still valid — the examples refresh, not the underlying capability.

The second framing survives tool churn. It also survives the CFO conversation. "We ran 847 courses last quarter" is a vanity metric. "After the curriculum, Tier-2 operators resolved service tickets with AI assistance 38% faster, with 4% fewer escalations" is a story worth funding.

Three corollaries fall out of the framing and are worth stating now:

1. **The curriculum outlives the tools.** A good literacy curriculum works in a world where today's vendor is replaced by a different vendor in 18 months. A training catalog built around a specific vendor's UI does not.
2. **Operator fluency is a set of transferable habits, not a vendor skill.** Prompt coaching, verification habits, escalation triggers, and data-handling instincts travel across tools.
3. **"Done" is a rubric, not a date.** A literacy program is not a project with an end state. It is a capability the organization maintains, like financial reporting hygiene or cybersecurity awareness.

## The regulatory floor the frame rests on

[mod-101 Chapter 05](../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md) treated EU AI Act Article 4 in depth. For this module, pull forward the two consequences that shape every design decision later.

- **Deployers must ensure sufficient literacy.** That is an outcome obligation, not a course-catalog obligation. An auditor reads your rationale that the content is sufficient for the role and context. They read your evidence that in-scope persons completed it. They are not scoring the quality of the slides.
- **Sufficient is role- and context-dependent.** That is the regulatory justification for *audience segmentation* ([Chapter 02](02-audience-segmentation-and-fluency-targets.md)) and *role-based playbooks* ([Chapter 04](04-role-based-playbooks-and-use-case-libraries.md)). A one-size "AI 101" course does not clear Article 4 for an operator making triage decisions in a regulated workflow.

If your organization touches the EU market, Article 4 is the audit question your program answers. If it does not, the Article 4 *shape* is still good design — proportionate, role-segmented, evidenced, refreshed — because the next jurisdiction's obligation will rhyme with it.

## The four-tier mental model you'll use for the rest of the module

Chapter 02 treats this in full. Name the tiers now so the rest of the module has a shared vocabulary.

- **Leadership tier** — executives and senior managers whose decisions set AI direction. Need *literacy to govern*, not fluency to operate.
- **Operators tier** — the broad population using approved AI tools to do their day job. Need fluency on the specific tasks they perform, verification habits, and escalation signals. This is the biggest tier by headcount by far.
- **Specialists tier** — functional experts whose role is inflected by AI: senior analysts, legal reviewers, trainers, auditors, change managers, enablement partners. Need deeper mental models and pattern libraries for their function.
- **Builders tier** — the small population commissioning, configuring, red-teaming, or administering AI systems. Deep technical and risk material. This tier *mostly defers out* to the AI Engineering and AI Governance curricula — you host the hand-off, you do not teach the depth.

Four tiers, roughly 90/8/1.5/0.5% headcount split in a typical mid-size enterprise. The design error to avoid is budgeting as if the shares were even.

## What this role teaches — and what it defers down

The enablement lead's curriculum is a program, not a personal teaching load. Most lectures, most workshops, most 1:1s are run by other people on and off the CoE team. You *design* the curriculum, run the flagship pieces, and commission the rest.

Two deferrals are load-bearing and recur through the module:

- **IC-level prompt craft for software engineers** defers to [`ai-assisted-software-engineer`](https://github.com/ai-engineering-curriculum/ai-assisted-software-engineer-learning) (level 20). That track owns pair-programming patterns, test-and-verify loops, repo-scoped prompt templates, and the engineer-specific fluency curriculum. Do not re-author it from the enablement side.
- **IC-level prompt craft for analysts** defers to [`ai-augmented-analyst`](https://github.com/ai-workforce-curriculum/ai-augmented-analyst-learning) (level 20). That track owns data-exploration prompts, chart-and-table prompts, retrieval-augmented analysis patterns. Likewise, do not rebuild it.

What you do run is **coaching at the organizational scope** — the posture that makes non-engineers productive with AI without needing to become engineers. [Chapter 06](06-prompt-coaching-for-non-engineers.md) treats this at length.

And **team-scope delivery** defers *down* to [`ai-augmented-team-manager`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning) (level 40). You publish the kit; the team manager delivers it to their team. If you are personally running one team's workshops every week, your scope is drifting. [Chapter 08](08-partnering-with-hr-ld-and-internal-comms.md) treats the handoff in detail.

## What a program that got the framing wrong looks like

Three failure shapes recur in enterprise AI training programs. Each one comes from framing the work as training-catalog-first instead of literacy-first.

- **The lunch-and-learn program.** A monthly speaker series, high attendance, high satisfaction scores, no behavior change. Operators enjoy the talks and continue using AI the way they did before. Attendance is the only metric; nobody can point to a task that is done differently because of the program.
- **The vendor-branded curriculum.** The approved-tool vendor ships a certification path; the CoE wires it into onboarding. Twelve months later the vendor is replaced and the entire curriculum is scrap.
- **The "AI 101" push.** One course, every employee, same content for everyone from the CEO to a warehouse operator. Nobody uses a skill from it in their actual job. The program clears a compliance checkbox and generates no fluency.

The common fault: content designed outward from what was convenient to produce, instead of inward from what each role needs to *do* with AI. The literacy frame flips the direction — role-and-task first, content-production second.

## The module's throughline

The rest of this module answers, in order:

1. [**Chapter 02**](02-audience-segmentation-and-fluency-targets.md) — segment the audience and set fluency targets per tier. Measurable, defensible.
2. [**Chapter 03**](03-the-foundational-ai-literacy-curriculum.md) — the foundational curriculum every in-scope person completes.
3. [**Chapter 04**](04-role-based-playbooks-and-use-case-libraries.md) — the per-function playbooks and prompt / agent libraries on top.
4. [**Chapter 05**](05-the-delivery-mix.md) — the full menu of delivery vehicles (workshops, office hours, bootcamps, challenges, spotlights, self-serve) and when each earns its slot.
5. [**Chapter 06**](06-prompt-coaching-for-non-engineers.md) — prompt coaching at the enablement scope, with the hard deferrals to the level-20 engineering and analyst tracks.
6. [**Chapter 07**](07-measuring-fluency-growth.md) — assessments, rubrics, and the benchmarks you reference when defending the program.
7. [**Chapter 08**](08-partnering-with-hr-ld-and-internal-comms.md) — the partner contract that gets the program delivered without you teaching every class.

Read in order the first time. After that, Chapters 03 and 04 are the ones you will come back to most.

## Summary

- Frame the work as *literacy* — a durable workforce capability — not as *training* — a course catalog. The frame survives tool churn and defends a budget on outcomes.
- Article 4 of the EU AI Act is the regulatory floor the frame rests on; even outside the EU, use its proportionate, role-segmented, evidenced shape.
- Four audience tiers — leadership, operators, specialists, builders — with a heavily skewed headcount distribution. Budget for the distribution, not against it.
- IC-level prompt craft for engineers and analysts defers to the level-20 tracks; team-scope delivery defers down to `ai-augmented-team-manager`. You run the organizational program.
- Three recognizable failure shapes — the lunch-and-learn program, the vendor-branded curriculum, the AI 101 push — all come from framing the work as training-catalog-first.
