# About this folder

- This is a folder for the backtrader beginner, which is also my learning path. 
- All the scripts in this folder are from the [Quickstart](https://www.backtrader.com/docu/quickstart/quickstart/) page.

# How Backtrader work?

- Initialization Cerebro
    - Create Cerebro engine by `bt.Cerebro()`, which is the core part of Backtrader. It is responsible for coordinating the entire backtesting process.
    - After creating Cerebro engine, we can configure the initial capital, commission rate and so on.
- Data Loading and Preprocessing
    - Backtrader will load the history data from data feed and perform some preprocessing, such as data cleaning and format conversion.
- initialization Strategy
    - Using `cerebro.add()` method, adding the strategy into Cerebro.
    - Cerebro will instantiate the strategy class and call the init function.
- Backtest Loop 
    - Backtrader will traverse historical data in chronological order, in each time step, it will:
        - Renew the data: giving the data to the stratetgy
        - using the next function
        - if there is order, Broker will deal with the order and simulate the trading process


# Tips

- Pay attention to the Adj Close