# YouTube Trending Videos Analysis
[Open Full Analysis Notebook](./SQL_YouTube_Trending_Analysis.ipynb)

## Executive Summary

As a junior data analyst at a digital media consultancy, I used SQL to analyze 6,351 US YouTube trending videos (Nov 2017 – June 2018) to understand how engagement (likes, dislikes, comments, views) varies across the trending rankings. Engagement is highly concentrated at the top: comment counts fall by roughly 85–87% with each 10x step down the rankings, and view counts are even more top-heavy between the 10th and 100th ranks.

## Key Business Questions & Insights

* **Most-liked video:** *BTS (방탄소년단) 'FAKE LOVE' Official MV* has the highest like count in the dataset.
* **Most-disliked and most-commented video:** *"So Sorry."* ranks #1 for both dislikes and comments, with 1,361,580 comments. High dislikes and high comments can go together, because controversial content drives discussion.
* **Top-10 comment depth:** The 10th most-commented video has 371,864 comments, or 27.3% of the #1 video's total (371,864 / 1,361,580).
* **Comment drop-off by rank:**
  * #10: 371,864 comments
  * #100: 53,665 comments (14.43% of #10)
  * #1000: 7,155 comments (13.33% of #100)
  * The two ratios are similar, which suggests a consistent ~85–87% decline in comments for every 10x step down in rank.
* **View drop-off by rank:** The view ratio between #10 and #100 is about 21.98%, and between #100 and #1000 about 12.56%. These ratios differ more than the comment ratios do, which suggests high view counts are clustered among the highest-ranked videos.


## Analytical Approach & Tools

* **Environment:** SQL (queries run against the `youtube.trending` table in a browser-based SQL app)
* **Key Techniques:**
  * Column selection and `ORDER BY ... DESC` to rank videos by likes, dislikes, comments, and views
  * `LIMIT` and `OFFSET` to isolate the 10th, 100th, and 1000th ranked videos
  * Ratio comparison across ranks to measure how steeply engagement drops off
* **Dataset columns used:** `title`, `channel_title`, `views`, `likes`, `dislikes`, `comment_count`

## Project Structure

## Project Structure

* `SQL_YouTube_Trending_Analysis.ipynb`: The complete notebook, including each analysis task, the SQL queries I wrote, screenshots of the query results, and my written analysis.
* `data/`: The `youtube.trending` dataset (6,351 videos, 16 columns) was accessed through the course SQL app.