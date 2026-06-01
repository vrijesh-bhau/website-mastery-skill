# 01 — Website Foundations

## Core Design Principles

### Visual Hierarchy
The most important principle. Controls what users see first, second, third.

**How to create hierarchy:**
- Size: Largest element = most important. Headlines bigger than body text
- Color: Bright/saturated colors draw attention first. Use sparingly
- Contrast: High-contrast elements stand out. Low-contrast recedes
- Spacing: More space around an element = more importance
- Position: Top-left (F-pattern) and center receive most attention
- Density: Empty space around focal points makes them prominent
- Motion: Animated elements capture attention (use deliberately)

**Hierarchy levels for any page:**
1. Primary (Hero headline, CTA button) — bold, large, high contrast
2. Secondary (Section headers, key stats) — distinct but not competing
3. Tertiary (Subheadings, feature titles) — clear hierarchy
4. Body (Descriptions, paragraphs) — readable, consistent
5. Meta (Tags, dates, small print) — minimal visual weight

### The 60-30-10 Rule
- 60% Dominant color (backgrounds, large areas)
- 30% Secondary color (headers, sections)
- 10% Accent color (CTAs, interactive elements, highlights)

### Gestalt Principles for Web

| Principle | Application |
|-----------|-------------|
| **Proximity** | Related elements grouped together. Cards, sections, form fields near their labels |
| **Similarity** | Same styles = same function. All buttons look alike. All links share a color |
| **Continuity** | Aligned elements guide the eye. Grids, lists, rows create visual flow |
| **Closure** | Incomplete shapes the brain completes. Hamburger menu, card truncation |
| **Figure-Ground** | Clear distinction between content and background. Cards on colored BG |
| **Common Region** | Elements in same bordered area are related. Cards, sidebars, modals |
| **Focal Point** | Visual anchor that draws attention first. Hero image, large headline |
| **Symmetry** | Balanced layouts feel stable and professional |

### Fitts's Law
Time to acquire a target = distance / size.
- Make CTAs large and close to where users look
- Place primary actions in easy-to-reach areas
- On mobile: thumbs reach bottom-center area easiest

### Hick's Law
More choices = longer decisions.
- Limit navigation to 5-7 items maximum
- Reduce form fields to essentials
- Present 3-4 pricing tiers, not 10
- Progressive disclosure: show more options only when needed

### Cognitive Load
Keep mental effort low:
- One primary action per screen
- Clear visual paths (don't make users hunt)
- Consistent patterns throughout
- Familiar UI conventions (users already know how to use them)
- Chunk information into digestible pieces (3-4 items per group)

## Design Frameworks

### Atomic Design (Brad Frost)
1. **Atoms** — Buttons, inputs, labels, icons (smallest components)
2. **Molecules** — Search bar (input + button), card (image + text + link)
3. **Organisms** — Header, footer, feature grid (complex components)
4. **Templates** — Page layouts with placeholder content
5. **Pages** — Filled templates with real content

### Design Thinking Process
1. **Empathize** — Understand users through research
2. **Define** — Frame the problem clearly
3. **Ideate** — Brainstorm solutions without judgment
4. **Prototype** — Build quick versions
5. **Test** — Validate with real users

### Mobile-First Design
Start with smallest screen, progressively enhance:
1. Content and core functionality for mobile
2. Add layout complexity for tablet
3. Add richer experiences for desktop
4. Never start with desktop and strip down

## Design Quality Ladder

| Level | Characteristics | Examples |
|-------|-----------------|----------|
| **1 — Functional** | Works but ugly. Default styles, no visual system | Internal tools, old web apps |
| **2 — Clean** | Consistent spacing, reasonable typography, basic grid | Bootstrap sites, templates |
| **3 — Professional** | Coherent color system, good typography, thoughtful spacing | Most SaaS, agency sites |
| **4 — Premium** | Refined spacing, custom illustrations, micro-interactions | Stripe, Linear, Notion |
| **5 — Master** | Bespoke animations, innovative interactions, perfect craft | Awwwards winners, Apple |

## The Premium Difference

What separates premium sites from average ones:

### Spacing Mastery
- **Whitespace is a design element**, not empty space
- Premium sites use 2-3x more spacing than average
- Consistent rhythm: all spacing follows a scale (4px, 8px, 16px, 24px, 32px, 48px, 64px, 96px, 128px)
- Section padding: 80-120px on desktop, 40-60px on mobile
- Card padding: 24-32px minimum
- Line height: 1.5-1.8 for body text

### Refinement Details
- Border radius: subtle (4-8px) or none. Avoid awkward in-between values
- Shadows: layered, realistic. Not just `box-shadow: 0 2px 4px #000`
- Transitions: 150-300ms ease-out for micro-interactions
- Loading states: skeleton screens, not spinners
- Empty states: helpful illustrations, not blank pages
- Error states: contextual, friendly, actionable — not red text

### Content Design
- Headlines: benefit-driven, specific, clear
- Body: scannable with short paragraphs (2-3 sentences max)
- Bullet points: 3-7 items per list
- CTAs: action-oriented starting with verbs ("Start free trial", not "Learn more")
- Social proof: recent, specific, relevant ("2,341 designers use this")

## Common Design Antipatterns

| ❌ Bad | ✅ Better |
|--------|-----------|
| Centered text on long paragraphs | Left-aligned for readability |
| Too many font sizes | 2-3 sizes maximum |
| Weak contrast (#999 on white) | WCAG AA minimum 4.5:1 |
| Autoplay carousels | Static hero with clear value prop |
| Generic stock photography | Custom illustrations or authentic photos |
| Walls of text | Short paragraphs, subheaders, visuals |
| Mystery meat navigation | Clear, descriptive link labels |
| Over-designed forms | Simple, single-column layout |
| Too many CTAs | One primary action per section |
| Inconsistent spacing | Systematic spacing rhythm |

## Accessibility Fundamentals

Design for ALL users, not just perfect-vision desktop users:
- Color contrast: WCAG AA 4.5:1 (text), 3:1 (large text/UI)
- Don't rely solely on color to convey information
- Focus indicators: visible, high-contrast focus rings
- Touch targets: minimum 44x44px
- Font size: minimum 16px for body text
- Line length: 45-75 characters optimal
- Alt text on all meaningful images
- Semantic HTML hierarchy (h1 → h2 → h3, not skipping levels)
- Aria labels where visual labels aren't possible

## Responsive Design System

### Breakpoints
```
Mobile: 320-480px
Tablet: 768-1024px
Desktop: 1280-1440px
Large: 1600-1920px
```

### Scaling Strategy
- Fonts: Use `clamp(min, preferred, max)` for fluid typography
- Spacing: Scale down by 50% on mobile
- Grid: 1 col mobile → 2 col tablet → 3-4 col desktop
- Navigation: Hamburger on mobile → full nav on desktop
- Images: `max-width: 100%` with height auto

## Performance & UX Tradeoffs

Every design decision has a performance impact:
- Custom fonts: beautiful but add load time (subset + preload + swap)
- Animations: delightful but can cause jank (use GPU-accelerated properties only)
- Images: essential but heavy (use WebP, lazy load, proper dimensions)
- 3D/render: impressive but battery-draining on mobile
- Videos: engaging but bandwidth-heavy (poster image, lazy load, autoplay muted)

**Priority: Content > Performance > Aesthetics**

## Design Decision Framework

When making any design decision, ask:
1. Does this help the user achieve their goal faster?
2. Does this reduce cognitive load?
3. Does this work on mobile?
4. Does this improve or harm performance?
5. Is this accessible?
6. Does this maintain visual consistency?
7. Does this support the brand identity?
