---
title: "Interface: CustomFormatter | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomFormatter"
extracted_at: "2025-06-22T09:35:28.272Z"
---

- [](/charting-library-docs/)- Interfaces- CustomFormatterOn this page# Interface: CustomFormatter[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CustomFormatter

## Methods[​](#methods)
### format[​](#format)
▸ format(`date`): `string`

Formats date and time

#### Parameters[​](#parameters)
NameType`date``Date`
#### Returns[​](#returns)
`string`

### formatLocal[​](#formatlocal)
▸ formatLocal(`date`): `string`

Converts date and time to local time zone.

#### Parameters[​](#parameters-1)
NameType`date``Date`
#### Returns[​](#returns-1)
`string`

### parse[​](#parse)
▸ parse(`value`): `string`

Returns a value in a format known by the UI.
Required when using `dateFormatter`, it has to return a date in the following format: `YYYY-MM-DD`.
#### Parameters[​](#parameters-2)
NameType`value``string`
#### Returns[​](#returns-2)
`string`

- [Methods](#methods)[format](#format)- [formatLocal](#formatlocal)- [parse](#parse)