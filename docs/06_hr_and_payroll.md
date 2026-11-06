# Module 06: HR & Payroll — UI & Content Blueprint

> **File Name:** `hr_module.html`  
> **Accent Theme:** Rose (`#e11d48`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Departmental Payroll Flow (7 cols) + Biometric Attendance Pulse (5 cols) | Statutory Compliance (5 cols) + Cost Centers 2x2 Matrix (7 cols) | Audited Salary Register (8 cols) + Reactive Digital Payslip Docket (4 cols)  
> **Contextual Watermark Art:** Employee ID Silhouette / Payroll Currency Seal / Team Organizational Chart  
> **Status:** Locked & Live (`hr_module.html` verified & synchronized)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Domain-Specific Visual Instruments (Zero Formulaic Cloning):**
   - **Row 1 (7 cols + 5 cols):** Departmental Payroll Weight & Headcount Flow (custom dual comparative horizontal bars in Rose & Lavender) + Biometric Attendance Pulse Donut (concentric multi-segment SVG donut with hollow centered metric and live terminal telemetry).
   - **Row 2 (5 cols + 7 cols):** Statutory NBR Tax, PF Trust & Gratuity Status (Challan TR-6 progress, PF match, actuarial reserve) + Cost Centers & Workforce Productivity 2x2 Matrix (Savar Plant, Software R&D, Commercial Sales, Shared Services).
   - **Row 3 (8 cols + 4 cols):** Executive Salary Register & Disbursal Table + Live Reactive Employee Digital Payslip Docket (updates instantaneously on row click with full earnings/deductions breakdown, NBR TIN, and BEFTN trace).
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors: Solid Royal Blue (`#2563eb`), Solid Royal Purple (`#7c3aed`), Solid Emerald Green (`#059669`), and Solid Sunset Orange (`#ea580c`), each equipped with an integrated mini SVG circular progress ring.
4. **Clean Borders & Zero Overlaps:**
   - No colored `border-l-4` strips on micro-cards; all cards use clean uniform frosted borders (`border border-slate-200/80`).
   - SVG charts use clean hollow text and zero needle or badge overlaps.
5. **No Cluttered In-Page Tabs:**
   - In-page submodule tabs removed; navigation handled seamlessly from the Executive Portal and future global sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/75 backdrop-blur-md border-b border-white/60 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Rose rounded icon badge + `HR & Payroll` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Workforce Telemetry, Salary Register & NBR Tax Compliance Hub`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterPayrollTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options.
  - **Export Button:** Clean outline button with download icon and `Export Salary Sheet` (`exportPayrollReport()`).

---

## 3. Top 4 HR & Payroll KPI Pillar Cards (Colorful Matte Glass)

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Total Monthly Payroll** | `৳ 1.12 Cr` | Budget: ৳ 1.18 Cr (94.9% Disbursed) | `On Budget` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Total Active Headcount**| `428 Staff` | Baseline: 414 Prior Qtr (+14 Net Hires) | `▲ +3.4% QoQ` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Daily Attendance Rate** | `96.4%` | Present: 412 Staff across 3 sites | `Optimal Rate` | Solid Matte Emerald Green (`#059669/90`) |
| **NBR Statutory Tax & PF** | `৳ 24.17 L` | 100% Withheld & Challan Deposited | `Audit Clean` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row Grid Architecture

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: DEPARTMENTAL PAYROLL FLOW (7 cols) & BIOMETRIC ATTENDANCE DONUT (5 cols)              │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 1: Departmental Headcount & Payroll Disbursal Flow (7)   │ CARD 2: Daily Biometric Shift│
│ • 5 Operating Divisions:                                      │   Pulse Donut (5 cols)       │
│   1. Engineering & Tech: 114 Staff | ৳ 38.50 L (34.4%)        │ • Multi-Segment SVG Donut:   │
│   2. Factory Ops & Depot: 162 Staff | ৳ 32.80 L (29.3%)       │   - Present & On Duty: 412   │
│   3. Commercial Sales: 64 Staff | ৳ 21.40 L (19.1%)           │   - Approved Leave: 10       │
│   4. Finance & Accounts: 48 Staff | ৳ 11.20 L (10.0%)         │   - Official Tour / Field: 4 │
│   5. HR & Governance: 40 Staff | ৳ 8.10 L (7.2%)              │   - Unexcused Absence: 2     │
│ • Dual comparative horizontal bars (Headcount vs Salary Cost) │ • Terminal telemetry: Tejgaon│
│                                                               │   Savar, Chittagong Port     │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 2: STATUTORY COMPLIANCE (5 cols) & COST CENTERS 2x2 MATRIX (7 cols)                       │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 3: Statutory NBR Tax, PF & Gratuity Status (5 cols)      │ CARD 4: Cost Centers & Labor │
│ • NBR Salary Withholding Tax (Section 50): ৳ 14.85 L (Challan)│   Productivity Matrix (7)    │
│ • Recognized PF Trust (8.33% match): ৳ 9.32 L (BRAC Trust)   │ • 2x2 Clean Frosted Grid:    │
│ • Audited Gratuity Fund Reserve: ৳ 18.40 L (Actuarial)        │   1. Savar Factory Plant     │
│ • BLA Compliance Score: 99.8% Clean                           │   2. Software R&D Lab        │
│                                                               │   3. Commercial Sales Unit   │
│                                                               │   4. Shared Executive G&A    │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 3: AUDITED SALARY REGISTER (8 cols) & LIVE DIGITAL PAYSLIP DOCKET (4 cols)               │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 5: Executive Salary Register Ledger Table (8 cols)       │ CARD 6: Live Employee Digital│
│ • 6 Audited Bangladesh Personnel (Tanvir, Farzana, Rafiqul...)│   Payslip Docket (4 cols)    │
│ • Department Filters: All (428), Tech, Operations, Commercial │ • Reactive on Row Selection  │
│ • Live Search on Staff Name, Code, Designation                │ • Full Earnings & Deductions │
│ • Basic, Allowances, PF/AIT Deductions, Net Disbursed         │ • TIN, Tax Circle, BEFTN Ref │
│ • Disbursal Status Pills (BEFTN Paid)                         │ • Annual Leave Telemetry     │
└───────────────────────────────────────────────────────────────┴──────────────────────────────┘
```

---

## 5. Row-by-Row Component Anatomy

### 5.1 Row 1: Payroll Flow & Biometric Pulse
- **Departmental Payroll & Headcount Flow (Card 1, 7 cols):** Custom SVG horizontal dual-bar chart mapping headcount volume and salary expenditure across 5 core corporate divisions.
- **Biometric Attendance Pulse Donut (Card 2, 5 cols):** Precision SVG concentric donut chart with centered rate label (`96.4% ON DUTY`), real-time breakdown of on-duty staff, approved leaves, field duties, and multi-site terminal synchronization rates.

### 5.2 Row 2: Statutory Compliance & Cost Centers
- **Statutory Tax & Gratuity Status (Card 3, 5 cols):** Real-time monitoring of Section 50 AIT tax deposit status (Challan TR-6), employer matching PF trust fund, and actuarial gratuity reserve under Bangladesh Labor Act.
- **Cost Centers & Workforce Productivity (Card 4, 7 cols):** 4 clean frosted micro-cards tracking operating expenditure, overtime hours, retention rates, and revenue output per employee without left-border colored lines.

### 5.3 Row 3: Salary Register & Live Digital Payslip
- **Executive Salary Register Table (Card 5, 8 cols):** Comprehensive payroll ledger displaying employee grades, basic pay, gross earnings, statutory tax/PF deductions, and net disbursed amounts.
- **Live Digital Payslip Docket (Card 6, 4 cols):** Interactive inspection panel displaying selected employee's itemized pay advice, bank account details, NBR Tax Circle & 12-digit TIN, BEFTN electronic advice trace number, and leave balances. Updates instantaneously upon clicking any row in the register.
