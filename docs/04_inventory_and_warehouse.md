# Module 04: Inventory & Warehouse — UI & Content Blueprint

> **File Name:** `inventory_module.html`  
> **Accent Theme:** Purple (`#7c3aed`), Royal Blue (`#2563eb`), Emerald (`#059669`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Multi-Hub Radial Capacity (8 cols) + ABC Velocity Spectrum (4 cols) | Safety Reorder Watch (5 cols) + Environmental Storage Zones (7 cols) | Master SKU Ledger (8 cols) + Live RFID Barcode Shelf Docket (4 cols)  
> **Contextual Watermark Art:** Warehouse High-Bay Storage / Forklift Pallets / Precision Barcode Laser Scan  
> **Status:** Locked & Live (`inventory_module.html` verified & synchronized)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Domain-Specific Visual Instruments (Zero Formulaic Cloning):**
   - **Row 1 (8 cols + 4 cols):** Multi-Hub Warehouse Bay Occupancy Hubs with 4 radial SVG meters + Stock Velocity ABC Spectrum (segmented gradient bar & turnover velocity).
   - **Row 2 (5 cols + 7 cols):** Safety Stock Reorder Watch & Lead-Time Countdown + Environmental Storage & Specialized Zones 2x2 Grid (Ambient, Cold Chain, Spares, Hazardous Vault).
   - **Row 3 (8 cols + 4 cols):** Enterprise Central SKU Master Table + Live Reactive Barcode/RFID Shelf Location Docket (updates instantaneously on row click).
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors: Solid Royal Blue (`#2563eb`), Solid Royal Purple (`#7c3aed`), Solid Emerald Green (`#059669`), and Solid Sunset Orange (`#ea580c`), each equipped with an integrated mini SVG circular progress ring.
4. **Clean Borders & Zero Overlaps:**
   - No heavy colored `border-l-4` strips on micro-cards; all cards use clean uniform frosted borders (`border border-slate-200/80`).
   - Clean SVG data visualizers with hollow centers and zero text collisions.
5. **No Cluttered In-Page Tabs:**
   - Module operations are self-contained; workspace switching is deferred to the future global application sidebar.

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
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options.
  - **Export Button:** Clean outline button with download icon and `Export Valuation Ledger` (`exportInventoryReport()`).

---

## 3. Top 4 Inventory KPI Pillar Cards (Colorful Matte Glass)

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Total Stock Valuation** | `৳ 6.84 Cr` | FIFO Method across 4 Hubs | `+3.4% MoM` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Active SKUs Managed** | `1,840 Items` | 98.4% In-Stock availability rate | `Optimal Stock` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Critical Reorder Alerts**| `12 SKUs` | Below safety buffer threshold | `Action Req.` | Solid Matte Emerald Green (`#059669/90`) |
| **Stock Velocity Ratio** | `4.2x / yr` | Avg holding period: 28 Days | `Fast Moving` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row Grid Architecture

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: MULTI-HUB STORAGE CAPACITY HUBS (8 cols) & STOCK VELOCITY ABC SPECTRUM (4 cols)       │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 1: Multi-Hub Storage Capacity & Bay Occupancy (8 cols)   │ CARD 2: ABC Stock Velocity   │
│ • 4 Core Hubs: Tejgaon Central (88.5%), Chittagong (74.2%),   │   Spectrum (4 cols)          │
│   Savar Industrial (86.0%), Bogura Depot (62.8%)             │ • Segmented Spectrum Bar:    │
│ • SVG Radial Capacity Rings + Active Pallet Counts            │   Class A (72.4%), B (21.2%) │
│ • Quick Bay Metrics: 145,000 sq ft, 94.2% Cross-Dock Rate     │   Class C (6.4%)             │
│                                                               │ • Annual Turnover 4.2x       │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 2: SAFETY STOCK REORDER WATCH (5 cols) & ENVIRONMENTAL STORAGE ZONES 2x2 (7 cols)        │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: Safety Stock Reorder Watch (5 cols)   │ CARD 4: Environmental Storage Zones (7 cols) │
│ • 12 Items Below Safety Threshold             │ • 2x2 Grid of specialized warehouse zones:   │
│ • 3 Imminent Depletion Items (<3 Days Lead)   │   1. Ambient Dry Goods (89.0% Full)          │
│ • Live Reorder Countdown & Auto-PO Badges     │   2. Cold Chain Vault -18°C (81.6% Full)     │
│ • Expedite All POs Interactive Action Button  │   3. Machinery Spares (74.6% Full)           │
│                                               │   4. Hazardous Chemicals Vault (54.6% Full)  │
│                                               │ • Clean uniform borders without left strips  │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: ENTERPRISE CENTRAL SKU MASTER (8 cols) & LIVE RFID SHELF DOCKET (4 cols)              │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 5: Central SKU Master Table (8 cols)     │ CARD 6: Live SKU Barcode RFID Docket (4 cols)│
│ • 6 Core Audited SKUs with Stock Level Gauges │ • Reactive Preview on Table Row Click        │
│ • Filters: All (1,840), In Stock, Low, Hubs  │ • Live Barcode Laser Visualization           │
│ • Live Search on SKU code & Item Description  │ • RFID EPC-96 Tag Reader & Frequency         │
│ • Valuation Breakdown Footer (Tejgaon, Ctg...)│ • Real-Time Physical Shelf & Bin Location    │
│                                               │ • Quick Adjust Count & Inter-Hub Transfer    │
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Component Anatomy

### 5.1 Row 1: Capacity Hubs & ABC Velocity Spectrum
- **Multi-Hub Storage Capacity (Card 1, 8 cols):** Features 4 distinct warehouse hubs, each displayed with an SVG radial ring gauge indicating exact pallet utilization, space allotment, and quick operational status badges.
- **Stock Velocity ABC Spectrum (Card 2, 4 cols):** Visualizes Pareto inventory classification (Class A 80/20 rule, Class B, Class C) with an SVG stacked spectrum bar, average holding days, and dead stock risk metrics.

### 5.2 Row 2: Reorder Watch & Environmental Storage Zones
- **Safety Stock Reorder Watch (Card 3, 5 cols):** Highlights imminent depletion items with visual progress buffer bars, lead-time day counters, and pending PO generation state.
- **Environmental Storage Zones 2x2 Grid (Card 4, 7 cols):** 4 clean frosted micro-cards displaying specialized warehouse climate zones with temperature/humidity indicators and capacity meters.

### 5.3 Row 3: Central SKU Master & Live Reactive Docket
- **Central SKU Master Table (Card 5, 8 cols):** Comprehensive multi-warehouse stock ledger with real-time stock status pills, on-hand counts vs safety buffers, and instant client-side search filtering.
- **Live SKU Barcode RFID Shelf Docket (Card 6, 4 cols):** Interactive inspection panel displaying the selected item's digital barcode laser, RFID identifier, physical aisle/rack/bin coordinates, and batch expiry. Clicking any table row seamlessly switches the live docket details.
