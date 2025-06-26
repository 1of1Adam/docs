---
title: "Implement streaming | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Streaming-Implementation"
extracted_at: "2025-06-22T09:32:45.040Z"
---

# Implement streaming
> **Tip:** This article is part of a tutorial about implementing Datafeed API.
We recommend that you follow the guide from the [start](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/).

At this stage, you will implement real-time data updates via WebSocket.
You will know how to:

- Connect to streaming and unsubscribe from it.
- Subscribe for data updates and handle them.

## Step 1. Connect to streaming
To connect your datafeed to the streaming API:

Import `apiKey` from [`helpers.js`](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Datafeed-Implementation#resolvesymbol) into `streaming.js`.

/chart‑project/src/streaming.js```
import { apiKey } from './helpers.js';

```

Create a new file called `streaming.js`, where you will implement a connection to WebSocket.

/chart‑project/src/streaming.js```
const socket = new WebSocket(
    'wss://streamer.cryptocompare.com/v2?api_key=' + apiKey
);

const channelToSubscription = new Map();

socket.addEventListener('open', () => {
    console.log('[socket] Connected');
});

socket.addEventListener('close', (reason) => {
    console.log('[socket] Disconnected:', reason);
});

socket.addEventListener('error', (error) => {
    console.log('[socket] Error:', error);
});

export function subscribeOnStream() {
    // To Do
}

export function unsubscribeFromStream() {
    // To Do
}

```

Import the functions from `streaming.js` into `datafeed.js`:

/chart‑project/src/datafeed.js```
import { subscribeOnStream, unsubscribeFromStream } from './streaming.js';

```

To subscribe for real-time data updates for a symbol, implement [`subscribeBars`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#subscribebars).
the library calls it every time the chart symbol or resolution is changed,
or when the chart needs to subscribe to a new symbol.
/chart‑project/src/datafeed.js```
// ...
// Use it to keep a record of the most recent bar on the chart
const lastBarsCache = new Map();
// ...
export default {
    // ...
    subscribeBars: (
        symbolInfo,
        resolution,
        onRealtimeCallback,
        subscriberUID,
        onResetCacheNeededCallback
    ) => {
        console.log('[subscribeBars]: Method call with subscriberUID:', subscriberUID);
        subscribeOnStream(
            symbolInfo,
            resolution,
            onRealtimeCallback,
            subscriberUID,
            onResetCacheNeededCallback,
            lastBarsCache.get(symbolInfo.full_name),
        );
    },
};

```

Implement [`unsubscribeBars`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#unsubscribebars) to stop receiving updates for the symbol when a user selects another symbol on the chart.

/chart‑project/src/datafeed.js```
unsubscribeBars: (subscriberUID) => {
    console.log('[unsubscribeBars]: Method call with subscriberUID:', subscriberUID);
    unsubscribeFromStream(subscriberUID);
},

```

## Step 2. Subscribe for updates
On the previous step, you connected your datafeed to WebSocket.
Now, you need to subscribe to the channels to receive updates:

Import `parseFullSymbol` from [`helpers.js`](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Datafeed-Implementation#resolvesymbol) into `streaming.js`.

/chart‑project/src/streaming.js```
import { parseFullSymbol, apiKey } from './helpers.js';

```

Implement `subscribeOnStream` to subscribe for updates.

/chart‑project/src/streaming.js```
// ...
const channelToSubscription = new Map();
// ...
export function subscribeOnStream(
    symbolInfo,
    resolution,
    onRealtimeCallback,
    subscriberUID,
    onResetCacheNeededCallback,
    lastDailyBar
)
{
    const parsedSymbol = parseFullSymbol(symbolInfo.full_name);
    const channelString = `0~${parsedSymbol.exchange}~${parsedSymbol.fromSymbol}~${parsedSymbol.toSymbol}`;
    const handler = {
        id: subscriberUID,
        callback: onRealtimeCallback,
    };
    let subscriptionItem = channelToSubscription.get(channelString);
    if (subscriptionItem) {
        // Already subscribed to the channel, use the existing subscription
        subscriptionItem.handlers.push(handler);
        return;
    }
    subscriptionItem = {
        subscriberUID,
        resolution,
        lastDailyBar,
        handlers: [handler],
    };
    channelToSubscription.set(channelString, subscriptionItem);
    console.log(
        '[subscribeBars]: Subscribe to streaming. Channel:',
        channelString
    );
    const subRequest = {
        action: 'SubAdd',
        subs: [channelString],
    };
    socket.send(JSON.stringify(subRequest));
}

```

## Step 3. Unsubscribe from streaming
Implement `unsubscribeFromStream` to unsubscribe from streaming:

/chart‑project/src/streaming.js```
export function unsubscribeFromStream(subscriberUID) {
    // Find a subscription with id === subscriberUID
    for (const channelString of channelToSubscription.keys()) {
        const subscriptionItem = channelToSubscription.get(channelString);
        const handlerIndex = subscriptionItem.handlers.findIndex(
            (handler) => handler.id === subscriberUID
        );
        if (handlerIndex !== -1) {
            // Remove from handlers
            subscriptionItem.handlers.splice(handlerIndex, 1);
            if (subscriptionItem.handlers.length === 0) {
                // Unsubscribe from the channel if it was the last handler
                console.log(
                    '[unsubscribeBars]: Unsubscribe from streaming. Channel:',
                    channelString
                );
                const subRequest = {
                    action: 'SubRemove',
                    subs: [channelString],
                };
                socket.send(JSON.stringify(subRequest));
                channelToSubscription.delete(channelString);
                break;
            }
        }
    }
}

```
## Step 4. Handle updates
The responses for requests look like this:

```
0~Bitfinex~BTC~USD~2~335394436~1548837377~0.36~3504.1~1261.4759999999999~1f

```
To handle updates coming from the WebSocket:

Implement the following function in `streaming.js`:

/chart‑project/src/streaming.js```
    // ...
socket.addEventListener('message', (event) => {
    const data = JSON.parse(event.data);
    console.log('[socket] Message:', data);
    const {
        TYPE: eventTypeStr,
        M: exchange,
        FSYM: fromSymbol,
        TSYM: toSymbol,
        TS: tradeTimeStr,
        P: tradePriceStr,
    } = data;

    if (parseInt(eventTypeStr) !== 0) {
        // Skip all non-trading events
        return;
    }
    const tradePrice = parseFloat(tradePriceStr);
    const tradeTime = parseInt(tradeTimeStr);
    const channelString = `0~${exchange}~${fromSymbol}~${toSymbol}`;
    const subscriptionItem = channelToSubscription.get(channelString);
    if (subscriptionItem === undefined) {
        return;
    }
    const lastDailyBar = subscriptionItem.lastDailyBar;
    let bar = {
        ...lastDailyBar,
        high: Math.max(lastDailyBar.high, tradePrice),
        low: Math.min(lastDailyBar.low, tradePrice),
        close: tradePrice,
    };
    console.log('[socket] Update the latest bar by price', tradePrice);
    subscriptionItem.lastDailyBar = bar;

    // Send data to every subscriber of that symbol
    subscriptionItem.handlers.forEach((handler) => handler.callback(bar));
});

```

Adjust the [`getBars`](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Datafeed-Implementation#getbars) method in `datafeed.js` to save the last bar data for the current symbol.

/chart‑project/src/datafeed.js```
//...
data.Data.forEach( ... );
if (firstDataRequest) {
    lastBarsCache.set(symbolInfo.full_name, {
        ...bars[bars.length - 1],
    });
}
console.log(`[getBars]: returned ${bars.length} bar(s)`);
// ...

```

Add `getNextDailyBarTime` function to `streaming.js`.

/chart‑project/src/streaming.js```
function getNextDailyBarTime(barTime) {
    const date = new Date(barTime * 1000);
    date.setDate(date.getDate() + 1);
    return date.getTime() / 1000;
}

```
CryptoCompare API provides a streaming of ticks, not bars.
So, you need to check that the new trade is related to the new daily bar.
Note that you might need a more comprehensive check for the production version.

Adjust the `socket.on` listener in `streaming.js`.

```
socket.on('m', data => {
    //...
    const lastDailyBar = subscriptionItem.lastDailyBar;
    const nextDailyBarTime = getNextDailyBarTime(lastDailyBar.time);

    let bar;
    if (tradeTime >= nextDailyBarTime) {
        bar = {
            time: nextDailyBarTime,
            open: tradePrice,
            high: tradePrice,
            low: tradePrice,
            close: tradePrice,
        };
        console.log('[socket] Generate new bar', bar);
    } else {
        bar = {
            ...lastDailyBar,
            high: Math.max(lastDailyBar.high, tradePrice),
            low: Math.min(lastDailyBar.low, tradePrice),
            close: tradePrice,
        };
        console.log('[socket] Update the latest bar by price', tradePrice);
    }
    subscriptionItem.lastDailyBar = bar;
    //...
});

```

## Result
🎉 Congrats!
At this point, you have implemented a datafeed with searching and resolving symbols, loading historical data,
and providing real-time data updates via WebSocket.
Now you can run `npx serve` from the `chart-project` folder (if you have not already done it before)
and check how the implementation works.
## Complete code
Click the following sections to reveal the complete code for the examples at this stage of the tutorial.

`index.html````
<!DOCTYPE HTML>
<html>
    <head>
        <title>TradingView Advanced Charts example</title>

        <!-- The script that loads the library -->
        <script
            type="text/javascript"
            src="charting_library_cloned_data/charting_library/charting_library.js">
        </script>

        <!-- Custom datafeed module -->
        <script type="module" src="src/main.js"></script>
    </head>

    <body style="margin:0px;">
        <!-- A container for the the library widget -->
        <div id="tv_chart_container">
        </div>
    </body>
</html>

```
`datafeed.js````
import { makeApiRequest, generateSymbol, parseFullSymbol } from './helpers.js';
import { subscribeOnStream, unsubscribeFromStream } from './streaming.js';

const lastBarsCache = new Map();

// DatafeedConfiguration implementation
const configurationData = {
    // Represents the resolutions for bars supported by your datafeed
    supported_resolutions: ['1D', '1W', '1M'],
    // The `exchanges` arguments are used for the `searchSymbols` method if a user selects the exchange
    exchanges: [{
        value: 'Bitfinex',
        name: 'Bitfinex',
        desc: 'Bitfinex',
    },
    {
        value: 'Kraken',
        // Filter name
        name: 'Kraken',
        // Full exchange name displayed in the filter popup
        desc: 'Kraken bitcoin exchange',
    },
    ],
    // The `symbols_types` arguments are used for the `searchSymbols` method if a user selects this symbol type
    symbols_types: [{
        name: 'crypto',
        value: 'crypto',
    },
    ],
};

// Obtains all symbols for all exchanges supported by CryptoCompare API
async function getAllSymbols() {
    const data = await makeApiRequest('data/v3/all/exchanges');
    let allSymbols = ;

    for (const exchange of configurationData.exchanges) {
        const pairs = data.Data[exchange.value].pairs;

        for (const leftPairPart of Object.keys(pairs)) {
            const symbols = pairs[leftPairPart].map(rightPairPart => {
                const symbol = generateSymbol(exchange.value, leftPairPart, rightPairPart);
                return {
                    symbol: symbol.short,
                    full_name: symbol.full,
                    description: symbol.short,
                    exchange: exchange.value,
                    type: 'crypto',
                };
            });
            allSymbols = [...allSymbols, ...symbols];
        }
    }
    return allSymbols;
}

export default {
    onReady: (callback) => {
        console.log('[onReady]: Method call');
        setTimeout(() => callback(configurationData));
    },

    searchSymbols: async (
        userInput,
        exchange,
        symbolType,
        onResultReadyCallback,
    ) => {
        console.log('[searchSymbols]: Method call');
        const symbols = await getAllSymbols();
        const newSymbols = symbols.filter(symbol => {
            const isExchangeValid = exchange === '' || symbol.exchange === exchange;
            const isFullSymbolContainsInput = symbol.full_name
                .toLowerCase()
                .indexOf(userInput.toLowerCase()) !== -1;
            return isExchangeValid && isFullSymbolContainsInput;
        });
        onResultReadyCallback(newSymbols);
    },

    resolveSymbol: async (
        symbolName,
        onSymbolResolvedCallback,
        onResolveErrorCallback,
        extension
    ) => {
        console.log('[resolveSymbol]: Method call', symbolName);
        const symbols = await getAllSymbols();
        const symbolItem = symbols.find(({
            full_name,
        }) => full_name === symbolName);
        if (!symbolItem) {
            console.log('[resolveSymbol]: Cannot resolve symbol', symbolName);
            onResolveErrorCallback('cannot resolve symbol');
            return;
        }
        // Symbol information object
        const symbolInfo = {
            ticker: symbolItem.full_name,
            name: symbolItem.symbol,
            description: symbolItem.description,
            type: symbolItem.type,
            session: '24x7',
            timezone: 'Etc/UTC',
            exchange: symbolItem.exchange,
            minmov: 1,
            pricescale: 100,
            has_intraday: false,
            has_no_volume: true,
            has_weekly_and_monthly: false,
            supported_resolutions: configurationData.supported_resolutions,
            volume_precision: 2,
            data_status: 'streaming',
        };

        console.log('[resolveSymbol]: Symbol resolved', symbolName);
        onSymbolResolvedCallback(symbolInfo);
    },

    getBars: async (symbolInfo, resolution, periodParams, onHistoryCallback, onErrorCallback) => {
        const { from, to, firstDataRequest } = periodParams;
        console.log('[getBars]: Method call', symbolInfo, resolution, from, to);
        const parsedSymbol = parseFullSymbol(symbolInfo.full_name);
        const urlParameters = {
            e: parsedSymbol.exchange,
            fsym: parsedSymbol.fromSymbol,
            tsym: parsedSymbol.toSymbol,
            toTs: to,
            limit: 2000,
        };
        const query = Object.keys(urlParameters)
            .map(name => `${name}=${encodeURIComponent(urlParameters[name])}`)
            .join('&');
        try {
            const data = await makeApiRequest(`data/histoday?${query}`);
            if (data.Response && data.Response === 'Error' || data.Data.length === 0) {
                // "noData" should be set if there is no data in the requested period
                onHistoryCallback(, {
                    noData: true,
                });
                return;
            }
            let bars = ;
            data.Data.forEach(bar => {
                if (bar.time >= from && bar.time < to) {
                    bars = [...bars, {
                        time: bar.time * 1000,
                        low: bar.low,
                        high: bar.high,
                        open: bar.open,
                        close: bar.close,
                    }];
                }
            });
            if (firstDataRequest) {
                lastBarsCache.set(symbolInfo.full_name, {
                    ...bars[bars.length - 1],
                });
            }
            console.log(`[getBars]: returned ${bars.length} bar(s)`);
            onHistoryCallback(bars, {
                noData: false,
            });
        } catch (error) {
            console.log('[getBars]: Get error', error);
            onErrorCallback(error);
        }
    },

    subscribeBars: (
        symbolInfo,
        resolution,
        onRealtimeCallback,
        subscriberUID,
        onResetCacheNeededCallback,
    ) => {
        console.log('[subscribeBars]: Method call with subscriberUID:', subscriberUID);
        subscribeOnStream(
            symbolInfo,
            resolution,
            onRealtimeCallback,
            subscriberUID,
            onResetCacheNeededCallback,
            lastBarsCache.get(symbolInfo.full_name),
        );
    },

    unsubscribeBars: (subscriberUID) => {
        console.log('[unsubscribeBars]: Method call with subscriberUID:', subscriberUID);
        unsubscribeFromStream(subscriberUID);
    },
};

```
`streaming.js````
import { parseFullSymbol, apiKey } from './helpers.js';

const socket = new WebSocket(
    'wss://streamer.cryptocompare.com/v2?api_key=' + apiKey
);
const channelToSubscription = new Map();

socket.addEventListener('open', () => {
    console.log('[socket] Connected');
});

socket.addEventListener('close', (reason) => {
    console.log('[socket] Disconnected:', reason);
});

socket.addEventListener('error', (error) => {
    console.log('[socket] Error:', error);
});

socket.addEventListener('message', (event) => {
    const data = JSON.parse(event.data);
    console.log('[socket] Message:', data);
    const {
        TYPE: eventTypeStr,
        M: exchange,
        FSYM: fromSymbol,
        TSYM: toSymbol,
        TS: tradeTimeStr,
        P: tradePriceStr,
    } = data;

    if (parseInt(eventTypeStr) !== 0) {
        // Skip all non-trading events
        return;
    }
    const tradePrice = parseFloat(tradePriceStr);
    const tradeTime = parseInt(tradeTimeStr);
    const channelString = `0~${exchange}~${fromSymbol}~${toSymbol}`;
    const subscriptionItem = channelToSubscription.get(channelString);
    if (subscriptionItem === undefined) {
        return;
    }
    const lastDailyBar = subscriptionItem.lastDailyBar;
    const nextDailyBarTime = getNextDailyBarTime(lastDailyBar.time);

    let bar;
    if (tradeTime >= nextDailyBarTime) {
        bar = {
            time: nextDailyBarTime,
            open: tradePrice,
            high: tradePrice,
            low: tradePrice,
            close: tradePrice,
        };
        console.log('[socket] Generate new bar', bar);
    } else {
        bar = {
            ...lastDailyBar,
            high: Math.max(lastDailyBar.high, tradePrice),
            low: Math.min(lastDailyBar.low, tradePrice),
            close: tradePrice,
        };
        console.log('[socket] Update the latest bar by price', tradePrice);
    }
    subscriptionItem.lastDailyBar = bar;

    // Send data to every subscriber of that symbol
    subscriptionItem.handlers.forEach((handler) => handler.callback(bar));
});

function getNextDailyBarTime(barTime) {
    const date = new Date(barTime * 1000);
    date.setDate(date.getDate() + 1);
    return date.getTime() / 1000;
}

export function subscribeOnStream(
    symbolInfo,
    resolution,
    onRealtimeCallback,
    subscriberUID,
    onResetCacheNeededCallback,
    lastDailyBar
) {
    const parsedSymbol = parseFullSymbol(symbolInfo.full_name);
    const channelString = `0~${parsedSymbol.exchange}~${parsedSymbol.fromSymbol}~${parsedSymbol.toSymbol}`;
    const handler = {
        id: subscriberUID,
        callback: onRealtimeCallback,
    };
    let subscriptionItem = channelToSubscription.get(channelString);
    if (subscriptionItem) {
        // Already subscribed to the channel, use the existing subscription
        subscriptionItem.handlers.push(handler);
        return;
    }
    subscriptionItem = {
        subscriberUID,
        resolution,
        lastDailyBar,
        handlers: [handler],
    };
    channelToSubscription.set(channelString, subscriptionItem);
    console.log(
        '[subscribeBars]: Subscribe to streaming. Channel:',
        channelString
    );
    const subRequest = {
        action: 'SubAdd',
        subs: [channelString],
    };
    socket.send(JSON.stringify(subRequest));
}

export function unsubscribeFromStream(subscriberUID) {
    // Find a subscription with id === subscriberUID
    for (const channelString of channelToSubscription.keys()) {
        const subscriptionItem = channelToSubscription.get(channelString);
        const handlerIndex = subscriptionItem.handlers.findIndex(
            (handler) => handler.id === subscriberUID
        );

        if (handlerIndex !== -1) {
            // Remove from handlers
            subscriptionItem.handlers.splice(handlerIndex, 1);

            if (subscriptionItem.handlers.length === 0) {
                // Unsubscribe from the channel if it was the last handler
                console.log(
                    '[unsubscribeBars]: Unsubscribe from streaming. Channel:',
                    channelString
                );
                const subRequest = {
                    action: 'SubRemove',
                    subs: [channelString],
                };
                socket.send(JSON.stringify(subRequest));
                channelToSubscription.delete(channelString);
                break;
            }
        }
    }
}

```
## What's next?
We hope this tutorial helped you understand the essentials of the [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) and how to work with it.
If you want to dive deeper into the details, we recommend checking out the following articles:

- [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor): get a better understanding of the Widget Constructor's capabilities and settings.
- [Datafeed Common Issues](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues): explore common issues that you might face when implementing the Datafeed API.
- [Customization Overview](https://www.tradingview.com/charting-library-docs/latest/customization/): learn how to customize UI elements and chart behavior.