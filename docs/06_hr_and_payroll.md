# Module 06: HR & Payroll — UI & Content Blueprint

> **File Name:** `hr_payroll_module.html`  
> **Accent Theme:** Rose / Crimson (`#e11d48`, `text-rose-600`, `bg-rose-50/70`)  
> **Parent Navigation:** `erp_cover_page.html` (Cover Portal)  
> **Contextual Watermark Art:** Employee Organization Tree / ID Badge & Salary Slip

---

## 1. Page Header & Navigation Bar
- **Top Bar:** Glassmorphic container (`bg-white/65 backdrop-blur-md border-b border-white/50`).
- **Breadcrumbs:** `Inceptia ERP / Human Resources & Payroll / Staff & Disbursal`
- **Back Navigation:** `← Back to Executive Portal` (links to `erp_cover_page.html`).
- **Header Actions:**
  - `+ Process Monthly Payroll` (Primary Rose Button)
  - `+ Add New Employee` (Secondary Button)
  - Department Filter (`Management`, `Engineering`, `Finance`, `Operations`, `HR`)
  - Month Selector (e.g. `November 2026`)

---

## 2. Top KPI Cards (4 HR Pillars)

1. **Total Active Headcount:**
   - Value: `1,248 Staff`
   - Subtext: `Full-time: 1,180 | Contractual: 68`
   - Badge: `▲ +12 Joined This Month`
   - Icon: Team Organization Hierarchy
2. **Monthly Net Salary Disbursal:**
   - Value: `৳ 68.4 লাখ`
   - Subtext: `Funded via Dutch-Bangla Bank Corporate Payroll`
   - Badge: `Batch Ready for Nov`
   - Icon: Bank Disbursal Safe
3. **Pending Leave Applications:**
   - Value: `3 Requests`
   - Subtext: `Senior engineering & commercial staff`
   - Badge: `1-Click Approval`
   - Icon: Calendar Clock
4. **Today's Attendance Rate:**
   - Value: `96.4%`
   - Subtext: `Biometric & Mobile Check-in recorded`
   - Badge: `On-Time: 92%`
   - Icon: Fingerprint / Checkmark ID

---

## 3. Submodule Navigation Tabs
1. **Employee Master Directory** *(Default Active View)*
2. **Monthly Payroll Processing & Salary Slips**
3. **Daily Attendance & Shift Rosters**
4. **Leave Management & Holiday Calendar**
5. **Tax & Deductions (Provident Fund, Gratuity, TDS)**
6. **Recruitment, Onboarding & Exit Clearance**

---

## 4. Main Content Area (Default: Employee Directory & Payroll)

### 4.1 Interactive Staff Directory & Payroll Table
| Employee ID | Full Name | Department | Designation | Gross Salary (৳) | Deductions / Tax | Net Payable (৳) | Status | Actions |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `EMP-10024` | Kazi Abir Hasan | Executive | Chief Technology Officer | 2,80,000 | 38,000 | 2,42,000 | `Active` | View Profile, Payslip |
| `EMP-10089` | Md. Tariqul Islam | Finance | Head of Accounts & Tax | 1,60,000 | 18,500 | 1,41,500 | `Active` | View Profile, Payslip |
| `EMP-10142` | Nusrat Jahan | Engineering | Senior Software Architect | 1,85,000 | 22,000 | 1,63,000 | `Active` | View Profile, Payslip |
| `EMP-10215` | S. M. Tanvir Ahmed | Operations | Project Director (Infrastructure) | 2,10,000 | 26,500 | 1,83,500 | `Active` | View Profile, Payslip |
| `EMP-10304` | Sabrina Akhter | HR & Admin | Assistant Manager - People & Culture | 85,000 | 7,200 | 77,800 | `Active` | View Profile, Payslip |
| `EMP-10411` | Fahim Al-Mamun | Procurement | SCM & Logistics Coordinator | 72,000 | 5,800 | 66,200 | `On Leave` | View Profile, Payslip |

---

## 5. Modal Blueprint: `+ Process Monthly Payroll`
- **Month Selection:** Select Year & Month.
- **Deduction Rules:** Automated PF (8.33%), Gratuity, Income Tax (TDS), Late attendance fine.
- **Bank Advice Letter:** Select Corporate Disbursal Bank (`Dutch-Bangla Bank` / `BRAC Bank`).
- **Summary Preview:** Total Gross, Total Tax Deducted, Net Disbursal Amount.
- **Buttons:** `Generate Bank Advice File`, `Lock & Disburse Salary`, `Cancel`.
