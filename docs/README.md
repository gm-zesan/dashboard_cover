# Inceptia ERP — Enterprise Architecture & Documentation Hub

> **System Version:** 4.8.2-Enterprise  
> **Master Cover Page:** [`erp_cover_page.html`](../erp_cover_page.html) (Locked & Live)  
> **Documentation Library:** Complete Design System & 8-Module Live Implementations

---

## 📚 Documentation & Module Implementation Index

| Module Code | Module Title | Live HTML File | Accent Theme | Domain-Specific Data Instruments & Architecture |
| :--- | :--- | :--- | :--- | :--- |
| **`00`** | [Master Design System](00_master_design_system.md) | Universal Standard | Multi | Colors, Typography, Frosted Glass Tokens, Watermarks, Component Library. |
| **`01`** | [Accounting & Finance](01_accounting_and_finance.md) | [`finance_module.html`](../finance_module.html) | 🔵 Royal Blue | Cash Flow Dual Spline + P&L Waterfall Bars + Accounts Matrix + General Ledger + Journal Docket. |
| **`02`** | [Sales & Invoicing](02_sales_and_invoicing.md) | [`sales_module.html`](../sales_module.html) | 🟢 Emerald | Revenue Trajectory Area + Stepped Polygon Funnel + Quota Speedometer Arc + Invoices Table + Mushak-6.3 Docket. |
| **`03`** | [Purchase & Suppliers](03_purchase_and_suppliers.md) | [`purchase_module.html`](../purchase_module.html) | 🟠 Amber | Spend Horizon with Budget Ceiling + 5-Stage Procurement Chevrons + Supplier SLA Scorecard + Cargo GPS Docket. |
| **`04`** | [Inventory & Warehouse](04_inventory_and_warehouse.md) | [`inventory_module.html`](../inventory_module.html) | 🟣 Purple | Multi-Hub Radial Capacity (4 Hubs) + ABC Velocity Spectrum + Reorder Watch + SKU Master + RFID Shelf Docket. |
| **`05`** | [CRM & Customers](05_crm_and_customers.md) | [`crm_module.html`](../crm_module.html) | 🔷 Indigo | 5-Stage Deal Horizon Flow + Customer 360 Health Radar + Acquisition Split + Deals Register + Client 360 Docket. |
| **`06`** | [HR & Payroll](06_hr_and_payroll.md) | [`hr_module.html`](../hr_module.html) | 🔴 Rose | Departmental Payroll Flow + Biometric Attendance Donut + NBR Tax/PF Status + Salary Register + Digital Payslip Docket. |
| **`07`** | [Project Management](07_project_management.md) | [`projects_module.html`](../projects_module.html) | 🟢 Teal | Milestone Gantt Timeline + Workload Squad Dial + Sprint Burndown + SBU Matrix + Projects Register + Risk Docket. |
| **`08`** | [Reports & Analytics](08_reports_and_analytics.md) | [`reports_module.html`](../reports_module.html) | 🟦 Cyan | Consolidated Revenue Horizon + Working Capital CCC Dial + Du-Pont ROE + Audit Filings Register + Regulatory Docket. |
| **`09`** | [Authentication & Login](09_login_authentication.md) | [`login.html`](../login.html) | 🔷 Royal Blue / Indigo | Executive Frosted Glass Gateway, Corporate Email & Password Credentials, Session Security. |

---

## 🏛️ 2-Tier Portal Architecture

```
                               ┌────────────────────────────────────────────────┐
                               │  TIER 1: EXECUTIVE COVER PORTAL               │
                               │  erp_cover_page.html                           │
                               │  • High-Level Consolidated Group KPIs          │
                               │  • 12-Month Financial Trend & Business Share   │
                               │  • Group Cash & Bank Liquidity (৳ 3.84 Cr)     │
                               │  • Executive Approvals Hub (6 Pending Items)   │
                               │  • 8 Modular Workspaces Launch Gateway         │
                               └───────────────────────┬────────────────────────┘
                                                       │
         ┌─────────────┬─────────────┬─────────────────┼─────────────┬─────────────┬─────────────┐
         ▼             ▼             ▼                 ▼             ▼             ▼             ▼
   ┌───────────┐ ┌───────────┐ ┌───────────┐     ┌───────────┐ ┌───────────┐ ┌───────────┐ ┌───────────┐
   │ Module 01 │ │ Module 02 │ │ Module 03 │ ... │ Module 05 │ │ Module 06 │ │ Module 07 │ │ Module 08 │
   │ Finance & │ │  Sales &  │ │ Purchase  │     │   CRM &   │ │   HR &    │ │  Project  │ │ Reports & │
   │ Accounts  │ │ Invoices  │ │ Suppliers │     │ Customers │ │  Payroll  │ │Management │ │ Analytics │
   └───────────┘ └───────────┘ └───────────┘     └───────────┘ └───────────┘ └───────────┘ └───────────┘
```

---

## 🔗 Seamless Inter-Page Linking & Unified Architectural Rules
1. **Full-Width Standard (`max-w-[1680px]`):**
   - Every module page matches the exact container width of `erp_cover_page.html`: `max-w-[1680px] w-full mx-auto px-4 sm:px-6 lg:px-8`.
2. **Domain-Specific Unique Visual Instruments:**
   - Every module features handcrafted, domain-specific visualizers (e.g. Sales has Polygon Funnel & Quota Speedometer; Purchase has Budget Ceiling & Cargo GPS; Inventory has Multi-Hub Radial Rings & ABC Velocity; CRM has Customer 360 Health Radar; HR has Biometric Attendance Donut; Projects has Multi-Track Gantt; Reports has Cash Conversion Cycle & Du-Pont ROE).
3. **No Colored Left-Border Strips (`border-l-4`):**
   - All micro-cards across matrix layouts use clean, uniform frosted borders (`border border-slate-200/80`).
4. **Master-Detail Reactive Inspection Dockets:**
   - Row 3 across all modules features an 8-column master table paired with a 4-column reactive inspector docket that updates instantly on row clicks without bulky popups or print buttons.
5. **From Module back to Executive Portal:**
   - Every module features a top navigation pill `← Executive Portal` linking directly to `erp_cover_page.html`.
