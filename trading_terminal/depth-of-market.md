---
title: "Depth of Market | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market"
extracted_at: "2025-06-22T09:16:07.194Z"
---

# Depth of Market## Overview
The **Depth of Market** (DOM) widget allows users to see the volume of bids and asks for an asset at different prices.
The widget supports frequent data updates, giving users a comprehensive view of supply and demand.
![DOM widget](https://www.tradingview.com/charting-library-docs/assets/images/dom-widget-static-3ee73e53b032e32a6c8bfeb7419cd496.png)

> **Tip:** You can find more information about interacting with the widget's UI in the [Depth of Market: what it is and how traders can use it](https://www.tradingview.com/support/solutions/43000516459-depth-of-market-dom-what-it-is-and-how-traders-can-use-it/) article.

## Connect widget

> **Info:** This widget is part of the [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).
Trading on the platform relies on two key components: the Broker API and the Trading Host.
Before implementing this widget, ensure that you have implemented the required Broker API methods.
We recommend reading the [Core concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/) section for a better understanding.

### 1. Provide data
The DOM widget displays data in static mode.
This means that the price series is fixed, while the current price moves within, above, or below the designated range.
The widget sources its data from the [`DatafeedQuoteValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedQuoteValues) and [`DOMData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DOMData) objects.
To provide this data, you need to implement the following [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) methods:

- [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes)
- [`subscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribequotes)
- [`unsubscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#unsubscribequotes)
- [`subscribeDepth`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribedepth)
- [`unsubscribeDepth`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#unsubscribedepth)

### 2. Enable the widget

- Add the [`dom_widget`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#dom_widget) featureset to the [`enabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#enabled_features) array of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) object.
Set the [`supportLevel2Data`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportlevel2data) flag, which enables [Level 2](https://www.investopedia.com/terms/l/level2.asp) data, to `true`.
Refer to the [Trading features configuration](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/trading-features-configuration) section for more information about configuration flags.
Implement the [`cancelOrders`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#cancelorders) method within your [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) implementation.
This method is required for the DOM widget.

### Example
The CodePen example below demonstrates how to enable the DOM widget in the UI
and implement [`subscribeDepth`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribedepth) and [`unsubscribeDepth`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#unsubscribedepth) to populate the DOM with fake data.
Since the DOM is supported only on larger viewports, it will not be displayed within the iframe below.
We recommend clicking the *Edit on CodePen* button to view the full example on CodePen, where the DOM widget is visible.
To open the DOM, click the *Trade* button in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).
See the Pen 
Trading Platform. Implement Depth of Market  by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
## Display DOM on start
If you want to display the DOM widget when a user opens the chart for the first time,
add the [`show_dom_first_time`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#show_dom_first_time) featureset to the [`enabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#enabled_features) array of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) object.