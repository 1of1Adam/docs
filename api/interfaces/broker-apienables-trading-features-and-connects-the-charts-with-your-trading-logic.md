---
title: "Interface: IBrokerTerminal | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal"
extracted_at: "2025-06-22T09:30:13.066Z"
---

# Interface: IBrokerTerminal[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IBrokerTerminal

The Broker API is a key component that enables trading.
Its main purpose is to connect TradingView charts with your trading logic.
Refer to the [Core trading concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/) article for more information.
## Hierarchy

[`IBrokerCommon`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon)

[`IBrokerAccountInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo)

↳ **`IBrokerTerminal`**

## Methods
### accountManagerInfo
▸ **accountManagerInfo**(): [`AccountManagerInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountManagerInfo)

The library calls `accountManagerInfo` to get information required for building the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).

#### Returns
[`AccountManagerInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountManagerInfo)

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[accountManagerInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#accountmanagerinfo)

### accountsMetainfo
▸ **accountsMetainfo**(): `Promise`<[`AccountMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountMetainfo)>

The library calls `accountsMetainfo` to get a list of accounts for a particular user.
The method should return an array that contains an ID and name for each account.
Note that if `accountsMetainfo` returns an array containing more than one element, you should implement the [setCurrentAccount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo#setcurrentaccount) method.
Refer to [Multiple accounts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/multiple-accounts) for more information.
#### Returns
`Promise`<[`AccountMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountMetainfo)>

#### Inherited from
[IBrokerAccountInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo).[accountsMetainfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo#accountsmetainfo)

### cancelOrder
▸ **cancelOrder**(`orderId`): `Promise`<`void`>

The library calls `cancelOrder` to request canceling an order.
You should handle this request on your backend side and provide the library with a new order state. To do this, call the [IBrokerConnectionAdapterHost.orderUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) method right afterwards.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `orderId` | `string` | The ID of the order to cancel. ||

#### Returns
`Promise`<`void`>

### cancelOrders
▸ **cancelOrders**(`symbol`, `side`, `ordersIds`): `Promise`<`void`>

The library calls `cancelOrders` to request canceling multiple orders for a symbol.
You should handle this request on your backend side and provide the library with a new order states. To do this, call the [IBrokerConnectionAdapterHost.orderUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) method right afterwards.
`cancelOrders` is only called when users click the *CXL all* button in the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) widget.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | The symbol identifier. ||
| `side` | [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.Side) | An order side. ||
| `ordersIds` | `string` | IDs of the orders to cancel. The orders are selected based on the specified `symbol` and `side`. ||

#### Returns
`Promise`<`void`>

### chartContextMenuActions
▸ **chartContextMenuActions**(`context`, `options?`): `Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#actionmetainfo)>

The library calls `chartContextMenuActions` when users open the [context menu](https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu) on the chart.
This method also renders the *Trade* button in the context menu.
This method should return an array of [ActionMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#actionmetainfo) elements, each of them representing one context menu item.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `context` | [`TradeContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradeContext) | A context object passed by the library. ||
| `options?` | [`DefaultContextMenuActionsParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DefaultContextMenuActionsParams) | Default options for the context menu action parameters. ||

#### Returns
`Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#actionmetainfo)>

A promise that resolves to an array of [ActionMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#actionmetainfo), which may be empty. In that case, the *Trade* button will
be removed from the context menu.
#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[chartContextMenuActions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#chartcontextmenuactions)

### closeIndividualPosition
▸ **closeIndividualPosition**(`individualPositionId`, `amount?`, `confirmId?`): `Promise`<`void`>

The library calls `closeIndividualPosition` if the [BrokerConfigFlags.supportCloseIndividualPosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportcloseindividualposition) or [BrokerConfigFlags.supportPartialCloseIndividualPosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpartialcloseindividualposition) configuration flag is `true`.
`closeIndividualPosition` allows [closing an individual position](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#close-positions) by ID.
Note that the library expects you to call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.
Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).
#### Parameters

 **|Name** | **Type** | **Description** ||
| `individualPositionId` | `string` | The individual position ID. ||
| `amount?` | `number` | The amount is specified if `supportPartialCloseIndividualPosition` is `true` and the user wants to close only [part of the individual position](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#partial-closing). ||
| `confirmId?` | `string` | The ID of the confirmed close position preview. This parameter is passed if [`supportPreviewClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpreviewcloseposition) is `true`. ||

#### Returns
`Promise`<`void`>

### closePosition
▸ **closePosition**(`positionId`, `amount?`, `confirmId?`): `Promise`<`void`>

The library calls `closePosition` to request [closing a position](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#close-positions) by ID.
You should handle this request on your backend side and provide the library with a new position state. To do this, call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.
Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).
`closePosition` is only called if the [BrokerConfigFlags.supportClosePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportcloseposition) or [BrokerConfigFlags.supportPartialClosePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpartialcloseposition) configuration flag is `true`.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `positionId` | `string` | The position ID. ||
| `amount?` | `number` | The amount is specified if [`supportPartialClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpartialcloseposition) is `true` and the user wants to close only [part of the position](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#partial-closing). ||
| `confirmId?` | `string` | The ID of the confirmed close position preview. This parameter is passed if [`supportPreviewClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpreviewcloseposition) is `true`. ||

#### Returns
`Promise`<`void`>

### connectionStatus
▸ **connectionStatus**(): [`ConnectionStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ConnectionStatus)

Defines a connection status for the Broker API.
If any other value than `1` ("Connected") is returned, the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) will display an endless spinner instead of users' trading data.
If you want to handle other scenarios, for example when the status is disconnected, you need to manage this scenario within your implementation and use the [IBrokerConnectionAdapterHost.connectionStatusUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#connectionstatusupdate) method.
If the method is not implemented or returns a value other than `1`,
the following error will appear in the console: *Method connectionStatus is not properly implemented*.
#### Returns
[`ConnectionStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ConnectionStatus)

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[connectionStatus](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#connectionstatus)

### currentAccount
▸ **currentAccount**(): [`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#accountid)

The library calls `currentAccount` to get the current account's ID.

#### Returns
[`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#accountid)

#### Inherited from
[IBrokerAccountInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo).[currentAccount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo#currentaccount)

### editIndividualPositionBrackets
▸ **editIndividualPositionBrackets**(`individualPositionId`, `brackets`): `Promise`<`void`>

This method is called if the [BrokerConfigFlags.supportIndividualPositionBrackets](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportindividualpositionbrackets) configuration flag is on.
It displays a dialog that enables take-profit and stop-loss editing.
Note that the library expects you to call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `individualPositionId` | `string` | ID of existing individual position to be modified ||
| `brackets` | [`Brackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Brackets) | new Brackets to be set for the individual position ||

#### Returns
`Promise`<`void`>

### editPositionBrackets
▸ **editPositionBrackets**(`positionId`, `brackets`, `customFields?`): `Promise`<`void`>

The library calls `editPositionBrackets` if the [BrokerConfigFlags.supportPositionBrackets](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpositionbrackets) configuration flag is `true`.
It shows a dialog that enables take-profit and stop-loss editing.
Note that the library expects you to call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `positionId` | `string` | The ID of the existing position to be modified. ||
| `brackets` | [`Brackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Brackets) | New brackets to be set for the position. ||
| `customFields?` | [`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomInputFieldsValues) | Custom fields to display in the dialog. ||

#### Returns
`Promise`<`void`>

### executions
▸ **executions**(`symbol`): `Promise`<[`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Execution)>

The library calls `executions` to request executions for the specified symbol.
If you want executions to be displayed on the chart, set the [BrokerConfigFlags.supportExecutions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportexecutions) to `true`.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | The symbol identifier. ||

#### Returns
`Promise`<[`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Execution)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[executions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#executions)

### formatter
▸ **formatter**(`symbol`, `alignToMinMove`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

Provide a custom price formatter for the specified symbol.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||
| `alignToMinMove` | `boolean` | align formatted number to the minimum movement amount of the symbol ||

#### Returns
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[formatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#formatter)

### getOrderDialogOptions
▸ **getOrderDialogOptions**(`symbol`): `Promise`<[`OrderDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderDialogOptions)>

Implement this method if you want to [add custom fields](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#add-custom-fields) to the standard Order Ticket.

Use the `symbol` parameter to return customization options for a particular symbol.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`Promise`<[`OrderDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderDialogOptions)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[getOrderDialogOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#getorderdialogoptions)

### getPositionDialogOptions
▸ **getPositionDialogOptions**(`symbol`): `Promise`<[`PositionDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionDialogOptions)>

Implement this method if you want to customize the position dialog.

Use the `symbol` parameter to return customization options for a particular symbol.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`Promise`<[`PositionDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionDialogOptions)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[getPositionDialogOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#getpositiondialogoptions)

### getSymbolSpecificTradingOptions
▸ **getSymbolSpecificTradingOptions**(`symbol`): `Promise`<[`SymbolSpecificTradingOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolSpecificTradingOptions)>

Implement this method if you want to have custom options available for different symbols.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`Promise`<[`SymbolSpecificTradingOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolSpecificTradingOptions)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[getSymbolSpecificTradingOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#getsymbolspecifictradingoptions)

### individualPositions
▸ **individualPositions**(): `Promise`<[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IndividualPosition)>

Called by Trading Platform to request [individual positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
Required if the [BrokerConfigFlags.supportPositionNetting](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpositionnetting) flag is set to `true`.
#### Returns
`Promise`<[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IndividualPosition)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[individualPositions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#individualpositions)

### isTradable
▸ **isTradable**(`symbol`): `Promise`<`boolean` | [`IsTradableResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IsTradableResult)>

The library calls `isTradable` to check if a symbol can be traded.
If the method returns `false`, users will see the *Non-tradable symbol* message in the UI when creating orders.
You can also display a custom message with the reason why the symbol cannot be traded and the possible solution to resolve the issue.
To do this, return an `IsTradableResult` object.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | The symbol identifier. ||

#### Returns
`Promise`<`boolean` | [`IsTradableResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IsTradableResult)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[isTradable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#istradable)

### leverageInfo
▸ **leverageInfo**(`leverageInfoParams`): `Promise`<[`LeverageInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeverageInfo)>

This method is called to receive leverageInfo from the broker.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `leverageInfoParams` | [`LeverageInfoParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeverageInfoParams) | information about the specific symbol to provide leverage information for ||

#### Returns
`Promise`<[`LeverageInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeverageInfo)>

### modifyOrder
▸ **modifyOrder**(`order`, `confirmId?`): `Promise`<`void`>

The library calls `modifyOrder` to request modifying an existing order.
You should handle this request on your backend side and provide the library with a new order state. To do this, call the [IBrokerConnectionAdapterHost.orderUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) method right afterwards.
Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).
To enable an order preview before modification, set the [BrokerConfigFlags.supportModifyOrderPreview](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportmodifyorderpreview) configuration flag to `true`.
Refer to [Enable order preview](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-order-preview) for more information.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `order` | [`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#order) | Order information. ||
| `confirmId?` | `string` | The ID of the confirmed order. This parameter is passed if [`supportModifyOrderPreview`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportmodifyorderpreview) is `true`. ||

#### Returns
`Promise`<`void`>

### orders
▸ **orders**(): `Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#order)>

The library calls `orders` to request data on the user's active orders. This data is displayed on the *Orders and Positions* pages of the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#orders-and-positions).

#### Returns
`Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#order)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[orders](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#orders)

### ordersHistory
▸ **ordersHistory**(): `Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#order)>

The library calls `ordersHistory` to request orders history.
It is expected that returned orders will have a final status (`rejected`, `filled`, `cancelled`).
This method is only required when you set the [BrokerConfigFlags.supportOrdersHistory](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportordershistory) flag to `true`.
This flag adds the *History* page, where order history is displayed, to the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).
Refer to the [History](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#history) section for more information.
#### Returns
`Promise`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#order)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[ordersHistory](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#ordershistory)

### placeOrder
▸ **placeOrder**(`order`, `confirmId?`): `Promise`<[`PlaceOrderResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlaceOrderResult)>

The library calls `placeOrder` to request placing an order pre-filled with partial or complete information.
You should handle this request on your backend side. For more information, refer to [Order creation](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#1-order-creation).
To display an order preview before placing it, set [BrokerConfigFlags.supportPlaceOrderPreview](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportplaceorderpreview) to `true`.
Refer to [Enable order preview](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-order-preview) for more information.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `order` | [`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder) | Order information. ||
| `confirmId?` | `string` | The ID of the confirmed order. This parameter is passed if [`supportPlaceOrderPreview`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportplaceorderpreview) is `true`. ||

#### Returns
`Promise`<[`PlaceOrderResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlaceOrderResult)>

An object with the order ID.

### positions
▸ **positions**(): `Promise`<[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position)>

Called by Trading Platform to request [positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
Required if the [BrokerConfigFlags.supportPositions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpositions) flag is set to `true`.
#### Returns
`Promise`<[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[positions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#positions)

### previewLeverage
▸ **previewLeverage**(`leverageSetParams`): `Promise`<[`LeveragePreviewResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeveragePreviewResult)>

This method is called to receive [LeveragePreviewResult](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeveragePreviewResult) object which holds messages about the leverage value set by the user.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `leverageSetParams` | [`LeverageSetParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeverageSetParams) | `leverageSetParams` is an object similar to leverageInfoParams, but contains an additional `leverage: number` field, which holds the leverage value set by the user. ||

#### Returns
`Promise`<[`LeveragePreviewResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeveragePreviewResult)>

### previewOrder
▸ **previewOrder**(`order`): `Promise`<[`OrderPreviewResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderPreviewResult)>

The library calls `previewOrder` to show an order preview when a user clicks *Buy order* or *Modify order* in the Order Ticket.
To [enable order preview](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-order-preview), set the [BrokerConfigFlags.supportPlaceOrderPreview](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportplaceorderpreview) or [BrokerConfigFlags.supportModifyOrderPreview](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportmodifyorderpreview) configuration flag to `true`.
This method returns estimated commission, fees, margin, and other information for the order without it actually being placed.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `order` | [`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder) | Order information. ||

#### Returns
`Promise`<[`OrderPreviewResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderPreviewResult)>

### quantityFormatter
▸ **quantityFormatter**(`symbol`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

Provide a custom quantity formatter for the specified symbol.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[quantityFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#quantityformatter)

### reversePosition
▸ **reversePosition**(`positionId`): `Promise`<`void`>

This method is called if the [BrokerConfigFlags.supportNativeReversePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportnativereverseposition) configuration flag is on.
It allows reversing the position by ID.
Note that the library expects you to call the [IBrokerConnectionAdapterHost.positionUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method right afterwards.
Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).
#### Parameters

 **|Name** | **Type** | **Description** ||
| `positionId` | `string` | position ||

#### Returns
`Promise`<`void`>

### setCurrentAccount
▸ **setCurrentAccount**(`id`): `void`

The library calls `setCurrentAccount` when users switch accounts using the drop-down menu in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).
This method provides your backend server with the ID of the selected account.
Note that `setCurrentAccount` is required if [accountsMetainfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo#accountsmetainfo) returns an array containing more than one element.
Refer to [Multiple accounts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/multiple-accounts) for more information.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `id` | [`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#accountid) | The ID of the selected account. ||

#### Returns
`void`

#### Inherited from
[IBrokerAccountInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo).[setCurrentAccount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerAccountInfo#setcurrentaccount)

### setLeverage
▸ **setLeverage**(`leverageSetParams`): `Promise`<[`LeverageSetResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeverageSetResult)>

This method is called to send user's leverage value to the broker. The value should be verified and corrected on the broker's side if required, and sent back in the response.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `leverageSetParams` | [`LeverageSetParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeverageSetParams) | `leverageSetParams` is an object similar to leverageInfoParams, but contains an additional `leverage: number` field, which holds the leverage value set by the user. ||

#### Returns
`Promise`<[`LeverageSetResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LeverageSetResult)>

### spreadFormatter
▸ **spreadFormatter**(`symbol`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

Provide a custom spread formatter for the specified symbol.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[spreadFormatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#spreadformatter)

### subscribeEquity
▸ **subscribeEquity**(): `void`

The method should be implemented if you use the standard Order Ticket and support stop loss. Equity is used to calculate Risk in Percent.

Once this method is called the broker should provide equity (Balance + P/L) updates via [IBrokerConnectionAdapterHost.equityUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#equityupdate) method.

#### Returns
`void`

### subscribeMarginAvailable
▸ **subscribeMarginAvailable**(`symbol`): `void`

The method should be implemented if you use the standard Order Ticket and want to show the margin meter.

Once this method is called the broker should provide margin available updates via [IBrokerConnectionAdapterHost.marginAvailableUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#marginavailableupdate) method.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`void`

### subscribePipValue
▸ **subscribePipValue**(`symbol`): `void`

The method should be implemented if you use a standard Order Ticket.
`pipValues` is displayed in the Order info and it is used to calculate the Trade Value and risks.
If this method is not implemented then `pipValue` from the `symbolInfo` is used in the order panel/dialog.
Once this method is called the broker should provide `pipValue` updates via [IBrokerConnectionAdapterHost.pipValueUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#pipvalueupdate) method.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`void`

### symbolInfo
▸ **symbolInfo**(`symbol`): `Promise`<[`InstrumentInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.InstrumentInfo)>

The library calls `symbolInfo` to request symbol information for the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) and [Depth of Market widget](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market).

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | The symbol identifier. ||

#### Returns
`Promise`<[`InstrumentInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.InstrumentInfo)>

#### Inherited from
[IBrokerCommon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon).[symbolInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#symbolinfo)

### unsubscribeEquity
▸ **unsubscribeEquity**(): `void`

The method should be implemented if you use the standard Order Ticket and support stop loss.

Once this method is called the broker should stop providing equity updates.

#### Returns
`void`

### unsubscribeMarginAvailable
▸ **unsubscribeMarginAvailable**(`symbol`): `void`

The method should be implemented if you use the standard Order Ticket want to show the margin meter.

Once this method is called the broker should stop providing margin available updates.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`void`

### unsubscribePipValue
▸ **unsubscribePipValue**(`symbol`): `void`

The method should be implemented if you use a standard Order Ticket and implement `subscribePipValue`.

Once this method is called the broker should stop providing `pipValue` updates.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`void`