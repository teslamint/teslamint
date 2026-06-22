# GitHub Profile README Design Spec

## Overview

Minimal, card-layout GitHub profile README for `teslamint/teslamint`.

- **Audience**: Recruiters + developer community (general purpose)
- **Role**: Backend developer (Python, FastAPI, MySQL)
- **Tone**: Clean and minimal
- **Language**: English

## Structure

### 1. Greeting & Introduction

Short greeting + 2-3 line self-introduction.

- Name: Jaehoon You
- Role: Backend developer
- Mention primary tech: Python, FastAPI
- No excessive emoji; one paragraph max
- Copy should be concrete about *what you build*, not just list tech names
  - Avoid: "I'm a backend developer who loves Python"
  - Prefer: "I build [what you actually make] with Python and FastAPI"

### 2. Tech Stack

shields.io badges grouped by category, 6-10 badges total.

| Category | Items |
|----------|-------|
| Languages | Python |
| Frameworks | FastAPI |
| Databases | MySQL |
| Infrastructure | Docker, Redis |

Badge style: `flat-square` for minimal look.

All badges use a **unified palette** (see Dark Mode & Palette section) instead of default brand colors.

### 3. Featured Projects

2-3 pinned/representative projects using [github-readme-stats repo pin cards](https://github.com/anuraghazra/github-readme-stats#github-extra-pins).

Per project:
- Repo pin card with link
- Auto-populated description and language from GitHub

Pin cards share the same unified palette as stats cards for visual consistency.

Use placeholder slots if specific projects are not yet decided.

### 4. GitHub Stats

Two cards side by side using [github-readme-stats](https://github.com/anuraghazra/github-readme-stats):

- **GitHub Stats card**: commits, PRs, issues, stars
- **Top Languages card**: language usage ratio

Cards use the unified palette (see Dark Mode & Palette section).

## Dark Mode & Palette

### Unified Palette

A single cohesive color palette applied across all badges + stats cards + repo pin cards. This prevents the "random brand colors" look of default badges.

| Element | Light Mode | Dark Mode |
|---------|-----------|----------|
| Badge background | `#2b2d30` | `#e8e8e8` |
| Badge text | `#ffffff` | `#1a1a1a` |
| Stats title color | `#2b2d30` | `#e8e8e8` |
| Stats icon color | `#4a7c59` | `#6db87d` |
| Stats text color | `#434343` | `#c9c9c9` |
| Stats bg color | `transparent` | `transparent` |

Exact values are adjustable; the key constraint is **one palette across all visual elements**.

### Dark Mode Rendering

GitHub supports `<picture>` with `media="(prefers-color-scheme: dark)"` for theme-adaptive images.

All externally-rendered images (stats cards, repo pins) must provide light and dark variants:

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="...dark-params...">
  <img src="...light-params..." />
</picture>
```

Badges also need light/dark variants via the same mechanism.

## Constraints

- No banner image
- Minimal emoji usage
- No WakaTime or extra widgets
- Keep total README under ~60 lines of rendered content
- All external images served via well-known services (shields.io, github-readme-stats)
- Final verification must be done on GitHub (push + check both light/dark mode)

## Out of Scope

- Blog post automation (github-readme-blog-posts-action)
- Visitor counter badges
- Animated SVGs or custom header images
- Multi-language toggle
