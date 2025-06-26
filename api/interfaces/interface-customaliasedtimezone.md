---
title: "Interface: CustomAliasedTimezone | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomAliasedTimezone"
extracted_at: "2025-06-22T09:35:20.807Z"
---

- [](/charting-library-docs/)- Interfaces- CustomAliasedTimezoneOn this page# Interface: CustomAliasedTimezone[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CustomAliasedTimezone

## Hierarchy[​](#hierarchy)

[`CustomTimezoneInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomTimezoneInfo)

↳ `CustomAliasedTimezone`

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
#### Inherited from[​](#inherited-from)
[CustomTimezoneInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomTimezoneInfo).[alias](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomTimezoneInfo#alias)

### id[​](#id)
• id: [`CustomTimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#customtimezoneid)

Id for the custom timezone.

### title[​](#title)
• title: `string`

Display name for the timezone

#### Inherited from[​](#inherited-from-1)
[CustomTimezoneInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomTimezoneInfo).[title](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomTimezoneInfo#title)

- [Hierarchy](#hierarchy)- [Properties](#properties)[alias](#alias)- [id](#id)- [title](#title)