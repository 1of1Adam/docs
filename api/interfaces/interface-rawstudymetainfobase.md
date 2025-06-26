---
title: "Interface: RawStudyMetaInfoBase | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase"
extracted_at: "2025-06-22T09:44:15.258Z"
---

- [](/charting-library-docs/)- Interfaces- RawStudyMetaInfoBaseOn this page# Interface: RawStudyMetaInfoBase[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).RawStudyMetaInfoBase

## Hierarchy[​](#hierarchy)

`RawStudyMetaInfoBase`

↳ [`RawStudyMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfo)

## Properties[​](#properties)
### _metainfoVersion[​](#_metainfoversion)
• `Optional` `Readonly` _metainfoVersion: `number`

Metainfo version of the study. The current version is 53, and the default one is 0.

### bands[​](#bands)
• `Optional` `Readonly` bands: readonly `Readonly`<[`StudyBandInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo)>[]

Bands

### behind_chart[​](#behind_chart)
• `Optional` `Readonly` behind_chart: `boolean`

Define should be study on series level or not

### defaults[​](#defaults)
• `Readonly` defaults: `Readonly`<`Partial`<[`StudyDefaults`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyDefaults)>>

an object containing settings that are applied when user clicks 'Apply Defaults'. See dedicated article: [Custom Studies Defaults](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/Custom-Studies-Defaults)

### description[​](#description)
• `Readonly` description: `string`

Description of the study. It will be displayed in the Indicators window and will be used as a name argument when calling the createStudy method

### filledAreas[​](#filledareas)
• `Optional` `Readonly` filledAreas: readonly `Readonly`<[`StudyFilledAreaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo)>[]

Filled area is a special object, which allows coloring an area between two plots or hlines. Please note, that it is impossible to fill the area between a band and a hline.

### financialPeriod[​](#financialperiod)
• `Optional` `Readonly` financialPeriod: [`FinancialPeriod`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#financialperiod)

Financial Period

### format[​](#format)
• `Readonly` format: [`StudyPlotValueFormat`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotvalueformat)

A type of data that an indicator displays, such as `volume` or `price`. Values on the [Price Scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale) depend on this data type.
Additionally, you can adjust a precision of indicator values. To do this, specify the `precision` property in [StudyPlotValuePrecisionFormat](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotValuePrecisionFormat).
For more information about `format`, refer to the [Metainfo](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/) article.

### groupingKey[​](#groupingkey)
• `Optional` `Readonly` groupingKey: `string`

Key for grouping studies

### inputs[​](#inputs)
• `Optional` `Readonly` inputs: [`StudyInputInfoList`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyinputinfolist)

An array of objects that represent input parameters. For more information, refer to the [Inputs](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/Custom-Studies-Inputs) article.

### isCustomIndicator[​](#iscustomindicator)
• `Optional` `Readonly` isCustomIndicator: `boolean`

should be `true` in Custom Study

### is_hidden_study[​](#is_hidden_study)
• `Optional` `Readonly` is_hidden_study: `boolean`

Whether the study should appear in Indicators list.

### is_price_study[​](#is_price_study)
• `Optional` `Readonly` is_price_study: `boolean`

Whether the study should appear on the main series pane

### linkedToSeries[​](#linkedtoseries)
• `Optional` `Readonly` linkedToSeries: `boolean`

Whether the study price scale should be the same as the main series one.

### name[​](#name)
• `Optional` `Readonly` name: `string`

Name for the study

### ohlcPlots[​](#ohlcplots)
• `Optional` `Readonly` ohlcPlots: [`MappedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MappedObject)<`Readonly`<[`StudyOhlcStylesInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOhlcStylesInfo)>>

array with study plots info. See dedicated article: [Custom Studies OHLC Plots](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Custom-Studies-OHLC-Plots)

### palettes[​](#palettes)
• `Optional` `Readonly` palettes: [`MappedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MappedObject)<`Readonly`<[`StudyPalettesInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPalettesInfo)>>

definitions of palettes that are used in plots and defaults. Palettes allows you use different styles (not only colors) for each line point.

This object contains palette names as keys, and palette info as values: `[palette.name]: { colors, valToIndex, addDefaultColor }`, where

- `colors`* - an object `{ [color_id]: { name: 'name' }}`, where name is a string that will appear on Style tab of study properties dialog.
- `valToIndex` - an object, the mapping between the values that are returned by the script and palette colors.
- `addDefaultColor` - boolean, if true the defaults are used for colorer type plot, when its value is null or undefined.

### plots[​](#plots)
• `Optional` `Readonly` plots: readonly `Readonly`<[`StudyPlotInformation`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotinformation)>[]

array with study plots info. See dedicated article: [Custom Studies Plots](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Custom-Studies-Plots)

### precision[​](#precision)
• `Optional` `Readonly` precision: `string` | `number`

Use [format](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#format) instead.

`Deprecated`

### priceScale[​](#pricescale)
• `Optional` `Readonly` priceScale: [`StudyTargetPriceScale`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyTargetPriceScale)

Price scale to use for the study

### shortDescription[​](#shortdescription)
• `Readonly` shortDescription: `string`

Short description of the study. Will be displayed on the chart

### styles[​](#styles)
• `Optional` `Readonly` styles: [`MappedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MappedObject)<`Readonly`<[`StudyStylesInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStylesInfo)>>

an object with plot id as keys and style info as values.

### symbolSource[​](#symbolsource)
• `Optional` `Readonly` symbolSource: [`SymbolInputSymbolSource`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolInputSymbolSource)

Symbol source

- [Hierarchy](#hierarchy)- [Properties](#properties)[_metainfoVersion](#_metainfoversion)- [bands](#bands)- [behind_chart](#behind_chart)- [defaults](#defaults)- [description](#description)- [filledAreas](#filledareas)- [financialPeriod](#financialperiod)- [format](#format)- [groupingKey](#groupingkey)- [inputs](#inputs)- [isCustomIndicator](#iscustomindicator)- [is_hidden_study](#is_hidden_study)- [is_price_study](#is_price_study)- [linkedToSeries](#linkedtoseries)- [name](#name)- [ohlcPlots](#ohlcplots)- [palettes](#palettes)- [plots](#plots)- [precision](#precision)- [priceScale](#pricescale)- [shortDescription](#shortdescription)- [styles](#styles)- [symbolSource](#symbolsource)