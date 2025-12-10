# Data-Visualization

This project demonstrates how to build a full analytical dashboard in **Power BI** using a 1000-row sales dataset.  
The focus is on **data visualization**, **insight generation**, and **visual storytelling**.

---

## 🎯 Objective
Create clear, compelling visualizations in Power BI that communicate business insights effectively using a custom dataset.

---

## 🗂 Dataset Description
A 1000-row sales dataset containing:

- Order ID  
- Order Date  
- Customer Name  
- Category  
- Sub-Category  
- State  
- Region  
- Sales  
- Profit  
- Quantity  
- Discount  

---

## 🛠 Tools Used
- Microsoft Power BI Desktop  
- Power Query (ETL)  
- DAX (Calculated Measures)  

---

## 🚀 Step-by-Step Implementation

### **1️⃣ Load Data**
1. Open Power BI Desktop.  
2. Go to **Home → Get Data → Text/CSV**.  
3. Select `sales_dataset_1000.csv`.  
4. Click **Load**.

---

### **2️⃣ Data Cleaning (Power Query)**
1. Open **Transform Data**.  
2. Validate data types:
   - Date → Order Date  
   - Decimal → Sales, Profit, Discount  
   - Whole Number → Quantity  
3. Add calculated columns:
   - **Year** → `Add Column → Date → Year`
   - **Month Name** → `Add Column → Date → Month → Name of Month`
4. Click **Close & Apply**.

---

### **3️⃣ Create DAX Measures**
```DAX
Total Sales = SUM('sales_dataset_1000'[Sales])
Total Profit = SUM('sales_dataset_1000'[Profit])
Avg Discount = AVERAGE('sales_dataset_1000'[Discount])
Total Quantity = SUM('sales_dataset_1000'[Quantity])
