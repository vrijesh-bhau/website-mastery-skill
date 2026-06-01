# 04 — Typography Mastery

## Typography Fundamentals

### Type Anatomy
Understanding type terminology helps make precise design decisions:
- **Ascender** — Stroke rising above x-height (b, d, f, h, k, l)
- **Descender** — Stroke dropping below baseline (g, j, p, q, y)
- **x-height** — Height of lowercase letters (tall x-height = readability)
- **Cap height** — Height of uppercase letters
- **Baseline** — Line letters sit on
- **Serif** — Small decorative strokes at letter ends
- **Sans-serif** — Letters without serifs
- **Stroke weight** — Thickness of letter strokes
- **Counter** — Enclosed space in letters (o, e, a)
- **Kerning** — Space between specific letter pairs
- **Tracking/letter-spacing** — Uniform space across all letters
- **Leading/line-height** — Vertical space between lines

### Font Categories

**Sans-serif** — Modern, clean, digital-first
- Examples: Inter, SF Pro, Helvetica, Neue Haas Grotesk, Satoshi, General Sans
- Best for: Body text, digital interfaces, modern brands
- Avoid: Long-form print where serifs aid readability

**Serif** — Traditional, trustworthy, editorial
- Examples: Garamond, Merriweather, Playfair Display, Source Serif
- Best for: Headlines, editorial content, luxury brands, long-form reading
- Avoid: Small mobile text, dense data UIs

**Display** — Decorative, attention-grabbing
- Examples: Anton, Bebas Neue, Fraunces, Cabinet Grotesk
- Best for: Large headlines, hero sections, creative brands
- Avoid: Body text, small sizes, long paragraphs

**Mono** — Technical, code-like, precise
- Examples: JetBrains Mono, Fira Code, Space Mono
- Best for: Code snippets, technical content, design accents
- Avoid: Long-form reading, general body text

**Script** — Handwritten, elegant
- Examples: Playlist Script, Cormorant
- Best for: Logos, short headlines, invitations
- Avoid: Body text, small sizes, serious corporate UIs

### Variable Fonts
Single font file that can adjust weight, width, slant, etc.
- Performance: One file replaces 5-10 static files
- Flexibility: Fine-tune weight (200-900) per element
- Animation: Morph between weights for effects
- Support: Modern browsers (check caniuse)

**Recommended variable fonts:**
- Inter — Excellent readability, massive weight range
- Satoshi — Modern geometric, variable from 200-900
- General Sans — Clean contemporary sans
- Cabinet Grotesk — Bold display sans
- Fraunces — Variable serif with optical size
- Roobert — Modern grotesk

## Typeface Selection

### The 2-Font System (Recommended)
1. **Display font** — Headlines, hero text, large UI (sans-serif or serif)
2. **Body font** — Paragraphs, descriptions, small UI (usually sans-serif)

### The 3-Font System
1. **Display font** — Large headlines, hero
2. **UI font** — Navigation, buttons, labels
3. **Body font** — Paragraph text, long content

### Choosing a Primary Font

**For digital products (SaaS, apps, tech):**
- Inter — Safe choice, excellent readability, variable
- Satoshi — Modern, warm alternative to Inter
- SF Pro — Apple ecosystem fit
- Roboto — Reliable, universal
- Plus Jakarta Sans — Modern Indonesian sans

**For creative/design brands:**
- Neue Haas Grotesk — Design industry standard
- Helvetica Now — Premium, timeless
- GT America — Sophisticated, versatile
- Founders Grotesk — Contemporary, sharp

**For editorial/content heavy:**
- Source Serif + Source Sans — Excellent pairing
- Merriweather + Open Sans — Classic combo
- Playfair Display + Inter — Elegant headlines + clean body

**For luxury/premium:**
- Cormorant Garamond — Elegant serif
- Didot — High-end fashion feel
- Trajan — Classical, formal
- Montserrat — Modern, ultra-bold for headlines

**For gaming/entertainment:**
- Rajdhani — Modern, sharp (used in The Antigle)
- Pixel fonts — Retro gaming
- Bebas Neue — Bold, condensed
- Anton — Heavy impact

## Typography Pairing System

### Safe Pairings (Always Work)

| Headline Font | Body Font | Vibe |
|---------------|-----------|------|
| Inter (700+) | Inter (400) | Clean, modern |
| Satoshi (700+) | Satoshi (400) | Warm, modern |
| Playfair Display | Inter | Editorial, elegant |
| Fraunces | Satoshi | Premium, sophisticated |
| Cabinet Grotesk | General Sans | Bold, contemporary |
| Space Grotesk | Inter | Techy, modern |
| Montserrat (800) | Open Sans | Bold, reliable |
| Merriweather | Source Sans | Traditional, readable |
| Anton | Inter | Impactful, aggressive |
| Cormorant | Satoshi | Luxury, refined |

### Pairing Rules
- **Contrast is key** — Different weights, x-heights, or categories
- **Avoid conflict** — Don't pair two fonts with similar personality
- **Size hierarchy** — Headlines should be 2-4x body size
- **Weight hierarchy** — Headline heavy (600-900), body regular (400)
- **Limit to 2** — Rarely need more than two font families

## Typography Scale

### Modern Type Scale (1.25 ratio)

```
--text-xs:     0.75rem  (12px)   — Captions, meta, labels
--text-sm:     0.875rem (14px)   — Small text, secondary info
--text-base:   1rem     (16px)   — Body text, paragraphs
--text-lg:     1.125rem (18px)   — Large body, sub-descriptions
--text-xl:     1.25rem  (20px)   — Subheadings, feature titles
--text-2xl:    1.5rem   (24px)   — Section headings
--text-3xl:    1.875rem (30px)   — Major section headings
--text-4xl:    2.25rem  (36px)   — Page headings
--text-5xl:    3rem     (48px)   — Hero headings
--text-6xl:    3.75rem  (60px)   — Large hero headings
--text-7xl:    4.5rem   (72px)   — Massive hero, marketing
--text-8xl:    6rem     (96px)   — Monumental, brand statements
--text-9xl:    8rem     (128px)  — Largest, very rare
```

### Fluid Type with clamp()
```
--text-xs:     clamp(0.75rem, 0.7rem + 0.25vw, 0.875rem)
--text-base:   clamp(1rem, 0.9rem + 0.5vw, 1.125rem)
--text-3xl:    clamp(1.5rem, 1rem + 2vw, 2rem)
--text-5xl:    clamp(2rem, 1.5rem + 3vw, 3.5rem)
--text-7xl:    clamp(2.5rem, 1.5rem + 5vw, 5rem)
```

## Spacing & Readability

### Line Height (Leading)
```
--leading-tight:    1.1-1.2    — Headlines, short text
--leading-normal:   1.5-1.6    — Body paragraphs
--leading-relaxed:  1.7-1.8    — Long-form reading
--leading-loose:    2.0        — Accessibility needs, short content
```

### Letter Spacing (Tracking)
```
--tracking-tight:   -0.02em  — Large headlines (tighten)
--tracking-normal:  0        — Body text
--tracking-wide:    0.05em   — Uppercase, small text
--tracking-wider:   0.1em    — All caps, labels, badges
```

### Line Length
- Optimal: 45-75 characters per line
- Maximum: 80 characters (use max-width or columns)
- Minimum: 30 characters (short lines break reading rhythm)
- CSS: `max-width: 65ch` on text containers

### Paragraph Spacing
- Between paragraphs: 1.5x line height
- Between sections: 2-4x line height
- No indentation for web (use spacing instead)

## Typography for Different Screens

### Mobile (320-480px)
- Body: 16px minimum (prevents zoom)
- Headlines: clamp(1.5rem, 1rem + 2vw, 2rem)
- Line height: 1.5 minimum
- Line length: Auto (full width, 30-50 chars)
- Reduce headline size by 30-50% from desktop

### Tablet (768-1024px)
- Body: 16-18px
- Headlines: clamp(2rem, 1.5rem + 2vw, 3rem)
- Line length: ~60 chars ideal

### Desktop (1280px+)
- Body: 16-20px (18px optimal for reading)
- Headlines: 2-5rem depending on hierarchy
- Line length: Max 75ch

## Typography & Brand Personality

The font you choose communicates before a word is read:

| Font Choice | Communicates |
|-------------|--------------|
| Rounded sans (Nunito, Quicksand) | Friendly, playful, approachable |
| Sharp sans (Inter, Satoshi) | Professional, modern, efficient |
| Geometric sans (Montserrat, Futura) | Clean, precise, contemporary |
| Humanist sans (Source Sans, Noto Sans) | Friendly, readable, warm |
| Old-style serif (Garamond, Georgia) | Classic, trustworthy, traditional |
| Transitional serif (Times, Merriweather) | Formal, authoritative |
| Modern serif (Didot, Bodoni) | Fashionable, elegant, high-end |
| Slab serif (Roboto Slab, Rockwell) | Strong, bold, dependable |
| Mono (JetBrains Mono, Fira Code) | Technical, precise, developer-oriented |

## Typography in UI Components

### Navigation
- 14-16px for text links
- 500-600 weight
- Uppercase only for 2-3 word labels (design choice)
- Letter-spacing: 0.02-0.05em for uppercase

### Buttons
- 14-18px
- 500-700 weight
- Uppercase for primary CTA only (optional)
- Never use thin (300) or light weights

### Cards
- Title: 18-24px, 600+ weight
- Description: 14-16px, 400 weight
- Meta/tags: 12-14px, 400-500 weight, reduced contrast

### Forms
- Labels: 14px, 500 weight, above the field
- Input text: 16px (prevents mobile zoom)
- Helper text: 12-13px, muted color
- Error text: 12-13px, red, near the field

### Tables
- Header: 13-14px, 600 weight, uppercase optional
- Body: 13-14px, 400 weight
- Numbers: Right-aligned, monospace or tabular figures if available

## Web Font Performance

### Loading Strategy
```html
<!-- Preload for critical text -->
<link rel="preload" href="/fonts/inter-var.woff2" as="font" type="font/woff2" crossorigin>

<!-- CSS with swap (show fallback first) -->
@font-face {
  font-family: 'Inter';
  src: url('/fonts/inter-var.woff2') format('woff2');
  font-weight: 100 900;
  font-display: swap;
}
```

### Font Subsetting
Create subset files with only needed characters:
- Latin basic (A-Z, a-z, 0-9, punctuation) — 50-70% size reduction
- Use `glyphhanger` or `pyftsubset` for automated subsetting
- Never load full Unicode fonts for English-only sites

### File Size Targets
- Variable font: 20-100kb (WOFF2)
- Static weight: 15-40kb per weight (WOFF2)
- Load 2-3 weights maximum per family
- Combine variable fonts for best performance

### FOIT/FOUT Management
- **FOIT** (Flash of Invisible Text) — Bad: text hidden while font loads
- **FOUT** (Flash of Unstyled Text) — Better: fallback font shown first
- `font-display: swap` enables FOUT (preferred for web)
- `font-display: optional` if text must not cause layout shift (critical UI)
- Size fallback fonts to match: use `size-adjust` in `@font-face` if needed

## Typography CSS System

```css
:root {
  /* Font families */
  --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
  --font-serif: 'Merriweather', Georgia, 'Times New Roman', serif;
  --font-mono: 'JetBrains Mono', 'Fira Code', monospace;
  --font-display: 'Cabinet Grotesk', var(--font-sans);

  /* Type scale */
  --text-xs: 0.75rem;
  --text-sm: 0.875rem;
  --text-base: 1rem;
  --text-lg: 1.125rem;
  --text-xl: 1.25rem;
  --text-2xl: 1.5rem;
  --text-3xl: 1.875rem;
  --text-4xl: 2.25rem;
  --text-5xl: 3rem;

  /* Line heights */
  --leading-none: 1;
  --leading-tight: 1.15;
  --leading-snug: 1.35;
  --leading-normal: 1.5;
  --leading-relaxed: 1.65;
  --leading-loose: 2;

  /* Font weights */
  --font-light: 300;
  --font-normal: 400;
  --font-medium: 500;
  --font-semibold: 600;
  --font-bold: 700;
  --font-extrabold: 800;
}
```

## Typography Checklist

- [ ] Maximum 2 font families (3 only if there's a clear reason)
- [ ] Body text minimum 16px
- [ ] Line height 1.5 for body, 1.1-1.2 for headings
- [ ] Line length max 75ch
- [ ] Type scale with minimum 5 steps
- [ ] Fallback fonts specified
- [ ] Font-display: swap set
- [ ] Variable fonts preferred over multiple weights
- [ ] All caps text has wider letter-spacing
- [ ] Headings are at least 2x body size
- [ ] Colors have sufficient contrast on all text sizes
- [ ] Mobile text doesn't require zoom (16px minimum)
- [ ] Font files are WOFF2 format
- [ ] Preloaded critical fonts
