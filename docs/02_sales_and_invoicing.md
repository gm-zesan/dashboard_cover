# Module 02: Sales & Invoicing — UI & Content Blueprint

> **File Name:** `sales_module.html`  
> **Accent Theme:** Emerald Green (`#059669`, `text-emerald-600`, `bg-emerald-50/70`)  
> **Parent Navigation:** `erp_cover_page.html` (Cover Portal)  
> **Contextual Watermark Art:** Invoice Document with Currency Ribbon & Checkmark Seal

---

## 1. Page Header & Navigation Bar
- **Top Bar:** Glassmorphic container (`bg-white/65 backdrop-blur-md border-b border-white/50`).
- **Breadcrumbs:** `Inceptia ERP / Sales & Commercial / Invoices & Quotations`
- **Back Navigation:** `← Back to Executive Portal` (links to `erp_cover_page.html`).
- **Header Actions:**
  - `+ Create Sales Invoice` (Primary Emerald Button)
  - `+ New Quotation / Estimate` (Secondary Outline Button)
  - Customer Filter Dropdown
  - Export Options (`PDF`, `Excel Batch`, `Challan Print`)

---

## 2. Top KPI Cards (4 Sales Pillars)

1. **Monthly Invoiced Sales:**
   - Value: `৳ 4.82 Cr`
   - Subtext: `Target: ৳ 5.20 Cr (92.6% Achieved)`
   - Badge: `▲ +14.2% MoM`
   - Icon: Currency Growth Chart
2. **Paid Collections (Cash Inflow):**
   - Value: `৳ 3.98 Cr`
   - Subtext: `Collection efficiency: 82.5%`
   - Badge: `▲ +9.4%`
   - Icon: Cash Inflow Register
3. **Overdue Receivables (Aging AR):**
   - Value: `৳ 84.2 লাখ`
   - Subtext: `14 customers exceeding 45 days credit`
   - Badge: `High Follow-up`
   - Icon: Exclamation Alert Shield
4. **Active Quotations / Pipeline:**
   - Value: `৳ 1.65 Cr`
   - Subtext: `8 Quotations awaiting client sign-off`
   - Badge: `Conversion: 68%`
   - Icon: Quotation Funnel

---

## 3. Submodule Navigation Tabs
1. **Sales Invoices & Billing** *(Default Active View)*
2. **Quotations & Commercial Estimates**
3. **Sales Orders (SO) & Proforma Invoices**
4. **Delivery Challans & Dispatch Tracking**
5. **Customer Credit Limits & Ledger Aging**
6. **Credit Notes, Refunds & Returns**
7. **Recurring Invoices & Annual Service Contracts (AMC)**

---

## 4. Main Content Area (Default: Invoices & Billing)

### 4.1 Filter & Search Bar
- Search: Invoice No., Customer Name, Sales Rep, or PO Reference.
- Status Filter: `All Invoices`, `Paid`, `Partially Paid`, `Unpaid`, `Overdue`, `Draft`.
- Timeframe: `This Month`, `Last 30 Days`, `Quarterly`, `Custom Date`.

### 4.2 Interactive Sales Invoices Data Table
| Invoice Date | Invoice # | Customer / Client | Total Amount (৳) | VAT / Tax (৳) | Paid Amount (৳) | Balance Due (৳) | Status | Actions |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 06 Nov 2026 | `INV-2026-1492` | Bashundhara Infrastructure Ltd | 34,50,000 | 4,50,000 | 34,50,000 | 0 | `Paid` | View, PDF |
| 05 Nov 2026 | `INV-2026-1491` | Walton Hi-Tech Industries PLC | 18,20,000 | 2,37,000 | 10,00,000 | 8,20,000 | `Partial` | View, Collect |
| 04 Nov 2026 | `INV-2026-1490` | Summit Power International | 42,80,000 | 5,58,000 | 0 | 42,80,000 | `Overdue` | Follow-up, PDF |
| 03 Nov 2026 | `INV-2026-1489` | Meghna Group of Industries | 12,40,000 | 1,61,000 | 12,40,000 | 0 | `Paid` | View, PDF |
| 02 Nov 2026 | `INV-2026-1488` | Beximco Pharmaceuticals Ltd | 28,90,000 | 3,75,000 | 0 | 28,90,000 | `Pending` | Send Reminder |
| 01 Nov 2026 | `INV-2026-1487` | Apex Footwear Limited | 8,75,000 | 1,14,000 | 8,75,000 | 0 | `Paid` | View, PDF |

---

## 5. Modal Blueprint: `+ Create Sales Invoice`
- **Customer Selection:** Dropdown with live credit limit check (e.g. *Limit: ৳ 50L, Available: ৳ 24L*).
- **Invoice Line Items Table:**
  - Product/Service Item, SKU, Unit Price, Qty, Discount (%), VAT (5%/7.5%/15%), Line Total.
  - `+ Add Line Item` row adder.
- **Payment Terms:** Net 15, Net 30, Net 60, Advance.
- **Summary:** Subtotal, VAT Total, Grand Total (BDT).
- **Buttons:** `Save as Draft`, `Issue Invoice & Send Email`, `Print Challan`.

