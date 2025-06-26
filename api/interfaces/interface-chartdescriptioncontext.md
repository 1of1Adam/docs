---
title: "Interface: ChartDescriptionContext | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartDescriptionContext"
extracted_at: "2025-06-22T09:34:05.202Z"
---

- [](/charting-library-docs/)- Interfaces- ChartDescriptionContextOn this page# Interface: ChartDescriptionContext[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ChartDescriptionContext

## Properties[​](#properties)
### chartCount[​](#chartcount)
• chartCount: `number`

Number of visible charts in the current layout

### chartIndex[​](#chartindex)
• chartIndex: `number`

Index of the current chart within a multi-chart layout

### chartType[​](#charttype)
• chartType: [`SeriesType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)

Style of chart

### chartTypeName[​](#charttypename)
• chartTypeName: `string`

Name of chart style

### description[​](#description)
• `Optional` description: `string`

Symbol's description from the Symbol Info

### exchange[​](#exchange)
• `Optional` exchange: `string`

Symbol's exchange

### interval[​](#interval)
• interval: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

Resolution (interval) of the chart

### isIntraday[​](#isintraday)
• isIntraday: `boolean`

Is the resolution (interval) intraday

### priceFormatter[​](#priceformatter)
• priceFormatter: [`ISymbolValueFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISymbolValueFormatter)

Symbol's default price formatter

### symbol[​](#symbol)
• symbol: `string`

Symbol identifier, typically the symbols ticker or name defined in the Symbol Info

### symbolInfo[​](#symbolinfo)
• symbolInfo: [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo)

The complete Symbol Info for the chart's main series

### ticker[​](#ticker)
• `Optional` ticker: `string`

Symbol's ticker identifier

### visibleData[​](#visibledata)
• `Optional` visibleData: [`ExportedData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportedData)

Visible data. Only included if [aria_detailed_chart_descriptions](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#aria_detailed_chart_descriptions) featureset is enabled

### visibleRange[​](#visiblerange)
• visibleRange: [`VisibleTimeRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisibleTimeRange)

Visible time range

- [Properties](#properties)[chartCount](#chartcount)- [chartIndex](#chartindex)- [chartType](#charttype)- [chartTypeName](#charttypename)- [description](#description)- [exchange](#exchange)- [interval](#interval)- [isIntraday](#isintraday)- [priceFormatter](#priceformatter)- [symbol](#symbol)- [symbolInfo](#symbolinfo)- [ticker](#ticker)- [visibleData](#visibledata)- [visibleRange](#visiblerange)