# Module 05: CRM & Customers — UI & Content Blueprint

> **File Name:** `crm_module.html`  
> **Accent Theme:** Indigo (`#4f46e5`), Royal Blue (`#2563eb`), Emerald (`#059669`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** 5-Stage Deal Horizon (7 cols) + Customer 360 Health Radar (5 cols) | Acquisition Channels (5 cols) + Account Tiering 2x2 Matrix (7 cols) | Enterprise Deals Register (8 cols) + Reactive Client 360 Docket (4 cols)  
> **Contextual Watermark Art:** Enterprise Handshake / Deal Growth Chart / Corporate Network Nodes  
> **Status:** Locked & Live (`crm_module.html` verified & synchronized)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Domain-Specific Visual Instruments (Zero Formulaic Cloning):**
   - **Row 1 (7 cols + 5 cols):** Enterprise Deal Pipeline Horizon (5-stage horizontal SVG flow with win probability & value progression) + Customer 360 Health Radar (custom SVG 5-axes spider web chart).
   - **Row 2 (5 cols + 7 cols):** Lead Acquisition Channels Split (multi-segmented bar & channel ROI breakdown) + Client Account Tiering & Expansion 2x2 Matrix (Strategic Tier 1, Growth Tier 2, Commercial Tier 3, At-Risk Watchlist).
   - **Row 3 (8 cols + 4 cols):** Enterprise Deals & Accounts Register Table + Live Reactive Client 360 Docket (real-time stakeholder preview, financial metrics, and next steps on row click).
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors: Solid Royal Blue (`#2563eb`), Solid Royal Purple (`#7c3aed`), Solid Emerald Green (`#059669`), and Solid Sunset Orange (`#ea580c`), each equipped with an integrated mini SVG circular progress ring.
4. **Clean Borders & Zero Overlaps:**
   - No colored `border-l-4` strips on micro-cards; all cards use clean uniform frosted borders (`border border-slate-200/80`).
   - Radar chart and stage flow use hollow centered text and clean coordinate positioning.
5. **No Cluttered In-Page Tabs:**
   - In-page submodule tabs removed; navigation handled seamlessly from the Executive Portal and future global sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/75 backdrop-blur-md border-b border-white/60 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Indigo rounded icon badge + `CRM & Customers` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Enterprise Accounts, Deals & Client Retention Hub`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterDealTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options.
  - **Export Button:** Clean outline button with download icon and `Export Pipeline` (`exportCRMReport()`).

---

## 3. Top 4 CRM KPI Pillar Cards (Colorful Matte Glass)

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Active Pipeline Value** | `৳ 9.20 Cr` | Target: ৳ 12.0 Cr (76.7% Coverage) | `▲ +18.4% MoM` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Sales Win Rate** | `34.8%` | Benchmark: 30.0% Target (+4.8% Alpha) | `Top Decile` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Qualified Opportunities**| `184 Leads`| MQL to SQL: 74.2% Qualified | `+12.6% Inflow` | Solid Matte Emerald Green (`#059669/90`) |
| **Average Client LTV** | `৳ 42.50 L` | Net Retention Rate: 114.2% NRR | `Healthy Cohort` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row Grid Architecture

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: DEAL PIPELINE HORIZON (7 cols) & CUSTOMER 360 HEALTH RADAR (5 cols)                   │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 1: Enterprise Deal Pipeline Horizon (7 cols)             │ CARD 2: Customer 360 Health  │
│ • 5-Stage Velocity & Win Probability Flow:                    │   Radar (5 cols)             │
│   1. Qualification: ৳ 3.40 Cr (24 Deals • 15%)                │ • 5-Axes Spider Web Chart:   │
│   2. Tech Pitch: ৳ 2.80 Cr (18 Deals • 35%)                   │   NPS & Sentiment (92/100)   │
│   3. Proposal: ৳ 1.90 Cr (12 Deals • 60%)                     │   Feature Adoption (85/100)  │
│   4. Negotiation: ৳ 1.10 Cr (6 Deals • 85%)                   │   Payment Timeliness (88/100)│
│   5. Closed Won: ৳ 3.98 Cr (28 Deals • 100%)                  │   Engagement Pulse (76/100)  │
│ • Conversion pills, glow connectors & weighted metrics        │   Expansion Ready (90/100)   │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 2: ACQUISITION CHANNELS (5 cols) & CLIENT TIERING 2x2 MATRIX (7 cols)                    │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 3: Lead Acquisition Channels & Velocity (5 cols)         │ CARD 4: Client Account       │
│ • Multi-Segmented Horizontal Track:                           │   Tiering Matrix (7 cols)    │
│   - Executive Referral: 42% (৳ 3.86 Cr, 48.2% Win)            │ • 2x2 Clean Frosted Grid:    │
│   - Enterprise Inbound: 28% (৳ 2.58 Cr, 32.5% Win)            │   1. Strategic Tier 1        │
│   - Industry Trade Expos: 18% (৳ 1.66 Cr, 26.0% Win)          │   2. Growth Mid-Market T2    │
│   - Partner SDR: 12% (৳ 1.10 Cr, 19.4% Win)                   │   3. Commercial Tier 3       │
│                                                               │   4. High Churn Risk Watch   │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 3: ENTERPRISE DEALS REGISTER (8 cols) & LIVE CLIENT 360 DOCKET (4 cols)                  │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 5: Enterprise Deals & Accounts Register (8 cols)         │ CARD 6: Live Client 360      │
│ • 6 Audited Enterprise Rows (Apex, Square, Beximco, Walton...)│   Opportunity Docket (4 cols)│
│ • Stage Filters: All (42), Negotiation, Proposal, Closed Won  │ • Reactive on Row Selection  │
│ • Live Search on Accounts, Key Stakeholder, AE                │ • Stakeholder Phone/Email    │
│ • Deal Value, Win Probability Progress Bars, Status Badges    │ • ACV, LTV, Next Step Notes  │
└───────────────────────────────────────────────────────────────┴──────────────────────────────┘
```

---

## 5. Row-by-Row Component Anatomy

### 5.1 Row 1: Pipeline Horizon & Health Radar
- **Enterprise Deal Pipeline Horizon (Card 1, 7 cols):** Custom SVG interactive stage flow diagram connecting 5 key deal phases from Lead Qualification through Closed Won with stage-specific deal value, active deal count, win probability, and stage conversion tags.
- **Customer 360 Health Radar (Card 2, 5 cols):** Custom SVG spider web chart evaluating enterprise health across 5 core dimensions (NPS, Product Adoption, Invoicing Timeliness, Support Engagement, Expansion Potential) with concentric pentagonal rings and glowing polygon fill.

### 5.2 Row 2: Acquisition Channels & Account Tiering
- **Lead Acquisition Channels (Card 3, 5 cols):** Segmented bar chart and breakdown cards tracking volume split, win rates, and average deal size across 4 channels (Executive Referral, Inbound Web, Trade Summits, SDR Outbound).
- **Client Account Tiering 2x2 Matrix (Card 4, 7 cols):** 4 clean frosted micro-cards displaying Strategic Tier 1, Growth Mid-Market, Emerging Commercial, and At-Risk Watchlist cohorts without any left-border colored lines.

### 5.3 Row 3: Deals Register & Live Reactive Docket
- **Enterprise Deals Register Table (Card 5, 8 cols):** Comprehensive interactive table with client logos, stakeholder titles, deal stages, probability meters, and assigned Account Executives.
- **Live Client 360 Opportunity Docket (Card 6, 4 cols):** Contextual inspection panel displaying selected client profile, ARR/LTV telemetry, decision maker contact information, and upcoming strategic meeting notes. Seamlessly updates when any table row is clicked.
