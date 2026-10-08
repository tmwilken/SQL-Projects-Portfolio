# SQL Portfolio: Data Analysis & Business Intelligence

## Overview
A collection of SQL projects demonstrating end-to-end data analysis, query optimization, and relational database management. Each project focuses on extracting actionable insights to solve real-world operational, content, and revenue problems.

---

## Featured Projects
| Project | Business Problem | Key Techniques & Tools | Industry | Folder |
| :--- | :--- | :--- | :--- | :--- |
| **Reader Engagement & Retention Analyis** | Identifying what behaviors early in a reader's actions predict whether they become loyal, long-term readers (and ultimately paying subscribers). | CTEs, window functions like `LAG` and `ROW_NUMBER`, date functions, and conditional aggregations | Digital Media | Planned |
| **Sustainability Impact Analysis** | Evaluating the environmental return on investment (ROI) of Intel's hardware repurposing program across three primary dimensions | `INNER JOIN`, CTEs, `CASE WHEN`, aggregate functions, `GROUP BY`, calculated fields, `NULL validation`, data segmentation | Technology | In Review |
| **Digital Music Store Analysis** | Analyzed invoice line items, customer lifetime behavior, and global genre demand to recommend inventory shifts and target marketing regions. | Multi-Table `JOIN`s (5+ tables), Aggregate Filtering (`HAVING`), Subqueries, Summary Tables | E-Commerce | [View Project](./SQL-Digital-Music-Store-Project) |

---

## Project Roadmap & Pipeline
| Status | Project | Industry | Core Analytical Focus |
| :--- | :--- | :--- | :--- |
| Planned | Reader Engagement and Retention Analysis | Digital Media | Identifying what behaviors early in a reader's actions predict whether they become loyal, long-term readers (and ultimately paying subscribers). |
| In Review |  Sustainability Impact Analysis | Technology | Evaluating the environmental return on investment (ROI) of Intel's hardware repurposing program across three primary dimensions |
| Completed | Construction Job Demand | Construction | Investigated the relationship between severe weather events and construction job demand using SQL subqueries to identify patterns that could inform demand forecasting and resource allocation. |
| Completed | GameJet Microtransactions | Mobile Gaming | Identify opportunities for improving monetization strategies, free-to-paid conversion, and revenue growth. |
| Completed | FastKitchen Customer Analysis | Food & Beverage | Consolidated registered and guest customer data using SQL outer joins to develop a comprehensive view of FastKitchen’s customer base and inform customer insights. |
| Completed | NBA Performance Analysis | Professional Sports | Examined NBA team performance, scoring trends, and evolving playing styles across 17 seasons to identify drivers of team success and inform coaching strategies. |
| Completed | [London Transit Analysis](./London-Transit-Analysis) | Transportation (Public Sector) | Analyzed London public transit ridership patterns, peak travel times, and line usage to inform service scheduling, resource allocation, and infrastructure planning. |
| Completed | [Startup Investment Analysis](./Crunchbase-Startup-Investment-Analysis-Project) | B2B DaaS | Assessed capital allocation and closure rates in venture-backed companies, analyzed high-loss sectors to assess risk vs. ROI profile. |
| Completed | [YouTube Trending Analysis](./youtube-trending-analysis) | Digital Media & Entertainment | Evaluated audience engagement patterns and identifying distribution drop-offs across top performance. |
| Completed | [Digital Music Store Analysis](./SQL-Digital-Music-Store-Project) | E-Commerce | Analyzed sales transactions, customer purchasing behavior, and global music genre demand to identify opportunities for inventory optimization and geographically targeted marketing strategies. |

---

## Repository Structure & Standards
Each project directory includes:
- **`README.md`**: Business context, schema documentation, key questions, and summary of findings.
- **`schema.sql` / Data Source**: DDL scripts or clear source links to reproduce the database locally.
- **`queries.sql`**: Fully annotated, production-style SQL formatted for readability with descriptive aliasing.

## Getting Started
To run these queries locally:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/tmwilken/SQL-Projects-Portfolio.git](https://github.com/tmwilken/SQL-Projects-Portfolio.git)
   cd SQL-Projects-Portfolio
2. **Database Setup:**
   - Navigate to the specific project folder (e.g., cd YouTube-Trend-Analysis).
   - Run the provided schema script or load the dataset into your SQL engine (PostgreSQL, MySQL, SQLite).
3. **Execute Queries:**
   Run the numbered SQL scripts sequentially using your client of choice (pgAdmin, DBeaver, VS Code SQLTools, MySQL Workbench).

---

## **Contact**
Tina Marie Wilken
- [LinkedIn](https://www.linkedin.com/in/tinamariewilken/)
- [Portfolio](https://github.com/tmwilken)
- [Email](mailto:tinamariewilken@gmail.com)

