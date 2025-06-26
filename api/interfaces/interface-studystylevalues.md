---
title: "Interface: StudyStyleValues | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleValues"
extracted_at: "2025-06-22T09:47:47.994Z"
---

- [](/charting-library-docs/)- Interfaces- StudyStyleValuesOn this page# Interface: StudyStyleValues[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyStyleValues

Study style values.

## Properties[​](#properties)
### bands[​](#bands)
• bands: [`StudyBandPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandPreferences)[]

Band styles.

### filledAreas[​](#filledareas)
• filledAreas: [`StudyFilledAreaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo)[]

Filled area descriptions.

### filledAreasStyle[​](#filledareasstyle)
• filledAreasStyle: `Record`<`string`, [`StudyFilledAreaStyle`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyfilledareastyle)>

Filled area styles.

### graphics[​](#graphics)
• graphics: `Object`

Graphics styles.

#### Type declaration[​](#type-declaration)
NameTypeDescription`hhists?``Record`<`string`, [`HHistPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.HHistPreferences)>Histogram style preferences`horizlines?``Record`<`string`, [`HorizLinePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.HorizLinePreferences)>Horizontal line style preferences`polygons?``Record`<`string`, [`PolygonPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PolygonPreferences)>Polygon style preferences`vertlines?``Record`<`string`, [`VertLinePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VertLinePreferences)>Vertical line style preferences

### ohlcPlots[​](#ohlcplots)
• ohlcPlots: `Record`<`string`, [`StudyOhlcPlotPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyohlcplotpreferences)>

OHLC plot styles.

### palettes[​](#palettes)
• palettes: `Record`<`string`, [`StudyPalettePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPalettePreferences)>

Palette styles.

### styles[​](#styles)
• styles: `Record`<`string`, [`StudyPlotPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotpreferences)>

Plot styles.

- [Properties](#properties)[bands](#bands)- [filledAreas](#filledareas)- [filledAreasStyle](#filledareasstyle)- [graphics](#graphics)- [ohlcPlots](#ohlcplots)- [palettes](#palettes)- [styles](#styles)