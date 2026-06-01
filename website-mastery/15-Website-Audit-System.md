# 15 — Website Audit System

## Audit Overview

A website audit evaluates a site across 10 critical dimensions. Each dimension scores 1-10, with a total possible score of 100.

## Audit Dimensions

### 1. Visual Quality (1-10)
**What it measures:** Aesthetic appeal, design cohesiveness, visual refinement.

**Score 1-3:** No visual system, inconsistent styling, clashing colors
**Score 4-6:** Basic visual system, some consistency, acceptable
**Score 7-8:** Coherent visual system, refined spacing, good color harmony
**Score 9-10:** Pixel-perfect, innovative, emotionally resonant, every detail intentional

**Checklist:**
- Is there a consistent color system?
- Are spacing/sizing values consistent?
- Is visual hierarchy clear?
- Are images high quality and optimized?
- Are there any visual inconsistencies (misaligned elements, odd spacing)?
- Do borders, shadows, and radii follow a system?

### 2. Professionalism (1-10)
**What it measures:** Trustworthiness, polish, apparent quality.

**Score 1-3:** Looks amateur, default styles, broken elements
**Score 4-6:** Looks like a template, functional but generic
**Score 7-8:** Looks like a real business investment, polished
**Score 9-10:** Looks like a market leader, award-worthy, premium

**Checklist:**
- Is the value proposition clear in 5 seconds?
- Is there a custom domain?
- Are there any broken links or images?
- Are CTAs clear and prominent?
- Does the site feel "finished" or "in progress"?
- Is the brand identity consistent throughout?

### 3. Modern Appearance (1-10)
**What it measures:** How contemporary the design feels.

**Score 1-3:** Looks 10+ years old, outdated patterns
**Score 4-6:** Looks 3-5 years old, some modern elements
**Score 7-8:** Looks current, follows modern patterns
**Score 9-10:** Ahead of trends, feels cutting-edge

**Checklist:**
- Does the design follow current UI patterns?
- Are typography choices current?
- Does it use modern CSS (grid, custom properties)?
- Are animations smooth and purposeful?
- Would it pass a "when was this made?" test?

### 4. Accessibility (1-10)
**What it measures:** Inclusive design for all users.

**Score 1-3:** Major barriers, color-only indicators, no alt text
**Score 4-6:** Some accessibility, basic alt text, minimal focus indicators
**Score 7-8:** WCAG AA compliant in most areas
**Score 9-10:** WCAG AAA compliant, excellent keyboard nav, screen-reader tested

**Checklist:**
- Color contrast meets WCAG AA minimum (4.5:1 text)
- Focus indicators visible on all interactive elements
- All images have meaningful alt text
- Semantic HTML used (h1-h6 hierarchy, nav, main, section)
- ARIA attributes where needed
- Forms have associated labels
- Site navigable by keyboard
- `prefers-reduced-motion` support
- Touch targets at least 44x44px

### 5. Responsiveness (1-10)
**What it measures:** Quality across all screen sizes.

**Score 1-3:** Desktop-only, broken on mobile, horizontal scroll
**Score 4-6:** Works on most screens, some issues
**Score 7-8:** Excellent across all common devices
**Score 9-10:** Flawless on every screen size, thoughtful mobile UX

**Checklist:**
- Works on 320px width (small mobile)
- Works on 768px (tablet)
- Works on 1440px+ (large desktop)
- Touch targets still comfortable on mobile
- No horizontal scroll on any device
- Navigation functional on mobile (hamburger or tab bar)
- Font sizes readable on mobile (16px minimum)
- Images resize properly
- No overlapping elements at any width

### 6. Conversion Potential (1-10)
**What it measures:** How well the site drives desired actions.

**Score 1-3:** No clear CTA, confusing user path, no conversion mechanism
**Score 4-6:** CTA present but weak, unclear user journey
**Score 7-8:** Clear conversion path, strong CTAs, good persuasion elements
**Score 9-10:** Optimized funnel, A/B tested, clear value at every step

**Checklist:**
- Primary CTA visible without scrolling (above fold)
- CTA copy is action-oriented ("Get started" not "Learn more")
- Value proposition clear in headline
- Social proof visible (testimonials, logos, counts)
- Forms minimize fields
- No distractions near CTAs
- Trust signals near conversion points
- Clear next step at page bottom

### 7. Performance (1-10)
**What it measures:** Load time, interactivity, visual stability.

**Score 1-3:** Loads > 10 seconds, janky interactions, layout shifts
**Score 4-6:** Loads 4-8 seconds, acceptable but slow
**Score 7-8:** Loads 1-3 seconds, smooth interactions
**Score 9-10:** Loads < 1 second, instant interactivity, 60fps

**Checklist:**
- First Contentful Paint (FCP) < 1.5s
- Largest Contentful Paint (LCP) < 2.5s
- First Input Delay (FID) < 100ms
- Cumulative Layout Shift (CLS) < 0.1
- Images optimized (WebP, proper dimensions, lazy loading)
- CSS/ JS minified
- Fonts loaded with display:swap
- No render-blocking resources
- Code splitting for route-based chunks

### 8. Mobile Experience (1-10)
**What it measures:** Mobile-specific UX quality.

**Score 1-3:** Unusable on mobile, tiny text, impossible tap targets
**Score 4-6:** Functional but frustrating, some mobile issues
**Score 7-8:** Good mobile experience, minor improvements needed
**Score 9-10:** Mobile-first excellence, feels like a native app

**Checklist:**
- No horizontal scroll on mobile
- Touch targets 44x44px minimum
- Forms optimized for mobile (correct input types, no zoom on focus)
- Navigation usable with one hand (thumb zone)
- Content prioritization (important info comes first)
- No hover-dependent interactions
- Click-to-call for phone numbers
- Mobile font sizes adequate
- No intrusive interstitials

### 9. Animation Quality (1-10)
**What it measures:** Motion design effectiveness and performance.

**Score 1-3:** No animations, or jarring/ broken animations
**Score 4-6:** Basic transitions, functional but not delightful
**Score 7-8:** Smooth, purposeful animations that enhance UX
**Score 9-10:** Award-worthy motion design, emotionally resonant

**Checklist:**
- Animations use GPU-accelerated properties (transform, opacity)
- Duration appropriate for context (100-500ms)
- Easing curves feel natural
- Animations have purpose (not decoration-only)
- No motion sickness risk
- `prefers-reduced-motion` supported
- No animation delay that frustrates
- Stagger animations are timed well
- Page transitions are smooth (if applicable)
- Hover states provide feedback

### 10. Content Hierarchy (1-10)
**What it measures:** Information structure and scannability.

**Score 1-3:** Walls of text, no hierarchy, confusing structure
**Score 4-6:** Some structure, basic headings, acceptable flow
**Score 7-8:** Clear hierarchy, scannable, logical flow
**Score 9-10:** Perfect information architecture, intuitive, effortless to scan

**Checklist:**
- H1 is clear and descriptive
- H2 sections are logically ordered
- Content is scannable (short paragraphs, bullet points)
- Visual hierarchy matches content importance
- Navigation reflects content structure
- Related content is grouped
- Calls to action are placed after relevant content
- No orphaned headings
- Clear section transitions

## Audit Score Interpretation

| Total Score | Grade | Meaning |
|------------|-------|---------|
| 90-100 | S | World-class. Ready for Awwwards. |
| 80-89 | A | Excellent. Minor polish needed. |
| 70-79 | B | Good. Some improvements recommended. |
| 60-69 | C | Acceptable. Significant improvements needed. |
| 50-59 | D | Below average. Major redesign recommended. |
| < 50 | F | Poor. Needs complete rebuild. |

## Audit Report Template

```
# Website Audit Report: [Site Name]

## Overall Score: XX/100 (Grade: X)

### Category Scores
1. Visual Quality:       X/10
2. Professionalism:      X/10
3. Modern Appearance:    X/10
4. Accessibility:        X/10
5. Responsiveness:       X/10
6. Conversion Potential: X/10
7. Performance:          X/10
8. Mobile Experience:    X/10
9. Animation Quality:    X/10
10. Content Hierarchy:   X/10

### Top Strengths
- Strength 1
- Strength 2
- Strength 3

### Critical Issues (Fix Immediately)
- Issue 1 with specific recommendation
- Issue 2 with specific recommendation

### Recommended Improvements
- Improvement 1 with implementation approach
- Improvement 2 with implementation approach

### Premium Enhancements
- Enhancement 1 (would elevate from good to great)
- Enhancement 2 (would elevate from great to excellent)

### Priority Actions
1. [Critical fix] — Time: 1-2 hours
2. [High impact] — Time: 2-4 hours
3. [Medium improvement] — Time: 4-8 hours
4. [Premium enhancement] — Time: 8-16 hours
```
