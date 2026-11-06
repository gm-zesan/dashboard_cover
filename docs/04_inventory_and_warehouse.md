# Module 04: Inventory & Warehouse — UI & Content Blueprint

> **File Name:** `inventory_module.html`  
> **Accent Theme:** Purple (`#7c3aed`, `text-purple-600`, `bg-purple-50/70`)  
> **Parent Navigation:** `erp_cover_page.html` (Cover Portal)  
> **Contextual Watermark Art:** Warehouse Storage Rack / Forklift & Pallet Stacks

---

## 1. Page Header & Navigation Bar
- **Top Bar:** Glassmorphic container (`bg-white/65 backdrop-blur-md border-b border-white/50`).
- **Breadcrumbs:** `Inceptia ERP / Warehouse & Logistics / Stock Inventory & Transfers`
- **Back Navigation:** `← Back to Executive Portal` (links to `erp_cover_page.html`).
- **Header Actions:**
  - `+ Stock Transfer Order` (Primary Purple Button)
  - `+ Adjust Stock / Audit Count` (Secondary Button)
  - Warehouse Filter (`Central Tejgaon`, `Chittagong Depot`, `Savar Factory`, `All`)
  - Barcode Scanner / SKU Search

---

## 2. Top KPI Cards (4 Inventory Pillars)

1. **Total Stock Valuation:**
   - Value: `৳ 6.84 Cr`
   - Subtext: `Valued on FIFO Method across 3 Hubs`
   - Badge: `▲ +3.4% MoM`
   - Icon: Pallet Stack / Valuation
2. **Total SKUs / Active Items:**
   - Value: `1,840 Items`
   - Subtext: `98.4% In-Stock availability rate`
   - Badge: `Optimal Stock`
   - Icon: Barcode Scanner
3. **Low-Stock Critical Alerts:**
   - Value: `12 SKUs`
   - Subtext: `Items below safety reorder threshold`
   - Badge: `Reorder Required`
   - Icon: Exclamation Alert Beacon
4. **Monthly Stock Turnover:**
   - Value: `4.2x`
   - Subtext: `Average inventory holding period: 28 Days`
   - Badge: `High Velocity`
   - Icon: Rotating Cycle Arrows

---

## 3. Submodule Navigation Tabs
1. **Stock Levels & Item Master** *(Default Active View)*
2. **Inter-Warehouse Transfers (Stock Transfer Orders)**
3. **Goods Inward (GRN Inspection)**
4. **Material Dispatch & Delivery Challans**
5. **Stock Adjustments & Physical Audit Count**
6. **Low-Stock Alerts & Auto-Reorder Trigger**
7. **Batch, Serial Number & Expiry Tracking**

---

## 4. Main Content Area (Default: Stock Levels & Item Master)

### 4.1 Interactive Inventory Data Table
| SKU / Item Code | Product / Material Name | Category | Primary Warehouse | Available Qty | Safety Min | Unit Cost (৳) | Total Value (৳) | Status | Actions |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `SKU-CBL-402` | Fiber Optic Cable 48-Core (Armored) | Networking | Central Tejgaon Hub | 45,000 Mtr | 10,000 Mtr | 85 / Mtr | 38,25,000 | `In Stock` | Transfer, History |
| `SKU-RFID-109` | Genvict Electronic Toll Tags (ETC) | Hardware | Savar Factory Depot | 1,250 Pcs | 2,500 Pcs | 680 / Pc | 8,50,000 | `Low Stock` | Reorder, Transfer |
| `SKU-STL-008` | MS Deformed Rebar 60-Grade (16mm) | Construction | Chittagong Port Yard | 180 Tons | 50 Tons | 82,000 / Ton | 1,47,60,000 | `In Stock` | Transfer, History |
| `SKU-SRV-201` | Dell PowerEdge R750 Rack Server | IT Equipment | Central Tejgaon Hub | 8 Units | 2 Units | 6,40,000 / Unit | 51,20,000 | `In Stock` | View Serial Nos |
| `SKU-UPS-094` | Industrial Lead-Acid Battery 12V 200Ah | Electrical | Savar Factory Depot | 64 Units | 100 Units | 24,500 / Unit | 15,68,000 | `Critical Low` | Reorder Now |

---

## 5. Modal Blueprint: `+ Stock Transfer Order`
- **Origin Warehouse:** Dropdown (e.g., *Tejgaon Central*).
- **Destination Warehouse:** Dropdown (e.g., *Chittagong Depot*).
- **Driver & Vehicle Details:** Transport vehicle no., Driver contact, Dispatch date.
- **Transfer Items List:** SKU search, Current Available Qty, Transfer Qty, Unit.
- **Buttons:** `Generate Delivery Challan`, `Dispatch Transfer`, `Cancel`.

