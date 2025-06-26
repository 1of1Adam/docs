---
title: "Interface: PreOrder | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PreOrder"
extracted_at: "2025-06-22T09:56:08.032Z"
---

- [](/charting-library-docs/)- Interfaces- PreOrderOn this page# Interface: PreOrder[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).PreOrder

Output value of the Order Ticket and input value of the broker's place order command.
This information is sufficient to place an order.
## Hierarchy[​](#hierarchy)

[`OrderTemplateBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase)

↳ `PreOrder`

## Properties[​](#properties)
### currentQuotes[​](#currentquotes)
• `Optional` currentQuotes: `Required`<`Pick`<[`TradingQuotes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradingQuotes), `"ask"` | `"bid"`>>

Current Quotes

#### Inherited from[​](#inherited-from)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[currentQuotes](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#currentquotes)

### customFields[​](#customfields)
• `Optional` customFields: [`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldsValues)

Custom input fields

#### Inherited from[​](#inherited-from-1)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[customFields](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#customfields)

### duration[​](#duration)
• `Optional` duration: [`OrderDuration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDuration)

Duration or expiration of an order

#### Inherited from[​](#inherited-from-2)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[duration](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#duration)

### guaranteedStop[​](#guaranteedstop)
• `Optional` guaranteedStop: `number`

Order Guaranteed Stop loss (Brackets)

#### Inherited from[​](#inherited-from-3)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[guaranteedStop](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#guaranteedstop)

### isClose[​](#isclose)
• `Optional` isClose: `boolean`

It is set to `true`, if the order closes a position.

### limitPrice[​](#limitprice)
• `Optional` limitPrice: `number`

Order limit price

#### Inherited from[​](#inherited-from-4)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[limitPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#limitprice)

### qty[​](#qty)
• qty: `number`

Order quantity

#### Overrides[​](#overrides)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[qty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#qty)

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

order / execution side

#### Overrides[​](#overrides-1)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[side](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#side)

### stopLoss[​](#stoploss)
• `Optional` stopLoss: `number`

Order Stop loss (Brackets)

#### Inherited from[​](#inherited-from-5)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[stopLoss](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#stoploss)

### stopPrice[​](#stopprice)
• `Optional` stopPrice: `number`

Order stop price

#### Inherited from[​](#inherited-from-6)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[stopPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#stopprice)

### stopType[​](#stoptype)
• `Optional` stopType: [`StopType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StopType)

Type of Stop Order

#### Inherited from[​](#inherited-from-7)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[stopType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#stoptype)

### symbol[​](#symbol)
• symbol: `string`

Symbol identifier

#### Overrides[​](#overrides-2)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#symbol)

### takeProfit[​](#takeprofit)
• `Optional` takeProfit: `number`

Order Take Profit (Brackets)

#### Inherited from[​](#inherited-from-8)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[takeProfit](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#takeprofit)

### trailingStopPips[​](#trailingstoppips)
• `Optional` trailingStopPips: `number`

Order Trailing stop (Brackets)

#### Inherited from[​](#inherited-from-9)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[trailingStopPips](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#trailingstoppips)

### type[​](#type)
• type: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)

Order Type

#### Overrides[​](#overrides-3)
[OrderTemplateBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase).[type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase#type)

- [Hierarchy](#hierarchy)- [Properties](#properties)[currentQuotes](#currentquotes)- [customFields](#customfields)- [duration](#duration)- [guaranteedStop](#guaranteedstop)- [isClose](#isclose)- [limitPrice](#limitprice)- [qty](#qty)- [side](#side)- [stopLoss](#stoploss)- [stopPrice](#stopprice)- [stopType](#stoptype)- [symbol](#symbol)- [takeProfit](#takeprofit)- [trailingStopPips](#trailingstoppips)- [type](#type)