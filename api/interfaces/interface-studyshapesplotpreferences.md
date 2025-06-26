---
title: "Interface: StudyShapesPlotPreferences | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyShapesPlotPreferences"
extracted_at: "2025-06-22T09:47:37.833Z"
---

- [](/charting-library-docs/)- Interfaces- StudyShapesPlotPreferencesOn this page# Interface: StudyShapesPlotPreferences[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyShapesPlotPreferences

Study shape plot style preferences.

## Hierarchy[​](#hierarchy)

[`StudyPlotBasePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences)

↳ `StudyShapesPlotPreferences`

## Properties[​](#properties)
### color[​](#color)
• color: `string`

Color.

### display[​](#display)
• display: [`StudyPlotDisplayMode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotdisplaymode)

Display mode. See [StudyPlotDisplayMode](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotdisplaymode).

`Example`

```
StudyPlotDisplayTarget.None // Do not display the plot.
```
#### Inherited from[​](#inherited-from)
[StudyPlotBasePreferences](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences).[display](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences#display)

### location[​](#location)
• location: [`MarkLocation`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.MarkLocation)

Location relative to the bar.

### plottype[​](#plottype)
• plottype: [`PlotShapeId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#plotshapeid)

Plot type.

### textColor[​](#textcolor)
• textColor: `string`

Text color.

### transparency[​](#transparency)
• `Optional` transparency: `number`

Transparency. A number between 1 and 100.

`Example`

```
80
```
#### Inherited from[​](#inherited-from-1)
[StudyPlotBasePreferences](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences).[transparency](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences#transparency)

### visible[​](#visible)
• `Optional` visible: `boolean`

Visibility

#### Inherited from[​](#inherited-from-2)
[StudyPlotBasePreferences](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences).[visible](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences#visible)

- [Hierarchy](#hierarchy)- [Properties](#properties)[color](#color)- [display](#display)- [location](#location)- [plottype](#plottype)- [textColor](#textcolor)- [transparency](#transparency)- [visible](#visible)