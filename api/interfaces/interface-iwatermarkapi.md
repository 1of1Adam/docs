---
title: "Interface: IWatermarkApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatermarkApi"
extracted_at: "2025-06-22T09:39:58.608Z"
---

- [](/charting-library-docs/)- Interfaces- IWatermarkApiOn this page# Interface: IWatermarkApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IWatermarkApi

An API object used to change the settings of the watermark.

## Methods[​](#methods)
### color[​](#color)
▸ color(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`string`>

Object that can be used to read/set/watch the color of the watermark text.

#### Returns[​](#returns)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`string`>

### setContentProvider[​](#setcontentprovider)
▸ setContentProvider(`provider`): `void`

Set a custom content provider for the watermark content.

#### Parameters[​](#parameters)
NameTypeDescription`provider`[`WatermarkContentProvider`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#watermarkcontentprovider)Custom watermark content provider, use `null` if you would like to revert back to the default content for the watermark.
#### Returns[​](#returns-1)
`void`

### visibility[​](#visibility)
▸ visibility(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Object that can be used to read/set/watch the visibility of the watermark.

#### Returns[​](#returns-2)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

- [Methods](#methods)[color](#color)- [setContentProvider](#setcontentprovider)- [visibility](#visibility)