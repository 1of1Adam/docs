---
title: "Interface: MomentumIndicatorOverrides | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MomentumIndicatorOverrides"
extracted_at: "2025-06-22T09:41:31.289Z"
---

- [](/charting-library-docs/)- Interfaces- MomentumIndicatorOverridesOn this page# Interface: MomentumIndicatorOverrides[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).MomentumIndicatorOverrides

Overrides for the 'Momentum' indicator.

Use these properties to customize indicator via [IChartWidgetApi.createStudy](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createstudy) and [IStudyApi.applyOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi#applyoverrides).

## Indexable[​](#indexable)
▪ [key: `string`]: [`StudyOverrideValueType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyoverridevaluetype)

## Properties[​](#properties)
### mom.color[​](#momcolor)
• mom.color: `string`

Default value: `#2196F3`

### mom.display[​](#momdisplay)
• mom.display: `number`

Default value: `15`

### mom.linestyle[​](#momlinestyle)
• mom.linestyle: `number`

Default value: `0`

### mom.linewidth[​](#momlinewidth)
• mom.linewidth: `number`

Default value: `1`

### mom.plottype[​](#momplottype)
• mom.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### mom.trackprice[​](#momtrackprice)
• mom.trackprice: `boolean`

Default value: `false`

### mom.transparency[​](#momtransparency)
• mom.transparency: `number`

Default value: `0`

### zero.color[​](#zerocolor)
• zero.color: `string`

Default value: `#787B86`

### zero.linestyle[​](#zerolinestyle)
• zero.linestyle: `number`

Default value: `2`

### zero.linewidth[​](#zerolinewidth)
• zero.linewidth: `number`

Default value: `1`

### zero.value[​](#zerovalue)
• zero.value: `number`

Default value: `0`

### zero.visible[​](#zerovisible)
• zero.visible: `boolean`

Default value: `true`

- [Indexable](#indexable)- [Properties](#properties)[mom.color](#momcolor)- [mom.display](#momdisplay)- [mom.linestyle](#momlinestyle)- [mom.linewidth](#momlinewidth)- [mom.plottype](#momplottype)- [mom.trackprice](#momtrackprice)- [mom.transparency](#momtransparency)- [zero.color](#zerocolor)- [zero.linestyle](#zerolinestyle)- [zero.linewidth](#zerolinewidth)- [zero.value](#zerovalue)- [zero.visible](#zerovisible)