---
title: "Drawing overrides | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/customization/overrides/Drawings-Overrides"
extracted_at: "2025-06-22T09:28:45.704Z"
---

# Drawing overridesThe [Overrides API](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/) includes properties that can be used to customize [drawing](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/) parameters such as colors, width, size, and more.
This article describes ways to customize drawings and contains a [list of overrides](#list-of-overrides) for each drawing.
## Customize drawings
This section describes ways to customize drawings.

### Specify default properties
You should use the [`overrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#overrides) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) to specify the drawing's default properties.
For example, the following code sample specifies that all *Horizontal Lines* should be green and dashed.
```
var widget = window.tvWidget = new TradingView.widget({
    // ...
    overrides: {
        "linetoolhorzline.linecolor": "rgba(48, 164, 22, 0.8)",
        "linetoolhorzline.linestyle": 2,
    }
});

```
### Change default properties on the fly
To change the drawing's default properties after the chart is initialized, use the [`applyOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#applyoverrides) method.
All drawings created after the `applyOverrides` call have new properties. For example, the following code sample specifies that all newly created *Horizontal Lines* should be purple.
```
widget.applyOverrides({ "linetoolhorzline.linecolor": "#7f11e0" });

```
### Change the existing drawing
If you want to change a drawing that is already on the chart, use the [`setProperties`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi#setproperties) method in [`ILineDataSourceApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi). For example, the code sample below specifies new properties for the existing *Icon*.

```
const iconId = widget.activeChart().getAllShapes().find(x => x.name === "icon").id;
const icon = widget.activeChart().getShapeById(iconId);
icon.setProperties({ size: 60, color: "#7f11e0" });

```
### Customize a single drawing
If you need to change a style of only one drawing, create the drawing using the [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#create-drawings) and pass overrides properties as a parameter. These properties are applied above the [default ones](#specify-default-properties) that are specified in `overrides`.

For example, the code sample below specifies that the default *Horizontal Line* color is green and creates one red  *Horizontal Line*.

```
var widget = window.tvWidget = new TradingView.widget({
    // ...
    overrides: {
        "linetoolhorzline.linecolor": "rgba(48, 164, 22, 0.8)",
    }
});

widget.onChartReady(() => {
    widget.chart().createShape(
        { price: 180 },
        {
            shape: "horizontal_line",
            overrides: { linecolor: "#FF0000" },
        }
    )
});

```
### Customize icons, stickers, and emojis
Note that you cannot customize icons, stickers, or emojis using [`overrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#overrides) in the Widget Constructor or the [`applyOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#applyoverrides) method.
To customize such drawings, create a new drawing using the [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#create-drawings) and specify the drawing properties in the `overrides` parameter. Consider the examples below.
#### Icons
```
widget.chart().createShape(
    { time: 1514796562, price: 180 },
    {
        shape: "icon",
        overrides: {
            color: "#5eeb34",
            size: 50,
        },
        icon: 0xf004, // Heart
    }
);

```
Refer to [Drawings list](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/Drawings-List#icons) for a list of icons.

#### Stickers
```
widget.chart().createShape(
    { time: 1514796562, price: 160 },
    {
        shape: "sticker",
        overrides: {
            sticker: "dislike",
            size: 90,
        },
    }
);

```
Refer to [Drawings list](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/Drawings-List#stickers) for a list of stickers.

#### Emojis
```
widget.activeChart().createMultipointShape(
    [{ time: 1712158200, price: 170 }],
    {
        shape: "emoji",
        overrides: {
            size: 30,
        },
        emoji: "u/1F602" // Grinning face
    }
);

```
Note that the emoji code requires `u/` before it.

Refer to [Drawings list](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/Drawings-List#emojis) for a list of emojis.

## List of overrides
Refer to [DrawingOverrides](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#drawingoverrides) for a list of overrides.