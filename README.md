# SQL-Project World-Bank-Debt-Analysis
# World Bank International Debt Analysis (2024)

## Overview

This repository contains a SQL-based analysis of international debt data compiled by the World Bank for the year 2024. The project explores debt obligations (in USD) of developing nations across various debt indicators, providing insights into global debt patterns. The analysis addresses key questions such as the total debt burden, the country with the highest debt, and the average debt across different indicators. The dataset is sourced from the World Bank’s International Debt Statistics (IDS) and processed using Python and SQLite.

## Project Goals

- Calculate the total amount of debt owed by countries in the dataset.
- Identify the country with the maximum debt load and its magnitude.
- Determine the average debt level across different debt indicators for 2024.
- Explore the distribution and prevalence of debt indicators to understand economic trends.

## Dataset

- **Source**: World Bank International Debt Statistics (IDS)
- **File**: `world_bank_debt.xlsx` (initial Excel file containing debt data from 1970 to 2030)
- **Processed Table**: `world_debt` (SQLite table with 2024 data)
- **Columns**:
  - `Country_Name`: Name of the country
  - `Country_Code`: ISO country code
  - `Series_Name`: Description of the debt indicator
  - `Series_Code`: Unique code for the debt indicator (e.g., `DT.DOD.DECT.CD`)
  - `Debt_Amount`: Debt value in USD for 2024
- **Notes**: The dataset was preprocessed to focus on 2024 data, with rows containing missing values dropped using `df.dropna()`.

## Technologies Used

- **Python**: For data manipulation and querying
  - Libraries: `pandas`, `sqlite3`
- **SQLite**: For database management and SQL queries
- **GitHub**: For version control and project hosting


## Key Sections

- Section 1: Introduction and data loading.
- Section 2: Count of distinct countries (123 countries).
- Section 3: List of distinct debt indicators (146 total, 30 with data for all countries).
- Section 4: Total debt (15,043,005.87 million USD).
- Section 5: Country with the highest debt (China, 2,119,167.08 million USD).
- Section 6: Average debt across indicators (e.g., 9,104.22 million USD for DT.TDS.DECT.CD).
- Section 7: Frequency of debt indicators (all 30 listed have 123 counts).
- Section 8: Intended for the highest principal repayment (query provided but not executed).
- Section 9: Maximum debt per country (query provided to conclude the analysis).

## Data Source
World Bank: For providing the International Debt Statistics dataset.

## Future Improvements
- Enhance preprocessing to handle sparse data (e.g., retain rows with missing values for specific indicators).
- Add visualizations (e.g., bar charts for debt distribution) using libraries like matplotlib or seaborn.
- Expand analysis to include debt-to-GDP ratios or regional comparisons.
