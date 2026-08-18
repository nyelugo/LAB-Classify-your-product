# Client briefs for review — from Vittal

**For:** Ugo Ahukannah · **Exercise:** EU AI Act — Classify your product (Week 7, Day 2–3)

Four client requests below, no category labels — same rules as yours. For each: your first-pass
risk category and why, a compact architecture (trigger → system behaviour → human review point →
output → logging/disclosure layer), who is provider / deployer / third-party vendor, the
obligations or controls you'd require, and your decision — **approve**, **approve with
controls**, or **deny and redesign**.

---

## Case 1 — regional logistics operator

A logistics company with a mostly hourly warehouse workforce wants to cut turnover by catching
burnout early. They're rolling out desk and floor cameras with a vendor's software that reads
facial expressions and voice tone during shifts and stand-ups, producing a weekly per-employee
"engagement score." Supervisors see the score on a dashboard and use it as one input for
coaching, performance conversations, and promotion shortlists. Employees are told the cameras
are "for safety monitoring" — not that emotional analysis feeds performance decisions — and
there's no opt-out or disclosure requirement when a score comes up in a coaching chat.

## Case 2 — national retail chain

A retailer gets ~400 CVs a week for store and warehouse roles and its two-person HR team can't
keep up. They want a tool that scores resumes and a short assessment against the job
description, ranking candidates "strong fit / maybe / not a fit," trained on five years of past
hiring and one-year retention outcomes. Recruiters mostly only open the "strong fit" folder;
lower-tier candidates get an automated rejection email, and it's still undecided whether a
recruiter has to look at any "not a fit" result before it goes out. HR wants to launch in six
weeks.

## Case 3 — consumer electronics retailer

The retailer wants a 24/7 chat widget for order status, warranty claims, and accessory
recommendations, built on a general-purpose language model with retrieval over their product and
policy docs. It has a friendly agent name and avatar, holds real conversations, and escalates to
a live person on frustration or out-of-scope requests. Nothing on screen states outright that
it's an AI rather than a person — just a small "beta support tool" label in the corner. It never
makes a binding decision itself (refunds still need a human click).

## Case 4 — regional grocery chain

The chain wants to cut food waste and improve shelf availability by forecasting daily demand per
store per SKU, using historical sales, weather forecasts, and calendar effects (holidays, local
events). Output feeds an internal ordering dashboard suggesting reorder quantities; store
managers can accept, adjust, or override any suggestion before it's submitted to the warehouse.
Only aggregate sales/product data is used — no customer- or employee-level data — and nothing
about the tool is customer-facing.
