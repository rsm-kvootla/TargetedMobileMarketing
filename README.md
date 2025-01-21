# TargetedMobileMarketing
Analysis to segment targeted customers and study the profitability of a targeted vs non-targeted mobile marketing approach
## Overview

This project focuses on analyzing Tuango’s mobile marketing campaigns to enhance the effectiveness of targeted push notifications. Tuango is a leading "deal-of-the-day" platform in China, and its business model revolves around promoting discounted deals to a large customer base. This analysis aims to identify key factors influencing customer responses and improve the profitability of mobile marketing strategies.

---

## Objectives

1. **Understand Campaign Effectiveness:** Evaluate the success of Tuango's customized push notifications in driving customer purchases.
2. **Optimize Targeting:** Identify key features that influence customer responses to promotional messages.
3. **Compare Strategies:** Analyze the profitability of targeted marketing against a non-targeted approach.

---

## Project Components

### Jupyter Notebook
The notebook includes:
- **Data Cleaning and Preprocessing:** Handling missing values and preparing datasets for analysis.
- **Exploratory Data Analysis (EDA):** Visualizing key trends and patterns in customer behavior.
- **Modeling:**
  - Logistic Regression: Predict customer response (`buyer`).
  - Linear Regression: Analyze order size and purchasing behavior.
- **Profitability Analysis:** Quantifying the impact of targeted versus non-targeted campaigns.

---

## Data Description

The project works with three datasets:
1. **Pre-Test Dataset:** Customers who received a customized push message.
2. **Post-Test Dataset:** Same customers’ behavior after receiving the message.
3. **Rollout Dataset:** A control group of customers who did not receive the push message.

### Key Variables:
- **`userid`:** Unique customer identifier.
- **`buyer`:** Indicates whether the customer purchased the Karaoke deal.
- **`ordersize`:** Number of Karaoke sessions purchased.
- **Recency, Frequency, and Monetary (RFM) Variables:**
  - `recency`: Days since the last purchase.
  - `frequency`: Number of deals purchased in the past year.
  - `monetary`: Average amount spent per order.
- **Demographics:**
  - `age`: Customer age.
  - `gender`: Customer gender.
  - `music`: Purchase history in the music category.

---
### Key Results:
1. A logistic regression was conducted to identify the key features to determine a target custmer segment:

Prediction Plots for Logistic Regression
![image](https://github.com/user-attachments/assets/539a6155-985f-485f-9de7-bd386cb41a3a)

Permutation Importance Plot
![image](https://github.com/user-attachments/assets/00437661-c50e-4f8d-90ac-347193b2ffe7)

2. A linear regression was conducted to ascertain ordersize based on existing buyer group, however the results were not significant.

3. Based on the output of the logistic regression, and the associated costs of email marketing and potential revenue, a breakeven response rate probability threshold was established to determine which potential customers to send mobile marketing messages to. A profitability analysis and Return on Marketing Investment analysis was conducted to ascertain the benefits of the campaign.
![image](https://github.com/user-attachments/assets/232f2d45-1889-437b-84c7-34e349fefc32)
![image](https://github.com/user-attachments/assets/2b2b29bd-68f2-47a7-a627-b62cb84c27a8)

This was also validated against the actual performance data.


