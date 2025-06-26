---
title: "Required methods | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods"
extracted_at: "2025-06-22T09:28:24.771Z"
---

# Required methodsThis article describes the required methods in the [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/).
The library calls these methods to initialize the chart, resolve requested symbols, and load data for them.
At the end of the article, you can find [diagrams](#sequence-diagrams) illustrating the sequence in which methods are called.

> **Tip:** Refer to the [How to connect data via Datafeed API](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/) tutorial that explains how to implement the methods step-by-step .

## onReady
The library calls the [`onReady`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalDatafeed#onready) method when the chart is initialized. This method supplies the library with the datafeed configuration data such as supported symbol types, exchanges, time intervals (resolution), currency codes and more. Call the [`OnReadyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#onreadycallback) and pass a [`DatafeedConfiguration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedConfiguration) object as a parameter:

```
onReady: (callback) => {
    console.log('[onReady]: Method call');
    setTimeout(() => callback(configurationData));
}

```
The following code sample shows the [`DatafeedConfiguration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedConfiguration) implementation:

```
const configurationData = {
    supports_search: true,
    supports_group_request: false,
    supports_marks: true,
    supports_timescale_marks: true,
    supports_time: true,
    exchanges: [
        { value: "", name: "All Exchanges", desc: "" },
        { value: "NasdaqNM", name: "NasdaqNM", desc: "NasdaqNM" },
        { value: "NYSE", name: "NYSE", desc: "NYSE" }
    ],
    symbols_types: [
        { name: "All types", value: "" },
        { name: "Stock", value: "stock" },
        { name: "Index", value: "index" }
    ],
    supported_resolutions: ["D", "2D", "3D", "W", "3W", "M", "6M"]
}

```
## searchSymbols
The library calls the [`searchSymbols`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#searchsymbols) method to request symbols that match some user input. Pass the resulting array of symbols as a parameter to [`SearchSymbolsCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#searchsymbolscallback).

```
searchSymbols: async (
    userInput,
    exchange,
    symbolType,
    onResultReadyCallback,
) => {
    console.log('[searchSymbols]: Method call');
    const symbols = await getMatchingSymbolsFromBackend(userInput, exchange, symbolType);
    onResultReadyCallback(newSymbols);
}

```
As a result, the library gets an array of [`SearchSymbolResultItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SearchSymbolResultItem) objects that have the following format:

```
[
    {
        "symbol": "<short symbol name>",
        "description": "<symbol description>",
        "exchange": "<symbol exchange name>",
        "ticker": "<symbol ticker name>",
        "type": "stock" // "futures"/"crypto"/"forex"/"index"
    },
    {
        //...
    }
]

```
If no symbol is found, pass an empty array to [`SearchSymbolsCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#searchsymbolscallback).

You can adjust the frequency of search requests utilizing the [`symbol_search_request_delay`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#symbol_search_request_delay) property.

## resolveSymbol
The library calls the [`resolveSymbol`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#resolvesymbol) method to get [symbol information](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology) such as the exchange, time zone, trading hours, etc. Specify this information in a [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo) object as demonstrated below:

```
const symbolInfo = {
    ticker: 'BTCUSD',
    name: 'BTCUSD',
    description: 'Bitcoin/USD',
    type: symbolItem.type,
    session: '24x7',
    timezone: 'Etc/UTC',
    exchange: 'Example Exchange',
    minmov: 1,
    pricescale: 100,
    has_intraday: false,
    visible_plots_set: 'ohlcv',
    has_weekly_and_monthly: false,
    supported_resolutions: ['1', '5', '30', '60', '1D', '1W'],
    volume_precision: 2,
    data_status: 'streaming',
};

```
Pass symbol information as a parameter to [`ResolveCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolvecallback). If the symbol cannot be resolved, call [`ErrorCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#datafeederrorcallback) and specify an error message.

```
resolveSymbol: async (
    symbolName,
    onSymbolResolvedCallback,
    onResolveErrorCallback,
    extension
) => {
    try {
        const symbolInfo = await getSymbolInfoFromBackend(symbolName, extension);
        onSymbolResolvedCallback(symbolInfo);
    } catch (err) {
        onResolveErrorCallback(err.message);
    }
}

```
### Multiple symbol resolving
In the [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo) object, you can provide both [name](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#name) and [ticker](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#ticker) as the symbol name.
The library behaves differently based on whether these values are the same or different:

- If the name and ticker are the same, the library makes a single `resolveSymbol` call.
- If the name and ticker differ, the library resolves the symbol twice: once for the entered name (e.g., `KO`) and again for the resolved ticker (e.g., `NYSE:KO`).

Multiple resolving happens because a single symbol name can correspond to multiple tickers.
For example, AAPL might return results for NASDAQ and LSE.
By resolving the ticker separately, the library ensures accurate and complete information, as the ticker is expected to be unique and is prioritized for data display.
### Display invalid symbol icon
You can display the default TradingView icon when error occurs. To do this, specify the `"unknown_symbol"` error message:

```
onResolveErrorCallback("unknown_symbol");

```
In this case, the chart shows the following icon and message.

![Ghost icon](https://www.tradingview.com/charting-library-docs/assets/images/ghost-icon-error-10c3bc63614496de3cf31bca60a8fbc4.png)

> **Tip:** If the icon is not displayed, make sure that the [`hide_image_invalid_symbol`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#hide_image_invalid_symbol) featureset is not enabled.

## getBars
The library calls [`getBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#getbars) to get historical data in a certain range. To transfer the requested data, pass an array of [`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Bar) objects to [`HistoryCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#historycallback).

> **Info:** The library caches historical data. Therefore, you do not need to implement a client-side cache.

### Bar order
The array of [`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Bar) items should be arranged in **ascending chronological order**, meaning that the timestamps of the bars should be getting bigger for each bar in the array. For example, `[1484179200, 1484265600, 1484611200, ...]`.

Note that for **daily, weekly, and monthly** bars, the [`time`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Bar#time) value should represent the **beginning of the trading day** at 00:00:00 UTC, not the beginning of the session.

### Correct amount of data
The library calculates the amount of data that is necessary to fill the chart space and requests it in [`getBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#getbars). You cannot change this amount. Return data to [`getBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#getbars) based on the following [`PeriodParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PeriodParams) properties:

- [`from`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PeriodParams#from) — Unix timestamp of the leftmost requested bar. The library requires data in the `[from, to)` time range.
- [`to`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PeriodParams#to) — Unix timestamp of the rightmost requested bar **(not inclusive)**.
- [`countBack`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PeriodParams#countback) — the required amount of bars to load.

It is more important to pass the required number of bars than to match the `[from, to)` time range for the following reasons:

- The library might miscalculate the `from` value. It may happen if you provide incorrect [`session`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#session) or [`session_holidays`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#session_holidays) values. In this case, the `[from, to)` range does not represent the required number of bars.
- The library calculates the correct `from` value, but your backend does not contain enough bars in the `[from, to)` range. It might happen if the market was opened, but the symbol was not traded.

In both cases, the library calls [`getBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#getbars) multiple times in order to get the missing data. It might cause potential issues. To avoid them, consider the following recommendations:

- Return at least two bars — returning only one may cause an error when clicking on the chart.
- Your response should always include **all the existing data** for the requested range.
- If the number of bars in the requested range is less than the `countBack` value, you should include earlier bars until the `countBack` count is reached. For example, the chart requests 300 bars in the range `[2019-06-01T00:00:00..2020-01-01T00:00:00)`, and your backend have only 250 bars in the requested period. Return these 250 bars and 50 bars prior to `2019-06-01T00:00:00`.
- In the unlikely case that the number of bars in the requested range is larger than the `countBack` value, then you should return all the bars in that range instead of truncating it to the `countBack` length.
- If there is no data left (in other words the current response to return an empty array, **and** there is no older data on the server), set [`noData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.HistoryMetadata#nodata) to `true` to prevent further requests.

The library can request more bars than are visible because some indicators require additional history, for example, Moving Average with the length `10`.

> **Info:** Previously, it was necessary to specify [`noData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.HistoryMetadata#nodata) and [`nextTime`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.HistoryMetadata#nexttime) to load data outside the requested range. For now, you can send this data in response to the current request. However, you can still use these properties if your datafeed supports only the `from`/`to` properties and requires another request from the library.

The following piece of code is just a snippet to begin with. You will have to change it to fit your requirements but copying & pasting the code below should render candles on the chart for a given symbol and nothing for all other symbols. It is also to illustrate the `noData: true` result.

```
resolveSymbol(symbolName, onSymbolResolvedCallback, onResolveErrorCallback, extension) {
    setTimeout(
        () => {
            // Return some simple symbol information for the TEST symbol
            if (symbolName === 'TEST') {
                onSymbolResolvedCallback({
                    "name": "TEST",
                    "timezone": "America/New_York",
                    "minmov": 1,
                    "minmov2": 0,
                    "pointvalue": 1,
                    "session": "24x7",
                    "has_intraday": false,
                    "visible_plots_set": "c",
                    "description": "Test Symbol",
                    "type": "stock",
                    "supported_resolutions": [
                        "D"
                    ],
                    "pricescale": 100,
                    "ticker": "TEST",
                    "exchange": "Test Exchange",
                    "has_daily": true,
                    "format": "price"
                });
            } else {
                // Ignore all other symbols
                onResolveErrorCallback('unknown_symbol');
            }
        },
        50
    );
}

getBars(symbolInfo, resolution, periodParams, onHistoryCallback, onErrorCallback) {
    setTimeout(
        () => {
            // For this piece of code only we will only return bars for the TEST symbol
            if (symbolInfo.ticker === 'TEST' && resolution === '1D') {
                // We are constructing an array for `countBack` bars.
                const bars = new Array(periodParams.countBack);

                // For constructing the bars we are starting from the `to` time minus 1 day, and working backwards until we have `countBack` bars.
                let time = new Date(periodParams.to * 1000);
                time.setUTCHours(0);
                time.setUTCMinutes(0);
                time.setUTCMilliseconds(0);
                time.setUTCDate(time.getUTCDate() - 1);

                // Fake price.
                let price = 100;

                for (let i = periodParams.countBack - 1; i > -1; i--) {
                    bars[i] = {
                        open: price,
                        high: price,
                        low: price,
                        close: price,
                        time: time.getTime(),
                    }

                    // Working out a random value for changing the fake price.
                    const volatility = 0.1;
                    const x = Math.random() - 0.5;
                    const changePercent = 2 * volatility * x;
                    const changeAmount = price * changePercent;
                    price = price + changeAmount;

                    // Note that this simple "-1 day" logic only works because the TEST symbol has a 24x7 session.
                    // For a more complex session we would need to, for example, skip weekends.
                    time.setUTCDate(time.getUTCDate() - 1);
                }

                // Once all the bars (usually countBack is around 300 bars) the array of candles is returned to the library.
                onHistoryCallback(bars);
            } else {
                // If no result, return an empty array and specify it to the library by changing the value of `noData` to true.
                onHistoryCallback(, {
                    noData: true
                });
            }
        },
        50
    );
}
}

```
## subscribeBars
The library calls [`subscribeBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#subscribebars) to receive real-time updates for a symbol. Call [`SubscribeBarsCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#subscribebarscallback) every time you want to update the most recent bar or add a new one. For example, if the chart has loaded data up to 14:00, you can only update the last bar (14:00) or add a newer bar (15:00).

dangerYou cannot update a historical bar using this method. Otherwise, you get the *putToCacheNewBar: time violation* [issue](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues#time-violation). If you need to change historical data, you should call [`resetCache`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#resetcache) and then `chart.resetData()` to redraw the chart.

If you return a bar that has the same [`time`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Bar#time) value as the most recent bar, the library replaces the most recent bar with the new one.

Consider the following example. The most recent bar (in pseudo-code) is `{time: 1419411578413, open: 10, high: 12, low: 9, close: 11}`.
You call `onRealtimeCallback({time: 1419411578413, open: 10, high: 14, low: 9, close: 14})`. As the bar with the time `1419411578413` already exists, and it is the most recent one, the library **replaces the entire bar** making the most recent bar `{time: 1419411578413, open: 10, high: 14, low: 9, close: 14}`.
Refer to the [tutorial][tutorial-subscribe-unsubscribe] to see the example of [`subscribeBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#subscribebars) implementation.

### Multiple subscriptions
The library provides a unique subscriber ID as a parameter when it calls `subscribeBars` and [`unsubscribeBars`](#unsubscribebars). This subscriber ID allows you to track and manage subscriptions for symbol updates.

The library can have multiple subscriptions at the same time, for example, when a user switches to another symbol or resolution. You should handle `subscribeBars` and `unsubscribeBars` calls for different resolutions and symbols as independent events. Note that the library can call these methods in any order and with a delay.

When you receive an update from the server, you should send the data via the specific callback for the subscriber which has the correct symbol name and [resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution).

dangerIf you send a subscriber data that does not match the subscriber's symbol and resolution, the *putToCacheNewBar: time violation* [issue](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues#time-violation) can occur.

Note that you should provide updates to all the subscriptions until the library unsubscribes from them. Therefore, you may require multiple connections to your backend server if you have multiple subscriptions.

Consider the following example. The current symbol is `AAPL`, and the resolution is `1D` (one day). You switch the resolution to `5` (five minutes). The library separately calls `subscribeBars` to subscribe for five-minute updates and `unsubscribeBars` to unsubscribe from one-day updates (after a short delay). During this period, the library has at least two active subscribers: for five-minute and one-day updates. You should send five-minute updates to the five-minute subscriber and continue to send one-day updates to the one-day subscriber until the library unsubscribes from the `1D` resolution.

Assume that the last bar (in pseudo-code) is:

- `{time: 1684368000000, open: 10, high: 12, low: 9, close: 11}` on the one-day chart
- `{time: 1684422300000, open: 10.5, high: 11.5, low: 10, close: 11}` on the five-minute chart

If the price jumps to `13`, you should send the following bars to the subscribers:

- `{time: 1684368000000, open: 10, high: 13, low: 9, close: 13}` to the one-day subscriber
- `{time: 1684422300000, open: 10.5, high: 13, low: 10, close: 13}` to the five-minute subscriber

## unsubscribeBars
The library calls [`unsubscribeBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#unsubscribebars) to stop receiving updates for the symbol when the user selects another symbol on the chart. The `listenerGuid` argument contains the same object that was passed to [`subscribeBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#subscribebars) before.

Refer to the [tutorial](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Streaming-Implementation#step-1-connect-to-streaming) to see the example of [`unsubscribeBars`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#unsubscribebars) implementation.

## Sequence diagrams
In this section, you can find diagrams illustrating the sequence of Datafeed API method calls.
Expand the sections below to view the diagrams for the following cases:
A user opens a chart for the first time.

[![Diagram illustrating the sequence of calls when a user opens chart for the first time](https://www.tradingview.com/charting-library-docs/img/datafeed-open-chart-first-time-diagram-light.svg)![Diagram illustrating the sequence of calls when a user opens chart for the first time](https://www.tradingview.com/charting-library-docs/img/datafeed-open-chart-first-time-diagram-dark.svg)](/charting-library-docs/img/datafeed-open-chart-first-time-diagram-light.svg)
A user switches to a new symbol or adds a new one to the chart.

[![Diagram illustrating the sequence of calls when a user switches to a new symbol](https://www.tradingview.com/charting-library-docs/img/datafeed-switch-to-new-symbol-diagram-light.svg)![Diagram illustrating the sequence of calls when a user switches to a new symbol](https://www.tradingview.com/charting-library-docs/img/datafeed-switch-to-new-symbol-diagram-dark.svg)](/charting-library-docs/img/datafeed-switch-to-new-symbol-diagram-light.svg)