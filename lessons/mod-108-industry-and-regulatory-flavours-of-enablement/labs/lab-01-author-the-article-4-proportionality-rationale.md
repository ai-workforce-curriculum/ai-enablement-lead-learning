# Lab 01 — Author the Article 4 Three-Tier Proportionality Rationale

**Duration:** 60–75 minutes
**Format:** guided solo authoring — one polished one-to-two-sentence proportionality rationale per Article 4 tier, red-teamed against the three distortions Chapter 02 names
**Grounding chapters:** [02 — EU AI Act Article 4 — Training Content at Depth](../02-eu-ai-act-article-4-training-content-at-depth.md) (the three tiers, the written-rationale sentence, the three distortions), [01 — The Industry-Flavour Problem](../01-the-industry-flavour-problem.md) (shape vs. content)

## Objective

Produce the **three proportionality-rationale sentences** — one for the leadership tier, one for the operator tier, one for the specialist tier — that Chapter 02 names as "the sentence the regulator reads," written in the regulator's own language and sized at one-to-two sentences each.

Chapter 02 writes a *worked example* rationale per tier ("The leadership tier equips the executive with the technical knowledge of AI systems' capabilities and failure modes…" and the parallel operator and specialist sentences). The lab's deliverable is not those sentences — the lab's deliverable is *your* sentences, written for *your* chosen organization, red-teamed against the three distortions, dated and signable.

This lab is not Exercise 01. Exercise 01 asks for the *whole tier outline* across five required sections (audience / content outline / duration / assessment / rationale). The outline-level exercise reliably under-produces on the rationale sentence because it is the smallest artifact on the deliverables list and the easiest to leave in a passive-voice first draft. This lab zooms in on that sentence at depth so the muscle is built before Exercise 01 runs.

## Prerequisites

- Chapter 02 read end-to-end, especially *The three tiers, concretely* (the worked example rationales), *The three distortions to resist*, and *Evidence the regulator reads*.
- Chapter 01 skimmed — the "shape vs. content" frame informs how the rationale is written against an industry overlay later.
- A chosen organization that has some EU-touching activity. If you don't have one in mind, pick one of these (the same three Exercise 01 uses, so you can carry forward):
  - A 6,000-person US-headquartered SaaS company with a 400-person EU engineering and sales presence across Dublin, Berlin, and Barcelona, no EU consumer customers but EU B2B customers and EU employees.
  - A 15,000-person US-headquartered financial services company with a 1,800-person London office post-Brexit and sales relationships with EU corporate clients.
  - A 3,500-person US-headquartered pharma / medical-device company with EU operations in Switzerland, Germany, and Belgium and EU clinical trials.
- A single markdown file.
- A timer.

## Why a lab, not an exercise

Exercise 01's acceptance criterion names the rationale as one of five required sections: *"The written proportionality rationale is one to two sentences in the regulator's own language — not corporate-tone filler."* That is the ask at the outline altitude. The problem is that the rationale is simultaneously the hardest sentence to write (the regulator's voice is different from both corporate-tone and operator-voice) and the smallest item on the page — so first drafts routinely land as "the leadership tier provides comprehensive AI awareness training appropriate to executives' responsibilities," which satisfies no part of Article 4 and reads as the first distortion Chapter 02 names (literacy-as-marketing).

A standalone drill with the three distortions as a red-team panel is the cheapest way to build the sentence-level muscle before the full curriculum build. Three sentences, three red-team passes, one revision cycle.

## Setup

Create `article-4-proportionality-rationales.md` with this skeleton:

```markdown
# Article 4 — Proportionality Rationales (Three Tiers) — <organization>

**Date drafted:** <today>
**Drafter:** AI Enablement Lead (me)
**Organization:** <name, size, EU-touching surface>
**Intended signers at Exercise 01 scope-definition stage:** enablement lead, head of AI governance, general counsel, chief people officer or HR partner, head of the EU subsidiary (if one exists)
**Version:** v0.1 — standalone sentence drill ahead of Exercise 01

---

## Tier 1 — Leadership

**Audience (one line, named populations):**

**Rationale v0.1 (one-to-two sentences, regulator's voice):**

**Red-team pass:**
- [ ] Not marketing e-learning distortion (short-video / certificate reading)
- [ ] Not blanket-engineering-course distortion (over-depth for the audience)
- [ ] Not literacy-as-communications distortion (internal-marketing voice)
- [ ] Specifically names the audience's *context* under Article 4's own language (decision-maker on deployment direction, not operator of tools)

**Rationale v0.2 (after red-team):**

---

## Tier 2 — Operator

<same shape>

---

## Tier 3 — Specialist

<same shape>

---

## Debrief — what the drill taught me

<entries>
```

Set your timer to 60 minutes and start. Treat the final 15 as the debrief-and-margin window.

---

## Step 1 — Minutes 0–5: ground in the Article 4 language (5 min)

Re-read these two short passages in Chapter 02 — not for content, for *voice*:

- *The three tiers, concretely* — the three worked-example rationale sentences at the end of each tier subsection.
- *The three distortions to resist* — the paragraph on each distortion.

Then add one line to your file naming, in your words, what each of the three worked-example sentences does *as a sentence*:

```markdown
**What the Chapter 02 worked rationales do, as sentences:**
- Leadership: names the technical knowledge, the organizational knowledge, and the *contextual judgment* appropriate to a decision-maker.
- Operator: names the envelope, the escalation, and the role-specific transparency obligations under Article 50 where applicable.
- Specialist: names the enablement-side layer and *explicitly defers* the engineering-depth content to the adjacent curricula.
```

This is the voice you are writing in. If your draft does not sound like these, revise until it does.

**Checkpoint 1:**

- [ ] The three-line note on the Chapter 02 voice is written and sits at the top of your file.
- [ ] Time on the clock is still under 5 minutes.

---

## Step 2 — Minutes 5–20: draft the leadership tier rationale (15 min)

Name your organization's leadership population in one line. Then write the leadership rationale as a one-to-two-sentence v0.1.

Template:

```markdown
**Audience:** Executives (C-suite and their direct reports), board members where applicable, and senior managers whose decisions set direction on AI investment, deployment, or policy at <org>. Approximately <N>% of in-scope headcount (~<count>).

**Rationale v0.1:** "The leadership tier equips <named population> with <specific knowledge classes — technical / organizational / contextual-judgment>, appropriate to the <audience>'s role as <Article 4-anchored framing: decision-maker on AI deployment direction, not operator of AI tools>."
```

**Red-team your v0.1 against the three distortions** (open the file section's four checkboxes and tick or un-tick honestly):

- **Marketing e-learning distortion.** Does the sentence read as "a short video and a quiz and a certificate"? If a compliance partner reading the sentence would picture the 20-minute SCORM package, the sentence is still in the distortion. Tell: adjectives like *awareness*, *introduction*, *overview* with no named depth. Fix: name the specific knowledge classes (technical / organizational / contextual-judgment) that Chapter 02 names.
- **Blanket-engineering-course distortion.** Does the sentence promise depth the leadership audience does not need and will not sit through? Tell: phrases like *in-depth technical training on AI model architectures*. Fix: Chapter 02 is explicit — for the leadership tier the material is at the *altitude a decision-maker needs*, not operator-altitude or specialist-altitude.
- **Literacy-as-communications distortion.** Does the sentence sound like internal marketing — exciting, visionary, forward-looking? Tell: words like *empower*, *transform*, *future-ready*, *champion*, *journey*. Fix: Chapter 02 is explicit that internal communications is a separate channel (mod-105), and the literacy curriculum is not that channel; the rationale sentence should read as a regulator would read it.

Write v0.2 below the checkbox. If v0.1 passed all three checkboxes and you can also honestly tick "specifically names the audience's context under Article 4's own language," copy v0.1 forward as v0.2 — do not manufacture a change for the sake of looking revised.

**Checkpoint 2:**

- [ ] Leadership tier audience line is specific to your organization — named population, headcount estimate.
- [ ] Rationale v0.1 is written in one-to-two sentences, not three, not a paragraph.
- [ ] All four red-team checkboxes are honestly ticked or revised against.
- [ ] Rationale v0.2 is final or a copy-forward from v0.1 with a note.

---

## Step 3 — Minutes 20–35: draft the operator tier rationale (15 min)

The operator tier is the *default* tier — most in-scope headcount lands here. Chapter 02's worked example names three content elements the rationale should reference: the acceptable-use and data-handling envelope, the failure signals that require escalation, and the transparency obligations attached to the operator's role under Article 50 *where applicable*.

Template:

```markdown
**Audience:** Employees and contractors at <org> using AI tools in the course of their work — the *default* tier. Approximately <N>% of in-scope headcount (~<count>).

**Rationale v0.1:** "The operator tier equips <named population> to <operate approved AI tools inside the organization's acceptable-use and data-handling envelope>, <recognize the failure signals that require escalation>, and <meet the transparency obligations attached to the operator's role under Article 50 where applicable>, appropriate to the operator's role as <a user of AI systems in the course of their work>."
```

Two specific tells for the operator sentence:

- **"Where applicable" is load-bearing.** Not every operator role produces content that interacts with people in a way that engages Article 50; the rationale honors that. A sentence that promises Article 50 transparency training to every operator uniformly is over-broad and signals the blanket-engineering-course distortion.
- **"Failure signals that require escalation" is the specific Chapter 02 phrase.** Not "best practices" or "responsible AI principles" — the regulator reads *escalation* as a verifiable operational behaviour and *failure signals* as a specific content area in the curriculum.

Red-team v0.1 against the three distortions. Write v0.2.

**Checkpoint 3:**

- [ ] Operator audience line specifies the operator population at your org, not "all employees."
- [ ] Rationale v0.1 names the envelope, the escalation, and Article 50 *where applicable* — not all uniformly.
- [ ] Red-team checkboxes ticked honestly; v0.2 landed.

---

## Step 4 — Minutes 35–50: draft the specialist tier rationale (15 min)

The specialist tier rationale has a specific structural move Chapter 02 is explicit about: it **defers** substantial content to the adjacent AI Engineering curricula (`applied-ai-engineer-learning`, `ai-risk-engineer-learning`) and names the enablement-side content as the policy / operating-model / escalation / transparency layer only.

Template:

```markdown
**Audience:** People at <org> whose job is to build, configure, red-team, administer, or deeply review AI tools — typically engineering, risk-engineering, ML, and security-engineering populations. Approximately <N>% of in-scope headcount (~<count>).

**Rationale v0.1:** "The specialist tier equips <named population> with the deeper technical and risk material appropriate to the specialist's context — deferred to the adjacent <named curricula> where the engineering-depth content lives, with the enablement-side content providing the policy, operating-model, escalation, and transparency layer."
```

Two tells for the specialist sentence:

- **The deferral is explicit and named.** The rationale should *reference* the adjacent curricula by name so the regulator can see the engineering-depth evidence trail without the enablement lead needing to be in the room. "The engineering-depth material is covered by the adjacent AI Engineering curricula" is weaker than "…is covered by `applied-ai-engineer-learning` and `ai-risk-engineer-learning`" (which names the evidence surface).
- **The enablement-side content is scoped.** The rationale names *what the enablement side owns* for this tier (policy, operating-model, escalation, transparency) — not "everything engineering plus some policy."

Red-team v0.1. Write v0.2.

**Checkpoint 4:**

- [ ] Specialist audience line names populations specifically (engineering, risk-engineering, ML, security-engineering), not "technical staff."
- [ ] Rationale v0.1 explicitly names the adjacent curricula the engineering-depth content defers to.
- [ ] The enablement-side layer is scoped to policy / operating-model / escalation / transparency — not padded.
- [ ] Red-team checkboxes ticked honestly; v0.2 landed.

---

## Step 5 — Minutes 50–55: cross-tier consistency pass (5 min)

Three tier sentences must read as a *family*, not three independent paragraphs. Open the file and check:

- [ ] All three sentences use the pattern "the [tier] equips [audience] with [content], appropriate to [audience]'s role as [context]." Variation in exact wording is fine; variation in *shape* breaks the family.
- [ ] No distortion-tell words (*empower*, *comprehensive*, *robust*, *transform*, *journey*) survive in any of the three sentences.
- [ ] The headcount percentages roll up to a defensible total — typical splits are roughly 1–3% leadership / 85–95% operator / 5–10% specialist, varying by industry. If your percentages don't roll up, revise the audience lines before the rationales ship.

Revise any sentence that fails the cross-tier pass.

---

## Step 6 — Minutes 55–75: debrief (15 min including margin)

Write a short debrief answering these four prompts. One or two sentences each.

```markdown
## Debrief — what the drill taught me

1. **Which tier's rationale took the most revision passes, and why?**
   <answer>

2. **Which of the three distortions was my v0.1 closest to on the tier that was hardest?** (marketing / blanket-engineering / literacy-as-communications)
   <answer>

3. **If this organization added an industry overlay (healthcare / finance / legal / education), which tier's rationale would change the most, and what specifically would be added?** (Cross-reference the industry chapter you are weakest on.)
   <answer>

4. **What is the sentence pattern I would default to in v0.1 next time I draft a proportionality rationale from scratch?**
   <answer>
```

**Checkpoint 6:**

- [ ] All four debrief prompts answered.
- [ ] Prompt 3 names a specific industry and a specific content addition — not a generic "add compliance content."

---

## Deliverable

- `article-4-proportionality-rationales.md` — one page, with:
  - Three tier-level sections, each carrying the audience line, v0.1, the red-team checkboxes, and v0.2.
  - The cross-tier consistency pass notes.
  - The four-prompt debrief.

## Expected output shape

Roughly 1–1.5 pages of markdown. Three polished rationale sentences, each one-to-two sentences, each in regulator voice, each red-teamed. Not three paragraphs. If the file is running past two pages, the drill has drifted into Exercise 01 and should be trimmed.

## Checkpoint — self-evaluation

- [ ] Three rationale sentences, each one-to-two sentences long, present as v0.2.
- [ ] Each sentence specifically names the audience's *context* under Article 4's own language — Chapter 02's phrasing ("appropriate to the [role]'s role as [context]") is the anchor, not corporate tone.
- [ ] No distortion-tell words remain (*empower*, *comprehensive*, *robust*, *transform*, *journey*, *awareness*, *introduction*, *overview*).
- [ ] The specialist rationale names the adjacent AI Engineering curricula explicitly (not "engineering tracks" in the abstract).
- [ ] Cross-tier shape is consistent — three sentences read as a family.
- [ ] The debrief names a specific industry overlay and specific content addition that would change one tier's rationale.

## Common failure modes

- **Corporate-tone first draft that never gets red-teamed.** The sentence reads as "comprehensive and robust AI literacy training appropriate to each audience's responsibilities." Every adjective is filler; no specific content is named; the regulator has no verifiable claim to read. Fix: write v0.1 fast and *expect* to revise through the red-team checkboxes — Chapter 02 is explicit that the rationale is the sentence an auditor reads most carefully.
- **Operator rationale over-claiming Article 50 uniformly.** The sentence promises Article 50 transparency training to every operator; most operator roles do not produce content that engages Article 50. Fix: the "where applicable" qualifier is load-bearing — honor it.
- **Specialist rationale re-producing engineering content.** The sentence promises deep technical content on model evaluation, red-teaming, Chapter III obligations in full. The enablement side does not own that content; the adjacent AI Engineering curricula do. Fix: Chapter 02 is explicit that the specialist tier *defers* substantial content to the adjacent curricula and the enablement side provides the policy / operating-model / escalation / transparency layer. Name the deferral; name the adjacent curricula.
- **Three tiers written in three different shapes.** Leadership reads as prose, operator reads as a list of bullet-targets, specialist reads as a job description. The regulator reads the three as a family and consistency is the diagnostic that the author thought across tiers. Fix: pass 5's cross-tier consistency pass is specifically for this.
- **Headcount percentages that don't roll up.** Leadership 10%, operator 70%, specialist 25% = 105%. Or operator 20% in an organization that is mostly line-of-business. The rollup is a tell that the audience lines were written independently and the author has not thought about *who in scope lands in each tier*. Fix: write the headcount splits once at the top of the file and check the sum before writing any rationale.

## What this lab prepares you for

Exercise 01 asks for the whole three-tier outline including the rationale sentences. In production, the rationale sentences are what the general counsel, the EU subsidiary lead, and (eventually) a market-surveillance authority read first — at outline review, at scope-definition signing, during any Article 4 inquiry. The outline bullets around them tell the story of *what you teach*; the rationale sentence tells the story of *why this is the right content for this audience under Article 4*. Running the sentence-level drill standalone, with the three distortions as the red-team panel, is the cheapest way to build that voice before Exercises 01 and 05 need it in multiple places. In production, these three sentences — once right — become the stable kernel that your industry-adjusted curriculum (Exercise 05) adds content to without re-writing the proportionality claim.
