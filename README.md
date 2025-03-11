# SQL-Project World-Bank-Debt-Analysis
World Bank International Debt Analysis (2024)
Overview
This repository contains a SQL-based analysis of international debt data compiled by the World Bank for the year 2024. The project explores debt obligations (in USD) of developing nations across various debt indicators, providing insights into global debt patterns. The analysis addresses key questions such as the total debt burden, the country with the highest debt, and the average debt across different indicators. The dataset is sourced from the World Bank’s International Debt Statistics (IDS) and processed using Python and SQLite.

Project Goals
Calculate the total amount of debt owed by countries in the dataset.
Identify the country with the maximum debt load and its magnitude.
Determine the average debt level across different debt indicators for 2024.
Explore the distribution and prevalence of debt indicators to understand economic trends.
Dataset
Source: World Bank International Debt Statistics (IDS)
File: world_bank_debt.xlsx (initial Excel file containing debt data from 1970 to 2030)
Processed Table: world_debt (SQLite table with 2024 data)
Columns:
Country_Name: Name of the country
Country_Code: ISO country code
Series_Name: Description of the debt indicator
Series_Code: Unique code for the debt indicator (e.g., DT.DOD.DECT.CD)
Debt_Amount: Debt value in USD for 2024
Notes: The dataset was preprocessed to focus on 2024 data, with rows containing missing values dropped using df.dropna().
Technologies Used
Python: For data manipulation and querying
Libraries: pandas, sqlite3
SQLite: For database management and SQL queries
GitHub: For version control and project hosting
Installation
To run this project locally, follow these steps:

Clone the Repository:
bash

Collapse

Wrap

Copy
git clone https://github.com/your-username/world-bank-debt-analysis.git
cd world-bank-debt-analysis
Install Dependencies: Ensure you have Python 3.x installed. Then, install the required libraries:
bash

Collapse

Wrap

Copy
pip install pandas sqlite3
Note: sqlite3 is included in Python’s standard library, so no additional installation is needed.
Prepare the Dataset:
Place the world_bank_debt.xlsx file in the project directory. You can obtain a sample dataset from the World Bank’s IDS portal (https://data.worldbank.org) or use the provided file if available.
Ensure the file structure matches the original (with yearly columns from 1970 to 2030).
Set Up the Database:
The notebook (World_Bank_Debt_Analysis.ipynb) includes code to preprocess the Excel file and create an SQLite database (debt_data.db). Run the notebook cells up to the database creation step to generate the world_debt table.
Usage
Run the Notebook:
Open World_Bank_Debt_Analysis.ipynb in a Jupyter Notebook environment (e.g., Jupyter Lab or VS Code with the Jupyter extension).
Execute the cells sequentially to:
Load and preprocess the dataset.
Create the SQLite database.
Run SQL queries to analyze the data.
The notebook is divided into sections (1–9) that guide you through the analysis process.
Key Analysis Steps:
Section 1: Introduction and data loading.
Section 2: Count of distinct countries (123 countries).
Section 3: List of distinct debt indicators (146 total, 30 with data for all countries).
Section 4: Total debt (15,043,005.87 million USD).
Section 5: Country with the highest debt (China, 2,119,167.08 million USD).
Section 6: Average debt across indicators (e.g., 9,104.22 million USD for DT.TDS.DECT.CD).
Section 7: Frequency of debt indicators (all 30 listed have 123 counts).
Section 8: Intended for the highest principal repayment (query provided but not executed).
Section 9: Maximum debt per country (query provided to conclude the analysis).
Output:
Results are displayed as pandas DataFrames within the notebook.
Key findings are summarized in the text cells.
Files
World_Bank_Debt_Analysis.ipynb: The main Jupyter Notebook containing the analysis.
world_bank_debt.xlsx: The raw dataset (if included; otherwise, download from the World Bank).
debt_data.db: The SQLite database generated during execution (created automatically).
README.md: This file, providing project documentation.
Contributions
This project is open for contributions. To contribute:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit them (git commit -m "Description of changes").
Push to the branch (git push origin feature-branch).
Open a pull request with a description of your changes.
License
This project is licensed under the MIT License. Feel free to use, modify, and distribute the code, provided you include the original license.

Acknowledgments
World Bank: For providing the International Debt Statistics dataset.

Future Improvements
Enhance preprocessing to handle sparse data (e.g., retain rows with missing values for specific indicators).
Add visualizations (e.g., bar charts for debt distribution) using libraries like matplotlib or seaborn.
Expand analysis to include debt-to-GDP ratios or regional comparisons.
