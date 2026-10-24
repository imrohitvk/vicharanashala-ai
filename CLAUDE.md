# Vicharanashala Website — Claude Instructions

This file is shared by everyone who works on the website with Claude. Keep it about the project, not about any one
person's machine, fork or habits. Personal setup (your fork name, your local paths, your own commit rules) goes in
your own `~/.claude/CLAUDE.md` or in a `CLAUDE.local.md` at the repo root (git-ignored and never published).

## What this is
Jekyll site for Vicharanashala (VLED Lab, IIT Ropar) — a lab for education design and EdTech.
- Live site: `https://vicharanashala.ai` (custom domain, set by the `CNAME` file)
- Main repo: `https://github.com/vicharanashala/vicharanashala-ai` (branch `main`); GitHub Pages builds the live site from it

Three audiences: students, faculty, government/funders.

---

## Technical setup — read before touching anything

**SCSS check (works without any Jekyll install):** `sass --no-source-map _sass/minima.scss /dev/null`
Pre-existing `@import` and `darken()`/`lighten()` deprecation warnings are from the minima base theme — not errors, not our problem to fix.

**Local preview is optional.** If you have a working Ruby + Jekyll setup, `jekyll serve` (or `bundle exec jekyll serve`) from the repo root previews the site at `http://127.0.0.1:4000/`. It is not required: GitHub Pages builds the site after a merge. GitHub Pages uses Jekyll 3.x (the `github-pages` gem in the `Gemfile`); a local Jekyll 4 build can differ slightly, so check the live site after merging. Build output (`_site/`) and `Gemfile.lock` are git-ignored; never commit them.

**GitHub Pages constraints:** Only whitelisted Jekyll plugins. We use `jekyll-feed` (whitelisted). No `_plugins/` directory. All custom code goes in `_layouts/`, `_includes/`, `_sass/`, `assets/`, `_data/` — all standard and supported. Third-party JS (Leaflet.js etc.) loads from CDN with integrity hashes — no installation needed.

---

## Contribution workflow

Several people contribute, each from their own fork. The live site only changes when a pull request into
`vicharanashala/vicharanashala-ai` `main` is merged. This is intentional.

1. Start from the latest `main` of the main repo (sync your fork first) and work on a branch.
2. Keep each change small and focused; say in the PR which pages it touches.
3. Run the SCSS check if you changed any styles.
4. `git add` specific files (not `git add .`), commit with a clear message.
5. Push the branch to your fork and open a PR into `vicharanashala/vicharanashala-ai` `main`.

Follow the contributor's own instructions on when to commit or push; Claude should not commit or push unless the
person it is working with asks.

**To check the live CSS after a merge:**
`curl -s https://vicharanashala.ai/assets/main.css | grep "1a1a1a"`
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
- The header (`_includes/header.html`) shows `assets/images/iit-ropar-logo.png` and the brand icon `assets/images/vicharanashala-icon.svg`.
- `assets/images/vicharanashala-logo-dark.png` — dark background logo. Use `mix-blend-mode: lighten` only on dark backgrounds. CANNOT be used cleanly on light backgrounds without a transparent PNG.
- `assets/images/iit-ropar-logo.png` — white square background, badge is circular.

---

## Site structure

**Repository layout:**
- Root keeps only what Jekyll/GitHub needs: `_config.yml`, `index.md` (homepage), `CNAME` (custom domain, must stay at root), `Gemfile`, `LICENSE`, `README.md`, `CLAUDE.md`.
- `pages/` — every inner page (Our Story, Team, Events, …). Each has a fixed `permalink:` in its front matter, so the folder never shows up in the URL. A new page goes here and MUST set `permalink:`.
- `docs/` — team how-to notes and the changelog. Not published.
- `exclude:` in `_config.yml` keeps `README.md`, `CLAUDE.md`, `CLAUDE.local.md`, `LICENSE`, `docs/` (and the Jekyll defaults) off the live site. It replaces Jekyll's built-in list, so keep the default entries in it. Any new non-website file at the root must be added there, or it will be published.

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
- `pages/ourstory.md` — Our Story: intro hero, lab space section (photo placeholder), reach map (Leaflet.js), timeline
- `pages/products.md` — 8-product grid + research narrative
- `pages/lab_initiatives.md` — Summership, Global Speaker Series, V-Talks
- `pages/national_initiatives.md` — GuruSetu, CBPAI
- `pages/openings.md` — Courses, coming-soon, intern interest, positions
- `pages/research_publications.md` — papers and datasets, driven by `_data/papers.yml` and `_data/datasets.yml`
- `pages/team-members.md` — team page
- `pages/vichara_logs.md` — Vi-Chintan live, Vi-Prayoga and Vi-Reports coming
- `pages/contact.md` — address, email (dled@iitrpr.ac.in), phone, LinkedIn
- `pages/events.md` — upcoming-event cards + on-site month calendar, driven by `_data/events.yml`
- `pages/for_students.md`, `pages/for_faculty.md`, `pages/for_partners.md` — audience landing pages
- `ict/` — standalone course pages for HB302 ICT in Education (unlisted, not in the nav)

---

## Reach map (`pages/ourstory.md`)

Built with **Leaflet.js** (CDN, no API key, fully GitHub Pages compatible).
Basemap: CARTO light (clean, minimal).

**Data file:** `_data/reach_cities.yml`
- Each entry: `city`, `state`, `lat`, `lng`, `type` (faculty / student / both)
- 150+ faculty cities loaded from CBPAI FDP cohorts 1–16 (Google Sheet)
- Student cities: not yet added — waiting on data from the website lead
- **To add a city:** edit `_data/reach_cities.yml` directly on GitHub — no code knowledge needed

**Pin colours:**
- Faculty: orange `#e48f38`
- Students: teal `#42a6ac`
- Both: purple `#8a5ab7`

---

## Content pending (needs the website lead's input, do not invent)

The website lead (currently Pavani) owns the content. This list may be out of date: check the page before acting on an item.

- **Lab space photo** (`pages/ourstory.md`) — placeholder exists, drop real photo in `assets/images/`
- **Testimonials** (`index.md`) — 3 placeholder cards, needs real student/faculty quotes
- **Openings form links** (`pages/openings.md`) — Register/Interest buttons need real form URLs
- **Vi-Reports** (`pages/vichara_logs.md`) — section exists, content coming
- **Vi-Prayoga** — LIVE from 11 Sep 2026. Articles are one markdown file each in `_prayoga/` (layout `prayoga-article`), listed automatically on `_logs/vi-prayoga.md`. How to add one: `docs/README-VI-PRAYOGA.md`. Article 1: *The Poll That Became a Classroom Experiment* (Pavani, 28 Jun 2026).
- **Team photos** — since 11 Sep 2026 each card uses `{% include team-photo.html name="…" %}`, which shows `assets/images/team/<name>.jpg` if it exists. Names follow the full-name pattern already used by the uploads (`s-r-s-iyengar`, `jinal-gupta`, `pavani-ayinampudi`…). Team members add their own photo by PR, no code: `docs/README-TEAM-PHOTOS.md`. `krishna-gelra`, `mudit-agrawal`, `s-hamsalekha` photos exist but have no card yet — roles to confirm with the website lead before adding.
- **Research Publications** (`pages/research_publications.md`) — needs domain framing + real papers
- **Student cities for reach map** — add to `_data/reach_cities.yml` with `type: student`
- **Transparent logo PNG** — needed to place the full Vicharanashala logo cleanly on light backgrounds
- **Video links** — Frame.io videos to be uploaded to YouTube, then embedded via `_includes/youtube.html`
- **Vi-Sakha** — removed from pages/products.md (superseded by Samagama).
- **Team page** — ops team bios needed for Atul, Harshdeep, Meenakshi Kalotra, Rajan Gupta. Roles for last 3 are placeholder — confirm with the website lead. All cards have photo placeholders; photos go in `assets/images/team/`.
- **Team LinkedIn links** — Sudarshan: sudarshan-iyengar-3560b8145, Pavani: pavani-ayinampudi, Prakash: prakash-hegade-16879917, Rohit: imrohitvk — all live.
- **Year recap video** — `Year_Recap_2.mp4` (72MB, held by the website lead). Upload to YouTube, share URL here. Goes on homepage between "How We Work" and Testimonials sections.

---

## Writing voice

- Conversational but substantive — not corporate, not academic-dry
- Use rhetorical questions to engage
- Positive framing — what the lab does, not what's wrong with the system
- India-specific policy context where relevant (NEP, UGC, ARPIT, NPTEL etc.)
- Avoid audit/checklist/declarative language ("we have X", "we do Y")
- Do NOT invent lab names, product names, or acronyms — use only established ones
- If suggesting content, label it clearly as a suggestion for the website lead to review

---

## What NOT to do

- Do not add `layout: page` to pages that need full layout control — use `layout: default` instead
- Do not push directly to the main repo's `main` — changes go in through a PR from your fork
- Do not commit binary files or `assets/images/` unless they are new logos/images being added
- Do not invent content (quotes, lab details, team names) — ask the website lead instead
- Do not add `parent:` front matter to pages for nav grouping — nav is now hardcoded in header.html
- Do not remove `top: 100%` or `z-index: 1000` from `.dropdown-content` — fixes browser bar clipping bug
- Do not suggest data-in-page solutions for anything that needs future editing — always use `_data/` files so non-technical editors can update via GitHub browser
- Do not put a new page at the root or leave out its `permalink:` — new pages go in `pages/` with a `permalink:`

---

## Proactive reminders (read before starting any feature)

- Content editors are non-technical and edit through the GitHub browser — always recommend the most maintainable approach upfront, not after being asked
- Before finishing any feature that stores data or content, ask: "Who updates this later, and can they do it without touching code?"
- If building something with editable data (lists, locations, quotes, links), default to `_data/` YAML files
- If adding third-party libraries, use CDN with integrity hash — no npm, no installation
