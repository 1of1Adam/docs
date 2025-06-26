---
title: "Interface: SetVisibleRangeOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SetVisibleRangeOptions"
extracted_at: "2025-06-22T09:45:08.379Z"
---

- [](/charting-library-docs/)- Interfaces- SetVisibleRangeOptionsOn this page# Interface: SetVisibleRangeOptions[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).SetVisibleRangeOptions

Options for setting the visible range.

Setting `applyDefaultRightMargin` or `percentRightMargin` will result in the `to` value
of the range specified being ignored and the timestamp of the latest bar on the chart
being used instead.
## Properties[​](#properties)
### applyDefaultRightMargin[​](#applydefaultrightmargin)
• `Optional` applyDefaultRightMargin: `boolean`

Apply the default right offset (margin) when setting the range.

### percentRightMargin[​](#percentrightmargin)
• `Optional` percentRightMargin: `number`

Apply a percentage right offset (margin) when setting the range.

### rejectByTimeout[​](#rejectbytimeout)
• `Optional` rejectByTimeout: `number`

In the current implementation, we cannot capture all errors during the `SetVisibleRange` process,
which means we cannot guarantee that the process will always be resolved or rejected.
To address this issue, you can use the `rejectByTimeout` option to ensure rejection after a specified timeout.- [Properties](#properties)[applyDefaultRightMargin](#applydefaultrightmargin)- [percentRightMargin](#percentrightmargin)- [rejectByTimeout](#rejectbytimeout)