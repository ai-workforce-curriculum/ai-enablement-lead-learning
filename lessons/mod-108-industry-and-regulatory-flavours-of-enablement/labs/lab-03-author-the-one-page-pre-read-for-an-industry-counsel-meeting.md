# Lab 03 — Author the One-Page Pre-Read for an Industry Counsel Meeting

**Duration:** 60–75 minutes
**Format:** guided solo authoring — one-page pre-read + attached operational context + proposed structure + explicit non-asks, red-teamed against the Chapter 08 drifted-sentence patterns
**Grounding chapters:** [08 — Partnering with Industry Counsel Without Opining](../08-partnering-with-industry-counsel-without-opining.md) (primarily *The pre-read discipline for industry conversations*, *The three postures to know by name*, *The sentence patterns that stay in scope*, *The four questions that signal drift*); the industry chapter you choose among [03](../03-healthcare-flavour-hipaa-and-phi.md) / [04](../04-finance-flavour-sr-11-7-and-finra.md) / [05](../05-legal-engineering-flavour.md) / [06](../06-education-flavour-ferpa-coppa-and-ed-tech.md)

## Objective

Produce the **one-page pre-read** Chapter 08 names as the discipline that keeps an industry-counsel conversation productive and inside role, with the attached operational context, a proposed structure for the answer (not a proposed answer), and the explicit non-asks that narrow the ask. The pre-read is for a specific, named conversation with a specific industry counterpart on a specific decision — not an abstract template.

Target outputs:

1. The **one-page pre-read** itself, structured in the three Chapter 08 sections (operational situation / specific decisions needed / timing signal), delivered as if sent to the counterpart 48 hours ahead of the meeting.
2. The **attached operational context** — workflow diagrams or descriptions, prompt examples, output patterns, intake responses, draft training content — enough that counsel can decide without an additional round of information requests.
3. The **proposed structure for the answer** (not the answer) — an articulation of "the decision could be made at level X / level Y / level Z; our operational preference is [X] for reasons [Y], but we defer to counsel on which level is load-bearing from a regulatory perspective."
4. The **explicit non-asks** — a short list of what you are *not* asking for, so the meeting does not become an open-ended review.
5. A **self-check against the drifted-sentence patterns** Chapter 08 names.

## Prerequisites

- Chapter 08 read end-to-end; specifically re-read *The three postures to know by name*, *The sentence patterns that stay in scope*, *The four questions that signal drift*, and *The pre-read discipline for industry conversations*.
- One of the four industry chapters read, matching the counterpart you choose.
- A chosen conversation to write the pre-read for. Pick exactly one — do not try to generalize across industries in a single pre-read; the lab is about one specific meeting:
  - **Healthcare — meeting with the privacy officer.** Conversation: whether the clinical-informatics team's use of an approved coding assistant (BAA on file) to draft patient-portal replies meets HIPAA's minimum necessary standard and the BAA's defined services. Chapter 03 and Chapter 08's healthcare case walk are the anchors.
  - **Finance — meeting with the MRM lead.** Conversation: routing a credit-memo-narrative-drafting tool through MRM for SR 11-7 classification; the intake packet carries the three sub-questions filled, the volume, and the operator population; the specific ask is a decision on classification plus routing to any adjacent surface (fair-lending, FINRA). Chapter 04's "is it a model?" question is the anchor.
  - **Legal engineering — meeting with the general counsel.** Conversation: whether the matter-level classification system for a specific M&A workstream permits use of the approved self-hosted model under the organization's privilege theory. Chapter 05's drifts and Chapter 08's licensed-professional disciplines are the anchors.
  - **Ed-tech vendor — meeting with the chief privacy officer.** Conversation: whether the workforce AI tool can be used on redacted learning-analytics samples from one customer where the customer contract is silent on learning analytics. Chapter 06's customer-contract-alignment rule and Chapter 07's product-vs-workforce boundary are the anchors.
- A single markdown file.
- A timer.

## Why a lab, not an exercise

Exercise 02 asks you to read a posting; Exercise 03 asks for a RACI + drift memos; Exercise 04 asks for a policy package; Exercise 05 asks for a curriculum. None of those asks you to simulate the *conversation* with the specific industry counterpart on a specific decision — the forty-five-minute meeting that produces either a clean decision carried back into the AUP / SOP / training, or an accumulated drift. This lab is the pre-read discipline standalone, with the counterpart's time as the constraint.

Running the lab cold builds the one-page discipline — three sections, attached context, proposed structure not proposed answer, explicit non-asks — before the first time it lands in a real calendar invite, where pausing to re-read Chapter 08 is not an option.

## Setup

Create `industry-counsel-pre-read.md` with this skeleton:

```markdown
# Industry Counsel Pre-Read — <conversation one-line name>

**Meeting date:** <48 hours from now, as if real>
**Counterpart role:** <privacy officer | MRM lead | general counsel | chief privacy officer>
**Counterpart name (placeholder):** <name>
**Drafter:** AI Enablement Lead (me)
**Meeting length:** 45 minutes (Chapter 08 default for industry-counsel cadence)
**Purpose:** <one-line decision-ask>
**Posture (named per Chapter 08):** Posture 1 — operator surfacing a question

---

## Section 1 — Operational situation

<entries>

## Section 2 — Specific decisions needed

<entries>

## Section 3 — Timing signal

<entries>

---

## Attached operational context

<entries>

## Proposed structure for the answer (not proposed answer)

<entries>

## Explicit non-asks

<entries>

---

## Self-check against Chapter 08's drifted sentence patterns

<entries>
```

Set your timer and start.

---

## Step 1 — Minutes 0–10: write the one-line purpose and name the posture (10 min)

Before any section, write the meeting's purpose as one line. Not "discuss the tool." A decision-ask.

Examples per conversation:

- Healthcare (privacy officer): *"Does the clinical-informatics team's proposed use of [tool] to draft patient-portal replies meet HIPAA's minimum necessary standard and the BAA's defined services?"*
- Finance (MRM lead): *"Is the proposed credit-memo-narrative-drafting workflow a model under SR 11-7 — and if yes, what MRM-side preconditions apply before production use?"*
- Legal engineering (general counsel): *"Does the matter-level classification v0.2 preserve attorney-client privilege for the specific M&A workstream under the organization's privilege theory?"*
- Ed-tech vendor (chief privacy officer): *"Can the workforce use [tool] on redacted learning-analytics samples from District X where the customer contract is silent on learning analytics — and at which level (AUP / per-customer / per-request) should the rule be set?"*

Then name the posture explicitly. Chapter 08: Posture 1 is "operator surfacing a question," Posture 2 is "co-author refining counsel's draft," Posture 3 is "carrier of a decision already made." For this lab, you are in Posture 1 — you have a question for counsel.

**Checkpoint 1:**

- [ ] The purpose line is a decision-ask with an identifiable yes/no (or structured-choice) answer, not an open-ended "discuss."
- [ ] The posture is named explicitly as Posture 1 at the top of the file.

---

## Step 2 — Minutes 10–25: write Section 1 (operational situation) (15 min)

Chapter 08 names what Section 1 carries: "what the user population is, what the tool is, what the data flow looks like, what the proposed change is." The section is operational — not interpretive, not conclusory. Counsel reads this to form their own picture of the situation before considering the question.

Template:

```markdown
## Section 1 — Operational situation

**The user population:** <specific role, specific count, specific location>.
**The tool:** <name, how deployed at the org, what approved uses already attach, what status it sits in on the envelope>.
**The data flow:**
- Input: <data classes touched, named in the industry's regulatory vocabulary>.
- Processing: <where the tool runs, where logs land, retention>.
- Output: <what the operator does with the output, downstream handling, any artifacts produced>.
**The proposed change:** <what the user population wants to do that is not currently permitted, or the use they have started that has triggered this conversation>.
**Current posture (not a conclusion — a status):** <hard pause | pilot in sandbox | active with escalation to this meeting | other>.
```

Two tells for Section 1:

- **No "it seems" or "I believe" sentences.** The section is operational facts in the industry's vocabulary. Interpretation belongs to counsel in the meeting, not to you in Section 1.
- **Data classes are named in the industry's vocabulary.** PHI, not "sensitive health information." MNPI, not "insider-ish stuff." Privileged communications, not "legal-ish documents." Learning analytics, not "ed data." Chapter 01's data-class-mismatch failure mode shows up in Section 1 drafts routinely.

**Checkpoint 2:**

- [ ] Every data class in Section 1 is named in the industry's regulatory vocabulary.
- [ ] The population, tool, data flow, proposed change, and current posture are all one-line each.
- [ ] No interpretive language in Section 1 — no "it seems," "I believe," "arguably."

---

## Step 3 — Minutes 25–35: write Section 2 (specific decisions needed) (10 min)

Chapter 08 names what Section 2 carries: "the specific questions that need a decision — framed as decisions, not conclusions." This is the section where the operator-surfaces-a-question posture is most visible.

Template:

```markdown
## Section 2 — Specific decisions needed

### Decision 1 — <one-line decision ask>

- Context: <2-3 sentence operational framing of the decision>.
- Options (not recommended answers — options to decide among):
  - (a) <option, with operational implications>.
  - (b) <option, with operational implications>.
  - (c) <option, with operational implications>.
- Cost of a wrong-fast decision: <specific operational cost>.
- Cost of a slow decision: <specific operational cost, including downstream — operator population held in a pause, business-line pressure, scorecard signal>.

### Decision 2 (if applicable) — <one-line decision ask>

<same shape>
```

Two tells for Section 2:

- **"Decision" framing, not "recommendation" framing.** The lead does not write "I recommend option B because…" — that is Posture 3 pretending to be Posture 1. The lead writes "options (a), (b), (c) each have these operational implications; the decision is counsel's."
- **One or two decisions per meeting, not five.** Chapter 08's pre-read discipline is explicit that the pre-read is one page; a Section 2 with five decisions is a sign the conversation has been batch-collected. Split into multiple meetings.

**Checkpoint 3:**

- [ ] Section 2 has one or two decisions, each framed as a decision for counsel (not a recommendation from the lead).
- [ ] Each decision names at least two options — not a single "shall we do X?" (which is a recommendation masked as a decision).
- [ ] Each decision names the cost of a wrong-fast decision AND the cost of a slow decision.

---

## Step 4 — Minutes 35–45: write Section 3 (timing signal) (10 min)

Chapter 08 names what Section 3 carries: "when the decision is needed, what the cost of a delay is, what the cost of a wrong-fast decision would be."

Template:

```markdown
## Section 3 — Timing signal

**Decision needed by:** <specific date, with calendar-day distance>.
**Operational holding posture until then:** <hard pause | pilot in sandbox | existing approved use continues | other>.
**If counsel needs more time:** <what gets unblocked at <date 2>; what escalation path is available at <date 3>>.
**The escalation path if counsel is bottlenecked:** <specific named role — CRO, head of AI governance, chief medical officer, chief academic officer — not "escalate to leadership">.
**Scorecard signal:** <the metric that would surface counsel-queue latency to the broader org if this decision runs past <date 2>>.
```

Three tells for Section 3:

- **Specific dates, not "ASAP."** "ASAP" is a timing non-signal; the counterpart cannot plan against it.
- **The holding posture during the pause is explicit.** Counsel reads Section 3 and knows whether the operator population is held in a pause (which creates business cost over time) or whether existing approved uses continue (which means the delay is lower-stakes).
- **The escalation path is a named role, not an abstraction.** Chapter 08's ongoing-relationship moves name the capacity-signal discipline: surface the bottleneck, do not backfill it quietly.

**Checkpoint 4:**

- [ ] Section 3 has a specific date (not "ASAP") for the decision.
- [ ] The holding posture is explicit.
- [ ] The escalation path is a named role.
- [ ] The scorecard signal is named with a specific metric.

---

## Step 5 — Minutes 45–55: write the attached operational context + proposed structure + explicit non-asks (10 min)

Three short artifacts below the pre-read proper.

**Attached operational context.** The specific operational material counsel needs to form a view without an additional round of requests. Chapter 08: "Workflow diagrams, prompt examples, output patterns, intake-question responses, training-content drafts."

```markdown
## Attached operational context

- `workflow.md` — the 6-step operator workflow for the proposed use.
- `prompt-examples.md` — three representative prompts the operator uses, with the operator's role and the matter / case / task context.
- `output-examples.md` — the output each prompt produced in last week's pilot.
- `intake-questionnaire-responses.md` — the intake fields the operator filled on submission.
- `draft-aup-delta.md` — the one-paragraph AUP delta that would land if counsel's decision is to approve.
```

You don't need to produce every attachment for the lab — name them and give one sentence of what each would contain. The lab is the pre-read, not the attachments.

**Proposed structure for the answer.** Not a proposed answer — a structure.

```markdown
## Proposed structure for the answer (not proposed answer)

The decision could be made at three levels:

- **AUP level** (blanket rule across all operators for this data class + tool combination).
- **Per-customer / per-matter level** (case-by-case rule tied to the specific matter, case, or customer contract).
- **Per-request level** (operator submits each use for counsel's review — expensive to operate; defensible when the data class is extremely sensitive).

Operationally, I prefer the <AUP level | per-matter level> for reasons <scale + consistency | matter-level sensitivity + outside-counsel coupling>, but I defer to counsel on which level is actually load-bearing from a regulatory perspective. If the per-request level is where the regulation lands, the enablement-side operational cost is <N hours/week of counsel time and <N> days of operator lead-time per request> — I name this not as an argument against it but so the operational cost is visible in the decision.
```

**Explicit non-asks.** Short list of what you are *not* asking counsel to review in this meeting.

```markdown
## Explicit non-asks

- I am *not* asking counsel to review the specific wording of the training module draft; the module will be re-reviewed when counsel's decision lands.
- I am *not* asking counsel to redraft the AUP's data-class vocabulary; I will carry any wording decision from this meeting into the AUP in the next walking-redline slot.
- I am *not* asking counsel to render an opinion on the parallel question of <adjacent regulatory question>; I will route that separately through <adjacent counterpart>.
```

**Checkpoint 5:**

- [ ] Attached operational context names 3–5 specific items, each one sentence.
- [ ] Proposed structure proposes a *structure*, not an answer — three plausible decision levels named with operational implications.
- [ ] Explicit non-asks lists at least two things you are specifically not asking for.

---

## Step 6 — Minutes 55–70: run the drifted-sentence red-team on your own pre-read (15 min)

Chapter 08's "sentence patterns that have drifted" list is your red-team. Open your full pre-read and scan for each pattern. Score honestly.

```markdown
## Self-check against Chapter 08's drifted sentence patterns

For each pattern, did the draft contain a sentence matching it? Quote the sentence and the section it appeared in; then rewrite to the in-scope pattern.

- [ ] *"Under [rule], the correct approach is…"* — found in: <section or none>. Rewrite: <in-scope version>.
- [ ] *"Legally, this is permitted / prohibited because…"* — found in: <section or none>. Rewrite: <in-scope version>.
- [ ] *"Our counsel's position on this is X."* (unless you have confirmed this with counsel for this specific question in this specific context) — found in: <section or none>. Rewrite: <in-scope version>.
- [ ] *"The precedent on this is Y."* (precedent-citing is a legal act) — found in: <section or none>. Rewrite: <in-scope version>.
- [ ] *"The regulatory requirement is Z."* (interpreting the regulatory requirement is a legal act; summarizing a confirmed requirement is fine) — found in: <section or none>. Rewrite: <in-scope version>.

Also scan for the four questions-that-signal-drift (Chapter 08's named list):

- [ ] Did the pre-read phrase any question as *"What is the legal interpretation of…?"* in a way that asks the lead to answer rather than counsel? Rewrite as *"Operationally, we see [pattern] — what is counsel's position?"*
- [ ] Did the pre-read phrase any question as *"Is this permitted under…?"* framed as if the lead has formed an opinion? Rewrite to carry the question to counsel.
- [ ] Did the pre-read phrase any question as *"Does this regulation apply to our use case?"* with an implied answer? Rewrite — the applicability question is counsel's.
- [ ] Did the pre-read phrase any question as *"What should we do about this new regulation / guidance / enforcement action?"* with a proposed direction? Rewrite — the direction itself is counsel's.
```

**Checkpoint 6:**

- [ ] Every row in the red-team table has an honest answer (found / not found) and a rewrite where a drift was found.
- [ ] No rewrite reads as a cosmetic swap ("I'd read" → "it seems to me"). Chapter 08's in-scope patterns are structural ("Operationally, we see X — what is counsel's position?"), not synonym substitutions.

---

## Step 7 — Minutes 70–75: final consistency pass (5 min)

Open the full pre-read one more time and check:

- The pre-read fits on one page. If it is spilling to two pages, trim Section 1 or split one of the Section 2 decisions off to a separate meeting.
- The named counterpart appears only as a role (privacy officer, MRM lead, general counsel, chief privacy officer) — not with a name that implies familiarity the pre-read does not carry.
- The posture is Posture 1 throughout — no sentences have drifted into Posture 2 (refining counsel's draft) or Posture 3 (carrying a decision already made). Chapter 08 names mixing postures as the common failure.
- The explicit non-asks are clearly separated from the asks. Counsel scanning quickly can see what you are and are not asking for.

---

## Deliverable

- `industry-counsel-pre-read.md` with:
  - The one-page pre-read in three Chapter 08 sections.
  - The attached operational context list.
  - The proposed structure for the answer.
  - The explicit non-asks.
  - The self-check against the drifted-sentence patterns.

## Expected output shape

Roughly 1.5–2 pages of markdown total. The pre-read itself is one page; the attached-context / proposed-structure / non-asks / self-check sections add another half-to-one page.

## Checkpoint — self-evaluation

- [ ] Pre-read is on one page and in three Chapter 08 sections (operational situation / specific decisions needed / timing signal).
- [ ] Posture 1 is named at the top; the pre-read stays in Posture 1 throughout.
- [ ] Section 1 names data classes in the industry's regulatory vocabulary, not generic vocabulary.
- [ ] Section 2 has one or two decisions, each framed as a decision for counsel with at least two options and the cost of a wrong-fast vs. slow decision.
- [ ] Section 3 has a specific date, a holding posture, an escalation path (named role), and a scorecard signal.
- [ ] Proposed structure proposes a *structure*, not an answer.
- [ ] Explicit non-asks lists at least two things you are not asking for.
- [ ] Every row of the drifted-sentence self-check is honestly answered; any drift was rewritten.

## Common failure modes

- **Drifting into Posture 3 while claiming Posture 1.** The pre-read says "the decision could be made at AUP level or per-request level" (Posture 1 shape) but every piece of operational framing argues for AUP level and the "preference" section reads as a recommendation. Counsel reads a recommendation; counsel's job is to ratify or redline the recommendation rather than decide. Fix: read the proposed-structure section back critically. If counsel could sign off on your preferred option without engaging the decision, you have written a recommendation, not a decision ask.
- **Section 1 renders interpretations.** "It seems clear that under the minimum necessary standard…" is a Section 1 drift — Section 1 is operational facts. Fix: cut every "it seems," "I believe," "arguably" from Section 1. Move the thought (if it's load-bearing) into the proposed-structure section as "one reading would be X" — and even there, defer to counsel.
- **Timing signal is "ASAP."** The counterpart cannot plan against ASAP; the pre-read does not carry the information counsel needs to prioritize. Fix: specific date, specific holding posture, specific escalation path.
- **Explicit non-asks section missing.** Without non-asks, the meeting becomes an open-ended review. Fix: Chapter 08 names this as the discipline that *narrows* the ask; a pre-read without non-asks is one that invites drift.
- **Cosmetic rewrites in the drifted-sentence self-check.** Swapping "Under [rule], the correct approach is…" for "In my view, under [rule], the correct approach is…" does not fix the drift — adding "in my view" is still rendering a legal conclusion. Fix: the in-scope rewrite is structural — "Operationally, we see [pattern] — what is counsel's position?" — not a synonym swap.
- **Writing a pre-read that generalizes across industries.** The lab's instruction is to pick one specific conversation. A pre-read that reads as "here's a template for industry counsel conversations" is not the lab's deliverable. Fix: the pre-read must name a specific conversation with a specific counterpart on a specific decision; the discipline is the specificity.

## What this lab prepares you for

Industry-counsel conversations are a recurring motion for the enablement lead in any regulated industry — Chapter 08 names them as standing, agenda-driven, short, and *not* open. The quality of each conversation is set primarily by the quality of the pre-read; a bad pre-read turns a 45-minute decision meeting into a 90-minute exploratory discussion that never resolves. Running the pre-read discipline standalone, with the Chapter 08 red-team on your own draft, is the cheapest way to build the muscle before the first real meeting — where counsel's time is scarce, the business-line-lead's expectations are hard, and the pre-read is on the counterpart's desk 48 hours ahead of your name coming up in the conversation. The lab's output composes directly with Exercises 03 and 04: the responsibility-split RACI shows which counterpart owns which obligation; the policy-package deliverables are the artifact-level consequence of the decisions that pre-reads surface; and a well-run quarterly artifact review (Chapter 08's ongoing-relationship moves) is a sequence of pre-reads like this one, run against each counterpart in turn.
