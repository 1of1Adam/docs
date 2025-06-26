---
title: "Interface: NumericFormattingParams | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.NumericFormattingParams"
extracted_at: "2025-06-22T09:41:59.965Z"
---

- [](/charting-library-docs/)- Interfaces- NumericFormattingParamsOn this page# Interface: NumericFormattingParams[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).NumericFormattingParams

Formatting options for numbers

## Properties[​](#properties)
### decimal_sign[​](#decimal_sign)
• decimal_sign: `string`

String that represents the decimal part of a number.
This character separates the integer part from the fractional part.
`Example`

```
"123.4" // Using a dot as the decimal sign
```
`Example`

```
"123,4" // Using a comma as the decimal sign
```
`Example`

```
"123'4" // Using an apostrophe as the decimal sign
```

### grouping_separator[​](#grouping_separator)
• grouping_separator: `string`

String that represents the grouping separator for large numbers.
This character separates groups of thousands to improve readability.
`Example`

```
"1 234.5" // Using a space as the grouping separator
```
`Example`

```
"1,234.5" // Using a comma as the grouping separator
```- [Properties](#properties)[decimal_sign](#decimal_sign)- [grouping_separator](#grouping_separator)