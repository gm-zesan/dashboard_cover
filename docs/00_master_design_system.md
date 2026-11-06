# Inceptia ERP — Master Design System & UI Specifications

> **Status:** Locked & Approved (Reference: `erp_cover_page.html`)  
> **Target Platform:** Desktop & Responsive Enterprise Web Application  
> **Design Philosophy:** Frosted Glassmorphism (Glass Hierarchy) + High-Contrast 3D Elevation + Bespoke Contextual Watermarks

---

## 1. Visual Foundation & Canvas

### 1.1 Canvas Background & Atmosphere
To achieve a high-end, translucent glassmorphism look (similar to Apple macOS, Stripe, and Fluent Design), the page uses a multi-layered atmospheric background:

- **Base Canvas Color:** `#f4f6fa` (Soft luminous cool-slate background).
- **Fixed Enterprise Wallpaper:** 
  - **Asset:** `assets/erp_bg.jpg` (High-resolution 3D Inceptia ERP Digital Ecosystem: interconnected nodes, global supply chains, data streams).
  - **Positioning:** `fixed inset-0 pointer-events-none z-0 overflow-hidden`
  - **CSS Styling:** `w-full h-full object-cover object-center opacity-30 filter contrast-105`
  - **Tint Overlay:** `<div class="absolute inset-0 bg-slate-900/[0.02]"></div>`
- **Ambient Aurora Mesh Light Pools:**
  Four soft, blurred ambient glow pools that subtly refract light through the frosted glass cards:
  ```html
  <div class="fixed inset-0 pointer-events-none z-0 overflow-hidden">
    <!-- Top-Left Royal Blue Glow Pool -->
    <div class="absolute -top-36 -left-24 w-[650px] h-[520px] bg-blue-500/10 rounded-full blur-[140px]"></div>
    <!-- Top-Right Violet/Indigo Glow Pool -->
    <div class="absolute -top-32 right-[-5%] w-[600px] h-[480px] bg-indigo-500/[0.09] rounded-full blur-[140px]"></div>
    <!-- Mid-Page Sky/Cyan Ambient Pool -->
    <div class="absolute top-[35%] left-[10%] w-[550px] h-[450px] bg-sky-400/[0.06] rounded-full blur-[160px]"></div>
    <!-- Bottom-Right Emerald Ambient Pool -->
    <div class="absolute bottom-16 right-[12%] w-[580px] h-[460px] bg-emerald-500/[0.05] rounded-full blur-[150px]"></div>
  </div>
  ```

---

## 2. Typography & Fonts

- **Font Family:** `'Plus Jakarta Sans', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`
- **Weights in Use:**
  - `400 (Regular)`: Secondary labels, timestamps, metadata.
  - `500 (Medium)`: Descriptions, table body cells, form inputs.
  - `600 (SemiBold)`: Subheadings, action buttons, table column headers.
  - `700 (Bold)`: Section titles, KPI labels, major metrics.
  - `800 (ExtraBold)`: Hero financial numbers (e.g., `৳ 4.82 Cr`), badge percentages.

### Typography Hierarchy:
| Element | Font Size | Weight | Color | Tracking |
| :--- | :--- | :--- | :--- | :--- |
| **Hero KPI Numbers** | `24px` (`text-2xl`) | `800` | `#ffffff` | `tracking-tight` |
| **Section Headings (H3)** | `14px` (`text-sm`) | `700` | `#0f172a` (`slate-900`) | `tracking-tight` |
| **Card Subheaders (H4)** | `12px` (`text-xs`) | `700` | `#0f172a` (`slate-900`) | Normal |
| **Body / Table Text** | `12px` (`text-xs`) | `500` / `600` | `#334155` (`slate-700`) | Normal |
| **Micro Labels & Badges** | `10px - 11px` (`text-[10px]` / `[11px]`) | `600` / `700` | `#64748b` (`slate-500`) | `uppercase tracking-wider` |

---

## 3. Glassmorphic Color Palette & Design Tokens

### 3.1 Primary Glass Card Tokens
```css
/* Standard Executive Card */
.executive-card {
  background: rgba(255, 255, 255, 0.55);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border: 1px solid rgba(255, 255, 255, 0.65);
  box-shadow: 0 4px 24px -4px rgba(15, 23, 42, 0.07), 0 1px 3px rgba(15, 23, 42, 0.04);
  transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}

.executive-card:hover {
  background: rgba(255, 255, 255, 0.78);
  border-color: rgba(255, 255, 255, 0.90);
  box-shadow: 0 10px 28px -5px rgba(15, 23, 42, 0.10), 0 2px 6px rgba(15, 23, 42, 0.06);
}

/* Modular Sub-Card */
.module-card {
  background: rgba(255, 255, 255, 0.55);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border: 1px solid rgba(255, 255, 255, 0.65);
  box-shadow: 0 2px 10px rgba(15, 23, 42, 0.03);
  transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}

.module-card:hover {
  background: rgba(255, 255, 255, 0.82);
  border-color: rgba(255, 255, 255, 0.90);
  box-shadow: 0 8px 24px -4px rgba(15, 23, 42, 0.08);
}
```

### 3.2 Top Vibrant KPI Glass Cards (The 4 Signature Pillars)
The 4 top KPI cards use rich, saturated enterprise colors with a 75%–90% translucent frosted glass finish:
1. **Total Revenue (Matte Royal Blue):**
   - Classes: `bg-[#2563eb]/75 hover:bg-[#2563eb]/85 backdrop-blur-md border border-white/30 text-white rounded-2xl p-4 shadow-md hover:shadow-lg`
   - Icon Badge: `bg-white/15 backdrop-blur-sm border border-white/20 text-white`
   - Percentage Pill: `bg-white/20 border border-white/25 text-white font-bold`
2. **Gross Profit (Matte Royal Purple):**
   - Classes: `bg-[#7c3aed]/75 hover:bg-[#7c3aed]/85 backdrop-blur-md border border-white/30 text-white rounded-2xl p-4 shadow-md hover:shadow-lg`
3. **Total Expenses (Matte Emerald Green):**
   - Classes: `bg-[#059669]/75 hover:bg-[#059669]/85 backdrop-blur-md border border-white/30 text-white rounded-2xl p-4 shadow-md hover:shadow-lg`
4. **Net Profit (Matte Sunset Orange):**
   - Classes: `bg-[#ea580c]/75 hover:bg-[#ea580c]/85 backdrop-blur-md border border-white/30 text-white rounded-2xl p-4 shadow-md hover:shadow-lg`

### 3.3 Semantic Departmental Palette
Each ERP module has an assigned brand accent color for icons, header bands, and active states:
- 🔵 **Accounting & Finance:** `Blue` (`#2563eb`, `bg-blue-50/70`, `text-blue-600`)
- 🟢 **Sales & Invoicing:** `Emerald` (`#059669`, `bg-emerald-50/70`, `text-emerald-600`)
- 🟠 **Purchase & Suppliers:** `Amber/Orange` (`#d97706`, `bg-amber-50/70`, `text-amber-600`)
- 🟣 **Inventory & Warehouse:** `Purple` (`#7c3aed`, `bg-purple-50/70`, `text-purple-600`)
- 🔷 **CRM & Customers:** `Indigo` (`#4f46e5`, `bg-indigo-50/70`, `text-indigo-600`)
- 🔴 **HR & Payroll:** `Rose` (`#e11d48`, `bg-rose-50/70`, `text-rose-600`)
- 🟢 **Project Management:** `Teal` (`#0d9488`, `bg-teal-50/70`, `text-teal-600`)
- 🟦 **Reports & Analytics:** `Cyan` (`#0891b2`, `bg-cyan-50/70`, `text-cyan-600`)

---

## 4. Contextual Watermark Art Specification

Every card on the dashboard features a bespoke vector SVG watermark silhouette anchored at the bottom-right corner. It creates a subtle, engraved glass luxury feel without ever competing with readable text.

### Implementation Rules:
1. **Container Class:** Must include `relative overflow-hidden group`
2. **Foreground Content:** All text, numbers, tables, and buttons must be wrapped in `relative z-10`
3. **Watermark Element:**
   ```html
   <!-- Contextual Watermark Art -->
   <div class="absolute -bottom-6 -right-6 w-32 h-32 pointer-events-none opacity-[0.045] group-hover:opacity-[0.08] group-hover:scale-105 transition-all duration-300 text-[color] z-0 select-none">
     <svg class="w-full h-full" fill="currentColor" viewBox="0 0 24 24">
       <!-- Clean SVG path -->
     </svg>
   </div>
   ```
4. **Opacity Standards:**
   - Dark KPI cards: `opacity-[0.08]` (Hover: `[0.14]`, color `text-white`)
   - Light Glass cards: `opacity-[0.045]` to `[0.05]` (Hover: `[0.08]` to `[0.10]`, color matching department theme)

---

## 5. UI Component Standards

### 5.1 Glass Header
- Container: `relative w-full border-b border-white/50 bg-white/65 backdrop-blur-md z-30 shadow-2xs`
- Controls: Search input with `⌘K` badge, date pill, interactive timeframe dropdown, and Group View selector.

### 5.2 Interactive Data Tables
- Header row: `border-b border-slate-100 text-slate-400 text-[10px] uppercase font-bold tracking-wider`
- Row hover: `hover:bg-slate-50/80 transition`
- Zebra / Dividers: `divide-y divide-slate-100 font-medium text-slate-700`

### 5.3 Badges & Status Pills
- **Active / Completed:** `px-2 py-0.5 rounded-full bg-emerald-50 text-emerald-700 font-semibold text-[10px]`
- **Pending / Action Required:** `px-2 py-0.5 rounded-full bg-amber-50 text-amber-700 font-semibold text-[10px]`
- **Funded / In-Progress:** `px-2 py-0.5 rounded-full bg-blue-50 text-blue-700 font-semibold text-[10px]`
- **Rejected / High Risk:** `px-2 py-0.5 rounded-full bg-rose-50 text-rose-700 font-semibold text-[10px]`

### 5.4 1-Click Action Buttons
- **Approve / Success Action:**
  `class="px-2.5 py-1 rounded-md bg-emerald-600 hover:bg-emerald-700 text-white font-semibold text-[10px] shadow-2xs transition flex items-center gap-1 cursor-pointer"`
- **Reject / Cancel Action:**
  `class="px-2 py-1 rounded-md bg-slate-200 hover:bg-rose-50 hover:text-rose-600 text-slate-600 font-semibold text-[10px] transition border border-slate-200 cursor-pointer"`
- **Primary Modal Launch Action:**
  `class="px-3.5 py-1.5 rounded-xl bg-blue-600 hover:bg-blue-700 text-white font-bold text-xs shadow-sm transition flex items-center gap-1.5 cursor-pointer"`

### 5.5 Toast Notifications
- Fixed container at `bottom-5 right-5 z-50 flex flex-col gap-2 pointer-events-none`
- Single toast bubble: `px-4 py-2.5 rounded-xl bg-slate-900/95 backdrop-blur-md text-white text-xs font-semibold shadow-lg border border-slate-700 flex items-center gap-2`
- Auto-dismiss after 3000ms with slide-up / fade-out transition.

---

## 6. Grid & Layout Architecture

```
[ Top Header: Navigation, Search ⌘K, Period, Profile ] (Fixed / Sticky 65% Glass)
---------------------------------------------------------------------------------
[ Row 1: 4 Vibrant Frosted KPI Cards (Revenue, GP, Expenses, Net Profit) ]
---------------------------------------------------------------------------------
[ Row 2: Main Split Grid (xl:grid-cols-12 gap-5 items-stretch) ]
  ├── Left 9 Columns (xl:col-span-9 space-y-5):
  │     ├── Revenue & Profit Trend Chart (7 cols) + Revenue Donut Chart (5 cols)
  │     ├── Key Modules Accordion Workspaces (8 modules in 2x4 grid with Search & Filter)
  │     └── Operations Row: Cash & Bank Liquidity (left) + Project Milestones (right)
  │
  └── Right 3 Columns (xl:col-span-3 flex flex-col justify-between gap-4):
        ├── Card 1: Today's Agenda (5 calendar items)
        ├── Card 2: Pending Approvals (3 items with 1-click Approve/Reject)
        ├── Card 3: Key Tasks (6 checklist items with live count & strike-through)
        └── Card 4: Recent Activity Log (Live audit stream, 100% flush bottom-aligned)
---------------------------------------------------------------------------------
[ Footer: Enterprise Version, Status Indicator, Copyright ] (65% Glass)
```

