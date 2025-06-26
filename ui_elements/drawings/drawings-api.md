---
title: "Drawings API | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api"
extracted_at: "2025-06-22T09:28:37.108Z"
---

# Drawings APIThis article describes how to manage drawings using the API.

> **Info:** Methods listed in this article are part of the [`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi) interface. To call these methods, you should use an `IChartWidgetApi` instance. To do this, use either the [`chart`](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods#chart) or [`activeChart`](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods#activechart) method.
For more information, refer to [Widget methods](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods).

## Create drawings
When you create a drawing, you need to specify its position on the chart. The position can be determined with either one or multiple points.
To create a drawing, use one of the methods below depending on the drawing type and number of points it requires.
### createShape
The [`createShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createshape) method allows you to create a drawing which position on the chart can be determined by only one point. For example, you can create arrows, vertical or horizontal lines, icons, and more. To do this, call `createShape` and pass information about the point and drawing as parameters.

#### Point
You should specify one of the objects below to provide information about the point.

- [`StickedPoint`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StickedPoint). A point is determined by an OHLC price on a bar at a specified timestamp.
- [`PricedPoint`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PricedPoint). A point is determined by a price and timestamp.
- [`TimePoint`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimePoint). A point is determined by a timestamp.

When you specify a drawing point, use timestamps that have associated data points on the chart.
Otherwise, the library adjusts the time value to the nearest appropriate point.
For example, the current chart resolution is one hour, and the following bars are displayed on the chart: `[09:00, 10:00, 11:00, ...]`.
If you specify a drawing at 09:30, the library shifts it to 09:00.
Moreover, if you change the resolution to 30 minutes and the data point at 09:30 appears, the library will still display the drawing at 09:00.
#### Drawing
You should specify a [`CreateShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions) object to provide information about the drawing, such as [drawing type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions#shape) and [overrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions#overrides), and configure user control over drawings. For example, you can use the [`lock`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions#lock) property to disable moving and deleting drawings in the UI.

Consider the code sample below that creates a play icon.

```
widget.chart().createShape(
    { time: 1514796562, price: 150 },
    {
      shape: "icon",
      icon: 0xf0da,
    }
)

```
Note that the [`icon`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions#icon) value should be a **hex number**, not a string.

### createMultipointShape
The [`createMultipointShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createmultipointshape) method allows you to create a drawing which position on the chart is determined by multiple points. For example, you can create triangles, trend lines, rectangles, and more. To do this, call `createMultipointShape` and pass an array of [points](#point) and a [`CreateMultipointShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateMultipointShapeOptions) object as parameters.

> **Tip:** You can check the number of required points in the *Settings* dialog of a certain drawing. If you pass a wrong number of points, you get the following issue: *Error: Wrong points count for "drawing_name". Required "number"*.

Consider the CodePen below that displays [*Parallel Channel*](https://www.tradingview.com/ideas/parallelchannel/?solution=43000518117) and *Info Line* right after the chart is loaded.

See the Pen 
Creating multipoint drawings by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
### createExecutionShape
The [`createExecutionShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createexecutionshape) method allows you to display an execution drawing on the chart. The execution is represented with buy/sell arrows. Unlike other types of drawings, users cannot change or move the execution drawings in the UI.

The `createExecutionShape` method returns an instance of the [`IExecutionLineAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExecutionLineAdapter) interface that provides an extensive API for adjusting the drawing settings. For example, you can specify an arrow color and text. Note that you cannot change the arrow size.

> **Tip:** If execution drawings created via `createExecutionShape` do not meet your requirements, you can emulate these drawings using the [`createShape`](#createshape) method.

Consider the CodePen below that demonstrates how to display buy/sell arrows using `createExecutionShape`and `createShape`. These arrows represent trading history.

See the Pen 
Drawings. Buy/Sell arrows by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
### createAnchoredShape
The [`createAnchoredShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createanchoredshape) method allows you to create an anchored drawing. These drawings are fixed on the same position and do not move when a user scrolls the chart. The drawing points are measured as percentage from the top-left corner of the chart.

To create an anchored drawing, call the `createAnchoredShape` method and pass a [`PositionPercents`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionPercents) and [`CreateAnchoredShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateAnchoredShapeOptions) objects as parameters.
For example, the code sample below creates an anchored text.
```
widget.activeChart().createAnchoredShape(
    { x: 0.1, y: 0.3 },
    { shape: "anchored_text", text: "This is an anchored drawing", overrides: { color: "green" }}
);

```
![Anchored drawing](https://www.tradingview.com/charting-library-docs/assets/images/anchored-drawing-194baa17ff0884270d082f959c24d65a.gif)
## Attach drawing to indicator
You can attach a drawing to a certain indicator on the chart.
To do this, specify the `ownerStudyId` property when you create a drawing using the methods [above](#create-drawings).
For example, the code sample below attaches an icon to the [*Exponential Moving Average (EMA)*](https://www.tradingview.com/support/solutions/43000592270-exponential-moving-average/) indicator.
```
// Create the EMA indicator
const emaId = await widget.activeChart().createStudy('Moving Average Exponential', false, false, { length: 26 });
// Draw an icon and attach it to EMA
widget.chart().createShape(
    { time: 1714796562, price: 170 },
    {
        shape: "icon",
        icon: 0xf0da,
        ownerStudyId: emaId,
    }
)

```
The attached drawing follows the indicator when the indicator is moved to another [pane](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#pane).
If you delete the indicator, all attached drawings are also deleted.
By default, drawings are displayed on the pane with the main [series](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#series). You can use `ownerStudyId` to display a drawing on a separate pane that contains indicator. For example, the code sample below creates the [*Moving Average Convergence/Divergence (MACD)*](https://www.tradingview.com/support/solutions/43000502344-macd-moving-average-convergence-divergence/) indicator and displays an arrow on the indicator's pane.

```
// Create the MACD indicator
const macdId = await widget.activeChart().createStudy('MACD', false, false, { in_0: 14, in_1: 30, in_3: 'close', in_2: 9 });
// Draw an arrow on the MACD pane
widget.activeChart().createMultipointShape(
    [
      {
          time: 1701698287,
          price: 2,
      },
      {
          time: 1701698287,
          price: -1,
      },
    ],
    {
        shape: 'arrow',
        text: "text",
        ownerStudyId: macdId
    }
)

```
![Drawing on a separate pane](https://www.tradingview.com/charting-library-docs/assets/images/drawing-on-macd-pane-b0cc552c7eeea9b856466793fc9dc472.png)
## Manage drawings
When you create a drawing using either [`createShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createshape), [`createMultipointShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createmultipointshape), or [`createAnchoredShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createanchoredshape), the methods return the drawing's ID. You can use this ID to refer to the drawing and manage it. For example, you can specify if users can select the drawing in the UI
or change drawing properties.
To do this, use the [`getShapeById`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getshapebyid) method and pass an ID as a parameter. `getShapeById` returns an instance of the [`ILineDataSourceApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi) interface that provides an extensive API for controlling the drawing.
The code sample below gets all drawing properties.

```
widget.activeChart().getShapeById(id).getProperties();

```
## Get drawings
To get a list of all drawings on the chart and their IDs, use the [`getAllShapes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getallshapes) method.

```
widget.activeChart().getAllShapes();

```
## Remove drawings
### removeEntity
When you create a drawing using either [`createShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createshape), [`createMultipointShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createmultipointshape), or [`createAnchoredShape`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createanchoredshape), the methods return the drawing's ID via a Promise. You can use this ID to remove the drawing from the chart.
To do this, use the [`removeEntity`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#removeentity) method.
```
widget.activeChart().removeEntity(id);

```
### removeAllShapes
To remove all drawings from the chart, use the [`removeAllShapes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#removeallshapes) method.

```
widget.activeChart().removeAllShapes();

```
## Drawing events
To handle an event raised when a drawing is added to the chart, call the [`subscribe`](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods#subscribe--unsubscribe) method with the [`drawing`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap#drawing) parameter.

```
widget.subscribe('drawing', (event) => {
    console.log(event.value);
});

```
You can also handle action events, such as moving a drawing or changing its properties.
To do this, subscribe to [`drawing_event`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap#drawing_event).
```
widget.subscribe('drawing_event', (id, type) => {
    console.log(id, type);
});

```
## Drawing Groups API
You can combine drawings into groups and manage them as single objects using the [group ID](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid).
To do this, call the [`shapesGroupController`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#shapesgroupcontroller) method that returns an instance of the [`IShapesGroupControllerApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IShapesGroupControllerApi) interface.
This interface provides methods for controlling the drawing groups.
For example, the code sample below creates a new group from the selected drawings.
```
widget.activeChart().shapesGroupController().createGroupFromSelection();

```
When working with groups, consider the following rules:

Each drawing tool may or may not be part of a specific group.
Drawings cannot be part of several groups at the same time.
- Only drawings of the same pane can be grouped.
- A group cannot be empty. Empty groups are automatically removed.
All drawings in the group have sequential z-indexes.
Thus, no other object can be placed between drawings in a group.
- Groups are bound with symbols.