# 09 — Ecommerce Design

## Ecommerce UX Principles

### Trust Signals
Ecommerce sites must overcome trust barriers:
- Secure payment badges (SSL, PCI)
- Money-back guarantee
- Return policy (clear, generous)
- Real reviews with photos
- Customer support availability
- Physical address/ phone number

### Decision Reduction
Too many choices reduce conversions:
- Show 12-24 products per page (not unlimited)
- Clear category hierarchy
- Good filters (price, size, color, brand)
- Sort by relevance, price, popularity
- "Best seller" badges reduce choice stress

### Friction Elimination
- Guest checkout (don't force account creation)
- Saved payment methods
- Auto-fill address suggestions
- Save cart across sessions
- One-click purchase (saved card)

## Homepage Structure (Ecommerce)

```
[NAVBAR] — Logo | Search | Categories | Cart | Account
[HERO] — Seasonal campaign / promotion / new collection
[CATEGORIES] — Shop by category grid (3-6)
[BEST SELLERS] — Top selling products grid
[NEW ARRIVALS] — Latest products
[SALE / PROMO] — Discounted section with banner
[TRENDING] — Social proof (what others are buying)
[NEWSLETTER] — Signup with discount
[FOOTER] — Links, Social, Legal, Support
```

## Product Listing Page (PLP)

### Layout Options

**Grid View (Default):**
- 2-4 columns (responsive)
- Product image, name, price
- Quick add to cart
- Hover: alternate image, color swatches

**List View (Alternative):**
- Single column with details
- More info visible without clicking
- Better for comparison shopping

**Masonry:**
- Varied image sizes
- Visual/ editorial feel (fashion, art)

### Product Card Blueprint
```
┌─────────────────┐
│                 │
│   [IMAGE]       │  ← High quality, white/ lifestyle bg
│   ▲ Badge       │  ← Sale | New | Best Seller
│                 │
├─────────────────┤
│  Product Name   │  ← 2-4 words
│  $29.99 $39.99  │  ← Price (sale strikethrough)
│  ★★★★☆ (128)   │  ← Rating + count
│  [Color dots]   │  ← Variant swatches
│  [Add to Cart]  │  ← Quick buy button
└─────────────────┘
```

### Filters & Sort

**Filter types:**
- Category/ department
- Price range (slider or checkbox)
- Size
- Color
- Brand
- Rating
- Availability

**Sort options:**
- Relevance
- Price: Low to High
- Price: High to Low
- Newest
- Best Selling
- Rating

**Filter UI:**
- Desktop: Sidebar or top bar
- Mobile: Bottom sheet or overlay
- Active filter tags (removable)
- Clear all filters button
- Count of results updates in real-time

## Product Detail Page (PDP)

### PDP Anatomy
```
[GALLERY] — Main image + thumbnails (zoom on hover)
[PRODUCT INFO] — Name, price, rating, description
[VARIANTS] — Size, color, options selector
[ADD TO CART] — Quantity selector + Add to Cart button
[TRUST BADGES] — Secure checkout, returns, shipping
[REVIEWS] — Customer reviews with photos
[RELATED] — You may also like
[FAQ] — Shipping, returns, sizing
```

### Premium PDP Enhancements
- **360° product view** — Drag to rotate product
- **AR view** — See product in real space (furniture, decor)
- **Video** — Product in use, unboxing
- **Size guide** — Interactive, popup with measurements
- **Stock indicator** — "Only 3 left in this color"
- **Recently viewed** — For return visitors
- **Social proof** — "12 people are viewing this right now"

### Image Gallery Design
- Main image: 800-1200px width, zoom on hover
- Thumbnails: Below main image, vertical on desktop
- Swipe on mobile
- Video thumbnail (play icon overlay)
- 360 spin: multiple images stitched
- Lifestyle + product-only shots (alternate)

## Cart & Checkout

### Cart Page
```
[CART ITEMS]
[PRODUCT IMAGE] [QTY] [REMOVE] [PRICE] [TOTAL]
[Subtotal]
[Shipping estimate]
[Tax estimate]
[Promo code input]
[Proceed to Checkout] button
[Continue shopping] link
```

**Cart best practices:**
- Show stock status near items
- Save for later option
- Recently removed undo
- Express checkout buttons (Shop Pay, Apple Pay)
- Trust badges near checkout button

### Checkout Flow

**Single-page checkout (preferred):**
1. Contact Info (email)
2. Shipping Address
3. Shipping Method
4. Payment
5. Review Order
6. Place Order

**Multi-step checkout:**
1. Cart → 2. Shipping → 3. Payment → 4. Confirmation
Progress indicator showing current step

**One-click checkout:**
- Saved payment + address
- Accelerated checkout (Shop Pay, PayPal, Apple Pay)
- Best for returning customers

### Checkout Design Rules
- Single column layout
- Clear labels on fields
- Inline validation (not after submit)
- Save address, detect country
- Payment logos visible
- Order summary visible throughout
- No distractions (no nav bar, no links out)
- Trust badges near payment
- Guest checkout option prominent

## Ecommerce Homepage Sections

### Hero / Banner
- Seasonal campaign
- New collection
- Major sale
- 1-2 slides max (not auto-rotating carousel)

### Category Grid
- 4-6 categories
- Large lifestyle images
- Category name overlay
- Shop now link

### Product Grids
- Best Sellers
- New Arrivals
- Trending
- Recommended (personalized)
- Recently Viewed

### Social Proof Elements
- Review highlights with photos
- Instagram feed (shoppable)
- "As seen on" (influencer/ press logos)
- Customer count ("Join 100,000+ customers")

### Email Capture
- "Get 10% off your first order"
- Popup (exit intent) or inline
- Minimal fields (email only)
- Privacy reassurance

## Mobile Ecommerce Design

### Mobile-Specific Patterns
- **Bottom tab nav** — Home, Categories, Cart, Account
- **Sticky cart bar** — Shows total + checkout button
- **Swipeable product images** — Gallery on PDP
- **Filter bottom sheet** — Slides up from bottom
- **Quick view modal** — Product detail without leaving page
- **Thumb-friendly targets** — 44px minimum tap area

### Mobile Checkout
- Auto-detect shipping country
- Saved addresses
- Apple Pay/ Google Pay (one touch)
- Biometric authentication (Face ID)
- Keyboard type matching field (email, number, tel)
- No hover-dependent interactions

## Ecommerce Trust Badges

### Types of Trust Badges
- **Security:** SSL, PCI Compliant, Norton, McAfee
- **Payment:** Visa, Mastercard, PayPal, Apple Pay, Amex
- **Shipping:** Free shipping, Fast delivery, Tracked
- **Returns:** Free returns, 30-day guarantee, No questions asked
- **Quality:** Authentic, Handmade, Organic, Certified

### Placement
- Near Add to Cart button
- In checkout (near payment)
- In footer (badge row)
- On homepage (near hero CTA or footer)

## Ecommerce Conversion Optimization

### Pricing Psychology
- **Charm pricing** — $19.99 vs $20.00 ($0.01 difference matters)
- **Bundle pricing** — "Buy together and save 15%"
- **Tiered pricing** — More quantity = lower per-unit cost
- **Free shipping threshold** — "Free shipping over $50" (increases cart size)
- **Price anchoring** — Show original price strikethrough

### Urgency Tactics
- **Low stock** — "Only 3 left in this color"
- **Time-limited sale** — "Sale ends in 4 hours"
- **Flash sale** — Countdown timer
- **Limited edition** — "Limited run, get yours"
- **Free shipping countdown** — "Order in 2 hours for free shipping"

### Abandoned Cart Recovery
- Email reminder (1 hour, 24 hours)
- Cart persistence (save across devices)
- Exit-intent popup with discount
- "Complete your look" product recommendations

## Ecommerce Design Anti-Patterns

| ❌ Bad | ✅ Better |
|--------|-----------|
| Forced account creation | Guest checkout option |
| Tiny product images | Large, zoomable images |
| Hidden shipping costs | Show early in checkout |
| Complicated returns | "Free returns, no questions" |
| Too many products per page | 24-48 max with good filters |
| Missing size guide for apparel | Interactive size guide |
| Auto-play video with sound | Autoplay muted, click for sound |
| No mobile optimization | Mobile-first responsive design |
| Cluttered product page | Clean, focused on product |
| Review hiding | Show all reviews, bad included (trust) |
