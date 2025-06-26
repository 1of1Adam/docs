---
title: "Interface: OrderDurationMetaInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDurationMetaInfo"
extracted_at: "2025-06-22T09:55:30.593Z"
---

- [](/charting-library-docs/)- Interfaces- OrderDurationMetaInfoOn this page# Interface: OrderDurationMetaInfo[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).OrderDurationMetaInfo

Order duration options that determine how long the order remains active.
Refer to [Enable Time in force menu](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-time-in-force-menu) for more information.
## Properties[​](#properties)
### default[​](#default)
• `Optional` default: `boolean`

Default duration.
Only one duration object in the durations array can have a `true` value for this field.
The default duration will be used when the user places orders in the silent mode and it will be the selected one when the user opens Order Ticket for the first time.

### hasDatePicker[​](#hasdatepicker)
• `Optional` hasDatePicker: `boolean`

If it is set to `true`, then the Display date control in Order Ticket for this duration type will be displayed.

### hasTimePicker[​](#hastimepicker)
• `Optional` hasTimePicker: `boolean`

If it is set to `true`, then the Display time control in Order Ticket for this duration type will be displayed.

### name[​](#name)
• name: `string`

Localized title of the duration. The title will be displayed in the Duration control of Order Ticket.

### supportedOrderTypes[​](#supportedordertypes)
• `Optional` supportedOrderTypes: [`OrderType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderType)[]

A list of order types for which this duration type will be displayed in the Duration control of Order Ticket. Default value is `[OrderType.Limit, OrderType.Stop, OrderType.StopLimit]`.

### value[​](#value)
• value: `string`

Duration identifier

- [Properties](#properties)[default](#default)- [hasDatePicker](#hasdatepicker)- [hasTimePicker](#hastimepicker)- [name](#name)- [supportedOrderTypes](#supportedordertypes)- [value](#value)