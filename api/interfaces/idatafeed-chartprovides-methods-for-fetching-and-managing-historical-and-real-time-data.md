---
title: "Interface: IDatafeedChartApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IDatafeedChartApi"
extracted_at: "2025-06-22T09:30:06.138Z"
---

# Interface: IDatafeedChartApi[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).IDatafeedChartApi

## Methods
### getBars
▸ **getBars**(`symbolInfo`, `resolution`, `periodParams`, `onResult`, `onError`): `void`

This function is called when the chart needs a history fragment defined by dates range.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbolInfo` | [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo) | A SymbolInfo object ||
| `resolution` | [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolutionstring) | Resolution of the symbol ||
| `periodParams` | [`PeriodParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.PeriodParams) | An object used to pass specific requirements for getting bars ||
| `onResult` | [`HistoryCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#historycallback) | Callback function for historical data ||
| `onError` | [`DatafeedErrorCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#datafeederrorcallback) | Callback function whose only argument is a text error message ||

#### Returns
`void`

### getMarks
▸ **getMarks**(`symbolInfo`, `from`, `to`, `onDataCallback`, `resolution`): `void`

The library calls this function to get marks for visible bars range.
The library assumes that you will call `onDataCallback` only once per `getMarks` call.
A few marks per bar are allowed (for now, the maximum is 10). The time of each mark must match the time of a bar. For example, if the bar times are `2023-01-01`, `2023-01-08`, and `2023-01-15`, then a mark cannot have the time `2023-01-05`.

**Remark:** This function will be called only if you confirmed that your back-end is supporting marks ([DatafeedConfiguration.supports_marks](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration#supports_marks)).

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbolInfo` | [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo) | A SymbolInfo object ||
| `from` | `number` | Unix timestamp (leftmost visible bar) ||
| `to` | `number` | Unix timestamp (rightmost visible bar) ||
| `onDataCallback` | [`GetMarksCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#getmarkscallback)<[`Mark`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Mark)> | Callback function containing an array of marks ||
| `resolution` | [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolutionstring) | Resolution of the symbol ||

#### Returns
`void`

### getServerTime
▸ **getServerTime**(`callback`): `void`

This function is called if the `supports_time` configuration flag is `true` when the chart needs to know the server time.
The library expects a callback to be called once.
The time is provided without milliseconds. Example: `1445324591`.
`getServerTime` is used to display countdown on the price scale.
Note that the countdown can be displayed only for [intraday](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-minutes-intraday) resolutions.
#### Parameters

 **|Name** | **Type** ||
| `callback` | [`ServerTimeCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#servertimecallback) ||

#### Returns
`void`

### getTimescaleMarks
▸ **getTimescaleMarks**(`symbolInfo`, `from`, `to`, `onDataCallback`, `resolution`): `void`

The library calls this function to get timescale marks for visible bars range.
The library assumes that you will call `onDataCallback` only once per `getTimescaleMarks` call.
**Remark:** This function will be called only if you confirmed that your back-end is supporting marks ([DatafeedConfiguration.supports_timescale_marks](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration#supports_timescale_marks)).

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbolInfo` | [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo) | A SymbolInfo object ||
| `from` | `number` | Unix timestamp (leftmost visible bar) ||
| `to` | `number` | Unix timestamp (rightmost visible bar) ||
| `onDataCallback` | [`GetMarksCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#getmarkscallback)<[`TimescaleMark`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.TimescaleMark)> | Callback function containing an array of marks ||
| `resolution` | [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolutionstring) | Resolution of the symbol ||

#### Returns
`void`

### getVolumeProfileResolutionForPeriod
▸ **getVolumeProfileResolutionForPeriod**(`currentResolution`, `from`, `to`, `symbolInfo`): [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolutionstring)

The library calls this function to get the resolution that will be used to calculate the Volume Profile Visible Range indicator.

Usually you might want to implement this method to calculate the indicator more accurately.
The implementation really depends on how much data you can transfer to the library and the depth of data in your data feed.
**Remark:** If this function is not provided the library uses currentResolution.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `currentResolution` | [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolutionstring) | Resolution of the symbol ||
| `from` | `number` | Unix timestamp (leftmost visible bar) ||
| `to` | `number` | Unix timestamp (rightmost visible bar) ||
| `symbolInfo` | [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo) | A Symbol object ||

#### Returns
[`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolutionstring)

A resolution

### resolveSymbol
▸ **resolveSymbol**(`symbolName`, `onResolve`, `onError`, `extension?`): `void`

The library will call this function when it needs to get SymbolInfo by symbol name.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbolName` | `string` | Symbol name or `ticker` ||
| `onResolve` | [`ResolveCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolvecallback) | Callback function returning a SymbolInfo ([LibrarySymbolInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo)) ||
| `onError` | [`DatafeedErrorCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#datafeederrorcallback) | Callback function whose only argument is a text error message ||
| `extension?` | [`SymbolResolveExtension`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SymbolResolveExtension) | An optional object with additional parameters ||

#### Returns
`void`

### searchSymbols
▸ **searchSymbols**(`userInput`, `exchange`, `symbolType`, `onResult`): `void`

Provides a list of symbols that match the user's search query.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `userInput` | `string` | Text entered by user in the symbol search field ||
| `exchange` | `string` | The requested exchange. Empty value means no filter was specified ||
| `symbolType` | `string` | Type of symbol. Empty value means no filter was specified ||
| `onResult` | [`SearchSymbolsCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#searchsymbolscallback) | Callback function that returns an array of results ([SearchSymbolResultItem](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SearchSymbolResultItem)) or empty array if no symbols found ||

#### Returns
`void`

### subscribeBars
▸ **subscribeBars**(`symbolInfo`, `resolution`, `onTick`, `listenerGuid`, `onResetCacheNeededCallback`): `void`

The library calls this function when it wants to receive real-time updates for a symbol.
The library assumes that you will call the callback provided by the `onTick` parameter every time you want to update the most recent bar or to add a new one.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbolInfo` | [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo) | A SymbolInfo object ||
| `resolution` | [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolutionstring) | Resolution of the symbol ||
| `onTick` | [`SubscribeBarsCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#subscribebarscallback) | Callback function returning a Bar object ||
| `listenerGuid` | `string` |  ||
| `onResetCacheNeededCallback` | () => `void` | Function to be executed when bar data has changed ||

#### Returns
`void`

### subscribeDepth
▸ **subscribeDepth**(`symbol`, `callback`): `string`

The library calls this function when it wants to receive real-time symbol data in the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) (DOM) widget.
Note that you should set the BrokerConfigFlags.supportLevel2Data configuration flag to `true`.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | A SymbolInfo object ||
| `callback` | [`DOMCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#domcallback) | A function returning an object to update DOM data ||

#### Returns
`string`

A unique identifier that will be used to unsubscribe from the data

### unsubscribeBars
▸ **unsubscribeBars**(`listenerGuid`): `void`

The library calls this function when it doesn't want to receive updates anymore.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `listenerGuid` | `string` | id to unsubscribe from ||

#### Returns
`void`

### unsubscribeDepth
▸ **unsubscribeDepth**(`subscriberUID`): `void`

The library calls this function to stop receiving real-time updates for the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) listener.
Note that you should set the BrokerConfigFlags.supportLevel2Data configuration flag to `true`.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `subscriberUID` | `string` | A string returned by `subscribeDepth` ||

#### Returns
`void`