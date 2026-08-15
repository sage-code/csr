# Computer Science Research

CSR Is a Sage-Code project for learning Computer Science. It contains basic information about Software Engineering & Programming. We focus on Julia language for explaining Algorithms and Data Structures (DSA). This project is highly experimental. We use AI to generate content. Join on your own risk.

## Computer Science Research

Computer Science Research (CSR) is a Sage-Code learning site covering software engineering, programming, algorithms, data structures, databases, platforms, and web development. It is built with [Hugo](https://gohugo.io/) and the Learn theme.

The published site is available at [sage-csr.vercel.app](https://sage-csr.vercel.app).

## Prerequisites

Install the **extended** edition of Hugo. This project uses theme assets that require the extended edition.

### Windows

With Windows Package Manager:

```powershell
winget install Hugo.Hugo.Extended
```

Alternatively, install the extended release from [Hugo releases](https://github.com/gohugoio/hugo/releases), then add its directory to your `PATH`.

Confirm the installation:

```powershell
hugo version
```

The output should include `extended`. Git is recommended for obtaining and contributing changes. No Node.js packages are required; `package.json` is intentionally empty.

## Run Locally

Clone the repository, then open its root directory in a terminal:

```powershell
git clone https://github.com/sage-code/csr.git
Set-Location csr
```

Start Hugo's development server:

```powershell
hugo server --buildDrafts
```

Open the local address displayed by Hugo, normally `http://localhost:1313/`. Hugo watches the project and reloads the site after edits.

Build the production site before sharing or deploying a change:

```powershell
hugo build
```

The generated static site is written to `public/`. Treat this directory as build output: edit the source files instead, then rebuild.

## Content Maintenance

All learning material lives in `content/`. Folders form the site hierarchy, and each folder's `_index.md` controls its section landing page. For example, `content/algorithms/sorting.md` becomes the Sorting article in the Algorithms section.

### Edit An Article

1. Edit the article's Markdown file under `content/`.
2. Keep the front matter between the opening and closing `+++` markers. At minimum, preserve a meaningful `title` and `weight`.
3. Write article content in Markdown. Use headings in order (`##`, then `###`) so the table of contents remains useful.
4. Run `hugo build` and check the rendered page locally with `hugo server --buildDrafts`.

The most useful front matter fields are:

```toml
+++
title = "Article title"
date = 2026-08-15T00:00:00Z
weight = 10
menuTitle = "Short navigation title"
disableToc = false
hidden = false
+++
```

`weight` controls order within a section; lower values appear first. Set `hidden = true` for work that should not appear in navigation. Use `draft = true` while an article is incomplete; preview it with `hugo server --buildDrafts`.

### Add An Article Or Section

Create an article from the repository root:

```powershell
hugo new content/algorithms/new-topic.md
```

Hugo uses `archetypes/default.md` to create the initial front matter. Replace its placeholder text, choose an appropriate `weight`, and build the site to verify the navigation order.

For a new top-level section, create a folder under `content/`, add an `_index.md` with its title and weight, then add articles beneath it. The `_index.md` pages are also where section introductions and navigation behavior belong.

### Site Configuration And Assets

- Update site-wide settings, menu shortcuts, and theme parameters in `hugo.toml`.
- Put custom styles, scripts, fonts, and images in `static/`; Hugo publishes them at the same relative path.
- Layout overrides live in `layouts/`. Change these only when altering the shared site presentation.
- Translation strings are in `i18n/`.

## Contribution Checklist

Before opening a pull request or deploying content:

1. Check titles, heading hierarchy, links, code examples, and factual claims.
2. Ensure new pages have sensible `weight` values and appear in the intended section.
3. Run `hugo build` with no build errors.
4. Preview the changed pages locally and check desktop and mobile navigation.

AI may assist with drafting, but contributors remain responsible for technical accuracy, clear explanations, and appropriate attribution.

---

Copyright (c) 2024 Sage-Code Laboratory.

This repository contains [Hugo](https://gohugo.io/), based project.
We also use "Learn" theme for this project. [Visit the documentation](https://learn.netlify.com/en/)
We use Gemini, Claude and ChatGPT equaly to create content.

## Contribution

* Join our Discord server and become a mentor or developer.
* Stay active, contribute with new articles, provide feedback.
* Promote your own content, blog articles or quizes you create.

## Distribution

Visit live distribution here: [sage-csr](https://sage-csr.vercel.app)

---
Copyright (c) 2024 Sage-Code Laboratory.