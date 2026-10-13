# Intel Device Repurposing: Sustainability Impact Analysis

## Executive Summary

Intel's device repurposing program processed 601,740 laptops and desktops in 2024, avoiding an estimated 6,768 metric tons of CO₂ and saving about 15.5 GWh of energy. Using SQL to join device and impact tables, I found that older hardware and devices in high-carbon-grid regions deliver the highest environmental return per unit, even though newer equipment makes up most of the volume. The analysis uses a simulated dataset and recommends how Intel's Sustainability Team should prioritize intake.

## Key Business Questions & Insights

**Key question:** Which device categories yield the highest net environmental return per unit, and how should Intel prioritize intake and resource allocation? **Primary KPI:** net avoided emissions (kg CO₂e) per repurposed unit.

* **Program totals:** 601,740 devices avoided 6,768.42 metric tons of CO₂ in 2024, with an average of 25.74 kWh saved per device per year. The notebook equates that to the annual electricity use of about 1,489 average U.S. homes.
* **Laptops vs. desktops:** The two are nearly identical per unit. Laptops average 25.80 kWh/yr and 0.0113 t CO₂, and desktops 25.62 kWh/yr and 0.0112 t CO₂. Laptops are 68% of the volume (408,064 vs. 193,676).
* **Device age:**
  * Newer devices (3 years old or less) are the largest group: 224,272 laptops and 92,919 desktops, about 53% of all devices.
  * Older devices (more than 6 years) are the smallest group (12,387 laptops and 7,852 desktops) but save the most per unit: 49.73 kWh/yr and 0.0218 t CO₂ for laptops, and 45.32 kWh/yr and 0.0198 t CO₂ for desktops. That is nearly double the 25.74 kWh fleet average and about 2.6x the per-laptop savings of newer devices (18.93 kWh/yr).
* **Regional grid intensity:** Energy savings per device are about the same across regions, but the carbon value of each kWh is not. Implied carbon intensity is roughly 0.60 kg CO₂/kWh in Asia, 0.40 in North America, and 0.25 in Europe, so the same kWh saved avoids about 2.4x more emissions in Asia than in Europe.
* **Recommendations:**
  1. Prioritize repurposing in high-carbon grid regions such as Asia.
  2. Target older, power-inefficient devices.
  3. Keep reconditioning laptops and newer assets, which show that value can be created before end of lifecycle.

## Analytical Approach & Tools

* **Environment:** SQLPad (SQL), documented in a Jupyter Notebook
* **Key Techniques:**
  * `INNER JOIN` of `intel.device_data` and `intel.impact_data` on `device_id`, with a check that all 601,740 rows matched
  * CTEs to build a reusable joined dataset
  * Feature engineering with `CASE WHEN` to bucket devices as newer (3 years or less), mid-age (4–6 years), or older (more than 6 years) from `model_year`
  * Data validation: null audit on `model_year`, valid category checks, and age sanity checks (no negative ages)
  * Aggregation with `COUNT()`, `AVG()`, `SUM()`, and `ROUND()`, plus unit conversion from kg to metric tons
* **Limitations:**
  * The dataset is simulated to mirror Intel's enterprise data and does not represent actual Intel operations.
  * Energy and CO₂ savings are modeled estimates, not meter readings.
  * There is no cost or device-lifespan data, so ROI and cost-effectiveness could not be assessed.

## Project Structure

* `Intel_Sustainability_Impact_Analysis.ipynb`: The complete notebook, including the business context, data integrity checks, SQL queries, screenshots of the query results, insights, and recommendations.
* `data/`: Two tables accessed through SQLPad: `intel.device_data` (device profiles) and `intel.impact_data` (601,740 repurposing impact records). Add CSV exports here if you want the repo to be reproducible.

## Data Source

Alvarez, R. (2026). *Intel* [Data set]. Coding for Data, Global Career Accelerators. https://globalcareeraccelerator.org/
