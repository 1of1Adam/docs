---
title: "Interface: Execution | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Execution"
extracted_at: "2025-06-22T09:54:14.107Z"
---

- [](/charting-library-docs/)- Interfaces- ExecutionOn this page# Interface: Execution[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).Execution

Describes a single execution.
Execution is when a buy or sell order is completed for a financial instrument.
## Hierarchy[​](#hierarchy)

[`CustomFields`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFields)

↳ `Execution`

## Properties[​](#properties)
### commission[​](#commission)
• `Optional` commission: `number`

Commission amount for executed trade

### netAmount[​](#netamount)
• `Optional` netAmount: `number`

Net amount for executed trade

### price[​](#price)
• price: `number`

Execution price

### qty[​](#qty)
• qty: `number`

Execution Quantity

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

Execution Side

### symbol[​](#symbol)
• symbol: `string`

Symbol name

### time[​](#time)
• time: `number`

Time (unix timestamp in milliseconds)

- [Hierarchy](#hierarchy)- [Properties](#properties)[commission](#commission)- [netAmount](#netamount)- [price](#price)- [qty](#qty)- [side](#side)- [symbol](#symbol)- [time](#time)