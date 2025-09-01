# COVID-19’s Impact on NYC Taxis

**Course:** STAT 5291 – Advanced Data Analytics
**Institution:** Columbia University, Department of Statistics
**Team Members:** Julieta Caroppo, Geraldine Nina Montano, JiangKun Wang, Anqi Wu, Jun Zheng
**Date:** May 2025

## Project Overview

This project investigates how the **COVID-19 pandemic** altered the long-term trajectory of **yellow taxi demand in New York City**. Using **NYC Taxi & Limousine Commission (TLC)** trip-level data (2014–2024), we quantify both the immediate disruptions and the evolving recovery of taxi ridership.

The analysis applies **regression-based methods and time series forecasting** to determine whether taxi demand has rebounded to pre-pandemic levels or settled at a new, lower equilibrium.

## Data

* **Source:** NYC TLC Yellow Taxi Trip Records (2014–2024) https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
* **Scale:** Hundreds of millions of trip-level observations aggregated into \~3,960 daily entries with 24 summary variables
* **Variables:** Trip counts, fares, trip distance, duration, passenger counts, borough-level pickups/dropoffs, etc.
* **Processing:**

  * Cleaned invalid/missing trip records (e.g., negative distances, malformed fares)
  * Standardized schema across years
  * Aggregated to **daily summaries** for modeling


## Methods

We applied multiple modeling approaches to capture structural shifts in taxi demand:

1. **Linear Regression (OLS):** Baseline associations between ridership and predictors (fares, distance, borough pickups, COVID phases).
2. **Segmented Regression:** Identified structural breaks in fare revenue trends around March 2020.
3. **Regression Discontinuity Design (RDD):** Quantified the abrupt decline in trip volume at the onset of COVID-19 (74.6% drop; \~173k fewer daily trips).
4. **SARIMAX Time Series Model:** Forecasted **counterfactual ridership** absent COVID-19 to assess cumulative lost demand (\~80 million rides, 2020–2022).

