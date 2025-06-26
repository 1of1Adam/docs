---
title: "How to enable debug mode | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/tutorials/enable-debug-mode"
extracted_at: "2025-06-22T09:16:24.172Z"
---

# How to enable debug modeThis article will guide you through enabling debug mode in the library.
This feature provides detailed logs and error messages in the browser's Developer Tools, helping you identify issues and ensure your application runs smoothly.
The library offers two debug options:

- Logging messages related to [connecting data](#enable-debug-mode-for-data-connection) using the Datafeed API.
- Logging messages related to [trading features](#enable-debug-mode-for-trading) in the Trading Platform.

## Enable debug mode for data connection
The [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) is a set of methods that allow you to connect market data to the library.
The debug mode in the Datafeed API is useful for identifying how the library loads, processes, and resolves data.
You can also check the number of bars requested versus the number of bars received.
You can enable the debug mode in two ways:

Set the [`debug`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#debug) property to `true` in the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).

```
const datafeed = new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com");
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: datafeed,
    symbol: "AAPL",
    interval: "1D",
    debug: true,
})

```

Call the [`setDebugMode`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#setdebugmode) method after the chart is initialized.

```
var widget = window.tvWidget = new TradingView.widget({ /* Widget Constructor properties */});

widget.onChartReady(() => {
    widget.setDebugMode(true);
});

```

Once the debug mode is enabled and you [run your app](https://www.tradingview.com/charting-library-docs/latest/tutorials/First-Run-Tutorial), you can access the console logs in the Developer Tools of your browser.
Below is an example of the generated logs.
```
2024-08-20T13:36:56.244Z Symbol resolve requested: `AAPL`
2024-08-20T13:36:56.504Z FEED [AAPL|1D]: Processing pending subscribers, count=2
2024-08-20T13:36:56.504Z FEED [AAPL|1D]: Leftmost subscriber requires 329 bars prior 2024-08-20T00:00:00.000Z
2024-08-20T13:36:56.505Z FEED [AAPL|1D]: Requesting data: [2023-05-18T00:00:00.000Z ... 2024-08-21T00:00:00.000Z, 330 bars]
2024-08-20T13:36:56.735Z FEED [AAPL|1D]: Receiving bars: total 330 bars in  [2016-11-30T00:00:00.000Z ... 2018-03-27T00:00:00.000Z], requested range: [2023-05-18T00:00:00.000Z ... 2024-08-21T00:00:00.000Z, 330 bars]

```
## Enable debug mode for trading
If you are working with [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/), you can also enable the debug mode for the trading part of your implementation.
This mode allows you to check which methods are triggered based on user actions, what data the library sends, and what it expects to receive.
Trading is based on two key components: the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) and the [Trading Host](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#trading-host).
The Broker API acts as a bridge between the library and your backend trading server, transmitting data between them.
The Trading Host provides the library with updates that it did not request, but these updates are necessary to display up-to-date information.
Therefore, the debug mode in trading offers several options, allowing you to choose which logs you want to see.
To enable debug mode, use the [`debug_broker`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#debug_broker) property in the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
You can set this property to one of the debug levels defined by the [`BrokerDebugMode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#brokerdebugmode) type:

- `all`: logs all possible debug messages.
- `broker-only`: logs only messages related to the Broker API.
- `host-only`: logs only messages related to the Trading Host.
- `normal`: logs messages for the Broker API and Trading Host but excludes frequently called methods, such as `connectionStatus`.

In the example below, the debug mode enables messages related to the Broker API.

```
const datafeed = new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com");
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: datafeed,
    symbol: "AAPL",
    interval: "1D",
    debug_broker: "broker-only",
})

```
Once the debug mode is enabled and you [run your app](https://www.tradingview.com/charting-library-docs/latest/tutorials/First-Run-Tutorial), you can access the console logs in the Developer Tools of your browser.
Below is an example of the generated logs.
```
2024-08-22T09:18:12.344Z Broker API   | id: 1 | method: placeOrder | CALLED with arguments: [{"symbol":"AAPL","type":2,"qty":100,"side":1,"seenPrice":173.68,"currentQuotes":{"ask":173.68,"bid":173.68},"stopType":0,"customFields":{}},null]
2024-08-22T09:18:12.344Z Broker API   | id: 1 | method: placeOrder |  RETURNED (async): {}

```
## What's next?
If you plan to connect data, we recommend reading the following articles:

[How to connect data via Datafeed API](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/).
Learn how to implement datafeed, display historical data, and stream real-time data via WebSocket.
[Datafeed: common issues](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues).
Explore detailed explanations and solutions for the most common issues that you may encounter when implementing the Datafeed API.

If you plan to implement trading features in Trading Platform, we recommend reading the following articles:

[Core trading concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/).
Learn about the trading components, how they integrate into the chart widget, and how they work together.
[Common Broker API issues](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues).
Explore detailed explanations and solutions for the most common issues that you may encounter when implementing the Broker API.