# Retail Analytics Dashboard

An interactive BI dashboard analysing retail transaction data — built to support sales, demographic, and regional decision-making for a retail business.

## Live dashboards

| Dashboard | Link | Covers |
|---|---|---|
| Sales Overview | [View on Tableau Public](https://public.tableau.com/app/profile/sneha.kamanahalli.shivakumar/viz/retail-bi-dashboard/SalesOverview) | Revenue by category, payment method, revenue by US state |
| Customer Segmentation | [View on Tableau Public](https://public.tableau.com/app/profile/sneha.kamanahalli.shivakumar/viz/retail-customer-segmentation/CustomerSegmentation) | Spend by age and gender, category preference by gender, seasonal patterns |
| Loyalty & Engagement | [View on Tableau Public](https://public.tableau.com/app/profile/sneha.kamanahalli.shivakumar/viz/retail-loyalty-engagement/LoyaltyEngagement) | Subscription status, purchase frequency, average order value by subscription |

![Sales Overview Dashboard](images/dashboard-overview.png)

## Overview

A retail business needs analytics that answer questions for different teams: which categories and regions drive revenue (sales), how spending varies across customer groups (marketing), and how loyal the customer base is (retention). This project splits those into three focused dashboards instead of one crowded view.

## Data

[Kaggle — Customer Shopping Latest Trends Dataset](https://www.kaggle.com/datasets/bhadramohit/customer-shopping-latest-trends-dataset). 3,900 retail transactions with product category, purchase amount, demographics, payment method, subscription status, purchase frequency, and US state location.

The original brief asked for revenue trends over time, but this dataset has no date field, so that isn't buildable from it. The dashboards focus instead on what the data does support well: category, location, demographics, payment behaviour, and loyalty.

## Key findings

**Sales Overview**
- Clothing leads revenue at $104,264 — more than Accessories ($74,200) and Footwear ($36,093) combined
- Spend is fairly even across all 6 payment methods, with Credit Card narrowly leading at ~$38K
- Spend is concentrated in a cluster of central/western US states

**Customer Segmentation**
- Spend is fairly consistent across age brackets, with 50-59 leading narrowly
- Male customers outspend female customers in every product category
- Seasonal spend is nearly flat year-round ($56K-$60K each season)

**Loyalty & Engagement**
- Only about 27% of customers are subscribed (1,053 of 3,900)
- Purchase frequency is evenly spread across all 7 cadences, from weekly to annual
- Average order value is almost identical for subscribers and non-subscribers (~$60 vs ~$59) — subscription affects frequency, not basket size

## How it was built

- Built in Tableau Public (Power BI Desktop isn't available on macOS)
- The dataset was already clean, so prep focused on age binning (10-year groups) and assigning a geographic role to the location field
- Split into three dashboards so each one answers a distinct question without overcrowding

## Next steps

- Add a time dimension if transaction-date data becomes available, to support trend analysis
- Build a drill-down from the location map into category breakdown per state
- Look into the gender spending gap further
