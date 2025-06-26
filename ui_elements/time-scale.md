---
title: "Time scale | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale"
extracted_at: "2025-06-22T09:14:45.492Z"
---

# Time scale**Time scale** (or time axis) is a horizontal scale at the bottom of the chart that displays the time of bars.

![Time scale](https://www.tradingview.com/charting-library-docs/assets/images/time-scale-3196a6556602023a8b3700cf1d833407.png)
## Time scale API
You can manage the time scale using the Time scale API.
For example, you can set a specific right margin or detect when the chart has been zoomed in/out.
Refer to [`ITimeScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimeScaleApi) for more information.
## Customize scale appearance
You can customize the appearance of the time scale using the [Overrides API](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/).
For example, the code sample below changes the text color and font size of the time and [price](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale) scales.
```
const datafeed = new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com");
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: datafeed,
    symbol: "AAPL",
    interval: "1D",
    overrides: {
        "scalesProperties.textColor": "#FF0000",
        "scalesProperties.fontSize": 14,
    }
})

```
Refer to the [Scale colors and fonts](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/chart-overrides#scale-colors-and-fonts) section to see the full list of the overrides properties.

## Date and time formatting
You can adjust the display format of date and time values using the [`custom_formatters`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_formatters) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
Check out the [Widget Constructor tutorial](https://www.youtube.com/watch?v=bdvmM3FNnSY&t=1466s) on YouTube for an implementation example.
## Time frame toolbar
Time frames are time period buttons displayed at the bottom-left corner of the chart.
When users switch a time frame, it causes the following changes to satisfy the selected time frame:

- The chart [resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution) changes.
- The bars scale horizontally to cover the entire requested date/time range.

For example, clicking `1Y` makes the chart switch the resolution to `1W` and
scale it accordingly to display weekly bars for the entire year.
Each time frame has its default chart resolution:

 **|Time frame** | **Chart resolution** ||
| 5Y | W ||
| 1Y | W ||
| 6M | 120 ||
| 3M | 60 ||
| 1M | 30 ||
| 5D | 5 ||
| 1D | 1 ||

### Time frame customization
You can customize displayed time frames using the [`time_frames`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#time_frames) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
Note that time frames that require resolutions that are unavailable for a particular symbol will be hidden.
You can also check out the [Widget Constructor tutorial](https://www.youtube.com/watch?v=bdvmM3FNnSY&t=2328s) on YouTube for an implementation example.
### Programmatic time frame setting
If you want to programmatically set the time frame for the active chart, use the [`setTimeFrame`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#settimeframe) method of the [`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi).
For example, the following code snippet applies the `1Y` time frame, which is the same as when users click `1Y` at the bottom of the chart:
```
const widget = new TradingView.widget(/* Widget properties */);

widget.onChartReady(() => {
    const chart = widget.chart();
    chart.setTimeFrame({val: {type: 'period-back', value: '12M'}, res: '1W'});
});

```
## Extended time scale
You can enable indicators to extend the time scale.
This allows you to create custom indicators that show bars at a higher resolution than the main series.
Refer to [Extending the time scale](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Studies-Extending-The-Time-Scale) for more information.
## Extended sessions
If you want to display extended sessions for some symbols, refer to the [Extended sessions](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Extended-Sessions) article for more information.