# Module 08: Reports & Analytics — UI & Content Blueprint

> **File Name:** `reports_module.html`  
> **Accent Theme:** Cyan (`#0891b2`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Multi-Entity Revenue Horizon (8 cols) + Working Capital CCC Dial (4 cols) | Du-Pont ROE & Financial Ratios (5 cols) + Subsidiary OPEX 2x2 Matrix (7 cols) | Statutory Filings Register (8 cols) + Reactive Regulatory Docket (4 cols)  
> **Contextual Watermark Art:** Analytical Data Curves / Financial Ratio Balance Scales / Executive Seal  
> **Status:** Locked & Live (`reports_module.html` verified & synchronized)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Domain-Specific Visual Instruments (Zero Formulaic Cloning):**
   - **Row 1 (8 cols + 4 cols):** Consolidated 6-Month Multi-Entity Revenue & Margin Horizon (custom multi-layer area/bar combo with consolidated gross margin curve) + Working Capital Cash Conversion Cycle (CCC) Dial (radial arc gauge with 42 days optimal liquidity & DSO/DIO/DPO formula breakdown).
   - **Row 2 (5 cols + 7 cols):** Executive Financial Ratios & Du-Pont ROE Analysis (3-tier Du-Pont breakdown: Margin x Turnover x Leverage) + Subsidiary OPEX Efficiency & Cost Allocation 2x2 Matrix (Tech, Logistics, Agro, Fintech).
   - **Row 3 (8 cols + 4 cols):** Statutory Audit Filings & Regulatory Compliance Register Table + Live Reactive Regulatory & Audit Docket (cryptographic SHA-256 validation fingerprint, Big-4 auditor assurance, submitting FCA officer details).
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors: Solid Royal Blue (`#2563eb`), Solid Royal Purple (`#7c3aed`), Solid Emerald Green (`#059669`), and Solid Sunset Orange (`#ea580c`), each equipped with an integrated mini SVG circular progress ring.
4. **Clean Borders & Zero Overlaps:**
   - No colored `border-l-4` strips on micro-cards; all cards use clean uniform frosted borders (`border border-slate-200/80`).
   - SVG charts feature centered hollow metrics with zero needle or badge overlaps.
5. **No Cluttered In-Page Tabs:**
   - In-page submodule tabs removed; navigation handled seamlessly from the Executive Portal and future global sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/75 backdrop-blur-md border-b border-white/60 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Cyan rounded icon badge + `Reports & Analytics` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Executive Intelligence / Consolidated Reports, Financial Ratios & Audit Trail`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterReportTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options.
  - **Export Button:** Clean outline button with download icon and `Export Financial BI` (`exportConsolidatedReport()`).

---

## 3. Top 4 Executive Analytics KPI Pillar Cards (Colorful Matte Glass)

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Consolidated Gross Margin** | `38.6%` | Target: 35.0% (+3.6% Alpha Margin) | `+4.4% Margin` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Group EBITDA Yield** | `৳ 2.84 Cr` | MTD Operating Profit (24.2% Margin) | `+18.2% YoY` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Net Profit Margin (PAT)** | `26.6%` | Net Profit: ৳ 1.28 Cr Disbursable | `Optimal Return`| Solid Matte Emerald Green (`#059669/90`) |
| **Statutory Audit Readiness** | `100% Score`| Big-4 Clean Assurance Opinion | `Certified Clean`| Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row Grid Architecture

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: MULTI-ENTITY REVENUE HORIZON (8 cols) & WORKING CAPITAL CCC DIAL (4 cols)              │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 1: Consolidated Multi-Entity Revenue Horizon (8 cols)    │ CARD 2: Working Capital Cash │
│ • 6-Month Inflow Bar & Area Stack (Jun – Nov 2026)            │   Conversion Dial (4 cols)   │
│ • Operating Revenue vs Invoiced Gross Track                   │ • Radial Arc Gauge: 42 Days  │
│ • Smooth Gross Margin Curve Overlay (38.6% Current Peak)      │ • Formula Breakdown:         │
│ • Total Group Revenue: ৳ 10.17 Cr (+24.8% YoY)                │   DSO 28d + DIO 34d - DPO 20d│
│                                                               │   = 42 Days (-16d Alpha)     │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 2: DU-PONT ROE ANALYSIS (5 cols) & SUBSIDIARY OPEX 2x2 MATRIX (7 cols)                   │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 3: Executive Financial Ratios & Du-Pont (5 cols)         │ CARD 4: Subsidiary OPEX      │
│ • ROE: 28.4% Deconstructed into 3 Drivers:                    │   Efficiency Matrix (7 cols) │
│   - Net Margin: 26.6% (PAT / Sales)                           │ • 2x2 Clean Frosted Grid:    │
│   - Asset Turnover: 0.92x (Sales / Assets)                    │   1. Inceptia Technologies   │
│   - Financial Leverage: 1.16x (Assets / Equity)               │   2. Inceptia Logistics Hubs │
│ • Current Ratio: 2.4x • Quick: 1.8x • D/E: 0.18               │   3. Inceptia Agro Processing│
│                                                               │   4. Inceptia Fintech Gateway│
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 3: STATUTORY FILINGS REGISTER (8 cols) & LIVE REGULATORY DOCKET (4 cols)                  │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 5: Statutory Audit Filings Register Table (8 cols)       │ CARD 6: Live Reactive        │
│ • 6 Core Filings (NBR IT-11GA, Mushak-9.1, RJSC XII, BSEC...) │   Regulatory Docket (4 cols) │
│ • Category Filters: All (6), NBR Tax, RJSC/BSEC, Banking/DIFE │ • SHA-256 Document Hash      │
│ • Live Search across Regulators, Filings, Audit Partners      │ • Big-4 Chartered Auditor    │
│ • Filing Dates, Responsible FCA Officers, Compliance Badges   │ • Submitting FCA Officer Info│
│                                                               │ • Regulatory Findings Notes  │
└───────────────────────────────────────────────────────────────┴──────────────────────────────┘
```

---

## 5. Row-by-Row Component Anatomy

### 5.1 Row 1: Consolidated Revenue Horizon & CCC Dial
- **Consolidated Multi-Entity Revenue Horizon (Card 1, 8 cols):** Custom SVG combo chart layering stacked monthly bar totals with a luminous emerald gross margin trajectory line, tracking consolidated group performance across all 4 subsidiaries.
- **Working Capital Cash Conversion Cycle Dial (Card 2, 4 cols):** Semi-circular radial gauge indicating 42 days net cash cycle with an itemized breakdown of Days Sales Outstanding (DSO), Days Inventory Outstanding (DIO), and Days Payable Outstanding (DPO).

### 5.2 Row 2: Du-Pont ROE & Subsidiary OpEx
- **Du-Pont ROE Analysis (Card 3, 5 cols):** Financial intelligence widget deconstructing Return on Equity into profit margin, asset utilization, and financial leverage alongside key solvency ratios.
- **Subsidiary OPEX Efficiency Matrix (Card 4, 7 cols):** 4 clean frosted micro-cards tracking operating expenditure, operating efficiency percentages, and group revenue contribution across all 4 legal entities without left-border colored lines.

### 5.3 Row 3: Statutory Filings & Live Regulatory Docket
- **Statutory Audit Filings Register Table (Card 5, 8 cols):** Audited compliance ledger detailing major regulatory submissions across NBR, RJSC, BSEC, Bangladesh Bank, and DIFE.
- **Live Reactive Regulatory Docket (Card 6, 4 cols):** Interactive inspection panel displaying selected filing's cryptographic SHA-256 checksum, external chartered auditor attestation, submitting officer credentials, and compliance clearance findings. Updates instantaneously upon clicking any row in the register.
