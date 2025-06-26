---
title: "Interface: TimezoneInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimezoneInfo"
extracted_at: "2025-06-22T09:49:09.238Z"
---

- [](/charting-library-docs/)- Interfaces- TimezoneInfoOn this page# Interface: TimezoneInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).TimezoneInfo

Supported timezone identifier are LibrarySymbolInfo.timezones and [LibrarySymbolInfo.exchange](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#exchange).
`exchange` is a special "timezone" that means the timezone of a currently active symbol.
Thus the actual timezone will be calculated every time a symbol changes.
## Properties[​](#properties)
### alias[​](#alias)
• `Optional` alias: [`TimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid) | `Etc/GMT-${number}` | `Etc/GMT-${number}:${number}` | `Etc/GMT+${number}` | `Etc/GMT+${number}:${number}`

Id of supported default timezone to use for the actual timezone calculations, see [TimezoneId](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid)

### id[​](#id)
• id: [`TimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid) | [`CustomTimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#customtimezoneid)

Timezone identifier [TimezoneId](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid)

### offset[​](#offset)
• `Optional` offset: `number`

Optional number to indicate an offset

## Accessors[​](#accessors)
### title[​](#title)
• `get` title(): `string`

Name of the timezone

#### Returns[​](#returns)
`string`

- [Properties](#properties)[alias](#alias)- [id](#id)- [offset](#offset)- [Accessors](#accessors)[title](#title)