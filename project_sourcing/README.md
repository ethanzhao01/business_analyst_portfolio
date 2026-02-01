# Supplier Risk & Kraljic Portfolio Analysis

## Executive Summary
This project implements a **data-driven supplier risk assessment** leveraging a **Multi-Criteria Decision-Making (MCDM)** model and the **Kraljic Portfolio Matrix**. The objective is to quantify sourcing concentration, supply risk exposure, and profit impact across the product catalog.

**Key Finding:** A small cluster of **Strategic products accounts for 83% of total spend**, signaling a high dependency risk that requires immediate proactive supplier management and resilience planning.

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

The matrix below visualizes the portfolio segmentation. **Strategic items** (top-right) represent the bulk of the risk and value, while **Bottleneck items** (bottom-right) expose the organization to high operational risk despite low financial impact.

<table border="0" width="100%">
  <tr>
    <td width="70%" valign="top">
      <img src="https://github.com/user-attachments/assets/b75f6cdc-c29e-41d9-becc-28a28526ac14" width="100%" alt="Kraljic Matrix Graph" />
    </td>
    <td width="30%" valign="middle">

| Quadrant | # Items | Avg Risk | Avg Profit | % Spend |
| :--- | ---: | ---: | ---: | ---: |
| **Strategic** | 10 | 0.61 | 0.61 | 83% |
| **Leverage** | 8 | 0.26 | 0.54 | 1% |
| **Bottleneck** | 8 | 0.47 | 0.30 | 11% |
| **Non-Critical** | 10 | 0.27 | 0.17 | 5% |

<br>
<em>Table: Portfolio Distribution by Kraljic Quadrant </em>
    </td>
  </tr>
</table>

### Key Insights
* **Concentration Risk:** Strategic products dominate the budget (83% of spend). The organization is highly dependent on a small set of critical suppliers.
* **Operational Vulnerability:** Bottleneck items have moderate-to-high risk (0.47) but low profit impact. These items often cause production stoppages disproportionate to their cost.
* **Missed Opportunities:** Leverage items show high profit impact but low risk, yet currently account for only 1% of spend, suggesting under-utilization of negotiation power.

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



