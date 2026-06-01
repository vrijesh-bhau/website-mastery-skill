# 19 — Research & Competitive Analysis

## Research-First Methodology

### The Golden Rule
**Never design without research.** Before creating any website:
1. Research the category (what do top sites in this space look like?)
2. Research competitors (who else does this?)
3. Research trends (what's current?)
4. Research code (what libraries/ patterns are proven?)

## Research Categories

### 1. Design Trend Research
Use CLI tools to fetch current design trends:
- Browse Awwwards recent winners
- Check Dribbble popular shots
- Read CSS Design Awards winners
- Search "web design trends [current year]"

### 2. Competitor Analysis
For each direct competitor (3-5):
- Visit their website (all pages)
- Note color system, typography, layout
- Identify unique features/ sections
- Note what works well and what doesn't
- Check their mobile experience
- Review their content strategy
- Analyze their pricing page

### 3. UI Pattern Research
For specific patterns you need:
- Search "best [pattern] examples" (e.g., "best pricing page examples")
- Check UI pattern libraries (Mobbin, Collect UI)
- Look at Dribbble shots for the pattern
- Find open-source implementations

### 4. Code/ Implementation Research
Before coding anything complex:
- Search "npm [library] example website"
- Check GitHub for similar implementations
- Look at CodePen for animation examples
- Search "[effect] CSS only" for CSS-only solutions
- Search "[library] template [framework]" for starter code

### 5. Color/ Typography Research
- Use Coolors for palette inspiration
- Check Fonts In Use for typography pairing ideas
- Browse Color Hunt for trending palettes
- Check Huemint for AI-generated palettes

## Web Search Research Prompts

### Design Research Prompts
```
"best designed websites [year]"
"[type] website design inspiration"  (e.g., "SaaS website design inspiration")
"modern [type] landing pages"
"[industry] website examples award"
"best [pattern] UI design"  (e.g., "best pricing page UI design")
```

### Technology Research Prompts
```
"how to build [effect] using [library]"  (e.g., "how to build parallax using Framer Motion")
"[library] tutorial hero section"
"open source [type] website template"
"react [component] example with code"
"modern [pattern] implementation CSS"
```

### Content Research Prompts
```
"best [industry] headlines"
"[type] value proposition examples"
"[industry] conversion optimization tips"
"[type] pricing strategy best practices"
```

## Reverse-Engineering Competitor Sites

### What to Look For
1. **Tech Stack** — Use builtwith.com, Wappalyzer, or browser inspector
2. **Framework** — Check for React, Vue, Next.js, etc. (look for `__NEXT_DATA__`, `__NUXT__`, `data-reactroot`)
3. **CSS Framework** — Check for Tailwind classes, Bootstrap classes
4. **Animation Libraries** — Check for GSAP, Framer Motion, Three.js in sources
5. **Fonts** — Use WhatFont extension or check CSS `@font-face`
6. **Analytics** — Check for GA, Mixpanel, Amplitude, etc.
7. **Hosting/ CDN** — Check network tab for domain
8. **CMS** — Check for WordPress, Contentful, Sanity patterns

### Analysis Protocol
For each competitor page:
1. Take screenshots (desktop + mobile)
2. Note first impression (5-second test)
3. Identify color system (use color picker)
4. Identify typography (use WhatFont)
5. Note spacing/ layout patterns
6. Identify animation patterns
7. Note CTA positioning and copy
8. Identify content sections and ordering
9. Check page load performance (Network tab)
10. Document everything in the analysis template

## GitHub Research Protocol

### Finding Production Code

**Search patterns:**
```
"[technology] real world example" (e.g., "React Three Fiber real world example")
"[library] demo site source code"
"[effect] implementation GitHub"
"awesome [technology]"  (curated lists of resources)
```

**What to look for in repositories:**
- Live demo links (usually in README)
- Production-quality code patterns
- Module/ component organization
- State management approaches
- Testing patterns
- Build configuration

## Open Source Website Templates

When building a new website, always check for:
- Existing templates in the target framework (Next.js, Astro, etc.)
- Open-source landing page templates
- Component libraries with pre-built sections
- Design systems with implementation code

## Research Documentation Template

```
# Research: [Topic/Site Type]

## Trend Analysis (as of [date])
- Trend 1: [Description] — [Source]
- Trend 2: [Description] — [Source]
- Trend 3: [Description] — [Source]

## Competitor Landscape
### Competitor A: [Name]
- URL: [URL]
- Strengths: [list]
- Weaknesses: [list]
- Key takeaway: [what to learn/ avoid]

### Competitor B: [Name]
- URL: [URL]
- Strengths: [list]
- Weaknesses: [list]
- Key takeaway: [what to learn/ avoid]

## Design Patterns to Use
- [Pattern] — [Why] — [Source]
- [Pattern] — [Why] — [Source]

## Design Patterns to Avoid
- [Pattern] — [Why]
- [Pattern] — [Why]

## Color Inspiration
- Palette 1: [colors] — [why it works]
- Palette 2: [colors] — [why it works]

## Typography Inspiration
- Pairing 1: [headline] + [body] — [why it works]
- Pairing 2: [headline] + [body] — [why it works]

## Code/ Implementation References
- [Repository/ CodePen URL] — [what it demonstrates]
- [Repository/ CodePen URL] — [what it demonstrates]

## Final Design Direction
Based on research, the site will use:
- Color: [primary palette direction]
- Font: [typography choice]
- Layout: [layout approach]
- Animation: [animation approach]
- Key differentiator: [what makes this unique vs competitors]
```

## Research Ethics

### Ethical Research Rules
1. **Analyze, don't copy** — Understand WHY something works, not just WHAT
2. **Credit sources** — When heavily inspired, acknowledge
3. **Respect copyright** — Don't use competitor images, copy, or branding
4. **Focus on patterns** — Extract design principles, not specific implementations
5. **Combine multiple sources** — One source = copy. Five sources = original
6. **Add your own value** — Every design should have something unique to your brand

## Research Output Quality Check

Before moving to design:
- [ ] Minimum 3 competitors analyzed
- [ ] Current design trends identified
- [ ] UI patterns collected from 5+ sources
- [ ] Color/typography direction established
- [ ] Implementation references found for complex features
- [ ] Research documented (can be referenced later)
- [ ] Clear direction set for the design phase
