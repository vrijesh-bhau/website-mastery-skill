# Not Gaming Playz Manager — The Antigle

**Purpose:** Dedicated maintainer skill for The Antigle gaming website by Mukund.

---

## Project Overview

| Property | Value |
|---|---|
| **Site Name** | The Antigle — Gaming by Mukund |
| **Creator** | Mukund (Not Gaming Playz) |
| **Location** | `G:\Welcome\projects\Not-Gaming-PLayz-main` |
| **Tech Stack** | Pure HTML5, CSS3, Vanilla JS (ES6+) |
| **Fonts** | Rajdhani (headings) + Inter (body) via Google Fonts |
| **Pages** | Home, Videos, Resources, Updates, About (5 pages) |
| **Content** | 36 videos, 9 resources, 3 updates (JSON-driven) |

---

## Feature Inventory (Total: 38)

### 26 Original Features (NEVER break these)
1. Fixed glassmorphism navbar
2. Hamburger mobile menu
3. Dark/Light theme toggle
4. Hero section with gradient text
5. Category cards (3)
6. Featured video (latest public)
7. Latest updates on home (3)
8. Videos page with filter/search
9. YouTube modal player
10. Resources page with filter/search
11. Download buttons (file + external)
12. Read-more toggle on descriptions
13. 3-dot context menu (copy link, share, report)
14. Updates page with post modal
15. About page (bio, story, contact)
16. Creator support / UPI donation
17. Smart Guard (private video detection)
18. Highlight Guard (shared link animation)
19. Donation Guard (emotional pre-download)
20. Creeper Easter Egg (logo click)
21. Cloudflare router
22. SEO (meta, OG tags)
23. Accessibility (ARIA, focus, skip link)
24. Session caching for JSON
25. Lazy loading images
26. Reduced motion support

### 12 Upgrade Features (v2.4.0 — additive, never remove)
27. Recently Added "NEW" badges (30-day window)
28. Latest Resources section on home (horizontal scroll)
29. Creator Picks section on home (horizontal scroll)
30. Related Content in video modals (tag-based scoring)
31. Loading skeleton shimmer placeholders
32. Search on Updates page
33. Keyboard shortcuts (`?` help, `/` search, `t` theme)
34. Scroll progress bar (gradient below navbar)
35. Scroll-to-top floating button
36. Footer stats (dynamic video/resource/update counts)
37. Premium support creator card (UPI copy, toggle details)
38. Version display in footer (`v2.4.0`)

---

## Architecture

```
project-root/
├── index.html                 → Home
├── videos.html                → Videos
├── resources.html             → Resources
├── updates.html               → Updates
├── about.html                 → About
├── assets/
│   ├── css/style.css          → Stylesheet (1,780 lines)
│   ├── js/main.js             → Core JS (1,888 lines)
│   ├── js/cloudflare-router.js
│   ├── js/donation-guard.js
│   ├── js/highlight.js
│   └── js/smart-guard.js
├── content/
│   ├── videos/index.json      → 36 video entries
│   ├── resources/index.json   → 9 resource entries
│   └── updates/index.json     → 3 update entries
└── assets/files/              → Downloadable resources
```

---

## Update Guidelines

### Adding New Content
- **Videos:** Edit `content/videos/index.json` — add entry with `id`, `title`, `description`, `category`, `thumbnail`, `youtube`, `date`, `tags`
- **Resources:** Edit `content/resources/index.json` — add entry with `id`, `title`, `description`, `category`, `thumbnail`, `file`/`external_link`, `download_type`, `youtube`, `date`, `tags`, `note`
- **Updates:** Edit `content/updates/index.json` — add entry with `id`, `title`, `date`, `summary`, `content`, `featured_image`

### Changing Creator Picks
Edit `CREATOR_PICKS` config in `assets/js/main.js:19-36`

### Changing "NEW" badge threshold
Edit `RECENT_DAYS` constant in `assets/js/main.js:41`

### Adding a new Upgrade Feature
1. Add CSS in `style.css` (append at end, mark with `/* UPGRADE MODULE */`)
2. Add JS in `main.js` (append at end, mark with `// UPGRADE MODULE`)
3. Wire up in `DOMContentLoaded` at bottom of main.js
4. NEVER modify existing code — only extend

---

## Critical Rules
1. NEVER delete existing features
2. NEVER remove existing code unless fixing a bug
3. ALL changes must be additive and backward compatible
4. Always verify: no console errors, mobile responsive, layout intact
5. Content JSON schema must remain backward compatible
