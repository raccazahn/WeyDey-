# 🇱🇷 WeyDey  Liberia's Trusted Cash-on-Delivery Marketplace
> *"No wahala. See am. Pay am. Done."*

[![Status](https://img.shields.io/badge/Status-Student%20Capstone%20%7C%20v1.0-blue)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

##  Overview
WeyDey is a Cash-on-Delivery (CoD) marketplace built specifically for the Liberian market. It solves the trust and logistics gap in local digital commerce by ensuring buyers only pay cash **after physically inspecting** the item at their door, while sellers receive same-day payouts via mobile money.

This project is a **student capstone initiative** addressing the near-total absence of trustworthy, logistics-backed digital trade in Monrovia. Starting with a focused pilot in **Sinkor**, WeyDey acts as the physical and financial bridge between buyers and sellers—eliminating upfront payments, scams, and chaotic WhatsApp trade groups.

## ✨ Core Features
- 🔒 **Open Box Inspection** — Buyers verify items before payment
- 📞 **IVR Auto-Confirmation** — Africa's Talking API scales order verification
- 💸 **Mobile Money Settlement** — Orange Money / Lonestar integration (zero cash holding)
- 🛵 **Rider Accountability App** — Offline-capable queue, cash logging & photo verification
- 🛡️ **Strike-Based Blacklist** — Fair consequence system for fake/no-show orders
- 📱 **PWA-First Architecture** — Buyer & Seller portals work like apps without installation
- 📲 **WhatsApp-Native Growth** — Every listing auto-generates a shareable link

## ️ Tech Stack
| Layer | Technology |
|-------|------------|
| **Frontend (Buyer/Seller)** | React + PWA |
| **Rider Mobile App** | React Native (Android first) |
| **Backend API** | Node.js / Express |
| **Database** | PostgreSQL |
| **Communications** | Africa's Talking (IVR & SMS) |
| **Payments** | Orange Money / Lonestar API |
| **File Storage** | Cloudflare R2 / AWS S3 |
| **Hosting** | Railway / Render |

## 📂 Project Structure
weydey/
├── prd/                 # Product Requirements Document
├── src/
│   ├── api/             # Backend: Express routes, controllers, state machine
│   ├── buyer-pwa/       # React frontend for buyers
│   ├── seller-portal/   # React frontend for sellers
│   └── rider-app/       # React Native mobile app
├── docs/                # Architecture diagrams, API specs, user guides
└── README.md

## 🚀 Getting Started
*(Setup instructions will be added as development progresses)*
git clone https://github.com/raccazahn/WeyDey-.git
cd weydey
# Follow setup guides in /docs

## 👥 Team & Roles
| Role | Responsibility |
|------|----------------|
| **Head of Programming** | Technical architecture, API integrations, code review, sprint planning |
| **Project Lead / Product** | PRD ownership, timeline management, stakeholder coordination |
| **Frontend Developers** | Buyer PWA, Seller portal, Rider app UI, Admin dashboard |
| **Backend Developers** | Order state machine, database schema, IVR/mobile money integrations |
| **UI/UX Designers** | Wireframes, design system, prototype testing |
| **Business & Research** | Market validation, unit economics, go-to-market strategy |
| **Operations Lead** | Rider onboarding, pickup station partnerships, logistics protocol |
| **Faculty Supervisor** | Academic oversight, milestone approval, strategic guidance |

## 📅 Roadmap
- [ ] **Month 0–1:** Foundation (Rider onboarding, API integrations, IVR setup)
- [ ] **Month 1–2:** Soft Launch (Buyer PWA, Seller portal, Rider app live)
- [ ] **Month 2–3:** Iteration (Open Box enforcement, strike system, WhatsApp links)
- [ ] **Month 3–4:** Zone 2 Expansion (Congo Town, featured listings)
- [ ] **Month 4–6:** Stability & Scale Decision (25 orders/day target, unit economics review)

## 📚 Documentation
- 📄 [Product Requirements Document (PRD)](./PRD.md)
- ️ System Architecture *(Coming soon)*
- 🔌 API Specification *(Coming soon)*
- 🧪 Testing & Pilot Guidelines *(Coming soon)*

## ⚖️ License
This project is licensed under the [MIT License](LICENSE).

## 🎓 Academic Context
This repository contains a **student capstone project**. All deliverables are developed under faculty supervision. Fields marked `[brackets]` in documentation are placeholders pending team finalisation. The brand name "WeyDey" is a working title.

---
*Built with ❤️ for Liberia’s digital commerce future.*
