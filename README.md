An interactive, Excel-based **Sales Performance Dashboard** built on top of a raw sales dataset.  
It provides a clean **corporate-style** view of:

- Monthly Sales & Profit  
- Regional Sales  
- Product Category Sales  
- Key KPIs (Total Sales, Total Profit, Average Order Value, Total Quantity Sold)

This dashboard is designed so you can easily extend it with **PivotTables** and **Slicers** directly inside Excel.

---

## 🧾 Files in This Repository

- `sales_data.csv`  
  Raw transactional sales data (date, region, product category, amounts, etc.).

- `Sales_Dashboard_Advanced.xlsx`  
  The prepared Excel dashboard with:
  - Formatted **Data** sheet (Excel Table)
  - **Monthly_Summary** (month-wise Sales & Profit)
  - **Regional_Summary** (region-wise Sales)
  - **Product_Summary** (product-category-wise Sales)
  - **Dashboard** sheet with KPI cards and charts

> You can upload these files directly to GitHub along with this README.

---

## 📊 Dashboard Features

### 1. Dashboard Sheet

**KPI Cards:**

- **Total Sales**
- **Total Profit**
- **Average Order Value**
- **Total Quantity Sold**

These are displayed in styled “cards” at the top of the Dashboard with consistent fonts, number formats, and borders.

**Charts:**

- **Monthly Sales (Bar Chart)**  
  Visualizes Sales Amount by Month.

- **Regional Sales (Bar Chart)**  
  Compares performance across regions.

- **Product Category Sales (Bar Chart)**  
  Shows contribution by product category.

---

### 2. Data Sheet

- All records loaded into an Excel **Table** (`SalesData`).
- Clean header formatting (dark blue with white bold text).
- **Conditional formatting** on:
  - `Sales_Amount` (color scale)
  - `Profit` (color scale)

This sheet is the **source** for any PivotTables and Slicers you create in Excel.

---

### 3. Summary Sheets

- `Monthly_Summary`
  - Aggregated Sales & Profit by Month
  - Data bars on Sales column

- `Regional_Summary`
  - Total Sales by Region
  - Data bars on Sales column

- `Product_Summary`
  - Total Sales by Product Category
  - Data bars on Sales column

These can be used directly for additional charts or PivotTables.

---

## 🔧 How to Use the Dashboard

### 1. Open the Dashboard

1. Download `Sales_Dashboard_Advanced.xlsx`.
2. Open it in **Microsoft Excel** (desktop version recommended).

You’ll land on the **Dashboard** sheet. Use it for a high-level overview.

---

### 2. Create True PivotTables (Optional but Recommended)

You can build your own PivotTables from the `Data` sheet:

1. Go to the **Data** sheet.
2. Click anywhere inside the `SalesData` table.
3. Go to **Insert → PivotTable**.
4. Choose “New Worksheet”.
5. Example configurations:

**Monthly Sales Pivot:**

- Rows: `Month`  
- Values: `Sales_Amount`, `Profit`  

**Regional Sales Pivot:**

- Rows: `Region`  
- Values: `Sales_Amount`  

**Product Sales Pivot:**

- Rows: `Product_Category`  
- Values: `Sales_Amount`  

---

### 3. Add Slicers for Interactivity

1. Click inside a PivotTable.
2. Go to **PivotTable Analyze → Insert Slicer**.
3. Choose fields like:
   - `Region`
   - `Product_Category`
   - `Sales_Rep`
   - `Customer_Type`
4. Arrange slicers near your PivotCharts or Dashboard.

Now you can filter the entire view interactively.

---

## 🔁 Updating the Data

If you have new sales data:

1. Replace/append rows in `sales_data.csv` (keeping the same column structure), then re-import to Excel, **or**  
2. In `Sales_Dashboard_Advanced.xlsx`, add new rows **below** the existing `SalesData` table in the **Data** sheet.
3. Right-click on any PivotTable → **Refresh**.
4. Charts and PivotTables update automatically.

---

## 🧮 Under the Hood (Logic)

- `Month` is derived from `Sale_Date`.
- `Profit` is calculated as:  
  \[
  \text{Profit} = (\text{Unit_Price} - \text{Unit_Cost}) \times \text{Quantity_Sold}
  \]
- KPIs on the Dashboard use aggregated values from the **Data** table.

---

## 🚀 Future Enhancements (Ideas)

You can extend this project by:

- Adding **PivotCharts** directly on the Dashboard.
- Creating **Region-specific** or **Product-specific** sub-dashboards.
- Adding **timelines** for date-based filtering.
- Integrating with Python/Power Query to auto-refresh data from external sources.

---

## 📄 License

Add your preferred license here, for example:

MIT License – feel free to use, modify, and share.
