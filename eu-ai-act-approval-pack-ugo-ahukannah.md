# EU AI Act Approval Pack — Ugo Ahukannah

**Client cases reviewed:** Vittal's four briefs ([`vittal-briefs-for-ugo.md`](./vittal-briefs-for-ugo.md))
**Reviewer:** Ugo Ahukannah · **Basis:** Regulation (EU) 2024/1689 as amended by Regulation (EU) 2026/1744
**Method:** classified blind — no answer key seen.

> Consulting-level assessment, not legal advice. Confirm final interpretation with counsel before launch.

---

## 1. Recognize — my four authored cases

Briefs: [`partner-brief-ugo-ahukannah.md`](./partner-brief-ugo-ahukannah.md) · Key: [`private-answer-key-ugo-ahukannah.md`](./private-answer-key-ugo-ahukannah.md)

| Case | Client | Intended category |
|---|---|---|
| 1 | MobiShare — cross-product member reliability score | Prohibited — Art 5(1)(c) |
| 2 | Nordhaven — internal promotion shortlisting | High-risk — Annex III(4) |
| 3 | Brightseed — support assistant + synthetic presenter | Limited risk — Art 50 |
| 4 | Lindqvist & Sons — SKU demand forecasting | Minimal risk |

## 2. Executive summary

Four cases, one in each tier. **One must not launch as designed** (Case 1); **one can launch but
only on controls that are not currently in the plan** (Case 2); **one needs a disclosure fix, not
a redesign** (Case 3); **one is clear** (Case 4).

The largest single exposure is **Case 1** — emotion recognition on employees is a prohibited
practice carrying the top fine band, up to €35m or 7% of worldwide turnover, and it has been in
force since 2 February 2025. No control set fixes it.

The most urgent *timing* issue is **Case 3**, and this is counter-intuitive: it is the lowest-risk
system of the three that need work, but its obligation (Article 50) has applied since **2 August
2026** and is enforceable today, whereas Case 2's Annex III high-risk obligations do not bite
until **2 December 2027** after the Digital Omnibus extension. Sequence the remediation
accordingly — Case 3 first because the clock has already run, Case 2 second because there is
runway, Case 1 immediately because it should never start.

One cross-cutting warning: Case 2's automated rejection emails are a **GDPR Article 22** problem
*today*, independent of the AI Act. Do not let the December 2027 date create a false sense of
runway on that specific feature.

## 3. Apply — first-pass classification

| Case | Likely category | Why this is my first-pass call |
|---|---|---|
| **1 — logistics burnout detection** | **Prohibited** — Art 5, emotion recognition in the workplace | Facial expression and voice tone analysis to infer worker emotional state, in the workplace, for evaluative purposes — coaching, performance conversations, promotion shortlists. That is the banned fact pattern exactly. The vendor's framing is irrelevant; so is the "one input among many" defence. Two aggravating facts: employees were told the cameras are for safety monitoring, so the deployment is covert; and the score feeds promotion, which would independently be Annex III(4) high-risk if it were not already prohibited. |
| **2 — retail CV screening** | **High-risk** — Annex III(4), employment: recruitment and selection | Scoring and ranking candidates for hiring is a listed high-risk use. Two design faults compound it: recruiters "mostly only" open the strong-fit folder and it is undecided whether anyone reads a "not a fit" before the automated rejection sends — so there may be no human in the loop at the point of detriment; and the model is trained on five years of past hiring plus one-year retention, so it learns who the company historically hired and who happened to stay, both of which encode existing bias and neither of which is a clean measure of merit. |
| **3 — electronics chat widget** | **Limited risk / transparency** — Art 50(1) | A conversational system with a human-styled name and avatar that a user could reasonably mistake for a person. It makes no binding decision — refunds still need a human click — so no Annex III area is engaged and it does not rise to high-risk. The obligation is disclosure. A "beta support tool" label in the corner does not discharge it: the duty is to inform the user they are interacting with an AI system, and the persona actively works against that inference. |
| **4 — grocery demand forecasting** | **Minimal risk** | Aggregate SKU-level forecasting from sales, weather and calendar data. No personal data, no Annex III area, no individual assessed, and store managers can accept, adjust or override every suggestion before it is submitted. No specific AI Act obligations attach. |

## 4. Integrate — architecture and role map

| Case | Architecture: trigger → behaviour → human review → output → logging/disclosure | Provider | Deployer | Vendor |
|---|---|---|---|---|
| **1** | Shift/stand-up begins → cameras and mics stream to vendor model inferring emotional state → **none before the score lands**; supervisor sees a finished weekly score → per-employee engagement score on a dashboard → scores retained and reused in performance and promotion; no disclosure to staff | Camera-software vendor (model + system placed on market under its name) | Logistics operator | Yes — the vendor is the AI Act provider; the operator cannot contract out of its own deployer duties, and here the practice is prohibited for both |
| **2** | Application submitted → model scores CV + assessment against the job description, trained on 5y hiring and retention outcomes → recruiter reviews strong-fit tier only; lower tiers may auto-reject unreviewed → strong / maybe / not-a-fit ranking + automated rejection email → needs full-ranking logs, candidate disclosure, and instructions for use | Vendor if purchased; the retailer itself if built in-house — **confirm before sign-off**, it determines who owns the technical documentation and conformity assessment | Retail chain | Likely — if bought in, require the provider's Art 13 instructions for use, Art 10 bias-testing evidence and Art 11 technical documentation as a procurement condition |
| **3** | Customer opens chat → GPAI model with retrieval over product and policy docs answers → escalates to a human on frustration or out-of-scope; refunds require a human click → conversational answer → **needs an explicit AI disclosure at the top of the conversation**, plus retention of chat logs per normal policy | GPAI model vendor is the upstream model provider; the retailer is the **downstream product provider** of the widget it ships under its own brand | Retail chain (also the product provider here) | Yes — GPAI supplier. "Powered by X" transfers no product-level obligation upward |
| **4** | Nightly/weekly planning cycle → model forecasts demand per store per SKU from sales, weather, calendar → store manager accepts, adjusts or overrides every suggestion → suggested reorder quantity to the warehouse → standard operational logging; no AI Act logging duty | Retailer if in-house; forecasting vendor if bought | Grocery chain | Only commercially — check weather/event data licence terms for downstream-use restrictions |

## 5. Verify — obligations and decision

Decision rules applied consistently: prohibited → deny and redesign · high-risk → approve only on
controls, oversight and documentation · limited risk → approve on disclosure and deployment
boundaries · minimal → approve, flagging parallel non-AI-Act issues.

| Case | Required obligations or controls | Decision |
|---|---|---|
| **1** | None available. The prohibition attaches to the practice itself, so no consent flow, disclosure, accuracy threshold or human-review layer makes it lawful. Also engages GDPR: covert biometric processing described to staff as safety monitoring. | **Deny and redesign** |
| **2** | Mandatory human review of every rejection before it sends (fixes both Art 14 and GDPR Art 22) · bias testing across demographic groups on the 5-year training set, and challenge retention-as-a-label · risk management system (Art 9) · data governance and documentation (Arts 10–11) · full-ranking logs retained ≥6 months (Art 12) · instructions for use and candidate-facing disclosure that AI is used in screening (Art 13) · registration and conformity assessment before the Annex III date. **Note: internal control self-assessment under Annex VI — Annex III(4) does not need a notified body.** **No FRIA**: a private retailer hiring for itself is not a public body, not a private entity providing a public service, and not a 5(b)/(c) deployer. | **Approve with controls** |
| **3** | Explicit "you are chatting with an AI assistant" notice at the start of every conversation, not a corner label and not implied by the persona · keep the human-escalation path · hold the boundary that no binding decision (refund, warranty outcome) is issued by the system alone — if that changes, the classification changes with it. | **Approve with controls** |
| **4** | No AI Act obligations. Parallel issues to flag: weather/event data licensing for downstream use; do not market the forecast as more than a forecast; and if the tool is ever extended to staff scheduling or productivity monitoring it moves into Annex III(4) and this assessment no longer holds. | **Approve** |

### Redesign option for the prohibited case (Case 1)

The client's actual need — catching burnout before it becomes turnover — is legitimate and
reachable without inferring emotion. Replace the biometric layer with **operational signals the
company already holds**: overtime concentration, consecutive-shift patterns, unfilled-shift rates,
absence clustering, voluntary pulse surveys, and exit-interview themes. Report at **team and site
level, not per employee**, so the output drives staffing and scheduling decisions rather than
individual performance judgements.

This lands in **minimal risk** if it stays aggregate and advisory. If the client insists on
per-employee attrition-risk flags, that is monitoring and evaluating workers under **Annex
III(4)** — high-risk, approvable only with the full control set, and requiring honest disclosure
to staff. Either path is lawful; the current design is not.

---

_Debrief (Phase 4 — intended vs inferred, client response, closing note) is held in
[`debrief-ugo-ahukannah.md`](./debrief-ugo-ahukannah.md) to keep this pack within the 3-page limit._
