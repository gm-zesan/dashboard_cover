# Module 02: Sales & Invoicing — UI & Content Blueprint

> **File Name:** `sales_module.html`  
> **Accent Theme:** Emerald Green (`#059669`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Design Persona:** High-Velocity Commercial Operations & Real-Time Master-Detail Docket  
> **Status:** Redesigned & Approved (Distinct Layout & Unique Specialized Graphs: Area Trajectory, 3D Polygon Funnel, Speedometer Arc Gauge, Leaderboard & Live Docket)

---

## 1. Architectural Philosophy & Distinct Sales DNA

Unlike the accounting/ledger-oriented structure of Finance, **Sales & Invoicing** is designed with high-velocity commercial workflows and distinctive visual graph types:

1. **Distinctive 3-Row Layout Structure:**
   - **Row 1 (5 cols + 4 cols + 3 cols):** The Commercial Analytics Trio
     - **Left (5 cols):** Sales Revenue Trajectory & Forecast (Spline Curved Area Chart with Illuminated Gradient Glow).
     - **Middle (4 cols):** Authentic 3D Stepped Polygon Sales Funnel (4-stage trapezoidal conversion flow).
     - **Right (3 cols):** Monthly Quota Achievement Speedometer (Semi-circular radial arc gauge with needle and optimal zones).
   - **Row 2 (7 cols + 5 cols):** Regional Expansion & Corporate Client Dominance
     - **Left (7 cols):** Regional Commercial Belts Matrix (Hybrid grid with progress indicators, quotas, and regional growth badges across 6 commercial hubs).
     - **Right (5 cols):** Top Corporate Enterprise Clients Leaderboard (Ranked VIP buyer podium with contract tiers, billed volume, and retention status).
   - **Row 3 (8 cols + 4 cols):** Master-Detail Invoicing Operations Hub
     - **Left (8 cols):** Commercial Invoices Register Table (Interactive master table with live multi-term search, status tabs, and 1-click row selection).
     - **Right (4 cols):** Live Reactive Mushak-6.3 Digital Docket & QR Inspector (A persistent interactive panel that instantly updates when clicking any invoice row in the table, showing NBR QR code, tax breakdown, and instant Print/Download actions).

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"`).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Emerald Green shopping bag icon badge + `Sales & Commercial Invoicing` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Commercial & Revenue / Sales Trajectory, Conversion Funnel & Live Invoice Docket`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterInvoiceTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026`.
  - **Export Button:** Clean outline button with download icon (`exportSalesReport()`).

---

## 3. Top 4 Sales KPI Pillar Cards (With Integrated Mini-Rings)

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Visual Add-on |
| :--- | :--- | :--- | :--- | :--- |
| **Gross Invoiced Sales** | `৳ 4.82 Cr` | Target: ৳ 5.20 Cr (92.6% Achieved) | `▲ +14.2% MoM` | Mini SVG Ring Progress (93%) |
| **Realized Cash Collections** | `৳ 3.98 Cr` | Realized Inflow (Efficiency: 82.5%) | `▲ +9.4% MoM` | Mini SVG Ring Progress (83%) |
| **Overdue Receivables (AR)** | `৳ 84.20 L` | 14 Accounts Exceeding 45-Day Terms | `Auto-Follow-up` | Alert Shield Badge |
| **Commercial Quotes In-Play** | `৳ 1.65 Cr` | 18 High-Probability Proposals | `Win Rate: 68.4%` | Checkmark Rosette |

---

## 4. Distinct Row-by-Row Layout Specifications

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: THE COMMERCIAL ANALYTICS TRIO (5 cols + 4 cols + 3 cols)                              │
├───────────────────────────────┬───────────────────────────────┬──────────────────────────────┤
│ CARD 1: Sales Trajectory (5)  │ CARD 2: Stepped Funnel (4)    │ CARD 3: Quota Speedometer (3)│
│ • Curved Spline Area Chart    │ • Authentic Polygon Funnel    │ • Semi-Circular Radial Gauge │
│ • Emerald Gradient Glow Fill  │ • Leads (8.4 Cr) → Quotes     │ • Needle at 92.6% Quota      │
│ • Planned Quota vs Actual     │   (4.6 Cr) → Orders (3.8 Cr)  │ • Colored Zones: Amber/Blue/ │
│ • Active Nov Month Node Callout│   → Realized Inflow (3.98 Cr) │   Emerald with Gap Indicator │
├───────────────────────────────┴───────────────────────────────┴──────────────────────────────┤
│ ROW 2: REGIONAL COMMERCIAL BELTS & CLIENT LEADERBOARD (7 cols + 5 cols)                      │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 4: Regional Commercial Belts Matrix (7 cols)             │ CARD 5: Client Leaderboard(5)│
│ • 6 Active Belts: Dhaka North, Chittagong Port, Dhaka South,  │ • Ranked VIP Buyer Podium    │
│   Gazipur Industrial, Sylhet Eastern, Khulna Corridor         │ • #1 Bashundhara (৳ 1.74 Cr) │
│ • Quota Progress Bars, Invoices Count & Leading Belt Marker   │ • #2 Walton (৳ 98.50 L)      │
│                                                               │ • #3 Summit (৳ 92.40 L)      │
│                                                               │ • #4 Meghna (৳ 54.20 L)      │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 3: MASTER-DETAIL INVOICING OPERATIONS HUB (8 cols + 4 cols)                              │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 6: Commercial Invoices Register (8 cols)                 │ CARD 7: Live Mushak-6.3 (4)  │
│ • Interactive 9-Column Master Table                           │ • Real-time reactive docket  │
│ • Tabs: All (342), Paid (280), Partial (38), Overdue (24)     │ • Auto-updates on row click  │
│ • Click any row to dynamically inspect details on the right   │ • NBR QR Code + Hash Box     │
│ • Subtotals, 15% VAT, Total BDT and Status Pills              │ • Line Items & VAT Sheet     │
│                                                               │ • 1-Click Print & PDF Actions│
└───────────────────────────────────────────────────────────────┴──────────────────────────────┘
```

---

## 5. Live Reactive Master-Detail Workflow

- **Zero Popups Required for Inspection:** Clicking any invoice row in the table automatically highlights that row (`.invoice-row-active`) and transitions the Mushak-6.3 Digital Docket on the right to display that invoice's live data:
  - Reference number
  - Billing date & work order reference
  - Client organization name & address
  - Specific product/service item description
  - Net subtotal, 15% VAT, and Grand Total BDT
  - NBR digital verification hash & QR code
- **Quick Print & PDF:** Dedicated print button and PDF download buttons work directly from the docket.
