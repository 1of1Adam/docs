---
title: "Watchlist | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List"
extracted_at: "2025-06-22T09:16:14.992Z"
---

# Watchlist## Overview
The **Watchlist** is a widget that allows users to track price movements and volume of specific financial instruments in real-time.
Watchlists also allow users to quickly switch between the symbols.
The Watchlist widget is displayed on the widget panel on the right side of the chart.

Users can manage their lists through the UI.
For example, they can create new lists, modify existing ones, export active lists, and perform other actions.
You can also programmatically manage user lists using the [Watchlist API](#watchlist-api).

## Enable the widget

> **Info:** The Watchlist widget requires quote data.
Therefore, you need to implement the [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes), [`subscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribequotes), and [`unsubscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#unsubscribequotes) methods within your Datafeed API.

The [`widgetbar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#widgetbar) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) allows managing the widget panel, including the Watchlist widget.
To enable the widget, set the [`watchlist`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WidgetBarParams#watchlist) property to `true`.
You can also select the default symbols for the default watchlist and make it read-only using the [`watchlist_settings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WidgetBarParams#watchlist_settings) property.
```
const datafeed = new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com");
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: datafeed,
    symbol: "AAPL",
    interval: "1D",
    widgetbar: {
        watchlist: true,
        watchlist_settings: {
            default_symbols: ["AAPL", "IBM", "MSFT"],
            readonly: true,
        },
    },
})

```
## Watchlist API
The Watchlist API provides extensive ways to interact with watchlists.
For example, you can modify watchlist values on the fly or subscribe to events to keep track of user watchlists.
Use the [`watchList`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#watchlist) method to retrieve the [`IWatchListApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi) object for interacting with the watchlist.

```
const watchlistApi = await widget.watchList();  // Get the Watchlist API

```
Watchlist items should be symbol names that your datafeed [`resolveSymbol`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#resolvesymbol) method can resolve.
This means that generally shorter names such as `AAPL` can be used if your datafeed understands it.
However, it is recommended that you provide the symbol names as they appear within the [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo) object,
for example, `NASDAQ:AAPL`.
### Create multiple watchlists
You cannot instantiate the widget with multiple watchlists directly from the Widget Constructor.
Instead, you should use the API to create multiple watchlists.
The code sample below shows how to create lists with and without specific items.
```
const watchlistApi = await widget.watchList(); // Get the Watchlist API
const firstList = watchlistApi.createList("First list"); // Create a new empty list
const secondList = watchlistApi.createList("Second list", ["AMZN", "ADBE"]); // Create another list with items

```
### Retrieve watchlist data
Use the [`getAllLists`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi#getalllists) method to get all watchlists' data such as their IDs, titles, and symbol IDs.

```
const watchlistApi = await widget.watchList(); // Get the Watchlist API
watchlistApi.getAllLists();

```
This method returns an instance of the `WatchListSymbolListMap` interface that contains watchlists' IDs and the corresponding [`WatchListSymbolList`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WatchListSymbolList) objects.

```
{
   "id123456789": {
      "id": "id123456789",
      "symbols": [
         "###TOP SECTION",
         "AAPL",
         "IBM",
         "###SECOND SECTION",
         "MSFT",
         "###NEW SECTION",
         "AMZN"
      ],
      "title": "Watchlist"
   },
   "id987654321": {
      "id": "id987654321",
      "symbols": [
         "MSFT",
         "ADBE",
         "AMZN"
      ],
      "title": "My list"
   }
}

```
You can also call the [`getActiveListId`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi#getactivelistid) method to get an ID of the active watchlist.

## Add sections
The more symbols users add, the more difficult it becomes to manage and navigate the list.
Sections in watchlists help users organize their lists more effectively.
Sections can be named, moved, and deleted.
You can also programmatically add sections to watchlists using sections dividers.
Any list item that has the `###` prefix is considered a section divider.

Adding sections to the default watchlist within the [Widget Constructor](#enable-the-widget).

```
widgetbar: {
    watchlist: true,
    watchlist_settings: {
        default_symbols: ["###TOP SECTION", "AAPL", "IBM", "###SECOND SECTION", "MSFT"],
        readonly: true,
    },
},

```

Adding sections with items to a new and existing watchlist using [API](#watchlist-api).

```
// Create new watchlist with a section and items
const watchlistApi = await widget.watchList();
const mySymbolList = watchlistApi.createList("My new list", ["###TEST SECTION", "AMZN", "ADBE"]);

// Add new section and item to the active watchlist
const activeListId = watchlistApi.getActiveListId();
const activeListItems = watchlistApi.getList(activeListId);
watchlistApi.updateList(activeListId, [...activeListItems, "###NEW TEST SECTION", "AAPL", "MSFT"]);

```

## Store watchlist items
Watchlist items are saved as part of the [user settings](https://www.tradingview.com/charting-library-docs/latest/saving_loading/user-settings).
By default, user settings are saved into the browser's [`localStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage),
but you can also save them using [`settings_adapter`](https://www.tradingview.com/charting-library-docs/latest/saving_loading/user-settings#settings-adapter) in your preferred storage.
If you want to store watchlist items separately from other settings,
you can implement your logic to store the watchlist data on your server.
You can use the `IWatchListApi` methods such as [`onListAdded`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi#onlistadded), [`onListChanged`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi#onlistchanged), [`onListRemoved`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi#onlistremoved), and [`onListRenamed`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi#onlistrenamed)
to know when something has changed and you should save it.
## Display logos
If you want to display logos for symbols within the Watchlist widget, follow the steps below:

- Add the [`show_symbol_logos`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#show_symbol_logos) featureset to the [`enabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#enabled_features) array.
Provide URLs for symbols in the [`logo_urls`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#logo_urls) property of the [`LibrarySymbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo) object.
Pass the object as a parameter to the callback of the [`resolveSymbol`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#resolvesymbol) method.
- Implement the [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes), [`subscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribequotes), and [`unsubscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#unsubscribequotes) methods within your Datafeed API.