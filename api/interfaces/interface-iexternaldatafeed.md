---
title: "Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IExternalDatafeed"
extracted_at: "2025-06-22T09:52:02.013Z"
---

- [](/charting-library-docs/)- Interfaces- IExternalDatafeedOn this page# Interface: IExternalDatafeed[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).IExternalDatafeed

## Methods[​](#methods)
### onReady[​](#onready)
▸ onReady(`callback`): `void`

This call is intended to provide the object filled with the configuration data.
The lib assumes that you will call the callback function and pass your datafeed [DatafeedConfiguration](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration) as an argument.
#### Parameters[​](#parameters)
NameTypeDescription`callback`[`OnReadyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#onreadycallback)callback to return your datafeed configuration ([DatafeedConfiguration](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration)) to the library.
#### Returns[​](#returns)
`void`

- [Methods](#methods)[onReady](#onready)