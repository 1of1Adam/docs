---
title: "Interface: CustomTimezoneInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomTimezoneInfo"
extracted_at: "2025-06-22T09:35:48.759Z"
---

- [](/charting-library-docs/)- Interfaces- CustomTimezoneInfoOn this page# Interface: CustomTimezoneInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CustomTimezoneInfo

## Hierarchy[​](#hierarchy)

`CustomTimezoneInfo`

↳ [`CustomAliasedTimezone`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomAliasedTimezone)

## Properties[​](#properties)
### alias[​](#alias)
• alias: [`TimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid) | `Etc/GMT-${number}` | `Etc/GMT-${number}:${number}` | `Etc/GMT+${number}` | `Etc/GMT+${number}:${number}`

Timezone identifier ([TimezoneId](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid)) to which this custom
timezone should be mapped to. This must be a timezone supported
by library.
Additionally, you can specify a `Etc/GMT` timezone id.
In order to conform with the POSIX style, those zone names
beginning with "Etc/GMT" have their sign reversed from the
standard ISO 8601 convention. In the "Etc" area, zones west
of GMT have a positive sign and those east have a negative
sign in their name (e.g "Etc/GMT-14" is 14 hours ahead of GMT).

### title[​](#title)
• title: `string`

Display name for the timezone

- [Hierarchy](#hierarchy)- [Properties](#properties)[alias](#alias)- [title](#title)