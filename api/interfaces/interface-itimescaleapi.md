---
title: "Interface: ITimeScaleApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimeScaleApi"
extracted_at: "2025-06-22T09:39:47.580Z"
---

- [](/charting-library-docs/)- Interfaces- ITimeScaleApiOn this page# Interface: ITimeScaleApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ITimeScaleApi

API object for interacting with the [time scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale).

You can retrieve this interface by using the [IChartWidgetApi.getTimeScale](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#gettimescale) method

## Methods[​](#methods)
### barSpacing[​](#barspacing)
▸ barSpacing(): `number`

Returns the current bar spacing

#### Returns[​](#returns)
`number`

### barSpacingChanged[​](#barspacingchanged)
▸ barSpacingChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`newBarSpacing`: `number`) => `void`>

Users will be notified every time `barSpacing` value is changed. This typically occurs when zooming in/out on the chart.
This is to detect when the chart has been zoomed in/out
#### Returns[​](#returns-1)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`newBarSpacing`: `number`) => `void`>

### coordinateToTime[​](#coordinatetotime)
▸ coordinateToTime(`x`): `number`

Returns the time associated to a given coordinate (distance in pixels from the leftmost visible bar)

#### Parameters[​](#parameters)
NameType`x``number`
#### Returns[​](#returns-2)
`number`

### defaultRightOffset[​](#defaultrightoffset)
▸ defaultRightOffset(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`number`>

Object that can be used to read/set/watch the default right offset (margin)

#### Returns[​](#returns-3)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`number`>

### defaultRightOffsetPercentage[​](#defaultrightoffsetpercentage)
▸ defaultRightOffsetPercentage(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`number`>

Object that can be used to read/set/watch the default right offset (in percent) (margin)

#### Returns[​](#returns-4)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`number`>

### rightOffset[​](#rightoffset)
▸ rightOffset(): `number`

Returns the current right offset

#### Returns[​](#returns-5)
`number`

### rightOffsetChanged[​](#rightoffsetchanged)
▸ rightOffsetChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`rightOffset`: `number`) => `void`>

Users will be notified every time `rightOffset` value is changed.
This is to detect when the chart has been scrolled left/right.
#### Returns[​](#returns-6)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`rightOffset`: `number`) => `void`>

### setBarSpacing[​](#setbarspacing)
▸ setBarSpacing(`newBarSpacing`): `void`

To set a new bar spacing

#### Parameters[​](#parameters-1)
NameType`newBarSpacing``number`
#### Returns[​](#returns-7)
`void`

### setRightOffset[​](#setrightoffset)
▸ setRightOffset(`offset`): `void`

To set a new right offset

#### Parameters[​](#parameters-2)
NameType`offset``number`
#### Returns[​](#returns-8)
`void`

### usePercentageRightOffset[​](#usepercentagerightoffset)
▸ usePercentageRightOffset(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Object that can be used to read/set/watch whether to use `defaultRightOffset` or `defaultRightOffsetPercentage`
option for the right offset (margin).

- `false`: use `defaultRightOffset`
- `true`: use `defaultRightOffsetPercentage`

Default: `false`

#### Returns[​](#returns-9)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

### width[​](#width)
▸ width(): `number`

Returns the current width of the chart in pixels

#### Returns[​](#returns-10)
`number`

- [Methods](#methods)[barSpacing](#barspacing)- [barSpacingChanged](#barspacingchanged)- [coordinateToTime](#coordinatetotime)- [defaultRightOffset](#defaultrightoffset)- [defaultRightOffsetPercentage](#defaultrightoffsetpercentage)- [rightOffset](#rightoffset)- [rightOffsetChanged](#rightoffsetchanged)- [setBarSpacing](#setbarspacing)- [setRightOffset](#setrightoffset)- [usePercentageRightOffset](#usepercentagerightoffset)- [width](#width)