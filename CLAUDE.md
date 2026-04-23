# CLAUDE.md — Instructions for Continuing This Project

This file tells Claude (and future collaborators) exactly what this project is, where things stand, and how to continue editing it in VS Code with Claude Code or Claude's chat interface.

## What This Project Is

A **static multi-page courses website** for Prof. Aaron Snowberger, who teaches computer science at five Korean universities (one per weekday):

| Day | University | Korean |
|---|---|---|
| Monday | Korea Transportation University | 교통대학교 |
| Tuesday | Wonkwang University | 원광대학교 |
| Wednesday | Jeonbuk University (am) | 전북대학교 |
| Wednesday | Hanbat University (pm) | 한밭대학교 |
| Thursday | Jeonbuk University | 전북대학교 |
| Friday | Jeonju National University of Education | 전주교육대학교 |

## Current State (as of last Claude session)

All six pages are complete and functional:

| File | Status | Notes |
|---|---|---|
| `index.html` | ✅ Complete | Today pill, announcements, uni groups, filters, lab CTA |
| `archive.html` | ✅ Complete | Semester/uni sort, thumbnails, topic filters |
| `policies.html` | ✅ Complete | Featured cards + full list + FAQ accordion |
| `policy-ai.html` | ✅ Complete | Full individual policy page with sidebar |
| `course.html` | ✅ Complete | Course template with schedule, grading, textbooks |
| `office-hours.html` | ✅ Complete | Weekly schedule, contact cards, Cal.com mock |

## Active TODOs / Next Steps

### High priority
- [ ] Fill in real course data (replace all placeholder CS-XXXX courses)
- [ ] Fill in real KakaoTalk / Google Classroom / GitHub Classroom links
- [ ] Add real profile image (via Cloudinary URL)
- [ ] Connect GitHub notes fetch to real repo path

### Medium priority
- [ ] Build out individual course pages for each of the 9 current courses
- [ ] Add more individual policy pages (policy-grading.html, policy-exams.html, etc.)
- [ ] Add real publication/lab data to the PAI Lab CTA section
- [ ] Consider adding a `sitemap.html` or `sitemap.xml` for SEO

### Low priority / nice to have
- [ ] Add ORCID, ResearchGate, or LinkedIn links to footer
- [ ] Consider light-mode refinement pass (test all pages in light mode)
- [ ] Add `<meta>` SEO tags to all pages
- [ ] Consider print stylesheet for policies pages

## Architecture Decisions (already made — don't change without reason)

1. **Pure static HTML** — no framework, no build step. All CSS/JS is inline in each file.
2. **Shared CSS** is stored in `parts/css.txt` during build sessions. When editing manually in VS Code, each file is self-contained.
3. **No external CSS files** — everything inline so pages work when opened directly as files.
4. **Fonts from Google Fonts CDN** — Playfair Display, DM Serif Display, IBM Plex Mono, DM Sans.
5. **Dark mode default** — `data-theme="dark"` on `<html>`, toggled via localStorage.
6. **EN/KO language toggle** — index.html has full `i18n` system via `T` object. Other pages have Korean inline but no full toggle yet.
7. **Click dropdowns** — NOT hover. Hover was explicitly rejected by the user.
8. **Hamburger is an overlay** (position:fixed) — NOT push-down. Uses `#mobile-backdrop`.

## Key CSS Classes Reference

```
.today-pill          — Teal pill with pulsing dot, shows today's campus
.uni-group           — Groups cards by university on homepage
.uni-badge           — Faded logo in upper-right of all cards/rows
.course-grid         — Auto-fill grid, 2-col when .thumbs-active
a.card               — Full-card anchor with gradient top border
.filter-panel        — Collapsible filter section (opens on .open)
.sched-row           — Schedule row: date | 16:9 thumb | info | hw
.grade-track         — Horizontal grading thermometer bar
.prereq-box          — Prerequisites box (blue tint)
.dropcap             — First-letter dropcap (Playfair, var(--text) color)
.book-cover-col      — Fixed-width image column, images right-aligned
.announce-item       — Homepage announcement row
.today-pill.noclass  — Weekend/no-class state (muted dot)
```

## Color Usage Guide (maintain these ratios)

```
~50% purple (--accent)  — Primary headings, main CTAs, active pills
~35% blue   (--accent2) — Secondary buttons, link metadata, filters
~15% teal   (--accent3) — Card borders, status indicators, code labels
         warn (#fbbf24) — HW due dates, warning announcements  
         error (#fb6f84) — Holiday dates, error states
```

## Editing in VS Code

### With Claude Code (recommended)
```bash
npm install -g @anthropic-ai/claude-code
claude
```
Then in the chat, paste the CLAUDE.md file and say "Continue building this site."

### Without Claude Code
Open the project folder in VS Code, open any `.html` file, and use the Claude sidebar extension or paste code into claude.ai with context from this file.

### Useful VS Code extensions for this project
- **Live Preview** (ms-vscode.live-server) — preview pages without a server
- **HTML CSS Support** (ecmel.vscode-html-css) — CSS class autocomplete
- **Auto Rename Tag** (formulahendry.auto-rename-tag) — sync HTML tags
- **Prettier** — format HTML/CSS on save

## Multi-Site Architecture

This is the **courses site** only. Related sites (built with Claude and deployed):

| Site | Purpose | Recommended Stack | URL |
|---|---|---|---|
| **PAI Lab site** | Research, publications, conference info | Astro on Vercel | [pailab.io](http://pailab.io) |
| **Contact site** | CV, bio, full contact info | Jekyll on GitHub pages | [aaronsnowberger.com](https://aaronsnowberger.com) or [press.aaron.kr](https://press.aaron.kr) |
| **Personal blog** | Writing, notes | Nextjs front for WP back | [aaron.kr](https://aaron.kr) (front), [notes.aaron.kr](https://notes.aaron.kr) (back) |

**Profile image strategy:** Host canonical image at Cloudinary. Use same URL in all sites. Update once → all sites reflect it instantly.

## How to Add a New Semester

1. **index.html**: Change `section.section-label` text and add/update uni-group cards
2. **archive.html**: Move current courses from Spring XXXX to archived (change `.is-current` class to none, add new semester group at top)
3. Update the "Today at" school schedule JS object if campus schedule changes

## Notes on Korean Text

- All Korean text uses HTML entities (&#xXXXX;) in the Python build scripts but actual UTF-8 in the final HTML files
- Korean university names are used both in full (연세대학교) and abbreviated (연세, YU) throughout
- Bilingual labels use `&mdash;` separator: `Room / 강의실`
- The 상대평가 / 절대평가 distinction (relative vs absolute grading) is important in Korean universities

## Session History

Let's keep this and update it continuously as we go along.

This project was built iteratively in multiple Claude sessions:
1. Session 1: Initial courses.html with dark theme, dot-grid background
2. Session 2: Multi-page site with nav, dropdowns, policies, archive
3. Session 3: Complete redesign — new color palette, animated mesh bg, all 6 pages
4. Session 4 (current): Bug fixes — course layout, colors, box shadows, hamburger overlay, announcements, README

## Asking Claude to Continue

Good prompts for continuation:
- "Here's my CLAUDE.md. Continue building this site. Today I want to [specific task]."
- "Based on CLAUDE.md, create a new course page for CS 3310."
- "Based on CLAUDE.md, add a new policy page for the exam policy."
- "Fix [specific issue] in [file]. Here is the current HTML: [paste relevant section]"
