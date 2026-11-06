# Module 04: Inventory & Warehouse — UI & Content Blueprint

> **File Name:** `inventory_module.html`  
> **Accent Theme:** Purple (`#7c3aed`), Royal Blue (`#2563eb`), Emerald (`#059669`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Unified 1/3 vs 2/3 Grid Split — **Left Columns: 4 cols (`lg:col-span-4`)** | **Right Columns: 8 cols (`lg:col-span-8`)**  
> **Contextual Watermark Art:** Warehouse Storage Rack / Forklift & Pallet Stacks / Barcode Laser Scan  
> **Status:** Locked & Approved (Consistent with `finance_module.html` 4-Col/8-Col Architecture)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Unified 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - All 3 body rows feature a continuous, aligned vertical division line:
     - **Left Column (`lg:col-span-4` / 33.3% width):** Stock turnover dual-bar chart, stock velocity telemetry, category valuation donut, and reorder critical risk watch.
     - **Right Column (`lg:col-span-8` / 66.7% width):** Expansive multi-hub warehouse capacity stage, 6-zone storage allocation grid, and 9-column SKU Master & Stock Ledger Hub.
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors identical to `erp_cover_page.html`: Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald Green (`#059669`), and Sunset Orange (`#ea580c`).
4. **Row 3 Perfect Height Balance:**
   - In the left 4-column space, **Inventory Valuation by Category** (Card 5A) and **Reorder Safety & Stockout Alerts** (Card 5B) stack vertically (`flex flex-col gap-3.5`), matching the exact height of the SKU Master Table (Card 6) on the right.
5. **No Cluttered In-Page Tabs:**
   - Submodule navigation (Inter-warehouse transfers, Stock Adjustments, Barcode Audit) is deferred to the future Global Application Sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Purple rounded icon badge + `Inventory & Warehouse` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Warehouse & Logistics / Stock Inventory, Hubs & Valuation`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterSKUTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportInventoryReport()`).

---

## 3. Top 4 Inventory KPI Pillar Cards (Colorful Matte Glass)

Styled identically to the master executive group dashboard `erp_cover_page.html`:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Total Stock Valuation** | `৳ 6.84 Cr` | FIFO Method across 3 Hubs | `▲ +3.4% MoM` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Active SKUs Managed** | `1,840 Items` | 98.4% In-Stock availability rate | `Optimal Stock` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Critical Reorder Alerts**| `12 SKUs` | Below safety buffer threshold | `Action Req.` | Solid Matte Emerald Green (`#059669/90`) |
| **Monthly Stock Turnover** | `4.2x` | Avg holding period: 28 Days | `High Velocity` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row 4-Col (Left) / 8-Col (Right) Cards Layout

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: STOCK TURNOVER & MULTI-HUB WAREHOUSE CAPACITY STAGE                                   │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 1: Stock Turnover Velocity (4 cols)      │ CARD 2: Multi-Hub Warehouse Capacity Flow (8)│
│ • 6-Month Inward vs Outward Dual-Bar Chart    │ • [GRAPH] Capacity Waterfall & Inflow Stage  │
│ • Turnover Velocity Spline Overlay (3.8-4.2x) │ • Total Hub Capacity (24k Pallets / 82% Full)│
│ • Compact Telemetry Widget (500x180)          │   → Tejgaon (12k) → Chittagong Port (7.5k)   │
│ • Range Toggles (6M / YTD / FY26)             │   → Savar Factory (4.5k) → Transit (850)     │
│                                               │ • Expansive Stage Width (740x175)            │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 2: STOCK VELOCITY & STORAGE ZONE ALLOCATION                                              │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: Stock Velocity Telemetry (4 cols)     │ CARD 4: Storage Zones & Hub Allocation (8)   │
│ • Fast-Moving (68%) vs Slow-Moving (8.4%)     │ • 6 Zone Micro-Cards (3 cols x 2 rows):      │
│ • Avg Holding Period: 28 Days                 │ • Raw Materials, Finished Goods Bay A,       │
│ • Quarantine QC Hold: ৳ 14.2 L                │   Cold Storage, Quarantine QC, Packaging Bay │
│ • Tight, Snug Column Fit                      │ • Capacity vs Utilized Progress Bars & Badges│
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: CATEGORY VALUATION, REORDER SAFETY & CENTRAL SKU HUB                                  │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ LEFT STACK (4 cols): 2 Paired Cards           │ RIGHT COLUMN (8 cols): SKU MASTER HUB        │
│                                               │                                              │
│ • CARD 5A: Inventory Valuation by Category    │ CARD 6: Central SKU Master & Stock Ledger    │
│   Segmented SVG Donut Graph & Legend          │ • Expansive 9-Column Data Table with 6 Rows  │
│   Finished Goods 46.2%, Raw Materials 34.5%,  │ • Filter Tabs: All (1,840), In Stock, Low    │
│   WIP 12.8%, Spare Parts 6.5%                 │ • Live Search, Hub Filter & Pagination       │
│                                               │ • Live Valuation Summary Bar:                │
│ • CARD 5B: Reorder Safety & Stockout Alerts   │   Total Stock = Active Value + Safety Buffer │
│   12 SKUs Critical, Lead Time Buffer 4.5d,    │ • Action Controls: View SKU Details Modal,   │
│   Auto-Reorder Generated: 8 POs               │   Audit Stock Count, Transfer Request        │
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Detailed Card Specifications

### 5.1 Row 1: Stock Velocity & Multi-Hub Warehouse Capacity Stage (4 cols + 8 cols)

#### Card 1: Stock Turnover Velocity Dual-Bar Graph
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Header: Purple icon + "Stock Turnover Velocity" + Range pill (`6M`, `YTD`).
  - Graph Area: Custom responsive SVG Dual-Bar Chart (`viewBox="0 0 500 180"`):
    - Inward Receipts Bar (Lavender `#c084fc`).
    - Outward Dispatched Bar (Vibrant Purple `#7c3aed`).
    - Turnover Ratio Spline in Emerald (`#059669`).
  - Footer Telemetry:
    - Monthly Inflow: `৳ 2.80 Cr` | Outflow: `৳ 3.40 Cr` | Turnover: `4.2x`
- **Contextual Watermark:** Rotating Logistics Cycle Arrows.

#### Card 2: Multi-Hub Warehouse Capacity & Stock Flow Stage
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Warehouse icon + "Multi-Hub Warehouse Capacity & Stock Flow Stage" + Space Pill (`Utilization: 82.4%`).
  - Graph Area: Expansive SVG Pipeline Waterfall / Stage Flow (`viewBox="0 0 740 175"`):
    1. **Total System Capacity:** `24,000 Pallets` (82.4% Utilized) — `slate-400`.
    2. **Tejgaon Central Distribution Hub:** `12,000 Pallets` (88.5% Full) — `purple-500`.
    3. **Chittagong Port Transit Depot:** `7,500 Pallets` (74.2% Full) — `blue-500`.
    4. **Savar Industrial Factory Store:** `4,500 Pallets` (86.0% Full) — `emerald-500`.
    5. **In-Transit Fleet Cargo:** `850 Pallets` (Inter-depot transfer) — `amber-500`.
  - Micro-Summary: Total Bay Space `145,000 sq ft` • Cross-Dock Efficiency `94.2%` • Quarantine `1.8%`.
- **Contextual Watermark:** High-Bay Storage Racks Art.

---

### 5.2 Row 2: Stock Velocity & Storage Zone Allocation (4 cols + 8 cols)

#### Card 3: Stock Velocity & Shelf Life Telemetry
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Metric Header: `4.2x` Annual Turnover with **28 Days** avg shelf life.
  - Velocity Classification Breakdown:
    - Fast-Moving Consumer Goods (FMCG): `68.2%` (High Liquidity)
    - Medium Velocity Goods: `23.4%` (Normal Lead Time)
    - Slow-Moving / Dead Stock Risk: `8.4%` (`৳ 57.4 L` flagged for liquidation)
  - Quarantine Quality Hold: `৳ 14.2 L` awaiting lab clearance.
- **Contextual Watermark:** Precision Barcode Scanner Art.

#### Card 4: Storage Zones & Hub Allocation
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - 3-Column x 2-Row Micro-Card Grid of the 6 core storage zones:
    1. **Raw Material Silos & Bay:** Capacity 8,000 Pallets | In-Stock: 7,120 (89.0%) • Badge: `Optimal`
    2. **Finished Goods Bay A:** Capacity 6,500 Pallets | In-Stock: 5,980 (92.0%) • Badge: `Near Capacity`
    3. **Temperature-Controlled Cold Store:** Capacity 3,000 Pallets | In-Stock: 2,450 (81.6%) • Badge: `Stable`
    4. **Quarantine & QC Testing Bay:** Capacity 1,500 Pallets | In-Stock: 820 (54.6%) • Badge: `Inspection`
    5. **Bulk Packaging Material Bay:** Capacity 3,500 Pallets | In-Stock: 2,640 (75.4%) • Badge: `Normal`
    6. **Heavy Machinery Spare Parts Rack:** Capacity 1,500 Pallets | In-Stock: 1,120 (74.6%) • Badge: `Controlled`
- **Contextual Watermark:** Automated Storage & Retrieval System (ASRS).

---

### 5.3 Row 3: Category Valuation, Reorder Safety & Central SKU Hub (4 cols + 8 cols)

#### Card 5A: Inventory Valuation by Category (Left Stack - Top)
- **Column Span:** Part of `lg:col-span-4` (Stacked above Card 5B)
- **Component Anatomy:**
  - SVG Segmented Donut Chart (`viewBox="0 0 160 160"`):
    - Finished Commercial Goods: `46.2%` (Purple `#7c3aed`)
    - Raw Polymers & Ingredients: `34.5%` (Blue `#2563eb`)
    - Work-in-Progress (WIP): `12.8%` (Emerald `#059669`)
    - Engineering Spare Parts: `6.5%` (Amber `#d97706`)
  - Center Donut Label: `৳ 6.84 Cr Total`
  - 2-Column Legend with BDT values and percentage badges.

#### Card 5B: Reorder Safety & Stockout Alerts (Left Stack - Bottom)
- **Column Span:** Part of `lg:col-span-4` (Stacked below Card 5A to match Card 6 height)
- **Component Anatomy:**
  - 4 Critical Stock Alert Tiers:
    - **Stockout Imminent (<3 Days):** `3 SKUs` — `rose-600 font-bold`
    - **Below Reorder Level (<7 Days):** `9 SKUs` — `amber-500`
    - **Healthy Buffer (>15 Days):** `1,642 SKUs` — `emerald-500`
    - **Overstocked / High Days on Hand:** `186 SKUs` — `blue-500`
  - Automation Badge: `Auto-PO generated for 8 low-stock items`.

#### Card 6: Central SKU Master & Stock Ledger (Right Column)
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Tab filters (`All SKUs (1,840)`, `In Stock (1,642)`, `Low Stock (12)`, `Quarantine (18)`) + Search.
  - Expansive 9-Column Interactive Table:
    1. **SKU Code:** `SKU-PL-8921` (monospace bold)
    2. **Item Description:** High-Density Polyethylene Resin 50kg
    3. **Category:** Raw Materials
    4. **Warehouse Hub:** Tejgaon Central (Bay 04)
    5. **On-Hand Qty:** `420 Bags`
    6. **Safety Min:** `150 Bags`
    7. **Valuation BDT (৳):** `18,90,000`
    8. **Stock Status:** `Optimal` (Emerald) / `Low Stock` (Rose) / `Reorder Placed` (Amber)
    9. **Action:** View Stock Ledger, Adjust Count, Transfer
  - Balanced Valuation Summary Footer:
    - Total Valuation: `৳ 6,84,00,000` = Tejgaon `৳ 4,12,00,000` + Chittagong `৳ 1,94,00,000` + Savar `৳ 78,00,000`.
- **Contextual Watermark:** Audited Warehouse Ledger Art.
