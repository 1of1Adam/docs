---
title: "Glossary | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary"
extracted_at: "2025-06-22T09:13:53.530Z"
---

# GlossaryThis article contains terms that are used in the Advanced Charts documentation.

## Trading terms
### Bracket order
An [order](#order) that helps users limit their losses and secure their profits
by bracketing positions with two opposing [stop-loss](#stop-loss-order) and [take-profit](#take-profit-order) orders.
Refer to [Bracket orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/brackets) for more information.
### Execution
The completion of a buy or sell order for a financial instrument. An execution involves matching a buyer and a seller and transferring ownership of the financial instrument.

### Individual position
The amount of a singular holding or investment in a financial instrument.

### Limit order
An [order](#order) to buy or sell a financial instrument when a given or better price is reached.
This order type guarantees a specific price but does not guarantee immediate execution.
### Limit price
The maximum price a buyer is willing to pay or the minimum price a seller is willing to accept.

### Market order
An [order](#order) to buy or sell a financial instrument at the current market price.
This order type guarantees immediate execution but does not guarantee a specific price.
### Net position
The difference between an investor's total number of open long and short positions at any given time.

### Order
A request made by a trader to buy or sell a financial instrument at a specified price and quantity. An order can have various attributes, such as a [limit price](#limit-price), [stop price](#stop-price), and [duration](#order-duration). Depending on whether an order has been executed or not, it can be in various statuses such as canceled, filled, placing, or rejected.
Refer to [Orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/orders) for more information.
### Order duration
The time during which an order remains active.

### Pip
The minimum price movement for Forex symbols. For more information on how to display pips, refer to the [Price format](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#how-to-display-pips) section.

### Position
The amount of a financial instrument held by an investor.
For more information, refer to [Positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
### Position netting
The process of aggregating multiple individual positions for one symbol into a single net position.
For more information, refer to [Position netting](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#position-netting).
### Quotes
Real-time price information for financial instruments, including the most recent bid and ask prices, opening and closing prices, price changes, and other market data.
Refer to [Quotes](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/quotes) for more information.
### Stop-loss order
A type of [order](#order) designed to limit losses by automatically closing a position at a given price when it moves unfavorably.

### Stop order
An [order](#order) to buy or sell a financial instrument at the market price as soon as it reaches a certain level.

### Stop price
A trigger price at which an order becomes a market or limit order.

### Take-profit order
A type of [limit order](#limit-order) that closes a position at a specific price to secure a profit.

### Tick
The minimum price movement.

## Technical terms
### Datafeed
A middleware that requests data from a server and sends it to the library. Refer to the [Connecting data](https://www.tradingview.com/charting-library-docs/latest/connecting_data/) article for more information.

### Date range
A period of time that is currently visible on the chart canvas. This range changes when users scale the chart. Refer to [Time scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale#time-frame-toolbar) for more information.

### Featureset
A toggle that allows you to enable or disable a certain feature. Refer to the [Featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets) article for more information.

### Pane
An area on the chart where a [series](#series) or [indicator](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/) is displayed. The picture below shows the red pane with the main series and the green pane with the indicator.

![Chart panes](https://www.tradingview.com/charting-library-docs/assets/images/pane-d44d70e4c4be2d846c4ecdd789fc0e17.png)
### Plot
A line or area that represents indicator values on a chart.

### Series
A collection of data points that represents a specific metric over time. A series can be of different styles that affect how data is displayed on the chart. Refer to [Chart styles](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/chart-overrides#chart-styles) for more information.

### Source symbol
A symbol that is used as a data source for a certain indicator. The indicator calculates its own data based on the symbol's data.

### Spread operators
Operators that allow comparison between a financial instrument, such as a stock,
and an additional variable, such as another financial instrument or a numerical value.
Spread operators can be enabled in the [Search Symbol](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Search#enable-spread-operators)
and [Compare Symbol](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/#enable-spread-operators) dialogs.