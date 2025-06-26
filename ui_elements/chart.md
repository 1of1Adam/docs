---
title: "Chart | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/Chart"
extracted_at: "2025-06-22T09:14:31.967Z"
---

# ChartThis article contains general information on how to customize and control the chart. For more information about certain chart elements, refer to the rest of the articles in the **UI Elements** section.

## Default chart settings
You should use the Widget Constructor to set up default chart settings like symbol, [resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution), [time zone](https://www.tradingview.com/charting-library-docs/latest/ui_elements/timezones), [locale](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Localization), [size](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor#chart-size), and others. Refer to the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor#chart-configuration) article for more information.

## Customization

> **Tip:** Refer to the [Customization](https://www.tradingview.com/charting-library-docs/latest/customization/) section for detailed information on how to customize the chart and its elements.

### Change colors
You can customize the colors of the chart to implement your corporate colors.
The articles listed below explain how to change colors in certain cases:

- [Chart Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/chart-overrides): specify default color of UI elements on the chart like scales and panes.
- [Custom themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes): specify default color of UI elements outside the chart like dialogs and toolbars.

### Show/hide chart elements
You can show/hide chart elements using [featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets).
If there is no featureset for an element you want to hide, you can do it by adding your custom [CSS file](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_css_url).
## Chart methods
You can use the Chart API to interact with the chart after it is initialized. For example, you can subscribe to chart events, manage drawings and indicators, get information about a current configuration, perform Z-order operations, and more. All methods are listed in [IChartWidgetApi](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi).

### Subscribe to events
You can subscribe to the chart events using methods like [`onDataLoaded`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#ondataloaded), [`onSymbolChanged`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#onsymbolchanged), [`onChartTypeChanged`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#oncharttypechanged), and others.
For example, the code sample below specifies a time frame when an interval is changed using the [`onIntervalChanged`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#onintervalchanged) method.
```
widget.activeChart().onIntervalChanged().subscribe(null, (interval, timeframeObj) =>
    timeframeObj.timeframe = {
        value: '12M',
        type: 'period-back'
});

```
### Manage chart
You can manage chart settings using methods like [`setSymbol`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#setsymbol), [`setResolution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#setresolution), [`resetData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#resetdata), [`clearMarks`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#clearmarks), and others.
For example, the code sample below specifies a new [range](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#date-range) using the [`setVisibleRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#setvisiblerange) method.
```
widget.activeChart().setVisibleRange(
    { from: Date.UTC(2023, 6, 12, 13, 30) / 1000 },
    { applyDefaultRightMargin: true }
)

```
### Execute action by ID
The [`executeActionById`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#executeactionbyid) method allows you to trigger specific actions programmatically through the API.
This is useful for customizing UI or replicating built-in functionality with custom components.
For example, you can replace built-in [top toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/#top-toolbar) buttons with custom ones or trigger actions for hidden UI elements.
```
widget.activeChart().executeActionById("chartReset");

```
Click to reveal the list of the `ChartActionId` types.

 **|Action ID** | **Purpose** ||
| `"chartProperties"` | Opens the *Chart settings* dialog. ||
| `"compareOrAdd"` | Opens or hides the [*Compare symbol*](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/#add-and-compare-new-series) dialog. ||
| `"scalesProperties"` | Opens or hides the *Chart settings* dialog. ||
| `"paneObjectTree"` | Opens the Object tree on the [widget bar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/#widget-bar). ||
| `"insertIndicator"` | Opens or hides a dialog for adding [indicators](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/). ||
| `"symbolSearch"` | Opens the [*Symbol Search*](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Search) dialog. ||
| `"changeInterval"` | Opens a dialog for changing [resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution). ||
| `"timeScaleReset"` | Resets the [time scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale) to its default state. ||
| `"chartReset"` | Resets the [chart](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Chart) view to its default state. ||
| `"seriesHide"` | Hides the selected series on the chart. ||
| `"studyHide"` | Hides the selected [indicator](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/) on the chart. ||
| `"lineToggleLock"` | Enables or disables the *Lock/Unlock* button in the floating toolbar of the selected [drawing](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/). ||
| `"lineHide"` | Hides the selected [drawing](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/) on the chart. ||
| `"scaleSeriesOnly"` | Enables or disables the *Scale price chart only* option for the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). ||
| `"drawingToolbarAction"` | Opens or hides the [drawing toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/#drawing-toolbar). ||
| `"stayInDrawingModeAction"` | Enables or disables the *Stay in drawing* mode. ||
| `"hideAllMarks"` | Shows or hides all [marks](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Marks) on the chart. ||
| `"showCountdown"` | Enables or disables *Countdown to bar close* option for the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). ||
| `"showSeriesLastValue"` | Shows or hides the series's last value on the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). ||
| `"showSymbolLabelsAction"` | Shows or hides the symbol's label on the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). ||
| `"showStudyLastValue"` | Shows or hides the indicator's last value on the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). ||
| `"showStudyPlotNamesAction"` | Shows or hides the indicator's label on the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). ||
| `"undo"` | Undoes the last applied action. ||
| `"redo"` | Redoes the last undone action. ||
| `"paneRemoveAllStudiesDrawingTools"` | Removes all [indicators](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/) and [drawings](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/) from the chart. ||
| `"showSymbolInfoDialog"` | Opens the *Security info* dialog. ||

### Manage drawings and indicators
You can create and manage drawings/indicators using methods like [`createStudy`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createstudy), [`getAllShapes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getallshapes), [`getShapeById`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getshapebyid), [`removeAllStudies`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#removeallstudies), and others.
For example, the code sample below adds the *Vertical line* drawing on the chart using the [`createShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createshape) method.
```
widget.activeChart().createShape(
    { time: 1514764800 },
    { shape: 'vertical_line' }
);

```
### Getters
You can get information about the current chart settings using methods like [`symbol`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#symbol), [`chartType`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#charttype), [`getVisibleRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getvisiblerange), and others.
For example, the code sample below gets the current resolution using the [`resolution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#resolution) method.
```
console.log(widget.activeChart().resolution());

```
You can also use chart methods to get objects that provide API to perform certain operations. For example:

- [`getSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getseries) returns [`ISeriesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi) that allows you to interact with a [series](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#series).
- [`selection`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#selection) returns [`ISelectionApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISelectionApi) that allows you to select drawings and indicators.
- [`getTimezoneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#gettimezoneapi) returns [`ITimezoneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimezoneApi) that allows you to manage the chart's time zone.

### Trading primitives

> **Warning:** Starting from version 29, the methods for creating trading primitives are only available in [Trading Platform].

You can create an order/position line and trade execution using the corresponding [`createOrderLine`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createorderline), [`createPositionLine`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createpositionline), [`createExecutionShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createexecutionshape) methods.
Refer to [Trading Primitives](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Trading-Primitives) for more information.
For example, the code sample below adds a new order line on the chart using the [`createOrderLine`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createorderline) method.

```
widget.activeChart().createOrderLine()
    .setTooltip("Additional order information")
    .setModifyTooltip("Modify order")
    .setCancelTooltip("Cancel order")
    .onMove(function() {
        this.setText("onMove called");
    })
    .onModify("onModify called", function(text) {
        this.setText(text);
    })
    .onCancel("onCancel called", function(text) {
        this.setText(text);
    })
    .setText("STOP: 73.5 (5,64%)")
    .setQuantity("2");

```