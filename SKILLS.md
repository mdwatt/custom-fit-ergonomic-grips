# Skills — Custom-Fit Ergonomic Grips Landing Page

Custom slash commands for working on this validation project.

---

## /build-page
**What it does:** Generates or rewrites `index.html` as a complete, ready-to-deploy landing page.

**Includes:**
- Tailwind CDN
- Hero section with headline + CTA
- Problem section (3 bullet pain points)
- Mockup image block (`assets/mockup.png`)
- How It Works (3 steps)
- Email capture form (Formspree)
- Simple footer with no legal promises

**Usage:** `/build-page` — generates the full file. Optionally pass a headline: `/build-page "Stop letting your grip slow you down"`

---

## /draft-post [community]
**What it does:** Drafts a community post tailored to a specific subreddit or group.

**Usage:**
- `/draft-post reddit` — general Reddit post (r/MouseReview tone)
- `/draft-post facebook` — Facebook group post (warmer, less technical tone)
- `/draft-post slack` — Slack/Discord message (casual, brief)

**Output:** Ready-to-paste post with title, body, and link placeholder. Follows community norms — no hard sell, problem-first framing.

---

## /update-copy [section]
**What it does:** Rewrites copy for a specific section of `index.html`.

**Usage:**
- `/update-copy hero` — rewrite headline and subheadline
- `/update-copy problem` — rewrite the pain-point section
- `/update-copy cta` — rewrite the call-to-action button and surrounding text
- `/update-copy howItWorks` — rewrite the 3-step explanation

---

## /add-analytics
**What it does:** Adds Plausible Analytics snippet to `index.html` `<head>`.

**Usage:** `/add-analytics yourusername.github.io`

Inserts:
```html
<script defer data-domain="yourusername.github.io" src="https://plausible.io/js/script.js"></script>
```

---

## /wire-form [formspree-id]
**What it does:** Replaces `YOUR_FORM_ID` placeholder in `index.html` with a real Formspree form ID.

**Usage:** `/wire-form xpwdkjrn`

---

## /etsy-scan-prompt
**What it does:** Outputs a structured research prompt you can paste into a browser or AI tool to manually scan Etsy for competing products.

**Output:**
```
Search Etsy for: "ergonomic mouse grip" "MX Master grip" "mouse grip attachment" "silicone mouse grip"

For each result record:
- Product name
- Review count
- Average rating
- Price
- Top complaint in reviews (1-star reviews)
- Top praise (5-star reviews)

Signal interpretation:
- 0 listings with 50+ reviews → low demand signal (or untapped market)
- Multiple listings with 100+ reviews mentioning "fatigue" or "comfort" → proven demand
- High reviews but low ratings → demand exists, current solutions are poor (opportunity)
```

---

## /check-signals
**What it does:** Gives you a simple scoring rubric to interpret your validation results.

**Output:**

| Signal | Score |
|--------|-------|
| 0–10 landing page signups from community posts | Red flag — wrong channel or wrong problem |
| 10–30 signups | Weak signal — refine messaging, try different community |
| 30–50 signups | Moderate signal — real interest, sharpen the value prop |
| 50+ signups | Strong signal — consider next step (prototype or pre-order) |
| Signups but no replies to follow-up email | Check if problem is strong enough to pay for |
| Replies with "I'd pay $X for this" | Green light for prototype investment |

**Etsy scan overlay:**
- Etsy demand confirmed + 50+ signups = proceed to prototype
- Etsy demand confirmed + crickets on page = messaging problem, not product problem
- No Etsy demand + 50+ signups = you may be first mover (higher risk, higher reward)
- No Etsy demand + crickets = stop here

---

## /deploy-checklist
**What it does:** Prints a step-by-step GitHub Pages deployment checklist.

**Output:**
```
[ ] Create GitHub repo named: custom-fit-ergonomic-grips
[ ] Push index.html and assets/ to main branch
[ ] GitHub repo → Settings → Pages → Source: main, / (root)
[ ] Wait ~60 seconds, visit: https://yourusername.github.io/custom-fit-ergonomic-grips/
[ ] Replace YOUR_FORM_ID in index.html with real Formspree ID
[ ] Test form submission end-to-end (submit a test email, confirm it arrives)
[ ] Add OG meta tags (og:title, og:description, og:image) for clean link previews in communities
[ ] Share in 1-2 communities and track signups for 72 hours
```
