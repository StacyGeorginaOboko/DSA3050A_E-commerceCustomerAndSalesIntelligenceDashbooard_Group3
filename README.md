# DSA3050A_E-commerceCustomerAndSalesIntelligenceDashbooard_Group3

## Group Members
| Name | Student ID | Role |
|------|-----------|------|
| [Patricia Kiarie] | [669781] | Business Lead / Docs Coordinator |
| [Stacy Oboko] | [670722] | Power Query Specialist A |
| [Jessica Kimani] | [668701] | Power Query Specialist B |
| [Monica Njoki] | [670176] | Data Modeller / DAX Lead |
| [Paul Mbuvi] | [669984] | Dashboard Designer A |
| [Mellisa Magani] | [669782] | Dashboard Designer B / Insights Lead |

---

## 1. Business Problem

Olist is a Brazilian e-commerce marketplace that connects small and medium-sized sellers with customers across Brazil. Like most multi-seller marketplaces, Olist's leadership needs visibility into which product categories and regions drive revenue and profit, how delivery performance affects customer satisfaction, and where returns, delays, or low review scores put future sales at risk.

**Problem statement:** Olist's management currently lacks a consolidated, interactive view of sales, customer, delivery, and review performance across categories and Brazilian states — making it difficult to identify underperforming regions, prioritize high-value customer segments, or link delivery/service issues to revenue risk.

## 2. Target Organization / Industry

- **Organization:** Olist (Brazilian e-commerce marketplace)
- **Industry:** Retail / E-commerce marketplace, operating as a SaaS marketplace layer for third-party sellers
- **Our role:** Business Intelligence Consulting Team engaged to build an executive Power BI dashboard for decision-making

## 3. Dataset Source

- **Name:** Brazilian E-Commerce Public Dataset by Olist
- **URL:** https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
- **Time period covered:** 2016–2018
- **License/type:** Real, anonymized transactional data released publicly by Olist (not synthetic or fabricated)

## 4. Dataset Description

The dataset is split across 9 related CSV files (relational structure, joined by order_id / customer_id / product_id / seller_id):

| File | Approx. Rows | Description |
|------|-------------|--------------|
| olist_orders_dataset.csv | ~99,000 | Order status and timestamps (purchase, approval, delivery) |
| olist_order_items_dataset.csv | ~112,000 | Line-item level product, price, freight per order |
| olist_order_payments_dataset.csv | ~104,000 | Payment type, installments, value |
| olist_order_reviews_dataset.csv | ~99,000 | Review score and text per order |
| olist_customers_dataset.csv | ~99,000 | Customer ID, city, state, zip prefix |
| olist_sellers_dataset.csv | ~3,000 | Seller ID, city, state, zip prefix |
| olist_products_dataset.csv | ~33,000 | Product category, weight, dimensions |
| olist_geolocation_dataset.csv | ~1,000,000 | Zip prefix to lat/long mapping |
| product_category_name_translation.csv | 71 | Portuguese-to-English category names |

**Total rows (combined):** well over 50,000 (order_items alone exceeds this on its own)
**Total columns (combined across tables):** 40+ across all 9 files, well above the 15-column minimum
**Related tables:** 9, joined on shared keys — satisfies the star-schema/multi-table requirement

**Known data quality issues to clean in Power Query (Week 2):**
- Missing values in delivery timestamps and review comments
- Duplicate rows in the geolocation table (multiple lat/long entries per zip prefix)
- Near-duplicate/multilingual review text
- Product category names in Portuguese requiring a translation join
- Some orders with mismatched or orphaned foreign keys across tables
- Inconsistent data types on ID and date columns when first loaded

## 5. Key Business Questions

1. Which product categories generate the highest revenue and profit margin, and which are underperforming?
2. Which Brazilian states/regions produce the most revenue, and which are underperforming relative to their customer base?
3. How does delivery performance (on-time vs. late) vary by state and seller, and does it correlate with review scores?
4. What payment methods and installment patterns are most common, and how do they relate to order value?
5. Which customer segments (by order frequency, order value, or region) represent the highest lifetime value?
6. What trends are visible in order volume and revenue over the 2016–2018 period?
7. What risks (late delivery clusters, low-review sellers, high-return categories) should management prioritize addressing?

---

## 6. Power Query Transformations
_To be completed in Week 2._

## 7. Data Model
_To be completed in Week 3._

## 8. DAX Measures
_To be completed in Week 3._

## 9. Dashboard Pages
_To be completed in Week 3–4._

## 10. Key Insights
_To be completed in Week 4._

## 11. Recommendations
_To be completed in Week 4._

## 12. Contribution Summary
_To be completed throughout — update per member as commits are made._
