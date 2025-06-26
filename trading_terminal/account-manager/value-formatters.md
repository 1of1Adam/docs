---
title: "Value formatters | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/value-formatters"
extracted_at: "2025-06-22T09:29:23.878Z"
---

# Value formattersYou can determine how the values appear in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) tables by using the [`formatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountManagerColumnBase#formatter) property of [`AccountManagerColumnBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountManagerColumnBase).
If no `formatter` is set, values are displayed as they are, separated by spaces.
When a `formatter` is defined, it processes only the values specified in the `dataFields` property.
If `dataFields` is an empty array, the `formatter` will receive the entire [order](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder)/[position](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) data object.
```
// AccountManagerColumnBase object
{
    id: "limitPrice",
    label: "Limit Price",
    dataFields: ["limitPrice"],
    formatter: "formatPrice",   // Standard formatter that displays symbol's price
},

```
The `formatter` property can contain either `StandardFormatterName` or `FormatterName` object.

- `StandardFormatterName` refers to the [built-in formatters](#built-in-formatters).
- `FormatterName` is a general type that can be a built-in name or any other string corresponding to a [custom formatter](#custom-formatters).

## Formatter and dataFields dependency
The `formatter` property expects that the [`dataFields`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountManagerColumnBase#datafields) property has certain types of values defined in a specific order.
`dataFields` is an array of strings that match the property names in the [order](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder)/[position](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) data object.
The values for these properties in the data object are expected to be a number, string, date, etc.
The mapping of the `formatter` and `dataFields` values is described in the [`StandardFormattersDependenciesMapping`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StandardFormattersDependenciesMapping) interface.
### Example
Assume that your data object has two custom fields: `balance` and `currency`.

```
{
  // <...other object fields...>
  balance: 1000.00,
  currency: "EUR",
}

```
You want to display the user's balance in a column. The balance value should have two decimal places and a currency symbol.
For this purpose, you can use the built-in [`fixedInCurrency`](#fixedInCurrency) formatter that expects the following arguments:

- A number that represents the price.
- A string that represents the currency code.

This means that `dataFields` should have the values of the followings types: `[number, string]`.
Then, the `AccountManagerColumnBase` object for the balance column should look as follows:
```
{
    id: "balance",
    label: "Balance",
    dataFields: ["balance", "currency"],
    formatter: "fixedInCurrency",
},

```
## Built-in formatters
The table below lists the built-in formatter values, expected types of the properties within `dataFields`,
and the default fields of the [order](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder)/[position](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) data object.

 **|Name** | **Value** | **Description** ||
| Date[#](#date) | `"date"` | Displays the date or time.

 Expected data type: `[date]`. ||
| DateOrDateTime[#](#dateOrDateTime) | `"dateOrDateTime"` | Displays either the date or both the date and time. This formatter accepts an object in the following format: 
`{ dateOrDateTime: number, hasTime: boolean }`. 
If `hasTime` is set to `true`, both the date and time are displayed; otherwise, only the date is displayed.

 Expected data type: `[date]`. ||
| Default[#](#default) | `"default"` | Displays data as a string with space-separated values.

 Expected data type: `[string]`. ||
| Empty[#](#empty) | `"empty"` | Displays an empty string instead of a value.

 Expected data type: `[string]`. ||
| Fixed[#](#fixed) | `"fixed"` | Displays a number with two decimal places.

 Expected data type: `[number]`. 
Often used for the following `dataFields` values: `["balance"]` or `["equity"]`. ||
| FixedInCurrency[#](#fixedInCurrency) | `"fixedInCurrency"` | Displays a number with two decimal places and adds the currency symbol.

 Expected data types: `[number, string]`.
 Often used for the following `dataFields` values: `["balance", "currency"]` or `["equity", "currency"]`. ||
| FormatPrice[#](#formatPrice) | `"formatPrice"` | Displays a symbol's price.

 Expected data type: `[number]`. 
Often used for the following `dataFields` values: `["limitPrice"]`, `["stopPrice"]`, `["avgPrice"]`. ||
| FormatPriceForexSup[#](#formatPriceForexSup) | `"formatPriceForexSup"` | Displays the price of the symbol with the last character shown in superscript. This formatter works only if the instrument type is set to `forex`. 

 Expected data type: `[number]`. 
 Often used for the following `dataFields` values: `["last"]`. ||
| FormatPriceInCurrency[#](#formatPriceInCurrency) | `"formatPriceInCurrency"` | Displays a symbol's price and adds the currency symbol.

 Expected data type: `[number, string]`. 
 Often used for the following  `dataFields` values: `["limitPrice", "currency"]`, `["stopPrice", "currency"]`, `["avgPrice", "currency"]`. ||
| FormatQuantity[#](#formatQuantity) | `"formatQuantity"` | Displays an integer or floating-point quantity with a space to separate thousands groups. 

 Expected data type: `[number]`. 
 Often used for the following `dataFields` values: `["qty"]` or `["filledQty"]`. ||
| IntegerSeparated[#](#integerSeparated) | `"integerSeparated"` | Displays integer values with thousands separated by non-breaking spaces. 

 Expected data type: `[number]`. 
 Often used for the following `dataFields` values: `["qty"]` or `["filledQty"]`. ||
| LocalDate[#](#localDate) | `"localDate"` | Displays the local date or time.

 Expected data type: `[date]`. ||
| LocalDateOrDateTime[#](#localDateOrDateTime) | `"localDateOrDateTime"` | Displays either the date or both the date and time in the local time zone. This formatter accepts an object in the following format: 
`{ dateOrDateTime: number, hasTime: boolean }`. 
If `hasTime` is set to `true`, both the date and time are displayed; otherwise, only the date is displayed.

 Expected data type: `[date]`. ||
| MarginPercent[#](#marginPercent) | `"marginPercent"` | Displays numeric values as percentages. If the value is below `0.01`, the formatter returns the raw value with a percentage sign. If the value is non-finite, the formatter returns `"> 200%"`. If the value is undefined, the formatter returns an empty string.

 Expected data type: `[number]`. 
 Often used for the following `dataFields` value: `["marginRate"]`. ||
| Percentage[#](#percentage) | `"percentage"` | Displays numeric values as percentages.

 Expected data type: `[number]`. ||
| Pips[#](#pips) | `"pips"` | Displays numbers as pips.

 Expected data type: `[number]`. 
 Often used for the following `dataFields` value: `["pipValue"]`. ||
| PositionSide[#](#positionSide) | `"positionSide"` | Displays the position side: Short or Long.

 Expected data type: `[number]`. 
 Often used for the following `dataFields` value: `["side"]`. ||
| Profit[#](#profit) | `"profit"` | Displays profit in the account currency. It also adds the `+` (plus) sign, separates thousands, and changes the cell text color to red or green. 

 Expected data type: `[number]`. ||
| ProfitInInstrumentCurrency[#](#profitInInstrumentCurrency) | `"profitInInstrumentCurrency"` | Displays profit in the instrument currency. It also adds the `+` (plus) sign, separates thousands, and changes the cell text color to red or green.

 Expected data types: `[number, string]`. ||
| Side[#](#side) | `"side"` | Displays the order side: Sell or Buy. 

 Expected data type: `[number]`. 
 Often used for the following `dataFields` value: `["side"]`. ||
| Status[#](#status) | `"status"` | Formats the order status.

 Expected data type: `[number]`. 
 Often used for the following `dataFields` value: `["status"]`. ||
| Symbol[#](#symbol) | `"symbol"` | Displays `brokerSymbol` and is used for a symbol field. Note that when you click a symbol, the chart changes according to the symbol field. 

 Expected data types: `[string, string, string]`. 
 Often used for the following `dataFields` value: `["brokerSymbol", "symbol", "message"]`. ||
| Text[#](#text) | `"text"` | Displays a text value.

Expected data type: `[string]`. 
 Often used for the following `dataFields` value: `["message"]`. ||
| Type[#](#type) | `"type"` | Displays the order type: Limit / Stop / Stop-limit / Market.

Expected data types: `[number, string, number]`. Often used for the following `dataFields` values: `["type", "parentId", "stopType"]`. ||
| VariablePrecision[#](#variablePrecision) | `"variablePrecision"` | Displays a number with variable precision.

 Expected data type: `[number]`. 
 Often used for the following `dataFields` value: `["qty"]`. ||

## Custom formatters
You can implement your custom formatter using the [`customFormatters`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountManagerInfo#customformatters) property in the [`AccountManagerInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#accountmanagerinfo) object.
Each custom formatter is an object with the following fields.

 **|Property** | **Required** | **Description** ||
| `name`[#](#name) | Yes | Unique formatter name. You should typecast it to [`FormatterName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#formattername). ||
| `formatText`[#](#formatText) | Yes | A function that is used for formatting a cell value to string. `formatText` is required because it is used to generate exported data. However, if you choose not to display this data, you can return an empty string. ||
| `formatElement`[#](#formatElement) | No | A function that is used for formatting a cell value to a string or an HTML element. If the `formatElement` function is provided, it only handles the formatting of displayed values. Otherwise, the `formatText` function is used. For optimal performance, it is recommended to only use `formatText` if you intend to display only string values. ||
| `isPriceFormatterNeeded`[#](#isPriceFormatterNeeded) | No | Allows usage of `priceFormatter`. ||

### Example
The CodePen example below implements two custom formatters that display the following:

- Dynamically changing text
- A button

These formatters are used to format values for custom columns of the *Positions* page.

See the Pen 
Implementing custom formmaters for Account Manager columns by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).