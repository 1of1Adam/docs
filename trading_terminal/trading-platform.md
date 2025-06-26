---
title: "Trading Platform | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/"
extracted_at: "2025-06-22T09:15:56.732Z"
---

# Trading Platform## Overview
[Trading Platform](https://github.com/tradingview/trading_platform) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)) is a standalone client-side solution that provides trading capabilities. Trading Platform is based on [Advanced Charts](https://www.tradingview.com/charting-library-docs/latest/getting_started/#what-is-advanced-charts) and contains all its [features](https://www.tradingview.com/charting-library-docs/latest/getting_started/Key-Features#advanced-charts-features).

If you already use Advanced Charts and want to get started with Trading Platform, refer to the [How to migrate from Advanced Charts](#how-to-migrate-from-advanced-charts) guide. Otherwise, you should refer to [Quick start](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start) to start the implementation from scratch.

[View Trading Platform demo](https://trading-terminal.tradingview-widget.com/)
## Trading Platform features
### Multiple-chart layout
Users can display up to 8 charts on one layout using the *Select Layout* button on the top toolbar.
Charts can be synchronized by a symbol, [interval (resolution)](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution), crosshair, time, and [date range](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#date-range).
![Multiple-chart layout](https://www.tradingview.com/charting-library-docs/assets/images/multiple-chart-layout-ea1fb3b94a8fb86aa8517602c4100752.png)
Selecting multiple-chart layouts is enabled by default.
If you want to disable this option,
add the [`header_layouttoggle`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#header_layouttoggle) and [`support_multicharts`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#support_multicharts) featuresets to the [`disabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#disabled_features) array of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
### Chart trading
Orders, positions, potential income and loss are displayed on the chart in Trading Platform. Users can place orders right from the chart. To enable chart trading, implement the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api). Then use the [`broker_factory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#broker_factory) method in [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) to pass the implementation to the library.

![Chart trading feature](https://www.tradingview.com/charting-library-docs/assets/images/trading-cap-a59edb8c88791854ce7dbc450ae38929.png)
### Depth of Market
The Depth of Market (DOM) widget supports frequent data updates and shows the volume for each price.
Data is displayed in static mode.
This means that the price series is fixed, while the current price moves within, above, or below the designated range.
Users can also place orders right from the widget.
Refer to [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) for more information.
![DOM widget](https://www.tradingview.com/charting-library-docs/assets/images/dom-widget-static-3ee73e53b032e32a6c8bfeb7419cd496.png)
### Watchlist
The Watchlist widget allows users to track their favorite symbols and switch quickly between the corresponding charts. Users can create multiple lists and sort symbols by their names, price changes, and volumes. Refer to [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List) for more information.

### Details
The Details widget displays a certain symbol's information such as bid/ask prices, trading hours, and a price range during the day. To display the widget, you should enable the [`details`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WidgetBarParams#details) property in the [`widgetbar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#widgetbar) settings. The widget requires quote data that you should send using the corresponding methods in the [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes) or [UDF](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF#quotes).

### News
The News widget displays news on a certain symbol. You can fetch news using RSS or the library's API. Refer to [News](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/news) for more information.

### Account Manager
The Account Manager (Trading Panel) widget displays information from your broker account, such as orders, positions, an account balance, and more. Users can manage their orders and positions from the widget. You can add custom tabs and tables to the widget. Refer to [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) for more information.

![Account Manager](https://www.tradingview.com/charting-library-docs/assets/images/account-manager-86ebf69afbfea3b80bc4541b26167351.png)
### Advanced Order Ticket
The Advanced Order Ticket dialog allows users to place different types of orders, including trailing stop, stop-loss, bracket orders, and more. To open this dialog, users should click the *Trade* button in [*Account Manager*](#account-manager).

![Order Ticket](https://www.tradingview.com/charting-library-docs/assets/images/order-ticket-cba466312927cc1e24a56ca7cbbc24a1.png)
You can add custom fields, enable an order preview, or implement your own custom Order Ticket.
Refer to [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) for more information.
### Buy/Sell buttons and lines
The Buy/Sell buttons are displayed next to the [legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend). Click the buttons to open [Order Ticket](#advanced-order-ticket) and place orders instantly. Trading Platform also supports bid/ask price lines on the chart.

![Buy/Sell Buttons](https://www.tradingview.com/charting-library-docs/assets/images/buy-sell-buttons-3c77c6e0eed1387b6da2dd24b31ddde9.png)

> **Tip:** The buttons can be customized with [CSS](https://www.tradingview.com/charting-library-docs/latest/customization/styles/CSS-Color-Themes#buysell-buttons-properties).

### Japanese chart types
Trading Platform includes all [chart types](https://www.tradingview.com/charting-library-docs/latest/getting_started/Key-Features#chart-types) available in Advanced Charts and additional types listed below:

- Renko
- Point-and-Figure
- Line Break
- Kagi

### Drawing templates
Trading Platform allows users to create drawing templates. For more information, refer to the [Drawings](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/#templates) article.

### Building seconds bars from ticks
Trading Platform can build seconds bars from ticks. For more information, refer to [`build_seconds_from_ticks`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#build_seconds_from_ticks).

## How to migrate from Advanced Charts
If you want to migrate from Advanced Charts to Trading Platform, you should replace the `charting_library` folder in your project with the same folder from the [trading_platform](https://github.com/tradingview/trading_platform) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)) repository.
At this point, you will have additional chart types (Renko, Point-and-Figure, Line Break, and Kagi), the synchronized multiple-chart layout, and an empty [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).

To enable the [Watchlist](#watchlist), [Details](#details), [Order Ticket](#advanced-order-ticket), [News](#news), and [Depth of Market](#depth-of-market) widgets, you need to implement the Datafeed API methods related to [trading](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods). You should also enable the corresponding [featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#trading-platform) or the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor#trading-platform-parameters) parameters. If you want to add [trading capabilities](#chart-trading), you should implement the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api). The part of the Trading Platform implementation is shown in the [`trading.html`](https://github.com/tradingview/trading_platform/blob/master/trading.html) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)) file.

Pay attention that data for the legend is requested in the [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes) method on the **[mobile version](https://www.tradingview.com/charting-library-docs/latest/mobile_specifics/) of Trading Platform**. If this method is not implemented, you may see the `N/A` values instead of prices.

## See also
For more information on how to integrate Trading Platform, refer to the following articles:

- [Core trading concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/): learn about the trading components, how they integrate into the chart widget, and how they work together.
- [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions): check the Widget Constructor parameters specific to Trading Platform.