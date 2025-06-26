---
title: "Interface: SingleBrokerMetaInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SingleBrokerMetaInfo"
extracted_at: "2025-06-22T09:30:18.191Z"
---

# Interface: SingleBrokerMetaInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).SingleBrokerMetaInfo

## Properties
### configFlags
• **configFlags**: [`BrokerConfigFlags`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags)

Broker Configuration Flags

### customNotificationFields
• `Optional` **customNotificationFields**: `string`

Optional field. You can use it if you have custom fields in orders or positions that should be taken into account when showing notifications.

**`Example`**

if you have field `additionalType` in orders and you want the chart to show a notification when it is changed, you should set:

```
customNotificationFields: ['additionalType']

```

### customUI
• `Optional` **customUI**: [`BrokerCustomUI`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerCustomUI)

This optional field can be used to replace the standard Order Ticket and the Add Protection dialogs with your own.
Values of the following two fields are functions that are called by the Trading Platform to show the dialogs. Each function shows a dialog and returns a `Promise` object that should be resolved when the operation is finished or cancelled.
**NOTE:** The returned `Promise` object should be resolved with either `true` or `false` value.

**`Example`**

```
customUI: {
    showOrderDialog?: (order: Order, focus?: OrderTicketFocusControl) => Promise<boolean>;
    showPositionDialog?: (position: Position | IndividualPosition, brackets: Brackets, focus?: OrderTicketFocusControl) => Promise<boolean>;
    showCancelOrderDialog?: (order: Order) => Promise<boolean>;
    showClosePositionDialog?: (position: Position | IndividualPosition) => Promise<boolean>;
}

```

### durations
• `Optional` **durations**: [`OrderDurationMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderDurationMetaInfo)

List of order duration options that determine how long the order remains active.
Specifying `durations` enables a drop-down menu in the Order Ticket for supported orders.
Refer to [Enable Time in force menu](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#enable-time-in-force-menu) for more information.
The objects have the following keys: `{ name, value, hasDatePicker?, hasTimePicker?, default?, supportedOrderTypes? }`.

### orderRules
• `Optional` **orderRules**: [`OrderRule`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderRule)

Order Rules