---
title: "Interface: StudyStyleInfoDefaults | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfoDefaults"
extracted_at: "2025-06-22T09:47:46.243Z"
---

- [](/charting-library-docs/)- Interfaces- StudyStyleInfoDefaultsOn this page# Interface: StudyStyleInfoDefaults[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyStyleInfoDefaults

Default study style preferences.

## Properties[​](#properties)
### bands[​](#bands)
• `Optional` bands: readonly [`StudyBandStyle`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle)[]

Default study bands style preferences.

### filledAreasStyle[​](#filledareasstyle)
• `Optional` filledAreasStyle: `Record`<`string`, [`StudyFilledAreaStyle`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyfilledareastyle)>

Default study filled areas style preferences.

### graphics[​](#graphics)
• `Optional` graphics: `Object`

Default study graphics style preferences.

#### Type declaration[​](#type-declaration)
NameTypeDescription`hhists?``Record`<`string`, [`HHistPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.HHistPreferences)>Histogram style preferences`horizlines?``Record`<`string`, [`HorizLinePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.HorizLinePreferences)>Horizontal line style preferences`polygons?``Record`<`string`, [`PolygonPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PolygonPreferences)>Polygon style preferences`vertlines?``Record`<`string`, [`VertLinePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VertLinePreferences)>Vertical line style preferences

### ohlcPlots[​](#ohlcplots)
• `Optional` ohlcPlots: `Record`<`string`, [`StudyOhlcPlotPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyohlcplotpreferences)>

Default study OHLC plot style preferences.

### palettes[​](#palettes)
• `Optional` palettes: `Record`<`string`, [`StudyPaletteStyle`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPaletteStyle)>

Default study paletes style preferences.

### styles[​](#styles)
• `Optional` styles: `Record`<`string`, [`StudyPlotPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotpreferences)>

Default study styles.

- [Properties](#properties)[bands](#bands)- [filledAreasStyle](#filledareasstyle)- [graphics](#graphics)- [ohlcPlots](#ohlcplots)- [palettes](#palettes)- [styles](#styles)