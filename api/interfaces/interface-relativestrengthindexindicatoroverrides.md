---
title: "Interface: RelativeStrengthIndexIndicatorOverrides | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RelativeStrengthIndexIndicatorOverrides"
extracted_at: "2025-06-22T09:44:25.137Z"
---

- [](/charting-library-docs/)- Interfaces- RelativeStrengthIndexIndicatorOverridesOn this page# Interface: RelativeStrengthIndexIndicatorOverrides[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).RelativeStrengthIndexIndicatorOverrides

Overrides for the 'Relative Strength Index' indicator.

Use these properties to customize indicator via [IChartWidgetApi.createStudy](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createstudy) and [IStudyApi.applyOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi#applyoverrides).

## Indexable[​](#indexable)
▪ [key: `string`]: [`StudyOverrideValueType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyoverridevaluetype)

## Properties[​](#properties)
### hlines background.color[​](#hlines-backgroundcolor)
• hlines background.color: `string`

Default value: `#7E57C2`

### hlines background.transparency[​](#hlines-backgroundtransparency)
• hlines background.transparency: `number`

Default value: `90`

### hlines background.visible[​](#hlines-backgroundvisible)
• hlines background.visible: `boolean`

Default value: `true`

### lowerlimit.color[​](#lowerlimitcolor)
• lowerlimit.color: `string`

Default value: `#787B86`

### lowerlimit.linestyle[​](#lowerlimitlinestyle)
• lowerlimit.linestyle: `number`

Default value: `2`

### lowerlimit.linewidth[​](#lowerlimitlinewidth)
• lowerlimit.linewidth: `number`

Default value: `1`

### lowerlimit.value[​](#lowerlimitvalue)
• lowerlimit.value: `number`

Default value: `30`

### lowerlimit.visible[​](#lowerlimitvisible)
• lowerlimit.visible: `boolean`

Default value: `true`

### lowerlimit.zorder[​](#lowerlimitzorder)
• lowerlimit.zorder: `number`

Default value: `-1.111`

### middlelimit.color[​](#middlelimitcolor)
• middlelimit.color: `string`

Default value: `#787B86`

### middlelimit.linestyle[​](#middlelimitlinestyle)
• middlelimit.linestyle: `number`

Default value: `2`

### middlelimit.linewidth[​](#middlelimitlinewidth)
• middlelimit.linewidth: `number`

Default value: `1`

### middlelimit.value[​](#middlelimitvalue)
• middlelimit.value: `number`

Default value: `50`

### middlelimit.visible[​](#middlelimitvisible)
• middlelimit.visible: `boolean`

Default value: `true`

### middlelimit.zorder[​](#middlelimitzorder)
• middlelimit.zorder: `number`

Default value: `-1.11`

### plot.color[​](#plotcolor)
• plot.color: `string`

Default value: `#7E57C2`

### plot.display[​](#plotdisplay)
• plot.display: `number`

Default value: `15`

### plot.linestyle[​](#plotlinestyle)
• plot.linestyle: `number`

Default value: `0`

### plot.linewidth[​](#plotlinewidth)
• plot.linewidth: `number`

Default value: `1`

### plot.plottype[​](#plotplottype)
• plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### plot.trackprice[​](#plottrackprice)
• plot.trackprice: `boolean`

Default value: `false`

### plot.transparency[​](#plottransparency)
• plot.transparency: `number`

Default value: `0`

### smoothed ma.display[​](#smoothed-madisplay)
• smoothed ma.display: `number`

Default value: `0`

### smoothed ma.linestyle[​](#smoothed-malinestyle)
• smoothed ma.linestyle: `number`

Default value: `0`

### smoothed ma.linewidth[​](#smoothed-malinewidth)
• smoothed ma.linewidth: `number`

Default value: `1`

### smoothed ma.plottype[​](#smoothed-maplottype)
• smoothed ma.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### smoothed ma.trackprice[​](#smoothed-matrackprice)
• smoothed ma.trackprice: `boolean`

Default value: `false`

### smoothed ma.transparency[​](#smoothed-matransparency)
• smoothed ma.transparency: `number`

Default value: `0`

### upperlimit.color[​](#upperlimitcolor)
• upperlimit.color: `string`

Default value: `#787B86`

### upperlimit.linestyle[​](#upperlimitlinestyle)
• upperlimit.linestyle: `number`

Default value: `2`

### upperlimit.linewidth[​](#upperlimitlinewidth)
• upperlimit.linewidth: `number`

Default value: `1`

### upperlimit.value[​](#upperlimitvalue)
• upperlimit.value: `number`

Default value: `70`

### upperlimit.visible[​](#upperlimitvisible)
• upperlimit.visible: `boolean`

Default value: `true`

### upperlimit.zorder[​](#upperlimitzorder)
• upperlimit.zorder: `number`

Default value: `-1.1`

- [Indexable](#indexable)- [Properties](#properties)[hlines background.color](#hlines-backgroundcolor)- [hlines background.transparency](#hlines-backgroundtransparency)- [hlines background.visible](#hlines-backgroundvisible)- [lowerlimit.color](#lowerlimitcolor)- [lowerlimit.linestyle](#lowerlimitlinestyle)- [lowerlimit.linewidth](#lowerlimitlinewidth)- [lowerlimit.value](#lowerlimitvalue)- [lowerlimit.visible](#lowerlimitvisible)- [lowerlimit.zorder](#lowerlimitzorder)- [middlelimit.color](#middlelimitcolor)- [middlelimit.linestyle](#middlelimitlinestyle)- [middlelimit.linewidth](#middlelimitlinewidth)- [middlelimit.value](#middlelimitvalue)- [middlelimit.visible](#middlelimitvisible)- [middlelimit.zorder](#middlelimitzorder)- [plot.color](#plotcolor)- [plot.display](#plotdisplay)- [plot.linestyle](#plotlinestyle)- [plot.linewidth](#plotlinewidth)- [plot.plottype](#plotplottype)- [plot.trackprice](#plottrackprice)- [plot.transparency](#plottransparency)- [smoothed ma.display](#smoothed-madisplay)- [smoothed ma.linestyle](#smoothed-malinestyle)- [smoothed ma.linewidth](#smoothed-malinewidth)- [smoothed ma.plottype](#smoothed-maplottype)- [smoothed ma.trackprice](#smoothed-matrackprice)- [smoothed ma.transparency](#smoothed-matransparency)- [upperlimit.color](#upperlimitcolor)- [upperlimit.linestyle](#upperlimitlinestyle)- [upperlimit.linewidth](#upperlimitlinewidth)- [upperlimit.value](#upperlimitvalue)- [upperlimit.visible](#upperlimitvisible)- [upperlimit.zorder](#upperlimitzorder)