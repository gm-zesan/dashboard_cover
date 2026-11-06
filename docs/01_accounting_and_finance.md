# Module 01: Accounting & Finance — UI & Content Blueprint

> **File Name:** `finance_module.html`  
> **Accent Theme:** Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald (`#059669`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Unified 1/3 vs 2/3 Grid Split — **Left Columns: 4 cols (`lg:col-span-4`)** | **Right Columns: 8 cols (`lg:col-span-8`)**  
> **Contextual Watermark Art:** Neoclassical Bank Treasury Building / General Ledger Scales / Chart Curves / Compliance Shield  
> **Status:** Updated & Approved (Narrower Left Column + Expansive Right Column Architecture)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Spans edge-to-edge on large desktop monitors without artificial bounding constraints.
2. **Unified 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - All 3 body rows feature a continuous, aligned vertical division line:
     - **Left Column (`lg:col-span-4` / 33.3% width):** Compact, highly focused financial telemetry (trend bars, cash flow stream, revenue donut, receivables aging).
     - **Right Column (`lg:col-span-8` / 66.7% width):** Expansive, wide-stage views (P&L Waterfall Bridge Chart with wide bars, 3-column Expense Accounts allocation grid, and 9-column General Ledger table).
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - The top 4 KPI cards feature high-saturation matte colors identical to `erp_cover_page.html`: Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald Green (`#059669`), and Sunset Orange (`#ea580c`).
4. **Row 3 Perfect Height Balance:**
   - In the left 4-column space, **Income & Revenue Sources** (Card 5A) and **Accounts Receivable (AR) Aging & Tax Compliance** (Card 5B) stack vertically (`flex flex-col gap-3.5`), matching the exact height of the General Ledger table (Card 6) on the right.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Royal Blue rounded icon badge + `Finance & Accounting` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Finance / Financial Performance, Statements & General Ledger`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterLedgerTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportFinancialReport()`).

---

## 3. Top 4 Financial KPI Pillar Cards (Colorful Matte Glass)

Styled identically to the master executive group dashboard `erp_cover_page.html`:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Operating Income** | `৳ 4.82 Cr` | vs ৳ 4.22 Cr (Prev Month) | `▲ +14.2% MoM` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Gross Profit** | `৳ 1.36 Cr` | Production & Delivery Margin | `▲ +18.6%` (Margin: 28.2%) | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Total Expenses** | `৳ 3.41 Cr` | vs ৳ 3.10 Cr (Consolidated OPEX) | `▲ +9.8%` | Solid Matte Emerald Green (`#059669/90`) |
| **Net Profit** | `৳ 1.28 Cr` | Net Bottom-Line Profit | `▲ +21.5%` (Margin: 26.6%) | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row 4-Col (Left) / 8-Col (Right) Cards Layout

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: CORE FINANCIAL PERFORMANCE GRAPHS                                                     │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 1: Financial Performance (4 cols)        │ CARD 2: Statement of Profit or Loss (8 cols) │
│ • 6-Month Income vs Expense Dual-Bar Chart    │ • [GRAPH] Interactive Waterfall Bridge Chart │
│ • Net Profit Margin % Spline Overlay          │ • Revenue (4.82 Cr) → COGS (-3.46 Cr)        │
│ • Compact Telemetry Widget (500x180)          │   → GP (1.36 Cr) → OPEX (-68 L)              │
│ • Period Range Toggles (6M / YTD / FY26)      │   → EBITDA (68 L) → Net Profit (1.28 Cr)     │
│                                               │ • Expansive Stage Width (740x175)            │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 2: LIQUIDITY STREAM & OPERATING EXPENDITURES                                             │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: Cash Flow & Liquidity Stream (4 cols) │ CARD 4: Expense Accounts Overview (8 cols)   │
│ • Inflows (+৳ 3.98 Cr) vs Outflows (৳ 2.70 Cr)│ • 6 Ledger Account Micro-Cards (#5100-#5600) │
│ • Surplus (+৳ 1.28 Cr) & 6.4 Mos Runway       │ • Raw Materials, Payroll, Fuel, Logistics,   │
│ • 4 Active Bank Accounts Breakdown            │   Admin, IT Cloud with Progress Bars & Badges│
│ • Tight, Snug Column Fit                      │ • Generous 3-Column x 2-Row Micro-Grid       │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: REVENUE DISTRIBUTION, RECEIVABLES & AUDITED GENERAL LEDGER                            │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ LEFT STACK (4 cols): 2 Paired Cards           │ RIGHT COLUMN (8 cols): GENERAL LEDGER HUB    │
│                                               │                                              │
│ • CARD 5A: Income & Revenue Sources           │ CARD 6: General Ledger & Vouchers            │
│   Segmented SVG Donut Graph & Legend          │ • Expansive 9-Column Data Table with 6 Rows  │
│   Commercial Sales 59.1%, Toll 24.5%,         │ • Type Tabs: All (284), PV, RV, JV, CV       │
│   AMC 11.2%, Bank Returns 5.2%                │ • Live Search, Status Filter & Pagination    │
│                                               │ • Live Balanced Trial Balance Bar:           │
│ • CARD 5B: Receivables (AR) Aging & Tax       │   Debits (1,22,42,000) = Credits (Balanced)  │
│   0-30d (64.1%), 31-60d (20.7%),              │ • Action Controls: View Voucher PDF Preview  │
│   61-90d (9.7%), >90d (5.5%) + NBR Form 9.1   │   Modal, Approve Vouchers, Batch Audit       │
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Detailed Card Specifications

### 5.1 Row 1: The Two Financial Performance Graphs (4 cols + 8 cols)

#### Card 1: Financial Performance Dual-Bar & Margin Spline Graph
- **Width:** `lg:col-span-4`.
- **Chart Element:** `<svg id="finance-svg">` (`viewBox="0 0 520 180"`).
- **Visualization:**
  - Blue bars: Operating Income for Jun–Nov 2026.
  - Slate bars: Total Expense.
  - Emerald spline line: Net Margin % trajectory with data points.
- **Interactivity:** Period selector (`6M / YTD / FY26`) and floating hover tooltip card (`#finance-tooltip`).

#### Card 2: Statement of Profit or Loss (P&L) Waterfall Bridge Graph
- **Width:** `lg:col-span-8` (Expansive 8-Column Stage).
- **Chart Element:** `<svg id="pl-waterfall-svg">` (`viewBox="0 0 740 175"`).
- **Waterfall Cascade:**
  1. Revenue (Turnover): `+৳ 4.82 Cr` (100% | Blue | bar width: 48px)
  2. Less COGS (Direct Materials): `-৳ 3.46 Cr` (-71.8% | Rose)
  3. Gross Profit (GP): `৳ 1.36 Cr` (**28.2% Margin** | Purple)
  4. Less OPEX (Admin & Overhead): `-৳ 0.68 Cr` (-14.1% | Amber)
  5. Operating EBITDA: `৳ 0.68 Cr` (**14.1% Margin** | Indigo)
  6. Add Other Income (Treasury/Returns): `+৳ 0.60 Cr` (+12.5% | Emerald)
  7. Net Profit before Tax (Final NPBT): `৳ 1.28 Cr` (**26.6% Margin** | Teal/Emerald)
- **Visual Features:** Connecting dashed bridge lines between steps, top value labels, and interactive hover tooltip (`#waterfall-tooltip`).
- **Footer Pills:** `Gross Margin: 28.2%`, `EBITDA: 14.1%`, `Net Profit: 26.6%`.

---

### 5.2 Row 2: Liquidity Stream & Operating Expenditures (4 cols + 8 cols)

#### Card 3: Cash Flow & Liquidity Stream
- **Width:** `lg:col-span-4` (Snug Telemetry Column).
- **Gauges:**
  - Operating Inflow: `+৳ 3.98 Cr` (+14.2% vs budget).
  - Operating Outflow: `-৳ 2.70 Cr` (67.8% utilization).
  - Runway Buffer: `6.4 Mos` (Liquid: `৳ 3.84 Cr`).
- **Active Corporate Bank Accounts:**
  1. `BRAC Bank (Corporate)` — Operating A/C: **৳ 1.82 Cr**
  2. `City Bank (Trade / LC)` — Import & LC: **৳ 1.15 Cr**
  3. `DBBL Payroll A/C` — Salary Pool: **৳ 68.4 লাখ**
  4. `Central Treasury Vault` — Cash Vault: **৳ 18.5 লাখ**

#### Card 4: Expense Accounts Overview & Budget Allocation
- **Width:** `lg:col-span-8` (Expansive Allocation Grid).
- **Layout:** Generous 3-column micro-card grid (`glass-micro-card` with `p-2.5`):
  - `#5100 Raw Materials & COGS:` ৳ 1.84 Cr / ৳ 2.20 Cr (83.6%) — `Optimal`
  - `#5200 Enterprise Payroll:` ৳ 68.5 L / ৳ 72.0 L (95.1%) — `On Track`
  - `#5300 Utilities & Site Fuel:` ৳ 22.4 L / ৳ 25.0 L (89.6%) — `Attention`
  - `#5400 Freight & Logistics:` ৳ 34.2 L / ৳ 38.0 L (90.0%) — `On Track`
  - `#5500 Admin & Facilities:` ৳ 18.2 L / ৳ 22.0 L (82.7%) — `Under Budget`
  - `#5600 Cloud Infra & IT:` ৳ 13.7 L / ৳ 15.0 L (91.3%) — `On Track`
- **Header Badge:** Total Spend: `৳ 3.41 Cr` (88.5% of Budget).

---

### 5.3 Row 3: Revenue Distribution, Receivables & Audited General Ledger (4 cols + 8 cols)

#### Card 5A: Income & Revenue Sources Donut Graph (Left Top, 4 cols)
- **Chart Type:** Interactive SVG Segmented Donut Chart (`viewBox="0 0 36 36"` with radius `15.9155`).
- **Revenue Segments:** Commercial Sales (59.1% | ৳ 2.85 Cr), Toll Automation (24.5% | ৳ 1.18 Cr), AMC Services (11.2% | ৳ 54.0 L), Bank Returns (5.2% | ৳ 25.0 L).
- **Dynamic Interaction:** Linked hover highlighting the slice, dimming other slices, and updating the central amount/label in real time.

#### Card 5B: Accounts Receivable (AR) Aging & Tax Compliance (Left Bottom, 4 cols)
- **Total Outstanding AR:** `৳ 84.5 লাখ` (100% matched with master group dashboard).
- **4-Tier Aging Breakdown:**
  1. `0–30 Days (Current Invoices):` **৳ 54.2 লাখ (64.1%)** — Emerald progress bar (`Healthy`)
  2. `31–60 Days (Grace Period):` **৳ 17.5 লাখ (20.7%)** — Blue progress bar (`Follow-up Due`)
  3. `61–90 Days (Payment Notice):` **৳ 8.2 লাখ (9.7%)** — Amber progress bar (`Payment Notice`)
  4. `>90 Days (Overdue / Review):` **৳ 4.6 লাখ (5.5%)** — Rose progress bar (`Provision / Legal`)
- **Compliance Badges:** NBR VAT Form 9.1 Filed (Clean) | Next Clearing: Walton (৳ 12.5 L) Nov 10.

#### Card 6: General Ledger Transactions & Vouchers Hub (Right 8 cols)
- **Width:** `lg:col-span-8` (Full Wide Ledger Stage).
- **Controls:** Type Tabs (`All (284)`, `PV`, `RV`, `JV`, `CV`), status selector (`Posted`, `Pending`, `Draft`).
- **Data Table:** Expansive 9-column table (`py-2 px-2`) displaying date, voucher ID, type tag, particulars (Dr/Cr), beneficiary, debit, credit, status badge, and `View`/`Approve` actions with ample horizontal margin.
- **Live Balanced Trial Balance Bar:**
  - Debits: `৳ 1,22,42,000` | Credits: `৳ 1,22,42,000` | Diff: `৳ 0.00 (Balanced)`.
- **Pagination:** `1-6 of 284 Vouchers`.

---

## 6. Modals Specification

- **Preserved Modal:**
  - **Voucher Preview / Print Modal (`#preview-modal`):** Used to inspect posted transaction details, beneficiary info, amount, and trigger `window.print()` for audited PDF voucher printouts.
- **Removed Modals & Actions:**
  - `+ New Journal Entry` and `Payment Voucher` modal forms have been removed from this page.

---

## 7. Data Synchronization Table with Cover Page

All financial figures in `finance_module.html` correlate 100% with the master executive dashboard `erp_cover_page.html`:

| Metric Name | `erp_cover_page.html` | `finance_module.html` | Status |
| :--- | :--- | :--- | :--- |
| **Total Revenue / Income** | `৳ 4.82 Cr` | `৳ 4.82 Cr` | Exact Match |
| **Cost of Goods Sold (COGS)**| Derived (৳ 3.46 Cr) | `৳ 3.46 Cr` (71.8%) | Exact Match |
| **Gross Profit** | `৳ 1.36 Cr (28.2%)` | `৳ 1.36 Cr (28.2%)` | Exact Match |
| **Operating Expenses (Total)**| `৳ 3.41 Cr` | `৳ 3.41 Cr` (Card 4) | Exact Match |
| **Net Profit / Net Margin** | `৳ 1.28 Cr (26.6%)` | `৳ 1.28 Cr (26.6%)` | Exact Match |
| **Net Liquid Balance** | `৳ 3.84 Cr` | `৳ 3.84 Cr` (Card 3) | Exact Match |
| **Accounts Receivable (AR)** | `৳ 84.5 লাখ` | `৳ 84.5 লাখ` (Card 5B) | Exact Match |
| **Cash Surplus** | `+৳ 18.3 লাখ` (Daily) | `+৳ 1.28 Cr` (Monthly) | Aligned |
