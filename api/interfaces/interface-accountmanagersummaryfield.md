---
title: "Interface: AccountManagerSummaryField | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerSummaryField"
extracted_at: "2025-06-22T09:53:08.318Z"
---

- [](/charting-library-docs/)- Interfaces- AccountManagerSummaryFieldOn this page# Interface: AccountManagerSummaryField[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).AccountManagerSummaryField

Custom field that will always be shown above the pages of the Account manager

## Properties[​](#properties)
### formatter[​](#formatter)
• `Optional` formatter: [`StandardFormatterName`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StandardFormatterName)

Name of the formatter to be used for data formatting. If `formatter` is not
set the value is displayed as is. Formatter can be a default or a custom one.

### informerMessage[​](#informermessage)
• `Optional` informerMessage: `string`

An optional parameter with text explaining the contents of this field.

### isDefault[​](#isdefault)
• `Optional` isDefault: `boolean`

Optional parameter which can be set to display the field by default.

### text[​](#text)
• text: `string`

Text to display for the summary field

### wValue[​](#wvalue)
• wValue: [`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValueReadonly)<`any`>

A WatchedValue object that can be used to read the state of field.

- [Properties](#properties)[formatter](#formatter)- [informerMessage](#informermessage)- [isDefault](#isdefault)- [text](#text)- [wValue](#wvalue)