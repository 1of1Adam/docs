---
title: "Interface: PositionDialogOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PositionDialogOptions"
extracted_at: "2025-06-22T09:56:04.391Z"
---

- [](/charting-library-docs/)- Interfaces- PositionDialogOptionsOn this page# Interface: PositionDialogOptions[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).PositionDialogOptions

## Hierarchy[​](#hierarchy)

[`TradingDialogOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TradingDialogOptions)

↳ `PositionDialogOptions`

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

- [Hierarchy](#hierarchy)- [Properties](#properties)[customFields](#customfields)