---
title: "Interface: OrderPreviewSection | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderPreviewSection"
extracted_at: "2025-06-22T09:55:39.070Z"
---

- [](/charting-library-docs/)- Interfaces- OrderPreviewSectionOn this page# Interface: OrderPreviewSection[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).OrderPreviewSection

Describes a single order preview section.
Order preview can have multiple sections that are divided by separators and may have titles.
## Properties[​](#properties)
### header[​](#header)
• `Optional` header: `string`

Optional title of the section.

### rows[​](#rows)
• rows: [`OrderPreviewSectionRow`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderPreviewSectionRow)[]

Order preview items. Each item is a row of the section table.

- [Properties](#properties)[header](#header)- [rows](#rows)