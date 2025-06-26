---
title: "UI elements | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/"
extracted_at: "2025-06-22T09:14:29.370Z"
---

# UI elementsThe library offers a feature-rich interface, providing the opportunity to tweak and customize it to fit specific needs.
This article serves as a guide to understanding the various parts of the interface.
Further articles within this section provide detailed explanations for each UI element.
The interface can be divided into the following main parts.

![User interface](https://www.tradingview.com/charting-library-docs/assets/images/user-interface-a5b2a6d4be777ffa1fb4a2942e890b74.png)
## Top toolbar
[##  Symbol SearchCustomize the button that allows searching for and displaying financial instruments by entering instrument names

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Search)[##  ResolutionManage the timeframe resolutions that define the duration of each bar

](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution)[##  Chart stylesAdjust properties for various chart styles to enhance the appearance of your main series

](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/chart-overrides#chart-styles)[##  IndicatorsCustomize built-in indicators and create your own using JavaScript

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/)[##  Save layouts and templatesAllow users to save and restore chart layouts and chart, drawing, and indicator templates for future use

](https://www.tradingview.com/charting-library-docs/latest/saving_loading/)[##  SnapshotsConfigure the settings for taking snapshots and managing their storage

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Snapshots)[##  Custom buttonsAdd custom buttons or drop-down menus to the top toolbar for quick access to specific functions

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Toolbars#custom-buttons-in-top-toolbar)[##  Multiple-chart layoutAllow users to display up to 8 charts on one layout (Trading Platform only)

](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#multiple-chart-layout)
## Chart
The main area on the chart where a [series](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#series) or [indicator](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/) is displayed is called **pane**.
The picture below shows the red pane with a main series and the green pane with an indicator.
![Chart panes](https://www.tradingview.com/charting-library-docs/assets/images/pane-d44d70e4c4be2d846c4ecdd789fc0e17.png)
The chart contains the following elements:

[##  ChartCustomize colors and learn how to use the Chart API to subscribe to events, manage drawings, and more

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Chart)[##  Price scaleCustomize the price scale appearance and manage it through the API

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale)[##  Time scaleCustomize the time scale appearance and manage it through the API

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale)[##  LegendCustomize the legend appearance: include symbol logos, set titles, and format prices according to your preferences

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend)[##  MarksDisplay additional information such as news, bar patterns, splits, and dividends on the chart or time scale

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Marks)[##  Market statusProvide users with updates on whether the market is open or closed for trading

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/market-status)[##  Context menuCustomize the dialog accessed through a right-click or ellipsis menu

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu)[##  Time zonesConfigure time zones to suit your application’s needs

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/timezones)
## Drawing toolbar
Drawings are the tools that can help you analyze the charts and make clear annotations to them.
For more information, refer to [Drawings](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/).
## Widget bar
The widget bar is a right side toolbar available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/) only.
You cannot change the widget bar location but you can hide it using the [`hide_right_toolbar`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#hide_right_toolbar) and [`hide_right_toolbar_tabs`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#hide_right_toolbar_tabs) featuresets.
The bar displays the following widgets:

[##  Object TreeAllow users to manage drawings, indicators, and symbols on the chart

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/object-tree/)[##  WatchlistAllow users to track real-time price movements and volume of selected financial instruments

](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List)[##  DetailsDisplay detailed information for a specific symbol, including bid/ask prices, trading hours, and daily price ranges

](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details)[##  NewsDisplay latest news related to specific symbols

](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/news/)
## Account Manager
The Account Manager is a widget available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/) only.
The widget displays the user's trading information, such as orders, positions, and account balance.
Users can manage their orders and positions from the Account Manager.
For more information, refer to [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).