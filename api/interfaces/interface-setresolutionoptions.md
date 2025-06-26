---
title: "Interface: SetResolutionOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetResolutionOptions"
extracted_at: "2025-06-22T09:45:05.960Z"
---

- [](/charting-library-docs/)- Interfaces- SetResolutionOptionsOn this page# Interface: SetResolutionOptions[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).SetResolutionOptions

Options for setting a chart's resolution.

## Properties[​](#properties)
### dataReady[​](#dataready)
• `Optional` dataReady: () => `void`

An optional callback function. Called when the data for the new resolution has loaded.

#### Type declaration[​](#type-declaration)
▸ (): `void`

Returns[​](#returns)
`void`

### doNotActivateChart[​](#donotactivatechart)
• `Optional` doNotActivateChart: `boolean`

A boolean flag. Allows to disable making the current chart active in the layout.

- [Properties](#properties)[dataReady](#dataready)- [doNotActivateChart](#donotactivatechart)