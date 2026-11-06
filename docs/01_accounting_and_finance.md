# Module 01: Accounting & Finance — UI & Content Blueprint

> **File Name:** `finance_module.html`  
> **Accent Theme:** Royal Blue (`#2563eb`, `text-blue-600`, `bg-blue-50/70`)  
> **Parent Navigation:** `erp_cover_page.html` (Cover Portal)  
> **Contextual Watermark Art:** Neoclassical Bank Treasury Building / General Ledger Scales

---

## 1. Page Header & Navigation Bar
- **Top Bar:** Glassmorphic container (`bg-white/65 backdrop-blur-md border-b border-white/50`).
- **Breadcrumbs:** `Inceptia ERP / Finance & Accounting / General Ledger & Vouchers`
- **Back Navigation:** `← Back to Executive Portal` (links to `erp_cover_page.html`).
- **Header Actions:**
  - `+ New Journal Entry` (Primary Blue Button)
  - `+ Create Payment Voucher` (Secondary Outline Button)
  - Date Range Picker (e.g. `Nov 1, 2026 - Nov 30, 2026`)
  - Export Dropdown (`Excel`, `PDF`, `CSV`)

---

## 2. Top KPI Cards (4 Department Pillars)
Four frosted glass cards with 75% opacity and department-specific metrics:

1. **Operating Cash & Bank Balance:**
   - Value: `৳ 3.84 Cr`
   - Subtext: `Across 4 active bank accounts (Net Liquidity)`
   - Badge: `▲ +6.4% MoM`
   - Icon: Bank Vault Shield
2. **Accounts Receivable (AR):**
   - Value: `৳ 84.5 লাখ`
   - Subtext: `৳ 12.8 লাখ overdue (> 30 days)`
   - Badge: `18 Invoices Pending`
   - Icon: Arrow-Down-Left (Incoming Funds)
3. **Accounts Payable (AP):**
   - Value: `৳ 42.1 লাখ`
   - Subtext: `৳ 8.5 লাখ due this week`
   - Badge: `11 Vendor Bills`
   - Icon: Arrow-Up-Right (Outgoing Bills)
4. **Current Month Net Margin:**
   - Value: `26.6%`
   - Subtext: `P&L Operating Profit: ৳ 1.28 Cr`
   - Badge: `▲ +3.2% vs Target`
   - Icon: Balance Scale / Chart

---

## 3. Submodule Sidebar & Tabs
Navigation tabs to toggle between core accounting submodules:
1. **General Ledger & Journal Entries** *(Default Active View)*
2. **Chart of Accounts (COA)**
3. **Accounts Receivable (AR / Customer Invoices)**
4. **Accounts Payable (AP / Supplier Bills)**
5. **Bank Reconciliation & Cash Book**
6. **Trial Balance & Financial Statements (P&L / Balance Sheet)**
7. **VAT, TDS & Tax Compliance (NBR Form 9.1)**

---

## 4. Main Content Area (Default: General Ledger & Vouchers)

### 4.1 Filter & Search Bar
- Search: Filter by Voucher No., Account Title, Cheque No., or Remarks.
- Filter Pills: `All Types`, `Payment Vouchers (PV)`, `Receipt Vouchers (RV)`, `Journal Vouchers (JV)`, `Contra (CV)`.
- Status: `Posted (Approved)`, `Draft`, `Pending Approval`.

### 4.2 Interactive Ledger Data Table
| Date | Voucher No. | Type | Account Debit / Credit | Reference / Beneficiary | Debit (৳) | Credit (৳) | Status | Actions |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 06 Nov 2026 | `PV-2026-0842` | Payment | BRAC Corporate A/C → Meghna Cement Ltd | Raw materials supply | - | 18,50,000 | `Posted` | View, PDF |
| 06 Nov 2026 | `RV-2026-1019` | Receipt | Cash In Hand ← BSRM Steels collection | Inv #INV-4921 | 8,20,000 | - | `Posted` | View, PDF |
| 05 Nov 2026 | `JV-2026-0412` | Journal | Depreciation Reserve → Plant Machinery | Monthly asset depreciation | 2,45,000 | 2,45,000 | `Posted` | View, PDF |
| 05 Nov 2026 | `CV-2026-0188` | Contra | City Bank LC → DBBL Payroll A/C | Fund transfer for salary | 68,40,000 | 68,40,000 | `Approved` | View, PDF |
| 04 Nov 2026 | `PV-2026-0841` | Payment | Petty Cash Vault → Office Admin | Facility utilities bill | - | 45,000 | `Posted` | View, PDF |
| 04 Nov 2026 | `JV-2026-0411` | Journal | Deferred VAT → Input Tax Receivable | October VAT reconciliation | 5,12,000 | 5,12,000 | `Pending` | Approve, Edit |

---

## 5. Modal Blueprint: `+ New Journal Entry`
- **Fields:**
  - Voucher Date, Currency (`BDT / USD / EUR`).
  - Credit Account (Dropdown with search).
  - Debit Account (Dropdown with search).
  - Amount, Reference No., Narration / Description.
  - Attachment upload (Cheque scan / Bill invoice).
- **Buttons:** `Save as Draft`, `Post & Print Voucher`, `Cancel`.

