---
title: "Interface: DOMData | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DOMData"
extracted_at: "2025-06-22T09:54:00.851Z"
---

- [](/charting-library-docs/)- Interfaces- DOMDataOn this page# Interface: DOMData[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).DOMData

Depth of Market (Order Book) Data

## Properties[​](#properties)
### asks[​](#asks)
• asks: [`DOMLevel`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DOMLevel)[]

Ask order levels (must be sorted by `price` in ascending order)

### bids[​](#bids)
• bids: [`DOMLevel`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.DOMLevel)[]

Bid order levels (must be sorted by `price` in ascending order)

### snapshot[​](#snapshot)
• snapshot: `boolean`

Whether the Depth of Market data is a snapshot (has the full set of depth data).

- If `true` then the data contains the full set of depth data.
- If `false` then data only contains updated levels.
- [Properties](#properties)[asks](#asks)- [bids](#bids)- [snapshot](#snapshot)