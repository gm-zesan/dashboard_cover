# Module 07: Project Management — UI & Content Blueprint

> **File Name:** `projects_module.html`  
> **Accent Theme:** Teal (`#0d9488`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Executive Milestone Gantt (8 cols) + Workload & Skill Dial (4 cols) | Sprint Burndown (5 cols) + SBU Delivery 2x2 Matrix (7 cols) | Projects Master Register (8 cols) + Reactive Milestone & Risk Docket (4 cols)  
> **Contextual Watermark Art:** Project Gantt Timeline / Milestone Compass / Architecture Blueprint Nodes  
> **Status:** Locked & Live (`projects_module.html` verified & synchronized)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Domain-Specific Visual Instruments (Zero Formulaic Cloning):**
   - **Row 1 (8 cols + 4 cols):** Executive Milestone Gantt Timeline & Stage Progress (multi-track SVG Gantt with today marker line, milestone diamonds, and phase bars) + Engineering Workload & Skill Squad Dial (radial arc gauge with 94.6% billable load & squad allocation rows).
   - **Row 2 (5 cols + 7 cols):** Sprint Velocity & Cumulative Issue Burndown (ideal burn line vs actual progress area) + SBU Delivery Units 2x2 Matrix (Enterprise ERP, Supply Chain IoT, Fintech Gateway, Cloud Infra).
   - **Row 3 (8 cols + 4 cols):** Enterprise Projects Master Register Table + Live Reactive Milestone & Risk Assessment Docket (real-time milestone checklist, financial budget burn, risk note, and delivery leadership).
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors: Solid Royal Blue (`#2563eb`), Solid Royal Purple (`#7c3aed`), Solid Emerald Green (`#059669`), and Solid Sunset Orange (`#ea580c`), each equipped with an integrated mini SVG circular progress ring.
4. **Clean Borders & Zero Overlaps:**
   - No colored `border-l-4` strips on micro-cards; all cards use clean uniform frosted borders (`border border-slate-200/80`).
   - Gantt markers, burndown lines, and gauges feature clean centered SVG typography without collisions.
5. **No Cluttered In-Page Tabs:**
   - In-page submodule tabs removed; navigation handled seamlessly from the Executive Portal and future global sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/75 backdrop-blur-md border-b border-white/60 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Teal rounded icon badge + `Project Management` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Enterprise Delivery / Client Projects, Milestones & SBU Performance`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterProjectTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options.
  - **Export Button:** Clean outline button with download icon and `Export Portfolio` (`exportProjectReport()`).

---

## 3. Top 4 Project KPI Pillar Cards (Colorful Matte Glass)

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Active Enterprise Projects**| `24 Projects`| 6 Major Projects Going Live in Q2 | `▲ +4 Active` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Portfolio Budget Burn** | `78.4%` | Disbursed: ৳ 3.84 Cr / ৳ 4.90 Cr | `On Budget` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **On-Time Milestone SLA** | `91.2%` | 28 of 31 Milestones Completed on Time | `High Delivery`| Solid Matte Emerald Green (`#059669/90`) |
| **Billable Utilization** | `94.6%` | 14,200 Billable Hours Logged | `Optimal Load` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row Grid Architecture

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: EXECUTIVE MILESTONE GANTT (8 cols) & WORKLOAD SQUAD DIAL (4 cols)                     │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 1: Executive Milestone Gantt Timeline (8 cols)           │ CARD 2: Workload & Skill Dial│
│ • 4 Core Strategic Tracks (Apex, Square, Beximco, PRAN)       │   (4 cols)                   │
│ • Q1-Q4 Horizon Grid (Oct, Nov, Dec, Jan)                     │ • Radial Arc Gauge: 94.6%    │
│ • Live "Today (Nov 6)" Vertical Red Indicator Line            │ • Squad Allocation Telemetry:│
│ • Milestone Diamonds, Phase Completion Bars & Critical Paths  │   Architects 98%, DevOps 96% │
│                                                               │   UI/UX 92%, QA 88%          │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 2: SPRINT BURNDOWN (5 cols) & SBU DELIVERY 2x2 MATRIX (7 cols)                           │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 3: Sprint Velocity & Burndown (5 cols)                   │ CARD 4: SBU Delivery Units   │
│ • Sprint 42 Burndown Area (154 / 160 Points Burned)           │   2x2 Matrix (7 cols)        │
│ • Ideal Linear Burndown vs Actual Trajectory                  │ • 2x2 Clean Frosted Grid:    │
│ • 6 Points Remaining to close sprint (Day 9 of 10)            │   1. Enterprise Solutions SBU│
│ • Defect Escape Rate: 0.8% Minimal                            │   2. Supply Chain & IoT SBU  │
│                                                               │   3. Fintech & Payments SBU  │
│                                                               │   4. Cloud Infrastructure SBU│
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 3: PROJECTS MASTER REGISTER (8 cols) & LIVE MILESTONE & RISK DOCKET (4 cols)             │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 5: Enterprise Projects Master Register (8 cols)          │ CARD 6: Live Project         │
│ • 6 Audited Projects (Apex ERP, Square Smart Hub, Beximco...) │   Milestone Docket (4 cols)  │
│ • SBU Filters: All (24), ERP (8), Supply Chain (6), Fintech(5)│ • Reactive on Row Selection  │
│ • Live Search on Project, Client, SBU Lead                    │ • 4-Stage Milestone Roadmap  │
│ • Budget & Burn Rate, Progress Bars, Target Dates, SLA Status │ • Fixed Price Budget Burn    │
│                                                               │ • Critical Path Risk Notes   │
└───────────────────────────────────────────────────────────────┴──────────────────────────────┘
```

---

## 5. Row-by-Row Component Anatomy

### 5.1 Row 1: Milestone Gantt & Workload Dial
- **Executive Milestone Gantt Timeline (Card 1, 8 cols):** Custom multi-track SVG timeline diagram tracking 4 flagship enterprise projects through October, November, December, and January with an illuminated current date line, milestone diamonds, and phase labels.
- **Engineering Workload & Skill Squad Dial (Card 2, 4 cols):** Semi-circular radial gauge indicating 94.6% billable squad utilization with granular allocation percentages across software architecture, DevOps, UI/UX, and QA automation.

### 5.2 Row 2: Sprint Burndown & SBU Matrix
- **Sprint Velocity & Burndown (Card 3, 5 cols):** Responsive SVG burndown tracking ideal sprint points against active burndown progress with zero defect escape.
- **SBU Delivery Units 2x2 Matrix (Card 4, 7 cols):** 4 clean frosted micro-cards displaying delivery performance, ARR weight, SLA compliance, and assigned personnel across all 4 SBUs without left-border colored lines.

### 5.3 Row 3: Projects Register & Live Milestone Docket
- **Enterprise Projects Master Register Table (Card 5, 8 cols):** Comprehensive project ledger with project logos, client tags, lead architects, budget numbers, and completion progress bars.
- **Live Project Milestone & Risk Docket (Card 6, 4 cols):** Interactive inspection panel displaying the selected project's milestone checklist, contract burn rate, delivery leadership, and critical path risk assessment notes. Seamlessly updates upon clicking any row in the register.
