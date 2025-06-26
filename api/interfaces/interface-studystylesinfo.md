---
title: "Interface: StudyStylesInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStylesInfo"
extracted_at: "2025-06-22T09:47:49.754Z"
---

- [](/charting-library-docs/)- Interfaces- StudyStylesInfoOn this page# Interface: StudyStylesInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyStylesInfo

Study styles description.

## Properties[​](#properties)
### char[​](#char)
• `Optional` `Readonly` char: `string`

Char to display with the plot. Applicable only to chars plot types.

### forceOverlay[​](#forceoverlay)
• `Optional` `Readonly` forceOverlay: `boolean`

optional flag to indicate the plot should be drawn on main page

### format[​](#format)
• `Optional` `Readonly` format: `Partial`<[`StudyPlotValuePrecisionFormat`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotValuePrecisionFormat)>

Info about the Price Scale formatting

### histogramBase[​](#histogrambase)
• `Optional` `Readonly` histogramBase: `number`

Histogram base. A price value which will be considered as a start base point when rendering plot with histogram, columns or area style.

### isHidden[​](#ishidden)
• `Optional` `Readonly` isHidden: `boolean`

If `true` then the styles tab will be hidden in the study dialog.

### joinPoints[​](#joinpoints)
• `Optional` `Readonly` joinPoints: `boolean`

If `true` then plot points will be joined with line, applicable only to `Circles` and `Cross` type plots. Default is false.

### maxHeight[​](#maxheight)
• `Optional` `Readonly` maxHeight: `number`

Maximum possible plot arrow size. Applicable only to arrow plot types.

### minHeight[​](#minheight)
• `Optional` `Readonly` minHeight: `number`

Minimum possible plot arrow size. Applicable only to arrow plot types.

### showLast[​](#showlast)
• `Optional` `Readonly` showLast: `number`

If defined, defines the number of bars to plot on chart.

### size[​](#size)
• `Optional` `Readonly` size: `number` | [`PlotSymbolSize`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.PlotSymbolSize)

Size of characters on the chart. Possible values are: `auto`, `tiny`, `small`, `normal`, `large`,`huge`. Applicable to `chars` and `shapes` plot types.

### text[​](#text)
• `Optional` `Readonly` text: `string`

Text to display with the plot. Applicable to `chars` and `shapes` plot types.

### title[​](#title)
• `Readonly` title: `string`

Title used in the study dialog styles tab.

### zorder[​](#zorder)
• `Optional` `Readonly` zorder: `number`

Used to control the zorder of the plot. Control if a plot is visually behind or in front of another.

- [Properties](#properties)[char](#char)- [forceOverlay](#forceoverlay)- [format](#format)- [histogramBase](#histogrambase)- [isHidden](#ishidden)- [joinPoints](#joinpoints)- [maxHeight](#maxheight)- [minHeight](#minheight)- [showLast](#showlast)- [size](#size)- [text](#text)- [title](#title)- [zorder](#zorder)