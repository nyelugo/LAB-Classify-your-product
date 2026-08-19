# Stretch — implementation roadmap for the strongest high-risk case

**Case 2, retail CV screening** (my partner's brief). Annex III(4), employment. The client wants to
launch in six weeks.

**Recommended launch posture: proceed on the six-week date, but with reduced automation scope —
human review enabled on every rejection, no unreviewed auto-reject in any tier — and complete the
provider obligations against the 2 December 2027 date.** Not a delay, and not a launch as designed.

Timing note that drives everything below: Annex III obligations apply from **2 December 2027** after
the Digital Omnibus extension, but **GDPR Article 22 applies to the automated rejection step
today**, so the human-review control cannot wait for the AI Act clock.

---

## Must-have before launch

Non-negotiable in the six weeks. Each closes a live exposure, not a future one.

| Owner | Item | Why it cannot wait |
|---|---|---|
| Deployer | **Mandatory human review of every rejection before it sends**, with time budgeted for it | Highest-value control in the engagement: removes the Art 22 exposure and the AI Act Art 14 oversight gap at once |
| Deployer | A named, competent recruiter assigned to oversight | Art 14 requires a person who can decline and override, not a permission nobody uses |
| Deployer | Candidate-facing disclosure that AI is used in screening | Transparency exposure exists now, and it is cheap |
| Deployer | Logging of **full rankings**, not just the strong-fit tier, retained ≥6 months | Without it, no access request or discrimination claim can be answered |
| Both | Settle in writing who is the **provider** — vendor if purchased, the retailer if built in-house | Decides who owns the documentation, and everything downstream depends on it |

## Can be phased against 2 December 2027

Real obligations, wrong thing to spend the six weeks on. Sequence them after launch, on a dated plan
rather than an intention.

| Owner | Item | Article |
|---|---|---|
| Provider | Risk management system, continuous rather than one-off | Art 9 |
| Provider | Data governance on the five-year training set: provenance, labelling, bias examination by demographic group — including a challenge to **retention-as-a-label**, which measures who stayed, not who was good | Art 10 |
| Provider | Technical documentation package | Art 11 + Annex IV |
| Provider | Instructions for use: capabilities, limitations, required oversight | Art 13 |
| Provider | Accuracy and robustness evidence, including performance parity across groups | Art 15 |
| Provider | Conformity assessment by **internal control under Annex VI** — Annex III(4) needs no notified body — then declaration of conformity and CE marking | Arts 43, 47–48 |
| Provider | Registration in the EU database before placement | Art 49 |
| Provider | Post-market monitoring, and an incident workflow that can file within **15 / 10 / 2 days** | Arts 72–73 |

**No FRIA.** A private retailer hiring for itself is not a public body, not a private entity
providing a public service, and not an Annex III 5(b)/(c) deployer.

## Vendor evidence to request

Procurement conditions, asked before signature — after signature they are favours.

- Article 11 technical documentation
- Article 10 bias-testing results, broken down by group rather than in aggregate
- Article 13 instructions for use
- Declaration of conformity and the registration number
- Contractual commitment to incident notification **inside** the client's own Article 73 window, not the vendor's convenience
- A clause prohibiting reuse of candidate data to train the vendor's general model

## Who owns monitoring after launch

The obligation most likely to be orphaned, because it belongs to nobody by default.

| Activity | Owner | Cadence |
|---|---|---|
| Model drift and performance parity across demographic groups | **Provider**, reporting to the deployer | Quarterly, and on any model version change |
| Outcome monitoring in the live workflow — rejection rates by group, override rates by recruiter | **Deployer** (HR) | Monthly; an override rate near zero means the human review has become a rubber stamp |
| Candidate complaints, access requests and contests | **Deployer** (HR with legal) | On receipt, with a standing route back to the provider for logic explanations |
| Serious incident detection and filing | **Deployer** detects, **provider** files under Art 73 | Continuous; the 2-day clock cannot be met by a process invented during the incident |
| Annual review of whether the use case still matches the assessment | **Deployer** | Yearly, or on any scope change |

The override-rate metric is the one to insist on: it is the only measure that tells you whether the
control you sold as the fix is actually operating, rather than merely existing on paper.
