# Portfolio Website — Claude Instructions

## Owner
- Full name: **Mathasith Piboonsilp**
- Nickname: Bio
- Initials: MP (used in nav logo as `[MP]`)

## Project Overview
Personal portfolio website built with plain HTML, CSS, and vanilla JavaScript. No frameworks, no build tools. All 5 pages are built — currently in the content-filling stage.

## Tech Stack
- HTML5, CSS3, Vanilla JavaScript
- FontAwesome 6.5 (CDN)
- Google Fonts: Poppins (headings), Inter (body) — both via CDN
- No React, Vue, jQuery, Webpack, Vite, or any other library

## File & Folder Structure (current)
```
portfolioWebsite/
├── CLAUDE.md                    ← Claude instructions (this file)
├── PROJECT_SPEC.md              ← design tokens, content placeholders, page status
├── index.html                   ← Home page (root — must stay here)
├── html/                        ← All inner pages live here
│   ├── experience.html
│   ├── self-development.html
│   ├── awards.html
│   └── leadership.html
├── css/
│   ├── style.css                ← Shared styles (variables, nav, cards, footer, buttons)
│   ├── home.css                 ← index.html only
│   ├── experience.css           ← html/experience.html only
│   ├── self-development.css     ← html/self-development.html only
│   ├── awards.css               ← html/awards.html only
│   └── leadership.css           ← html/leadership.html only
├── js/
│   └── main.js                  ← Shared JS (mobile nav, active link, filter, scroll-reveal)
└── images/
    └── (user-supplied photos)
```

## Path Rules (critical — do not break these)
- `index.html` links to inner pages as `html/pagename.html`
- Inner pages (`html/*.html`) link back to home as `../index.html`
- Inner pages link to each other as `pagename.html` (same folder, no prefix)
- Inner pages reference CSS as `../css/filename.css`
- Inner pages reference JS as `../js/main.js`
- `index.html` references CSS as `css/filename.css` and JS as `js/main.js`

## CSS Architecture
Each page has exactly two stylesheet links in `<head>`:
1. `style.css` — shared base (always first)
2. `[page].css` — page-specific overrides (always second)

Never put styles in a `<style>` tag inside HTML. All styles go in the CSS files.

## Design Tokens (defined in css/style.css as CSS variables)
| Variable       | Value     | Usage                  |
|----------------|-----------|------------------------|
| --primary      | #2563EB   | Blue — main accent     |
| --primary-dark | #1D4ED8   | Hover state for primary|
| --accent       | #10B981   | Green — secondary accent|
| --bg           | #0F172A   | Page background        |
| --surface      | #1E293B   | Card / nav background  |
| --surface-2    | #263147   | Tech pill background   |
| --text         | #F1F5F9   | Primary text           |
| --text-muted   | #94A3B8   | Secondary / muted text |
| --border       | #334155   | Border color           |
| --radius       | 12px      | Card border radius     |
| --radius-sm    | 8px       | Small border radius    |
| --nav-height   | 68px      | Fixed nav height       |
| --max-w        | 1100px    | Max content width      |

## Category Tag Colors
| Category    | Class           | Color   |
|-------------|-----------------|---------|
| Production  | .tag-production | #2563EB |
| Competition | .tag-competition| #7C3AED |
| Academic    | .tag-academic   | #D97706 |
| Personal    | .tag-personal   | #10B981 |
| Open Source | .tag-opensource | #EC4899 |
| Cert        | .tag-cert       | #0891B2 |
| Workshop    | .tag-workshop   | #059669 |
| Award       | .tag-award      | #D97706 |
| Honor       | .tag-honor      | #7C3AED |
| Leadership  | .tag-leadership | #2563EB |
| Volunteer   | .tag-volunteer  | #10B981 |

## Shared Components (defined in style.css)
- `.navbar` — fixed top nav with mobile hamburger
- `.card` + `.card-grid` — base card and auto-fill grid
- `.filter-bar` + `.filter-btn` — category filter buttons (experience page)
- `.btn`, `.btn-primary`, `.btn-outline` — button variants
- `.section` — standard section padding
- `.section-title`, `.section-divider`, `.section-subtitle` — section headings
- `.page-hero` — inner page hero banner
- `.footer` — shared footer with socials

## Page Status
| File                        | Status    | Notes                              |
|-----------------------------|-----------|------------------------------------|
| index.html                  | Built     | Needs real content filled in       |
| html/experience.html        | Built     | Needs real project cards filled in |
| html/self-development.html  | Built     | Needs real certs/workshops filled  |
| html/awards.html            | Built     | Needs real awards filled in        |
| html/leadership.html        | Built     | Needs real events/skills filled in |
| css/style.css               | Complete  | Shared — do not add page styles    |
| css/home.css                | Complete  |                                    |
| css/experience.css          | Complete  |                                    |
| css/self-development.css    | Complete  |                                    |
| css/awards.css              | Complete  |                                    |
| css/leadership.css          | Complete  |                                    |
| js/main.js                  | Complete  | Shared — nav, filter, scroll reveal|

## Remaining Placeholders (still need real content)
All placeholders use `[bracket]` syntax. Things still to fill:
- Personal: tagline, title/role, email, GitHub URL, LinkedIn URL, CV PDF URL
- Profile photo: add `images/profile.jpg`, then swap placeholder div for `<img>`
- Experience: all 5 category cards (project name, role, description, learnings, tech, links)
- Self-Dev: all certification and workshop cards
- Awards: competition placements and honour/scholarship entries
- Leadership: event cards (add real photos to `images/`) and verify soft skills list
- Footer socials: GitHub URL, LinkedIn URL, email across all pages

## Workflow Rules
- Never put CSS inside a `<style>` tag in HTML — use the page CSS file
- Never add features not discussed without asking
- Placeholder content uses `[brackets]`
- Keep JS minimal — no libraries beyond what is already loaded
- When adding a new page, follow the same structure: two CSS links, shared nav, page-hero, sections, shared footer, year script, main.js
