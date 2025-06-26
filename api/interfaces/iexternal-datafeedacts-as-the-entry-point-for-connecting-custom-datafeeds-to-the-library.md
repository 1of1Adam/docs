---
title: "Interface: IExternalDatafeed | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IExternalDatafeed"
extracted_at: "2025-06-22T09:30:03.341Z"
---

# Interface: IExternalDatafeed[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).IExternalDatafeed

## Methods
### onReady
▸ **onReady**(`callback`): `void`

This call is intended to provide the object filled with the configuration data.
The lib assumes that you will call the callback function and pass your datafeed [DatafeedConfiguration](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration) as an argument.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `callback` | [`OnReadyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#onreadycallback) | callback to return your datafeed configuration ([DatafeedConfiguration](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration)) to the library. ||

#### Returns
`void`