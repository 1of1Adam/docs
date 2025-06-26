---
title: "Interface: ConnorsRSIIndicatorOverrides | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ConnorsRSIIndicatorOverrides"
extracted_at: "2025-06-22T09:34:38.986Z"
---

- [](/charting-library-docs/)- Interfaces- ConnorsRSIIndicatorOverridesOn this page# Interface: ConnorsRSIIndicatorOverrides[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ConnorsRSIIndicatorOverrides

Overrides for the 'Connors RSI' indicator.

Use these properties to customize indicator via [IChartWidgetApi.createStudy](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createstudy) and [IStudyApi.applyOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi#applyoverrides).

## Indexable[​](#indexable)
▪ [key: `string`]: [`StudyOverrideValueType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyoverridevaluetype)

## Properties[​](#properties)
### crsi.color[​](#crsicolor)
• crsi.color: `string`

Default value: `#2196F3`

### crsi.display[​](#crsidisplay)
• crsi.display: `number`

Default value: `15`

### crsi.linestyle[​](#crsilinestyle)
• crsi.linestyle: `number`

Default value: `0`

### crsi.linewidth[​](#crsilinewidth)
• crsi.linewidth: `number`

Default value: `1`

### crsi.plottype[​](#crsiplottype)
• crsi.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### crsi.trackprice[​](#crsitrackprice)
• crsi.trackprice: `boolean`

Default value: `false`

### crsi.transparency[​](#crsitransparency)
• crsi.transparency: `number`

Default value: `0`

### hlines background.color[​](#hlines-backgroundcolor)
• hlines background.color: `string`

Default value: `#2196F3`

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

- [Indexable](#indexable)- [Properties](#properties)[crsi.color](#crsicolor)- [crsi.display](#crsidisplay)- [crsi.linestyle](#crsilinestyle)- [crsi.linewidth](#crsilinewidth)- [crsi.plottype](#crsiplottype)- [crsi.trackprice](#crsitrackprice)- [crsi.transparency](#crsitransparency)- [hlines background.color](#hlines-backgroundcolor)- [hlines background.transparency](#hlines-backgroundtransparency)- [hlines background.visible](#hlines-backgroundvisible)- [lowerlimit.color](#lowerlimitcolor)- [lowerlimit.linestyle](#lowerlimitlinestyle)- [lowerlimit.linewidth](#lowerlimitlinewidth)- [lowerlimit.value](#lowerlimitvalue)- [lowerlimit.visible](#lowerlimitvisible)- [upperlimit.color](#upperlimitcolor)- [upperlimit.linestyle](#upperlimitlinestyle)- [upperlimit.linewidth](#upperlimitlinewidth)- [upperlimit.value](#upperlimitvalue)- [upperlimit.visible](#upperlimitvisible)