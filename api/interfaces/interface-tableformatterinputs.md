---
title: "Interface: TableFormatterInputs<T> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TableFormatterInputs"
extracted_at: "2025-06-22T09:56:28.364Z"
---

- [](/charting-library-docs/)- Interfaces- TableFormatterInputsOn this page# Interface: TableFormatterInputs<T>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).TableFormatterInputs

## Type parameters[​](#type-parameters)
NameType`T`extends [`TableFormatterInputValues`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tableformatterinputvalues) = [`TableFormatterInputValues`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#tableformatterinputvalues)
## Properties[​](#properties)
### prevValues[​](#prevvalues)
• `Optional` prevValues: `Partial`<`T` extends [...args: A[]] ? [...A[]] : `never`>

Optional field. It is array of previous values so you can compare and format accordingly. It exists if current column has the `highlightDiff: true` key.

### values[​](#values)
• values: `T` extends [...args: A[]] ? [...A[]] : `never`

Array of values to be formatted. Values are obtained by extracting dependent properties from the data object.

- [Type parameters](#type-parameters)- [Properties](#properties)[prevValues](#prevvalues)- [values](#values)