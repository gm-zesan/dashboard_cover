# Module 03: Purchase & Suppliers — UI & Content Blueprint

> **File Name:** `purchase_module.html`  
> **Accent Theme:** Amber / Bronze (`#d97706`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald (`#059669`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Unified 1/3 vs 2/3 Grid Split — **Left Columns: 4 cols (`lg:col-span-4`)** | **Right Columns: 8 cols (`lg:col-span-8`)**  
> **Contextual Watermark Art:** Procurement Delivery Truck / Purchase Order Clipboard / Vendor Verification Stamp  
> **Status:** Locked & Approved (Consistent with `finance_module.html` 4-Col/8-Col Architecture)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Unified 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - All 3 body rows feature a continuous, aligned vertical division line:
     - **Left Column (`lg:col-span-4` / 33.3% width):** Spend velocity dual-bar chart, AP outflow stream, spend category donut, and supplier quality scorecard.
     - **Right Column (`lg:col-span-8` / 66.7% width):** Expansive procurement lifecycle stage, 6-category cost center grid, and 9-column Audited Purchase Orders Hub.
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors identical to `erp_cover_page.html`: Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald Green (`#059669`), and Sunset Orange (`#ea580c`).
4. **Row 3 Perfect Height Balance:**
   - In the left 4-column space, **Spend by Category** (Card 5A) and **Supplier Quality & SLA Compliance** (Card 5B) stack vertically (`flex flex-col gap-3.5`), matching the exact height of the PO Master Table (Card 6) on the right.
5. **No Cluttered In-Page Tabs:**
   - Submodule navigation (PR, RFQ, GRN, Vendor Master) is deferred to the future Global Application Sidebar. The page remains focused on executive procurement monitoring and audited PO execution.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Amber rounded icon badge + `Purchase & Suppliers` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Procurement & SCM / Purchase Orders, Vendors & AP Stream`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterPOTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportPurchaseReport()`).

---

## 3. Top 4 Procurement KPI Pillar Cards (Colorful Matte Glass)

Styled identically to the master executive group dashboard `erp_cover_page.html`:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Total Spend This Month** | `৳ 2.14 Cr` | Budget: ৳ 2.50 Cr (85.6% Utilized) | `Controlled` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Pending PO Approvals** | `৳ 32.50 L` | 4 High-Value POs awaiting MD sign-off | `Action Req.` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Goods Inward (GRN In-Transit)**| `6 Shipments`| Chittagong Port & Tejgaon Hub Depot | `In Transit` | Solid Matte Emerald Green (`#059669/90`) |
| **Active Verified Suppliers** | `142 Vendors`| 98.2% On-time delivery rating | `Top Tier: 18` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row 4-Col (Left) / 8-Col (Right) Cards Layout

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: SPEND VELOCITY & PROCUREMENT LIFECYCLE STAGE                                          │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 1: Spend Velocity (4 cols)               │ CARD 2: Procurement Lifecycle & Lead Time (8)│
│ • 6-Month Budget vs Actual Spend Dual-Bar     │ • [GRAPH] Multi-Stage Procurement Flow       │
│ • Budget Variance Spline Overlay              │ • Indents/PR (3.40 Cr) → RFQ Quotes (2.80 Cr)│
│ • Compact Telemetry Widget (500x180)          │   → Approved PO (2.14 Cr) → GRN (1.82 Cr)    │
│ • Range Toggles (6M / YTD / FY26)             │   → Disbursed AP Payments (1.64 Cr)          │
│                                               │ • Expansive Stage Width (740x175)            │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 2: AP PAYABLES STREAM & COST CENTER ALLOCATION                                           │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: AP Outflow & Cash Runway (4 cols)     │ CARD 4: Cost Center & Vendor Allocation (8)  │
│ • Outflow Realized (+৳ 1.64 Cr) vs Due        │ • 6 Procurement Micro-Cards (3 cols x 2 rows)│
│ • Days Payable Outstanding (DPO): 42 Days     │ • Raw Materials, Plant Machinery, Fuel,      │
│ • Top 4 Vendor Payment Channels (L/C, RTGS)   │   IT Systems, Logistics, Packaging Materials │
│ • Tight, Snug Column Fit                      │ • Budget vs Utilized Progress Bars & Badges  │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: SPEND DISTRIBUTION, SUPPLIER QUALITY & AUDITED PO HUB                                 │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ LEFT STACK (4 cols): 2 Paired Cards           │ RIGHT COLUMN (8 cols): PO MASTER HUB         │
│                                               │                                              │
│ • CARD 5A: Spend Distribution by Category     │ CARD 6: Audited Purchase Orders (PO) Hub     │
│   Segmented SVG Donut Graph & Legend          │ • Expansive 9-Column Data Table with 6 Rows  │
│   Raw Materials 52.4%, Machinery 22.1%,       │ • Filter Tabs: All (142), Approved, Pending  │
│   Fuel 14.2%, Admin/IT 11.3%                  │ • Live Search, Vendor Filter & Pagination    │
│                                               │ • Live Procurement Summary Bar:              │
│ • CARD 5B: Supplier Quality & SLA Compliance  │   Committed POs = Realized GRN + In-Transit  │
│   On-time (98.2%), QC Reject (1.4%),          │ • Action Controls: View PO Details Modal,    │
│   Top Tier: 18, Audit Certified: 100%         │   Approve Sign-off, Download PO Slip         │
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Detailed Card Specifications

### 5.1 Row 1: Spend Velocity & Procurement Lifecycle Stage (4 cols + 8 cols)

#### Card 1: Procurement Spend vs Budget Dual-Bar Graph
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Header: Amber icon + "Procurement Spend Velocity" + Range pill (`6M`, `YTD`).
  - Graph Area: Custom responsive SVG Dual-Bar Chart (`viewBox="0 0 500 180"`):
    - Budget Ceiling Bar (Slate/Amber light `#fde68a`).
    - Actual PO Spend Bar (Vibrant Amber `#d97706`).
    - Budget Utilization Spline in Royal Blue (`#2563eb`).
  - Footer Telemetry:
    - Budget: `৳ 2.50 Cr` | PO Issued: `৳ 2.14 Cr` | Variance: `-14.4% (Favorable)`
- **Contextual Watermark:** Procurement Scales / Spend Ledger Art.

#### Card 2: Procurement Lifecycle & Lead Time Stage
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Flow icon + "Procurement Lifecycle & Lead Time Stage" + Lead Time Pill (`Avg Lead Time: 14 Days`).
  - Graph Area: Expansive SVG Pipeline Waterfall / Stage Flow (`viewBox="0 0 740 175"`):
    1. **Stage 1 (Purchase Requisitions / Indents):** `৳ 3.40 Cr` (48 Indents) — `slate-400`.
    2. **Stage 2 (Supplier RFQs & Bids):** `৳ 2.80 Cr` (32 Quotations) — `blue-400`.
    3. **Stage 3 (Approved Purchase Orders):** `৳ 2.14 Cr` (34 POs) — `amber-500`.
    4. **Stage 4 (Goods Received Notes - GRN):** `৳ 1.82 Cr` (Inspected & Inward) — `emerald-500`.
    5. **Stage 5 (Settled AP Payments):** `৳ 1.64 Cr` (Disbursed to Vendors) — `teal-600`.
  - Micro-Summary: PO Conversion `76.4%` • Avg Price Savings `8.2%` • Pending QC `৳ 32.0 L`.
- **Contextual Watermark:** Global Supply Chain Cargo Nodes.

---

### 5.2 Row 2: AP Payables Stream & Cost Center Allocation (4 cols + 8 cols)

#### Card 3: AP Outflow & Cash Runway Stream
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Metric Header: `৳ 1.64 Cr` disbursed out of `৳ 2.14 Cr` committed.
  - DPO Health Meter: **42 Days** (Target: 45 Days — `Optimal` green badge).
  - Outflow Mechanism Breakdown:
    - Import Letters of Credit (L/C): `৳ 94.5 L` (57.6%)
    - Bank RTGS Vendor Settlement: `৳ 52.1 L` (31.8%)
    - Pay Order / Account Cheques: `৳ 14.2 L` (8.7%)
    - Petty Cash / Local Purchases: `৳ 3.2 L` (1.9%)
- **Contextual Watermark:** Treasury Cash Register / Delivery Truck.

#### Card 4: Cost Center & Vendor Category Allocation
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - 3-Column x 2-Row Micro-Card Grid of the 6 core procurement centers:
    1. **Raw Materials & Polymers:** Budget ৳ 1.20 Cr | Spend: ৳ 1.12 Cr (93.3%) • Badge: `Optimal`
    2. **Industrial Plant Machinery:** Budget ৳ 50.0 L | Spend: ৳ 47.3 L (94.6%) • Badge: `CapEx Cap`
    3. **Fuel, Energy & Utilities:** Budget ৳ 35.0 L | Spend: ৳ 30.4 L (86.8%) • Badge: `Controlled`
    4. **Packaging Materials:** Budget ৳ 22.0 L | Spend: ৳ 18.2 L (82.7%) • Badge: `Favorable`
    5. **IT Infrastructure & Cloud Licenses:** Budget ৳ 15.0 L | Spend: ৳ 12.1 L (80.6%) • Badge: `On Budget`
    6. **Logistics & Freight Forwarding:** Budget ৳ 8.0 L | Spend: ৳ 6.8 L (85.0%) • Badge: `On Track`
- **Contextual Watermark:** Factory Cost Center Matrix.

---

### 5.3 Row 3: Spend Distribution, Supplier Quality & Audited PO Hub (4 cols + 8 cols)

#### Card 5A: Spend Distribution by Category (Left Stack - Top)
- **Column Span:** Part of `lg:col-span-4` (Stacked above Card 5B)
- **Component Anatomy:**
  - SVG Segmented Donut Chart (`viewBox="0 0 160 160"`):
    - Raw Materials & Polymers: `52.4%` (Amber `#d97706`)
    - Capital Machinery & Parts: `22.1%` (Blue `#2563eb`)
    - Fuel, Energy & Generator: `14.2%` (Purple `#7c3aed`)
    - Admin, IT & Packaging: `11.3%` (Emerald `#059669`)
  - Center Donut Label: `৳ 2.14 Cr Total`
  - 2-Column Legend with BDT values and percentage badges.

#### Card 5B: Supplier Quality & SLA Compliance Scorecard (Left Stack - Bottom)
- **Column Span:** Part of `lg:col-span-4` (Stacked below Card 5A to match Card 6 height)
- **Component Anatomy:**
  - 4 Vendor Quality Telemetry Bars:
    - **On-Time Delivery SLA:** `98.2%` (Target >95%) — `emerald-500`
    - **QC Inspection Pass Rate:** `98.6%` (Rejection: 1.4%) — `emerald-500`
    - **Price Competitiveness Index:** `94.1%` — `blue-500`
    - **High-Risk Vendor Watchlist:** `2 Vendors` — `rose-500`
  - Supplier Compliance Badge: `100% Tax & Trade License Validated`.

#### Card 6: Audited Purchase Orders (PO) Hub (Right Column)
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Tab filters (`All POs (142)`, `Approved (98)`, `Pending Sign-off (12)`, `Inward GRN (32)`) + Search.
  - Expansive 9-Column Interactive Table:
    1. **PO Date:** `06 Nov 2026`
    2. **PO #:** `PO-2026-0814` (monospace bold link)
    3. **Vendor / Supplier Name:** Bengal Polychem Industries PLC
    4. **Cost Center / Department:** Production / Raw Materials
    5. **Item Summary:** HDPE Granules (Grade A - 20 Tons)
    6. **Tax / VAT 7.5% (৳):** `1,35,000`
    7. **Total BDT (৳):** `19,35,000`
    8. **Status:** `Approved` (Emerald) / `Pending Sign-off` (Amber) / `In-Transit` (Blue)
    9. **Action:** View PO Slip, Approve, Track GRN
  - Balanced Reconciliation Summary Footer:
    - Total Committed POs: `৳ 2,14,00,000` = Realized GRN `৳ 1,81,50,000` + In-Transit `৳ 32,50,000`.
- **Contextual Watermark:** Audited Purchase Order Stamp.
