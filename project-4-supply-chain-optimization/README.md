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
    * Named Ranges for model scalability and auditability.

---

## 📉 Problem Statement
A global manufacturer operates four factories: **Santiago, Antwerp, Vancouver, and Nagoya**. Current capacity is insufficient to meet projected regional demand. 

**The Challenge:**
1. Which factories should be expanded to maximize ROI?
2. How should production be allocated to minimize the "Total Cost of Ownership" (Production + Shipping + Expansion)?

---

## 🏗️ Model Architecture

### 1. Objective Function
Minimize $Z$, where:
$$Z = \text{Production Costs} + \text{Transportation Costs} + \text{Expansion Costs}$$

### 2. Decision Variables
* **Production Flows:** Quantity of units shipped from Factory $i$ to Region $j$.
* **Expansion Decisions:** Binary variables $\{0, 1\}$ representing the decision to expand a specific factory.

### 3. Key Constraints
* **Demand Satisfaction:** Total units received by a region must be $\ge$ regional demand.
* **Capacity Constraint:** Total units produced by a factory must be $\le$ (Current Capacity + Expanded Capacity).
* **Binary Integrity:** Expansion variables must be constrained to binary (0 or 1).

---

## 🚀 Key Results & Insights
Based on the optimization run:
* **Optimized Total Cost:** $96,061,140.
* **Strategic Decisions:** The model recommended expansion for **Santiago, Antwerp, and Vancouver**, while keeping **Nagoya** at current capacity.
* **Service Level:** Achieved 100% demand fulfillment across all global regions.
* **Logistics Efficiency:** Vancouver was prioritized for North American demand due to significantly lower transportation costs ($50,000 per unit vs $140,000 from Nagoya).

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
4. Observe how the "Expansion Decisions" and "Production" variables update to reach the minimum total cost.

---

### 📩 Contact
**[Your Name]** [Your LinkedIn Profile Link] | [Your Email Address]
