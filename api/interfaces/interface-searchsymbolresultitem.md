---
title: "Interface: SearchSymbolResultItem | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.SearchSymbolResultItem"
extracted_at: "2025-06-22T09:52:19.281Z"
---

- [](/charting-library-docs/)- Interfaces- SearchSymbolResultItemOn this page# Interface: SearchSymbolResultItem[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).SearchSymbolResultItem

[Symbol Search](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Search) result item.
Pass the resulting array of symbols as a parameter to [SearchSymbolsCallback](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#searchsymbolscallback) of the [`searchSymbols`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#searchsymbols) method.
`Example`

```
{	description: 'Apple Inc.',	exchange: 'NasdaqNM',	symbol: 'AAPL',	ticker: 'AAPL',	type: 'stock',}
```
## Properties[​](#properties)
### description[​](#description)
• description: `string`

Description

### exchange[​](#exchange)
• exchange: `string`

Exchange name

### exchange_logo[​](#exchange_logo)
• `Optional` exchange_logo: `string`

URL of image to be displayed as the logo for the exchange. The `show_exchange_logos` featureset needs to be enabled for this to be visible in the UI.

The image should ideally be square in dimension. You can use any image type which
the browser supports natively. Simple SVG images are recommended.
Examples:

- `https://yourserver.com/exchangeLogo.svg`
- `/images/myImage.png`
- `data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3...`
- `data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAASABIAAD/4...`

### logo_urls[​](#logo_urls)
• `Optional` logo_urls: [`string`, `string`] | [`string`]

URL of image/s to be displayed as the logo/s for the symbol. The `show_symbol_logos` featureset needs to be enabled for this to be visible in the UI.

- If a single url is returned then that url will solely be used to display the symbol logo.
If two urls are provided then the images will be displayed as two partially overlapping
circles with the first url appearing on top. This is typically used for FOREX where you would
like to display two country flags as the symbol logo.

The image/s should ideally be square in dimension. You can use any image type which
the browser supports natively. Simple SVG images are recommended.
Examples:

- `https://yourserver.com/symbolName.svg`
- `/images/myImage.png`
- `data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3...`
- `data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAASABIAAD/4...`

### symbol[​](#symbol)
• symbol: `string`

Short symbol name

### ticker[​](#ticker)
• `Optional` ticker: `string`

It is a unique identifier for a particular symbol in your [symbology](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology).

You should avoid using colons (":") in ticker values unless you are following the TradingView format: "NYSE:IBM". Using colons may cause unexpected behaviour and display bugs.

Corresponds with [LibrarySymbolInfo.ticker](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo#ticker).

### type[​](#type)
• type: `string`

Type of symbol

'stock' | 'futures' | 'forex' | 'index'

- [Properties](#properties)[description](#description)- [exchange](#exchange)- [exchange_logo](#exchange_logo)- [logo_urls](#logo_urls)- [symbol](#symbol)- [ticker](#ticker)- [type](#type)