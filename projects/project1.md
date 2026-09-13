## Project 1

### Research Question
How is median household income associated with broadband subscription rates across North Carolina counties?
### Dataset
The dataset comes from the U.S. Census Bureau’s 2024 American Community Survey (ACS) 5-Year Estimates through the Census API and contains county-level data for North Carolina, with each row representing a county and including median household income, broadband subscription rates, and computer ownership percentages.
### Variables 
- **Median Household Income:** the income (in dollars)  for each North Carolina county.
- **Broadband Subscription Rate:** the percentage of households in each county with a broadband internet subscription.

### Data Cleaning and Preparation

I used pandas to prepare the data for analysis.

```python
target_cols = ["Median_Household_Income", "Pct_Broadband", "Pct_Computer"]
df[target_cols] = df[target_cols].apply(pd.to_numeric, errors="coerce")
df = df.dropna(subset=target_cols)
### Visualizations

The project includes a scatterplot examining the relationship between median household income and broadband subscription rates, as well as a histogram showing the distribution of broadband subscription rates across North Carolina counties.

### Source
U.S. Census Bureau — 2024 American Community Survey (ACS) 5-Year Estimates.

