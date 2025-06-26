---
title: "Module: Datafeed | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#quotedata"
extracted_at: "2025-06-22T09:52:25.570Z"
---

- [](/charting-library-docs/)- Modules- DatafeedOn this page# Module: DatafeedDatafeed JS API for TradingView Advanced Charts

## Interfaces[​](#interfaces)

- [Bar](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Bar)
- [CurrencyItem](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.CurrencyItem)
- [DOMData](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DOMData)
- [DOMLevel](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DOMLevel)
- [DatafeedConfiguration](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration)
- [DatafeedQuoteValues](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedQuoteValues)
- [DatafeedSymbolType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedSymbolType)
- [Exchange](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Exchange)
- [HistoryMetadata](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.HistoryMetadata)
- [IDatafeedChartApi](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IDatafeedChartApi)
- [IDatafeedQuotesApi](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IDatafeedQuotesApi)
- [IExternalDatafeed](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IExternalDatafeed)
- [LibrarySubsessionInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySubsessionInfo)
- [LibrarySymbolInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo)
- [Mark](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Mark)
- [MarkCustomColor](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.MarkCustomColor)
- [PeriodParams](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.PeriodParams)
- [QuoteDataResponse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse)
- [QuoteErrorData](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteErrorData)
- [QuoteOkData](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteOkData)
- [SearchSymbolResultItem](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SearchSymbolResultItem)
- [SymbolInfoPriceSource](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SymbolInfoPriceSource)
- [SymbolResolveExtension](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SymbolResolveExtension)
- [TimescaleMark](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.TimescaleMark)
- [Unit](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Unit)

## Type Aliases[​](#type-aliases)
### CustomTimezones[​](#customtimezones)
Ƭ CustomTimezones: `"Africa/Cairo"` | `"Africa/Casablanca"` | `"Africa/Johannesburg"` | `"Africa/Lagos"` | `"Africa/Nairobi"` | `"Africa/Tunis"` | `"America/Anchorage"` | `"America/Argentina/Buenos_Aires"` | `"America/Bogota"` | `"America/Caracas"` | `"America/Chicago"` | `"America/El_Salvador"` | `"America/Juneau"` | `"America/Lima"` | `"America/Los_Angeles"` | `"America/Mexico_City"` | `"America/New_York"` | `"America/Phoenix"` | `"America/Santiago"` | `"America/Sao_Paulo"` | `"America/Toronto"` | `"America/Vancouver"` | `"Asia/Almaty"` | `"Asia/Ashkhabad"` | `"Asia/Bahrain"` | `"Asia/Bangkok"` | `"Asia/Chongqing"` | `"Asia/Colombo"` | `"Asia/Dhaka"` | `"Asia/Dubai"` | `"Asia/Ho_Chi_Minh"` | `"Asia/Hong_Kong"` | `"Asia/Jakarta"` | `"Asia/Jerusalem"` | `"Asia/Kabul"` | `"Asia/Karachi"` | `"Asia/Kathmandu"` | `"Asia/Kolkata"` | `"Asia/Kuala_Lumpur"` | `"Asia/Kuwait"` | `"Asia/Manila"` | `"Asia/Muscat"` | `"Asia/Nicosia"` | `"Asia/Qatar"` | `"Asia/Riyadh"` | `"Asia/Seoul"` | `"Asia/Shanghai"` | `"Asia/Singapore"` | `"Asia/Taipei"` | `"Asia/Tehran"` | `"Asia/Tokyo"` | `"Asia/Yangon"` | `"Atlantic/Azores"` | `"Atlantic/Reykjavik"` | `"Australia/Adelaide"` | `"Australia/Brisbane"` | `"Australia/Perth"` | `"Australia/Sydney"` | `"Europe/Amsterdam"` | `"Europe/Athens"` | `"Europe/Belgrade"` | `"Europe/Berlin"` | `"Europe/Bratislava"` | `"Europe/Brussels"` | `"Europe/Bucharest"` | `"Europe/Budapest"` | `"Europe/Copenhagen"` | `"Europe/Dublin"` | `"Europe/Helsinki"` | `"Europe/Istanbul"` | `"Europe/Lisbon"` | `"Europe/London"` | `"Europe/Luxembourg"` | `"Europe/Madrid"` | `"Europe/Malta"` | `"Europe/Moscow"` | `"Europe/Oslo"` | `"Europe/Paris"` | `"Europe/Prague"` | `"Europe/Riga"` | `"Europe/Rome"` | `"Europe/Stockholm"` | `"Europe/Tallinn"` | `"Europe/Vienna"` | `"Europe/Vilnius"` | `"Europe/Warsaw"` | `"Europe/Zurich"` | `"Pacific/Auckland"` | `"Pacific/Chatham"` | `"Pacific/Fakaofo"` | `"Pacific/Honolulu"` | `"Pacific/Norfolk"` | `"US/Mountain"`

### DOMCallback[​](#domcallback)
Ƭ DOMCallback: (`data`: [`DOMData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DOMData)) => `void`

#### Type declaration[​](#type-declaration)
▸ (`data`): `void`

Parameters[​](#parameters)
NameType`data`[`DOMData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DOMData)
Returns[​](#returns)
`void`

### DatafeedErrorCallback[​](#datafeederrorcallback)
Ƭ DatafeedErrorCallback: (`reason`: `string`) => `void`

#### Type declaration[​](#type-declaration-1)
▸ (`reason`): `void`

Parameters[​](#parameters-1)
NameType`reason``string`
Returns[​](#returns-1)
`void`

### GetMarksCallback[​](#getmarkscallback)
Ƭ GetMarksCallback<`T`>: (`marks`: `T`[]) => `void`

#### Type parameters[​](#type-parameters)
Name`T`
#### Type declaration[​](#type-declaration-2)
▸ (`marks`): `void`

Parameters[​](#parameters-2)
NameType`marks``T`[]
Returns[​](#returns-2)
`void`

### HistoryCallback[​](#historycallback)
Ƭ HistoryCallback: (`bars`: [`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Bar)[], `meta?`: [`HistoryMetadata`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.HistoryMetadata)) => `void`

#### Type declaration[​](#type-declaration-3)
▸ (`bars`, `meta?`): `void`

Parameters[​](#parameters-3)
NameType`bars`[`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Bar)[]`meta?`[`HistoryMetadata`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.HistoryMetadata)
Returns[​](#returns-3)
`void`

### LibrarySessionId[​](#librarysessionid)
Ƭ LibrarySessionId: `"regular"` | `"extended"` | `"premarket"` | `"postmarket"`

### MarkConstColors[​](#markconstcolors)
Ƭ MarkConstColors: `"red"` | `"green"` | `"blue"` | `"yellow"`

### Nominal[​](#nominal)
Ƭ Nominal<`T`, `Name`>: `T` & { `[species]`: `Name`  }

This is the generic type useful for declaring a nominal type,
which does not structurally matches with the base type and
the other types declared over the same base type
Usage:

`Example`

```
type Index = Nominal<number, 'Index'>;// let i: Index = 42; // this fails to compilelet i: Index = 42 as Index; // OK
```
`Example`

```
type TagName = Nominal<string, 'TagName'>;
```
#### Type parameters[​](#type-parameters-1)
NameType`T``T``Name`extends `string`

### OnReadyCallback[​](#onreadycallback)
Ƭ OnReadyCallback: (`configuration`: [`DatafeedConfiguration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration)) => `void`

#### Type declaration[​](#type-declaration-4)
▸ (`configuration`): `void`

Parameters[​](#parameters-4)
NameType`configuration`[`DatafeedConfiguration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration)
Returns[​](#returns-4)
`void`

### QuoteData[​](#quotedata)
Ƭ QuoteData: [`QuoteOkData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteOkData) | [`QuoteErrorData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteErrorData)

### QuotesCallback[​](#quotescallback)
Ƭ QuotesCallback: (`data`: [`QuoteData`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#quotedata)[]) => `void`

Callback to provide Quote data.

#### Type declaration[​](#type-declaration-5)
▸ (`data`): `void`

Parameters[​](#parameters-5)
NameTypeDescription`data`[`QuoteData`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#quotedata)[]Quote Data
Returns[​](#returns-5)
`void`

### QuotesErrorCallback[​](#quoteserrorcallback)
Ƭ QuotesErrorCallback: (`reason`: `string`) => `void`

Error callback for quote data request.

#### Type declaration[​](#type-declaration-6)
▸ (`reason`): `void`

Parameters[​](#parameters-6)
NameTypeDescription`reason``string`message describing the reason for the error
Returns[​](#returns-6)
`void`

### ResolutionString[​](#resolutionstring)
Ƭ ResolutionString: [`Nominal`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#nominal)<`string`, `"ResolutionString"`>

Resolution or time interval is a time period of one bar. Advanced Charts supports tick, intraday (seconds, minutes, hours), and DWM (daily, weekly, monthly) resolutions. The table below describes how to specify different types of resolutions:

ResolutionFormatExampleTicks`xT``1T` — one tick, `5T` — five ticks, `100T` — one hundred ticksSeconds`xS``1S` — one secondMinutes`x``1` — one minuteHours`x` minutes`60` — one hourDays`xD``1D` — one dayWeeks`xW``1W` — one weekMonths`xM``1M` — one monthYears`xM` months`12M` — one year
Refer to [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution) for more information.

### ResolveCallback[​](#resolvecallback)
Ƭ ResolveCallback: (`symbolInfo`: [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo)) => `void`

#### Type declaration[​](#type-declaration-7)
▸ (`symbolInfo`): `void`

Parameters[​](#parameters-7)
NameType`symbolInfo`[`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo)
Returns[​](#returns-7)
`void`

### SearchSymbolsCallback[​](#searchsymbolscallback)
Ƭ SearchSymbolsCallback: (`items`: [`SearchSymbolResultItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SearchSymbolResultItem)[]) => `void`

#### Type declaration[​](#type-declaration-8)
▸ (`items`): `void`

Parameters[​](#parameters-8)
NameType`items`[`SearchSymbolResultItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SearchSymbolResultItem)[]
Returns[​](#returns-8)
`void`

### SeriesFormat[​](#seriesformat)
Ƭ SeriesFormat: `"price"` | `"volume"`

### ServerTimeCallback[​](#servertimecallback)
Ƭ ServerTimeCallback: (`serverTime`: `number`) => `void`

#### Type declaration[​](#type-declaration-9)
▸ (`serverTime`): `void`

Parameters[​](#parameters-9)
NameType`serverTime``number`
Returns[​](#returns-9)
`void`

### SubscribeBarsCallback[​](#subscribebarscallback)
Ƭ SubscribeBarsCallback: (`bar`: [`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Bar)) => `void`

#### Type declaration[​](#type-declaration-10)
▸ (`bar`): `void`

Parameters[​](#parameters-10)
NameType`bar`[`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Bar)
Returns[​](#returns-10)
`void`

### TimeScaleMarkShape[​](#timescalemarkshape)
Ƭ TimeScaleMarkShape: `"circle"` | `"earningUp"` | `"earningDown"` | `"earning"`

### Timezone[​](#timezone)
Ƭ Timezone: `"Etc/UTC"` | [`CustomTimezones`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#customtimezones)

### VisiblePlotsSet[​](#visibleplotsset)
Ƭ VisiblePlotsSet: `"ohlcv"` | `"ohlc"` | `"c"`

- [Interfaces](#interfaces)- [Type Aliases](#type-aliases)[CustomTimezones](#customtimezones)- [DOMCallback](#domcallback)- [DatafeedErrorCallback](#datafeederrorcallback)- [GetMarksCallback](#getmarkscallback)- [HistoryCallback](#historycallback)- [LibrarySessionId](#librarysessionid)- [MarkConstColors](#markconstcolors)- [Nominal](#nominal)- [OnReadyCallback](#onreadycallback)- [QuoteData](#quotedata)- [QuotesCallback](#quotescallback)- [QuotesErrorCallback](#quoteserrorcallback)- [ResolutionString](#resolutionstring)- [ResolveCallback](#resolvecallback)- [SearchSymbolsCallback](#searchsymbolscallback)- [SeriesFormat](#seriesformat)- [ServerTimeCallback](#servertimecallback)- [SubscribeBarsCallback](#subscribebarscallback)- [TimeScaleMarkShape](#timescalemarkshape)- [Timezone](#timezone)- [VisiblePlotsSet](#visibleplotsset)