# Geyang Dai personal site guide

This site uses the al-folio Jekyll template and is deployed by GitHub Actions.
Edit content on the `main` branch. Do not edit the `gh-pages` branch directly,
because it is generated automatically.

## Daily workflow

```bash
cd /Users/daigeyang/Desktop/随便写写/geyang_dai.github.io
git pull origin main
# edit files
git status
git add <changed-files>
git commit -m "Describe the change"
git push origin main
```

After pushing to `main`, GitHub Actions builds the site and updates `gh-pages`.
The public site is:

```txt
https://geyangdai.github.io/
```

## What to edit

### Homepage

Edit:

```txt
_pages/about.md
```

This controls the first page at `https://geyangdai.github.io/`.
The top `--- ... ---` block is front matter. It controls title, subtitle,
profile photo, contact info, and whether sections like news/posts/publications
are shown.

The text below the front matter is regular Markdown. You can write paragraphs,
lists, links, and LaTeX math there.

### Name, URL, theme settings

Edit:

```txt
_config.yml
```

Important settings for this repository:

```yaml
url: https://geyangdai.github.io
baseurl:
```

For a user homepage repo named `geyangdai.github.io`, `baseurl` must stay empty.

### Social links

Edit:

```txt
_data/socials.yml
```

This controls email, Google Scholar, GitHub, ORCID, RSS, and other icons.

### Publications

Edit:

```txt
_bibliography/papers.bib
```

Add publications as BibTeX entries. To feature a paper on the homepage, include:

```bibtex
selected={true}
```

### CV page

Edit one of these, depending on which format you prefer:

```txt
_data/cv.yml
assets/json/resume.json
```

The template can render CV information from structured data. If you prefer a
PDF-only CV, replace:

```txt
assets/pdf/example_pdf.pdf
```

with your real CV PDF and update links in `_data/socials.yml` or `_pages/cv.md`.

### News

Edit or add files in:

```txt
_news/
```

Each file is a small announcement. Good for talks, preprints, awards, visits,
or teaching updates.

### Blog posts

Add Markdown files in:

```txt
_posts/
```

File name format:

```txt
YYYY-MM-DD-title.md
```

Each post needs front matter, for example:

```markdown
---
layout: post
title: "A note on heat kernels"
date: 2026-05-27
description: "Short notes on Gaussian estimates"
tags: analysis pde probability
categories: math
---

Write the post here.
```

### Projects / research topics

Edit or add files in:

```txt
_projects/
```

For a math PhD site, this section can be repurposed as research topics,
lecture notes, reading groups, or expository projects.

### Images and PDFs

Put images in:

```txt
assets/img/
```

Put PDFs in:

```txt
assets/pdf/
```

The profile photo currently uses:

```txt
assets/img/prof_pic.jpg
```

## Writing LaTeX math

MathJax is enabled in `_config.yml`:

```yaml
enable_math: true
```

Inline math:

```markdown
The heat equation is \( \partial_t u - \Delta u = 0 \).
```

Display math:

```markdown
$$
\partial_t u - \Delta u = f,\qquad u(0,x)=u_0(x).
$$
```

Align-style equations:

```markdown
$$
\begin{aligned}
\frac{d}{dt}\int_\Omega \frac{|u|^2}{2}\,dx
&= \int_\Omega u\,\partial_t u\,dx \\
&= -\int_\Omega |\nabla u|^2\,dx.
\end{aligned}
$$
```

For TikZ examples, see:

```txt
_posts/2023-12-12-tikzjax.md
```

## Local preview

Your Mac system Ruby is too old for this project. The template expects the
Ruby/Bundler setup used in GitHub Actions, so local preview needs either Docker
or a modern Ruby environment.

### Option A: Docker, easiest after Docker is installed

Install Docker Desktop, then run:

```bash
cd /Users/daigeyang/Desktop/随便写写/geyang_dai.github.io
docker compose pull
docker compose up
```

Open:

```txt
http://localhost:8080
```

Stop the server with `Ctrl+C`.

### Option B: Ruby with rbenv

Install a modern Ruby, matching the GitHub Actions workflow:

```bash
brew install rbenv ruby-build
rbenv install 3.3.5
rbenv local 3.3.5
gem install bundler
bundle install
bundle exec jekyll serve
```

Open:

```txt
http://127.0.0.1:4000
```

If the site does not rebuild after config changes, stop and rerun:

```bash
bundle exec jekyll serve
```

## Upload and deploy

After editing:

```bash
git status
git add _pages/about.md _bibliography/papers.bib _data/socials.yml
git commit -m "Update homepage content"
git push origin main
```

GitHub Actions will build the site. Check:

```txt
https://github.com/GeyangDai/geyangdai.github.io/actions
```

The generated site is served from the `gh-pages` branch. Do not edit that branch.

## AI agent notes

This template includes agent guidance:

```txt
AGENTS.md
.github/agents/customize.agent.md
.github/agents/docs.agent.md
.agents/skills/al-folio-bootstrap/SKILL.md
.agents/skills/al-folio-v1-migration/SKILL.md
```

Use the customization agent for site content tasks such as:

- updating the homepage;
- adding publications;
- editing social links;
- creating posts or research pages;
- removing template demo pages.

The important boundary: this repository should contain your site content and
configuration. Avoid editing generated files or plugin-owned internals unless
there is a specific reason.

## Good first cleanup tasks

The template still contains demo content. Recommended next edits:

- replace `assets/img/prof_pic.jpg` with your real photo;
- update `_data/socials.yml`;
- replace `_bibliography/papers.bib` demo papers with your papers;
- remove or rewrite demo posts in `_posts/`;
- update `_news/` with your real announcements;
- decide whether to keep `projects`, `repositories`, `teaching`, and `people`.
