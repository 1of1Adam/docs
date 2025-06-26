---
title: "Interface: IChartWidgetApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi/"
extracted_at: "2025-06-22T09:29:56.202Z"
---

# Interface: IChartWidgetApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IChartWidgetApi

The main chart API.

This interface can be retrieved by using the following widget ([IChartingLibraryWidget](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget)) methods:

- `chart` ([IChartingLibraryWidget.chart](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#chart))
- `activeChart` ([IChartingLibraryWidget.activeChart](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#activechart))

## Methods
### applyLineToolsState
▸ **applyLineToolsState**(`state`): `Promise`<`void`>

Apply line tools state to the chart which will restore the drawings from the saved content.

This method requires that the [`saveload_separate_drawings_storage`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#saveload_separate_drawings_storage) featureset is enabled.

#### Parameters

 **|Name** | **Type** ||
| `state` | [`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState) ||

#### Returns
`Promise`<`void`>

### applyStudyTemplate
▸ **applyStudyTemplate**(`template`): `void`

Apply a study template to the chart.

**Example**

```
widget.activeChart().applyStudyTemplate(template);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `template` | `object` | A study template object. ||

#### Returns
`void`

### availableZOrderOperations
▸ **availableZOrderOperations**(`sources`): [`AvailableZOrderOperations`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AvailableZOrderOperations)

Get an object with operations available for the specified set of entities.

**Example**

```
widget.activeChart().availableZOrderOperations([id]);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `sources` | readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | An array of entity IDs. ||

#### Returns
[`AvailableZOrderOperations`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AvailableZOrderOperations)

### barTimeToEndOfPeriod
▸ **barTimeToEndOfPeriod**(`unixTime`): `number`

Get the bar time to the end of the period

#### Parameters

 **|Name** | **Type** | **Description** ||
| `unixTime` | `number` | date timestamp ||

#### Returns
`number`

### bringForward
▸ **bringForward**(`sources`): `void`

Move the sources one level up in the Z-order.

**Example**

```
widget.activeChart().bringForward([id]);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `sources` | readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | An array of source IDs. ||

#### Returns
`void`

### bringToFront
▸ **bringToFront**(`sources`): `void`

Move the sources to the top of the Z-order.

**Example**

```
widget.activeChart().bringToFront([id]);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `sources` | readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | An array of source IDs. ||

#### Returns
`void`

### canZoomOut
▸ **canZoomOut**(): `boolean`

Check if the chart can be zoomed out using the [zoomOut](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#zoomout) method.

**Example**

```
if(widget.activeChart().canZoomOut()) {
    widget.activeChart().zoomOut();
};

```
#### Returns
`boolean`

`true` if the chart can be zoomed out.

### cancelSelectBar
▸ **cancelSelectBar**(): `void`

Cancel any active bar selection requests.

**Example**

```
widget.activeChart().cancelSelectBar();

```
#### Returns
`void`

### chartType
▸ **chartType**(): [`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)

Returns the main series style type.

```
console.log(widget.activeChart().chartType());

```
#### Returns
[`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)

### clearMarks
▸ **clearMarks**(`marksToClear?`): `void`

Remove marks from the chart.

**Example**

```
widget.activeChart().clearMarks();

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `marksToClear?` | [`ClearMarksMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ClearMarksMode) | type of marks to clear. If nothing is specified both bar & timescale marks will be removed. ||

#### Returns
`void`

### createAnchoredShape
▸ **createAnchoredShape**<`TOverrides`>(`position`, `options`): `Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Create a new anchored drawing. Anchored drawings maintain their position when the chart's visible range changes.

**Example**

```
widget.createAnchoredShape({ x: 0.1, y: 0.9 }, { shape: 'anchored_text', text: 'Hello, charts!', overrides: { color: 'green' }});

```
For more information, refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#createanchoredshape).

#### Type parameters

 **|Name** | **Type** ||
| `TOverrides` | extends `object` ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `position` | [`PositionPercents`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionPercents) | Percent-based x and y position of the new drawing, relative to the top left of the chart. ||
| `options` | [`CreateAnchoredShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateAnchoredShapeOptions)<`TOverrides`> | An options object for the new drawing. ||

#### Returns
`Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

### createExecutionShape
▸ **createExecutionShape**(): `Promise`<[`IExecutionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExecutionLineAdapter)>

Creates a new trade execution on the chart.
Starting from version 29, this method is only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).
**Example**
```
const executionLine = widget.activeChart().createExecutionShape();
executionLine
    .setText("@1,320.75 Limit Buy 1")
    .setTooltip("@1,320.75 Limit Buy 1")
    .setTextColor("rgba(0,255,0,0.5)")
    .setArrowColor("#0F0")
    .setDirection("buy")
    .setTime(widget.activeChart().getVisibleRange().from)
    .setPrice(160);

```
#### Returns
`Promise`<[`IExecutionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExecutionLineAdapter)>

An API object for interacting with the execution.

### createMultipointShape
▸ **createMultipointShape**<`TOverrides`>(`points`, `options`): `Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Create a new multi point drawing.

**Example**

```
const from = Date.now() / 1000 - 500 * 24 * 3600; // 500 days ago
const to = Date.now() / 1000;
widget.activeChart().createMultipointShape(
    [{ time: from, price: 150 }, { time: to, price: 150 }],
    {
        shape: "trend_line",
        lock: true,
        disableSelection: true,
        disableSave: true,
        disableUndo: true,
        text: "text",
    }
);

```
For more information, refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#createmultipointshape).

#### Type parameters

 **|Name** | **Type** ||
| `TOverrides` | extends `object` ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `points` | [`ShapePoint`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapepoint) | An array of points that define the drawing. ||
| `options` | [`CreateMultipointShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateMultipointShapeOptions)<`TOverrides`> | An options object for the new drawing. ||

#### Returns
`Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Promise of the ID for the new drawing if it was created successfully.

### createOrderLine
▸ **createOrderLine**(): `Promise`<[`IOrderLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IOrderLineAdapter)>

Creates a new trading order on the chart.
Starting from version 29, this method is only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).
**Example**

```
const orderLine = await widget.activeChart().createOrderLine();
orderLine
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
#### Returns
`Promise`<[`IOrderLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IOrderLineAdapter)>

An API object for interacting with the order.

### createPositionLine
▸ **createPositionLine**(): `Promise`<[`IPositionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPositionLineAdapter)>

Creates a new trading position on the chart.
Starting from version 29, this method is only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).
**Example**

```
const positionLine = await widget.chart().createPositionLine();
positionLine
    .onModify(function() {
        this.setText("onModify called");
    })
    .onReverse("onReverse called", function(text) {
        this.setText(text);
    })
    .onClose("onClose called", function(text) {
        this.setText(text);
    })
    .setText("PROFIT: 71.1 (3.31%)")
    .setTooltip("Additional position information")
    .setProtectTooltip("Protect position")
    .setCloseTooltip("Close position")
    .setReverseTooltip("Reverse position")
    .setQuantity("8.235")
    .setPrice(160)
    .setExtendLeft(false)
    .setLineStyle(0)
    .setLineLength(25);

```
#### Returns
`Promise`<[`IPositionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPositionLineAdapter)>

An API object for interacting with the position.

### createShape
▸ **createShape**<`TOverrides`>(`point`, `options`): `Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Create a new single point drawing.

**Example**

```
widget.activeChart().createShape({ time: 1514764800 }, { shape: 'vertical_line' });

```
For more information, refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#createshape).

#### Type parameters

 **|Name** | **Type** ||
| `TOverrides` | extends `object` ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `point` | [`ShapePoint`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapepoint) | A point. The location of the new drawing. ||
| `options` | [`CreateShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions)<`TOverrides`> | An options object for the new drawing. ||

#### Returns
`Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Promise of the ID for the new drawing if it was created successfully.

### createStudy
▸ **createStudy**<`TOverrides`>(`name`, `forceOverlay?`, `lock?`, `inputs?`, `overrides?`, `options?`): `Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

Adds an indicator or a symbol for comparison to the chart.
For more information, refer to the [Indicators](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/) article.
#### Type parameters

 **|Name** | **Type** ||
| `TOverrides` | extends `Partial`<[`SingleIndicatorOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#singleindicatoroverrides)> ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `name` | `string` | name of an indicator as shown in the `Indicators` widget ||
| `forceOverlay?` | `boolean` | forces the Charting Library to place the created indicator on the main pane ||
| `lock?` | `boolean` | whether a user will be able to remove/change/hide the indicator or not ||
| `inputs?` | `Record`<`string`, [`StudyInputValue`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyinputvalue)> | **From version v22**, it's an object containing named properties from the indicator properties dialog. ||
| `overrides?` | `TOverrides` | An object that contains [overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#customize-a-single-indicator) for a new indicator. Note that you should not specify the indicator name. Overrides for built-in indicators are listed in [`SingleIndicatorOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#singleindicatoroverrides). ||
| `options?` | [`CreateStudyOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateStudyOptions) | study creation options ||

#### Returns
`Promise`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)>

ID of the created study

### createStudyTemplate
▸ **createStudyTemplate**(`options`): `object`

Save the current study template to a object.

**Example**

```
const options = { saveSymbol: true, saveInterval: true };
const template = widget.activeChart().createStudyTemplate(options);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `options` | [`CreateStudyTemplateOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateStudyTemplateOptions) | An object of study template options. ||

#### Returns
`object`

A study template object.

### crossHairMoved
▸ **crossHairMoved**(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`params`: [`CrossHairMovedEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CrossHairMovedEventParams)) => `void`>

Get a subscription object for the crosshair moving over the chart.

**Example**

```
widget.activeChart().crossHairMoved().subscribe(
    null,
    ({ time, price }) => console.log(time, price)
);

```
#### Returns
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`params`: [`CrossHairMovedEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CrossHairMovedEventParams)) => `void`>

A subscription object for the crosshair moving over the chart.

### dataReady
▸ **dataReady**(`callback?`): `boolean`

Provide a callback function that will be called when chart data is loaded.
If chart data is already loaded when this method is called, the callback is called immediately.
**Example**

```
widget.activeChart().dataReady(() => {
    // ...
}

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `callback?` | () => `void` | A callback function called when chart data is loaded. ||

#### Returns
`boolean`

### endOfPeriodToBarTime
▸ **endOfPeriodToBarTime**(`unixTime`): `number`

Get the end of period to bar time

#### Parameters

 **|Name** | **Type** | **Description** ||
| `unixTime` | `number` | date timestamp ||

#### Returns
`number`

### executeActionById
▸ **executeActionById**(`actionId`): `void`

Execute an action by ID.
See [Chart methods](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Chart#execute-action-by-id) for more information.
**Example**

```
// Undoes the last applied action
widget.activeChart().executeActionById("undo");

// Opens or hides the drawing toolbar
widget.activeChart().executeActionById("drawingToolbarAction");

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `actionId` | [`ChartActionId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#chartactionid) | An action ID. ||

#### Returns
`void`

### exportData
▸ **exportData**(`options?`): `Promise`<[`ExportedData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportedData)>

Export the current data from the chart.

**Example**

```
// Exports series' data only
widget.activeChart().exportData({ includeTime: false, includedStudies:  });
// Exports series' data with times
widget.activeChart().exportData({ includedStudies:  });
// Exports series' data with with user time
widget.activeChart().exportData({ includeTime: false, includeUserTime: true, includedStudies:  });
// Exports data for the indicator which ID is STUDY_ID
widget.activeChart().exportData({ includeTime: false, includeSeries: false, includedStudies: ['STUDY_ID'] });
// Exports all available data from the chart
widget.activeChart().exportData({ includeUserTime: true });
// Exports series' data before 2018-01-01
widget.activeChart().exportData({ includeTime: false, to: Date.UTC(2018, 0, 1) / 1000 });
// Exports series' data after 2018-01-01
widget.activeChart().exportData({ includeTime: false, from: Date.UTC(2018, 0, 1) / 1000 });
// Exports series' data in the range between 2018-01-01 and 2018-02-01
widget.activeChart().exportData({ includeTime: false, from: Date.UTC(2018, 0, 1) / 1000, to: Date.UTC(2018, 1, 1) / 1000 });
// Exports all displayed data on the chart
widget.activeChart().exportData({ includeDisplayedValues: true });

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `options?` | `Partial`<[`ExportDataOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportDataOptions)> | Optional object of options to control the exported data. ||

#### Returns
`Promise`<[`ExportedData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportedData)>

A promise that resolves with the exported data.

### getAllPanesHeight
▸ **getAllPanesHeight**(): `number`

Get an array of the heigh of all panes.

**Example**

```
console.log(widget.activeChart().getAllPanesHeight());

```
#### Returns
`number`

An array of heights.

### getAllShapes
▸ **getAllShapes**(): [`EntityInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EntityInfo)

Get an array of IDs and name for all drawings on the chart.

**Example**

```
widget.activeChart().getAllShapes().forEach(({ name }) => console.log(name));

```
#### Returns
[`EntityInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EntityInfo)

An array of drawing information.

### getAllStudies
▸ **getAllStudies**(): [`EntityInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EntityInfo)

Get an array of IDs and names for all studies on the chart.

**Example**

```
widget.activeChart().getAllStudies().forEach(({ name }) => console.log(name));

```
#### Returns
[`EntityInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EntityInfo)

An array of study information.

### getCheckableActionState
▸ **getCheckableActionState**(`actionId`): `boolean`

Get the state of a checkable action.

**Example**

```
if (widget.activeChart().getCheckableActionState("drawingToolbarAction")) {
    // ...
};

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `actionId` | [`ChartActionId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#chartactionid) | An action ID. ||

#### Returns
`boolean`

`null` if the action with specified id doesn't exist or is not checkable, `true` if the action is checked, `false` otherwise.

### getLineToolsState
▸ **getLineToolsState**(): [`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState)

Get the line tools state containing the drawings on the active chart.

This method requires that the [`saveload_separate_drawings_storage`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#saveload_separate_drawings_storage) featureset is enabled.

#### Returns
[`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState)

### getPanes
▸ **getPanes**(): [`IPaneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPaneApi)

Get an array of API objects for interacting with the chart panes.

**Example**

```
widget.activeChart().getPanes()[1].moveTo(0);

```
#### Returns
[`IPaneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPaneApi)

### getPriceToBarRatio
▸ **getPriceToBarRatio**(): `number`

Get the chart's price to bar ratio.

**Example**

```
console.log(widget.activeChart().getPriceToBarRatio());

```
#### Returns
`number`

The ratio or `null` if no ratio is defined.

### getSeries
▸ **getSeries**(): [`ISeriesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi)

Get the main series.

**Example**

```
widget.activeChart().getSeries().setVisible(false);

```
#### Returns
[`ISeriesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi)

An API object for interacting with the main series.

### getShapeById
▸ **getShapeById**(`entityId`): [`ILineDataSourceApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi)

Get a drawing by ID.

**Example**

```
widget.activeChart().getShapeById(id).bringToFront();

```
For more information, refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#manage-drawings).

#### Parameters

 **|Name** | **Type** | **Description** ||
| `entityId` | [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | A drawing ID. ||

#### Returns
[`ILineDataSourceApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi)

An API object for interacting with the drawing.

### getStudyById
▸ **getStudyById**(`entityId`): [`IStudyApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi)

Get a study by ID.

**Example**

```
widget.activeChart().getStudyById(id).setVisible(false);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `entityId` | [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | The study ID. ||

#### Returns
[`IStudyApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi)

An API object for interacting with the study.

### getTimeScale
▸ **getTimeScale**(): [`ITimeScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimeScaleApi)

Get an API object for interacting with the timescale.

**Example**

```
var time = widget.activeChart().getTimeScale().coordinateToTime(100);

```
#### Returns
[`ITimeScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimeScaleApi)

### getTimezoneApi
▸ **getTimezoneApi**(): [`ITimezoneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimezoneApi)

Get an API object for interacting with the chart timezone.

#### Returns
[`ITimezoneApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimezoneApi)

### getVisibleRange
▸ **getVisibleRange**(): [`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)

Get the current visible time range.

**Example**

```
console.log(widget.activeChart().getVisibleRange());

```
#### Returns
[`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)

### isMaximized
▸ **isMaximized**(): `boolean`

Check if the chart is maximized or not.

#### Returns
`boolean`

`true` if maximized, `false` otherwise.

### isPriceToBarRatioLocked
▸ **isPriceToBarRatioLocked**(): `boolean`

Get the locked/unlocked state of the chart's price to bar ratio.

**Example**

```
console.log(widget.activeChart().isPriceToBarRatioLocked());

```
#### Returns
`boolean`

### isSelectBarRequested
▸ **isSelectBarRequested**(): `boolean`

Check if bar selection mode is active or not.

**Example**

```
var isRequested = widget.activeChart().isSelectBarRequested();

```
#### Returns
`boolean`

`true` if active, `false` otherwise.

### loadChartTemplate
▸ **loadChartTemplate**(`templateName`): `Promise`<`void`>

Load and apply a chart template.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `templateName` | `string` | The name of the template to load. ||

#### Returns
`Promise`<`void`>

### marketStatus
▸ **marketStatus**(): [`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`MarketStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.MarketStatus)>

Get a readonly watched value that can be used to read/subscribe to the state of the chart's market status.

#### Returns
[`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`MarketStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.MarketStatus)>

### maximizeChart
▸ **maximizeChart**(): `void`

Maximize to its full size currently selected chart.

**Example**

```
widget.activeChart().maximizeChart();

```
#### Returns
`void`

### onChartTypeChanged
▸ **onChartTypeChanged**(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`chartType`: [`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)) => `void`>

Get a subscription object for the chart type changing.

**Example**

```
widget.activeChart().onChartTypeChanged().subscribe(
    null,
    (chartType) => console.log('The type of chart is changed')
);

```
#### Returns
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`chartType`: [`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)) => `void`>

A subscription object for the chart type changing.

### onDataLoaded
▸ **onDataLoaded**(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

Get a subscription object for new data being loaded for the chart.

**Example**

```
widget.activeChart().onDataLoaded().subscribe(
    null,
    () => console.log('New history bars are loaded'),
    true
);

```
#### Returns
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

A subscription object for new data loaded for the chart.

### onHoveredSourceChanged
▸ **onHoveredSourceChanged**(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`sourceId`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)) => `void`>

Get a subscription object for the ID of the study or series hovered by the crosshair.

#### Returns
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`sourceId`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)) => `void`>

A subscription object for the ID of the study or series hovered by the crosshair. Subscribers will be called with `null` if there is no study or series hovered.

### onIntervalChanged
▸ **onIntervalChanged**(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`interval`: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring), `timeFrameParameters`: { `timeframe?`: [`TimeFrameValue`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timeframevalue)  }) => `void`>

Get a subscription object for the chart resolution (interval) changing. This method also allows you to track whether the chart's [date range](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#date-range) is changed.
The `timeframe` argument represents if a user clicks on the [time frame toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale#time-frame-toolbar) or changes the date range manually.
If `timeframe` is `undefined`, you can change a date range before data loading starts.
To do this, you can specify a time frame value or a certain date range.
**Examples**

The following code sample specifies a time frame value:

```
widget.activeChart().onIntervalChanged().subscribe(null, (interval, timeframeObj) =>
    timeframeObj.timeframe = {
        value: "12M",
        type: "period-back"
});

```
The following code sample specifies a certain date range:

```
widget.activeChart().onIntervalChanged().subscribe(null, (interval, timeframeObj) =>
    timeframeObj.timeframe = {
        from: new Date('2015-01-01').getTime() / 1000,
        to: new Date('2017-01-01').getTime() / 1000,
        type: "time-range"
    });

```
#### Returns
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`interval`: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring), `timeFrameParameters`: { `timeframe?`: [`TimeFrameValue`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timeframevalue)  }) => `void`>

A subscription object for the chart interval (resolution) changing.

### onSymbolChanged
▸ **onSymbolChanged**(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

Get a subscription object for the chart symbol changing.

**Example**

```
widget.activeChart().onSymbolChanged().subscribe(null, () => console.log('The symbol is changed'));

```
#### Returns
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

A subscription object for when a symbol is resolved (ie changing resolution, timeframe, currency, etc.)

### onVisibleRangeChanged
▸ **onVisibleRangeChanged**(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`range`: [`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)) => `void`>

Get a subscription object for the chart's visible range changing.

**Example**

```
widget.activeChart().onVisibleRangeChanged().subscribe(
    null,
    ({ from, to }) => console.log(from, to)
);

```
#### Returns
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`range`: [`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)) => `void`>

A subscription object for the chart's visible range changing.

### priceFormatter
▸ **priceFormatter**(): [`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)

Returns the object with 'format' function that you can use to format the prices.

```
widget.activeChart().priceFormatter().format(123);

```
#### Returns
[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)

### refreshMarks
▸ **refreshMarks**(): `void`

Force the chart to re-request all bar marks and timescale marks.

**Example**

```
widget.activeChart().refreshMarks();

```
#### Returns
`void`

### reloadLineToolsFromServer
▸ **reloadLineToolsFromServer**(): `void`

Manually trigger the chart to request the linetools again from the [IExternalSaveLoadAdapter.loadLineToolsAndGroups](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalSaveLoadAdapter#loadlinetoolsandgroups) method
or the 'load_line_tools' endpoint of the [Save and load REST API](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/).
This method requires that the [`saveload_separate_drawings_storage`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#saveload_separate_drawings_storage) featureset is enabled.

#### Returns
`void`

### removeAllShapes
▸ **removeAllShapes**(): `void`

Remove all drawings from the chart.

**Example**

```
widget.activeChart().removeAllShapes();

```
#### Returns
`void`

### removeAllStudies
▸ **removeAllStudies**(): `void`

Remove all studies from the chart.

**Example**

```
widget.activeChart().removeAllStudies();

```
#### Returns
`void`

### removeEntity
▸ **removeEntity**(`entityId`, `options?`): `void`

Remove an entity (e.g. drawing or study) from the chart.

**Example**

```
widget.activeChart().removeEntity(id);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `entityId` | [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | The ID of the entity. ||
| `options?` | [`UndoOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoOptions) | Optional undo options. ||

#### Returns
`void`

### requestSelectBar
▸ **requestSelectBar**(): `Promise`<`number`>

Switch the chart to bar selection mode.

**Example**

```
widget.activeChart().requestSelectBar()
    .then(function(time) {
        console.log('user selects bar with time', time);
    })
    .catch(function() {
        console.log('bar selection was rejected');
    });

```
#### Returns
`Promise`<`number`>

A promise that resolves to the timestamp of a bar selected by the user. Rejects if the bar selection was already requested or is cancelled.

### resetData
▸ **resetData**(): `void`

Force the chart to re-request data, for example if there are [internet connection issues](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues#internet-connection-issues).
Before calling this function the IChartWidgetApi.resetCache method should be called.
**Example**

```
widget.activeChart().resetData();

```
#### Returns
`void`

### resolution
▸ **resolution**(): [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

Get the current resolution (interval).

**Example**

```
console.log(widget.activeChart().resolution());

```
#### Returns
[`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

### restoreChart
▸ **restoreChart**(): `void`

Restore to its initial size currently selected chart.

**Example**

```
widget.activeChart().restoreChart();

```
#### Returns
`void`

### selection
▸ **selection**(): [`ISelectionApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISelectionApi)

Get an API object for interacting with the selection.

**Example**

```
widget.activeChart().selection().clear();

```
#### Returns
[`ISelectionApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISelectionApi)

### sendBackward
▸ **sendBackward**(`sources`): `void`

Move the sources one level down in the Z-order.

**Example**

```
widget.activeChart().sendBackward([id]);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `sources` | readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | An array of source IDs. ||

#### Returns
`void`

### sendToBack
▸ **sendToBack**(`entities`): `void`

Move the group to the bottom of the Z-order.

**Example**

```
widget.activeChart().sendToBack([id]);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `entities` | readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | An array of entity IDs. ||

#### Returns
`void`

### setAllPanesHeight
▸ **setAllPanesHeight**(`heights`): `void`

Set the height for each pane in the order provided.

**Example**

```
console.log(widget.activeChart().setAllPanesHeight([250, 400, 200]));

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `heights` | readonly `number` | An array of heights. ||

#### Returns
`void`

### setChartType
▸ **setChartType**(`type`, `callback?`): `void`

Change the chart's type.

**Example**

```
widget.activeChart().setChartType(12); // Specifies the High-low type

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `type` | [`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType) | A chart type. ||
| `callback?` | () => `void` | An optional callback function. Called when the chart type has changed and data has loaded. ||

#### Returns
`void`

A promise that resolves with a boolean value. It's `true` when the chart type has been set and `false` when setting the chart type is not possible.

### setDragExportEnabled
▸ **setDragExportEnabled**(`enabled`): `void`

Enable or disable drag-to-export feature.

**Example**

```
// Enable drag-to-export, disable default chart drag to scroll
widget.activeChart().setDragExportEnabled(true);
widget.subscribe('dragstart', (params) => {
		// create a HTML element for drag image
		const dragImage = createDragImage();
		// set drag image
     params.setDragImage(dragImage, 0, 0);
     const exportData = widget.activeChart().exportData();
 	// transform export data to csv
		const csvData = transformExportDataToCsv(exportData);
     params.setData('text/plain', csvData);
 });

```
To implement drag-to-export, you need to handle the `dragstart` event in your application and set the data to the `dataTransfer` object.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `enabled` | `boolean` | `true` to enable drag-to-export, `false` to disable. ||

#### Returns
`void`

### setPriceToBarRatio
▸ **setPriceToBarRatio**(`ratio`, `options?`): `void`

Set the chart's price to bar ratio.

**Example**

```
widget.activeChart().setPriceToBarRatio(0.4567, { disableUndo: true });

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `ratio` | `number` | The new price to bar ratio. ||
| `options?` | [`UndoOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoOptions) | Optional undo options. ||

#### Returns
`void`

### setPriceToBarRatioLocked
▸ **setPriceToBarRatioLocked**(`value`, `options?`): `void`

Lock or unlock the chart's price to bar ratio.

**Example**

```
widget.activeChart().setPriceToBarRatioLocked(true, { disableUndo: false });

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `value` | `boolean` | `true` to lock, `false` to unlock. ||
| `options?` | [`UndoOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoOptions) | Optional undo options. ||

#### Returns
`void`

### setResolution
▸ **setResolution**(`resolution`, `options?`): `Promise`<`boolean`>

Change the chart's interval (resolution).

**Example**

```
widget.activeChart().setResolution('2M');

```
Note: if you are attempting to change multiple charts (multi-chart layouts) at the same time with
multiple `setResolution` calls then you should set `doNotActivateChart` option to `true`.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `resolution` | [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring) | A resolution. ||
| `options?` | [`SetResolutionOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetResolutionOptions) | () => `void` | Optional object of options for the new resolution or optional callback that is called when the data for the new resolution has loaded. ||

#### Returns
`Promise`<`boolean`>

A promise that resolves with a boolean value. It's `true` when the resolution has been set and `false` when setting the resolution is not possible.

### setScrollEnabled
▸ **setScrollEnabled**(`enabled`): `void`

Enable or disable scrolling of the chart.

**Example**

```
widget.activeChart().setScrollEnabled(false);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `enabled` | `boolean` | `true` to enable scrolling, `false` to disable. ||

#### Returns
`void`

### setSymbol
▸ **setSymbol**(`symbol`, `options?`): `Promise`<`boolean`>

Change the chart's symbol.

**Example**

```
widget.activeChart().setSymbol('IBM');

```
Note: if you are attempting to change multiple charts (multi-chart layouts) at the same time with
multiple `setSymbol` calls then you should set `doNotActivateChart` option to `true`.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | A symbol. ||
| `options?` | [`SetSymbolOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetSymbolOptions) | () => `void` | Optional object of options for the new symbol or optional callback that is called when the data for the new symbol has loaded. ||

#### Returns
`Promise`<`boolean`>

A promise that resolves with a boolean value. It's `true` when the symbol has been set and `false` when setting the symbol is not possible.

### setTimeFrame
▸ **setTimeFrame**(`timeFrame`): `void`

Set the time frame for this chart.

**Note:** This action will set this chart as active in a multi-chart layout.

**Example**
To apply the '1Y' timeframe:
```
tvWidget.setTimeFrame({
  val: { type: 'period-back', value: '12M' },
  res: '1W',
});

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `timeFrame` | [`RangeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RangeOptions) | Object specifying the range and resolution to be applied ||

#### Returns
`void`

### setVisibleRange
▸ **setVisibleRange**(`range`, `options?`): `Promise`<`void`>

Scroll and/or scale the chart so a time range is visible.

**Example**

```
widget.activeChart().setVisibleRange(
    { from: 1420156800, to: 1451433600 },
    { percentRightMargin: 20 }
)

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `range` | [`SetVisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#setvisibletimerange) | A range that will be made visible. ||
| `options?` | [`SetVisibleRangeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetVisibleRangeOptions) | Optional object of options for the new visible range. ||

#### Returns
`Promise`<`void`>

A promise that resolves when the visible range is set.

### setZoomEnabled
▸ **setZoomEnabled**(`enabled`): `void`

Enable or disable zooming of the chart.

**Example**

```
widget.activeChart().setZoomEnabled(false);

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `enabled` | `boolean` | `true` to enable zooming, `false` to disable. ||

#### Returns
`void`

### shapesGroupController
▸ **shapesGroupController**(): [`IShapesGroupControllerApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IShapesGroupControllerApi)

Get an API object for interacting with groups of drawings.
Refer to the [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#drawing-groups-api) article for more information.
**Example**

```
widget.activeChart().shapesGroupController().createGroupFromSelection();

```
#### Returns
[`IShapesGroupControllerApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IShapesGroupControllerApi)

### showPropertiesDialog
▸ **showPropertiesDialog**(`studyId`): `void`

Show the properties dialog for a study or drawing.

**Example**

```
const chart = widget.activeChart();
chart.showPropertiesDialog(chart.getAllShapes()[0].id);`

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `studyId` | [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | An ID of the study or drawing. ||

#### Returns
`void`

### symbol
▸ **symbol**(): `string`

Get the name of the current symbol.

**Example**

```
console.log(widget.activeChart().symbol());

```
#### Returns
`string`

### symbolExt
▸ **symbolExt**(): [`SymbolExt`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolExt)

Get an extended information object for the current symbol.

**Example**

```
console.log(widget.activeChart().symbolExt().name);

```
#### Returns
[`SymbolExt`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolExt)

### zoomOut
▸ **zoomOut**(): `void`

Zoom out. The method has the same effect as clicking on the "Zoom out" button.

#### Returns
`void`