---
title: "Interface: WatchlistSettings | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WatchlistSettings"
extracted_at: "2025-06-22T09:50:35.187Z"
---

- [](/charting-library-docs/)- Interfaces- WatchlistSettingsOn this page# Interface: WatchlistSettings[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).WatchlistSettings

## Properties[​](#properties)
### default_symbols[​](#default_symbols)
• default_symbols: `string`[]

Sets the list of default symbols for watchlist.
Any item in the list which is prefixed with `###` will be considered a section divider in the watchlist.
`Default`

[]

Example:

```
default_symbols: ['###TOP SECTION', 'AAPL', 'IBM', '###SECOND SECTION', 'MSFT']
```

### readonly[​](#readonly)
• `Optional` readonly: `boolean`

Enables read-only mode for the watchlist.

`Default`

```
false
```- [Properties](#properties)[default_symbols](#default_symbols)- [readonly](#readonly)