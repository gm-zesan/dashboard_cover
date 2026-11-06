# Module 03: Purchase & Suppliers — UI & Content Blueprint

> **File Name:** `purchase_module.html`  
> **Accent Theme:** Amber / Golden Bronze (`#d97706`, `text-amber-600`, `bg-amber-50/70`)  
> **Parent Navigation:** `erp_cover_page.html` (Cover Portal)  
> **Contextual Watermark Art:** Procurement Delivery Truck / Purchase Order Clipboard

---

## 1. Page Header & Navigation Bar
- **Top Bar:** Glassmorphic container (`bg-white/65 backdrop-blur-md border-b border-white/50`).
- **Breadcrumbs:** `Inceptia ERP / Procurement & SCM / Purchase Orders & Vendors`
- **Back Navigation:** `← Back to Executive Portal` (links to `erp_cover_page.html`).
- **Header Actions:**
  - `+ Issue Purchase Order (PO)` (Primary Amber Button)
  - `+ New Purchase Requisition (PR)` (Secondary Button)
  - Vendor Filter
  - Status Filter (`Open POs`, `Pending Approval`, `Received`)

---

## 2. Top KPI Cards (4 Procurement Pillars)

1. **Total Spend This Month:**
   - Value: `৳ 2.14 Cr`
   - Subtext: `Across 34 Vendor POs (Budget: ৳ 2.50 Cr)`
   - Badge: `Controlled (85.6%)`
   - Icon: Currency Spend Scale
2. **Pending PO Approvals:**
   - Value: `৳ 32.5 লাখ`
   - Subtext: `4 High-value purchase orders awaiting MD sign-off`
   - Badge: `Action Required`
   - Icon: Certified Rosette Stamp
3. **Goods Inward (GRN Pending):**
   - Value: `6 Shipments`
   - Subtext: `Expected at Chittagong / Tejgaon Warehouse`
   - Badge: `In Transit`
   - Icon: Logistics Cargo Crate
4. **Active Supplier Count:**
   - Value: `142 Vendors`
   - Subtext: `98.2% On-time delivery rating`
   - Badge: `Top Tier: 18`
   - Icon: Verified Supplier Badge

---

## 3. Submodule Navigation Tabs
1. **Purchase Orders (PO)** *(Default Active View)*
2. **Purchase Requisitions (PR / Indent Approval)**
3. **Vendor & Supplier Master Database**
4. **Request for Quotation (RFQ) Comparison Matrix**
5. **Goods Received Notes (GRN) & Inspection**
6. **Supplier Bills & AP Invoices**
7. **Import L/C & Customs Clearance Tracking**

---

## 4. Main Content Area (Default: Purchase Orders)

### 4.1 Interactive Purchase Orders Data Table
| PO Date | PO Number | Supplier / Vendor | Items Description | Total Value (৳) | Delivery Due | Status | Actions |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 06 Nov 2026 | `PO-2026-0904` | Genvict Technologies Ltd | Toll RFID Sensors & Tag Antennas | 18,50,000 | 18 Nov 2026 | `Approved` | View PO, Track |
| 05 Nov 2026 | `PO-2026-0903` | LafargeHolcim Bangladesh | Special Clinker Cement (400 Tons) | 36,00,000 | 12 Nov 2026 | `Dispatched` | View GRN, PDF |
| 04 Nov 2026 | `PO-2026-0902` | Schneider Electric BD | HT Switchgear Panels & Breakers | 24,80,000 | 25 Nov 2026 | `Pending MD` | Approve, Edit |
| 03 Nov 2026 | `PO-2026-0901` | Rahimafrooz Batteries Ltd | Industrial UPS & Solar Battery Bank | 9,40,000 | 10 Nov 2026 | `Received (GRN)` | View Invoice |
| 01 Nov 2026 | `PO-2026-0900` | Cisco Systems / Flora Telecom | Enterprise Edge Core Switches | 14,20,000 | 15 Nov 2026 | `Received (GRN)` | Archive, PDF |

---

## 5. Modal Blueprint: `+ Issue Purchase Order`
- **Supplier Selection:** Dropdown with supplier rating & payment term info.
- **PO Header:** Delivery warehouse address, Expected delivery date, Shipping method.
- **Items Grid:** Item name, SKU, Order Qty, Unit Cost, Tax Rate, Line Total.
- **Approver Routing:** Automatic multi-tier routing (Procurement Manager → Head of SCM → CFO/MD if > ৳ 10L).
- **Buttons:** `Send for Approval`, `Save Draft`, `Cancel`.
