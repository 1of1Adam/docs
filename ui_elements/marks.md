---
title: "Marks | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/Marks"
extracted_at: "2025-06-22T09:14:48.029Z"
---

# MarksMarks allow you to display some extra information like news, bar patterns, splits/dividends, and more [on the chart](#marks-on-the-chart) or [time scale](#marks-on-the-time-scale).

Use the [`subscribe`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#subscribe) method to handle events raised when users interact with marks. You can also [refresh](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#refreshmarks) and [clear](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#clearmarks) marks using the chart methods.

## Marks on the chart
Marks on the chart are circles that are attached to bars and contain a character inside. You can customize the circle size and color. If you want to display two characters (like 'ED', 'AB', 'CD', etc.), you should enable the [`two_character_bar_marks_labels`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets) featureset.

One bar can have several marks. When a user clicks on the mark, the tooltip appears. The tooltip can only contain plain text. HTML code is not supported.

Marks are requested from your datafeed if you set [`supports_marks`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedConfiguration#supports_marks) to `true`. The library calls [`getMarks`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/additional-methods#getmarks) or requests [/marks](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF#marks) to get mark data for the visible data range.

## Marks on the time scale
Marks on the time scale are figures above the time scale. Each mark has a character inside and a pop-up tooltip with information strings. The tooltip does not support HTML code. You can specify a time scale mark shape using the [`shape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimescaleMark#shape) property. Images can be displayed within time scale marks by providing an image URL in the [`imageUrl`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimescaleMark#imageurl) property.

Time scale marks are requested from your datafeed if you set [`supports_timescale_marks`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedConfiguration#supports_timescale_marks) to `true`. The library calls [`getTimescaleMarks`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/additional-methods#gettimescalemarks) or requests [/timescale_marks](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF#timescale-marks) to get mark data for the visible data range.