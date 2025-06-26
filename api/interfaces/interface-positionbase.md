---
title: "Interface: PositionBase | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase"
extracted_at: "2025-06-22T09:56:02.423Z"
---

- [](/charting-library-docs/)- Interfaces- PositionBaseOn this page# Interface: PositionBase[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).PositionBase

Describes a single position.

## Hierarchy[​](#hierarchy)

`PositionBase`

↳ [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position)

## Properties[​](#properties)
### avgPrice[​](#avgprice)
• avgPrice: `number`

The weighted average price of all positions for a symbol.
The library uses this value to draw a position line on the chart.

### id[​](#id)
• id: `string`

Position ID. Usually id should be equal to brokerSymbol

### longQty[​](#longqty)
• `Optional` longQty: `number`

Long position quantity

### message[​](#message)
• `Optional` message: [`OrderOrPositionMessage`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderOrPositionMessage)

Message describing the state of the position

### qty[​](#qty)
• qty: `number`

Position Quantity (positive number)

### shortQty[​](#shortqty)
• `Optional` shortQty: `number`

Short position quantity

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

Position Side

### symbol[​](#symbol)
• symbol: `string`

Symbol name

- [Hierarchy](#hierarchy)- [Properties](#properties)[avgPrice](#avgprice)- [id](#id)- [longQty](#longqty)- [message](#message)- [qty](#qty)- [shortQty](#shortqty)- [side](#side)- [symbol](#symbol)