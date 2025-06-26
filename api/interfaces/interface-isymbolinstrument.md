---
title: "Interface: ISymbolInstrument | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISymbolInstrument"
extracted_at: "2025-06-22T09:39:44.734Z"
---

- [](/charting-library-docs/)- Interfaces- ISymbolInstrumentOn this page# Interface: ISymbolInstrument[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ISymbolInstrument

PineJS execution context symbol information.

## Properties[​](#properties)
### close[​](#close)
• close: `number`

Close bar value

### currencyCode[​](#currencycode)
• `Optional` currencyCode: `string`

Currency Code

### high[​](#high)
• high: `number`

High bar value

### index[​](#index)
• index: `number`

Index

### info[​](#info)
• `Optional` info: [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo)

Symbol information

### interval[​](#interval)
• interval: `number`

Interval

### isBarClosed[​](#isbarclosed)
• isBarClosed: `boolean`

Whether the bar is closed

### isFirstBar[​](#isfirstbar)
• isFirstBar: `boolean`

Whether this is the first bar

### isLastBar[​](#islastbar)
• isLastBar: `boolean`

Whether this is the last bar

### isNewBar[​](#isnewbar)
• isNewBar: `boolean`

Whether this is a new bar

### low[​](#low)
• low: `number`

Low bar value

### minTick[​](#mintick)
• minTick: `number`

Minimum tick amount

### open[​](#open)
• open: `number`

Open bar value

### period[​](#period)
• period: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

Bar resolution

### periodBase[​](#periodbase)
• periodBase: `string`

Period Base

### resolution[​](#resolution)
• resolution: `string`

Resolution

### ticker[​](#ticker)
• ticker: `string`

Ticker

### tickerid[​](#tickerid)
• tickerid: `string`

Ticker ID

### time[​](#time)
• time: `number`

Time

### unitId[​](#unitid)
• `Optional` unitId: `string`

Unit ID

### updatetime[​](#updatetime)
• updatetime: `number`

Time of the update

### volume[​](#volume)
• volume: `number`

Bar Volume value

## Methods[​](#methods)
### bartime[​](#bartime)
▸ bartime(): `number`

Time of the bar.

#### Returns[​](#returns)
`number`

the timestamp in milliseconds

### isdwm[​](#isdwm)
▸ isdwm(): `boolean`

#### Returns[​](#returns-1)
`boolean`

true if the bar resolution is day/week/month, false if it is intraday

- [Properties](#properties)[close](#close)- [currencyCode](#currencycode)- [high](#high)- [index](#index)- [info](#info)- [interval](#interval)- [isBarClosed](#isbarclosed)- [isFirstBar](#isfirstbar)- [isLastBar](#islastbar)- [isNewBar](#isnewbar)- [low](#low)- [minTick](#mintick)- [open](#open)- [period](#period)- [periodBase](#periodbase)- [resolution](#resolution)- [ticker](#ticker)- [tickerid](#tickerid)- [time](#time)- [unitId](#unitid)- [updatetime](#updatetime)- [volume](#volume)- [Methods](#methods)[bartime](#bartime)- [isdwm](#isdwm)