# MERX Demand Forecasting: Research Deliverables

## Objective  
To build a demand forecasting system for MERX Inventory Management System (IMS), we first:  
1. **Identified a robust feature set** tailored to our use cases  
2. **Researched publicly available datasets** for model prototyping until live customer data becomes available  

---

## 1. Strategic Feature List for Forecasting Model

A comprehensivelist of predictors based on best practices in inventory forecasting across retail, manufacturing, and distribution sectors:

### A. Internal Time-Series & Inventory Features
- Historical Sales (daily/weekly/monthly)
- Inventory On-Hand
- Lead Time (supplier/production/delivery)
- Reorder Point, Safety Stock Levels
- Purchase Orders and Inbound Shipments

### B. Seasonality & Time-based Features
- Day of Week, Month, Quarter
- Holidays, Weekends, Festivals
- Fiscal Year/Quarter Flags
- Rolling averages, Moving trends (7, 30, 90-day windows)

### C. Product & Channel Metadata
- Product Category, Unit Price, Gross Margin
- SKU ID, Product Hierarchies
- Warehouse Location, Region, Sales Channel (B2B, B2C, eCommerce)

### D. External and Market Signals
- Weather Data (temperature, rain)
- Public Events or Disruptions
- Google Trends / Sentiment Indicators
- COVID or Global Disruption Flags

### E. Promotions and Pricing
- Active Promotions (discounts, flash sales)
- Competitor Price Tracking (if feasible)
- Price Changes and Elasticity Metrics

### F. Operational KPIs
- Stockouts / Backorders (binary or count)
- Inventory Turnover Ratio
- Fulfillment Delay Incidents
- Return Rates / Damaged Goods Percent

### G. Advanced / AI Signals (Future Enhancements)
- Anomaly detection from IoT logs
- Forecast confidence intervals
- Vendor reliability score
- Simulation outcomes (Digital Twin integration)

---

##  2. Public Datasets for Initial Model Development

A list of datasets ideal for prototyping demand forecasting models across MERX’s target markets:

### a. [Retail Store Inventory Forecasting (Kaggle)](https://www.kaggle.com/datasets/anirudhchauhan/retail-store-inventory-forecasting-dataset)
- Synthetic dataset with store, product, daily sales, promotions, weather
- Good for starting time-series models with lag features

### b. [StarsWei Extended Dataset (GitHub)](https://github.com/StarsWei/Retail-Store-Inventory-and-Demand-Forecasting)
- Same as above but with added COVID-19 impact flag
- Allows exploration of disruption-aware forecasting

### c. [FreshRetailNet-50K (ArXiv)](https://arxiv.org/abs/2505.16319)
- Realistic hourly perishable goods data across 50,000 SKUs
- Includes stockouts, promotions, weather, product freshness
- Ideal for experimenting with inventory-censored demand models

### d. [Google BigQuery Retail Demo Dataset](https://colab.research.google.com/github/GoogleCloudPlatform/vertex-ai-samples/blob/main/notebooks/official/workbench/demand_forecasting/forecasting-retail-demand.ipynb)
- Sample retail dataset with multi-product sales over time
- Used in Vertex AI forecasting pipelines

### e. [FMCG Forecasting Dataset (PapersWithCode)](https://paperswithcode.com/dataset/predictive-analytics-for-retail-inventory)
- Annotated data for predictive analytics across retail SKUs
- Includes seasonality, pricing, promotions



