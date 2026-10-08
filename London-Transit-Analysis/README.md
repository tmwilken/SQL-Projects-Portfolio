# London Underground Ridership: SQL Analysis of TfL RODS Data

## Executive Summary

As a data analyst for Transport for London (TfL), I used SQL to analyze the Rolling Origin and Destination Survey (RODS), which models a typical November weekday on the London Underground across 6,295 rows and about 4.88 million daily journeys. Zone 1 originates more than half of all trips and the PM Peak is the busiest period, with commuting between home and work driving the network. Zone 1 works as an employment center while outer zones are mainly residential, and tourist travel fills the midday lull between commuter peaks.

## Key Business Questions & Insights

* **Total daily demand:** The system handles about 4,878,330 journeys on a typical weekday.
* **Where trips start:** Zone 1 originates 2,522,837 journeys, or 51.7% of the total. That is nearly double Zone 2 (1,294,626) and more than Zones 3–5 combined (about 1.06M).
* **When trips happen:** The PM Peak (4–7pm) is the busiest period at 1,367,309 journeys, ahead of the AM Peak (1,258,027) and Midday (1,221,556). The two commuter peaks together make up roughly 54% of all journeys.
* **Why people travel:**
  * "Home" is the most common origin purpose (1,835,593 trips), followed by "Work" (1,400,886).
  * Home-to-Work (1,182,048) and Work-to-Home (999,123) are the two largest origin-destination purpose pairs, which confirms that workforce commuting anchors the network.
* **Timing follows purpose:** The AM Peak is dominated by departures from home, and the PM Peak by departures from work.
* **Zone-level split:** In Zone 1, Work is the top origin purpose (935,202 trips, ahead of Home at 653,373). In Zone 2 the order reverses (Home 586,397, Work 318,529), which supports a central-employment, outer-residential pattern.
* **Tourist travel:** Tourism-related trips cluster at Midday, with Home-to-Tourist (14,228) the largest single flow. They fill the lull between the commuter peaks.
* **Operational takeaway:** Service planning should balance the tidal flows of the peaks and the gap between the city center and the outer zones.

## Analytical Approach & Tools

* **Environment:** SQLPad (PostgreSQL-compatible syntax), documented in a Jupyter Notebook
* **Key Techniques:**
  * `SUM()` aggregation across single- and multi-column `GROUP BY` combinations (zone, time period, origin purpose, destination purpose)
  * `WHERE ... OR` filtering to isolate tourism-related trips
  * Multi-level `ORDER BY` to group and rank results for comparison
  * Percentage and ratio calculations from query results
  * Translating findings into operational recommendations for stakeholders
* **Dataset columns used:** `entry_zone`, `time_period`, `origin_purpose`, `destination_purpose`, `distance`, `daily_journeys`

## Project Structure

* `SQL_London_Transit_Analyis.ipynb`: The complete notebook, including each analysis task, the SQL queries I wrote, screenshots of the query results, and my written analysis.
* `data/`: The `tfl.rods` dataset (6,295 rows, 6 columns) was accessed through SQLPad.
## Data Source

Alvarez, R. (2026). *Tfl RODS* [Data set]. Coding for Data, Global Career Accelerators. https://globalcareeraccelerator.org/
