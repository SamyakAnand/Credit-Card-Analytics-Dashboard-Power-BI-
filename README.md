# ⭐ **README.md — Credit Card Analytics Dashboard (Power BI)**

This project is an end-to-end **Power BI analytics solution** that provides deep insights into:

* Credit card **revenue**
* Customer **demographics**
* Spending **behavior**
* Transaction patterns
* High-value segments
* Risk profiling
* Expenditure trends
* Performance by age, education, income, job, state

The dashboard consists of **two fully-designed pages**:

1. **Transaction Report**
2. **Customer Report**

Both pages include slicers, KPI cards, interactive charts, and detailed data tables for dynamic exploration.

---

## 🚀 **Project Highlights**

### ✔ Fully Interactive Power BI Dashboard

Users can slice/filter by:

* Quarter
* Gender
* Income Level
* Education
* Customer Job
* Expenditure Type
* Payment Mode
* Week Start Date
* Risk Level
* Card Category
  and more…

### ✔ Clean & Professional UI

Designed with:

* Proper alignment & pixel-perfect layout
* Consistent chart sizes
* Modern theme with neon blue & purple tones
* Clean typography and border radius
* Clear drill-down paths

### ✔ End-to-End BI Project

Includes:

* Data Cleaning
* Data Modeling
* DAX Measures
* Data Visualization
* Insights extraction

---

# 🗂 **Project Folder Structure**

```
📁 Credit-Card-Analytics-Dashboard
│
├── 📄 CC_Dashboard.pbix
├── 📄 README.md
├── 📄 credit_card.csv
├── 📄 customer.csv
├── 📄 theme.json
├── 📄 CC_Customer Report.png
└── 📄 CC_Transaction Report.png
```

---

# 📥 **Data Sources**

The dataset includes:

### 🧾 Transaction Table

* Card Category
* Annual Fees
* Total Transaction Amount
* Interest Earned
* Week_Start_Date
* Expenditure Type
* Payment Mode (Chip, Online, Swipe)
* Delinquency Status

### 🧍‍♂️ Customer Table

* Customer Age
* Gender
* Education Level
* Income Level
* Customer Job
* State
* Dependent Count

These tables were merged using **Client_Num** keys.

---

# 🧹 **Data Cleaning Steps (Power Query)**

✔ Removed null & duplicate records
✔ Standardized categorical values
✔ Converted date fields to datetime
✔ Extracted Quarter, Month, Year
✔ Cleaned numeric formats (income, revenue, interest)
✔ Created Age Bins (20–30, 30–40, etc.)
✔ Removed unused columns

---

# 🧠 **Key DAX Measures**

```DAX
Total Revenue = SUM(credit_card[Total_Trans_Amt])

Total Interest = SUM(credit_card[Interest_Earned])

Avg Utilization = AVERAGE(credit_card[Avg_Utilization_Ratio])

Total Customers = DISTINCTCOUNT(customer[Client_Num])

Revenue Per Customer = DIVIDE([Total Revenue], [Total Customers], 0)

Quarterly Growth = 
CALCULATE(
    [Total Revenue],
    FILTER(
        ALL('Date'),
        'Date'[Quarter] = MAX('Date'[Quarter]) - 1
    )
)
```

---

# 📊 **Dashboard Pages**

---

## 🟦 **Page 1 – Credit Card Transaction Report**

![Transaction Report](https://github.com/SamyakAnand/Credit-Card-Analytics-Dashboard-Power-BI-/blob/main/CC_Transaction%20Report.png)

### 🔹 **KPIs**

* Total Revenue
* Total Interest
* Total Transaction Amount
* Total Transaction Count

### 🔹 **Slicers**

* Quarter (Q1–Q4)
* Income Group (High, Med, Low)
* Gender (M, F)
* Card Category
* Risk Rating
* Payment Mode
* Start Date

### 🔹 **Visuals**

* Revenue & Transaction Combo Chart by Quarter
* Expenditure Pie/Bar Charts
* Revenue by Expenditure Type
* Card Category Summary Table
* Payment Mode Revenue
* Expenditure Matrix (Bills, Entertainment, Food, Grocery, Travel, etc.)

---

## 🟪 **Page 2 – Credit Card Customer Report**

![Customer Report](https://github.com/SamyakAnand/Credit-Card-Analytics-Dashboard-Power-BI-/blob/main/CC_Customer%20Report.png)

### 🔹 **KPIs**

* Revenue
* Total Interest
* Average Income
* Customer Satisfaction Score

### 🔹 **Slicers**

* Quarter
* Gender
* Income Group
* Age Group
* Payment Mode
* Education
* Job

### 🔹 **Visuals**

* Revenue Trend by Week (Line Chart)
* Revenue by Age Group
* Customer Job Table
* Revenue by Income Group
* Revenue by Education
* Revenue by Jobs
* Top States
* Revenue by Dependents

---

# 🎨 **Design & Layout Approach**

The dashboard follows a **professional, pixel-perfect layout**:

### KPI Cards

```
Width = 230 px  
Height = 95 px  
Spacing = 20 px  
```

### Big Charts

```
Width = 510 px  
Height = 260 px  
```

### Slicers

```
Height = 45–55 px  
Width  = 130–180 px  
```

### Small Bar Charts

```
Width = 300–310 px  
Height = 220 px  
```

### Tables

```
Width = 510–1040 px  
Height = 260–300 px  
```

Spacing between visuals: **12–15 px**

---

# 🔍 **Insights Delivered**

### 📈 Revenue Insights

* Q3 generated the highest overall revenue
* Platinum & Gold cards contribute most to interest income
* Swipe transactions dominate total volume

### 🧍‍♂️ Demographic Insights

* Age group **40–50** has the highest revenue
* Graduate & High-school customers spend the most
* Businessmen and Govt employees generate stable income

### ☑ Behavioral Patterns

* Bills, Entertainment, Fuel, Grocery account for **70%+ expenditure**
* Online & Chip payments are rising
* Medium-income customers perform the highest number of transactions

---

# 📌 **Technologies Used**

* **Power BI** (Desktop)
* **DAX**
* **Power Query**
* **Data Modeling (Star Schema)**
* **Custom Theme JSON**

---

# 📘 **How to Use This Project**

1. Clone or download the repository
2. Open the `.pbix` file in Power BI Desktop
3. Load datasets if needed
4. Interact using slicers and visual filters
5. Modify DAX measures or visuals if you want to customize

---

# 🏁 **Conclusion**

This project demonstrates:

* Advanced Power BI design skills
* Complete analytical storytelling
* Strong ETL + DAX + visualization knowledge
* Business-ready dashboard creation

It is ideal for:

* Portfolio
* Data Analyst Resume
* BI Engineer Job Applications
* Business Presentations