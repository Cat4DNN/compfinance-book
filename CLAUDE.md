# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is **Serge Youmbi's personal academic website** — a Zola-based static site showcasing research at the intersection of Category Theory, Deep Learning, and Computational Finance. Built on a customized AdiDoks theme.

**Sections:**
- **About** — Academic profile and background
- **Research** — Research areas and ongoing projects
- **Publications** — Academic papers and publications
- **Gallery** — Mathematical formulas and concept visualizations (KaTeX)
- **Blog** — Technical articles and tutorials
- **Contact** — Contact information and collaboration opportunities

## Commands

```bash
# Development server with live reload (http://127.0.0.1:1111/)
zola serve

# Build for production (outputs to ./public/)
zola build

# Validate content and links without building
zola check
```

**Requirement:** Zola ≥ 0.15.0 (CI uses 0.19.2)

## Architecture

### Template Hierarchy

All templates extend `templates/base.html`:

```
base.html
├── index.html (homepage)
├── page.html
├── section.html
├── taxonomy_list.html, taxonomy_single.html (tags)
├── about/section.html
├── research/section.html
├── publications/section.html
├── gallery/section.html
├── blog/section.html, blog/page.html
└── contact/section.html
```

**Macros** (`templates/macros/`):
- `head.html` — SEO, Open Graph, JSON-LD
- `header.html` — Navigation with active section highlighting
- `math.html` — KaTeX integration (enabled globally)

### Content Structure

Content uses TOML frontmatter (`+++` delimited):

```markdown
+++
title = "Post Title"
description = "Short description"
date = 2025-01-15T09:00:00+00:00
template = "blog/page.html"

[taxonomies]
tags = ["category-theory", "deep-learning"]

[extra]
lead = "Lead paragraph shown below title"
math = true
+++

Content with $\LaTeX$ math support...
```

### Styling

Sass compiles from `sass/`:

```
main.scss
├── bootstrap/scss/ (Bootstrap framework)
├── common/ (_variables.scss, _fonts.scss, _global.scss, _dark.scss)
├── components/ (_code.scss, _alerts.scss, _fintech.scss, _search.scss)
├── layouts/ (_header.scss, _footer.scss, _pages.scss, _sidebar.scss)
└── _custom.scss (site-specific customizations)
```

**Key custom styles** in `_custom.scss`:
- `.gradient-text` — Animated gradient text for hero sections
- `.about-page`, `.research-page`, `.publications-page`, `.contact-page` — Section-specific styling
- Dark mode support throughout

### Configuration (`config.toml`)

- `math = true` with `library = "katex"` — KaTeX enabled globally
- `build_search_index = true` — FlexSearch-based search
- `taxonomies = [{name = "tags"}]` — Blog post tagging
- Theme color: `#6366f1` (indigo primary)

### Deployment

GitHub Pages via `.github/workflows/deploy.yml`:
- Triggers on push to `main`
- Uses Zola 0.19.2
- Deploys to GitHub Pages

## Content Guidelines

- **Blog posts**: Use `[taxonomies] tags = [...]` for categorization
- **Math content**: Use KaTeX syntax — inline `$...$`, block `$$...$$`
- **Research/Publications**: Update content in respective `_index.md` files

## Conventions

- Follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages
- Math-heavy content should set `[extra] math = true` in frontmatter
