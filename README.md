# Trade Assistant Panel ReadMe

This ReadMe file provides an overview of the code for the Trade Assistant Panel, developed by the Forex Robot Easy Team. Please note that ForexRobotEasy is not the official developer of this product. We are only providing a sample code that can work as described in the product.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/trade-assistant-panel-review-simplify-your-forex-trading-strategy/).

## Code Description

The Trade Assistant Panel is a trading panel that allows users to execute various types of market orders and manage open positions. The panel provides buttons for buying, selling, buying stop, buying limit, selling stop, and selling limit. It also includes an editable field to input the order ticket number for modifying existing positions.

The code is written in MQL5 and requires the following libraries and classes:

- Trade.mqh: Provides the necessary functions for trading operations.
- Button.mqh: Defines the CButton class for creating buttons.
- Edit.mqh: Defines the CEdit class for creating editable fields.

The global variables defined in the code include:

- trade: An instance of the CTrade class for performing trading operations.
- buyButton, sellButton, buyStopButton, buyLimitButton, sellStopButton, sellLimitButton: Instances of the CButton class for creating buttons.
- ticketEdit: An instance of the CEdit class for creating an editable field.

The code initializes the Trade Assistant Panel in the OnInit() function. It creates the buttons and sets their OnClick events to the respective functions.

The OnBuyButtonClick() function handles the buy button click event. It retrieves the current ask price and uses the trade.Buy() function to execute a buy order with a fixed lot size of 0.01.

Similarly, the OnSellButtonClick() function handles the sell button click event. It retrieves the current bid price and uses the trade.Sell() function to execute a sell order with a fixed lot size of 0.01.

The OnBuyStopButtonClick() function handles the buy stop button click event. It retrieves the current bid price and calculates the stop price as the current price plus 10 times the minimum price change (Point). It then uses the trade.BuyStop() function to execute a buy stop order with a fixed lot size of 0.01 and the calculated stop price.

The OnBuyLimitButtonClick() function handles the buy limit button click event. It retrieves the current ask price and calculates the limit price as the current price minus 10 times the minimum price change (Point). It then uses the trade.BuyLimit() function to execute a buy limit order with a fixed lot size of 0.01 and the calculated limit price.

The OnSellStopButtonClick() function handles the sell stop button click event. It retrieves the current ask price and calculates the stop price as the current price minus 10 times the minimum price change (Point). It then uses the trade.SellStop() function to execute a sell stop order with a fixed lot size of 0.01 and the calculated stop price.

The OnSellLimitButtonClick() function handles the sell limit button click event. It retrieves the current bid price and calculates the limit price as the current price plus 10 times the minimum price change (Point). It then uses the trade.SellLimit() function to execute a sell limit order with a fixed lot size of 0.01 and the calculated limit price.

The OnTick() function is triggered on every tick and is used to update the order information. It retrieves the order ticket number from the ticketEdit field and checks if it is not zero. If the ticket is valid, it retrieves the current bid price and uses the trade.ModifyPosition() function to modify the position with the specified ticket and the current price.

The OnDeinit() function is triggered on deinitialization and is used to close all open positions. It uses the trade.CloseAll() function to close all open positions.

## Product Description

The Trade Assistant Panel is a powerful tool designed to simplify forex trading strategies. Developed by the Forex Robot Easy Team, this panel allows traders to execute market orders with ease and manage their open positions effectively.

With the Trade Assistant Panel, traders can quickly execute buy and sell orders with a fixed lot size of 0.01. It also provides additional functionalities such as buy stop, buy limit, sell stop, and sell limit orders, allowing traders to implement more advanced trading strategies.

The panel is equipped with user-friendly buttons and an editable field to input the order ticket number for modifying existing positions. Traders can easily modify their positions by specifying the desired price and using the ModifyPosition function.

Please note that this code is a sample provided by ForexRobotEasy and is not the official developer of the Trade Assistant Panel. To find the official developer and more information about this product, please refer to the MQL5 platform.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/trade-assistant-panel-review-simplify-your-forex-trading-strategy/).
