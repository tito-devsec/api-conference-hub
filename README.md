# APICon 2026 — Tanzania's Conference for API Builders

> Three days of talks, workshops and live demos for API builders, platform engineers, API cyber expert and developer-experience leaders — held at **JNICC Posta, Dar es Salaam, Tanzania**.

![TanStack Start](https://img.shields.io/badge/TanStack_Start-v1-ef4444)
![React](https://img.shields.io/badge/React-19-61dafb)
![Vite](https://img.shields.io/badge/Vite-7-646cff)
![TypeScript](https://img.shields.io/badge/TypeScript-strict-3178c6)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-v4-38bdf8)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952b3)
![Bun](https://img.shields.io/badge/Bun-runtime-000000)
![Cloudflare Workers](https://img.shields.io/badge/Deploy-Cloudflare_Workers-f38020)

---

## 📌 About APICon 2026

APICon is Tanzania's home for everyone who designs, ships and operates APIs. The 2026 edition brings together engineers, founders and partners across East Africa for keynotes, hands-on workshops and live integration demos — all under one roof.

- 📅 **When:** 2026 (live countdown on the homepage)
- 📍 **Where:** Julius Nyerere International Convention Centre (JNICC Posta), Dar es Salaam
- 🎟️ **Who it's for:** API builders, platform engineers, DX leaders, founders, students

## 🌐 Live preview

- App: --
- Conference landing page: `/apiconference/index.html`

## ✨ Features

The conference landing page (`public/apiconference/index.html`) ships as a self-contained, fully responsive site:

- **Hero carousel** with three rotating slides and gradient overlays
- **Live countdown timer** to the event date
- **Services grid** — what attendees get out of the conference
- **About** section + **Schedule** with Day 1 / Day 2 / Day 3 tabs
- **Featured Speakers** section
- **Our Team** — interactive showcase of the seven people behind APICon, with:
  - Smooth slide / fade / scale transitions when switching members
  - One large active member on display, with thumbnail navigation
  - Name, role, short bio and social links: **X · GitHub · Instagram · LinkedIn**
  - Honors `prefers-reduced-motion`
- **Gallery**, **FAQ accordion**, **Sponsors**, **Pricing tiers** and **Contact form**
- **Slow smooth in-page scrolling** and on-scroll reveal animations
- Fully responsive Bootstrap 5 grid, mobile-first

## 👥 The Team

The seven people behind APICon 2026 — building Tanzania's API community.

| # | Name          | Role                          | Socials                    |
|---|---------------|-------------------------------|----------------------------|
| 1 | Eng. Ndaga    | Founder                       | X · GitHub · IG · LinkedIn |
| 2 | Tito Oscar    | Developer                     | X · GitHub · IG · LinkedIn |
| 3 | Edger         | Head of Programming           | X · GitHub · IG · LinkedIn |
| 4 | Gilbert       | Partnerships & Sponsorship    | X · GitHub · IG · LinkedIn |
| 5 | Fatma         | Marketing & Communications    | X · GitHub · IG · LinkedIn |
| 6 | Baraka        | Operations & Logistics        | X · GitHub · IG · LinkedIn |
| 7 | Grace         | Community & Volunteers        | X · GitHub · IG · LinkedIn |

> Update names, bios, photos and social URLs in the `team` array near the bottom of `public/apiconference/index.html`.

## 🧱 Tech stack

**App shell**
- [TanStack Start v1](https://tanstack.com/start) — full-stack React framework
- React 19 · TypeScript (strict) · Vite 7
- Tailwind CSS v4 (via `src/styles.css`)
- shadcn/ui (`new-york` style) + lucide-react icons
- Bun runtime · deployed to Cloudflare Workers (`wrangler.jsonc`)

**Conference static page** (`public/apiconference/`)
- Bootstrap 5.3 · Lineicons · Animate.css
- Google Fonts (Poppins)
- Vanilla JS for the countdown, team slider, scroll-reveal and smooth scrolling

## 📁 Project structure

```text
.
├── public/
│   └── apiconference/
│       ├── index.html       ← the conference landing page
│       ├── favicon.svg
│       └── logo.png
├── src/
│   ├── routes/              ← TanStack Start file-based routes
│   │   ├── __root.tsx
│   │   └── index.tsx
│   ├── components/ui/       ← shadcn/ui components
│   ├── hooks/
│   ├── lib/utils.ts
│   ├── router.tsx
│   └── styles.css           ← Tailwind v4 + design tokens
├── components.json
├── vite.config.ts
├── wrangler.jsonc
└── package.json
```

## 🚀 Getting started

**Prerequisites:** [Bun](https://bun.sh) (recommended) or Node.js 20+.

```bash
# 1. Install dependencies
bun install

# 2. Start the dev server
bun run dev

# 3. Build for production
bun run build

# 4. Preview the production build
bun run start
```

The conference landing page is served at:

```
http://localhost:3000/apiconference/index.html
```

## ✏️ Editing the conference page

All copy, schedule and team data live in a single file:

```
public/apiconference/index.html
```

Quick pointers:

| What you want to change       | Where to look in `index.html`                |
|-------------------------------|----------------------------------------------|
| Page title / meta description | `<head>` block at the top                    |
| Hero slides + headlines       | `#main-slide` carousel section               |
| Countdown target date         | The `tick()` function in the `<script>` tag  |
| Schedule (Day 1–3)            | `#schedules` section                         |
| Featured speakers             | `#team` section                              |
| **Our Team** (7 members)      | `team = [...]` array near bottom of script   |
| FAQ                           | `#faq` accordion                             |
| Sponsors                      | `#sponsors` section                          |
| Pricing tiers                 | `#pricing` section                           |
| Contact details               | `#contact` section + footer                  |

## ♿ Accessibility & UX

- Respects `prefers-reduced-motion` — disables custom smooth scrolling and team-switch animations for users who request reduced motion.
- Keyboard-navigable controls (Bootstrap accordion, tabs, carousel).
- Semantic landmarks (`<header>`, `<section>`, `<footer>`) and meaningful `alt` text on imagery.
- High-contrast color tokens defined as CSS variables (`--ink`, `--teal`, `--muted`).

## ☁️ Deployment

- The TanStack Start app builds to a Cloudflare Workers bundle — config lives in `wrangler.jsonc`.
- Static assets in `public/` (including `apiconference/index.html`) are served directly.
- One-click publishing is also available via Lovable.

## 🛣️ Roadmap

- [ ] Online ticketing & checkout
- [ ] Call-for-Proposals (CFP) submission form
- [ ] Sponsor portal with downloadable prospectus
- [ ] Bilingual toggle (English / Kiswahili)
- [ ] Replace placeholder avatars with real team photos
- [ ] Wire up real social account URLs for each team member

## 🙏 Credits

Developed with ❤️ by **[Titodevsec](https://titodevsec.online)**.

Built by the APICon team:
**Eng. Ndaga · Tito Oscar · Edger · Gilbert · Fatma · Baraka · Grace**

## 📄 License

Released under the **MIT License**. Replace this section if your team prefers a different license.
