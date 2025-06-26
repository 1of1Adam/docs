---
title: "Interface: HistoryMetadata | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.HistoryMetadata"
extracted_at: "2025-06-22T09:51:54.564Z"
---

- [](/charting-library-docs/)- Interfaces- HistoryMetadataOn this page# Interface: HistoryMetadata[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).HistoryMetadata

Information passed to `onHistoryCallback` for getBars.

## Properties[​](#properties)
### nextTime[​](#nexttime)
• `Optional` nextTime: `number`

The time of the next available bar in history. The time value should be represented with a Unix timestamp in milliseconds.

You can pass the `nextTime` value to the library if there is no data in the time range that the library requests.
Therefore, you notify the library about available data before the requested range and ensure that the next data request is for the right range.
For more information, refer to the [How nextTime works](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF#how-nexttime-works) section.

### noData[​](#nodata)
• `Optional` noData: `boolean`

Optional value indicating to the library that there is no more data on the server.

- [Properties](#properties)[nextTime](#nexttime)- [noData](#nodata)