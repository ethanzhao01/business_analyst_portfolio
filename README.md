# Supply Chain Analytics & Optimization Portfolio

## Executive Summary
This portfolio showcases **end-to-end supply chain decision-making**, spanning **risk assessment, demand planning, and network optimization**. Across three projects, I apply analytical and optimization techniques to move from **diagnosing risk**, to **anticipating demand**, to **optimizing structural decisions** under real-world constraints.

The common theme is **decision support**: translating complex data and trade-offs into **clear, actionable insights** for sourcing, planning, and operations leaders.

<br>

## Portfolio Overview

| Project | Core Question | Methodology | Decision Impact |
| :--- | :--- | :--- | :--- |
| **Supplier Risk & Kraljic Portfolio Analysis** | Where are we most exposed to supply risk? | MCDM + Kraljic Matrix | Supplier strategy & risk mitigation |
| **Demand Forecasting & Seasonal Scenario Analysis** | How volatile is demand, and how much buffer do we need? | Seasonal Indexing + Scenario Bands | Inventory & safety stock planning |
| **Strategic Supply Chain Network Optimization** | Where should we produce and invest capacity? | Mixed Integer Programming (MIP) | Capacity investment & network design |

<br>

## 1. Supplier Risk & Kraljic Portfolio Analysis

**Problem:** Traditional procurement metrics over-emphasize cost and ignore structural supply risk.  
**Approach:** A **Multi-Criteria Decision-Making (MCDM)** model combined with the **Kraljic Matrix** to quantify supply risk and profit impact at the product level.

**Key Insight:**  
> **Strategic products represent 93% of total spend**, creating a critical dependency that demands proactive supplier partnerships and resilience planning.

**Outcome:**  
Clear, quadrant-based sourcing strategies (Partnership, Exploit, Secure, Automate) aligned to actual risk exposure rather than intuition.

📁 *Folder:* `/project_sourcing`

<br>

## 2. Demand Forecasting & Seasonal Scenario Analysis

**Problem:** Linear forecasts mask seasonal peaks and promotion-driven volatility, leading to chronic stockouts or excess inventory.  
**Approach:** A **multi-model forecasting framework** comparing linear trends against **Seasonal Indexing**, augmented with **High / Low demand scenarios** to define a safe operating range.

**Key Insight:**  
> Across all categories, the stress-tested “High Case” reveals a consistent **~115% upside gap**, indicating current safety stock policies are under-calibrated.

**Outcome:**  
Category-specific strategies:
- **Electronics:** Pre-build inventory ahead of Q4 peak  
- **Office Supplies:** Event-driven ordering aligned with promotions  
- **Basics:** Level-loaded replenishment for cost efficiency  

📁 *Folder:* `/project_forecasting`

<br>

## 3. Strategic Supply Chain Network Optimization (MIP)

**Problem:** Production, transportation, and capacity decisions are often made in silos, inflating total system cost.  
**Approach:** A **Mixed Integer Programming (MIP)** model in Excel Solver that jointly optimizes:
- Production allocation  
- Transportation flows  
- Binary factory expansion decisions  

**Key Insight:**  
> Expanding capacity at **3 out of 4 factories** minimizes total cost, demonstrating that **selective investment** outperforms both over-expansion and under-investment.

**Outcome:**  
A quantified trade-off between fixed capital costs and variable operating savings, supporting data-driven network design decisions.

📁 *Folder:* `/project_optimization`

<br>

## Skills & Tools Demonstrated

**Analytics & Modeling**
- Supply Chain Risk Assessment  
- Demand Forecasting & Scenario Planning  
- Network Design & Capacity Optimization  
- Mixed Integer Programming (MIP)  

**Tools**
- Excel (Advanced formulas, Solver, dashboards)  
- Optimization modeling & constraint logic  
- Data normalization and weighted scoring  

<br>

## How to Navigate This Repository
Each project folder contains:
- A detailed `README.md` with business framing and insights  
- Model files (Excel-based)  
- Output visuals used for decision-making  

This structure mirrors how analytics work is consumed in real organizations:  
**Context → Model → Insight → Decision.**

<br>

## Future Direction
Planned extensions include:
- Integrating uncertainty and scenario analysis into optimization models  
- Carbon-aware network optimization  
- Re-implementing optimization logic in Python (PuLP / Pyomo)  

---

*This portfolio is designed for roles in Supply Chain Analytics, Operations, and Strategic Planning, where analytical rigor and business judgment must coexist.*
