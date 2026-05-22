---
name: Gym Customer Segmentation
tools: Python, Pandas, Scikit-learn, Matplotlib, Clustering
image: /assets/img/projects/gym-customer-segmentation.png
description: Segmented 2,000 gym members into 3 distinct customer profiles using K-Means clustering in Python, delivering targeted marketing strategies for each segment.
url: /projects/gym-customer-segmentation/
---

# Gym Customer Segmentation

This project used Python clustering techniques to segment 2,000 gym members into meaningful customer groups. The goal was to help a gym chain better understand its customer base and design more targeted marketing strategies.

Tools used: Python, Pandas, Scikit-learn, Matplotlib — K-Means and Agglomerative Clustering

## Business Problem

A gym chain lacked visibility into customer differences, making it difficult to personalise offers or allocate marketing spend effectively. The goal was to identify actionable segments to guide campaign strategy.

## Method

After cleaning and scaling the data, I used the Elbow Method and Silhouette Analysis to determine the optimal number of clusters. I then applied K-Means clustering as the primary method and Agglomerative clustering for validation. Each segment was profiled across demographic and behavioural features to support business interpretation.

## Key Findings

The analysis identified three customer segments:

1. Youthful, Economically-Conscious Individuals — younger members with price sensitivity; highest churn risk
2. Wealthy Metropolitan Executives — high income, low visit frequency; receptive to premium add-ons
3. Knowledgeable Suburban Adults — consistent, family-oriented members; strongest retention base

## Business Recommendations

Each segment was matched with targeted marketing actions:

- Segment 1: Digital-first, budget membership tiers and referral incentives to improve retention
- Segment 2: Premium wellness packages and off-peak executive services to increase visit frequency
- Segment 3: Family and community membership bundles to deepen loyalty

## Project Files

- [View full GitHub repository](https://github.com/Deliacolaco/data-analytics-projects/tree/main/gym-customer-segmentation)
- [View project report](https://github.com/Deliacolaco/data-analytics-projects/blob/main/gym-customer-segmentation/report/gym_customer_segmentation_report.pdf)
- [View Python notebook](https://github.com/Deliacolaco/data-analytics-projects/blob/main/gym-customer-segmentation/code/gym_customer_segmentation.ipynb)

## Note

Dataset not included due to university assessment restrictions. All analysis and outputs are original work.