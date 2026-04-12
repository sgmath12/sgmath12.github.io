# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal GitHub Pages blog (sgmath12.github.io) for Seungju Cho, a PhD student at KAIST. It uses the [minima-reboot](https://github.com/aterenin/minima-reboot) Jekyll theme — a Bootstrap-based port of Jekyll's default Minima theme. The repo serves double duty: it IS the theme source (with `minima-reboot.gemspec`) and a live demo/personal blog.

## Commands

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve

# Build static site
bundle exec jekyll build
```

The site is served at `http://localhost:4000` by default.

## Architecture

**Jekyll site structure:**
- `_config.yml` — site configuration: title, author, plugins, navigation pages (`header_pages`), footer icons, pagination, and kramdown settings
- `_posts/` — blog posts in Markdown, named `YYYY-MM-DD-title.md`
- `_layouts/` — HTML templates; `post.html` includes MathJax for math rendering
- `_includes/` — reusable HTML fragments; `head-includes.html` is intentionally empty and is the hook for adding custom `<head>` content
- `_sass/` — SCSS styles; `minima-reboot/_layout.scss` handles layout tweaks and the CSS-only responsive nav
- `assets/main.scss` — entry point that imports `minima-reboot.scss`

**Key customizations in this repo:**
- MathJax is loaded via `_includes/mathjax.html` and included in `_layouts/post.html` for math typesetting in posts
- Navigation links: About, Posts, GitHub (configured via `header_pages` in `_config.yml`)
- GitHub footer icon linking to `sgmath12`
- `kramdown` with `parse_block_html: true` (allows HTML inside Markdown blocks)

## Writing Posts

Posts go in `_posts/` with front matter:
```yaml
---
layout: post
title: "Post Title"
date: YYYY-MM-DD
---
```

Math equations use MathJax syntax (`$$...$$` for display, `$...$` inline). Posts are written in both Korean and English.

## Plugins

- `jekyll-seo-tag` — SEO metadata
- `jekyll-paginate` — pagination on the home page (5 posts per page, set via `paginate` in `_config.yml`)
- `jekyll-feed` — RSS feed
- `jekyll-redirect-from` — URL redirects via front matter
