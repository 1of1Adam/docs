---
title: "Interface: WatchedValueSubscribeOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.WatchedValueSubscribeOptions"
extracted_at: "2025-06-22T09:56:48.109Z"
---

- [](/charting-library-docs/)- Interfaces- WatchedValueSubscribeOptionsOn this page# Interface: WatchedValueSubscribeOptions[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).WatchedValueSubscribeOptions

## Properties[​](#properties)
### callWithLast[​](#callwithlast)
• `Optional` callWithLast: `boolean`

if it is set to true then the callback will be executed with the previous value (if available)

### once[​](#once)
• `Optional` once: `boolean`

Subscribe for only one update, and remove subscription afterwards. (the callback will be executed only once)

- [Properties](#properties)[callWithLast](#callwithlast)- [once](#once)