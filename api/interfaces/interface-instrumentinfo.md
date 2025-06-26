---
title: "Interface: InstrumentInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.InstrumentInfo"
extracted_at: "2025-06-22T09:55:05.306Z"
---

- [](/charting-library-docs/)- Interfaces- InstrumentInfoOn this page# Interface: InstrumentInfo[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).InstrumentInfo

## Properties[​](#properties)
### allowedDurations[​](#alloweddurations)
• `Optional` allowedDurations: `string`[]

Array of strings with valid duration values. You can check that in Order Ticket.

### allowedOrderTypes[​](#allowedordertypes)
• `Optional` allowedOrderTypes: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)[]

Supported order types for the instrument

### baseCurrency[​](#basecurrency)
• `Optional` baseCurrency: `string`

The first currency quoted in a currency pair. Used for crypto currencies only.

### bigPointValue[​](#bigpointvalue)
• `Optional` bigPointValue: `number`

The value represented by a full point of price movement in the contract currency. This value is used to calculate the Total Value (symbol currency) of the order.

### brokerSymbol[​](#brokersymbol)
• `Optional` brokerSymbol: `string`

Display name for the symbol

### currency[​](#currency)
• `Optional` currency: `string`

Instrument currency that is displayed in Order Ticket

### description[​](#description)
• description: `string`

A description to be displayed in the UI dialogs.

### leverage[​](#leverage)
• `Optional` leverage: `string`

Leverage

### limitPriceStep[​](#limitpricestep)
• `Optional` limitPriceStep: `number`

Minimal price change for limit price field of the Limit and Stop Limit order. If set it will override the `minTick` value.

### lotSize[​](#lotsize)
• `Optional` lotSize: `number`

Lot size

### marginRate[​](#marginrate)
• `Optional` marginRate: `number`

The margin requirement for the instrument. A 3% margin rate should be represented as 0.03.

### minTick[​](#mintick)
• minTick: `number`

Minimal price change (e.g., 0.00001 for EURUSD). Used for price fields.

### pipSize[​](#pipsize)
• pipSize: `number`

Size of 1 pip (e.g., 0.0001 for EURUSD)

### pipValue[​](#pipvalue)
• pipValue: `number`

Value of 1 pip for the instrument in the account currency

### priceMagnifier[​](#pricemagnifier)
• `Optional` priceMagnifier: `number`

The value represents how much price is multiplied in relation to base monetary unit.

### qty[​](#qty)
• qty: [`QuantityMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.QuantityMetainfo)

Quantity field step and boundaries

### quoteCurrency[​](#quotecurrency)
• `Optional` quoteCurrency: `string`

The second currency quoted in a currency pair. Used for crypto currencies only.

### stopPriceStep[​](#stoppricestep)
• `Optional` stopPriceStep: `number`

Minimal price change for stop price field of the Stop and Stop Limit order. If set it will override the `minTick` value.

### type[​](#type)
• `Optional` type: [`SymbolType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#symboltype)

Instrument type. `forex` enables negative pips. You can check that in Order Ticket.

### units[​](#units)
• `Optional` units: `string`

Units of quantity or amount. Displayed instead of the Units label in the Quantity/Amount field.

### variableMinTick[​](#variablemintick)
• `Optional` variableMinTick: `string`

Dynamic minimum price movement.
It is used if the instrument's minimum price movement changes depending on the price range.
For example: `0.01 10 0.02 25 0.05`, where `minTick` is `0.01` for a price less than `10`, `minTick` is `0.02` for a price less than `25`, `minTick` is `0.05` for a price more and equal than `25`.

- [Properties](#properties)[allowedDurations](#alloweddurations)- [allowedOrderTypes](#allowedordertypes)- [baseCurrency](#basecurrency)- [bigPointValue](#bigpointvalue)- [brokerSymbol](#brokersymbol)- [currency](#currency)- [description](#description)- [leverage](#leverage)- [limitPriceStep](#limitpricestep)- [lotSize](#lotsize)- [marginRate](#marginrate)- [minTick](#mintick)- [pipSize](#pipsize)- [pipValue](#pipvalue)- [priceMagnifier](#pricemagnifier)- [qty](#qty)- [quoteCurrency](#quotecurrency)- [stopPriceStep](#stoppricestep)- [type](#type)- [units](#units)- [variableMinTick](#variablemintick)