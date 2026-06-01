# 08 — SaaS & Startup Design

## SaaS Design Principles

SaaS websites have unique requirements compared to other sites:
- **Trust is everything** — Users are committing to recurring payment
- **Complexity must feel simple** — Powerful features, clear interface
- **Value must be instant** — Show ROI immediately
- **Onboarding is a product** — First experience determines retention
- **Performance is expected** — Sub-second loads are table stakes

## Homepage Structure (SaaS)

```
[NAVBAR] — Logo | Features | Pricing | About | Blog | [CTA Button]
[HERO] — Headline + subheadline + CTA + hero image/demo
[SOCIAL PROOF] — Logo bar / user count / testimonials
[PROBLEM/ SOLUTION] — "You have X problem. We solve it."
[FEATURES] — Grid, bento, or alternating rows
[HOW IT WORKS] — 3 steps
[INTEGRATIONS] — Partner logos
[TESTIMONIALS] — Customer quotes with results
[PRICING] — Tier cards with monthly/annual toggle
[FAQ] — Objections addressed
[FINAL CTA] — "Start free trial" (full-width)
[FOOTER] — Links, legal, social, sitemap
```

### SaaS Color Schemes
Most successful SaaS companies use:
- **Blue** (trust, reliability) — Salesforce, HubSpot, Slack
- **Purple** (innovation, creativity) — Linear, Notion (purple-ish)
- **Green** (growth, wealth) — Supabase, Cal.com
- **Dark + accent** (premium, developer) — Vercel, Stripe

### Common SaaS Sections

**Integrations Section:**
- Grid of partner logos
- "Works with X, Y, Z"
- Searchable for many integrations
- Interactive: click to see integration details

**Security/ Compliance Section:**
- Badges (SOC 2, GDPR, HIPAA)
- Encryption explanation
- Uptime guarantee
- Data center locations map

**Enterprise Section:**
- Enterprise features list
- SSO, audit logs, custom contracts
- Customer success stories (large companies)
- "Talk to sales" CTA

## Pricing Page Design

### Pricing Structure Options

**Flat-rate pricing:**
One plan, one price. Simple but limiting.
Best for: Simple tools with broad appeal.

**Usage-based pricing:**
Pay for what you use. Scales naturally.
Best for: APIs, cloud services, dev tools.

**Per-seat pricing:**
Price per user. Grows with team.
Best for: Collaboration tools, project management.

**Tiered (3 plans):**
Basic → Pro → Enterprise. Most common.
Best for: Most SaaS products.

### Pricing Page Layout
```
[HEADER] — Transparent pricing, no hidden fees
[TOGGLE] — Monthly / Annual (save 20%)
[CARDS] — 3 columns: Starter | Pro (★) | Enterprise
[COMPARISON TABLE] — Full feature breakdown
[FAQ] — Questions about billing, plans, switching
[CTA] — "Still unsure? Start free trial"
```

### Pricing Card Detail
```
┌─────────────────┐
│   PRO PLAN      │  ← Tier name
│  ★ MOST POP ★  │  ← Badge
├─────────────────┤
│   $29/mo        │  ← Price (per month or user)
│  or $290/yr     │  ← Annual price with savings
├─────────────────┤
│  Everything in  │
│  Starter, plus: │
│  ✓ Feature 1    │
│  ✓ Feature 2    │
│  ✓ Feature 3    │
│  ✓ Feature 4    │
├─────────────────┤
│  [Start Trial]  │  ← Button
│  No CC required │  ← Friction-reducer
└─────────────────┘
```

## Onboarding Flow Design

### Onboarding Stages

**Stage 1: Account Creation**
- Email + password (or OAuth)
- Optional: name, company
- No credit card for free trial
- 5-10 seconds max

**Stage 2: Quick Setup**
- Select use case / role (1-3 options)
- Connect integrations if needed
- Import data (optional)
- 30-60 seconds

**Stage 3: First "Aha" Moment**
- Guided first action
- See value instantly
- Progress indicator showing setup completion
- 1-2 minutes

**Stage 4: Deepening**
- Feature discovery prompts
- Team invitations
- Advanced settings
- Days 2-7

### Onboarding UX Rules
- **Less is more** — Only ask what's essential
- **Show progress** — "3 of 5 steps complete"
- **Allow skipping** — Every step should be skippable
- **Celebrate milestones** — Confetti, success messages
- **Don't ask for payment early** — Value before credit card
- **Templates > blank** — Pre-built templates reduce empty-state paralysis

## Dashboard UI Design

### SaaS Dashboard Components

**KPI Cards:**
- 3-6 key metrics
- Each card: icon, metric name, value, trend (up/down), sparkline
- Link to detail view

**Main Chart:**
- Revenue, users, or primary metric
- Time range selector (7d, 30d, 90d, 1y)
- Interactive (hover for values, click to drill down)

**Secondary Content:**
- Recent activity feed
- Quick actions panel
- Alerts/ notifications
- Team member list/ online status

**Navigation:**
- Sidebar (desktop), bottom tab (mobile)
- Clear icons + labels
- Active state indication
- Collapse on mobile

### SaaS Design Patterns

**Empty States:**
```
┌─────────────────────────┐
│                         │
│   [Friendly Illustration]
│                         │
│   "No projects yet"     │
│   "Create your first    │
│    project to get       │
│    started."            │
│                         │
│   [Create Project]      │  ← Primary CTA
│                         │
│   Watch quick tutorial  │  ← Secondary link
│                         │
└─────────────────────────┘
```

**Loading States:**
- Skeleton screens (preferred over spinners)
- Shimmer animation matching layout
- Mimic final content structure

**Error States:**
- Friendly messaging (not technical)
- Actionable: "Try again" or "Contact support"
- Maintain UI structure (don't break layout)

## Startup Landing Page Variations

### Beta Launch
- "Get early access" — Waitlist form
- Limited spots countdown
- Founder story
- Early adopter benefits

### Post-Launch (Growth)
- "Trusted by X companies" — Social proof heavy
- Case studies
- Free trial + demo
- Comparison vs competitors

### Enterprise-Focused
- ROI calculator
- Security badges prominent
- Customer stories (enterprise logos)
- "Talk to sales" — Not self-serve

### Developer-Focused
- Code snippet in hero
- GitHub stars, npm downloads
- API-first messaging
- Documentation link
- No fluff, straight to value

## SaaS Conversion Optimization

**Free Trial Friction Reducers:**
- No credit card required
- Email-only signup (no password)
- Pre-populated demo data
- Guided first tour

**Demo Request Page:**
- Calendar picker (not email back-and-forth)
- Pre-recorded demo option (auto-play)
- Specific use case selection (personalize demo)

**Enterprise Sales Page:**
- Case studies with specific results
- Security compliance badges
- Integrations count
- SLA/ uptime guarantee
- "Talk to sales" with direct calendar link

## SaaS Design Anti-Patterns

| ❌ Bad | ✅ Better |
|--------|-----------|
| Generic stock photos | Product screenshots or custom illustrations |
| Walls of feature text | Benefit-driven, scannable |
| Weak CTA ("Learn More") | Action-oriented ("Start free trial") |
| Hidden pricing | Transparent, upfront |
| No social proof on hero | Logo bar or user count |
| Over-designed forms | Minimal, single-column |
| Too many nav items | 4-5 essential links |
| Auto-playing videos with sound | Autoplay muted, user initiates sound |
| No mobile pricing view | Mobile-optimized pricing cards |
| Unclear value prop | Clear, specific headline |

## SaaS Page Speed Checklist

- [ ] First load under 2 seconds
- [ ] Time to interactive under 3 seconds
- [ ] Lighthouse performance score 90+
- [ ] Images optimized (WebP, compressed)
- [ ] Fonts loaded with swap display
- [ ] Code splitting for route-based chunks
- [ ] Lazy load below-fold content
- [ ] CDN for static assets
- [ ] Minified CSS/ JS
- [ ] Server-side rendering or static generation where possible
