# KY Kindergarten Readiness Analysis

## Project Overview

This project looks at Kentucky county-level data for factors that can affect kindergarten readiness.
It uses three datasets:

* County Health Rankings (children in poverty, high school completion)
* Childcare subsidies
* Graduation rates

The goal is to see how these factors compare between counties.


## Data Dictionary

| Column               | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| state                | State abbreviation (KY for all rows)                                        |
| county               | County name in Kentucky                                                     |
| child\_poverty\_pct  | Percent of children living in poverty (decimal format, e.g., 0.278 = 27.8%) |
| hs\_completion\_pct  | Percent of adults with a high school diploma or higher (decimal format)     |
| year                 | Year of the childcare subsidies data                                        |
| childcare\_subsidies | Number of children receiving childcare subsidies                            |
| grad\_rate           | High school graduation rate (percent)                                       |


## Data Summary

* **Rows**: 120 counties
* **Columns**: 7 total after merging datasets
* **Sources**: Mix of quantitative and qualitative data
* **Example row**: `KY, Adair, 0.278, 0.857879, 2022, 253, 94.9`


## Data Sources

* **County Health Rankings (National)** – [https://www.countyhealthrankings.org/](https://www.countyhealthrankings.org/)
* **Children Receiving Childcare Subsidies (KY KIDS COUNT)** – [https://kyyouth.org/kids-count-data-center/](https://kyyouth.org/kids-count-data-center/)
* **Cohort Graduation Rate** – [Kentucky Department of Education](https://education.ky.gov/)
## Project Objective

Look for patterns in how poverty, education levels, childcare access, and graduation rates vary between Kentucky counties.

## Setup Instructions

### 1. Clone the repository

git clone <your_repo_url>
cd KY-Kindergarten-Readiness

### 2. Create and activate a virtual environment

python -m venv venv
# On Windows
venv\Scripts\activate
# On Mac/Linux
source venv/bin/activate

### 3. Install dependencies


pip install -r requirements.txt

### 4. Open the notebook

jupyter notebook notebooks/analysis.ipynb

## Technologies Used

* **Python** – Data cleaning and analysis
* **Pandas** – Handling and merging datasets
* **Matplotlib / Seaborn** – Data visualizations
* **SQLite** – Storing and joining cleaned data (to be added)
* **Jupyter Notebook** – Organizing analysis


## Feature Engineering & Functions


## Database Integration



## Visualizations



## Project Summary




