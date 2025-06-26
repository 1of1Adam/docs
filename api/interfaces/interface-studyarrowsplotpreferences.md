---
title: "Interface: StudyArrowsPlotPreferences | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyArrowsPlotPreferences"
extracted_at: "2025-06-22T09:45:39.798Z"
---

- [](/charting-library-docs/)- Interfaces- StudyArrowsPlotPreferencesOn this page# Interface: StudyArrowsPlotPreferences[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyArrowsPlotPreferences

Study arrow plot style preferences.

## Hierarchy[​](#hierarchy)

[`StudyPlotBasePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences)

↳ `StudyArrowsPlotPreferences`

## Properties[​](#properties)
### colordown[​](#colordown)
• colordown: `string`

Down arrow color.

### colorup[​](#colorup)
• colorup: `string`

Up arrow color.

### display[​](#display)
• display: [`StudyPlotDisplayMode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotdisplaymode)

Display mode. See [StudyPlotDisplayMode](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotdisplaymode).

`Example`

```
StudyPlotDisplayTarget.None // Do not display the plot.
```
#### Inherited from[​](#inherited-from)
[StudyPlotBasePreferences](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences).[display](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences#display)

### maxHeight[​](#maxheight)
• `Optional` maxHeight: `number`

Maximum arrow height.

### minHeight[​](#minheight)
• `Optional` minHeight: `number`

Minimum arrow height.

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

- [Hierarchy](#hierarchy)- [Properties](#properties)[colordown](#colordown)- [colorup](#colorup)- [display](#display)- [maxHeight](#maxheight)- [minHeight](#minheight)- [transparency](#transparency)- [visible](#visible)