# 05 — Layouts & Information Architecture

## Grid Systems

### CSS Grid
The most powerful layout tool for modern web design.

**Key properties:**
```css
.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 24px;
}
```

**Common grid configurations:**
- 12-column — Most flexible, standard for complex layouts
- 6-column — Simplified, common in dashboards
- 4-column — Good for card grids
- 3-column — Trifold layouts, feature sections
- 2-column — Sidebar + content, split hero

### Flexbox
Best for one-dimensional layouts:
- Navigation bars (horizontal items)
- Card rows (wrapping items)
- Centering content
- Button groups
- Form layouts

### When to use Grid vs Flexbox

| Need | Use |
|------|-----|
| 2D layout (rows AND columns) | Grid |
| 1D alignment (row OR column) | Flexbox |
| Card grids | Grid (for alignment), Flex (for wrapping) |
| Navigation | Flexbox |
| Page-level layout | Grid |
| Component-level layout | Flexbox |
| Unknown number of items | Flexbox (with wrap) |
| Known number of items in rows | Grid |

## Visual Hierarchy Layouts

### F-Pattern Layout
Users scan in an F-shape: left-to-right top, then left-to-right lower, then down the left side.

**Best for:** Content-heavy pages, blogs, news, documentation
**Structure:**
- Important info in top-left and top row
- Secondary info in left column
- Less important content on right
- Key elements near top of page

**Implementation:**
```
[HEADLINE (full width)]
[---META---]  [---SIDEBAR---]
[BODY LEFT]   [SIDEBAR TOP  ]
[BODY LEFT]   [SIDEBAR BOTTOM]
[BODY LEFT]   [SIDEBAR BOTTOM]
```

### Z-Pattern Layout
Users scan in a Z-shape: top-left → top-right → bottom-left → bottom-right.

**Best for:** Landing pages, simple pages, calls-to-action
**Structure:**
- Logo top-left, CTA top-right
- Diagonal motion through content
- CTA bottom-right (final action point)

**Implementation:**
```
[LOGO]  [NAV]  [CTA]
[                    ]
[    VISUAL CONTENT   ]
[                    ]
[INFO]  [INFO]  [CTA]
```

### Bento Grid Layout
Irregular grid with cells of different sizes, like Japanese bento boxes.

**Best for:** Feature sections, dashboard overviews, portfolio highlights
**Structure:**
- 1-2 large cells (hero features, main content)
- 4-6 smaller cells (secondary features, stats, testimonials)
- Organic, asymmetrical feel
- Natural visual hierarchy through cell size

**Implementation example:**
```
┌──────────────────────┬──────────┐
│                      │  CELL 2  │
│     CELL 1 (LARGE)   │  (small) │
│                      ├──────────┤
│                      │  CELL 3  │
│                      │  (small) │
├──────────┬───────────┴──────────┤
│ CELL 4   │      CELL 5          │
│ (medium) │      (medium)        │
└──────────┴──────────────────────┘
```

### Magazine/Editorial Layout
Mixed content sizes and positions for visual interest.

**Best for:** Content platforms, blogs, news, portfolios
**Structure:**
- Large hero article/image
- Grid of smaller articles
- Mixed aspect ratios
- Pull quotes, sidebars for visual breaks

### Dashboard Layout
Information-dense, functional, scannable.

**Best for:** Analytics, admin panels, monitoring tools
**Structure:**
- Sidebar navigation (left)
- Top bar (search, profile, notifications)
- Grid of cards/charts (main area)
- Fixed-width side panel (optional)

### Storytelling Layout
Linear, narrative-driven scrolling.

**Best for:** Product launches, brand stories, case studies
**Structure:**
- Full-bleed sections
- Alternating text/image rows
- Parallax or scroll-triggered animations
- Progressive reveal of information
- Strong narrative arc

## Information Architecture

### Content Hierarchy System

**Level 1: Primary Navigation**
The main sections of the site (4-7 items max):
```
Home  |  Features  |  Pricing  |  About  |  Blog  |  Contact
```

**Level 2: Secondary Navigation**
Sub-sections within main areas:
```
Features
├── Product Overview
├── Integrations
├── Security
└── API
```

**Level 3: Page-Level Hierarchy**
Structure within a single page using headings:
```
H1: Main headline
├── H2: Major section
│   ├── H3: Sub-section
│   └── H3: Sub-section
└── H2: Major section
    ├── H3: Sub-section
    └── H3: Sub-section
```

### Navigation Architecture

**Flat Architecture:**
- All pages accessible from top nav
- Best for: Small sites (5-10 pages), landing pages
- Pros: Simple, all content equally accessible
- Cons: Doesn't scale to large sites

**Hierarchical Architecture:**
- Parent/child page relationships
- Best for: Documentation, ecommerce, large sites
- Pros: Scalable, organized, logical
- Cons: Deep pages get buried

**Faceted Architecture:**
- Content filtered by multiple attributes
- Best for: Ecommerce, search results, resource libraries
- Pros: Powerful filtering, user-controlled exploration
- Cons: Complex to implement

**Hub-and-Spoke:**
- Central page links to all content
- Best for: Portfolios, product launches
- Pros: Controlled user journey
- Cons: Limited exploration

## Section Architecture

### Standard Page Structure

```
[STICKY NAVBAR]
[HERO SECTION]
  └─ Headline
  └─ Subheadline
  └─ CTA Button
  └─ Hero Image/Video

[SOCIAL PROOF]
  └─ Logo bar / Testimonials / Stats

[FEATURES]
  └─ Feature grid / alternating rows / bento

[HOW IT WORKS]
  └─ Step 1 → Step 2 → Step 3

[ABOUT / STORY]
  └─ Brand narrative, mission, team

[TESTIMONIALS]
  └─ Quote cards, case studies, video

[PRICING]
  └─ Tier cards, comparison table

[FAQ]
  └─ Accordion items addressing objections

[CTA / WAITING]
  └─ Final call to action

[FOOTER]
  └─ Links, social, legal, newsletter
```

### Hero Section Layouts

**Centered Hero:**
```
┌─────────────────────────────────┐
│                                 │
│           HEADLINE              │
│         Subheadline             │
│        [CTA]  [Link]            │
│                                 │
│   ┌─────────────────────────┐   │
│   │     Hero Image/Video    │   │
│   └─────────────────────────┘   │
│                                 │
└─────────────────────────────────┘
```

**Split Hero:**
```
┌──────────────────┬──────────────┐
│                  │              │
│   HEADLINE       │              │
│   Subheadline    │     IMAGE    │
│   [CTA] [Link]   │              │
│                  │              │
└──────────────────┴──────────────┘
```

**Full-Image Hero:**
```
┌─────────────────────────────────┐
│  ┌───────────────────────────┐  │
│  │     HEADLINE              │  │
│  │     Subheadline           │  │
│  │     [CTA]                 │  │
│  └───────────────────────────┘  │
│                                 │
│  [background image/video]       │
└─────────────────────────────────┘
```

## Responsive Layout Strategy

### Mobile (320-480px)
- Single column grid
- Full-width sections
- Vertical stacking of all content
- Reduced padding (16-24px)
- Simplified navigation (hamburger)
- Larger touch targets (44px min)
- Full-width buttons

### Tablet (768-1024px)
- 2-column grid possible
- Split hero (left text, right image)
- Sidebar begins to appear
- 3-feature columns
- Standard padding (24-40px)

### Desktop (1280px+)
- Multi-column grid
- Full hero layouts
- Sidebars, multi-column features
- Generous padding (80-120px)
- Rich secondary content
- Hover states active

### Common Breakpoints
```css
/* Mobile first approach */
.container {
  padding: 0 16px;
  max-width: 100%;
}

@media (min-width: 640px) {
  .container { padding: 0 24px; }
}

@media (min-width: 768px) {
  .container { padding: 0 32px; }
}

@media (min-width: 1024px) {
  .container { padding: 0 48px; max-width: 1200px; margin: 0 auto; }
}

@media (min-width: 1280px) {
  .container { padding: 0 64px; max-width: 1440px; }
}
```

## Layout Spacing System

### Section Spacing
```
--space-section: clamp(3rem, 5vw, 6rem)     /* Between major sections */
--space-section-sm: clamp(2rem, 3vw, 4rem)   /* Between minor sections */
--space-section-lg: clamp(5rem, 8vw, 10rem)  /* Between hero and content */
```

### Element Spacing
```
--space-1:  4px
--space-2:  8px
--space-3:  12px
--space-4:  16px
--space-5:  20px
--space-6:  24px
--space-8:  32px
--space-10: 40px
--space-12: 48px
--space-16: 64px
--space-20: 80px
--space-24: 96px
```

## Layout Anti-Patterns

| ❌ Bad | ✅ Better |
|--------|-----------|
| Infinite scroll without clear sections | Defined sections with breathing room |
| Too many columns on mobile | Single column, linear flow |
| Inconsistent padding | Systematic spacing throughout |
| Content stretched full-width | Constrained max-width containers |
| Orphaned headings | Clear section headers with margin |
| Disconnected visual breaks | Consistent section transitions |
| Cluttered sidebar | Streamlined, purposeful sidebar |
| Floating/stray elements | All elements in the grid system |

## Layout Decision Framework

When choosing a layout, ask:
1. What's the primary user goal? (read, buy, learn, compare)
2. What's the content type? (text-heavy, visual, interactive)
3. What device? (mobile-first, desktop-primary)
4. How many items? (3 features, 30 articles, 1 product)
5. What's the narrative? (linear story, scannable info, comparison)

### Layout by Content Type

| Content Type | Recommended Layout |
|--------------|-------------------|
| Single product/feature | Storytelling, alternating rows |
| Multiple features (3-6) | Grid cards, bento grid |
| Articles/list (10-50) | Magazine grid, list with thumbnails |
| Products (50-500) | Product grid with filters |
| Data/analytics | Dashboard grid |
| Documentation | Sidebar + content |
| Portfolio | Masonry, full-bleed grid |
| Landing page | Z-pattern, single-column narrative |
| Dashboard | Card grid, sidebar layout |
