# EU AI Act Approval Pack - Ugo Ahukannah

**Lab:** Classify your product · **Partner:** Vittal Navale · **Basis:** Regulation (EU) 2024/1689 as
amended by Regulation (EU) 2026/1744

> Consulting-level assessment, not legal advice. Confirm final interpretation with counsel before launch.

This document has the two parts the lab setup requires — **Private answer key** and **Consulting
response** — followed by my consulting review of my partner's four cases. The debrief is held
separately in [`debrief-ugo-ahukannah.md`](./debrief-ugo-ahukannah.md) to keep this pack within the
3-page limit for the review itself.

---

## Part 1 - Private answer key

Not shared with my partner until after both blind reviews were exchanged. Each case below is
written to land in one specific tier, with the intended category and the reason for it.

### Case 1 - Prohibited

**Client:** MobiShare (urban mobility)

MobiShare runs car and e-scooter sharing in six European cities. They lose money on a small
group of users who damage vehicles, park badly and dispute charges, but they cannot tell who
those users are until after the damage. They want a "member reliability score" built from ride
telemetry, cancellation history, app behaviour, payment disputes, how quickly people respond to
support messages, and public review sentiment. The score would sit in the customer profile and
follow the member across all MobiShare products — so a low score would also mean rejection from
their new insurance partner offer and their apartment-block parking subscription, neither of
which is about driving. Support staff can see the score but the gating is automatic.

**Intended category:** **Prohibited** — Art 5(1)(c) social scoring

**Why I chose it:** A general-purpose reliability score built from behavioural signals, used to deny access in **unrelated contexts** (insurance offer, parking subscription) — the detriment is disconnected from the behaviour that produced the score, and disproportionate. Deliberately built by a **private** company: the prohibition is not limited to public authorities, which is the most common and most expensive misreading.

### Case 2 - High-risk

**Client:** Nordhaven Group (facilities management, 4,000 staff)

Nordhaven promotes supervisors to regional team leads once a year, and HR says the process is
inconsistent between regions. They want a system that shortlists internal candidates for
promotion by learning from the last eight years of promotion decisions and subsequent
performance reviews. Inputs are tenure, shift-attendance records, completed training modules,
customer-complaint counts attached to each supervisor's team, and free-text manager comments.
The system outputs a ranked shortlist per region, and HR business partners say they will "sanity
check" the top ten before the panel sees it, though the panel only ever receives the ranked list.

**Intended category:** **High-risk** — Annex III point 4, employment and workers management

**Why I chose it:** AI ranking internal candidates for promotion is a consequential decision about people in an Annex III protected area. Trained on eight years of past promotion decisions, so it inherits historical bias (Art 10 problem). The "sanity check" is cosmetic — the panel only ever sees the ranked list, so oversight is not effective under Art 14.

### Case 3 - Limited risk / transparency

**Client:** Brightseed Nutrition (D2C supplements)

Brightseed wants to cut support costs and refresh their marketing at the same time. Two pieces:
a customer-facing assistant on their website that answers product questions, order status and
returns in a warm conversational style with a first name and a photo; and a set of short
promotional videos featuring a synthetic presenter with a cloned voice, so they can localise
campaigns into nine languages without reshooting. The assistant escalates anything about health
conditions to a human. Nobody is refused anything by either system — worst case a customer gets
a wrong answer about shipping times.

**Intended category:** **Limited risk / transparency** — Art 50

**Why I chose it:** Two Art 50 triggers in one brief: a conversational assistant with a human name and photo (users must be told they are talking to an AI, and the persona actively obscures it), and a synthetic presenter with a cloned voice (AI-generated content must be labelled). Nobody is refused anything, so no Annex III area is engaged — the duty is disclosure, not conformity assessment.

### Case 4 - Minimal risk

**Client:** Lindqvist & Sons (regional grocery wholesaler)

Lindqvist supplies 140 independent grocers and is carrying too much stock on slow lines while
running out of fast ones. They want demand forecasting per SKU per depot, learning from three
years of order history, seasonality, local event calendars and weather data, to generate
suggested replenishment quantities. The purchasing team reviews the suggestions in a weekly
planning session and can change any number before orders go out. No customer or employee data is
involved, and no individual is assessed or affected by the output — the affected parties are
purchasing staff deciding how many pallets to order.

**Intended category:** **Minimal risk**

**Why I chose it:** AI is genuinely involved, but the output is a stock quantity, not an assessment of a person. No Annex III area, no personal data, meaningful human review before anything happens. No specific AI Act obligations — though GDPR, consumer protection and supplier-contract terms still apply, and the client should not market this as more than forecasting.

---

## Part 2 - Consulting response

The same four cases as they were sent to my partner, with every category label removed — this is
the version shared for blind review, also held standalone in
[`partner-brief-ugo-ahukannah.md`](./partner-brief-ugo-ahukannah.md) for the swap.

### Case 1 — MobiShare (urban mobility)

MobiShare runs car and e-scooter sharing in six European cities. They lose money on a small
group of users who damage vehicles, park badly and dispute charges, but they cannot tell who
those users are until after the damage. They want a "member reliability score" built from ride
telemetry, cancellation history, app behaviour, payment disputes, how quickly people respond to
support messages, and public review sentiment. The score would sit in the customer profile and
follow the member across all MobiShare products — so a low score would also mean rejection from
their new insurance partner offer and their apartment-block parking subscription, neither of
which is about driving. Support staff can see the score but the gating is automatic.

### Case 2 — Nordhaven Group (facilities management, 4,000 staff)

Nordhaven promotes supervisors to regional team leads once a year, and HR says the process is
inconsistent between regions. They want a system that shortlists internal candidates for
promotion by learning from the last eight years of promotion decisions and subsequent
performance reviews. Inputs are tenure, shift-attendance records, completed training modules,
customer-complaint counts attached to each supervisor's team, and free-text manager comments.
The system outputs a ranked shortlist per region, and HR business partners say they will "sanity
check" the top ten before the panel sees it, though the panel only ever receives the ranked list.

### Case 3 — Brightseed Nutrition (D2C supplements)

Brightseed wants to cut support costs and refresh their marketing at the same time. Two pieces:
a customer-facing assistant on their website that answers product questions, order status and
returns in a warm conversational style with a first name and a photo; and a set of short
promotional videos featuring a synthetic presenter with a cloned voice, so they can localise
campaigns into nine languages without reshooting. The assistant escalates anything about health
conditions to a human. Nobody is refused anything by either system — worst case a customer gets
a wrong answer about shipping times.

### Case 4 — Lindqvist & Sons (regional grocery wholesaler)

Lindqvist supplies 140 independent grocers and is carrying too much stock on slow lines while
running out of fast ones. They want demand forecasting per SKU per depot, learning from three
years of order history, seasonality, local event calendars and weather data, to generate
suggested replenishment quantities. The purchasing team reviews the suggestions in a weekly
planning session and can change any number before orders go out. No customer or employee data is
involved, and no individual is assessed or affected by the output — the affected parties are
purchasing staff deciding how many pallets to order.

---

## Part 3 - Consulting review of my partner's four cases

### Executive summary

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

### Apply — first-pass classification

| Case | Likely category | Why this is my first-pass call |
|---|---|---|
| **1 — logistics burnout detection** | **Prohibited** — Art 5, emotion recognition in the workplace | Facial expression and voice tone analysis to infer worker emotional state, in the workplace, for evaluative purposes — coaching, performance conversations, promotion shortlists. That is the banned fact pattern exactly. The vendor's framing is irrelevant; so is the "one input among many" defence. Two aggravating facts: employees were told the cameras are for safety monitoring, so the deployment is covert; and the score feeds promotion, which would independently be Annex III(4) high-risk if it were not already prohibited. |
| **2 — retail CV screening** | **High-risk** — Annex III(4), employment: recruitment and selection | Scoring and ranking candidates for hiring is a listed high-risk use. Two design faults compound it: recruiters "mostly only" open the strong-fit folder and it is undecided whether anyone reads a "not a fit" before the automated rejection sends — so there may be no human in the loop at the point of detriment; and the model is trained on five years of past hiring plus one-year retention, so it learns who the company historically hired and who happened to stay, both of which encode existing bias and neither of which is a clean measure of merit. |
| **3 — electronics chat widget** | **Limited risk / transparency** — Art 50(1) | A conversational system with a human-styled name and avatar that a user could reasonably mistake for a person. It makes no binding decision — refunds still need a human click — so no Annex III area is engaged and it does not rise to high-risk. The obligation is disclosure. A "beta support tool" label in the corner does not discharge it: the duty is to inform the user they are interacting with an AI system, and the persona actively works against that inference. |
| **4 — grocery demand forecasting** | **Minimal risk** | Aggregate SKU-level forecasting from sales, weather and calendar data. No personal data, no Annex III area, no individual assessed, and store managers can accept, adjust or override every suggestion before it is submitted. No specific AI Act obligations attach. |

### Integrate — architecture and role map

| Case | Architecture: trigger → behaviour → human review → output → logging/disclosure | Provider | Deployer | Vendor |
|---|---|---|---|---|
| **1** | Shift/stand-up begins → cameras and mics stream to vendor model inferring emotional state → **none before the score lands**; supervisor sees a finished weekly score → per-employee engagement score on a dashboard → scores retained and reused in performance and promotion; no disclosure to staff | Camera-software vendor (model + system placed on market under its name) | Logistics operator | Yes — the vendor is the AI Act provider; the operator cannot contract out of its own deployer duties, and here the practice is prohibited for both |
| **2** | Application submitted → model scores CV + assessment against the job description, trained on 5y hiring and retention outcomes → recruiter reviews strong-fit tier only; lower tiers may auto-reject unreviewed → strong / maybe / not-a-fit ranking + automated rejection email → needs full-ranking logs, candidate disclosure, and instructions for use | Vendor if purchased; the retailer itself if built in-house — **confirm before sign-off**, it determines who owns the technical documentation and conformity assessment | Retail chain | Likely — if bought in, require the provider's Art 13 instructions for use, Art 10 bias-testing evidence and Art 11 technical documentation as a procurement condition |
| **3** | Customer opens chat → GPAI model with retrieval over product and policy docs answers → escalates to a human on frustration or out-of-scope; refunds require a human click → conversational answer → **needs an explicit AI disclosure at the top of the conversation**, plus retention of chat logs per normal policy | GPAI model vendor is the upstream model provider; the retailer is the **downstream product provider** of the widget it ships under its own brand | Retail chain (also the product provider here) | Yes — GPAI supplier. "Powered by X" transfers no product-level obligation upward |
| **4** | Nightly/weekly planning cycle → model forecasts demand per store per SKU from sales, weather, calendar → store manager accepts, adjusts or overrides every suggestion → suggested reorder quantity to the warehouse → standard operational logging; no AI Act logging duty | Retailer if in-house; forecasting vendor if bought | Grocery chain | Only commercially — check weather/event data licence terms for downstream-use restrictions |

### Verify — obligations and decision

Decision rules applied consistently: prohibited → deny and redesign · high-risk → approve only on
controls, oversight and documentation · limited risk → approve on disclosure and deployment
boundaries · minimal → approve, flagging parallel non-AI-Act issues.

| Case | Required obligations or controls | Decision |
|---|---|---|
| **1** | None available. The prohibition attaches to the practice itself, so no consent flow, disclosure, accuracy threshold or human-review layer makes it lawful. Also engages GDPR: covert biometric processing described to staff as safety monitoring. | **Deny and redesign** |
| **2** | Mandatory human review of every rejection before it sends (fixes both Art 14 and GDPR Art 22) · bias testing across demographic groups on the 5-year training set, and challenge retention-as-a-label · risk management system (Art 9) · data governance and documentation (Arts 10–11) · full-ranking logs retained ≥6 months (Art 12) · instructions for use and candidate-facing disclosure that AI is used in screening (Art 13) · registration and conformity assessment before the Annex III date. **Note: internal control self-assessment under Annex VI — Annex III(4) does not need a notified body.** **No FRIA**: a private retailer hiring for itself is not a public body, not a private entity providing a public service, and not a 5(b)/(c) deployer. | **Approve with controls** |
| **3** | Explicit "you are chatting with an AI assistant" notice at the start of every conversation, not a corner label and not implied by the persona · keep the human-escalation path · hold the boundary that no binding decision (refund, warranty outcome) is issued by the system alone — if that changes, the classification changes with it. | **Approve with controls** |
| **4** | No AI Act obligations. Parallel issues to flag: weather/event data licensing for downstream use; do not market the forecast as more than a forecast; and if the tool is ever extended to staff scheduling or productivity monitoring it moves into Annex III(4) and this assessment no longer holds. | **Approve** |

#### Redesign option for the prohibited case (Case 1)

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
