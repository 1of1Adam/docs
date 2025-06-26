---
title: "Interface: IPriceScaleApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi"
extracted_at: "2025-06-22T09:39:27.965Z"
---

- [](/charting-library-docs/)- Interfaces- IPriceScaleApiOn this page# Interface: IPriceScaleApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IPriceScaleApi

The Price Scale API allows interacting with the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale).
You can retrieve this interface by evoking the following methods of the [IPaneApi](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPaneApi):

- `getLeftPriceScales`
- `getRightPriceScales`
- `getMainSourcePriceScale`

## Methods[​](#methods)
### currency[​](#currency)
▸ currency(): [`CurrencyInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CurrencyInfo)

Returns the current currency set on the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). Returns `null` if no currency is specified.

#### Returns[​](#returns)
[`CurrencyInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CurrencyInfo)

### getMode[​](#getmode)
▸ getMode(): [`PriceScaleMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.PriceScaleMode)

Returns current mode of the price scale

#### Returns[​](#returns-1)
[`PriceScaleMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.PriceScaleMode)

### getStudies[​](#getstudies)
▸ getStudies(): [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]

Returns an array of IDs of all studies attached to the price scale

#### Returns[​](#returns-2)
[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]

### getVisiblePriceRange[​](#getvisiblepricerange)
▸ getVisiblePriceRange(): [`VisiblePriceRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisiblePriceRange)

Returns current visible price range of the price scale.
The result is an object with `from` and `to`,
which are the boundaries of the price scale visible range.
#### Returns[​](#returns-3)
[`VisiblePriceRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisiblePriceRange)

### hasMainSeries[​](#hasmainseries)
▸ hasMainSeries(): `boolean`

Returns `true` if the price scale contains the main series

#### Returns[​](#returns-4)
`boolean`

### isAutoScale[​](#isautoscale)
▸ isAutoScale(): `boolean`

Returns `true` when the price scale has auto scaling enabled

#### Returns[​](#returns-5)
`boolean`

### isInverted[​](#isinverted)
▸ isInverted(): `boolean`

Returns whether the price scale is inverted or not

#### Returns[​](#returns-6)
`boolean`

### isLocked[​](#islocked)
▸ isLocked(): `boolean`

Returns `true` when the price scale is locked

#### Returns[​](#returns-7)
`boolean`

### setAutoScale[​](#setautoscale)
▸ setAutoScale(`isAutoScale`): `void`

Set whether auto scaling should be enabled or not for the price scale

#### Parameters[​](#parameters)
NameTypeDescription`isAutoScale``boolean`set to `true` to enable auto scaling
#### Returns[​](#returns-8)
`void`

### setCurrency[​](#setcurrency)
▸ setCurrency(`currency`): `void`

Sets a currency on the price scale.

#### Parameters[​](#parameters-1)
NameTypeDescription`currency``string`currency supported by your backend (for example 'EUR', 'USD'). A null value will reset the currency to default.
#### Returns[​](#returns-9)
`void`

### setInverted[​](#setinverted)
▸ setInverted(`isInverted`): `void`

Changes current inverted state of the price scale

#### Parameters[​](#parameters-2)
NameTypeDescription`isInverted``boolean`set to `true` if the price scale should become inverted
#### Returns[​](#returns-10)
`void`

### setLocked[​](#setlocked)
▸ setLocked(`isLocked`): `void`

Set whether the price scale should be locked or not

#### Parameters[​](#parameters-3)
NameTypeDescription`isLocked``boolean`set to `true` to lock the price scale
#### Returns[​](#returns-11)
`void`

### setMode[​](#setmode)
▸ setMode(`newMode`): `void`

Changes current mode of the price scale

#### Parameters[​](#parameters-4)
NameTypeDescription`newMode`[`PriceScaleMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.PriceScaleMode)new mode to set for the price scale
#### Returns[​](#returns-12)
`void`

### setUnit[​](#setunit)
▸ setUnit(`unit`): `void`

Sets a unit on the price scale.

#### Parameters[​](#parameters-5)
NameTypeDescription`unit``string`unit supported by your backend (for example 'weight', 'energy'). A null value will reset the unit to default.
#### Returns[​](#returns-13)
`void`

### setVisiblePriceRange[​](#setvisiblepricerange)
▸ setVisiblePriceRange(`range`): `void`

Sets current visible price range of the price scale,

#### Parameters[​](#parameters-6)
NameTypeDescription`range`[`VisiblePriceRange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.VisiblePriceRange)an object with `from` and `to`, which are the boundaries of the price scale visible range.
#### Returns[​](#returns-14)
`void`

### unit[​](#unit)
▸ unit(): [`UnitInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UnitInfo)

Returns the current unit set on the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). Returns `null` if no unit is specified.

#### Returns[​](#returns-15)
[`UnitInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UnitInfo)

- [Methods](#methods)[currency](#currency)- [getMode](#getmode)- [getStudies](#getstudies)- [getVisiblePriceRange](#getvisiblepricerange)- [hasMainSeries](#hasmainseries)- [isAutoScale](#isautoscale)- [isInverted](#isinverted)- [isLocked](#islocked)- [setAutoScale](#setautoscale)- [setCurrency](#setcurrency)- [setInverted](#setinverted)- [setLocked](#setlocked)- [setMode](#setmode)- [setUnit](#setunit)- [setVisiblePriceRange](#setvisiblepricerange)- [unit](#unit)