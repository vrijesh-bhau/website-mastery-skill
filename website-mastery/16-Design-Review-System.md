# 16 — Design Review System

## The Design Review Process

### When to Review
- Before starting development (wireframes/ mockups)
- After development (pre-deployment QA)
- When redesigning existing pages
- When reviewing competitor sites
- Before client presentation

### Review Roles
When reviewing, adopt these perspectives:
1. **End user** — "Can I achieve my goal easily?"
2. **Business owner** — "Does this drive business results?"
3. **Design critic** — "Is this visually excellent?"
4. **Developer** — "Is this practical to build?"
5. **Accessibility advocate** — "Can everyone use this?"

## Review Dimensions

### 1. First Impression (5-second test)
What does a user see and understand in 5 seconds?

**Check:**
- Can you identify what the company does?
- Can you identify the primary action?
- Does the design feel trustworthy?
- Is the visual style consistent with the brand?

### 2. Navigation & Wayfinding
**Check:**
- How many nav items? (5-7 ideal)
- Is current location always clear?
- Is the logo linked to home?
- Is there a clear path to key pages?
- Is search available for content-heavy sites?
- Are breadcrumbs provided for deep pages?

### 3. Content Readability
**Check:**
- Font size minimum 16px for body
- Line length 45-75 characters
- Line height 1.5 for body text
- Sufficient color contrast
- Headings clearly distinguishable from body
- Paragraphs are short (2-5 sentences)
- Bullet points used for lists

### 4. Call-to-Action Effectiveness
**Check:**
- Primary CTA visible without scrolling
- CTA stands out (contrast, size, whitespace)
- CTA copy is action-oriented
- Secondary CTAs don't compete with primary
- CTAs have hover states
- Multiple CTAs are consistent in style
- Each page has one clear primary action

### 5. Visual Consistency
**Check:**
- Same button styles throughout
- Consistent heading hierarchy
- Consistent spacing rhythm
- Same border radius on all cards
- Same shadow depth for similar elements
- Consistent icon style
- Same color usage rules across pages

### 6. Mobile UX
**Check:**
- Navigation functional on mobile
- Touch targets large enough (44px)
- No horizontal scroll
- Text readable without zoom
- Forms functional on mobile
- Images scale properly
- Content priority: important info first

### 7. Performance Indicators
**Check:**
- Fast loading (< 3 seconds on 3G)
- Smooth scrolling (60fps)
- Images load progressively (blur-up or lazy load)
- No layout shifts during load
- Animations at 60fps
- Bundle sizes reasonable

### 8. Accessibility Basics
**Check:**
- Semantic HTML structure
- Alt text on images
- Keyboard navigable
- Focus indicators visible
- Color contrast sufficient
- `prefers-reduced-motion` supported
- Form labels properly associated
- Error messages are descriptive

## Review Scoring Matrix

Each criterion scored 1-5:

| Score | Meaning |
|-------|---------|
| 5 | Excellent — no improvement needed |
| 4 | Good — minor polish possible |
| 3 | Acceptable — noticeable improvement needed |
| 2 | Poor — significant problem |
| 1 | Critical — must fix before launch |

### Category Weights

| Category | Weight | Why |
|----------|--------|-----|
| First Impression | 15% | Most important — determines bounce |
| Navigation | 10% | Users must find what they need |
| Readability | 10% | Content must be consumable |
| CTAs | 15% | Directly impacts conversions |
| Consistency | 10% | Builds trust and professionalism |
| Mobile UX | 15% | 60%+ of traffic is mobile |
| Performance | 10% | Affects bounce and SEO |
| Accessibility | 15% | Legal requirement + ethical |

### Weighted Score Calculation
```
Total = (First * 0.15) + (Nav * 0.10) + (Read * 0.10) + (CTA * 0.15) + (Consistency * 0.10) + (Mobile * 0.15) + (Perf * 0.10) + (Access * 0.15)
```

## Review Output Template

```
# Design Review: [Page/Site Name]

## Overall Score: [X/5] — [Grade]

## Score Breakdown

| Category | Score | Weight | Weighted |
|----------|-------|--------|----------|
| First Impression | X/5 | 15% | X.X |
| Navigation | X/5 | 10% | X.X |
| Readability | X/5 | 10% | X.X |
| CTAs | X/5 | 15% | X.X |
| Consistency | X/5 | 10% | X.X |
| Mobile UX | X/5 | 15% | X.X |
| Performance | X/5 | 10% | X.X |
| Accessibility | X/5 | 15% | X.X |
| **Total** | | **100%** | **X.X/5** |

## Critical Issues (Score 1-2)
1. **[Issue]** — [Specific location] — [Recommendation]
2. **[Issue]** — [Specific location] — [Recommendation]

## Improvements (Score 3)
1. **[Improvement]** — [Suggestion]
2. **[Improvement]** — [Suggestion]

## Polish Items (Score 4)
1. **[Polish]** — [Fine-tuning suggestion]

## Premium Enhancements
1. **[Enhancement]** — [Would elevate from X to Y]
2. **[Enhancement]** — [Would create wow factor]

## Action Plan
### Immediate (high impact, low effort)
- [Action 1]
- [Action 2]

### Short-term (medium impact, medium effort)
- [Action 3]
- [Action 4]

### Long-term (high impact, high effort)
- [Action 5]
- [Action 6]
```

## Common Design Issues & Solutions

| Issue | Solution |
|-------|----------|
| Low contrast text | Darken text or lighten background to meet WCAG AA |
| Inconsistent spacing | Define and apply a spacing scale system |
| Weak CTA | Larger button, contrasting color, action copy |
| No visual hierarchy | Apply size/ color/ spacing system |
| Too many fonts | Limit to 2 families, use weight/ size for hierarchy |
| Poor mobile nav | Bottom tab bar or hamburger with clear labels |
| Slow loading | Compress images, lazy load, code split |
| Missing hover states | Add transition on all interactive elements |
| Unclear value prop | Rewrite headline to communicate benefit in 5 words |
| Form too long | Remove optional fields, use multi-step with progress |
| Hard-to-read text | Increase line height to 1.5+, shorten line length to 75ch |
| Generic stock photos | Replace with custom illustrations or authentic photography |
| No social proof | Add testimonials, user count, or logo bar |
| Confusing navigation | Reduce items to 5-7, use clear labels |
| Autoplay carousel | Remove carousel, use single hero or manual navigation |

## Premium Enhancement Suggestions

| Current | Premium Enhancement |
|---------|-------------------|
| Static hero | Animated hero with particle/ 3D background |
| Default cursor | Custom cursor follower (creative sites only) |
| Basic hover | Magnetic hover, tilt card, glow effect |
| Page load | Staggered reveal animation |
| Static testimonials | Video testimonials |
| Plain forms | Animated form fields, interactive validation |
| Standard cards | Glassmorphism cards on gradient backgrounds |
| Basic pricing | Interactive pricing with toggle animation |
| Regular images | Lazy load with blur-up placeholder |
| Page transitions | Morphing shared-element transitions |
| Static icons | Animated SVG icons on hover |
| Static counters | Animated count-up numbers on scroll |
