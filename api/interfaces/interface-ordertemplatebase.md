---
title: "Interface: OrderTemplateBase | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplateBase"
extracted_at: "2025-06-22T09:55:46.273Z"
---

- [](/charting-library-docs/)- Interfaces- OrderTemplateBaseOn this page# Interface: OrderTemplateBase[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).OrderTemplateBase

## Hierarchy[​](#hierarchy)

`OrderTemplateBase`

↳ [`OrderTemplate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplate)

↳ [`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PreOrder)

## Properties[​](#properties)
### currentQuotes[​](#currentquotes)
• `Optional` currentQuotes: `Required`<`Pick`<[`TradingQuotes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradingQuotes), `"ask"` | `"bid"`>>

Current Quotes

### customFields[​](#customfields)
• `Optional` customFields: [`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldsValues)

Custom input fields

### duration[​](#duration)
• `Optional` duration: [`OrderDuration`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDuration)

Duration or expiration of an order

### guaranteedStop[​](#guaranteedstop)
• `Optional` guaranteedStop: `number`

Order Guaranteed Stop loss (Brackets)

### limitPrice[​](#limitprice)
• `Optional` limitPrice: `number`

Order limit price

### qty[​](#qty)
• `Optional` qty: `number`

Order quantity

### side[​](#side)
• `Optional` side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

order / execution side

### stopLoss[​](#stoploss)
• `Optional` stopLoss: `number`

Order Stop loss (Brackets)

### stopPrice[​](#stopprice)
• `Optional` stopPrice: `number`

Order stop price

### stopType[​](#stoptype)
• `Optional` stopType: [`StopType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StopType)

Type of Stop Order

### symbol[​](#symbol)
• symbol: `string`

Symbol identifier

### takeProfit[​](#takeprofit)
• `Optional` takeProfit: `number`

Order Take Profit (Brackets)

### trailingStopPips[​](#trailingstoppips)
• `Optional` trailingStopPips: `number`

Order Trailing stop (Brackets)

### type[​](#type)
• `Optional` type: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)

Order Type

- [Hierarchy](#hierarchy)- [Properties](#properties)[currentQuotes](#currentquotes)- [customFields](#customfields)- [duration](#duration)- [guaranteedStop](#guaranteedstop)- [limitPrice](#limitprice)- [qty](#qty)- [side](#side)- [stopLoss](#stoploss)- [stopPrice](#stopprice)- [stopType](#stoptype)- [symbol](#symbol)- [takeProfit](#takeprofit)- [trailingStopPips](#trailingstoppips)- [type](#type)