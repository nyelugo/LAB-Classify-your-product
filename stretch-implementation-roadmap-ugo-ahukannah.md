# Stretch — implementation roadmap for the strongest high-risk case

**Case 2, retail CV screening** (Vittal's brief). Annex III(4), employment. The client wants to
launch in six weeks; this is what each party would actually need. Obligations bite **2 December
2027** under the Digital Omnibus extension — but GDPR Art 22 applies to the automated rejection
step today, so the human-review control cannot wait for the AI Act date.

**What the provider needs before market placement** — the vendor if bought in, the retailer
itself if built in-house; settle this first, because it decides who owns the paperwork.

- Risk management system covering foreseeable misuse, run continuously, not once (Art 9)
- Data governance on the 5-year training set: provenance, labelling, and bias examination across
  demographic groups — including a challenge to *retention-as-a-label*, which measures who stayed,
  not who was good (Art 10)
- Technical documentation package complete before placement (Art 11 + Annex IV)
- Automatic logging of full rankings, not just the strong-fit tier, retained ≥6 months (Art 12)
- Instructions for use stating capabilities, limitations and required oversight (Art 13)
- Human oversight designed in, such that a recruiter can see and override any tier (Art 14)
- Accuracy and robustness evidence, including performance parity across groups (Art 15)
- Conformity assessment by **internal control under Annex VI** — Annex III(4) does not require a
  notified body (Art 43); then declaration of conformity and CE marking (Arts 47–48)
- Registration in the EU database before placement (Art 49)
- Post-market monitoring live, and an incident workflow that can file within **15 / 10 / 2 days**
  under Art 73 — built before go-live, not during the first incident

**What the deployer needs before first use** — the retail chain:

- A named, competent recruiter assigned to oversight, with time budgeted for it
- **Mandatory human review of every rejection before it sends** — the single highest-value control
  in this engagement; fixes the Art 14 gap and the GDPR Art 22 exposure at once
- Candidate-facing disclosure that AI is used in screening
- Use strictly per the provider's instructions; log retention ≥6 months
- **No FRIA** — a private retailer hiring for itself is not a public body, not a private entity
  providing a public service, and not an Annex III 5(b)/(c) deployer

**Evidence to demand from the vendor**, as procurement conditions rather than post-signature asks:
the Art 11 technical documentation, Art 10 bias-testing results broken down by group, the Art 13
instructions for use, the declaration of conformity and registration number, and a contractual
commitment to incident notification inside the client's own Art 73 window.

**Realistic view on the six weeks:** the human-review control and candidate disclosure are
achievable in that window. Bias testing and documentation are not, if the model is being built
in-house. Recommend launching with mandatory human review on every tier and a reduced automation
scope, then completing the provider obligations against the December 2027 date.
