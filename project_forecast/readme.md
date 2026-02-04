
# Demand Forecasting & Seasonal Scenario Analysis

##  Executive Summary
This project implements a **multi-model demand forecasting framework** designed to optimize procurement timing and inventory buffers across disparate product lines. By validating a **Seasonal Indexing model** against a standard linear baseline, the project identifies the most resilient forecast for high-volatility categories.

**Key Feature:** The dashboard includes an interactive **Category Slicer**, allowing stakeholders to instantly toggle between **Electronics** (Seasonal), **Basics** (High Volume), and **Office Supplies** (Promo-Driven) to view specific risk profiles.

<br>

<img width="1886" height="977" alt="0aefdda8-b6e1-4192-a4f2-3e6ae3a4384b" src="https://github.com/user-attachments/assets/b7ba75ce-ac2e-4a25-971f-93c42e51764b" />

<br>
<br>

## Business Problem

Standard linear forecasting methods often "smooth out" the peaks and valleys of seasonal demand. In a multi-category supply chain, applying a "one-size-fits-all" forecast creates distinct risks:
* **Electronics:** Risk of stockouts during the "Golden Quarter" (Q4) due to 3x demand surges.
* **Office Supplies:** Missed opportunities during "Spring Promo" events due to uncaptured marketing spikes.
* **Basics:** Over-ordering during non-peak months if growth trends are extrapolated linearly without seasonal dampening.

This project replaces static assumptions with a **Dynamic Scenario Planner** that calculates a category-specific "Safe Operating Range."


<br>

## Methodology

**1. Model Comparison**
Two distinct mathematical engines were evaluated:

* **Linear Regression:** Captures long-term growth but ignores cyclicality.
* **Seasonal Indexing:** Calculates weights for each month based on historical deviation from the mean, specifically tailored for categories like Electronics.

**2. Scenario Generation (Risk Buffers)**
Rather than providing a single "point forecast," the 2024 projection includes a **Scenario Band**. The "High Case" and "Low Case" are calculated based on the historical variance discovered during the backtesting phase, serving as a guide for Safety Stock and MOQs.

<br>

## Results

The chart below demonstrates the **Category Slicer** in action. The graph updates dynamically to show the **Seasonal Index** (Solid Line) vs. the **Risk Scenarios** (Shaded Area) for the selected product family.


<div align="center">

<img width="731" height="426" alt="image" src="https://github.com/user-attachments/assets/a182afa3-fdbf-4b4b-8546-67a2c487812c" />

| Model Comparison | Historical Error (Proxy) | 2024 Strategy |
| --- | --- | --- |
| **Seasonal Index** | **~4.8%** | **Primary (Recommended)** |
| Linear Forecast | ~11.2% | Reference Only |

</div>

### Key Insights

* **Universal Risk Exposure:** The `Stress_Test` model reveals a consistent **~115% Gap** between the Baseline Forecast and the "High Demand" scenario across all categories. This indicates that current Safety Stock policies are under-calibrated for *any* upside volatility.
* **Electronics Fragility:** With a volatility ratio of **3.1x**, Electronics requires the largest "Buffer Zone." The model suggests a "High Case" inventory build starting in **August** to meet the November peak.
* **Promo Sensitivity (Office):** Unlike the smooth seasonality of Electronics, Office Supplies shows sharp, isolated spikes (e.g., "Spring Promo"). The forecast model separates these as "Event Drivers" rather than organic trend.

<br>

## Recommendations

Based on the 2024 forecast, the following actions are recommended:

| Category | Forecast Behavior | Procurement Action |
| --- | --- | --- |
| **Electronics** | **High Volatility** | Capacitize Suppliers: Reserve "High Case" capacity for Q4 now to avoid expedited air freight later. |
| **Office** | **Promo-Driven** | Spot Buys: Use the "Spring Promo" flag to trigger one-off spot buys rather than increasing permanent safety stock. |
| **Basics** | **Growth Trend** | Contract Negotiation: Leverage the steady growth volume to negotiate long-term cost reductions. |

<br>


## Skills & Tools Demonstrated

- Interactive Dashboards: Implemented Slicers to allow users to drill down into specific product families without navigating multiple sheets.
- Risk Modeling: Calculated "High/Low" demand bands based on category-specific historical volatility.
- Data Integrity: Standardized inconsistent raw data (e.g., acutal typos, "Sum of" headers) into a clean, modeled dataset.

<br>

## Future Enhancements

Future enhancements would focus on integrating external market variables and automated safety stock logic to transition the tool from a static forecast into a dynamic inventory optimization engine.
