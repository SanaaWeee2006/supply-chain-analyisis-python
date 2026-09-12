  # Supply Chain Analysis 

---

## Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#data-cleaning-preparation">Data Cleaning & Preparation</a>
- <a href="#analysis">Analysis</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>

---

<h2><a class="anchor" id="overview"></a>Overview</h2>
This project analyzes the delivery operations of a global e-commerce company managing end-to-end order fulfillment across multiple regions. The analysis covers 172,765 orders spanning January 2015 through January 2018, focusing on identifying root causes of chronic late deliveries, quantifying their financial impact, and establishing a data-driven framework for improvement.

<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

The company operates a global e-commerce platform selling products across categories including sporting goods, fitness equipment, outdoor gear, footwear, and apparel across multiple international regions. Actual shipping times frequently deviate from scheduled delivery windows, creating eroded customer trust, reduced order profitability, and an inability to make reliable commitments to buyers at point of purchase.

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>
dataset link - https://www.kaggle.com/datasets/saicharankomati/dataco-supply-chain-dataset

---
<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- SQL (Common Table Expressions (CTEs), Joins, Filtering)
- Python (Pandas, Matplotlib, Seaborn, Scipy)
- Github

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
vendor-performance-analysis/
│
├── README.md
├── .gitignore
├── Vendor Performance Report.pdf
│
├── ingestion_db.py
│   └── Ingests CSV files into the database
│
├── get_vendor_summary.py
│   └── Generates a vendor summary table for analysis
│
├── exploratory_data_analysis.ipynb
│   └── Exploratory data analysis and visualizations
│
└── vendor_performance_analysis.ipynb
    └── Vendor performance analysis
```

---
<h2><a class="anchor" id="data-cleaning-preparation"></a>Data Cleaning & Preparation</h2>

- Removed transactions with:
  - Gross Profit <= 0
  - Profit Margin <= 0
  - Sales Quantity = 0
- Created summary tables with vendor-level metrics
- Converted data types, handles outliers, merged lookup tables

---
<h2><a class="anchor" id="exploratory-data-analysis"></a>Exploratory Data Analysis (EDA)</h2>

**Negative or Zero Values Detected:**
- Gross Profit: Min -52,00.78 (loss making sales)
- Profit Margin: Min -inf (sales at zero or below cost)
- Unsold Inventory: Indicating slow-moving stock

**Outliers Identified:**
- High Freight Costs (upto 257K)
- Large Purchase/Actual Prices

**Correlation Analysis:**
- Weak between Purchases Price & Profit
- Strong between Purchase Qty & Sales Qty
- Negative between Profit Margin & Sales Price

---
<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

1. **Brands for Promotions:** 198 brands with low sales but high profit margins
2. **Top Vendors:** Top 10 Vendors contribute approximately 65% of purchases. **This possess risk of over-reliance**
3. **Bulk Purchasing Impact:** Vendors buying in bulk get the lowest Unit purchase price, hence reducing cost per unit.
4. **Inventory Turnover:** $2.71M worth of unsold inventory
5. **Vendor Profitability:**
       - High Profit Vendors: Mean Margin = 31.17%
       - Low Profit vendors: Mean Margin = 41.55%
6. **Hypotheseis Testing:** Statistically significant difference in profit margins. **This highlights the need to diversify vendor strategies.**

---
<h2><a class="anchor" id="Power-BI-dashboard"></a>Dashboard</h2>

dashboard link: https://github.com/SanaaWeee2006/vendor-performance-analysis-sql-python/blob/main/vendor_performance_analysis_dashboard.pbix <br>
image - https://github.com/SanaaWeee2006/vendor-performance-analysis-sql-python/blob/main/dashboard.png

---
<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone the repository:
```bash
git clone https://github.com/SanaaWeee2006/vendor-performance-analysis-sql-python.git
```
2. Load the CSVs and ingest into database:
```bash
python ingestion_db.py
```
3. Create vendor summary table:
```bash
python get_vendor_summary.py
```
5. Open and run notebooks:
   - 'exploratory_data_analysis.ipynb'
   - 'vendor_performance_analysis.ipynb'


---
<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- Diversify vendor base to reduce risk
- Optimize bulk order strategies
- Reprice slow-moving, high-margin brands
- clear unsold inventory strategically

---
<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

Author: Sana Perween

Email: [per.sana.21@gmail.com] <br>
LinkedIn: [www.linkedin.com/in/30sana] 
