# Aaron Snowberger — Courses Site

A multi-page static HTML/CSS/JS website for Prof. Aaron Snowberger's teaching portfolio across five Korean universities.

## Site Map

| File | URL | Description |
|---|---|---|
| `index.html` | `/` | Homepage — current semester courses grouped by university |
| `archive.html` | `/archive` | Complete course history (2023–present) |
| `policies.html` | `/policies` | All academic policies with FAQ accordion |
| `policy-ai.html` | `/policy-ai` | Full AI & ChatGPT use policy (individual policy template) |
| `course.html` | `/course` | Individual course page template (CS 4820 sample) |
| `office-hours.html` | `/office-hours` | Weekly campus schedule + Cal.com booking widget |

## Design System

### Colors
```css
/* Dark mode */
--accent:  #9b65ff   /* Purple — primary CTAs, headings, main accent */
--accent2: #7eb8f7   /* Blue   — secondary buttons, metadata */
--accent3: #6dccdd   /* Teal   — tert. accents, card borders, status */
--warn:    #fbbf24   /* Amber  — warnings, HW due dates */
--error:   #fb6f84   /* Pink   — holidays, errors */

/* Light mode swaps */
--accent:  #7c3aff
--accent2: #2563eb
--accent3: #0badbc
```

**Color mix target:** ~50% purple, ~35% blue, ~15% teal across the site.

### Typography
```
Headings:    Playfair Display (700, italic) / DM Serif Display (fallback)
Body:        DM Sans (300, 400, 500)
Monospace:   IBM Plex Mono (400, 500) — labels, code, badges
```

### Background
- Radial gradient orbs (fixed) — purple top-left, blue top-right, teal bottom
- Animated CSS mesh grid via `body::before` — `@keyframes meshWave` 22s loop
- No background images needed

### Component Patterns

**Sliding fill buttons** (all interactive elements):
```css
background: linear-gradient(to right, VAR_COLOR 50%, var(--tag-bg) 50%);
background-size: 205% 100%;
background-position: 100%;
transition: background-position .32s ease;
/* on hover: background-position: 0 */
```
Variants: `.pill` (purple), `.pill-blue`, `.pill-teal`, `.back-btn`, `.ql-btn`

**Today pill** (index + office-hours):
```html
<div class="today-pill" id="today-pill">
  <span class="today-dot"></span>
  <span id="today-text"></span>
</div>
```
JS populates based on `new Date().getDay()` → school schedule map.

**Uni badge** (cards + archive rows):
```html
<div class="uni-badge"><span class="ub-abbr">YU</span><span>연세</span></div>
```
Absolutely positioned top-right, 12% opacity, pointer-events:none.

**Card top border:**
```css
a.card::before { height: 2px; background: linear-gradient(90deg, accent3, accent, accent2); opacity: .55; }
a.card:hover::before { opacity: 1; }
```

## File Structure
```
/
├── index.html           — Homepage
├── archive.html         — Course archive
├── policies.html        — Policies hub
├── policy-ai.html       — Individual policy (template)
├── course.html          — Individual course (template)
├── office-hours.html    — OH + booking
└── README.md
```

## JavaScript Patterns

**Shared JS** (inlined in every page, from `parts/js.txt`):
- Theme toggle (`applyTheme`) — persists to `localStorage`
- Language toggle — currently triggers class `.lang-btn-all` swap only; full i18n on index.html only
- Dropdown menus — click-based, close-on-outside-click
- Hamburger overlay — fixed position, backdrop div (`#mobile-backdrop`), `body.overflow:hidden`
- Filter panel toggle (`#filter-toggle-btn` / `#filter-panel`)
- Thumbnail toggle (`#thumb-toggle` / `#thumb-section.thumbs-active`)

**Page-specific JS:**
- `index.html`: Today-at pill, school/topic/sort filters, GitHub notes fetch
- `archive.html`: Year/topic/sort/university filters + "By University" view
- `course.html`: IntersectionObserver sidebar active link tracking
- `policy-ai.html`: Same IntersectionObserver pattern
- `office-hours.html`: Today card highlight

## Updating Content

### Add a new course to index.html
1. Find the correct `<div class="uni-group" data-school="...">` section
2. Copy an existing `<a class="card">` block
3. Update: `href`, `data-title`, `data-tag`, `card-code`, `card-title`, `card-desc`, `card-tags`, time, room, `card-thumb` gradient, `uni-badge`

### Add a new announcement
```html
<a class="announce-item" href="LINK">
  <span class="ann-dot new|info|warn|teal"></span>
  <div class="ann-body">
    <div class="ann-title">Title</div>
    <div class="ann-desc">Description</div>
  </div>
  <div class="ann-meta">
    <span class="ann-date">Apr 21</span>
    <span class="ann-badge course|lab|admin">Label</span>
    <span class="ann-arrow">→</span>
  </div>
</a>
```

### Add a new policy page
1. Copy `policy-ai.html`
2. Update: title, code (POL-02 etc.), section IDs + sidebar links
3. Replace section content
4. Update related cards at bottom

### GitHub Notes (index.html)
Change the repo path in the `fetchNotes()` function:
```js
const r = await fetch('https://api.github.com/repos/AaronSnowberger/pai-lab/contents/notes');
```
Notes directory should contain `.md` files. Graceful fallback to hardcoded sample notes on failure.

### Profile image (Cloudinary)
```html
<!-- Use this URL pattern everywhere (all sites): -->
<img src="https://res.cloudinary.com/YOUR_CLOUD/image/upload/v1/profile/snowberger.jpg" />
```
Update once in Cloudinary → all sites update automatically.

## Deployment

Pure static HTML — drop files in any static host:
- **GitHub Pages**: push to `gh-pages` branch or `docs/` folder
- **Netlify / Vercel**: drag-and-drop folder or connect repo
- **Cloudflare Pages**: connect repo, no build command needed

No build step, no dependencies, no package.json required.

## Future Migration Path

When the site grows, consider migrating to:
1. **Hugo + Academic/PaperMod theme** — add YAML frontmatter to each course, templates auto-render
2. **Quarto** — great if you want to publish Jupyter notebooks alongside course pages
3. **Astro** — component islands, good for the PAI Lab site

The PAI Lab site should be a **separate Astro project** linked from this site.
