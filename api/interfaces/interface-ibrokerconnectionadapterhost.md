---
title: "Interface: IBrokerConnectionAdapterHost | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost"
extracted_at: "2025-06-22T09:54:34.492Z"
---

- [](/charting-library-docs/)- Interfaces- IBrokerConnectionAdapterHostOn this page# Interface: IBrokerConnectionAdapterHost[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IBrokerConnectionAdapterHost

The Trading Host is an API for interaction between the Broker API and the library code related to trading.
Its main purpose is to receive information from your backend server where trading logic is implemented and provide updates to the library.
Refer to the [Core trading concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/) article for more information.
## Properties[​](#properties)
### factory[​](#factory)
• factory: [`IBrokerConnectionAdapterFactory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterFactory)

Broker Connection Adapter Factory object

## Methods[​](#methods)
### activateBottomWidget[​](#activatebottomwidget)
▸ activateBottomWidget(): `Promise`<`void`>

#### Returns[​](#returns)
`Promise`<`void`>

`Deprecated`

This method will be removed from the library in the next major version. Please use [setAccountManagerVisibilityMode](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#setaccountmanagervisibilitymode) instead.
Activate bottom widget

### connectionStatusUpdate[​](#connectionstatusupdate)
▸ connectionStatusUpdate(`status`, `info?`): `void`

Triggers a connection status update throughout the broker by reinvoking [IBrokerCommon.connectionStatus](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#connectionstatus).

#### Parameters[​](#parameters)
NameTypeDescription`status`[`ConnectionStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.ConnectionStatus)new connection status to propagate internally to the host`info?`[`DisconnectionInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DisconnectionInfo)additional information to provide when entering a disconnected status
#### Returns[​](#returns-1)
`void`

### cryptoBalanceUpdate[​](#cryptobalanceupdate)
▸ cryptoBalanceUpdate(`symbol`, `balance`): `void`

Call this method when a broker connection has received a balance update.
This method is required by the crypto Order Ticket.
It should be implemented when the [BrokerConfigFlags.supportBalances](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportbalances) flag is set to `true` in [SingleBrokerMetaInfo.configFlags](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SingleBrokerMetaInfo#configflags).
#### Parameters[​](#parameters-1)
NameTypeDescription`symbol``string`symbol ID`balance`[`CryptoBalance`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CryptoBalance)updated crypto balance
#### Returns[​](#returns-2)
`void`

### currentAccountUpdate[​](#currentaccountupdate)
▸ currentAccountUpdate(): `void`

Call this method when user account has been changed synchronously. The terminal will re-request all displayed information.

#### Returns[​](#returns-3)
`void`

### defaultContextMenuActions[​](#defaultcontextmenuactions)
▸ defaultContextMenuActions(`context`, `params?`): `Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]>

Provides default buy/sell, show properties actions to be returned as a default by [IBrokerCommon.chartContextMenuActions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerCommon#chartcontextmenuactions).

#### Parameters[​](#parameters-2)
NameTypeDescription`context`[`TradeContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradeContext)trade context`params?`[`DefaultContextMenuActionsParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DefaultContextMenuActionsParams)optional parameters
#### Returns[​](#returns-4)
`Promise`<[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]>

### defaultDropdownMenuActions[​](#defaultdropdownmenuactions)
▸ defaultDropdownMenuActions(`options?`): [`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]

Provides default dropdown list of actions. You can use default actions in IBrokerConnectionAdapterHost.setButtonDropdownActions

#### Parameters[​](#parameters-3)
NameTypeDescription`options?``Partial`<[`DefaultDropdownActionsParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DefaultDropdownActionsParams)>options for the dropdown menu actions
#### Returns[​](#returns-5)
[`ActionMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#actionmetainfo)[]

### defaultFormatter[​](#defaultformatter)
▸ defaultFormatter(`symbol`, `alignToMinMove`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Generates and returns the default value formatter for the symbol

#### Parameters[​](#parameters-4)
NameTypeDescription`symbol``string`symbol identifier`alignToMinMove``boolean`whether the formatted number should be aligned to minimum movement for the symbol
#### Returns[​](#returns-6)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

### domPanelVisibility[​](#dompanelvisibility)
▸ domPanelVisibility(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`boolean`>

Returns whether DOM Panel is visible or not.

#### Returns[​](#returns-7)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`boolean`>

### domUpdate[​](#domupdate)
▸ domUpdate(`symbol`, `equity`): `void`

Update the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) data for a specified symbol.

#### Parameters[​](#parameters-5)
NameTypeDescription`symbol``string`symbol identifier`equity`[`DOMData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DOMData)Depth of Market data
#### Returns[​](#returns-8)
`void`

### equityUpdate[​](#equityupdate)
▸ equityUpdate(`equity`): `void`

Call this method when a broker connection has received an equity update. This method is required by the standard Order Ticket to calculate risks.

#### Parameters[​](#parameters-6)
NameTypeDescription`equity``number`updated equity
#### Returns[​](#returns-9)
`void`

### executionUpdate[​](#executionupdate)
▸ executionUpdate(`execution`): `void`

Call this method when an execution is added.

#### Parameters[​](#parameters-7)
NameTypeDescription`execution`[`Execution`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Execution)execution which was added
#### Returns[​](#returns-10)
`void`

### getAccountManagerVisibilityMode[​](#getaccountmanagervisibilitymode)
▸ getAccountManagerVisibilityMode(): [`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValueReadonly)<[`BottomWidgetBarMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.BottomWidgetBarMode)>

Method to retrieve the current visibility mode of the Account Manager.

#### Returns[​](#returns-11)
[`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValueReadonly)<[`BottomWidgetBarMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.BottomWidgetBarMode)>

### getOrderTicketSetting[​](#getorderticketsetting)
▸ getOrderTicketSetting<`K`>(`settingName`): `Promise`<[`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTicketSettings)[`K`]>

Retrieves the current value for a specified [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) setting in the ellipsis menu.

#### Type parameters[​](#type-parameters)
NameTypeDescription`K`extends keyof [`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTicketSettings)A key of the OrderTicketSettings type.
#### Parameters[​](#parameters-8)
NameTypeDescription`settingName``K`The name of the Order Ticket setting.
#### Returns[​](#returns-12)
`Promise`<[`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTicketSettings)[`K`]>

A promise that resolves with the value of the specified setting.

### getQty[​](#getqty)
▸ getQty(`symbol`): `Promise`<`number`>

Returns the quantity for a given symbol.

#### Parameters[​](#parameters-9)
NameTypeDescription`symbol``string`symbol
#### Returns[​](#returns-13)
`Promise`<`number`>

- quantity for the given symbol

### getSymbolMinTick[​](#getsymbolmintick)
▸ getSymbolMinTick(`symbol`): `Promise`<`number`>

Returns symbol `minTick`.

#### Parameters[​](#parameters-10)
NameTypeDescription`symbol``string`symbol identifier
#### Returns[​](#returns-14)
`Promise`<`number`>

### individualPositionPLUpdate[​](#individualpositionplupdate)
▸ individualPositionPLUpdate(`individualPositionId`, `pl`): `void`

Call this method when a broker connection has received an individual position [profit and loss](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#provide-profit-and-loss) update.

#### Parameters[​](#parameters-11)
NameTypeDescription`individualPositionId``string`ID of the individual position`pl``number`updated profit / loss for the individual position
#### Returns[​](#returns-15)
`void`

### individualPositionPartialUpdate[​](#individualpositionpartialupdate)
▸ individualPositionPartialUpdate(`id`, `changes`): `void`

Call this method when an individual position has not changed, but fields that you added to the individual position object to display in the Account Manager have changed.

#### Parameters[​](#parameters-12)
NameTypeDescription`id``string`ID of the updated individual position`changes``Partial`<[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)>changes to the individual position object
#### Returns[​](#returns-16)
`void`

### individualPositionUpdate[​](#individualpositionupdate)
▸ individualPositionUpdate(`individualPosition`, `isHistoryUpdate?`): `void`

Call this method when an individual position is added or changed.

#### Parameters[​](#parameters-13)
NameTypeDescription`individualPosition`[`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)updated individual position`isHistoryUpdate?``boolean`whether the change is a history update
#### Returns[​](#returns-17)
`void`

### individualPositionsFullUpdate[​](#individualpositionsfullupdate)
▸ individualPositionsFullUpdate(): `void`

Call this method to clear the current cache for individual positions and notify the chart that it needs to request individual positions again.

#### Returns[​](#returns-18)
`void`

### marginAvailableUpdate[​](#marginavailableupdate)
▸ marginAvailableUpdate(`marginAvailable`): `void`

Call this method when a broker connection has received a margin available update.
This method is required by the standard Order Ticket to display the margin meter.
This method should be used when [BrokerConfigFlags.supportMargin](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportmargin) is set to `true` in [SingleBrokerMetaInfo.configFlags](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SingleBrokerMetaInfo#configflags).
The Trading Platform subscribes to margin available updates using [IBrokerTerminal.subscribeMarginAvailable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#subscribemarginavailable).
#### Parameters[​](#parameters-14)
NameTypeDescription`marginAvailable``number`updated available margin
#### Returns[​](#returns-19)
`void`

### numericFormatter[​](#numericformatter)
▸ numericFormatter(`decimalPlaces?`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Generates and returns a number formatter with the desired decimal places

#### Parameters[​](#parameters-15)
NameTypeDescription`decimalPlaces?``number`decimal places
#### Returns[​](#returns-20)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

### orderPanelVisibility[​](#orderpanelvisibility)
▸ orderPanelVisibility(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`boolean`>

Returns whether the order panel is visible or not.

#### Returns[​](#returns-21)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`boolean`>

### orderPartialUpdate[​](#orderpartialupdate)
▸ orderPartialUpdate(`id`, `orderChanges`): `void`

Call this method when an order is not changed, but the fields that you added to the order object to display in the Account Manager have changed.
It should be used only if you want to display custom fields in the Account Manager.
#### Parameters[​](#parameters-16)
NameTypeDescription`id``string`order id`orderChanges``Partial`<[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)>changes made to the order object
#### Returns[​](#returns-22)
`void`

### orderUpdate[​](#orderupdate)
▸ orderUpdate(`order`): `void`

Call this method to notify the chart that it needs to update information after an order is added or changed.

#### Parameters[​](#parameters-17)
NameTypeDescription`order`[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)order which was added or changed
#### Returns[​](#returns-23)
`void`

### ordersFullUpdate[​](#ordersfullupdate)
▸ ordersFullUpdate(): `void`

Call this method to clear the current cache for orders and notify the chart that it needs to request orders again.

#### Returns[​](#returns-24)
`void`

### patchConfig[​](#patchconfig)
▸ patchConfig(`config`): `void`

Patch changes into the current broker configuration

#### Parameters[​](#parameters-18)
NameTypeDescription`config``Partial`<[`BrokerConfigFlags`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags)>partial configuration changes to apply
#### Returns[​](#returns-25)
`void`

### pipValueUpdate[​](#pipvalueupdate)
▸ pipValueUpdate(`symbol`, `pipValues`): `void`

Call this method when a broker connection has a `pipValue` update.
The library subscribes to `pipValue` updates using [IBrokerTerminal.subscribePipValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#subscribepipvalue).
#### Parameters[​](#parameters-19)
NameTypeDescription`symbol``string`symbol with updated pip values`pipValues`[`PipValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PipValues)updated pip values
#### Returns[​](#returns-26)
`void`

### plUpdate[​](#plupdate)
▸ plUpdate(`positionId`, `pl`): `void`

Call this method when a broker connection has received a [profit and loss](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#provide-profit-and-loss) update.
Use this method when the [BrokerConfigFlags.supportPLUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportplupdate) flag is set to `true` in [SingleBrokerMetaInfo.configFlags](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SingleBrokerMetaInfo#configflags).
#### Parameters[​](#parameters-20)
NameTypeDescription`positionId``string`ID of the position`pl``number`updated profit / loss value
#### Returns[​](#returns-27)
`void`

### positionPartialUpdate[​](#positionpartialupdate)
▸ positionPartialUpdate(`id`, `positionChanges`): `void`

Call this method when a position is not changed, but the fields that you added to the position object to display in the Account Manager have changed.
It should be used only if you want to display custom fields in the Account Manager.
#### Parameters[​](#parameters-21)
NameTypeDescription`id``string`id of the position`positionChanges``Partial`<[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position)>changes to the position object
#### Returns[​](#returns-28)
`void`

### positionUpdate[​](#positionupdate)
▸ positionUpdate(`position`, `isHistoryUpdate?`): `void`

Call this method when a position is added or changed.

#### Parameters[​](#parameters-22)
NameTypeDescription`position`[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position)position which was added or changed`isHistoryUpdate?``boolean`whether the change is a history update
#### Returns[​](#returns-29)
`void`

### positionsFullUpdate[​](#positionsfullupdate)
▸ positionsFullUpdate(): `void`

Call this method to clear the current cache for positions and notify the chart that it needs to request positions again.

#### Returns[​](#returns-30)
`void`

### quantityFormatter[​](#quantityformatter)
▸ quantityFormatter(`decimalPlaces?`): `Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

Generates and returns a quantity formatter with the desired decimal places

#### Parameters[​](#parameters-23)
NameTypeDescription`decimalPlaces?``number`decimal places
#### Returns[​](#returns-31)
`Promise`<[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.INumberFormatter)>

### realtimeUpdate[​](#realtimeupdate)
▸ realtimeUpdate(`symbol`, `data`): `void`

Trading quote realtime update

#### Parameters[​](#parameters-24)
NameTypeDescription`symbol``string`symbol identifier`data`[`TradingQuotes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradingQuotes)realtime updated data for the symbol quotes
#### Returns[​](#returns-32)
`void`

### sellBuyButtonsVisibility[​](#sellbuybuttonsvisibility)
▸ sellBuyButtonsVisibility(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`boolean`>

Returns whether the buy/sell buttons are visible or not.

#### Returns[​](#returns-33)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`boolean`>

### setAccountManagerVisibilityMode[​](#setaccountmanagervisibilitymode)
▸ setAccountManagerVisibilityMode(`mode`): `void`

Method to set a new visibility mode for the Account Manager.

#### Parameters[​](#parameters-25)
NameType`mode`[`BottomWidgetBarMode`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.BottomWidgetBarMode)
#### Returns[​](#returns-34)
`void`

### setDurations[​](#setdurations)
▸ setDurations(`durations`): `void`

Set expiration durations

#### Parameters[​](#parameters-26)
NameTypeDescription`durations`[`OrderDurationMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDurationMetaInfo)[]Expiration options for orders
#### Returns[​](#returns-35)
`void`

### setOrderTicketSetting[​](#setorderticketsetting)
▸ setOrderTicketSetting<`K`>(`settingName`, `value`): `Promise`<`void`>

Updates the value of a specified [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) setting in the ellipsis menu.

#### Type parameters[​](#type-parameters-1)
NameTypeDescription`K`extends keyof [`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTicketSettings)A key of OrderTicketSettings type.
#### Parameters[​](#parameters-27)
NameTypeDescription`settingName``K`The name of the Order Ticket setting to be updated.`value`[`OrderTicketSettings`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTicketSettings)[`K`]The new value to be assigned to the setting.
#### Returns[​](#returns-36)
`Promise`<`void`>

A promise that resolves when the setting is successfully updated.

### setQty[​](#setqty)
▸ setQty(`symbol`, `quantity`): `void`

Sets the quantity for a given symbol.

#### Parameters[​](#parameters-28)
NameTypeDescription`symbol``string`symbol`quantity``number`quantity to update
#### Returns[​](#returns-37)
`void`

### showCancelBracketsDialog[​](#showcancelbracketsdialog)
▸ showCancelBracketsDialog(`orderId`, `handler`): `Promise`<`void`>

Shows the cancel brackets dialog

#### Parameters[​](#parameters-29)
NameTypeDescription`orderId``string`id of order`handler`() => `Promise`<`void`>cancel brackets confirmation handler (called when brackets should be cancelled)
#### Returns[​](#returns-38)
`Promise`<`void`>

### showCancelMultipleBracketsDialog[​](#showcancelmultiplebracketsdialog)
▸ showCancelMultipleBracketsDialog(`orderId`, `handler`): `Promise`<`void`>

Shows the cancel brackets dialog for multiple brackets

#### Parameters[​](#parameters-30)
NameTypeDescription`orderId``string`id of order`handler`() => `Promise`<`void`>cancel brackets confirmation handler (called when brackets should be cancelled)
#### Returns[​](#returns-39)
`Promise`<`void`>

### showCancelMultipleOrdersDialog[​](#showcancelmultipleordersdialog)
▸ showCancelMultipleOrdersDialog(`symbol`, `side`, `qty`, `handler`): `Promise`<`void`>

Shows the cancel Order Ticket for multiple orders

#### Parameters[​](#parameters-31)
NameTypeDescription`symbol``string`symbol for which to cancel orders`side`[`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)side of the order`qty``number`quantity of the order`handler`() => `Promise`<`void`>cancel orders confirmation handler (called when orders should be cancelled)
#### Returns[​](#returns-40)
`Promise`<`void`>

### showCancelOrderDialog[​](#showcancelorderdialog)
▸ showCancelOrderDialog(`orderId`, `handler`): `Promise`<`void`>

Shows the cancel Order Ticket for specified order

#### Parameters[​](#parameters-32)
NameTypeDescription`orderId``string`id of order to potentially cancel`handler`() => `Promise`<`void`>cancel order confirmation handler (called when order should be cancelled)
#### Returns[​](#returns-41)
`Promise`<`void`>

### showConfirmDialog[​](#showconfirmdialog)
▸ showConfirmDialog(`title`, `content`, `mainButtonText?`, `cancelButtonText?`, `showDisableConfirmationsCheckbox?`): `Promise`<`boolean`>

Displays a confirmation dialog to a user and returns a Promise to the result.

#### Parameters[​](#parameters-33)
NameTypeDescription`title``string`title of the confirmation dialog`content``string` | `string`[]content for the dialog`mainButtonText?``string`text for the main button (`true` result)`cancelButtonText?``string`text for the cancel button (`false` result)`showDisableConfirmationsCheckbox?``boolean`show disable confirmations checkbox within the dialog
#### Returns[​](#returns-42)
`Promise`<`boolean`>

### showMessageDialog[​](#showmessagedialog)
▸ showMessageDialog(`title`, `text`, `textHasHTML?`): `void`

Displays a message dialog to a user.

#### Parameters[​](#parameters-34)
NameTypeDescription`title``string`title of the message dialog`text``string`message`textHasHTML?``boolean`whether message text contains HTML
#### Returns[​](#returns-43)
`void`

### showNotification[​](#shownotification)
▸ showNotification(`title`, `text`, `notificationType?`): `void`

Shows notification message

#### Parameters[​](#parameters-35)
NameTypeDescription`title``string`notification title`text``string`notification content`notificationType?`[`NotificationType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.NotificationType)type of notification (default: NotificationType.Error)
#### Returns[​](#returns-44)
`void`

### showOrderDialog[​](#showorderdialog)
▸ showOrderDialog<`T`>(`order`, `focus?`): `Promise`<`boolean`>

Shows the Order Ticket

#### Type parameters[​](#type-parameters-2)
NameType`T`extends [`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PreOrder)
#### Parameters[​](#parameters-36)
NameTypeDescription`order``T`order to show in the dialog`focus?`[`OrderTicketFocusControl`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderTicketFocusControl)input control to focus on when dialog is opened
#### Returns[​](#returns-45)
`Promise`<`boolean`>

### showPositionBracketsDialog[​](#showpositionbracketsdialog)
▸ showPositionBracketsDialog(`position`, `brackets`, `focus`): `Promise`<`boolean`>

Shows the position brackets dialog

#### Parameters[​](#parameters-37)
NameTypeDescription`position`[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position) | [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)position or individual position`brackets`[`Brackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Brackets)brackets for the position or individual position`focus`[`OrderTicketFocusControl`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderTicketFocusControl)input control to focus on when dialog is opened
#### Returns[​](#returns-46)
`Promise`<`boolean`>

### showReversePositionDialog[​](#showreversepositiondialog)
▸ showReversePositionDialog(`position`, `handler`): `Promise`<`boolean`>

Shows reverse position dialog

#### Parameters[​](#parameters-38)
NameTypeDescription`position``string`position to be reversed`handler`() => `Promise`<`boolean`>reverse position confirmation handler (called when the position should be reversed)
#### Returns[​](#returns-47)
`Promise`<`boolean`>

### showSimpleConfirmDialog[​](#showsimpleconfirmdialog)
▸ showSimpleConfirmDialog(`title`, `content`, `mainButtonText?`, `cancelButtonText?`, `showDisableConfirmationsCheckbox?`): `Promise`<`boolean`>

Displays a simple confirmation dialog to a user and returns a Promise to the result.

#### Parameters[​](#parameters-39)
NameTypeDescription`title``string`title of the confirmation dialog`content``string` | `string`[]content for the dialog`mainButtonText?``string`text for the main button (`true` result)`cancelButtonText?``string`text for the cancel button (`false` result)`showDisableConfirmationsCheckbox?``boolean`show disable confirmations checkbox within the dialog
#### Returns[​](#returns-48)
`Promise`<`boolean`>

### showTradingProperties[​](#showtradingproperties)
▸ showTradingProperties(): `void`

Shows trading properties

#### Returns[​](#returns-49)
`void`

### silentOrdersPlacement[​](#silentordersplacement)
▸ silentOrdersPlacement(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`boolean`>

Returns if orders can be sent to the broker without showing the order ticket.

#### Returns[​](#returns-50)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`boolean`>

### subscribeSuggestedQtyChange[​](#subscribesuggestedqtychange)
▸ subscribeSuggestedQtyChange(`symbol`, `listener`): `void`

Adds a callback to be executed whenever there's a change of quantity for a given symbol.

It's the user's responsibility to manage the unsubscription of any added listener

#### Parameters[​](#parameters-40)
NameTypeDescription`symbol``string`symbol to which the callback will be linked to`listener`[`SuggestedQtyChangedListener`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#suggestedqtychangedlistener)callback
#### Returns[​](#returns-51)
`void`

### unsubscribeSuggestedQtyChange[​](#unsubscribesuggestedqtychange)
▸ unsubscribeSuggestedQtyChange(`symbol`, `listener`): `void`

Remove a previously added callback from the list.

#### Parameters[​](#parameters-41)
NameTypeDescription`symbol``string`symbol to remove the callback from`listener`[`SuggestedQtyChangedListener`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#suggestedqtychangedlistener)callback to be removed
#### Returns[​](#returns-52)
`void`

- [Properties](#properties)[factory](#factory)- [Methods](#methods)[activateBottomWidget](#activatebottomwidget)- [connectionStatusUpdate](#connectionstatusupdate)- [cryptoBalanceUpdate](#cryptobalanceupdate)- [currentAccountUpdate](#currentaccountupdate)- [defaultContextMenuActions](#defaultcontextmenuactions)- [defaultDropdownMenuActions](#defaultdropdownmenuactions)- [defaultFormatter](#defaultformatter)- [domPanelVisibility](#dompanelvisibility)- [domUpdate](#domupdate)- [equityUpdate](#equityupdate)- [executionUpdate](#executionupdate)- [getAccountManagerVisibilityMode](#getaccountmanagervisibilitymode)- [getOrderTicketSetting](#getorderticketsetting)- [getQty](#getqty)- [getSymbolMinTick](#getsymbolmintick)- [individualPositionPLUpdate](#individualpositionplupdate)- [individualPositionPartialUpdate](#individualpositionpartialupdate)- [individualPositionUpdate](#individualpositionupdate)- [individualPositionsFullUpdate](#individualpositionsfullupdate)- [marginAvailableUpdate](#marginavailableupdate)- [numericFormatter](#numericformatter)- [orderPanelVisibility](#orderpanelvisibility)- [orderPartialUpdate](#orderpartialupdate)- [orderUpdate](#orderupdate)- [ordersFullUpdate](#ordersfullupdate)- [patchConfig](#patchconfig)- [pipValueUpdate](#pipvalueupdate)- [plUpdate](#plupdate)- [positionPartialUpdate](#positionpartialupdate)- [positionUpdate](#positionupdate)- [positionsFullUpdate](#positionsfullupdate)- [quantityFormatter](#quantityformatter)- [realtimeUpdate](#realtimeupdate)- [sellBuyButtonsVisibility](#sellbuybuttonsvisibility)- [setAccountManagerVisibilityMode](#setaccountmanagervisibilitymode)- [setDurations](#setdurations)- [setOrderTicketSetting](#setorderticketsetting)- [setQty](#setqty)- [showCancelBracketsDialog](#showcancelbracketsdialog)- [showCancelMultipleBracketsDialog](#showcancelmultiplebracketsdialog)- [showCancelMultipleOrdersDialog](#showcancelmultipleordersdialog)- [showCancelOrderDialog](#showcancelorderdialog)- [showConfirmDialog](#showconfirmdialog)- [showMessageDialog](#showmessagedialog)- [showNotification](#shownotification)- [showOrderDialog](#showorderdialog)- [showPositionBracketsDialog](#showpositionbracketsdialog)- [showReversePositionDialog](#showreversepositiondialog)- [showSimpleConfirmDialog](#showsimpleconfirmdialog)- [showTradingProperties](#showtradingproperties)- [silentOrdersPlacement](#silentordersplacement)- [subscribeSuggestedQtyChange](#subscribesuggestedqtychange)- [unsubscribeSuggestedQtyChange](#unsubscribesuggestedqtychange)