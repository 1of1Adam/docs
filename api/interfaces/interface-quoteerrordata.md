---
title: "Interface: QuoteErrorData | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteErrorData"
extracted_at: "2025-06-22T09:52:13.095Z"
---

- [](/charting-library-docs/)- Interfaces- QuoteErrorDataOn this page# Interface: QuoteErrorData[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).QuoteErrorData

Quote Data Error Response

## Hierarchy[​](#hierarchy)

[`QuoteDataResponse`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse)

↳ `QuoteErrorData`

## Properties[​](#properties)
### n[​](#n)
• n: `string`

Symbol name. This value must be exactly the same as in the request

#### Inherited from[​](#inherited-from)
[QuoteDataResponse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse).[n](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse#n)

### s[​](#s)
• s: `"error"`

Status code for symbol. Expected values: `ok` | `error`

#### Overrides[​](#overrides)
[QuoteDataResponse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse).[s](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse#s)

### v[​](#v)
• v: `object`

Quote Values

#### Overrides[​](#overrides-1)
[QuoteDataResponse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse).[v](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse#v)

- [Hierarchy](#hierarchy)- [Properties](#properties)[n](#n)- [s](#s)- [v](#v)