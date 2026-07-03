# DebtSQL

A SQL-based exploratory analysis of the World Bank's international debt dataset, built as a Jupyter notebook (`debt_Analysis.ipynb`) that runs SQL queries directly against the data using `ipython-sql` / `sqlite3`.

## About

Countries, like individuals, take on debt to manage their economies, funding things like infrastructure so citizens can lead comfortable lives. The World Bank is one of the organizations that provides this kind of debt financing.

This notebook analyzes the World Bank's international debt data, which records the amount of debt (in USD) owed by developing countries across a range of debt categories ("indicators"). Using SQL queries run inline in the notebook, it works through questions such as:

1. What is the total amount of debt owed by the countries in the dataset?
2. Which country owes the most debt, and how much?
3. What is the average amount of debt across the different debt indicators?
4. Which debt indicator accounts for the highest average and highest total debt?
5. Which indicator is the most common one across countries?
6. Which countries carry the highest maximum debt in a single category?

## Contents

| File | Description |
|---|---|
| `debt_Analysis.ipynb` | Jupyter notebook containing the full SQL-based analysis, with markdown commentary explaining each step and finding. |

## Tech Stack

- **Python** / **Jupyter Notebook**
- **SQL** (via the `ipython-sql` extension, using the `%%sql` magic)
- `sqlite3` / `sqlalchemy` / `psycopg2` for database connectivity
- `pandas` for supplementary data handling

## Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook or JupyterLab

### Installation

Clone the repository:

```bash
git clone https://github.com/DakshSaijwal/DebtSQL.git
cd DebtSQL
```

Install the required packages:

```bash
pip install ipython-sql sqlalchemy psycopg2 pandas jupyter
```

### Running the Notebook

```bash
jupyter notebook debt_Analysis.ipynb
```

The notebook loads the `%sql` extension and connects to a local database containing the `international_debt` table, then walks through the analysis step by step using `%%sql` cells.

> **Note:** The notebook expects an `international_debt` table to already be available in the connected database. If you're starting from scratch, load the World Bank international debt dataset (e.g., from Kaggle or a `.csv` export) into a SQLite/Postgres database and name the table `international_debt` before running the queries.

## Sample Insight

Some of the findings surfaced in the notebook:
- The dataset covers debt data for **124 distinct countries**.
- **China** holds the highest total debt across all indicators.
- Long-term debt repayment (`DT.AMT.DLXF.CD`) is both the highest average-debt category and one of the most common indicators across countries.

## License

No license has been specified for this repository. All rights reserved by the author unless stated otherwise.

## Author

[Daksh Saijwal](https://github.com/DakshSaijwal)
