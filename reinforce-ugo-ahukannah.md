# Reinforce — counter-arguments, legal checkpoints, and next artefacts

Companion to [`eu-ai-act-approval-pack-ugo-ahukannah.md`](./eu-ai-act-approval-pack-ugo-ahukannah.md).
For each of my partner's four cases: the strongest argument against my call and why it fails, the
point where a legal team must verify rather than take my reading, and the one operational artefact
the client needs next.

---

## Case 1 — logistics operator, workplace emotion monitoring (prohibited)

**The counter-argument, put at its strongest.** The client will say this is aggregate wellbeing
analytics, not evaluation — and, more dangerously, that Article 5(1)(f)'s **medical and safety
carve-out** covers it, because the cameras were installed for safety monitoring and fatigue in a
warehouse is a genuine safety matter.

**Why it fails.** The carve-out is narrow and purpose-bound: it permits emotion inference *for*
medical or safety reasons, such as detecting driver fatigue to prevent an accident. It does not
launder a system whose outputs feed coaching, performance conversations and promotion shortlists —
that is evaluative use of worker emotion, which is the banned core. The safety framing also cuts
the other way here: staff were told the cameras were for safety, so the deployment is covert as to
its actual purpose, which forecloses any transparency or consent-based defence rather than
supporting one.

**Where legal must verify.** Whether a genuinely separated fatigue-detection function could be
carved out and run under the exception, with no data path into performance systems; the works
council or employee-representation consultation duties in each member state, which are triggered
independently of the AI Act; and the GDPR Article 9 position on biometric and emotional inference.

**Operational artefact needed next:** an **employee-facing transparency notice and works council
consultation pack** for the redesigned aggregate system — plus a written decommissioning record for
the biometric layer, because "we stopped using it" is worth nothing without evidence of when and
how.

## Case 2 — retail chain, CV screening (high-risk)

**The counter-argument.** Recruiters *do* review — they open the strong-fit folder before making
calls, so a human is in the loop. And a "not a fit" outcome is not a legal effect: nobody has a
right to a job, and the candidate can apply again.

**Why it fails.** Human review of the accepted set is not review of the rejected set. Article 22
attaches where the detriment lands, and the detriment here is the rejection nobody read. On the
second limb, exclusion from employment is the paradigm "similarly significant effect" in EDPB
guidance — the absence of an entitlement to the job is not the test; the significance of the
exclusion is.

**Where legal must verify.** Whether Article 22(2)(a) contract necessity could ever be argued for
volume triage (I read it as unavailable, but it is the one place a reasonable lawyer might differ);
national employment-law rules on automated hiring and on retention of applicant data; and the
discrimination exposure created by using **one-year retention as the training label**, which is a
proxy for who fitted the existing culture.

**Operational artefact needed next:** a **logging and audit policy** covering full rankings rather
than just the strong-fit tier, paired with a **candidate-facing AI disclosure notice**. Not a FRIA —
a private retailer hiring for itself is outside Article 27.

## Case 3 — electronics retailer, support chat widget (transparency)

**The counter-argument.** Article 50(1) does not apply where AI use is **obvious from the context**.
This is a support widget on a retail site in 2026; every user knows support chat is automated, and
there is a "beta support tool" label in the corner.

**Why it fails.** The exemption is judged against a reasonably well-informed user *encountering
this design* — and the design works against obviousness: a human first name, an avatar, and
conversational turn-taking are precisely the features that make a user believe they are talking to
a person. A label reading "beta support tool" is ambiguous about *what* is beta and does not state
the material fact. A client cannot build a human-seeming persona and then rely on the humanness
being obvious.

**Where legal must verify.** Whether the "obvious from context" exemption is arguable on these
facts; unfair and misleading commercial practices rules, which bite on the persona independently of
the AI Act; and consumer law on warranty handling if the assistant's answers ever bind the retailer.

**Operational artefact needed next:** a **transparency notice and disclosure copy set** — the
opening-message disclosure, the persistent in-widget label, and the escalation wording — reviewed
once and reused, rather than written ad hoc by whoever ships the next release.

## Case 4 — grocery chain, demand forecasting (minimal)

**The counter-argument.** Food distribution is critical infrastructure, so this belongs in Annex III
point 2; and the system does make decisions, since reorder quantities drive what reaches shelves.

**Why it fails.** Annex III(2) covers AI as a safety component in the management and operation of
critical digital infrastructure, road traffic, and utilities supply. Grocery replenishment is
commercially important but is not that, and the Act's concern in that tier is safety of supply
systems, not commercial continuity. More decisively, nothing here assesses a person: the outputs
are pallet counts, every one of which a store manager can override.

**Where legal must verify.** Licensing terms on the weather and event data feeds for downstream
commercial use; whether sharing forecasts with suppliers raises competition-law issues; and a
periodic confirmation that no personal data has crept into the feature set.

**Operational artefact needed next:** a **scope-boundary and re-classification trigger note** — one
page stating that this assessment covers SKU forecasting only, and that any extension to staff
scheduling, productivity monitoring or individual-level prediction moves the system into Annex
III(4) and voids the approval. This is the artefact that matters most for a minimal-risk system,
because minimal-risk systems are the ones that drift.

---

## The pattern across all four

Three of the four counter-arguments are the same move in different clothing: **re-describing the
system so the trigger appears not to apply** — "it's wellbeing analytics", "a human does review",
"everyone knows it's a bot". The Act keys off what the system does to people, not what it is
called, so the answer in each case is to return to the mechanism: whose emotion is inferred, where
the detriment lands, what the user would believe. Case 4 is the mirror image — a client-side
argument for *more* regulation than applies — and the answer there is the same discipline in
reverse: check the Annex entry against the actual use, not the industry label.
