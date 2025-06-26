---
title: "Interface: QuoteOkData | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteOkData"
extracted_at: "2025-06-22T09:52:18.217Z"
---

- [](/charting-library-docs/)- Interfaces- QuoteOkDataOn this page# Interface: QuoteOkData[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).QuoteOkData

Quote Data Ok Response

## Hierarchy[​](#hierarchy)

[`QuoteDataResponse`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse)

↳ `QuoteOkData`

## Properties[​](#properties)
### n[​](#n)
• n: `string`

Symbol name. This value must be exactly the same as in the request

#### Inherited from[​](#inherited-from)
[QuoteDataResponse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse).[n](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse#n)

### s[​](#s)
• s: `"ok"`

Status code for symbol. Expected values: `ok` | `error`

#### Overrides[​](#overrides)
[QuoteDataResponse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse).[s](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse#s)

### v[​](#v)
• v: [`DatafeedQuoteValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedQuoteValues)

Quote Values

#### Overrides[​](#overrides-1)
[QuoteDataResponse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse).[v](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.QuoteDataResponse#v)

- [Hierarchy](#hierarchy)- [Properties](#properties)[n](#n)- [s](#s)- [v](#v)