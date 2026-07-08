# Social Masla — Marketing Consultancy Website

A lightweight, static marketing website for **Social Masla**, a performance & growth marketing consultancy founded by Piyush Sachdeva. Built as plain HTML with Tailwind CSS (via CDN) and vanilla JavaScript — no build step, no framework, no dependencies to install.

The design system mirrors the **"Modern Minimal"** shadcn/ui aesthetic (structure and typography), recolored with a custom **Ink / Yale Blue / Powder Blue / Porcelain / Dry Sage** palette.

---

## Pages

| File | Purpose |
|------|---------|
| [`index.html`](index.html) | Home — hero, animated trust strip, "what we do", and a contact form |
| [`about.html`](about.html) | About — founder story (Piyush Sachdeva), stats, approach, platforms |
| [`consultation.html`](consultation.html) | Consultation — services, process, engagement tiers, FAQ |
| [`contact.html`](contact.html) | Contact — enquiry form with business details |

All pages share a common header/nav, footer, design tokens, and light/dark theme toggle.

---

## Tech stack

- **HTML** — four standalone pages (no templating; shared markup is duplicated per page)
- **Tailwind CSS** — loaded from the CDN (`cdn.tailwindcss.com`), configured inline per page
- **CSS custom properties** — the color system lives in `:root` (light) and `.dark` (dark) blocks; Tailwind tokens (`bg-primary`, `text-foreground`, …) are mapped to these variables
- **Google Fonts** — Inter (UI/body), Source Serif 4 (display numbers & quotes), JetBrains Mono (accents)
- **Vanilla JavaScript** — no libraries; all interactivity is hand-written and dependency-free

---

## Key features

- **Light / dark mode** — a header toggle, class-based, persisted to `localStorage`, with a no-flash inline init script.
- **Fully responsive** — including a **full-screen mobile menu** on the home page (hamburger → overlay, with body-scroll lock).
- **Animated trust strip** (home) — stat numbers count up and fade in when scrolled into view.
- **Hero micro-interactions** (home) — subtle, hover-only motion: eyebrow lift, a soft text sheen on "More growth.", and button/arrow movement.
- **Interactive particle background** (home) — a lightweight `<canvas>` field of drifting dashes that react to the cursor; pauses off-screen and respects reduced-motion.
- **Contact forms** — wired to [FormSubmit](https://formsubmit.co) with client-side validation, a honeypot bot trap, and **business-email-only** filtering (blocks free/disposable providers).
- **Accessibility** — `prefers-reduced-motion` is honored across every animation (counters, hero, particles); decorative emoji/icons are `aria-hidden`.

---

## Color palette

| Name | Hex | Role |
|------|-----|------|
| Ink Black | `#0D1821` | Text (light) / background (dark) |
| Yale Blue | `#344966` | Primary (buttons, links, ring) |
| Powder Blue | `#B4CDED` | Accent / primary-on-dark |
| Porcelain | `#F0F4EF` | Background (light) / text (dark) |
| Dry Sage | `#BFCC94` | Complementary accent (particles, highlights) |

A few intermediate surface/border/muted shades are derived from these five. The tokens are defined identically in each page's `<style>` block.

---

## Project structure

```
.
├── index.html            # Home
├── about.html            # About Us
├── consultation.html     # Consultation
├── contact.html          # Contact
├── favicon.ico           # Multi-size favicon (root, auto-requested)
├── assets/
│   ├── logo.png              # Header/footer logo (founder photo)
│   ├── favicon-16.png
│   ├── favicon-32.png
│   ├── apple-touch-icon.png
│   ├── piyush-sachdeva.png   # About-page founder photo
│   └── piyushautomates.png
├── resources/            # Source imagery (favicon source, references)
├── README.md
└── .claude/
    └── launch.json       # Local dev-server config for the preview tooling
```

---

## Running locally

There's no build step — the site is static files.

**Quickest:** open `index.html` directly in a browser.

**With a local server** (recommended, so relative asset paths and `fetch` behave correctly):

```bash
# from the project root
python3 -m http.server 4599
# then visit http://localhost:4599
```

---

## Forms & FormSubmit setup

Both contact forms POST to FormSubmit's AJAX endpoint, delivering to **hello@socialmasla.com**.

> **One-time activation required:** the first real submission triggers a confirmation email from FormSubmit to that inbox. Click its activation link once — until then, submissions are not delivered. To change the destination address, update the `FORM_ENDPOINT` constant in [`index.html`](index.html) and [`contact.html`](contact.html).

Validation is client-side (a deterrent, not a hard gate): it blocks free/personal and disposable email domains and uses a hidden honeypot field to catch bots.

---

## Notes & known constraints

- **Tailwind is loaded via CDN**, which prints a console warning that it's not for production. For a production deploy, compile Tailwind with the CLI/PostCSS instead.
- **Shared markup is duplicated** across the four HTML files (header, footer, design tokens). A change to the nav or palette must be made in each file. Consolidating into a shared CSS file / templating step is a natural next improvement.
- The **full-screen mobile menu** currently exists on the home page only; the other pages don't yet have a mobile nav.
- Client-side email validation can be bypassed by a determined bot; FormSubmit's own server-side protections are the backstop.
