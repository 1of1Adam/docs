---
title: "Interface: StudyFilledAreaInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo"
extracted_at: "2025-06-22T09:46:23.185Z"
---

- [](/charting-library-docs/)- Interfaces- StudyFilledAreaInfoOn this page# Interface: StudyFilledAreaInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyFilledAreaInfo

A description of a study filled area.

## Properties[​](#properties)
### bottomColor[​](#bottomcolor)
• `Optional` `Readonly` bottomColor: `string`

Color for the bottom of the filled area.

### bottomValue[​](#bottomvalue)
• `Optional` `Readonly` bottomValue: `number`

Value at which the bottom of the filled area is drawn.

`Example`

```
75 // Drawn at price = 75
```

### fillToIntersection[​](#filltointersection)
• `Optional` `Readonly` fillToIntersection: `boolean`

Should the area be filled up to the point that two plots intersect, instead of by plot index?

Used for plot_plot filled area types.

### fillgaps[​](#fillgaps)
• `Optional` `Readonly` fillgaps: `boolean`

Should gaps in the area be filled?

### id[​](#id)
• `Readonly` id: `string`

Study ID.

### isHidden[​](#ishidden)
• `Optional` `Readonly` isHidden: `boolean`

Filled area's style inputs visibility flag. Used to hide the band from the style tab of study properties dialogs.

### objAId[​](#objaid)
• `Readonly` objAId: `string`

Study band ID.

`See`

StudyBandInfo

### objBId[​](#objbid)
• `Readonly` objBId: `string`

Study band ID.

`See`

StudyBandInfo

### palette[​](#palette)
• `Optional` `Readonly` palette: `string`

Color palette ID.

### title[​](#title)
• `Readonly` title: `string`

Title that will appear in the styles tab of the study settings dialog.

### topColor[​](#topcolor)
• `Optional` `Readonly` topColor: `string`

Color for the top of the filled area.

### topValue[​](#topvalue)
• `Optional` `Readonly` topValue: `number`

Value at which the top of the filled area is drawn.

`Example`

```
75 // Drawn at price = 75
```

### type[​](#type)
• `Readonly` type: [`FilledAreaType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.FilledAreaType)

Filled area type.

### zorder[​](#zorder)
• `Optional` `Readonly` zorder: `number`

Filled area z-order.

- [Properties](#properties)[bottomColor](#bottomcolor)- [bottomValue](#bottomvalue)- [fillToIntersection](#filltointersection)- [fillgaps](#fillgaps)- [id](#id)- [isHidden](#ishidden)- [objAId](#objaid)- [objBId](#objbid)- [palette](#palette)- [title](#title)- [topColor](#topcolor)- [topValue](#topvalue)- [type](#type)- [zorder](#zorder)