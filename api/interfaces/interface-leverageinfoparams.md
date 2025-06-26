---
title: "Interface: LeverageInfoParams | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams"
extracted_at: "2025-06-22T09:55:10.483Z"
---

- [](/charting-library-docs/)- Interfaces- LeverageInfoParamsOn this page# Interface: LeverageInfoParams[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).LeverageInfoParams

An API object representing an order. Used when requesting leverage information from a broker.

## Hierarchy[​](#hierarchy)

`LeverageInfoParams`

↳ [`LeverageSetParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageSetParams)

## Properties[​](#properties)
### customFields[​](#customfields)
• `Optional` customFields: [`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldsValues)

Custom data for the broker.

### orderType[​](#ordertype)
• orderType: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)

The type of the order.

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

The order side. Buy or sell.

### symbol[​](#symbol)
• symbol: `string`

The order symbol.

- [Hierarchy](#hierarchy)- [Properties](#properties)[customFields](#customfields)- [orderType](#ordertype)- [side](#side)- [symbol](#symbol)