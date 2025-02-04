# Stock Data Analysis and Visualization

## Overview
This script fetches historical stock data from Yahoo Finance for a set of predefined companies, stores the data in an SQLite database, and visualizes stock prices and trading volumes using Plotly. It also calculates and plots moving averages to analyze trends over time.

## Prerequisites
Ensure you have the following Python libraries installed before running the script:

```sh
pip install pandas numpy yfinance sqlite3 matplotlib plotly
```

## Features
- Fetches 10 years of historical stock data for Google, Amazon, Microsoft, Tesla, and Facebook.
- Stores the stock data in an SQLite database.
- Retrieves data from the database and calculates:
  - 90-day and 180-day moving averages for stock prices.
  - 30-day moving average for trading volume.
- Plots stock price trends and trading volume trends using Plotly.

## Usage
1. Run the script to fetch and store stock data:
   ```sh
   python script.py
   ```
2. The script will generate interactive charts displaying stock prices, moving averages, and trading volume trends.
3. The stock data is stored in an SQLite database named `stock_data.db`.

## Code Breakdown
1. **Fetching Stock Data**
   - Uses `yfinance` to get stock history.
   - Converts data into a pandas DataFrame.
   - Stores the data in SQLite tables.

2. **Database Management**
   - Creates a table for each stock.
   - Stores stock data with columns: Date, Open, High, Low, Close, Volume.

3. **Data Analysis & Visualization**
   - Calculates moving averages (90-day, 180-day, 30-day for volume).
   - Plots stock prices with moving averages.
   - Plots trading volume with its 30-day moving average.

## Example Output
- Line chart of stock prices with 90-day and 180-day moving averages.
- Bar chart of trading volume with 30-day moving average.

## Notes
- Ensure an active internet connection for fetching stock data.
- If no data is available for a stock, it will be skipped with an error message.
- The SQLite database can be queried using standard SQL commands to analyze stock data further.

## License
This project is licensed under the MIT License.

