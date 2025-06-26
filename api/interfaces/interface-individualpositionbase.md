---
title: "Interface: IndividualPositionBase | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPositionBase"
extracted_at: "2025-06-22T09:55:03.704Z"
---

- [](/charting-library-docs/)- Interfaces- IndividualPositionBaseOn this page# Interface: IndividualPositionBase[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IndividualPositionBase

Describes an individual position.

## Hierarchy[​](#hierarchy)

`IndividualPositionBase`

↳ [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)

## Properties[​](#properties)
### date[​](#date)
• date: `number`

Individual position open date (UNIX timestamp in milliseconds)

### id[​](#id)
• id: `string`

Individual position ID. Usually id should be equal to brokerSymbol

### price[​](#price)
• price: `number`

Individual position price

### qty[​](#qty)
• qty: `number`

Individual position Quantity

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

Individual position Side

### symbol[​](#symbol)
• symbol: `string`

Symbol name

- [Hierarchy](#hierarchy)- [Properties](#properties)[date](#date)- [id](#id)- [price](#price)- [qty](#qty)- [side](#side)- [symbol](#symbol)