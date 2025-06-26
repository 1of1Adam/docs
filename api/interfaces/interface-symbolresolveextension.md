---
title: "Interface: SymbolResolveExtension | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SymbolResolveExtension"
extracted_at: "2025-06-22T09:52:22.233Z"
---

- [](/charting-library-docs/)- Interfaces- SymbolResolveExtensionOn this page# Interface: SymbolResolveExtension[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).SymbolResolveExtension

Additional information about the Symbol's currency or unit

## Properties[​](#properties)
### currencyCode[​](#currencycode)
• `Optional` currencyCode: `string`

Indicates the currency for conversions if `currency_codes` configuration field is set,
and `currency_code` is provided in the original symbol information ([LibrarySymbolInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo)).
Read more about [currency conversion](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale#enable-currency-conversion).

### session[​](#session)
• `Optional` session: `string`

Trading session type, such as `"regular"` or `"extended"`, that the chart should currently display.

### unitId[​](#unitid)
• `Optional` unitId: `string`

Indicates the unit for conversion if `units` configuration
field is set and `unit_id` is provided in the original symbol information ([LibrarySymbolInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo)).- [Properties](#properties)[currencyCode](#currencycode)- [session](#session)- [unitId](#unitid)