# Module 08: Reports & Analytics — UI & Content Blueprint

> **File Name:** `reports_module.html`  
> **Accent Theme:** Cyan (`#0891b2`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Unified 1/3 vs 2/3 Grid Split — **Left Columns: 4 cols (`lg:col-span-4`)** | **Right Columns: 8 cols (`lg:col-span-8`)**  
> **Contextual Watermark Art:** Analytical Data Curves / Financial Ratio Balance Scales / Executive Seal  
> **Status:** Locked & Approved (Consistent with `finance_module.html` 4-Col/8-Col Architecture)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Unified 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - All 3 body rows feature a continuous, aligned vertical division line:
     - **Left Column (`lg:col-span-4` / 33.3% width):** Multi-year revenue/EBITDA dual-bar chart, working capital cycle telemetry, entity revenue contribution donut, and statutory audit readiness scorecard.
     - **Right Column (`lg:col-span-8` / 66.7% width):** Expansive multi-entity financial ratio stage, 6-entity OPEX efficiency grid, and 9-column Master Compliance & Audit Filings Hub.
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors identical to `erp_cover_page.html`: Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald Green (`#059669`), and Sunset Orange (`#ea580c`).
4. **Row 3 Perfect Height Balance:**
   - In the left 4-column space, **Revenue Contribution by Entity** (Card 5A) and **Statutory Audit & Regulatory Health** (Card 5B) stack vertically (`flex flex-col gap-3.5`), matching the exact height of the Compliance Filings Table (Card 6) on the right.
5. **No Cluttered In-Page Tabs:**
   - Submodule navigation (Custom report builder, Tax schedules, Data warehouse exports) is deferred to the future Global Application Sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Cyan rounded icon badge + `Reports & Analytics` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Executive Intelligence / Consolidated Reports, Financial Ratios & Audit Trail`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterReportTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportConsolidatedReport()`).

---

## 3. Top 4 Executive Analytics KPI Pillar Cards (Colorful Matte Glass)

Styled identically to the master executive group dashboard `erp_cover_page.html`:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Consolidated Gross Margin** | `38.6%` | vs 34.2% (Prev Financial Year) | `▲ +4.4% Margin` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Group EBITDA** | `৳ 2.84 Cr` | MTD Consolidated Operating Profit | `▲ +18.2% YoY` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Net Profit Margin** | `26.6%` | Net Profit: ৳ 1.28 Cr | `Optimal Return`| Solid Matte Emerald Green (`#059669/90`) |
| **Statutory Audit Readiness** | `100% Score`| Clean opinion by External Chartered Auditor | `Certified Clean`| Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row 4-Col (Left) / 8-Col (Right) Cards Layout

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: CONSOLIDATED REVENUE VELOCITY & EXECUTIVE FINANCIAL RATIO STAGE                       │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 1: Consolidated Revenue Velocity (4 cols)│ CARD 2: Executive Financial Ratio Stage (8)  │
│ • 6-Month Gross Revenue vs OPEX Dual-Bar Chart│ • [GRAPH] Multi-Ratio Performance Waterfall  │
│ • EBITDA Margin Spline Overlay (24%-28%)      │ • Gross Margin (38.6%) → OPEX Ratio (10.4%)  │
│ • Compact Telemetry Widget (500x180)          │   → Net Margin (26.6%) → Current Ratio (2.4x)│
│ • Range Toggles (6M / YTD / FY26)             │   → Quick Ratio (1.8x) → ROE Return (22.4%)  │
│                                               │ • Expansive Stage Width (740x175)            │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 2: WORKING CAPITAL CYCLE & OPERATING ENTITY OPEX EFFICIENCY                              │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: Working Capital Cycle Telemetry (4)   │ CARD 4: Operating Entity OPEX Efficiency (8) │
│ • Cash Conversion Cycle (CCC): 34 Days        │ • 6 Entity Micro-Cards (3 cols x 2 rows):    │
│ • DIO (28 Days) + DSO (34 Days) - DPO (42 Days│ • Digital Solutions, Industrial Polymers,    │
│ • Operating Cash Flow Surplus: +৳ 1.28 Cr     │   Logistics & Port, EPC Engineering, Agro    │
│ • Tight, Snug Column Fit                      │ • Margin vs Target Progress Bars & Badges    │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: ENTITY CONTRIBUTION, AUDIT READINESS & MASTER COMPLIANCE HUB                          │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ LEFT STACK (4 cols): 2 Paired Cards           │ RIGHT COLUMN (8 cols): COMPLIANCE MASTER HUB │
│                                               │                                              │
│ • CARD 5A: Revenue Contribution by Entity     │ CARD 6: Master Audit Trail & Scheduled Filing│
│   Segmented SVG Donut Graph & Legend          │ • Expansive 9-Column Data Table with 6 Rows  │
│   Digital 44.5%, Polymers 28.2%,              │ • Filter Tabs: All (38), Certified, Due, NBR │
│   Logistics 16.4%, Engineering 10.9%          │ • Live Search, Auditor Filter & Pagination   │
│                                               │ • Live Compliance Status Summary Bar:        │
│ • CARD 5B: Statutory Audit & Regulatory Health│   100% Statutory Filings Cleared for FY26    │
│   NBR Tax: 100%, RJSC Returns: Up to date,    │ • Action Controls: View Audit Certificate    │
│   Bangladesh Bank Form C: Cleared             │   Modal, Download Statutory PDF, Verify Hash │
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Detailed Card Specifications

### 5.1 Row 1: Revenue Velocity & Executive Financial Ratio Stage (4 cols + 8 cols)

#### Card 1: Consolidated Revenue Velocity Dual-Bar Graph
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Header: Cyan icon + "Consolidated Revenue Velocity" + Range pill (`6M`, `YTD`).
  - Graph Area: Custom responsive SVG Dual-Bar Chart (`viewBox="0 0 500 180"`):
    - Consolidated Revenue Bar (Vibrant Cyan `#0891b2`).
    - Operating Expenditure Bar (Light Slate/Cyan `#cbd5e1`).
    - EBITDA Margin Spline in Sunset Orange (`#ea580c`).
  - Footer Telemetry:
    - Group Revenue: `৳ 4.82 Cr` | Group OPEX: `৳ 3.41 Cr` | EBITDA: `৳ 2.84 Cr`
- **Contextual Watermark:** Financial Trend Wave Curves Art.

#### Card 2: Executive Multi-Entity Financial Ratio Stage
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Scales icon + "Executive Financial Ratio & Profitability Stage" + Rating Pill (`Health Rating: AAA`).
  - Graph Area: Expansive SVG Ratio Stage Waterfall (`viewBox="0 0 740 175"`):
    1. **Gross Profit Margin:** `38.6%` (Benchmark >32%) — `blue-500`.
    2. **EBITDA Margin:** `28.2%` (Benchmark >22%) — `cyan-600`.
    3. **Net Profit Margin:** `26.6%` (Net Earnings ৳ 1.28 Cr) — `emerald-500`.
    4. **Current Ratio (Liquidity):** `2.4x` (Current Assets / Liabilities) — `purple-500`.
    5. **Quick Ratio (Acid Test):** `1.8x` (Excluding inventory) — `teal-500`.
    6. **Return on Equity (ROE):** `22.4%` (Consolidated Annualized) — `amber-500`.
  - Micro-Summary: Debt-to-Equity `0.28` • Interest Coverage `8.4x` • Solvency Index `Optimal`.
- **Contextual Watermark:** Neoclassical Financial Pillar Architecture.

---

### 5.2 Row 2: Working Capital Cycle & Entity OPEX Efficiency (4 cols + 8 cols)

#### Card 3: Working Capital Cycle Telemetry
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Metric Header: **34 Days** Cash Conversion Cycle (CCC).
  - Cash Cycle Components:
    - Days Inventory Outstanding (DIO): `28 Days`
    - Days Sales Outstanding (DSO): `34 Days`
    - Days Payable Outstanding (DPO): `42 Days`
    - Net CCC Formula: `28 + 34 - 42 = 34 Days`
  - Liquid Reserve: `6.4 Months` operational runway in primary bank accounts.
- **Contextual Watermark:** Precision Currency Flow Meter Art.

#### Card 4: Operating Entity OPEX Efficiency & Margin Grid
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - 3-Column x 2-Row Micro-Card Grid of the 6 corporate entities:
    1. **Inceptia Digital Solutions Ltd:** Revenue ৳ 2.14 Cr | Margin: 42.5% • Badge: `Top Margin`
    2. **Inceptia Industrial Polymers PLC:** Revenue ৳ 1.36 Cr | Margin: 28.4% • Badge: `Optimal`
    3. **Inceptia Port Logistics & Freight:** Revenue ৳ 79.0 L | Margin: 32.1% • Badge: `High Velocity`
    4. **Inceptia Engineering & EPC:** Revenue ৳ 52.5 L | Margin: 24.6% • Badge: `On Track`
    5. **Inceptia Agro-Tech Processing:** Revenue ৳ 32.0 L | Margin: 18.2% • Badge: `Controlled`
    6. **Inceptia Healthcare Diagnostics:** Revenue ৳ 24.0 L | Margin: 26.5% • Badge: `Growth Phase`
- **Contextual Watermark:** Corporate Entity Performance Matrix.

---

### 5.3 Row 3: Entity Contribution, Audit Readiness & Master Compliance Hub (4 cols + 8 cols)

#### Card 5A: Revenue Contribution by Business Line (Left Stack - Top)
- **Column Span:** Part of `lg:col-span-4` (Stacked above Card 5B)
- **Component Anatomy:**
  - SVG Segmented Donut Chart (`viewBox="0 0 160 160"`):
    - Digital Cloud Solutions: `44.5%` (Cyan `#0891b2`)
    - Industrial Polymers: `28.2%` (Blue `#2563eb`)
    - Port Logistics & Freight: `16.4%` (Purple `#7c3aed`)
    - EPC Engineering: `10.9%` (Emerald `#059669`)
  - Center Donut Label: `৳ 4.82 Cr Total`
  - 2-Column Legend with BDT values and percentage badges.

#### Card 5B: Statutory Audit & Regulatory Health Watch (Left Stack - Bottom)
- **Column Span:** Part of `lg:col-span-4` (Stacked below Card 5A to match Card 6 height)
- **Component Anatomy:**
  - 4 Statutory Compliance Tiers:
    - **NBR Corporate Tax & VAT:** `100% Cleared` (All returns filed) — `emerald-500`
    - **RJSC Annual Returns:** `Up-to-Date` (Form XII & Balance Sheet) — `emerald-500`
    - **Bangladesh Bank Foreign Remittance:** `Form C Approved` — `blue-500`
    - **External Auditor Opinion:** `Unqualified (Clean)` — `emerald-500`
  - Statutory Seal: `Certified by A. Qasem & Co. Chartered Accountants`.

#### Card 6: Master Audit Trail & Scheduled Compliance Filings Hub (Right Column)
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Tab filters (`All Filings (38)`, `Certified (32)`, `Scheduled (4)`, `Statutory NBR (2)`) + Search.
  - Expansive 9-Column Interactive Table:
    1. **Filing Period:** `FY2026 - Q2`
    2. **Report Title:** Consolidated Statement of Cash Flows & P&L
    3. **Entity:** Inceptia Enterprise Group (Consolidated)
    4. **Regulatory Authority:** National Board of Revenue (NBR)
    5. **Certifying Partner:** A. Qasem & Co. Chartered Accountants
    6. **Submission Date:** `04 Nov 2026`
    7. **Audit Status:** `Certified Clean` (Emerald pill)
    8. **Compliance Score:** `100% Passed`
    9. **Action:** View Audit Certificate Modal, Download Signed PDF, Hash Check
  - Balanced Filing Reconciliation Summary Footer:
    - 38 Statutory Filings: 32 Certified Clean, 4 In Progress, 2 Scheduled for Next Period.
- **Contextual Watermark:** Audited Executive Compliance Stamp Art.
