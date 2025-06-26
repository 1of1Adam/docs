---
title: "Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomTableElementFormatter"
extracted_at: "2025-06-22T09:53:59.577Z"
---

- [](/charting-library-docs/)- Interfaces- CustomTableElementFormatterOn this page# Interface: CustomTableElementFormatter<T>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).CustomTableElementFormatter

## Type parameters[​](#type-parameters)
NameType`T`extends [`TableFormatterInputValues`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tableformatterinputvalues) = [`TableFormatterInputValues`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tableformatterinputvalues)
## Properties[​](#properties)
### formatElement[​](#formatelement)
• `Optional` formatElement: [`CustomTableFormatElementFunction`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#customtableformatelementfunction)<`T`>

Formatter to generate HTML element

### formatText[​](#formattext)
• formatText: [`TableFormatTextFunction`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tableformattextfunction)<`T`>

Formatter to generate text. Return an empty string if you don't need to display this

### isPriceFormatterNeeded[​](#ispriceformatterneeded)
• `Optional` isPriceFormatterNeeded: `boolean`

Allow usage of priceFormatter

### name[​](#name)
• name: [`FormatterName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#formattername)

Custom formatter name

- [Type parameters](#type-parameters)- [Properties](#properties)[formatElement](#formatelement)- [formatText](#formattext)- [isPriceFormatterNeeded](#ispriceformatterneeded)- [name](#name)