---
title: "Interface: BracketOrderBase | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase"
extracted_at: "2025-06-22T09:53:23.113Z"
---

- [](/charting-library-docs/)- Interfaces- BracketOrderBaseOn this page# Interface: BracketOrderBase[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).BracketOrderBase

An object that contains information about a placed order.

## Hierarchy[​](#hierarchy)

[`PlacedOrderBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase)

↳ `BracketOrderBase`

↳↳ [`BracketOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrder)

## Properties[​](#properties)
### avgPrice[​](#avgprice)
• `Optional` avgPrice: `number`

Average fulfilled price for the order (double)

#### Inherited from[​](#inherited-from)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[avgPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#avgprice)

### customFields[​](#customfields)
• `Optional` customFields: [`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldsValues)

An object that contains the results of broker specific user inputs (for example a digital signature).
There are two possible kinds of custom fields: an input field with a checkbox and a custom combobox.
#### Inherited from[​](#inherited-from-1)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[customFields](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#customfields)

### duration[​](#duration)
• `Optional` duration: [`OrderDuration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDuration)

Order duration

#### Inherited from[​](#inherited-from-2)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[duration](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#duration)

### filledQty[​](#filledqty)
• `Optional` filledQty: `number`

Filled order quantity (double)

#### Inherited from[​](#inherited-from-3)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[filledQty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#filledqty)

### guaranteedStop[​](#guaranteedstop)
• `Optional` guaranteedStop: `number`

Guaranteed stop loss price (double). Available when Brackets are enabled and supportGuaranteedStop flag is set to true

#### Inherited from[​](#inherited-from-4)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[guaranteedStop](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#guaranteedstop)

### id[​](#id)
• id: `string`

Order ID

#### Inherited from[​](#inherited-from-5)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#id)

### limitPrice[​](#limitprice)
• `Optional` limitPrice: `number`

Price for the limit order (double)

#### Inherited from[​](#inherited-from-6)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[limitPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#limitprice)

### message[​](#message)
• `Optional` message: [`OrderOrPositionMessage`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderOrPositionMessage)

Message describing the state of the order

#### Inherited from[​](#inherited-from-7)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[message](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#message)

### parentId[​](#parentid)
• parentId: `string`

If an order is a bracket, it should contain an ID of a parent order/position.

### parentType[​](#parenttype)
• parentType: [`ParentType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.ParentType)

Type of the bracket's parent.

### qty[​](#qty)
• qty: `number`

Order quantity (double)

#### Inherited from[​](#inherited-from-8)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[qty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#qty)

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

Order side (buy or sell)

#### Inherited from[​](#inherited-from-9)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[side](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#side)

### status[​](#status)
• status: [`OrderStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderStatus)

Order status

#### Inherited from[​](#inherited-from-10)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[status](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#status)

### stopLoss[​](#stoploss)
• `Optional` stopLoss: `number`

Stop loss price (double). Available when Brackets are enabled

#### Inherited from[​](#inherited-from-11)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[stopLoss](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#stoploss)

### stopPrice[​](#stopprice)
• `Optional` stopPrice: `number`

Price for the stop order (double)

#### Inherited from[​](#inherited-from-12)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[stopPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#stopprice)

### stopType[​](#stoptype)
• `Optional` stopType: [`StopType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StopType)

Stop Loss type. It should be set to 1 (StopType.TrailingStop) for trailing stop orders.

#### Inherited from[​](#inherited-from-13)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[stopType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#stoptype)

### symbol[​](#symbol)
• symbol: `string`

Symbol name

#### Inherited from[​](#inherited-from-14)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#symbol)

### takeProfit[​](#takeprofit)
• `Optional` takeProfit: `number`

Take profit price (double). Available when Brackets are enabled

#### Inherited from[​](#inherited-from-15)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[takeProfit](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#takeprofit)

### trailingStopPips[​](#trailingstoppips)
• `Optional` trailingStopPips: `number`

Trailing stop Pips value (double). Available when Brackets are enabled

#### Inherited from[​](#inherited-from-16)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[trailingStopPips](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#trailingstoppips)

### type[​](#type)
• type: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)

Order type

#### Inherited from[​](#inherited-from-17)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#type)

### updateTime[​](#updatetime)
• `Optional` updateTime: `number`

Last update time (unix timestamp in milliseconds)

#### Inherited from[​](#inherited-from-18)
[PlacedOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase).[updateTime](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PlacedOrderBase#updatetime)

- [Hierarchy](#hierarchy)- [Properties](#properties)[avgPrice](#avgprice)- [customFields](#customfields)- [duration](#duration)- [filledQty](#filledqty)- [guaranteedStop](#guaranteedstop)- [id](#id)- [limitPrice](#limitprice)- [message](#message)- [parentId](#parentid)- [parentType](#parenttype)- [qty](#qty)- [side](#side)- [status](#status)- [stopLoss](#stoploss)- [stopPrice](#stopprice)- [stopType](#stoptype)- [symbol](#symbol)- [takeProfit](#takeprofit)- [trailingStopPips](#trailingstoppips)- [type](#type)- [updateTime](#updatetime)