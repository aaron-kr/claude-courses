# Aaron Snowberger — Courses Site

A **Jekyll site** for Prof. Aaron Snowberger's teaching portfolio across five Korean universities. Hosted on GitHub Pages at [aaronkr-courses.github.io](https://aaronkr-courses.github.io).

## Quick Start

```bash
bundle install
bundle exec jekyll serve --livereload
# → http://localhost:4000
```

**First run:** Copy images from the existing Jekyll site:
```bash
cp -r ../aaronkr-courses.github.io/assets/img/ ./assets/img/
```

## Site Map

| URL | File | Description |
|---|---|---|
| `/` | `index.md` | Homepage — today pill, current courses |
| `/courses/2026/ut-iot/` | `_courses/2026/ut-iot.md` | IoT course (UT) |
| `/courses/2026/ut-db/` | `_courses/2026/ut-db.md` | Database Design (UT) |
| `/courses/2026/wku-php/` | `_courses/2026/wku-php.md` | PHP (WKU) |
| `/courses/2026/hb-cpp/` | `_courses/2026/hb-cpp.md` | C++ (HB) |
| `/courses/2026/jbnu-pe/` | `_courses/2026/jbnu-pe.md` | Power Electronics (JBNU) |
| `/courses/2026/jbnu-dc/` | `_courses/2026/jbnu-dc.md` | Circuit Theory DC (JBNU) |
| `/courses/2026/jbnu-devs/` | `_courses/2026/jbnu-devs.md` | Device Analysis (JBNU) |
| `/courses/2026/jnue-iss/` | `_courses/2026/jnue-iss.md` | Info Society & Software (JNUE) |
| `/archive/` | `_pages/archive.md` | All courses by semester |
| `/policies/` | `_pages/policies.md` | Shared academic policies |
| `/office-hours/` | `_pages/office-hours.md` | Campus schedule + contact |

## Design System

### Colors
```css
--accent:  #9b65ff   /* Purple — primary CTAs, headings */
--accent2: #7eb8f7   /* Blue   — secondary buttons */
--accent3: #6dccdd   /* Teal   — card borders, status */
--warn:    #fbbf24   /* Amber  — HW, warnings */
--error:   #fb6f84   /* Pink   — holidays */
```

### Fonts
- `IBM Plex Mono` — nav brand, code labels, badges
- `Playfair Display` — headings, stat numbers
- `DM Sans` — body text (weight 300)

## Key Files

| File | Purpose |
|---|---|
| `_includes/policies.md` | **Single source of truth** for all shared academic policies |
| `_includes/schedule.html` | Renders schedule from `_data/YYYY_*_lectures.yml` |
| `_includes/course_card.html` | Card component used on home/archive pages |
| `_sass/_variables.scss` | All color & layout variables |
| `_config.yml` | Site settings + course category display order |

## Adding a New Course

1. Create `_courses/YYYY/school-subject.md` with proper front matter
2. Create `_data/YYYY_school_subject_lectures.yml` with week-by-week schedule
3. Done — the nav, homepage, and archive will automatically include it

### Minimal course front matter:
```yaml
---
layout: course
title: Course Title
subtitle: 한국어 부제목
description: SECTION_CODE • YYYY년 N학기 • 대학교이름
logo: school-logo.png
importance: 1
category: 2026-1
now: Yes
data_file: 2026_ut_example_lectures

grading:
  attendance: 10
  midterm: 25
  final: 25
  homework: 25
  project: 15

information:
  - section: 123456
    time: Mon 9am-12pm
    location: Building 101
    kakaotalk: https://open.kakao.com/...

Main-Text:
  - text: "주교재"
    author: "Author"
    title: <strong>Book Title</strong>
    publisher: "Publisher | Year"
    link: "https://..."
    image: books/book.jpg
---
[Overview markdown here]
```

## Adding a New Semester

1. Add to `course_categories` in `_config.yml`
2. Create `_courses/YYYY/` directory
3. Add course files (see above)
4. Add data files to `_data/`

## Multi-Site Architecture

| Site | Stack | URL |
|---|---|---|
| **Courses** (this site) | Jekyll on GitHub Pages | [aaronkr-courses.github.io](https://aaronkr-courses.github.io) |
| **Research / Lab** | Astro on Vercel | [pailab.io](https://pailab.io) |
| **Contact / CV** | Jekyll on GitHub Pages | [aaronsnowberger.com](https://aaronsnowberger.com) |
| **Personal blog** | Next.js + WordPress | [aaron.kr](https://aaron.kr) |

**Profile image:** Host at Cloudinary. Same URL across all sites.
