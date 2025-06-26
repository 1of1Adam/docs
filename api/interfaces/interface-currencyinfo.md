---
title: "Interface: CurrencyInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CurrencyInfo"
extracted_at: "2025-06-22T09:35:17.641Z"
---

- [](/charting-library-docs/)- Interfaces- CurrencyInfoOn this page# Interface: CurrencyInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CurrencyInfo

Contains information on the currency currently displayed on the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale).
To get a `CurrencyInfo` instance, call the [IPriceScaleApi.currency](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPriceScaleApi#currency) method.
## Properties[​](#properties)
### currencies[​](#currencies)
• currencies: `string`[]

Available currencies for the price scale provided by the datafeed.

### originalCurrencies[​](#originalcurrencies)
• originalCurrencies: `string`[]

Original currencies for the price scale.

### selectedCurrency[​](#selectedcurrency)
• selectedCurrency: `string`

Returns the currently selected currency for the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale). Returns `null` if there are several different currencies on the scale.

### symbols[​](#symbols)
• symbols: `string`[]

Symbols on the price scale

- [Properties](#properties)[currencies](#currencies)- [originalCurrencies](#originalcurrencies)- [selectedCurrency](#selectedcurrency)- [symbols](#symbols)