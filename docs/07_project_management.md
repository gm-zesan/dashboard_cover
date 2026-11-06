# Module 07: Project Management — UI & Content Blueprint

> **File Name:** `projects_module.html`  
> **Accent Theme:** Teal (`#0d9488`), Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Sunset Orange (`#ea580c`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Grid Architecture:** Unified 1/3 vs 2/3 Grid Split — **Left Columns: 4 cols (`lg:col-span-4`)** | **Right Columns: 8 cols (`lg:col-span-8`)**  
> **Contextual Watermark Art:** Project Gantt Timeline / Milestone Compass / Architecture Blueprint Nodes  
> **Status:** Locked & Approved (Consistent with `finance_module.html` 4-Col/8-Col Architecture)

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora light pools.
2. **Unified 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - All 3 body rows feature a continuous, aligned vertical division line:
     - **Left Column (`lg:col-span-4` / 33.3% width):** Project burnup dual-bar chart, resource billable stream, SBU budget donut, and SLA milestone risk monitor.
     - **Right Column (`lg:col-span-8` / 66.7% width):** Expansive project milestone Gantt/phase flow stage, 6-SBU delivery grid, and 9-column Projects Master Hub.
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors identical to `erp_cover_page.html`: Royal Blue (`#2563eb`), Royal Purple (`#7c3aed`), Emerald Green (`#059669`), and Sunset Orange (`#ea580c`).
4. **Row 3 Perfect Height Balance:**
   - In the left 4-column space, **Budget by SBU** (Card 5A) and **Project Health & SLA Risk Watch** (Card 5B) stack vertically (`flex flex-col gap-3.5`), matching the exact height of the Projects Master Table (Card 6) on the right.
5. **No Cluttered In-Page Tabs:**
   - Submodule navigation (Task Kanban, Timesheets, Sprint Backlog) is deferred to the future Global Application Sidebar.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/65 backdrop-blur-md border-b border-white/50 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"` with hover pill effect).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Teal rounded icon badge + `Project Management` (h1, bold, tracking-tight).
  - Breadcrumbs: `Inceptia ERP / Enterprise Delivery / Client Projects, Milestones & SBU Performance`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon and `⌘K` keyboard badge (`oninput="filterProjectTable()"`).
  - **Date Range Selector Dropdown:** Rounded pill showing `Nov 1 – Nov 30, 2026` with popup options (`Today`, `This Week`, `This Month`, `Q2 FY2026`).
  - **Export Button:** Clean outline button with download icon and `Export` label (`exportProjectReport()`).

---

## 3. Top 4 Project KPI Pillar Cards (Colorful Matte Glass)

Styled identically to the master executive group dashboard `erp_cover_page.html`:

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Active Enterprise Projects**| `24 Projects`| 6 Major projects going live in Q2 | `▲ +4 Active` | Solid Matte Royal Blue (`#2563eb/90`) |
| **Budget Burn Velocity** | `78.4%` | Total Commitment: ৳ 3.84 Cr | `On Budget` | Solid Matte Royal Purple (`#7c3aed/90`) |
| **On-Time Milestone SLA** | `91.2%` | 28 of 31 milestones completed on schedule | `High Delivery`| Solid Matte Emerald Green (`#059669/90`) |
| **Billable Hours Logged** | `14,200 hrs` | 94.6% Resource utilization efficiency | `Productive` | Solid Matte Sunset Orange (`#ea580c/90`) |

---

## 4. 3-Row 4-Col (Left) / 8-Col (Right) Cards Layout

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: BUDGET VELOCITY & ENTERPRISE MILESTONE GANTT STAGE                                    │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 1: Project Budget Velocity (4 cols)      │ CARD 2: Enterprise Milestone Gantt Stage (8) │
│ • 6-Month Budgeted vs Burned Dual-Bar Chart   │ • [GRAPH] Multi-Phase Project Lifecycle Stage│
│ • Burn Velocity Spline Overlay (72%-78%)      │ • Architecture (42 L) → Engineering (1.15 Cr)│
│ • Compact Telemetry Widget (500x180)          │   → QA Integration (58 L) → Client UAT (34 L)│
│ • Range Toggles (6M / YTD / FY26)             │   → Go-Live Deployment (85 L)                │
│                                               │ • Expansive Stage Width (740x175)            │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 2: RESOURCE REALIZATION & STRATEGIC BUSINESS UNITS (SBU)                                 │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ CARD 3: Resource Allocation Stream (4 cols)   │ CARD 4: SBU Delivery Performance Grid (8)    │
│ • Billable Realization: 91.2% (14,200 hrs)    │ • 6 SBU Micro-Cards (3 cols x 2 rows):       │
│ • Blended Billing Rate: ৳ 1,450 / hr          │ • FinTech Core, Telecom OSS/BSS, Supply Chain│
│ • Engineer Utilization: 94.6%                 │   Automation, HealthTech, Cloud, Industrial  │
│ • Tight, Snug Column Fit                      │ • Budget vs Burn Progress Bars & Badges      │
├───────────────────────────────────────────────┴──────────────────────────────────────────────┤
│ ROW 3: SBU BUDGET DISTRIBUTION, SLA HEALTH & AUDITED PROJECTS HUB                            │
├───────────────────────────────────────────────┬──────────────────────────────────────────────┤
│ LEFT STACK (4 cols): 2 Paired Cards           │ RIGHT COLUMN (8 cols): PROJECTS MASTER HUB   │
│                                               │                                              │
│ • CARD 5A: Budget Allocation by SBU           │ CARD 6: Client Projects & Deliverables Hub   │
│   Segmented SVG Donut Graph & Legend          │ • Expansive 9-Column Data Table with 6 Rows  │
│   FinTech 36.4%, Telecom 24.8%,               │ • Filter Tabs: All (24), Active, Live, Due   │
│   Automation 21.2%, Cloud & IoT 17.6%         │ • Live Search, PM Filter & Pagination        │
│                                               │ • Live Milestone Summary Bar:                │
│ • CARD 5B: Project Health & SLA Risk Watch    │   Committed Value = Realized + Work-in-Prog  │
│   20 On Track, 3 Critical Path, 1 Creep,      │ • Action Controls: View Milestone Gantt Modal│
│   Client Sign-off SLA: 98.2%                  │   Audit Timesheet, Log Milestone Deliverable │
└───────────────────────────────────────────────┴──────────────────────────────────────────────┘
```

---

## 5. Row-by-Row Detailed Card Specifications

### 5.1 Row 1: Budget Velocity & Enterprise Milestone Gantt Stage (4 cols + 8 cols)

#### Card 1: Project Budget Velocity Dual-Bar Graph
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Header: Teal icon + "Project Burnup & Budget Velocity" + Range pill (`6M`, `YTD`).
  - Graph Area: Custom responsive SVG Dual-Bar Chart (`viewBox="0 0 500 180"`):
    - Allocated Budget Bar (Light Teal `#99f6e4`).
    - Actual Spend / Burned Bar (Vibrant Teal `#0d9488`).
    - Delivery Velocity Spline in Purple (`#7c3aed`).
  - Footer Telemetry:
    - Allocated: `৳ 3.84 Cr` | Incurred: `৳ 3.01 Cr` | Efficiency: `78.4%`
- **Contextual Watermark:** Blueprint Compass & Milestone Ruler Art.

#### Card 2: Enterprise Milestone Gantt & Lifecycle Stage
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Gantt icon + "Enterprise Milestone Gantt & Lifecycle Stage" + Status Pill (`On-Time: 91.2%`).
  - Graph Area: Expansive SVG Pipeline Waterfall / Stage Flow (`viewBox="0 0 740 175"`):
    1. **Architecture & Design Blueprint:** `৳ 42.0 L` (100% Completed) — `teal-500`.
    2. **Core Platform Engineering:** `৳ 1.15 Cr` (92.4% Executed) — `blue-500`.
    3. **System Integration & QA:** `৳ 58.0 L` (78.0% Executed) — `purple-500`.
    4. **Client User Acceptance (UAT):** `৳ 34.0 L` (54.0% In Progress) — `amber-500`.
    5. **Final Cutover & Go-Live:** `৳ 85.0 L` (Scheduled Dec 2026) — `emerald-600`.
  - Micro-Summary: Total Sprints `42 Completed` • Story Points `1,280 Pts` • Blockers `0`.
- **Contextual Watermark:** Enterprise Milestone Flow Network.

---

### 5.2 Row 2: Resource Realization & SBU Performance (4 cols + 8 cols)

#### Card 3: Resource Allocation & Billable Realization Stream
- **Column Span:** `lg:col-span-4` (Left 1/3)
- **Component Anatomy:**
  - Metric Header: `14,200 hrs` logged with **91.2%** billable realization rate.
  - Resource Efficiency Breakdown:
    - Senior Architects & Leads: `98.2% Billable` (৳ 2,200/hr)
    - Full-Stack Engineers: `94.0% Billable` (৳ 1,450/hr)
    - QA & DevOps Engineers: `88.5% Billable` (৳ 1,100/hr)
    - Non-Billable Internal R&D: `8.8%` (Strategic IP creation)
  - Blended Realization Rate: `৳ 1,450/hr` across enterprise accounts.
- **Contextual Watermark:** Stopwatch Precision Timer Art.

#### Card 4: Strategic Business Units (SBU) Delivery Grid
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - 3-Column x 2-Row Micro-Card Grid of the 6 core business units:
    1. **FinTech Core Systems (6 Projects):** Budget ৳ 1.40 Cr | Burn: ৳ 1.12 Cr (80.0%) • Badge: `Optimal`
    2. **Telecom OSS/BSS Unit (5 Projects):** Budget ৳ 95.0 L | Burn: ৳ 78.4 L (82.5%) • Badge: `On Track`
    3. **Supply Chain Automation (4 Projects):** Budget ৳ 82.0 L | Burn: ৳ 61.2 L (74.6%) • Badge: `Favorable`
    4. **HealthTech Digital Systems (3 Projects):** Budget ৳ 45.0 L | Burn: ৳ 32.8 L (72.8%) • Badge: `Controlled`
    5. **Cloud Infrastructure Migration (4 Projects):** Budget ৳ 38.0 L | Burn: ৳ 29.5 L (77.6%) • Badge: `On Track`
    6. **Industrial IoT & Smart Sensors (2 Projects):** Budget ৳ 24.0 L | Burn: ৳ 16.2 L (67.5%) • Badge: `Early Phase`
- **Contextual Watermark:** SBU Delivery Matrix.

---

### 5.3 Row 3: SBU Budget Distribution, SLA Health & Audited Projects Hub (4 cols + 8 cols)

#### Card 5A: Budget Allocation by SBU (Left Stack - Top)
- **Column Span:** Part of `lg:col-span-4` (Stacked above Card 5B)
- **Component Anatomy:**
  - SVG Segmented Donut Chart (`viewBox="0 0 160 160"`):
    - FinTech Core Systems: `36.4%` (Teal `#0d9488`)
    - Telecom OSS/BSS: `24.8%` (Blue `#2563eb`)
    - Supply Chain Automation: `21.2%` (Purple `#7c3aed`)
    - Cloud Infrastructure & IoT: `17.6%` (Sunset Orange `#ea580c`)
  - Center Donut Label: `৳ 3.84 Cr Total`
  - 2-Column Legend with BDT values and percentage badges.

#### Card 5B: Project Health & SLA Milestone Risk Watch (Left Stack - Bottom)
- **Column Span:** Part of `lg:col-span-4` (Stacked below Card 5A to match Card 6 height)
- **Component Anatomy:**
  - 4 Milestone Health Telemetry Tiers:
    - **On Schedule & Healthy:** `20 Projects` — `emerald-500`
    - **Critical Path Monitoring:** `3 Projects` (Within 3 days of deadline) — `amber-500`
    - **Scope Creep / Change Req:** `1 Project` (Pending CR approval) — `blue-500`
    - **SLA Breach Risk:** `0 Projects` — `emerald-500`
  - Milestone Certification: `98.2% Client Sign-off acceptance score`.

#### Card 6: Client Projects & Deliverables Master Hub (Right Column)
- **Column Span:** `lg:col-span-8` (Right 2/3)
- **Component Anatomy:**
  - Header: Tab filters (`All Projects (24)`, `Active (18)`, `UAT (4)`, `Completed (2)`) + Search.
  - Expansive 9-Column Interactive Table:
    1. **Project Code:** `PRJ-FIN-802` (monospace bold)
    2. **Project Title:** Next-Gen Core Payment Switch
    3. **Client Organization:** BRAC Bank PLC
    4. **Lead PM:** Engr. Rafidul Islam, PMP
    5. **Contract Value (৳):** `85,00,000`
    6. **Current Milestone:** Phase 3: Integration QA
    7. **Burn %:** `74.5%` (Progress bar)
    8. **Health:** `Healthy` (Emerald) / `Critical Path` (Amber)
    9. **Action:** View Gantt Modal, Review Sprints, Audit Timesheet
  - Balanced Contract Reconciliation Footer:
    - Total Committed Contracts: `৳ 3,84,00,000` = Incurred `৳ 3,01,20,000` + Remaining Buffer `৳ 82,80,000`.
- **Contextual Watermark:** Audited Project Ledger Art.
