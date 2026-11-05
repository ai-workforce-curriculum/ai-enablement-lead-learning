# Exercise 03 — Role-Based Playbook for One Function

**Estimated effort:** 4 hours
**Format:** a complete playbook artifact, 10–20 pages, Markdown or docx
**Grounding chapters:** [04 — Role-Based Playbooks and Use-Case Libraries](../04-role-based-playbooks-and-use-case-libraries.md), [06 — Prompt Coaching for Non-Engineers](../06-prompt-coaching-for-non-engineers.md)

## Objective

Author a complete role-based playbook — the per-function artifact from Chapter 04 — for **one** function in your chosen organization. This is the deepest single artifact in the module and the one that turns the foundational curriculum into measurable productivity.

## Prerequisites

- Chapters 04 and 06 read.
- Fluency target map from Exercise 01 in hand.
- Foundational curriculum outline from Exercise 02 is useful but not required.
- A specific function to author against. Pick the one in your chosen organization where AI adoption would have the largest near-term impact. Common choices: customer service, sales, operations, finance. Avoid engineering for this exercise (it defers to level 20) unless you specifically want to practice the deferral pattern.

## Problem statement

The function you have chosen has agreed to be the lead function for the role-based rollout. The function's senior IC and a specialist-tier contributor (a champion from that function) are available for authoring sessions. Your governance co-author is reviewing what you produce for data-handling alignment.

By the end of the exercise, the function should have a signed v1 of their playbook that could be rolled out at the next cohort workshop.

## Requirements

Deliver one complete playbook with the following sections. Match the structure named in Chapter 04 — do not freestyle.

### 1. Cover material

- Playbook name (e.g., "Customer Service AI Playbook v1.0").
- Named owner (the specialist-tier contributor who maintains it).
- Function sponsor (the function's senior IC or manager who signed off).
- Governance co-signer.
- Date, version, next review date.
- A one-paragraph scope statement — what this playbook covers and what it explicitly does not.

### 2. Use-case inventory

A ranked list of 3–12 use cases for the function, each with:

- Use-case name (task-shaped, not technology-shaped).
- Frequency (how often an operator in this role performs this task).
- Impact (the business reason this task matters).
- Cross-reference to the foundational curriculum's acceptable-use and data-handling modules.

Minimum 3; soft maximum 8 for a v1 playbook.

### 3. Prompt library

For **at least three** of the use cases above, write a complete prompt-library entry. Each entry has:

- Entry name.
- When to use it (1–2 sentences).
- The prompt template, verbatim, with `[[BRACKETED]]` placeholders named for *content*, not for variable names.
- Data classes accepted in each placeholder, per the SOP.
- One filled-in example (anonymized) showing input and expected output.
- Two or three sentences on known failure modes.

### 4. Agent / workflow library (if applicable)

At least one entry even if speculative — if your organization does not yet have any commissioned internal agents, author a "future state" entry showing what one would look like for a high-value use case. Mark it as "future state (not yet commissioned)." Entry shape per Chapter 04.

### 5. Verification and escalation notes

Function-specific, not generic. Name:

- The verification habits for the three or four most-used outputs in this function (what the operator checks, against what, when).
- The escalation signals that mean "stop and call" for this function — three to five signals.
- The named roles (not individuals, but *named roles*) to whom escalations go.

### 6. Worked examples

Two before-and-after examples:

- The task performed without AI (time, output, verification cost).
- The task performed with the playbook's recommended pattern (time, output, verification cost).

These are the examples that will be featured in use-case spotlights ([Chapter 05](../05-the-delivery-mix.md)).

### 7. The explicit deferrals

Name any depth that *this playbook does not cover* and where it routes to:

- IC-engineering depth → `ai-assisted-software-engineer` (if applicable).
- IC-analyst depth → `ai-augmented-analyst` (if applicable).
- Team-scope delivery → `ai-augmented-team-manager`.
- Builder-tier work → the appropriate engineering curriculum.

### 8. Maintenance plan

- Refresh cadence (quarterly is typical).
- Trigger events (policy change, envelope change, prompt failure spike).
- The feedback loop from prompt-coaching sessions ([Chapter 06](../06-prompt-coaching-for-non-engineers.md)) back into the library.

## Starter guidance

- Resist writing more than eight use cases for v1. The remaining use cases go into a *backlog*, not v1 of the playbook. A playbook with 30 use cases is a playbook nobody reads.
- The prompt entries are the hardest part. Write them *as if an operator is going to copy them verbatim into a tool mid-task*. If an entry is long and literary, the operator will skip it. Short, imperative, placeholder-first.
- The worked examples are the credibility-earning part. If both examples sound invented, the playbook loses credibility with its function. Take time to ground them in real work patterns.
- For the "data classes accepted" line, reference your organization's actual data taxonomy from [mod-103](../../mod-103-policy-co-authoring-with-governance/README.md). "Public, internal. Not confidential or restricted." The line must be specific; "appropriate data" is not an answer.
- Do not include vendor-specific UI instructions in the main prompt entries. If the tool changes, those paragraphs become scrap. Put them in a short appendix if needed.

## Deliverables

- `role-based-playbook-<function>.md` (or `.docx`): the complete playbook as described above.
- A short *authoring retrospective* (3–5 sentences) naming what you would change about the playbook authoring process after producing it — what took longer than expected, what turned out to be unnecessary, what was missing.

## Acceptance criteria

- 10–20 pages at normal body-text size. Shorter suggests under-building; longer suggests the use-case list has grown into a reference manual.
- All eight required sections present and populated for a specific function.
- Prompt library has at least three complete entries, each with every required field.
- Verification and escalation notes are function-specific, not paraphrases of the foundational curriculum.
- Both worked examples are concrete and plausible — a reader from that function nods at them rather than squints.
- Deferrals are named explicitly where applicable; nothing is implicitly in-scope that should be out of scope.
- The playbook names an owner, a sponsor, and a governance co-signer.

## Stretch goals

- Author a second function's playbook at a lighter level (just use-case inventory and one prompt entry per use case) to show you can transfer the pattern.
- Dry-run one of the prompt entries with a real AI tool using synthetic but realistic inputs. Note at least one edit the exercise surfaced that you would make to the prompt.
- Draft the three-slide "introduce the playbook to the function" deck a team manager would use. This ties into the Chapter 08 deferral — your artifact is the deck; the team manager delivers it.
- Write the function's first adoption-challenge brief ([Chapter 05](../05-the-delivery-mix.md)) built around one of the playbook's use cases.

## Why this exercise matters

The role-based playbook is the artifact that closes the loop between "literacy content delivered" and "operator does the job faster with AI." Most organizations have the foundational curriculum and not the playbooks; the result is a workforce that passes the knowledge check and shows no productivity delta. Producing one playbook end-to-end, including the deferral pattern, is the practice reps needed to author the next seven.
