---
title: "Chart overrides | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/customization/overrides/chart-overrides"
extracted_at: "2025-06-22T09:28:43.586Z"
---

# Chart overridesThis article describes [Overrides API](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/) properties that affect elements on the chart. You can find a full list of properties on the [ChartPropertiesOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides) page.

All properties are divided into four groups:

- [`paneProperties`](#paneproperties) — affect elements on the main chart pane.
- [`scalesProperties`](#scalesproperties) — affect price and time scales.
- [`mainSeriesProperties`](#mainseriesproperties) — affect series.
- [`tradingProperties`](#trading-platform) — affect Trading Platform features.

## paneProperties
These properties affect elements located on the chart's pane (inside the highlighted area).

### Chart background color
You can specify a background color using the following properties:

 **|Property** | **Description** ||
| [`paneProperties.backgroundType`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesbackgroundtype) | Pane background type. ||
| [`paneProperties.background`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesbackground) | Pane background color. ||
| [`paneProperties.backgroundGradientStartColor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesbackgroundgradientstartcolor) | Pane background gradient start color. ||
| [`paneProperties.backgroundGradientEndColor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesbackgroundgradientendcolor) | Pane background gradient end color. ||

Background color can be either solid or gradient. Note that the default background type is `gradient` in the **dark theme**. The following code samples demonstrate how to specify background in the dark theme:

Gradient color```
var widget = (window.tvWidget = new TradingView.widget({
    // ...
    theme: "dark",
    overrides: {
        "paneProperties.backgroundGradientStartColor": "#020024",
        "paneProperties.backgroundGradientEndColor": "#4f485e",
    },
}));

```

Solid color```
var widget = (window.tvWidget = new TradingView.widget({
    // ...
    theme: "dark",
    overrides: {
        "paneProperties.background": "#020024",
        "paneProperties.backgroundType": "solid"
    },
}));

```

### Grid lines
You can specify grid lines using the following properties:

 **|Property** | **Description** ||
| [`paneProperties.vertGridProperties.color`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesvertgridpropertiescolor) | Pane vertical grid color. ||
| [`paneProperties.vertGridProperties.style`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesvertgridpropertiesstyle) | Pane vertical grid line style. ||
| [`paneProperties.horzGridProperties.color`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieshorzgridpropertiescolor) | Pane horizontal grid color. ||
| [`paneProperties.horzGridProperties.style`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieshorzgridpropertiesstyle) | Pane horizontal grid line style. ||
| [`paneProperties.gridLinesMode`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesgridlinesmode) | Pane grid line mode. ||

The code sample below specifies a dotted grid line.

Dotted grid line```
var widget = (window.tvWidget = new TradingView.widget({
    // ...
    overrides: {
        "paneProperties.horzGridProperties.style": 1,
    },
}));

```
### Pane separator
You can change the color of the pane separator using the following property (it's also available in Chart settings but you'll have to at least have a pane in addition to main series to see it):

 **|Property** | **Description** ||
| [`paneProperties.separatorColor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesseparatorcolor) | Pane separator color. ||

Here's a code sample:

Pane separator color```
var widget = (window.tvWidget = new TradingView.widget({
    // ...
    overrides: {
        "paneProperties.separatorColor": "#9598a1"
    },
}));

```
### Legend
You can specify a legend using the following properties:

 **|Property** | **Description** ||
| [`paneProperties.legendProperties.showLastDayChange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowlastdaychange) | Ability to show daily changes in the chart legend. ||
| [`paneProperties.legendProperties.showStudyArguments`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowstudyarguments) | Study legend input values visibility. ||
| [`paneProperties.legendProperties.showStudyTitles`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowstudytitles) | Studies legend title visibility. ||
| [`paneProperties.legendProperties.showStudyValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowstudyvalues) | Studies legend value visibility. ||
| [`paneProperties.legendProperties.showSeriesTitle`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowseriestitle) | Series legend title visibility. ||
| [`paneProperties.legendProperties.showSeriesOHLC`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowseriesohlc) | Study legend OHLC values visibility. ||
| [`paneProperties.legendProperties.showBarChange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowbarchange) | Series legend change value visibility. ||
| [`paneProperties.legendProperties.showVolume`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowvolume) | Series legend volume value visibility. ||
| [`paneProperties.legendProperties.showBackground`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesshowbackground) | Legend background visibility. ||
| [`paneProperties.legendProperties.backgroundTransparency`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertieslegendpropertiesbackgroundtransparency) | Legend background transparency percentage. ||

Some properties that relate to the [`mainSeriesProperties`](#mainseriesproperties) group also affect the chart's legend.

 **|Property** | **Description** ||
| [`mainSeriesProperties.statusViewStyle.showExchange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesstatusviewstyleshowexchange) | Main series legend exchange visibility. ||
| [`mainSeriesProperties.statusViewStyle.showInterval`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesstatusviewstyleshowinterval) | Main series legend interval visibility. ||
| [`mainSeriesProperties.statusViewStyle.symbolTextSource`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesstatusviewstylesymboltextsource) | Main series legend text style. ||

The code sample below removes OHLCV values and chart resolution from the legend. It also specifies the `"long-description"` text style in the legend.

Legend```
var widget = (window.tvWidget = new TradingView.widget({
    // ...
    overrides: {
        "paneProperties.legendProperties.showVolume": false,
        "paneProperties.legendProperties.showSeriesOHLC": false,

        "mainSeriesProperties.statusViewStyle.showInterval": false,
        "mainSeriesProperties.statusViewStyle.symbolTextSource": "long-description",
    },
}));

```

### Margin
Use the following properties to specify a margin applied when users scale the chart:

 **|Property** | **Description** ||
| [`paneProperties.topMargin`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiestopmargin) | Pane auto scaling top margin percentage. ||
| [`paneProperties.bottomMargin`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#panepropertiesbottommargin) | Pane auto scaling bottom margin percentage. ||

## scalesProperties
These properties affect appearance of the [time](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale) and [price](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale) scales.

### Price scale position
You can use the [`priceScaleSelectionStrategyName`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#pricescaleselectionstrategyname) property to specify a price scale position.
If you want to change the price scale position on the fly, you should use the [`changePriceScale`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi#changepricescale) method.
```
widget.activeChart().getSeries().changePriceScale('new-left');

```
### Scale colors and fonts
You can specify scale colors and fonts using the following properties:

 **|Property** | **Description** ||
| [`scalesProperties.lineColor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertieslinecolor) | Scales (axis) border line color. ||
| [`scalesProperties.textColor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiestextcolor) | Scales (axis) text color. ||
| [`scalesProperties.fontSize`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesfontsize) | Scales (axis) font size. ||
| [`scalesProperties.axisHighlightColor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesaxishighlightcolor) | Sets the highlight color of the scales when adding a drawing. ||

### Labels on the scale
Advanced Charts and Trading Platform include labels that allow you to display additional information on the price scale like a symbol name, bid/ask prices, indicators, and more. You can use the properties below to enable these labels:

 **|Property** | **Description** ||
| [`scalesProperties.showSeriesLastValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesshowserieslastvalue) | Series last value label visibility. ||
| [`scalesProperties.showStudyLastValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesshowstudylastvalue) | Study label value label visibility. ||
| [`scalesProperties.showSymbolLabels`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesshowsymbollabels) | Symbol name label visibility. ||
| [`scalesProperties.showStudyPlotLabels`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesshowstudyplotlabels) | Study plot labels visibility. ||
| [`scalesProperties.showBidAskLabels`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesshowbidasklabels) | Bid/ask labels visibility. ||
| [`scalesProperties.showPrePostMarketPriceLabel`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesshowprepostmarketpricelabel) | Pre/post market price labels visibility. ||
| [`mainSeriesProperties.highLowAvgPrice.highLowPriceLabelsVisible`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertieshighlowavgpricehighlowpricelinesvisible) | High/low price labels visibility. ||
| [`mainSeriesProperties.highLowAvgPrice.averageClosePriceLabelVisible`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertieshighlowavgpriceaverageclosepricelabelvisible) | Average close price lines label visibility. ||

You can display values focused in the crosshair in labels on the scales. To do this, specify the following properties:

 **|Property** | **Description** ||
| [`scalesProperties.showPriceScaleCrosshairLabel`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesshowpricescalecrosshairlabel) | Price scale crosshair label visibility. ||
| [`scalesProperties.showTimeScaleCrosshairLabel`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesshowtimescalecrosshairlabel) | Time scale crosshair label visibility. ||
| [`scalesProperties.crosshairLabelBgColorLight`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiescrosshairlabelbgcolorlight) | Crosshair label light theme background color. ||
| [`scalesProperties.crosshairLabelBgColorDark`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiescrosshairlabelbgcolordark) | Crosshair label dark theme background color. ||

You can specify label colors and display mode using the properties below:

 **|Property** | **Description** ||
| [`mainSeriesProperties.priceAxisProperties.alignLabels`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiespriceaxispropertiesalignlabels) | Main series price axis label alignment behavior. ||
| [`scalesProperties.axisLineToolLabelBackgroundColorActive`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesaxislinetoollabelbackgroundcoloractive) | Dynamically changes the background color of all labels on the price scale when a drawing is in motion. ||
| [`scalesProperties.axisLineToolLabelBackgroundColorCommon`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesaxislinetoollabelbackgroundcolorcommon) | Configures the background color of a label shown on an axis scale when a drawing is selected. ||
| [`scalesProperties.seriesLastValueMode`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#scalespropertiesserieslastvaluemode) | Series last value label display mode. ||

### Price scale mode
You can specify a price scale mode using the following properties:

 **|Property** | **Description** ||
| [`mainSeriesProperties.priceAxisProperties.percentage`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiespriceaxispropertiespercentage) | Main series price axis percentage mode. ||
| [`mainSeriesProperties.priceAxisProperties.indexedTo100`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiespriceaxispropertiesindexedto100) | Main series price axis indexed to 100 mode. ||
| [`mainSeriesProperties.priceAxisProperties.log`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiespriceaxispropertieslog) | Main series price axis log mode. ||
| [`mainSeriesProperties.priceAxisProperties.isInverted`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiespriceaxispropertiesisinverted) | Main series price axis inverted mode. ||

Note that you cannot change the price scale mode using the [`applyOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#applyoverrides) method. If you want to change the mode on the fly, you should use the [Price Scale API](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi). Consider the code sample below that enables [Logarithmic mode](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.PriceScaleMode#log):

```
const priceScale = widget.activeChart().getPanes()[0].getRightPriceScales()[0];
priceScale.setMode(1);

```
## mainSeriesProperties
These properties affect the main series and UI elements related to its values. A series is a collection of data points that represents a specific metric over time.

### Series visibility
If you want to hide the main series, set the [`mainSeriesProperties.visible`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesvisible) property to `false`.
You can also use the [`setVisible`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi#setvisible) method to change the visibility of the series on the fly.
```
widget.activeChart().getSeries().setVisible(true);

```
To check if the series is currently visible or not, use the [`isVisible`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi#isvisible) method:

```
widget.activeChart().getSeries().isVisible();

```
### Chart styles
Advanced Charts and Trading Platform support multiple [chart styles](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle) including Bars, Candles, Line, Area, and more.
You can specify the style using the [`mainSeriesProperties.style`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesstyle) property.
For each style, there is a group of properties that you can specify to adjust the main series. Properties of one group have the same name pattern. You can use these patterns to find properties for a certain style on the [ChartPropertiesOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides) page. The table below contains styles and the corresponding patterns.

 **|Style** | **Name patterns** ||
| Line | `mainSeriesProperties.lineStyle` ||
| Baseline | `mainSeriesProperties.baselineStyle` ||
| Stepline | `mainSeriesProperties.steplineStyle` ||
| Bars | `mainSeriesProperties.barStyle` ||
| Candles | `mainSeriesProperties.candleStyle` ||
| Volume candles | `mainSeriesProperties.volCandlesStyle` ||
| Area | `mainSeriesProperties.areaStyle` ||
| HLC Area | `mainSeriesProperties.hlcAreaStyle` ||
| HLC bars | `mainSeriesProperties.hlcBarsStyle` ||
| Line With Markers | `mainSeriesProperties.lineWithMarkersStyle` ||
| Hollow Candles | `mainSeriesProperties.hollowCandleStyle` ||
| Heikin Ashi | `mainSeriesProperties.haStyle` ||
| Columns | `mainSeriesProperties.columnStyle` ||
| High-low | `mainSeriesProperties.hiloStyle` ||
| Renko | `mainSeriesProperties.renkoStyle` ||
| Line Break | `mainSeriesProperties.pbStyle` ||
| Kagi | `mainSeriesProperties.kagiStyle` ||
| Point-and-Figure | `mainSeriesProperties.pnfStyle` ||

You can also change the chart style properties on the fly. To do this, use the [`setChartStyleProperties`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi#setchartstyleproperties) method.
For example, the code sample changes the [properties](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CandleStylePreferences) of the Candles style.
```
widget.chart().getSeries().setChartStyleProperties(1, {
    upColor: '#10F9E0',
    downColor: '#1029F9',
    borderUpColor: '#10F9E0',
    borderDownColor: '#1029F9'
});

```

Properties that can be changed using `setChartStyleProperties` are listed in interfaces like [`BarStylePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BarStylePreferences), [`RenkoStylePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RenkoStylePreferences), and [`AreaStylePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AreaStylePreferences).
Refer to the [SeriesPreferencesMap](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SeriesPreferencesMap) page to see the list of such interfaces.
### Session
Advanced Charts and Trading Platform support pre-market and post-market sessions. To enable them, you should set the [`mainSeriesProperties.sessionId`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiessessionid) to `"extended"`. For more information about the sessions, refer to [Trading Sessions](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Trading-Sessions) and [Extended Sessions](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Extended-Sessions).

### Countdown
On the price scale, you can display a countdown to the bar close. To do this, set the [`mainSeriesProperties.showCountdown`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesshowcountdown) property to `true`.
Note that you should also implement the [`getServerTime`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/additional-methods#getservertime) method to display the countdown.
### Price line
You can specify a price line using the following properties:

 **|Property** | **Description** ||
| [`mainSeriesProperties.showPriceLine`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesshowpriceline) | Main series price line visibility. ||
| [`mainSeriesProperties.priceLineWidth`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiespricelinewidth) | Main series price line width. ||
| [`mainSeriesProperties.priceLineColor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiespricelinecolor) | Main series price line color. ||

### Additional lines
Advanced Charts and Trading Platform include additional lines that can be displayed on the chart. You can enable them using the toggle properties in the table below. For each line, there is a group of properties that you can specify to adjust this line. Properties of one group have the same name pattern. You can use these patterns to find properties for a certain line on the [ChartPropertiesOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides) page.

 **|Line** | **Toggle** | **Name patterns** ||
| Bid/ask | [`mainSeriesProperties.bidAsk.visible`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesbidaskvisible) | `mainSeriesProperties.bidAsk` ||
| High/low price | [`highLowAvgPrice.highLowPriceLinesVisible`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertieshighlowavgpricehighlowpricelinesvisible) | `mainSeriesProperties.highLowAvgPrice` ||
| Previous close price | [`mainSeriesProperties.showPrevClosePriceLine`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesshowprevclosepriceline) | `mainSeriesProperties.prevClosePrice` ||

### minTick
The [`minTick`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesmintick) property allows you to change the [`pricescale`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#pricescale), [`minmov`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#minmov), and [`fractional`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#fractional) properties for the current symbol at once. For more information about these properties, refer to [Price Format](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#price-format).
All `minTick` possible values are represented below as objects for better readability:
```
{ priceScale: 1, minMove: 1, frac: false },
{ priceScale: 10, minMove: 1, frac: false },
{ priceScale: 100, minMove: 1, frac: false },
{ priceScale: 1000, minMove: 1, frac: false },
{ priceScale: 10000, minMove: 1, frac: false },
{ priceScale: 100000, minMove: 1, frac: false },
{ priceScale: 1000000, minMove: 1, frac: false },
{ priceScale: 10000000, minMove: 1, frac: false },
{ priceScale: 100000000, minMove: 1, frac: false },
{ priceScale: 2, minMove: 1, frac: true },
{ priceScale: 4, minMove: 1, frac: true },
{ priceScale: 8, minMove: 1, frac: true },
{ priceScale: 16, minMove: 1, frac: true },
{ priceScale: 32, minMove: 1, frac: true },
{ priceScale: 64, minMove: 1, frac: true },
{ priceScale: 128, minMove: 1, frac: true },
{ priceScale: 320, minMove: 1, frac: true },

```
If you want to reset the `pricescale`, `minmov`, and `fractional` properties to their values initialized in [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo), set `minTick` to `"default"`.

Specify the [`mainSeriesProperties.minTick`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesmintick) property as demonstrated below:

```
// Set minTick to "default"
tvWidget.applyOverrides({ "mainSeriesProperties.minTick": "default" });

// Set series' minTick to { priceScale: 10000, minMove: 1, frac: false }
tvWidget.applyOverrides({ "mainSeriesProperties.minTick": "10000,1,false" });

// Set minTick for overlay studies to { priceScale: 10000, minMove: 1, frac: false }
tvWidget.applyStudiesOverrides({ "overlay.minTick": "10000,1,false" });

```
## Time zone
If you want to change a time zone that is set in [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor), you should use the [`timezone`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#timezone) property.

```
tvWidget.applyOverrides({ "timezone": "Europe/Belgrade"});

```
## Trading Platform
You can use `tradingProperties` to customize Trading Platform features such as orders and positions.
Refer to the [Trading overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/trading-overrides#adjust-display-of-trading-features) for more information.