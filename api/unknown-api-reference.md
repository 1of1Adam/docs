---
title: "API Reference | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/"
extracted_at: "2025-06-22T09:30:30.487Z"
---

- [](/charting-library-docs/)- API ReferenceOn this page# API Reference

## Structure[​](#structure)
The API is structured as a modular system of types, interfaces, and enumerations.
The library's API is divided into three modules, where each module consists of interfaces that define properties and methods specific to its functionality.
### Charting Library module[​](#charting-library-module)
The [Charting Library module](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library) is designed to manage chart creation, customize the UI appearance, and handle user interactions.

#### Key features[​](#key-features)

- Manage drawings and indicators displayed on the chart.
- Customize chart themes, layouts, and behaviors.
- Handle user interactions through events and methods.

#### Common interfaces[​](#common-interfaces)
[##  Advanced Charts Widget OptionsProperties for Advanced Chart widget to customize its appearance and behavior

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions/)[##  Trading Platform Widget OptionsProperties for Trading Platform widget to customize its appearance and behavior

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions/)[##  IChartingLibrary WidgetPrimary interface for library interactions

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget/)[##  IChart WidgetPrimary interface for chart interactions, such as creating drawings and indicators

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi/)

### Datafeed module[​](#datafeed-module)
The [Datafeed module](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed) is designed to integrate custom data sources and controlling data flow to the chart.

#### Key features[​](#key-features-1)

- Connect any market data source to Advanced Charts.
- Handle custom symbology logic to map your backend symbols to TradingView's requirements.
- Synchronize chart data with live market data updates.

#### Common interfaces[​](#common-interfaces-1)
[##  SymbolInfoDefines the structure and metadata for symbols, including properties like ticker and exchange

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo/)[##  IExternal DatafeedActs as the entry point for connecting custom datafeeds to the library

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IExternalDatafeed)[##  IDatafeed ChartProvides methods for fetching and managing historical and real-time data

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IDatafeedChartApi)[##  IDatafeed QuotesEnables the retrieval and management of real-time market quotes

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IDatafeedQuotesApi)

### Broker module[​](#broker-module)
The [Broker module](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker) is designed to integrate trading capabilities provided by [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).

#### Key features[​](#key-features-2)

- Enable creating market, limit, and other order types directly from the chart interface.
- Provide real-time market quotes to power trading features like the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket), [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List), and [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market).
- Support multiple account setups for users with diverse trading needs.

#### Common interfaces[​](#common-interfaces-2)
[##  Broker APIEnables trading features and connects the charts with your trading logic

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal)[##  Trading HostReceives trading information from your backend server and provides the library with updates

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost)[##  Broker configurationDefines configuration for additional Trading Platform features

](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SingleBrokerMetaInfo)

## Best practices for navigation[​](#best-practices-for-navigation)

- Identify the module relevant to your task: [creating charts](#charting-library-module), [managing datafeeds](#datafeed-module), or [enabling trading](#broker-module).
- Examine the available interfaces within the module. Each interface defines a set of properties and methods relevant to a specific feature or functionality.
- Follow type links and explore enumerations. If a property uses a non-primitive type, follow the link to the corresponding type definition. This will reveal additional properties and their relationships.
- Get back into the context and use your browser’s navigation to return to higher-level modules or interfaces when needed.

### Browse TypeScript definition[​](#browse-typescript-definition)
Alternatively, if you are more comfortable browsing the API through a TypeScript definition file, you can use the following links:

- [Charting Library and Broker TypeScript definition](https://github.dev/tradingview/charting_library/blob/master/charting_library/charting_library.d.ts)
- [Datafeed TypeScript definition](https://github.dev/tradingview/charting_library/blob/master/charting_library/datafeed-api.d.ts)

#### Keyboard shortcuts for Visual Studio Code[​](#keyboard-shortcuts-for-visual-studio-code)
ActionWindows shortcutmacOS shortcutFindCtrl + FCmd + FGo to definitionF12 or Ctrl + ClickF12 or Cmd + ClickGo backCtrl + -Cmd + -- [Structure](#structure)[Charting Library module](#charting-library-module)- [Datafeed module](#datafeed-module)- [Broker module](#broker-module)- [Best practices for navigation](#best-practices-for-navigation)[Browse TypeScript definition](#browse-typescript-definition)