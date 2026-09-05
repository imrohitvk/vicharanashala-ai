# Vicharanashala Website — Claude Instructions

## What this is
Jekyll site for Vicharanashala (VLED Lab, IIT Ropar) — a lab for education design and EdTech.
Live at: `https://vicharanashala.github.io/vicharanashala-ai`
Fork (preview): `https://pavaniasn.github.io/vicharanashala-ai`

Three audiences: students, faculty, government/funders.

---

## Technical setup — read before touching anything

**No local Jekyll build.** System Ruby is 2.6.10, incompatible with the gem versions GitHub Pages uses. Never run `bundle exec jekyll build`, `bundle install`, or `jekyll serve`. They will fail. Do not try to fix this — local build is not needed.

**SCSS validation only:** `sass --no-source-map _sass/minima.scss /dev/null`
Pre-existing `@import` and `darken()`/`lighten()` deprecation warnings are from the minima base theme — not errors, not our problem to fix.

**GitHub Pages constraints:** Only whitelisted Jekyll plugins. We use `jekyll-feed` (whitelisted). No `_plugins/` directory. All custom code goes in `_layouts/`, `_includes/`, `_sass/`, `assets/`, `_data/` — all standard and supported. Third-party JS (Leaflet.js etc.) loads from CDN with integrity hashes — no installation needed.

---

## Deployment workflow

All work is pushed to **Pavani's fork** (`origin: github.com/pavaniasn/vicharanashala-ai`).
The **live org site** (`vicharanashala.github.io/vicharanashala-ai`) only updates after a PR is raised from pavaniasn → vicharanashala and merged. This is intentional.

**Standard process every session:**
1. Validate SCSS before committing: `sass --no-source-map _sass/minima.scss /dev/null`
2. `git add` specific files (not `git add .`)
3. Commit with a clear message
4. `git push origin main` — always push after committing

**To check if custom CSS is live on fork:**
`curl -s https://pavaniasn.github.io/vicharanashala-ai/assets/main.css | grep "1a1a1a"`
If it returns output, CSS is compiling correctly.

---

## Design system

**Colors:**
- Dark / primary: `#1a1a1a`
- Background: `#f9f9f7`
- Mid background: `#efefec`
- Grey (text muted): `#767676`
- Border: `#e2e2de`
- Dark text on dark: `#f9f9f7`
- Brand orange (logo icon, faculty map pins): `#e48f38`
- Brand teal (logo icon, student map pins): `#42a6ac`

**Typography:** Inter (loaded via Google Fonts in head.html), 17px base, 1.72 line-height

**Max widths:** Home sections use `.home-inner` (900px). Page layout wrapper is 860px. Timeline is 680px.

**Key layout classes:**
- `.home-hero` — compact dark band (background `#1a1a1a`, padding 2.5rem/3rem)
- `.home-section.hs-light` — off-white section
- `.home-section.hs-mid` — grey section
- `.home-section.hs-dark` — dark section
- `.home-inner` — content constraint for home sections
- `.home-label` — small uppercase label above section headings
- Icons: Phosphor Icons (`ph ph-*`), loaded via CDN in head.html

**Logos:**
- `assets/images/vicharanashala-logo-dark.png` — dark background logo. Use `mix-blend-mode: lighten` only on dark backgrounds. CANNOT be used cleanly on light backgrounds without a transparent PNG. Pending: get transparent-background version from logo designer.
- `assets/images/iit-ropar-logo.png` — white square background, badge is circular.
- Both logos currently NOT in the header — to be placed manually once a transparent Vicharanashala PNG is available.

---

## Site structure

**Layouts:**
- `home.html` — used only for index.md. No `.wrapper` constraint. No footer (removed).
- `default.html` — base layout with `<main class="page-content"><div class="wrapper">`. No footer (removed). Use this for full-control inner pages.
- `page.html` — extends default, auto-generates `<h1>` from front matter `title:`. Use only for simple content pages.

**Footer:** Removed from all layouts. `footer.html` include still exists with IIT Ropar logo + LinkedIn if needed later.

**Navigation (hardcoded in `_includes/header.html`):**
- About → Our Story, Team
- Work → Products, Research, Lab Initiatives, National Initiatives
- Programmes → Events, Openings, Vichara Logs
- Contact (standalone)

`header_pages` in `_config.yml` is no longer used for rendering — nav is now hardcoded. Keep it for reference but it doesn't control the nav.

**Dropdown fix:** `.dropdown-content` must have `top: 100%` and `z-index: 1000` to prevent clipping into browser bar. Already set — do not remove.

**Pages built:**
- `index.md` — Home: compact dark hero (tagline + CTA + stats), Start Here, Vision, Challenges, What We Built, How We Work, Testimonials (placeholder), Events strip
- `ourstory.md` — Our Story: intro hero, lab space section (photo placeholder), reach map (Leaflet.js), timeline
- `products.md` — 8-product grid + research narrative
- `lab_initiatives.md` — Summership, Global Speaker Series, V-Talks
- `national_initiatives.md` — GuruSetu, CBPAI
- `openings.md` — Courses, coming-soon, intern interest, positions
- `research_publications.md` — placeholder structure
- `team-members.md` — team page
- `vichara_logs.md` — Vi-Chintan live, Vi-Prayoga and Vi-Reports coming
- `contact.md` — address, email (dled@iitrpr.ac.in), phone, LinkedIn
- `events.md` — Google Calendar embed (placeholder ID needs replacing)
- `for_students.md`, `for_faculty.md`, `for_partners.md` — audience landing pages

---

## Reach map (`ourstory.md`)

Built with **Leaflet.js** (CDN, no API key, fully GitHub Pages compatible).
Basemap: CARTO light (clean, minimal).

**Data file:** `_data/reach_cities.yml`
- Each entry: `city`, `state`, `lat`, `lng`, `type` (faculty / student / both)
- 150+ faculty cities loaded from CBPAI FDP cohorts 1–16 (Google Sheet)
- Student cities: not yet added — waiting on data from Pavani
- **To add a city:** edit `_data/reach_cities.yml` directly on GitHub — no code knowledge needed

**Pin colours:**
- Faculty: orange `#e48f38`
- Students: teal `#42a6ac`
- Both: purple `#8a5ab7`

---

## Content pending (needs Pavani's input, do not invent)

- **Lab space photo** (`ourstory.md`) — placeholder exists, drop real photo in `assets/images/`
- **Testimonials** (`index.md`) — 3 placeholder cards, needs real student/faculty quotes
- **Events calendar** (`events.md`) — replace `REPLACE_WITH_CALENDAR_ID` with real Google Calendar ID, set calendar to public
- **Openings form links** (`openings.md`) — Register/Interest buttons need real form URLs
- **Vi-Prayoga and Vi-Reports** (`vichara_logs.md`) — sections exist, content coming
- **Research Publications** (`research_publications.md`) — needs domain framing + real papers
- **Student cities for reach map** — add to `_data/reach_cities.yml` with `type: student`
- **Transparent logo PNG** — needed to place Vicharanashala logo cleanly in the light header
- **Video links** — Frame.io videos to be uploaded to YouTube, then embedded via `_includes/youtube.html`
- **Vi-Sakha** — removed from products.md (superseded by Samagama).
- **Team page** — ops team bios needed for Atul, Harshdeep, Meenakshi Kalotra, Rajan Gupta. Roles for last 3 are placeholder — confirm with Pavani. All cards have photo placeholders; photos go in `assets/images/team/`.
- **Team LinkedIn links** — Sudarshan: sudarshan-iyengar-3560b8145, Pavani: pavani-ayinampudi, Prakash: prakash-hegade-16879917, Rohit: imrohitvk — all live.
- **Year recap video** — `Year_Recap_2.mp4` (72MB, local at `/Users/pavania/Downloads/Lab Footage/`). Upload to YouTube, share URL here. Goes on homepage between "How We Work" and Testimonials sections.

---

## Writing voice

- Conversational but substantive — not corporate, not academic-dry
- Use rhetorical questions to engage
- Positive framing — what the lab does, not what's wrong with the system
- India-specific policy context where relevant (NEP, UGC, ARPIT, NPTEL etc.)
- Avoid audit/checklist/declarative language ("we have X", "we do Y")
- Do NOT invent lab names, product names, or acronyms — use only established ones
- If suggesting content, label it clearly as a suggestion for Pavani to review

---

## What NOT to do

- Do not run `bundle exec jekyll build` or `bundle install`
- Do not add `layout: page` to pages that need full layout control — use `layout: default` instead
- Do not push to upstream (the org repo) — only push to `origin` (the fork)
- Do not commit binary files or `assets/images/` unless they are new logos/images being added
- Do not invent content (quotes, lab details, team names) — ask Pavani instead
- Do not add `parent:` front matter to pages for nav grouping — nav is now hardcoded in header.html
- Do not remove `top: 100%` or `z-index: 1000` from `.dropdown-content` — fixes browser bar clipping bug
- Do not suggest data-in-page solutions for anything that needs future editing — always use `_data/` files so non-technical editors can update via GitHub browser

---

## Proactive reminders (read before starting any feature)

- Pavani is non-technical — always recommend the most maintainable approach upfront, not after being asked
- Before finishing any feature that stores data or content, ask: "Who updates this later, and can they do it without touching code?"
- If building something with editable data (lists, locations, quotes, links), default to `_data/` YAML files
- If adding third-party libraries, use CDN with integrity hash — no npm, no installation
