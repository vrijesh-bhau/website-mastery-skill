# 20 — Complete Website Checklists

## Pre-Development Checklist

### Strategy & Planning
- [ ] Website purpose clearly defined
- [ ] Target audience identified and documented
- [ ] Primary goal/ conversion defined
- [ ] Key performance indicators (KPIs) established
- [ ] Competitor analysis completed
- [ ] Content strategy defined
- [ ] Site map created (all pages)
- [ ] User flow mapped (how users navigate)
- [ ] Tech stack chosen and justified
- [ ] Hosting/ deployment platform selected
- [ ] Domain name selected (or existing)

### Design Preparation
- [ ] Brand guidelines available (colors, fonts, logos)
- [ ] Color system defined (primary, secondary, neutrals, semantic)
- [ ] Typography system defined (font families, scale, weights)
- [ ] Spacing system defined (consistent scale)
- [ ] Design inspiration collected (5+ references)
- [ ] Wireframes/ mockups created for key pages
- [ ] Mobile-first layouts approved
- [ ] Content for all pages prepared (or placeholders)
- [ ] Image assets collected/ created
- [ ] Icon set selected (or to be created)

### Technical Setup
- [ ] Version control initialized (git)
- [ ] Project scaffolding created
- [ ] Build tool configured (if applicable)
- [ ] CSS setup complete (variables, reset, base styles)
- [ ] Font loading configured (preload, swap, subset)
- [ ] Meta tags template created
- [ ] SEO foundation: title tag, description, OG tags
- [ ] Analytics account set up (GA, Plausible, etc.)
- [ ] Favicon created
- [ ] 404 page planned

## Development Checklist

### HTML/ Structure
- [ ] Semantic HTML5 elements used (header, nav, main, section, footer)
- [ ] Heading hierarchy correct (h1 → h2 → h3, not skipping levels)
- [ ] h1 present on every page (unique, descriptive)
- [ ] All links have href (no broken links)
- [ ] All images have alt text (meaningful descriptions)
- [ ] Forms have proper labels and accessible validation
- [ ] ARIA attributes where HTML semantics insufficient
- [ ] Skip-to-content link present (accessibility)
- [ ] Landmarks defined (banner, navigation, main, complementary, contentinfo)

### CSS/ Styling
- [ ] CSS custom properties used for design tokens
- [ ] Responsive design: mobile, tablet, desktop tested
- [ ] No hard-coded pixel values where relative units work better (rem, em, %)
- [ ] Fluid typography with clamp() where appropriate
- [ ] Consistent spacing rhythm
- [ ] No browser-specific hacks (or documented)
- [ ] Print stylesheet considered (or at least not breaking)
- [ ] `prefers-reduced-motion` media query implemented
- [ ] `prefers-color-scheme` for dark mode (if applicable)
- [ ] Transitions on interactive elements (hover, focus, active)
- [ ] No `!important` (or very few, documented)

### JavaScript/ Interactivity
- [ ] No console errors at any stage
- [ ] JavaScript works without errors on all target browsers
- [ ] Progressive enhancement: core functionality works without JS
- [ ] Event listeners properly attached and cleaned up
- [ ] No memory leaks (check with performance tools)
- [ ] Debouncing/ throttling on scroll/ resize events
- [ ] Async/defer on non-critical scripts
- [ ] Animations GPU-accelerated (transform, opacity only)
- [ ] Reduced motion respected
- [ ] Forms have client-side validation (with server-side backup)

### Performance
- [ ] Images optimized (WebP, proper dimensions, compressed)
- [ ] Images lazy-loaded below the fold
- [ ] Critical CSS inlined (or loaded early)
- [ ] Non-critical CSS deferred
- [ ] JavaScript code-split (route-based chunks)
- [ ] Font display: swap configured
- [ ] No render-blocking resources above the fold
- [ ] Preload key resources (fonts, hero image)
- [ ] Preconnect to required origins (fonts, analytics)
- [ ] Lighthouse score: 90+ Performance, 90+ Accessibility
- [ ] Total page size under 1MB (ideally under 500kb)
- [ ] Time to Interactive under 3 seconds (3G)

### SEO
- [ ] Unique title tag per page (50-60 characters)
- [ ] Unique meta description per page (150-160 characters)
- [ ] Open Graph tags (og:title, og:description, og:image, og:url)
- [ ] Twitter Card tags
- [ ] Canonical URL set on each page
- [ ] robots.txt present and correct
- [ ] sitemap.xml generated and submitted
- [ ] Structured data/ schema markup (JSON-LD where applicable)
- [ ] Semantic HTML for content hierarchy
- [ ] Clean URL structure (no query params for content pages)
- [ ] SSL/ HTTPS enforced
- [ ] No duplicate content issues

### Accessibility
- [ ] Color contrast meets WCAG AA (4.5:1 text, 3:1 large text)
- [ ] Focus indicators visible on all interactive elements
- [ ] All functionality available via keyboard
- [ ] No keyboard traps
- [ ] Form inputs have associated labels
- [ ] Error messages clear and helpful
- [ ] Images have meaningful alt text
- [ ] Video/ audio has captions or transcripts
- [ ] Touch targets minimum 44x44px
- [ ] Not reliant on color alone to convey information
- [ ] Page zoom to 200% without loss of content
- [ ] Screen reader tested (VoiceOver, NVDA, or similar)

### Mobile
- [ ] Viewport meta tag correct
- [ ] Touch targets 44x44px minimum
- [ ] No horizontal scroll at any width
- [ ] Navigation usable with one hand (thumb reachable)
- [ ] Forms usable on mobile (correct input types, no zoom on focus)
- [ ] Font sizes readable (16px minimum body)
- [ ] Click-to-call on phone numbers (tel: links)
- [ ] No hover-dependent interactions
- [ ] Media queries cover all common breakpoints
- [ ] Tested on real mobile devices (not just emulator)

### Security
- [ ] HTTPS enforced (redirect HTTP → HTTPS)
- [ ] No sensitive data in client-side code
- [ ] Form submissions over HTTPS
- [ ] Content Security Policy headers considered
- [ ] XSS prevention (escape user input)
- [ ] No exposed API keys in client code
- [ ] Third-party scripts audited (no tracking without consent)

## Pre-Deployment Checklist

### Final QA
- [ ] All links work (internal and external)
- [ ] All images load
- [ ] All forms submit correctly
- [ ] No console errors
- [ ] No 404 pages (except intentional)
- [ ] Favicon displays correctly
- [ ] Custom 404 page styled
- [ ] Page loads correctly in:
  - [ ] Chrome (latest)
  - [ ] Firefox (latest)
  - [ ] Safari (latest)
  - [ ] Edge (latest)
  - [ ] Mobile Chrome
  - [ ] Mobile Safari
  - [ ] Samsung Internet
- [ ] Email tested (transactional, notifications, forms)
- [ ] All third-party integrations working
- [ ] Analytics tracking verified (events, page views)

### Content Review
- [ ] No placeholder content (Lorem Ipsum)
- [ ] All images have correct captions/ alt text
- [ ] Spelling and grammar checked
- [ ] Factual accuracy verified
- [ ] Legal pages present (privacy policy, terms of service)
- [ ] Cookie consent implemented (if needed)
- [ ] Contact information correct
- [ ] Links to external sites open in new tab (with rel="noopener")
- [ ] No broken internal links

### Performance Final Check
- [ ] Lighthouse mobile score: 90+ Performance
- [ ] Lighthouse desktop score: 95+ Performance
- [ ] Largest Contentful Paint (LCP) < 2.5s
- [ ] First Input Delay (FID) < 100ms
- [ ] Cumulative Layout Shift (CLS) < 0.1
- [ ] Total page weight < 500kb (ideally)
- [ ] Web Vitals all pass
- [ ] Load tested (if applicable)

## Post-Deployment Checklist

### Immediate (Day 1)
- [ ] Domain DNS propagated (check with whatsmydns.net)
- [ ] SSL certificate active (no mixed content warnings)
- [ ] Analytics receiving data
- [ ] Forms submitted and received
- [ ] Search console submitted (sitemap.xml)
- [ ] Social preview images correct (test with social share debuggers)
- [ ] Back up completed

### Short-term (Week 1)
- [ ] Monitor analytics for issues (high bounce rate on specific pages)
- [ ] Check server logs for errors
- [ ] Monitor form submission rate
- [ ] Check all third-party integrations
- [ ] Test on real devices
- [ ] Gather initial user feedback
- [ ] Fix any critical bugs found post-launch

### Ongoing
- [ ] Regular performance audits (monthly)
- [ ] Content updates (per content calendar)
- [ ] SEO monitoring and improvements
- [ ] Security updates (dependencies, CMS)
- [ ] A/B testing (continuous improvement)
- [ ] User feedback collection
- [ ] Analytics review (weekly/ monthly)
- [ ] Competitor monitoring (quarterly)
- [ ] Trend updates (bi-annual redesign if needed)
- [ ] Backup verification (monthly)
