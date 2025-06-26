---
title: "Interface: SuccessFormatterParseResult<T> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SuccessFormatterParseResult"
extracted_at: "2025-06-22T09:56:22.138Z"
---

- [](/charting-library-docs/)- Interfaces- SuccessFormatterParseResultOn this page# Interface: SuccessFormatterParseResult<T>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).SuccessFormatterParseResult

## Type parameters[​](#type-parameters)
Name`T`
## Hierarchy[​](#hierarchy)

[`FormatterParseResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterParseResult)

↳ `SuccessFormatterParseResult`

## Properties[​](#properties)
### res[​](#res)
• res: `true`

Returns if the formatter support parsing

#### Overrides[​](#overrides)
[FormatterParseResult](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterParseResult).[res](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.FormatterParseResult#res)

### suggest[​](#suggest)
• `Optional` suggest: `string`

Optional value returned by the default formatter

### value[​](#value)
• value: `T`

Returned value once parsing is done

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Properties](#properties)[res](#res)- [suggest](#suggest)- [value](#value)