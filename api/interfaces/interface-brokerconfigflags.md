---
title: "Interface: BrokerConfigFlags | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags"
extracted_at: "2025-06-22T09:53:26.498Z"
---

- [](/charting-library-docs/)- Interfaces- BrokerConfigFlagsOn this page# Interface: BrokerConfigFlags[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).BrokerConfigFlags

## Properties[​](#properties)
### closePositionCancelsOrders[​](#closepositioncancelsorders)
• `Optional` closePositionCancelsOrders: `boolean`

Closing a position cancels its brackets.

`Default`

```
false
```

### positionPLInInstrumentCurrency[​](#positionplininstrumentcurrency)
• `Optional` positionPLInInstrumentCurrency: `boolean`

Enables displaying Profit & Loss values in instrument currency.

`Default`

```
false
```

### requiresFIFOCloseIndividualPositions[​](#requiresfifocloseindividualpositions)
• `Optional` requiresFIFOCloseIndividualPositions: `boolean`

Enables closing of individual positions in FIFO order.

`Default`

```
false
```

### showNotificationsLog[​](#shownotificationslog)
• `Optional` showNotificationsLog: `boolean`

Enables the Notifications log tab in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).

`Default`

```
true
```

### showQuantityInsteadOfAmount[​](#showquantityinsteadofamount)
• `Optional` showQuantityInsteadOfAmount: `boolean`

Changes Amount to Quantity in Order Ticket.

`Default`

```
false
```

### supportAddBracketsToExistingOrder[​](#supportaddbracketstoexistingorder)
• `Optional` supportAddBracketsToExistingOrder: `boolean`

Enables adding brackets to the existing order.

`Default`

```
true
```

### supportBalances[​](#supportbalances)
• `Optional` supportBalances: `boolean`

Allows getting crypto balances for an account.
Balances are displayed as the first table of the Account Summary tab.
Use the flag for crypto currencies only.
This flag requires the [IBrokerConnectionAdapterHost.cryptoBalanceUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#cryptobalanceupdate) method to be implemented.
`Default`

```
false
```

### supportCancellingBothBracketsOnly[​](#supportcancellingbothbracketsonly)
• `Optional` supportCancellingBothBracketsOnly: `boolean`

Modifies the confirmation dialog text for closing a bracket order.
When set to `true`, the text explicitly states that cancelling a bracket order will also cancel its associated pair.
When set to `false`, the text will include the ID of the singular bracket order being cancelled.
Note that the library does not cancel orders itself.
You should implement the [IBrokerTerminal.cancelOrder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#cancelorder) or [IBrokerTerminal.cancelOrders](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#cancelorders) method.
`Default`

```
false
```

### supportCloseIndividualPosition[​](#supportcloseindividualposition)
• `Optional` supportCloseIndividualPosition: `boolean`

Enables individual [position closing](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#close-positions).
This flag requires the [IBrokerTerminal.closeIndividualPosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#closeindividualposition) method to be implemented.
`Default`

```
false
```

### supportClosePosition[​](#supportcloseposition)
• `Optional` supportClosePosition: `boolean`

Enables [position closing](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#close-positions).

- If `supportClosePosition` is set to `false`, positions are closed using [market orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/orders#order-types) of the opposite side. The library calls the [IBrokerTerminal.placeOrder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#placeorder) method, passing the `isClose` property set to `true` in the `PreOrder` object.
- If `supportClosePosition` is set to `true`, the library calls the [IBrokerTerminal.closePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#closeposition) method.

`Default`

```
false
```

### supportCryptoBrackets[​](#supportcryptobrackets)
• `Optional` supportCryptoBrackets: `boolean`

Enables crypto brackets.

`Default`

```
false
```

### supportCryptoExchangeOrderTicket[​](#supportcryptoexchangeorderticket)
• `Optional` supportCryptoExchangeOrderTicket: `boolean`

Enables cryptocurrency trading (exchanging).
This flag switches the Order Ticket to Crypto Exchange mode,
which provides additional controls for entering the quantity in either the base or quote currency.
`Default`

```
false
```

### supportCustomOrderInfo[​](#supportcustomorderinfo)
• `Optional` supportCustomOrderInfo: `boolean`

Allows brokers to add their own parameters that will be displayed in Order info.

`Default`

```
false
```

### supportDemoLiveSwitcher[​](#supportdemoliveswitcher)
• `Optional` supportDemoLiveSwitcher: `boolean`

Enables demo live switcher.

`Default`

```
true
```

### supportEditAmount[​](#supporteditamount)
• `Optional` supportEditAmount: `boolean`

Enables order quantity editing.
If you set this flag to `false`, the quantity control in the Order Ticket will be disabled when users modify orders.
`Default`

```
true
```

### supportExecutions[​](#supportexecutions)
• `Optional` supportExecutions: `boolean`

If set to `true`, executions are displayed on the chart.
This flag requires the [`executions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#executions) method to be implemented.
`Default`

```
false
```

### supportGuaranteedStop[​](#supportguaranteedstop)
• `Optional` supportGuaranteedStop: `boolean`

Enables guaranteed stop loss orders.
If you set this flag to `true`, the library displays guaranteed stop orders and a user can place a guaranteed stop order using the Order Ticket.
`Default`

```
false
```

### supportIndividualPositionBrackets[​](#supportindividualpositionbrackets)
• `Optional` supportIndividualPositionBrackets: `boolean`

Enables brackets for individual positions: take-profit and stop-loss orders.
If you set this flag to `true`, the library displays an Edit button for individual positions and Edit position... in the individual position's context menu.
This flag requires the [IBrokerTerminal.editIndividualPositionBrackets](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#editindividualpositionbrackets) method to be implemented.
`Default`

```
false
```

### supportLevel2Data[​](#supportlevel2data)
• `Optional` supportLevel2Data: `boolean`

Enables Level 2 data for the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) widget.
This flag requires the [`subscribeDepth`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribedepth) and [`unsubscribeDepth`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#unsubscribedepth) methods to be implemented.
`Default`

```
false
```

### supportLeverage[​](#supportleverage)
• `Optional` supportLeverage: `boolean`

Enables trading with leverage.
If the flag is set to `true`, you should calculate the leverage using the [IBrokerTerminal.leverageInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#leverageinfo) method.
`Default`

```
false
```

### supportLeverageButton[​](#supportleveragebutton)
• `Optional` supportLeverageButton: `boolean`

Displays a leverage button in the UI.
Note that you should also enable the [BrokerConfigFlags.supportLeverage](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportleverage) flag.
If `supportLeverageButton` is set to `true`, the leverage input field appears in the Order Ticket.
Clicking the input field activates a dedicated Leverage Dialog.
`Default`

```
true
```

### supportLimitOrders[​](#supportlimitorders)
• `Optional` supportLimitOrders: `boolean`

Enables limit orders type in the Order Ticket.

`Default`

```
true
```

### supportMargin[​](#supportmargin)
• `Optional` supportMargin: `boolean`

Allows margin.
If `supportMargin` is set to `true`, you should call [IBrokerConnectionAdapterHost.marginAvailableUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#marginavailableupdate) when the Trading Platform subscribes to margin available updates using [IBrokerTerminal.subscribeMarginAvailable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#subscribemarginavailable).
`Default`

```
false
```

### supportMarketBrackets[​](#supportmarketbrackets)
• `Optional` supportMarketBrackets: `boolean`

Enables brackets for market orders.

`Default`

```
true
```

### supportMarketOrders[​](#supportmarketorders)
• `Optional` supportMarketOrders: `boolean`

Enables market orders type in the Order Ticket.

`Default`

```
true
```

### supportModifyBrackets[​](#supportmodifybrackets)
• `Optional` supportModifyBrackets: `boolean`

Enables order brackets editing.
If you set this flag to `false`, the bracket's control in the Order Ticket will be disabled,
and the Modify button will be hidden from the chart and in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).
`Default`

```
true
```

### supportModifyDuration[​](#supportmodifyduration)
• `Optional` supportModifyDuration: `boolean`

Allows modifying existing [order duration](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-time-in-force-menu).

`Default`

```
false
```

### supportModifyOrderPreview[​](#supportmodifyorderpreview)
• `Optional` supportModifyOrderPreview: `boolean`

Allows providing the estimated commission, fees, margin, and other order information before modifying the order without actually modifying it.
This information will be displayed in the Order confirmation dialog.
This flag requires the [IBrokerTerminal.previewOrder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#previeworder) method to be implemented and `confirmId` parameter to be passed in the [IBrokerTerminal.modifyOrder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#modifyorder) method.
Refer to [Enable order preview](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#add-custom-fields) for more information.
`Default`

```
false
```

### supportModifyOrderPrice[​](#supportmodifyorderprice)
• `Optional` supportModifyOrderPrice: `boolean`

Enables order price editing.
If you set this flag to `false`, the price control in the Order Ticket will be disabled when users modify orders.
`Default`

```
true
```

### supportModifyOrderType[​](#supportmodifyordertype)
• `Optional` supportModifyOrderType: `boolean`

Allows modifying order type.

`Default`

```
false
```

### supportModifyTrailingStop[​](#supportmodifytrailingstop)
• `Optional` supportModifyTrailingStop: `boolean`

Allows modifying trailing stop orders.

`Default`

```
true
```

### supportMultiposition[​](#supportmultiposition)
• `Optional` supportMultiposition: `boolean`

Enables [multiple positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#multiposition) for one instrument at the same time.

Note that if the flag is set to `true`:

- The [default reversal](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#default-reversal) in the library does not work. You need to implement the [native reversal](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#native-reversal) on your backend side.
- The Flatten button in the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) widget will be disabled.

`Default`

```
false
```

### supportNativeReversePosition[​](#supportnativereverseposition)
• `Optional` supportNativeReversePosition: `boolean`

Enables [native](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#native-reversal) position reversing. You should implement the [IBrokerTerminal.reversePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#reverseposition) method to process reversing on your backend side.
Note that the [supportReversePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportreverseposition) flag should be set to `true` to enable the reverse option in the UI.
If `supportNativeReversePosition` is set to `false`, the library handles reversing using the built-in mechanism. For more information, refer to the [Default reversal](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#default-reversal) section.

`Default`

```
false
```

### supportOnlyPairPositionBrackets[​](#supportonlypairpositionbrackets)
• `Optional` supportOnlyPairPositionBrackets: `boolean`

`Stop Loss` and `Take Profit` are added or removed only together.

`Default`

```
false
```

### supportOrderBrackets[​](#supportorderbrackets)
• `Optional` supportOrderBrackets: `boolean`

Enables order brackets: take-profit and stop-loss.

`Default`

```
false
```

### supportOrdersHistory[​](#supportordershistory)
• `Optional` supportOrdersHistory: `boolean`

Enables orders history.
If `supportOrdersHistory` is set to `true`, the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) will have an additional tab: Orders History.
This flag requires the [`ordersHistory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#ordershistory) method to be implemented.
The method should return a list of orders with the `filled`, `cancelled`, and `rejected` statuses from previous trade sessions.
`Default`

```
false
```

### supportPLUpdate[​](#supportplupdate)
• `Optional` supportPLUpdate: `boolean`

Allows using your own [profit and loss](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#provide-profit-and-loss) (P&L) values for positions.
By default, `supportPLUpdate` is set to `true`, which means:

- You should calculate the P&L value for a position on your backend server.
- Once calculated, call the [IBrokerConnectionAdapterHost.plUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#plupdate) method to provide the library with updated values.
- If [position netting](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#position-netting) is enabled, you should also call [IBrokerConnectionAdapterHost.individualPositionPLUpdate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#individualpositionplupdate).

If `supportPLUpdate` is set to `false`, the library automatically calculates P&L values as the difference between the current trade and the average position price.
However, we recommend using your own P&L calculations for positions.
This helps avoid any discrepancies between the P&L values of the account and positions due to potential delays.
`Default`

```
true
```

### supportPartialCloseIndividualPosition[​](#supportpartialcloseindividualposition)
• `Optional` supportPartialCloseIndividualPosition: `boolean`

Enables [partial individual position closing](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#partial-closing).
This flag requires the [IBrokerTerminal.closeIndividualPosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#closeindividualposition) method to be implemented.
`Default`

```
false
```

### supportPartialClosePosition[​](#supportpartialcloseposition)
• `Optional` supportPartialClosePosition: `boolean`

Enables [partial position closing](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#partial-closing).
This flag requires the [IBrokerTerminal.closePosition](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#closeposition) method to be implemented.
`Default`

```
false
```

### supportPlaceOrderPreview[​](#supportplaceorderpreview)
• `Optional` supportPlaceOrderPreview: `boolean`

Allows providing the estimated commission, fees, margin, and other order information before placing the order without actually placing it.
This information will be displayed in the Order confirmation dialog.
This flag requires the [IBrokerTerminal.previewOrder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#previeworder) method to be implemented and `confirmId` parameter to be passed in the [IBrokerTerminal.placeOrder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#placeorder) method.
Refer to [Enable order preview](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#add-custom-fields) for more information.
`Default`

```
false
```

### supportPositionBrackets[​](#supportpositionbrackets)
• `Optional` supportPositionBrackets: `boolean`

Enables position brackets: take-profit and stop-loss orders.
If you set `supportPositionBrackets` to `true`, the library displays an Edit button for positions and Edit position... in the position's context menu.
This flag requires the [IBrokerTerminal.editPositionBrackets](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal#editpositionbrackets) method to be implemented.
`Default`

```
false
```

### supportPositionNetting[​](#supportpositionnetting)
• `Optional` supportPositionNetting: `boolean`

Enables [position netting](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#position-netting).
This flag requires the [`positions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#positions) and [`individualPositions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#individualpositions) method to be implemented.
If you set this flag to `true`, the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) will have two tabs: Individual Positions and Net Positions.

`Default`

```
false
```

### supportPositions[​](#supportpositions)
• `Optional` supportPositions: `boolean`

Enables [positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
This flag requires the [`positions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#positions) method to be implemented.
If you set `supportPositions` to `false`, the Positions tab in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) will be hidden.
`Default`

```
true
```

### supportPreviewClosePosition[​](#supportpreviewcloseposition)
• `Optional` supportPreviewClosePosition: `boolean`

Allows brokers to send position closing information that will be displayed in Close Position Dialog

`Default`

```
false
```

### supportReversePosition[​](#supportreverseposition)
• `Optional` supportReversePosition: `boolean`

Enables [position reversing](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions#reverse-positions).
If `supportReversePosition` is set to `false`, the Reverse Position button will be hidden from the UI.
`Default`

```
false
```

### supportStopLimitOrders[​](#supportstoplimitorders)
• `Optional` supportStopLimitOrders: `boolean`

Enables stop-limit orders type in the Order Ticket.

`Default`

```
false
```

### supportStopLimitOrdersInBothDirections[​](#supportstoplimitordersinbothdirections)
• `Optional` supportStopLimitOrdersInBothDirections: `boolean`

Whether stop-limit orders should behave like Limit-if-Touched in both directions.
Enabling this flag prevents the check of stop price direction from the stop limit Order Ticket.

### supportStopLoss[​](#supportstoploss)
• `Optional` supportStopLoss: `boolean`

Enables stop loss orders. If this flag is set to `true`, the library displays stop loss orders and a user can place a stop loss order using the Order Ticket.
If you set this flag to `false`, the [BrokerConfigFlags.supportTrailingStop](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supporttrailingstop) and/or [BrokerConfigFlags.supportGuaranteedStop](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags#supportguaranteedstop) flag should be set to `true`.
If the `supportStopLoss`, `supportTrailingStop`, and `supportGuaranteedStop` flags are set to `false`, the default value will be used.
`Default`

```
true
```

### supportStopOrders[​](#supportstoporders)
• `Optional` supportStopOrders: `boolean`

Enables stop orders type in the Order Ticket.

`Default`

```
true
```

### supportStopOrdersInBothDirections[​](#supportstopordersinbothdirections)
• `Optional` supportStopOrdersInBothDirections: `boolean`

Whether stop orders should behave like Market-if-Touched in both directions.
Enabling this flag prevents the check of stop price direction from the stop limit Order Ticket.
`Default`

```
false
```

### supportStrictCheckingLimitOrderPrice[​](#supportstrictcheckinglimitorderprice)
• `Optional` supportStrictCheckingLimitOrderPrice: `boolean`

Whether the integration supports limit price validation in the order ticket to eliminate the possibility to place
an order on the wrong side of the market that will most likely trigger and get filled immediately.

### supportSymbolSearch[​](#supportsymbolsearch)
• `Optional` supportSymbolSearch: `boolean`

Enables symbol searching.

`Default`

```
false
```

### supportTrailingStop[​](#supporttrailingstop)
• `Optional` supportTrailingStop: `boolean`

Enables trailing stop orders.
If you set this flag to `true`, the library displays trailing stop orders and a user can place a trailing stop order using the Order Ticket.
`Default`

```
false
```- [Properties](#properties)[closePositionCancelsOrders](#closepositioncancelsorders)- [positionPLInInstrumentCurrency](#positionplininstrumentcurrency)- [requiresFIFOCloseIndividualPositions](#requiresfifocloseindividualpositions)- [showNotificationsLog](#shownotificationslog)- [showQuantityInsteadOfAmount](#showquantityinsteadofamount)- [supportAddBracketsToExistingOrder](#supportaddbracketstoexistingorder)- [supportBalances](#supportbalances)- [supportCancellingBothBracketsOnly](#supportcancellingbothbracketsonly)- [supportCloseIndividualPosition](#supportcloseindividualposition)- [supportClosePosition](#supportcloseposition)- [supportCryptoBrackets](#supportcryptobrackets)- [supportCryptoExchangeOrderTicket](#supportcryptoexchangeorderticket)- [supportCustomOrderInfo](#supportcustomorderinfo)- [supportDemoLiveSwitcher](#supportdemoliveswitcher)- [supportEditAmount](#supporteditamount)- [supportExecutions](#supportexecutions)- [supportGuaranteedStop](#supportguaranteedstop)- [supportIndividualPositionBrackets](#supportindividualpositionbrackets)- [supportLevel2Data](#supportlevel2data)- [supportLeverage](#supportleverage)- [supportLeverageButton](#supportleveragebutton)- [supportLimitOrders](#supportlimitorders)- [supportMargin](#supportmargin)- [supportMarketBrackets](#supportmarketbrackets)- [supportMarketOrders](#supportmarketorders)- [supportModifyBrackets](#supportmodifybrackets)- [supportModifyDuration](#supportmodifyduration)- [supportModifyOrderPreview](#supportmodifyorderpreview)- [supportModifyOrderPrice](#supportmodifyorderprice)- [supportModifyOrderType](#supportmodifyordertype)- [supportModifyTrailingStop](#supportmodifytrailingstop)- [supportMultiposition](#supportmultiposition)- [supportNativeReversePosition](#supportnativereverseposition)- [supportOnlyPairPositionBrackets](#supportonlypairpositionbrackets)- [supportOrderBrackets](#supportorderbrackets)- [supportOrdersHistory](#supportordershistory)- [supportPLUpdate](#supportplupdate)- [supportPartialCloseIndividualPosition](#supportpartialcloseindividualposition)- [supportPartialClosePosition](#supportpartialcloseposition)- [supportPlaceOrderPreview](#supportplaceorderpreview)- [supportPositionBrackets](#supportpositionbrackets)- [supportPositionNetting](#supportpositionnetting)- [supportPositions](#supportpositions)- [supportPreviewClosePosition](#supportpreviewcloseposition)- [supportReversePosition](#supportreverseposition)- [supportStopLimitOrders](#supportstoplimitorders)- [supportStopLimitOrdersInBothDirections](#supportstoplimitordersinbothdirections)- [supportStopLoss](#supportstoploss)- [supportStopOrders](#supportstoporders)- [supportStopOrdersInBothDirections](#supportstopordersinbothdirections)- [supportStrictCheckingLimitOrderPrice](#supportstrictcheckinglimitorderprice)- [supportSymbolSearch](#supportsymbolsearch)- [supportTrailingStop](#supporttrailingstop)