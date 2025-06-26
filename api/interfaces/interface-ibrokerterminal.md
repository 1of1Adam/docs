---
title: "Interface: IBrokerTerminal | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal"
extracted_at: "2025-06-22T09:54:36.393Z"
---

- [](/charting-library-docs/)- Interfaces- IBrokerTerminalOn this page# Interface: IBrokerTerminal[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IBrokerTerminal

The Broker API is a key component that enables trading.
Its main purpose is to connect TradingView charts with your trading logic.
Refer to the [Core trading concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/) article for more information.
## Hierarchy[​](#hierarchy)

[`IBrokerCommon`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon)

[`IBrokerAccountInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo)

↳ `IBrokerTerminal`

## Methods[​](#methods)
### accountManagerInfo[​](#accountmanagerinfo)
▸ accountManagerInfo(): [`AccountManagerInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerInfo)

The library calls `accountManagerInfo` to get information required for building the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).

#### Returns[​](#returns)
[`AccountManagerInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerInfo)

#### Inherited from[​](#inherited-from)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[accountManagerInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#accountmanagerinfo)

### accountsMetainfo[​](#accountsmetainfo)
▸ accountsMetainfo(): `Promise`<[`AccountMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountMetainfo)[]>

The library calls `accountsMetainfo` to get a list of accounts for a particular user.
The method should return an array that contains an ID and name for each account.
Note that if `accountsMetainfo` returns an array containing more than one element, you should implement the [setCurrentAccount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo#setcurrentaccount) method.
Refer to [Multiple accounts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/multiple-accounts) for more information.
#### Returns[​](#returns-1)
`Promise`<[`AccountMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountMetainfo)[]>

#### Inherited from[​](#inherited-from-1)
[IBrokerAccountInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo).[accountsMetainfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo#accountsmetainfo)

### cancelOrder[​](#cancelorder)
▸ cancelOrder(`orderId`): `Promise`<`void`>

The library calls `cancelOrder` to request canceling an order.
You should handle this request on your backend side and provide the library with a new order state. To do this, call the [IBrokerConnectionAdapterHost.orderUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#orderupdate) method right afterwards.
#### Parameters[​](#parameters)
NameTypeDescription`orderId``string`The ID of the order to cancel.
#### Returns[​](#returns-2)
`Promise`<`void`>

### cancelOrders[​](#cancelorders)
▸ cancelOrders(`symbol`, `side`, `ordersIds`): `Promise`<`void`>

The library calls `cancelOrders` to request canceling multiple orders for a symbol.
You should handle this request on your backend side and provide the library with a new order states. To do this, call the [IBrokerConnectionAdapterHost.orderUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#orderupdate) method right afterwards.
`cancelOrders` is only called when users click the CXL all button in the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) widget.

#### Parameters[​](#parameters-1)
NameTypeDescription`symbol``string`The symbol identifier.`side`[`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)An order side.`ordersIds``string`[]IDs of the orders to cancel. The orders are selected based on the specified `symbol` and `side`.
#### Returns[​](#returns-3)
`Promise`<`void`>

### chartContextMenuActions[​](#chartcontextmenuactions)
▸ chartContextMenuActions(`context`, `options?`): `Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]>

The library calls `chartContextMenuActions` when users open the [context menu](https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu) on the chart.
This method also renders the Trade button in the context menu.
This method should return an array of [ActionMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo) elements, each of them representing one context menu item.

#### Parameters[​](#parameters-2)
NameTypeDescription`context`[`TradeContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradeContext)A context object passed by the library.`options?`[`DefaultContextMenuActionsParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DefaultContextMenuActionsParams)Default options for the context menu action parameters.
#### Returns[​](#returns-4)
`Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]>

A promise that resolves to an array of [ActionMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo), which may be empty. In that case, the Trade button will
be removed from the context menu.
#### Inherited from[​](#inherited-from-2)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[chartContextMenuActions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#chartcontextmenuactions)

### closeIndividualPosition[​](#closeindividualposition)
▸ closeIndividualPosition(`individualPositionId`, `amount?`, `confirmId?`): `Promise`<`void`>

The library calls `closeIndividualPosition` if the [BrokerConfigFlags.supportCloseIndividualPosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportcloseindividualposition) or [BrokerConfigFlags.supportPartialCloseIndividualPosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportpartialcloseindividualposition) configuration flag is `true`.
`closeIndividualPosition` allows [closing an individual position](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#close-positions) by ID.
Note that the library expects you to call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.
Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).
#### Parameters[​](#parameters-3)
NameTypeDescription`individualPositionId``string`The individual position ID.`amount?``number`The amount is specified if `supportPartialCloseIndividualPosition` is `true` and the user wants to close only [part of the individual position](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#partial-closing).`confirmId?``string`The ID of the confirmed close position preview. This parameter is passed if [`supportPreviewClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpreviewcloseposition) is `true`.
#### Returns[​](#returns-5)
`Promise`<`void`>

### closePosition[​](#closeposition)
▸ closePosition(`positionId`, `amount?`, `confirmId?`): `Promise`<`void`>

The library calls `closePosition` to request [closing a position](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#close-positions) by ID.
You should handle this request on your backend side and provide the library with a new position state. To do this, call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.
Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).
`closePosition` is only called if the [BrokerConfigFlags.supportClosePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportcloseposition) or [BrokerConfigFlags.supportPartialClosePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportpartialcloseposition) configuration flag is `true`.

#### Parameters[​](#parameters-4)
NameTypeDescription`positionId``string`The position ID.`amount?``number`The amount is specified if [`supportPartialClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpartialcloseposition) is `true` and the user wants to close only [part of the position](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#partial-closing).`confirmId?``string`The ID of the confirmed close position preview. This parameter is passed if [`supportPreviewClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpreviewcloseposition) is `true`.
#### Returns[​](#returns-6)
`Promise`<`void`>

### connectionStatus[​](#connectionstatus)
▸ connectionStatus(): [`ConnectionStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.ConnectionStatus)

Defines a connection status for the Broker API.
If any other value than `1` ("Connected") is returned, the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) will display an endless spinner instead of users' trading data.
If you want to handle other scenarios, for example when the status is disconnected, you need to manage this scenario within your implementation and use the [IBrokerConnectionAdapterHost.connectionStatusUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#connectionstatusupdate) method.
If the method is not implemented or returns a value other than `1`,
the following error will appear in the console: Method connectionStatus is not properly implemented.
#### Returns[​](#returns-7)
[`ConnectionStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.ConnectionStatus)

#### Inherited from[​](#inherited-from-3)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[connectionStatus](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#connectionstatus)

### currentAccount[​](#currentaccount)
▸ currentAccount(): [`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountid)

The library calls `currentAccount` to get the current account's ID.

#### Returns[​](#returns-8)
[`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountid)

#### Inherited from[​](#inherited-from-4)
[IBrokerAccountInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo).[currentAccount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo#currentaccount)

### editIndividualPositionBrackets[​](#editindividualpositionbrackets)
▸ editIndividualPositionBrackets(`individualPositionId`, `brackets`): `Promise`<`void`>

This method is called if the [BrokerConfigFlags.supportIndividualPositionBrackets](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportindividualpositionbrackets) configuration flag is on.
It displays a dialog that enables take-profit and stop-loss editing.
Note that the library expects you to call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.

#### Parameters[​](#parameters-5)
NameTypeDescription`individualPositionId``string`ID of existing individual position to be modified`brackets`[`Brackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Brackets)new Brackets to be set for the individual position
#### Returns[​](#returns-9)
`Promise`<`void`>

### editPositionBrackets[​](#editpositionbrackets)
▸ editPositionBrackets(`positionId`, `brackets`, `customFields?`): `Promise`<`void`>

The library calls `editPositionBrackets` if the [BrokerConfigFlags.supportPositionBrackets](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportpositionbrackets) configuration flag is `true`.
It shows a dialog that enables take-profit and stop-loss editing.
Note that the library expects you to call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.

#### Parameters[​](#parameters-6)
NameTypeDescription`positionId``string`The ID of the existing position to be modified.`brackets`[`Brackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Brackets)New brackets to be set for the position.`customFields?`[`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldsValues)Custom fields to display in the dialog.
#### Returns[​](#returns-10)
`Promise`<`void`>

### executions[​](#executions)
▸ executions(`symbol`): `Promise`<[`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Execution)[]>

The library calls `executions` to request executions for the specified symbol.
If you want executions to be displayed on the chart, set the [BrokerConfigFlags.supportExecutions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportexecutions) to `true`.
#### Parameters[​](#parameters-7)
NameTypeDescription`symbol``string`The symbol identifier.
#### Returns[​](#returns-11)
`Promise`<[`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Execution)[]>

#### Inherited from[​](#inherited-from-5)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[executions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#executions)

### formatter[​](#formatter)
▸ formatter(`symbol`, `alignToMinMove`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Provide a custom price formatter for the specified symbol.

#### Parameters[​](#parameters-8)
NameTypeDescription`symbol``string`symbol identifier`alignToMinMove``boolean`align formatted number to the minimum movement amount of the symbol
#### Returns[​](#returns-12)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

#### Inherited from[​](#inherited-from-6)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[formatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#formatter)

### getOrderDialogOptions[​](#getorderdialogoptions)
▸ getOrderDialogOptions(`symbol`): `Promise`<[`OrderDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDialogOptions)>

Implement this method if you want to [add custom fields](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#add-custom-fields) to the standard Order Ticket.

Use the `symbol` parameter to return customization options for a particular symbol.

#### Parameters[​](#parameters-9)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-13)
`Promise`<[`OrderDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDialogOptions)>

#### Inherited from[​](#inherited-from-7)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[getOrderDialogOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#getorderdialogoptions)

### getPositionDialogOptions[​](#getpositiondialogoptions)
▸ getPositionDialogOptions(`symbol`): `Promise`<[`PositionDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionDialogOptions)>

Implement this method if you want to customize the position dialog.

Use the `symbol` parameter to return customization options for a particular symbol.

#### Parameters[​](#parameters-10)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-14)
`Promise`<[`PositionDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionDialogOptions)>

#### Inherited from[​](#inherited-from-8)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[getPositionDialogOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#getpositiondialogoptions)

### getSymbolSpecificTradingOptions[​](#getsymbolspecifictradingoptions)
▸ getSymbolSpecificTradingOptions(`symbol`): `Promise`<[`SymbolSpecificTradingOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolSpecificTradingOptions)>

Implement this method if you want to have custom options available for different symbols.

#### Parameters[​](#parameters-11)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-15)
`Promise`<[`SymbolSpecificTradingOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolSpecificTradingOptions)>

#### Inherited from[​](#inherited-from-9)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[getSymbolSpecificTradingOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#getsymbolspecifictradingoptions)

### individualPositions[​](#individualpositions)
▸ individualPositions(): `Promise`<[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)[]>

Called by Trading Platform to request [individual positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
Required if the [BrokerConfigFlags.supportPositionNetting](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportpositionnetting) flag is set to `true`.
#### Returns[​](#returns-16)
`Promise`<[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)[]>

#### Inherited from[​](#inherited-from-10)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[individualPositions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#individualpositions)

### isTradable[​](#istradable)
▸ isTradable(`symbol`): `Promise`<`boolean` | [`IsTradableResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IsTradableResult)>

The library calls `isTradable` to check if a symbol can be traded.
If the method returns `false`, users will see the Non-tradable symbol message in the UI when creating orders.
You can also display a custom message with the reason why the symbol cannot be traded and the possible solution to resolve the issue.
To do this, return an `IsTradableResult` object.
#### Parameters[​](#parameters-12)
NameTypeDescription`symbol``string`The symbol identifier.
#### Returns[​](#returns-17)
`Promise`<`boolean` | [`IsTradableResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IsTradableResult)>

#### Inherited from[​](#inherited-from-11)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[isTradable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#istradable)

### leverageInfo[​](#leverageinfo)
▸ leverageInfo(`leverageInfoParams`): `Promise`<[`LeverageInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfo)>

This method is called to receive leverageInfo from the broker.

#### Parameters[​](#parameters-13)
NameTypeDescription`leverageInfoParams`[`LeverageInfoParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams)information about the specific symbol to provide leverage information for
#### Returns[​](#returns-18)
`Promise`<[`LeverageInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfo)>

### modifyOrder[​](#modifyorder)
▸ modifyOrder(`order`, `confirmId?`): `Promise`<`void`>

The library calls `modifyOrder` to request modifying an existing order.
You should handle this request on your backend side and provide the library with a new order state. To do this, call the [IBrokerConnectionAdapterHost.orderUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#orderupdate) method right afterwards.
Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).
To enable an order preview before modification, set the [BrokerConfigFlags.supportModifyOrderPreview](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportmodifyorderpreview) configuration flag to `true`.
Refer to [Enable order preview](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-order-preview) for more information.
#### Parameters[​](#parameters-14)
NameTypeDescription`order`[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)Order information.`confirmId?``string`The ID of the confirmed order. This parameter is passed if [`supportModifyOrderPreview`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportmodifyorderpreview) is `true`.
#### Returns[​](#returns-19)
`Promise`<`void`>

### orders[​](#orders)
▸ orders(): `Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)[]>

The library calls `orders` to request data on the user's active orders. This data is displayed on the Orders and Positions pages of the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#orders-and-positions).

#### Returns[​](#returns-20)
`Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)[]>

#### Inherited from[​](#inherited-from-12)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[orders](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#orders)

### ordersHistory[​](#ordershistory)
▸ ordersHistory(): `Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)[]>

The library calls `ordersHistory` to request orders history.
It is expected that returned orders will have a final status (`rejected`, `filled`, `cancelled`).
This method is only required when you set the [BrokerConfigFlags.supportOrdersHistory](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportordershistory) flag to `true`.
This flag adds the History page, where order history is displayed, to the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).
Refer to the [History](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#history) section for more information.
#### Returns[​](#returns-21)
`Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)[]>

#### Inherited from[​](#inherited-from-13)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[ordersHistory](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#ordershistory)

### placeOrder[​](#placeorder)
▸ placeOrder(`order`, `confirmId?`): `Promise`<[`PlaceOrderResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlaceOrderResult)>

The library calls `placeOrder` to request placing an order pre-filled with partial or complete information.
You should handle this request on your backend side. For more information, refer to [Order creation](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#1-order-creation).
To display an order preview before placing it, set [BrokerConfigFlags.supportPlaceOrderPreview](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportplaceorderpreview) to `true`.
Refer to [Enable order preview](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-order-preview) for more information.
#### Parameters[​](#parameters-15)
NameTypeDescription`order`[`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PreOrder)Order information.`confirmId?``string`The ID of the confirmed order. This parameter is passed if [`supportPlaceOrderPreview`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportplaceorderpreview) is `true`.
#### Returns[​](#returns-22)
`Promise`<[`PlaceOrderResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlaceOrderResult)>

An object with the order ID.

### positions[​](#positions)
▸ positions(): `Promise`<[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position)[]>

Called by Trading Platform to request [positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
Required if the [BrokerConfigFlags.supportPositions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportpositions) flag is set to `true`.
#### Returns[​](#returns-23)
`Promise`<[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position)[]>

#### Inherited from[​](#inherited-from-14)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[positions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#positions)

### previewLeverage[​](#previewleverage)
▸ previewLeverage(`leverageSetParams`): `Promise`<[`LeveragePreviewResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeveragePreviewResult)>

This method is called to receive [LeveragePreviewResult](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeveragePreviewResult) object which holds messages about the leverage value set by the user.

#### Parameters[​](#parameters-16)
NameTypeDescription`leverageSetParams`[`LeverageSetParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageSetParams)`leverageSetParams` is an object similar to leverageInfoParams, but contains an additional `leverage: number` field, which holds the leverage value set by the user.
#### Returns[​](#returns-24)
`Promise`<[`LeveragePreviewResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeveragePreviewResult)>

### previewOrder[​](#previeworder)
▸ previewOrder(`order`): `Promise`<[`OrderPreviewResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderPreviewResult)>

The library calls `previewOrder` to show an order preview when a user clicks Buy order or Modify order in the Order Ticket.
To [enable order preview](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-order-preview), set the [BrokerConfigFlags.supportPlaceOrderPreview](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportplaceorderpreview) or [BrokerConfigFlags.supportModifyOrderPreview](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportmodifyorderpreview) configuration flag to `true`.
This method returns estimated commission, fees, margin, and other information for the order without it actually being placed.

#### Parameters[​](#parameters-17)
NameTypeDescription`order`[`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PreOrder)Order information.
#### Returns[​](#returns-25)
`Promise`<[`OrderPreviewResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderPreviewResult)>

### quantityFormatter[​](#quantityformatter)
▸ quantityFormatter(`symbol`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Provide a custom quantity formatter for the specified symbol.

#### Parameters[​](#parameters-18)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-26)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

#### Inherited from[​](#inherited-from-15)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[quantityFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#quantityformatter)

### reversePosition[​](#reverseposition)
▸ reversePosition(`positionId`): `Promise`<`void`>

This method is called if the [BrokerConfigFlags.supportNativeReversePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportnativereverseposition) configuration flag is on.
It allows reversing the position by ID.
Note that the library expects you to call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.
Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).
#### Parameters[​](#parameters-19)
NameTypeDescription`positionId``string`position
#### Returns[​](#returns-27)
`Promise`<`void`>

### setCurrentAccount[​](#setcurrentaccount)
▸ setCurrentAccount(`id`): `void`

The library calls `setCurrentAccount` when users switch accounts using the drop-down menu in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).
This method provides your backend server with the ID of the selected account.
Note that `setCurrentAccount` is required if [accountsMetainfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo#accountsmetainfo) returns an array containing more than one element.
Refer to [Multiple accounts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/multiple-accounts) for more information.
#### Parameters[​](#parameters-20)
NameTypeDescription`id`[`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountid)The ID of the selected account.
#### Returns[​](#returns-28)
`void`

#### Inherited from[​](#inherited-from-16)
[IBrokerAccountInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo).[setCurrentAccount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo#setcurrentaccount)

### setLeverage[​](#setleverage)
▸ setLeverage(`leverageSetParams`): `Promise`<[`LeverageSetResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageSetResult)>

This method is called to send user's leverage value to the broker. The value should be verified and corrected on the broker's side if required, and sent back in the response.

#### Parameters[​](#parameters-21)
NameTypeDescription`leverageSetParams`[`LeverageSetParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageSetParams)`leverageSetParams` is an object similar to leverageInfoParams, but contains an additional `leverage: number` field, which holds the leverage value set by the user.
#### Returns[​](#returns-29)
`Promise`<[`LeverageSetResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageSetResult)>

### spreadFormatter[​](#spreadformatter)
▸ spreadFormatter(`symbol`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Provide a custom spread formatter for the specified symbol.

#### Parameters[​](#parameters-22)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-30)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

#### Inherited from[​](#inherited-from-17)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[spreadFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#spreadformatter)

### subscribeEquity[​](#subscribeequity)
▸ subscribeEquity(): `void`

The method should be implemented if you use the standard Order Ticket and support stop loss. Equity is used to calculate Risk in Percent.

Once this method is called the broker should provide equity (Balance + P/L) updates via [IBrokerConnectionAdapterHost.equityUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#equityupdate) method.

#### Returns[​](#returns-31)
`void`

### subscribeMarginAvailable[​](#subscribemarginavailable)
▸ subscribeMarginAvailable(`symbol`): `void`

The method should be implemented if you use the standard Order Ticket and want to show the margin meter.

Once this method is called the broker should provide margin available updates via [IBrokerConnectionAdapterHost.marginAvailableUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#marginavailableupdate) method.

#### Parameters[​](#parameters-23)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-32)
`void`

### subscribePipValue[​](#subscribepipvalue)
▸ subscribePipValue(`symbol`): `void`

The method should be implemented if you use a standard Order Ticket.
`pipValues` is displayed in the Order info and it is used to calculate the Trade Value and risks.
If this method is not implemented then `pipValue` from the `symbolInfo` is used in the order panel/dialog.
Once this method is called the broker should provide `pipValue` updates via [IBrokerConnectionAdapterHost.pipValueUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#pipvalueupdate) method.

#### Parameters[​](#parameters-24)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-33)
`void`

### symbolInfo[​](#symbolinfo)
▸ symbolInfo(`symbol`): `Promise`<[`InstrumentInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.InstrumentInfo)>

The library calls `symbolInfo` to request symbol information for the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) and [Depth of Market widget](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market).

#### Parameters[​](#parameters-25)
NameTypeDescription`symbol``string`The symbol identifier.
#### Returns[​](#returns-34)
`Promise`<[`InstrumentInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.InstrumentInfo)>

#### Inherited from[​](#inherited-from-18)
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon).[symbolInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#symbolinfo)

### unsubscribeEquity[​](#unsubscribeequity)
▸ unsubscribeEquity(): `void`

The method should be implemented if you use the standard Order Ticket and support stop loss.

Once this method is called the broker should stop providing equity updates.

#### Returns[​](#returns-35)
`void`

### unsubscribeMarginAvailable[​](#unsubscribemarginavailable)
▸ unsubscribeMarginAvailable(`symbol`): `void`

The method should be implemented if you use the standard Order Ticket want to show the margin meter.

Once this method is called the broker should stop providing margin available updates.

#### Parameters[​](#parameters-26)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-36)
`void`

### unsubscribePipValue[​](#unsubscribepipvalue)
▸ unsubscribePipValue(`symbol`): `void`

The method should be implemented if you use a standard Order Ticket and implement `subscribePipValue`.

Once this method is called the broker should stop providing `pipValue` updates.

#### Parameters[​](#parameters-27)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-37)
`void`

- [Hierarchy](#hierarchy)- [Methods](#methods)[accountManagerInfo](#accountmanagerinfo)- [accountsMetainfo](#accountsmetainfo)- [cancelOrder](#cancelorder)- [cancelOrders](#cancelorders)- [chartContextMenuActions](#chartcontextmenuactions)- [closeIndividualPosition](#closeindividualposition)- [closePosition](#closeposition)- [connectionStatus](#connectionstatus)- [currentAccount](#currentaccount)- [editIndividualPositionBrackets](#editindividualpositionbrackets)- [editPositionBrackets](#editpositionbrackets)- [executions](#executions)- [formatter](#formatter)- [getOrderDialogOptions](#getorderdialogoptions)- [getPositionDialogOptions](#getpositiondialogoptions)- [getSymbolSpecificTradingOptions](#getsymbolspecifictradingoptions)- [individualPositions](#individualpositions)- [isTradable](#istradable)- [leverageInfo](#leverageinfo)- [modifyOrder](#modifyorder)- [orders](#orders)- [ordersHistory](#ordershistory)- [placeOrder](#placeorder)- [positions](#positions)- [previewLeverage](#previewleverage)- [previewOrder](#previeworder)- [quantityFormatter](#quantityformatter)- [reversePosition](#reverseposition)- [setCurrentAccount](#setcurrentaccount)- [setLeverage](#setleverage)- [spreadFormatter](#spreadformatter)- [subscribeEquity](#subscribeequity)- [subscribeMarginAvailable](#subscribemarginavailable)- [subscribePipValue](#subscribepipvalue)- [symbolInfo](#symbolinfo)- [unsubscribeEquity](#unsubscribeequity)- [unsubscribeMarginAvailable](#unsubscribemarginavailable)- [unsubscribePipValue](#unsubscribepipvalue)