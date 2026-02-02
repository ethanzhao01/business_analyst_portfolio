# Supplier Risk & Kraljic Portfolio Analysis

## Executive Summary
This project implements a **data-driven supplier risk assessment** leveraging a **Multi-Criteria Decision-Making (MCDM)** model and the **Kraljic Portfolio Matrix**. The objective is to quantify sourcing concentration, supply risk exposure, and profit impact across the product catalog.

**Key Finding:** A core group of **Strategic products accounts for 93% of total spend**, signaling a critical dependency that requires immediate proactive supplier management and resilience planning.

<img width="1238" height="609" alt="9a7f0fd8-3500-4ec8-9e31-5f8fedbe36db" src="https://github.com/user-attachments/assets/6d3f8006-7d59-4d07-a1d3-a0f313a68acf" />

<br>

## Business Problem
Standard procurement evaluations often over-index on cost, creating "blind spots" in the supply chain. This analysis addresses hidden disruption risks, such as single-source dependencies, regional concentration, and high-profit products supported by fragile supply bases. The goal is to transition from reactive purchasing to a **structured, repeatable framework** that objectively balances cost efficiency with supply resilience.

<br>

## Methodology

**1. Data Preparation & Normalization**
Supplier records were analyzed at the **Product × Region** level, incorporating financials (Cost, Profit Impact), logistics (Lead Time, Variability), and risk factors (Single-Source, ESG). To ensure comparability across disparate metrics (e.g., days vs. dollars), all continuous variables were normalized to a **0–1 scale**, while skewed distributions like volume were log-transformed.

**2. Weighted Scoring (MCDM)**
We calculated a composite risk and profit score using a weighted sum model. Weights were assigned based on relative business importance across cost, reliability, profit impact, and sustainability.

$$\text{Weighted Score} = \sum (\text{Normalized Metric}_i \times \text{Weight}_i)$$

**3. Kraljic Segmentation**
Final scores were aggregated to the product level using weighted averages. Products were then mapped onto the Kraljic Matrix based on their **Supply Risk Index** (X-axis) and **Profit Impact Index** (Y-axis), classifying them into Strategic, Leverage, Bottleneck, or Non-Critical categories.

<br>

## Results

The matrix below visualizes the portfolio segmentation. **Strategic items** (top-right) represent the overwhelming majority of spend and value, while **Bottleneck items** expose the organization to moderate risk despite negligible financial impact.

<br>

<table border="0" width="100%">
  <tr>
    <td width="60%" valign="top">
      <img width="519" height="274" alt="image" src="https://github.com/user-attachments/assets/bfb19bd6-d738-4f2a-94e5-e62135663ea5" />
    </td>
    <td width="40%" valign="middle" style="padding-left: 20px;">

**Table 1: Portfolio Segmentation Summary**

| Quadrant&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | # Items | Avg Profit | Avg Risk | % Spend |
| :--- | ---: | ---: | ---: | ---: |
| **Strategic** | 16 | 0.70 | 0.57 | 93.3% |
| **Leverage** | 2 | 0.64 | 0.26 | 2.9% |
| **Bottleneck** | 2 | 0.46 | 0.39 | 0.5% |
| **Non-Critical** | 16 | 0.34 | 0.26 | 3.3% |

<br>
<p align="center"><em>Data updated: Feb 2026</em></p>

  </tr>
</table>

### Key Insights
* **Critical Dependency:** Strategic products now account for **93.3% of spend** across 16 items. Any disruption here would have a massive financial impact, making these relationships the top priority.
* **Low Leverage Potential:** Only 2.9% of spend sits in the "Leverage" quadrant, suggesting that opportunities for purely price-based negotiation are limited.
* **Operational Noise:** Bottleneck items account for less than **0.5% of spend** but still carry elevated risk scores (0.39). These should be secured with safety stock to prevent disproportionate operational headaches.
* **Tail Spend:** Non-critical items make up a significant volume count (16 items) but only 3.3% of spend, making them ideal candidates for automated purchasing.

<br>

## Recommendations

Based on the quadrant analysis, the following sourcing strategies are recommended to optimize the portfolio:

| Quadrant | Primary Strategy | Action Plan |
| :--- | :--- | :--- |
| **Strategic** | **Partnership** | Develop long-term alliances, introduce dual sourcing to mitigate dependency, and actively monitor risk indicators. |
| **Leverage** | **Exploit** | Increase competitive bidding and consolidate volumes to maximize pricing power. |
| **Bottleneck** | **Secure Supply** | Build safety stock buffers and proactively identify alternative suppliers to reduce operational fragility. |
| **Non-Critical** | **Efficiency** | Standardize specifications, reduce supplier count, and automate purchasing to cut administrative costs. |


<br>

## Skills & Tools Demonstrated
This project demonstrates proficiency in **Supply Chain Analytics**, **MCDM Modeling**, and **Data Aggregation**. Technical execution involved advanced Excel logic (SUMPRODUCT, conditional arrays) and data normalization techniques to translate raw procurement data into actionable business intelligence.

<br>

## Future Enhancements
Next steps include performing sensitivity analysis on scoring weights, simulating supplier failure scenarios, and integrating time-series monitoring to track risk exposure changes over time.



