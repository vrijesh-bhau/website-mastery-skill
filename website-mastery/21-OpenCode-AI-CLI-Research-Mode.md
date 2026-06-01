# 21 — OpenCode AI CLI Research Mode

## Critical Directive

**This module is MANDATORY reading before any website project.**

When creating, designing, or improving ANY website, you MUST actively use available internet access (websearch, webfetch) to gather fresh inspiration, modern patterns, and current best practices.

Do NOT rely only on existing knowledge if internet access is available.

## Research Workflow

### Step 1: Design Trend Research
Use websearch to find current design inspiration:

**Search queries to use:**
```
"best designed websites [current year] award"
"[site type] website design inspiration [current year]"  
(e.g., "SaaS website design inspiration 2026")

"modern [site type] landing page examples"
(e.g., "modern AI tool landing page examples")

"Awwwards winner [month year]"
(e.g., "Awwwards winner May 2026")

"[pattern] UI design examples"  
(e.g., "pricing page UI design examples 2026")
```

### Step 2: Technology & Implementation Research
Find production-ready code and implementations:

**Search queries:**
```
"react [component/effect] example code"  
(e.g., "react three fiber floating object example code")

"GSAP [effect] CodePen"
(e.g., "GSAP scroll trigger reveal CodePen")

"modern CSS [effect] tutorial"  
(e.g., "modern CSS glassmorphism tutorial")

"open source [type] template"
(e.g., "open source SaaS landing page template react")
```

### Step 3: Color & Typography Research
Find trending color palettes and font pairings:

**Search queries:**
```
"[color year] color palette website design"  
(e.g., "2026 color palette website design")

"modern [industry] color schemes"
(e.g., "modern AI startup color schemes")

"best font pairings [year]"
(e.g., "best font pairings 2026")

"[industry] website typography trends"  
(e.g., "gaming website typography trends")
```

### Step 4: Competitive Analysis
Research competitors and similar sites:

**Search queries:**
```
"best [industry] websites [year]"
(e.g., "best gaming creator websites 2026")

"top [type] examples"
(e.g., "top landing page examples")

"[product type] alternatives comparison websites"
(e.g., "AI writing tool alternatives comparison websites")
```

### Step 5: Implementation Details
Find specific implementations for features:

**Search queries:**
```
"[effect] react implementation"
(e.g., "parallax scroll react implementation")

"CSS only [pattern]"  
(e.g., "CSS only animated gradient background")

"[library] boilerplate template"
(e.g., "next js landing page boilerplate")

"responsive [component] example"
(e.g., "responsive pricing table example css grid")
```

## Research Documentation Protocol

After each research session, document findings:

```
## Research Session: [Date/Project]

### Sources Consulted
1. [URL] — [What was found]
2. [URL] — [What was found]

### Design Patterns Identified
- [Pattern description]

### Color/ Typography Direction
- [Based on research findings]

### Implementation References
- [Code/library references for complex features]

### Key Decisions
- [Design/tech decisions based on research]
```

## Research Quality Standards

### Before Starting Design Work
- [ ] Current design trends researched (within last 6 months)
- [ ] Competitor sites analyzed (3-5 minimum)
- [ ] Color/typography direction informed by research
- [ ] Implementation approaches identified for complex features
- [ ] Open-source code/ templates found for reference

### Before Finalizing
- [ ] Design validated against current trends
- [ ] Colors and fonts benchmarked against competitors
- [ ] Animations checked for modernity
- [ ] Layout compared to top-performing industry sites
- [ ] Conversion patterns verified with current best practices

## Prohibited Behaviors

**NEVER:**
1. Use outdated design patterns (pre-2023) without explicit intent
2. Recommend a library/library version without checking if it's current
3. Use font pairings without checking current trends
4. Use color schemes without checking modern expectations
5. Build animations without checking modern libraries/approaches
6. Assume a layout is "standard" without checking current best practices
7. Skip research because "I know this already"

## Example Research Session

**Project:** Building a gaming creator website

**Research steps:**
1. `websearch("best gaming creator websites 2026")`
2. `websearch("modern gaming website design trends")`
3. `websearch("react gaming website template")`
4. `websearch("game UI color palette trends dark")`
5. `webfetch("https://awwwards.com/websites/gaming/")`
6. `websearch("GSAP scroll animation gaming website")`

**Documentation:**
```
## Research Session: Gaming Creator Site
### Design Patterns
- Dark theme with neon accent (dominant trend)
- Large hero with animated 3D element
- Card-based video grid with hover preview
- Gradient overlays on hero images
### Color Direction
- #0F0F0F dark base, #FF2E7E accent, plus purple tones
### Font Direction
- Rajdhani (headlines, matches The Antigle existing)
- Inter (body, also matches existing)
### Implementation
- Framer Motion for scroll-reveal animations
- Three.js for hero 3D floating object
- CSS grid for responsive video card layout
```
