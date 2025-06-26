---
title: "Interface: DatafeedConfiguration | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedConfiguration"
extracted_at: "2025-06-22T09:51:47.993Z"
---

- [](/charting-library-docs/)- Interfaces- DatafeedConfigurationOn this page# Interface: DatafeedConfiguration[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).DatafeedConfiguration

Datafeed configuration data.
Pass the resulting array of properties as a parameter to [OnReadyCallback](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#onreadycallback) of the [`onReady`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#onready) method.
## Properties[​](#properties)
### currency_codes[​](#currency_codes)
• `Optional` currency_codes: (`string` | [`CurrencyItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.CurrencyItem))[]

Supported currencies for currency conversion.

When a currency code is supplied as a string then the library will automatically convert it to `{ id: value, code: value }` object.

`Example`

```
`["USD", "EUR", "GBP"]`
```
`Example`

```
`[{ id: "USD", code: "USD", description: "$" }, { id: "EUR", code: "EUR", description: "€" }]`
```

### exchanges[​](#exchanges)
• `Optional` exchanges: [`Exchange`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Exchange)[]

List of exchange descriptors.
An empty array leads to an absence of the exchanges filter in the Symbol Search list.
Use `value=''` if you wish to include all exchanges.

### supported_resolutions[​](#supported_resolutions)
• `Optional` supported_resolutions: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#resolutionstring)[]

List of [resolutions](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution) that the chart should support.
Each item of the array is expected to be a string that has a specific [format](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-format).
If you set this property to `undefined` or an empty array, the Resolution drop-down menu displays the list of resolutions available for
the current symbol ([LibrarySymbolInfo.supported_resolutions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo#supported_resolutions)).
`Example`

```
`["1", "15", "240", "D", "6M"]` will give you "1 minute, 15 minutes, 4 hours, 1 day, 6 months" in the _Resolution_ drop-down menu.
```

### supports_marks[​](#supports_marks)
• `Optional` supports_marks: `boolean`

Does the datafeed supports marks on bars (`true`), or not (`false | undefined`).

### supports_time[​](#supports_time)
• `Optional` supports_time: `boolean`

Set this one to `true` if your datafeed provides server time (unix time). It is used to adjust Countdown on the Price scale.

### supports_timescale_marks[​](#supports_timescale_marks)
• `Optional` supports_timescale_marks: `boolean`

Does the datafeed supports marks on the timescale (`true`), or not (`false | undefined`).

### symbols_grouping[​](#symbols_grouping)
• `Optional` symbols_grouping: `Record`<`string`, `string`>

Set it if you want to group symbols in the [Symbol Search](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Search).
Represents an object where keys are symbol types SymbolType and values are regular expressions (each regular expression should divide an instrument name into 2 parts: a root and an expiration).
Sample:

```
{  "futures": `/^(.+)([12]!|[FGHJKMNQUVXZ]\d{1,2})$/`,  "stock": `/^(.+)([12]!|[FGHJKMNQUVXZ]\d{1,2})$/`,}
```
It will be applied to the instruments with futures and stock as a type.
Refer to [Symbol grouping](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Search#symbol-grouping) for more information.

### symbols_types[​](#symbols_types)
• `Optional` symbols_types: [`DatafeedSymbolType`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedSymbolType)[]

List of filter descriptors.

Setting this property to `undefined` or an empty array leads to the absence of filter types in Symbol Search list. Use `value = ''` if you wish to include all filter types.
`value` within the descriptor will be passed as `symbolType` argument to [IDatafeedChartApi.searchSymbols](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.IDatafeedChartApi#searchsymbols)

### units[​](#units)
• `Optional` units: `Record`<`string`, [`Unit`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Unit)[]>

Supported unit groups. Each group can have several unit objects.

`Example`

```
{    weight: [        { id: 'kg', name: 'kg', description: 'Kilograms' },        { id: 'lb', name: 'lb', description: 'Pounds'},    ]}
```- [Properties](#properties)[currency_codes](#currency_codes)- [exchanges](#exchanges)- [supported_resolutions](#supported_resolutions)- [supports_marks](#supports_marks)- [supports_time](#supports_time)- [supports_timescale_marks](#supports_timescale_marks)- [symbols_grouping](#symbols_grouping)- [symbols_types](#symbols_types)- [units](#units)