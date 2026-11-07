# Module 10: Performance Management (PMS) & Talent Appraisals — UI & Content Blueprint

> **File Name:** `performance_module.html`  
> **Accent Theme:** Electric Violet (`#7c3aed`), Royal Indigo (`#4f46e5`), Emerald (`#059669`), Sunset Amber (`#d97706`), Rose (`#e11d48`)  
> **Parent Navigation:** `erp_cover_page.html` (Executive Portal)  
> **Container Width:** Full Desktop Width (`max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8` matching `erp_cover_page.html`)  
> **Visual Architecture:** 9-Box Talent Matrix (7 cols) + Bell-Curve Calibration Console & 360° Feedback (5 cols) | OKRs & Strategic Alignment (5 cols) + Universal KPIs & Competency Library (7 cols) | Audited Appraisals Roster (8 cols) + Cryptographic Appraisal Dossier Docket (4 cols)  
> **Status:** Live & Approved

---

## 1. Architectural Philosophy & Full-Width Rules

1. **Full-Width Canvas Consistency:**
   - Matches the exact master viewport width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
   - Translucent frosted glass cards against `assets/erp_bg.jpg` with ambient aurora violet/indigo light pools.
2. **Domain-Specific Unique Visual Instruments:**
   - **Row 1 (7 cols + 5 cols):**
     - **9-Box Talent Matrix (7 cols):** 3x3 Performance vs. Potential interactive matrix mapping 1,280 employees across 9 quadrants (Stars, High Pros, Core Performers, Risk PIPs) with interactive quadrant filtering.
     - **Bell-Curve Calibration Console & 360° Feedback (5 cols):** Real-time bell curve quota deviation tracker (O, A, B, C, D distribution: 10% - 25% - 50% - 12% - 3%) with committee session controls and multi-rater radar pulse.
   - **Row 2 (5 cols + 7 cols):**
     - **OKRs & Key Results Progress Hub (5 cols):** Enterprise strategic objectives with weighted milestones, progress rings, and key result status bars.
     - **Universal KPIs & Competency Framework Library (7 cols):** Role-based scoring weightage (KPIs 70%, Behavioral Competencies 30%) with active evaluation sliders.
   - **Row 3 (8 cols + 4 cols):**
     - **Master Appraisals Roster & Review Cycles Table (8 cols):** Real-time employee appraisal database with multi-criteria filtering by Department, Grade Band, 9-Box Cell, and Review State.
     - **Reactive Executive Appraisal Dossier Docket (4 cols):** Instant inspection drawer displaying cryptographic tamper seal (`SHA256:793CC78B3D186B30-PMS-SEALED`), KPI score breakdown, 360° radar summary, committee sign-offs, and PIP action toggles.
3. **Colorful Executive KPI Cards (Cover Page DNA):**
   - Top 4 KPI cards feature high-saturation matte colors: Solid Electric Violet (`#7c3aed`), Solid Emerald (`#059669`), Solid Amber (`#d97706`), and Solid Rose (`#e11d48`), each equipped with an integrated mini SVG circular progress ring.
4. **Clean Borders & Zero Overlaps:**
   - Uniform frosted borders (`border border-slate-200/80`) with zero colored `border-l-4` strips.

---

## 2. Page Header & Navigation Bar

- **Sticky Frosted Container:** `bg-white/75 backdrop-blur-md border-b border-white/60 sticky top-0 z-30 shadow-2xs`.
- **Width:** `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8 py-3 relative z-10`.
- **Left Navigation & Branding:**
  - Back Button: `← Executive Portal` (`a href="erp_cover_page.html"`).
  - Vertical Separator: `h-5 w-px bg-slate-300/60`.
  - Icon & Title: Electric Violet rounded icon badge + `Performance Management (PMS)`.
  - Breadcrumbs: `Inceptia ERP / Annual Review Cycles, 9-Box Talent Matrix & Calibration Hub`.
- **Right Quick Controls:**
  - **Quick Search Input:** Rounded pill with search icon (`oninput="filterAppraisalsTable()"`).
  - **Cycle Selector Dropdown:** `FY2026 Annual Cycle (H1/H2 Calibration)`.
  - **Action Button:** `Start Review Cycle` or `Calibration Session`.

---

## 3. Top 4 PMS Executive KPI Pillar Cards (Colorful Matte Glass)

| KPI Metric | Value | Baseline / Comparison | Badge Indicator | Background Styling |
| :--- | :--- | :--- | :--- | :--- |
| **Total Appraisals Roster** | `1,280 Staff` | 94.2% Submitted (1,206 Done) | `H1/H2 Active` | Solid Matte Electric Violet (`#7c3aed/90`) |
| **Mean Performance Score** | `3.88 / 5.0` | +0.14 vs FY25 (Target: 3.75 - 3.90) | `Bell-Curve Fit` | Solid Matte Emerald Green (`#059669/90`) |
| **9-Box High Potentials (HiPo)** | `184 Leaders` | 14.4% Succession Pipeline Identified | `Key Talent` | Solid Matte Amber (`#d97706/90`) |
| **PIP Interventions & Watch** | `18 Staff` | 1.4% Underperformance Action | `Action Log` | Solid Matte Rose (`#e11d48/90`) |

---

## 4. 13 Core Functionalities & Technical Endpoints

| # | Functionality Name | System Route | Status | UI Manifestation & Behavioral Capabilities |
| :-: | :--- | :--- | :-: | :--- |
| **1** | **PMS Dashboard / Overview** | `/admin/performance_management` | `200 OK` | Top 4 KPI summary cards, cycle countdown, and submission progress bar. |
| **2** | **Performance Review Cycles** | `/admin/performance_management/cycles` | `200 OK` | Review cycle timeline (Self-Review → Manager Review → Calibration → Executive Sign-off). |
| **3** | **Appraisals Roster** | `/admin/performance_management/appraisals` | `200 OK` | 8-column data table with live reactive search, department filters, and rating badges. |
| **4** | **Universal KPIs & Competencies** | `/admin/performance_management/kpis` | `200 OK` | KPI library weightages (70% Hard KPIs, 30% Core Behavioral Competencies). |
| **5** | **OKRs & Key Results** | `/admin/performance_management/okrs` | `200 OK` | Strategic corporate and departmental OKR progress meters. |
| **6** | **360° Multi-Rater Feedback** | `/admin/performance_management/reviews_360` | `200 OK` | Anonymous peer & upward review distribution radar with completion counters. |
| **7** | **Calibration Sessions** | `/admin/performance_management/calibrations` | `200 OK` | Executive committee calibration schedule, members roster, and session locking. |
| **8** | **Calibration Console** | `/admin/performance_management/calibrations/session/1` | `200 OK` | Real-time bell curve quota deviation meter (O, A, B, C, D) with drag adjustments. |
| **9** | **9-Box Talent Matrix** | `/admin/performance_management/talent_matrix` | `200 OK` | 3x3 interactive matrix mapping High/Med/Low Performance vs. High/Med/Low Potential. |
| **10** | **PIP Management** | `/admin/performance_management/pips` | `200 OK` | 30/60/90-day improvement milestones, weekly check-in logs, and appeal workflows. |
| **11** | **PMS Settings & Grade Bands** | `/admin/performance_management/settings` | `200 OK` | O (4.5-5.0), A (3.8-4.4), B (3.0-3.7), C (2.0-2.9), D (<2.0) score thresholds. |
| **12** | **Executive Appraisal Dossier** | `/admin/performance_management/dossier/2` | `200 OK` | Cryptographic tamper seal (`SHA256:793CC78B3D186B30-PMS-SEALED`) verified inspect docket. |
| **13** | **Evaluation Form View** | `/admin/performance_management/evaluate/1` | `200 OK` | Reactive slider-based evaluation score card with lock state and feedback annotations. |

---

## 5. Master-Detail 3-Row Grid Architecture

```
┌──────────────────────────────────────────────────────────────────────────────────────────────┐
│ ROW 1: 9-BOX TALENT MATRIX (7 cols) & BELL-CURVE CALIBRATION CONSOLE (5 cols)                │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 1: 9-Box Talent Grid (3x3 Matrix) (7 cols)               │ CARD 2: Bell-Curve & 360°    │
│ • Potential vs Performance Grid:                              │   Multi-Rater Console (5)    │
│   - Star Talent (86) | High Growth (98) | Enigmas (24)        │ • Quotas:                    │
│   - High Professionals (210) | Core Performers (485) | D (42) │   - O: 10% (Act: 9.8%)       │
│   - Specialists (194) | Effective (123) | PIP Risk (18)       │   - A: 25% (Act: 26.2%)      │
│ • Interactive Quadrant Filter: click updates roster below     │   - B: 50% (Act: 49.5%)      │
│                                                               │   - C: 12% (Act: 11.8%)      │
│                                                               │   - D: 3% (Act: 2.7%)        │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 2: OKRs & KEY RESULTS (5 cols) & UNIVERSAL KPIS & COMPETENCY FRAMEWORK (7 cols)          │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 3: Strategic OKR Horizon (5 cols)                        │ CARD 4: KPIs & Competency    │
│ • 4 Core Corporate Objectives:                                │   Framework Library (7 cols) │
│   1. Revenue Scale: ৳ 48.0 Cr ARR (88.4%)                     │ • Weighted Evaluation Model: │
│   2. Platform Reliability: 99.98% Uptime (94.1%)              │   - Quantitative KPIs (70%)  │
│   3. Enterprise Retention: 95% NRR (91.0%)                    │   - Behavioral Values (30%)  │
│   4. Talent Capability Index (86.2%)                          │ • Real-time Scoring Sliders  │
├───────────────────────────────────────────────────────────────┴──────────────────────────────┤
│ ROW 3: MASTER APPRAISALS ROSTER (8 cols) & CRYPTOGRAPHIC DOSSIER DOCKET (4 cols)             │
├───────────────────────────────────────────────────────────────┬──────────────────────────────┤
│ CARD 5: Master Appraisals Roster Table (8 cols)               │ CARD 6: Cryptographic Dossier│
│ • Filter by: Department, Rating Band, 9-Box Category, Status  │   Docket (4 cols)            │
│ • Columns: Employee, Dept, Self, Manager, Final Rating, 9-Box │ • 🔒 SHA256:793CC78B3D186B30 │
│ • Reactive selection: clicking any row updates the docket     │ • Score breakdown by Pillar  │
│                                                               │ • 360° Multi-Rater Radar     │
│                                                               │ • Committee Sign-off Actions │
└───────────────────────────────────────────────────────────────┴──────────────────────────────┘
```

