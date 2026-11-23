# Lab 02 — Run the 20-Minute Intake Pre-Review Session (Solo Dry-Run)

**Duration:** 45 minutes (the 20-minute session plus a 15-minute preparation step and a 10-minute debrief)
**Format:** guided solo dry-run — you play the enablement runner *and* the BU-side requester across a 20-minute pre-review conversation, producing the notes that reshape the request before submission
**Grounding chapters:** [06 — The Intake Questionnaire](../06-the-intake-questionnaire.md), [02 — The Governance Council Liaison Seat](../02-the-governance-council-liaison-seat.md), [07 — What You Route Out — Counsel, SOC, Architect](../07-what-you-route-out-counsel-soc-architect.md)

## Objective

Run the **20-minute pre-review session** Chapter 06 names as "the preempt against formality" — the session that happens before the requester submits the intake questionnaire, where you reality-check the business justification, map the actual task and data classes, surface policy touchpoints the requester would not notice alone, and (critically) *reshape the request* if the current framing would land the tool in a classification that makes the rollout infeasible.

This lab is not Exercise 03 (which fills the questionnaire *after* the session has happened). This lab operates one step earlier — the twenty minutes in which the request is still reshapable, before submission locks it into a classification trajectory. Chapter 06: "Doing that reshaping *before* submission is cheap; doing it *after* council decline is expensive."

## Prerequisites

- Chapter 06 read end to end, especially the *The pre-review session — the preempt against formality* section.
- Chapter 02 read (so you understand how a well-run pre-review produces a clean Section 1 item for the next council pre-read).
- Chapter 07 read (so you remember that you do *not* propose a classification during the session — classification is architect/head-of-governance output).
- A chosen tool and organization. If you have carried a pairing through Exercises 01–03, use it. If not, pick one:
  - 3,000-person US bank — BU requests a "customer-service copilot" for the retail-banking call-center team.
  - 12,000-person global pharma — BU requests a "literature-search assistant" for a 60-person medical-affairs writing team.
  - 500-person SaaS company — BU requests a "meeting-notes tool" for a 220-person go-to-market org.
- A timer. Twenty minutes is the lab's frame.
- A single markdown file.

## Why a lab, not an exercise

Exercise 03's completed questionnaire is the *output artifact* once the pre-review has already surfaced what it was going to surface. This lab is the *conversation that makes the questionnaire worth submitting*. Chapter 06 names the failure mode directly: "the most common failure of an intake questionnaire is that it fills out as a formality instead of as a decision input. Fields get filled with 'see attached' or 'standard'; the risk-classification inputs get rubber-stamped; the resulting packet gives the council nothing to act on." The pre-review session is the countermeasure, and the countermeasure lives in the facilitator's reflexes, not in the questionnaire's field set.

A solo dry-run — with the requester played in character — is the cheapest way to build those reflexes before the real session, where you cannot stop to re-read the chapter.

## Setup

Create `intake-pre-review-session.md` with this skeleton:

```markdown
# Intake Pre-Review Session — <tool> / <organization>

**Date of dry-run:** <today>
**Runner:** AI Enablement Lead (me)
**Requester (played by me in character):** <specific role title — e.g., "Head of Retail-Banking Call-Center Operations, L40">
**Tool under pre-review:** <vendor, product name, deployment model>
**Session length:** 20 minutes (Chapter 06 default)
**Expected downstream:** submission to intake questionnaire within <N> days; schema-complete tag within <M> days; `awaiting-council-decision` for the <next date> council.

## Pre-session prep — the raw-request read (15 min, before the timer starts)

<entries>

## Session script — minute by minute (20 min on the timer)

<entries>

## Session outputs — what gets carried into the questionnaire and what gets reshaped

<entries>

## Debrief — what the session taught me (10 min, after the timer)

<entries>
```

---

## Step 1 — Pre-session prep: read the raw request as the requester wrote it (15 min, before you start the timer)

The pre-review session only works if the runner has already read whatever the requester put in writing before the session. Treat this as a literal read-aloud exercise.

Write the "raw request" as the requester would have submitted it — three to five sentences, in BU voice, enthusiastic, under-specified. Example scaffold:

```markdown
## Pre-session prep — the raw-request read

**Raw request (as the BU sponsor wrote it):**

> "We want to roll out <vendor-tool> to <BU team> — we think it'll save about <N> hours a week per person. Our team has been testing it on personal accounts and the results have been great. We'd love to have it rolled out by <soon>. Low risk — nothing sensitive goes into it."

**Four flags I would raise before the session even starts (read the raw request through four lenses):**

1. **Business-justification reality check** — what question would I ask to tell whether this is a real problem or a budget line looking for a justification?
2. **Data-class realism check** — is "nothing sensitive goes into it" plausible given the actual work this BU does? What data classes would I expect to leak into prompts if nobody said no?
3. **Cohort-and-reach check** — who exactly is in the "BU team"? How big, which geography, which role mix? The raw request will almost always understate this.
4. **Envelope check** — is this tool (or a near-neighbor) already in the approved-tooling envelope? Is there a parallel BU already using it?
```

The four flags are not for the session itself — they are what you walk *into* the session knowing to probe on. Chapter 06 names the pre-review runner's job as "reality-check the business justification, map the actual task and data classes, surface policy touchpoints the requester would not notice on their own, run the envelope check in the session, not as a follow-up." The four flags map to those four jobs.

**Checkpoint 1:**

- [ ] The raw request is three to five sentences, in BU voice, with at least one under-specified claim (the "low risk — nothing sensitive goes into it" line or equivalent).
- [ ] All four lenses have a question written for them.
- [ ] You have not yet started the 20-minute timer.

---

## Step 2 — Minutes 0–3: the open and the reality-check on business justification (3 min on the timer)

Start the timer. Write the open the runner would say at the start of the session.

```markdown
**Open (runner says):** "We have twenty minutes. The point of this session is to make sure the questionnaire you submit is the questionnaire the architect and council can act on — so we are going to walk the fields together before you file, not after. I may ask some questions that feel like pushback; they are the questions the council will ask next cycle, and better to answer them now than after a decline. Ready?"
```

Then do the reality-check turn. In character as the requester, write 2–3 sentences of business justification. In character as the runner, write the follow-up question that probes whether this is a real problem.

Example shape:

```markdown
**Requester (in character):** "The team is spending about <N> hours a week on <task> and we think the tool can cut that by half."
**Runner (in character):** "How do we know the <N> hours — did someone measure, or is that a rough feel? And which part of the <task> is the time going into — intake, decision, write-up?"
**Requester response (in character):** "<honest answer — usually: 'rough feel, we haven't instrumented it,' which is useful to surface now>"
```

Chapter 06: "is this a real problem, or a budget line looking for a justification?" The reality-check turn is where that question gets asked without turning the session into an interrogation.

**Checkpoint 2:**

- [ ] The open names "twenty minutes" and frames the session as pre-submission, not post-submission.
- [ ] The open names "pushback as the council's question in advance" — the requester hears it as help, not as resistance.
- [ ] The business-justification exchange includes at least one runner question about measurement or instrumentation of the baseline.

---

## Step 3 — Minutes 3–9: data-class realism (6 min on the timer)

This is the section most pre-review sessions under-run. The raw request's "nothing sensitive goes into it" line is almost always wrong — not maliciously, but because the requester is thinking about *intent*, not about *what operators will actually paste in once the tool is on their screen all day*.

Do the data-class realism turn. In character:

```markdown
**Runner (in character):** "Walk me through the three most common tasks on your team this week. Not the ideal use cases — what the team did yesterday. For each one, what data was on the screen?"
**Requester (in character, three tasks):**
1. <task 1 — with the data classes that were on the screen>
2. <task 2 — with the data classes that were on the screen>
3. <task 3 — with the data classes that were on the screen>
**Runner (in character):** "Okay, so if we map those to <org data classification scheme>, we're looking at <class A> and <class B> as the realistic input classes — which is different from 'nothing sensitive.' Not blocking; just something the questionnaire should reflect honestly so the classification lands right."
```

Chapter 06: "Map the actual task and data classes, not the sanitized ones." The purpose of asking for three real tasks is that *one* task is the sanitized answer and *three* tasks start to leak the real data classes the tool would actually see.

If you did Exercise 01, reference its data classification scheme by name. If not, propose the two or three classes this session is surfacing and note that the questionnaire will need to pin them to a real scheme.

**Checkpoint 3:**

- [ ] The data-class turn asks for three real tasks the team did *recently*, not three ideal use cases.
- [ ] The runner names the realistic input classes explicitly and maps them to a named classification scheme (or marks `<!-- needs-research: confirm scheme name -->`).
- [ ] The runner's redirect uses "not blocking; just" language — the reshape is collaborative, not corrective.

---

## Step 4 — Minutes 9–14: policy touchpoints (5 min on the timer)

Chapter 06 names policy touchpoints as "the field where the enablement-side reading shows up explicitly." The runner's job here is to surface which AUP sections and which SOP sections the tool is likely to require revisions in — most of the time the answer is "no new revisions required" and that itself is a useful signal, but when there *is* a revision needed, this is where it gets flagged.

Do the touchpoints turn. In character:

```markdown
**Runner (in character):** "Based on the three tasks you just described, I want to flag two policy touchpoints. First, the current AUP Section 3 (prohibited uses) says <existing prohibited use>; the <task 2> you described isn't prohibited, but it lands close enough to the line that I'd propose adding an approved-use entry at the next walking redline so your team doesn't have to guess. Second, the SOP accident path references a <role-level contact> for the SOC — your team is in <geography>, and we should confirm the SOC's out-of-hours channel works there."
**Requester (in character):** "<usually surprised — most requesters have never read the AUP or the SOP in detail>"
```

Chapter 06: the policy-touchpoints field reads "no new revisions required" most of the time and occasionally reads "AUP section 3 may need an added approved use; propose at next walking redline." The runner names the specific section, the specific delta, and the specific next move — not a vague "we'll need to update policy."

**Checkpoint 4:**

- [ ] The runner names at least one specific AUP or SOP section by number or title — not "the policy."
- [ ] If a revision is proposed, it names the walking-redline slot it would land in, per Chapter 01's cadence. If no revision is needed, the runner says so explicitly and the questionnaire will record "no new revisions required."
- [ ] The runner does not propose a legal reading or a risk classification — if either slipped in, strike through and rewrite as a hook or an input.

---

## Step 5 — Minutes 14–18: envelope check (4 min on the timer)

Chapter 06 says the envelope check runs *in the session*, not as a follow-up. Do it now, in character:

```markdown
**Runner (in character):** "Last thing — this tool. Is <vendor-product> already in the approved-tooling envelope? Let me check <reference to the envelope list or the mod-102 approved-tool register>. [Pause.] It looks like <inside envelope / adjacent product is inside / not in envelope>; that changes the shape of the next step — <describe>."
**Requester (in character):** "<usually relieved if inside; usually surprised if the near-neighbor is inside and would have worked>"
```

If the tool is inside the envelope, much of the policy / DPA / SSO / security review work has already been done. If it is adjacent to an inside-envelope tool, the near-neighbor may be a faster path and this is when to surface it. If it is outside the envelope, the envelope-admission workstream runs in parallel with intake — a meaningful delta the requester needs to hear now, not next cycle.

**Checkpoint 5:**

- [ ] The envelope status is explicitly named (inside / adjacent / outside), not glossed with "we'll check."
- [ ] If the near-neighbor path is faster, the runner surfaces it — this is one of the places the pre-review session pays for itself.
- [ ] The runner does not promise an envelope-admission timeline; that is a council / architect call.

---

## Step 6 — Minutes 18–20: the reshape and the close (2 min on the timer)

The session's last two minutes are where the reshape (if any) and the next-step commit happen. In character:

```markdown
**Runner (in character):** "Quick summary. We're going to submit the questionnaire with <specific reshape from the session — e.g., the realistic data classes, the two policy touchpoints, the envelope status — spelled out>. I'll send you a draft of the submission within <N> days for your review; once you sign off, I file it and it enters the `schema-complete` pipeline for the <next date> council. You will not need to attend the council unless they open a discussion ask; I'll report back within two business days after."
**Requester (in character):** "<usually accepts; occasionally pushes back on timeline, which is a flag for the runner>"
```

Chapter 02: the status tags move items through the pipeline (`pre-intake` → `intake-in-progress` → `schema-complete` → `awaiting-council-decision`). The close names which tag this item will be in at the next council.

**Checkpoint 6:**

- [ ] The close names the specific reshape from the session — the delta between the raw request and the submission.
- [ ] The close names the next status tag and the next council date.
- [ ] The close names the report-back SLA to the requester after the council.

---

## Step 7 — Session outputs (write-up after the timer)

Stop the timer. Fill in the session-outputs section — what the questionnaire carries forward and what got reshaped.

```markdown
## Session outputs — what gets carried into the questionnaire and what gets reshaped

### Carried forward unchanged
- <field or claim from the raw request that survives into the submission>

### Reshaped during the session
| Raw-request framing | Reshaped framing | Why the reshape (one-sentence rationale) |
|---------------------|------------------|------------------------------------------|
|                     |                  |                                          |

### Flagged for the submission as `<!-- needs-research: ... -->`
- <organization-specific fact the runner did not confirm in session>

### Flagged for a walking-redline slot (policy touchpoints)
- <specific AUP or SOP section + specific delta + slot owner>

### Pre-review session summary — three sentences for the top of the submission
> <three sentences naming what the pre-review surfaced that the raw request would have missed — operator-side judgment made visible>
```

The three-sentence pre-review summary is the artifact that signals to the architect and the head of governance that this submission has been triaged with operator-side judgment rather than rubber-stamped. Chapter 06 and Exercise 03 both name this as the most load-bearing three sentences in the submission.

**Checkpoint 7:**

- [ ] The reshape table has at least two rows — the data-class reshape and at least one other.
- [ ] No row in the reshape table proposes a risk classification; every reshape is an input, not a classification output.
- [ ] The three-sentence pre-review summary names *specific* things surfaced (a measurement gap, a data class the raw request mislabeled, a policy touchpoint the requester did not notice), not a mood ("the request is well-framed").

---

## Step 8 — 10-minute debrief (after the timer)

Write the debrief answering these four prompts. One or two sentences each.

```markdown
## Debrief — what the session taught me

1. **Which section of the session was hardest to stay in character for — and why?**
   <answer>
2. **Where did the session nearly drift into architect or classification territory, and what pulled it back?**
   <answer>
3. **Which Chapter 06 preempt did the dry-run most clearly validate — the business-justification reality check, the data-class realism turn, the policy touchpoints, or the envelope check?**
   <answer>
4. **In a real session, where is this dry-run likely to break first?** (Common answers: the requester is more defensive than the character played here; the twenty minutes overrun; the runner proposes a classification; the data-class turn gets one sanitized answer and moves on; the policy touchpoints get waved past.)
   <answer>
```

**Checkpoint 8:**

- [ ] All four prompts answered.
- [ ] Prompt 2 names a specific moment in the session where the drift started and names the specific move that pulled it back.

---

## Deliverable

- `intake-pre-review-session.md` — the raw-request read, the four flags, the six session turns (open, business-justification, data-class, policy-touchpoints, envelope, reshape+close), the session outputs with the three-sentence summary, and the four-prompt debrief.

## Expected output shape

Roughly 2–3 pages of markdown. Six session turns visible, each annotated with the runner's move and the requester's response. One reshape table with at least two rows. One three-sentence pre-review summary that could be lifted verbatim into Exercise 03's submission.

## Checkpoint — self-evaluation

- [ ] The open names "twenty minutes" and frames pushback as the council's question in advance.
- [ ] The data-class turn asks for three real tasks, not three ideal use cases, and names the realistic input classes explicitly.
- [ ] The policy-touchpoints turn names at least one specific AUP or SOP section — not "the policy."
- [ ] The envelope check runs *in* the session and names inside / adjacent / outside explicitly.
- [ ] The close names the reshape, the next status tag, the next council date, and the report-back SLA.
- [ ] No turn proposes a risk classification; every input is framed as an input.
- [ ] The three-sentence pre-review summary names specific things surfaced, not a mood.
- [ ] The debrief names a specific drift moment and the specific move that pulled it back.

## Common failure modes

- **Running the session as an interrogation.** The runner's job is to help the requester submit a questionnaire the council can act on, not to litigate the request. "Not blocking; just" language and the "pushback as the council's question in advance" framing from the open are what keep the session collaborative.
- **Accepting the sanitized first answer on data classes.** The single biggest payoff of the twenty minutes is the data-class realism turn, and the technique is asking for three real recent tasks. If the dry-run moves on after one task, re-run Step 3.
- **Proposing a classification during the session.** Chapter 06 and Chapter 07 both name this as the drift. You collect inputs; the architect's schema produces the classification; `head-of-ai-governance` ratifies. If a classification sentence slipped into your Step 4 or Step 7, strike through and rewrite as an input.
- **Running the envelope check as a follow-up.** Chapter 06 is explicit — the check runs in the session. If the dry-run punted it to "I'll check later," re-do Step 5.
- **A three-sentence pre-review summary that reads as a mood, not a finding.** "The request is well-framed and the team is motivated" is a mood; "the pre-review surfaced that the realistic input classes are <A> and <B> rather than 'nothing sensitive,' that AUP Section 3 may need an added approved use at the next walking redline, and that the vendor product is adjacent to <near-neighbor> which is already inside the envelope" is three findings. The architect reads for findings; moods tell them nothing.

## What this lab prepares you for

Pre-review sessions are the recurring artifact-producing move of the intake workflow — one per request, usually several per cycle at a mature CoE. The first time you sit one with a real requester, the pressure is on your runner-vs-schema discipline (you collect inputs; the architect designs the schema; the council classifies), not on your knowledge of the questionnaire's fields. Running one session cold in this lab, in character as both the runner and the requester, builds the muscle before the real session where stopping to re-read Chapter 06 is not an option. In production, this lab's three-sentence pre-review summary composes directly into Exercise 03's submission; this lab's reshape table becomes the evidence that the submission has been triaged with operator-side judgment.
