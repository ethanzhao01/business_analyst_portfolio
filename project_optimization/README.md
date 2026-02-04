# Strategic Supply Chain Network Optimization (MIP)

## Executive Summary
This project implements a **strategic supply chain network optimization model** using **Mixed Integer Programming (MIP)** in **Excel Solver**. The objective is to minimize **total end-to-end supply chain cost** by jointly optimizing **production allocation, transportation flows, and factory capacity expansion decisions**, while maintaining a **100% demand service level** across all regions.

**Key Finding:** The optimal solution expands capacity at **3 out of 4 factories**, indicating that **selective capital investment** is cost-justified when it reduces downstream transportation and production inefficiencies.

<img width="1423" height="601" alt="Weixin Image_20260116135500_2161_4" src="https://github.com/user-attachments/assets/818c6367-3eb8-44c6-a1d3-152e9b639dcb" />


<br>

## Business Problem
Global manufacturers often make production, transportation, and capacity decisions in silos. This leads to:
- Excess transportation costs due to poor plant–market alignment  
- Overloaded facilities alongside underutilized capacity  
- Capital investments made without evaluating total system impact  

This project reframes the problem as a **single integrated optimization model**, enabling data-driven evaluation of **fixed expansion costs versus variable operating costs**.

<br>

## Methodology

### 1. Network Cost Modeling
The supply chain network consists of **4 factories** (São Paulo, Rotterdam, Vancouver, Shanghai) serving **4 demand regions** (North America, Europe, South America, Rest of World). Inputs include:
- Unit production costs by factory  
- Unit transportation costs by factory–region lane  
- Fixed expansion costs and associated capacity increases  

All costs are modeled in USD with standardized demand and capacity units.

<br>

### 2. Decision Variables
The optimization model determines:
- **Shipment quantities** from each factory to each region (continuous)
- **Binary expansion decisions** (0 = no expansion, 1 = expand)
- **Effective factory capacity** after expansion

Binary expansion variables require a **Mixed Integer Programming (MIP)** formulation.

<br>

### 3. Objective Function
The model minimizes **total supply chain cost**, defined as:

<p align="center"><strong>
Total Cost = Production Cost + Transportation Cost + Capacity Expansion Cost
</strong></p>

This structure allows the solver to explicitly trade off fixed capital investment against ongoing operational savings.

<br>

### 4. Constraints
- **Demand fulfillment:** All regional demand must be met (100% service level)
- **Capacity limits:** Factory shipments cannot exceed available capacity
- **Expansion logic:** Capacity increases only if expansion is selected
- **Non-negativity:** Shipment quantities ≥ 0

The model is solved using **Excel Solver (Simplex LP with Integer Constraints)**.

<br>

## Results

The optimal solution reallocates production flows and selectively expands capacity to minimize cost while fully satisfying demand.

**Table 1: Cost Breakdown (Optimal Solution)**

| Cost Component | Value (USD) |
| :--- | ---: |
| Production | 88.8M |
| Transportation | 4.8M |
| Expansion | 2.4M |
| **Total** | **96.1M** |

<br>

### Key Insights
- **Selective expansion dominates blanket investment:** Expanding only **3 factories** yields a lower total cost than expanding none or all.
- **Transportation–capacity trade-off:** Fixed expansion costs are offset by long-term reductions in transportation expense.
- **System-level optimization matters:** Locally suboptimal decisions can be globally optimal when modeled holistically.

<br>

## Recommendations

| Area | Recommendation | Rationale |
| :--- | :--- | :--- |
| Capacity Planning | Targeted expansion | Expand only where network savings exceed fixed costs |
| Network Design | Reallocate flows | Produce closer to demand to reduce transport cost |
| Capital Allocation | Quantitative justification | Use MIP to evaluate ROI before expansion |
| Planning Process | Integrated optimization | Replace siloed planning with end-to-end models |

<br>

## Skills & Tools Demonstrated
- Supply Chain Network Design  
- Mixed Integer Programming (MIP)  
- Strategic Capacity Planning  
- Excel Solver (advanced optimization modeling)  
- Cost trade-off analysis  

<br>

## Future Enhancements
Future work includes adding carbon emission constraints, modeling demand uncertainty through scenarios, and reimplementing the model in **Python (PuLP / Pyomo)** for scalability.
