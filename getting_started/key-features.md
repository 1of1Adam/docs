---
title: "Key features | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/getting_started/Key-Features"
extracted_at: "2025-06-22T09:13:47.278Z"
---

# Key featuresThis topic describes the key features of Advanced Charts and [Trading Platform](#trading-platform-features). You can find a full list of features on the [TradingView website](https://www.tradingview.com/HTML5-stock-forex-bitcoin-charting-library/?feature=technical-analysis-charts). Note that some [features](#unsupported-features) that are available on [tradingview.com](https://www.tradingview.com/chart/) are not supported in the libraries.

## Advanced Charts features
The following features are available in Advanced Charts and Trading Platform.

### Mobile friendliness
Advanced Charts and Trading Platform are compatible with mobile devices.

> **Info:** The chart layout adapts to the device type and screen size by resizing/hiding elements.
This means that some features, such as [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#watchlist) and [News](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#news), may not be supported on smaller devices.

The library supports mouse and touch-based inputs and recognizes single and multi-touch gestures.
Refer to the [Mobile app development](https://www.tradingview.com/charting-library-docs/latest/mobile_specifics/) topic for more information.
### Chart types
Advanced Charts and Trading Platform support the following chart types:

- Bars
- Candles
- Hollow candles
- Line
- Line with markers
- Step line
- Area
- HLC area
- HLC bars
- Baseline
- Columns
- High-low
- Heikin Ashi

> **Info:** The types below are available in the Trading Platform only.

- Renko
- Point-and-Figure
- Line Break
- Kagi

### Indicators
Advanced Charts and Trading Platform support more than 100 [indicators](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/). Follow the [Indicators List](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/Indicators-List) page to see all available indicators.

You can also create your custom indicators in JavaScript. Refer to [Custom Studies](https://www.tradingview.com/charting-library-docs/latest/custom_studies/) for more information. Note that [Pine Script®](https://www.tradingview.com/pine-script-docs/) is not supported in the libraries.

### Drawings
Advanced Charts and Trading Platform support more than 70 [drawings](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/). Follow the [Drawings List](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/Drawings-List) page to see all available drawings.

### Compare symbols
Advanced Charts and Trading Platform allow you to display multiple symbols on the same chart. The library brings them to the common time zone and trading session. If some symbol's trading session is longer than others, the extra data is cut by default. Alternatively, you can [extend the time scale](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Studies-Extending-The-Time-Scale#for-overlay-study) using the [`secondary_series_extend_time_scale`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#important-features) featureset. For example, the current symbol's session starts at 09:00, and you add another symbol whose session starts at 08:00. In this case, the `08:00` timestamp appears on the time scale.

### Advanced price scale
Advanced Charts and Trading Platform include additional logarithmic, percent, fractional, and other price scales. You can also display symbols in different currencies and units. For more information, refer to [Price Scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale).

### Building custom resolutions
Advanced Charts and Trading Platform can build bars with a higher resolution using lower resolution data. For example, they can build 2-minute bars from 1-minute bars. For more information, refer to [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution).

### Resolution in seconds and ticks
Advanced Charts and Trading Platform support resolutions in seconds and ticks. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#resolutions) topic for more information.

### Trading hours
Advanced Charts and Trading Platform display trading hours for a symbol in a separate widget. The libraries also support [pre-market and post-market](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Extended-Sessions) trading sessions.

### Chart snapshot
Users can take [snapshots](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Snapshots) in the UI. All snapshots are stored on the TradingView servers. The data storage period is not limited in time. You can also change the storage path using the [API](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#snapshot_url).

### Time zones
Advanced Charts and Trading Platform support more than 80 time zones and daylight saving time for each of them. Users can select a time zone in the UI and observe the chart in the exchange's time zone or any time zone from the [list](https://www.tradingview.com/charting-library-docs/latest/ui_elements/timezones#supported-time-zones).

If a time zone you want to provide is not supported in the library, you can request it on [GitHub Issues](https://github.com/tradingview/charting_library/issues) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)). You can also create a [custom time zone](https://www.tradingview.com/charting-library-docs/latest/ui_elements/timezones#custom-time-zones).

### Theme
Advanced Charts and Trading Platform include pre-designed dark and light themes. Note that users cannot switch the theme in the UI unless you develop this option outside the library. For more information, refer to the [Theme](https://www.tradingview.com/charting-library-docs/latest/customization/#theme) section.

## Trading Platform features
Refer to the [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/) article for more information about the features.

## Unsupported features
Neither Advanced Charts nor Trading Platform provides full functionality of the charts on [tradingview.com](https://www.tradingview.com/chart/). Since Advanced Charts and Trading Platform are client-side solutions, they do not support the client-server features listed below.

- Pine Script®
- Alerts
- Bar Replay Tool
- Range Bars
- TradingView data
- Strategy Tester
- Screener Widget
- Technicals in the Details widget
- Hotlists
- Calendars
- Chats
- Heatmap
- Patterns

> **Tip:** Consider using the TradingView [Widgets](https://www.tradingview.com/charting-library-docs/latest/getting_started/product-comparison#widgets) to display Calendars, Hotlists, and Heatmaps.