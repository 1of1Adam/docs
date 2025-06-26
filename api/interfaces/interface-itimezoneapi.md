---
title: "Interface: ITimezoneApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ITimezoneApi"
extracted_at: "2025-06-22T09:39:52.371Z"
---

- [](/charting-library-docs/)- Interfaces- ITimezoneApiOn this page# Interface: ITimezoneApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ITimezoneApi

## Methods[​](#methods)
### availableTimezones[​](#availabletimezones)
▸ availableTimezones(): readonly [`TimezoneInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimezoneInfo)[]

Array of supported TimezoneInfo

#### Returns[​](#returns)
readonly [`TimezoneInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimezoneInfo)[]

### getTimezone[​](#gettimezone)
▸ getTimezone(): [`TimezoneInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimezoneInfo)

Returns the current TimezoneInfo

#### Returns[​](#returns-1)
[`TimezoneInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimezoneInfo)

### onTimezoneChanged[​](#ontimezonechanged)
▸ onTimezoneChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`timezone`: [`TimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid)) => `void`>

To be notified when the timezone is changed

Example:

```
timezoneApi.onTimezoneChanged().subscribe(    null,    timezone => console.log(`New timezone: ${timezone}`),    true);
```
#### Returns[​](#returns-2)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<(`timezone`: [`TimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid)) => `void`>

### setTimezone[​](#settimezone)
▸ setTimezone(`timezone`, `options?`): `void`

Sets the current timezone

#### Parameters[​](#parameters)
NameType`timezone`[`TimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezoneid) | [`CustomTimezoneId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#customtimezoneid)`options?`[`UndoOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoOptions)
#### Returns[​](#returns-3)
`void`

- [Methods](#methods)[availableTimezones](#availabletimezones)- [getTimezone](#gettimezone)- [onTimezoneChanged](#ontimezonechanged)- [setTimezone](#settimezone)