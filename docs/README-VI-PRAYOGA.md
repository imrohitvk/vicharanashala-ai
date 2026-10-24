# Adding an article to Vi-Prayoga

Each Vi-Prayoga article is **one text file** in the `_prayoga/` folder. The
Vi-Prayoga page lists every article automatically, newest first — nothing else
needs editing.

## 1. Create the file

In `_prayoga/`, add a new file named `YYYY-MM-DD-short-name.md`, for example
`2026-10-02-the-deadline-we-moved.md`. (The date at the front just keeps the
folder in order.)

## 2. Start it with this block, then paste the article underneath

```markdown
---
layout: prayoga-article
title: "Your Title Here"
slug: your-title-here
subtitle: "One line under the title, shown on the article and on the Vi-Prayoga page"
number: 2
author: Your Name
date: 2026-10-02
---

Your first paragraph.

## A section heading

Leave a blank line between paragraphs.
```

- `slug` becomes the web address: `/logs/vi-prayoga/your-title-here/`. Don't change
  it after you've shared the link.
- `number` is the article's place in the series (Vi-Prayoga 1, 2, 3…). Leave the
  line out if you don't want a number shown.
- Put `##` in front of a line to make it a section heading.

## 3. Commit, push, and raise a pull request

Same as any other change to this site (see `CLAUDE.md`). The article appears on
the fork first, and on the live lab site once the pull request is merged.
