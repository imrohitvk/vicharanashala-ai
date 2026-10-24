# Vicharanashala Website

[![Website](https://img.shields.io/website?url=https%3A%2F%2Fvicharanashala.ai&label=vicharanashala.ai)](https://vicharanashala.ai)
[![Built with Jekyll](https://img.shields.io/badge/built%20with-Jekyll-c00?logo=jekyll)](https://jekyllrb.com/)
[![Hosted on GitHub Pages](https://img.shields.io/badge/hosted%20on-GitHub%20Pages-222?logo=github)](https://pages.github.com/)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

The official website of **Vicharanashala**, the Lab for Education Design (VLED Lab) at IIT Ropar.

*Innovations that make learning feel human again.*

**Live site:** https://vicharanashala.ai

The site introduces the lab's products, research, initiatives and events to three audiences: students, faculty, and
government and funding partners.

---

## Contents

- [Tech stack](#tech-stack)
- [Repository structure](#repository-structure)
- [Editing content (no code needed)](#editing-content-no-code-needed)
- [Local development (optional)](#local-development-optional)
- [Contributing](#contributing)
- [Deployment](#deployment)
- [Conventions](#conventions)
- [Troubleshooting](#troubleshooting)
- [Contact](#contact)
- [License](#license)

---

## Tech stack

| Part | What we use |
|---|---|
| Site generator | [Jekyll](https://jekyllrb.com/) via GitHub Pages (`github-pages` gem, Jekyll 3.x) |
| Theme | [Minima](https://github.com/jekyll/minima) 2.5, heavily customised in `_sass/minima.scss` |
| Plugins | `jekyll-feed` only (GitHub Pages whitelist; no custom `_plugins/`) |
| Fonts and icons | Inter (Google Fonts), [Phosphor Icons](https://phosphoricons.com/) via CDN |
| Map | [Leaflet.js](https://leafletjs.com/) with CARTO light tiles via CDN |
| Hosting | GitHub Pages, custom domain `vicharanashala.ai` (`CNAME`) |

There is no npm, no build pipeline and no server code. Third-party libraries load from a CDN with integrity hashes.

---

## Repository structure

```
.
├── _config.yml          Site settings, collections and the exclude list
├── index.md             Homepage
├── pages/               All other pages (Our Story, Team, Products, Events, ...)
├── _data/               Editable content in YAML (events, papers, datasets, map, photos)
├── _projects/           Collection: one file per product   -> /projects/<slug>/
├── _initiatives/        Collection: one file per initiative -> /initiatives/<slug>/
├── _logs/               Collection: Vichara Logs sections   -> /logs/<slug>/
├── _prayoga/            Collection: Vi-Prayoga articles     -> /logs/vi-prayoga/<slug>/
├── _layouts/            Page templates (home, default, page, prayoga-article, ...)
├── _includes/           Reusable pieces (header, team photo, YouTube embed, ...)
├── _sass/               Styles (minima.scss holds the site's design system)
├── assets/              Images, JavaScript, map data, main stylesheet entry
├── ict/                 Standalone HB302 ICT in Education course pages (unlisted)
├── docs/                Team how-to guides and changelog (not published)
├── CNAME                Custom domain, must stay at the repository root
├── CLAUDE.md            Project notes for contributors using Claude (not published)
├── Gemfile              Ruby dependencies for GitHub Pages
└── LICENSE
```

Every file in `pages/` sets its own `permalink:`, so the folder name never appears in a URL
(`pages/events.md` is served at `/events/`).

---

## Editing content (no code needed)

Most updates only need a change to one YAML file, made directly in the GitHub web editor.

| To change | Edit | Notes |
|---|---|---|
| Events (upcoming list and calendar) | `_data/events.yml` | Field guide at the top of the file; posters go in `assets/images/events/` |
| Working papers on the Research page | `_data/papers.yml` | Add at the bottom; `arxiv` is the arXiv id only |
| Datasets on the Research page | `_data/datasets.yml` | Add at the bottom; leave out platforms a dataset is not on |
| Reach map on Our Story | `_data/reach_cities.yml` | `type` is `faculty`, `student` or `both` |
| "VLED in Action" photos | `_data/moments.yml` | Images go in `assets/images/moments/` |
| Team photos | upload to `assets/images/team/` | See [docs/README-TEAM-PHOTOS.md](docs/README-TEAM-PHOTOS.md) |
| Vi-Prayoga articles | add a file to `_prayoga/` | See [docs/README-VI-PRAYOGA.md](docs/README-VI-PRAYOGA.md) |

### Adding a new page

Create `pages/<name>.md` with front matter such as:

```yaml
---
layout: default        # or "page" for a simple page with an automatic <h1>
title: My New Page
permalink: /my-new-page/
---
```

The navigation menu is hardcoded in `_includes/header.html`, so add a link there if the page should appear in the menu.

---

## Local development (optional)

You do not need a local build to contribute: GitHub Pages builds the site after every merge. A local preview helps when
you change layouts or styles.

**Option A: match GitHub Pages** (needs a Ruby version supported by the `github-pages` gem, usually Ruby 3.x)

```bash
bundle install
bundle exec jekyll serve
```

**Option B: plain Jekyll** (works on newer Ruby versions; Jekyll 4, so output can differ slightly from production)

```bash
gem install jekyll jekyll-feed minima:2.5.2 webrick
JEKYLL_NO_BUNDLER_REQUIRE=true jekyll serve
```

Either way, open http://127.0.0.1:4000/. To run the SCSS check only (no Jekyll needed):

```bash
sass --no-source-map _sass/minima.scss /dev/null
```

The `@import` and `darken()`/`lighten()` deprecation warnings come from the Minima base theme and can be ignored.

---

## Contributing

1. Fork this repository and keep your fork's `main` in sync with this one.
2. Make your change. Keep it small and focused on one thing.
3. If you touched styles, run the SCSS check above.
4. Stage the specific files you changed (avoid `git add .`), commit with a clear message, and push to your fork.
5. Open a pull request into `vicharanashala/vicharanashala-ai` `main` and say which pages it affects.

The live site changes only when a pull request is merged.

---

## Deployment

- GitHub Pages builds and publishes the site from `main` of this repository.
- The custom domain comes from the `CNAME` file and `url: "https://vicharanashala.ai"`, `baseurl: ""` in `_config.yml`.
- The `exclude:` list in `_config.yml` keeps repository files (`README.md`, `CLAUDE.md`, `LICENSE`, `docs/`, ...)
  off the live site. Any new non-website file at the root must be added to it, or it will be published.
- After a merge, allow a minute or two for the build, then check the live page.

---

## Conventions

- Content that people will update later belongs in `_data/` YAML, not hardcoded in a page.
- Use `layout: default` for pages that need full layout control, `layout: page` for simple text pages.
- Only GitHub Pages whitelisted plugins; no `_plugins/` folder.
- Third-party JavaScript from a CDN with an integrity hash; no npm.
- Do not commit build output (`_site/`) or `Gemfile.lock`; both are git-ignored.
- Colours, typography and layout classes are documented in [CLAUDE.md](CLAUDE.md#design-system).

---

## Troubleshooting

**My fork's GitHub Pages preview looks wrong and its links break.**
This is expected. With `baseurl: ""` (needed for the custom domain), styles, images and menu links point to the root of
the domain, so on `<user>.github.io/vicharanashala-ai/` they resolve to the wrong place. Use a local preview to check
how pages look, and do not change `baseurl`, as that would break the live site.

**A page shows the wrong URL or a 404 after moving it.**
Check that its front matter still has the correct `permalink:`.

**A new file at the root shows up on the live site.**
Add it to the `exclude:` list in `_config.yml`.

---

## Contact

- Vicharanashala, Lab for Education Design, IIT Ropar
- Email: [dled@iitrpr.ac.in](mailto:dled@iitrpr.ac.in)
- LinkedIn: [vicharanashala](https://www.linkedin.com/company/vicharanashala)

For questions about the website content, contact the website team through the email above or open an issue.

---

## License

Released under the [MIT License](LICENSE).
