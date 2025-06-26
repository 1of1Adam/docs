---
title: "Core trading concepts | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/"
extracted_at: "2025-06-22T09:15:58.687Z"
---

# Core trading conceptsTrading Platform provides the ability to trade right from the chart.
Users can manage orders, track positions, monitor their potential profits and losses, and more.
In this article, you will learn about the trading components, how they integrate into the chart widget, and how they work together.
## Components
Trading in Trading Platform is based on two key components: the [Broker API](#broker-api) and the [Trading Host](#trading-host).
The diagram below illustrates how these components should be integrated with the library and your backend server.

[![Diagram illustrating trading components](https://www.tradingview.com/charting-library-docs/img/trading-components-diagram-light.svg)](/charting-library-docs/img/trading-components-diagram-light.svg)

> **Info:** The *Backend trading server* and *Broker API* are the parts that you should implement.

### Broker API
The Broker API is a component that enables trading.
Its purpose is to connect TradingView charts with your trading logic.
In JavaScript terms, the Broker API is an object that implements a particular interface.
You can implement the Broker API through the [`IBrokerTerminal`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal) interface.

### Trading Host
The Trading Host is an API for interaction between the Broker API and the trading-related library code.
Its purpose is to receive information from your backend server where the trading logic is implemented and provide updates to the library.
The Trading Host is described by the [`IBrokerConnectionAdapterHost`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost) interface.
You should call the Trading Host methods from your [Broker API](#broker-api) implementation.
## How to enable trading
### Implement quote methods

> **Info:** To use Trading Platform, in addition to the [required](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods) Datafeed API methods, you should implement the quote-related methods.

- [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes)
- [`subscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribequotes)
- [`unsubscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#unsubscribequotes)

The library calls these methods to request [quotes](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/quotes), which are data sets that show the most recent bid and ask prices, opening and closing prices, price changes, and other market data.
Quotes are used in most Trading Platform features including the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket), [Legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend), and widgets, such as [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List), [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details), [News](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/news), and [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market).
### Connect Broker API
To enable trading, you should pass the function that returns a new object of the Broker API implementation to the library.
To do this, use the [`broker_factory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#broker_factory) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor#trading-platform-parameters).
Note that this function should accept the Trading Host instance as a parameter.
In the code sample below, the function assigned to `broker_factory` accepts `tradingHost` parameter,
which is an instance of [`IBrokerConnectionAdapterHost`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost).
This function returns an instance of `BrokerSample` that implements [`IBrokerTerminal`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal).
```
const datafeed = new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com");
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: datafeed,
    symbol: "AAPL",
    interval: "1D",
    broker_factory: function(tradingHost: IBrokerConnectionAdapterHost) { return new Brokers.BrokerSample(tradingHost, datafeed); },
})

```
## How library gets user's data
When the chart is initially loaded, the library requests data from your Broker API implementation through the following methods:

- [`orders`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#orders)
- [`positions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#positions)
- [`executions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#executions)
- [`individualPositions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#individualpositions) (optional, required if the [`supportPositionNetting`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpositionnetting) flag is set to `true`).

Using these methods, the library retrieves data about the orders, positions, and executions the user already had before the chart creation.
Then, the library gets updates for these orders and positions through the Trading Host methods.
Refer to the [next section](#how-components-work-together) for a step-by-step example.
## How components work together
To understand how the library, [Broker API](#broker-api), [Trading Host](#trading-host), and your implemented trading logic should work together,
consider the following step-by-step example.
Suppose a user wants to buy 10 AAPL shares.
This user action initiates three consecutive steps:
[![Diagram illustrating the action steps](https://www.tradingview.com/charting-library-docs/img/create-order-steps-diagram-light.svg)](/charting-library-docs/img/create-order-steps-diagram-light.svg)
In the subsequent sections, you will delve into each of these steps, finding detailed explanations and sequence diagrams:

- [Order creation](#1-order-creation)
- [Execution update](#2-execution-update)
- [Equity update](#3-equity-update)

You can also refer to the diagram that illustrates the entire process, starting from creating the order in the UI until the position is established.

Expand to view the diagram of the entire process.

[![Diagram illustrating the entire process of creating order](https://www.tradingview.com/charting-library-docs/img/create-order-complete-diagram-light.svg)](/charting-library-docs/img/create-order-complete-diagram-light.svg)
### 1. Order creation
The diagram below illustrates the process of creating an order.

[![Order creation diagram](https://www.tradingview.com/charting-library-docs/img/order-creation-diagram-light.svg)](/charting-library-docs/img/order-creation-diagram-light.svg)

- The user specifies 10 units of AAPL shares in the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) and clicks the *Buy* button.
- The library interprets this action as a trigger to notify your Broker API implementation that the user wants to create the order.
The library calls the [`placeOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#placeorder) method, passing along the order data.
The code sample below shows an example of the data object:
```
{
    "symbol": "NasdaqNM:AAPL",
    "type": 2,  // OrderType.Market
    "side": 1,  // Side.Buy
    "qty": 10,
    "currentQuotes": {
        "ask": 173.68,
        "bid": 173.68
    },
    "customFields": {}
}

```
Note that your Broker API implementation should interpret this call as a notification of the user's intent to create the order.
- Your Broker API implementation responds with [`PlaceOrderResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlaceOrderResult).
The library waits for your backend server to create the order within 10 seconds and provide the updated information.
Note that the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue) if it fails to receive a timely order update.
- Your Broker API implementation requests your backend server to create the order.
- Your backend server creates the order and prepares the updated information.
- Your backend server provides a response to your Broker API implementation with updated information.
Your Broker API implementation calls the [`orderUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) method.
As a parameter, it sends the [`PlacedOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder) object to the library.
Note that the `qty`, `id`, `symbol`, and `side` properties must be identical to the data provided in step 3 within the `placeOrder` method.

The code sample below shows an example of the `PlacedOrder` object:
```
{
    "id": "1",
    "qty": 10,
    "side": 1,   // Side.Buy
    "status": 6, // OrderStatus.Working
    "symbol": "NasdaqNM:AAPL",
    "type": 2    // OrderType.Market
}

```

> **Info:** Here, the object has a `status` property that indicates the order's current [status](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.OrderStatus).
Initially, when the order is created but has not been executed, it is assigned the *working* status.
Once the order is executed, its status should be updated to *filled*.
This will be done [further](#2-execution-update).

- The Trading Host receives updates and informs the library and the UI that the order has been created.
- The user sees the new working order in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).

After this, the backend server should [execute the working order](#2-execution-update) and add a new position.

### 2. Execution update
At this point, the user can see the new working order in the Account Manager.
Following this, your backend server is responsible for executing the order and creating a position.
The diagram below illustrates this process.
[![Execution update diagram](https://www.tradingview.com/charting-library-docs/img/execution-update-diagram-light.svg)](/charting-library-docs/img/execution-update-diagram-light.svg)

Your backend server executes the order and prepares the updated information.
Note that the order execution and update might be processed on external sources, such as exchanges.
However, your server is expected to manage this information and provide it in the format required by the library.
- Your backend server provides a response to your Broker API implementation with updated information.
Your Broker API implementation calls the [`executionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#executionupdate) method.
As a parameter, it sends the [`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Execution) object.
The code sample below shows an example of this object:
```
{
    "price": 173.68,
    "qty": 10,
    "side": 1,  // Side.Buy
    "symbol": "NasdaqNM:AAPL",
    "time": 1697032262341
}

```

Your Broker API implementation calls the [`orderUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) method to update the order status to *filled*.
As a parameter, your Broker API implementation sends the [`PlacedOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder) object.
The code sample below shows an example of this object:
```
{
    "id": "1",
    "qty": 10,
    "side": 1,    // Side.Buy
    "status": 2,  // OrderStatus.Filled
    "symbol": "NasdaqNM:AAPL",
    "type": 2,    // OrderType.Market
}

```

Your Broker API implementation calls the [`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method to notify the Trading Host that the position is added.
As a parameter, it sends the [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) object.
The code sample below shows an example of this object:
```
{
    "id": "NasdaqNM:AAPL",
    "qty": 10,
    "side": 1,  // Side.Buy
    "symbol": "NasdaqNM:AAPL",
    "avgPrice": 173.68
}

```

- The Trading Host receives updates and informs the library and the UI that the order has been executed and the position has been added.
- The user sees a new position of 10 AAPL shares in the Account Manager.

After this, your backend server should [update user's equity](#3-equity-update).

### 3. Equity update
At this stage, the user sees that the order has been executed and the position has been created.
Next, your backend server should update the user's equity and the Profit & Loss (P&L) values for all active positions whenever there is a price change.

> **Info:** To keep the UI data up-to-date, you should constantly provide updates of users' entity and P&L values whenever changes occur.

The diagram below illustrates the process of updating the equity and P&L values.

[![Equity update diagram](https://www.tradingview.com/charting-library-docs/img/equity-update-diagram-light.svg)](/charting-library-docs/img/equity-update-diagram-light.svg)

Your backend server calculates the user's equity and P&L and prepares the updated information.
Note that the calculations might be processed on external sources, such as exchanges.
However, your server is expected to manage this information and provide it in the format required by the library.
- Your backend server provides a response to your Broker API implementation with updated information.
Your Broker API implementation calls the [`equityUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#equityupdate) method to notify the Trading Host about equity updates.
As a parameter, it sends the accurate equity amount, for example, `[10000000]`.
- Your Broker API implementation calls the [`plUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#plupdate) method to notify the Trading Host about P&L updates.
- The Trading Host notifies the library and the UI about updates.
- The user sees updated equity and P&L values in the Account Manager.

At this stage, the user owns the position of 10 AAPL shares.

## Implementation example
You can reference the example of the Broker API implementation on GitHub.
However, the repository is private and requires you to [get access](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access) first.
The [Broker API example](https://github.com/tradingview/trading_platform/tree/master/broker-sample) 🔐 includes TypeScript source code, which can serve as a template for your implementation.
Note that this example does not establish a connection with an actual broker but simulates order and position management as a mock setup.
This implementation is also used on the [Trading Platform demo page](https://trading-terminal.tradingview-widget.com/) where you can experiment with various trading features.