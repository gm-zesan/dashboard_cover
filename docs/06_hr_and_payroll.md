# Module 06: HR & Payroll — UI & Content Blueprint

> **File Name:** `hr_module.html`  
> **Accent Theme:** Rose (`#e11d48`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Unified 1/3 vs 2/3 Grid Split — **Left Columns: 4 cols (`lg:col-span-4`)** | **Right Columns: 8 cols (`lg:col-span-8`)**  
> **Contextual Watermark Art:** Employee ID Silhouette / Payroll Currency Seal / Team Organizational Chart  
> **Status:** Locked & Approved (Consistent with `finance_module.html` 4-Col/8-Col Architecture)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Unified 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - All 3 body rows feature a continuous, aligned vertical division line:
     - **Left Column (`lg:col-span-4` / 33.3% width):** Payroll expense dual-bar chart, statutory benefits liquidity stream, department headcount donut, and NBR tax compliance scorecard.
     - **Right Column (`lg:col-span-8` / 66.7% width):** Expansive departmental attendance stage, 6-department cost center grid, and 9-column Salary Register Hub.
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors identical to `erp_cover_page.html`: Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald Green (`#059669`), and Sunset Orange (`#ea580c`).
4. **Row 3 Perfect Height Balance:**
   - In the left 4-column space, **Headcount by Department** (Card 5A) and **Tax & Statutory Compliance** (Card 5B) stack vertically (`flex flex-col gap-3.5`), matching the exact height of the Salary Register Table (Card 6) on the right.
5. **No Cluttered In-Page Tabs:**
   - Submodule navigation (Leave management, Recruitment, Performance KPIs) is deferred to the future Global Application Sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Rose rounded icon badge + `HR & Payroll` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Human Resources & Talent / Payroll Register & Workforce Telemetry`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterPayrollTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportPayrollReport()`).

---

## 3. Top 4 HR & Payroll KPI Pillar Cards (Colorful Matte Glass)

Styled identically to the master executive group dashboard `erp_cover_page.html`:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Total Monthly Payroll** | `৳ 1.12 Cr` | Budget: ৳ 1.18 Cr (94.9% Disbursed) | `On Budget` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Total Enterprise Headcount**| `428 Staff` | 14 New hires joined this quarter | `▲ +3.4% QoQ` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **Daily Attendance Rate** | `96.4%` | 412 on duty today across all sites | `Optimal` | Solid Matte Emerald Green (`#059669/90`) |
| **Open Job Requisitions** | `14 Positions`| Avg time-to-hire: 21 Days | `Talent Pipeline`| Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row 4-Col (Left) / 8-Col (Right) Cards Layout

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: PAYROLL EXPENSE & WORKFORCE ATTENDANCE STAGE                                          │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 1: Payroll Expense Velocity (4 cols)     │ CARD 2: Departmental Workforce & Attendance  │
│ • 6-Month Gross vs Net Payroll Dual-Bar Chart │ • [GRAPH] Workforce Allocation & Flow Stage  │
│ • Headcount Velocity Spline (402 → 428 Staff) │ • Total Headcount (428 Staff / 96.4% Present)│
│ • Compact Telemetry Widget (500x180)          │   → Production (180) → R&D (106)             │
│ • Range Toggles (6M / YTD / FY26)             │   → Sales (78) → Finance & Admin (64)        │
│                                               │ • Expansive Stage Width (740x175)            │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 2: STATUTORY BENEFITS & DEPARTMENTAL COST CENTERS                                        │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: Statutory Benefits & PF Liquidity (4) │ CARD 4: Departmental Cost Center Grid (8)    │
│ • Net Disbursed: ৳ 1.02 Cr | PF: ৳ 14.8 L     │ • 6 Department Micro-Cards (3 cols x 2 rows):│
│ • Gratuity Reserve: ৳ 38.2 L | Health Ins.    │ • Factory Ops, Engineering R&D, Sales Team,  │
│ • BEFTN Salary Disbursement: 100% Cleared     │   SCM Logistics, Finance & Tax, HR & Admin   │
│ • Tight, Snug Column Fit                      │ • Headcount vs Budget Progress Bars & Badges │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: WORKFORCE DISTRIBUTION, TAX COMPLIANCE & AUDITED SALARY REGISTER                      │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ LEFT STACK (4 cols): 2 Paired Cards           │ RIGHT COLUMN (8 cols): SALARY REGISTER HUB   │
│                                               │                                              │
│ • CARD 5A: Headcount by Department            │ CARD 6: Employee Payroll Disbursement Hub    │
│   Segmented SVG Donut Graph & Legend          │ • Expansive 9-Column Data Table with 6 Rows  │
│   Operations 42.1%, Engineering 24.8%,        │ • Filter Tabs: All (428), Disbursed, Hold    │
│   Sales 18.2%, Finance & Admin 14.9%          │ • Live Search, Department Filter & Paging    │
│                                               │ • Live Payroll Summary Bar:                  │
│ • CARD 5B: Tax & Labor Law Compliance Watch   │   Gross Pay = Net Disbursed + TDS + PF Trust │
│   TDS Deducted: 100%, PF Trust Audited: Clean,│ • Action Controls: View Payslip PDF Modal,   │
│   Overtime Audited: Within Legal Limit        │   Bank Advice Sheet, Issue Salary Certificate│
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Detailed Card Specifications

### 5.1 Row 1: Payroll Velocity & Workforce Attendance Stage (4 cols + 8 cols)

#### Card 1: Payroll Expense Velocity Dual-Bar Graph
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Header: Rose icon + "Payroll Expense Velocity" + Range pill (`6M`, `YTD`).
  - Graph Area: Custom responsive SVG Dual-Bar Chart (`viewBox="0 0 500 180"`):
    - Gross Salary Commitment Bar (Light Rose `#fecdd3`).
    - Net Disbursed Salary Bar (Vibrant Rose `#e11d48`).
    - Staff Headcount Growth Spline in Royal Blue (`#2563eb`).
  - Footer Telemetry:
    - Gross Commitment: `৳ 1.12 Cr` | Net Disbursed: `৳ 1.02 Cr` | Tax Withheld: `৳ 10.0 L`
- **Contextual Watermark:** Payroll Vault & Coin Stacks Art.

#### Card 2: Departmental Workforce & Attendance Flow Stage
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Team icon + "Workforce Deployment & Live Attendance Stage" + Status Pill (`Present: 96.4%`).
  - Graph Area: Expansive SVG Pipeline Waterfall / Stage Flow (`viewBox="0 0 740 175"`):
    1. **Total Enterprise Headcount:** `428 Personnel` — `slate-400`.
    2. **Plant Operations & Production:** `180 Personnel` (97.2% Attendance) — `rose-500`.
    3. **Engineering & Software R&D:** `106 Personnel` (98.1% Attendance) — `blue-500`.
    4. **Commercial Sales & Business Dev:** `78 Personnel` (94.8% Attendance) — `emerald-500`.
    5. **Executive Finance & Administration:** `64 Personnel` (96.8% Attendance) — `purple-500`.
  - Micro-Summary: On Approved Leave `12 Staff` • Business Travel `4 Staff` • Unexcused `0`.
- **Contextual Watermark:** Corporate Organizational Hierarchy Art.

---

### 5.2 Row 2: Statutory Benefits & Departmental Cost Centers (4 cols + 8 cols)

#### Card 3: Statutory Benefits & Provident Fund Liquidity
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Metric Header: `৳ 1.12 Cr` Payroll with **100%** on-time bank disbursement.
  - Statutory Fund Breakdown:
    - Recognized Provident Fund (RPF): `৳ 14.8 L` (Transferred to Trustee account)
    - Gratuity Fund Reserve: `৳ 38.2 L` (Actuarially funded)
    - Employee Health & Life Insurance: `৳ 6.4 L` (428 lives covered)
  - Bank Advice Clearing: Disbursed via Corporate City Bank BEFTN.
- **Contextual Watermark:** Certified Employee Benefit Seal.

#### Card 4: Departmental Cost Center & Overtime Allocation
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - 3-Column x 2-Row Micro-Card Grid of the 6 core departmental cost centers:
    1. **Plant Operations (180 Staff):** Budget ৳ 42.0 L | Actual: ৳ 41.2 L (98.1%) • Badge: `Optimal`
    2. **Software & Systems R&D (106 Staff):** Budget ৳ 38.0 L | Actual: ৳ 36.4 L (95.8%) • Badge: `Favorable`
    3. **Commercial & Sales (78 Staff):** Budget ৳ 22.0 L | Actual: ৳ 20.8 L (94.5%) • Badge: `On Track`
    4. **Supply Chain & Logistics (32 Staff):** Budget ৳ 8.5 L | Actual: ৳ 8.1 L (95.3%) • Badge: `Controlled`
    5. **Finance & Accounts (18 Staff):** Budget ৳ 5.5 L | Actual: ৳ 5.2 L (94.5%) • Badge: `Standard`
    6. **HR & General Admin (14 Staff):** Budget ৳ 4.0 L | Actual: ৳ 3.8 L (95.0%) • Badge: `Optimal`
- **Contextual Watermark:** Departmental Budget Allocation Matrix.

---

### 5.3 Row 3: Workforce Distribution, Tax Compliance & Audited Salary Hub (4 cols + 8 cols)

#### Card 5A: Headcount Distribution by Department (Left Stack - Top)
- **Column Span:** Part of `lg:col-span-4` (Stacked above Card 5B)
- **Component Anatomy:**
  - SVG Segmented Donut Chart (`viewBox="0 0 160 160"`):
    - Plant Operations: `42.1%` (Rose `#e11d48`)
    - Software & Engineering R&D: `24.8%` (Blue `#2563eb`)
    - Commercial Sales: `18.2%` (Purple `#7c3aed`)
    - Executive Finance & Admin: `14.9%` (Emerald `#059669`)
  - Center Donut Label: `428 Personnel`
  - 2-Column Legend with staff counts and percentage badges.

#### Card 5B: Labor Law & NBR Tax Compliance Watch (Left Stack - Bottom)
- **Column Span:** Part of `lg:col-span-4` (Stacked below Card 5A to match Card 6 height)
- **Component Anatomy:**
  - 4 Compliance Audit Tiers:
    - **TDS Salary Withholding:** `100% Compliant` (Deposited via NBR Challan) — `emerald-500`
    - **Provident Fund Audit:** `Certified Clean` (FY2026 External Audit) — `emerald-500`
    - **Overtime Limits:** `Compliant` (All shifts within 60hr/week ceiling) — `blue-500`
    - **Minimum Wage Verification:** `100% Passed` — `emerald-500`
  - Regulatory Pill: `NBR Form 108 Tax Filing Complete`.

#### Card 6: Employee Payroll Disbursement Hub (Right Column)
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Tab filters (`All Staff (428)`, `Disbursed (426)`, `Pending Onboarding (2)`) + Search.
  - Expansive 9-Column Interactive Table:
    1. **Emp ID:** `EMP-8492` (monospace bold)
    2. **Employee Name:** S. M. Farhan Chowdhury
    3. **Department:** Software & Systems R&D
    4. **Designation:** Lead Architect
    5. **Basic Salary (৳):** `1,60,000`
    6. **Allowances (৳):** `65,000`
    7. **TDS & PF Deductions (৳):** `32,000`
    8. **Net Payable BDT (৳):** `1,93,000`
    9. **Action:** View Payslip PDF, Bank Advice, Tax Sheet
  - Balanced Payroll Summary Footer:
    - Total Gross Payroll: `৳ 1,12,00,000` = Net Disbursed `৳ 1,02,00,000` + Tax/PF Trust `৳ 10,00,000`.
- **Contextual Watermark:** Audited Salary Register Art.
