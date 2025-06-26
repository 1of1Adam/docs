---
title: "Interface: LeverageSetParams | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageSetParams"
extracted_at: "2025-06-22T09:55:17.676Z"
---

- [](/charting-library-docs/)- Interfaces- LeverageSetParamsOn this page# Interface: LeverageSetParams[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).LeverageSetParams

An API object representing an order and leverage. Used when requesting that a broker updates a order's leverage.

## Hierarchy[​](#hierarchy)

[`LeverageInfoParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams)

↳ `LeverageSetParams`

## Properties[​](#properties)
### customFields[​](#customfields)
• `Optional` customFields: [`CustomInputFieldsValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldsValues)

Custom data for the broker.

#### Inherited from[​](#inherited-from)
[LeverageInfoParams](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams).[customFields](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams#customfields)

### leverage[​](#leverage)
• leverage: `number`

The requested leverage value.

### orderType[​](#ordertype)
• orderType: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)

The type of the order.

#### Inherited from[​](#inherited-from-1)
[LeverageInfoParams](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams).[orderType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams#ordertype)

### side[​](#side)
• side: [`Side`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.Side)

The order side. Buy or sell.

#### Inherited from[​](#inherited-from-2)
[LeverageInfoParams](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams).[side](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams#side)

### symbol[​](#symbol)
• symbol: `string`

The order symbol.

#### Inherited from[​](#inherited-from-3)
[LeverageInfoParams](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams).[symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.LeverageInfoParams#symbol)

- [Hierarchy](#hierarchy)- [Properties](#properties)[customFields](#customfields)- [leverage](#leverage)- [orderType](#ordertype)- [side](#side)- [symbol](#symbol)