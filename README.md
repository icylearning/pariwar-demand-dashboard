# 🛒 Pariwar &mdash; Predictive Sales & Demand Engine (Everything Under One Roof)

An end-to-end, AI-powered inventory and demand forecasting platform customized for **Pariwar Hypermarket & Departmental Stores**. Provides automated sales velocity prediction, safety stock calculation, dead capital identification, and instant purchase order generation.

Built with **HTML5, Tailwind CSS, and Vanilla JavaScript** &mdash; zero build steps, instant local preview.

---

## ⚡ Quick Start

### 1. Direct Browser Preview
Double-click or open the following file in your browser:
```
C:\Users\jalna\.gemini\antigravity\scratch\analytics-dashboard\index.html
```

### 2. Local Python Server (Recommended for full CSV fetch support)
Open PowerShell or your terminal:
```powershell
cd C:\Users\jalna\.gemini\antigravity\scratch\analytics-dashboard
python -m http.server 3000
```
Then visit **[http://localhost:3000](http://localhost:3000)** in Chrome, Edge, or Firefox.

---

## 🔄 The 6-Step Retailer Workflow

StockPulse AI guides shopkeepers through an intuitive 6-stage lifecycle:

```
[1. Setup & Profile] ➔ [2. Data Ingestion & Mapping] ➔ [3. AI Engine Processing]
                                                                │
[6. PO Execution]   ⬅ [5. Stockout Alerts & Actions]  ⬅ [4. Interactive Forecast]
```

### Step 1: Account Setup & Store Profiling
* Choose your business category: **Grocery & FMCG**, **Apparel & Fashion**, **Electronics**, or **Pharmacy & Health**.
* Configure supplier constraints: Local vs. Regional supplier lead times (e.g., 3 days vs. 7 days) and reorder frequencies.

### Step 2: Sales Data Upload & Validation
* **Flexible Ingestion**: Drag and drop sales spreadsheets (`.csv` or `.xlsx`) from POS systems (Tally, Zoho Books, Square, Shopify).
* **Smart Column Mapping**: Automatically detects and matches columns:
  * `Item_Name` ➔ Product Title
  * `Units_Sold` ➔ Volume / Quantity
  * `Date` ➔ Transaction Timestamp
  * `Unit_Price` / `Cost_Price` ➔ Financials
* Includes pre-packaged test data: **[sample_sales_data.csv](file:///C:/Users/jalna/.gemini/antigravity/scratch/analytics-dashboard/sample_sales_data.csv)** with instant 1-click loading.

### Step 3: Historical Cleaning & Engine Processing
* Simulated machine learning pipeline that cleans store closure gaps, normalizes anomalous spikes, factors seasonal event weights, and computes dynamic safety stock with a 95% service level.

### Step 4: Demand Forecast Review
* **Interactive Horizon Slider**: Adjust predictions from **7 Days** (rapid reorders) up to **60 Days** (quarterly planning).
* **Festival & Event Multiplier Slider**: Simulate surge spikes (from **0%** up to **+50%** for holidays/Diwali/mega sales).
* **Category Buckets**:
  * ⚡ **Fast Movers**: High sales velocity requiring immediate stock boost.
  * **Steady Stock**: Safe buffers with standard reorder points.
  * ❄️ **Dead Stock Warning**: Slow-moving products tying up dead working capital.

### Step 5: Stockout Alert & Actionable Recommendations
* Real-time countdown alerts: *"Product X will run out in 2.4 days based on current velocity. Reorder now to beat supplier lead time."*
* Shelf-Life & Perishables Tracker with 1-click **"Apply Markdown"** button that stimulates velocity before expiration.

### Step 6: PO Generation & Export
* Automated Purchase Orders auto-grouped by vendor (**Metro Fresh Foods**, **Apex Naturals**, **Zenith Global Tech**, **Vogue Threads**).
* **One-Click PO Modal**:
  * Formatted printable invoice layout (`window.print()` / PDF export).
  * **"Send via WhatsApp"** button: Automatically drafts a pre-formatted message with items, quantities, and expected delivery date for direct messaging to suppliers.

---

## 📂 Project Architecture

```
analytics-dashboard/
├── index.html              # Complete 6-step dashboard interface & modals
├── styles.css              # Typography, range sliders, print styles for POs
├── app.js                  # Math engine (ROP, Safety Stock, Forecasts, CSV mapper, POs)
├── sample_sales_data.csv   # Pre-configured multi-category sales dataset for testing
└── README.md               # User guide & documentation
```
