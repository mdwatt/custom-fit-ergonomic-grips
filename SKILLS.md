# Skills — Custom-Fit Ergonomic Grips Landing Page

Custom slash commands for working on this top-of-funnel landing page. This page has no form of its own — every CTA links out to `https://www.customfitgrip.com`.

---

## /build-page
**What it does:** Generates or rewrites `index.html` as a complete, ready-to-deploy landing page.

**Includes:**
- Vanilla CSS (no framework)
- Hero section with headline + CTA linking to `https://www.customfitgrip.com`
- Problem section (pain points: grip/wrist fatigue, no personalized fit options)
- Product image / device visuals
- How It Works (3 steps, no photo upload required)
- Devices grid, each with its own CTA to the main site
- Simple footer with no legal/medical promises

**Usage:** `/build-page` — generates the full file. Optionally pass a headline: `/build-page "Stop letting your grip slow you down"`

---

## /draft-post [community]
**What it does:** Drafts a community post tailored to a specific subreddit or group.

**Usage:**
- `/draft-post reddit` — general Reddit post (r/MouseReview tone)
- `/draft-post facebook` — Facebook group post (warmer, less technical tone)
- `/draft-post slack` — Slack/Discord message (casual, brief)

**Output:** Ready-to-paste post with title, body, and link placeholder. Follows community norms — no hard sell, problem-first framing. Link points to the landing page, which itself routes to the main site.

---

## /update-copy [section]
**What it does:** Rewrites copy for a specific section of `index.html`.

**Usage:**
- `/update-copy hero` — rewrite headline and subheadline
- `/update-copy problem` — rewrite the pain-point section
- `/update-copy cta` — rewrite CTA button text (destination stays `https://www.customfitgrip.com`)
- `/update-copy howItWorks` — rewrite the 3-step explanation

---

## /add-analytics
**What it does:** Adds Plausible Analytics snippet to `index.html` `<head>`.

**Usage:** `/add-analytics go.customfitgrip.com`

Inserts:
```html
<script defer data-domain="go.customfitgrip.com" src="https://plausible.io/js/script.js"></script>
```

---

## /etsy-scan-prompt
**What it does:** Outputs a structured research prompt you can paste into a browser or AI tool to manually scan Etsy for competing products.

**Output:**
```
Search Etsy for: "ergonomic mouse grip" "MX Master grip" "mouse grip attachment" "silicone mouse grip" "keyboard wrist rest"

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
**What it does:** Gives you a simple scoring rubric to interpret how well this page is driving traffic to the main site. Since this page has no form, the key metric is outbound click-throughs to `www.customfitgrip.com` (via analytics), not on-page signups.

**Output:**

| Signal | Score |
|--------|-------|
| 0–10 click-throughs from community posts | Red flag — wrong channel or wrong problem |
| 10–30 click-throughs | Weak signal — refine messaging, try different community |
| 30–50 click-throughs | Moderate signal — real interest, sharpen the value prop |
| 50+ click-throughs | Strong signal — traffic and messaging are working |
| Click-throughs but low conversion on main site | Landing page messaging problem is not to blame — check the main site's intake/checkout flow |

**Etsy scan overlay:**
- Etsy demand confirmed + strong click-through rate = messaging and channel are working
- Etsy demand confirmed + crickets on page = messaging problem, not product problem
- No Etsy demand + strong click-through rate = you may be first mover (higher risk, higher reward)
- No Etsy demand + crickets = revisit positioning or channel

---

## /deploy-checklist
**What it does:** Prints a step-by-step GitHub Pages deployment checklist.

**Output:**
```
[ ] Push index.html, assets/, and CNAME to main branch
[ ] GitHub repo → Settings → Pages → Source: main, / (root)
[ ] Confirm custom domain (go.customfitgrip.com) resolves via CNAME
[ ] Verify every CTA links to https://www.customfitgrip.com (no dead links, no forms)
[ ] Add/verify OG meta tags (og:title, og:description, og:image) for clean link previews in communities
[ ] Share in 1-2 communities and track click-throughs for 72 hours
```
