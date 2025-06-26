---
title: "Interface: IPaneApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPaneApi"
extracted_at: "2025-06-22T09:39:22.690Z"
---

- [](/charting-library-docs/)- Interfaces- IPaneApiOn this page# Interface: IPaneApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IPaneApi

You can retrieve this interface by using the [IChartWidgetApi.getPanes](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getpanes) method

## Methods[​](#methods)
### collapse[​](#collapse)
▸ collapse(): `void`

Collapse the current pane

#### Returns[​](#returns)
`void`

### getHeight[​](#getheight)
▸ getHeight(): `number`

Returns the pane's height

#### Returns[​](#returns-1)
`number`

### getLeftPriceScales[​](#getleftpricescales)
▸ getLeftPriceScales(): readonly [`IPriceScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi)[]

Returns an array of the PriceScaleApi instances that allows interaction with right price scales.
The array may be empty if there is not any price scale on the left side of the pane
#### Returns[​](#returns-2)
readonly [`IPriceScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi)[]

### getMainSourcePriceScale[​](#getmainsourcepricescale)
▸ getMainSourcePriceScale(): [`IPriceScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi)

Returns an instance of the PriceScaleApi that allows you to interact with the price scale of the main source
or `null` if the main source is not attached to any price scale (it is in 'No Scale' mode)
#### Returns[​](#returns-3)
[`IPriceScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi)

### getPriceScaleById[​](#getpricescalebyid)
▸ getPriceScaleById(`priceScaleId`): [`IPriceScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi)

Returns an instance of the PriceScaleApi that allows you to interact with the price scale of the main source
or `null` if the main source is not attached to any price scale (it is in 'No Scale' mode)
#### Parameters[​](#parameters)
NameType`priceScaleId``string`
#### Returns[​](#returns-4)
[`IPriceScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi)

### getRightPriceScales[​](#getrightpricescales)
▸ getRightPriceScales(): readonly [`IPriceScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi)[]

Returns an array of the PriceScaleApi instances that allows interaction with right price scales.
The array may be empty if there is not any price scale on the right side of the pane
#### Returns[​](#returns-5)
readonly [`IPriceScaleApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi)[]

### hasMainSeries[​](#hasmainseries)
▸ hasMainSeries(): `boolean`

Returns `true` if the price scale contains the main series

#### Returns[​](#returns-6)
`boolean`

### isCollapsed[​](#iscollapsed)
▸ isCollapsed(): `boolean`

Returns the pane's collapsed state

#### Returns[​](#returns-7)
`boolean`

### isMaximized[​](#ismaximized)
▸ isMaximized(): `boolean`

Returns the maximized state of the pane

#### Returns[​](#returns-8)
`boolean`

### moveTo[​](#moveto)
▸ moveTo(`paneIndex`): `void`

Moves the pane to a new position, `paneIndex` should be a number between 0 and all panes count - 1

#### Parameters[​](#parameters-1)
NameType`paneIndex``number`
#### Returns[​](#returns-9)
`void`

### paneIndex[​](#paneindex)
▸ paneIndex(): `number`

Returns the pane's index, it's a number between 0 and all panes count - 1

#### Returns[​](#returns-10)
`number`

### restore[​](#restore)
▸ restore(): `void`

Restore the size of a previously collapsed pane

#### Returns[​](#returns-11)
`void`

### setHeight[​](#setheight)
▸ setHeight(`height`): `void`

Sets the pane's height

#### Parameters[​](#parameters-2)
NameType`height``number`
#### Returns[​](#returns-12)
`void`

### setMaximized[​](#setmaximized)
▸ setMaximized(`value`): `void`

Change the maximized state of the pane

#### Parameters[​](#parameters-3)
NameType`value``boolean`
#### Returns[​](#returns-13)
`void`

- [Methods](#methods)[collapse](#collapse)- [getHeight](#getheight)- [getLeftPriceScales](#getleftpricescales)- [getMainSourcePriceScale](#getmainsourcepricescale)- [getPriceScaleById](#getpricescalebyid)- [getRightPriceScales](#getrightpricescales)- [hasMainSeries](#hasmainseries)- [isCollapsed](#iscollapsed)- [isMaximized](#ismaximized)- [moveTo](#moveto)- [paneIndex](#paneindex)- [restore](#restore)- [setHeight](#setheight)- [setMaximized](#setmaximized)