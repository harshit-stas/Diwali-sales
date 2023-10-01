# Outlier Analysis

This project provides a script for performing an outlier analysis on a dataset. The script loads a dataset, cleans it, performs an outlier analysis on a specified column, and removes the outliers.

## Dependencies

This project requires the following Python libraries:

- pandas
- numpy
- sklearn
- seaborn
- matplotlib
- scipy

## Usage

1. Define the file path and encoding for your dataset in the `main` function.
2. Specify the column you want to perform an outlier analysis on in the `outliers_analysis` function.
3. Run the script.

The script will load your dataset, clean it, perform an outlier analysis on the specified column, and remove the outliers. It will then create a box plot of the specified column both before and after removing the outliers.

## Functions

- `load_data(file_path, encoding)`: Loads a CSV file from a specified file path and returns it as a pandas DataFrame.
- `clean_data(data)`: Fills missing values in the 'Amount' column with the mean of the column and drops the 'Status' and 'unnamed1' columns.
- `outliers_analysis(data, column)`: Creates a boxplot for the specified column, calculates the first quartile (Q1), third quartile (Q3), and interquartile range (IQR) of the column, identifies any values that are below Q1 - 1.5*IQR or above Q3 + 1.5*IQR as outliers, prints the range of these outlier values, creates a plot with annotations for each outlier, removes the outliers from the dataset, and returns a new DataFrame that doesn't include these outliers.
- `main()`: Calls these functions in sequence to load the data, clean it, perform an outlier analysis on the 'Amount' column, and remove the outliers.

## Note

Removing outliers can sometimes result in loss of information. It's important to understand why an outlier has occurred before deciding to remove it.
