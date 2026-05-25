---
name: Student Retention Analytics, Macquarie University
tools: Qlik Sense, Python, Pandas, Scikit-learn, XGBoost, Dashboarding
image: /assets/img/projects/student-retention-analytics-mqu.png
description: Built an executive Qlik Sense dashboard and contributed to predictive modelling to analyse student retention, progression, equity outcomes, and attrition risk across Macquarie University.
url: /projects/student-retention-analytics-mqu/
---

# Student Retention Analytics

**Macquarie University · BUSA8031 – Business Analytics Project · 2025**

Group project. I designed and built **Dashboard 2: Institutional Retention & Progress Insights**, the dashboard used by University Executives to monitor retention, equity outcomes, and faculty performance at an institutional level.

---

## Overview

This project was built for Macquarie University's Business Intelligence and Reporting (BIR) team. They had de-identified enrolment and retention data going back to 2020, but no connected view that pulled demographics, academic performance, and retention outcomes together.

We built two Qlik Sense dashboards for different stakeholder groups, plus a machine learning model that flags students most at risk of not continuing.

---

## Business Problem

Two different groups at the university needed visibility into student retention, but at completely different levels.

Course Directors needed to see which specific units were driving high fail rates, withdrawals, and drop-off, and which student cohorts were most at risk within their programs.

University Executives needed an institution-wide view of retention trends, faculty performance, equity outcomes, and academic progress to guide policy, resourcing, and student support strategy.

The data existed, but it was spread across systems. Trends often got noticed too late to act on.

---

## My Contribution — Dashboard 2

I built Dashboard 2 in Qlik Sense for University Executives. The goal was to give senior leaders one place they could go for retention insight, ready to use in strategy meetings, funding reviews, and policy conversations.

The dashboard covers:

- Institutional retention trends from 2020–2025

- Faculty-level retention comparison

- Equity vs non-equity student outcomes

- Completion and continuation patterns

- Average WAM movement by year

- Filters by faculty, academic year, attendance mode, and student type

### What executives could see for the first time

Two things stood out once the dashboard was in front of executives: the **2025 retention plateau** after four years of steady growth, and the **equity gap closing from 68% to 74%**. Both were findings that previously sat buried in long annual reports.

### Design choices and why

| Design choice | Reason |

|---|---|

| Faculty-level comparison, not cohort-level | Executives plan by faculty, not by cohort. Cohort-level views are more useful for Course Directors, so they sit in Dashboard 1. |

| Equity vs non-equity split as a core view | Equity is one of the university's strategic priorities. Putting the gap front and centre means it gets discussed, not skimmed past. |

| Filters by attendance mode and student type | Lets executives check whether trends hold up across delivery modes and across domestic vs international students. Headline numbers often hide differences between these groups. |

| WAM trend shown alongside retention | If retention drops while WAM holds steady, the issue is engagement, not academic difficulty. The two need different responses. |

---

## Dataset

Two de-identified Macquarie University datasets covering 2020–2025:

- **Enrolment Data:** 284,818 unit-level records across 43 variables

- **Retention Data:** 52,434 course-level records across 13 variables

Key variables included:

- Gender

- Citizenship

- Equity status

- Grade

- Unit status

- WAM

- Credit points

- Faculty

- Course

- Study mode

- Academic year

- Retention outcome

Both datasets were merged on a shared course admission key.

> Raw datasets are not included due to university data governance restrictions. All analysis and outputs are original work.

---

## Tools Used

**My contribution:**

- Qlik Sense

**Team-wide data preparation and modelling:**

- Python

- Pandas

- NumPy

- Scikit-learn

- XGBoost

- Matplotlib

---

## Method

Two decisions shaped most of the work.

The team cleaned up the retention outcome first. The raw data had about a dozen continuation codes, which were collapsed into three categories: **Retained**, **Completed**, and **Not Retained**. This kept the outcome consistent across every chart and the predictive model.

For the model, a time-aware split was used to avoid leakage. Features only used data up to year *t*, and the target was retention in year *t+1*. Training ran on 2020–2022, validation on 2023, and 2024 was held back as a true test set. This is how the model would actually run in production.

For Dashboard 2, I built each chart against a specific executive use case. Every filter and KPI had to answer the question: **what would a senior leader do with this?** If the answer was not clear, the chart did not make it in.

---

## Key Findings

**71.4% retention rate · 63.2 average WAM · 5.6× model uplift · 66% attrition captured in top 20%**

### From Dashboard 2

- Retention improved steadily from 2020 to 2024 and then plateaued in 2025. Existing support strategies may have reached their limit.

- Business and Science & Engineering consistently outperformed other faculties; Arts was more volatile year-on-year.

- Larger faculties had stronger retention and completion outcomes, likely because of bigger peer networks and more shared administrative resources.

- Equity student retention improved from 68% to 74%, narrowing but not closing the gap with non-equity students.

- WAM rose steadily before stabilising in 2025. Since grades held up, the retention issues are more likely about engagement and support than academic difficulty.

### From the team's predictive model

- XGBoost reached a PR-AUC of 0.465 on the 2024 test set, a 5.6× uplift over the random baseline of 0.083.

- Flagging the top 20% of highest-risk students would capture around 66% of future attrition cases.

- The strongest risk drivers were repeated fails and withdrawals, low credits-earned-to-attempted ratios, and concentration in large 2000-level core units.

---

## Limitations & What I Would Do Differently

- **Model precision has an operational cost.** PR-AUC of 0.465 is a strong uplift, but a meaningful share of flagged students will not actually drop out. Any rollout would need to balance outreach capacity against false positives.

- **The 2025 plateau is a question, not an answer.** Dashboard 2 shows the plateau clearly, but it cannot explain it. The next step would be pairing it with surveys, exit interviews, or course feedback.

- **Equity is a single flag in the data.** That hides differences between equity sub-groups, which can mean very different things. A future version could break this down further if the underlying data allows.

- **The two dashboards are separate.** An executive who spots a weak faculty in Dashboard 2 has to switch to Dashboard 1 to see the unit-level detail. A linked design would close that gap.

---

## Recommendations

### For Course Directors

- Reach out early, around weeks 3–4, to students with multiple fails or withdrawals.

- Review unit sequencing, especially high-enrolment 2000-level core units.

- Use Dashboard 1 filters to check cohort-level retention each semester.

### For University Executives

- Use the predictive model to flag at-risk students early, before they drop off.

- Use Dashboard 2 faculty comparisons to direct support resources where outcomes are weakest.

- Keep investing in equity support programs to close the remaining retention gap.

- Investigate what is behind the 2025 plateau before it turns into a sustained decline.

---

## Project Files

- [View Report PDF](https://github.com/Deliacolaco/data-analytics-projects/blob/main/student-retention-analytics-mqu/student-retention-analytics.pdf){:target="_blank"}
- [View GitHub Project Folder](https://github.com/Deliacolaco/data-analytics-projects/tree/main/student-retention-analytics-mqu){:target="_blank"}
- [View Dashboard](https://23cen6dozz61syg.ap.qlikcloud.com/sense/app/9b261911-3aea-4951-99d3-3e603903742e/overview){:target="_blank"}

## Note

This was a group project. The raw datasets are not publicly shared because they contain real de-identified university data.