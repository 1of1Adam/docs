---
title: "Interface: StudyCharsPlotPreferences | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyCharsPlotPreferences"
extracted_at: "2025-06-22T09:46:02.935Z"
---

- [](/charting-library-docs/)- Interfaces- StudyCharsPlotPreferencesOn this page# Interface: StudyCharsPlotPreferences[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyCharsPlotPreferences

Base type for all study plot style preferences.

## Hierarchy[​](#hierarchy)

[`StudyPlotBasePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences)

↳ `StudyCharsPlotPreferences`

## Properties[​](#properties)
### char[​](#char)
• `Optional` char: `string`

Character

### color[​](#color)
• color: `string`

Color

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

Location for the mark

### textColor[​](#textcolor)
• textColor: `string`

Text color

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

- [Hierarchy](#hierarchy)- [Properties](#properties)[char](#char)- [color](#color)- [display](#display)- [location](#location)- [textColor](#textcolor)- [transparency](#transparency)- [visible](#visible)