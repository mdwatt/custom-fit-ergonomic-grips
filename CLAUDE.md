# Custom-Fit Ergonomic Grips — Landing Page

## Project Purpose
No-hardware validation landing page for a custom-fit ergonomic grip product (targeting power users of mice like MX Master 3, Logitech G502, etc.). Goal: collect pre-interest emails and measure demand *before* any physical product investment (~$800 threshold).

## Tech Stack
- **HTML/CSS/JS** — single `index.html`, no framework, no build step
- **Tailwind CSS** — loaded via CDN (`<script src="https://cdn.tailwindcss.com">`)
- **Formspree** — email capture (`action="https://formspree.io/f/YOUR_FORM_ID"`)
- **GitHub Pages** — hosting (push `main` branch, enable Pages in repo settings)

## File Structure
```
/
├── index.html          # Single-page landing page
├── assets/
│   ├── mockup.png      # Product render or Figma export
│   └── og-image.png    # Open Graph image for social sharing
├── CLAUDE.md
├── AGENTS.md
└── SKILLS.md
```

## Key Sections in index.html
1. **Hero** — headline, subheadline, single CTA ("Get Early Access")
2. **Problem** — who this is for (lawyers, devs, designers using mice 6+ hrs/day)
3. **Mockup/Render** — image of the grip concept
4. **How It Works** — 3-step simple explanation
5. **Social Proof placeholder** — "Join X others on the waitlist"
6. **Email Form** — Formspree form, first name + email only
7. **Footer** — no promises, no money collected

## Validation Goals
- Target: 50+ signups from cold community posts = strong signal
- Track: form submissions (Formspree dashboard), page visits (add Plausible or Umami analytics, both free)
- Share into: r/MechanicalKeyboards, r/MouseReview, Logitech MX Master Facebook groups, dev/legal productivity Slack/Discord communities

## DO NOT
- Collect payment or deposit of any kind
- Promise a ship date
- Over-engineer: no React, no Next.js, no CMS, no database

## Formspree Setup
1. Create free account at formspree.io
2. Create a new form, copy the form ID
3. Replace `YOUR_FORM_ID` in index.html with real ID
4. Submissions arrive in your email inbox

## Deploying to GitHub Pages
1. Push repo to GitHub
2. Settings → Pages → Source: `main` branch, `/ (root)` folder
3. Live at `https://yourusername.github.io/custom-fit-ergonomic-grips/`
