---
title: "Interface: StudyStyleInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfo"
extracted_at: "2025-06-22T09:47:44.451Z"
---

- [](/charting-library-docs/)- Interfaces- StudyStyleInfoOn this page# Interface: StudyStyleInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyStyleInfo

Study style description.

## Properties[​](#properties)
### bands[​](#bands)
• `Optional` bands: readonly `Readonly`<[`StudyBandInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo)>[]

Study band descriptions.

### defaults[​](#defaults)
• `Optional` defaults: [`StudyStyleInfoDefaults`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfoDefaults)

Default study description values.

### filledAreas[​](#filledareas)
• `Optional` filledAreas: readonly `Readonly`<[`StudyFilledAreaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo)>[]

Study filled area descriptions. Filled area is a special object, which allows coloring an area between two plots.

### palettes[​](#palettes)
• `Optional` palettes: `Record`<`string`, `Readonly`<[`StudyPalettesInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPalettesInfo)>>

Study color palettes descriptions.

### plots[​](#plots)
• `Optional` plots: readonly `Readonly`<[`StudyPlotInformation`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotinformation)>[]

Study plot descriptions.

### styles[​](#styles)
• `Optional` styles: `Record`<`string`, `Readonly`<[`StudyStylesInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStylesInfo)>>

Study plot style descriptions. An object with `plot id` as keys and style info as values

- [Properties](#properties)[bands](#bands)- [defaults](#defaults)- [filledAreas](#filledareas)- [palettes](#palettes)- [plots](#plots)- [styles](#styles)