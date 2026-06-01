# 02 — UI-UX Mastery

## UX Design Foundations

### User Experience Layers
1. **Strategy** — User needs + product objectives
2. **Scope** — Features + content requirements
3. **Structure** — Information architecture + interaction design
4. **Skeleton** — Layout + navigation + interface design
5. **Surface** — Visual design (colors, typography, spacing)

### UX Research Methods

**Before building:**
- **User interviews** — 1-on-1 conversations about needs, pain points
- **Surveys** — Quantitative data from larger audiences
- **Competitive analysis** — What competitors do well/poorly
- **Analytics review** — Existing data on user behavior

**During/after building:**
- **Usability testing** — Watch users attempt tasks, note friction
- **A/B testing** — Compare two versions, pick the winner
- **Heatmaps** — See where users click, scroll, hover
- **Session recordings** — Watch real user sessions
- **Feedback widgets** — In-app feedback collection

### Information Architecture
How content is organized, labeled, and navigated:

- **Hierarchy** — Tree structure with parent/child pages
- **Breadth vs Depth** — Wide nav (many top items) vs deep nav (many levels)
- **Flat vs Nested** — Flat for simple sites, nested for complex
- **Taxonomy** — Consistent labeling system
- **Faceted navigation** — Multiple filter dimensions (price, category, rating)

### Navigation Patterns
- **Top navbar** — Most common, works for 4-7 items
- **Sidebar** — Good for dashboards, docs (many items)
- **Hamburger menu** — Mobile standard, hides nav behind icon
- **Mega menu** — Large dropdown with categories, images (ecommerce)
- **Bottom tab bar** — Mobile app navigation (1-5 items)
- **Breadcrumbs** — Shows current location, enables backtracking
- **Sticky nav** — Stays visible while scrolling
- **Progress nav** — Shows step progression (checkout flows)

## UI Design Patterns

### Hero Sections
**Purpose:** Capture attention, communicate value, drive action

**Anatomy:**
- Headline (5-12 words, benefit-focused)
- Subheadline (1-2 sentences elaborating)
- Primary CTA button
- Optional: secondary link, social proof, hero image/video, stats

**Variations:**
- **Split hero** — Text left, image right
- **Centered hero** — Everything centered (SaaS common)
- **Full-screen hero** — Takes full viewport height
- **Minimal hero** — Just headline + CTA (Apple style)
- **Video hero** — Background video playing
- **3D hero** — Interactive 3D scene
- **Animated hero** — Lottie/Rive animation

### Feature Sections
**Purpose:** Explain what the product/service does

**Layout options:**
- **Grid of cards** — 3 columns, icon + title + description
- **Alternating rows** — Image left → text right, then swap
- **Single feature highlight** — Large image with offset text
- **Bento grid** — Irregular grid with different-sized cells
- **Timeline** — Features shown chronologically
- **Interactive demo** — Live product mockup

### CTA (Call to Action) Design

**Best practices:**
- Make it visually distinct (contrasting color, more weight)
- Use action-first language ("Start your free trial")
- Create urgency naturally ("Join 10,000+ creators")
- Position after value is established
- Repeat 2-3 times per page (hero, mid-page, footer)
- Minimize friction (one click, not a form)

**Button states:**
- Default (resting)
- Hover (subtle change — darken, lift, glow)
- Active/click (momentary feedback)
- Loading (spinner or progress)
- Disabled (grayed out, only if necessary)
- Success (confirmation)

### Pricing Tables

**Tier structure:**
- 3 tiers is optimal (good, better, best)
- Highlight the recommended tier ("Most popular" badge)
- Free tier if applicable (lowest friction)
- Enterprise tier (hidden or custom pricing)

**Elements per tier:**
- Tier name
- Price (monthly/annual toggle)
- Key feature list (5-10 items)
- CTA button
- Feature comparison checkmarks

### Testimonials & Social Proof

**Types:**
- Quote cards (photo + name + role + quote)
- Logo bar (trusted by X companies)
- Case study previews (stats + quote)
- Video testimonials
- Rating/ review stars
- User count ("Join 50,000+")

**Best practices:**
- Real photos, not stock
- Specific results ("Increased sales by 40%")
- Include name, title, company for credibility
- Video over text where possible
- Carousel or grid layout

### Forms

**Conversion killers to avoid:**
- Optional fields that aren't optional
- Asking for too much information upfront
- No inline validation
- Unclear error messages
- No progress indicator for multi-step forms
- Generic placeholder text that disappears

**Best practices:**
- Single-column layout (faster completion)
- Labels outside fields (always visible)
- Inline validation (check after user finishes each field)
- Smart defaults and autocomplete
- Error messages near the field, not at top
- Show password requirements before submission
- Mobile-friendly input types (type="email", type="tel")

## Micro-interactions

Small, functional animations that give feedback:

**Types:**
- **Hover** — Button darkens, card lifts, link underlines
- **Click** — Button presses, toggle flips
- **Scroll** — Progress bar fills, nav changes style
- **Load** — Skeleton shimmer, progress bar, spinner
- **Empty** — Illustration + message (not blank page)
- **Error** — Shake animation, inline error appearing
- **Success** — Checkmark animation, green flash
- **Drag** — Element follows cursor, snap on release

**Design rules:**
- Duration: 200-300ms (too fast = missed, too slow = annoying)
- Easing: ease-out for most (natural deceleration)
- Purpose-driven: every micro-interaction must communicate something
- Don't animate critical UX (payment errors, validation)

## Mobile UX

### Thumb Zone
The screen area reachable by thumb:
- **Easy** — Bottom 1/3 of screen (primary actions here)
- **Stretch** — Middle 1/3
- **Hard** — Top 1/3 (least reachable, put less important items)

### Mobile Nav Conventions
- Bottom tab bar (1-5 tabs) — best for thumb reach
- Hamburger menu (more items) — second best
- Top navbar with back button — standard for sub-pages
- Swipe gestures — back, dismiss, navigate between tabs

### Mobile Form Design
- Input fields: full width, large touch targets
- Dropdowns: use native select when possible
- Date pickers: use platform-native
- Keyboard: correct type for each field (email, number, tel)
- Auto-focus first field, next button goes to next field
- Large enough tap targets (min 44px)

## Onboarding UX

**Goal:** Get users to the "aha moment" as fast as possible

**Types:**
- **Value-first** — Let them use the product, explain as they go
- **Tour** — Step-by-step walkthrough (least effective, skip if possible)
- **Checklist** — Progressive tasks to complete setup
- **Demo** — Show the product in action before they try

**Rules:**
- Collect minimum info to start
- Show progress ("3 of 5 steps complete")
- Allow skipping
- Don't ask for payment too early
- Celebrate milestones

## Error UX

**Good error messages:**
- What happened (in plain language)
- Why it happened (if helpful)
- How to fix it (actionable)
- No blame ("Something went wrong" not "You entered wrong data")

**404 pages:**
- Apologize briefly
- Explain what might have happened
- Offer navigation options (home, search, popular pages)
- Keep brand personality (funny = ok, but keep it useful)

## Landing Page UX Flow

The ideal user journey:
1. **Attract** — Headline matches what they searched for
2. **Engage** — Subheadline and hero build interest
3. **Social Proof** — They see others trust you
4. **Explain** — Features clearly articulated
5. **Visualize** — They see the product working
6. **Overcome** — FAQs address objections
7. **Convert** — CTA is clear, easy, low-commitment
8. **Reassure** — Money-back guarantee, support available
9. **Follow Up** — Thank you page with next steps

## UX Laws for Web Design

| Law | Meaning | Application |
|-----|---------|-------------|
| **Jakob's Law** | Users prefer familiar patterns | Don't reinvent navigation, search, checkout |
| **Fitts's Law** | Bigger + closer = faster | Make CTAs large, place near content |
| **Hick's Law** | More choices = slower decisions | Limit options, progressive disclosure |
| **Miller's Law** | Average human can hold 7(±2) items | Chunk content, limit nav items |
| **Postel's Law** | Be conservative in what you send, liberal in what you accept | Flexible inputs, forgiving forms |
| **Tesler's Law** | Some complexity is essential | Move complexity to system, not user |
| **Von Restorff Effect** | Unique elements stand out | Make CTA distinct from other elements |
| **Serial Position Effect** | Users remember first and last items best | Place key info at top/bottom of lists |
| **Aesthetic-Usability Effect** | Attractive designs feel more usable | Invest in visual design, it improves perceived usability |
| **Doherty Threshold** | Productivity soars when UI responds <400ms | Optimize load times, instant feedback |
