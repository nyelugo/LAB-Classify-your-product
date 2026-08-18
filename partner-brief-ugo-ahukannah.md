# Client briefs for review — from Ugo Ahukannah

**For:** Vittal · **Exercise:** EU AI Act — Classify your product (Week 7, Day 2–3)

Four client requests below, as they came out of discovery calls. They are written the way
clients actually talk: the business problem is clear, the legal position is not. No category
labels — that is the point of the exercise.

For each one, please come back with: your first-pass risk category and why, a compact
architecture (trigger → system behaviour → human review point → output → logging/disclosure
layer), who is provider / deployer / third-party vendor, the obligations or controls you would
require, and your decision — **approve**, **approve with controls**, or **deny and redesign**.

---

## Case 1 — MobiShare (urban mobility)

MobiShare runs car and e-scooter sharing in six European cities. They lose money on a small
group of users who damage vehicles, park badly and dispute charges, but they cannot tell who
those users are until after the damage. They want a "member reliability score" built from ride
telemetry, cancellation history, app behaviour, payment disputes, how quickly people respond to
support messages, and public review sentiment. The score would sit in the customer profile and
follow the member across all MobiShare products — so a low score would also mean rejection from
their new insurance partner offer and their apartment-block parking subscription, neither of
which is about driving. Support staff can see the score but the gating is automatic.

## Case 2 — Nordhaven Group (facilities management, 4,000 staff)

Nordhaven promotes supervisors to regional team leads once a year, and HR says the process is
inconsistent between regions. They want a system that shortlists internal candidates for
promotion by learning from the last eight years of promotion decisions and subsequent
performance reviews. Inputs are tenure, shift-attendance records, completed training modules,
customer-complaint counts attached to each supervisor's team, and free-text manager comments.
The system outputs a ranked shortlist per region, and HR business partners say they will "sanity
check" the top ten before the panel sees it, though the panel only ever receives the ranked list.

## Case 3 — Brightseed Nutrition (D2C supplements)

Brightseed wants to cut support costs and refresh their marketing at the same time. Two pieces:
a customer-facing assistant on their website that answers product questions, order status and
returns in a warm conversational style with a first name and a photo; and a set of short
promotional videos featuring a synthetic presenter with a cloned voice, so they can localise
campaigns into nine languages without reshooting. The assistant escalates anything about health
conditions to a human. Nobody is refused anything by either system — worst case a customer gets
a wrong answer about shipping times.

## Case 4 — Lindqvist & Sons (regional grocery wholesaler)

Lindqvist supplies 140 independent grocers and is carrying too much stock on slow lines while
running out of fast ones. They want demand forecasting per SKU per depot, learning from three
years of order history, seasonality, local event calendars and weather data, to generate
suggested replenishment quantities. The purchasing team reviews the suggestions in a weekly
planning session and can change any number before orders go out. No customer or employee data is
involved, and no individual is assessed or affected by the output — the affected parties are
purchasing staff deciding how many pallets to order.
