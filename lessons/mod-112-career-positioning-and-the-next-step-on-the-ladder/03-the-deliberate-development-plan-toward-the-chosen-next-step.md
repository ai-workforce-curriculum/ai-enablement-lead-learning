# The Deliberate Development Plan Toward the Chosen Next Step

> The path is chosen in [Chapter 02](02-choosing-the-next-step-on-the-ladder.md). That decision does not move the lead a level on its own — eighteen to thirty-six months of specific, named preparation does. This chapter authors the preparation plan at module altitude: the signature artefacts the next-step hiring audience reads, the gaps the plan has to close, the sponsor and mentor surfaces the plan runs on, and the quarterly review that keeps the plan honest. The plan is not a goal-setting document; it is a working document the lead lives inside.

## Why "deliberate" is load-bearing in the chapter title

The common failure mode at level 45 is not that leads do not develop; it is that they develop in the surface they are already strongest at, and avoid the gaps the next step rewards closing. A lead whose strongest surface is exec writing will keep writing executive memos — well — and will arrive at an interview panel for `senior-ai-governance-architect` with no architectural decision records and no standards-mapping artefacts. The strength was still being built, just not against the target.

Deliberate practice (as the educational-psychology literature has used the term since Ericsson's foundational work) is practice *against a specific, named gap*, with feedback, at an altitude where the practitioner is not yet comfortable. The deliberate development plan this chapter authors is the role-specific adaptation of that discipline. It starts from the gap read in Chapter 02 and works backward to the practice that closes it, not forward from the strengths that are already there.

The plan is also deliberate because the preparation window is finite. Eighteen to thirty-six months sounds like a lot until the lead has one 14-hour operating week and one 6-hour writing week per fortnight to allocate against it. Deliberate practice is the discipline that puts the writing week against the architectural decision record and not against the thirteenth draft of a training-curriculum revision.

## The three outputs the plan produces

The plan is a working document; it produces three outputs for the next-step hiring audience to read, plus an instrument the lead reads for their own.

1. **The signature-artefact set.** Four to six specific artefacts the lead will have co-authored or sole-authored by the time the next-step hiring conversation lands. Chosen to close the gaps named in Chapter 02; written to an altitude the next-step audience will recognise.
2. **The credential moves.** The specific credentials from the portfolio ([mod-111 Chapter 07](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/07-the-credentials-portfolio-as-shared-vocabulary.md)) the lead will add or deepen before the hiring conversation. Not every credential; the subset that signals the chosen path, per [Chapter 04](04-positioning-the-credentials-portfolio-externally.md).
3. **The public artefact set.** The talk, the writing, the open-source enablement artefact that establishes credibility externally. Treated at length in [Chapter 05](05-the-public-artifact-set-conference-talk-writing-open-source.md); summarised here as one of the plan's outputs.

The instrument for the lead's own reading is the fourth output:

4. **The sponsor and mentor map.** The named people whose sponsorship or mentorship the plan depends on — the current sponsor who will endorse the step, the external sponsor who will hire the step, the mentor who has already made the move the lead is planning to make. Named with the current state of the relationship and the specific investment the lead is making in it.

## Reading the plan against the chosen path

The four paths from Chapter 02 drive different plans. The four below are patterns, not scripts — a lead with one of the two governance paths and a strong existing architect-partnership may hybridise, and a lead moving toward CAIO may draw on all four. But the pattern is the orientation; the hybridisation is the refinement.

### Path A plan — toward `head-of-ai-governance`

**Gap read (from Chapter 02).** Control-library authorship; direct regulator engagement; risk-acceptance decision ownership; audit-bearing conformity posture if certification is in scope.

**Signature-artefact set (4–6 artefacts).**

- **Two policy-stack ADRs** (architectural decision records) on the enablement-side policy stack — not training material; decision records at the altitude `senior-ai-governance-architect` would read as colleagues. Documented decisions with alternatives considered, trade-offs named, and the specific standards-mapping (NIST / ISO / EU AI Act article) called out.
- **One incident post-mortem co-authored with `head-of-ai-governance`** — the enablement-side contribution is the lead's, but the post-mortem is co-signed, and the control-change recommendations are the lead's authorship.
- **One standards-reading brief** — a 2-to-3-page position paper on where ISO/IEC 42001 and NIST AI RMF overlap and where they diverge, read at the AI council in a standing agenda slot. Positions the lead as a reader who can speak to both without a glossary.
- **One cross-BU conformity review** — a quarterly review the lead has run that pulled evidence from three or more BUs, mapped it against the policy stack, and produced a one-page council report with ratified actions.
- **Optionally, one regulator-touching artefact** — a response the lead co-authored to a regulator inquiry, an industry-body submission, or an Article 73 serious-incident-reporting support package where the organisation was the deployer. Only if the organisation's exposure made this a real artefact; do not manufacture.

**Credential moves.** Add or deepen: ISO/IEC 42001 Lead Implementer (with Lead Auditor if the organisation is pursuing certification); AIGP if not already held at exam level. The combination AIGP + Lead Implementer is the external signal for this path.

**Sponsor and mentor map.** Current sponsor: the exec sponsor who ratified the operating model (often the CIO or COO at level 60–70 depending on org shape). Endorsement target: the sitting `head-of-ai-governance` or the GC's AI deputy. Mentor target: a sitting head of governance one or two orgs away — met through IAPP, the governance network, or a prior partner.

### Path B plan — toward `senior-ai-governance-architect`

**Gap read.** Standards-body depth; architectural writing discipline; red-team-to-control literacy; taxonomy authorship.

**Signature-artefact set.**

- **One policy taxonomy document** — the enablement-side policy stack re-read as a taxonomy, with the control library the taxonomy plugs into named separately. Approximately 10–15 pages; the architect's equivalent of the service catalog.
- **Three to four policy-shape ADRs** — the architectural decisions the lead has made (or formally co-made) on policy shape. Each with alternatives, trade-offs, standards-mapping, and the decision date and owner.
- **One commissioning brief at architectural altitude** — a commissioning brief ([mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md)) authored or re-authored to the altitude an applied- or agentic-engineer peer consumes it as a specification. Includes the architectural constraints (data residency, model-provenance, guardrail surfaces) named as decisions, not as wishes.
- **One red-team-to-control translation artefact** — co-authored with `ai-risk-engineer` at peer level. A worked example of a red-team finding translated into a control-library modification. Positions the lead as a reader who understands the engineering side of risk, not only the enablement side.
- **Optionally, one standards-mapping document** — a mapping between the organisation's control library and one or two standards (ISO/IEC 42001 Annex A, NIST AI RMF categories). Only if the organisation does not already have this artefact; if it does, the lead's contribution is to the maintenance of it, not the authorship.

**Credential moves.** ISO/IEC 42001 Lead Auditor (not only Lead Implementer — the auditor stream signals architectural read-of-controls); deepened NIST AI RMF reading at operating depth. Consider ACM / IEEE membership for the architect-network signal if not already held.

**Sponsor and mentor map.** Current sponsor: often the `head-of-ai-governance` directly, more rarely the CIO. Endorsement target: the sitting senior architect in the role, or the deputy GC if the path is through the governance organisation. Mentor target: a sitting senior governance architect, often met at ISO technical committee participation, IEEE standards groups, or through the AIGP community.

### Path C plan — toward `chief-ai-officer`

**Gap read.** P&L ownership; M&A diligence exposure; board-level governance scaffolding beyond the enablement seat; a leadership record across engineering, product, and go-to-market.

**Signature-artefact set.**

- **Two board updates authored and signed** — not drafts; the board-update version of the exec-communication story ([Chapter 01](01-the-exec-communication-story-that-ties-the-track-together.md)) landed at the board. Signed or co-signed with the current CAIO or exec sponsor.
- **One quantified portfolio-level ROI narrative** — the full enablement program's ROI, bands and all, that the CFO has signed off on. Approximately 5–8 pages; the quarterly review's ROI deep-dive at its most defensible.
- **One cross-functional reorganisation led** — an enablement-related reorg the lead ran across at least two functions (HR, L&D, IT, Procurement, Finance, Legal). The reorg does not have to be large — the lead has to have been the named owner, not the embedded consultant.
- **One strategic memo at CAIO altitude** — a memo on an enterprise-level AI decision (a major vendor consolidation, a BU-level AI-revenue thesis, a cross-portfolio build-vs-buy call) that the CAIO or CEO acted on.
- **One executive-education signal** — completion of an executive AI strategy program (e.g., MIT Sloan, Wharton, INSEAD, HBS) or equivalent. Not a credential in the IAPP sense; a signal to the board-level audience that the lead has spent time at the altitude.

**Credential moves.** AIGP if not held at exam level (IAPP's AI governance signal at board-facing altitude); an executive-education program selection (one is enough; three is accumulation). Consider board-readiness training (NACD, IoD, or equivalent) if the step is near-term.

**Sponsor and mentor map.** Current sponsor: the sitting CAIO (or CIO / COO if no CAIO is in seat). Endorsement target: the CEO, the board chair's AI committee lead, or the search partner the CAIO uses. Mentor target: a sitting or recently-sitting CAIO one or two organisations away; executive-education cohort peers; a C-suite executive coach engaged for the final preparation year.

### Path D plan — toward `ai-engineering-manager`

**Gap read.** Engineering technical fluency beyond the brief altitude; engineering hiring and performance management; engineering-culture work.

**Signature-artefact set.**

- **One commissioning-brief-at-depth** — the deepest commissioning brief the lead has authored, extended with the architectural decisions the lead negotiated with the applied- or agentic-engineer peers. Includes the engineering-side decisions (deployment pipeline, observability posture, on-call ownership) that a brief at commissioning altitude does not usually carry.
- **One partnership-outcome record** with an `applied-ai-engineer` peer — the full lifecycle of a commissioned internal tool, from brief to acceptance to retirement, from the commissioner's perspective but including the engineering-side artefacts (code review participation, architecture review attendance, acceptance criteria).
- **One engineering-fluency artefact** — the lead has shipped code, contributed to an engineering repository, or built a production-quality open-source artefact that an engineering-manager audience will read as credible technical work. A prompt library is not sufficient; a well-engineered open-source enablement tool (automated policy-stack renderer, scorecard dashboard, intake-triage bot) is the shape.
- **One engineering-culture contribution** — a documented contribution to an engineering team's culture (on-call rotation design, incident-review template, code-review posture) that reads as an engineering-adjacent leadership move, not an enablement-side intervention.
- **Optionally, a return-to-code quarter** — some leads moving to path D spend a quarter embedded with an engineering team, shipping against a specific scope, to refresh technical fluency. This is organisation-specific and not universally available; where it is, it is a strong signal.

**Credential moves.** PMP if not held (or documented equivalent); consider a modern technical credential (AWS / Azure / GCP certifications in the AI service layer; a vendor-specific AI-infrastructure credential) if the engineering context rewards it. Avoid credential inflation; one strong technical signal is sufficient.

**Sponsor and mentor map.** Current sponsor: often the CIO or VP of Engineering under whom the applied- and agentic-engineer peers roll up. Endorsement target: the sitting director of engineering or VP of AI engineering. Mentor target: a sitting AI engineering manager, usually met through the applied-ai-engineer partner surface or through engineering-management communities (The Engineering Manager newsletter, Rands Leadership Slack, LeadDev conferences).

## The quarterly review that keeps the plan honest

The plan is a document. The discipline is the quarterly review. Once a quarter, in the week after the organisational quarterly ritual closes, the lead takes a 90-minute block and runs the review.

### The review's four questions

1. **Which signature artefacts moved forward this quarter?** Which were shipped; which had a specific milestone met; which were parked. The parked artefacts are not necessarily a problem — a parked ADR waiting on a governance-council decision is in flight, not stalled — but a parked artefact that has been parked for two quarters is a signal that the plan is no longer current.
2. **What signalled in the chosen direction?** New sponsor conversations, mentor conversations, external approaches, internal organisational shifts. Each is noted briefly; patterns across quarters are what matters.
3. **What signalled against the chosen direction?** Approaches from a different direction, surface shifts that make the current path less energising, organisational changes that close an internal path. Not every counter-signal is a path-change — but a quarter with multiple counter-signals is a quarter to re-run Chapter 02's decision instrument.
4. **What is the next-quarter commitment?** One or two specific artefacts to move forward. One or two specific conversations to have. One credential milestone if applicable. The commitment is explicit; it is what the next review reads against.

### The anti-pattern the review guards against

The anti-pattern is the plan becoming aspirational wallpaper. The lead writes the plan, signs it internally, puts it in the notes folder, and never re-reads it. Twelve months in, the plan is stale, the signals have shifted, the sponsor has rotated, and the artefact set has not moved. The quarterly review is the forcing function; losing the review is the signal the plan itself has decayed.

The review takes 90 minutes and lives in the personal notes, not in the work calendar. It is private the way the Chapter 02 decision memo is private — a work artefact that cannot be delegated to a work process.

## The role of the sponsor in the plan

Every plan runs on a sponsor. The sponsor is not the lead's manager (though they may be the same person); the sponsor is the exec who will endorse the step externally when it is time. [mod-101 Chapter 06](../mod-101-role-and-the-org-wide-enablement-operating-model/06-credentials-and-the-90-day-entry-plan.md)'s 90-day plan named the sponsor as the counterpart for the operating model's early ratification; the deliberate development plan treats the sponsor relationship as a two-year-plus investment.

Specific moves that the plan runs through the sponsor:

- **Standing exposure.** The sponsor is one of the people reading the quarterly board-update version of the exec-communication story. By quarter six, the sponsor has read enough of the lead's board-ready writing to endorse it without a prep call.
- **Standing conversation.** A monthly or quarterly one-on-one that is explicitly about the next step, not about the operating program. The sponsor needs to hear the plan over time; they will not read it in a single pitch.
- **Specific introductions.** The sponsor introduces the lead to counterparts in the lead's chosen path's organisational neighbourhood — a sitting head of governance from a peer organisation, a board member with AI exposure, a sitting CAIO one or two orgs away. These introductions are rarely spontaneous; the plan names specific asks for them.
- **The endorsement itself.** When the hiring conversation lands, the sponsor is the lead's primary external endorser. The endorsement's quality is the sum of eighteen months of standing exposure, not a single phone call.

A plan without a named sponsor is a plan that will land the lead in an external search without an inside endorser. External searches work, but they are slower and riskier. The plan that has a sponsor named by the end of the first review quarter is the plan that compounds across the preparation window.

## The relationship to the chapters around

- [Chapter 02](02-choosing-the-next-step-on-the-ladder.md) chose the path; this chapter builds against it.
- [Chapter 04](04-positioning-the-credentials-portfolio-externally.md) deepens the credential-moves output into an external signalling discipline.
- [Chapter 05](05-the-public-artifact-set-conference-talk-writing-open-source.md) deepens the public-artefact set into a specific three-artefact plan.
- [Chapter 06](06-the-decision-points-that-separate-this-role-from-adjacent-tracks.md) names the signals that would cause the plan's chosen path to shift inside the preparation window.

## Summary

- **The deliberate development plan is the chapter that turns the Chapter 02 decision into practice.** Without a plan, the chosen path is aspirational; with a plan, it is a working document the lead lives inside.
- **The plan produces three outputs for the external audience and one for the lead's own reading:** the signature-artefact set, the credential moves, the public artefact set, and the sponsor-and-mentor map.
- **Each of the four paths carries a different signature-artefact set and credential move pattern.** The patterns are the orientation; the lead hybridises based on their specific organisation and partnerships.
- **The plan runs on a quarterly review** — 90 minutes, private, after the organisational ritual closes, reading four questions against the current state. The review is the forcing function; losing it is the plan's primary failure mode.
- **Every plan runs on a named sponsor.** The sponsor's endorsement is built over standing exposure, standing conversation, and specific introductions — not a single pitch.
