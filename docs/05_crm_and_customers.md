# Module 05: CRM & Customers — UI & Content Blueprint

> **File Name:** `crm_module.html`  
> **Accent Theme:** Indigo (`#4f46e5`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Unified 1/3 vs 2/3 Grid Split — **Left Columns: 4 cols (`lg:col-span-4`)** | **Right Columns: 8 cols (`lg:col-span-8`)**  
> **Contextual Watermark Art:** Customer Handshake / Deal Growth Chart / Corporate Network Nodes  
> **Status:** Locked & Approved (Consistent with `finance_module.html` 4-Col/8-Col Architecture)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Unified 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - All 3 body rows feature a continuous, aligned vertical division line:
     - **Left Column (`lg:col-span-4` / 33.3% width):** Lead velocity dual-bar chart, CLV retention stream, industry sector donut, and churn risk health monitor.
     - **Right Column (`lg:col-span-8` / 66.7% width):** Expansive enterprise deal pipeline stage, 6-sector account tier grid, and 9-column Enterprise Accounts & Deals Master Hub.
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors identical to `erp_cover_page.html`: Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald Green (`#059669`), and Sunset Orange (`#ea580c`).
4. **Row 3 Perfect Height Balance:**
   - In the left 4-column space, **Accounts by Industry** (Card 5A) and **Account Health & Churn Risk Watch** (Card 5B) stack vertically (`flex flex-col gap-3.5`), matching the exact height of the Deals Master Table (Card 6) on the right.
5. **No Cluttered In-Page Tabs:**
   - Submodule navigation (Lead scoring, Contact book, Support tickets) is deferred to the future Global Application Sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Indigo rounded icon badge + `CRM & Customers` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Commercial & CRM / Enterprise Accounts, Deals & Client Retention`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterDealTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportCRMReport()`).

---

## 3. Top 4 CRM KPI Pillar Cards (Colorful Matte Glass)

Styled identically to the master executive group dashboard `erp_cover_page.html`:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Active Pipeline Value** | `৳ 9.20 Cr` | 42 Enterprise Deals in Negotiation | `▲ +18.4% MoM` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Sales Win Rate** | `34.8%` | Target: 30% (Industry avg 24%) | `High Velocity` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **New Leads This Month** | `184 Leads` | 74% MQL Qualified conversion | `Optimal Flow` | Solid Matte Emerald Green (`#059669/90`) |
| **Average Customer LTV** | `৳ 42.50 L` | Net Retention Rate: 114.2% | `Top Retention` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row 4-Col (Left) / 8-Col (Right) Cards Layout

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: LEAD VELOCITY & ENTERPRISE DEAL PIPELINE STAGE                                        │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 1: Lead Velocity & Win Rate (4 cols)     │ CARD 2: Enterprise Deal Pipeline Stage (8)   │
│ • 6-Month Inbound Leads vs Deals Won Bar      │ • [GRAPH] Multi-Stage Sales Velocity Flow    │
│ • Win Rate % Spline Overlay (28%-35%)         │ • Leads (14.8 Cr) → Discovery (9.2 Cr)       │
│ • Compact Telemetry Widget (500x180)          │   → Proposal (5.4 Cr) → Negotiation (3.8 Cr) │
│ • Range Toggles (6M / YTD / FY26)             │   → Closed Won Deals (2.65 Cr)               │
│                                               │ • Expansive Stage Width (740x175)            │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 2: CLIENT RETENTION & INDUSTRY SECTOR ALLOCATION                                         │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: Client Retention & ARR Velocity (4)   │ CARD 4: Industry Sector & Tier Grid (8)      │
│ • NRR Rate (114%) & Churn Rate (0.8%)         │ • 6 Industry Micro-Cards (3 cols x 2 rows):  │
│ • Annual Recurring Revenue (ARR): ৳ 12.8 Cr   │ • Banking & FinTech, Manufacturing, Telecom, │
│ • Avg Sales Cycle: 24 Days                    │   Pharma & Health, FMCG Retail, Public Sector│
│ • Tight, Snug Column Fit                      │ • Pipeline vs Won Progress Bars & Badges     │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: SECTOR DISTRIBUTION, HEALTH WATCH & AUDITED DEALS HUB                                 │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ LEFT STACK (4 cols): 2 Paired Cards           │ RIGHT COLUMN (8 cols): DEALS MASTER HUB      │
│                                               │                                              │
│ • CARD 5A: Accounts by Industry Sector        │ CARD 6: Enterprise Accounts & Deals Hub      │
│   Segmented SVG Donut Graph & Legend          │ • Expansive 9-Column Data Table with 6 Rows  │
│   Banking 38.4%, Manufacturing 28.2%,         │ • Filter Tabs: All (42), Qualified, Won, Due │
│   Telecom 18.5%, Pharma 14.9%                 │ • Live Search, Account Manager & Pagination  │
│                                               │ • Live Pipeline Summary Bar:                 │
│ • CARD 5B: Account Health & Churn Risk Watch  │   Total Pipeline = Committed + In-Progress   │
│   NPS: +72, Health Score: 92%,                │ • Action Controls: View Deal Room Modal,     │
│   High-Risk Watchlist: 3 Accounts             │   Log Activity, Schedule Review              │
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Detailed Card Specifications

### 5.1 Row 1: Lead Velocity & Enterprise Deal Pipeline Stage (4 cols + 8 cols)

#### Card 1: Lead Velocity & Win Rate Dual-Bar Graph
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Header: Indigo icon + "Lead Velocity & Conversion" + Range pill (`6M`, `YTD`).
  - Graph Area: Custom responsive SVG Dual-Bar Chart (`viewBox="0 0 500 180"`):
    - Inbound MQL Leads Bar (Light Indigo `#a5b4fc`).
    - Deals Won Bar (Vibrant Indigo `#4f46e5`).
    - Win Rate % Spline in Emerald (`#059669`).
  - Footer Telemetry:
    - Inbound: `184 Leads` | Won: `64 Deals` | Win Rate: `34.8%`
- **Contextual Watermark:** Deal Win Ribbon / Upward Arrow Art.

#### Card 2: Enterprise Deal Pipeline & Customer Lifecycle Stage
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Funnel icon + "Enterprise Deal Pipeline & Stage Conversion" + Status Pill (`Cycle: 24 Days`).
  - Graph Area: Expansive SVG Pipeline Waterfall / Stage Flow (`viewBox="0 0 740 175"`):
    1. **Stage 1 (Inbound & Prospecting):** `৳ 14.80 Cr` (84 Leads) — `slate-400`.
    2. **Stage 2 (Qualified Discovery & Demo):** `৳ 9.20 Cr` (42 Deals) — `indigo-500`.
    3. **Stage 3 (Proposal & RFP Response):** `৳ 5.40 Cr` (28 Proposals) — `blue-500`.
    4. **Stage 4 (Legal & Commercial Negotiation):** `৳ 3.80 Cr` (18 Contracts) — `amber-500`.
    5. **Stage 5 (Closed Won & Contracting):** `৳ 2.65 Cr` (12 Deals Closed) — `emerald-600`.
  - Micro-Summary: Avg Deal Size `৳ 42.5 L` • Win Probability `68%` • Slippage `<5%`.
- **Contextual Watermark:** Global Corporate Network Nodes.

---

### 5.2 Row 2: Client Retention & Industry Sector Allocation (4 cols + 8 cols)

#### Card 3: Client Retention & ARR Velocity Stream
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Metric Header: `৳ 12.8 Cr` ARR with **114.2%** Net Retention Rate.
  - Retention & Churn Health Breakdown:
    - Expansion Revenue: `+18.4%` (Upsell to existing clients)
    - Gross Churn Rate: `0.8%` (Industry best-in-class <2%)
    - Net Promoter Score (NPS): `+72 (World Class)`
  - Active Contract Renewals: `৳ 3.40 Cr` scheduled in next 60 days.
- **Contextual Watermark:** Customer Handshake & Seal Art.

#### Card 4: Industry Sector & Strategic Account Tier Grid
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - 3-Column x 2-Row Micro-Card Grid of the 6 core customer industries:
    1. **Banking & FinTech Systems:** Pipeline ৳ 3.50 Cr | Won: ৳ 1.15 Cr (32.8%) • Badge: `Top Tier`
    2. **Manufacturing & Heavy Industries:** Pipeline ৳ 2.60 Cr | Won: ৳ 78.0 L (30.0%) • Badge: `Growth`
    3. **Telecommunications & Data Centers:** Pipeline ৳ 1.70 Cr | Won: ৳ 42.0 L (24.7%) • Badge: `Optimal`
    4. **Pharmaceuticals & Health Networks:** Pipeline ৳ 1.40 Cr | Won: ৳ 30.0 L (21.4%) • Badge: `On Track`
    5. **FMCG & Retail Superstores:** Pipeline ৳ 1.10 Cr | Won: ৳ 28.0 L (25.5%) • Badge: `Active`
    6. **Public Utilities & Government:** Pipeline ৳ 80.0 L | Won: ৳ 15.0 L (18.8%) • Badge: `Review`
- **Contextual Watermark:** Industry Sector Distribution Matrix.

---

### 5.3 Row 3: Sector Distribution, Health Watch & Audited Deals Hub (4 cols + 8 cols)

#### Card 5A: Accounts Distribution by Industry (Left Stack - Top)
- **Column Span:** Part of `lg:col-span-4` (Stacked above Card 5B)
- **Component Anatomy:**
  - SVG Segmented Donut Chart (`viewBox="0 0 160 160"`):
    - Banking & Financial Services: `38.4%` (Indigo `#4f46e5`)
    - Industrial Manufacturing: `28.2%` (Blue `#2563eb`)
    - Telecommunications & ISP: `18.5%` (Purple `#7c3aed`)
    - Pharmaceuticals & Healthcare: `14.9%` (Emerald `#059669`)
  - Center Donut Label: `৳ 9.20 Cr Total`
  - 2-Column Legend with BDT values and percentage badges.

#### Card 5B: Account Health & Churn Risk Watch (Left Stack - Bottom)
- **Column Span:** Part of `lg:col-span-4` (Stacked below Card 5A to match Card 6 height)
- **Component Anatomy:**
  - 4 Account Health Telemetry Tiers:
    - **Champions (>90 Health Score):** `34 Accounts` — `emerald-500`
    - **Stable (75–90 Health Score):** `18 Accounts` — `blue-500`
    - **Needs Attention (60–75 Score):** `6 Accounts` — `amber-500`
    - **Critical Churn Risk (<60 Score):** `2 Accounts` — `rose-600`
  - Customer Success Alert: `Executive meeting scheduled for 2 critical accounts`.

#### Card 6: Enterprise Accounts & Deals Master Hub (Right Column)
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Tab filters (`All Deals (42)`, `Negotiation (18)`, `Won (12)`, `At Risk (3)`) + Search.
  - Expansive 9-Column Interactive Table:
    1. **Client / Account Name:** Standard Chartered Bank (Corporate)
    2. **Industry:** Banking & FinTech
    3. **Account Manager:** Tanvir Ahmed (VP Enterprise)
    4. **Deal Title:** Core Cloud ERP Migration
    5. **Value BDT (৳):** `65,00,000`
    6. **Probability:** `85%` (Emerald pill)
    7. **Expected Close:** `24 Nov 2026`
    8. **Stage:** `Contract Review` (Purple)
    9. **Action:** View Deal Room, Log Call, Update Stage
  - Balanced Pipeline Summary Footer:
    - Total Active Pipeline: `৳ 9,20,00,000` = Weighted Forecast `৳ 6,85,00,000` (74.4% Realization).
- **Contextual Watermark:** Corporate Deal Ledger Art.
