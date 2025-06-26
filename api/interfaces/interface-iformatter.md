---
title: "Interface: IFormatter<T> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IFormatter"
extracted_at: "2025-06-22T09:54:39.735Z"
---

- [](/charting-library-docs/)- Interfaces- IFormatterOn this page# Interface: IFormatter<T>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IFormatter

Definition of a formatter

## Type parameters[​](#type-parameters)
Name`T`
## Hierarchy[​](#hierarchy)

`IFormatter`

↳ [`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)

## Methods[​](#methods)
### format[​](#format)
▸ format(`value?`, `options?`): `string`

Whatever the input type, formats the data following a certain logic and return that value as a string

#### Parameters[​](#parameters)
NameType`value?``T``options?`[`FormatterFormatOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterFormatOptions)
#### Returns[​](#returns)
`string`

### parse[​](#parse)
▸ parse(`value`, `options?`): [`ErrorFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ErrorFormatterParseResult) | [`SuccessFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult)<`T`>

Check if the input value satisfies the logic and return either an error or the result of the parsing

#### Parameters[​](#parameters-1)
NameType`value``string``options?`[`FormatterParseOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterParseOptions)
#### Returns[​](#returns-1)
[`ErrorFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ErrorFormatterParseResult) | [`SuccessFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult)<`T`>

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Methods](#methods)[format](#format)- [parse](#parse)