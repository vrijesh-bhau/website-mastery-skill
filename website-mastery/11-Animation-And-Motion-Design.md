# 11 — Animation & Motion Design

## Motion Design Principles

### Why Animation Matters
- **Guides attention** — Animated elements attract the eye
- **Provides feedback** — Confirms user actions instantly
- **Creates continuity** — Smooth transitions between states
- **Builds hierarchy** — Animation speed = importance
- **Delights users** — Premium feel, memorable experience
- **Tells stories** — Sequential reveals create narratives

### The 12 Principles of Web Animation
Adapted from Disney's principles:

1. **Easing** — Natural movement accelerates/decelerates (never linear)
2. **Offset & Delay** — Elements don't move simultaneously (stagger)
3. **Parenting** — Elements move in relation to each other
4. **Transformation** — Change size, not just position
5. **Value Change** — Animate numeric values (counters)
6. **Masking** — Reveal content through borders (clip paths, gradients)
7. **Overlay** — Elements move on different planes (parallax)
8. **Cloning** — Element spawns copies (particle effects)
9. **Obscuration** — Element hidden behind another (3D reveals)
10. **Dimensionality** — Use 3D transforms (rotateX, rotateY, translateZ)
11. **Dolly & Pan** — Camera movements through scenes
12. **Blur & Glow** — Depth cues (focus/defocus)

### When NOT to Animate
- Critical reading (long-form text, documentation)
- Data-dense interfaces (dashboards showing many numbers)
- Accessibility-compromised (prefers-reduced-motion)
- Performance-sensitive (low-end devices, battery saving)
- Repeated/frequent interactions (loading spinner that doesn't stop)
- Payment/ form submission (don't delay critical feedback)

## Animation Libraries

### Framer Motion (React)
Best for: React projects, complex UI animations

**Key capabilities:**
- `motion.div` — Animate any element
- `AnimatePresence` — Mount/unmount animations
- `layoutId` — Shared layout animations (morphing)
- `useScroll`, `useTransform` — Scroll-linked animations
- `drag` — Drag interactions
- `gesture` — Hover, tap, whileInView

### GSAP (GreenSock Animation Platform)
Best for: Complex timeline animations, cross-framework, scroll-triggered

**Key capabilities:**
- `gsap.to()` — Animate to values
- `gsap.from()` — Animate from values
- `gsap.timeline()` — Sequence animations
- `ScrollTrigger` — Scroll-based animations (powerful)
- `MotionPath` — Animate along SVG paths
- `TextPlugin` — Text reveal animations

### Motion One
Best for: Lightweight, performant animations (size ~4kb)

**Key capabilities:**
- `animate()` — Simple animation API
- `scroll()` — Scroll-linked animations
- `inView()` — Trigger on viewport entry
- `spring()` — Spring physics animations

### CSS Animations & Transitions
Best for: Simple, lightweight animations (no JS needed)

**Key capabilities:**
- `transition` — Smooth state changes (hover, focus, active)
- `@keyframes` — Complex multi-step animations
- `animation` — Named animation sequences
- `prefers-reduced-motion` — Accessibility queries

## Animation Types & Implementation

### 1. Entrance Animations
Elements animate in when they appear (page load or scroll into view).

**Common entrance animations:**
- Fade in (opacity 0 → 1)
- Slide up (translateY 20-50px → 0)
- Scale in (scale 0.8-0.95 → 1)
- Clip reveal (clip-path revealing from center)
- Blur in (blur 10px → 0)
- Stagger (entrance delay per element in a group)

**Implementation approach:**
```
Element enters viewport → trigger animation → animate to final state
```

### 2. Scroll Animations
Elements animate based on scroll position.

**Types:**
- **Scroll reveal** — Element animates when it enters viewport
- **Parallax** — Element moves at different speed than scroll
- **Progress-based** — Animation progress = scroll progress
- **Pin & reveal** — Element pins while content scrolls over it

### 3. Hover & Interaction Animations
**Button hover:**
- Lift (translateY -2px + shadow increase)
- Scale (1.02-1.05)
- Background color shift
- Icon animation (arrow slides right)

**Card hover:**
- Image zoom scale (1.05-1.1)
- Shadow depth increase
- Border glow
- Information overlay reveal

**Link hover:**
- Underline slide in
- Color change
- Subtle weight change (if variable font)

### 4. Page Transitions
Animations when navigating between pages (SPA/Multi-page app).

**Types:**
- Slide (page slides in from right)
- Fade (page fades in over current)
- Morph (shared element morphs between pages)
- Scale (page zooms in/out)
- Cover (overlay wipes across)

### 5. Loading Animations
**Types:**
- Skeleton shimmer (preferred — shows layout)
- Progress bar (determinate/ indeterminate)
- Spinner (only for short waits)
- Logo animation (branded)
- Content placeholder with pulse

## Performance Guidelines

### GPU-Accelerated Properties Only
For smooth 60fps animations, ONLY animate these properties:
- `transform` (translate, scale, rotate)
- `opacity`
- `filter` (on GPU-compatible browsers)

**Never animate these properties:**
- `width` / `height` (causes layout recalculations)
- `top` / `left` / `right` / `bottom` (causes layout)
- `margin` / `padding` (causes layout)
- `box-shadow` (causes paint, expensive)

### Performance Targets
- **60fps** — Target for all animations
- **30fps** — Acceptable for complex scenes (3D)
- **<30fps** — Must optimize

### Will-Change Property
```css
.animated-element {
  will-change: transform, opacity;
}
```
Use sparingly — only on elements currently animating. Remove after animation.

### Reduce Motion Support
```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

## Animation Timing

### Duration Guidelines
- **Micro-interactions** — 100-200ms (hover, click feedback)
- **UI transitions** — 200-300ms (menu open, modal show)
- **Content reveals** — 400-600ms (elements entering view)
- **Page transitions** — 300-500ms (page changes)
- **Hero animations** — 800-1500ms (hero entrance sequence)
- **Background loops** — 3000ms+ (ambient animation)

### Easing Functions
```css
--ease-out: cubic-bezier(0.16, 1, 0.3, 1);         /* Natural deceleration */
--ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);      /* Smooth start/end */
--ease-out-expo: cubic-bezier(0.19, 1, 0.22, 1);    /* Dramatic deceleration */
--ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);   /* Bouncy ending */
--ease-smooth: cubic-bezier(0.4, 0, 0.2, 1);        /* Standard smooth */
```

**When to use which:**
- **ease-out** — Default for most UI (feels natural)
- **ease-in-out** — Transitions between screens
- **ease-out-expo** — Hero reveals, dramatic entrances
- **spring** — Playful interactions, cards, notifications
- **linear** — Only for continuous motion (loading spinner)

## Scroll Animation Systems

### ScrollTrigger (GSAP)
The most powerful scroll animation system.

**Common patterns:**
- **Reveal on scroll** — Trigger animation when element enters viewport
- **Pin and scroll** — Pin an element while content scrolls over it
- **Progress** — Animation tied to scroll progress (0-100%)
- **Snap** — Snap sections into view (full-page scroll)

### Intersection Observer (Vanilla)
Lightweight scroll detection without GSAP:
```js
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.1 });

document.querySelectorAll('.animate-on-scroll').forEach(el => observer.observe(el));
```

## Animation Decision Framework

When considering an animation, ask:
1. Does this improve user understanding?
2. Does this provide feedback for an action?
3. Does this guide attention to something important?
4. Will this feel slow or fast enough?
5. Does this respect reduced motion preferences?
6. Will this perform well on the target device?
7. Is this consistent with other animations in the site?

If NO to questions 1-3: Don't animate.
If YES to all: Animate with performance in mind.

## Animation Checklist

- [ ] All animations use GPU-accelerated properties only (transform, opacity)
- [ ] Duration is appropriate (micro 100-200ms, UI 200-400ms, reveals 400-600ms)
- [ ] Easing is natural (not linear, not overly bouncy)
- [ ] No animation on elements that contain critical information
- [ ] Reduced motion media query implemented
- [ ] Animations don't block user interaction
- [ ] Scroll animations work without JS (progressive enhancement)
- [ ] Animations don't trigger on initial page load (only on user action or scroll)
- [ ] Mobile performance tested (not janky on mid-range devices)
- [ ] Each animation has a purpose (no decoration-only motion)
- [ ] Stagger delays are felt but not frustrating (50-150ms between items)
- [ ] Hover states work on touch devices too (no hover-only animations)
