# Module 01: Accounting & Finance — UI & Content Blueprint

> **File Name:** `finance_module.html`  
> **Accent Theme:** Royal Blue (`#2563eb`, `text-blue-600`, `bg-blue-50/70`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Contextual Watermark Art:** Neoclassical Bank Treasury Building / General Ledger Scales / Chart Curves  
> **Status:** Updated & Approved (Compact High-Density Visual Graphs Layout)

---

## 1. Architectural Philosophy & Compact Layout Rules

1. **Modular Workspace Independence:**
   - Unlike the master cover portal (`erp_cover_page.html`), this is a dedicated, deep-dive financial workspace.
   - **No Internal Module Workspaces Card:** Navigation across other modules is handled via a unified global sidebar (to be integrated globally), eliminating clutter inside the page canvas.
2. **Executive Focus & Decluttered Header:**
   - Creation buttons (`+ New Journal Entry`, `Payment Voucher`) and creation modals have been removed from the header. This keeps the page focused on performance analytics, financial statements, and ledger auditing.
   - The period badge (`FY 2026-27 (Period 05)`) is removed from the header branding, leaving clean typography with breadcrumbs.
3. **Graph-First Visual Representation:**
   - Both **Statement of Profit or Loss (P&L)** and **Income & Revenue Sources** are represented with interactive visual SVG graphs rather than heavy text tables.
   - P&L uses an executive **Waterfall / Bridge Chart** to immediately visualize the deduction cascade from Revenue to Net Profit.
   - Income Sources uses an interactive **Segmented Donut Chart** with linked hover effects and dynamic central totals.
4. **Compact Card Sizing ("Coto Coto" Density):**
   - Padding reduced to `p-3.5` across all cards to minimize vertical bloat.
   - Chart heights constrained to `h-40 sm:h-44` (viewBox `520x180` and `540x175`).
   - Expense Accounts formatted as a compact 3-column micro-card grid (`glass-micro-card`) rather than a tall table.
   - General Ledger table uses compact row height (`py-2`) with balanced trial balance totals.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-4 w-px bg-slate-300/60`.
  - Icon & Title: Royal Blue rounded icon badge + `Finance & Accounting` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Finance / Financial Performance, Statements & General Ledger`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterLedgerTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1–30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportFinancialReport()`).

---

## 3. Top 4 Financial KPI Pillar Cards (Compact Height)

Four high-contrast frosted glass cards with 58% opacity, soft backdrop blur, and contextual SVG watermark art:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Visual Icon / Watermark |
| :--- | :--- | :--- | :--- | :--- |
| **Operating Income** | `৳ 4.82 Cr` | vs ৳ 4.22 Cr (Prev Month) | `▲ +14.2% MoM` (Emerald) | Currency / Treasury Shield |
| **Gross Profit** | `৳ 1.36 Cr` | Production & Delivery Margin | `Margin: 28.2%` (Violet) | Bar Growth Analytics |
| **Operating Expenses** | `৳ 3.41 Cr` | vs ৳ 3.10 Cr (Consolidated OPEX) | `▲ +9.8% Spend` (Amber) | Clipboard Ledger Book |
| **Net Cash Flow & Profit**| `৳ 1.28 Cr` | Net Bottom-Line Profit | `Margin: 26.6%` (Rose) | Lightning / Cash Inflow Wave |

---

## 4. Standalone Financial Cards Structure

The page body is organized into 4 responsive grid rows featuring 6 standalone executive cards:

```
┌───────────────────────────────────────────────┬──────────────────────────────────────────────┐
│ CARD 1: Financial Performance Graph (7 cols)  │ CARD 2: Cash Flow & Liquidity Stream (5 cols)│
│ • 6-Month Income vs Expense Bar Chart         │ • Inflows (+৳ 3.98 Cr) vs Outflows (৳ 2.70 Cr)│
│ • Net Profit Margin % Spline Overlay          │ • Surplus (+৳ 1.28 Cr) & 6.4 Mos Runway       │
│ • Interactive SVG Tooltips & Period Toggles   │ • 4 Corporate Bank Balances                  │
├───────────────────────────────────────────────┼──────────────────────────────────────────────┤
│ CARD 3: Statement of Profit or Loss (7 cols)  │ CARD 4: Income & Revenue Sources (5 cols)    │
│ • [GRAPH] Interactive Waterfall Bridge Chart  │ • [GRAPH] Segmented SVG Donut Chart          │
│ • Revenue (4.82 Cr) → COGS (-3.46 Cr)         │ • Commercial Sales (59.1% / ৳ 2.85 Cr)       │
│   → GP (1.36 Cr) → OPEX (-68 L)               │ • Toll Automation (24.5% / ৳ 1.18 Cr)        │
│   → EBITDA (68 L) → Other (+60 L)             │ • AMC Services (11.2% / ৳ 54.0 L)            │
│   → Net Profit (1.28 Cr / 26.6%)              │ • Bank Returns (5.2% / ৳ 25.0 L)             │
│ • Gross (28.2%), EBITDA (14.1%), NP (26.6%)   │ • Interactive slice & legend linked hover    │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ CARD 5: Expense Accounts Overview & Corporate Budget Allocation (12 cols)                    │
│ • Compact 3-Column x 2-Row Micro-Card Grid (#5100-#5600)                                     │
│ • Spend vs Budget, Visual Progress Bars, Burn Rate, and Status Tags                          │
├──────────────────────────────────────────────────────────────────────────────────────────────┤
│ CARD 6: General Ledger Transactions & Double-Entry Vouchers Hub (12 cols)                    │
│ • Compact Ledger Table with Type Tabs: All (284), PV, RV, JV, CV                             │
│ • Status Filter: Posted / Approved, Pending Audit, Draft                                     │
│ • Live Balanced Trial Balance Bar: Debits (৳ 1,22,42,000) = Credits (৳ 1,22,42,000)         │
│ • Action Controls: View Voucher PDF Preview Modal, Approve Vouchers, Pagination              │
└──────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 5. Detailed Specifications per Standalone Card

### 5.1 Card 1: Financial Performance Graph View
- **Grid Footprint:** `col-span-12 lg:col-span-7`.
- **Visualization:** Dual-layer SVG rendering (`viewBox="0 0 520 180"`):
  - Multi-bar columns comparing **Operating Income** (Blue `#2563eb`) and **Expenses** (Slate `#94a3b8`) for Jun–Nov 2026.
  - Spline curve overlay indicating **Net Margin %** (Emerald `#10b981`) with circular data markers.
- **Interactivity:** Dynamic SVG cursor tracking with animated glassmorphic tooltip card (`#finance-tooltip`) rendering Income, Expense, Net Profit, and Margin % upon hover.
- **Period Filter:** Pill toggles for `6M`, `YTD`, and `FY26`.

### 5.2 Card 2: Cash Flow & Liquidity Stream
- **Grid Footprint:** `col-span-12 lg:col-span-5`.
- **Cash Flow Gauges:**
  - **Operating Cash Inflow:** `৳ 3.98 Cr` (+14.2% vs budget).
  - **Operating Cash Outflow:** `৳ 2.70 Cr` (67.8% utilization).
  - **Net Operating Surplus:** `+৳ 1.28 Cr` with runway indicator (`6.4 Months Operating Buffer`).
- **Active Bank Balances Mini-Grid:**
  1. `BRAC Bank (Corporate)` — Operating A/C: **৳ 1.82 Cr** (`Active`)
  2. `City Bank (Trade / LC)` — Import & LC: **৳ 1.15 Cr** (`Active`)
  3. `Dutch-Bangla Bank` — Payroll Disbursement: **৳ 68.4 লাখ** (`Funded`)
  4. `Central Treasury` — Petty & Vault: **৳ 18.5 লাখ** (`Reserve`)

### 5.3 Card 3: Statement of Profit or Loss (P&L) — Waterfall Bridge Graph
- **Grid Footprint:** `col-span-12 lg:col-span-7`.
- **Graph Type:** Financial Waterfall / Step-Down Bridge Chart (`viewBox="0 0 540 175"`).
- **Mathematical Flow & Coordinate Bridge:**
  1. **Revenue (Turnover):** `+৳ 4.82 Cr` (Solid Blue `#2563eb`, 100%)
  2. **Less COGS (Direct Materials):** `-৳ 3.46 Cr` (Step-down Rose `#f43f5e`, -71.8%)
  3. **Gross Profit (GP Subtotal):** `৳ 1.36 Cr` (Purple `#8b5cf6`, **28.2% Margin**)
  4. **Less OPEX (Admin & Overhead):** `-৳ 0.68 Cr` (Step-down Amber `#f59e0b`, -14.1%)
  5. **Operating EBITDA (Subtotal):** `৳ 0.68 Cr` (Indigo `#6366f1`, **14.1% Margin**)
  6. **Add Other Income (Treasury/Returns):** `+৳ 0.60 Cr` (Step-up Emerald `#10b981`, +12.5%)
  7. **Net Profit before Tax (Final Total):** `৳ 1.28 Cr` (Teal/Emerald `#059669`, **26.6% Margin**)
- **Visual Features:** Connecting dashed alignment bridge lines between adjacent bars, value labels above each bar, and floating hover tooltip (`#waterfall-tooltip`).
- **Bottom Footnote Pills:** `Gross Margin: 28.2%`, `EBITDA: 14.1%`, `Net Profit: 26.6%`.

### 5.4 Card 4: Income & Revenue Sources — Donut Graph
- **Grid Footprint:** `col-span-12 lg:col-span-5`.
- **Graph Type:** Interactive SVG Segmented Donut Chart (`viewBox="0 0 36 36"` with radius `15.9155`).
- **Revenue Segments:**
  1. **Commercial Product Sales:** `59.1%` | `৳ 2.85 Cr` (Blue `#2563eb` | `stroke-dasharray="59.1, 100"`)
  2. **Toll Highway Automation:** `24.5%` | `৳ 1.18 Cr` (Emerald `#10b981` | `stroke-dashoffset="-59.1"`)
  3. **Engineering & AMC Services:** `11.2%` | `৳ 54.0 লাখ` (Purple `#8b5cf6` | `stroke-dashoffset="-83.6"`)
  4. **Treasury & Bank Returns:** `5.2%` | `৳ 25.0 লাখ` (Amber `#f59e0b` | `stroke-dashoffset="-94.8"`)
- **Interactive Dual-Link Hover:** Hovering any slice or legend item highlights that slice (`stroke-width="5.5"`), dims remaining slices, and dynamically updates the center display from `৳ 4.82 Cr / Total Revenue` to that slice's amount and percentage.
- **Bottom Footnote:** `Realized Collection: 94.2% (৳ 4.54 Cr)`.

### 5.5 Card 5: Expense Accounts Overview & Budget Allocation (Compact Micro-Grid)
- **Grid Footprint:** `col-span-12`.
- **Layout:** Sleek 3-column x 2-row micro-card grid (`glass-micro-card` with `p-2.5`):
  - `#5100 Direct Materials & COGS:` Spent `৳ 1.84 Cr` of `৳ 2.20 Cr` (83.6%) — `Optimal`
  - `#5200 Enterprise Payroll & Benefits:` Spent `৳ 68.5 L` of `৳ 72.0 L` (95.1%) — `On Track`
  - `#5300 Utilities, Power & Site Fuels:` Spent `৳ 22.4 L` of `৳ 25.0 L` (89.6%) — `Attention`
  - `#5400 Freight, Logistics & Customs:` Spent `৳ 34.2 L` of `৳ 38.0 L` (90.0%) — `On Track`
  - `#5500 Administrative & Facilities:` Spent `৳ 18.2 L` of `৳ 22.0 L` (82.7%) — `Under Budget`
  - `#5600 Cloud Infra, IT & Software:` Spent `৳ 13.7 L` of `৳ 15.0 L` (91.3%) — `On Track`
- **Top Summary Badge:** Total Spend: `৳ 3.41 Cr` (88.5% of Budget).

### 5.6 Card 6: General Ledger & Double-Entry Vouchers Hub
- **Grid Footprint:** `col-span-12`.
- **Type Filtering:** `All (284)`, `Payment (PV)`, `Receipt (RV)`, `Journal (JV)`, `Contra (CV)`.
- **Balanced Trial Balance Bar:**
  - Total Debits: `৳ 1,22,42,000`
  - Total Credits: `৳ 1,22,42,000`
  - Difference: `৳ 0.00 (Balanced)`
- **Audited Voucher Records:**
  - Shows 6 key recent vouchers with date, voucher number, type pill, accounts, narration, debits, credits, status badge, and `View` / `Approve` actions.
- **Pagination:** Clean controls with page count `Showing 1-6 of 284 Vouchers`.

---

## 6. Modals Specification

- **Preserved Modal:**
  - **Voucher Preview / Print Modal (`#preview-modal`):** Used to inspect posted transaction details, beneficiary info, amount, and trigger `window.print()` for audited PDF voucher printouts.
- **Removed Modals & Actions:**
  - `+ New Journal Entry` and `Payment Voucher` modal forms have been removed from this page.
  - Future data-entry vouchers will be handled via dedicated voucher creation workflows or drawer components.

---

## 7. Data Synchronization Table with Cover Page

All financial figures in `finance_module.html` correlate 100% with the master executive dashboard `erp_cover_page.html`:

| Metric Name | `erp_cover_page.html` | `finance_module.html` | Status |
| :--- | :--- | :--- | :--- |
| **Total Revenue / Income** | `৳ 4.82 Cr` | `৳ 4.82 Cr` | Exact Match |
| **Cost of Goods Sold (COGS)**| Derived (৳ 3.46 Cr) | `৳ 3.46 Cr` (71.8%) | Exact Match |
| **Gross Profit** | `৳ 1.36 Cr (28.2%)` | `৳ 1.36 Cr (28.2%)` | Exact Match |
| **Operating Expenses (Total)**| `৳ 3.41 Cr` | `৳ 3.41 Cr` (Card 5) | Exact Match |
| **Net Profit / Net Margin** | `৳ 1.28 Cr (26.6%)` | `৳ 1.28 Cr (26.6%)` | Exact Match |
| **Net Liquid Balance** | `৳ 3.84 Cr` | `৳ 3.84 Cr` (Card 2) | Exact Match |
| **Cash Surplus** | `+৳ 18.3 লাখ` (Daily) | `+৳ 1.28 Cr` (Monthly) | Aligned |
