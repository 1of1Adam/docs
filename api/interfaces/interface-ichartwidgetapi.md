---
title: "Interface: IChartWidgetApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi"
extracted_at: "2025-06-22T09:38:33.154Z"
---

- [](/charting-library-docs/)- Interfaces- IChartWidgetApiOn this page# Interface: IChartWidgetApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IChartWidgetApi

The main chart API.

This interface can be retrieved by using the following widget ([IChartingLibraryWidget](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget)) methods:

- `chart` ([IChartingLibraryWidget.chart](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#chart))
- `activeChart` ([IChartingLibraryWidget.activeChart](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#activechart))

## Methods[​](#methods)
### applyLineToolsState[​](#applylinetoolsstate)
▸ applyLineToolsState(`state`): `Promise`<`void`>

Apply line tools state to the chart which will restore the drawings from the saved content.

This method requires that the [`saveload_separate_drawings_storage`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#saveload_separate_drawings_storage) featureset is enabled.

#### Parameters[​](#parameters)
NameType`state`[`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState)
#### Returns[​](#returns)
`Promise`<`void`>

### applyStudyTemplate[​](#applystudytemplate)
▸ applyStudyTemplate(`template`): `void`

Apply a study template to the chart.

Example

```
widget.activeChart().applyStudyTemplate(template);
```
#### Parameters[​](#parameters-1)
NameTypeDescription`template``object`A study template object.
#### Returns[​](#returns-1)
`void`

### availableZOrderOperations[​](#availablezorderoperations)
▸ availableZOrderOperations(`sources`): [`AvailableZOrderOperations`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AvailableZOrderOperations)

Get an object with operations available for the specified set of entities.

Example

```
widget.activeChart().availableZOrderOperations([id]);
```
#### Parameters[​](#parameters-2)
NameTypeDescription`sources`readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]An array of entity IDs.
#### Returns[​](#returns-2)
[`AvailableZOrderOperations`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AvailableZOrderOperations)

### barTimeToEndOfPeriod[​](#bartimetoendofperiod)
▸ barTimeToEndOfPeriod(`unixTime`): `number`

Get the bar time to the end of the period

#### Parameters[​](#parameters-3)
NameTypeDescription`unixTime``number`date timestamp
#### Returns[​](#returns-3)
`number`

### bringForward[​](#bringforward)
▸ bringForward(`sources`): `void`

Move the sources one level up in the Z-order.

Example

```
widget.activeChart().bringForward([id]);
```
#### Parameters[​](#parameters-4)
NameTypeDescription`sources`readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]An array of source IDs.
#### Returns[​](#returns-4)
`void`

### bringToFront[​](#bringtofront)
▸ bringToFront(`sources`): `void`

Move the sources to the top of the Z-order.

Example

```
widget.activeChart().bringToFront([id]);
```
#### Parameters[​](#parameters-5)
NameTypeDescription`sources`readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]An array of source IDs.
#### Returns[​](#returns-5)
`void`

### canZoomOut[​](#canzoomout)
▸ canZoomOut(): `boolean`

Check if the chart can be zoomed out using the [zoomOut](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#zoomout) method.

Example

```
if(widget.activeChart().canZoomOut()) {    widget.activeChart().zoomOut();};
```
#### Returns[​](#returns-6)
`boolean`

`true` if the chart can be zoomed out.

### cancelSelectBar[​](#cancelselectbar)
▸ cancelSelectBar(): `void`

Cancel any active bar selection requests.

Example

```
widget.activeChart().cancelSelectBar();
```
#### Returns[​](#returns-7)
`void`

### chartType[​](#charttype)
▸ chartType(): [`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)

Returns the main series style type.

```
console.log(widget.activeChart().chartType());
```
#### Returns[​](#returns-8)
[`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)

### clearMarks[​](#clearmarks)
▸ clearMarks(`marksToClear?`): `void`

Remove marks from the chart.

Example

```
widget.activeChart().clearMarks();
```
#### Parameters[​](#parameters-6)
NameTypeDescription`marksToClear?`[`ClearMarksMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ClearMarksMode)type of marks to clear. If nothing is specified both bar & timescale marks will be removed.
#### Returns[​](#returns-9)
`void`

### createAnchoredShape[​](#createanchoredshape)
▸ createAnchoredShape<`TOverrides`>(`position`, `options`): `Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Create a new anchored drawing. Anchored drawings maintain their position when the chart's visible range changes.

Example

```
widget.createAnchoredShape({ x: 0.1, y: 0.9 }, { shape: 'anchored_text', text: 'Hello, charts!', overrides: { color: 'green' }});
```
For more information, refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#createanchoredshape).

#### Type parameters[​](#type-parameters)
NameType`TOverrides`extends `object`
#### Parameters[​](#parameters-7)
NameTypeDescription`position`[`PositionPercents`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionPercents)Percent-based x and y position of the new drawing, relative to the top left of the chart.`options`[`CreateAnchoredShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateAnchoredShapeOptions)<`TOverrides`>An options object for the new drawing.
#### Returns[​](#returns-10)
`Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

### createExecutionShape[​](#createexecutionshape)
▸ createExecutionShape(): `Promise`<[`IExecutionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExecutionLineAdapter)>

Creates a new trade execution on the chart.
Starting from version 29, this method is only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).
Example
```
const executionLine = widget.activeChart().createExecutionShape();executionLine    .setText("@1,320.75 Limit Buy 1")    .setTooltip("@1,320.75 Limit Buy 1")    .setTextColor("rgba(0,255,0,0.5)")    .setArrowColor("#0F0")    .setDirection("buy")    .setTime(widget.activeChart().getVisibleRange().from)    .setPrice(160);
```
#### Returns[​](#returns-11)
`Promise`<[`IExecutionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExecutionLineAdapter)>

An API object for interacting with the execution.

### createMultipointShape[​](#createmultipointshape)
▸ createMultipointShape<`TOverrides`>(`points`, `options`): `Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Create a new multi point drawing.

Example

```
const from = Date.now() / 1000 - 500 * 24 * 3600; // 500 days agoconst to = Date.now() / 1000;widget.activeChart().createMultipointShape(    [{ time: from, price: 150 }, { time: to, price: 150 }],    {        shape: "trend_line",        lock: true,        disableSelection: true,        disableSave: true,        disableUndo: true,        text: "text",    });
```
For more information, refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#createmultipointshape).

#### Type parameters[​](#type-parameters-1)
NameType`TOverrides`extends `object`
#### Parameters[​](#parameters-8)
NameTypeDescription`points`[`ShapePoint`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapepoint)[]An array of points that define the drawing.`options`[`CreateMultipointShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateMultipointShapeOptions)<`TOverrides`>An options object for the new drawing.
#### Returns[​](#returns-12)
`Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Promise of the ID for the new drawing if it was created successfully.

### createOrderLine[​](#createorderline)
▸ createOrderLine(): `Promise`<[`IOrderLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IOrderLineAdapter)>

Creates a new trading order on the chart.
Starting from version 29, this method is only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).
Example

```
const orderLine = await widget.activeChart().createOrderLine();orderLine    .setTooltip("Additional order information")    .setModifyTooltip("Modify order")    .setCancelTooltip("Cancel order")    .onMove(function() {        this.setText("onMove called");    })    .onModify("onModify called", function(text) {        this.setText(text);    })    .onCancel("onCancel called", function(text) {        this.setText(text);    })    .setText("STOP: 73.5 (5,64%)")    .setQuantity("2");
```
#### Returns[​](#returns-13)
`Promise`<[`IOrderLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IOrderLineAdapter)>

An API object for interacting with the order.

### createPositionLine[​](#createpositionline)
▸ createPositionLine(): `Promise`<[`IPositionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPositionLineAdapter)>

Creates a new trading position on the chart.
Starting from version 29, this method is only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).
Example

```
const positionLine = await widget.chart().createPositionLine();positionLine    .onModify(function() {        this.setText("onModify called");    })    .onReverse("onReverse called", function(text) {        this.setText(text);    })    .onClose("onClose called", function(text) {        this.setText(text);    })    .setText("PROFIT: 71.1 (3.31%)")    .setTooltip("Additional position information")    .setProtectTooltip("Protect position")    .setCloseTooltip("Close position")    .setReverseTooltip("Reverse position")    .setQuantity("8.235")    .setPrice(160)    .setExtendLeft(false)    .setLineStyle(0)    .setLineLength(25);
```
#### Returns[​](#returns-14)
`Promise`<[`IPositionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPositionLineAdapter)>

An API object for interacting with the position.

### createShape[​](#createshape)
▸ createShape<`TOverrides`>(`point`, `options`): `Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Create a new single point drawing.

Example

```
widget.activeChart().createShape({ time: 1514764800 }, { shape: 'vertical_line' });
```
For more information, refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#createshape).

#### Type parameters[​](#type-parameters-2)
NameType`TOverrides`extends `object`
#### Parameters[​](#parameters-9)
NameTypeDescription`point`[`ShapePoint`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapepoint)A point. The location of the new drawing.`options`[`CreateShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions)<`TOverrides`>An options object for the new drawing.
#### Returns[​](#returns-15)
`Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Promise of the ID for the new drawing if it was created successfully.

### createStudy[​](#createstudy)
▸ createStudy<`TOverrides`>(`name`, `forceOverlay?`, `lock?`, `inputs?`, `overrides?`, `options?`): `Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Adds an indicator or a symbol for comparison to the chart.
For more information, refer to the [Indicators](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/) article.
#### Type parameters[​](#type-parameters-3)
NameType`TOverrides`extends `Partial`<[`SingleIndicatorOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#singleindicatoroverrides)>
#### Parameters[​](#parameters-10)
NameTypeDescription`name``string`name of an indicator as shown in the `Indicators` widget`forceOverlay?``boolean`forces the Charting Library to place the created indicator on the main pane`lock?``boolean`whether a user will be able to remove/change/hide the indicator or not`inputs?``Record`<`string`, [`StudyInputValue`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyinputvalue)>From version v22, it's an object containing named properties from the indicator properties dialog.`overrides?``TOverrides`An object that contains [overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#customize-a-single-indicator) for a new indicator. Note that you should not specify the indicator name. Overrides for built-in indicators are listed in [`SingleIndicatorOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#singleindicatoroverrides).`options?`[`CreateStudyOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateStudyOptions)study creation options
#### Returns[​](#returns-16)
`Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

ID of the created study

### createStudyTemplate[​](#createstudytemplate)
▸ createStudyTemplate(`options`): `object`

Save the current study template to a object.

Example

```
const options = { saveSymbol: true, saveInterval: true };const template = widget.activeChart().createStudyTemplate(options);
```
#### Parameters[​](#parameters-11)
NameTypeDescription`options`[`CreateStudyTemplateOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateStudyTemplateOptions)An object of study template options.
#### Returns[​](#returns-17)
`object`

A study template object.

### crossHairMoved[​](#crosshairmoved)
▸ crossHairMoved(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`params`: [`CrossHairMovedEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CrossHairMovedEventParams)) => `void`>

Get a subscription object for the crosshair moving over the chart.

Example

```
widget.activeChart().crossHairMoved().subscribe(    null,    ({ time, price }) => console.log(time, price));
```
#### Returns[​](#returns-18)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`params`: [`CrossHairMovedEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CrossHairMovedEventParams)) => `void`>

A subscription object for the crosshair moving over the chart.

### dataReady[​](#dataready)
▸ dataReady(`callback?`): `boolean`

Provide a callback function that will be called when chart data is loaded.
If chart data is already loaded when this method is called, the callback is called immediately.
Example

```
widget.activeChart().dataReady(() => {    // ...}
```
#### Parameters[​](#parameters-12)
NameTypeDescription`callback?`() => `void`A callback function called when chart data is loaded.
#### Returns[​](#returns-19)
`boolean`

### endOfPeriodToBarTime[​](#endofperiodtobartime)
▸ endOfPeriodToBarTime(`unixTime`): `number`

Get the end of period to bar time

#### Parameters[​](#parameters-13)
NameTypeDescription`unixTime``number`date timestamp
#### Returns[​](#returns-20)
`number`

### executeActionById[​](#executeactionbyid)
▸ executeActionById(`actionId`): `void`

Execute an action by ID.
See [Chart methods](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Chart#execute-action-by-id) for more information.
Example

```
// Undoes the last applied actionwidget.activeChart().executeActionById("undo");// Opens or hides the drawing toolbarwidget.activeChart().executeActionById("drawingToolbarAction");
```
#### Parameters[​](#parameters-14)
NameTypeDescription`actionId`[`ChartActionId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#chartactionid)An action ID.
#### Returns[​](#returns-21)
`void`

### exportData[​](#exportdata)
▸ exportData(`options?`): `Promise`<[`ExportedData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportedData)>

Export the current data from the chart.

Example

```
// Exports series' data onlywidget.activeChart().exportData({ includeTime: false, includedStudies: [] });// Exports series' data with timeswidget.activeChart().exportData({ includedStudies: [] });// Exports series' data with with user timewidget.activeChart().exportData({ includeTime: false, includeUserTime: true, includedStudies: [] });// Exports data for the indicator which ID is STUDY_IDwidget.activeChart().exportData({ includeTime: false, includeSeries: false, includedStudies: ['STUDY_ID'] });// Exports all available data from the chartwidget.activeChart().exportData({ includeUserTime: true });// Exports series' data before 2018-01-01widget.activeChart().exportData({ includeTime: false, to: Date.UTC(2018, 0, 1) / 1000 });// Exports series' data after 2018-01-01widget.activeChart().exportData({ includeTime: false, from: Date.UTC(2018, 0, 1) / 1000 });// Exports series' data in the range between 2018-01-01 and 2018-02-01widget.activeChart().exportData({ includeTime: false, from: Date.UTC(2018, 0, 1) / 1000, to: Date.UTC(2018, 1, 1) / 1000 });// Exports all displayed data on the chartwidget.activeChart().exportData({ includeDisplayedValues: true });
```
#### Parameters[​](#parameters-15)
NameTypeDescription`options?``Partial`<[`ExportDataOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportDataOptions)>Optional object of options to control the exported data.
#### Returns[​](#returns-22)
`Promise`<[`ExportedData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportedData)>

A promise that resolves with the exported data.

### getAllPanesHeight[​](#getallpanesheight)
▸ getAllPanesHeight(): `number`[]

Get an array of the heigh of all panes.

Example

```
console.log(widget.activeChart().getAllPanesHeight());
```
#### Returns[​](#returns-23)
`number`[]

An array of heights.

### getAllShapes[​](#getallshapes)
▸ getAllShapes(): [`EntityInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EntityInfo)[]

Get an array of IDs and name for all drawings on the chart.

Example

```
widget.activeChart().getAllShapes().forEach(({ name }) => console.log(name));
```
#### Returns[​](#returns-24)
[`EntityInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EntityInfo)[]

An array of drawing information.

### getAllStudies[​](#getallstudies)
▸ getAllStudies(): [`EntityInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EntityInfo)[]

Get an array of IDs and names for all studies on the chart.

Example

```
widget.activeChart().getAllStudies().forEach(({ name }) => console.log(name));
```
#### Returns[​](#returns-25)
[`EntityInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EntityInfo)[]

An array of study information.

### getCheckableActionState[​](#getcheckableactionstate)
▸ getCheckableActionState(`actionId`): `boolean`

Get the state of a checkable action.

Example

```
if (widget.activeChart().getCheckableActionState("drawingToolbarAction")) {    // ...};
```
#### Parameters[​](#parameters-16)
NameTypeDescription`actionId`[`ChartActionId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#chartactionid)An action ID.
#### Returns[​](#returns-26)
`boolean`

`null` if the action with specified id doesn't exist or is not checkable, `true` if the action is checked, `false` otherwise.

### getLineToolsState[​](#getlinetoolsstate)
▸ getLineToolsState(): [`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState)

Get the line tools state containing the drawings on the active chart.

This method requires that the [`saveload_separate_drawings_storage`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#saveload_separate_drawings_storage) featureset is enabled.

#### Returns[​](#returns-27)
[`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState)

### getPanes[​](#getpanes)
▸ getPanes(): [`IPaneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPaneApi)[]

Get an array of API objects for interacting with the chart panes.

Example

```
widget.activeChart().getPanes()[1].moveTo(0);
```
#### Returns[​](#returns-28)
[`IPaneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPaneApi)[]

### getPriceToBarRatio[​](#getpricetobarratio)
▸ getPriceToBarRatio(): `number`

Get the chart's price to bar ratio.

Example

```
console.log(widget.activeChart().getPriceToBarRatio());
```
#### Returns[​](#returns-29)
`number`

The ratio or `null` if no ratio is defined.

### getSeries[​](#getseries)
▸ getSeries(): [`ISeriesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi)

Get the main series.

Example

```
widget.activeChart().getSeries().setVisible(false);
```
#### Returns[​](#returns-30)
[`ISeriesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi)

An API object for interacting with the main series.

### getShapeById[​](#getshapebyid)
▸ getShapeById(`entityId`): [`ILineDataSourceApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi)

Get a drawing by ID.

Example

```
widget.activeChart().getShapeById(id).bringToFront();
```
For more information, refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#manage-drawings).

#### Parameters[​](#parameters-17)
NameTypeDescription`entityId`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)A drawing ID.
#### Returns[​](#returns-31)
[`ILineDataSourceApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi)

An API object for interacting with the drawing.

### getStudyById[​](#getstudybyid)
▸ getStudyById(`entityId`): [`IStudyApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi)

Get a study by ID.

Example

```
widget.activeChart().getStudyById(id).setVisible(false);
```
#### Parameters[​](#parameters-18)
NameTypeDescription`entityId`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)The study ID.
#### Returns[​](#returns-32)
[`IStudyApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi)

An API object for interacting with the study.

### getTimeScale[​](#gettimescale)
▸ getTimeScale(): [`ITimeScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimeScaleApi)

Get an API object for interacting with the timescale.

Example

```
var time = widget.activeChart().getTimeScale().coordinateToTime(100);
```
#### Returns[​](#returns-33)
[`ITimeScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimeScaleApi)

### getTimezoneApi[​](#gettimezoneapi)
▸ getTimezoneApi(): [`ITimezoneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimezoneApi)

Get an API object for interacting with the chart timezone.

#### Returns[​](#returns-34)
[`ITimezoneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimezoneApi)

### getVisibleRange[​](#getvisiblerange)
▸ getVisibleRange(): [`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)

Get the current visible time range.

Example

```
console.log(widget.activeChart().getVisibleRange());
```
#### Returns[​](#returns-35)
[`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)

### isMaximized[​](#ismaximized)
▸ isMaximized(): `boolean`

Check if the chart is maximized or not.

#### Returns[​](#returns-36)
`boolean`

`true` if maximized, `false` otherwise.

### isPriceToBarRatioLocked[​](#ispricetobarratiolocked)
▸ isPriceToBarRatioLocked(): `boolean`

Get the locked/unlocked state of the chart's price to bar ratio.

Example

```
console.log(widget.activeChart().isPriceToBarRatioLocked());
```
#### Returns[​](#returns-37)
`boolean`

### isSelectBarRequested[​](#isselectbarrequested)
▸ isSelectBarRequested(): `boolean`

Check if bar selection mode is active or not.

Example

```
var isRequested = widget.activeChart().isSelectBarRequested();
```
#### Returns[​](#returns-38)
`boolean`

`true` if active, `false` otherwise.

### loadChartTemplate[​](#loadcharttemplate)
▸ loadChartTemplate(`templateName`): `Promise`<`void`>

Load and apply a chart template.

#### Parameters[​](#parameters-19)
NameTypeDescription`templateName``string`The name of the template to load.
#### Returns[​](#returns-39)
`Promise`<`void`>

### marketStatus[​](#marketstatus)
▸ marketStatus(): [`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`MarketStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.MarketStatus)>

Get a readonly watched value that can be used to read/subscribe to the state of the chart's market status.

#### Returns[​](#returns-40)
[`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`MarketStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.MarketStatus)>

### maximizeChart[​](#maximizechart)
▸ maximizeChart(): `void`

Maximize to its full size currently selected chart.

Example

```
widget.activeChart().maximizeChart();
```
#### Returns[​](#returns-41)
`void`

### onChartTypeChanged[​](#oncharttypechanged)
▸ onChartTypeChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`chartType`: [`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)) => `void`>

Get a subscription object for the chart type changing.

Example

```
widget.activeChart().onChartTypeChanged().subscribe(    null,    (chartType) => console.log('The type of chart is changed'));
```
#### Returns[​](#returns-42)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`chartType`: [`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)) => `void`>

A subscription object for the chart type changing.

### onDataLoaded[​](#ondataloaded)
▸ onDataLoaded(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

Get a subscription object for new data being loaded for the chart.

Example

```
widget.activeChart().onDataLoaded().subscribe(    null,    () => console.log('New history bars are loaded'),    true);
```
#### Returns[​](#returns-43)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

A subscription object for new data loaded for the chart.

### onHoveredSourceChanged[​](#onhoveredsourcechanged)
▸ onHoveredSourceChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`sourceId`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)) => `void`>

Get a subscription object for the ID of the study or series hovered by the crosshair.

#### Returns[​](#returns-44)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`sourceId`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)) => `void`>

A subscription object for the ID of the study or series hovered by the crosshair. Subscribers will be called with `null` if there is no study or series hovered.

### onIntervalChanged[​](#onintervalchanged)
▸ onIntervalChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`interval`: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring), `timeFrameParameters`: { `timeframe?`: [`TimeFrameValue`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timeframevalue)  }) => `void`>

Get a subscription object for the chart resolution (interval) changing. This method also allows you to track whether the chart's [date range](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#date-range) is changed.
The `timeframe` argument represents if a user clicks on the [time frame toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale#time-frame-toolbar) or changes the date range manually.
If `timeframe` is `undefined`, you can change a date range before data loading starts.
To do this, you can specify a time frame value or a certain date range.
Examples

The following code sample specifies a time frame value:

```
widget.activeChart().onIntervalChanged().subscribe(null, (interval, timeframeObj) =>    timeframeObj.timeframe = {        value: "12M",        type: "period-back"});
```
The following code sample specifies a certain date range:

```
widget.activeChart().onIntervalChanged().subscribe(null, (interval, timeframeObj) =>    timeframeObj.timeframe = {        from: new Date('2015-01-01').getTime() / 1000,        to: new Date('2017-01-01').getTime() / 1000,        type: "time-range"    });
```
#### Returns[​](#returns-45)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`interval`: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring), `timeFrameParameters`: { `timeframe?`: [`TimeFrameValue`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timeframevalue)  }) => `void`>

A subscription object for the chart interval (resolution) changing.

### onSymbolChanged[​](#onsymbolchanged)
▸ onSymbolChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

Get a subscription object for the chart symbol changing.

Example

```
widget.activeChart().onSymbolChanged().subscribe(null, () => console.log('The symbol is changed'));
```
#### Returns[​](#returns-46)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

A subscription object for when a symbol is resolved (ie changing resolution, timeframe, currency, etc.)

### onVisibleRangeChanged[​](#onvisiblerangechanged)
▸ onVisibleRangeChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`range`: [`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)) => `void`>

Get a subscription object for the chart's visible range changing.

Example

```
widget.activeChart().onVisibleRangeChanged().subscribe(    null,    ({ from, to }) => console.log(from, to));
```
#### Returns[​](#returns-47)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`range`: [`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)) => `void`>

A subscription object for the chart's visible range changing.

### priceFormatter[​](#priceformatter)
▸ priceFormatter(): [`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)

Returns the object with 'format' function that you can use to format the prices.

```
widget.activeChart().priceFormatter().format(123);
```
#### Returns[​](#returns-48)
[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)

### refreshMarks[​](#refreshmarks)
▸ refreshMarks(): `void`

Force the chart to re-request all bar marks and timescale marks.

Example

```
widget.activeChart().refreshMarks();
```
#### Returns[​](#returns-49)
`void`

### reloadLineToolsFromServer[​](#reloadlinetoolsfromserver)
▸ reloadLineToolsFromServer(): `void`

Manually trigger the chart to request the linetools again from the [IExternalSaveLoadAdapter.loadLineToolsAndGroups](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalSaveLoadAdapter#loadlinetoolsandgroups) method
or the 'load_line_tools' endpoint of the [Save and load REST API](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/).
This method requires that the [`saveload_separate_drawings_storage`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#saveload_separate_drawings_storage) featureset is enabled.

#### Returns[​](#returns-50)
`void`

### removeAllShapes[​](#removeallshapes)
▸ removeAllShapes(): `void`

Remove all drawings from the chart.

Example

```
widget.activeChart().removeAllShapes();
```
#### Returns[​](#returns-51)
`void`

### removeAllStudies[​](#removeallstudies)
▸ removeAllStudies(): `void`

Remove all studies from the chart.

Example

```
widget.activeChart().removeAllStudies();
```
#### Returns[​](#returns-52)
`void`

### removeEntity[​](#removeentity)
▸ removeEntity(`entityId`, `options?`): `void`

Remove an entity (e.g. drawing or study) from the chart.

Example

```
widget.activeChart().removeEntity(id);
```
#### Parameters[​](#parameters-20)
NameTypeDescription`entityId`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)The ID of the entity.`options?`[`UndoOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoOptions)Optional undo options.
#### Returns[​](#returns-53)
`void`

### requestSelectBar[​](#requestselectbar)
▸ requestSelectBar(): `Promise`<`number`>

Switch the chart to bar selection mode.

Example

```
widget.activeChart().requestSelectBar()    .then(function(time) {        console.log('user selects bar with time', time);    })    .catch(function() {        console.log('bar selection was rejected');    });
```
#### Returns[​](#returns-54)
`Promise`<`number`>

A promise that resolves to the timestamp of a bar selected by the user. Rejects if the bar selection was already requested or is cancelled.

### resetData[​](#resetdata)
▸ resetData(): `void`

Force the chart to re-request data, for example if there are [internet connection issues](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues#internet-connection-issues).
Before calling this function the IChartWidgetApi.resetCache method should be called.
Example

```
widget.activeChart().resetData();
```
#### Returns[​](#returns-55)
`void`

### resolution[​](#resolution)
▸ resolution(): [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

Get the current resolution (interval).

Example

```
console.log(widget.activeChart().resolution());
```
#### Returns[​](#returns-56)
[`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

### restoreChart[​](#restorechart)
▸ restoreChart(): `void`

Restore to its initial size currently selected chart.

Example

```
widget.activeChart().restoreChart();
```
#### Returns[​](#returns-57)
`void`

### selection[​](#selection)
▸ selection(): [`ISelectionApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISelectionApi)

Get an API object for interacting with the selection.

Example

```
widget.activeChart().selection().clear();
```
#### Returns[​](#returns-58)
[`ISelectionApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISelectionApi)

### sendBackward[​](#sendbackward)
▸ sendBackward(`sources`): `void`

Move the sources one level down in the Z-order.

Example

```
widget.activeChart().sendBackward([id]);
```
#### Parameters[​](#parameters-21)
NameTypeDescription`sources`readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]An array of source IDs.
#### Returns[​](#returns-59)
`void`

### sendToBack[​](#sendtoback)
▸ sendToBack(`entities`): `void`

Move the group to the bottom of the Z-order.

Example

```
widget.activeChart().sendToBack([id]);
```
#### Parameters[​](#parameters-22)
NameTypeDescription`entities`readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]An array of entity IDs.
#### Returns[​](#returns-60)
`void`

### setAllPanesHeight[​](#setallpanesheight)
▸ setAllPanesHeight(`heights`): `void`

Set the height for each pane in the order provided.

Example

```
console.log(widget.activeChart().setAllPanesHeight([250, 400, 200]));
```
#### Parameters[​](#parameters-23)
NameTypeDescription`heights`readonly `number`[]An array of heights.
#### Returns[​](#returns-61)
`void`

### setChartType[​](#setcharttype)
▸ setChartType(`type`, `callback?`): `void`

Change the chart's type.

Example

```
widget.activeChart().setChartType(12); // Specifies the High-low type
```
#### Parameters[​](#parameters-24)
NameTypeDescription`type`[`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)A chart type.`callback?`() => `void`An optional callback function. Called when the chart type has changed and data has loaded.
#### Returns[​](#returns-62)
`void`

A promise that resolves with a boolean value. It's `true` when the chart type has been set and `false` when setting the chart type is not possible.

### setDragExportEnabled[​](#setdragexportenabled)
▸ setDragExportEnabled(`enabled`): `void`

Enable or disable drag-to-export feature.

Example

```
// Enable drag-to-export, disable default chart drag to scrollwidget.activeChart().setDragExportEnabled(true);widget.subscribe('dragstart', (params) => {		// create a HTML element for drag image		const dragImage = createDragImage();		// set drag image     params.setDragImage(dragImage, 0, 0);     const exportData = widget.activeChart().exportData(); 	// transform export data to csv		const csvData = transformExportDataToCsv(exportData);     params.setData('text/plain', csvData); });
```
To implement drag-to-export, you need to handle the `dragstart` event in your application and set the data to the `dataTransfer` object.

#### Parameters[​](#parameters-25)
NameTypeDescription`enabled``boolean``true` to enable drag-to-export, `false` to disable.
#### Returns[​](#returns-63)
`void`

### setPriceToBarRatio[​](#setpricetobarratio)
▸ setPriceToBarRatio(`ratio`, `options?`): `void`

Set the chart's price to bar ratio.

Example

```
widget.activeChart().setPriceToBarRatio(0.4567, { disableUndo: true });
```
#### Parameters[​](#parameters-26)
NameTypeDescription`ratio``number`The new price to bar ratio.`options?`[`UndoOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoOptions)Optional undo options.
#### Returns[​](#returns-64)
`void`

### setPriceToBarRatioLocked[​](#setpricetobarratiolocked)
▸ setPriceToBarRatioLocked(`value`, `options?`): `void`

Lock or unlock the chart's price to bar ratio.

Example

```
widget.activeChart().setPriceToBarRatioLocked(true, { disableUndo: false });
```
#### Parameters[​](#parameters-27)
NameTypeDescription`value``boolean``true` to lock, `false` to unlock.`options?`[`UndoOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoOptions)Optional undo options.
#### Returns[​](#returns-65)
`void`

### setResolution[​](#setresolution)
▸ setResolution(`resolution`, `options?`): `Promise`<`boolean`>

Change the chart's interval (resolution).

Example

```
widget.activeChart().setResolution('2M');
```
Note: if you are attempting to change multiple charts (multi-chart layouts) at the same time with
multiple `setResolution` calls then you should set `doNotActivateChart` option to `true`.
#### Parameters[​](#parameters-28)
NameTypeDescription`resolution`[`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)A resolution.`options?`[`SetResolutionOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetResolutionOptions) | () => `void`Optional object of options for the new resolution or optional callback that is called when the data for the new resolution has loaded.
#### Returns[​](#returns-66)
`Promise`<`boolean`>

A promise that resolves with a boolean value. It's `true` when the resolution has been set and `false` when setting the resolution is not possible.

### setScrollEnabled[​](#setscrollenabled)
▸ setScrollEnabled(`enabled`): `void`

Enable or disable scrolling of the chart.

Example

```
widget.activeChart().setScrollEnabled(false);
```
#### Parameters[​](#parameters-29)
NameTypeDescription`enabled``boolean``true` to enable scrolling, `false` to disable.
#### Returns[​](#returns-67)
`void`

### setSymbol[​](#setsymbol)
▸ setSymbol(`symbol`, `options?`): `Promise`<`boolean`>

Change the chart's symbol.

Example

```
widget.activeChart().setSymbol('IBM');
```
Note: if you are attempting to change multiple charts (multi-chart layouts) at the same time with
multiple `setSymbol` calls then you should set `doNotActivateChart` option to `true`.
#### Parameters[​](#parameters-30)
NameTypeDescription`symbol``string`A symbol.`options?`[`SetSymbolOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetSymbolOptions) | () => `void`Optional object of options for the new symbol or optional callback that is called when the data for the new symbol has loaded.
#### Returns[​](#returns-68)
`Promise`<`boolean`>

A promise that resolves with a boolean value. It's `true` when the symbol has been set and `false` when setting the symbol is not possible.

### setTimeFrame[​](#settimeframe)
▸ setTimeFrame(`timeFrame`): `void`

Set the time frame for this chart.

Note: This action will set this chart as active in a multi-chart layout.

Example
To apply the '1Y' timeframe:
```
tvWidget.setTimeFrame({  val: { type: 'period-back', value: '12M' },  res: '1W',});
```
#### Parameters[​](#parameters-31)
NameTypeDescription`timeFrame`[`RangeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RangeOptions)Object specifying the range and resolution to be applied
#### Returns[​](#returns-69)
`void`

### setVisibleRange[​](#setvisiblerange)
▸ setVisibleRange(`range`, `options?`): `Promise`<`void`>

Scroll and/or scale the chart so a time range is visible.

Example

```
widget.activeChart().setVisibleRange(    { from: 1420156800, to: 1451433600 },    { percentRightMargin: 20 })
```
#### Parameters[​](#parameters-32)
NameTypeDescription`range`[`SetVisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#setvisibletimerange)A range that will be made visible.`options?`[`SetVisibleRangeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetVisibleRangeOptions)Optional object of options for the new visible range.
#### Returns[​](#returns-70)
`Promise`<`void`>

A promise that resolves when the visible range is set.

### setZoomEnabled[​](#setzoomenabled)
▸ setZoomEnabled(`enabled`): `void`

Enable or disable zooming of the chart.

Example

```
widget.activeChart().setZoomEnabled(false);
```
#### Parameters[​](#parameters-33)
NameTypeDescription`enabled``boolean``true` to enable zooming, `false` to disable.
#### Returns[​](#returns-71)
`void`

### shapesGroupController[​](#shapesgroupcontroller)
▸ shapesGroupController(): [`IShapesGroupControllerApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IShapesGroupControllerApi)

Get an API object for interacting with groups of drawings.
Refer to the [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#drawing-groups-api) article for more information.
Example

```
widget.activeChart().shapesGroupController().createGroupFromSelection();
```
#### Returns[​](#returns-72)
[`IShapesGroupControllerApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IShapesGroupControllerApi)

### showPropertiesDialog[​](#showpropertiesdialog)
▸ showPropertiesDialog(`studyId`): `void`

Show the properties dialog for a study or drawing.

Example

```
const chart = widget.activeChart();chart.showPropertiesDialog(chart.getAllShapes()[0].id);`
```
#### Parameters[​](#parameters-34)
NameTypeDescription`studyId`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)An ID of the study or drawing.
#### Returns[​](#returns-73)
`void`

### symbol[​](#symbol)
▸ symbol(): `string`

Get the name of the current symbol.

Example

```
console.log(widget.activeChart().symbol());
```
#### Returns[​](#returns-74)
`string`

### symbolExt[​](#symbolext)
▸ symbolExt(): [`SymbolExt`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolExt)

Get an extended information object for the current symbol.

Example

```
console.log(widget.activeChart().symbolExt().name);
```
#### Returns[​](#returns-75)
[`SymbolExt`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolExt)

### zoomOut[​](#zoomout)
▸ zoomOut(): `void`

Zoom out. The method has the same effect as clicking on the "Zoom out" button.

#### Returns[​](#returns-76)
`void`

- [Methods](#methods)[applyLineToolsState](#applylinetoolsstate)- [applyStudyTemplate](#applystudytemplate)- [availableZOrderOperations](#availablezorderoperations)- [barTimeToEndOfPeriod](#bartimetoendofperiod)- [bringForward](#bringforward)- [bringToFront](#bringtofront)- [canZoomOut](#canzoomout)- [cancelSelectBar](#cancelselectbar)- [chartType](#charttype)- [clearMarks](#clearmarks)- [createAnchoredShape](#createanchoredshape)- [createExecutionShape](#createexecutionshape)- [createMultipointShape](#createmultipointshape)- [createOrderLine](#createorderline)- [createPositionLine](#createpositionline)- [createShape](#createshape)- [createStudy](#createstudy)- [createStudyTemplate](#createstudytemplate)- [crossHairMoved](#crosshairmoved)- [dataReady](#dataready)- [endOfPeriodToBarTime](#endofperiodtobartime)- [executeActionById](#executeactionbyid)- [exportData](#exportdata)- [getAllPanesHeight](#getallpanesheight)- [getAllShapes](#getallshapes)- [getAllStudies](#getallstudies)- [getCheckableActionState](#getcheckableactionstate)- [getLineToolsState](#getlinetoolsstate)- [getPanes](#getpanes)- [getPriceToBarRatio](#getpricetobarratio)- [getSeries](#getseries)- [getShapeById](#getshapebyid)- [getStudyById](#getstudybyid)- [getTimeScale](#gettimescale)- [getTimezoneApi](#gettimezoneapi)- [getVisibleRange](#getvisiblerange)- [isMaximized](#ismaximized)- [isPriceToBarRatioLocked](#ispricetobarratiolocked)- [isSelectBarRequested](#isselectbarrequested)- [loadChartTemplate](#loadcharttemplate)- [marketStatus](#marketstatus)- [maximizeChart](#maximizechart)- [onChartTypeChanged](#oncharttypechanged)- [onDataLoaded](#ondataloaded)- [onHoveredSourceChanged](#onhoveredsourcechanged)- [onIntervalChanged](#onintervalchanged)- [onSymbolChanged](#onsymbolchanged)- [onVisibleRangeChanged](#onvisiblerangechanged)- [priceFormatter](#priceformatter)- [refreshMarks](#refreshmarks)- [reloadLineToolsFromServer](#reloadlinetoolsfromserver)- [removeAllShapes](#removeallshapes)- [removeAllStudies](#removeallstudies)- [removeEntity](#removeentity)- [requestSelectBar](#requestselectbar)- [resetData](#resetdata)- [resolution](#resolution)- [restoreChart](#restorechart)- [selection](#selection)- [sendBackward](#sendbackward)- [sendToBack](#sendtoback)- [setAllPanesHeight](#setallpanesheight)- [setChartType](#setcharttype)- [setDragExportEnabled](#setdragexportenabled)- [setPriceToBarRatio](#setpricetobarratio)- [setPriceToBarRatioLocked](#setpricetobarratiolocked)- [setResolution](#setresolution)- [setScrollEnabled](#setscrollenabled)- [setSymbol](#setsymbol)- [setTimeFrame](#settimeframe)- [setVisibleRange](#setvisiblerange)- [setZoomEnabled](#setzoomenabled)- [shapesGroupController](#shapesgroupcontroller)- [showPropertiesDialog](#showpropertiesdialog)- [symbol](#symbol)- [symbolExt](#symbolext)- [zoomOut](#zoomout)