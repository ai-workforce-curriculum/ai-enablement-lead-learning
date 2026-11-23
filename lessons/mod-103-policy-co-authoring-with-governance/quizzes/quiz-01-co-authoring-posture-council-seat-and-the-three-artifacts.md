# Quiz 01 — Co-Authoring Posture, the Council Seat, and the Three Artifacts

**Format:** multiple choice · **Questions:** 10 · **Estimated effort:** 20–25 minutes
**Grounding:** [Chapter 01](../01-the-co-author-posture-and-the-redline-log.md), [Chapter 02](../02-the-governance-council-liaison-seat.md), [Chapter 03](../03-nist-ai-rmf-govern-and-iso-iec-42001-for-the-enablement-seat.md), [Chapter 04](../04-the-one-page-acceptable-use-policy.md), [Chapter 05](../05-the-data-handling-sop.md), [Chapter 06](../06-the-intake-questionnaire.md), [Chapter 07](../07-what-you-route-out-counsel-soc-architect.md)

## How to take this quiz

Pick the single best answer for each question. Each question tests whether you can *apply* a chapter idea — paraphrasing the chapter is not enough. The answer key with short explanations is at the bottom; resist reading it until you have your own answers written down.

---

### Q1. A time-pressed enablement lead sends the acceptable-use policy draft to `head-of-ai-governance` with a two-line email: *"Here it is — let me know if you have edits, otherwise I'll route for signature next Friday."* Governance replies three days later with no substantive redlines and a countersignature. Under Chapter 01, the failure posture this most closely matches — and the near-term consequence — is:

- **A.** No-artifact; the policy will quietly be renegotiated on a whiteboard at the next meeting.
- **B.** Hand-off; governance signed without participating in the thinking, and within six months the policy will carry carveouts nobody can defend and the org will be on its fourth draft.
- **C.** Abdication; governance will now rewrite the document in governance voice that operators cannot parse.
- **D.** Successful co-authoring — a quick turnaround is the sign of a well-shaped draft.

### Q2. Which of the following best describes what the redline log must capture — and why it, rather than the signed PDF, is treated as the artifact of co-authoring?

- **A.** A short summary of each co-author meeting so stakeholders can reconstruct who said what.
- **B.** One row per redline with before text, after text, the partner's rationale in their own language, and a resolution tag (`accepted`, `revised`, `escalated`, `declined`) — kept in the same repo as the draft because heads of governance, counsel, and CISOs turn over and the next partners can only inherit the reasoning behind each clause through the log.
- **C.** A standing weekly minute entry filed to the shared drive; auditors prefer the PDF because it carries the signatures.
- **D.** A redline log is optional once the policy is signed; its only purpose is to track open items until signature.

### Q3. At the next AI governance council, the enablement lead plans to (a) walk counsel through why their GDPR position on vendor retention is wrong, (b) propose a redesigned risk-classification tier, and (c) push for a change to next quarter's program plan. Which of the three is the only one that even belongs in the room for the enablement seat — and what is the correction to the other two?

- **A.** (a) only — legal corrections are part of co-authoring; (b) is architect work; (c) is `head-of-ai-governance` program leadership.
- **B.** (c) only — the enablement seat votes on program direction; the other two are out of scope.
- **C.** None of the three — (a) is counsel's reading and the correct move is to ask counsel a specific question rather than counter-argue; (b) is `senior-ai-governance-architect` territory and the correct move is to bring evidence that a control is not being evidenced in practice, not to propose a replacement; (c) is `head-of-ai-governance` program leadership and the enablement seat consumes it, does not shape it at council.
- **D.** All three — the enablement seat should bring positions on every substantive agenda item.

### Q4. The council pre-read for Tuesday's meeting arrives in the chair's inbox 48 hours ahead. It is three pages long, every item is tagged `informational`, and Section 3 ("field signal from champions") contains a single anecdote from one champion in one BU. Under Chapter 02, the three defects — in order of how they damage the seat — are:

- **A.** Length first, timing second, naming third; shorten the document and resubmit.
- **B.** Timing first, length second, naming third; 48 hours ahead is too early.
- **C.** The all-informational tag means the seat is not being used (if everything is informational, the seat is wasted); the single-anecdote Section 3 fails the pattern threshold (field signal is a pattern surfaced across multiple champions or BUs, not one voice); and the three-page length violates the one-page constraint that keeps the council's scarce time usable.
- **D.** Section 3 is correct as a one-champion observation; the other two are stylistic.

### Q5. A governance partner in a 42001 pre-certification conversation asks: *"which pieces of your work map to Clause 7, and which to Annex A?"* Under Chapter 03, the correct enablement-side framing is:

- **A.** The enablement seat owns Annex A directly, since its controls are operator-facing; Clause 7 is a governance-only concern.
- **B.** Clause 7 (Support — especially 7.2 Competence and 7.3 Awareness) is the enablement lead's primary audit-evidence surface — training records evidence 7.2, awareness-communication records evidence 7.3 — while Annex A is `senior-ai-governance-architect` territory where the architect writes the Statement of Applicability and the enablement side feeds the training/competence/awareness evidence the architect needs.
- **C.** All ten clauses are the enablement lead's authoring surface; the architect's work begins outside 42001 entirely.
- **D.** Clause 7 is architect territory and Annex A is counsel territory; the enablement seat has no mapping to either.

### Q6. An AUP draft contains this "if-in-doubt" section: *"If a situation is not covered, ask your manager or governance, or escalate to security if you think the issue is sensitive — use your best judgment."* Under Chapter 04, the primary problem with this sentence — and the fix — is:

- **A.** The sentence is too short; it should enumerate at least three scenarios.
- **B.** The sentence hedges two or three defaults performing as one and will therefore be ignored because it contains no actual default; the fix is to pick deliberately — either "ask your manager" (right when managers have been trained to make the call) or "do not use the tool" (right in high-risk environments) — as one sentence, without the "or" branches.
- **C.** The sentence is fine as long as managers are copied on every escalation.
- **D.** The sentence should be moved to the data-handling SOP; the AUP does not need an if-in-doubt default.

### Q7. An enablement lead finishes an AUP draft where every one of the seven sections carries an identical co-author tag: *"Drafter: AI Enablement Lead; Redliner: head-of-ai-governance; Legal signer: counsel; Security signer: CISO delegate; Privacy signer: DPO."* Under Chapter 04, what does the uniform tag reveal, and what is the correct redraft move?

- **A.** Uniform tags are the mark of a fully co-authored policy; no change needed.
- **B.** Uniform tags are evidence that the author has not thought about section-level ownership — not every section needs every signature (review cadence does not need a legal signer; data classes needs a privacy signer; escalation paths need a security signer); the redraft makes each tag specific to that section's actual owners, producing non-uniform tags as the evidence of real co-authoring.
- **C.** Uniform tags are fine for the first draft; governance will adjust them in the walking redline.
- **D.** Uniform tags are a hand-off failure; the fix is to delete the tags entirely and let governance decide.

### Q8. The data-handling SOP for a new tool is ready except that the CISO delegate has not signed sections 2 and 3 (retention, egress) and the DPO has not signed section 4 (the accident path, which they co-sign with security). Launch is in four days. Governance and counsel have ratified the document. Under Chapter 05, the correct call is:

- **A.** Launch; governance and counsel coverage is sufficient, and security/privacy can sign in the first week post-launch.
- **B.** Launch to a small subset while the signatures land.
- **C.** Do not launch — security and privacy are the critical co-authors on the data-handling SOP, and without **both** their signatures the tool is not approved for GA; this is a hard launch gate, not a judgment call.
- **D.** Launch; the SOP is operational and sits outside the artifact-set gate.

### Q9. An enablement lead has been running intake for three quarters. They notice that the "data classes touched" field is systematically mis-filled by requesters in regulated-domain tasks, and want to help. Under Chapter 06, which of the following is the correct move — and which is the drift Chapter 07 names as most insidious?

- **A.** Rewrite the field definition in the next schema release; this is enablement-side runner work.
- **B.** Write a quarterly evidence memo to `senior-ai-governance-architect` naming the specific submissions where the field was mis-filled, framing the proposal as a shape of refinement for the architect's decision — not a redesigned field, not a proposed value enumeration; the drift to avoid is the architect-level one where you write the redesigned field yourself, which Chapter 07 names as the most insidious because it feels like upgrade and is actually quiet role collapse.
- **C.** Add a validation rule to the submission form that rejects non-conforming values; keep the schema itself unchanged.
- **D.** Raise the issue at council as a decision ask and let the chair decide between the two options.

### Q10. A user Slacks the enablement lead on a Friday afternoon: *"I think I just pasted a customer's full support history into the chat assistant by mistake — what do I do?"* Under Chapters 05 and 07, what is enablement-side and what is SOC-side in the next hour?

- **A.** Enablement runs the full forensic workstream (log analysis, vendor coordination, notification-clock management); SOC is informed when the investigation closes.
- **B.** Enablement tells the user to delete the prompt immediately to reduce blast radius; SOC handles anything that remains.
- **C.** Enablement handles the first ten minutes — triages the accident shape (this is the paste-mistake path), runs the SOP's accident-path script with the user including "do not delete the prompt" so evidence is preserved, names the role-level contact and channel, packages the enablement-side evidence (prompt text, output, timestamp, user context), and hands off to the SOC and `ai-risk-engineer` for the forensic workstream; SOC handles forensic acquisition, model/log forensics, vendor coordination, and any regulator-notification-clock management, with `head-of-ai-governance` and counsel owning regulator-facing communications.
- **D.** Enablement escalates the message directly to counsel so counsel can decide the notification clock before any technical response.

---

## Answer key

**Q1 — B.** Chapter 01 names hand-off ("Here, approve this") as the posture where the enablement side writes the whole thing, governance signs without substantive redlines because they did not participate in the thinking, and six months later the policy has three carveouts nobody can defend and the org is on its fourth draft. A quick countersignature without redlines is the diagnostic signal, not a win. (Chapter 01 — *Why "posture" is the first word of this module*.)

**Q2 — B.** Chapter 01 defines the minimum-viable log as one row per redline with Before / After / Rationale / Resolution, kept in the same repo as the draft, and names personnel turnover as the reason the log — not the signed PDF — is the artifact: when the head of governance / counsel / CISO rotates, the next partner inherits the reasoning behind each clause only through the log. Auditors usually find the log more valuable than the policy itself because it shows *how* decisions are made, not only what the current one is. (Chapter 01 — *The redline log* and *Why the log survives personnel changes*.)

**Q3 — C.** Chapter 02's "What you do not do at council" names three drifts: argue a legal reading (correct move: ask counsel a specific question, don't counter-argue), redesign the control library (bring evidence that a control is not being evidenced; don't propose replacement controls), and vote on program direction (consume it; don't shape it). All three of the vignette's items are drifts; none belongs in the room from the enablement seat. (Chapter 02 — *What you do not do at council*.)

**Q4 — C.** Chapter 02 names the pre-read discipline: one page, three sections, named ask per item (`decision` / `discussion` / `informational`). The chapter is explicit that "if everything is informational, you are not using the seat." Section 3 (field signal) requires a *pattern* — Exercise 04 names the threshold as at least three champions reporting the same pattern or the pattern observed across at least two BUs; a single-user anecdote fails the threshold. Length violates the one-page rule that keeps the council's scarce time useful. (Chapter 02 — *The pre-read* and *Job 3*.)

**Q5 — B.** Chapter 03 is explicit: Clauses 5, 6, and 7 are the enablement lead's primary surfaces, with 7.2 Competence and 7.3 Awareness as the primary audit evidence surfaces (training records evidence 7.2; awareness-communication records evidence 7.3). Annex A is architect territory — the architect designs the Statement of Applicability against Annex A; the enablement side operates the pieces that touch training, competence, and awareness and feeds the evidence the architect needs. (Chapter 03 — *The clauses this role touches* and *Annex A*.)

**Q6 — B.** Chapter 04 names the "if-in-doubt" default as the most important sentence in the document, says to pick one of the two standard defaults ("ask your manager" or "do not use the tool") deliberately, and is explicit that hedged compound forms like "ask your manager or governance" are "two sentences performing as one and will be ignored because [they] contain no default." (Chapter 04 — *Section 5 — The "if-in-doubt" default*.)

**Q7 — B.** Chapter 04's uniformity test states: "If every section's tag is identical, the author has not thought about section-level ownership. Non-uniform tags are evidence of real co-authoring; uniform tags are evidence of hand-off." The chapter also names which sections need which signers: review cadence does not need a legal signer; data classes needs a privacy signer; escalation paths need a security signer. (Chapter 04 — *Co-author tags per section*.)

**Q8 — C.** Chapter 05 is explicit: security and privacy are the critical co-authors on the data-handling SOP and their signatures are a hard launch gate — "without both signatures the tool is not approved for GA. This is a hard launch gate — not a soft conversation at the governance council." Governance and counsel ratify at the end of the cycle but do not substitute for security + privacy on this artifact. (Chapter 05 — *Why security and privacy are the critical co-authors*.)

**Q9 — B.** Chapter 06 is explicit that schema is architect-owned and the enablement side does not redesign it: the move is the co-authoring beat on schema — a cyclic evidence memo to `senior-ai-governance-architect` framed as architect-decides, with specific submission references and a shape of refinement, not a redesigned field or proposed value enumeration. Chapter 07 names the control-library/architecture drift as the most insidious of the three because it feels like upgrade and reads like competence — "they are not; they are quiet role collapse." (Chapter 06 — *The co-authoring beat on schema*; Chapter 07 — *Drift 3*.)

**Q10 — C.** Chapter 05's accident path is the crown-jewel section: operator-voice, first ten minutes, "do not delete the prompt" because the deleted prompt still exists in the tool's retention and deleting it destroys evidence; triage the accident shape (paste-mistake, subtly-wrong-output, tool-malfunction); contact a named role on a named channel; preserve exact prompt / output / timestamp / user context; hand off to SOC. Chapter 07 draws the enablement/SOC boundary: enablement convenes, triages, and hands off within an SLA — the SOC and `ai-risk-engineer` run forensic acquisition, log/model forensics, vendor coordination, and `head-of-ai-governance` + counsel own regulator-facing communications. A (enablement runs forensics) and D (counsel decides the clock first) both drift into routed-out work; B (delete the prompt) destroys evidence. (Chapter 05 — *The accident path* and *Where the SOP ends and SOC-side handling begins*; Chapter 07 — *Drift 2*.)
