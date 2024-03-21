# Uber Rideshare Data Analysis

## Overview

This project involves the analysis of Uber rideshare data using Python and pandas. The dataset contains information about over 693,000 rides with 57 different attributes.

## Dataset

### Loading the Dataset

```python
import pandas as pd

# Load the dataset
uber = pd.read_csv(r"rideshare_kaggle.csv")

# Display basic information about the dataset
print(uber.shape)
print(uber.head())
```

### Filtering by Ride Name

```python
# Filtering through the 'name' column
ride_name_counts = uber['name'].value_counts()
print(ride_name_counts)

# Creating a new DataFrame with selected ride names
selected_ride_names = ['Shared', 'UberPool', 'Black SUV', 'UberX', 'Taxi', 'Lux']
new_uber = uber[uber['name'].isin(selected_ride_names)]
print(new_uber.head())
```

### Dataset After Filtering

```python
# Display information about the new DataFrame
print(new_uber.shape)
```

### Saving Filtered Dataset to CSV

```python
# Save the filtered dataset to a new CSV file
new_uber.to_csv(r'D:\ML training\python\data2.csv', index=False)
```

## Project Structure

- **Data Exploration**: Initial exploration of the dataset.
- **Data Cleaning**: Handling missing values, outliers, and any data preprocessing.
- **Analysis**: In-depth analysis of ride data, including patterns, trends, and insights.
- **Visualization**: Visual representations of key findings using matplotlib or other libraries.
- **Conclusion**: Summarize the key findings and insights from the analysis.

## Files

- **rideshare_kaggle.csv**: Original dataset.
- **data2.csv**: Filtered dataset containing selected ride names.

## Dependencies

- pandas
- matplotlib (for data visualization)

## How to Use

1. Clone the repository to your local machine.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Run the Jupyter notebooks or Python scripts to reproduce the analysis.

## Contribution Guidelines

Feel free to contribute by submitting bug reports, feature requests, or pull requests. Ensure code follows PEP 8 standards.

