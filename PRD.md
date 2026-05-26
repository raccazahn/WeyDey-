# WeyDey — Product Requirements Document

**Liberia's Trusted Cash-on-Delivery Marketplace**  
*"No wahala. See am. Pay am. Done."*

---

## Document Information

| **Field** | **Details** |
|-----------|-------------|
| **Project Name** | WeyDey — CoD Marketplace (working title) |
| **Document Type** | Product Requirements Document (PRD) |
| **Version** | v1.0 — Draft for Supervisor Review |
| **Date** | May 2026 |
| **Status** | Draft — Awaiting Supervisor Approval |
| **Classification** | Student Project — Internal Use Only |
| **Course / Institution** | [Institution Name] — [Course Code / Name] |
| **Project Supervisor** | [Professor Name] — Faculty Supervisor |
| **Team Lead (Programming)** | [Your Name] — Head of Programming |
| **Contributing Teams** | Programming ● Design ● Business & Research ● Ops |

> **NOTE TO SUPERVISOR:** Fields marked [brackets] should be completed by the team before formal submission. The brand name "WeyDey" is a working placeholder. The team will finalise the brand identity before launch.

---

## 1. Executive Summary

WeyDey is a Cash-on-Delivery (CoD) marketplace designed for the Liberian market. Buyers browse and order goods online, pay cash only after physically inspecting the item at their door, and sellers receive payment the same day via mobile money. No upfront payment. No scams. No banking licence required.

This project was initiated as a student capstone to solve a real, documented market problem: the near-total absence of trustworthy, logistics-backed digital commerce in Liberia. Most digital trade currently happens through chaotic WhatsApp groups where buyers are routinely scammed and sellers have no reliable fulfilment path.

WeyDey addresses this by acting as the physical and financial bridge between buyer and seller, beginning with a focused pilot in Sinkor, Montserrado County, before scaling zone by zone.

| **Aspect** | **Details** |
|------------|-------------|
| **Problem** | Trust & logistics chaos in Liberian digital trade |
| **Solution** | CoD + Open Box inspection + same-day settlement |
| **Market** | Monrovia, Liberia — 1.2M population |
| **Model** | Commission per order + delivery fee |

---

## 2. Problem Statement

### 2.1 The Market Reality

The majority of digital trade in Monrovia occurs through Facebook Marketplace and WhatsApp communities. This informal system fails users in three consistent, compounding ways:

| Failure Mode | Buyer Experience | Seller Experience ||--------------|------------------|-------------------|
| **No Trust Layer** | Pays upfront, receives nothing or receives damaged goods | Legitimate sellers lose buyers to scammers with no way to differentiate |
| **No Last-Mile Logistics** | Must self-coordinate cross-town pickup, often during working hours | Deals collapse at the logistics stage even after price is agreed |
| **No Discoverability** | Items scroll off WhatsApp in hours; impossible to search | Must repost daily across multiple groups; high fatigue, low retention |

### 2.2 Why Existing Platforms Fall Short

1. **Facebook Marketplace**: No delivery infrastructure, no payment protection, high scam density
2. **WhatsApp groups**: Ephemeral, unmoderated, unsearchable, no commercial structure
3. **Jumia Liberia**: Weak local last-mile presence, high return rates, not culturally adapted to cash-first behaviour
4. **Mobile money transfers**: Solve payment but not trust — buyer still pays before seeing the item

---

## 3. Project Goals & Academic Objectives

### 3.1 Product Vision

> To be the most trusted way to buy and sell anything in Liberia — where every transaction is protected by a physical inspection, every delivery is accountable, and every Liberian can participate regardless of digital literacy.

### 3.2 Academic Objectives

This project fulfils the following learning outcomes as agreed with the supervising professor:

| # | Objective | Deliverable |
|---|-----------|-------------|
| 1 | Apply software engineering principles to a real-world market problem | Functional web application (buyer + seller + rider portals) |
| 2 | Design and document a complete system architecture | System architecture diagram + API specification |
| 3 | Build and test a multi-actor state machine (order lifecycle) | Order management backend with full state logging |
| 4 | Integrate third-party APIs (IVR, mobile money, file storage) | Working Africa's Talking IVR + mobile money settlement flow |
| 5 | Conduct user research and validate product-market fit | User interviews with 10+ Liberian buyers and sellers |
| 6 | Demonstrate feasibility via a working pilot | 25+ orders completed in Sinkor pilot zone |

### 3.3 Product Goals — Pilot Phase

| # | Goal | Metric | Target |
|---|------|--------|--------|
| G1 | Validate CoD model in Sinkor | Order completion rate | 85%+ |
| G2 | Prove rider cash accountability | Cash reconciliation accuracy | 99% |
| G3 | Build seller confidence | Seller NPS | 50+ |
| G4 | Drive WhatsApp-native growth | Orders from WA share links | 40%+ |
| G5 | Reach pilot break-even | Daily orders — Sinkor zone | 25 orders/day by Month 6 |

### 3.4 Out of Scope — v1.0

1. Digital or card payment processing
2. Seller storefronts or branded pages
3. Inter-county delivery (outside Montserrado)
4. Buyer and seller ratings system (planned for v2.0)
5. Physical warehousing or inventory ownership by the platform6. Native iOS or Android app (PWA first)

---

## 4. Team Structure & Roles

> This is a supervised student group project. All product, design, and technical decisions are subject to review and approval by the faculty supervisor before implementation.

| Role | Team Member | Responsibilities |
|------|-------------|------------------|
| **Faculty Supervisor** | [Professor Name] | Project oversight, milestone approval, academic grading, strategic guidance |
| **Project Lead / Product** | [Student Name] | Overall coordination, PRD ownership, stakeholder communication, timeline management |
| **Head of Programming ★** | [Your Name] | Technical architecture, sprint planning, code review, API integrations, team lead for all engineering deliverables |
| **Frontend Developer(s)** | [Student Name(s)] | Buyer PWA, Seller portal, Rider app UI, Admin dashboard |
| **Backend Developer(s)** | [Student Name(s)] | Order state machine, API layer, database schema, IVR integration |
| **UI/UX Designer(s)** | [Student Name(s)] | Wireframes, user flows, design system, prototype testing |
| **Business & Research** | [Student Name(s)] | Market research, user interviews, unit economics, go-to-market strategy |
| **Operations Lead** | [Student Name] | Rider onboarding plan, pickup station partnerships, logistics protocol |

★ **You are here** — Head of Programming. Your team owns all deliverables under Sections 8 (Technical Architecture) and 5.2 (Feature Specifications).

---

## 5. User Personas

The following personas are based on research into Liberian digital commerce behaviour and direct observation of WhatsApp marketplace communities in Monrovia.

### PERSONA 1 — The Cautious Buyer

**Korto, 28 — Sinkor, Monrovia**  
Government office worker. Smartphone user. Was scammed once on WhatsApp — sent mobile money, never received the item. Now refuses to pay upfront for anything online.

- **Goals:** Find good prices without leaving work. Pay only after she sees and approves the item.
- **Pain points:** Can't tell real sellers from scammers. Items look different from photos. Sellers go silent after payment.

### PERSONA 2 — The Market Seller

**Emmanuel, 35 — Waterside Market**  
Sells phones and accessories. Manages 3 WhatsApp groups (400+ members). Spends 2 hours daily reposting items. Had 6 buyers not show up this month.

- **Goals:** Reach buyers outside his circles. Get paid reliably. Stop wasting time on fake inquiries.
- **Pain points:** Buyers negotiate and vanish. No-shows waste delivery time. Uncertain when cash will arrive.

### PERSONA 3 — The Rider / Agent

**James, 24 — Motorbike Owner, Congo Town**  
Owns a motorbike, currently doing informal errands. Wants steady income with flexibility. Has a smartphone and Orange Money account.

- **Needs:** Clear delivery instructions, transparent earnings per trip, fair dispute process, offline-capable app.
### PERSONA 4 — The Pickup Station Partner

**Fanta, 42 — Corner Shop Owner, Sinkor**  
Runs a corner provisions shop. Trusted community figure. Open 7am–8pm daily. Has space and is comfortable receiving packages.

- **Needs:** Small per-package fee, no liability for lost items, minimal extra workload, official WeyDey pickup point listing.

---

## 6. Core Features & Requirements

### 6.1 Feature Priority Matrix

| Feature | Priority | Version | Why It Exists |
|---------|----------|---------|---------------|
| Buyer browsing — no login required | P0 — Critical | v1.0 | Zero friction to discover listings |
| Seller listing via phone number only | P0 — Critical | v1.0 | No account barrier to post |
| Photo upload (max 5 per listing) | P0 — Critical | v1.0 | Visual proof = trust |
| IVR auto-confirmation call (Africa's Talking) | P0 — Critical | v1.0 | Scales beyond 200 orders/day |
| Open Box checklist enforced in Rider App | P0 — Critical | v1.0 | Dispute prevention protocol |
| Mobile money settlement (Orange / Lonestar) | P0 — Critical | v1.0 | Avoids regulatory cash-holding risk |
| Rider App — order queue, cash log, photo | P0 — Critical | v1.0 | Rider accountability layer |
| Rider cash bond onboarding system | P0 — Critical | v1.0 | Fraud deterrent before first delivery |
| County / zone filter on browse | P1 — High | v1.0 | Relevance for Liberian geography |
| WhatsApp share link per listing | P1 — High | v1.0 | Primary organic growth mechanic |
| Seller 'Mark as Sold' button | P1 — High | v1.0 | Prevents failed delivery attempts |
| Strike-based buyer blacklist | P1 — High | v1.0 | Deters fake orders fairly |
| Pickup station partner portal | P1 — High | v1.0 | Solves buyer-not-home problem |
| Admin ops dashboard | P1 — High | v1.0 | Manual dispute resolution for pilot |
| Order status SMS to buyer | P2 — Medium | v1.1 | Reduces inbound support calls |
| Featured listing (paid placement) | P2 — Medium | v1.1 | First revenue beyond commission |
| Buyer / seller ratings & reviews | P3 — Low | v2.0 | Trust layer after network matures |

### 6.2 Key Feature Specifications

#### 6.2.1 — IVR Order Confirmation

Human phone calls cannot scale past 200 orders/day. The IVR (Interactive Voice Response) system replaces human callers from day one.

1. Triggered automatically 15 minutes after order placement
2. Buyer hears: "You placed a WeyDey order for [item]. Press 1 to confirm you have cash ready. Press 2 to cancel."
3. Press 1 → order moves to CONFIRMED, rider assigned, seller notified
4. Press 2 or no answer after 2 attempts → order auto-cancelled
5. SMS fallback if call fails: confirmation link sent to buyer's phone
6. Recommended provider: Africa's Talking API (active in Liberia, affordable, well-documented)

#### 6.2.2 — Open Box Inspection Protocol

| Step | Rider Action | System Action |
|------|--------------|---------------|| 1 | Photograph item before sealing at seller location | Photo timestamped and stored against order ID |
| 2 | Arrive at buyer's door, tap 'Arrived' in app | Buyer receives 'Your rider is here' SMS |
| 3 | Open box with buyer present — 3-minute inspection cap | Countdown timer displayed in Rider App |
| 4 | Buyer accepts → rider taps 'Collected', enters cash amount | Receipt SMS to buyer; mobile money deposit triggered |
| 5 | Buyer rejects → rider photographs item, calls ops line | Dispute ticket auto-created; 24h resolution SLA |

#### 6.2.3 — Mobile Money Settlement Flow

> **CRITICAL ARCHITECTURAL RULE:** WeyDey must never hold third-party funds in a personal or company bank account. All collected cash is routed through a licensed mobile money provider. This protects the project from Central Bank of Liberia regulatory exposure.

1. Rider deposits collected cash at nearest Orange Money / Lonestar agent within 2 hours of delivery
2. Rider uploads deposit receipt photo in the Rider App
3. System verifies via mobile money API and triggers seller payout automatically
4. Seller receives funds (minus commission + delivery fee) within 4 hours of delivery confirmation
5. WeyDey commission credited to platform mobile money account

#### 6.2.4 — Rider Cash Bond & Onboarding

1. Submit national ID or passport
2. Submit motorbike registration document
3. Pay refundable $20 USD cash bond (held against theft or order abandonment)
4. Complete 30-minute in-person protocol training with ops team
5. Bond returned in full after 90-day clean record or upon clean voluntary departure

#### 6.2.5 — Strike-Based Blacklist System

| Strike | Trigger | Consequence |
|--------|---------|-------------|
| Strike 1 | IVR confirmed but not home at delivery | Warning SMS sent to buyer phone |
| Strike 2 | Second no-show within 30 days | Next order requires 10% mobile money deposit upfront |
| Strike 3 | Third no-show or confirmed fraudulent order | Account suspended 90 days; appeal available via ops call |

---

## 7. Order Lifecycle — State Machine

Every order moves through a defined set of states. Each transition is logged with a timestamp and the actor responsible. No money moves without a confirmed state change.

| # | State | Triggered By | Actor | Next Action |
|---|-------|--------------|-------|-------------|
| 1 | PLACED | Buyer submits order | System | IVR call sent within 15 min |
| 2 | CONFIRMED | Buyer presses 1 on IVR | Buyer | Rider assigned; seller notified |
| 3 | COLLECTED | Rider picks up item from seller | Rider | Dispatch photo taken; route starts |
| 4 | EN ROUTE | Rider taps 'Departed' in app | Rider | Buyer receives ETA SMS |
| 5 | AT DOOR | Rider taps 'Arrived' in app | Rider | 3-minute inspection window opens |
| 6 | DELIVERED | Buyer accepts; rider logs cash amount | Rider + Buyer | Mobile money deposit triggered |
| 7 | SETTLED | Rider deposit receipt confirmed | System | Seller paid; commission retained |
| 8 | CANCELLED | No IVR answer / buyer rejects / ops decision | System / Ops | Reason logged; rider partial fee paid |
| 9 | DISPUTED | Buyer rejects at door; both parties disagree | Ops | Ticket created; 24h resolution SLA |
---

## 8. Technical Architecture

> This section is owned by the Programming Team. All technology choices below are recommendations — final decisions require Programming Team Lead approval and Supervisor sign-off.

### 8.1 System Components

| Component | Recommended Tech | Responsibility |
|-----------|------------------|----------------|
| **Buyer Web App** | React + PWA | Browse listings, place orders, track delivery status. No app install required. |
| **Seller Web Portal** | React + PWA | Post/manage listings, view settlement history, mark items sold. |
| **Rider Mobile App** | React Native (Android first) | Order queue, GPS logging, Open Box checklist, cash entry, photo upload. |
| **Admin / Ops Dashboard** | React + Node.js | Order monitoring, dispute management, rider management, blacklist controls. |
| **Backend API** | Node.js / Express | Order state machine, authentication, settlement triggers, all business logic. |
| **Database** | PostgreSQL | Orders, listings, users, rider logs, audit trail, blacklist, receipts. |
| **IVR & SMS** | Africa's Talking API | Automated confirmation calls, delivery SMS notifications, fallback links. |
| **Mobile Money** | Orange Money / Lonestar API | Rider deposit verification, automated seller payout. |
| **File Storage** | Cloudflare R2 (or AWS S3) | Listing photos, dispatch photos, receipt uploads. 90-day retention policy. |
| **Hosting** | Railway or Render | Low cost, fast deployment, scalable. Suitable for student project budget. |

### 8.2 Technical Risk Register

| Risk | Level | Mitigation |
|------|-------|------------|
| Mobile money API unavailable or rate-limited | Medium | Payment retry queue; manual fallback log; ops team notified on failure |
| Rider app offline in low-connectivity zones | High | Full offline mode required; all data syncs on reconnect; no GPS dependency for order completion |
| Africa's Talking IVR fails | Low | SMS confirmation link as fallback; 2 call attempts before auto-cancel |
| Photo storage costs grow unexpectedly | Medium | Compress all uploads to max 800px on client before upload; 90-day auto-deletion policy |
| Concurrent order state conflicts in DB | Low | Optimistic locking on all order state transitions |
| Mobile money API integration blocked (regulatory) | Medium | Engage Orange Money early; have Lonestar as backup; manual settlement as last resort |

---

## 9. Business Model & Unit Economics

### 9.1 Revenue Streams

| Revenue Stream | Rate | Notes |
|----------------|------|-------|
| **Platform Commission** | 8–10% per order | Deducted before seller settlement. Core revenue engine. |
| **Buyer Delivery Fee** | $1.50–$2.00 flat | Covers rider fuel + wage contribution. Not a profit centre. |
| **Featured Listings** | $2–5 / 7 days | Gold badge + top placement. Launched in v1.1 once seller base established. |
| **Pickup Station Fee** | $0.50 per pickup | Optional; only applies when buyer collects from partner station. |

### 9.2 Sinkor Pilot Unit Economics

**Assumptions:** Average basket $12 USD • 10% commission • $2 delivery fee • 1 rider @ $15/day • 22 working days/month

| Metric | 10 orders/day | 25 orders/day ||--------|---------------|---------------|
| Gross Revenue (commission + delivery fee) | $32.00 | $80.00 |
| Rider Cost (wages + fuel) | $15.00 | $20.00 |
| IVR + SMS Cost (est.) | $1.50 | $3.75 |
| **Net Daily Margin** | **$15.50** | **$56.25** |
| Monthly Net (22 working days) | $341 | $1,237 |
| Break-even daily order volume | ~9 orders/day | — |

> **Break-even at approximately 9 orders/day is achievable within the first month of pilot. 25 orders/day is the threshold for a healthy operation. The unit economics are sound — the critical variable is adoption speed.**

---

## 10. Go-to-Market Strategy

### 10.1 Phase 1 — Sinkor Pilot (Months 1–3)

1. Recruit 10 founding sellers via personal outreach at Waterside Market and Red Light
2. Recruit 2 vetted riders from existing motorbike community networks
3. Sign 3 pickup station partners (pharmacy, provisions shop, print shop)
4. Target: 100 orders in first 30 days of live operation
5. All listings auto-generate a WhatsApp share link — primary growth channel
6. Ops team handles all disputes manually during pilot

### 10.2 Phase 2 — Zone Expansion (Months 4–6)

1. Add Congo Town and Paynesville zones based on Sinkor demand signals
2. Rider network grows from 2 to 6 based on order volume
3. Featured listings monetisation launched
4. Target: 25 orders/day across all active zones

### 10.3 Growth Engine

> Zero advertising budget in Phase 1. Every listing is a WhatsApp share link. Every successful delivery generates a real story shared in a community group. Trust travels person-to-person — the most powerful distribution channel in Liberia.

1. Seller incentive: listings always free, no monthly fee
2. Buyer referral: refer a friend who completes an order, earn $1 delivery credit
3. Community agent programme: trusted locals earn $0.25 per referred completed order

---

## 11. Risk Register

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Rider absconds with collected cash | Medium | Critical | Cash bond + mandatory mobile money deposit within 2h + rider ID verification at onboarding |
| Regulatory challenge on cash handling | Medium | High | Route all funds through licensed mobile money. Obtain legal opinion before launch. |
| Low seller adoption at launch | Medium | High | Personal onboarding by ops team. Zero fees forever. Show first 10 sellers the unit economics directly. |
| High Return-to-Origin (RTO) rate | High | High | IVR pre-confirms cash availability. Strike system deters no-shows. 3-minute inspection cap. |
| Competitor copies the model | High | Medium | Moat = rider network + blacklist data + pickup station relationships. Ship fast, iterate faster. |
| Power or connectivity outages | High | Medium | Rider app full offline mode required. SMS fallback for all critical notifications. |
| Fake or fraudulent listings | Medium | High | Phone number required to post. Strike system. Community report button on every listing. |
| CBL licensing triggered at scale | Low | Critical | Monitor monthly cash flow. Engage CBL proactively when approaching $10K monthly volume. |

---

## 12. Key Performance Indicators (KPIs)

| KPI | Definition | Month 1 | Month 3 | Month 6 |
|-----|------------|---------|---------|---------|
| Order Completion Rate | Delivered ÷ Confirmed orders | 70% | 82% | 88% |
| Return-to-Origin Rate | Cancelled at door ÷ all deliveries | <20% | <12% | <8% |
| Seller 30-Day Retention | Sellers active after 30 days | 60% | 70% | 80% |
| Cash Reconciliation Accuracy | Logged vs. settled cash | 95% | 98% | 99.5% |
| Daily Active Orders | Orders placed per day (all zones) | 5 | 15 | 25+ |
| WhatsApp Referral Rate | Orders from WA share links | 20% | 35% | 45% |
| Dispute Resolution Time | Hours from open to closed ticket | 48h | 24h | 12h |
| Rider On-Time Rate | Deliveries within promised window | 75% | 85% | 92% |

---

## 13. Project Roadmap & Milestones

| Timeline | Milestone | Key Deliverables |
|----------|-----------|------------------|
| **Month 0–1** | Foundation | Rider onboarding system, mobile money API integration, IVR setup, 10 founding sellers signed, 2 riders vetted, 3 pickup station partners contracted |
| **Month 1–2** | Soft Launch | Buyer PWA live, Seller portal live, Rider App (Android) live, first 100 orders completed, ops team handling all disputes manually |
| **Month 2–3** | Iteration | Open Box checklist enforced in Rider App, strike system live, photo upload on all listings, WhatsApp share link on every listing |
| **Month 3–4** | Zone 2 | Congo Town zone added, 2 additional riders recruited, IVR fully replacing human confirmation calls, featured listing revenue launched |
| **Month 4–6** | Stability | 25 orders/day target hit, dispute resolution under 24h, rider retention above 80%, Paynesville zone scoped and planned |
| **Month 6+** | Scale Decision | Full unit economics review with Supervisor. If confirmed, prepare seed funding pitch for 3-county expansion (Buchanan, Gbarnga). If not, deepen Sinkor density first. |

---

## 14. Open Questions for Supervisor

> The following questions require supervisor input or external research before development begins. Each is assigned to a team role and has a target resolution date.

| # | Question | Owner | Target Date |
|---|----------|-------|-------------|
| 1 | Which mobile money provider — Orange Money or Lonestar — offers better API access and settlement terms for a new project? | Programming Lead | Before Month 0 |
| 2 | Is the $20 rider cash bond legally structured as a deposit under Liberian labour law, and does it require formal documentation? | Supervisor / Legal Research | Before Month 0 |
| 3 | Does Africa's Talking support IVR in Liberia with local Liberian English voice? If not, what is the fallback? | Programming Lead | Month 0 |
| 4 | At what transaction volume does the Central Bank of Liberia require formal notification or licensing for a payment facilitation platform? | Supervisor / Research Team | Month 1 |
| 5 | What is the minimum viable Rider App feature set — and should v1.0 be Android only given device distribution in Monrovia? | Programming Lead | Month 0 |
| 6 | Should the platform trademark the name 'WeyDey' or wait for the final brand name decision before filing? | Project Lead + Supervisor | Month 0 |
| 7 | What data protection obligations apply to storing buyer phone numbers and order histories under Liberian law? | Supervisor / Research Team | Month 1 |

---

## 15. Appendix

### 15.1 Competitive Landscape

| Platform | CoD Available | Local Delivery | Trust Layer | Liberia-Specific |
|----------|---------------|----------------|-------------|------------------|
| Facebook Marketplace | No | No | None | Partial |
| WhatsApp Groups | No | No | None | Yes |
| Jumia Liberia | Yes | Partial | Some | Weak |
| **WeyDey (this project)** | **Yes** | **Yes** | **Full — IVR + Open Box** | **Yes — built for Liberia** |

### 15.2 Glossary

| Term | Definition |
|------|------------|
| **CoD** | Cash on Delivery — buyer pays cash when goods arrive at their door |
| **IVR** | Interactive Voice Response — automated phone call system (press 1 to confirm) |
| **Open Box** | WeyDey's policy requiring the buyer to inspect goods before paying |
| **RTO** | Return to Origin — when a delivery fails and the item returns to the seller |
| **PWA** | Progressive Web App — a website that works like a mobile app without app store download |
| **State Machine** | Software system that tracks an order through defined stages (Placed → Confirmed → Delivered etc.) |
| **CBL** | Central Bank of Liberia — the regulatory authority for financial transactions in Liberia |
| **Strike System** | WeyDey's graduated consequence system for buyers who place fake or abandoned orders |

---

## Supervisor Approval

> This document requires review and sign-off by the faculty supervisor before the project proceeds to the development phase. Please annotate any sections requiring revision.

| Role | Name & Signature    | Date    |
|------|------------------|------|
| Faculty Supervisor | | |
| Project Lead | | |
| Head of Programming | | |
| Head of Business & Research | | |
| Head of Operations Lead | | |

---

**End of Document**  
*WeyDey PRD v1.0 — Student Project*  
*Page 1 of 1 — WeyDey CoD Marketplace | Confidential — Student Use Only*
