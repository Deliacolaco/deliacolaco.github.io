---
name: "Retail Margin & Pricing Optimisation"
tools: "Python, SQL, Tableau"
image: "/assets/img/projects/retail-margin-pricing-optimisation.png"
description: Analysed Australian retail pricing and profitability data to uncover discount thresholds driving margin loss and visualised insights in executive Tableau dashboards. 
featured: true
url: /projects/retail-margin-pricing-optimisation/
---
# Retail Margin & Pricing Optimisation, Australian Retail

## Project Overview

A mid-size Australian retailer needed to understand which product categories were driving margin, which were dragging it, and where pricing adjustments would have the highest impact on profitability. This project analyses four years of retail transaction data across four regions (NSW, VIC, QLD, WA) and three product categories (Furniture, Office Supplies, Technology) to answer three core commercial questions.

---

## Business Questions

#### Question 1 — Profitability by Region and Category

Which category is most profitable by region—and does that answer change when you look at **margin % versus total profit**? Is that margin improving or declining over time by quarter, or is a strong overall number hiding a deteriorating trend underneath?

#### Question 2 — Discount Frequency and Margin Impact

Which categories have the highest frequency of discounted transactions by region—and is that discounting resulting in negative profit? At what exact discount threshold does profit turn negative for each category-region combination, producing a specific and defensible discount cap recommendation?

#### Question 3 — Does Discounting Justify Itself?

Does discounting above **30%** actually drive meaningful volume uplift, or is the business sacrificing margin for no commercial benefit? Specifically, if discount caps are introduced, will the sales team's objection that volume will drop hold up against the transaction-level data?

---

## Tools & Approach

#### Python
**Python**
Data cleaning, exploratory analysis, quadrant segmentation, and margin waterfall analysis.
- **Libraries:** Pandas, Matplotlib, Seaborn, SQLAlchemy.

- **[Quadrant Segmentation](/assets/img/projects/figures/quadrant-segmentation.png){:target="_blank" rel="noopener noreferrer"}** — Classified all 12 category-region combinations into four strategic quadrants (Invest, Grow, Fix, Review) using total sales (median threshold) and total profit (zero threshold) as axes.
- **Margin Waterfall** — Built for each product category to separate cost structure problems from discounting problems, showing revenue without discount, discount loss, cost, and actual profit at each stage. View the margin waterfalls for **[Furniture](/assets/img/projects/figures/margin-waterfall-furniture.png){:target="_blank" rel="noopener noreferrer"}**, **[Office Supplies](/assets/img/projects/figures/margin-waterfall-office-supplies.png){:target="_blank" rel="noopener noreferrer"}**, and **[Technology](/assets/img/projects/figures/margin-waterfall-technology.png){:target="_blank" rel="noopener noreferrer"}**. 

#### SQL (SQLite via Jupyter)
- Three layers of discount and margin analysis across all category-region combinations.
- Queries cover margin by quarter, discount frequency, profit threshold analysis, and volume comparison.

#### Tableau Public
- Built two interactive dashboards for different stakeholder groups:
  - **CFO Summary Dashboard** – Executive-level profitability and margin overview.
  - **Commercial Deep Dive Dashboard** – Detailed pricing, discount, and margin analysis.

---

## Dataset

- **Source:** Kaggle Superstore Sales Dataset (synthetic, realistic retail structure).
- Reframed as an Australian retailer by mapping US regions to **NSW, VIC, QLD, WA** and converting USD to AUD (×1.55).
- Created two derived metrics:
  - **Cost = Sales − Profit**
  - **Margin % = (Profit / Sales) × 100**
- Used the **median sales value ($83.56 AUD)** rather than the mean ($353.75 AUD) for sales segmentation due to the dataset's right-skewed distribution.

---

## Key Findings

#### 1. VIC Furniture is the only loss-making segment

- Weighted margin: **-1.70%**
- Average profit per transaction: **-$8.96**
- Total sales: **$255,033**
- Cost accounts for **97%** of actual sales revenue, indicating a structural cost issue beyond discounting.
- Margin waterfall analysis confirms that even eliminating all discounts would only recover $291,791,  
insufficient to make VIC Furniture commercially viable without supplier cost renegotiation.

#### 2. VIC Furniture is the most heavily discounted segment

- **67.84%** of transactions receive a discount.
- Average discount: **29.74%**
- More than double the furniture discount depth in every other region.

#### 3. Profit turns negative between 20% and 30% discount

- Average profit at **20% discount:** **$38.82**
- Average profit at **30% discount:** **-$74.96**
- Most category-region combinations become unprofitable somewhere between **20% and 40%** discount.

#### 4. VIC Office Supplies 80% discount tier is the single biggest margin drain

- Total profit lost: **$47,376**
- Discount frequency: **63.85%**
- Average discount: **25.36%**

#### 5. Discounting above 30% does not drive meaningful volume

Comparing transactions below and above 30% discount across all twelve category-region combinations shows an increase of only **+0.04 units sold per transaction**, providing virtually no commercial justification for heavy discounting.

#### 6. WA and NSW Technology are the strongest performing segments

- **WA Technology:** 19.70% margin
- **NSW Technology:** 13.40% margin
- NSW Technology generates **$75,084** profit from **$415,304** in sales and sits firmly in the high sales, high profit quadrant.

---

## Recommendations

#### 1. Cap VIC Furniture discounts at 20%

Transaction-level analysis shows VIC Furniture remains profitable at a **20%** average discount but becomes loss-making at **30%**. Introducing a 20% cap would improve profitability with negligible volume impact.

#### 2. Renegotiate VIC Furniture supplier costs

With costs consuming **97%** of revenue, supplier costs—not discounting alone—are the primary driver of poor margins. Supplier renegotiation or category restructuring should be prioritised.

#### 3. Eliminate the VIC Office Supplies 80% discount tier

Removing this pricing tier would recover a significant proportion of the **$47,376** currently being lost while maintaining sales volume.

#### 4. Cap VIC Technology discounts at 30%

The category remains healthy overall, but high-discount transactions significantly erode profitability. Removing discounts above 30% is a low-risk improvement.

#### 5. Introduce a default 20% company-wide discount policy

Analysis across every category-region combination shows no meaningful volume benefit above **20%** discount, making this a commercially defensible default pricing policy.

#### 6. Protect high-performing categories

Continue investing in:

- WA Technology
- NSW Technology
- NSW Office Supplies

These segments generate strong margins with relatively low discount dependency and should not be subjected to unnecessary discount pressure.

---

# Dashboards

### CFO Summary Dashboard

High-level executive dashboard covering:

- Total Sales
- Total Profit
- Average Margin
- Profit by Region
- Profit by Category
- Quarterly Profit Trends

<a href="https://public.tableau.com/app/profile/delia.colaco/viz/AustralianRetailMarginDiscountAnalysisCFOSummary/CFOSummary"
   target="_blank"
   rel="noopener noreferrer">
  <strong>View CFO Dashboard</strong>
</a>

---

### Commercial Deep Dive Dashboard

Commercial dashboard covering:

- Discount Frequency
- Margin vs Discount
- Profit Threshold Analysis
- Margin Waterfall
- Discount Loss Treemap
- Sales Volume vs Discount Analysis

<a href="https://public.tableau.com/app/profile/delia.colaco/viz/AustralianRetailMarginDiscountAnalysis/CommercialMarginDiscountAnalysisAustralianRetail?publish=yes"
   target="_blank"
   rel="noopener noreferrer">
  <strong>View Commercial Deep Dive Dashboard</strong>
</a>

---

### Skills Demonstrated

- Python
- Pandas
- SQL
- SQLite
- Tableau
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Commercial Pricing Analysis
- Profitability Analysis
- Dashboard Design
- Data Storytelling
- Business Analytics
