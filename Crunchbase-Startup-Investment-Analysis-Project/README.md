# Startup Investments: SQL Analysis of Crunchbase Funding Data

## Executive Summary

As a strategic advisor to a global venture capital firm, I used SQL to analyze the Crunchbase company investments dataset (over 27,000 companies) to see which startups attracted the most funding and which sectors carry the most risk. Mobile company Clearwire was the top-funded company at $5.7B, while cleantech made up half of the twelve best-funded companies that shut down. Closed companies are still only about 7.4% of funded cleantech companies, slightly below the 7.9% rate across the full dataset.

## Key Business Questions & Insights

* **Top-funded company:** Clearwire (mobile) received $5.7B in total funding, which is 5.7x (470% more than) the 12th-ranked company, BlackBerry (hardware), at $1.0B. Clearwire is also the only company in the top 12 with an 'acquired' status.
* **Top-funded company that closed:** Abound Solar (cleantech) raised $510M before shutting down. The next closed company, Amp'd Mobile, raised $374M.
* **Cleantech concentration among failures:** Six of the twelve best-funded closed companies are in the cleantech category: Abound Solar, AltraBiofuels, SolFocus, Range Fuels, SulfurCell, and Ausra.
* **Cleantech failure rate:** Of 827 funded cleantech companies, 61 have closed, which is 7.38%. That is slightly below the 7.9% closed rate for the full table. Cleantech failures are therefore concentrated among very large raises, not more frequent overall.
* **Name-based exploration:** 275 cleantech companies have "solar", "power", or "energy" in their names (case-insensitive match).

## Analytical Approach & Tools

* **Environment:** SQLPad (PostgreSQL-compatible syntax), documented in a Jupyter Notebook
* **Key Techniques:**
  * Filtering with `WHERE`, including `IS NOT NULL` to exclude companies with no funding data
  * Combining conditions with `AND` / `OR` to isolate closed and cleantech companies
  * `ORDER BY ... DESC` and `LIMIT` to rank the top-funded companies
  * Case-insensitive pattern matching with `ILIKE` for name searches
  * Ratio and percentage calculations to compare funding levels and failure rates
* **Dataset columns used:** `name`, `category_code`, `status`, `funding_total_usd`

## Project Structure

* `SQL_Analyzing_Startup_Investments.ipynb`: The complete notebook, including each analysis task, the SQL queries I wrote, screenshots of the query results, and my written analysis.
* `assets/`: Screenshots of query results used in the notebook and this README.
* `data/`: The `crunchbase.companies` dataset (20 columns, over 27,000 rows) was accessed through SQLPad; add a CSV export here if you want the repo to be reproducible.

## Data Source

Alvarez, R. (2026). *Crunchbase* [Data set]. Coding for Data, Global Career Accelerators. https://globalcareeraccelerator.org/
