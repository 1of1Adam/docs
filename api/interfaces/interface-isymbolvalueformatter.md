---
title: "Interface: ISymbolValueFormatter | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISymbolValueFormatter"
extracted_at: "2025-06-22T09:54:56.110Z"
---

- [](/charting-library-docs/)- Interfaces- ISymbolValueFormatterOn this page# Interface: ISymbolValueFormatter[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).ISymbolValueFormatter

Specific formatter for number

## Hierarchy[​](#hierarchy)

[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)

↳ `ISymbolValueFormatter`

↳↳ [`IPriceFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IPriceFormatter)

## Methods[​](#methods)
### format[​](#format)
▸ format(`price`, `options?`): `string`

Default formatter function used to assign the correct sign (+ or -) to a number

#### Parameters[​](#parameters)
NameType`price``number``options?`[`SymbolValueFormatterFormatOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolValueFormatterFormatOptions)
#### Returns[​](#returns)
`string`

#### Overrides[​](#overrides)
[INumberFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter).[format](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter#format)

### formatChange[​](#formatchange)
▸ formatChange(`currentPrice`, `prevPrice`, `options?`): `string`

Formatter for a price change

#### Parameters[​](#parameters-1)
NameTypeDescription`currentPrice``number`current price`prevPrice``number`previous price`options?`[`SymbolValueFormatterFormatOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolValueFormatterFormatOptions)format options
#### Returns[​](#returns-1)
`string`

#### Overrides[​](#overrides-1)
[INumberFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter).[formatChange](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter#formatchange)

### parse[​](#parse)
▸ parse(`value`, `options?`): [`ErrorFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ErrorFormatterParseResult) | [`SuccessFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult)<`number`>

Check if the input value satisfies the logic and return either an error or the result of the parsing

#### Parameters[​](#parameters-2)
NameType`value``string``options?`[`FormatterParseOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterParseOptions)
#### Returns[​](#returns-2)
[`ErrorFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ErrorFormatterParseResult) | [`SuccessFormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult)<`number`>

#### Inherited from[​](#inherited-from)
[INumberFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter).[parse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter#parse)

- [Hierarchy](#hierarchy)- [Methods](#methods)[format](#format)- [formatChange](#formatchange)- [parse](#parse)