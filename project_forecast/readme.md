
# Demand Forecasting & Seasonal Scenario Analysis

## Executive Summary

This project implements a **multi-model demand forecasting framework** designed to optimize procurement timing and inventory buffers. By validating a **Seasonal Indexing model** against a linear baseline, the project identifies the most resilient forecast for high-volatility product categories.

**Key Finding:** The Seasonal Index model reduced forecast error by **over 50% compared to linear trends**, capturing critical Q4 surges that would have otherwise resulted in significant stockouts.
<br>

<img width="1886" height="977" alt="0aefdda8-b6e1-4192-a4f2-3e6ae3a4384b" src="https://github.com/user-attachments/assets/b7ba75ce-ac2e-4a25-971f-93c42e51764b" />

<br>
<br>

## Business Problem

Standard linear forecasting methods often "smooth out" the peaks and valleys of seasonal demand, leading to **under-ordering during peak periods** and **excess capital tied up in slow months**. This project seeks to replace "gut-feel" adjustments with a validated, seasonal approach that provides suppliers with a clear "High/Low" operating range.

<br>

## Methodology

**1. Backtesting & Model Validation**
To verify the math before projecting into 2024, I performed a **retrospective analysis (In-Sample Testing)**. I used 2022 actual data to generate a 2023 forecast, which was then compared against 2023 actual results to determine the most accurate logic.

**2. Model Comparison**
Two distinct mathematical engines were evaluated:

* **Linear Regression:** Captures long-term growth but ignores cyclicality.
* **Seasonal Indexing:** Calculates weights for each month based on historical deviation from the mean, specifically tailored for categories like Electronics.

**3. Scenario Generation (Risk Buffers)**
Rather than providing a single "point forecast," the 2024 projection includes a **Scenario Band**. The "High Case" and "Low Case" are calculated based on the historical variance discovered during the backtesting phase, serving as a guide for Safety Stock and MOQs.

<br>

## Results

The chart below visualizes the 2024 projection for basics products. The **Seasonal Index** (solid line) tracks the expected demand, while the **shaded area** represents the "Safe Operating Range" for procurement teams.

<div align="center">

<img width="731" height="426" alt="image" src="https://github.com/user-attachments/assets/a182afa3-fdbf-4b4b-8546-67a2c487812c" />

| Model Comparison | Historical Error (Proxy) | 2024 Strategy |
| --- | --- | --- |
| **Seasonal Index** | **~4.8%** | **Primary (Recommended)** |
| Linear Forecast | ~11.2% | Reference Only |

</div>

### Key Insights

* **Seasonality Dominance:** Electronics demand shows a **15-20% surge** starting in October. Using the Seasonal Index ensures inventory is staged 60 days prior to the peak.
* **Resilience Planning:** The "High Case" scenario provides a 2024 ceiling, allowing procurement to book supplier capacity in advance to avoid expedited shipping costs.
* **Forecast Stability:** By anchoring the 2024 forecast in 2022-2023 seasonality patterns, the model filters out "noise" while retaining the "signal" of annual cycles.

<br>

## Recommendations

Based on the 2024 forecast, the following actions are recommended:

| Category | Forecast Behavior | Procurement Action |
| --- | --- | --- |
| **Electronics** | **High Volatility** | Utilize the **High-Case scenario** for Q4 component orders to prevent stockouts. |
| **Basics** | **Stable Trend** | Utilize the **Linear Baseline** to negotiate lower prices through long-term, steady volume commitments. |
| **All Categories** | **Scenario Planning** | Shared the **Buffer Zone** with Tier-1 suppliers to ensure production capacity aligns with our "High Case" projection. |

<br>


## Skills & Tools Demonstrated

This project demonstrates proficiency in **Predictive Analytics**, **Backtesting Methodologies**, and **Advanced Excel Modeling**. Technical execution involved seasonal indexing math, dynamic array formulas for scenario generation, and UX-focused dashboard design on macOS.

<br>

## Future Enhancements

Future enhancements would focus on integrating external market variables and automated safety stock logic to transition the tool from a static forecast into a dynamic inventory optimization engine.
