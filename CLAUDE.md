# Custom-Fit Ergonomic Grips — Landing Page

## Project Purpose
Top-of-funnel landing page for the Custom Fit Grip product line (keyboard wrist rests, mouse grips, and comfort accessories aimed at power users of devices like the MX Master 3, Logitech G502, and long-session keyboard users). This page does **not** collect emails or signups itself — every CTA ("Start Your Custom Fit", "Start fitting", "Begin intake form") routes visitors to the main site/app at `www.customfitgrip.com`, where device selection, measurement intake, and checkout actually happen.

## Tech Stack
- **HTML/CSS/JS** — single `index.html`, no framework, no build step
- **Vanilla CSS** — custom `<style>` block in `index.html` (no Tailwind or other CSS framework)
- **No forms on this page** — CTAs are plain `<a>` links to `https://www.customfitgrip.com`
- **GitHub Pages** — hosting (push `main` branch, enable Pages in repo settings), served on custom domain `go.customfitgrip.com` via `CNAME`

## File Structure
```
/
├── index.html          # Single-page landing page
├── assets/              # Logo, hero image, OG image, etc.
├── CNAME                # Custom domain: go.customfitgrip.com
├── CLAUDE.md
├── AGENTS.md
└── SKILLS.md
```

## Key Sections in index.html
1. **Topbar** — logo, nav links (#how, #products, #faq, #contact), CTA to main site
2. **Hero** — headline, subheadline, product image, stats (production time, made-to-order, intake time), CTA to main site
3. **How It Works** (`#how`) — 3-step explanation (choose device → pick measurements → review and checkout) plus a "what you'll need" note
4. **Devices we fit** (`#products`) — product/device grid, each with its own "Start fitting" CTA to main site
5. **FAQ** (`#faq`) — common questions, matched by a JSON-LD FAQPage schema in `<head>`
6. **Final CTA** (`#form`) — despite the `id`, this is not a form; it's a closing CTA banner linking to main site
7. **Footer** (`#contact`) — company name (Zion Insight Holdings LLC, DBA Custom Fit Grip), support email, footer nav

## Validation Goals
- This page is a funnel/awareness layer, not the conversion point — conversion (signups, intake, purchase) happens on `www.customfitgrip.com`
- Track: page visits and outbound click-throughs to `www.customfitgrip.com` (add Plausible or Umami analytics, both free)
- Share into: r/MechanicalKeyboards, r/MouseReview, Logitech MX Master Facebook groups, dev/legal productivity Slack/Discord communities

## DO NOT
- Add an email capture form or signup mechanic to this page — that flow lives on the main site
- Make medical, orthopedic, or FDA/clinical claims (no "treats," "cures," or diagnosis language for RSI, arthritis, carpal tunnel, etc.)
- Promise a ship date beyond the general production window (3–7 business days) stated for orders placed through the main site
- Over-engineer: no React, no Next.js, no CMS, no database

## Deploying to GitHub Pages
1. Push repo to GitHub
2. Settings → Pages → Source: `main` branch, `/ (root)` folder
3. Live at `https://go.customfitgrip.com/` (custom domain via `CNAME`)
