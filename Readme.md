
# PowerCo Churn Prediction

## Project Overview

PowerCo Churn Prediction is an exploratory data analysis project based on customer and historical pricing data from an energy company.

The project investigates customer characteristics, consumption patterns, pricing trends, and factors associated with customer churn. The analysis is currently documented in:

- `notebooks/EDA_BCG_Submission.ipynb`

## Objectives

The main objectives of this project are to:

- Understand the structure and quality of the available data.
- Explore customer consumption, margins, tenure, and product information.
- Analyse the distribution of customer churn.
- Compare churned and retained customers.
- Examine historical pricing variables and trends over time.
- Identify features that may support future churn prediction modelling.

## Datasets

The project uses two datasets stored in the `data` directory.

### Customer Data

File: `data/client_data.csv`

This dataset contains customer-level information, including:

- Customer identifiers
- Electricity and gas consumption
- Forecast consumption
- Product information
- Customer tenure
- Number of active products
- Gross margin
- Churn status

### Pricing Data

File: `data/price_data.csv`

This dataset contains historical pricing information, including:

- Price dates
- Variable electricity prices
- Fixed electricity prices
- Prices for different tariff periods

## Exploratory Data Analysis

The notebook covers:

1. Importing Python packages.
2. Loading the customer and pricing datasets.
3. Inspecting the first rows and dataset dimensions.
4. Reviewing data types, descriptive statistics, and unique values.
5. Checking for missing values.
6. Exploring categorical variables.
7. Analysing customer churn distribution.
8. Comparing numerical variables by churn status.
9. Visualising historical pricing distributions.
10. Examining pricing trends over time.
11. Summarising the main findings and limitations.

## Key Findings

The analysis shows that:

- The customer dataset contains 14,606 records and 26 variables.
- The data includes numerical, categorical, identifier, and date-related variables.
- No pandas-level missing values were identified in the customer dataset.
- Consumption and margin variables have different scales and varying degrees of skewness.
- Churn is a binary and imbalanced outcome.
- Approximately 9.7% of customers are classified as churned.
- Customer characteristics can be compared using consumption, tenure, product, and margin variables.
- Historical pricing data can be used to examine price distributions and changes over time.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure

```text
PowerCo/
├── data/
│   ├── client_data.csv
│   └── price_data.csv
├── notebooks/
│   └── EDA_BCG_Submission.ipynb
└── README.md
```

## Installation

Create a virtual environment and install the required packages:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install pandas matplotlib seaborn jupyter
```

If PowerShell prevents script execution, activate the environment using Command Prompt:

```cmd
.venv\Scripts\activate.bat
```

## Running the Notebook

From the project root, start Jupyter Notebook:

```powershell
jupyter notebook
```

Open the following file and run the cells in order:

```text
notebooks/EDA_BCG_Submission.ipynb
```

The notebook expects the datasets to be available at:

```text
data/client_data.csv
data/price_data.csv
```

## Future Work

Potential next steps include:

- Engineering additional customer and pricing features.
- Investigating the relationship between pricing and churn.
- Encoding categorical variables.
- Building classification models to predict churn.
- Evaluating models using precision, recall, F1-score, and ROC-AUC.
- Addressing class imbalance using suitable modelling techniques.
- Developing business recommendations from the model results.

## Scope and Limitations

This project focuses on exploratory data analysis and does not currently contain a production-ready churn prediction model. The observed relationships describe patterns in the data and should not be interpreted as causal.

No artificial imputation, row deletion, or outlier removal was performed during the initial analysis.