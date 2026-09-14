---
name: "Retail Margin & Pricing Optimisation"
tools: "Python, SQL, Tableau"
image: "/assets/img/projects/retail-margin-pricing-optimisation.png"
description: Analysed Australian retail pricing and profitability data to uncover discount thresholds driving margin loss and visualised insights in executive Tableau dashboards. 
featured: true
url: /projects/retail-margin-pricing-optimisation/
---
# Retail Margin & Pricing Optimisation, Australian Retail

The analysis found one loss-making segment where high costs—not discounting—were the underlying problem, and identified a single pricing tier responsible for **&#36;47,376 in avoidable margin loss**. It also showed that discounts above **30%** add almost no sales volume, supporting a recommended **20% company-wide discount cap**.

[Read the full technical breakdown on GitHub →](https://github.com/Deliacolaco/data-analytics-projects/blob/main/retail-margin-pricing-optimisation/README.md){:target="_blank" rel="noopener noreferrer"}

## Project Overview

A mid-size Australian retailer needed to understand which product categories were driving margin, which were dragging it, and where pricing changes would have the greatest impact on profitability. I analysed four years of retail transactions across NSW, VIC, QLD and WA, covering Furniture, Office Supplies and Technology, to understand profitability over time, when discounts start destroying profit, and whether deeper discounts actually increase sales volume.

---

## Tools & Approach

Used Python and SQL to analyse four years of sales data, compare profitability across regions and categories, trace how discounts and costs affect margin, and test whether deeper discounts increase sales volume. I then built two interactive Tableau dashboards: a high-level summary for a CFO and a detailed pricing view for a commercial manager.

The supporting charts show which parts of the business need investment or attention and separate cost problems from discounting problems. View the supporting analysis for **[Furniture](/assets/img/projects/figures/margin-waterfall-furniture.png){:target="_blank" rel="noopener noreferrer"}**, **[Office Supplies](/assets/img/projects/figures/margin-waterfall-office-supplies.png){:target="_blank" rel="noopener noreferrer"}**, and **[Technology](/assets/img/projects/figures/margin-waterfall-technology.png){:target="_blank" rel="noopener noreferrer"}**.

---

## Dataset

- **Source:** Kaggle Superstore Sales Dataset (synthetic, realistic retail structure).
- Reframed as an Australian retailer by mapping US regions to **NSW, VIC, QLD, WA** and converting USD to AUD (×1.55).
- Created two derived metrics:
  - **Cost = Sales − Profit**
  - **Margin % = (Profit / Sales) × 100**
- I used the middle value instead of the average because a few very large orders were skewing the numbers.

---

## Key Findings

#### 1. VIC Furniture has a cost problem, not just a discount problem

This segment was quietly losing money on every sale—a **-1.70% margin**—while costs consumed **97% of revenue**. It was also the most heavily discounted segment: **67.84% of transactions** were discounted, at an average depth of **29.74%**, more than double every other Furniture region.

#### 2. Profit disappears beyond modest discounts, with one tier causing the biggest loss

Profit fell sharply as discounts moved from **20% to 30%**, with average profit falling from **&#36;38.82 to -&#36;74.96**. The worst single pricing tier was the **80% discount on VIC Office Supplies**, responsible for **&#36;47,376 in lost profit**.

#### 3. Heavy discounting adds almost no sales volume

Orders discounted above **30%** sold only **0.04 more units per transaction** than orders below that level, giving little commercial reason to sacrifice margin.

#### 4. Technology is the strongest area of the business

WA Technology delivered a 19.70% margin, while NSW Technology generated **&#36;75,084 profit** from **&#36;415,304** in sales.

---

## Recommendations

#### 1. Cap VIC Furniture discounts at 20%

Introduce a clear cap to prevent deeper discounts from turning otherwise profitable sales into losses.

#### 2. Renegotiate VIC Furniture supplier costs

Supplier costs—not discounting alone—are the primary driver of poor margins. Supplier renegotiation or category restructuring should be prioritised.

#### 3. Eliminate the VIC Office Supplies 80% discount tier

Remove this extreme pricing tier while maintaining sales volume through more sustainable offers.

#### 4. Cap VIC Technology discounts at 30%

The category remains healthy overall, but high-discount transactions significantly erode profitability. Removing discounts above 30% is a low-risk improvement.

#### 5. Introduce a default 20% company-wide discount policy

Make a **20% cap** the default policy, with exceptions requiring commercial approval.

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
- Discount Loss Treemap
- Sales Volume vs Discount Analysis

<a href="https://public.tableau.com/app/profile/delia.colaco/viz/AustralianRetailMarginDiscountAnalysis/CommercialMarginDiscountAnalysisAustralianRetail?publish=yes"
   target="_blank"
   rel="noopener noreferrer">
  <strong>View Commercial Deep Dive Dashboard</strong>
</a>

---

[View GitHub Project Folder](https://github.com/Deliacolaco/data-analytics-projects/tree/main/retail-margin-pricing-optimisation){:target="_blank"}
