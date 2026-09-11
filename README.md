# VirtuBox Data Analyst Assessment — Saksham Tyagi

## Q1 — Dataset

1. **Dataset name:** Brazilian E-Commerce Public Dataset by Olist
2. **Source and URL:** Kaggle — https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
3. **Number of rows and columns:** [FILL IN — check your sheet, e.g. ~100k orders across 9 linked CSV files: orders, order_items, products, customers, payments, reviews, sellers, geolocation]
4. **Brief description:** Real e-commerce order data from Olist, a Brazilian marketplace, covering 2016–2018. Includes order status, item details, pricing, freight, customer location, payment type, and review scores across multiple linked tables.
5. **Why I selected this dataset:** It's a large, real-world, multi-table dataset with enough complexity (joins across orders/items/customers/payments/reviews) to support genuine business analysis rather than a single flat file.
6. **Business opportunities/problems it could help investigate:** Customer retention and repeat-purchase behavior, delivery performance and its effect on reviews, regional sales patterns, and payment-method trends.

---

## Q2 — Business Framing

**A. Business problem/opportunity:** Management wants to understand which customers drive the most value and why some customers don't return, to prioritize retention spend.

**B. Analysis questions (3–5):**
1. Which customer segments (by recency, frequency, monetary value) contribute the most revenue?
2. Does delivery delay correlate with lower review scores?
3. Which product categories have the highest repeat-purchase rate?
4. How does order value vary by region/state?
5. Which payment method is associated with highest order value?

**C. Hypotheses:**
1. Customers who order more frequently also leave higher review scores.
2. Late deliveries significantly reduce review scores.

---

## Q3 — Data Cleaning

**What changed and why:** [FILL IN based on your actual notebook — summarize briefly]

| Change | Why was it necessary? | What would happen if you didn't do it? |
|---|---|---|
| Removed duplicate order IDs | Duplicate rows would inflate order counts and revenue totals | Revenue/insight numbers would be overstated |
| Converted date columns (order_purchase_timestamp, delivery dates) to datetime | Needed to calculate delivery time and time-based trends | Date math and trend analysis would be impossible/incorrect |
| Handled missing review comments/scores | Missing values would break aggregation and average-score calculations | Averages and counts would be skewed or throw errors |

---

## Q4 — Key Insights

| Insight | Evidence | Why relevant | Business impact | Recommendation |
|---|---|---|---|---|
| [FILL IN — e.g. Top 20% of customers by RFM score generate X% of revenue] | [your RFM output numbers] | Shows where retention effort should focus | Retaining this segment protects majority of revenue | Launch loyalty program for top RFM tier |
| [FILL IN — 2nd insight] | | | | |
| [FILL IN — 3rd insight] | | | | |
| [FILL IN — 4th insight] | | | | |
| [FILL IN — 5th insight] | | | | |

*(Pull these directly from your existing RFM segment breakdown — you likely already have 5 of these from your project.)*

---

## Q5 — Unexpected Result

1. **Initial expectation:** [e.g. Expected high-value customers to also order most frequently]
2. **What the data showed:** [e.g. A segment with high monetary value but low frequency — one-time big spenders]
3. **Why this likely happened:** [your reasoning]
4. **Additional analysis performed:** [e.g. cross-checked against product category — found large one-off purchases like furniture]
5. **Conclusion:** [state clearly, and note if data can't fully explain it — that's fine to say]

---

## Q6 — Data Quality & Limitations

1. **Issue:** Dataset covers only 2016–2018 (Brazil) — not current or globally representative.
   **Effect:** Findings may not generalize to other markets or time periods.
   **Handled by:** Framing all conclusions as specific to this dataset/timeframe.

2. **Issue:** Some review comments are missing/blank.
   **Effect:** Sentiment-based analysis is limited to available reviews only.
   **Effect handled by:** Excluded blank reviews from text-based analysis rather than imputing.

3. **Issue:** No customer demographic data (age, income) beyond location.
   **Effect:** Can't segment by demographics, only behavior/geography.
   **Handled by:** Limited segmentation to RFM + geographic variables.

**A. Two limitations:** (1) Single-country, single-platform dataset — not generalizable. (2) No repeat-customer identifier beyond customer_unique_id, so lifetime value estimates are approximate.

**B. One conclusion that CANNOT be made:** We cannot conclude anything about current (2026) customer behavior, since the data ends in 2018.

---

## Q7 — Recommendations

1. **What:** Launch a loyalty/retention program targeting the top RFM-tier customers.
   **Supporting insight:** Q4 insight #1.
   **Who acts:** Marketing/CRM team.
   **Outcome:** Higher repeat-purchase rate, protected revenue base.
   **Measure:** Repeat purchase rate of targeted segment over next 2 quarters.

2. **What:** [FILL IN]
3. **What:** [FILL IN]

---

## Q10 — How I Used AI

1. **AI tools used:** Claude
2. **What I used it for:** Structuring the assessment write-up (README format), organizing insights into the required table formats, and clarifying ambiguous instructions in the assessment brief.
3. **Example where AI helped:** Drafting the README structure and question-by-question framework so I could focus on filling in actual analysis results.
4. **Example where I verified/corrected AI output:** [FILL IN — e.g. "Verified all RFM numbers, dataset row/column counts, and insight evidence against my own notebook output before submitting."]

---

## Methodology

Analysis performed using Python (Pandas, NumPy, Matplotlib/Seaborn) in [Jupyter/Colab]. RFM segmentation applied on the Olist dataset by joining orders, order_items, customers, and payments tables. Processed data and full code available in this repository under `/code`.
