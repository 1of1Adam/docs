---
title: "Interface: BracketOrder | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrder"
extracted_at: "2025-06-22T09:53:21.638Z"
---

- [](/charting-library-docs/)- Interfaces- BracketOrderOn this page# Interface: BracketOrder[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).BracketOrder

An object that contains information about a bracket order.

## Hierarchy[​](#hierarchy)

[`BracketOrderBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase)

[`CustomFields`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFields)

↳ `BracketOrder`

## Properties[​](#properties)
### avgPrice[​](#avgprice)
• `Optional` avgPrice: `number`

Average fulfilled price for the order (double)

#### Inherited from[​](#inherited-from)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[avgPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#avgprice)

### customFields[​](#customfields)
• `Optional` customFields: [`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldsValues)

An object that contains the results of broker specific user inputs (for example a digital signature).
There are two possible kinds of custom fields: an input field with a checkbox and a custom combobox.
#### Inherited from[​](#inherited-from-1)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[customFields](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#customfields)

### duration[​](#duration)
• `Optional` duration: [`OrderDuration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDuration)

Order duration

#### Inherited from[​](#inherited-from-2)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[duration](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#duration)

### filledQty[​](#filledqty)
• `Optional` filledQty: `number`

Filled order quantity (double)

#### Inherited from[​](#inherited-from-3)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[filledQty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#filledqty)

### guaranteedStop[​](#guaranteedstop)
• `Optional` guaranteedStop: `number`

Guaranteed stop loss price (double). Available when Brackets are enabled and supportGuaranteedStop flag is set to true

#### Inherited from[​](#inherited-from-4)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[guaranteedStop](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#guaranteedstop)

### id[​](#id)
• id: `string`

Order ID

#### Inherited from[​](#inherited-from-5)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#id)

### limitPrice[​](#limitprice)
• `Optional` limitPrice: `number`

Price for the limit order (double)

#### Inherited from[​](#inherited-from-6)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[limitPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#limitprice)

### message[​](#message)
• `Optional` message: [`OrderOrPositionMessage`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderOrPositionMessage)

Message describing the state of the order

#### Inherited from[​](#inherited-from-7)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[message](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#message)

### parentId[​](#parentid)
• parentId: `string`

If an order is a bracket, it should contain an ID of a parent order/position.

#### Inherited from[​](#inherited-from-8)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[parentId](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#parentid)

### parentType[​](#parenttype)
• parentType: [`ParentType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.ParentType)

Type of the bracket's parent.

#### Inherited from[​](#inherited-from-9)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[parentType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#parenttype)

### qty[​](#qty)
• qty: `number`

Order quantity (double)

#### Inherited from[​](#inherited-from-10)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[qty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#qty)

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

Order side (buy or sell)

#### Inherited from[​](#inherited-from-11)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[side](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#side)

### status[​](#status)
• status: [`OrderStatus`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderStatus)

Order status

#### Inherited from[​](#inherited-from-12)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[status](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#status)

### stopLoss[​](#stoploss)
• `Optional` stopLoss: `number`

Stop loss price (double). Available when Brackets are enabled

#### Inherited from[​](#inherited-from-13)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[stopLoss](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#stoploss)

### stopPrice[​](#stopprice)
• `Optional` stopPrice: `number`

Price for the stop order (double)

#### Inherited from[​](#inherited-from-14)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[stopPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#stopprice)

### stopType[​](#stoptype)
• `Optional` stopType: [`StopType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StopType)

Stop Loss type. It should be set to 1 (StopType.TrailingStop) for trailing stop orders.

#### Inherited from[​](#inherited-from-15)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[stopType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#stoptype)

### symbol[​](#symbol)
• symbol: `string`

Symbol name

#### Inherited from[​](#inherited-from-16)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#symbol)

### takeProfit[​](#takeprofit)
• `Optional` takeProfit: `number`

Take profit price (double). Available when Brackets are enabled

#### Inherited from[​](#inherited-from-17)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[takeProfit](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#takeprofit)

### trailingStopPips[​](#trailingstoppips)
• `Optional` trailingStopPips: `number`

Trailing stop Pips value (double). Available when Brackets are enabled

#### Inherited from[​](#inherited-from-18)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[trailingStopPips](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#trailingstoppips)

### type[​](#type)
• type: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)

Order type

#### Inherited from[​](#inherited-from-19)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#type)

### updateTime[​](#updatetime)
• `Optional` updateTime: `number`

Last update time (unix timestamp in milliseconds)

#### Inherited from[​](#inherited-from-20)
[BracketOrderBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase).[updateTime](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BracketOrderBase#updatetime)

- [Hierarchy](#hierarchy)- [Properties](#properties)[avgPrice](#avgprice)- [customFields](#customfields)- [duration](#duration)- [filledQty](#filledqty)- [guaranteedStop](#guaranteedstop)- [id](#id)- [limitPrice](#limitprice)- [message](#message)- [parentId](#parentid)- [parentType](#parenttype)- [qty](#qty)- [side](#side)- [status](#status)- [stopLoss](#stoploss)- [stopPrice](#stopprice)- [stopType](#stoptype)- [symbol](#symbol)- [takeProfit](#takeprofit)- [trailingStopPips](#trailingstoppips)- [type](#type)- [updateTime](#updatetime)