# Supplier Risk & Kraljic Portfolio Analysis

## Executive Summary
This project applies a **data-driven supplier risk assessment** using a **Multi-Criteria Decision-Making (MCDM)** model and the **Kraljic Portfolio Matrix**.  
The objective is to identify sourcing concentration, supply risk exposure, and profit impact across products, enabling procurement teams to prioritize actions that improve resilience while controlling cost.

The analysis shows that a **small set of Strategic products accounts for the majority of total spend**, indicating high dependency risk and the need for proactive supplier management.

---

## Business Problem
Traditional supplier evaluations tend to focus heavily on cost, which can mask:
- Supply disruption risk
- Single-source and regional concentration
- High-profit products with fragile supply bases
- Excess effort spent on low-impact items

The business requires a **structured and repeatable framework** to:
- Rank suppliers and products objectively
- Balance cost efficiency with supply resilience
- Allocate procurement effort where it delivers the most value

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

