# Vendor Performance Analysis | Python • SQL • Pandas • Visualization

## Project Overview

**Vendor Performance Analysis** is a data analytics project focused on evaluating vendor and brand-level sales performance, profitability, and operational metrics.

The project combines **SQL, Python, Pandas, SQLite, Matplotlib, and Seaborn** to transform vendor sales data into meaningful business insights.

The analysis focuses on understanding vendor contribution, sales performance, gross profit, profit margins, product performance, and identifying brands with **lower sales but stronger profit margins**.

---

## Business Objective

The primary objective of this project is to evaluate vendor performance and identify opportunities for improving sales and profitability.

The analysis aims to answer key business questions such as:

* Which vendors generate the highest sales?
* Which vendors contribute the most gross profit?
* Which vendors have the highest profit margins?
* Which brands/products perform strongly?
* Which brands have low sales but high profit margins?
* What relationships exist between sales, quantity, and profitability?
* Which vendors or brands may require further business attention?

---

## Dataset

The analysis is based on vendor sales data containing summarized information about vendors, products, sales quantities, sales values, and profitability.

### Key Analytical Attributes

* Vendor
* Product / Brand
* Total Sales Quantity
* Total Sales Dollars
* Gross Profit
* Profit Margin
* Product-related performance metrics

The dataset is analyzed at both **vendor and brand/product levels** to understand overall business performance.

---

## Tools & Technologies

| Tool                 | Purpose                           |
| -------------------- | --------------------------------- |
| **Python**           | Data analysis and processing      |
| **Pandas**           | Data manipulation and aggregation |
| **NumPy**            | Numerical analysis                |
| **SQLite**           | SQL-based data querying           |
| **Matplotlib**       | Data visualization                |
| **Seaborn**          | Statistical visualization         |
| **Jupyter Notebook** | Analysis environment              |

---

## Project Workflow

```text
Vendor Sales Data
        │
        ▼
     SQLite
   SQL Analysis
        │
        ▼
      Python
        │
        ├── Data Exploration
        ├── Data Cleaning
        ├── Aggregation
        ├── Statistical Analysis
        └── Business Analysis
        │
        ▼
   Visualization
        │
        ├── Distribution Analysis
        ├── Outlier Analysis
        ├── Correlation Analysis
        └── Vendor / Brand Analysis
        │
        ▼
 Business Insights
```

---

## SQL Analysis

SQLite is used to query and analyze the vendor sales data.

The analysis includes:

### Vendor Performance

* Vendor-level sales analysis
* Sales quantity analysis
* Gross profit analysis
* Profit margin analysis

### Brand Performance

* Brand-level sales analysis
* Average profit margin
* Identification of high-margin brands

### Business Filtering

The analysis focuses on records with positive:

* Sales
* Gross Profit
* Profit Margin
* Sales Quantity

This provides a cleaner basis for evaluating profitable vendor and brand performance.

---

## Python Analysis

Python and Pandas are used for exploratory data analysis and business analysis.

### Exploratory Data Analysis

The project examines:

* Dataset structure
* Numerical statistics
* Data distributions
* Vendor and brand frequency
* Relationships between numerical variables

### Statistical Analysis

Descriptive statistics are used to understand:

* Mean
* Standard deviation
* Minimum and maximum values
* Quartiles
* Distribution patterns

---

## Outlier Analysis

Boxplots are used to identify potential outliers across important numerical variables.

This helps identify vendors, products, or transactions with unusually high or low values.

Potential outliers can then be investigated further to determine whether they represent:

* Exceptional business performance
* Large-volume vendors
* Unusual transactions
* Data quality issues

---

## Correlation Analysis

A correlation matrix is used to examine relationships between numerical business metrics.

The analysis helps understand relationships between measures such as:

* Sales
* Sales Quantity
* Gross Profit
* Profit Margin

A heatmap is used to make these relationships easier to interpret.

---

## Vendor & Brand Performance

Vendor and brand performance is evaluated using aggregated metrics such as:

* **Total Sales Dollars**
* **Total Sales Quantity**
* **Gross Profit**
* **Average Profit Margin**

This allows the analysis to distinguish between high-volume vendors, highly profitable vendors, and vendors with stronger margins.

---

## Low-Sales / High-Margin Analysis

One of the key analytical components of the project is identifying brands with:

> **Relatively low sales but relatively high profit margins**

Percentile-based thresholds are used to identify these brands.

The analysis compares:

* Total Sales Dollars
* Profit Margin

Brands falling below the defined sales threshold while exceeding the defined profit-margin threshold are selected for further investigation.

This helps identify potential opportunities where improving sales volume could potentially increase overall profitability.

---

## Visualizations

The project uses several visualization techniques:

### Distribution Plots

Used to understand the distribution of numerical business metrics.

### Boxplots

Used to identify potential outliers.

### Count Plots

Used to understand vendor and brand frequency.

### Correlation Heatmap

Used to identify relationships between numerical variables.

### Scatter Plot

Used to analyze the relationship between:

**Total Sales Dollars vs. Profit Margin**

The scatter plot also highlights brands that meet the low-sales/high-margin criteria.

---

## Business Insights

The analysis provides a framework for understanding vendor and brand performance from multiple perspectives.

Potential business questions generated from the analysis include:

* Should high-margin but low-sales brands receive additional marketing?
* Are high-sales vendors also generating strong profit margins?
* Which vendors contribute significantly to overall profitability?
* Are certain vendors heavily dependent on sales volume?
* Which brands have potential for growth?
* Are there vendors with strong sales but relatively weak margins?

These insights can support further investigation into **pricing, promotions, inventory strategy, vendor relationships, and product positioning**.

---

## Key Skills Demonstrated

### Python

* Pandas
* NumPy
* Data Cleaning
* Data Transformation
* GroupBy Analysis
* Aggregation
* Exploratory Data Analysis

### SQL

* SQLite
* SQL Queries
* Filtering
* Aggregation
* `GROUP BY`
* Business Metrics

### Data Analysis

* Descriptive Statistics
* Percentile Analysis
* Outlier Detection
* Correlation Analysis
* Vendor Performance Analysis
* Brand Performance Analysis

### Data Visualization

* Matplotlib
* Seaborn
* Distribution Plots
* Boxplots
* Heatmaps
* Scatter Plots

---

## Project Structure

```text
Vendor-Performance-Analysis/
│
├── Vendor_Performance_Analysis.ipynb
├── inventory.db
└── README.md
```

| File                                | Description                                       |
| ----------------------------------- | ------------------------------------------------- |
| `Vendor_Performance_Analysis.ipynb` | Complete Python-based vendor performance analysis |
| `inventory.db`                      | SQLite database containing the vendor sales data  |
| `README.md`                         | Project documentation                             |

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Open the Notebook

```bash
jupyter notebook
```

Open:

```text
Vendor_Performance_Analysis.ipynb
```

### 4. Run the Notebook

Run the notebook cells sequentially to reproduce the analysis and visualizations.

---

## Key Takeaway

This project demonstrates an end-to-end **vendor performance analytics workflow**, combining SQL-based data extraction with Python-based exploratory analysis, statistical analysis, visualization, and business insight generation.

The analysis demonstrates how sales and profitability data can be used to identify **high-performing vendors, profitable brands, performance gaps, and potential growth opportunities**.

---

## Author

**Vijay K G**

Aspiring Data Analyst

**Skills:**
`SQL` • `Python` • `Pandas` • `Excel` • `Power BI` • `Data Analysis`


<img width="443" height="527" alt="Screenshot 2026-10-05 140339" src="https://github.com/user-attachments/assets/a1ab1f51-7650-4e38-854e-b07979bd7129" />
<img width="293" height="492" alt="Screenshot 2026-10-05 140412" src="https://github.com/user-attachments/assets/03560db6-5d5d-472a-b136-d04282861674" />
<img width="291" height="509" alt="Screenshot 2026-10-05 140423" src="https://github.com/user-attachments/assets/ffdd8e00-1bc5-4fff-8479-35f876cebc60" />
<img width="278" height="501" alt="Screenshot 2026-10-05 140434" src="https://github.com/user-attachments/assets/4c07d531-e61d-4c34-a147-64c4790cb730" />
<img width="290" height="422" alt="Screenshot 2026-10-05 140456" src="https://github.com/user-attachments/assets/7e84084e-4d0c-42a2-a59f-281f7664f1d5" />
<img width="290" height="452" alt="Screenshot 2026-10-05 140507" src="https://github.com/user-attachments/assets/054fe21f-4375-487d-8ac4-4d680e697ac7" />
<img width="291" height="403" alt="Screenshot 2026-10-05 140518" src="https://github.com/user-attachments/assets/f6677cb1-c85c-4ec2-ba05-83b365907974" />
<img width="286" height="361" alt="Screenshot 2026-10-05 140537" src="https://github.com/user-attachments/assets/daac9332-de1b-488b-aac8-7bcd0c32985e" />
<img width="283" height="425" alt="Screenshot 2026-10-05 140545" src="https://github.com/user-attachments/assets/ab1e6352-d3ef-414c-ac17-1c49c38f1bf9" />










