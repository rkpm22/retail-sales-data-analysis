# 📦 Retail Sales Analytics & Customer Segmentation
## 🚀 Project Goal
This project analyzes historical retail transaction data to:

Understand sales patterns across time, geography, and products

Identify customer segments based on purchasing behavior

Perform churn analysis to flag inactive customers

Generate actionable marketing strategies


## 1. 📊 Data Overview
Dataset contains retail transactions including:

Invoice No, Stock Code, Description

Quantity, Unit Price

Invoice Date, Customer ID, Country

Objective: derive business insights from sales and customer activity


## 2. 🧹 Data Cleaning
Key steps taken:

Removed rows with missing Description using a reference lookup table of most frequent descriptions per StockCode

Filtered out rows with Quantity <= 0 or UnitPrice <= 0

Dropped helper columns after imputation

Verified data consistency across all relevant columns

## 3. ⚙️ Feature Engineering
Added new columns to aid in analysis:

TotalRevenue = Quantity × UnitPrice

Extracted Year and Month from InvoiceDate

Created RFM_Score for each customer

Defined churn using time since last purchase

## 4. 📈 Exploratory Data Analysis (EDA)
📅 Monthly Sales
2011 analyzed (2010 incomplete)

Clear seasonality observed: sales spike in Nov and Dec

🌍 Country-Wise Sales
UK is dominant, but other countries contribute significantly

Bar + percentage plots used for visual clarity

📦 Product-Wise Sales
Top 5 products contribute a major portion of revenue

Revenue by StockCode and percentage charts used

## 5. 🎯 RFM Customer Segmentation
RFM Metrics:
Recency: Days since last purchase

Frequency: Number of purchases

Monetary: Total amount spent

### Scoring & Segmenting

| Segment              | RFM Score Range | Strategy                         |
|----------------------|-----------------|----------------------------------|
| Champion             | 9–12            | Reward & retain                  |
| Loyal                | 7–8             | Upsell & engage                  |
| Potential Loyalist   | 5–6             | Convert to loyal                 |
| Needs Attention      | 3–4             | Re-engage                        |
| At Risk              | 0–2             | Win back with personalized offers |

## 6. 🔁 Churn Analysis
Churn defined as no purchase in 90+ days

Churned customers flagged

Histogram plotted showing churn threshold and customer distribution

## 🧠 Tools Used
Python (Pandas, Matplotlib)

Jupyter Notebook

RFM Scoring

Custom Segmentation Logic

Data Visualization
