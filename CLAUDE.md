# CLAUDE.md — Instructions for Continuing This Project

This file tells Claude (and future collaborators) exactly what this project is, where things stand, and how to continue editing it.

## What This Project Is

A **Jekyll-based courses website** for Prof. Aaron Snowberger, who teaches computer science at five Korean universities (one per weekday):

| Day | University | Korean | Abbr |
|---|---|---|---|
| Monday | Korea Transportation University | 교통대학교 | UT |
| Tuesday | Wonkwang University | 원광대학교 | WKU |
| Wednesday AM | Jeonbuk University | 전북대학교 | JBNU |
| Wednesday PM | Hanbat University | 한밭대학교 | HB |
| Thursday | Jeonbuk University | 전북대학교 | JBNU |
| Friday | Jeonju National University of Education | 전주교육대학교 | JNUE |

## Architecture Overview

This is a **Jekyll site** targeting **GitHub Pages** (simple push-to-deploy, no Docker, no custom build). It was converted from a static HTML prototype (`index.html`, `course.html`, etc.) in April 2026.

### Directory Structure

```
claude-courses/
├── _config.yml              # Minimal Jekyll config (GitHub Pages compatible)
├── Gemfile                  # github-pages gem
├── .gitignore
│
├── _layouts/
│   ├── default.html         # Base layout: nav + footer + shared JS
│   ├── course.html          # Course detail page (extends default)
│   └── page.html            # Generic content page (extends default)
│
├── _includes/
│   ├── head.html            # <head> meta/fonts/CSS
│   ├── nav.html             # Sticky nav with dropdowns (auto-built from site.courses)
│   ├── footer.html          # Footer
│   ├── schedule.html        # Flex-row schedule renderer (uses site.data[data_file])
│   ├── textbooks.html       # Textbook list from page front matter
│   ├── about_aaron.html     # Instructor bio box (uses _data/staff.yml)
│   ├── course_card.html     # Card component for course listings
│   ├── course_scripts.html  # Sidebar intersection-observer JS (course pages only)
│   └── policies.md          # *** SHARED POLICIES CONTENT *** (single source of truth)
│
├── _sass/
│   ├── main.scss            # Import manifest
│   ├── _variables.scss      # Color & layout variables
│   ├── _base.scss           # Body, typography, footer, mesh background
│   ├── _nav.scss            # Navigation
│   ├── _components.scss     # Pills, buttons, cards, tags, filters, today-pill
│   ├── _home.scss           # Homepage hero, stats-bar, announcements, uni-groups
│   ├── _course.scss         # Course hero, grading bar, textbooks, instructor
│   └── _schedule.scss       # Schedule flex rows
│
├── assets/
│   └── css/
│       └── main.scss        # Jekyll SCSS entry point (front matter + @import "main")
│
├── _pages/
│   ├── archive.md           # /archive/ — all courses by semester
│   ├── policies.md          # /policies/ — full policies page
│   └── office-hours.md      # /office-hours/ — campus schedule + contact
│
├── index.md                 # / — homepage (current courses + today pill)
│
├── _courses/
│   ├── 2026/
│   │   ├── ut-iot.md        # IoT — Korea Transportation Univ
│   │   ├── ut-db.md         # Database Design — Korea Transportation Univ
│   │   ├── wku-php.md       # PHP — Wonkwang University
│   │   ├── hb-cpp.md        # C++ — Hanbat University
│   │   ├── jbnu-pe.md       # Power Electronics — Jeonbuk Univ
│   │   ├── jbnu-dc.md       # Circuit Theory (DC) — Jeonbuk Univ
│   │   ├── jbnu-devs.md     # Device Analysis — Jeonbuk Univ
│   │   └── jnue-iss.md      # Info Society & Software — JNUE (3 sections)
│   ├── 2025/                # (to be migrated from aaronkr-courses.github.io)
│   ├── 2024/
│   └── 2023/
│
└── _data/
    ├── staff.yml            # Instructor info
    ├── 2026_hb_cpp_lectures.yml
    ├── 2026_jbnu_dc_lectures.yml
    ├── 2026_jbnu_devs_lectures.yml
    ├── 2026_jbnu_pe_lectures.yml
    ├── 2026_jnue_iss_lectures.yml
    ├── 2026_ut_db_lectures.yml
    ├── 2026_ut_iot_lectures.yml
    └── 2026_wku_php_lectures.yml
    (+ 2025, 2024, 2023 data files to be added)
```

## Current State (as of Session 7 — April 2026)

| Component | Status | Notes |
|---|---|---|
| Jekyll scaffolding | ✅ Complete | Gemfile, _config.yml, .gitignore |
| SCSS design system | ✅ Complete | 7 partials extracted from HTML prototype |
| Layouts | ✅ Complete | default, course, page |
| Includes | ✅ Complete | All 9 includes including shared policies |
| Home page | ✅ Complete | Today pill, stats bar, course grid by semester, announcements |
| Archive page | ✅ Complete | All semesters, auto-built from collections |
| Policies page | ✅ Complete | Uses shared `_includes/policies.md` |
| Office Hours page | ✅ Complete | Campus schedule + contact |
| Announcements | ✅ Complete | `_data/announcements.yml` → homepage conditional section |
| 2026 courses | ✅ Complete | All 8 courses in `_courses/2026/` |
| 2026 data files | ✅ Complete | All 8 `_data/2026_*_lectures.yml` files |
| 2025 courses | ✅ Complete | 14 courses in `_courses/2025/` (7 spring + 7 fall) |
| 2025 data files | ✅ Complete | 14 `_data/2025_*_lectures.yml` files |
| 2024 courses | ✅ Complete | 13 courses in `_courses/2024/` (6 spring + 7 fall) |
| 2024 data files | ✅ Complete | 13 `_data/2024_*_lectures.yml` files |
| 2023 courses | ✅ Complete | 7 courses in `_courses/2023/` (all redirect to external sites) |
| Special/Online courses | ✅ Complete | 5 courses in `_courses/special/` (iksan 2021, hs-python/web 2023, eduonix) |
| Special data files | ✅ Complete | `_data/2021/iksan_gg_lectures.yml` (nested year subdirectory) |
| AI Policy page | ✅ Complete | `_pages/policy-ai.md` at `/policies/ai/`; linked from nav + policies page |
| Assets (images) | ⏳ Pending | Must be copied from `../aaronkr-courses.github.io/assets/` |
| i18n / lang toggle | ⏳ Partial | `data-en`/`data-ko` attrs exist; full toggle not wired |

## Active TODOs / Next Steps

### Required to go live
- [ ] **Copy assets** from `../aaronkr-courses.github.io/assets/img/` to `./assets/img/`
- [ ] **Test Jekyll build** locally: `bundle install && bundle exec jekyll serve`
- [ ] **Set GitHub Pages source** to root `/` (not `/docs`)

### Next sessions
- [ ] Wire up full i18n toggle (data-en / data-ko attributes on all nav/page elements)
- [ ] Add a 404.html page
- [ ] Add `favicon` from Cloudinary

### Later / Nice to have
- [ ] Add `sitemap.xml` (auto via jekyll-sitemap plugin)
- [ ] Add SEO meta tags (auto via jekyll-seo-tag plugin)
- [ ] Consider merging `_courses` MD + `_data` YAML into single per-course file for simpler maintenance

## Architecture Decisions (do not change without reason)

1. **Jekyll + GitHub Pages** — Simple push-to-deploy. No Docker, no custom GitHub Actions build. Uses only GitHub Pages-compatible plugins.
2. **SCSS via Jekyll** — All CSS in `_sass/` partials, compiled by Jekyll. No separate CSS build step.
3. **Collections** — `_courses/` is a Jekyll collection. `permalink: /courses/:path/` gives year-based URLs automatically (e.g. `/courses/2026/hb-cpp/`).
4. **Nested `_data/`** — Lecture data files live in `_data/YYYY/school_subject_lectures.yml` (e.g. `_data/2026/hb_cpp_lectures.yml`). Course front matter uses `data_file: 2026/hb_cpp_lectures`. The `schedule.html` include splits on `/` to access `site.data["2026"]["hb_cpp_lectures"]`. Non-year data (staff, announcements) stays in `_data/` root.
5. **Shared policies** — `_includes/policies.md` is the single source of truth for all shared policy text. Course pages use `{% include policies.md %}`. Never duplicate this content in course files.
6. **Grading bar** — Grading percentages are in a structured `grading:` block in each course's front matter. The `course.html` layout generates the thermometer bar from this data.
7. **Dark mode default** — `data-theme="dark"` on `<html>`, toggled via localStorage. Same as HTML prototype.
8. **Click dropdowns** — NOT hover. Hover was explicitly rejected in earlier sessions.
9. **Hamburger is an overlay** — `position: fixed`, NOT push-down. Uses `#mobile-backdrop`.

## Design System

### Color palette (CSS custom properties)
```scss
--accent:  #9b65ff  /* Purple — primary CTAs, headings */
--accent2: #7eb8f7  /* Blue   — secondary buttons, metadata */
--accent3: #6dccdd  /* Teal   — card borders, status */
--warn:    #fbbf24  /* Amber  — HW due dates, warnings */
--error:   #fb6f84  /* Pink   — holidays, errors */
```

### Typography
- `IBM Plex Mono` — nav brand, code labels, badges, metadata
- `Playfair Display` / `DM Serif Display` — h1, stat numbers
- `DM Sans` — body text (weight 300)

### Color usage ratio (maintain)
- ~50% purple (`--accent`) — primary headings, main CTAs
- ~35% blue (`--accent2`) — secondary buttons, links
- ~15% teal (`--accent3`) — card borders, status indicators

## Data File Format (`_data/YYYY/school_subject_lectures.yml`)

```yaml
- date: 3/4           # Date string (M/D format)
  week: 1             # Week number
  title: >            # HTML-safe title
    <strong>수업 소개</strong>
  readings: "Book, Chapter 1"  # String (not array)
  hw: "https://classroom.github.com/..."
  slides: "https://docs.google.com/..."
  img: 2024/hb-cpp/1-cpp-intro.jpg   # Relative to /assets/img/
  logistics: >        # Optional logistics HTML
    <a href="...">Link</a>

# No-class row (holiday/test):
- date: 4/22
  week: 8
  title: >
    <strong>Midterm Test</strong>
```

## Course Front Matter Format (`_courses/YEAR/school-subject.md`)

```yaml
---
layout: course
title: Course Title
subtitle: 한국어 부제목        # optional
description: SECTION_CODE • YYYY년 N학기 • 대학교이름
logo: school-logo.png         # filename in /assets/img/
img: assets/img/books/book.jpg
importance: 1                 # sort order (lower = higher priority)
category: 2026-1              # YYYY-N (semester key)
now: Yes                      # omit or "No" for past courses
data_file: 2026_ut_iot_lectures  # key into site.data

grading:
  attendance: 10
  midterm: 25
  final: 25
  homework: 25
  project: 15

information:
  - section: 442213
    time: 월 123 | Mon 9am-12pm
    location: W18동 214호
    kakaotalk: https://open.kakao.com/...

Main-Text:
  - text: "주교재"
    author: "Author Name"
    title: <strong>Book Title</strong>
    publisher: "Publisher | Date"
    link: "https://..."
    image: books/book.jpg

Supplementary:
  - text: "부교재"
    # ... same fields
---

[Markdown body = Overview/description content only]
```

## How to Add a New Semester

1. Create `_courses/YYYY/` directory
2. Add course files following the format above
3. Add data files to `_data/` as `YYYY_school_subject_lectures.yml`
4. Add the new category to `course_categories` in `_config.yml`
5. The nav, homepage, and archive will automatically include the new courses

## How to Run Locally

```bash
cd claude-courses
bundle install
bundle exec jekyll serve --livereload
# → http://localhost:4000
```

## Assets Note

Book/logo images are NOT currently in this repo. Copy them from the existing Jekyll site:

```bash
cp -r ../aaronkr-courses.github.io/assets/img/ ./assets/img/
```

## Old Static HTML Files

The original prototype HTML files (`index.html`, `course.html`, `archive.html`, `policies.html`, `policy.html`, `office-hours.html`, `courses.html`) remain in the repo root for reference. They are excluded from Jekyll processing because they have no front matter (except they may conflict with compiled output). **Safe to delete** once the Jekyll site is confirmed working. They are preserved in git history.

## Session History

1. Session 1: Initial `courses.html` with dark theme, dot-grid background
2. Session 2: Multi-page static site with nav, dropdowns, policies, archive
3. Session 3: Complete redesign — new color palette, animated mesh bg, all 6 pages
4. Session 4: Bug fixes — course layout, colors, box shadows, hamburger overlay, announcements, README
5. Session 5 (current): **Complete Jekyll conversion** — new architecture, all 2026 courses migrated, shared policies, SCSS system
