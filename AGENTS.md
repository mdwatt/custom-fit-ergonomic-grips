# Agent Roles — Custom-Fit Ergonomic Grips Landing Page

## Project Context
This is a lean top-of-funnel landing page. One static HTML file, no backend, no forms. Its only job is to get visitors to click through to the main site/app at `www.customfitgrip.com`, where device selection, measurement intake, and checkout actually happen. Agent work is scoped to: copy, layout, CTA links, analytics, and community post drafting. Do not suggest architectural upgrades unless the user explicitly asks.

---

## Agent: Copywriter
**Trigger:** "write the hero copy", "update the CTA", "rewrite the problem section"

**Responsibilities:**
- Write punchy, specific headline (pain-first, not product-first)
- Keep copy scannable: short paragraphs, bold key phrases
- CTA text: "Start Your Custom Fit", "Start fitting", "Begin intake form" — all link out to `https://www.customfitgrip.com`, not a local form
- Tone: confident, direct, not salesy — this is a community of power users who distrust hype

**Constraints:**
- No shipping promises beyond the stated 3–7 business day production window
- No medical, orthopedic, or FDA/clinical claims — do not use "treats," "cures," or diagnostic language when referencing RSI, arthritis, carpal tunnel, or grip strength issues; describe comfort/fit benefits only
- Problem statement must be specific: "your palm aches after 4 hours on the MX Master 3" beats "ergonomic discomfort"

---

## Agent: UI Builder
**Trigger:** "build the landing page", "add a section", "style a section", "make it mobile-friendly"

**Responsibilities:**
- Work only in `index.html` using the existing vanilla CSS (no Tailwind or other framework)
- Mobile-first layout (most community link clicks come from phones)
- Dark mode friendly (many MX Master / dev communities use dark themes)
- Every primary CTA is an `<a>` tag pointing to `https://www.customfitgrip.com` — never add an email/signup `<form>` to this page
- Keep the page fast: no external fonts, no heavy JS, no image carousels

**Key pattern:**
```html
<a class="btn btn-primary" href="https://www.customfitgrip.com" rel="noopener">Start Your Custom Fit</a>
```

---

## Agent: Community Researcher
**Trigger:** "find communities to share in", "draft a Reddit post", "write the Facebook group post"

**Responsibilities:**
- Identify 3–5 subreddits or groups where MX Master / ergonomic grip users congregate
- Draft authentic, non-spammy posts: lead with the problem, not the product
- Do NOT post links without context — community rules prohibit cold promos
- Frame as: "sharing something that's helped with grip/wrist fatigue" rather than a hard sell — the link goes to the landing page, which itself routes to the main site

**Target communities:**
- r/MouseReview — hardware-focused, receptive to new products
- r/MechanicalKeyboards — crossover audience (desk setup, comfort)
- r/productivity — lawyers, devs, office workers
- r/ProgrammerHumor or r/cscareerquestions — dev audience with RSI awareness
- Logitech MX Master Facebook groups (search "MX Master" on Facebook)
- Dev/legal Slack communities (e.g., Lawyers in Tech, Dev communities)

**Post template:**
```
Title: Anyone else deal with palm/wrist fatigue on long sessions?

I've been dealing with palm fatigue after long coding/writing sessions and found a
custom-molded grip/wrist rest option worth checking out. Curious if others have the
same problem and what's worked for you.

[link to landing page]
```

---

## Agent: Analytics Setup
**Trigger:** "add analytics", "track visitors", "how many click-throughs"

**Responsibilities:**
- Add Plausible Analytics or Umami (both free, privacy-respecting, no GDPR banner needed)
- Track outbound clicks to `www.customfitgrip.com` as the key conversion event (this page has no form to submit)
- Plausible: one `<script>` tag, no cookies, works with GitHub Pages
- Do not add Google Analytics (overkill, cookie consent required, alienates privacy-conscious dev audience)

**Plausible snippet:**
```html
<script defer data-domain="go.customfitgrip.com" src="https://plausible.io/js/script.js"></script>
```

---

## General Agent Rules
- **No scope creep:** If not asked for it, don't build it. One HTML file is the goal.
- **No forms:** This page never collects email or personal data directly — it hands off to the main site
- **No medical claims:** Never imply FDA approval, orthopedic benefit, or treatment of RSI/arthritis/grip conditions
- **Preserve simplicity:** The entire page should be editable by someone who knows basic HTML.
- **Validate before suggesting:** Check if a section already exists in `index.html` before proposing to add it.
- **Signal over aesthetics:** A clear CTA that gets clicked is worth more than a beautiful page that doesn't.
