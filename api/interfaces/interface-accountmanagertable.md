---
title: "Interface: AccountManagerTable | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerTable"
extracted_at: "2025-06-22T09:53:09.638Z"
---

- [](/charting-library-docs/)- Interfaces- AccountManagerTableOn this page# Interface: AccountManagerTable[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).AccountManagerTable

Account Summary table meta-info
NOTE: make sure that you have a unique string `id` field in each row to identify it.
## Properties[​](#properties)
### changeDelegate[​](#changedelegate)
• changeDelegate: [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISubscription)<(`data`: ) => `void`>

This delegate is used to watch the data changes and update the table.
Pass new account manager data row by row to the `fire` method of the delegate.

### columns[​](#columns)
• columns: [`AccountManagerColumn`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountmanagercolumn)[]

Table columns

### deleteDelegate[​](#deletedelegate)
• `Optional` deleteDelegate: [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISubscription)<(`id`: `string`) => `void`>

This delegate is used to watch the data deletions and update the table.
Pass the id of the row that needs to be deleted to the `fire` method of the delegate.

### flags[​](#flags)
• `Optional` flags: [`AccountManagerTableFlags`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerTableFlags)

Option flags for the table.

### id[​](#id)
• id: `string`

Unique identifier of a table.

### initialSorting[​](#initialsorting)
• `Optional` initialSorting: [`SortingParameters`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SortingParameters)

Optional sorting of the table. If set, then the table will be sorted by these parameters, if the user has not enabled sorting by a specific column.

### title[​](#title)
• `Optional` title: `string`

Optional title of a table.

## Methods[​](#methods)
### getData[​](#getdata)
▸ getData(`paginationLastId?`): `Promise`<[]>

This function is used to request table data. It should return Promise (or Deferred) and resolve it with an array of data rows.

Each row is an object. Keys of this object are column names with the corresponding values.

There is a predefined field `isTotalRow` which can be used to mark a row that should be at the bottom of the table.

#### Parameters[​](#parameters)
NameTypeDescription`paginationLastId?``string` | `number`Last pagination id
#### Returns[​](#returns)
`Promise`<[]>

- [Properties](#properties)[changeDelegate](#changedelegate)- [columns](#columns)- [deleteDelegate](#deletedelegate)- [flags](#flags)- [id](#id)- [initialSorting](#initialsorting)- [title](#title)- [Methods](#methods)[getData](#getdata)