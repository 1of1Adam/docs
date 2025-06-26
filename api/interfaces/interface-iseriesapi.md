---
title: "Interface: ISeriesApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeriesApi"
extracted_at: "2025-06-22T09:39:37.137Z"
---

- [](/charting-library-docs/)- Interfaces- ISeriesApiOn this page# Interface: ISeriesApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ISeriesApi

Series API

You can retrieve this interface by using the [IChartWidgetApi.getSeries](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getseries) method

## Methods[​](#methods)
### bringToFront[​](#bringtofront)
▸ bringToFront(): `void`

Places main series on top of all other chart objects

#### Returns[​](#returns)
`void`

### changePriceScale[​](#changepricescale)
▸ changePriceScale(`newPriceScale`): `void`

Changes the price scale of the main series

#### Parameters[​](#parameters)
NameType`newPriceScale`[`SeriesPriceScale`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#seriespricescale)
#### Returns[​](#returns-1)
`void`

### chartStyleProperties[​](#chartstyleproperties)
▸ chartStyleProperties<`T`>(`chartStyle`): [`SeriesPreferencesMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SeriesPreferencesMap)[`T`]

Returns properties for a specific chart style

#### Type parameters[​](#type-parameters)
NameType`T`extends [`ChartStyle`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle)
#### Parameters[​](#parameters-1)
NameType`chartStyle``T`
#### Returns[​](#returns-2)
[`SeriesPreferencesMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SeriesPreferencesMap)[`T`]

### detachNoScale[​](#detachnoscale)
▸ detachNoScale(): `void`

Makes the main series to be an overlay source

#### Returns[​](#returns-3)
`void`

### detachToLeft[​](#detachtoleft)
▸ detachToLeft(): `void`

Pins the main series to a new price axis at left

#### Returns[​](#returns-4)
`void`

### detachToRight[​](#detachtoright)
▸ detachToRight(): `void`

Pins the main series to a new price axis at right

#### Returns[​](#returns-5)
`void`

### entityId[​](#entityid)
▸ entityId(): [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)

Value that is returned when a study is created via API

#### Returns[​](#returns-6)
[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)

### isUserEditEnabled[​](#isusereditenabled)
▸ isUserEditEnabled(): `boolean`

Returns `true` if a user is able to remove/change/hide the main series

#### Returns[​](#returns-7)
`boolean`

### isVisible[​](#isvisible)
▸ isVisible(): `boolean`

Returns `true` if the main series is visible

#### Returns[​](#returns-8)
`boolean`

### mergeDown[​](#mergedown)
▸ mergeDown(): `void`

Merges the main series down (if possible)

#### Returns[​](#returns-9)
`void`

### mergeUp[​](#mergeup)
▸ mergeUp(): `void`

Merges the main series up (if possible)

#### Returns[​](#returns-10)
`void`

### sendToBack[​](#sendtoback)
▸ sendToBack(): `void`

Places main series behind all other chart objects

#### Returns[​](#returns-11)
`void`

### setChartStyleProperties[​](#setchartstyleproperties)
▸ setChartStyleProperties<`T`>(`chartStyle`, `newPrefs`): `void`

Sets properties for a specific chart style

#### Type parameters[​](#type-parameters-1)
NameType`T`extends [`ChartStyle`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle)
#### Parameters[​](#parameters-2)
NameType`chartStyle``T``newPrefs``DeepPartial`<[`SeriesPreferencesMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SeriesPreferencesMap)[`T`]>
#### Returns[​](#returns-12)
`void`

### setUserEditEnabled[​](#setusereditenabled)
▸ setUserEditEnabled(`enabled`): `void`

Enables or disables removing/changing/hiding the main series by the user

#### Parameters[​](#parameters-3)
NameType`enabled``boolean`
#### Returns[​](#returns-13)
`void`

### setVisible[​](#setvisible)
▸ setVisible(`visible`): `void`

Shows/hides the main series

#### Parameters[​](#parameters-4)
NameType`visible``boolean`
#### Returns[​](#returns-14)
`void`

### unmergeDown[​](#unmergedown)
▸ unmergeDown(): `void`

Unmerges the main series down (if possible)

#### Returns[​](#returns-15)
`void`

### unmergeUp[​](#unmergeup)
▸ unmergeUp(): `void`

Unmerges the main series up (if possible)

#### Returns[​](#returns-16)
`void`

- [Methods](#methods)[bringToFront](#bringtofront)- [changePriceScale](#changepricescale)- [chartStyleProperties](#chartstyleproperties)- [detachNoScale](#detachnoscale)- [detachToLeft](#detachtoleft)- [detachToRight](#detachtoright)- [entityId](#entityid)- [isUserEditEnabled](#isusereditenabled)- [isVisible](#isvisible)- [mergeDown](#mergedown)- [mergeUp](#mergeup)- [sendToBack](#sendtoback)- [setChartStyleProperties](#setchartstyleproperties)- [setUserEditEnabled](#setusereditenabled)- [setVisible](#setvisible)- [unmergeDown](#unmergedown)- [unmergeUp](#unmergeup)