---
title: "Interface: IBrokerCommon | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon"
extracted_at: "2025-06-22T09:54:28.588Z"
---

- [](/charting-library-docs/)- Interfaces- IBrokerCommonOn this page# Interface: IBrokerCommon[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IBrokerCommon

## Hierarchy[​](#hierarchy)

`IBrokerCommon`

↳ [`IBrokerTerminal`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal)

## Methods[​](#methods)
### accountManagerInfo[​](#accountmanagerinfo)
▸ accountManagerInfo(): [`AccountManagerInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerInfo)

The library calls `accountManagerInfo` to get information required for building the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).

#### Returns[​](#returns)
[`AccountManagerInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerInfo)

### chartContextMenuActions[​](#chartcontextmenuactions)
▸ chartContextMenuActions(`context`, `options?`): `Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]>

The library calls `chartContextMenuActions` when users open the [context menu](https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu) on the chart.
This method also renders the Trade button in the context menu.
This method should return an array of [ActionMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo) elements, each of them representing one context menu item.

#### Parameters[​](#parameters)
NameTypeDescription`context`[`TradeContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradeContext)A context object passed by the library.`options?`[`DefaultContextMenuActionsParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DefaultContextMenuActionsParams)Default options for the context menu action parameters.
#### Returns[​](#returns-1)
`Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]>

A promise that resolves to an array of [ActionMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo), which may be empty. In that case, the Trade button will
be removed from the context menu.

### connectionStatus[​](#connectionstatus)
▸ connectionStatus(): [`ConnectionStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.ConnectionStatus)

Defines a connection status for the Broker API.
If any other value than `1` ("Connected") is returned, the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) will display an endless spinner instead of users' trading data.
If you want to handle other scenarios, for example when the status is disconnected, you need to manage this scenario within your implementation and use the [IBrokerConnectionAdapterHost.connectionStatusUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#connectionstatusupdate) method.
If the method is not implemented or returns a value other than `1`,
the following error will appear in the console: Method connectionStatus is not properly implemented.
#### Returns[​](#returns-2)
[`ConnectionStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.ConnectionStatus)

### executions[​](#executions)
▸ executions(`symbol`): `Promise`<[`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Execution)[]>

The library calls `executions` to request executions for the specified symbol.
If you want executions to be displayed on the chart, set the [BrokerConfigFlags.supportExecutions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportexecutions) to `true`.
#### Parameters[​](#parameters-1)
NameTypeDescription`symbol``string`The symbol identifier.
#### Returns[​](#returns-3)
`Promise`<[`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Execution)[]>

### formatter[​](#formatter)
▸ formatter(`symbol`, `alignToMinMove`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Provide a custom price formatter for the specified symbol.

#### Parameters[​](#parameters-2)
NameTypeDescription`symbol``string`symbol identifier`alignToMinMove``boolean`align formatted number to the minimum movement amount of the symbol
#### Returns[​](#returns-4)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

### getOrderDialogOptions[​](#getorderdialogoptions)
▸ getOrderDialogOptions(`symbol`): `Promise`<[`OrderDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDialogOptions)>

Implement this method if you want to [add custom fields](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#add-custom-fields) to the standard Order Ticket.

Use the `symbol` parameter to return customization options for a particular symbol.

#### Parameters[​](#parameters-3)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-5)
`Promise`<[`OrderDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDialogOptions)>

### getPositionDialogOptions[​](#getpositiondialogoptions)
▸ getPositionDialogOptions(`symbol`): `Promise`<[`PositionDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionDialogOptions)>

Implement this method if you want to customize the position dialog.

Use the `symbol` parameter to return customization options for a particular symbol.

#### Parameters[​](#parameters-4)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-6)
`Promise`<[`PositionDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionDialogOptions)>

### getSymbolSpecificTradingOptions[​](#getsymbolspecifictradingoptions)
▸ getSymbolSpecificTradingOptions(`symbol`): `Promise`<[`SymbolSpecificTradingOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolSpecificTradingOptions)>

Implement this method if you want to have custom options available for different symbols.

#### Parameters[​](#parameters-5)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-7)
`Promise`<[`SymbolSpecificTradingOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolSpecificTradingOptions)>

### individualPositions[​](#individualpositions)
▸ individualPositions(): `Promise`<[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)[]>

Called by Trading Platform to request [individual positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
Required if the [BrokerConfigFlags.supportPositionNetting](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportpositionnetting) flag is set to `true`.
#### Returns[​](#returns-8)
`Promise`<[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)[]>

### isTradable[​](#istradable)
▸ isTradable(`symbol`): `Promise`<`boolean` | [`IsTradableResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IsTradableResult)>

The library calls `isTradable` to check if a symbol can be traded.
If the method returns `false`, users will see the Non-tradable symbol message in the UI when creating orders.
You can also display a custom message with the reason why the symbol cannot be traded and the possible solution to resolve the issue.
To do this, return an `IsTradableResult` object.
#### Parameters[​](#parameters-6)
NameTypeDescription`symbol``string`The symbol identifier.
#### Returns[​](#returns-9)
`Promise`<`boolean` | [`IsTradableResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IsTradableResult)>

### orders[​](#orders)
▸ orders(): `Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)[]>

The library calls `orders` to request data on the user's active orders. This data is displayed on the Orders and Positions pages of the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#orders-and-positions).

#### Returns[​](#returns-10)
`Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)[]>

### ordersHistory[​](#ordershistory)
▸ ordersHistory(): `Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)[]>

The library calls `ordersHistory` to request orders history.
It is expected that returned orders will have a final status (`rejected`, `filled`, `cancelled`).
This method is only required when you set the [BrokerConfigFlags.supportOrdersHistory](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportordershistory) flag to `true`.
This flag adds the History page, where order history is displayed, to the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).
Refer to the [History](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#history) section for more information.
#### Returns[​](#returns-11)
`Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)[]>

### positions[​](#positions)
▸ positions(): `Promise`<[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position)[]>

Called by Trading Platform to request [positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
Required if the [BrokerConfigFlags.supportPositions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportpositions) flag is set to `true`.
#### Returns[​](#returns-12)
`Promise`<[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position)[]>

### quantityFormatter[​](#quantityformatter)
▸ quantityFormatter(`symbol`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Provide a custom quantity formatter for the specified symbol.

#### Parameters[​](#parameters-7)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-13)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

### spreadFormatter[​](#spreadformatter)
▸ spreadFormatter(`symbol`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Provide a custom spread formatter for the specified symbol.

#### Parameters[​](#parameters-8)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-14)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

### symbolInfo[​](#symbolinfo)
▸ symbolInfo(`symbol`): `Promise`<[`InstrumentInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.InstrumentInfo)>

The library calls `symbolInfo` to request symbol information for the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) and [Depth of Market widget](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market).

#### Parameters[​](#parameters-9)
NameTypeDescription`symbol``string`The symbol identifier.
#### Returns[​](#returns-15)
`Promise`<[`InstrumentInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.InstrumentInfo)>

- [Hierarchy](#hierarchy)- [Methods](#methods)[accountManagerInfo](#accountmanagerinfo)- [chartContextMenuActions](#chartcontextmenuactions)- [connectionStatus](#connectionstatus)- [executions](#executions)- [formatter](#formatter)- [getOrderDialogOptions](#getorderdialogoptions)- [getPositionDialogOptions](#getpositiondialogoptions)- [getSymbolSpecificTradingOptions](#getsymbolspecifictradingoptions)- [individualPositions](#individualpositions)- [isTradable](#istradable)- [orders](#orders)- [ordersHistory](#ordershistory)- [positions](#positions)- [quantityFormatter](#quantityformatter)- [spreadFormatter](#spreadformatter)- [symbolInfo](#symbolinfo)