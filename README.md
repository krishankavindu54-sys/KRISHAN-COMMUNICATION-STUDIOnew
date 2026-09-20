# Apex Communication & Mobile Care POS System

A high-performance, modern Web Point of Sale (POS), Phone Repair Service & Utility Bill Payment Management system built with **Next.js 14+ (App Router, TypeScript)**, **Tailwind CSS**, and **Persistent JSON/SQLite Database**.

Designed specifically for **Communication Shops, Mobile Phone Repair & Service Centers, Reload & Utility Payment Counters, and Retailers**.

---

## 🚀 Key Features

### 1. 📱 Phone Repair Service & Job Tracking (`/repairs`)
- **Customer & Device Intake**:
  - Customer name, phone number, and NIC.
  - Brand presets (*Samsung, Apple, Xiaomi, Redmi, Vivo, Oppo, Huawei, Realme, Nokia, etc.*) & model.
  - IMEI / Serial number, Screen Lock PIN / Pattern note, and device color.
  - Common hardware fault checkboxes (*Display, Charging Port, Battery, Water Damage, Dead/No Power, Mic/Speaker, etc.*).
  - Accessories received (*SIM Card, SD Card, Back Cover, Device Only*).
  - Estimated Repair Cost, Advance Paid, and Auto-calculated Balance Due.
  - Status Workflow: `Received` &rarr; `In Progress` &rarr; `Waiting Parts` &rarr; `Ready for Pickup` &rarr; `Delivered / Settled`.
- **80mm Thermal Repair Chit / Job Card**:
  - Direct support for **80mm Thermal Receipt Printers**.
  - Job Number Barcode & QR Code.
  - Reported faults, condition notes, advance amount, balance due, terms & conditions, and signature lines.
- **Settle & Deliver**: Collect remaining balance when customer picks up the phone and mark completed.

### 2. 🧾 Utility Bill Payments with Tiered Commissions (`/bills`)
- **Supported Providers**:
  - 🌾 **එකාබද්ද වලව මව් නදී** (Walawe Irrigation & Water)
  - ⚡ **Ceylon Electricity Board (CEB)** / ලංකා විදුලිබල මණ්ඩලය
  - 💧 **National Water Supply & Drainage Board** / ජල සම්පාදන මණ්ඩලය
  - 📱 **Mobitel Postpaid & Reload**
  - 📶 **Dialog Axiata** (Mobile, TV, Broadband)
  - ☎️ **Sri Lanka Telecom (SLT)** (Megaline, Fiber)
- **Automated Tiered Service Fee Commission Formula**:
  - Bill Amount **< Rs. 5,000** &rarr; **+ Rs. 30** service fee
  - Bill Amount **Rs. 5,000 to Rs. 15,000** &rarr; **+ Rs. 40** service fee
  - Bill Amount **> Rs. 15,000** &rarr; **+ Rs. 50** service fee
- **Multi-Bill Batch Processing (එකවර බිල්පත් කිහිපයක් එකතු කිරීම)**:
  - Add 1, 2, 3, or more bills into a batch queue before checking out together.
  - Live summary: Total Bills Subtotal + Total Service Fees = Grand Total Payable.
- **80mm Thermal Bill Receipt**:
  - Itemized receipt showing each provider, Account Number, Reference Number, Bill Amount, Service Fee, and Grand Total.

### 3. 📒 Customer Debtors & Credit Book (`/debtors`)
- **Overview Metrics**: Total Outstanding Balance (මුළු හිඟ ණය), Active Debtors Count, Total Customers.
- **Debtor Profiles**: Name, Phone, NIC/Address, Credit Limit, Current Balance.
- **Credit & Settlement Actions**:
  - **Add Credit (ණය ලබාදීම)**: Record new credit sale with description & amount.
  - **Settle Payment (ණය පියවීම)**: Record customer payment and decrement outstanding balance.
- **Chronological Ledger**: Complete timeline of credit given vs payments received.
- **80mm Printable Statement**: Print a statement of account for customers.

### 4. 🛒 Communication Shop Retail POS (`/`)
- Touch & keyboard-friendly product catalog with visual category tabs.
- Quick search with global hotkey shortcut (`/` or `F2`).
- Hardware & Camera Barcode Scanner support.
- Line item discounts, custom item charging, and cart-level discounts.
- Customer loyalty point accrual.
- Hold / Park order functionality.
- Split payments (Cash, Card, Digital / UPI).
- 80mm thermal retail sales receipts with QR codes.

### 5. 📦 Products & Inventory Management (`/products`)
- Full CRUD operations with category tagging, cost price, selling price, and gross margin calculations.
- Low stock warnings and out-of-stock indicators.
- Stock level adjustments (+/- quantity) with audit logging reasons.

### 6. 📊 Orders & Analytics (`/orders`, `/analytics`)
- Searchable transaction ledger with filters by payment status and customer.
- One-click order refund with automatic stock restoration.
- Revenue, profit, top selling products, and category breakdown reports.

---

## ⚙️ Technology Stack

- **Framework**: [Next.js 14](https://nextjs.org/) (App Router, React 18, TypeScript)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Database**: Embedded Persistent JSON/SQLite (`data/pos-db.json`) + Optional Supabase Dual Mode
- **Printing**: Native 80mm & 58mm Thermal Receipt CSS print engine + SVG Barcodes / QR Codes

---

## 💻 How to Run Locally

```bash
# 1. Install dependencies
npm install

# 2. Run the development server
npm run dev

# 3. Build for production
npm run build
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📤 Pushing to GitHub

This repository is ready to push directly to GitHub:

```bash
# Initialize git repository (if not already initialized)
git init

# Add all files (the .gitignore will automatically exclude node_modules and .next)
git add .

# Commit changes
git commit -m "Initial commit: Communication shop POS with phone repairs, bill payments, and debtors"

# Set branch to main
git branch -M main

# Link your GitHub repository
git remote add origin https://github.com/<your-username>/<your-repo-name>.git

# Push to GitHub
git push -u origin main
```
