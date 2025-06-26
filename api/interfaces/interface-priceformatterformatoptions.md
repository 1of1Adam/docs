---
title: "Interface: PriceFormatterFormatOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.PriceFormatterFormatOptions"
extracted_at: "2025-06-22T09:56:09.813Z"
---

- [](/charting-library-docs/)- Interfaces- PriceFormatterFormatOptionsOn this page# Interface: PriceFormatterFormatOptions[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).PriceFormatterFormatOptions

Format options

## Hierarchy[​](#hierarchy)

[`SymbolValueFormatterFormatOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolValueFormatterFormatOptions)

↳ `PriceFormatterFormatOptions`

## Properties[​](#properties)
### cutFractionalByPrecision[​](#cutfractionalbyprecision)
• `Optional` cutFractionalByPrecision: `boolean`

Cuts price by priceScalePrecision, without rounding

### ignoreLocaleNumberFormat[​](#ignorelocalenumberformat)
• `Optional` ignoreLocaleNumberFormat: `boolean`

Ignore locale number format settings like decimal/thousands separators

#### Inherited from[​](#inherited-from)
[SymbolValueFormatterFormatOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolValueFormatterFormatOptions).[ignoreLocaleNumberFormat](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolValueFormatterFormatOptions#ignorelocalenumberformat)

### removeAllEndingZeros[​](#removeallendingzeros)
• `Optional` removeAllEndingZeros: `boolean`

Remove all trailing zeroes in decimal part

### signNegative[​](#signnegative)
• `Optional` signNegative: `boolean`

Add minus sign to result string

### signPositive[​](#signpositive)
• `Optional` signPositive: `boolean`

Add plus sign to result string

#### Inherited from[​](#inherited-from-1)
[SymbolValueFormatterFormatOptions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolValueFormatterFormatOptions).[signPositive](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.SymbolValueFormatterFormatOptions#signpositive)

### tailSize[​](#tailsize)
• `Optional` tailSize: `number`

Add `tailSize` digits to fractional part of result string

### useRtlFormat[​](#usertlformat)
• `Optional` useRtlFormat: `boolean`

Use Right to left format

- [Hierarchy](#hierarchy)- [Properties](#properties)[cutFractionalByPrecision](#cutfractionalbyprecision)- [ignoreLocaleNumberFormat](#ignorelocalenumberformat)- [removeAllEndingZeros](#removeallendingzeros)- [signNegative](#signnegative)- [signPositive](#signpositive)- [tailSize](#tailsize)- [useRtlFormat](#usertlformat)