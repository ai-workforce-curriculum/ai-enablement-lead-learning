# Quiz 01 — The Six-Family Cost Model, Projected ROI, the Four-Column Build-vs-Buy Matrix, the Three-Way Partnership, Stack Consolidation, and the Vendor-Vetting Rubric

**Format:** multiple choice · **Questions:** 12 · **Estimated effort:** 25–30 minutes
**Grounding:** [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md), [Chapter 02](../02-projecting-roi-with-confidence-bands.md), [Chapter 03](../03-the-build-vs-buy-matrix-at-enterprise-scope.md), [Chapter 04](../04-partnering-with-procurement-finance-and-it.md), [Chapter 05](../05-reconciling-the-tool-stack-across-bus.md), [Chapter 06](../06-the-vendor-vetting-rubric.md)

## How to take this quiz

Pick the single best answer for each question. Each question presents a concrete situation and asks you to *apply* a chapter idea to it — paraphrasing the chapter is not enough. Answer key with short explanations is at the bottom; resist the urge to read it until you have your own answers written down.

---

### Q1. An enablement lead takes last year's cost-model draft into the first Finance working session. The model reports $1.8M of annual spend: $1.6M in tool-license invoices and $200K in the CoE lead's and two program managers' salaries. The CFO's finance partner opens the review with "where is the rest?" Under Chapter 01's six-family taxonomy, the single largest line the model is most likely missing is:

- **A.** Family 3 — Training production and delivery, because curriculum development labor is often absorbed into L&D.
- **B.** Family 5 — Champion-network operating cost, because recognition and rewards accumulate at enterprise scale.
- **C.** Family 4 — Embedded enablement partner FTE. Chapter 01's worked example has Family 4 as the top line at enterprise scale with a champion network (BU-embedded partners, 100+ champions at ~12% of fully-loaded time, shadow enablement, governance partner time); it is also named as "the single most common gap in published enablement cost models."
- **D.** Family 6 — Downstream support, because incident-response cost dominates at mature programs.

### Q2. A BU lead argues that the full annual Microsoft 365 license spend (which pre-dates any AI program) should sit in the AI denominator because "we only pay for M365 Copilot because we already have M365." Under Chapter 01's five named undercounts and the AI-incremental cost rule, the grounded response is:

- **A.** Agree; the base M365 licenses enable Copilot and so belong in the denominator.
- **B.** Disagree. The AI-incremental cost rule is explicit: pre-existing spend on Microsoft 365 or Google Workspace that existed before AI add-ons was not AI-program cost; only the incremental AI license (the Copilot add-on per-user charge) belongs in the AI denominator. The rule is published in the methodology appendix with a worked example so this conversation does not re-open each quarter.
- **C.** Agree; Finance will resolve the boundary during monthly invoice reconciliation.
- **D.** Disagree, but fold the full M365 spend into the "other / small lines" materiality bucket to keep the conversation moving.

### Q3. An enablement lead's three-year ROI projection for a drafting-copilot rollout shows a steady-state value starting in month two at near-full magnitude, a three-year central ROI of 3.4x, and a per-year ROI in year three nearly identical to the per-year ROI in year one. No ramp region is visible on the J-curve. Under Chapter 02's three projection-specific theatre patterns, this projection is specifically:

- **A.** A legitimate aggressive-adoption scenario; the vendor's benchmark data supports a fast ramp.
- **B.** The walking-band pattern — the summary slide narrower than the methodology appendix.
- **C.** The attribution-by-assertion pattern — the attribution fraction has no evidence source.
- **D.** The hockey-stick projection — no ramp, no crossover, no plateau, steady-state magnitude starting in month one or two, with the one-year and three-year per-year ROI almost identical. The tell matches exactly; the remediation is to model the J-curve honestly (ramp, crossover, steady state, plateau) and allow the ramp to be negative for the first several months.

### Q4. The quarterly ROI slide carries the line "Projected 3-year ROI: 2.1x." A board member asks for the uncertainty. The enablement lead's Finance partner is the organization's authority on uncertainty-reporting conventions. Under Chapter 02's refusing-the-point-estimate discipline, the strongest response is:

- **A.** "The point estimate is 2.1x. The 90% band is 1.4x–2.9x. The band is wide because the attribution fraction and the ramp length carry the largest uncertainty; a cohort-comparison update at the end of the first operating quarter will narrow the band."
- **B.** "The ROI is 2.1x and we're confident in that estimate; the Finance team asked us to keep bands off the summary for readability."
- **C.** "The ROI is between 2.0x and 2.2x — a tight planning range the leadership team can act on."
- **D.** "We'll update the number when more adoption data comes in; for now, 2.1x is the best estimate."

### Q5. A Column 4 (internal build) case for a RAG-grounded internal knowledge assistant reports a three-year TCO of $1.2M — $900K build cost in year one, $100K/year ongoing maintenance over years two and three. The reported TCO is lower than every vendor candidate in Columns 1 and 2. Under Chapter 03's three failure modes, the most likely pattern is:

- **A.** Vendor capture — one vendor conversation dominated the writeup.
- **B.** Capability-only scoring — non-capability dimensions carry less than 40% of weight.
- **C.** Build hubris — the maintenance commitment is undercounted. Chapter 03 names typical ongoing maintenance for a non-trivial internal build as 1-3 FTE on an ongoing basis for the life of the tool; $100K/year is a fraction of a single FTE. A build case that forgets ongoing maintenance has typically understated TCO by 40-70% across the three-year horizon. The remediation is a peer review with an engineering lead who will inherit the maintenance.
- **D.** Pilot sprawl — multiple competing pilots inside one BU.

### Q6. The organization is choosing between a general-purpose knowledge-work copilot (Column 1), the Microsoft Copilot add-on across M365 (Column 2), and an industry-specific tool (Column 3) for the specific task "generate first-pass meeting summaries in Teams for standing operational meetings." The organization already runs M365, has an active DPA with Microsoft, and the task is a commodity knowledge-work use case with no regulated-data exposure. Under Chapter 03's reusable column-wins patterns, the most likely winner is:

- **A.** Column 1 — frontier capability and cross-tool reach matter most for this workflow.
- **B.** Column 2 — commodity workflow value inside an existing SaaS surface. The add-on is already integrated, the data is already under the existing DPA, no new vendor relationship is required, and Column 1 and Column 3 are unlikely to differentiate on this task. (The decision can still flip if, for example, the Column 2 add-on fails the Stage 2 POC on capability-fit — but the column pattern predicts Column 2.)
- **C.** Column 3 — domain-specific accuracy and workflow fit dominate.
- **D.** Column 4 — the data-boundary constraints no vendor can meet point to internal build.

### Q7. Procurement has flagged two vendor responses in the current RFP: Vendor A holds SOC 2 Type I, dated 90 days ago; Vendor B holds SOC 2 Type II, with an operating-effectiveness period ending 60 days ago. Both claim "SOC 2 certified." Under Chapter 04's contract-term vocabulary, how should the enablement lead read the difference in the Stage 2 writeup?

- **A.** They are equivalent — both are current and both are SOC 2.
- **B.** Vendor A is stronger because the Type I attestation is more recent.
- **C.** SOC 2 Type I is a design-only attestation (controls were designed as of a point in time); SOC 2 Type II adds operating-effectiveness evidence across a period. Type II is the enterprise bar; Type I is not. The writeup should flag Vendor A as not meeting the SOC 2 Type II baseline and let Procurement and Security carry the lens from there — the enablement lead's job is to read the attestations correctly, not to make the compliance decision.
- **D.** Neither — only ISO 27001 is enterprise-grade for AI vendors.

### Q8. At the three-way partnership working session, the IT director proposes that the enablement lead co-own the organization's SSO architecture decisions "because AI rollouts touch identity most often." Under Chapter 04's out-of-scope lines, the grounded response is:

- **A.** Accept; the role's authority on AI tools extends to the identity surface they integrate with.
- **B.** Decline. SSO architecture, identity-store configuration, DLP policy configuration, and admin-surface integration standards are explicitly IT operational decisions — the enablement lead carries the use case's requirements to the conversation and lets IT decide the implementation. Accepting co-ownership here produces artifacts IT will not sign and dilutes the role's credibility on the surfaces it does own.
- **C.** Accept, with the caveat that Finance co-signs each decision.
- **D.** Decline, but propose that enablement own SCIM provisioning while IT retains SSO architecture.

### Q9. The annual stack inventory shows BU-A and BU-D both running Microsoft Copilot across M365 through separate purchasing arrangements (two contracts, same vendor, same tool, no shared enterprise agreement). Under Chapter 05's four overlap patterns and their matched remediations, this is:

- **A.** Pattern 1 (platform add-on duplicates a standalone tool) — run a bounded capability comparison and let TCO decide.
- **B.** Pattern 2 (same vendor across BUs with no shared contract). The remediation is Procurement-driven consolidation at the renewal-plus-90 interface from Chapter 04. Consolidation to a single enterprise agreement is typically a 10-25% price improvement and does *not* require any tool change at the BU level — the operators keep the same tool; the paper consolidates.
- **C.** Pattern 3 (overlapping tools in the same category across BUs) — run the build-vs-buy matrix with switching cost weighted.
- **D.** Pattern 4 (pilot sprawl inside a single BU) — close the Stage 3 decision from mod-102.

### Q10. A consolidation memo lands on the executive sponsor's desk. The BLUF reports "$1.8M annual savings over two years from retiring Chorus and standardizing on Gong across all sales BUs." The memo does not mention that BU-B operators have reported higher workflow fit on Chorus for their specific call-intelligence pattern, or that the Chorus-trained champion network has been building domain expertise for 14 months. Under Chapter 05's five surfacing principles and three failure patterns, the memo most clearly fails on:

- **A.** The vendor-driven consolidation pattern — a vendor pushed the memo through.
- **B.** The consolidation-that-never-ships pattern — the memo is not tied to a renewal date.
- **C.** The clear-the-decks reconciliation pattern plus two surfacing-principle failures — the savings headline is foregrounded, the local-optimum sacrifice (BU-B's workflow-fit advantage) is absent, and the champion-carry language (re-skilling the Chorus champions on Gong) is missing. Remediation: force switching cost onto the first page, name the local-optimum sacrifice explicitly, and write the champion-carry plan before resubmitting.
- **D.** The build-hubris pattern — the memo compares a buy to a buy, not to an internal build.

### Q11. A pre-pilot vendor-vetting rubric was completed for Vendor X 14 months ago at pilot-commit. The pilot converted to a running rollout; the vendor has since been acquired by a larger platform company and has shifted its model sub-processor from one hyperscaler to another. The rubric has not been refreshed. Under Chapter 06's four triggers and three failure modes, the issue is specifically:

- **A.** The stale-score failure mode on its own — the rubric date is more than 12 months old on a live vendor.
- **B.** The polished-pitch illusion — pitch-era scores do not match production reality.
- **C.** The security-only review — only Dimensions 2 and 3 were ever scored.
- **D.** Both the stale-score failure mode (date > 12 months on a live vendor, caught by the annual portfolio sweep) *and* two unaddressed signal-event triggers (vendor acquisition, major sub-processor shift) that should have prompted a rubric re-run inside the signal-event trigger — not waited on to renewal. The remediation is to refresh the rubric now, re-score Dimensions 2 (model provenance / sub-processor chain) and 4 (commercial resilience / acquisition exposure) against the new facts, and log the signal-event as a precedent for the next one.

### Q12. The vendor portfolio shows twelve live vendors: one vendor at 68% of total AI spend (a hyperscaler platform add-on), two vendors each at ~6%, and nine small vendors each under 3%. Four of the nine small vendors are single-sourced tools in regulated-workflow categories (no viable alternatives in market). Under Chapter 06's portfolio-level concentration view, the honest read of the portfolio is:

- **A.** Clean — twelve vendors with appropriate diversification.
- **B.** Concentration-risk at the top (one vendor at 68% is a single point of failure for most of the program); concentration-risk at the long tail (four of twelve tools single-sourced, exceeding the 20%-of-tools rough bar Chapter 06 names). Both are acceptable *with explicit acknowledgment*; the role's job is to put the concentration view on the dashboard quarterly so drift does not surprise anyone and to carry the single-sourcing lines through to the next vendor-vetting and renewal cycles. Concentration is not an optimization target, but it is a line that must be visible.
- **C.** Diffuse — twelve vendors is too many to manage; the concentration risk is operational-complexity on the long tail.
- **D.** Only the top line matters; the four single-sourced tools are Procurement's lens, not enablement's.

---

## Answer key

**Q1 — C.** Chapter 01's worked example shows Family 4 at the top of the model at enterprise scale ($3.01M in the sketch, ~29% of the $10.5M total) and the chapter names it directly as "the single most common gap in published enablement cost models." The model in the vignette carries Family 1 and part of Family 2 and omits Families 3–6; Family 4 is the single largest line missing. Families 3, 5, and 6 are also missing but smaller. (Chapter 01 — *Family 4 — Embedded enablement partner FTE* and *A worked example — a cost model, sketched*.)

**Q2 — B.** Chapter 01 names the AI-incremental cost rule as the fifth of the five undercounts: "Microsoft 365 and Google Workspace seats existed before the AI add-ons; only the incremental AI license belongs in the AI denominator. Separate the AI-incremental cost from the pre-existing baseline explicitly in the methodology note." The rule is published in the methodology appendix with a worked example precisely so the conversation does not re-open. Folding the full M365 spend into the materiality bucket would understate the incremental and overstate the baseline both. (Chapter 01 — *Common undercounts* and Exercise 01's methodology-appendix requirements.)

**Q3 — D.** Chapter 02's hockey-stick pattern is exactly this: "Steady-state value starts in month one and compounds. No ramp, no crossover, no plateau. Reverse-engineered from the target ROI number. Tell: a one-year ROI that is nearly identical to the three-year ROI on a per-year basis." The vignette matches the tell exactly. The walking band is a summary/appendix mismatch (different pattern); attribution by assertion is about the attribution fraction lacking a source (different pattern). The remediation is to model the J-curve honestly — ramp cost is negative for the first several months. (Chapter 02 — *Theatre to watch for in projected ROI → The hockey-stick projection* and *Modelling the J-curve*.)

**Q4 — A.** Chapter 02 writes the canonical three-sentence form of the honest projection: "The point estimate is 2.1x. The 90% band is 1.4x–2.9x. The band is wide because the attribution fraction and the ramp length carry the largest uncertainty; a cohort-comparison update at the end of the first operating quarter will narrow the band." Option A is this verbatim. B is the "the CFO's finance team said no bands" pattern the chapter names and rejects (the enablement lead's Finance partner is where the standard is resolved). C is a point estimate wearing a narrow band for cover. D defers rather than reporting the uncertainty. (Chapter 02 — *Refusing the point estimate — what to say instead*.)

**Q5 — C.** Chapter 03's build-hubris pattern is "the writeup concludes 'we should build' because the team wants to build … Tell: the year-three internal-build TCO is lower than any vendor's, on the assumption that maintenance is a small line." The Column 4 TCO shape in Chapter 03 names typical ongoing operating cost as "1-3 full-time engineering seats on an ongoing basis … this cost persists for the life of the tool. The build case that forgets ongoing maintenance has typically understated TCO by 40-70% across the three-year horizon." $100K/year is a fraction of one FTE for a RAG-grounded assistant; the pattern matches. Remediation: peer review with the engineering lead who will inherit maintenance. (Chapter 03 — *TCO shape for Column 4 (internal build)* and *Failure modes → Build hubris*.)

**Q6 — B.** Chapter 03's "when each column wins" names Column 2 directly: "Column 2 wins on commodity workflow value inside an existing SaaS surface. Meeting summaries in Teams or Zoom, document drafting inside M365 or Workspace, standard-feature use cases. The platform add-on is already integrated, already covered by a DPA, and does not require a new vendor relationship." The vignette matches the pattern exactly. Column 1 wins on frontier capability and cross-tool reach (not needed here); Column 3 wins on domain-specific accuracy (no regulated data); Column 4 is reserved for data-boundary, differentiated workflow, or forced build (none of these). (Chapter 03 — *When each column wins*.)

**Q7 — C.** Chapter 04 is explicit: "SOC 2 Type I is *not* SOC 2 Type II — Type I is design-only; Type II includes operating-effectiveness evidence over a period. Learn to tell them apart on the vendor's trust page in ten seconds." The enablement lead's job is to read the attestations correctly in the Stage 2 writeup; Procurement and Security carry the compliance-decision lens. Flagging Vendor A's Type I as not meeting the Type II baseline is the right read; treating them as equivalent, or ranking A higher because its attestation is more recent, misreads the attestation structure. (Chapter 04 — *Security attestations*.)

**Q8 — B.** Chapter 04's out-of-scope section is explicit about the three lines the enablement lead does not own: "Contract execution … Final budget authority … IT operational decisions. SSO architecture, identity-store configuration, DLP policy configuration, admin-surface integration standards — these are IT's calls. The enablement lead carries the use case's requirements to the conversation and lets IT decide the implementation." Accepting co-ownership on SSO architecture produces artifacts IT will not sign and dilutes the role's credibility; proposing SCIM-but-not-SSO is still inside IT's operational surface. The grounded move is to decline cleanly and remain inside the use-case / requirements lane. (Chapter 04 — *What is out of scope for the enablement lead*.)

**Q9 — B.** Chapter 05's Pattern 2 is this exact shape: "Same vendor, different BUs, no shared contract. The organization is paying retail across two contracts instead of an enterprise agreement." The remediation is also explicit: "Procurement-driven consolidation. The Procurement renewal-plus-90 interface is the lever; consolidation to a single enterprise agreement is typically a 10-25% price improvement and does not require any tool change at the BU level." This is the easy consolidation pattern — the paper consolidates, operators keep the tool, no switching cost, no local-optimum sacrifice. Pattern 1 is about add-on vs standalone (different vendors); Pattern 3 is overlapping tools in the same category (different vendors); Pattern 4 is a Stage 3 close inside one BU. (Chapter 05 — *Reading the inventory — four overlap patterns → Pattern 2*.)

**Q10 — C.** Chapter 05's clear-the-decks reconciliation pattern is "the case is framed around savings headline, with switching cost in a footnote" — the vignette matches. The vignette also fails two of the five surfacing principles directly: (2) carry the local-optimum sacrifice on the writeup — BU-B's workflow-fit advantage on Chorus is absent; (4) protect the champion network across the transition — the 14-month Chorus-trained champion network has no re-skilling plan. The vendor-driven pattern is different (vendor-led, not consolidation-led); the never-ships pattern is about deferral; build hubris is about internal builds. Remediation names three specific moves: switching cost on page one, local-optimum sacrifice named, champion-carry plan written. (Chapter 05 — *Surfacing consolidation without stripping teams → The surfacing move* and *The failure patterns → The clear-the-decks reconciliation*.)

**Q11 — D.** Chapter 06 names two of the four triggers that apply here. The stale-score failure mode fires on its own ("a rubric date more than 12 months old on a live vendor" — 14 months exceeds the 12-month bar; remediated via the annual portfolio sweep). *Separately*, two signal events — vendor acquisition and major sub-processor shift — are named in the signal-event trigger ("a material event — vendor acquisition, pricing model change, public incident, major sub-processor shift, significant capability release or regression. The rubric is re-run at the material event, not waited on to renewal"). Both apply; naming only the stale-score failure misses the signal-event triggers. The remediation re-scores Dimension 2 (model provenance / sub-processor chain) and Dimension 4 (commercial resilience / acquisition exposure) against the new facts. (Chapter 06 — *When to run the rubric → Signal event* and *Failure modes → The stale score*.)

**Q12 — B.** Chapter 06's portfolio concentration view asks three questions quarterly: vendor count, spend concentration on the top one/three/five, single-sourced-tool fraction. The vignette shows concentration at the top (68% on one vendor is a clear top-one concentration — Chapter 06 names "80% of spend on one vendor is concentration risk"; 68% is in the same family) *and* at the tail (four of twelve single-sourced is 33%, exceeding Chapter 06's 20%-of-spend rough bar on single-sourced tools). The chapter's framing is explicit: "The concentration view is not an optimization target; it is a dashboard the role reads so concentration drift does not surprise anyone." The right read is to carry both concentrations as named lines and route them into the next renewal and vetting cycles — not to treat the portfolio as clean, not to describe the long tail as merely operational complexity, and not to hand concentration off to Procurement alone. (Chapter 06 — *Vendor concentration — the composite view*.)
