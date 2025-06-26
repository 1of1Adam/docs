---
title: "Interface: RawStudyMetaInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfo"
extracted_at: "2025-06-22T09:44:13.466Z"
---

- [](/charting-library-docs/)- Interfaces- RawStudyMetaInfoOn this page# Interface: RawStudyMetaInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).RawStudyMetaInfo

## Hierarchy[​](#hierarchy)

[`RawStudyMetaInfoBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase)

↳ `RawStudyMetaInfo`

## Properties[​](#properties)
### _metainfoVersion[​](#_metainfoversion)
• `Optional` `Readonly` _metainfoVersion: `number`

Metainfo version of the study. The current version is 53, and the default one is 0.

#### Inherited from[​](#inherited-from)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[_metainfoVersion](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#_metainfoversion)

### bands[​](#bands)
• `Optional` `Readonly` bands: readonly `Readonly`<[`StudyBandInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo)>[]

Bands

#### Inherited from[​](#inherited-from-1)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[bands](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#bands)

### behind_chart[​](#behind_chart)
• `Optional` `Readonly` behind_chart: `boolean`

Define should be study on series level or not

#### Inherited from[​](#inherited-from-2)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[behind_chart](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#behind_chart)

### defaults[​](#defaults)
• `Readonly` defaults: `Readonly`<`Partial`<[`StudyDefaults`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyDefaults)>>

an object containing settings that are applied when user clicks 'Apply Defaults'. See dedicated article: [Custom Studies Defaults](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/Custom-Studies-Defaults)

#### Inherited from[​](#inherited-from-3)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[defaults](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#defaults)

### description[​](#description)
• `Readonly` description: `string`

Description of the study. It will be displayed in the Indicators window and will be used as a name argument when calling the createStudy method

#### Inherited from[​](#inherited-from-4)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[description](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#description)

### filledAreas[​](#filledareas)
• `Optional` `Readonly` filledAreas: readonly `Readonly`<[`StudyFilledAreaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo)>[]

Filled area is a special object, which allows coloring an area between two plots or hlines. Please note, that it is impossible to fill the area between a band and a hline.

#### Inherited from[​](#inherited-from-5)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[filledAreas](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#filledareas)

### financialPeriod[​](#financialperiod)
• `Optional` `Readonly` financialPeriod: [`FinancialPeriod`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#financialperiod)

Financial Period

#### Inherited from[​](#inherited-from-6)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[financialPeriod](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#financialperiod)

### format[​](#format)
• `Readonly` format: [`StudyPlotValueFormat`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotvalueformat)

A type of data that an indicator displays, such as `volume` or `price`. Values on the [Price Scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale) depend on this data type.
Additionally, you can adjust a precision of indicator values. To do this, specify the `precision` property in [StudyPlotValuePrecisionFormat](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotValuePrecisionFormat).
For more information about `format`, refer to the [Metainfo](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/) article.

#### Inherited from[​](#inherited-from-7)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[format](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#format)

### groupingKey[​](#groupingkey)
• `Optional` `Readonly` groupingKey: `string`

Key for grouping studies

#### Inherited from[​](#inherited-from-8)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[groupingKey](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#groupingkey)

### id[​](#id)
• `Readonly` id: [`RawStudyMetaInfoId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#rawstudymetainfoid)

Identifier for Study

### inputs[​](#inputs)
• `Optional` `Readonly` inputs: [`StudyInputInfoList`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyinputinfolist)

An array of objects that represent input parameters. For more information, refer to the [Inputs](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/Custom-Studies-Inputs) article.

#### Inherited from[​](#inherited-from-9)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[inputs](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#inputs)

### isCustomIndicator[​](#iscustomindicator)
• `Optional` `Readonly` isCustomIndicator: `boolean`

should be `true` in Custom Study

#### Inherited from[​](#inherited-from-10)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[isCustomIndicator](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#iscustomindicator)

### is_hidden_study[​](#is_hidden_study)
• `Optional` `Readonly` is_hidden_study: `boolean`

Whether the study should appear in Indicators list.

#### Inherited from[​](#inherited-from-11)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[is_hidden_study](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#is_hidden_study)

### is_price_study[​](#is_price_study)
• `Optional` `Readonly` is_price_study: `boolean`

Whether the study should appear on the main series pane

#### Inherited from[​](#inherited-from-12)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[is_price_study](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#is_price_study)

### linkedToSeries[​](#linkedtoseries)
• `Optional` `Readonly` linkedToSeries: `boolean`

Whether the study price scale should be the same as the main series one.

#### Inherited from[​](#inherited-from-13)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[linkedToSeries](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#linkedtoseries)

### name[​](#name)
• `Optional` `Readonly` name: `string`

Name for the study

#### Inherited from[​](#inherited-from-14)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[name](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#name)

### ohlcPlots[​](#ohlcplots)
• `Optional` `Readonly` ohlcPlots: [`MappedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MappedObject)<`Readonly`<[`StudyOhlcStylesInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOhlcStylesInfo)>>

array with study plots info. See dedicated article: [Custom Studies OHLC Plots](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Custom-Studies-OHLC-Plots)

#### Inherited from[​](#inherited-from-15)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[ohlcPlots](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#ohlcplots)

### palettes[​](#palettes)
• `Optional` `Readonly` palettes: [`MappedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MappedObject)<`Readonly`<[`StudyPalettesInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPalettesInfo)>>

definitions of palettes that are used in plots and defaults. Palettes allows you use different styles (not only colors) for each line point.

This object contains palette names as keys, and palette info as values: `[palette.name]: { colors, valToIndex, addDefaultColor }`, where

- `colors`* - an object `{ [color_id]: { name: 'name' }}`, where name is a string that will appear on Style tab of study properties dialog.
- `valToIndex` - an object, the mapping between the values that are returned by the script and palette colors.
- `addDefaultColor` - boolean, if true the defaults are used for colorer type plot, when its value is null or undefined.

#### Inherited from[​](#inherited-from-16)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[palettes](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#palettes)

### plots[​](#plots)
• `Optional` `Readonly` plots: readonly `Readonly`<[`StudyPlotInformation`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyplotinformation)>[]

array with study plots info. See dedicated article: [Custom Studies Plots](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Custom-Studies-Plots)

#### Inherited from[​](#inherited-from-17)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[plots](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#plots)

### precision[​](#precision)
• `Optional` `Readonly` precision: `string` | `number`

Use [format](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#format) instead.

`Deprecated`

#### Inherited from[​](#inherited-from-18)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[precision](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#precision)

### priceScale[​](#pricescale)
• `Optional` `Readonly` priceScale: [`StudyTargetPriceScale`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyTargetPriceScale)

Price scale to use for the study

#### Inherited from[​](#inherited-from-19)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[priceScale](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#pricescale)

### shortDescription[​](#shortdescription)
• `Readonly` shortDescription: `string`

Short description of the study. Will be displayed on the chart

#### Inherited from[​](#inherited-from-20)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[shortDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#shortdescription)

### styles[​](#styles)
• `Optional` `Readonly` styles: [`MappedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MappedObject)<`Readonly`<[`StudyStylesInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStylesInfo)>>

an object with plot id as keys and style info as values.

#### Inherited from[​](#inherited-from-21)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[styles](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#styles)

### symbolSource[​](#symbolsource)
• `Optional` `Readonly` symbolSource: [`SymbolInputSymbolSource`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolInputSymbolSource)

Symbol source

#### Inherited from[​](#inherited-from-22)
[RawStudyMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase).[symbolSource](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfoBase#symbolsource)

- [Hierarchy](#hierarchy)- [Properties](#properties)[_metainfoVersion](#_metainfoversion)- [bands](#bands)- [behind_chart](#behind_chart)- [defaults](#defaults)- [description](#description)- [filledAreas](#filledareas)- [financialPeriod](#financialperiod)- [format](#format)- [groupingKey](#groupingkey)- [id](#id)- [inputs](#inputs)- [isCustomIndicator](#iscustomindicator)- [is_hidden_study](#is_hidden_study)- [is_price_study](#is_price_study)- [linkedToSeries](#linkedtoseries)- [name](#name)- [ohlcPlots](#ohlcplots)- [palettes](#palettes)- [plots](#plots)- [precision](#precision)- [priceScale](#pricescale)- [shortDescription](#shortdescription)- [styles](#styles)- [symbolSource](#symbolsource)