# 03 — Professional Color Systems

## Color Psychology

### What Colors Communicate

| Color | Emotions | Best For | Avoid For |
|-------|----------|----------|-----------|
| **Blue** | Trust, security, professionalism, calm | SaaS, finance, tech, healthcare | Food, entertainment (low appetite appeal) |
| **Green** | Growth, health, nature, wealth | Finance, health, environmental, SaaS | Luxury (traditional luxury uses black/gold) |
| **Red** | Urgency, passion, excitement, danger | Sales, entertainment, food, CTAs | Calm/meditation apps, healthcare |
| **Purple** | Creativity, luxury, wisdom, mystery | Beauty, creative tools, spirituality | Menswear, heavy industry |
| **Orange** | Enthusiasm, warmth, confidence, fun | Entertainment, food, creative, fitness | Corporate B2B, finance |
| **Yellow** | Optimism, clarity, warmth, caution | Kids, entertainment, food, attention-grabbing | Luxury, serious professional services |
| **Black** | Power, elegance, sophistication, premium | Luxury, fashion, premium brands | Content-heavy reading sites |
| **White** | Cleanliness, simplicity, purity, openness | Healthcare, minimal design, everything | Dark/moody brands |
| **Pink** | Playful, feminine, creative, warm | Beauty, fashion, creative tools | Corporate B2B, traditional brands |
| **Gray** | Neutral, professional, mature, stable | Backgrounds, text, secondary elements | Primary brand color (too safe) |
| **Gold** | Premium, success, luxury, quality | Badges, awards, luxury accents | Primary UI color (hard to read) |

### Cultural Color Awareness
- White: Purity (West) / Mourning (East)
- Red: Good luck (China) / Danger (West)
- Green: Nature (West) / Sacred (Islam)
- Purple: Royalty (West) / Mourning (Brazil, Thailand)

## Building a Color System

### Core Colors
1. **Primary** — Main brand color, used for CTAs, key UI
2. **Secondary** — Supporting color, used for accents, less prominent UI
3. **Accent** — Used sparingly for highlights, special elements

### Neutrals
A good neutral scale has 8-12 steps:
```
50   #F9FAFB   (lightest — page bg)
100  #F3F4F6   (card bg)
200  #E5E7EB   (border, divider)
300  #D1D5DB   (disabled)
400  #9CA3AF   (placeholder)
500  #6B7280   (secondary text)
600  #4B5563   (body text)
700  #374151   (heading text)
800  #1F2937   (dark UI)
900  #111827   (darkest, near-black)
```

### Semantic Colors
- **Success** — Green (#10B981 or similar)
- **Warning** — Amber/Orange (#F59E0B)
- **Error** — Red (#EF4444)
- **Info** — Blue (#3B82F6)

### Dark Mode Colors
Never simply invert light mode. Design a separate palette:
- Background: #0F0F0F to #1A1A2E range
- Surface/cards: slightly lighter than BG (2-5% lighter)
- Text: #E0E0E0 to #FFFFFF
- Muted: #888888 range
- Primary: Keep same or lighten slightly

## 100+ Professional Color Palettes

### SaaS & Startup Palettes

**1. Linear-style (Minimal Blue)**
- #5E6AD2 (primary purple-blue)
- #FFFFFF, #F5F5F5 (backgrounds)
- #1A1A2E (dark text)
- #10B981 (success green)
- *Why it works: Clean, modern, trustworthy. Common among dev tools.*

**2. Stripe-style (Dark Purple)**
- #635BFF (primary purple)
- #0A2540 (dark navy)
- #00D4AA (teal accent)
- #FFFFFF, #F6F9FC (light bg)
- *Why it works: Bold contrast. Dark bg makes bright purple pop.*

**3. Notion-style (Clean Gray)**
- #FFFFFF (pure white bg)
- #37352F (near-black text)
- #E1625F (red accent for highlights)
- #2383E2 (blue for links)
- #F7F6F3 (sidebar bg)
- *Why it works: Content-forward. Colors recede, leaving text as hero.*

**4. Vercel-style (Dark + White)**
- #000000 (pure black)
- #FFFFFF (pure white)
- #0070F3 (blue accent)
- #666666 (medium gray)
- *Why it works: Maximum contrast. Monochrome with one accent.*

**5. Tailwind-style (Indigo)**
- #6366F1 (indigo primary)
- #0F172A (dark slate)
- #22C55E (green)
- #F59E0B (amber)
- #EC4899 (pink)
- *Why it works: Versatile, modern, works in light and dark mode.*

**6. Supabase-style (Dark Green)**
- #3ECF8E (bright green)
- #18181B (near-black)
- #F5F5F5 (light bg)
- #1EB854 (darker green)
- *Why it works: Green = growth. Distinctive in SaaS space.*

**7. Render-style (Deep Purple)**
- #1E1E2E (dark purple bg)
- #7C3AED (vivid purple)
- #10B981 (teal)
- #F59E0B (amber)
- *Why it works: Rich, developer-focused, premium feel.*

**8. Cal.com-style (Bright Red-Orange)**
- #292929 (dark bg)
- #FF5C00 (vivid orange)
- #FFFFFF (white)
- #8B8B8B (gray)
- *Why it works: High-energy, memorable. Subverts blue SaaS norm.*

**9. Dub-style (Emerald)**
- #0D0D0D (near-black)
- #10B981 (emerald green)
- #F5F5F5 (light bg)
- #6EE7B7 (light green)
- *Why it works: Fresh, distinctive. Green = growth, money, success.*

**10. PlanetScale-style (Blue-Teal)**
- #0A1E2A (dark blue bg)
- #35DDBF (teal accent)
- #E2E8F0 (light text on dark)
- #172554 (dark blue card)
- *Why it works: Sophisticated dark mode. Deep blues feel enterprise.*

### Premium / Luxury Palettes

**11. Apple-style (Pure Minimal)**
- #F5F5F7 (warm light gray bg)
- #1D1D1F (dark text)
- #0071E3 (blue link)
- #FFFFFF (white cards)
- *Why it works: Maximum whitespace. Typography and photography do the work.*

**12. Chanel-style (Black + White + Gold)**
- #000000 (pure black)
- #FFFFFF (pure white)
- #C9A84C (gold accent)
- #F5F5F5 (light gray)
- *Why it works: Timeless. Gold adds warmth to stark black/white.*

**13. Minimal Luxury (Warm Neutrals)**
- #FDFBF7 (warm white bg)
- #2D2A24 (warm dark text)
- #C8A27E (rose gold accent)
- #E8DED1 (warm beige)
- *Why it works: Warmth feels premium. Beige = sophistication.*

**14. Modern Luxury (Charcoal + Sage)**
- #1A1A1A (near-black)
- #D4D4C8 (warm gray text)
- #9CAF88 (sage green)
- #2D2D2D (dark cards)
- *Why it works: Understated. Color recedes, letting material quality speak.*

**15. High-End Fashion (Oxblood)**
- #1A0A0E (near-black with red tint)
- #FFFFFF (white)
- #8B2240 (oxblood red)
- #D4A574 (gold accent)
- *Why it works: Dramatic, emotional. Red undertones feel passionate.*

### Gaming Palettes

**16. Cyberpunk (Neon Purple + Cyan)**
- #0D0221 (deep purple-black)
- #FF2E7E (hot pink)
- #00FFF0 (cyan)
- #B200FF (purple)
- *Why it works: High energy. Neon against dark = classic gaming aesthetic.*

**17. Valorant-style (Red + White + Dark Blue)**
- #111122 (dark navy bg)
- #FF4655 (striking red)
- #FFFFFF (white text)
- #0F1923 (alternate dark)
- *Why it works: Red creates urgency. Clean, competitive feel.*

**18. Minecraft-style (Warm Earth)**
- #1A1A2E (dark)
- #5CBF63 (grass green)
- #8B5CF6 (purple accent)
- #D4A574 (warm brown)
- *Why it works: Earthy tones match game aesthetic. But modernized.*

**19. Fortnite-style (Bright Pop)**
- #1C1C3A (dark purple)
- #FF00FF (magenta)
- #00FFFF (cyan)
- #FFD700 (gold)
- #FF3366 (pink)
- *Why it works: Vibrant, playful. Maximum saturation = fun.*

**20. Dark Gaming (Red + Black)**
- #0A0A0A (pure black)
- #FF1A1A (red)
- #CCCCCC (gray text)
- #1A1A1A (dark cards)
- *Why it works: Aggressive, intense. Common for competitive gaming.*

**21. Arcade Retro (Neon Grid)**
- #0F0F23 (dark blue)
- #FF00FF (pink)
- #00FF00 (green)
- #FFFF00 (yellow)
- *Why it works: Nostalgic. Pixel-perfect for retro-themed sites.*

**22. Gaming Creator (Vibrant Purple + Cyan)**
- #1A0A2E (deep purple)
- #A855F7 (bright purple)
- #22D3EE (cyan)
- #F5F5F5 (white text on dark)
- *Why it works: Modern creator aesthetic. Purple = gaming community.*

### Creator & Personal Brand Palettes

**23. Clean Creator (White + Teal)**
- #FFFFFF (white)
- #0D9488 (teal)
- #1A1A2E (dark text)
- #F0FDFA (light teal bg)
- *Why it works: Fresh, approachable. Teal is unique but not loud.*

**24. Bold Creator (Dark + Yellow)**
- #1A1A1A (dark)
- #FACC15 (yellow)
- #FFFFFF (white)
- #333333 (gray)
- *Why it works: Yellow = optimism, creativity. Stands out in feeds.*

**25. Warm Creator (Cream + Coral)**
- #FEF9EF (cream bg)
- #FF6B6B (coral)
- #2D3436 (dark text)
- #FFEAA7 (light yellow)
- *Why it works: Warm, inviting. Feels personal and friendly.*

**26. Minimal Creator (Gray + One Color)**
- #FAFAFA (light bg)
- #1A1A1A (dark text)
- #FF5757 (single accent red)
- #E5E5E5 (borders)
- *Why it works: Content-first. Accent color directs attention.*

**27. Tech Creator (Dark + Gradient)**
- #0F172A (slate 900)
- blue-500 to purple-500 gradient
- #94A3B8 (muted text)
- #38BDF8 (light blue)
- *Why it works: Modern developer aesthetic. Gradients add depth.*

**28. Lifestyle Creator (Pastel)**
- #FDE68A (soft yellow)
- #FCA5A5 (soft pink)
- #67E8F9 (soft cyan)
- #FFFFFF (white)
- *Why it works: Soft, dreamy. Popular on Instagram -> web.*
- *When NOT to use: Serious/professional services, B2B.*

### Ecommerce Palettes

**29. Fashion Ecommerce (Black + White + Hot Pink)**
- #000000 (black)
- #FFFFFF (white)
- #FF1493 (hot pink accent)
- #F5F5F5 (light gray)
- *Why it works: High contrast makes products pop. Pink = feminine fashion.*

**30. Premium Ecommerce (Navy + Gold)**
- #1B1B2F (navy)
- #D4AF37 (gold)
- #F5F5F5 (light gray)
- #FFFFFF (white)
- *Why it works: Navy = trust. Gold = premium. Classic luxury combo.*

**31. Modern Ecommerce (White + Slate + Green)**
- #FFFFFF (white)
- #0F172A (dark slate)
- #10B981 (emerald green accent)
- #F1F5F9 (light slate)
- *Why it works: Clean product focus. Green = "buy" psychologically.*

**32. Organic Ecommerce (Earth Greens)**
- #F0FDF4 (light green)
- #166534 (dark green)
- #D4A574 (warm brown)
- #F5F5F5 (white)
- *Why it works: Natural, organic. Trustworthy for health/eco products.*

**33. Luxury Beauty (Rose + Gold)**
- #FDF2F8 (light pink)
- #BE185D (deep rose)
- #D4AF37 (gold accents)
- #1A1A1A (dark text)
- *Why it works: Feminine, luxurious. Rose = beauty standard.*

### Dark Mode Primary Palettes

**34. Vibrant Purple Dark**
- BG: #0F0A1E
- Primary: #A855F7
- Text: #E2E8F0
- Muted: #6B7280
- Accent: #22D3EE (cyan)

**35. Electric Blue Dark**
- BG: #0A0F1E
- Primary: #3B82F6
- Text: #F1F5F9
- Muted: #64748B
- Accent: #F59E0B (amber)

**36. Matrix Green Dark**
- BG: #0A0A0A
- Primary: #22C55E
- Text: #E0E0E0
- Muted: #6B7280
- Accent: #A855F7

**37. Sunset Dark**
- BG: #1A0A0A
- Primary: #FF6B6B
- Text: #E2E8F0
- Muted: #9CA3AF
- Accent: #FACC15

**38. Ocean Dark**
- BG: #0A1628
- Primary: #60A5FA
- Text: #E2E8F0
- Muted: #64748B
- Accent: #34D399

### Gradient Systems

**39. Purple to Blue (Vercel-style)**
`from #6366F1 to #3B82F6`

**40. Pink to Purple (Linear-style)**
`from #EC4899 to #8B5CF6`

**41. Orange to Red (Warm)**
`from #F97316 to #EF4444`

**42. Cyan to Teal (Fresh)**
`from #22D3EE to #14B8A6`

**43. Indigo to Pink (Vibrant)**
`from #4F46E5 to #EC4899`

**44. Green to Teal (Growth)**
`from #22C55E to #14B8A6`

**45. Sunset Gradient**
`from #F59E0B via #EF4444 to #EC4899`

**46. Midnight Gradient**
`from #0F172A via #1E1B4B to #0F0A1E`

**47. Gold Gradient**
`from #D4AF37 to #F5D76E`

**48. Glass Gradient (for glassmorphism)**
`from rgba(255,255,255,0.1) to rgba(255,255,255,0.05)`

### Glassmorphism Color Guide

**When it works:** Hero sections, cards, navbars, modals over complex backgrounds
**When it fails:** Heavy text content, data-heavy UIs, accessibility-critical interfaces

**Key colors:**
- Background must be visible through the glass (gradient, image, or pattern)
- Glass element: `background: rgba(255, 255, 255, 0.1-0.2)`
- Border: `rgba(255, 255, 255, 0.2)`
- Shadow: Layered `box-shadow` for depth
- Blur: `backdrop-filter: blur(10-20px)`

**Frosted Glass dark variant:**
- `background: rgba(0, 0, 0, 0.2)`
- `border: rgba(255, 255, 255, 0.05)`
- `backdrop-filter: blur(20px)`

### Neumorphism Color Guide

**When it works:** UI mockups, music apps, design tools, iOS-style components
**When it fails:** Content-heavy pages, text-heavy interfaces, accessibility-critical

**Core principle:**
- Base color + two shadows (light source from top-left)
- Works best on mid-tone backgrounds (20-60% gray)

**Key colors:**
- BG: #E0E0E0 (or similar mid-tone)
- Shadow-light: #FFFFFF (or lighter version of BG)
- Shadow-dark: #A0A0A0 (or darker version of BG)
- Raised element: lighter + dark shadow bottom-right
- Inset element: darker + light shadow bottom-right

## Accessibility & Color

### WCAG Contrast Ratios
- **AA Normal text** — 4.5:1 minimum
- **AA Large text** (18px+ / 14px bold+) — 3:1 minimum
- **AAA Normal text** — 7:1 minimum
- **AAA Large text** — 4.5:1 minimum
- **UI components** (borders, icons) — 3:1 minimum

### Quick Contrast Check

**Common failing combinations:**
- Gray on white (#999 on #FFF = 2.7:1 — FAIL)
- Blue on black (#0070F3 on #000 = 2.3:1 — FAIL)
- Yellow on white (#FFD700 on #FFF = 1.2:1 — FAIL)

**Common passing combinations:**
- Black on white (#000 on #FFF = 21:1 — PASS AAA)
- White on blue (#FFF on #0070F3 = 6.8:1 — PASS AA)
- Dark gray on white (#333 on #FFF = 11.5:1 — PASS AAA)

### Color Blindness Considerations
- 8% of men have some form of color blindness
- Never rely solely on color to convey information
- Use icons + text + patterns in addition to color
- Test with filters: Deuteranopia, Protanopia, Tritanopia
- Red/green is the most common deficiency
- Blue/orange is the safest high-contrast pair

## Color Hierarchy System

For any website, assign colors by function:

```
--color-brand-primary:    #... (main CTA, key UI)
--color-brand-secondary:  #... (supporting accents)
--color-bg:               #... (page background)
--color-surface:          #... (card, sidebar backgrounds)
--color-text-primary:     #... (headings, body text)
--color-text-secondary:   #... (meta, captions, labels)
--color-text-muted:       #... (placeholders, disabled)
--color-border:           #... (dividers, borders)
--color-success:          #... (positive feedback)
--color-warning:          #... (caution states)
--color-error:            #... (error states)
--color-info:             #... (informational)
```

## Color Application Rules

1. **One job per color** — Primary = CTAs. Don't use it for borders
2. **Less is more** — 3-4 colors max for most interfaces
3. **Neutrals do the heavy lifting** — 80-90% of UI should be neutral
4. **Accent proportion** — Accent color should cover <10% of the page
5. **Dark mode is not inverted** — Design separate luminance relationships
6. **Test on real screens** — Colors look different on OLED vs LED vs LCD
7. **Consider brand context** — A color that works for FinTech may fail for Gaming
8. **Build a system, not a palette** — Colors need roles, not just hex values
