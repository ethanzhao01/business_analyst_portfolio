# Strategic Supply Chain Network Optimization Model

## 📌 Project Overview
This project features a **Mixed-Integer Linear Programming (MILP)** model built in Excel to optimize a global manufacturing and distribution network. The objective is to determine the most cost-effective way to meet global demand while evaluating whether to invest in factory expansions.

The model balances **production costs**, **transportation logistics**, and **capital expenditures (CAPEX)** for facility expansion across four global regions: North America, Europe, South America, and Rest of World (RoW).

---

## 🛠️ Technical Stack
* **Tool:** Microsoft Excel
* **Engine:** Frontline Solver (Simplex LP Algorithm)
* **Modeling Techniques:**
    * Linear Programming (LP) for flow optimization.
    * Binary Integer Programming for "Go/No-Go" expansion decisions.
    * Constraint Management (Demand satisfaction vs. Capacity limits).

---

## 📉 Problem Statement
A global manufacturer operates four factories: **São Paulo, Rotterdam, Vancouver, and Shanghai**. Current capacity is insufficient to meet projected regional demand. 

**The Challenge:**
1. Which factory expansions yield the highest network efficiency?
2. How should production be allocated to minimize the "Total Cost of Ownership" (Production + Shipping + Expansion)?

---

## 🏗️ Model Architecture

### 1. Objective Function
Minimize $Z$ (Cell B32), where:
$$Z = \text{Production Costs} + \text{Transportation Costs} + \text{Expansion Costs}$$

### 2. Decision Variables
* **Production Flows ($B20:E23):** Quantity of units shipped from each factory to each region.
* **Expansion Decisions ($I20:I23):** Binary variables {0, 1} representing the decision to expand a specific factory.

### 3. Key Constraints
* **Demand Satisfaction ($B24:E24 >= B13:E13):** Total units received by a region must meet or exceed demand.
* **Capacity Constraint ($F20:F23 <= J20:J23):** Total production at any factory cannot exceed its "New Capacity" (Current + Added).
* **Binary Integrity ($I20:I23 = binary):** Expansion decisions are restricted to 0 (No) or 1 (Yes).

---

## 🚀 Key Results & Insights
Based on the optimization run:
* **Optimized Total Cost:** $96,061,140.
* **Expansion Strategy:** The model recommended expansion for **São Paulo, Rotterdam, and Vancouver**, while **Shanghai** remains at current capacity to minimize fixed costs.
* **Service Level:** Achieved 100% demand fulfillment across all global regions.
* **Cost Efficiency:** Even with a $2.4M investment in expansion, the total cost is minimized by reducing high-cost transportation routes and leveraging more efficient production centers.

---

## 📁 Repository Structure
* `/model`: Contains the `.xlsx` file with the Solver configuration.
* `/images`: Screenshots of the Solver parameters and final dashboard.
* `README.md`: Project documentation.

---

## 💡 How to Use
1. Download the `supply_chain_optimization.xlsx` file.
2. Ensure the **Solver Add-in** is enabled in Excel (**File > Options > Add-ins**).
3. Open the file, navigate to the **Data** tab, click **Solver**, and hit **Solve**.

---

### 📩 Contact
**[Your Name]** - [Your LinkedIn Profile] | [Your Email Address]
