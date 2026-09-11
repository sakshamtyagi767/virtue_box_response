
##  Executive Management Presentation (5–7 Slides)

### Slide 1: Business Problem & Strategic Opportunity
* **Title:** Unlocking E-Commerce Growth: Customer Retention & Delivery Excellence
* **Context:** Evaluation of 100,000+ orders across 2016–2018 to discover revenue expansion levers.
* **Core Challenge:** While top-line sales have reached $13.59M, customer retention is below 4%, and geographic logistics bottlenecks threaten customer loyalty.
* **Objective:** Present data-driven strategies to improve customer lifetime value (LTV) and optimize regional fulfillment SLAs.

---

### Slide 2: Data Foundation & Methodology
* **Dataset Scope:** 100k+ orders, 95k+ customers, 7 relational tables covering transactions, payments, products, and reviews.
* **ETL Pipeline:** 
  * Timestamp standardization & missing data normalization.
  * Order-level payment & review deduplication to safeguard financial metric accuracy.
  * Customer-level behavioral aggregation using `customer_unique_id`.
* **Analytical Frameworks:** Executive KPI tracking, RFM customer segmentation, Logistics SLA lead-time modeling.

---

### Slide 3: Executive Key Findings
* **Total Marketplace Revenue:** **$13.59 Million** across **98,666 orders**.
* **Average Order Value (AOV):** **$137.75** (peaks when multi-month installment options are used).
* **On-Time Delivery SLA:** **92.1%** overall marketplace on-time rate.
* **Average Customer Rating:** **4.08 / 5.0** stars.
* **Concentration Risk:** Top 3 product categories account for >25% of total platform sales.

---

### Slide 4: Deep Dive — Retention (RFM) & Regional Logistics
* **Customer Retention Gap:**
  * 96.2% of buyers purchase only once.
  * **23.9% of historical high-spenders are currently "At-Risk"** (no orders in 180+ days).
* **Regional Logistics Friction:**
  * Southeast (SP, PR) enjoy fast fulfillment: **8.3 days average delivery**, delay rate <6%.
  * North & Northeast (RR, AP, AM) suffer severe delays: **20 to 28 days average delivery**, delay rate up to 18.5%.
  * Delivery delays directly correlate with a 65% increase in 1-star reviews.

---

### Slide 5: Strategic Recommendations
1. **Decentralized Logistics Fulfillment:** Partner with regional 3PL hubs in Northern Brazil to reduce transit times from 24 days to under 12 days.
2. **Automated RFM Win-Back Campaigns:** Trigger customized promotions offering free freight to the 23,800+ "At-Risk" customers to capture $1.2M+ in reactivation sales.
3. **Financing & Basket Size Optimization:** Promote zero-interest installment payment plans for high-value categories ($150+) to drive higher Average Order Value.

---

### Slide 6: Expected Business Impact & Success Metrics
| Strategic Initiative | Expected Business Outcome | Primary Metric to Track |
| :--- | :--- | :--- |
| **Regional 3PL Hubs** | Delivery lead times cut by 40–50% in remote states | Regional Average Delivery Days & On-Time SLA % |
| **RFM Win-Back Workflows** | 10–12% reactivation of dormant high-value customers | Cohort Repeat Purchase Rate & Reactivation GMV |
| **Installment Financing UX** | 8–10% lift in basket size on high-ticket categories | Average Order Value (AOV) & Credit Installment Adoption |

---

### Slide 7: Limitations & Future Analytical Roadmap
* **Limitations of Current Dataset:**
  * Lacks product cost (COGS) and marketing ad spend (CAC); analysis focuses on Gross Merchandise Value rather than Net Margin.
  * Customer tracking spans an 18-month window; long-term multi-year cohorts require continuous telemetry.
* **Next Steps for Data Team:**
  * Ingest real-time ad channel conversion data to calculate precise Customer Acquisition Cost (CAC) vs. LTV.
  * Implement predictive machine learning models to forecast shipping delays before carrier dispatch.
