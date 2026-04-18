# ClientWord / Clientward — Product Plan
(working name: EndorseMe → now leaning toward Clientward, domain clientward.co available for $13)

## What It Is

A testimonial collection and aggregation tool for freelancers and service businesses.
You send a link, your client leaves a review, it lives in your dashboard forever.
No widgets. No walls of love. No complexity. Just a permanent home for every good
thing a client ever said about you — organized, searchable, ready to use.

---

## The Problem

Good client feedback is scattered everywhere: email threads, Slack messages, texts,
LinkedIn comments. Most freelancers never collect it systematically. When they need
it — for a proposal, a website update, an outreach email — they can't find it.

The tools that exist (Senja, Testimonial.to, Endorsal, Famewall) are built for
SaaS founders and creator-economy people. They're priced and designed around
product reviews and "walls of love" widgets. Service businesses and freelancers
with repeat client relationships are an afterthought.

---

## The Market Gap

Every tool in the $19–29/month range caps you at one project or "space."
Want to organize by client or project? Pay $59–79/month.

Nobody owns this positioning: **send a link, client submits in 60 seconds,
testimonial is in your dashboard organized by project and client, forever.**

---

## Target Customer

- Freelancers: cinematographers, video editors, designers, copywriters, consultants
- Agencies of one or small service businesses
- Anyone with repeat client relationships who wants to capture feedback systematically

NOT for: SaaS companies, e-commerce stores, product reviews.

---

## Core User Flow (MVP)

1. User signs up (email/password via Supabase Auth)
2. User creates a Project (e.g. "Nike Brand Video — March 2026")
3. App generates a unique collection link for that project
4. User pastes that link into their follow-up email to the client
5. Client clicks link, fills out a simple form:
   - Name
   - Company / Role (optional)
   - Testimonial text
   - Star rating (optional)
6. Testimonial appears in user's dashboard under the correct project
7. User can copy the testimonial text, tag it, or mark it as featured
8. Simple export: copy to clipboard, download as plain text

---

## MVP Scope (v1)

### Must Have
- [ ] Auth (sign up, log in, log out) — Supabase Auth
- [ ] Projects (create, name, archive)
- [ ] Unique collection link per project
- [ ] Public collection form (no login required for submitter)
- [ ] Dashboard: view all testimonials, filterable by project
- [ ] Copy to clipboard
- [ ] Featured flag (star a testimonial)
- [ ] Basic settings (name, email, account)
- [ ] Stripe billing (free tier + paid tier)

### Not in MVP (v2+)
- Video testimonials
- Embeddable website widgets
- Import from Google / LinkedIn / social
- Email sequences / automation
- Team seats
- Custom domains
- Public "wall of love" page

---

## Pricing Model

| Tier    | Price      | Limits                              |
|---------|------------|-------------------------------------|
| Free    | $0/month   | 3 projects, 10 testimonials total   |
| Pro     | $19/month  | Unlimited projects + testimonials   |

Simple. No per-seat, no per-response metering, no feature gating beyond the limit.
The upgrade trigger is hitting the project or testimonial cap.

---

## Tech Stack

| Layer       | Tool                        |
|-------------|----------------------------|
| Framework   | Next.js (App Router)        |
| Database    | Supabase (Postgres + Auth)  |
| Hosting     | Vercel                      |
| Payments    | Stripe                      |
| Email       | Resend                      |
| Styling     | Inline styles (consistent with therateguide.com approach) |

---

## Competitive Positioning

| Tool           | Their Audience         | Price for Multi-Project | Our Advantage          |
|----------------|------------------------|-------------------------|------------------------|
| Senja          | Creators, indie SaaS   | $59/month (5 projects)  | $19 unlimited          |
| Testimonial.to | Indie hackers          | +$30 per space          | $19 unlimited          |
| Endorsal       | E-commerce, mid-market | $79/month (3 properties)| $19 unlimited          |
| Famewall       | Entrepreneurs, coaches | $25/month (15 walls)    | Simpler, service-first |

---

## Go-To-Market

**Launch audience:** therateguide.com email list. These are creative freelancers
who already trust a tool Derek built. They're the exact target customer.

**Positioning message:** "Every good thing a client ever said about you — in one place."

**Launch offer:** Free Pro tier for the first 100 signups from the list.

---

## Open Questions

- Final domain name — clientward.co is available for $13, clientword.com also available
- Whether to add a simple embeddable widget in v1 or hold for v2
- Whether the collection form should allow photo upload from submitter
- Annual pricing discount ($15/month billed annually vs $19/month)

## Name Research (2026-04-17)

Domains checked and rejected: endorseme.com (taken), vouched.co (taken),
cosigned.co (taken), proofbox.co (available but generic), clientbrag.com (available
but "brag" feels self-promotional), clientshout.com (available but phonetically awkward).

**Frontrunner: clientward.co** — "ward" implies orientation toward clients,
directional, distinctive, not owned in this space. $13/yr. Grab it.

Runner-up: clientword.com — "take my client's word for it" writes itself. Clean,
professional, immediately understood.

## Build Timeline

- Weeks 1–2: Scaffold Next.js app, Supabase auth, basic dashboard
- Weeks 3–4: Collection link + public form (core loop)
- Week 5: Stripe integration, deploy to Vercel
- Week 6: Email therateguide.com list, offer free Pro to first 50 signups
- First dollar: ~6 weeks from start
- $5K/month target: 6–12 months
