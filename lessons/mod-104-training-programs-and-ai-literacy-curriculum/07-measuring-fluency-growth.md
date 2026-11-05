# Measuring Fluency Growth

> The AI literacy program that cannot show its impact gets cut in the next budget cycle. "People liked it" is not enough. "People attended" is not enough. "People completed the course" clears Article 4 and nothing else. Measurement is the substrate that lets the program defend itself in the exec review, pass the auditor's walk-through, and iterate on the parts that are actually working. This chapter builds the measurement stack.

## The four layers of measurement

Measurement stacks. Each layer is necessary but not sufficient; each adds a different kind of defensibility.

| Layer | What it measures | Who reads it | What it defends against |
|---|---|---|---|
| **L1 — Completion** | Who took what, when | Auditors, compliance, LMS admins | Article 4 non-compliance claim |
| **L2 — Knowledge** | Did the learner retain the content | L&D partners, cohort facilitators | Program design failure |
| **L3 — Task-level proficiency** | Can the learner do the role's named tasks with AI assistance | The exec sponsor, the operator's manager | "The training didn't change anything" |
| **L4 — Business outcome** | Did the organization's metrics move | CFO, executive office | "What are we getting for this investment" |

Programs that measure only L1 and L2 are the ones that get cut. Programs that measure through L4 are the ones that compound budget year over year. [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) treats the exec-scorecard construction that L4 feeds; this chapter builds the stack through L3 in depth and L4 at its interface to the exec scorecard.

## Layer 1 — completion

The compliance layer. The single question: for every in-scope person, is there a dated record showing they completed the relevant content and passed the relevant assessment within the refresh cadence?

- **Data source.** LMS (or equivalent system of record). One row per person per module per cycle. Columns: person, scope tier, module, completion date, assessment score, retake count if any.
- **Pass bar.** Published, typically 80% on the knowledge check. Lower bars raise the question of whether the check is proportionate; higher bars raise the question of whether the content is proportionate.
- **Refresh cadence.** Annual at minimum. Also triggered by changes to policy or the approved-tool envelope. A record older than the cadence counts as *lapsed*; lapsed records are evidence of program failure in the audit.
- **Exceptions handling.** Named process for people who legitimately miss the window (parental leave, medical leave) and a named process for people who refuse. Refusers surface to their manager and to HR, not to the enablement lead; the lead publishes completion data and does not run disciplinary processes.

The audit question this layer answers: *show me who is in scope, who has completed, and who has lapsed.* The answer is one query, not a conversation. If the answer is not one query, the layer is not built yet.

## Layer 2 — knowledge check

The content-retention layer. The single question: after taking the content, can the learner answer scenario-based questions grounded in the organization's own policy, SOP, and approved-tool envelope?

Item design is the thing to get right. Three rules:

1. **Items are grounded in the organization's own documents.** "What data class may be pasted into [tool] for [task]?" with the answer visible in the SOP. Not "who founded Anthropic."
2. **Items are scenario-based, not definition-based.** "An operator is drafting a reply to a customer who claims their product was misdiagnosed. What do they do?" Not "define a hallucination."
3. **Items are maintained as the policy changes.** A knowledge check whose items are not refreshed when the SOP changes is a check that will produce false confidence.

Scoring: 80% pass bar, two retakes, remediation after that. The remediation is a short conversation with a champion or the operations analyst; it is not escalation and it is not punitive. Operators who miss a retake twice usually have a content-availability problem (they skipped a module) or a reading-comprehension problem; both are solvable with a 15-minute re-read.

Item bank hygiene: keep the bank larger than the number of items per attempt (5–10x) so the item pool is non-trivial. Rotate retired items out. Audit for item bias (regional, functional) quarterly.

## Layer 3 — task-level proficiency rubrics

The layer that separates literacy programs from training programs. The single question: for each of the named tasks in a tier's fluency target map ([Chapter 02](02-audience-segmentation-and-fluency-targets.md)), can the operator produce output that meets the rubric at the stated quality bar?

A rubric per task. Each rubric is a short table of criteria — four to seven rows — scored on a short scale (1–4 or 1–5). The scoring is usually done by the operator's manager, a specialist-tier contributor, or (for lower-stakes outputs) peer review. For some tasks, an AI-assisted rubric scorer is appropriate; the enablement lead's team validates samples by hand.

### A worked rubric example — "Draft a tier-1 service reply"

| Criterion | 1 — Not met | 2 — Partial | 3 — Meets | 4 — Exceeds |
|---|---|---|---|---|
| On-brand voice | Reply is off-brand enough to require a rewrite | Reply needs noticeable editing | Reply matches brand standard | Reply exemplifies brand voice |
| Policy citation accuracy | Cites policies that don't exist or misstates | Minor policy misstatement | Accurate policy citation | Accurate citation with clear link to source |
| Customer-specific detail | Generic reply; no customer specifics | Partial customer context | Customer context fully reflected | Customer context used to pre-empt next question |
| Verification evidence | No evidence operator verified AI output | Partial verification | All numbers / facts verified against source | Verification visibly logged per SOP |
| Escalation sensitivity | Missed an escalation signal that was present | Noticed but did not escalate | Escalated per the playbook | Escalated and documented the signal |

Quality bar: all criteria at 3 or above. A "meets rubric" score is reported per operator, per task, per quarter.

The rubric does three things at once:

- Makes "proficiency" measurable, not editorial.
- Gives coaches and managers a concrete tool for the coaching session.
- Produces the data for the behavioral layer of the fluency target.

### Rubric authoring

Rubrics are authored by the same three-partied team that authors the playbook ([Chapter 04](04-role-based-playbooks-and-use-case-libraries.md)) — the function senior IC, the specialist contributor, and the enablement lead with governance co-author. The function senior IC's seat is critical; a rubric authored in the CoE in isolation will not reflect how the work is actually judged.

Rubric revision: quarterly, with versioning. When the rubric changes, the historical scores are reported against the version they were scored under; do not rewrite the past.

### Where rubrics are not appropriate

Rubrics fit outputs with observable quality criteria. They do not fit tasks where the output is a decision ("should we approve this loan"), a conversation ("the sales call went well"), or a non-artifact ("the manager used AI to think through the restructuring"). For these tasks, Layer 4 business metrics or behavioral indicators carry more weight than a rubric would.

Do not force a rubric onto a task where the output is not an artifact. Bad rubrics produce worse data than no rubrics.

## Layer 4 — business outcome, at the program interface

Layer 4 is where the enablement program hands off to the exec scorecard. [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) treats the scorecard itself; here, the question is what Layer 4 metrics the literacy program is accountable for.

Three clusters recur:

- **Productivity deltas tied to the taught tasks.** If the sales playbook has five named use cases, the question is: did the operators who completed the playbook produce output faster, at equal or higher quality, in the measured quarter versus the pre-period baseline? The source of truth is the function's own system (CRM, service platform, financial system), not a self-report survey.
- **Incident deltas.** Did the organization's AI-related incident rate change after the program rolled out? This cuts both ways — a well-trained population *surfaces* more small-case incidents because operators now recognize them, which is a signal the training is working, not failing. [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) treats the incident measurement layer.
- **Retention and engagement signals.** Does the organization's broader talent-engagement data (eNPS, retention by cohort, internal mobility) shift in populations with high AI fluency? This is a slower signal; read against the Microsoft Work Trend Index benchmarks for context, do not isolate the training program as the sole cause.

Layer 4 reads are *claims*, not direct measurements. The program is one of many forces acting on business metrics. Do not over-claim causation; report correlation with the caveats.

## External benchmarks worth referencing (not citing as evidence)

Two external benchmarks come up repeatedly in exec conversations about AI training programs. Know them so you can place your program alongside, but *do not* cite them as evidence for your own program's impact.

- **Josh Bersin's research on AI in L&D** (`joshbersin.com` and the Bersin Academy). Bersin publishes a continuing body of research on how enterprises build AI capability and the practices that correlate with higher adoption. Useful as reference for *shape* (what mature programs do). Not useful as evidence that *your* program is working — Bersin is a market observer, not a validator of your numbers.
- **Microsoft Work Trend Index** (`microsoft.com/en-us/worklab`). The annual Work Trend report and related research include population-level data on AI usage, operator sentiment, and reported productivity. Useful as context for *where your population sits* relative to the broader workforce. Not useful as a target to hit; the benchmark population is not your population.

The pattern to apply: "our program's shape is consistent with what [Bersin / Microsoft] identifies as high-performing" is a reasonable framing. "Our completion rate beats the Microsoft benchmark" is not a meaningful framing; the denominators are different.

<!-- needs-research: refresh the Josh Bersin AI-in-L&D and Microsoft Work Trend Index citations against the most recent cycle (2026 editions, if published) when resources.md is next revised. -->

## Pre- and post-assessment design

Several questions the exec sponsor will ask reduce to one capability: *can you show growth?* The answer is a pre- and post-assessment design that produces comparable scores before and after the program.

The reliable design:

- **Pre-assessment** administered at onboarding or at the opening of a new cohort. Covers the knowledge check and a rubric-scored artifact if practical (operators produce a representative task output under test conditions).
- **Post-assessment** at the end of the foundational curriculum or the role-based workshop. Same knowledge-check item types from the same bank. Same rubric-scored task format (different prompt, same rubric).
- **Deltas** reported per operator, per cohort, and per tier. Published quarterly.

Pitfalls:

- **Different items pre and post.** Same bank, rotated items, not the same items. If you use the same items, operators memorize; if you use different banks, the delta is not comparable.
- **Rubric drift.** The pre-assessment and the post-assessment are scored against the *same* version of the rubric. Version the rubric and track which version each score was against.
- **Self-report inflation.** Operators asked "how fluent are you now" versus "how fluent were you then" systematically under-report the "then" state. Rely on objective outputs, not retrospective self-report.

## The measurement artifact — the fluency scorecard

The output of this chapter is the **fluency scorecard** — one artifact that aggregates L1–L4 into a readable monthly view for the CoE and quarterly for the exec sponsor.

Rows for each tier (leadership, operators, specialists, builders), and for each major function. Columns:

- Completion rate (L1), by tier / function.
- Average knowledge-check score (L2).
- Share of operators meeting the rubric bar on named tasks (L3).
- Headline business-outcome delta, sourced from the function's system (L4).
- Open issues: lapsed records, failed rubric cohorts, incident signals.

The CoE's operations analyst maintains the scorecard. The enablement lead reviews it monthly. The exec sponsor sees a one-page extract quarterly. [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) treats how this becomes the exec scorecard.

## Common measurement failures

- **Attendance as the headline.** Attendance is a cost metric, not a value metric. Reporting attendance as the headline trains the exec sponsor to think of the program as an event series.
- **Satisfaction ("smile sheets") as the proxy for effectiveness.** Session satisfaction correlates weakly with behavior change. Collect it; do not headline it.
- **No pre-assessment.** Post-only scores look flat because there is no reference point. Build the pre-assessment from day one.
- **Rubrics scored by the trainer.** The trainer is motivated to score charitably. The operator's manager or a peer in the specialist tier is a more reliable grader.
- **Benchmarks weaponized.** Treating Microsoft Work Trend Index or Bersin data as targets rather than context produces gaming without growth.

## Where this chapter feeds

- [Chapter 08](08-partnering-with-hr-ld-and-internal-comms.md) treats the HR / L&D partnership that often runs much of Layer 1 and Layer 2 instrumentation.
- [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) is where the fluency scorecard feeds the executive scorecard.
- [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) is where Layer 4 incident data is sourced.
- Exercise 06 asks you to design the pre/post assessment and one task-level rubric end-to-end.

## Summary

- Measurement stacks across four layers — completion, knowledge, task-level proficiency, business outcome. Each defends a different audience's question.
- Layer 3 — task-level rubrics — is the one that separates a literacy program from a training program. Build rubrics per named task, authored by the function + specialist + CoE.
- Rubrics do not fit every task; force-fitting produces worse data than no data. Use Layer 4 signals for non-artifact tasks.
- Reference external benchmarks (Josh Bersin AI-in-L&D, Microsoft Work Trend Index) as context, not as evidence that your program is working.
- Pre- and post-assessments share item banks and rubric versions, not specific items. Report deltas, not raw scores.
- The one artifact to maintain is the fluency scorecard — the monthly CoE view, the quarterly exec extract.
