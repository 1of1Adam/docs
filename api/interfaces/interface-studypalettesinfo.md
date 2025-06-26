---
title: "Interface: StudyPalettesInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPalettesInfo"
extracted_at: "2025-06-22T09:47:14.868Z"
---

- [](/charting-library-docs/)- Interfaces- StudyPalettesInfoOn this page# Interface: StudyPalettesInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyPalettesInfo

A description of a study color palettes.

## Properties[​](#properties)
### addDefaultColor[​](#adddefaultcolor)
• `Optional` `Readonly` addDefaultColor: `boolean`

Use default color for [StudyPlotType.Colorer](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyPlotType#colorer) plots when the value is `NaN`.

### colors[​](#colors)
• `Readonly` colors: [`MappedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MappedObject)<[`StudyPaletteInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPaletteInfo)> | [`StudyPaletteInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPaletteInfo)[]

Palette colors.

### valToIndex[​](#valtoindex)
• `Optional` `Readonly` valToIndex: [`MappedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MappedObject)<`number`>

Mapping from values returned by the study to palette color index.

- [Properties](#properties)[addDefaultColor](#adddefaultcolor)- [colors](#colors)- [valToIndex](#valtoindex)