# 10 — Dashboard Design

## Dashboard Design Principles

### Information Density Balance
Dashboards must display lots of data without overwhelming:
- **KPI cards** — Most important numbers stand out
- **Visual hierarchy** — Most important info at top-left
- **Progressive disclosure** — Summary → detail on click
- **White space** — Don't fill every pixel with data
- **Consistent card sizes** — Grid alignment for scannability

### Data-Ink Ratio
Maximize data, minimize non-data ink:
- Remove chart borders and backgrounds where possible
- Use light gridlines, not prominent ones
- Avoid 3D charts (distorts perception)
- Remove decorative elements from data displays
- Use color purposefully (one semantic color per data type)

## Dashboard Layout Architecture

### Common Layout Structure
```
[TOP BAR] — Logo/name | Search | Notifications | Profile
[SIDEBAR] — Navigation menu (main sections)
[MAIN CONTENT]:
  [KPI ROW] — 3-6 metric cards
  [PRIMARY CHART] — Main visualization
  [SECONDARY ROW] — 2-3 smaller charts
  [DATA TABLE] — Detailed records
  [ACTIVITY FEED] — Recent events
```

### Sidebar Navigation
- Icons + labels (icons alone for collapsed)
- Sections grouped by function
- Active state indication
- Badge count for notifications
- Collapsible on mobile/ small screens
- Pin favorite items

### KPI Cards

**Anatomy:**
```
┌────────────────────────┐
│  ↑ 12%     [ICON]     │  ← Trend indicator + icon
│  $128,430              │  ← Primary metric (large)
│  Revenue               │  ← Label
│  vs $114,670 last month│  ← Comparison period
└────────────────────────┘
```

**Best practices:**
- 3-6 cards maximum (any more = noise)
- Consistent card width (2-3 per row)
- Semantic colors for trends (green = up, red = down)
- Sparkline for historical context
- Link to detailed view on click
- Skeleton loading states

## Chart Types & When to Use

| Type | Best For | Avoid For |
|------|----------|-----------|
| **Line chart** | Trends over time, continuous data | Categorical comparisons |
| **Bar chart** | Comparing categories, ranking | Showing trends/ patterns over time |
| **Pie/ Donut** | Parts of a whole (2-4 segments max) | Many categories, comparisons |
| **Area chart** | Volume over time, cumulative data | Precise value reading |
| **Scatter plot** | Correlation, distribution | Time series |
| **Heat map** | Density, patterns across 2 dimensions | Precise values |
| **Radar/ spider** | Multi-dimensional comparison | More than 6 dimensions |
| **Funnel** | Conversion stages (sales, signup) | Non-sequential data |
| **Progress bar** | Goal tracking, completion | Comparative data |
| **Gauge** | Single metric against target | Multiple data points |

### Chart Design Rules
- **Direct labels** over legends (reduce eye movement)
- **Consistent colors** across all charts (revenue always blue, etc.)
- **Sort data** by value (descending for bars, chronological for lines)
- **Zero baseline** for bar charts (don't distort)
- **Interactive** — hover for exact values, click to drill down
- **Responsive** — charts must work on mobile (may need separate views)

## Data Table Design

### Table Best Practices
- **Horizontal scroll** for many columns (with sticky first column)
- **Sortable headers** (click to sort asc/desc)
- **Filterable** — Search within table, column-specific filters
- **Pagination** — 10-25 rows per page (or virtual scroll)
- **Row hover** — Highlight for readability
- **Selectable rows** — Checkboxes for batch actions
- **Inline actions** — Edit, delete, view on each row (reveal on hover)
- **Responsive** — Cards on mobile, tables on desktop

### Table Cell Types
```
[Text] — Regular, left-aligned
[Number] — Right-aligned, monospace font
[Status] — Colored badge (Active, Pending, Failed)
[Date] — Relative + absolute ("2 hours ago — Jan 15, 2024")
[Avatar + Name] — Image + text combination
[Progress] — Mini progress bar
[Actions] — Icon buttons (edit, delete, more)
```

## Dashboard States

### Loading State
```
┌────────────────────────┐
│  ████████████░░░░░░   │  ← Skeleton bars
│                        │
│  ┌──────────────────┐  │
│  │ ██████████████   │  │  ← Skeleton card
│  │ ██               │  │
│  └──────────────────┘  │
└────────────────────────┘
```

### Empty State
```
┌────────────────────────┐
│                        │
│    [Illustration]      │
│    "No data yet"       │
│    "Add your first     │
│     project to get     │
│     started."          │
│                        │
│    [Add Project]       │  ← Primary CTA
│                        │
└────────────────────────┘
```

### Error State
```
┌────────────────────────┐
│                        │
│    [Error icon]        │
│    "Failed to load"    │
│    "Something went     │
│     wrong. Please       │
│     try again."        │
│                        │
│    [Try Again]  [Support]
│                        │
└────────────────────────┘
```

## Mobile Dashboard Design

### Mobile Adaptations
- KPI cards stack vertically (1 column)
- Charts simplify (may show less detail)
- Sidebar becomes bottom tab bar (4-5 items)
- Full-screen data views (table → card list)
- Swipe gestures for navigation
- Pull-to-refresh
- Floating action button for primary action

### Mobile Dashboard Optimization
- Show only 3-4 KPI cards (not 6)
- Single chart per viewport
- Summarize data tables (show key fields only)
- Thumb-friendly tap targets (44px minimum)
- Offline capability for cached data
- Push notification integration

## Dashboard Color Systems

### Semantic Color System
```
--color-success:   #10B981  (green — positive, growth)
--color-warning:   #F59E0B  (amber — caution, attention)
--color-error:     #EF4444  (red — negative, critical)
--color-info:      #3B82F6  (blue — informational)
--color-neutral:   #6B7280  (gray — default, inactive)
```

### Chart Color Palettes
**Sequential (single hue):**
#E0F2FE → #BAE6FD → #7DD3FC → #38BDF8 → #0EA5E9 → #0284C7 → #0369A1

**Categorical (distinct):**
#3B82F6, #10B981, #F59E0B, #EF4444, #8B5CF6, #EC4899

**Divergent (two extremes + middle):**
#EF4444 → #FCA5A5 → #F1F5F9 → #86EFAC → #22C55E

## Dashboard Anti-Patterns

| ❌ Bad | ✅ Better |
|--------|-----------|
| All data at once without hierarchy | Progressive disclosure |
| 3D charts (distorts data) | 2D, clean charts |
| Pie charts with 10+ segments | Bar chart or grouped |
| Scrolling horizontally for main content | Responsive, vertical-first |
| Tiny click targets (charts, rows) | Minimum 44px touch targets |
| No loading states | Skeleton screens |
| Inconsistent date formats | Standardized format everywhere |
| Too many colors for data | Consistent semantic colors |
| Auto-refresh without user control | Manual refresh + optional auto |
| No table sorting/ filtering | Sortable, filterable tables |
