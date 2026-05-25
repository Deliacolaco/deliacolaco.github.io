---
name: Student Retention Analytics, Macquarie University
tools: Qlik Sense, Python, Pandas, Scikit-learn, XGBoost, Dashboarding
image: /assets/img/projects/student-retention-analytics-mqu.png
description: Built an executive Qlik Sense dashboard and contributed to predictive modelling to analyse student retention, progression, equity outcomes, and attrition risk across Macquarie University.
url: /projects/student-retention-analytics-mqu/
---

# Student Retention Analytics, Macquarie University

Macquarie University · BUSA8031 – Business Analytics Project · 2025

## Overview

This group project was developed for Macquarie University's Business Intelligence and Reporting team. Using de-identified enrolment and retention data from 2020–2025, the project analysed student progression patterns, attrition risk factors, and institutional retention trends.

The final solution included two Qlik Sense dashboards for different user groups and a machine learning model to predict students at risk of not continuing.

My main contribution was designing and building Dashboard 2: Institutional Retention & Progress Insights, created for university executive stakeholders.

## Business Problem

Macquarie University needed a clearer way to monitor student retention across faculties, cohorts, equity groups, and academic years.

Course Directors needed visibility into unit-level patterns linked to drop-off, while senior leaders needed an institutional view of retention, completion, equity outcomes, and academic performance.

## Dataset

The project used two de-identified Macquarie University datasets:

- Enrolment Data: 284,818 unit-level records
- Retention Data: 52,434 course-level records
- Period covered: 2020–2025

Key variables included gender, citizenship, equity status, grade, unit status, WAM, credit points, faculty, course, study mode, academic year, and retention outcome.

Raw datasets are not included due to university data governance restrictions.

## Tools Used

- Qlik Sense
- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib

## Method

The team cleaned and merged enrolment and retention datasets using a shared course admission key. A derived retention outcome variable was created to classify students as retained, completed, or not retained.

Dashboard 1 focused on Course Directors, supporting unit-level exploration of retention, completion, and academic performance.

Dashboard 2 focused on University Executives, showing institutional retention trends, faculty performance, equity group outcomes, WAM movement, and strategic KPIs.

The predictive modelling component used a time-aware approach, where historical data was used to predict future retention risk.

## My Contribution

My main contribution was designing and building Dashboard 2 in Qlik Sense.

This dashboard focused on:

- Institutional retention trends
- Faculty-level performance comparison
- Equity and non-equity student outcomes
- Completion and progression patterns
- Average WAM movement across years
- Executive-level monitoring for strategic decision-making

I also contributed to report discussion, strategic recommendations, key takeaways, and supported other team members across the project.

## Key Findings

- Retention improved steadily from 2020 to 2024 before plateauing in 2025.
- Business and Science & Engineering outperformed other faculties.
- Larger faculties showed stronger retention and completion outcomes.
- Equity student retention improved from approximately 68% to 74%, narrowing the gap with non-equity students.
- Average WAM rose consistently before stabilising in 2025.
- XGBoost achieved a PR-AUC of 0.465 on the 2024 test set.
- Targeting the top 20% highest-risk students would capture 66% of future attrition cases.

## Recommendations

For Course Directors:

- Use early outreach during weeks 3–4 for students showing academic friction.
- Review high-risk core units and unit sequencing pressure points.
- Track cohort-level changes semester by semester.

For University Executives:

- Use predictive risk scoring to identify high-risk students earlier.
- Compare faculty-level retention patterns to allocate support resources.
- Continue targeted equity support to narrow retention gaps.

## Project Files

- [View Report PDF](https://github.com/Deliacolaco/data-analytics-projects/blob/main/student-retention-analytics-mqu/student-retention-analytics.pdf)
- [View GitHub Project Folder](https://github.com/Deliacolaco/data-analytics-projects/tree/main/student-retention-analytics-mqu)
- [View Dashboard](https://23cen6dozz61syg.ap.qlikcloud.com/sense/app/9b261911-3aea-4951-99d3-3e603903742e/overview)

## Note

This was a group project. The raw datasets are not publicly shared because they contain real de-identified university data.