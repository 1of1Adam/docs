---
title: "Interface: IDatafeedQuotesApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IDatafeedQuotesApi"
extracted_at: "2025-06-22T09:52:00.950Z"
---

- [](/charting-library-docs/)- Interfaces- IDatafeedQuotesApiOn this page# Interface: IDatafeedQuotesApi[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).IDatafeedQuotesApi

Quotes datafeed API

## Methods[​](#methods)
### getQuotes[​](#getquotes)
▸ getQuotes(`symbols`, `onDataCallback`, `onErrorCallback`): `void`

This function is called when the library needs quote data.
The library assumes that `onDataCallback` is called once when all the requested data is received.
#### Parameters[​](#parameters)
NameTypeDescription`symbols``string`[]symbol names.`onDataCallback`[`QuotesCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#quotescallback)callback to return the requested data.`onErrorCallback`[`QuotesErrorCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#quoteserrorcallback)callback for responding with an error.
#### Returns[​](#returns)
`void`

### subscribeQuotes[​](#subscribequotes)
▸ subscribeQuotes(`symbols`, `fastSymbols`, `onRealtimeCallback`, `listenerGUID`): `void`

Trading Platform calls this function when it wants to receive real-time quotes for a symbol.
The library assumes that you will call `onRealtimeCallback` every time you want to update the quotes.
#### Parameters[​](#parameters-1)
NameTypeDescription`symbols``string`[]list of symbols that should be updated rarely (once per minute). These symbols are included in the watchlist but they are not visible at the moment.`fastSymbols``string`[]list of symbols that should be updated frequently (at least once every 10 seconds)`onRealtimeCallback`[`QuotesCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#quotescallback)callback to send realtime quote data updates`listenerGUID``string`unique identifier of the listener
#### Returns[​](#returns-1)
`void`

### unsubscribeQuotes[​](#unsubscribequotes)
▸ unsubscribeQuotes(`listenerGUID`): `void`

Trading Platform calls this function when it doesn't want to receive updates for this listener anymore.
`listenerGUID` will be the same object that the Library passed to `subscribeQuotes` before.
#### Parameters[​](#parameters-2)
NameTypeDescription`listenerGUID``string`unique identifier of the listener
#### Returns[​](#returns-2)
`void`

- [Methods](#methods)[getQuotes](#getquotes)- [subscribeQuotes](#subscribequotes)- [unsubscribeQuotes](#unsubscribequotes)