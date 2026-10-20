# SQL Portfolio: Data Analysis & Business Intelligence

## Overview
A collection of SQL projects demonstrating end-to-end data analysis, query optimization, and relational database management. Each project focuses on extracting actionable insights to solve real-world operational, content, and revenue problems.

---

## Featured Projects
| Project | Business Problem | Key Techniques & Tools | Industry | Folder |
| :--- | :--- | :--- | :--- | :--- |
| **Reader Engagement & Retention Analyis** | Identifying what behaviors early in a reader's actions predict whether they become loyal, long-term readers (and ultimately paying subscribers). | CTEs, window functions like `LAG` and `ROW_NUMBER`, date functions, and conditional aggregations | Digital Media | Planned |
| **Sustainability Impact Analysis** | Evaluating the environmental return on investment (ROI) of Intel's hardware repurposing program across three primary dimensions | `INNER JOIN`, CTEs, `CASE WHEN`, aggregate functions, `GROUP BY`, calculated fields, `NULL validation`, data segmentation | Technology | [View Project](./Intel-Sustainability-Impact-Analysis) |
| **Digital Music Store Analysis** | Analyzed invoice line items, customer lifetime behavior, and global genre demand to recommend inventory shifts and target marketing regions. | Multi-Table `JOIN`s (5+ tables), Aggregate Filtering (`HAVING`), Subqueries, Summary Tables | E-Commerce | [View Project](./SQL-Digital-Music-Store-Project) |

---

## Project Roadmap & Pipeline
| Status | Project | Industry | Core Analytical Focus |
| :--- | :--- | :--- | :--- |
| Planned | Reader Engagement and Retention Analysis | Digital Media | Identifying what behaviors early in a reader's actions predict whether they become loyal, long-term readers (and ultimately paying subscribers). |
| Completed |  [Sustainability Impact Analysis(./Intel-Sustainability-Impact-Analysis] | Technology | Evaluating the environmental return on investment (ROI) of Intel's hardware repurposing program across three primary dimensions |
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

