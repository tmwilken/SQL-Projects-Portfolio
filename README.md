# SQL Portfolio: Data Analysis & Business Intelligence

## Overview
A collection of SQL projects demonstrating end-to-end data analysis, query optimization, and relational database management. Each project focuses on extracting actionable insights to solve real-world operational, content, and revenue problems.

---

## Featured Projects
| Project | Business Problem | Key Techniques & Tools | Dialect | Folder |
| :--- | :--- | :--- | :--- | :--- |
| **Startup Investment & Risk Analysis** | Evaluated capital allocation and closure rates across 27,000+ venture-backed companies, analyzing high-loss sectors (cleantech) to assess risk vs. ROI profile[cite: 9, 12, 13, 14]. | Multi-Condition Filtering (`AND`/`OR`), `NULL` Value Handling (`IS NOT NULL`), Pattern Matching (`ILIKE`), Sector Failure Rate Analysis[cite: 10, 15, 16] | SQL / PostgreSQL | [View Project](./Startup-Investments-Analysis) |
| **YouTube Trending Engagement Analysis** | Analyzed 6,300+ trending videos to evaluate audience engagement patterns across views, likes, dislikes, and comments, identifying distribution drop-offs across top performance tiers. | Rank Sampling (`LIMIT`, `OFFSET`), Multi-Metric Sorting (`ORDER BY`), Engagement Distribution & Ratio Analysis | SQL / PostgreSQL | [View Project](./YouTube-Trend-Analysis) |
| **Digital Music Store Analysis** | Analyzed invoice line items, customer lifetime behavior, and global genre demand to recommend inventory shifts and target marketing regions. | Multi-Table `JOIN`s (5+ tables), Aggregate Filtering (`HAVING`), Subqueries, Summary Tables | PostgreSQL / MySQL | [View Project](./Digital-Music-Store) |

---

## Project Roadmap & Pipeline
| Status | Project | Industry | Core Analytical Focus |
| :--- | :--- | :--- | :--- |
| In Review |  Sustainability Impact Analysis | Technology | Evaluating the environmental return on investment (ROI) of Intel's hardware repurposing program across three primary dimensions |
| Planned | Reader Engagement and Retention Analysis | Digital Media | Identifying what behaviors early in a reader's actions predict whether they become loyal, long-term readers (and ultimately paying subscribers). |

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

