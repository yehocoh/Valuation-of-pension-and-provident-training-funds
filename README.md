# Valuation-of-pension-and-provident-training-funds
Valuation of funds, based on the published individual asset report

# README for ISIN Data Processing

This README provides an overview of the Python code and functions used for processing ISIN data. The code is designed to extract and manipulate financial data related to various securities using Python libraries such as pandas, openpyxl, and yfinance.

## Code Overview

### Retrieving Stock Information by ISIN
- The script uses the `yfinance` library to retrieve stock information based on the ISIN (International Securities Identification Number).
- It demonstrates how to fetch stock information for a specific ISIN and print details like the stock name and price.

### Processing Stock Data from Excel Files
- The code defines functions to process data from Excel files containing stock information.
- The `process_workbook` function reads data from an Excel workbook and returns a DataFrame with specific columns.
- The `process_folder` function processes multiple Excel files within a folder and combines the data into a single DataFrame.

### Processing Mutual Fund Data from Excel Files
- Similar to stock data, the code also includes functions to process mutual fund data from Excel files.
- The `process_workbook_2` and `process_folder_2` functions handle mutual fund data processing.

### Data Cleaning and Transformation
- The code renames columns, converts data types, and filters rows based on specific criteria to clean the data.
- It ensures that ISIN codes are valid (length 12) and filters out rows with missing or empty ISIN values.

### Retrieving Stock Prices by ISIN
- The script attempts to retrieve stock prices for a list of unique ISIN codes using `yfinance`. It handles cases where the stock price data may not be available.

### Currency Conversion
- The code converts non-USD currency values to USD for calculating the current portfolio value.
- It uses exchange rate data from Yahoo Finance to perform the conversion.

### Calculating Portfolio Value and Differences
- The script calculates the current portfolio value and the differences (gap) between the reported and updated portfolio values.

### Summary Table Generation
- The code generates a summary table that aggregates data by company number, fund type, year, and quarter.
- It provides a summary of portfolio values, gaps, and other relevant metrics.

## How to Use
1. Ensure you have the required Python libraries (`yfinance`, `openpyxl`, `pandas`) installed.
2. Modify the code to specify the path to your Excel data files and the desired sheets for processing.
3. Run the Python script in your preferred development environment.

## Example Data
- The code includes an example dataset for demonstration purposes. You can replace this with your own data by modifying the `folder_path` variable.

## Output
- The code generates summary tables and prints them to the console, providing insights into portfolio values, gaps, and other relevant metrics.

Feel free to adapt and use this code to process ISIN data for your specific needs.
