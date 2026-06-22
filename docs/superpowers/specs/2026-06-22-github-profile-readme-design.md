# GitHub Profile README Design Spec

## Overview

Minimal, card-layout GitHub profile README for `teslamint/teslamint`.

- **Audience**: Recruiters + developer community (general purpose)
- **Role**: Backend developer (Python, Java/Spring)
- **Tone**: Clean and minimal
- **Language**: English

## Structure

### 1. Greeting & Introduction

Short greeting + 2-3 line self-introduction.

- Name: Jaehoon You
- Role: Backend developer
- Mention primary tech: Python, Java/Spring
- No excessive emoji; one paragraph max

### 2. Tech Stack

shields.io badges grouped by category, 8-12 badges total.

| Category | Items |
|----------|-------|
| Languages | Python, Java |
| Frameworks | Spring Boot |
| Databases | PostgreSQL |
| Infrastructure | Docker, Redis |

Badge style: `flat-square` for minimal look.

### 3. Featured Projects

2-3 pinned/representative projects as linked cards.

Per project:
- Repository name with link
- One-line description
- Tech badges

Use placeholder slots if specific projects are not yet decided.

### 4. GitHub Stats

Two cards side by side using [github-readme-stats](https://github.com/anuraghazra/github-readme-stats):

- **GitHub Stats card**: commits, PRs, issues, stars
- **Top Languages card**: language usage ratio

Theme: `default` or transparent background to match minimal tone.

## Constraints

- No banner image
- Minimal emoji usage
- No WakaTime or extra widgets
- Keep total README under ~60 lines of rendered content
- All external images served via well-known services (shields.io, github-readme-stats)

## Out of Scope

- Blog post automation (github-readme-blog-posts-action)
- Visitor counter badges
- Animated SVGs or custom header images
- Multi-language toggle
