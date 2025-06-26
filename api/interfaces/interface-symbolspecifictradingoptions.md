---
title: "Interface: SymbolSpecificTradingOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolSpecificTradingOptions"
extracted_at: "2025-06-22T09:56:24.873Z"
---

- [](/charting-library-docs/)- Interfaces- SymbolSpecificTradingOptionsOn this page# Interface: SymbolSpecificTradingOptions[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).SymbolSpecificTradingOptions

## Properties[​](#properties)
### allowedDurations[​](#alloweddurations)
• `Optional` allowedDurations: `string`[]

Array of strings with valid duration values. You can check that in Order Ticket.

### allowedOrderTypes[​](#allowedordertypes)
• `Optional` allowedOrderTypes: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)[]

Supported order types for the instrument.

### supportAddBracketsToExistingOrder[​](#supportaddbracketstoexistingorder)
• `Optional` supportAddBracketsToExistingOrder: `boolean`

Using this flag you can disable adding brackets to the existing order.

### supportBracketsInPips[​](#supportbracketsinpips)
• `Optional` supportBracketsInPips: `boolean`

Whether brackets could be set in ticks/pips.

`Default`

```
true
```

### supportIndividualPositionBrackets[​](#supportindividualpositionbrackets)
• `Optional` supportIndividualPositionBrackets: `boolean`

Whether trade brackets are supported for the symbol.
Defaults to the value in the config.

### supportModifyBrackets[​](#supportmodifybrackets)
• `Optional` supportModifyBrackets: `boolean`

Using this flag you can disable existing order's brackets modification. If you set it to `false`,
additional fields will be disabled in Order Ticket on the chart,

### supportModifyOrderBrackets[​](#supportmodifyorderbrackets)
• `Optional` supportModifyOrderBrackets: `boolean`

Whether the integration supports the modification of existing order brackets.

### supportModifyPositionBrackets[​](#supportmodifypositionbrackets)
• `Optional` supportModifyPositionBrackets: `boolean`

Whether the integration supports the modification of existing position brackets.

### supportOrderBrackets[​](#supportorderbrackets)
• `Optional` supportOrderBrackets: `boolean`

Whether order brackets are supported for the symbol.
Defaults to the value in the config.

### supportPositionBrackets[​](#supportpositionbrackets)
• `Optional` supportPositionBrackets: `boolean`

Whether position brackets are supported for the symbol.
Defaults to the value in the config.

### supportReversePosition[​](#supportreverseposition)
• `Optional` supportReversePosition: `boolean`

Whether position reversing is supported for the symbol.
Defaults to the value in the config.

### warningMessage[​](#warningmessage)
• `Optional` warningMessage: `string`

A symbol-specific message that can be used to warn users.

- [Properties](#properties)[allowedDurations](#alloweddurations)- [allowedOrderTypes](#allowedordertypes)- [supportAddBracketsToExistingOrder](#supportaddbracketstoexistingorder)- [supportBracketsInPips](#supportbracketsinpips)- [supportIndividualPositionBrackets](#supportindividualpositionbrackets)- [supportModifyBrackets](#supportmodifybrackets)- [supportModifyOrderBrackets](#supportmodifyorderbrackets)- [supportModifyPositionBrackets](#supportmodifypositionbrackets)- [supportOrderBrackets](#supportorderbrackets)- [supportPositionBrackets](#supportpositionbrackets)- [supportReversePosition](#supportreverseposition)- [warningMessage](#warningmessage)