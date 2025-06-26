---
title: "Interface: OrderPreviewResult | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderPreviewResult"
extracted_at: "2025-06-22T09:55:33.965Z"
---

- [](/charting-library-docs/)- Interfaces- OrderPreviewResultOn this page# Interface: OrderPreviewResult[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).OrderPreviewResult

Describes the result of the order preview.

## Properties[​](#properties)
### confirmId[​](#confirmid)
• `Optional` confirmId: `string`

Confirmation ID. A unique identifier that should be passed to `placeOrder` method

### errors[​](#errors)
• `Optional` errors: [`OrderPreviewMessage`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#orderpreviewmessage)[]

Error messages

### sections[​](#sections)
• sections: [`OrderPreviewSection`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderPreviewSection)[]

Order preview section

### warnings[​](#warnings)
• `Optional` warnings: [`OrderPreviewMessage`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#orderpreviewmessage)[]

Warning messages

- [Properties](#properties)[confirmId](#confirmid)- [errors](#errors)- [sections](#sections)- [warnings](#warnings)