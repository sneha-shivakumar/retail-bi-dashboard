# Retail Analytics Dashboard

A three-part interactive BI project analysing retail transaction data — built to support sales, demographic, and loyalty decision-making for a retail business.

## Live dashboards

| Dashboard | Link | Covers |
|---|---|---|
| **Sales Overview** | [View on Tableau Public →](https://public.tableau.com/app/profile/sneha.kamanahalli.shivakumar/viz/retail-bi-dashboard/SalesOverview) | Revenue by category, payment method breakdown, revenue by US state |
| **Customer Segmentation** | [View on Tableau Public →](https://public.tableau.com/app/profile/sneha.kamanahalli.shivakumar/viz/retail-customer-segmentation/CustomerSegmentation) | Spend by age group and gender, category preference by gender, seasonal purchasing patterns |
| **Loyalty & Engagement** | [View on Tableau Public →](https://public.tableau.com/app/profile/sneha.kamanahalli.shivakumar/viz/retail-loyalty-engagement/LoyaltyEngagement) | Subscription status breakdown, purchase frequency distribution, AOV by subscription status |

![Sales Overview Dashboard](images/dashboard-overview.png)

## The problem

A retail business needs a single analytics suite that answers questions across three different stakeholder groups: which product categories and regions drive revenue (sales), how spending varies across customer demographics (marketing), and how engaged and loyal the customer base actually is (retention). This project splits those concerns into three focused, purpose-built dashboards rather than one overcrowded view.

## The data

**Source:** [Kaggle — Customer Shopping Latest Trends Dataset](https://www.kaggle.com/datasets/bhadramohit/customer-shopping-latest-trends-dataset)
3,900 retail transactions, covering product category, purchase amount, customer demographics, payment method, subscription status, purchase frequency, and US state-level location data.

**A scoping note:** the original brief for this project called for revenue trend analysis over time. This dataset has no date field, so that metric isn't reliably buildable from it — rather than force a misleading time series, the dashboards focus on the segmentations the data actually supports well: category, location, demographics, payment behaviour, and loyalty signals.

## Key findings

**Sales Overview**
- Clothing leads revenue at $104,264 — more than Accessories ($74,200) and Footwear ($36,093) combined
- Spend is evenly spread across all 6 payment methods (Credit Card leads narrowly at ~$38K)
- Spend is geographically concentrated in a cluster of central/western US states

**Customer Segmentation**
- Spend is fairly consistent across age brackets, with 50-59 leading narrowly
- Male customers out-spend female customers in every single product category
- Seasonal spend is nearly flat year-round (56K-60K each season) — no strong seasonality in this dataset

**Loyalty & Engagement**
- Only ~27% of customers are subscribed (1,053 of 3,900) — a clear retention opportunity
- Purchase frequency is evenly distributed across all 7 cadences (Weekly through Annually) — no dominant buying pattern
- Average order value is nearly identical for subscribers and non-subscribers (~$60 vs ~$59) — subscription drives frequency, not basket size

## How it was built

- **Tool:** Tableau Public (chosen over Power BI as this was built on macOS, where Power BI Desktop isn't available)
- **Data prep:** the dataset was already clean (no missing values or duplicates); work focused on age binning (10-year groups) and geographic role assignment for the Location field
- **Structure:** split into three dashboards rather than one, so each serves a distinct stakeholder question without overcrowding

## What I'd do next

- Add a time dimension if transaction-date data becomes available, to support real trend analysis
- Build a drill-down from the location map into category breakdown per state
- Investigate the gender spending gap further with a targeted marketing angle
