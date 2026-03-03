# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a bilingual (English/Chinese) personal blog called "Baby Shark Blog" built with [Hugo](https://gohugo.io/) and the [lightbi-hugo](https://github.com/binokochumolvarghese/lightbi-hugo) theme (included as a git submodule).

Deployed to Netlify at: https://babyshark33.netlify.app/

## Development Commands

```bash
# Start local dev server
hugo server

# Build the site
hugo

# Start dev server with drafts
hugo server -D
```

## Architecture

- **hugo.toml** — Main site configuration (languages, menus, theme params)
- **content/en/** — English content
- **content/zh-cn/** — Chinese content
- **themes/lightbi-hugo/** — Theme (git submodule, do not edit directly)
- **layouts/partials/** — Custom partial overrides (`head_custom.html`, `footer_custom.html`)
- **assets/img/** — Site images
- **archetypes/default.md** — Template for new content

### Content Sections

Each language directory mirrors the same structure:
- `post/` — Blog posts (main content)
- `notes/` — Short notes
- `collections/` — Curated collections
- `about/` — About page

### Content Front Matter Format

Posts use YAML front matter:
```yaml
---
title: "Post Title"
date: YYYY-MM-DD
tags: ["tag1", "tag2"]
image: "/img/image-name.png"
Description: "Post description"
---
```

### Bilingual Setup

English content lives in `content/en/` (`languages.en`) and Chinese content in `content/zh-cn/` (`languages.zh-cn`).
