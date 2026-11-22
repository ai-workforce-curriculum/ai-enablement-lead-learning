# Lab 01 — Run the Three Stage-Gate Reviews on a Single Candidate

**Duration:** 75–90 minutes
**Format:** guided hands-on — gate-facilitator simulation across three review packs
**Grounding chapters:** [01 — The Three-Stage Tool Selection Decision](../01-the-three-stage-selection-decision.md), [06 — Partnering with Peers on Evidence and Build](../06-partnering-with-peers-on-evidence-and-build.md)

## Objective

Build the **three stage-gate review packs** — one per stage — for a single candidate carried end-to-end. Each pack is what a facilitator needs *in the room* to run a 30/60/45-minute gate: attendees, the one question the gate answers, the pre-circulated one-pager, the go/no-go options on the table (there are always at least three, including "return to the previous stage"), and the decision line that lands in the decision log.

This lab is not Exercise 01, which produces the three one-pager artifacts that live *inside* the pack. The lab operates one layer out — the meeting plumbing those artifacts get read through. If Exercise 01 is the contents of the folder, this lab is the folder, the invite, the agenda, and the facilitator script.

## Prerequisites

- Chapter 01 read, especially the three "Stage X gate" blocks that name attendees and the gate question.
- Chapter 06 skimmed far enough to know which gates the `ai-risk-engineer` L25 and the `applied-ai-engineer` L30 appear on and in what role.
- A chosen organization and a chosen candidate. Carry forward the pair from Exercise 01 if you have it. If not, pick one:
  - 3,000-person US bank evaluating a code assistant for a 180-engineer platform team
  - 12,000-person global pharma evaluating a meeting-notes tool for medical affairs
  - 500-person SaaS company evaluating a general-purpose chat assistant for the whole company
- A blank markdown file.

## Why a lab, not an exercise

The three Exercise 01 one-pagers answer *what should be on the page*. This lab answers *how the room reads the page and reaches a decision in under an hour*. Those are different failure modes: the first fails as thin content; the second fails as a gate that everyone attends and nobody decides. The second is the more common failure in practice, and it is the one the facilitator pack prevents.

## Setup

Create `stage-gate-review-packs.md` with this skeleton:

```markdown
# Stage-Gate Review Packs — <organization> / <candidate>

**Owner:** AI Enablement Lead (facilitator at all three gates)
**Candidate:** <tool / capability / build>
**Decision log target:** `<org>/decisions/<yyyy-qN>-<candidate-slug>.md`

## Gate 1 — Problem naming

<entries>

## Gate 2 — Candidate evaluation

<entries>

## Gate 3 — Pilot-vs-rollout commit

<entries>

## Decision-log stub

<entries>
```

Each gate pack uses this template — copy it into each gate section:

```markdown
- **Duration:** <minutes> (Chapter 01 default — do not stretch)
- **Attendees (named by role):**
  - Required: <roles>
  - Read-only / optional: <roles>
- **The one question this gate answers:** <single sentence, verbatim from Chapter 01>
- **Pre-read:** <path to the one-pager artifact; must be circulated at least 24h ahead>
- **Go/no-go options on the table (name all three or more):**
  1. <option>
  2. <option>
  3. <option — must include the "return to previous stage" option explicitly>
- **Facilitator script — what you say at the open:** <2–3 sentences>
- **Decision-line template:** <the sentence that ends the meeting and lands in the log>
- **Sign-off required at close:** <roles who sign>
```

If you cannot populate all eight fields for a gate, that gate's pack is not ready — the gate itself will be ceremonial.

---

## Step 1 — Gate 1 pack: Problem naming (15 min)

Chapter 01 — *Stage 1 gate* — names a 30-minute review, attended by the problem owner (often a function lead or an `ai-augmented-team-manager` L40 for the affected team), the enablement lead, and a security / data partner on read-only. Go/no-go: *is this problem named well enough to evaluate candidates against it?*

Fill in the Gate 1 pack now. Specific moves:

1. Name the **attendees by role** for your organization. If the problem owner is the medical-affairs function lead, say so; do not write "function lead." If your BU's `ai-augmented-team-manager` L40 is a real role title in the org (e.g., "Head of Medical Affairs Operations"), use that title.
2. Write **the one question** verbatim from Chapter 01. This is a vocabulary discipline, not a rewriting opportunity — the same sentence must appear on every Gate 1 pack you ever run.
3. Name **the three go/no-go options** explicitly. Chapter 01 names two (pass to Stage 2, iterate on Stage 1). The third is always *"close this intake — the problem does not survive naming."* Learners forget the third.
4. Write the **facilitator script** — two or three sentences. Example skeleton: *"We have 30 minutes. The question on the table is whether this problem is named well enough to evaluate candidates against it. If the answer is no, we iterate; we do not open Stage 2 on a half-named problem."*
5. Write the **decision line template.** Example: *"Gate 1 outcome: <pass / iterate / close>. Named problem: <one-sentence restatement>. Pain measurement: <number or 'target to instrument'>. Cohort: <size + role>."*

**Checkpoint 1 — do not proceed until all four are true:**

- [ ] The question field is verbatim from Chapter 01, not paraphrased.
- [ ] Attendees are named by actual role title for your organization, not generic role name.
- [ ] Three or more go/no-go options are listed, including the "close this intake" option.
- [ ] The decision-line template leaves one blank per field — a facilitator could paste it into a shared doc and fill it in live.

---

## Step 2 — Gate 2 pack: Candidate evaluation (20 min)

Chapter 01 — *Stage 2 gate* — names a one-hour review, attended by the enablement lead, security / privacy partner, procurement partner, the Stage 1 problem owner, and an `ai-risk-engineer` L25 on read-only for anything touching sensitive data. Go/no-go: *is this candidate ready to commit to Stage 3?*

Fill in the Gate 2 pack now. Specific moves:

1. Name **the attendees by role**, including the `ai-risk-engineer` L25 read-only slot. Chapter 06 is explicit that the risk engineer is an evidence consumer, not an approver — reflect this in your attendees list by putting them on read-only at Gate 2.
2. The **one question** — verbatim from Chapter 01.
3. The **go/no-go options** are richer at Stage 2. At minimum:
   1. Pass to Stage 3 on this candidate.
   2. Return to Stage 2 on a different candidate (the "no" from your Stage 2 one-pager).
   3. **Defer** — the candidate is strong but the approved-tooling envelope is not ready; open envelope-admission work in parallel and revisit in a defined window. Chapter 01 names the defer option specifically.
   4. Close the intake entirely.
4. **Facilitator script** — explicitly name the Chapter 01 rule that the build-vs-buy line must appear in the pre-read even when the answer is trivially "buy." If the pre-read does not contain the line, the gate does not open; iterate first.
5. **Decision line template** — must include the explicit build-vs-buy line, the envelope-status line, and the recommended-candidate line. Example: *"Gate 2 outcome: <pass to Stage 3 / return / defer / close>. Build-vs-buy: <one sentence>. Envelope status: <inside / admission-work-in-flight / outside>. Recommended candidate: <name + one-sentence rationale>."*

**Checkpoint 2:**

- [ ] The `ai-risk-engineer` L25 is on the attendees list in a read-only role when the candidate touches sensitive data; your pack states the condition.
- [ ] The "defer" option is on the go/no-go list.
- [ ] The decision-line template explicitly surfaces build-vs-buy, envelope status, and the recommended candidate — three fields, not one summary sentence.
- [ ] The facilitator script names the *"no POC extension past six weeks"* rule from Chapter 01 as a prior condition for Gate 2 opening.

---

## Step 3 — Gate 3 pack: Pilot-vs-rollout commit (20 min)

Chapter 01 — *Stage 3 gate* — names a 45-minute review, attended by the enablement lead, problem owner, security / privacy partner, procurement, the executive sponsor (often a BU lead or a `chief-ai-officer` L70 delegate for enterprise-visible tools), and a `head-of-ai-governance` L60 or delegate for anything that will show up in the governance council. Go/no-go: *commit to pilot, commit to rollout, or return to Stage 2.*

Fill in the Gate 3 pack now. Specific moves:

1. Name **the attendees by role**, including the executive sponsor and the governance delegate. If Chapter 06's red-team threshold applies to your candidate (sensitive data, customer-facing deployment, high-stakes decision support, regulator-touching workflow), add *"red-team evidence from `ai-risk-engineer` L25 — on the table as a pre-read"* to the required fields. Chapter 06: evidence lands before the commit, not after.
2. The **one question** — verbatim from Chapter 01.
3. The **go/no-go options** are three:
   1. Commit to pilot (default).
   2. Commit to rollout (only if all four Chapter 01 conditions hold — low risk, prior evidence, inside envelope, small cohort).
   3. Return to Stage 2.
   Chapter 01: "The third option is the one people forget; name it explicitly."
4. The **facilitator script** must state the "miss one, pilot first" rule for the direct-to-rollout path, and must name the Chapter 05 pre-mortem as a prerequisite — the pre-mortem is run at the end of Stage 3 before the commit. If the pre-mortem has not been run, the commit does not happen.
5. **Decision line template** — includes the named kill-switch owner, the named Chapter 03 artifact that must exist before the chosen path starts, and the pre-mortem outcome. Example: *"Gate 3 outcome: <pilot / rollout / return>. Pre-mortem: <ran, three sentences logged at path> / <re-run required>. Kill-switch owner: <role>. First Chapter 03 artifact to exist before start: <name>."*

**Checkpoint 3:**

- [ ] The three go/no-go options include "return to Stage 2" by name.
- [ ] The facilitator script names the "miss one, pilot first" rule from Chapter 01.
- [ ] The pack names the Chapter 05 pre-mortem as a prerequisite; the pack does *not* collapse the pre-mortem into the gate itself.
- [ ] The red-team evidence requirement from Chapter 06 is either on the required attendees/pre-read list, or an explicit line names why it does not apply to this candidate.

---

## Step 4 — Write the decision-log stub (10 min)

Chapter 01's closing line: *"the decision log is the artifact that survives the role, not the slide deck."* Build the stub that each of the three gates will append to.

Write a short section at the bottom of your file:

```markdown
## Decision-log stub

Path: `<org>/decisions/<yyyy-qN>-<candidate-slug>.md`

| Gate | Date | Question | Outcome | One-page artifact | Signatures |
|------|------|----------|---------|-------------------|------------|
| 1    |      |          |         |                   |            |
| 2    |      |          |         |                   |            |
| 3    |      |          |         |                   |            |

Each row filled in at the close of its gate. No row is retroactively edited; corrections land as appended notes.
```

Fill in the "Question" column for each row using the verbatim Chapter 01 question. Leave the other columns blank — those are filled in live at each gate.

**Checkpoint 4:**

- [ ] The decision-log stub has three rows, one per gate.
- [ ] The Question column in each row is verbatim from Chapter 01.
- [ ] The path convention is specific — not "somewhere in SharePoint"; a real folder with a real filename pattern.

---

## Step 5 — Red-team the three packs (15 min)

Read all three packs aloud. For each gate, answer these four questions; any failure gets a `<!-- fix: ... -->` comment in the pack.

1. **Could a stand-in facilitator (not you) run this gate from the pack alone?** If they need you in the room to clarify the question or the options, the pack is not ready.
2. **Does each gate's go/no-go list include the "no-happy-path" option?** Gate 1: close the intake. Gate 2: defer, or return with a different candidate. Gate 3: return to Stage 2. If a pack is missing its no-happy-path option, the gate is ceremonial.
3. **Is the pack short enough to actually read in the meeting?** Each pack should fit on half a page at body-text size. A one-pager per gate is a one-pager, not an operating manual.
4. **Does the gate close with a signed decision line?** Chapter 01's whole point is that the decision log survives the role. If the pack does not produce a one-line entry for the log, the gate is a conversation, not a gate.

**Expected output of Step 5:** two to five items flagged with `<!-- fix: ... -->`, which become your next revision pass. A pack set that passes red-team on first draft either is unusually complete or has not been red-teamed hard enough.

---

## Deliverable

- `stage-gate-review-packs.md` — three gate packs (eight fields each), the decision-log stub, and the red-team flags from Step 5.

## Expected output shape

Roughly 1.5–2 pages of markdown. Three gate packs, each half a page or less. One decision-log stub. Three to five red-team flags. The organization-specific detail (actual role titles, actual candidate name) visible throughout.

## Checkpoint — self-evaluation

- [ ] All three gates have the eight-field pack filled in.
- [ ] Each gate's "one question" is verbatim from Chapter 01, and the same sentence would appear on every future gate pack for every future candidate.
- [ ] Each gate's go/no-go list includes the no-happy-path option (close / defer / return).
- [ ] The Gate 2 pack names the `ai-risk-engineer` L25 as a read-only attendee when the candidate touches sensitive data.
- [ ] The Gate 3 pack names the Chapter 05 pre-mortem as a prerequisite, and — if Chapter 06's red-team threshold applies — names the red-team evidence as a required pre-read.
- [ ] The decision-log stub exists with three rows and a real filename path convention.
- [ ] Red-team Step 5 produced at least two flagged items.

## Common failure modes

- **A gate pack with two "pass" options and no "return" option.** The gate is pre-decided and the pack is theatre. Add the no-happy-path option, even if you expect it to be rare.
- **Attendees listed as generic roles.** "Governance" is not an attendee; "`head-of-ai-governance` L60 or their analyst-level delegate" is. The pack must survive the week the L60 is on vacation.
- **Collapsing the pre-mortem into Gate 3 itself.** Chapter 05 is explicit: the pre-mortem is run *before* the commit, as a prerequisite, not as an agenda item inside the 45-minute gate. If Gate 3 runs the pre-mortem live, the gate will overrun and the commit will slide.
- **No decision-line template.** The gate ends with "good discussion, thanks all" and the decision log stays empty. The template is the artifact that keeps that from happening.

## What this prepares you for

Three-stage selection is not a framework; it is a meeting cadence. The gate packs you build here are the plumbing that turns the framework into an operating rhythm the role can run every quarter without reinventing the meeting. In the real role, you will use this pack set the first time a candidate gets handed to you and every time after that — you will edit the organization-specific details (attendees, filename conventions) and reuse the eight-field template unchanged. That is the altitude.
