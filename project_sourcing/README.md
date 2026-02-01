# Supplier Risk & Kraljic Portfolio Analysis

## Executive Summary
This project applies a **data-driven supplier risk assessment** using a **Multi-Criteria Decision-Making (MCDM)** model and the **Kraljic Portfolio Matrix**.  The objective is to identify sourcing concentration, supply risk exposure, and profit impact across products, enabling procurement teams to prioritize actions that improve resilience while controlling cost.

The analysis shows that a **small set of Strategic products accounts for the majority of total spend**, indicating high dependency risk and the need for proactive supplier management.

---

## Business Problem
Traditional supplier evaluations tend to focus heavily on cost, which can mask other important factors such as supply disruption risk, single-source and regional concentration, high-profit products with fragile supply bases, excess effort spent on low-impact items. The business requires a **structured and repeatable framework** to rank suppliers and products objectively, to balance cost efficiency with supply resilience, and to allocate procurement effort where it delivers the most value.

---

## Methodology

### 1. Data Preparation
- Supplier records defined at **Product × Region** level
- Metrics included:
  - Cost
  - Lead time and variability
  - Order volume
  - Supply risk
  - Profit impact
  - Environmental impact
  - Single-source risk

### 2. Normalization
- All continuous variables normalized to a **0–1 scale**
- Volume normalized to handle skewed distributions
- Binary risks (e.g., single-source) **scaled**, not subtracted

### 3. Weighted Scoring (MCDM)
A composite score was calculated using:

   **Final_Weighted_Score = Σ (Normalized_Metric × Weight)**

   Weights reflect relative business importance across cost, reliability, profit impact, and sustainability.

### 4. Product-Level Aggregation
- Supplier scores aggregated to the **product level**
- Weighted averages used for multi-region products
- Logical rules applied for single-region and global suppliers

### 5. Kraljic Segmentation
Products were positioned on:
- **Supply Risk Index (X-axis)**
- **Profit Impact Index (Y-axis)**

Each product was classified into:
- Strategic
- Leverage
- Bottleneck
- Non-Critical

---

## Skills Demonstrated
- Supply chain and procurement analytics
- Multi-criteria decision modeling (MCDM)
- Data normalization and aggregation
- Advanced Excel formulas (SUMPRODUCT, IFS, conditional logic)
- Kraljic Portfolio Matrix application
- Translating analysis into business decisions

---

## Results

### Kraljic Matrix Analysis

The Kraljic Matrix segments products by Supply Risk and Profit Impact using weighted average indices at the product level.
- **Strategic** items represent 83% of total spend, with both high average risk and high profit impact (0.61 / 0.61). This indicates strong dependence on a small set of critical products, making supplier stability and long-term partnerships essential.

- **Bottleneck** items account for 11% of spend and exhibit moderate-to-high supply risk (0.47) with lower profit impact, suggesting the need for risk mitigation and supply assurance rather than cost optimization.

- **Leverage**items show high profit impact (0.54) but low supply risk and minimal spend (1%), indicating underutilized opportunities for negotiation and consolidation.

- **Non-critical** items contribute 5% of spend with low risk and low profit impact, making them suitable for transactional purchasing and process efficiency improvements.

<table border="0">
  <tr>
    <td width="800">
      <img width="800" alt="Kraljic Matrix Graph" src="https://github.com/user-attachments/assets/b75f6cdc-c29e-41d9-becc-28a28526ac14" />
    </td>
    <td valign="middle">

| Quadrant | # Items | Avg Risk | Avg Profit | % Spend |
| :--- | ---: | ---: | ---: | ---: |
| **Strategic** | 10 | 0.61 | 0.61 | 83% |
| **Leverage** | 8 | 0.26 | 0.54 | 1% |
| **Bottleneck** | 8 | 0.47 | 0.30 | 11% |
| **Non-Critical** | 10 | 0.27 | 0.17 | 5% |

  </tr>
</table>

### Key Insights
- Strategic products dominate spend, creating concentration risk
- Leverage products present negotiation and cost-reduction opportunities
- Bottleneck items have low spend but high operational sensitivity
- Non-critical items should be simplified and automated

---

## Recommendations

### Strategic
- Develop long-term supplier partnerships
- Introduce dual sourcing where feasible
- Actively monitor risk indicators

### Leverage
- Increase competitive bidding
- Consolidate volume to improve pricing power

### Bottleneck
- Build safety stock or buffers
- Identify alternative suppliers proactively

### Non-Critical
- Standardize specifications
- Reduce supplier count and automate purchasing

---

## Next Steps / Future Enhancements
- Sensitivity analysis on scoring weights
- Scenario simulations (supplier failure, demand spikes)
- Integration with BI tools (Power BI / Tableau)
- ESG and geopolitical risk overlays
- Time-series monitoring of supplier risk



