---
title: "Interface: QuoteDataResponse | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse"
extracted_at: "2025-06-22T09:52:11.967Z"
---

- [](/charting-library-docs/)- Interfaces- QuoteDataResponseOn this page# Interface: QuoteDataResponse[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).QuoteDataResponse

## Hierarchy[​](#hierarchy)

`QuoteDataResponse`

↳ [`QuoteErrorData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteErrorData)

↳ [`QuoteOkData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteOkData)

## Properties[​](#properties)
### n[​](#n)
• n: `string`

Symbol name. This value must be exactly the same as in the request

### s[​](#s)
• s: `"error"` | `"ok"`

Status code for symbol. Expected values: `ok` | `error`

### v[​](#v)
• v: `unknown`

Quote Values

- [Hierarchy](#hierarchy)- [Properties](#properties)[n](#n)- [s](#s)- [v](#v)