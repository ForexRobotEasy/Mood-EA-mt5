# Mood EA mt5

This code is a sample implementation of the Mood EA trading strategy for MetaTrader 5 (MT5) platform. The Mood EA strategy is developed by the Forex Robot Easy Team, and more information about this strategy can be found on their website [forexroboteasy.com](https://forexroboteasy.com).

## Strategy Description

The Mood EA strategy is based on the concept of trader momentum. It uses the Momentum indicator to identify oversold and overbought conditions in the market. When the momentum value exceeds a certain threshold, the strategy opens a sell order, and when the momentum value falls below a certain threshold, the strategy opens a buy order.

## Required Libraries

This code requires the following libraries to be included:

- Trade.mqh: This library provides functions for trading operations.
- PositionInfo.mqh: This library provides functions to retrieve information about open positions.
- Momentum.mqh: This library provides functions to calculate the Momentum indicator.

## Constants

The code defines a constant `RISK_PERCENTAGE` which represents the risk percentage for drawdown management. This constant can be adjusted to control the level of risk in the trading strategy.

## Objects Initialization

The code initializes two objects:

- `CTrade trade`: This object is used for trading operations.
- `CMomentum momentum`: This object is used to calculate the Momentum indicator.

## OnTick Function

The `OnTick` function is the main entry point of the trading strategy and is called on every tick of the market. It performs the following steps:

1. Calculates the current momentum value using the `iMomentum` function from the `momentum` object.
2. Checks if the current momentum value is greater than 70. If true, it opens a sell order.
3. Calculates the lot size based on the risk percentage, account balance, and tick value.
4. Executes the sell order using the `Sell` function from the `trade` object.
5. Checks if the current momentum value is less than 30. If true, it opens a buy order.
6. Calculates the lot size based on the risk percentage, account balance, and tick value.
7. Executes the buy order using the `Buy` function from the `trade` object.

## OnDeinit Function

The `OnDeinit` function is called when the EA is stopped or removed from the chart. It provides contact information for settings and personal bonus. The contact information for the Forex Robot Easy Team is mentioned as 'info@forexroboteasy.com'. Users can contact them for more information and personal bonus.

## Product Description

This code represents a sample implementation of the Mood EA trading strategy. It is designed to harness trader momentum and identify oversold and overbought conditions in the market. The strategy opens sell orders when the momentum value exceeds 70 and opens buy orders when the momentum value falls below 30. The lot size for each order is calculated based on the risk percentage, account balance, and tick value.

Please note that ForexRobotEasy is not the official developer of this product. This code is provided as a sample that can work as described in the official product. To find the official developer of this product, please refer to the MQL5 platform.

For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/mood-ea-mt5-review-harnessing-trader-momentum/).
