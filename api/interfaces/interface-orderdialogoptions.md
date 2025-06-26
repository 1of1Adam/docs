---
title: "Interface: OrderDialogOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDialogOptions"
extracted_at: "2025-06-22T09:55:27.080Z"
---

- [](/charting-library-docs/)- Interfaces- OrderDialogOptionsOn this page# Interface: OrderDialogOptions[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).OrderDialogOptions

## Hierarchy[​](#hierarchy)

[`TradingDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradingDialogOptions)

↳ `OrderDialogOptions`

## Properties[​](#properties)
### customFields[​](#customfields)
• `Optional` customFields: [`TradingDialogCustomField`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tradingdialogcustomfield)[]

Custom fields that are displayed in the Order Ticket.
Refer to the [Add custom fields](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#add-custom-fields) section for more information.
Example

```
customFields: [    {        inputType: 'TextWithCheckBox',        id: '2410',        title: 'Digital Signature',        placeHolder: 'Enter your personal digital signature',        value: {            text: '',            checked: false,        },        customInfo: {            asterix: true,            checkboxTitle: 'Save',        },    }]
```
#### Inherited from[​](#inherited-from)
[TradingDialogOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradingDialogOptions).[customFields](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradingDialogOptions#customfields)

### showTotal[​](#showtotal)
• `Optional` showTotal: `boolean`

Using this flag, you can change `Trade Value` to `Total` in the Order Info section of the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket).

- [Hierarchy](#hierarchy)- [Properties](#properties)[customFields](#customfields)- [showTotal](#showtotal)