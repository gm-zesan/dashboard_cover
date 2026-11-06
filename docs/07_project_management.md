# Module 07: Project Management — UI & Content Blueprint

> **File Name:** `project_module.html`  
> **Accent Theme:** Teal (`#0d9488`, `text-teal-600`, `bg-teal-50/70`)  
> **Parent Navigation:** `erp_cover_page.html` (Cover Portal)  
> **Contextual Watermark Art:** Mountain Summit Milestone Flag / Gantt Roadmap Timeline

---

## 1. Page Header & Navigation Bar
- **Top Bar:** Glassmorphic container (`bg-white/65 backdrop-blur-md border-b border-white/50`).
- **Breadcrumbs:** `Inceptia ERP / Enterprise Projects / Milestones & Delivery`
- **Back Navigation:** `← Back to Executive Portal` (links to `erp_cover_page.html`).
- **Header Actions:**
  - `+ Create New Project` (Primary Teal Button)
  - `+ Add Milestone / Task` (Secondary Button)
  - Portfolio Health Filter (`Good (90%+)`, `At Risk`, `Delayed`)
  - Project Lead Selector

---

## 2. Top KPI Cards (4 Project Pillars)

1. **Active Projects Portfolio:**
   - Value: `18 Projects`
   - Subtext: `Total contract valuation: ৳ 42.5 Cr`
   - Badge: `92% Healthy`
   - Icon: Project Roadmap Flag
2. **ERP Implementation Progress:**
   - Value: `78% Completed`
   - Subtext: `Go-Live scheduled: Dec 15, 2026`
   - Badge: `On Track`
   - Icon: Target Bullseye Compass
3. **Milestones Due This Month:**
   - Value: `8 Milestones`
   - Subtext: `4 In Review, 3 In-Progress, 1 Completed`
   - Badge: `High Priority`
   - Icon: Calendar Checklist
4. **Budget Utilization vs Actual:**
   - Value: `64.2% Spent`
   - Subtext: `৳ 27.3 Cr utilized of ৳ 42.5 Cr budget`
   - Badge: `Under Budget (+5.8%)`
   - Icon: Budget Ledger

---

## 3. Submodule Navigation Tabs
1. **Projects Portfolio & Milestones** *(Default Active View)*
2. **Gantt Chart & Deliverables Timeline**
3. **Task Board (Sprint / Kanban)**
4. **Resource Allocation & Man-Hour Utilization**
5. **Budget, Actual Cost & Expense Burn Rate**
6. **Project Risk Register & Issue Log**

---

## 4. Main Content Area (Default: Projects Portfolio)

### 4.1 Interactive Projects Data Table
| Project Name | Client / Division | Project Lead | Budget (৳) | Progress | Current Milestone | Next Review | Status | Actions |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Inceptia ERP Enterprise Core | Internal / All Divisions | Kazi Abir Hasan | 2,50,00,000 | `78%` | UAT Sign-off & Migration | 10 Nov 2026 | `On Track` | View Gantt |
| Bashundhara House Infrastructure | Real Estate Division | Engr. S. Tanvir | 18,40,00,000 | `42%` | Structural Foundation Phase | 15 Nov 2026 | `In Progress` | View Gantt |
| China Sourcing Phase 1 (Genvict) | SCM & Hardware | Fahim Al-Mamun | 3,80,00,000 | `85%` | Equipment Customs Clearance | 12 Nov 2026 | `Near Finish` | View Details |
| Kalna Toll Plaza Automation | RHD Bangladesh | Kazi Faisal | 8,90,00,000 | `60%` | Lane Sensor Hardware Setup | 20 Nov 2026 | `On Track` | View Gantt |
| Cloud Migration & Disaster Recovery | IT Infrastructure | Nusrat Jahan | 1,20,00,000 | `95%` | Final DR Drill Testing | 08 Nov 2026 | `Completed` | Sign-off Report |

---

## 5. Modal Blueprint: `+ Create New Project`
- **Project Name & Code:** Name, Client/Division, Project Code (e.g., `PRJ-2026-042`).
- **Project Lead & Core Team:** Lead manager, Team members selection.
- **Financials:** Approved budget (BDT), Billing model (Milestone / Fixed / T&M).
- **Timeline:** Planned start date, Target go-live date, Key milestones.
- **Buttons:** `Initiate Project`, `Save Draft`, `Cancel`.
