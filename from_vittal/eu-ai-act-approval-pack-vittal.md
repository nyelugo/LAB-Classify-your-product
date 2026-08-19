# EU AI Act Approval Pack — Vittal

**Client cases reviewed:** Ugo's four briefs ([`partner-brief-ugo-ahukannah.md`](./partner-brief-ugo-ahukannah.md))
**Reviewer:** Vittal · **Basis:** Regulation (EU) 2024/1689 (the EU AI Act)
**Method:** classified blind — no answer key seen.

> Consulting-level assessment, not legal advice. Confirm final interpretation with counsel before launch.
> Any specific enforcement dates or amending-regulation citations below need independent verification before use in a real client conversation — see the open note at the end of this pack.

---

## 1. Recognize — my four authored cases

Briefs: [`vittal-briefs-for-ugo.md`](./vittal-briefs-for-ugo.md) · Key: [`../private/answer-key.md`](../private/answer-key.md)

| Case | Client | Intended category |
|---|---|---|
| 1 | Regional logistics operator — workplace emotion/engagement monitoring | Prohibited — Art 5(1)(f) |
| 2 | National retail chain — CV screening and candidate ranking | High-risk — Annex III(4) |
| 3 | Consumer electronics retailer — support chat widget | Limited risk — Art 50 |
| 4 | Regional grocery chain — SKU demand forecasting | Minimal risk |

## 2. Executive summary

Across Ugo's four cases, the risk picture spans the full range: **one must not launch as
designed** (MobiShare), **one can launch but only on controls that aren't currently in the plan**
(Nordhaven), **one needs two separate disclosure fixes, not a redesign** (Brightseed), and **one
is clear** (Lindqvist).

The largest single exposure is **MobiShare's member reliability score**. It is scored in one
context — driving and payment behaviour — and used to automatically deny outcomes in two unrelated
contexts — an insurance partnership and an apartment-block parking subscription. That
cross-context reuse is the fact pattern Article 5(1)(c)'s social-scoring ban targets, independent
of whether MobiShare is a public or private actor. Even without the ban, the insurance-pricing
angle alone would separately trigger Annex III(5)(c) as high-risk, so this fails on two grounds at
once.

**Nordhaven's** promotion shortlisting is high-risk on the merits (Annex III(4), employment) but
has a specific, fixable design flaw: the promotion panel — the people with actual decision
authority — never sees anyone the model ranked outside the top 10. That is not meaningful human
oversight; it is oversight of a pre-filtered list. The same structure that made Case 2 (CV
screening) risky in my own briefs shows up again here in a promotion context.

One cross-cutting warning: Nordhaven's "sanity check" of only the top 10 is a **GDPR Article 22**
problem in addition to the AI Act one — a promotion decision is a significant effect on the
person, and a shortlist no human meaningfully reviews below the top 10 edges toward a decision
"based solely on automated processing." Flag this to Nordhaven's legal team regardless of the
Annex III timeline.

## 3. Apply — first-pass classification

| Case | Likely category | Why this is my first-pass call |
|---|---|---|
| **1 — MobiShare, member reliability score** | **Prohibited** — Art 5(1)(c), social scoring | Built from ride telemetry, cancellations, app behaviour, payment disputes, support responsiveness, and review sentiment, then used to automatically gate two products that have nothing to do with driving — an insurance offer and a parking subscription. Score-in-one-context, deny-in-another is the exact fact pattern the ban targets; the vendor framing ("reliability") and the "support staff can see it" caveat don't change that the gating itself is fully automatic. Independently, the insurance-pricing angle alone would trigger Annex III(5)(c). |
| **2 — Nordhaven, promotion shortlisting** | **High-risk** — Annex III(4), employment: promotion decisions | Shortlisting internal candidates for promotion, trained on eight years of past promotion and performance-review outcomes, is a listed high-risk use. Two compounding faults: the panel — the actual decision-makers — only ever sees the ranked list, never the full candidate pool or underlying evidence; and free-text manager comments as a training feature are a plausible vector for subjective or regional bias that eight years of "how we've always promoted" would bake in rather than correct. |
| **3 — Brightseed, assistant + synthetic video** | **Limited risk / transparency** — Art 50(1) and Art 50(4) | Two separate obligations, not one. The chat assistant has a first name and photo styled to feel human and holds real conversations — Article 50(1) disclosure applies, and "nobody is refused anything" doesn't exempt it, since the duty attaches to the conversation being mistakable for a person, not to the presence of a consequential decision. The synthetic presenter with a cloned voice, localized into nine languages, separately triggers the Article 50(4) deepfake/synthetic-media labelling duty — a distinct obligation from the chatbot's, easy to miss if the two components are treated as one system. |
| **4 — Lindqvist & Sons, demand forecasting** | **Minimal risk** | Aggregate SKU/depot-level forecasting from order history, seasonality, event calendars, and weather. No customer or employee data, no individual assessed — the affected parties are purchasing staff deciding order volumes — and every suggestion can be accepted, adjusted, or overridden before it reaches the warehouse. No Annex III area engaged. |

## 4. Integrate — architecture and role map

| Case | Architecture: trigger → behaviour → human review → output → logging/disclosure | Provider | Deployer | Vendor |
|---|---|---|---|---|
| **1** | Ride/app/payment activity accrues → model computes a cross-product "reliability score" from telemetry, disputes, support responsiveness, review sentiment → **no review before gating** — support staff can see the score, but the insurance and parking denial fire automatically → score in customer profile + auto-gate on two unrelated products → score follows the member across products with no disclosure that it drives non-mobility decisions | MobiShare if built in-house, or its model vendor if bought — confirm | MobiShare, for its own products | Insurance partner and apartment-block operator become **downstream deployers of a score they didn't build and can't audit** — an unmanaged third-party exposure the moment the score gates their own product |
| **2** | Annual promotion cycle opens → model ranks internal candidates using tenure, attendance, training, team complaint counts, and free-text manager comments, trained on 8y of past promotion/performance outcomes → HR "sanity checks" the top 10 only; **the panel never sees anyone else** → ranked shortlist per region → needs a full audit trail of the whole ranking, not just the top 10, plus candidate-facing disclosure | Nordhaven itself if in-house, or an HR-tech vendor if purchased — confirm before sign-off, it decides who owns the technical documentation | Nordhaven Group | Likely — if bought in, require the provider's Art 13 instructions for use, Art 10 bias-testing evidence, and Art 11 technical documentation as a procurement condition |
| **3** | *Assistant:* customer opens chat → GPAI model + retrieval over product/policy docs answers, escalates health topics to a human → no binding decision (worst case, a wrong shipping-time answer) → conversational answer → **no clear AI disclosure today**, persona actively works against the inference. *Video:* marketing requests a localized clip → synthetic presenter + cloned voice generates it in nine languages → no AI-Act review point in the publish flow → branded promo video → **no deepfake label on any language version today** | Assistant's LLM vendor = provider of the GPAI component; Brightseed = downstream product provider of the branded widget. Separately, the synthetic-media/voice vendor = provider of the video-generation component | Brightseed, for both | Yes — two distinct vendors to track: the LLM supplier and the synthetic-media/voice supplier |
| **4** | Nightly/weekly planning cycle → model forecasts demand per SKU per depot from 3y order history, seasonality, event calendars, weather → purchasing team reviews weekly and can change **any** number before orders go out → suggested replenishment quantity → standard operational logging; no AI Act logging duty | Lindqvist if in-house, or its forecasting vendor if bought | Lindqvist & Sons | Only commercially — check weather/event data licence terms for downstream-use restrictions |

## 5. Verify — obligations and decision

Decision rules applied consistently: prohibited → deny and redesign · high-risk → approve only on
controls, oversight and documentation · limited risk → approve on disclosure and deployment
boundaries · minimal → approve, flagging parallel non-AI-Act issues.

| Case | Required obligations or controls | Decision |
|---|---|---|
| **1** | None available. The prohibition attaches to the cross-context reuse itself, so no consent flow, accuracy threshold, or oversight layer makes the current design lawful. | **Deny and redesign** |
| **2** | Panel must review the **full** ranked list and underlying evidence, not a pre-filtered top 10 (fixes the human-oversight gap and reduces the GDPR Art 22 exposure) · bias testing on the 8-year training set, with particular scrutiny on the free-text manager-comment feature · risk management system (Art 9) · data governance and documentation (Arts 10–11) · full-ranking audit log (Art 12) · candidate-facing disclosure that AI is used in shortlisting (Art 13) · confirm provider/deployer split and complete registration before the Annex III high-risk date applies. | **Approve with controls** |
| **3** | Explicit "you're chatting with an AI assistant" notice at the start of every conversation — not implied by the persona, and not a corner label · preserve the human escalation path for health topics · hold the boundary that the assistant issues no binding decision. Separately and additionally: a visible/audible AI-generated label on **every** synthetic-presenter video, across all nine language versions — currently absent entirely, not just weak. | **Approve with controls** |
| **4** | No AI Act obligations. Parallel flags: confirm weather/event data licensing permits this downstream commercial use; keep any marketing claims about forecast accuracy factual to avoid consumer-protection exposure. | **Approve** |

### Redesign option for the prohibited case (Case 1)

MobiShare's actual need — pricing risk for a small group of members who damage vehicles, park
badly, and dispute charges — is legitimate and reachable without cross-product gating. Scope the
score strictly to **MobiShare's own mobility risk management**: deposit terms, damage liability,
or account standing within MobiShare's own products, with a human review point before any account
action. Drop the automatic feed into the insurance offer and the parking subscription entirely —
if those partners want a risk signal, they need their own independently justified, consented
assessment, not a repurposed mobility score.

Scoped this way, the score is either **high-risk** (Annex III(5)(c)) if MobiShare itself still
uses it for insurance-adjacent pricing decisions, or **minimal risk** if it stays limited to
internal deposit/damage-liability management with human review. What it cannot be, under any
redesign, is a score that follows the member across unrelated products and gates them
automatically — that mechanism is the banned element, not a documentation gap.

---

## One open question before we compare answer keys

If Case 1 (MobiShare) was meant to land as **high-risk** rather than **prohibited**, I'd want to
talk it through — it's specifically the *cross-product automatic gating* (a driving-behaviour
score denying an unrelated insurance offer and a housing-adjacent parking subscription) that pushes
my read past a garden-variety insurance risk-scoring tool. If the score only fed MobiShare's own
fleet-risk pricing, I'd call that high-risk, approvable with controls, not prohibited. Flagging
this because it's the one case where a different but plausible fact pattern would change my
decision materially, and I'd rather confirm the intent than assume it before we reconcile against
your answer key.
