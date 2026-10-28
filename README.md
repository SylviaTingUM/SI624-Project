# Socioeconomic Conditions and Medicare Spending Across U.S. Counties

**SI 624 Final Project — Technical Report**  
University of Michigan School of Information

**Team:** Sylvia Feng, Denali Wood, and Taqi Abusaif

## Project Overview

This project examines associations between county-level socioeconomic conditions and standardized Medicare spending per capita. It combines 2023 county-level Original Medicare (fee-for-service) data from the Centers for Medicare & Medicaid Services (CMS) with socioeconomic measures from the U.S. Census Bureau's 2023 American Community Survey (ACS) 5-Year Estimates (2019–2023).

The analysis considers median household income, poverty rate, and unemployment rate, alongside beneficiary age, dual-eligibility percentage, and Medicare Advantage participation. Methods include data cleaning, descriptive statistics, exploratory visualizations, correlation analysis, and multiple linear regression. Results describe county-level associations, not causal effects.

## Repository Structure

```text
SI624-Project/
├── main.ipynb                  # Main technical report and analysis
├── main.html                   # Exported HTML version of the report
├── data/                       # Input datasets
├── figures/                    # Figures exported from the main notebook
│   ├── income_spending.png
│   ├── rate_spending.png
│   └── quartile.png
├── supplementary_notebooks/    # Supporting notebooks and exploratory work
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

## Data Sources

- **CMS Medicare Geographic Variation Public Use File:** County-level Original Medicare spending and beneficiary characteristics for 2023.
- **ACS 2023 5-Year Estimates:** County-level socioeconomic indicators, representing the 2019–2023 survey period.

The main notebook expects these input files relative to the repository root:

```text
data/2014-2024 Original Medicare Geographic Variation Public Use File.csv
data/ACS_2023_5Year_County_Socioeconomic.csv
```

## Setup and Execution

Run the following commands from the **repository root** (the folder containing `main.ipynb`):

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab main.ipynb
```

On Windows, activate the environment using `.venv\Scripts\activate` instead of the `source` command above.

In JupyterLab, select the Python environment and run the notebook cells in order. The notebook reads files from `data/` and saves three figures to `figures/`. To view the exported report without running Python, open `main.html` in a web browser.