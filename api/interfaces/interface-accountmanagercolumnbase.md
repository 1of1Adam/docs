---
title: "Interface: AccountManagerColumnBase<TFormatterName> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerColumnBase"
extracted_at: "2025-06-22T09:53:02.713Z"
---

- [](/charting-library-docs/)- Interfaces- AccountManagerColumnBaseOn this page# Interface: AccountManagerColumnBase<TFormatterName>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).AccountManagerColumnBase

Column properties for the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) pages.

## Type parameters[​](#type-parameters)
NameType`TFormatterName`extends [`StandardFormatterName`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StandardFormatterName) | [`FormatterName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#formattername)
## Properties[​](#properties)
### alignment[​](#alignment)
• `Optional` alignment: [`CellAlignment`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#cellalignment)

Horizontal alignment of the cell value. The default value is `left`.

AlignmentDescriptionleftIt aligns the cell value to the left.rightIt aligns the cell value to the right.

### dataFields[​](#datafields)
• dataFields: `TFormatterName` extends [`StandardFormatterName`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StandardFormatterName) ? [`StandardFormattersDependenciesMapping`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.StandardFormattersDependenciesMapping)[`TFormatterName`<`TFormatterName`>] : `string`[]

The `dataFields` array contains fields from an order/position data object.
`dataFields` is used to generate the values displayed in a column.
The displayed value in the column updates only when the corresponding values in the data object change.
If no [formatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerColumnBase#formatter) is specified, the displayed values will be space-separated in the column.
When a `formatter` is defined, it processes only the specified values.
If an empty array is assigned to `dataFields`, the `formatter` will receive the entire data object.
Example

- For a column with `dataFields` set as `['avgPrice', 'qty']`, the displayed value updates only when the `avgPrice` or `qty` values in the data object change.
- For a column with an empty `dataFields` array, the displayed value updates if any values in the data object change.

### formatter[​](#formatter)
• `Optional` formatter: `TFormatterName`

Defines a formatter to be applied for data formatting, which can either belong to the `StandardFormatterName` or `FormatterName` type.
If no specific formatter is set, the value is displayed as is.
Default formatter names are enumerated in [StandardFormatterName](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.StandardFormatterName).
Refer to the [Built-in formatters](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/value-formatters#built-in-formatters) section to see the full list of formatters.
You can also create custom formatters using the [AccountManagerInfo.customFormatters](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerInfo#customformatters) property.

### help[​](#help)
• `Optional` help: `string`

Tooltip string for the column.

### hideByDefault[​](#hidebydefault)
• `Optional` hideByDefault: `boolean`

Setting `hideByDefault` to `true` hides the column by default.

### highlightDiff[​](#highlightdiff)
• `Optional` highlightDiff: `boolean`

`highlightDiff` can be set with [`StandardFormatterName.FormatPrice`](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/value-formatters#formatPrice)
and [`StandardFormatterName.FormatPriceForexSup`](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/value-formatters#formatPriceForexSup) formatters to highlight the changes of the field.
If `highlightDiff is `true`, the custom formatters will also get previous values.

### id[​](#id)
• id: `string`

Unique column identifier.

### isCapitalize[​](#iscapitalize)
• `Optional` isCapitalize: `boolean`

If set to `true`, the first character of every word in the sentence in the column
will be capitalized. The default value is `true`.

### label[​](#label)
• label: `string`

Column title. It will be displayed in the table's header row.

### notHideable[​](#nothideable)
• `Optional` notHideable: `boolean`

Setting `notHideable` to `true` prevents the column from being hidden.

### notSortable[​](#notsortable)
• `Optional` notSortable: `boolean`

When set to `true` will prevent column sorting.

### showZeroValues[​](#showzerovalues)
• `Optional` showZeroValues: `boolean`

Setting `showZeroValues` to `true` hides any zero values. The default value is `true`.

### sortProp[​](#sortprop)
• `Optional` sortProp: `string`

Data object key that is used for data sorting.

If `sortProp` is not provided, the first element of the `dataFields` array will be used.
If the `dataFields` array is empty, the column sorting will be unavailable.

### tooltipProperty[​](#tooltipproperty)
• `Optional` tooltipProperty: `string`

Key of the row object that is used to get the tooltip to display when hovering over a cell.
The tooltip property refers to an object whose keys are property names and
values are the corresponding tooltips.- [Type parameters](#type-parameters)- [Properties](#properties)[alignment](#alignment)- [dataFields](#datafields)- [formatter](#formatter)- [help](#help)- [hideByDefault](#hidebydefault)- [highlightDiff](#highlightdiff)- [id](#id)- [isCapitalize](#iscapitalize)- [label](#label)- [notHideable](#nothideable)- [notSortable](#notsortable)- [showZeroValues](#showzerovalues)- [sortProp](#sortprop)- [tooltipProperty](#tooltipproperty)