---
title: "Interface: StudyBandInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo"
extracted_at: "2025-06-22T09:45:42.444Z"
---

- [](/charting-library-docs/)- Interfaces- StudyBandInfoOn this page# Interface: StudyBandInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyBandInfo

A description of a study band.

## Hierarchy[​](#hierarchy)

`StudyBandInfo`

↳ [`StudyBandPreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandPreferences)

## Properties[​](#properties)
### id[​](#id)
• `Optional` `Readonly` id: `string`

Band ID. Used in [StudyFilledAreaInfo.objAId](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo#objaid) and [StudyFilledAreaInfo.objBId](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo#objbid).

`See`

StudyFilledAreaInfo

### isHidden[​](#ishidden)
• `Optional` `Readonly` isHidden: `boolean`

Band style inputs visibility flag. Used to hide the band from the style tab of study properties dialogs.

### name[​](#name)
• `Readonly` name: `string`

Band name.

### zorder[​](#zorder)
• `Optional` `Readonly` zorder: `number`

Band z-order.

- [Hierarchy](#hierarchy)- [Properties](#properties)[id](#id)- [isHidden](#ishidden)- [name](#name)- [zorder](#zorder)