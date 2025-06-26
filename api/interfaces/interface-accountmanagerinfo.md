---
title: "Interface: AccountManagerInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerInfo"
extracted_at: "2025-06-22T09:53:04.562Z"
---

- [](/charting-library-docs/)- Interfaces- AccountManagerInfoOn this page# Interface: AccountManagerInfo[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).AccountManagerInfo

The information object that is used to build the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).

## Properties[​](#properties)
### accountTitle[​](#accounttitle)
• accountTitle: `string`

Name of the broker

### customFormatters[​](#customformatters)
• `Optional` customFormatters: [`CustomTableElementFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomTableElementFormatter)<[`TableFormatterInputValues`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tableformatterinputvalues)>[]

An optional array for defining [custom formatters](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/value-formatters#custom-formatters).
Each formatter description is an object with the following fields:

`name` ([FormatterName](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#formattername)): Unique formatter name.

`formatText` ([TableFormatTextFunction](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tableformattextfunction)):
Function that is used for formatting a cell value to a string.
The `formatText` field is required because it is used to generate exported data.
You can return an empty string if you do not need this function.

`formatElement` ([CustomTableFormatElementFunction](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#customtableformatelementfunction) | `undefined`):
Optional function that is used for formatting a cell value to a string or an HTML element.

If the `formatElement` function is provided, it only handles the formatting of displayed values.
Otherwise the `formatText` function is used.
For optimal performance, it is recommended to only use `formatText` if you intend to display only string values.
Example

```
{    name: 'closeButton' as FormatterName, // Typecast to FormatterName. Use constant in real code    formatText: () => '', // Returns an empty string because we don't need to display this in the exported data    formatElement: ({ values: [id] }: TableFormatterInputs<[id: string]>) => {        const button = document.createElement('button');        button.innerText = 'Close';        button.addEventListener('click', () => {            event.stopPropagation();            closePosition(id);        });        return button;    },}
```

### historyColumns[​](#historycolumns)
• `Optional` historyColumns: [`AccountManagerColumn`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountmanagercolumn)[]

An array of data objects that create columns for the [History](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#history) page where all orders from previous sessions are shown.
Note that this page is only shown
if you set the [BrokerConfigFlags.supportOrdersHistory](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportordershistory) to `true`
and implement the [`ordersHistory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#ordershistory) method.

### historyColumnsSorting[​](#historycolumnssorting)
• `Optional` historyColumnsSorting: [`SortingParameters`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SortingParameters)

Optional sorting of the table on the [History](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#history) page.

### individualPositionColumns[​](#individualpositioncolumns)
• `Optional` individualPositionColumns: [`AccountManagerColumn`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountmanagercolumn)[]

You can display any field of an [IndividualPosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)
or add your own fields to an individualPosition object and display them.

### marginUsed[​](#marginused)
• `Optional` marginUsed: [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`number`>

Margin used

### orderColumns[​](#ordercolumns)
• orderColumns: [`OrderTableColumn`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#ordertablecolumn)[]

An array of data objects that create columns for the [Orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#orders-and-positions) page.
You can display any field of an [Order](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)
or add your own fields to an order object and display them.

### orderColumnsSorting[​](#ordercolumnssorting)
• `Optional` orderColumnsSorting: [`SortingParameters`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SortingParameters)

Optional sorting of the orders table.

### pages[​](#pages)
• pages: [`AccountManagerPage`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerPage)[]

Adds [custom pages](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#custom-pages) to the Account Manager. Each page is a set of tables.

### positionColumns[​](#positioncolumns)
• `Optional` positionColumns: [`AccountManagerColumn`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountmanagercolumn)[]

An array of data objects that create columns for the [Positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#orders-and-positions) page.
You can display any field of a [Position](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position)
or add your own fields to a position object and display them.

### possibleOrderStatuses[​](#possibleorderstatuses)
• `Optional` possibleOrderStatuses: [`OrderStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderStatus)[]

Optional list of statuses to be used in the orders filter. Default list is used if it hasn't been set.

### summary[​](#summary)
• summary: [`AccountManagerSummaryField`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerSummaryField)[]

Custom fields that are always displayed at the top-right corner of the Account Manager.
Refer to the [Account Summary row](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#account-summary-row) section for more information.
## Methods[​](#methods)
### contextMenuActions[​](#contextmenuactions)
▸ contextMenuActions(`contextMenuEvent`, `activePageActions`): `Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]>

A function for creating a custom [context menu](https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu) for positions and orders in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).

#### Parameters[​](#parameters)
NameTypeDescription`contextMenuEvent``MouseEvent` | `TouchEvent`MouseEvent or TouchEvent object passed by a browser`activePageActions`[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]array of `ActionMetaInfo` items for the current page
#### Returns[​](#returns)
`Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]>

`Promise` that is resolved with an array of `ActionMetaInfo`

- [Properties](#properties)[accountTitle](#accounttitle)- [customFormatters](#customformatters)- [historyColumns](#historycolumns)- [historyColumnsSorting](#historycolumnssorting)- [individualPositionColumns](#individualpositioncolumns)- [marginUsed](#marginused)- [orderColumns](#ordercolumns)- [orderColumnsSorting](#ordercolumnssorting)- [pages](#pages)- [positionColumns](#positioncolumns)- [possibleOrderStatuses](#possibleorderstatuses)- [summary](#summary)- [Methods](#methods)[contextMenuActions](#contextmenuactions)