---
title: "Interface: IndividualPosition | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition"
extracted_at: "2025-06-22T09:55:01.884Z"
---

- [](/charting-library-docs/)- Interfaces- IndividualPositionOn this page# Interface: IndividualPosition[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IndividualPosition

Describes an individual position.

## Hierarchy[​](#hierarchy)

[`IndividualPositionBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase)

[`CustomFields`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFields)

↳ `IndividualPosition`

## Properties[​](#properties)
### date[​](#date)
• date: `number`

Individual position open date (UNIX timestamp in milliseconds)

#### Inherited from[​](#inherited-from)
[IndividualPositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase).[date](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase#date)

### id[​](#id)
• id: `string`

Individual position ID. Usually id should be equal to brokerSymbol

#### Inherited from[​](#inherited-from-1)
[IndividualPositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase#id)

### price[​](#price)
• price: `number`

Individual position price

#### Inherited from[​](#inherited-from-2)
[IndividualPositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase).[price](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase#price)

### qty[​](#qty)
• qty: `number`

Individual position Quantity

#### Inherited from[​](#inherited-from-3)
[IndividualPositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase).[qty](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase#qty)

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

Individual position Side

#### Inherited from[​](#inherited-from-4)
[IndividualPositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase).[side](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase#side)

### symbol[​](#symbol)
• symbol: `string`

Symbol name

#### Inherited from[​](#inherited-from-5)
[IndividualPositionBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase).[symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase#symbol)

- [Hierarchy](#hierarchy)- [Properties](#properties)[date](#date)- [id](#id)- [price](#price)- [qty](#qty)- [side](#side)- [symbol](#symbol)