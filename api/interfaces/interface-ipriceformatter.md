---
title: "Interface: IPriceFormatter | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IPriceFormatter"
extracted_at: "2025-06-22T09:54:49.105Z"
---

- [](/charting-library-docs/)- Interfaces- IPriceFormatterOn this page# Interface: IPriceFormatter[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IPriceFormatter

Specific formatter for numbers

## Hierarchy[​](#hierarchy)

[`ISymbolValueFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter)

↳ `IPriceFormatter`

## Methods[​](#methods)
### format[​](#format)
▸ format(`price`, `options?`): `string`

Price formatter

#### Parameters[​](#parameters)
NameType`price``number``options?`[`PriceFormatterFormatOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PriceFormatterFormatOptions)
#### Returns[​](#returns)
`string`

#### Overrides[​](#overrides)
[ISymbolValueFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter).[format](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter#format)

### formatChange[​](#formatchange)
▸ formatChange(`price`, `prevPrice`, `options?`): `string`

Price change formatter

#### Parameters[​](#parameters-1)
NameType`price``number``prevPrice``number``options?`[`PriceFormatterFormatOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PriceFormatterFormatOptions)
#### Returns[​](#returns-1)
`string`

#### Overrides[​](#overrides-1)
[ISymbolValueFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter).[formatChange](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter#formatchange)

### parse[​](#parse)
▸ parse(`value`, `options?`): [`ErrorFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ErrorFormatterParseResult) | [`SuccessFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult)<`number`>

Check if the input value satisfies the logic and return either an error or the result of the parsing

#### Parameters[​](#parameters-2)
NameType`value``string``options?`[`FormatterParseOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterParseOptions)
#### Returns[​](#returns-2)
[`ErrorFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ErrorFormatterParseResult) | [`SuccessFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult)<`number`>

#### Inherited from[​](#inherited-from)
[ISymbolValueFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter).[parse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter#parse)

- [Hierarchy](#hierarchy)- [Methods](#methods)[format](#format)- [formatChange](#formatchange)- [parse](#parse)