---
title: "Interface: PeriodParams | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.PeriodParams"
extracted_at: "2025-06-22T09:52:10.536Z"
---

- [](/charting-library-docs/)- Interfaces- PeriodParamsOn this page# Interface: PeriodParams[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).PeriodParams

Parameters passed to getBars

## Properties[​](#properties)
### countBack[​](#countback)
• countBack: `number`

The exact amount of bars to load, should be considered a higher priority than `from` if your datafeed supports it

### firstDataRequest[​](#firstdatarequest)
• firstDataRequest: `boolean`

Used to identify if it's the first call of getBars

### from[​](#from)
• from: `number`

Unix timestamp (leftmost requested bar)

### to[​](#to)
• to: `number`

Unix timestamp (rightmost requested bar - not inclusive)

- [Properties](#properties)[countBack](#countback)- [firstDataRequest](#firstdatarequest)- [from](#from)- [to](#to)