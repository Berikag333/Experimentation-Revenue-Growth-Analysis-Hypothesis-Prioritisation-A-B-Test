# Experimentation-Revenue-Growth-Analysis-Hypothesis-Prioritisation-A-B-Test
Prioritise growth hypotheses (ICE/RICE) and evaluate an A/B test using conversion, revenue, and statistical significance to make a business decision.

# Experimentation & Revenue Growth Analysis: Hypothesis Prioritisation + A/B Test

## Overview
This project supports revenue growth for an e-commerce business by combining structured hypothesis prioritisation with A/B test analysis. The work includes ranking growth ideas using ICE and RICE frameworks, then evaluating an experiment using conversion, revenue, and statistical testing to make a clear decision.

## Data
- hypotheses_us.csv: hypotheses + Reach, Impact, Confidence, Effort
- orders_us.csv: transactionId, visitorId, date, revenue, group
- visits_us.csv: date, group, visits

Note: visitors may appear in both groups; data is cleaned to ensure valid experiment analysis.

## Part 1 — Hypothesis Prioritisation
- Compute ICE scores and rank hypotheses
- Compute RICE scores and rank hypotheses
- Compare ranking differences and explain why priorities change

## Part 2 — A/B Test Analysis
- Cumulative revenue by group
- Cumulative average order value (AOV) by group
- Relative AOV difference (B vs A)
- Daily conversion rates and comparison
- Outlier analysis:
  - orders per user (scatter + 95th/99th percentiles)
  - order revenue (scatter + 95th/99th percentiles)
- Statistical testing (raw and filtered):
  - conversion difference
  - AOV difference
- Decision: stop and declare a winner / stop with no difference / continue

## Deliverables
- Ranked hypothesis table (ICE and RICE)
- KPI charts for revenue, AOV, conversion
- Outlier thresholds and filtered datasets
- Statistical test results with interpretation
- Final recommendation on the experiment outcome

## Objective
Prioritise revenue-growth hypotheses using ICE and RICE frameworks, then analyse an A/B test to determine whether the experimental variant improves performance.

## 1) Data Preparation
Load datasets, convert date fields, validate types, and remove invalid users (e.g., visitors appearing in both A and B groups) to ensure clean experiment groups.

## 2) Hypothesis Prioritisation (ICE vs RICE)
### ICE
Calculate ICE = (Impact × Confidence) / Effort and rank hypotheses.

### RICE
Calculate RICE = (Reach × Impact × Confidence) / Effort and rank hypotheses.

### Interpretation
Compare ICE vs RICE rankings and explain changes (typically driven by Reach).

## 3) A/B Test Monitoring (Cumulative Metrics)
Analyse experiment dynamics using cumulative KPIs:
- cumulative revenue by group
- cumulative average order value (AOV) by group
- relative AOV difference (B vs A)
- conversion rate by day and cumulative conversion

Summarise observations and possible explanations for trends.

## 4) Outlier Detection
Identify abnormal users/orders that may distort results:
- orders per user (95th and 99th percentiles)
- order revenue (95th and 99th percentiles)

Define thresholds and create filtered datasets excluding anomalies.

## 5) Statistical Testing
Test differences between groups using both raw and filtered data:
- conversion rate difference
- average order value difference

Define hypotheses (H0/H1), set alpha, select the test, and interpret p-values.

## 6) Decision
Based on business impact and statistical evidence, choose one outcome:
1) Stop test and declare a leading group  
2) Stop test and conclude no meaningful difference  
3) Continue test (if evidence is insufficient)

## Tech
Python, pandas, matplotlib/plotly, scipy.stats, Jupyter Notebook

## Author
**Erika González**  
MBA | Marketing & Data Analytics  
Focus areas: Experimentation, Growth Analytics, Business Decision-Making
