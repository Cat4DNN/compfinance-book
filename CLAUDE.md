# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Handbook of Computational Finance** - A Zola static site for a finance book combining category theory with AI-driven approaches to quantitative finance. Built on the AdiDoks theme.

- **URL**: https://cat4dnn.github.io/compfinance-book
- **Author**: Serge Youmbi

## Commands

```bash
# Development server with live reload (http://127.0.0.1:1111/)
zola serve

# Build for production (outputs to ./public/)
zola build

# Validate content and links without building
zola check
```

**Requirement**: Zola ≥ 0.15.0 (CI uses 0.19.2)

## Architecture

### Content Structure

This project uses `chapters/` as the main documentation section (not `docs/`):

```
content/
├── _index.md           # Homepage with navigation menu and feature cards
├── chapters/           # Main book content (primary section)
│   ├── _index.md       # Chapter listing
│   ├── part-1/         # Mathematical foundations
│   └── part-2/         # Trading strategies
├── videos/             # Video tutorials
├── gallery/            # Visual content
├── author/             # Author profile
├── resources/          # External resources
└── blog/               # Blog posts
```

### Chapter Page Frontmatter

```markdown
+++
title = "Chapter Title"
description = "Brief description"
date = 2024-01-01T08:00:00+00:00
weight = 10                          # Controls ordering
template = "chapters/page.html"      # Must use chapters template

[extra]
lead = "Introduction paragraph"
toc = true                           # Enable table of contents
+++
```

### Template Hierarchy

```
templates/base.html                  # Root template
├── index.html                       # Homepage
├── chapters/page.html              # Individual chapter pages
├── chapters/section.html           # Chapter listing
├── videos/page.html, section.html  # Video content
├── gallery/section.html            # Image gallery
└── macros/                         # Reusable components
    ├── docs-sidebar.html           # Chapter navigation sidebar
    ├── math.html                   # KaTeX integration
    └── head.html                   # SEO, Open Graph, JSON-LD
```

### Key Configuration

Math is enabled globally (`config.toml`):
```toml
math = true
library = "katex"
```

Use LaTeX notation directly in markdown:
- Inline: `$\mathcal{C}$`
- Display: `$$F: \mathcal{C} \to \mathcal{D}$$`

### Styling

Edit `sass/_custom.scss` for project customizations. Bootstrap is included via `sass/bootstrap/`.

## Deployment

GitHub Pages via `.github/workflows/deploy.yml`:
- Triggers on push to `main` or manual dispatch
- Builds with Zola 0.19.2
- Deploys to `public/`

## Conventions

- Follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
- Chapter files use `weight` for ordering (lower = earlier)
- Code examples should include Python, Haskell, or Julia implementations
- Mathematical content uses KaTeX notation
