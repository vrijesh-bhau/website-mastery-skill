# 13 — Interactive Web Experiences

## Cursor Systems

### Custom Cursor Types

**Follower cursor:**
A custom element that follows the mouse cursor. Common for premium/creative sites.

**Implementation considerations:**
- Use `transform: translate()` for performance (GPU-accelerated)
- Add a delay/easing for smooth following effect
- Hide system cursor with `cursor: none` on the body
- Show system cursor on interactive elements (or use custom hover states)

**Hover-reactive cursor:**
Cursor changes size, color, or shape when hovering interactive elements.

**Common interactions:**
- Cursor enlarges over links/buttons
- Cursor changes to a "view" icon over images
- Cursor becomes a crosshair over draggable elements
- Cursor shows a "+" over expandable elements

### When to use custom cursors
**Good for:** Creative portfolios, agency sites, interactive experiences
**Bad for:** Content-heavy sites, ecommerce, accessible UX, touch-only devices

### Cursor Accessibility
- Only replace cursor with `pointer` style on interactive elements
- Don't hide system cursor unless custom cursor covers entire page
- Ensure custom cursor doesn't obscure text
- Test with keyboard navigation (custom cursor shouldn't interfere)
- Disable on touch devices (no hover)

## Parallax Systems

### Types of Parallax

**Layer parallax:**
Multiple layers move at different speeds as user scrolls. Creates depth.

**Mouse parallax:**
Elements move based on mouse position. Creates 3D-like depth.

**Scroll parallax:**
Content and background move at different scroll speeds.

### Performance Guidelines
- Use `transform: translateZ()` + `perspective` for GPU-accelerated parallax
- Keep layers minimal (3-5 maximum for performance)
- Don't use on mobile (or reduce effect significantly)
- Test on mid-range devices (not just high-end)
- Consider `position: sticky` as a lightweight alternative

### When to Use Parallax
- **Hero sections** — Background moves slower than content
- **Storytelling** — Layer reveal creates narrative depth
- **Product showcases** — Multiple product angles
- **Scrolling galleries** — Video/ image sequences

### When NOT to use Parallax
- Long text sections (motion sickness)
- Mobile-first experiences (performance)
- Accessibility-sensitive content
- Dashboard/ data interfaces

## Mouse Interaction Effects

### Mouse-Reactive Elements
Effects that respond to cursor position:

- **Tilt on hover** — Card slightly rotates toward cursor
- **Glow follow** — Radial gradient following cursor
- **Magnetic buttons** — Button pulls toward cursor
- **Reveal on hover** — Image sharpens/colors as cursor approaches
- **Distortion** — Image or text warps near cursor

### Implementation Pattern (Mouse Tracking)
```js
element.addEventListener('mousemove', (e) => {
  const rect = element.getBoundingClientRect();
  const x = (e.clientX - rect.left) / rect.width - 0.5;
  const y = (e.clientY - rect.top) / rect.height - 0.5;
  element.style.transform = `rotateY(${x * 10}deg) rotateX(${-y * 10}deg)`;
});

element.addEventListener('mouseleave', () => {
  element.style.transform = 'rotateY(0deg) rotateX(0deg)';
});
```

## Interactive Backgrounds

### Particle Systems
**Good for:** Hero sections, full-screen backgrounds, creative sites
**Performance considerations:**
- < 100 particles for mobile
- < 500 particles for desktop
- Simple shapes (circles, squares) over complex textures
- No collision detection (expensive)

### Gradient Animations
- Animated mesh gradients (moving color points)
- Subtle hue shifts over time
- Mouse-reactive gradient position

### Noise/ Grain Texture
- Subtle animated noise overlay for depth
- CSS-based or canvas-based
- Very low performance cost
- Adds "premium film" feel

### Wave/ Ripple Effects
- Canvas-based wave animations
- Reactive to mouse click/ position
- Water-like surface distortion

## Scroll-Based Interactions

### Scroll Progress Elements
- **Progress bar** — Indicates reading position (top of page)
- **Scroll-triggered counter** — Numbers count up as user scrolls
- **Scroll-linked animations** — Animation progress = scroll progress

### Section Transitions
- **Full-page scroll snap** — Each section snaps to viewport
- **Horizontal scroll section** — Scrolls horizontally within a section
- **Split-screen scroll** — Two panels scroll at different rates
- **Accordion scroll** — Sections expand as user scrolls past

## Audio Interactions

### Web Audio in UX
- **Hover sounds** — Subtle tones on hover (use sparingly)
- **Click confirmation** — Satisfying click sound
- **Scroll-based audio** — Ambient sound that changes with scroll
- **Background ambient** — Environmental audio (muted, optional)

### Audio Rules
- Never autoplay audio (user must initiate)
- Provide mute/ volume controls
- Keep audio files small (10-30kb, compressed)
- Use Web Audio API for programmatic sounds
- Test with screen readers (no interference)

## Gamification Elements

### Types of Gamification
- **Progress tracking** — "3 of 10 tasks complete"
- **Streak counters** — "Day 5 streak!"
- **Badge/ achievement** — Unlock visual rewards
- **Points system** — Accumulate for actions
- **Leaderboards** — Competitive ranking
- **Confetti/ celebration** — On completing goals

### Implementation Guidelines
- Gamification must serve user goals, not distract
- Celebrations should be short (< 2 seconds)
- Progress indicators should motivate, not pressure
- Leaderboards should be optional, not anxiety-inducing

## Immersive Storytelling

### Storytelling Pattern
```
[Scene 1] → [Scene 2] → [Scene 3] → [Scene 4]
  |             |            |            |
 [Scroll]     [Scroll]     [Scroll]     [Scroll]
 [Reveal]     [Animate]    [Transform]  [CTA]
```

### Scrollytelling (Scroll Storytelling)
- Each scroll position reveals a new "scene"
- Text, visuals, and animations change per scene
- Camera movement or element transformation drives narrative

**Examples:**
- Apple product pages (scroll reveals product features)
- The Boat (scroll-driven film)
- Year in Review (Wrapped-style data narrative)

### Interactive Video
- Video controlled by scroll position
- Frame-by-frame scrubbing
- Branching narrative (choose your path)

## Interactive Experience Decision Guide

| Experience | Best For | Performance Cost | Accessibility Impact |
|-----------|----------|-----------------|---------------------|
| Custom cursor | Creative sites, portfolio | Low | Medium (screen readers) |
| Parallax | Storytelling, hero | Medium | High (motion sickness) |
| Particle bg | Hero, premium landing | Medium-High | Low |
| Scroll snap | Sections, showcase | Low | Medium |
| Audio interaction | Creative, gaming | Low | High (needs alternatives) |
| Gamification | Learning, onboarding | Low | Medium |
| Scrollytelling | Product launch, brand | Medium | High (needs text version) |
| Mouse tilt | Cards, product showcase | Low | Low |

## Interactive Experience Checklist

- [ ] All interactions work with keyboard (not just mouse)
- [ ] Touch device support considered (not hover-dependent)
- [ ] `prefers-reduced-motion` respected
- [ ] Performance budget established (fps target, memory limit)
- [ ] Fallback for non-supporting browsers
- [ ] No interaction required for core functionality
- [ ] Loading states for JS-heavy interactions
- [ ] Mobile testing completed (mid-range device)
- [ ] Battery life considered (limit CPU-intensive effects)
- [ ] Screen reader tested (no unexpected behavior)
- [ ] Custom cursor hidden on touch devices
- [ ] Audio requires user action to play
