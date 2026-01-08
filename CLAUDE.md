# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a bilingual (English/German) Quarto documentation website for TUM ITO (IT Operations) system administrators. The site is deployed to GitHub Pages via automated workflow.

## Build Commands

```bash
# Preview website locally (auto-refreshes on changes)
quarto preview

# Render the HTML website
quarto render
```

## Architecture

### Directory Structure
- `_quarto.yml` - Main site configuration (navbar, sidebars, theme)
- `en/` - English content
- `de/` - German content
- `_site/` - Generated HTML output (gitignored)

### Content Organization
Both `en/` and `de/` have parallel chapter structures:
- `index.qmd` - Language introduction
- `chapters/01-*.qmd` through `chapters/08-*.qmd` - Topic chapters

### Deployment
GitHub Actions workflow (`.github/workflows/publish.yml`) runs on push to main:
1. Renders HTML website
2. Deploys to GitHub Pages

## Content Guidelines

- Content uses Mermaid diagrams for flowcharts and mindmaps
- Tables follow standard Quarto markdown format
- Callouts (`::: {.callout-tip}`, `::: {.callout-note}`) are used for important information
- Grid layouts (`::: {.grid}`) used for side-by-side content
- Keep English and German chapters in sync structurally
