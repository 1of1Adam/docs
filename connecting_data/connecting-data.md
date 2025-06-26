---
title: "Connecting Data | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/connecting_data/"
extracted_at: "2025-06-22T09:14:12.810Z"
---

# Connecting Data## Overview
The library is meant to be used on your own site, with your own source of market data. It does NOT include any market data. If you want to display TradingView market data, please check our [widgets](https://www.tradingview.com/widget/).

Unlike simple charts, the primary aim of which is just displaying data, the library gives users control over the chart.
Thus, market data connection API is designed in such a way, that all interactions (data requests, symbol information requests and symbol search) are initiated by the user.
## Datafeed API
The market data connection API ([Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/)) is a set of methods that must be implemented in JavaScript.

All these methods are called by the library as needed.

The library expects to get an implementation of the Datafeed API in the [datafeed](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#datafeed) field of the constructor.

## UDF
If you don’t have sufficient JavaScript knowledge, or if you don’t yet have a Web-based server API that you can fetch data from, then you can use a ready-made [UDF adapter](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF) that implements the [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) and makes simple HTTP(S) requests at the specified URL in a specific format. This adapter does not support data streaming out of the box (but it still can be added there). Do not use UDF with data grouping (see [`supports_group_request`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF#data-feed-configuration-data)) if your backend has more than **100** symbols.

Also, the UDF adapter can be used as an **example** implementation of the Datafeed API. You can copy [its code](https://github.com/tradingview/charting_library/tree/master/datafeeds/udf) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/)) and start editing it.

## Go ahead
[Start implementing Datafeed API if you have an existing Web API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/)

[Start with a predefined UDF adapter and implement a server-side API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF)