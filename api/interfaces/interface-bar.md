---
title: "Interface: Bar | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Bar"
extracted_at: "2025-06-22T09:51:41.847Z"
---

- [](/charting-library-docs/)- Interfaces- BarOn this page# Interface: Bar[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).Bar

Bar data point

## Properties[​](#properties)
### close[​](#close)
• close: `number`

Closing price

### high[​](#high)
• high: `number`

High price

### low[​](#low)
• low: `number`

Low price

### open[​](#open)
• open: `number`

Opening price

### time[​](#time)
• time: `number`

Bar time.
Amount of milliseconds since Unix epoch start in UTC timezone.
`time` for daily, weekly, and monthly bars is expected to be a trading day (not session start day) at 00:00 UTC.
The library adjusts time according to `session` from [LibrarySymbolInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo).

### volume[​](#volume)
• `Optional` volume: `number`

Trading Volume

- [Properties](#properties)[close](#close)- [high](#high)- [low](#low)- [open](#open)- [time](#time)- [volume](#volume)