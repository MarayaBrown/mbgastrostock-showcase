# MBGastroStock - Demo Mode Guide

## Quick Start

**Try the live demo:** https://mbgastrostock.vercel.app/?demo=true

No registration needed. Full interactive experience with sample data and guided walkthrough.

---

## What's in the Demo?

### 📊 Dashboard
- **Real-time inventory view** with stock status indicators
- **Color-coded inventory states:**
  - 🟢 Green: Stock ok (above minimum)
  - 🟡 Yellow: Low stock (below minimum)
  - 🔴 Red: Out of stock (agotado)
- **20 sample products** across 4 realistic categories

### 📦 Sample Products

#### Verduras (Vegetables)
- Tomates (Tomatoes) - 15 kg → minimum 5 kg
- Lechuga (Lettuce) - 8 heads → minimum 10 heads (⚠️ LOW)
- Cebolla (Onion) - 0 kg → minimum 3 kg (❌ OUT)
- Papa (Potato) - 25 kg → minimum 10 kg

#### Lácteos (Dairy)
- Queso (Cheese) - 5 kg
- Leche (Milk) - 20 L
- Yogur (Yogurt) - 12 units
- Crema (Cream) - 3 L

#### Pastas (Grains & Bread)
- Pasta Seca (Dry Pasta) - 50 units
- Arroz (Rice) - 100 kg
- Harina (Flour) - 25 kg
- Pan (Bread) - 12 units

#### Bebidas (Beverages)
- Jugo (Juice) - 30 L
- Agua (Water) - 100 units
- Gaseosa (Soda) - 50 units
- Cerveza (Beer) - 24 units

### 👥 Demo Team Members

- **Sofía Morales** (Admin) — Manager principal
- **Diego Ramírez** (Member) — Asistente de cocina
- **Ana Torres** (Member) — Personal de almacén

### 🎯 Guided Walkthrough (7 Steps)

The demo includes an **interactive step-by-step guide** with:

1. **Welcome** — Introduction to the app
2. **Dashboard Overview** — Stock at a glance
3. **Stock Tab** — Detailed inventory management
4. **Add to Team** — Managing team permissions
5. **Inventory Alert** — Low stock notifications
6. **Settings** — User preferences and configurations
7. **Export Data** — Generate PDF reports (demo data)

**Features of the walkthrough:**
- 🔆 Spotlight highlighting that illuminates each section
- 💬 Contextual tooltips explaining each feature
- ⌨️ Keyboard navigation support
- 🎨 Dark mode optimized for visibility
- ▶️/◀️ Navigation buttons to go forward/back through steps

### 📱 Mobile Experience

#### PWA Install Button
On mobile devices, a prominent **"📱 Agregar a inicio"** button appears in the hero section:

**Android (Chrome/Edge):**
- Uses native `beforeinstallprompt` event
- One-tap installation to home screen
- Works like any native app

**iOS (Safari):**
- Detects iOS user agent
- Shows visual 3-step guide in modal:
  1. Click share button
  2. Select "Add to Home Screen"
  3. Tap "Add"

### 🎨 User Interface

#### Desktop View (1440px)
- Two-column layout
- Sidebar navigation
- Full-width content area
- All tabs visible

#### Mobile View (375px)
- Single column layout
- Bottom navigation (if used)
- Touch-optimized spacing
- Responsive component sizing

---

## How Demo Mode Works

### Technical Details

1. **Query Parameter:** `?demo=true` activates demo mode
2. **Isolated State:** Demo data exists only in memory, never touches the real database
3. **Demo Component:** Special `DemoVistaComercio` component renders instead of production `VistaComercio`
4. **No Authentication:** No login required for demo mode
5. **Sample Data:** Pre-populated with 20 products and 3 team members

### Files Involved

- `src/components/demo/DemoVistaComercio.jsx` — Main demo view component
- `src/components/demo/DemoWalkthrough.jsx` — Guided walkthrough system
- `src/hooks/useDemo.js` — Demo data and state management
- `src/utils/demoData.js` — Sample product and team data

---

## Key Features to Explore

### 1. Real-time Stock Updates
- Modify product quantities (in your mind — demo data is read-only visually)
- See automatic state recalculation
- Understand how the app prioritizes low-stock items

### 2. Role-Based Access
- Admin can view all team data
- Members see limited information
- Understand permission levels without needing multiple logins

### 3. Data Export
- Export visible inventory to PDF
- See how reports look
- Understand data portability

### 4. Responsive Design
- Test on multiple screen sizes
- Try the walkthrough on both desktop and mobile
- Verify touch interactions on mobile

### 5. Accessibility
- Navigate using keyboard only (Tab, Enter)
- Reduced motion preference respected
- High contrast colors for visibility

---

## Demo Limitations (By Design)

❌ **Cannot:**
- Modify actual data (demo-only)
- Create real user accounts
- Access production database
- Save custom settings
- Generate real reports

✅ **Can:**
- See the full UI/UX
- Interact with all buttons and tabs
- Follow the guided walkthrough
- Test mobile responsiveness
- Understand the workflow

---

## Sharing the Demo

### Share with Others
- **Desktop:** https://mbgastrostock.vercel.app/?demo=true
- **Mobile:** Same URL, responsive layout adapts automatically
- **QR Code:** Can generate QR pointing to demo URL for printed materials

### Embed in Presentation
- Screenshots available in `/screenshots` directory
- Use demo data examples in pitch decks
- Show walkthrough in live demonstrations

---

## Feedback & Improvements

The demo is designed to be **learnable** and **safe to explore**:
- Try any action without breaking anything
- All features are fully functional
- Perfect for understanding the app workflow before diving into setup

**Questions?** Check the main README.md for setup instructions.
