# Module_5_API_Assignment
Personal finance planner that will allow users to visualize their savings composed by investments in shares and cryptocurrencies to assess if they have enough money as an emergency fund.

## Working Parameters
average_household_income = 12000
btc_investment = 1.3
eth_investment = 5.2
my_agg = 200
my_spy = 50

## APIs used for Analysis
https://api.alternative.me/v2/ticker/Bitcoin/?convert=CAD
https://api.alternative.me/v2/ticker/Ethereum/?convert=CAD
https://github.com/alpacahq/alpaca-py

Note: There are other functions available to automate the processes including == Trading Client == with orders posting. :construction_worker:

## Libraries used in code

os - Access the env file
requests - Access APIs
pandas as pd - Data Frames
dotenv import load_dotenv - Access the env file
alpaca_trade_api as tradeapi - Access Alpaca SDK
MCForecastTools import MCSimulation - Monte Carlo Simulations
json - Access and manage Json responses

## Key Functions Demostrated
1. load_dotenv()
2. json.dumps(response_data_btc, indent=4)
3. os.getenv("ALPACA_API_KEY")
4. REST(
    alpaca_api_key,
    alpaca_secret_key,
    api_version="v2")
5. alpaca.get_bars(
    tickers,
    timeframe,
    start = today,
    end = today
).df
6. df_savings.plot(kind='pie',y='amount')
7. start_date = pd.Timestamp("2017-09-20", tz="America/New_York").isoformat()
8. MC_thirtyyear = MCSimulation(
    portfolio_data = df_ticker,
    weights = [.40,.60],
    num_simulation = 500,
    num_trading_days = 252*30
) 
9. MC_thirtyyear.calc_cumulative_return()
10. MC_thirtyyear.plot_simulation()
11. MC_thirtyyear.plot_distribution()
12. MC_thirtyyear.summarize_cumulative_return()

## RESULT OF ACTIVITY
### Portfilio Analysis
The current value of your 1.3 BTC is $32963.48
The current value of your 5.2 ETH is $9038.75
The total invesment value is $42002.23
The current value of your 50 SPY shares is $18711.00
The current value of your 200 AGG shares is $19500.00
Your total profolio saving is $80213.23
Congratulations! You have enough money in your emergency fund.

### 30 year Monte Carlo Simulation
Initial Investment = 20,000
Weights 40% Bonds 60% Shares
There is a 95% chance that an initial investment of $20000 in the portfolio over the next 30 years will end within in the range of $21375.83 and $282550.64

Initial Investment = 30,000
Weights 40% Bonds 60% Shares
here is a 95% chance that an initial investment of $30000.0 in the portfolio over the next 30 years will end within in the range of $32063.75 and $423825.95

### 5 year Monte Carlo Simulation
Initial Investment = 50000
Weights 20% Bonds 80% Shares
There is a 95% chance that an initial investment of $50000 in the portfolio over the next 5 years will end within in the range of $35180.69 and $151313.12

### 10 year Monte Carlo Simulation
Initial Investment = 95000
Weights 5% Bonds 95% Shares
There is a 95% chance that an initial investment of $95000 in the portfolio over the next 10 years will end within in the range of $54848.91 and $671379.5




