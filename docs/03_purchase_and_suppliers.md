# Module 03: Purchase & Suppliers — UI & Content Blueprint

> **File Name:** `purchase_module.html`  
> **Accent Theme:** Amber / Bronze (`#d97706`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald (`#059669`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Design Persona:** Strategic SCM Sourcing, Budget Variance Control & Inward Cargo Tracking  
> **Status:** Locked & Approved (Distinct Layout & Specialized Procurement Graphs: Spend Horizon Stacked Bar, Lifecycle Lead-Time Pipeline, Quality SLA Scorecard & Live Inward GRN Docket)

---

## 1. Architectural Philosophy & Distinct Procurement DNA

Unlike Finance or Sales, **Purchase & Suppliers** is designed specifically around procurement budget control, vendor lead times, and inward goods logistics:

1. **Distinctive 3-Row Layout Structure:**
   - **Row 1 (7 cols + 5 cols):** Procurement Spend Horizon & Lifecycle Pipeline
     - **Left (7 cols):** Procurement Spend Horizon & Multi-Category Stacked Bar Chart with upper Budget Ceiling line (`৳ 2.50 Cr`) and monthly variance.
     - **Right (5 cols):** Procurement Lifecycle & Lead-Time Pipeline (5-stage execution flow with cycle turnaround metrics).
   - **Row 2 (4 cols + 8 cols):** Vendor Governance & Major Sourcing Verticals
     - **Left (4 cols):** Supplier SLA & Quality Compliance Scorecard (Non-overlapping progress telemetry: On-time SLA 98.2%, QC Pass 98.6%, Price Index 94.1%, NBR Tax 100%).
     - **Right (8 cols):** Strategic Spend Categories & Major Sourcing 2x2 Frosted Grid (Raw Polymers, Plant Machinery, Utilities & Energy, Packaging & Freight).
   - **Row 3 (8 cols + 4 cols):** Master-Detail Purchase Orders & Inward Shipment Hub
     - **Left (8 cols):** Audited Purchase Orders (PO) Hub Table (Filter tabs: All, Approved, Pending Sign-off, In Transit; live multi-term search `⌘K`).
     - **Right (4 cols):** Live Purchase Order & Inward Shipment Docket (Master-detail inspector: clicking any PO in the table immediately updates the docket with PO details, ISO 9001 test seal, and live cargo GPS/truck tracker with progress bar).

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"`).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Amber Procurement Icon badge + `Purchase & Suppliers` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Procurement & SCM / Purchase Orders, Vendor Relations & Inward Goods`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterPOTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026`.
  - **Export Button:** Clean outline button with download icon (`exportPurchaseReport()`).

---

## 3. Top 4 Procurement KPI Pillar Cards

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Visual Detail |
| :--- | :--- | :--- | :--- | :--- |
| **Total Spend This Month** | `৳ 2.14 Cr` | Budget: ৳ 2.50 Cr (85.6% Utilized) | `Controlled` | Savings: ৳ 36.0 L |
| **Pending PO Approvals** | `৳ 32.50 L` | 4 High-Value POs awaiting MD sign-off | `Action Req.` | Avg Sign-off: 2.1 Days |
| **Goods Inward (GRN In-Transit)**| `6 Shipments`| Chittagong Port & Tejgaon Hub Depots | `In Transit` | QC Pass: 98.6% |
| **Active Verified Suppliers** | `142 Vendors`| 98.2% On-time delivery rating | `Top Tier: 18` | Compliance: 100% |

---

## 4. Distinct Row-by-Row Layout Specifications

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: PROCUREMENT SPEND HORIZON & LIFECYCLE PIPELINE (7 cols + 5 cols)                      │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 1: Procurement Spend Horizon & Budget Ceiling (7 cols)   │ CARD 2: Lifecycle Pipeline(5)│
│ • Multi-Category Stacked Bar Chart (Jun to Nov)               │ • 5-Stage Execution Flow     │
│ • Raw Materials (Amber) + CapEx (Blue) + Utilities (Teal)     │ • 1. Indents / PR (৳ 3.40 Cr)│
│ • Upper Red Dashed Budget Ceiling Line (৳ 2.50 Cr)            │ • 2. Supplier Bids (৳ 2.80 Cr│
│ • Nov Active Month Marker (-14.4% Savings Callout)            │ • 3. Approved PO (৳ 2.14 Cr) │
│                                                               │ • 4. Goods Inward (৳ 1.82 Cr)│
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 2: VENDOR GOVERNANCE & STRATEGIC SPEND VERTICALS (4 cols + 8 cols)                       │
├───────────────────────────────┬──────────────────────────────────────────────────────────────┤
│ CARD 3: Supplier SLA (4 cols) │ CARD 4: Strategic Spend Categories 2x2 Grid (8 cols)         │
│ • Non-overlapping Progress:   │ • Raw Polymers & Chemicals: ৳ 1.12 Cr (93.3% utilized)       │
│   - On-time Delivery (98.2%)  │ • Plant Machinery & CapEx: ৳ 47.30 L (94.6% utilized)        │
│   - QC Pass Rate (98.6%)      │ • Fuel, Energy & Generator: ৳ 30.40 L (86.8% utilized)       │
│   - Price Benchmark (94.1%)   │ • Packaging & Logistics: ৳ 24.30 L (86.8% utilized)          │
│   - NBR Tax Validated (100%)  │ • Clean Frosted Cards with Progress Meters & Top Suppliers   │
├───────────────────────────────┴──────────────────────────────────────────────────────────────┤
│ ROW 3: MASTER-DETAIL PURCHASE ORDERS & INWARD SHIPMENT HUB (8 cols + 4 cols)                 │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 5: Audited Purchase Orders (PO) Hub (8 cols)             │ CARD 6: Live PO Docket (4)   │
│ • Interactive 9-Column Master Table                           │ • Real-time reactive docket  │
│ • Tabs: All (142), Approved (98), Pending (12), In-Transit(32)│ • Auto-updates on row click  │
│ • Click any row to dynamically inspect details & cargo tracker│ • ISO 9001 Tested Seal       │
│ • PO Date, Supplier, Cost Center, Items, VAT 7.5%, Total BDT  │ • Live Inward Cargo Tracker  │
│                                                               │ • GPS Route & ETA Progress   │
└───────────────────────────────────────────────────────────────┴──────────────────────────────┘
```

---

## 5. Live Reactive Master-Detail Workflow

- **Click Any PO to Inspect:** Clicking any row in the table (`.po-row-active`) immediately transitions the right-hand docket to display:
  - Purchase order number & issued date
  - Supplier corporate name, trade license, and banking details
  - Specific item specifications and quantities
  - Quality certification seal (`ISO 9001 Passed`)
  - Live Inward Logistics Tracker (Destination depot, transport carrier truck ID, and animated ETA progress bar).
- **Clean Layout:** No clutter, zero overlapping text or needle lines, and no redundant buttons.
