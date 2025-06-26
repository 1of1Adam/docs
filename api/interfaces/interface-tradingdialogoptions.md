---
title: "Interface: TradingDialogOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradingDialogOptions"
extracted_at: "2025-06-22T09:56:44.419Z"
---

- [](/charting-library-docs/)- Interfaces- TradingDialogOptionsOn this page# Interface: TradingDialogOptions[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).TradingDialogOptions

## Hierarchy[​](#hierarchy)

`TradingDialogOptions`

↳ [`OrderDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderDialogOptions)

↳ [`PositionDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionDialogOptions)

## Properties[​](#properties)
### customFields[​](#customfields)
• `Optional` customFields: [`TradingDialogCustomField`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tradingdialogcustomfield)[]

Custom fields that are displayed in the Order Ticket.
Refer to the [Add custom fields](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#add-custom-fields) section for more information.
Example

```
customFields: [    {        inputType: 'TextWithCheckBox',        id: '2410',        title: 'Digital Signature',        placeHolder: 'Enter your personal digital signature',        value: {            text: '',            checked: false,        },        customInfo: {            asterix: true,            checkboxTitle: 'Save',        },    }]
```- [Hierarchy](#hierarchy)- [Properties](#properties)[customFields](#customfields)