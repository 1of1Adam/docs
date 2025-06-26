---
title: "Legend | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend"
extracted_at: "2025-06-22T09:14:38.528Z"
---

# LegendLegend is a list of series and indicators at the top-left corner of any chart.
Note that the legend position cannot be changed.
![Legend](https://www.tradingview.com/charting-library-docs/assets/images/legend-overview-589e075d0acfbee82e1827ff021a6366.gif)
## Configure legend
In the *Chart settings → Status line* dialog, users can configure the legend.

![Chart settings](https://www.tradingview.com/charting-library-docs/assets/images/legend-chart-settings-ba5635efa6a732d07c7112aac491d3f8.png)
### Symbol logos
If you want to display logos for symbols within the legend, follow the steps below:

Enable the [`show_symbol_logos`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#show_symbol_logos) and [`show_symbol_logo_in_legend`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#show_symbol_logo_in_legend) featuresets.
The *Logo* option appears in the settings dialog.
Provide URLs for symbols in the [`logo_urls`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#logo_urls) property of the [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo) object.
Pass the object as a parameter to the callback of the [`resolveSymbol`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#resolvesymbol) method.

### Open market status
By default, the library displays the current [market status](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Status) as an icon within the legend for the main series of the chart.
You can hide the market status by adding the [`display_market_status`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#display_market_status) featureset to the [`disabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#disabled_features) array.
### Title
In the *Title* drop-down, users can select what title to display in the legend:

- Description
- Ticker
- Ticker and description

You can also set the title using the [Overrides API](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/).
For example, the code sample below sets ticker as the legend title.
```
chartApi.applyOverrides({ "mainSeriesProperties.statusViewStyle.symbolTextSource": "ticker" })

```
### Last day change values

> **Info:** Last day change can be displayed in Trading Platform only as it requires quote data.

Last day change is a parameter represented by two values: daily change and percentage daily change. You should specify these values in the [`ch`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedQuoteValues#ch) and [`chp`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedQuoteValues#chp) properties of `DatafeedQuoteValues`
and pass them to the library when it calls [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes).
Last day change is displayed in *Data Window* on the right toolbar. You can also add this parameter to the chart legend using the [overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/):

```
var widget = window.tvWidget = new TradingView.widget({
    // ...
    overrides: {
        "paneProperties.legendProperties.showLastDayChange": true,
    }
});

```
Users can toggle the *Last day change values* option in the *Chart settings* dialog to change the last day change visibility in the legend. This option is hidden by default. To display it, you should enable one of the following featuresets:

- [`legend_last_day_change`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#legend_last_day_change) — adds the extra *Last day change values* option to the *Chart settings* dialog.
- [`show_last_price_and_change_only_in_series_legend`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#show_last_price_and_change_only_in_series_legend) — adds the last day change to the legend and hides the OHLC values. Also, the extra *Last day change values* option appears in the *Chart settings* dialog.

### Resolution
To disable resolution changing in the Legend, use the [`legend_inplace_edit`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#legend_inplace_edit) featureset.
If you want to completely remove the *Resolution* button from the *Legend*, use the [`hide_resolution_in_legend`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#hide_resolution_in_legend) featureset.

## Visibility customization
You can use [featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets) or [overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/) to customize the legend's visibility such as hiding or displaying particular legend elements.
The sections below describe customization via featuresets.
For more information about override properties that affect the legend, refer to [Legend](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/chart-overrides#legend).
### Hide legend
You can hide the legend widget from the chart.
To do this, include the `legend_widget` [featureset](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets) in the [`disabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#disabled_features) array.
![Disable legend](https://www.tradingview.com/charting-library-docs/assets/images/legend-hide-widget-3dd01451f395dfc5103ec54c4af6d01e.png)
### Hide legend buttons
You can hide all legend buttons by including the `edit_buttons_in_legend` in [`disabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#disabled_features).
Besides, disabling `show_hide_button_in_legend`, `format_button_in_legend`,
or `delete_button_in_legend` allows customizing particular legend buttons.
For example, the *Settings* button is hidden in the image below.
![Hide settings button](https://www.tradingview.com/charting-library-docs/assets/images/legend-hide-settings-button-ea0b509607eabb58e03b821aa1f09a22.png)
### Hide context menu
When right-clicking the legend, you can access the context menu.
To disable this feature, include `legend_context_menu` in [`disabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#disabled_features).
![Hide context menu](https://www.tradingview.com/charting-library-docs/assets/images/legend-context-menu-c540f1b35be76b429f05e5fcf6314aa4.png)
## Price formatting
Prices are formatted according to the `pricescale`, `minmov`, `minmove2`, `fractional`, and `variable_tick_size` properties specified in the [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo) object.
For more information, refer to the [Price format](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#price-format) section.
You can also apply custom formatting using the [`numeric_formatting`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#numeric_formatting) property of [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).

```
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com"),
    symbol: "AAPL",
    interval: "1D",
    numeric_formatting: { decimal_sign: "," },
})

```
In the code sample above, the comma separates the decimal/fractional part of the price.

## NaN values in legend
If `NaN` values appear in the legend instead of the expected data,
ensure that you have implemented the [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes) and [`subscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribequotes) methods of the [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/).
This issue appears in [mobile applications](https://www.tradingview.com/charting-library-docs/latest/mobile_specifics/) when running outside of tracking mode.
Outside this mode, the legend shows only three values: the closing price, price change, and price change percentage.
The library retrieves these values from the [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes) request, otherwise, it displays `NaN`.
Note that open, high, and low prices and indicator values are displayed in the tracking mode only.
To activate this mode, users should long tap on the chart. A single tap on the chart exits this mode.
## Display delayed data information
Follow the steps below to enable the *Data is delayed* section in the legend:

- Add the [`display_data_mode`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#display_data_mode) featureset to the [`enabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#enabled_features) array of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) object.
Provide the following properties in the [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo) object.
Pass this object as a parameter to the callback of the [`resolveSymbol`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#resolvesymbol) method.

- [`data_status`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#data_status) – specify `"delayed_streaming"`.
- [`delay`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#delay) – specify delay in seconds.

The image below shows the *Data is delayed* section and the *D* icon in the legend.

![Data is delayed](https://www.tradingview.com/charting-library-docs/assets/images/data-is-delayed-741f2420c57908102a90defe6f7294c6.png)