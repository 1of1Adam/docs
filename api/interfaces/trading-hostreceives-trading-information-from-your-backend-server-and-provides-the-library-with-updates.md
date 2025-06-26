---
title: "Interface: IBrokerConnectionAdapterHost | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost"
extracted_at: "2025-06-22T09:30:15.488Z"
---

# Interface: IBrokerConnectionAdapterHost[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IBrokerConnectionAdapterHost

The Trading Host is an API for interaction between the Broker API and the library code related to trading.
Its main purpose is to receive information from your backend server where trading logic is implemented and provide updates to the library.
Refer to the [Core trading concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/) article for more information.
## Properties
### factory
• **factory**: [`IBrokerConnectionAdapterFactory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterFactory)

Broker Connection Adapter Factory object

## Methods
### activateBottomWidget
▸ **activateBottomWidget**(): `Promise`<`void`>

#### Returns
`Promise`<`void`>

**`Deprecated`**

This method will be removed from the library in the next major version. Please use [setAccountManagerVisibilityMode](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#setaccountmanagervisibilitymode) instead.
Activate bottom widget

### connectionStatusUpdate
▸ **connectionStatusUpdate**(`status`, `info?`): `void`

Triggers a connection status update throughout the broker by reinvoking [IBrokerCommon.connectionStatus](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#connectionstatus).

#### Parameters

 **|Name** | **Type** | **Description** ||
| `status` | [`ConnectionStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ConnectionStatus) | new connection status to propagate internally to the host ||
| `info?` | [`DisconnectionInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DisconnectionInfo) | additional information to provide when entering a disconnected status ||

#### Returns
`void`

### cryptoBalanceUpdate
▸ **cryptoBalanceUpdate**(`symbol`, `balance`): `void`

Call this method when a broker connection has received a balance update.
This method is required by the crypto Order Ticket.
It should be implemented when the [BrokerConfigFlags.supportBalances](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportbalances) flag is set to `true` in [SingleBrokerMetaInfo.configFlags](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SingleBrokerMetaInfo#configflags).
#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol ID ||
| `balance` | [`CryptoBalance`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CryptoBalance) | updated crypto balance ||

#### Returns
`void`

### currentAccountUpdate
▸ **currentAccountUpdate**(): `void`

Call this method when user account has been changed synchronously. The terminal will re-request all displayed information.

#### Returns
`void`

### defaultContextMenuActions
▸ **defaultContextMenuActions**(`context`, `params?`): `Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#actionmetainfo)>

Provides default buy/sell, show properties actions to be returned as a default by [IBrokerCommon.chartContextMenuActions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerCommon#chartcontextmenuactions).

#### Parameters

 **|Name** | **Type** | **Description** ||
| `context` | [`TradeContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradeContext) | trade context ||
| `params?` | [`DefaultContextMenuActionsParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DefaultContextMenuActionsParams) | optional parameters ||

#### Returns
`Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#actionmetainfo)>

### defaultDropdownMenuActions
▸ **defaultDropdownMenuActions**(`options?`): [`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#actionmetainfo)

Provides default dropdown list of actions. You can use default actions in IBrokerConnectionAdapterHost.setButtonDropdownActions

#### Parameters

 **|Name** | **Type** | **Description** ||
| `options?` | `Partial`<[`DefaultDropdownActionsParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DefaultDropdownActionsParams)> | options for the dropdown menu actions ||

#### Returns
[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#actionmetainfo)

### defaultFormatter
▸ **defaultFormatter**(`symbol`, `alignToMinMove`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

Generates and returns the default value formatter for the symbol

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||
| `alignToMinMove` | `boolean` | whether the formatted number should be aligned to minimum movement for the symbol ||

#### Returns
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

### domPanelVisibility
▸ **domPanelVisibility**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Returns whether DOM Panel is visible or not.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

### domUpdate
▸ **domUpdate**(`symbol`, `equity`): `void`

Update the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) data for a specified symbol.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||
| `equity` | [`DOMData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DOMData) | Depth of Market data ||

#### Returns
`void`

### equityUpdate
▸ **equityUpdate**(`equity`): `void`

Call this method when a broker connection has received an equity update. This method is required by the standard Order Ticket to calculate risks.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `equity` | `number` | updated equity ||

#### Returns
`void`

### executionUpdate
▸ **executionUpdate**(`execution`): `void`

Call this method when an execution is added.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `execution` | [`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Execution) | execution which was added ||

#### Returns
`void`

### getAccountManagerVisibilityMode
▸ **getAccountManagerVisibilityMode**(): [`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`BottomWidgetBarMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.BottomWidgetBarMode)>

Method to retrieve the current visibility mode of the Account Manager.

#### Returns
[`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`BottomWidgetBarMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.BottomWidgetBarMode)>

### getOrderTicketSetting
▸ **getOrderTicketSetting**<`K`>(`settingName`): `Promise`<[`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderTicketSettings)[`K`]>

Retrieves the current value for a specified [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) setting in the ellipsis menu.

#### Type parameters

 **|Name** | **Type** | **Description** ||
| `K` | extends keyof [`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderTicketSettings) | A key of the OrderTicketSettings type. ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `settingName` | `K` | The name of the Order Ticket setting. ||

#### Returns
`Promise`<[`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderTicketSettings)[`K`]>

A promise that resolves with the value of the specified setting.

### getQty
▸ **getQty**(`symbol`): `Promise`<`number`>

Returns the quantity for a given symbol.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol ||

#### Returns
`Promise`<`number`>

- quantity for the given symbol

### getSymbolMinTick
▸ **getSymbolMinTick**(`symbol`): `Promise`<`number`>

Returns symbol `minTick`.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||

#### Returns
`Promise`<`number`>

### individualPositionPLUpdate
▸ **individualPositionPLUpdate**(`individualPositionId`, `pl`): `void`

Call this method when a broker connection has received an individual position [profit and loss](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#provide-profit-and-loss) update.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `individualPositionId` | `string` | ID of the individual position ||
| `pl` | `number` | updated profit / loss for the individual position ||

#### Returns
`void`

### individualPositionPartialUpdate
▸ **individualPositionPartialUpdate**(`id`, `changes`): `void`

Call this method when an individual position has not changed, but fields that you added to the individual position object to display in the Account Manager have changed.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `id` | `string` | ID of the updated individual position ||
| `changes` | `Partial`<[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IndividualPosition)> | changes to the individual position object ||

#### Returns
`void`

### individualPositionUpdate
▸ **individualPositionUpdate**(`individualPosition`, `isHistoryUpdate?`): `void`

Call this method when an individual position is added or changed.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `individualPosition` | [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IndividualPosition) | updated individual position ||
| `isHistoryUpdate?` | `boolean` | whether the change is a history update ||

#### Returns
`void`

### individualPositionsFullUpdate
▸ **individualPositionsFullUpdate**(): `void`

Call this method to clear the current cache for individual positions and notify the chart that it needs to request individual positions again.

#### Returns
`void`

### marginAvailableUpdate
▸ **marginAvailableUpdate**(`marginAvailable`): `void`

Call this method when a broker connection has received a margin available update.
This method is required by the standard Order Ticket to display the margin meter.
This method should be used when [BrokerConfigFlags.supportMargin](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportmargin) is set to `true` in [SingleBrokerMetaInfo.configFlags](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SingleBrokerMetaInfo#configflags).
The Trading Platform subscribes to margin available updates using [IBrokerTerminal.subscribeMarginAvailable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#subscribemarginavailable).
#### Parameters

 **|Name** | **Type** | **Description** ||
| `marginAvailable` | `number` | updated available margin ||

#### Returns
`void`

### numericFormatter
▸ **numericFormatter**(`decimalPlaces?`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

Generates and returns a number formatter with the desired decimal places

#### Parameters

 **|Name** | **Type** | **Description** ||
| `decimalPlaces?` | `number` | decimal places ||

#### Returns
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

### orderPanelVisibility
▸ **orderPanelVisibility**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Returns whether the order panel is visible or not.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

### orderPartialUpdate
▸ **orderPartialUpdate**(`id`, `orderChanges`): `void`

Call this method when an order is not changed, but the fields that you added to the order object to display in the Account Manager have changed.
It should be used only if you want to display custom fields in the Account Manager.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `id` | `string` | order id ||
| `orderChanges` | `Partial`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#order)> | changes made to the order object ||

#### Returns
`void`

### orderUpdate
▸ **orderUpdate**(`order`): `void`

Call this method to notify the chart that it needs to update information after an order is added or changed.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `order` | [`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#order) | order which was added or changed ||

#### Returns
`void`

### ordersFullUpdate
▸ **ordersFullUpdate**(): `void`

Call this method to clear the current cache for orders and notify the chart that it needs to request orders again.

#### Returns
`void`

### patchConfig
▸ **patchConfig**(`config`): `void`

Patch changes into the current broker configuration

#### Parameters

 **|Name** | **Type** | **Description** ||
| `config` | `Partial`<[`BrokerConfigFlags`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags)> | partial configuration changes to apply ||

#### Returns
`void`

### pipValueUpdate
▸ **pipValueUpdate**(`symbol`, `pipValues`): `void`

Call this method when a broker connection has a `pipValue` update.
The library subscribes to `pipValue` updates using [IBrokerTerminal.subscribePipValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#subscribepipvalue).
#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol with updated pip values ||
| `pipValues` | [`PipValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PipValues) | updated pip values ||

#### Returns
`void`

### plUpdate
▸ **plUpdate**(`positionId`, `pl`): `void`

Call this method when a broker connection has received a [profit and loss](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#provide-profit-and-loss) update.
Use this method when the [BrokerConfigFlags.supportPLUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportplupdate) flag is set to `true` in [SingleBrokerMetaInfo.configFlags](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SingleBrokerMetaInfo#configflags).
#### Parameters

 **|Name** | **Type** | **Description** ||
| `positionId` | `string` | ID of the position ||
| `pl` | `number` | updated profit / loss value ||

#### Returns
`void`

### positionPartialUpdate
▸ **positionPartialUpdate**(`id`, `positionChanges`): `void`

Call this method when a position is not changed, but the fields that you added to the position object to display in the Account Manager have changed.
It should be used only if you want to display custom fields in the Account Manager.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `id` | `string` | id of the position ||
| `positionChanges` | `Partial`<[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position)> | changes to the position object ||

#### Returns
`void`

### positionUpdate
▸ **positionUpdate**(`position`, `isHistoryUpdate?`): `void`

Call this method when a position is added or changed.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `position` | [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) | position which was added or changed ||
| `isHistoryUpdate?` | `boolean` | whether the change is a history update ||

#### Returns
`void`

### positionsFullUpdate
▸ **positionsFullUpdate**(): `void`

Call this method to clear the current cache for positions and notify the chart that it needs to request positions again.

#### Returns
`void`

### quantityFormatter
▸ **quantityFormatter**(`decimalPlaces?`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

Generates and returns a quantity formatter with the desired decimal places

#### Parameters

 **|Name** | **Type** | **Description** ||
| `decimalPlaces?` | `number` | decimal places ||

#### Returns
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)>

### realtimeUpdate
▸ **realtimeUpdate**(`symbol`, `data`): `void`

Trading quote realtime update

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol identifier ||
| `data` | [`TradingQuotes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingQuotes) | realtime updated data for the symbol quotes ||

#### Returns
`void`

### sellBuyButtonsVisibility
▸ **sellBuyButtonsVisibility**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Returns whether the buy/sell buttons are visible or not.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

### setAccountManagerVisibilityMode
▸ **setAccountManagerVisibilityMode**(`mode`): `void`

Method to set a new visibility mode for the Account Manager.

#### Parameters

 **|Name** | **Type** ||
| `mode` | [`BottomWidgetBarMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.BottomWidgetBarMode) ||

#### Returns
`void`

### setDurations
▸ **setDurations**(`durations`): `void`

Set expiration durations

#### Parameters

 **|Name** | **Type** | **Description** ||
| `durations` | [`OrderDurationMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderDurationMetaInfo) | Expiration options for orders ||

#### Returns
`void`

### setOrderTicketSetting
▸ **setOrderTicketSetting**<`K`>(`settingName`, `value`): `Promise`<`void`>

Updates the value of a specified [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) setting in the ellipsis menu.

#### Type parameters

 **|Name** | **Type** | **Description** ||
| `K` | extends keyof [`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderTicketSettings) | A key of OrderTicketSettings type. ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `settingName` | `K` | The name of the Order Ticket setting to be updated. ||
| `value` | [`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderTicketSettings)[`K`] | The new value to be assigned to the setting. ||

#### Returns
`Promise`<`void`>

A promise that resolves when the setting is successfully updated.

### setQty
▸ **setQty**(`symbol`, `quantity`): `void`

Sets the quantity for a given symbol.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol ||
| `quantity` | `number` | quantity to update ||

#### Returns
`void`

### showCancelBracketsDialog
▸ **showCancelBracketsDialog**(`orderId`, `handler`): `Promise`<`void`>

Shows the cancel brackets dialog

#### Parameters

 **|Name** | **Type** | **Description** ||
| `orderId` | `string` | id of order ||
| `handler` | () => `Promise`<`void`> | cancel brackets confirmation handler (called when brackets should be cancelled) ||

#### Returns
`Promise`<`void`>

### showCancelMultipleBracketsDialog
▸ **showCancelMultipleBracketsDialog**(`orderId`, `handler`): `Promise`<`void`>

Shows the cancel brackets dialog for multiple brackets

#### Parameters

 **|Name** | **Type** | **Description** ||
| `orderId` | `string` | id of order ||
| `handler` | () => `Promise`<`void`> | cancel brackets confirmation handler (called when brackets should be cancelled) ||

#### Returns
`Promise`<`void`>

### showCancelMultipleOrdersDialog
▸ **showCancelMultipleOrdersDialog**(`symbol`, `side`, `qty`, `handler`): `Promise`<`void`>

Shows the cancel Order Ticket for multiple orders

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol for which to cancel orders ||
| `side` | [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.Side) | side of the order ||
| `qty` | `number` | quantity of the order ||
| `handler` | () => `Promise`<`void`> | cancel orders confirmation handler (called when orders should be cancelled) ||

#### Returns
`Promise`<`void`>

### showCancelOrderDialog
▸ **showCancelOrderDialog**(`orderId`, `handler`): `Promise`<`void`>

Shows the cancel Order Ticket for specified order

#### Parameters

 **|Name** | **Type** | **Description** ||
| `orderId` | `string` | id of order to potentially cancel ||
| `handler` | () => `Promise`<`void`> | cancel order confirmation handler (called when order should be cancelled) ||

#### Returns
`Promise`<`void`>

### showConfirmDialog
▸ **showConfirmDialog**(`title`, `content`, `mainButtonText?`, `cancelButtonText?`, `showDisableConfirmationsCheckbox?`): `Promise`<`boolean`>

Displays a confirmation dialog to a user and returns a Promise to the result.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `title` | `string` | title of the confirmation dialog ||
| `content` | `string` | `string` | content for the dialog ||
| `mainButtonText?` | `string` | text for the main button (`true` result) ||
| `cancelButtonText?` | `string` | text for the cancel button (`false` result) ||
| `showDisableConfirmationsCheckbox?` | `boolean` | show disable confirmations checkbox within the dialog ||

#### Returns
`Promise`<`boolean`>

### showMessageDialog
▸ **showMessageDialog**(`title`, `text`, `textHasHTML?`): `void`

Displays a message dialog to a user.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `title` | `string` | title of the message dialog ||
| `text` | `string` | message ||
| `textHasHTML?` | `boolean` | whether message text contains HTML ||

#### Returns
`void`

### showNotification
▸ **showNotification**(`title`, `text`, `notificationType?`): `void`

Shows notification message

#### Parameters

 **|Name** | **Type** | **Description** ||
| `title` | `string` | notification title ||
| `text` | `string` | notification content ||
| `notificationType?` | [`NotificationType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.NotificationType) | type of notification (default: NotificationType.Error) ||

#### Returns
`void`

### showOrderDialog
▸ **showOrderDialog**<`T`>(`order`, `focus?`): `Promise`<`boolean`>

Shows the Order Ticket

#### Type parameters

 **|Name** | **Type** ||
| `T` | extends [`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder) ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `order` | `T` | order to show in the dialog ||
| `focus?` | [`OrderTicketFocusControl`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.OrderTicketFocusControl) | input control to focus on when dialog is opened ||

#### Returns
`Promise`<`boolean`>

### showPositionBracketsDialog
▸ **showPositionBracketsDialog**(`position`, `brackets`, `focus`): `Promise`<`boolean`>

Shows the position brackets dialog

#### Parameters

 **|Name** | **Type** | **Description** ||
| `position` | [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) | [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IndividualPosition) | position or individual position ||
| `brackets` | [`Brackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Brackets) | brackets for the position or individual position ||
| `focus` | [`OrderTicketFocusControl`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.OrderTicketFocusControl) | input control to focus on when dialog is opened ||

#### Returns
`Promise`<`boolean`>

### showReversePositionDialog
▸ **showReversePositionDialog**(`position`, `handler`): `Promise`<`boolean`>

Shows reverse position dialog

#### Parameters

 **|Name** | **Type** | **Description** ||
| `position` | `string` | position to be reversed ||
| `handler` | () => `Promise`<`boolean`> | reverse position confirmation handler (called when the position should be reversed) ||

#### Returns
`Promise`<`boolean`>

### showSimpleConfirmDialog
▸ **showSimpleConfirmDialog**(`title`, `content`, `mainButtonText?`, `cancelButtonText?`, `showDisableConfirmationsCheckbox?`): `Promise`<`boolean`>

Displays a simple confirmation dialog to a user and returns a Promise to the result.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `title` | `string` | title of the confirmation dialog ||
| `content` | `string` | `string` | content for the dialog ||
| `mainButtonText?` | `string` | text for the main button (`true` result) ||
| `cancelButtonText?` | `string` | text for the cancel button (`false` result) ||
| `showDisableConfirmationsCheckbox?` | `boolean` | show disable confirmations checkbox within the dialog ||

#### Returns
`Promise`<`boolean`>

### showTradingProperties
▸ **showTradingProperties**(): `void`

Shows trading properties

#### Returns
`void`

### silentOrdersPlacement
▸ **silentOrdersPlacement**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Returns if orders can be sent to the broker without showing the order ticket.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

### subscribeSuggestedQtyChange
▸ **subscribeSuggestedQtyChange**(`symbol`, `listener`): `void`

Adds a callback to be executed whenever there's a change of quantity for a given symbol.

It's the user's responsibility to manage the unsubscription of any added listener

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol to which the callback will be linked to ||
| `listener` | [`SuggestedQtyChangedListener`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#suggestedqtychangedlistener) | callback ||

#### Returns
`void`

### unsubscribeSuggestedQtyChange
▸ **unsubscribeSuggestedQtyChange**(`symbol`, `listener`): `void`

Remove a previously added callback from the list.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | symbol to remove the callback from ||
| `listener` | [`SuggestedQtyChangedListener`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#suggestedqtychangedlistener) | callback to be removed ||

#### Returns
`void`