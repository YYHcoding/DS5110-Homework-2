# DS5110 — Homework 2

## Student Information

- Student: Yanhui Yang
- Course: DS5110
- Assignment: Homework 2
- Topic: Tidy Data, Join Cardinality, and Data Visualization

## Project Overview

This homework explores tidy data principles, data reshaping,
join cardinality, and data visualization using Python and pandas.

The assignment includes transforming quarterly revenue data
from wide to long format, examining the relationship between
orders and shipments, and constructing an analysis-ready table.

## Project Files

- `DS5110_HW@_YanhuiY_ang.ipynb` — Jupyter Notebook containing the analysis.
- `company_quarterly_revenue_raw.csv` — Original quarterly revenue data.
- `orders-1.csv` — Order information.
- `shipments.csv` — Shipment information.
- `WRITEUP.md` — Written analysis and discussion.
- `README.md` — Project documentation.

## How to Run

1. Download all project files into the same folder.
2. Open the Jupyter Notebook using JupyterLab or VS Code.
3. Make sure Python, pandas, and matplotlib are installed.
4. Restart the kernel and run all cells.
5. Review the outputs, visualizations, and validation results.

## Key Findings

- The revenue data was reshaped into 60 rows and 3 columns.
- Orders and shipments have a one-to-many relationship.
- Joining the tables increased the row count from 20 to 35.
- Row multiplication affected the mean order amount for some customers.
- The final order-level analysis table contains 20 rows and 7 columns.
- The final table has no missing values or duplicate order IDs.

## AI Usage Disclosure

I used ChatGPT as a learning assistant while completing this
assignment. AI assistance included explaining tidy data
principles, pandas operations, join cardinality, and the
effects of row multiplication.

ChatGPT also helped me review my analysis, interpret the
validation results, organize the written report, and improve
the clarity and grammar of my English explanations.

I ran the Python code, examined the outputs, and checked
the results in my Jupyter Notebook.