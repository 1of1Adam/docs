---
title: "Interface: StudyPlotBasePreferences | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBasePreferences"
extracted_at: "2025-06-22T09:47:18.620Z"
---

- [](/charting-library-docs/)- Interfaces- StudyPlotBasePreferencesOn this page# Interface: StudyPlotBasePreferences[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyPlotBasePreferences

Base type for all study plot style preferences.

## Hierarchy[​](#hierarchy)

`StudyPlotBasePreferences`

↳ [`StudyArrowsPlotPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyArrowsPlotPreferences)

↳ [`StudyCharsPlotPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyCharsPlotPreferences)

↳ [`StudyLinePlotPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyLinePlotPreferences)

↳ [`StudyShapesPlotPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyShapesPlotPreferences)

## Properties[​](#properties)
### display[​](#display)
• display: [`StudyPlotDisplayMode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotdisplaymode)

Display mode. See [StudyPlotDisplayMode](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotdisplaymode).

`Example`

```
StudyPlotDisplayTarget.None // Do not display the plot.
```

### transparency[​](#transparency)
• `Optional` transparency: `number`

Transparency. A number between 1 and 100.

`Example`

```
80
```

### visible[​](#visible)
• `Optional` visible: `boolean`

Visibility

- [Hierarchy](#hierarchy)- [Properties](#properties)[display](#display)- [transparency](#transparency)- [visible](#visible)