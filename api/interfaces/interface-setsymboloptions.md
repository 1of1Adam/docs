---
title: "Interface: SetSymbolOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetSymbolOptions"
extracted_at: "2025-06-22T09:45:07.008Z"
---

- [](/charting-library-docs/)- Interfaces- SetSymbolOptionsOn this page# Interface: SetSymbolOptions[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).SetSymbolOptions

Options for setting a chart's symbol.

## Properties[​](#properties)
### dataReady[​](#dataready)
• `Optional` dataReady: () => `void`

An optional callback function. Called when the data for the new symbol has loaded.

#### Type declaration[​](#type-declaration)
▸ (): `void`

Returns[​](#returns)
`void`

### doNotActivateChart[​](#donotactivatechart)
• `Optional` doNotActivateChart: `boolean`

A boolean flag. Allows to disable making the current chart active in the layout.

- [Properties](#properties)[dataReady](#dataready)- [doNotActivateChart](#donotactivatechart)