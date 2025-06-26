---
title: "Overrides | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/customization/overrides/"
extracted_at: "2025-06-22T09:15:14.228Z"
---

# OverridesThe Overrides API allows you to customize elements on the chart like panes, scales, series, drawings, indicators, legends, and more.

## Chart and drawings
To override a property that relates to the chart, drawing, or trading element, you should specify this property in the [`overrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#overrides) parameter of [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor). The code sample below changes the chart background color and chart style using [`paneProperties.background`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesbackground) and [`mainSeriesProperties.style`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesstyle).

```
var widget = window.tvWidget = new TradingView.widget({
    // ...
    overrides: {
        "paneProperties.background": "#020024",
        "mainSeriesProperties.style": 2,
    }
});

```
If you want to change a property's value on the fly, you can use the [`applyOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#applyoverrides) method.

```
widget.applyOverrides({ "mainSeriesProperties.visible": false });

```
For more information on how to customize different entities using overrides, refer to the corresponding topics:

- [Chart overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/chart-overrides)
- [Drawings overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/Drawings-Overrides)
- [Trading overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/trading-overrides)

## Indicators
You can also customize indicators using overrides. Refer to the [Indicator Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides) article for more information.