# The One-Page Acceptable-Use Policy

> Twenty pages gets read by zero operators. One page, in operator voice, with concrete named uses on both sides of the line, gets read by every operator who opens the tool and most of the ones who did not. Length is a signing-surface problem, not a user problem — and you are the author who has to defend both.

## Why this is the first artifact

The acceptable-use policy (AUP) is artifact 1 of the rollout artifact set introduced in [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md). Every rollout opens with it; every policy conversation points back to it. It is also the artifact most likely to have been drafted on one side and pushed to the other for approval — producing the "hand-off" shape [Chapter 01](01-the-co-author-posture-and-the-redline-log.md) names as a failure posture.

This chapter is where the enablement side learns to draft an AUP that is *shaped to invite* the governance, legal, security, and privacy redline — a document your co-authors are happy to react to, not one they feel compelled to rewrite.

## Why one page

Length is the single biggest contributor to an unread policy. Operators do not read twenty-page AUPs. Line managers do not read aloud from twenty-page AUPs at team meetings. Champions cannot summarize twenty-page AUPs. The twenty-page draft is not a policy — it is a defense document.

One page is a hard constraint, not a soft target. The constraint forces the drafter to write *concretely* instead of *comprehensively*. Comprehensive is the governance partner's job inside the control library; concrete is the enablement side's job in the operator-facing document.

If the draft spills onto page three, something is wrong with how you are carving the content. The usual cause is restating the data classification scheme (that belongs in the data-handling SOP) or restating legal positions (that belongs in counsel's opinion, not the AUP).

## The seven sections of a usable AUP

### 1 — Scope and in-scope users

- Which tool (name it; include the version if version matters).
- Which environments (production, sandbox, both).
- Which populations are covered — employees, contractors, consultants, and others "acting on behalf of the organization" (the phrase that matches EU AI Act Article 4 deployer-side literacy language — see [mod-101 Chapter 05](../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md)).

If any of the three lines is vague, the policy is not scoped — it is advisory.

### 2 — Approved uses

At least five, named concretely, in operator voice. "Summarize meeting notes you took yourself" is a usable sentence; "productivity use cases" is not. Each approved use is a sentence that a line manager could read aloud without needing to improvise what it means.

The hard part is writing approved uses that are *concrete enough to be useful* without writing a cookbook. The test: can a reader tell within five seconds whether their intended use is on the list?

### 3 — Prohibited uses

At least five, named concretely, including the ones that are actually contested at your organization. The failure mode is listing the obvious — "do not use the tool to commit fraud" — and omitting the contested — "do not paste customer PII into prompts." The contested ones are the reason the policy exists.

Prohibited uses should include at least one entry on each of: sensitive data classes, external-facing output without review, high-risk decision categories (hiring, firing, credit, benefits eligibility, safety-of-life). The specifics are yours; the shape is non-negotiable.

### 4 — Data classes allowed and forbidden

Reference the organization's data classification scheme by name. Map which classes are allowed as input, which are allowed as output, and which are forbidden entirely. Do *not* re-author the classification scheme — the operational detail lives in the data-handling SOP ([Chapter 05](05-the-data-handling-sop.md)).

If no classification scheme exists at the organization yet, say so in the AUP and propose the minimum classes this policy needs. Flag the gap in the redline log so privacy can close it.

### 5 — The "if-in-doubt" default

**One sentence.** This is the most important sentence in the document — it is what a user does when the policy does not cover their case. Two standard defaults, each legitimate in different organizational postures:

- "Ask your manager." Right when the organization has already pushed AI judgment into line management and when managers have been trained to make the call. Pushes the decision to a role that has more context than policy drafting, but only if that role is prepared.
- "Do not use the tool." Right in high-risk environments where the cost of misuse exceeds the cost of a slower approval. Pre-decides against adoption on edge cases, which is sometimes exactly the choice to make.

Pick deliberately. Do not hedge. "Ask your manager or governance" is two sentences performing as one and will be ignored because it contains no default.

### 6 — Escalation path to governance and security

Named **roles**, not named **people**. People turn over; roles do not. Time-bound SLA expectations for governance response. Clear separation between governance questions (goes to `head-of-ai-governance` or `ai-governance-analyst` depending on the question) and security incidents (goes to the SOC and `ai-risk-engineer` — see [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)).

### 7 — Review cadence

When the policy reopens, by whom, and against what inputs. Annual at a minimum; biannually is more realistic for an actively-rolling AI estate. Name the inputs: council decisions since last review, incidents since last review, champion-network field signal, regulatory updates since last review.

A policy without a review cadence section is a policy that freezes at launch and drifts into irrelevance. The review cadence is the preempt.

## Co-author tags per section

Each of the seven sections carries a **co-author tag** — a short block naming who drafted it, who redlines it, who signs the legal reading, who signs the security reading, and who signs the privacy reading. A usable tag might look like:

```
Drafter: AI Enablement Lead (this role)
Redliner: head-of-ai-governance (L60)
Legal signer: counsel (data-protection practice)
Security signer: CISO delegate
Privacy signer: Data Protection Officer
```

Not every section needs every signature. Review cadence does not need a legal signer; data classes needs a privacy signer; escalation paths need a security signer.

**The uniformity test.** If every section's tag is identical, the author has not thought about section-level ownership. Non-uniform tags are evidence of real co-authoring; uniform tags are evidence of hand-off.

## The signing surface

The policy is signed by, at minimum:

- `head-of-ai-governance` (L60) — ratifies the policy.
- Counsel — signs the legal reading.
- CISO or delegate — signs the security reading.
- Privacy / DPO — signs the privacy reading.
- This role — signs as drafter and owner of operational enforcement.

Missing a signature is not a soft problem. Treat it as a launch gate — the AUP without full signature is not ready for the rollout artifact set ([mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md)).

## Two failure modes to call out specifically

### The vague AUP

"Do not misuse the tool" tells a user nothing. Vague AUPs feel safe to draft because they are hard to redline — there is no concrete claim to disagree with. They also fail as enforcement artifacts, because every ambiguous case drifts to interpretation. Operators then reinterpret in a direction that reads "permitted" and the policy's intent quietly erodes.

The fix is to write to the test — can a line manager read the section aloud at a team meeting and have operators know whether their case is covered. If not, rewrite.

### The frozen AUP

Drafted at launch, signed, never reopened. Six months later, the tool is being used for tasks the AUP did not anticipate and the policy no longer reflects what the organization permits. The review cadence section is the preempt; the walking-redline habit from [Chapter 01](01-the-co-author-posture-and-the-redline-log.md) is what makes the preempt real.

## Legal hooks, not legal opinions

The AUP must contain legal hooks — named data classes, named jurisdictions, named counterparty relationships — that counsel can attach obligations to. The AUP must *not* contain legal opinions — "this would violate GDPR" or "this exceeds the DPA's authorized use." Those are counsel's writing, not yours.

This is a load-bearing discipline in co-authoring and the first drift [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) names.

## Summary

- The AUP is a one-page operator-facing document, not a defense document. One page is a hard constraint.
- Seven sections: scope and in-scope users, approved uses, prohibited uses, data classes, if-in-doubt default, escalation path, review cadence.
- Approved and prohibited uses each need at least five concrete named entries. "Productivity" and "misuse" fail the aloud-at-a-team-meeting test.
- The if-in-doubt default is one sentence. Pick "ask your manager" or "do not use the tool" deliberately.
- Co-author tags per section, non-uniform, with drafter / redliner / legal-security-privacy signers named.
- Legal hooks, not legal opinions. See [Chapter 07](07-what-you-route-out-counsel-soc-architect.md).
- Signing surface is `head-of-ai-governance`, counsel, security, privacy, and this role. Missing any signature is a launch gate.
- Review cadence is the preempt for a frozen AUP; the walking redline from [Chapter 01](01-the-co-author-posture-and-the-redline-log.md) is how the cadence stays real.
