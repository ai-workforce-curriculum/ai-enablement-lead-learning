# Lab 01 — Author the Module 4 Data-Handling Scenario Triad

**Duration:** 60–75 minutes
**Format:** guided hands-on — worked scenario + two independent builds + red-team pass
**Grounding chapters:** [03 — The Foundational AI Literacy Curriculum](../03-the-foundational-ai-literacy-curriculum.md) (Module 4, Module 5, Module 6), [07 — Measuring Fluency Growth](../07-measuring-fluency-growth.md) (item-design rules)

## Objective

Produce **three complete, scorable Module 4 data-handling scenarios** — the content that carries the 30–40-minute data-handling module in Chapter 03. Each scenario names the correct operator action, two plausible-wrong actions, the SOP data class triggered, the verification habit from Module 5 if any, the escalation signal from Module 6 if any, and a scoring criterion suitable for the Chapter 07 assessment layer.

This lab operates one layer below the module's exercises. [Exercise 02](../exercises/exercise-02-foundational-ai-literacy-curriculum-outline.md) asks for *three named* scenarios as part of the curriculum outline — a line of description each. This lab is where you write the triad *end-to-end* in scorable form, which is the substance the auditor reads and the specialist-tier grader scores against.

## Prerequisites

- Chapter 03 read, specifically Module 4; Modules 5 and 6 skimmed (verification habits, escalation signals).
- Chapter 07 skimmed (item-design rules: grounded, scenario-based, policy-refreshing).
- A specific organization to author against. Carry forward the one you used in [Exercise 01](../exercises/exercise-01-audience-segmentation-and-fluency-target-map.md) / [Exercise 02](../exercises/exercise-02-foundational-ai-literacy-curriculum-outline.md). If none, pick a plausible mid-size organization — a 3,000-person US bank, a 12,000-person global pharma, a 500-person SaaS company, or similar.
- A named data-classification taxonomy. If your org does not have one, use the standard five-class shape: `public / internal / confidential / restricted / regulated`. Chapter 03 Module 4 names this taxonomy choice as the organization's.
- A blank markdown file.

## Why a lab, not an exercise

Exercise 02 's acceptance criterion for Module 4 is "at least three named, organization-specific scenarios." Named is a line. Scorable is a page. The gap between the two is where most Module 4 content fails an Article 4 walk-through: the scenario is named but produces no evidence a grader could defensibly score. This lab closes that gap for three scenarios at a time so the pattern is reusable across the remaining 20+ your foundational curriculum will need.

## Setup

Open a single file called `module-4-scenario-triad.md` and paste this skeleton. Fill the organization header before you start Step 1.

```markdown
# Module 4 Data-Handling Scenarios — <organization-name>

**Module:** Foundational curriculum Module 4 — The data-handling SOP, in scenarios
**Data-class taxonomy:** <five-class shape or your organization's>
**Scoring grader:** operator's manager or specialist-tier contributor (per Chapter 07)
**Version:** v0.1 — draft for pilot cohort review
**Changelog:** v0.1 (today) — initial triad.

---

## Scenario 1 — <short task-shaped name>

**Context (3–5 sentences):**

**The moment of decision (one sentence presented to the operator):**

**Correct action:**

**Plausible-wrong action A — what it looks like and why it fails:**

**Plausible-wrong action B — what it looks like and why it fails:**

**Data class(es) triggered:**

**Verification habit from Module 5 (if any):**

**Escalation signal from Module 6 (if any) and named-role route:**

**Scoring criterion (one line, observable):**

---

## Scenario 2 — <short task-shaped name>

<same shape>

---

## Scenario 3 — <short task-shaped name>

<same shape>
```

---

## Step 1 — Walk the worked scenario (15 min)

Fill in Scenario 1 by following this worked example and adapting it to your organization. The example is for a bank; adapt the counterparts for pharma, SaaS, hospital, manufacturer, etc.

### Worked example — "Summarizing a customer complaint in an approved chatbot"

**Context.** A branch-support employee receives a written complaint from a customer who disputes a transaction and references their medical condition as the reason they could not resolve the issue sooner. The employee wants to use the organization's approved generative chatbot to draft a concise summary of the complaint for the handoff to the complaints team.

**The moment of decision.** The complaint text is in the operator's clipboard. The approved chatbot window is open. What do they do before pressing paste?

**Correct action.** Open the data-handling SOP reference card. Classify the complaint text: it contains a customer identifier (restricted) and references health information about the customer (regulated). The approved chatbot is approved for internal and confidential data only, not for restricted or regulated. The operator does not paste. They route the summarization task to the approved intake path for regulated-data drafting (per the service catalog) and note the customer's health reference as an escalation signal (Module 6) for the complaints-team handoff.

**Plausible-wrong action A — paste with redactions.** The operator redacts the customer's name and account number by hand and pastes the rest. This fails because (a) hand-redaction is not a sanctioned transformation under the SOP — redaction has to be done by the approved tool, not by eye; (b) the health reference still reaches the model even after name redaction; (c) the SOP forbids regulated data in this tool regardless of the identifier being present.

**Plausible-wrong action B — summarize in head and type a non-verbatim prompt.** The operator decides to retype the complaint "in their own words" into the chatbot, believing paraphrase removes the data-class obligation. This fails because the SOP governs the content, not the exact wording — the operator is still sending regulated-class content to a tool not approved for it, and the auditor would read this as a knowing bypass.

**Data class(es) triggered.** Restricted (customer identifier) and regulated (health reference). The scenario is specifically designed to exercise the operator's recognition of *compound* data classes in a single artifact — the most common Module 4 failure.

**Verification habit from Module 5.** Not applicable here — no output has been generated. The decision point is upstream of the AI step.

**Escalation signal from Module 6 and named-role route.** The customer's health reference is a Module-6 escalation signal independent of the AI question — route to the Senior Complaints Specialist on duty (current roster at `<link to the complaints-team roster>`), not to the operator's line manager by default.

**Scoring criterion.** "The operator classifies both data classes present in the artifact (restricted *and* regulated), refuses to paste into the non-approved tool, routes the summarization task to the sanctioned intake path, and names the health reference as a Module-6 escalation signal to the complaints-team handoff."

---

**Why each field is in the template:**

- **Context** is not generic — it names the role, the tool, and the artifact in the operator's hand. A scenario that opens with "An employee is using an AI tool…" is too generic to score.
- **The moment of decision** is where the operator's attention lands. Compressing it to one sentence forces the author to isolate *the* decision, not a monologue.
- **Correct action** is the concrete behavior, not a principle. "Follow the SOP" is not an answer. "Open the SOP card, classify, do X" is.
- **Plausible-wrong actions** are the heart of the scoring. They have to be *attractive* — the mistakes operators actually make — not strawmen. Chapter 03 Module 4 is where the auditor reads for proportionality; the strength of the wrong answers is a proxy for how hard the module is working.
- **Data class(es) triggered** forces the author to read their own SOP as they design the scenario. A scenario where the author cannot name the class is a scenario the operator cannot classify either.
- **Verification habit** threads Module 5 into Module 4 where the two meet — when AI output is in play, the scenario tests both.
- **Escalation signal** threads Module 6 the same way. A scenario with no escalation signal is still valid; a scenario with one not named is unscored.
- **Scoring criterion** is the one-line observable the grader uses. A grader reading this line should be able to score two different operators and arrive at the same score.

**Checkpoint 1 — do not proceed until all three are true:**

- [ ] Every field in Scenario 1 is populated with something specific; nothing says "appropriate," "effective," or "as the SOP requires."
- [ ] The two plausible-wrong actions are things a real operator in your organization would plausibly do — not strawmen.
- [ ] Reading the scenario aloud takes under 90 seconds. If it is longer, the scenario has grown into a case study; cut.

---

## Step 2 — Independent build (25 min)

Author Scenarios 2 and 3 on your own, without consulting the worked example. Each must:

- Trigger a **different data-class combination** from Scenario 1. The triad exists to exercise the operator's classification skill across the SOP, not to test the same class three times. For the worked bank example above, Scenario 2 might trigger `internal + confidential` only (a sanctioned paste with a verification obligation), and Scenario 3 might trigger `restricted` alone (a sanctioned tool use that still requires a specific redaction step the SOP names).
- Name a **different role** in the organization, where plausible. If Scenario 1 is about branch-support, Scenarios 2 and 3 might be about relationship management, operations, or legal. A triad all in one function is weaker evidence than a triad across three functions.
- Use a **different approved tool** from the envelope where plausible. If your organization has only one approved tool, this constraint relaxes — but note the thinness in the Notes.

The goal is for a cohort reading all three scenarios to see the SOP operating across the realistic surface area of their day job, not against a single contrived class.

**Expected output after Step 2:**

- Scenario 2 and Scenario 3 both complete, all fields populated.
- Across the triad, at least three distinct data classes are triggered somewhere (not necessarily three per scenario).
- At least one scenario includes a Module-5 verification step (AI output is in play); at least one includes a Module-6 escalation signal; at least one scenario is a "do not use the AI tool" decision point so the triad does not implicitly teach that AI is always appropriate.

**Checkpoint 2:**

- [ ] Scenarios 2 and 3 are not variants of Scenario 1 with the name changed.
- [ ] Across the three, at least three distinct SOP data classes are exercised.
- [ ] At least one scenario's correct action is *not* to use the AI tool — the triad teaches refusal as well as use.
- [ ] Every scoring criterion is a single observable sentence a grader could apply consistently.

---

## Step 3 — The item-design red-team (15 min)

Chapter 07 names three rules for assessment items and four common failures. Read your triad aloud against this checklist. Any scenario that fails a check gets a `<!-- fix: ... -->` comment appended to it — do not silently paper over.

1. **Grounded-in-policy check.** For each correct action and plausible-wrong action, can you point at the paragraph or line in your organization's SOP or acceptable-use policy that supports it? If the answer is "it's implicit" or "it's common sense," the scenario is not grounded. The item-design rule from Chapter 07 is *grounded in the organization's own documents*; implicit answers produce ungradable scenarios.
2. **Not-trivia check.** None of the three scenarios should be answerable by someone who has not read the organization's policy. "Who founded OpenAI" is the Chapter 07 anti-example; "a user named John opens a chatbot" without organization-specific stakes is the same failure wearing a scenario costume.
3. **Verification-and-escalation thread check.** Across the three, does Module 5 (verification) appear at least once, and Module 6 (escalation) at least once? If both are absent, the triad teaches data classification only, which is thinner than the module asks for.
4. **Pre-asked-the-question check.** Ask yourself: could an operator *pass this scenario by guessing the pattern of the correct answer without actually reading the SOP?* If a reader can see that the "correct action" is always "do not paste," they will optimize for that pattern. Mix the correct outcomes across the triad — one "do not use," one "use with a verification step," one "use with a redaction step."
5. **Audit-readability check.** If an Article 4 auditor read only your triad with no other context, would the scoring criteria tell them how a grader produces consistent scores? If the criteria are written in the authoring voice rather than the grading voice, the module is not evidence yet.

**Expected output of Step 3:** a short list — two to five items — of scenario edits you will make before the triad goes to the pilot cohort. These are the real refinements the item bank needs before Article 4 evidence can defensibly rest on it.

---

## Step 4 — Freshness and handoff (5 min)

Chapter 03's refresh-cadence section names three triggers that regenerate Module 4 scenarios: policy change, envelope change, and incidents surfacing escalation signals not on the list. Chapter 07 adds item-bank hygiene (keep the bank 5–10× the per-attempt size; rotate retired items; audit for bias quarterly).

Add two short sections at the bottom of your file:

1. **Refresh triggers.** Which of the three regeneration triggers each scenario is sensitive to. Example: "Scenario 1 refreshes on any change to the regulated-class SOP line; Scenario 2 refreshes on envelope changes; Scenario 3 is bank-stable until the incident log surfaces a new escalation signal in this function."
2. **Grader handoff.** A two-line note to the specialist-tier contributor or operator's manager who will score these items on behalf of the assessment. Name what to do with a borderline submission and where to log a scoring disagreement for the next rubric revision.

---

## Deliverable

- `module-4-scenario-triad.md` — three complete scenarios, every field populated, red-team comments visible where applicable, refresh-trigger section and grader-handoff section at the bottom.

## Expected output shape

Roughly 2 pages at normal body-text size, table-light. Each scenario fits on roughly half a page. If you have produced four pages, you have drifted into case-study authoring; cut to the skeleton. If you have produced one page, you have under-filled the fields; expand until a grader could score an operator consistently from them.

## Checkpoint — self-evaluation

- [ ] Three scenarios, each with every template field populated with something specific (no "appropriate," "effective," or "as the SOP requires").
- [ ] At least three distinct SOP data classes exercised across the triad.
- [ ] At least one scenario where the correct action is *not* to use the AI tool.
- [ ] At least one Module-5 verification thread and at least one Module-6 escalation signal somewhere in the triad.
- [ ] The scoring criteria are written in grading voice — a specialist contributor could read them and arrive at the same score as another.
- [ ] Refresh triggers are named per scenario; grader handoff is explicit.
- [ ] Red-team Step 3 produced at least two edits before this triad goes to the pilot cohort — a triad that passes red-team on first draft either is unusually complete or has not been red-teamed hard enough.

## What this lab prepares you for

The scenario triad is the reusable unit of Module 4 content. Chapter 03 names Module 4 as "the module that fails Article 4 audits when it is thin" and as the module where the 30–40-minute time budget is spent. Producing one triad carefully — grounded in the SOP, scorable by a grader, refresh-triggered against the policy — is the template for the 20+ scenarios your final module will carry. The Chapter 07 knowledge-check item bank also draws from this triad; one scenario typically produces one or two scenario-based multiple-choice items with the correct action as the answer and the two plausible-wrong actions as distractors.
