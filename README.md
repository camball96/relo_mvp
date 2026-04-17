# relo — UI/UX MVP Prototype

> ⚠️ **This is not a functional application.** This repo is a static HTML prototype built to explore the look, feel, and flow of the relo CRM concept before committing to a full build.

---

## What This Is

A pure HTML/CSS mockup of **relo** — a customer relationship management tool. The goal was to click through the core screens in-browser and get a real feel for the layout, navigation, and overall vibe before writing a single line of real application code.

No frameworks. No backend. No working buttons (well, mostly). Just vibes.

---

## Pages

| Page      | URL              | Description                                          |
| --------- | ---------------- | ---------------------------------------------------- |
| Login     | `index.html`     | Landing / sign-in screen                             |
| Dashboard | `dashboard.html` | Overview with stats, activity feed, and charts       |
| Customers | `customers.html` | Customer directory table with filters and pagination |

---

## What Works

- Navigating between the three pages above
- General layout and visual design
- Placeholder data and UI components (charts, tables, stats cards)

## What Doesn't Work

- Login / authentication (clicking Login just goes to the dashboard)
- All sidebar nav links except Dashboard and Customers
- Search, filters, pagination
- Add Customer, Send Invite, and all action buttons
- Any data is hardcoded/fake

---

## Purpose

This MVP exists purely to answer the question:

> _"Does this feel right before I build it properly?"_

If the layout, flow, and aesthetic pass the vibe check, a proper project will be scaffolded on top of this concept. Think of this as a clickable wireframe, not a product.

---

## Stack

- Plain HTML5
- CSS (inline/embedded)
- No JavaScript frameworks
- No backend or database
- Hosted on GitHub Pages for easy sharing and review

---

## Next Steps (if moving forward)

- [ ] Decide on frontend framework (React, Vue, etc.)
- [ ] Define backend/data requirements
- [ ] Flesh out remaining pages (Subscriptions, Revenue, Customer Detail)
- [ ] Replace all placeholder data with real data models
- [ ] Build out proper auth flow

---
