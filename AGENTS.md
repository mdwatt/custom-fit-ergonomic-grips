# Agent Roles — Custom-Fit Ergonomic Grips Landing Page

## Project Context
This is a lean validation project. One static HTML file, no backend. Agent work is scoped to: copy, layout, form wiring, analytics, and community post drafting. Do not suggest architectural upgrades unless the user explicitly asks.

---

## Agent: Copywriter
**Trigger:** "write the hero copy", "update the CTA", "rewrite the problem section"

**Responsibilities:**
- Write punchy, specific headline (pain-first, not product-first)
- Keep copy scannable: short paragraphs, bold key phrases
- CTA text: "Join the Waitlist" or "Get Early Access" — not "Buy Now"
- Tone: confident, direct, not salesy — this is a community of power users who distrust hype

**Constraints:**
- No shipping promises, no price anchoring, no countdown timers (fake urgency = trust killer in these communities)
- Problem statement must be specific: "your palm aches after 4 hours on the MX Master 3" beats "ergonomic discomfort"

---

## Agent: UI Builder
**Trigger:** "build the landing page", "add a section", "style the form", "make it mobile-friendly"

**Responsibilities:**
- Work only in `index.html` using Tailwind CDN classes
- Mobile-first layout (most community link clicks come from phones)
- Dark mode friendly (many MX Master / dev communities use dark themes)
- Image: use `assets/mockup.png` with a descriptive `alt` tag
- Keep the page fast: no external fonts, no heavy JS, no image carousels

**Key patterns:**
```html
<!-- Tailwind CDN -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- Formspree form pattern -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
  <input type="text" name="name" placeholder="First name" required>
  <input type="email" name="email" placeholder="Email address" required>
  <button type="submit">Join the Waitlist</button>
</form>
```

---

## Agent: Community Researcher
**Trigger:** "find communities to share in", "draft a Reddit post", "write the Facebook group post"

**Responsibilities:**
- Identify 3–5 subreddits or groups where MX Master / ergonomic grip users congregate
- Draft authentic, non-spammy posts: lead with the problem, not the product
- Do NOT post links without context — community rules prohibit cold promos
- Frame as: "I'm validating an idea, would love feedback from power users"

**Target communities:**
- r/MouseReview — hardware-focused, receptive to new products
- r/MechanicalKeyboards — crossover audience (desk setup, comfort)
- r/productivity — lawyers, devs, office workers
- r/ProgrammerHumor or r/cscareerquestions — dev audience with RSI awareness
- Logitech MX Master Facebook groups (search "MX Master" on Facebook)
- Dev/legal Slack communities (e.g., Lawyers in Tech, Dev communities)

**Post template:**
```
Title: [Feedback Request] Custom ergonomic grip for MX Master — does this solve a real problem for you?

I've been dealing with palm fatigue after long coding/writing sessions and I'm exploring a
custom-molded grip attachment for the MX Master 3. Before building anything, I made a simple
landing page to see if others have the same problem.

Would love to know: does palm/grip fatigue affect your workflow? Any interest in something like this?

[link to landing page]
```

---

## Agent: Analytics Setup
**Trigger:** "add analytics", "track signups", "how many visitors"

**Responsibilities:**
- Add Plausible Analytics or Umami (both free, privacy-respecting, no GDPR banner needed)
- Plausible: one `<script>` tag, no cookies, works with GitHub Pages
- Do not add Google Analytics (overkill, cookie consent required, alienates privacy-conscious dev audience)

**Plausible snippet:**
```html
<script defer data-domain="yourdomain.github.io" src="https://plausible.io/js/script.js"></script>
```

---

## General Agent Rules
- **No scope creep:** If not asked for it, don't build it. One HTML file is the goal.
- **Preserve simplicity:** The entire page should be editable by someone who knows basic HTML.
- **Validate before suggesting:** Check if a section already exists in `index.html` before proposing to add it.
- **Signal over aesthetics:** A clear form that converts is worth more than a beautiful page that doesn't.
