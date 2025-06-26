---
title: "Interface: SingleBrokerMetaInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SingleBrokerMetaInfo"
extracted_at: "2025-06-22T09:56:13.551Z"
---

- [](/charting-library-docs/)- Interfaces- SingleBrokerMetaInfoOn this page# Interface: SingleBrokerMetaInfo[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).SingleBrokerMetaInfo

## Properties[​](#properties)
### configFlags[​](#configflags)
• configFlags: [`BrokerConfigFlags`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerConfigFlags)

Broker Configuration Flags

### customNotificationFields[​](#customnotificationfields)
• `Optional` customNotificationFields: `string`[]

Optional field. You can use it if you have custom fields in orders or positions that should be taken into account when showing notifications.

`Example`

if you have field `additionalType` in orders and you want the chart to show a notification when it is changed, you should set:

```
customNotificationFields: ['additionalType']
```

### customUI[​](#customui)
• `Optional` customUI: [`BrokerCustomUI`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerCustomUI)

This optional field can be used to replace the standard Order Ticket and the Add Protection dialogs with your own.
Values of the following two fields are functions that are called by the Trading Platform to show the dialogs. Each function shows a dialog and returns a `Promise` object that should be resolved when the operation is finished or cancelled.
NOTE: The returned `Promise` object should be resolved with either `true` or `false` value.

`Example`

```
customUI: {    showOrderDialog?: (order: Order, focus?: OrderTicketFocusControl) => Promise<boolean>;    showPositionDialog?: (position: Position | IndividualPosition, brackets: Brackets, focus?: OrderTicketFocusControl) => Promise<boolean>;    showCancelOrderDialog?: (order: Order) => Promise<boolean>;    showClosePositionDialog?: (position: Position | IndividualPosition) => Promise<boolean>;}
```

### durations[​](#durations)
• `Optional` durations: [`OrderDurationMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDurationMetaInfo)[]

List of order duration options that determine how long the order remains active.
Specifying `durations` enables a drop-down menu in the Order Ticket for supported orders.
Refer to [Enable Time in force menu](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-time-in-force-menu) for more information.
The objects have the following keys: `{ name, value, hasDatePicker?, hasTimePicker?, default?, supportedOrderTypes? }`.

### orderRules[​](#orderrules)
• `Optional` orderRules: [`OrderRule`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderRule)[]

Order Rules

- [Properties](#properties)[configFlags](#configflags)- [customNotificationFields](#customnotificationfields)- [customUI](#customui)- [durations](#durations)- [orderRules](#orderrules)