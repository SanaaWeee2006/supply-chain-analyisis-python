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

- Python (numpy, Pandas, Matplotlib, Seaborn)
- Data Cleaning
- Data Preparation
- Data Transformation
- Data Visualization
---

<h2><a class="anchor" id="data-cleaning-preparation"></a>Data Cleaning & Preparation</h2>

- Removed columns which are empty, identical, or have only one value 
- Filtered Cancelled orders from Delivery Status as they are no relevant for delivery time analysis
- Hnadled missing values.
- Added order processing time columns for identifying delayed orders.

---
<h2><a class="anchor" id="analysis">Analysis</a> 
  
- Late Delivery Rate at 54.71% - More than half of all orders arrive late. This is not an edge-case problem- it is the default experience for the majority of customers.
- $2.1M Profit at Risk - Orders that experienced delays collectively generated $2.1M in profit that is under constant pressure from further operational deterioration.
- 90th Percentile Delay = 3 Days - Even the most extreme cases are contained within 3 days of lateness, suggesting the problem is systemic and process-driven rather than catastrophic.
- Order-level profitability was classified into three tiers based on Order Profit Per Order. While 80.7% of orders are profitable, the 18.7% loss-making share represents a meaningful drag that is disproportionately concentrated among delayed shipments.
- The delay distribution shows that 31.0% of all orders arrive exactly 1 day late the single largest cohort. Combined, orders delayed by 1-4 days account for 54.7% of all order volume, directly mapping to the overall.
- First Class Shipping Mode causes 100% delay rate. Second Class causes 79.8%. Standard Class causes 39.8%. Same Day: 0%. The mode assignment logic is the most impactful single variable to fix.
- Central Africa leads at 58.7% but all regions cluster between 55-59%. This rules out a localized logistics failure and confirms a company-wide systemic issue.
- No segment receives preferential service. All customers - Consumer, Corporate, Home Office experience the same broken delivery promise.
- Health & Beauty (56.9%) and Pet Shop (56.6%) Lead by Department - These departments marginally outpace others in delay rate, warranting an inventory and carrier audit for these product categories.
- August and September are the highest months at 55.4%, with December close behind. These reflect mid-year promotions and Q4 holiday surge overwhelming fulfilment capacity. July represents a notable low-point (~53.75%), confirming seasonal variation is plannable.

---
<h2><a class="anchor" id="strategic-recommendations"></a>Strategic Recommendations</h2>

- Immediately Audit First Class & Second-Class Shipping Capacity
- Deploy the Predictive Alert System
- Resolve Payment Processing Bottlenecks
- Develop Seasonal Surge Capacity Plans
- Default to Standard Class for Eligible Orders
- Investigate High-Delay Departments in Africa

- This analysis has surfaced a clear and urgent picture: a global e-commerce operation where the majority of orders (54.71%) fail to meet their promised delivery windows, costing $2.1M in at-risk profit and undermining customer trust at scale.

---
<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

Author: Sana Perween

Email: [per.sana.21@gmail.com] <br>
LinkedIn: [www.linkedin.com/in/30sana] 
