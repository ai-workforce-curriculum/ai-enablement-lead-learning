# Learning from the AI Incident Database and OECD.AI

> The enablement lead's single greatest investigative advantage before an incident arrives is **prior reading of other organisations' incidents**. Two public precedent surfaces carry that reading cost at a reasonable depth: the AI Incident Database (AIID), maintained by the Responsible AI Collaborative, and the OECD.AI AI Incidents Monitor (AIM). Reading them routinely — before the incident — is how the enablement side learns incident *shapes* at the cost of other organisations' pain instead of the cost of its own. This chapter is about reading at the right altitude.

## Two external precedent surfaces

### The AI Incident Database

The AI Incident Database is a public repository of reported AI-related incidents maintained by the Responsible AI Collaborative at [incidentdatabase.ai](https://incidentdatabase.ai/). It indexes reports of harm attributed to AI systems, each incident composed of multiple source reports from news coverage, academic analysis, vendor disclosures, and researcher write-ups. Each entry has:

- A canonical incident identifier.
- A short description of the harm.
- A set of source-reports (the primary news or disclosure items).
- Tags for the AI system type, the deployer, the alleged harm, and the affected population.
- Timeline and geography.

The database's taxonomy evolves; the version at the time of reading matters. The database is not an adjudication — entries are reported incidents, and some are contested, retracted, or refined over time. The enablement lead reads it as an evidence-of-reporting surface, not as a liability register.

### The OECD.AI AI Incidents Monitor

The OECD.AI Policy Observatory maintains the AI Incidents Monitor at [oecd.ai](https://oecd.ai/en/incidents). The AIM is a tracker drawn from news-source monitoring; it emphasises incidents in OECD jurisdictions and tags against the OECD AI principles and the AI Act risk framing (for EU-touching reports). Entries carry:

- Incident date.
- Country and sector.
- A short description.
- Links to the underlying news reports.
- Tags for incident type and affected population.

The two databases overlap significantly but not completely. AIID is deeper on the US-centric tech-industry incidents and has longer-tail academic coverage; AIM is better at surfacing European and public-sector incidents and is tagged against policy-maker vocabulary. Reading both periodically is the cheapest way to see both surfaces; either alone is insufficient.

### A reading-cadence proposal

The enablement lead reads AIID and AIM on a cadence, not on an "as needed" basis:

- **Monthly scan.** Twenty minutes. Walk the new incidents in the last month in both databases. Flag any that overlap with the organisation's deployed tools, deployed vendors, deployed use cases, or regulatory exposure.
- **Quarterly deep-read.** Two hours. Pull two or three incidents of direct relevance into the governance-council read-aheads from [mod-103 Chapter 02](../mod-103-policy-co-authoring-with-governance/02-the-governance-council-liaison-seat.md). The read-aheads are where the enablement side teaches the council in slow time.
- **On-vendor-change.** When the organisation adds or removes a vendor from the approved envelope, scan both databases for incidents attributed to that vendor or that vendor's underlying model family.
- **On-incident.** During an active incident, the ai-risk-engineer may ask the enablement lead to pull precedent from the databases. This is a supporting-mode task; the finding goes to the ai-risk-engineer, not to the organisation's narrative.

<!-- needs-research: AIID and OECD.AI AIM are both evolving public surfaces; the exact feature set and URL structure may shift. Verify the cadence proposal against the live surfaces on each refresh cycle. -->

## Reading at the right altitude

The enablement lead does not read these databases for forensic detail. The databases are typically not deep enough for engineered root-cause analysis — they are reported-harm surfaces. The ai-risk-engineer (L25) reads them for a different purpose.

The enablement lead reads them for four specific things.

### 1. The incident's enablement-side shape

Who filed the report? Was the first-signal source a champion-equivalent inside the organisation, a user, a journalist, a regulator, a researcher? What was the latency from first-signal to escalation? Was there a kill-switch pull — publicly visible or not — and how long did it take? These are *enablement-side* features, and they are exactly what the enablement lead needs to drill the four signal sources from [Chapter 01](01-the-enablement-side-of-the-incident-path.md) against.

Many AIID entries do not spell these out explicitly. The enablement lead reads the source reports and reconstructs the enablement-side shape from them. The reconstruction is imperfect and should be flagged as such. It is still better than reading the incident at the level of "a chatbot said a bad thing."

### 2. The policy-coupling weakness

Did the deploying organisation have a policy that the incident exposed as insufficient? Did the policy exist but not reach the operator? Did the operator know the policy and act outside it anyway? Was there a tool in use that was not in the organisation's approved envelope ("shadow use")?

Each of these failure modes is a specific weakness in the artefact set from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md). Reading enough incidents against the artefact set produces a sense of *which artefacts fail most often* for the shape of deployment the enablement lead is running. That sense is what keeps the artefact set calibrated against evidence rather than against the organisation's internal intuition.

### 3. The communication posture

How did the deploying organisation communicate about the incident — to users, to the public, to regulators? Was there a kill-switch pull that was communicated clearly, a vendor-side disclosure, a silence that became a bigger story than the incident itself? What did the external party (customer, regulator, press) say about the organisation's communication posture?

The enablement lead does not communicate externally during an incident ([Chapter 01](01-the-enablement-side-of-the-incident-path.md) posture 3). The enablement lead *is* responsible for internal communications — champion network, help channel, exec informational — and for not pre-empting the external communications the governance side owns. The databases are a reading of what internal and external communications look like when they go wrong, which is almost always worth the twenty minutes a month.

### 4. The regulator-visibility of the incident class

Did a regulator respond publicly to the incident? Did a regulator open an inquiry? Was an Article 73-equivalent reporting obligation (in the EU) or a state-attorney-general notification (in the US) triggered? The enablement lead does not run those obligations — but the enablement lead is responsible for *preserving the evidence* the obligation requires, and for not accidentally triggering or waiving an obligation through a premature response (Chapter 07).

Reading what regulators actually do in incidents of the class the organisation is deploying is the calibration surface for "how fast does the enablement side need to preserve evidence, pull the tool, and notify governance so the organisation's clock does not slip?" That calibration is not available in internal policy; it is available in the public record of other organisations' incidents.

## The "shadow use" sub-pattern

One specific sub-pattern that recurs across both databases is worth naming explicitly: an incident involving an AI tool that was not in the deploying organisation's approved envelope — an operator using a consumer tool for work, pasting organisational data into it, often against policy, sometimes without a policy that named the specific tool. The incident surfaces because of harm, and the organisation's position becomes the uncomfortable one of answering for a tool it did not approve.

The AI Incident Database and the OECD.AI AIM both include entries that read this way. The enablement-side lesson is not "ban all consumer tools" — a policy stance that typically fails on contact with the "I already have ChatGPT at home" resistance pattern from [mod-105 Chapter 06](../mod-105-champion-networks-and-change-management/06-ai-specific-resistance-patterns-adkar-and-kotter.md). The enablement-side lesson is that:

- The one-page AUP from [mod-103 Chapter 04](../mod-103-policy-co-authoring-with-governance/04-the-one-page-acceptable-use-policy.md) has to name the shadow-use case specifically, not just the approved-use case.
- The approved envelope has to be close enough to the operators' actual needs that shadow use is rarely the easier path.
- The champion network is the fastest surface for detecting shadow use and bringing it back into the approved envelope or getting the approved envelope revised.

A shadow-use incident is an enablement-system failure, not only an operator failure. Reading precedent is how the enablement lead calibrates the rate at which the organisation's own program is drifting into shadow use.

## What the databases are not

Two important limits on the precedent surface.

- **Not an engineering surface.** For model-level root cause — specific prompt injection techniques, specific jailbreak patterns, specific evaluation protocols — the enablement lead points the ai-risk-engineer (L25) at MITRE ATLAS, the OWASP Top 10 for LLM Applications, and the vendor's own incident disclosures. The two databases are the harm surface, not the attack surface. See `resources.md` for references.
- **Not comprehensive.** Both databases are built on reported incidents; unreported incidents are invisible. Many organisations do not disclose incidents publicly; many are disclosed through channels the databases do not index. The enablement lead reads the databases for a sample, not a census. A low count for an incident class in the databases does not mean the class is rare — it means it is not well-reported.

## Bringing precedent into the governance-council read-ahead

One of the most valuable uses of the database reading is to teach the governance council in slow time, before an incident. The read-ahead from [mod-103 Chapter 02](../mod-103-policy-co-authoring-with-governance/02-the-governance-council-liaison-seat.md) has a slot for "field signal"; incidents from AIID or AIM of direct relevance belong in that slot on a quarterly cadence.

Shape of the read-ahead paragraph:

- **One or two sentences on the incident's harm shape.** From AIID or AIM.
- **One sentence on the parallel in the organisation's own deployment.** "This shape could occur in our Tool X rollout if operator Y uses it for use case Z."
- **One sentence on the artefact-set gap the parallel exposes.** "Our data-handling SOP does not name this use case explicitly; the walking-redline backlog has a candidate amendment."
- **One sentence on the specific mitigating change.** "The amendment is co-authored by `head-of-ai-governance` and this role; target is next council cycle."

That shape makes the council the primary audience for the precedent reading and makes the enablement lead the primary carrier of external precedent into internal policy. Both are correct role moves and both scale.

## Summary

- Two external precedent surfaces carry most of the enablement-side reading cost at reasonable depth: the AI Incident Database (AIID) at the Responsible AI Collaborative, and the OECD.AI AI Incidents Monitor. Read both; neither is a complete surface alone.
- Read on a cadence — monthly scan, quarterly deep-read, on-vendor-change, on-incident — not "as needed."
- Read at the enablement altitude, not the engineering altitude. Four specific lenses: enablement-side shape, policy-coupling weakness, communication posture, regulator-visibility of the class.
- The "shadow use" sub-pattern is a recurring class; the lesson is that the AUP must name it, the approved envelope must be close enough to real needs that shadow use is rarely easier, and the champion network is the fastest detection surface.
- The databases are not an engineering surface (point the ai-risk-engineer at MITRE ATLAS and OWASP LLM Top 10) and are not comprehensive (reported incidents only).
- The highest-value use of the reading is feeding the governance-council read-ahead quarterly, so the council learns precedent in slow time instead of under incident pressure.
