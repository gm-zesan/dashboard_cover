# Inceptia ERP — Enterprise Architecture & Documentation Hub

> **System Version:** 4.8.2-Enterprise  
> **Master Cover Page:** [`erp_cover_page.html`](../erp_cover_page.html) (Locked & Approved)  
> **Documentation Library:** Complete Design System & 8-Module Blueprints

---

## 📚 Documentation Index

| Doc Code | Title | Target File | Accent Theme | Description |
| :--- | :--- | :--- | :--- | :--- |
| **`00`** | [Master Design System](00_master_design_system.md) | Universal | Multi | Colors, Typography, Frosted Glass Tokens, Watermarks, Component Library. |
| **`01`** | [Accounting & Finance](01_accounting_and_finance.md) | `finance_module.html` | 🔵 Royal Blue | Chart of Accounts, General Ledger, Vouchers, AR/AP, Bank Rec, Trial Balance. |
| **`02`** | [Sales & Invoicing](02_sales_and_invoicing.md) | `sales_module.html` | 🟢 Emerald | Quotations, Tax Invoices, Challans, Credit Limits, AR Aging, Collections. |
| **`03`** | [Purchase & Suppliers](03_purchase_and_suppliers.md) | `purchase_module.html` | 🟠 Amber | Purchase Requisitions, RFQs, PO Approvals, GRN Inspection, Vendor Master. |
| **`04`** | [Inventory & Warehouse](04_inventory_and_warehouse.md) | `inventory_module.html` | 🟣 Purple | Item Master, Multi-Warehouse Transfers, Stock Audit, FIFO Valuation, Alerts. |
| **`05`** | [CRM & Customers](05_crm_and_customers.md) | `crm_module.html` | 🔷 Indigo | Sales Pipeline, Customer 360, Deal Stages, Follow-up Logs, Support Tickets. |
| **`06`** | [HR & Payroll](06_hr_and_payroll.md) | `hr_module.html` | 🔴 Rose | Staff Directory, Monthly Payroll Processing, Attendance Rosters, Leaves, TDS. |
| **`07`** | [Project Management](07_project_management.md) | `projects_module.html` | 🟢 Teal | Project Portfolios, Gantt Deliverables, Milestones, Budget Burn Rate. |
| **`08`** | [Reports & Analytics](08_reports_and_analytics.md) | `reports_module.html` | 🟦 Cyan | Financial Statements (P&L, Balance Sheet), BI Query Builder, Auto-Exports. |

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

## 🔗 Seamless Inter-Page Linking
1. **From Cover Page to Module:**
   - In `erp_cover_page.html`, clicking any module card or submodule row will link directly to the target module HTML file (e.g. `finance_module.html`).
2. **From Module back to Cover Page:**
   - Every module page features a top breadcrumb and a dedicated `← Back to Executive Portal` link pointing directly back to `erp_cover_page.html`.
3. **Unified 3-Row 4-Col (Left) / 8-Col (Right) Architectural Grid:**
   - Every module workspace uses `max-w-[1680px]` full-width container matching `erp_cover_page.html`.
   - **Row 1:** Left 4 cols (Compact Trend/Conversion Dual-Bar Chart) + Right 8 cols (Expansive Analytical Waterfall/Pipeline Stage).
   - **Row 2:** Left 4 cols (Velocity Stream & Telemetry) + Right 8 cols (6-Category Cost Center / Territory / Zone Grid).
   - **Row 3:** Left Stack of 2 cards (Segmented Donut Chart + Risk/Compliance Watch) + Right 8 cols (Audited 9-Column Master Data Hub).
   - In-page submodule tabs are removed in favor of the upcoming Global Application Sidebar.
4. **Design Synchronization:**
   - All 8 module pages share the **exact same Design DNA** (`docs/00_master_design_system.md`), ensuring that moving between pages feels like using a cohesive, billion-dollar enterprise platform.

