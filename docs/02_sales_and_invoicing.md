# Module 02: Sales & Invoicing — UI & Content Blueprint

> **File Name:** `sales_module.html`  
> **Accent Theme:** Emerald Green (`#059669`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Unified 1/3 vs 2/3 Grid Split — **Left Columns: 4 cols (`lg:col-span-4`)** | **Right Columns: 8 cols (`lg:col-span-8`)**  
> **Contextual Watermark Art:** Commercial Invoice Document / Currency Growth Arrows / Sales Funnel / Verified Badge  
> **Status:** Locked & Approved (Consistent with `finance_module.html` 4-Col/8-Col Architecture)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Unified 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - All 3 body rows feature a continuous, aligned vertical division line:
     - **Left Column (`lg:col-span-4` / 33.3% width):** Compact, highly focused sales telemetry (Target vs Actual dual-bar chart, collections velocity stream, category donut, AR aging risk watch).
     - **Right Column (`lg:col-span-8` / 66.7% width):** Expansive, wide-stage views (Commercial Pipeline Conversion Waterfall/Funnel, 6-Territory Performance Grid, and 9-column Commercial Invoices Data Hub).
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors identical to `erp_cover_page.html`: Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald Green (`#059669`), and Sunset Orange (`#ea580c`).
4. **Row 3 Perfect Height Balance:**
   - In the left 4-column space, **Revenue Distribution by Category** (Card 5A) and **Accounts Receivable (AR) Aging & Credit Risk Watch** (Card 5B) stack vertically (`flex flex-col gap-3.5`), matching the exact height of the Invoices Master Table (Card 6) on the right.
5. **No Cluttered In-Page Tabs:**
   - Submodule navigation is deferred to the future Global Application Sidebar. The page remains focused on executive commercial performance and audited invoice execution.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Emerald Green rounded icon badge + `Sales & Invoicing` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Sales & Commercial / Invoices, Deliveries & Revenue Recognition`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterInvoiceTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportSalesReport()`).

---

## 3. Top 4 Sales KPI Pillar Cards (Colorful Matte Glass)

Styled identically to the master executive group dashboard `erp_cover_page.html`:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Gross Invoiced Sales** | `৳ 4.82 Cr` | Target: ৳ 5.20 Cr (92.6% Achieved) | `▲ +14.2% MoM` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Paid Collections** | `৳ 3.98 Cr` | Realized Inflow (Collection: 82.5%) | `▲ +9.4%` (DSO: 34d) | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Overdue Receivables** | `৳ 84.20 L` | 14 accounts exceeding 45 days | `High Follow-up` | Solid Matte Emerald Green (`#059669/90`) |
| **Active Pipeline Value** | `৳ 1.65 Cr` | 18 Quotations awaiting client PO | `Conversion: 68%` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row 4-Col (Left) / 8-Col (Right) Cards Layout

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: SALES PERFORMANCE & COMMERCIAL PIPELINE STAGE                                         │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 1: Sales Performance (4 cols)            │ CARD 2: Commercial Pipeline & Conversion (8) │
│ • 6-Month Target vs Invoiced Dual-Bar Chart   │ • [GRAPH] Multi-Stage Pipeline Waterfall     │
│ • Realization Spline Overlay (68%-94%)        │ • Leads (8.40 Cr) → Quotations (4.60 Cr)     │
│ • Compact Telemetry Widget (500x180)          │   → Orders (3.80 Cr) → Invoiced (4.82 Cr)    │
│ • Range Toggles (6M / YTD / FY26)             │   → Realized Cash (3.98 Cr)                  │
│                                               │ • Expansive Stage Width (740x175)            │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 2: COLLECTIONS VELOCITY & TERRITORY PERFORMANCE                                          │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: Collections Velocity Stream (4 cols)  │ CARD 4: Regional Territory Performance (8)   │
│ • Inflow (+৳ 3.98 Cr) vs Due (৳ 84.2 L)       │ • 6 Territory Micro-Cards (3 cols x 2 rows): │
│ • Days Sales Outstanding (DSO): 34 Days       │ • Dhaka North, Dhaka South, Chittagong Port, │
│ • Top 4 Payment Gateways / Cheques Clearing   │   Gazipur Hub, Sylhet Division, Export Sales │
│ • Tight, Snug Column Fit                      │ • Target vs Achieved Progress Bars & Badges  │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: PRODUCT DISTRIBUTION, CREDIT RISK WATCH & AUDITED INVOICE HUB                         │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ LEFT STACK (4 cols): 2 Paired Cards           │ RIGHT COLUMN (8 cols): INVOICE MASTER HUB    │
│                                               │                                              │
│ • CARD 5A: Revenue Distribution by Category   │ CARD 6: Commercial Sales Invoices & Challan  │
│   Segmented SVG Donut Graph & Legend          │ • Expansive 9-Column Data Table with 6 Rows  │
│   Software 48.2%, Hardware 26.4%,             │ • Filter Tabs: All (342), Paid, Partial, Due │
│   Services 15.6%, Maintenance 9.8%            │ • Live Search, Customer Filter & Pagination  │
│                                               │ • Live Collections Summary Bar:              │
│ • CARD 5B: AR Aging & Credit Risk Watch       │   Gross Invoiced = Collections + Receivables │
│   0-30d (64.1%), 31-60d (20.7%),              │ • Action Controls: View Invoice PDF Modal,   │
│   61-90d (9.7%), >90d (5.5%) + Credit Exposure│   Collect Payment, Issue Challan Slip        │
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Detailed Card Specifications

### 5.1 Row 1: Sales Velocity & Commercial Pipeline Stage (4 cols + 8 cols)

#### Card 1: Sales Performance Target vs Realized Dual-Bar Graph
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Header: Emerald icon + "Sales Performance & Velocity" + Period selector pill (`6M`, `YTD`).
  - Graph Area: Custom responsive SVG Dual-Bar Chart (`viewBox="0 0 500 180"`) displaying:
    - Target Bar (Light Emerald/Gray `#cbd5e1` / `#a7f3d0`).
    - Actual Invoiced Bar (Vibrant Emerald `#059669`).
    - Realization Rate Spline line in Golden Amber (`#d97706`).
  - Footer Telemetry:
    - Target: `৳ 5.20 Cr` | Invoiced: `৳ 4.82 Cr` | Run-rate: `92.6%`
- **Contextual Watermark:** Upward Trend Ribbon / Financial Chart Curves (`opacity-[0.045]`).

#### Card 2: Commercial Pipeline & Conversion Flow Stage
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Funnel icon + "Commercial Pipeline & Sales Conversion Stage" + Status Pill (`Conversion: 68.4%`).
  - Graph Area: Expansive SVG Pipeline Waterfall / Stage Flow (`viewBox="0 0 740 175"`):
    1. **Stage 1 (Leads & RFPs):** `৳ 8.40 Cr` (72 Inquiries) — Bar in `indigo-400`.
    2. **Stage 2 (Commercial Quotes):** `৳ 4.60 Cr` (38 Proposals) — Bar in `blue-500`.
    3. **Stage 3 (Confirmed Orders / SO):** `৳ 3.80 Cr` (26 Work Orders) — Bar in `emerald-500`.
    4. **Stage 4 (Invoiced Deliveries):** `৳ 4.82 Cr` (MTD Invoiced) — Bar in `teal-600`.
    5. **Stage 5 (Realized Cash Collections):** `৳ 3.98 Cr` (Bank Realized) — Bar in `emerald-700`.
  - Micro-Summary Pills: Win Rate `68.4%` • Avg Deal Cycle `18 Days` • Lost Pipeline `৳ 1.15 Cr`.
- **Contextual Watermark:** Pipeline Funnel / Conversion Stage Art.

---

### 5.2 Row 2: Collections Velocity & Territory Performance (4 cols + 8 cols)

#### Card 3: Collections Velocity & Cash Realization Stream
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Metric Header: `৳ 3.98 Cr` collected against `৳ 4.82 Cr` billed (`82.5%`).
  - DSO Health Meter: **34 Days** (Target: <45 Days — `Healthy` green badge).
  - Inflow Channel Breakdown:
    - Corporate BEFTN / RTGS: `৳ 2.85 Cr` (71.6%)
    - Bank Account Cheques: `৳ 78.4 L` (19.7%)
    - Digital Payment Gateway: `৳ 24.6 L` (6.2%)
    - Cash on Delivery / Counter: `৳ 10.0 L` (2.5%)
- **Contextual Watermark:** Currency Register / Checkmark Seal.

#### Card 4: Regional Territory Performance & Quota Allocation
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - 3-Column x 2-Row Micro-Card Grid of the 6 core commercial zones:
    1. **Dhaka North (Corporate Headquarters):** Target ৳ 1.80 Cr | Invoiced: ৳ 1.74 Cr (96.6%) • Badge: `Exceeded`
    2. **Dhaka South (Commercial & Wholesale):** Target ৳ 1.10 Cr | Invoiced: ৳ 98.5 L (89.5%) • Badge: `On Track`
    3. **Chittagong Port & Export Division:** Target ৳ 95.0 L | Invoiced: ৳ 92.4 L (97.2%) • Badge: `Optimal`
    4. **Gazipur Industrial Belt:** Target ৳ 65.0 L | Invoiced: ৳ 54.2 L (83.3%) • Badge: `Follow-up`
    5. **Sylhet & Eastern Region:** Target ৳ 45.0 L | Invoiced: ৳ 42.1 L (93.5%) • Badge: `On Track`
    6. **Khulna & Southern Corridor:** Target ৳ 25.0 L | Invoiced: ৳ 20.8 L (83.2%) • Badge: `Growth Phase`
- **Contextual Watermark:** Geographical Region / Distribution Grid.

---

### 5.3 Row 3: Product Distribution, AR Aging & Audited Invoices Hub (4 cols + 8 cols)

#### Card 5A: Revenue Distribution by Product Category (Left Stack - Top)
- **Column Span:** Part of `lg:col-span-4` (Stacked above Card 5B)
- **Component Anatomy:**
  - SVG Segmented Donut Chart (`viewBox="0 0 160 160"`):
    - Enterprise Software Licenses & SaaS: `48.2%` (Emerald `#059669`)
    - Industrial Hardware & Automation: `26.4%` (Blue `#2563eb`)
    - Professional Implementation Services: `15.6%` (Purple `#7c3aed`)
    - Maintenance AMCs & Support: `9.8%` (Amber `#d97706`)
  - Center Donut Label: `৳ 4.82 Cr Total`
  - 2-Column Legend with BDT values and percentage badges.

#### Card 5B: Accounts Receivable (AR) Aging & Credit Risk Watch (Left Stack - Bottom)
- **Column Span:** Part of `lg:col-span-4` (Stacked below Card 5A to match Card 6 height)
- **Component Anatomy:**
  - 4 Horizontal Aging Bars:
    - **0–30 Days (Current):** `৳ 54.0 L` (64.1%) — `emerald-500`
    - **31–60 Days (Standard Credit):** `৳ 17.4 L` (20.7%) — `blue-500`
    - **61–90 Days (Warning Zone):** `৳ 8.2 L` (9.7%) — `amber-500`
    - **> 90 Days (Critical Default Risk):** `৳ 4.6 L` (5.5%) — `rose-500`
  - Credit Limit Exposure Badge: `84.2% Total Credit Line Utilized across 82 accounts`.

#### Card 6: Commercial Sales Invoices & Challan Master Hub (Right Column)
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Tab filters (`All Invoices (342)`, `Paid (280)`, `Partially Paid (38)`, `Overdue (24)`) + Search pill.
  - Expansive 9-Column Interactive Table:
    1. **Date:** `06 Nov 2026`
    2. **Invoice #:** `INV-2026-1492` (monospace bold link)
    3. **Customer / Corporate Client:** Bashundhara Infrastructure Ltd
    4. **PO / Contract Ref:** `PO-BSH-8821`
    5. **Subtotal (৳):** `30,00,000`
    6. **VAT 15% (৳):** `4,50,000`
    7. **Total BDT (৳):** `34,50,000`
    8. **Status:** `Paid` (Emerald badge) / `Partial` (Amber badge) / `Overdue` (Rose badge)
    9. **Action:** View PDF, Print Challan, Collect Payment
  - Balanced Reconciliation Summary Footer:
    - Total Invoiced: `৳ 4,82,00,000` = Collections `৳ 3,97,80,000` + Pending `৳ 84,20,000`.
- **Contextual Watermark:** Audited Invoice Ledger Art.

---

## 6. Interactive Scripts & Modals

1. **Search & Filter Script:**
   - Real-time client-side search across Invoice #, Customer Name, and PO Reference.
2. **Tab Switching:**
   - Filters between All, Paid, Partial, and Overdue without page reload.
3. **Quick Invoice PDF Preview:**
   - Lightweight modal previewing the formatted tax invoice with NBR Mushak-6.3 compliance.
