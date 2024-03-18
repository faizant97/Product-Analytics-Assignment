# Uber Wait Time Analysis

This project focuses on analyzing the impact of extending wait times on Uber's Express POOL service. The goal is to understand how extending wait times from 2 minutes to 5 minutes affects various metrics such as rider cancellations, driver payouts, and the overall efficiency of trip matching during commuting and non-commuting hours.

## Dataset Description

The dataset, `DataSetUber.xlsx`, contains real-world data collected from Uber's operations. It includes several key metrics such as wait times, trip matching effectiveness, rider cancellations, driver payouts, and trip types categorized into commuting and non-commuting hours.

### Columns in the Dataset

- `period_start`: The start time of the data collection period.
- `treat`: Indicates if the observation is from the control group (2-minute wait, `False`) or the treatment group (5-minute wait, `True`).
- `commute`: Indicates if the trip occurred during commuting hours (`True`) or non-commuting hours (`False`).
- `wait_time`: The wait time experienced by riders.
- Other metrics include `trips_pool`, `trips_express`, `rider_cancellations`, `total_driver_payout`, `total_matches`, and `total_double_matches`.

## Analysis Overview

The analysis involves several key steps:

1. **Data Preparation**: Loading the dataset and preparing it for analysis, including converting string-formatted wait times into numeric values.
2. **Grouping Data**: Segregating the dataset into control and treatment groups, further divided into commuting and non-commuting hours.
3. **Statistical Analysis**: Conducting statistical tests to estimate the effects of extended waiting times on the defined metrics.

## Getting Started

### Prerequisites

Ensure you have Python installed on your system along with the following libraries:
- pandas
- numpy
- statsmodels (for regression analysis)

You can install these libraries using pip:

```sh
pip install pandas numpy statsmodels
```

### Instructions

1. **Load the Dataset**: Start by loading the `DataSetUber.xlsx` file. Use the `pandas` library to read the data from the relevant sheet.

```python
import pandas as pd

file_path = "<localpath/DataSetUber.xlsx"
df = pd.read_excel(file_path, sheet_name="Switchbacks")
```

2. **Prepare the Data**: Convert `wait_time` to a numeric column and filter the data based on treatment/control groups and commuting times.

3. **Conduct Analysis**: Perform your analysis to understand the impact of wait times. This may involve calculating mean differences, conducting regression analysis, and interpreting the results.

4. **Results Interpretation**: Summarize the findings from your analysis, focusing on the implications of extending wait times on Uber's operational metrics.

## Contributing

Feel free to fork this project and submit pull requests with enhancements or additional analyses. For major changes, please open an issue first to discuss what you would like to change.



