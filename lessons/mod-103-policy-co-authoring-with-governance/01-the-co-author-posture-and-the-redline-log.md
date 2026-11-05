# The Co-Author Posture and the Redline Log

> A policy that reads as one side handing another a draft to approve gets ignored by both when it reaches the operator. A policy that reads as the written outcome of two sides negotiating gets enforced by both. This chapter is the posture — and the small artifact — that makes the second reading true.

## Why "posture" is the first word of this module

Most AI-tool policies in large organizations are not wrong. They are *orphaned* — authored on one side of a wall, pushed over for approval, received without ownership, and then quietly disregarded when a user is in the middle of a task and the policy feels like someone else's rule. The fix is not a stricter policy. The fix is a different *posture* for how the policy was written in the first place.

Co-authoring is the posture where the enablement side drafts, the governance partners redline, and the two sides sign something they both think they wrote. It sounds obvious. It is nearly always skipped under time pressure. Three skipped shapes are worth naming.

- **Hand-off** — "Here, approve this." The enablement side writes the whole thing. Governance signs without substantive redlines because they did not participate in the thinking. Six months later, the policy has three carveouts that nobody can defend and the org is on its fourth draft.
- **Abdication** — "You tell me what the policy should be." The enablement side asks governance to produce the whole thing. Governance writes a document in governance voice that operators cannot parse. Nobody enforces it; champions quietly rewrite it on wikis.
- **No-artifact** — "Let's do it together on a whiteboard." The two sides meet, align, and leave the room feeling aligned. Nothing durable gets written. The next time anyone asks what the policy says, the answer is a recollection of a meeting.

Co-authoring is none of those. It is the posture of writing a draft that is *specifically shaped to invite the other side's redline* — then capturing the redline in a log that survives personnel changes.

## The four partners this role co-authors with

The enablement lead's co-authors on any policy artifact in this track are:

- **Legal counsel.** Writes the legal reading — what the regulation obliges, what the contract permits, what the disclosure requirement is. You write *hooks* for legal (named data classes, named jurisdictions, named counterparty relationships); legal writes *opinions* that attach to those hooks. The distinction is Chapter 07.
- **Risk & compliance.** Writes the risk classification, the control mapping, the residual-risk statement. In mature orgs this is the `head-of-ai-governance` (L60) and the `senior-ai-governance-architect` (L50) between them — the architect designs the taxonomy, the head of governance ratifies.
- **Information security.** Writes the technical controls that enforce the policy — DLP rules, tenancy settings, logging configuration, access review. You write the user-facing procedure that sits on top of the controls; security writes the controls themselves.
- **Privacy.** Writes the data-class mapping, the retention statement, the data-subject-rights touchpoint. In EU-touching orgs this is non-negotiable. You name the data classes; privacy attaches the obligations each class carries.

Each partner brings a language the enablement side cannot fake. The co-authoring posture is exactly the admission that you need their language on the page — and that they need yours.

## What the enablement side brings that none of the four brings

If you only bring convening, you will be mistaken for an executive assistant. The enablement side brings three pieces of content the four partners usually cannot source alone.

1. **The operator-voice reading.** Policies drafted by legal, security, privacy, and governance are optimized for defensibility. They often fail the "line manager reads this aloud at a team meeting" test. Your job is to redraft until the document survives that test without losing its legal and technical hooks.
2. **Champion-network field signal.** You see where the current policy fails in practice — the use case that champions keep asking about, the data class that keeps getting pasted in by mistake, the carveout that only exists because a VP once asked for it. That signal is feedstock for every redline cycle.
3. **Training-package coupling.** When the policy changes, the training package has to change in the same cycle. None of the four partners owns the training package. If the policy change ships without the training change, operators learn the old policy and the new policy simultaneously — and they default to whichever is easier.

The co-authoring posture is a trade: the partners' language for your three contributions. Without the trade, the policy has one half of what it needs.

## The redline log — the artifact of co-authoring

The draft is not the artifact. The signed PDF is not the artifact. The artifact is the **redline log** — the running record that proves the two sides negotiated.

A minimum-viable redline log is a table with one row per redline:

| Date | Document | Section | Partner | Before | After | Rationale | Resolution |
|------|----------|---------|---------|--------|-------|-----------|------------|

- **Before / After** capture the exact text that changed — not a summary.
- **Rationale** is the partner's reason in their own language. "Legal: Article 4 requires 'sufficient literacy' — must map in-scope persons, not only staff." This is the line a future head of governance reads to understand *why* the policy says what it says.
- **Resolution** is one of `accepted`, `revised` (with a pointer to the final text), `escalated` (with who it escalated to), or `declined` (with reason). A redline that nobody records as declined becomes a stale redline that resurfaces every refresh cycle.

Keep the log in the same repository as the draft. Not in a separate ticketing system. Not in a shared drive the next head of governance cannot find. In the same place, versioned alongside the policy, visible to every co-author.

## Why the log survives personnel changes and the draft does not

Heads of governance turn over every two to four years. Legal counsel rotates. CISOs leave. When the person who signed the original policy is gone, the only way the next person inherits the reasoning behind each clause is the redline log. Without the log, every refresh cycle starts from a blank page because the new partners cannot see what the previous partners cared about.

In audit conversations, the log is usually more valuable than the policy itself. Auditors want to know *how* the organization makes policy decisions, not only what the current decision is. A clean redline log answers the audit question in one artifact.

## Cadence — the walking redline

Do not try to run co-authoring as one long meeting. The hit-rate on long meetings is low; partners come under-prepared, and the meeting ends with one person agreeing to "pull it together." That person then writes a draft nobody actually redlined.

Run the co-authoring as a **walking redline** — a weekly or biweekly 30-minute slot during the drafting window, held with one or two partners at a time, with the current draft on screen and the redline log open. Each slot produces three to eight rows in the log. After four to six slots, the draft is ready for the ratification signature.

This is the cadence [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) assumes when it names draft-policy artifacts as something handed to `head-of-ai-governance` for ratification. Co-authoring is what fills the gap between "draft" and "ratified."

## Where this posture ends

Co-author is not owner. The policy's final ownership stays with `head-of-ai-governance` (L60). The legal opinion stays with counsel. The control-library architecture stays with `senior-ai-governance-architect` (L50). This role co-authors; it does not take over.

Chapter 07 treats the three handoffs — legal opinion, SOC-side incident handling, control-library architecture — that are easy to accidentally own once you have been convening the co-authoring for a few cycles. Read it after you have internalized this chapter, not before.

## Summary

- Co-authoring is a posture, not a process step: the written outcome of two sides negotiating, not one side's draft pushed to the other for approval.
- The three failure postures to rule out are hand-off, abdication, and no-artifact.
- The four co-author partners are legal counsel, risk & compliance, information security, and privacy — each brings a language you cannot fake.
- The enablement side brings three pieces nobody else sources: operator-voice reading, champion-network field signal, and training-package coupling.
- The artifact of co-authoring is the redline log — a row-per-redline running record of what changed, why, and how it resolved. The log survives personnel changes; the signed PDF does not.
- Run co-authoring as a walking redline on a weekly or biweekly cadence, not as one long meeting.
- Co-author is not owner. See [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) for the three handoffs this posture is most easily blurred into.
