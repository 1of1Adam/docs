---
title: "Interface: IWatchListApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi"
extracted_at: "2025-06-22T09:39:53.758Z"
---

- [](/charting-library-docs/)- Interfaces- IWatchListApiOn this page# Interface: IWatchListApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IWatchListApi

An API object for interacting with the [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List) widget.
The Watchlist is a widget that allows users to track price movements and volume of specific financial instruments in real-time.
Watchlists also allow users to quickly switch between the symbols.
The Watchlist widget is displayed on the widget panel on the right side of the chart.
Notes about watchlist contents

Watchlist items should be symbol names which your datafeed [`resolveSymbol`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#resolvesymbol) method can resolve. This
means that generally shorter names such as `AAPL` can be used if your datafeed understands it. However,
it is recommend that you provide the symbol names as they appear within the `LibrarySymbolInfo` object, for
example, `NASDAQ:AAPL`.
## Methods[​](#methods)
### createList[​](#createlist)
▸ createList(`listName?`, `symbols?`): [`WatchListSymbolList`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WatchListSymbolList)

Create a list of symbols with `listName` name. If the `listName` parameter is not provided or there is no WatchList then `null` will be returned;

#### Parameters[​](#parameters)
NameTypeDescription`listName?``string`name for the watchlist`symbols?``string`[]Symbol IDs for the watchlist. Any list item that has the `###` prefix is considered a section divider in the watchlist.
#### Returns[​](#returns)
[`WatchListSymbolList`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WatchListSymbolList)

WatchListSymbolList

### defaultList[​](#defaultlist)
▸ defaultList(): `string`[]

Get a default list of symbols.

#### Returns[​](#returns-1)
`string`[]

default list of symbols

### deleteList[​](#deletelist)
▸ deleteList(`listId`): `void`

Delete a watchlist of symbols

#### Parameters[​](#parameters-1)
NameTypeDescription`listId``string`watchlist ID
#### Returns[​](#returns-2)
`void`

### getActiveListId[​](#getactivelistid)
▸ getActiveListId(): `string`

Get the ID of the current watchlist. If there is no WatchList then `null` will be returned.

#### Returns[​](#returns-3)
`string`

id of active watchlist

### getAllLists[​](#getalllists)
▸ getAllLists(): [`WatchListSymbolListMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WatchListSymbolListMap)

Get all watchlists. If there is no WatchList then `null` will be returned.

#### Returns[​](#returns-4)
[`WatchListSymbolListMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WatchListSymbolListMap)

object of all watchlists

### getList[​](#getlist)
▸ getList(`id?`): `string`[]

Get a list of symbols.
If the `id` parameter is not provided, the current list will be returned. If there is no watchList, `null` will be returned.
#### Parameters[​](#parameters-2)
NameTypeDescription`id?``string`Watchlist ID
#### Returns[​](#returns-5)
`string`[]

list of symbols for watchlist

### onActiveListChanged[​](#onactivelistchanged)
▸ onActiveListChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)>

Subscription for when the active watchlist is changed to a different list. Use the `subscribe` method of the returned [ISubscription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription) object to subscribe to the notifications.

#### Returns[​](#returns-6)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)>

### onListAdded[​](#onlistadded)
▸ onListAdded(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`WatchListSymbolListAddedCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watchlistsymbollistaddedcallback)>

Subscription for when a new list is added to the watchlist widget. Use the `subscribe` method of the returned [ISubscription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription) object to subscribe to the notifications.

#### Returns[​](#returns-7)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`WatchListSymbolListAddedCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watchlistsymbollistaddedcallback)>

### onListChanged[​](#onlistchanged)
▸ onListChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`WatchListSymbolListChangedCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watchlistsymbollistchangedcallback)>

Subscription for when the symbols of the active watchlist are changed. Use the `subscribe` method of the returned [ISubscription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription) object to subscribe to the notifications.

#### Returns[​](#returns-8)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`WatchListSymbolListChangedCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watchlistsymbollistchangedcallback)>

### onListRemoved[​](#onlistremoved)
▸ onListRemoved(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`WatchListSymbolListRemovedCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watchlistsymbollistremovedcallback)>

Subscription for when a list is removed from the watchlist widget. Use the `subscribe` method of the returned [ISubscription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription) object to subscribe to the notifications.

#### Returns[​](#returns-9)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`WatchListSymbolListRemovedCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watchlistsymbollistremovedcallback)>

### onListRenamed[​](#onlistrenamed)
▸ onListRenamed(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`WatchListSymbolListRenamedCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watchlistsymbollistrenamedcallback)>

Subscription for when a list is renamed. Use the `subscribe` method of the returned [ISubscription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription) object to subscribe to the notifications.

#### Returns[​](#returns-10)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`WatchListSymbolListRenamedCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watchlistsymbollistrenamedcallback)>

### renameList[​](#renamelist)
▸ renameList(`listId`, `newName`): `void`

Rename the watchlist.

#### Parameters[​](#parameters-3)
NameTypeDescription`listId``string`ID of the watchlist`newName``string`New name to set for the watchlist
#### Returns[​](#returns-11)
`void`

### saveList[​](#savelist)
▸ saveList(`list`): `boolean`

Save a list of symbols.

#### Parameters[​](#parameters-4)
NameType`list`[`WatchListSymbolList`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WatchListSymbolList)
#### Returns[​](#returns-12)
`boolean`

If there is no watchList or an equivalent list already exists, `false` will be returned. Otherwise, `true` will be returned.

### setActiveList[​](#setactivelist)
▸ setActiveList(`id`): `void`

Make the watchlist with the specified `id` active.

#### Parameters[​](#parameters-5)
NameTypeDescription`id``string`watchlist ID
#### Returns[​](#returns-13)
`void`

### setList[​](#setlist)
▸ setList(`symbols`): `void`

Obsolete. Use `updateList` instead.

Set the list of symbols for the watchlist. It will replace the entire list.

#### Parameters[​](#parameters-6)
NameTypeDescription`symbols``string`[]symbol IDs
#### Returns[​](#returns-14)
`void`

### updateList[​](#updatelist)
▸ updateList(`listId`, `symbols`): `void`

Edit the list of symbols for a watchlist.

#### Parameters[​](#parameters-7)
NameTypeDescription`listId``string`ID of the watchlist`symbols``string`[]Symbols to be set for the watchlist. Any list item that has the `###` prefix is considered a section divider in the watchlist.
#### Returns[​](#returns-15)
`void`

- [Methods](#methods)[createList](#createlist)- [defaultList](#defaultlist)- [deleteList](#deletelist)- [getActiveListId](#getactivelistid)- [getAllLists](#getalllists)- [getList](#getlist)- [onActiveListChanged](#onactivelistchanged)- [onListAdded](#onlistadded)- [onListChanged](#onlistchanged)- [onListRemoved](#onlistremoved)- [onListRenamed](#onlistrenamed)- [renameList](#renamelist)- [saveList](#savelist)- [setActiveList](#setactivelist)- [setList](#setlist)- [updateList](#updatelist)