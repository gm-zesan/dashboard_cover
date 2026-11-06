# Module 05: CRM & Customers — UI & Content Blueprint

> **File Name:** `crm_module.html`  
> **Accent Theme:** Indigo (`#4f46e5`, `text-indigo-600`, `bg-indigo-50/70`)  
> **Parent Navigation:** `erp_cover_page.html` (Cover Portal)  
> **Contextual Watermark Art:** Customer 360 User Shield / Handshake Partnership Seal

---

## 1. Page Header & Navigation Bar
- **Top Bar:** Glassmorphic container (`bg-white/65 backdrop-blur-md border-b border-white/50`).
- **Breadcrumbs:** `Inceptia ERP / CRM & Commercial / Leads & Client Accounts`
- **Back Navigation:** `← Back to Executive Portal` (links to `erp_cover_page.html`).
- **Header Actions:**
  - `+ Add New Lead / Deal` (Primary Indigo Button)
  - `+ Log Meeting / Call` (Secondary Button)
  - Pipeline Stage Filter (`Lead`, `Discovery`, `Proposal`, `Negotiation`, `Won`)
  - Territory Filter (`Dhaka`, `Chittagong`, `International`)

---

## 2. Top KPI Cards (4 CRM Pillars)

1. **Active Pipeline Value:**
   - Value: `৳ 14.8 Cr`
   - Subtext: `Across 42 qualified enterprise deals`
   - Badge: `▲ +18.5% QoQ`
   - Icon: Deal Pipeline Funnel
2. **Deals Won This Quarter:**
   - Value: `৳ 5.60 Cr`
   - Subtext: `16 major contracts closed successfully`
   - Badge: `Win Rate: 34.2%`
   - Icon: Trophy / Achievement Star
3. **Follow-ups Due Today:**
   - Value: `9 Clients`
   - Subtext: `Calls, demos & contract presentations`
   - Badge: `Urgent Actions`
   - Icon: Calendar Schedule Clock
4. **Key Account Retention:**
   - Value: `96.8%`
   - Subtext: `Annual client renewal & satisfaction rate`
   - Badge: `Loyal Client Base`
   - Icon: Heart / Customer Handshake

---

## 3. Submodule Navigation Tabs
1. **Sales Pipeline & Deals** *(Default Active View — Kanban / Table)*
2. **Customer Master Database (Customer 360 Profiles)**
3. **Lead Generation & Campaign Assignment**
4. **Follow-up Reminders & Meeting Logs**
5. **Customer Support Tickets & SLA Escalation**
6. **Commercial Proposals & Contract Archives**

---

## 4. Main Content Area (Default: Sales Pipeline & Deals)

### 4.1 Interactive Deals Data Table
| Deal Title | Customer / Enterprise | Deal Stage | Deal Value (৳) | Expected Close | Lead Owner | Probability | Actions |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Dhaka-Mawa Expressway ETC Extension | Roads & Highways Dept (RHD) | `Negotiation` | 4,20,00,000 | 25 Nov 2026 | Abir Hasan | 85% | View Deal, Log |
| Bashundhara Commercial Tower ERP | Bashundhara Group | `Proposal Sent` | 1,15,00,000 | 30 Nov 2026 | Kazi Faisal | 60% | Edit Proposal |
| Factory Automation IoT Sensors | Walton Hi-Tech Industries | `Discovery` | 85,00,000 | 15 Dec 2026 | S. M. Tanvir | 40% | Schedule Demo |
| Chittagong Port WMS Cloud Suite | Chittagong Port Authority | `Won / Final Contract` | 2,80,00,000 | Closed | Abir Hasan | 100% | Generate SO |
| Industrial Battery Supply Contract | Summit Power International | `Negotiation` | 95,00,000 | 20 Nov 2026 | Sabrina Noor | 75% | View Terms |

---

## 5. Modal Blueprint: `+ Add New Lead / Deal`
- **Company / Client Name:** Company title, Industry category.
- **Contact Person:** Full name, Designation, Direct mobile, Official email.
- **Deal Details:** Deal title, Estimated value (BDT), Pipeline stage, Expected close date.
- **Assigned Sales Representative:** Sales manager selector.
- **Next Follow-up Action:** Date & meeting note.
- **Buttons:** `Create Deal`, `Save Draft`, `Cancel`.
