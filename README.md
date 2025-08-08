# KY Kindergarten Readiness Analysis

## Project Overview

This project looks at Kentucky county-level data for factors that can affect kindergarten readiness.
It uses three datasets:

County Health Rankings (children in poverty, high school completion)
Childcare subsidies
Graduation rates

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

**Rows**: 120 counties
**Columns**: 7 total after merging datasets
**Sources**: Mix of quantitative and qualitative data
**Example row**: `KY, Adair, 0.278, 0.857879, 2022, 253, 94.9`


## Data Sources

**County Health Rankings (National)** – [https://www.countyhealthrankings.org/](https://www.countyhealthrankings.org/)
**Children Receiving Childcare Subsidies (KY KIDS COUNT)** – [https://kyyouth.org/kids-count-data-center/](https://kyyouth.org/kids-count-data-center/)
**Cohort Graduation Rate** – [Kentucky Department of Education](https://education.ky.gov/)

## Project Objective

Look for patterns in how poverty, education levels, childcare access, and graduation rates vary between Kentucky counties.

## Setup Instructions

### 1. Clone the repository

git clone https://github.com/KCrowe03/KY-Kindergarten-Readiness.git

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

**Python** – Data cleaning and analysis
**Pandas** – Handling and merging datasets
**Matplotlib / Seaborn** – Data visualizations
**SQLite** – Stored cleaned data and joined tables for final dataset
**Jupyter Notebook** – Organizing analysis



## Feature Engineering & Functions

I created 4 functions to help prepare and format the data:

A function to check for missing values in any column
A function to format percentages as readable strings
A function to round values for easier chart labels
A function to calculate the range of childcare subsidies

## Database Integration

I saved each cleaned dataset as its own table inside a SQLite database (ky_readiness.db).

Then I used a SQL query to join the three tables into one final dataset:

chr = (poverty + high school data)
subsidies = (childcare subsidy numbers)
graduation = (high school grad rates)

This shows how data can be joined using SQL instead of just Python.



## Visualizations

I created 3 charts to help compare counties and spot trends:

1. A horizontal bar chart showing graduation rates by county
2. A vertical bar chart showing childcare subsidies by county
3. A scatter plot comparing child poverty and graduation rate


## Project Summary

This project looks at how three things connect to high school graduation in Kentucky:

Child poverty
High school completion
Childcare support

I used three public datasets, cleaned and combined them, then explored the data using SQL and Python. I made a few small functions to keep things organized and built simple charts to help others understand the data. This doesn’t prove cause and effect, but it helps show where counties may need more support.

## Next steps

I want to expand this project by adding a Kentucky map in Tableau with all 120 counties. I want to find more datasets that include FIPS codes so I can combine them more easily. 
One idea is to filter the childcare subsidies data and see if there’s a clear pattern with poverty levels, number of subsidies, and graduation rates.
I’m also interested in how Kentucky can better prepare children for kindergarten, and how universal childcare/Pre-K programs might connect to higher graduation rates. 






