
## 📦 Requirements
- **Tableau Desktop** (any recent version with *Sample – Superstore*).
- Optional: Excel/CSV viewer if you export raw/clean data.

## 🚀 Quick start
1. Open `superstore_project.twbx` in Tableau.
2. Use the sheet tabs (bottom) in order:
   - `S01`–`S04` — initial visuals (trend, bars, histogram, map)  
   - `S05`–`S08` — advanced visuals (dual-axis, heatmap, parameter switch, dynamic filters)  
   - `S09`–`S11` — analytics (regression & clustering)  
   - `D01`, `D02` — dashboards  
   - `Story1` — story points
3. Export screenshots from each view to `/figures/` using the naming below.

## 📊 Visuals & Sheets
- **S01** Monthly Sales Trend  
- **S02** Sales by Category  
- **S03** Profit Histogram  
- **S04** Sales Map (State)  
- **S05** Dual-Axis Sales vs Profit  
- **S06** Heatmap Region × Category  
- **S07** Parameter Metric Switch *(Sales/Profit/Discount)*  
- **S08** Dynamic Filters Demo *(Region → State cascading, Top-N Customers parameter)*  
- **S09** Regression: Discount → Profit *(trend line + R²)*  
- **S10** Customer Clusters *(k-means via Analytics → Cluster)*  
- **S11** Cluster Profiles *(avg Sales/Profit by Cluster)*  
- **D01** Operational Dashboard  
- **D02** Analytical (Segmentation) Dashboard  
- **Story1** Regional Investment Case

## 🔁 Repro tips (key placements)
- **S09 (Regression):**  
  Columns = `AVG(Discount)` (continuous) • Rows = `SUM(Profit)` (continuous) • Marks = Circle • Add `Order ID` to **Detail** • Analytics → **Trend Line (Linear)**.
- **S10 (Clustering):**  
  Columns = `SUM(Sales)` • Rows = `SUM(Quantity)` • `Customer Name` on **Detail** • Analytics → **Cluster** (K=3/4).
- **S11 (Profiles):**  
  **Cluster** → Columns • `AVG(Profit)` (and/or `AVG(Sales)`) → Rows • Marks = Bar • Labels on.

## 🧠 Notes
- **Dataset:** Tableau **Sample – Superstore** (bundled).  
- **Extract:** workbook saved as `.twbx` with a `.hyper` extract for reproducibility.  
- **Interactivity:** Cascading Region→State filters, **Top-N Customers** parameter, dashboard actions (highlight/filter).  
- **Analytics:** Linear regression (R² via *Describe Trend Model*); k-means clustering with cluster profiles.

## 📝 Citations
- Tableau Software. *Sample – Superstore* dataset (included with Tableau Desktop).

## 📄 License
MIT for this repo’s documentation and artifacts. *(The Sample – Superstore dataset is provided by Tableau for educational/demo use.)*
