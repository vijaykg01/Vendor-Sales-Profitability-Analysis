# Vendor Sales & Profitability Analysis

## 📌 Project Overview

This project analyzes vendor sales and profitability data using **Python, Pandas, SQLite, Matplotlib, and Seaborn**.

The main objective is to explore vendor and brand-level performance, understand sales and profit patterns, identify outliers, and find **brands with relatively low sales but high profit margins** that may have potential for further business analysis.

---

## 🎯 Objectives

* Analyze vendor sales performance.
* Explore sales and profitability distributions.
* Identify potential outliers in numerical data.
* Analyze relationships between numerical variables.
* Compare vendors and brands based on sales and profit margin.
* Identify brands with **low sales but high profit margins**.
* Visualize important patterns using charts and plots.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **SQLite** – Database connection and SQL queries
* **Jupyter Notebook** – Analysis environment

---

## 📂 Project Structure

```text
Vendor-Sales-Analysis/
│
├── Vendor_Sales_Analysis.ipynb
├── inventory.db
└── README.md
```

---

## 🔄 Analysis Workflow

### 1. Import Required Libraries

The project uses Python libraries such as:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import sqlite3
```

These libraries are used for data extraction, cleaning, analysis, and visualization.

---

### 2. Connect to SQLite Database

A connection is established with the SQLite database:

```python
conn = sql.connect("inventory.db")
```

The analysis retrieves data from the `vendor_sales_summary` table.

---

### 3. Load Vendor Sales Data

The vendor summary data is loaded into a Pandas DataFrame using SQL:

```sql
SELECT *
FROM vendor_sales_summary
```

This allows the data to be analyzed using Pandas and Python.

---

### 4. Exploratory Data Analysis

Summary statistics are generated to understand the numerical variables:

```python
df.describe().T
```

This helps examine:

* Count
* Mean
* Standard deviation
* Minimum
* Maximum
* Quartiles

---

### 5. Distribution Analysis

Histograms with KDE curves are used to understand the distribution of numerical variables.

This helps identify:

* Data distribution
* Skewness
* Concentration of values
* Potential unusual observations

---

### 6. Outlier Detection

Boxplots are created for numerical columns to identify potential outliers.

```python
sns.boxplot(y=df[col])
```

This helps detect values that are significantly different from the rest of the dataset.

---

### 7. Data Filtering

Records are filtered to focus on vendors with meaningful sales and profitability:

```sql
WHERE GrossProfit > 0
  AND ProfitMargin > 0
  AND TotalSalesQuantity > 0
```

This removes records that do not meet the required positive sales and profitability conditions.

---

### 8. Vendor and Brand Analysis

Categorical variables such as:

* `VendorName`
* `Description`

are analyzed using count plots.

The analysis focuses on the most frequently occurring vendors and product/brand descriptions.

---

### 9. Correlation Analysis

A correlation matrix is calculated for numerical variables:

```python
correlation_matrix = df[numerical_col].corr()
```

A heatmap is then used to visualize relationships between numerical variables.

This helps identify variables that have stronger positive or negative relationships.

---

## 📊 Brand Performance Analysis

Brand-level performance is calculated using:

* **Total Sales Dollars**
* **Average Profit Margin**

```python
brand_performance = df.groupby('Description').agg({
    'TotalSalesDollars':'sum',
    'ProfitMargin':'mean'
}).reset_index()
```

This provides a summarized view of brand performance.

---

## 🔎 Identifying Target Brands

The project calculates threshold values using percentiles:

* **15th percentile of sales** → Low-sales threshold
* **85th percentile of profit margin** → High-margin threshold

Brands meeting both conditions are identified:

```python
(brand_performance["TotalSalesDollars"] <= low_sales_threshold)
&
(brand_performance["ProfitMargin"] >= high_margin_threshold)
```

These brands represent products with:

> **Low sales but relatively high profit margins**

Such brands can be further investigated to understand why their sales volume is low despite having strong margins.

---

## 📈 Visualizations

The project includes several visualizations:

### Distribution Plots

Used to understand numerical variable distributions.

### Boxplots

Used for detecting potential outliers.

### Count Plots

Used to analyze the frequency of vendors and brands.

### Correlation Heatmap

Used to understand relationships between numerical variables.

### Scatter Plot

Used to compare:

* Total Sales Dollars
* Profit Margin

The scatter plot also highlights the identified target brands.

---

## 💡 Key Business Insight

The analysis focuses on identifying brands that have:

**Low Sales + High Profit Margin**

These brands may represent potential opportunities for further investigation. Possible business questions include:

* Why are these products generating low sales?
* Is customer awareness low?
* Are these products under-promoted?
* Is pricing affecting sales volume?
* Could additional marketing increase sales while maintaining margins?
* Are these products suitable for targeted promotions?

> Note: The notebook identifies these brands based on the defined statistical thresholds. Further business investigation would be required before making recommendations.

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the Project Folder

```bash
cd Vendor-Sales-Analysis
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

SQLite is included with Python, so no separate SQLite installation is normally required.

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Vendor_Sales_Analysis.ipynb
```

### 5. Run the Notebook

Run the cells sequentially to reproduce the analysis and visualizations.

---

## 📌 Skills Demonstrated

This project demonstrates practical experience in:

* Python for Data Analysis
* Pandas
* NumPy
* SQL
* SQLite
* Exploratory Data Analysis (EDA)
* Data Filtering
* Data Aggregation
* GroupBy Analysis
* Statistical Analysis
* Correlation Analysis
* Outlier Detection
* Data Visualization
* Business Insight Generation

---

## 👨‍💻 Author

**Vijay K G**

Aspiring Data Analyst

**Skills:**
`SQL` | `Python` | `Pandas` | `Excel` | `Power BI` | `Data Analysis`

---

## ⭐ Project Purpose

This project was created as part of my journey toward becoming a **Data Analyst**, with a focus on applying Python, SQL, and data visualization techniques to a practical business dataset.
