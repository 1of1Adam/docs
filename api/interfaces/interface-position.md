---
title: "Interface: Position | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position"
extracted_at: "2025-06-22T09:56:00.620Z"
---

- [](/charting-library-docs/)- Interfaces- PositionOn this page# Interface: Position[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).Position

Describes a single position.

## Hierarchy[​](#hierarchy)

[`PositionBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase)

[`CustomFields`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFields)

↳ `Position`

## Properties[​](#properties)
### avgPrice[​](#avgprice)
• avgPrice: `number`

The weighted average price of all positions for a symbol.
The library uses this value to draw a position line on the chart.
#### Inherited from[​](#inherited-from)
[PositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase).[avgPrice](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase#avgprice)

### id[​](#id)
• id: `string`

Position ID. Usually id should be equal to brokerSymbol

#### Inherited from[​](#inherited-from-1)
[PositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase#id)

### longQty[​](#longqty)
• `Optional` longQty: `number`

Long position quantity

#### Inherited from[​](#inherited-from-2)
[PositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase).[longQty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase#longqty)

### message[​](#message)
• `Optional` message: [`OrderOrPositionMessage`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderOrPositionMessage)

Message describing the state of the position

#### Inherited from[​](#inherited-from-3)
[PositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase).[message](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase#message)

### qty[​](#qty)
• qty: `number`

Position Quantity (positive number)

#### Inherited from[​](#inherited-from-4)
[PositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase).[qty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase#qty)

### shortQty[​](#shortqty)
• `Optional` shortQty: `number`

Short position quantity

#### Inherited from[​](#inherited-from-5)
[PositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase).[shortQty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase#shortqty)

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

Position Side

#### Inherited from[​](#inherited-from-6)
[PositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase).[side](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase#side)

### symbol[​](#symbol)
• symbol: `string`

Symbol name

#### Inherited from[​](#inherited-from-7)
[PositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase).[symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionBase#symbol)

- [Hierarchy](#hierarchy)- [Properties](#properties)[avgPrice](#avgprice)- [id](#id)- [longQty](#longqty)- [message](#message)- [qty](#qty)- [shortQty](#shortqty)- [side](#side)- [symbol](#symbol)