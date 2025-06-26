---
title: "Interface: StudyLinePlotPreferences | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyLinePlotPreferences"
extracted_at: "2025-06-22T09:46:44.132Z"
---

- [](/charting-library-docs/)- Interfaces- StudyLinePlotPreferencesOn this page# Interface: StudyLinePlotPreferences[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyLinePlotPreferences

Study line plot style preferences.

## Hierarchy[​](#hierarchy)

[`StudyPlotBasePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences)

↳ `StudyLinePlotPreferences`

## Properties[​](#properties)
### color[​](#color)
• color: `string`

Line color.

### display[​](#display)
• display: [`StudyPlotDisplayMode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotdisplaymode)

Display mode. See [StudyPlotDisplayMode](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotdisplaymode).

`Example`

```
StudyPlotDisplayTarget.None // Do not display the plot.
```
#### Inherited from[​](#inherited-from)
[StudyPlotBasePreferences](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences).[display](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences#display)

### linestyle[​](#linestyle)
• linestyle: [`LineStyle`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.LineStyle)

Line style.

### linewidth[​](#linewidth)
• linewidth: `number`

Line width.

### plottype[​](#plottype)
• plottype: [`LineStudyPlotStyle`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.LineStudyPlotStyle)

Plot style.

### showLast[​](#showlast)
• `Optional` `Readonly` showLast: `number`

If defined, defines the number of bars to plot on chart.

### trackPrice[​](#trackprice)
• trackPrice: `boolean`

Price line visibility flag.

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

- [Hierarchy](#hierarchy)- [Properties](#properties)[color](#color)- [display](#display)- [linestyle](#linestyle)- [linewidth](#linewidth)- [plottype](#plottype)- [showLast](#showlast)- [trackPrice](#trackprice)- [transparency](#transparency)- [visible](#visible)