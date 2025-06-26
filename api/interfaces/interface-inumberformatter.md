---
title: "Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter"
extracted_at: "2025-06-22T09:54:41.791Z"
---

- [](/charting-library-docs/)- Interfaces- INumberFormatterOn this page# Interface: INumberFormatter[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).INumberFormatter

Specific formatter for number

## Hierarchy[​](#hierarchy)

[`IFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IFormatter)<`number`>

↳ `INumberFormatter`

↳↳ [`ISymbolValueFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter)

## Methods[​](#methods)
### format[​](#format)
▸ format(`value?`, `options?`): `string`

Whatever the input type, formats the data following a certain logic and return that value as a string

#### Parameters[​](#parameters)
NameType`value?``number``options?`[`FormatterFormatOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterFormatOptions)
#### Returns[​](#returns)
`string`

#### Inherited from[​](#inherited-from)
[IFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IFormatter).[format](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IFormatter#format)

### formatChange[​](#formatchange)
▸ formatChange(`currentPrice`, `prevPrice`, `options?`): `string`

Formatter for a price change

#### Parameters[​](#parameters-1)
NameTypeDescription`currentPrice``number`current price`prevPrice``number`previous price`options?`[`FormatterFormatOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterFormatOptions)format options
#### Returns[​](#returns-1)
`string`

### parse[​](#parse)
▸ parse(`value`, `options?`): [`ErrorFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ErrorFormatterParseResult) | [`SuccessFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult)<`number`>

Check if the input value satisfies the logic and return either an error or the result of the parsing

#### Parameters[​](#parameters-2)
NameType`value``string``options?`[`FormatterParseOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterParseOptions)
#### Returns[​](#returns-2)
[`ErrorFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ErrorFormatterParseResult) | [`SuccessFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult)<`number`>

#### Inherited from[​](#inherited-from-1)
[IFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IFormatter).[parse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IFormatter#parse)

- [Hierarchy](#hierarchy)- [Methods](#methods)[format](#format)- [formatChange](#formatchange)- [parse](#parse)