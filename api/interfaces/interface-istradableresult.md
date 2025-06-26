---
title: "Interface: IsTradableResult | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IsTradableResult"
extracted_at: "2025-06-22T09:55:07.071Z"
---

- [](/charting-library-docs/)- Interfaces- IsTradableResultOn this page# Interface: IsTradableResult[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IsTradableResult

Show a custom message with the reason why the symbol cannot be traded

## Properties[​](#properties)
### reason[​](#reason)
• `Optional` reason: `string`

Reason is displayed in Order Ticket

### shortReason[​](#shortreason)
• `Optional` shortReason: `string`

shortReason is displayed in the legend

### solutions[​](#solutions)
• `Optional` solutions: [`TradableSolutions`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tradablesolutions)

Solution available to user to resolve the issue

### tradable[​](#tradable)
• tradable: `boolean`

Is the symbol tradable

- [Properties](#properties)[reason](#reason)- [shortReason](#shortreason)- [solutions](#solutions)- [tradable](#tradable)