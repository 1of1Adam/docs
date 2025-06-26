---
title: "Indicators | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/"
extracted_at: "2025-06-22T09:14:49.904Z"
---

# IndicatorsAn indicator (study) is a mathematical function built based on trading statistics such as opening and closing prices, minimum and maximum prices, trading volumes, and more. You can make predictions about the future movement of the market by analyzing changes in values of the indicator. The values of indicator functions can be displayed on the chart in the form of lines, columns, points, and geometric figures. For more information about indicators, refer to the [Technical Indicator](https://www.investopedia.com/terms/t/technicalindicator.asp) article.

## Built-in indicators
Advanced Charts and Trading Platform support more than 100 indicators. Refer to [Indicators List](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/Indicators-List) to see all available indicators.

## Custom indicators
You can create your custom indicators in JavaScript. Refer to [Custom Studies](https://www.tradingview.com/charting-library-docs/latest/custom_studies/) for more information. Note that [Pine Script®](https://www.tradingview.com/pine-script-docs/) is not supported in the libraries.

## Add an indicator
Indicators can be added [in the UI](#ui) and [using the API](#api).

### UI
Users can add indicators in the UI as demonstrated below.

Users can also change the indicator's parameters in the *Settings* dialog.

> **Info:** Users cannot see or change the code of built-in or custom indicators.

### API
You can use the [`createStudy`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createstudy) method to add an indicator to the chart. The method has the `inputs` parameter that allows you to specify an indicator's options. To get a list of options available for a certain indicator, call the [`getStudyInputs`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#getstudyinputs) method and pass the indicator's name as a parameter. Note that the indicator's name should match the one provided in the drop-down list.

```
widget.getStudyInputs('MACD');

```
The code sample below demonstrates how to create an indicator.

```
widget.activeChart().createStudy('MACD', false, false, { in_0: 14, in_1: 30, in_3: 'close', in_2: 9 });
widget.activeChart().createStudy('Moving Average Exponential', false, false, { length: 26 });
widget.activeChart().createStudy('Stochastic', false, false, { in_0: 26 }, {"%d.color" : "#FF0000"});
widget.activeChart().createStudy('Price Channel', true, false, { in_0: 26 }, null, {checkLimit: false, priceScale: 'new-left'});

```
## Add and compare new series
Users can add new [series](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#series) to the chart to compare symbols. To do this in the UI, users should click the *Compare or Add Symbol* button. They can also specify a price scale and display the new symbol on a new pane.

To add a symbol programmatically, you should use the *Overlay* indicator.

```
widget.activeChart().createStudy('Overlay', true, false, { symbol: 'IBM' });

```
Alternatively, you can use the *Compare* indicator that allows you to additionally specify the data source. However, unlike *Overlay*, this indicator does not support the [*Allow extend time scale*](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Studies-Extending-The-Time-Scale#for-overlay-study) feature or logos in the [*Legend*](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend#display-logos).

```
widget.activeChart().createStudy('Compare', false, false, { source: 'open', symbol: 'IBM'});

```
### Enable spread operators
**Spread operators** are operators that allow comparison between a financial instrument, such as a stock,
and an additional variable, such as another financial instrument or a numerical value.

> **Warning:** The library does not handle the spread calculations, you should perform them on your server.
For example, when users enter "APPL-TSLA", the [datafeed](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) is called with the `AAPL-TSLA` symbol name.
The library expects your datafeed to resolve the symbol information and return the relevant data.

To display spread operators, include the [`show_spread_operators`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#show_spread_operators) and [`compare_symbol_search_spread_operators`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#compare_symbol_search_spread_operators)
featuresets in the [`enabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#enabled_features) array.

## Visibility customization
### Hide indicators
You can use the [`studies_access`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#studies_access) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) to customize the list of indicators available to users. For example, you can hide some indicators or only make them available to certain users.
Check out the [Widget Constructor tutorial](https://youtu.be/bdvmM3FNnSY?t=1035&feature=shared) on YouTube for an implementation example.
### Hide volume-based indicators
If your datafeed does not provide volume data and you want to hide all volume-based indicators, you should add the indicators below to the blacklist in [`studies_access`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#studies_access).

- Accumulation/Distribution
- Chaikin Money Flow
- Ease of Movement
- Elders Force Index
- Klinger Oscillator
- Money Flow Index
- Net Volume
- On Balance Volume
- Price Volume Trend
- VWAP
- Volume Oscillator

### Hide the Volume indicator
The library adds the *Volume* indicator to all financial instruments that have volume data. If you do not want to show this indicator, you should include the [`create_volume_indicator_by_default`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#create_volume_indicator_by_default) featureset in the [`disabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#disabled_features) array.

### Limit indicator amount
You can use the [`study_count_limit`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#study_count_limit) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) to set the maximum amount of indicators that can be displayed on the chart simultaneously.

## Style customization
You can use the [`studies_overrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#studies_overrides) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) to specify the indicator's default parameters such as colors, line width, a plot type, and more. Refer to the [Indicator Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides) article for more information on how to customize an indicator.

## Indicator API
After an indicator is created, you can manage it using `IStudyApi`.
For example, you can change the indicator's visibility or position. Refer to [`IStudyApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi) for more information.