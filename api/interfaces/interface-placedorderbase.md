---
title: "Interface: PlacedOrderBase | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase"
extracted_at: "2025-06-22T09:55:55.464Z"
---

- [](/charting-library-docs/)- Interfaces- PlacedOrderBaseOn this page# Interface: PlacedOrderBase[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).PlacedOrderBase

An object that contains information about a placed order.

## Hierarchy[​](#hierarchy)

`PlacedOrderBase`

↳ [`BracketOrderBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase)

↳ [`PlacedOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrder)

## Properties[​](#properties)
### avgPrice[​](#avgprice)
• `Optional` avgPrice: `number`

Average fulfilled price for the order (double)

### customFields[​](#customfields)
• `Optional` customFields: [`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldsValues)

An object that contains the results of broker specific user inputs (for example a digital signature).
There are two possible kinds of custom fields: an input field with a checkbox and a custom combobox.

### duration[​](#duration)
• `Optional` duration: [`OrderDuration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDuration)

Order duration

### filledQty[​](#filledqty)
• `Optional` filledQty: `number`

Filled order quantity (double)

### guaranteedStop[​](#guaranteedstop)
• `Optional` guaranteedStop: `number`

Guaranteed stop loss price (double). Available when Brackets are enabled and supportGuaranteedStop flag is set to true

### id[​](#id)
• id: `string`

Order ID

### limitPrice[​](#limitprice)
• `Optional` limitPrice: `number`

Price for the limit order (double)

### message[​](#message)
• `Optional` message: [`OrderOrPositionMessage`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderOrPositionMessage)

Message describing the state of the order

### qty[​](#qty)
• qty: `number`

Order quantity (double)

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

Order side (buy or sell)

### status[​](#status)
• status: [`OrderStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderStatus)

Order status

### stopLoss[​](#stoploss)
• `Optional` stopLoss: `number`

Stop loss price (double). Available when Brackets are enabled

### stopPrice[​](#stopprice)
• `Optional` stopPrice: `number`

Price for the stop order (double)

### stopType[​](#stoptype)
• `Optional` stopType: [`StopType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StopType)

Stop Loss type. It should be set to 1 (StopType.TrailingStop) for trailing stop orders.

### symbol[​](#symbol)
• symbol: `string`

Symbol name

### takeProfit[​](#takeprofit)
• `Optional` takeProfit: `number`

Take profit price (double). Available when Brackets are enabled

### trailingStopPips[​](#trailingstoppips)
• `Optional` trailingStopPips: `number`

Trailing stop Pips value (double). Available when Brackets are enabled

### type[​](#type)
• type: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)

Order type

### updateTime[​](#updatetime)
• `Optional` updateTime: `number`

Last update time (unix timestamp in milliseconds)

- [Hierarchy](#hierarchy)- [Properties](#properties)[avgPrice](#avgprice)- [customFields](#customfields)- [duration](#duration)- [filledQty](#filledqty)- [guaranteedStop](#guaranteedstop)- [id](#id)- [limitPrice](#limitprice)- [message](#message)- [qty](#qty)- [side](#side)- [status](#status)- [stopLoss](#stoploss)- [stopPrice](#stopprice)- [stopType](#stoptype)- [symbol](#symbol)- [takeProfit](#takeprofit)- [trailingStopPips](#trailingstoppips)- [type](#type)- [updateTime](#updatetime)