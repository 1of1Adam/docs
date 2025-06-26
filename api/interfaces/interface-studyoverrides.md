---
title: "Interface: StudyOverrides | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOverrides"
extracted_at: "2025-06-22T09:47:03.768Z"
---

- [](/charting-library-docs/)- Interfaces- StudyOverridesOn this page# Interface: StudyOverrides[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyOverrides

Indicator overrides.
See [Indicator Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides).
Use these properties to specify default indicator style via [ChartingLibraryWidgetOptions.studies_overrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#studies_overrides) and [IChartingLibraryWidget.applyStudiesOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#applystudiesoverrides).

## Indexable[​](#indexable)
▪ [key: `string`]: [`StudyOverrideValueType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyoverridevaluetype)

## Properties[​](#properties)
### 52 week high/low.high source[​](#52-week-highlowhigh-source)
• 52 week high/low.high source: `string`

- Default value: `close`
- Input type: `text`
- Options: `["close","high"]`

### 52 week high/low.low source[​](#52-week-highlowlow-source)
• 52 week high/low.low source: `string`

- Default value: `close`
- Input type: `text`
- Options: `["close","low"]`

### accelerator oscillator.plot.color[​](#accelerator-oscillatorplotcolor)
• accelerator oscillator.plot.color: `string`

Default value: `#000080`

### accelerator oscillator.plot.display[​](#accelerator-oscillatorplotdisplay)
• accelerator oscillator.plot.display: `number`

Default value: `15`

### accelerator oscillator.plot.linestyle[​](#accelerator-oscillatorplotlinestyle)
• accelerator oscillator.plot.linestyle: `number`

Default value: `0`

### accelerator oscillator.plot.linewidth[​](#accelerator-oscillatorplotlinewidth)
• accelerator oscillator.plot.linewidth: `number`

Default value: `1`

### accelerator oscillator.plot.plottype[​](#accelerator-oscillatorplotplottype)
• accelerator oscillator.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `histogram`

### accelerator oscillator.plot.trackprice[​](#accelerator-oscillatorplottrackprice)
• accelerator oscillator.plot.trackprice: `boolean`

Default value: `false`

### accelerator oscillator.plot.transparency[​](#accelerator-oscillatorplottransparency)
• accelerator oscillator.plot.transparency: `number`

Default value: `0`

### accumulation/distribution.plot.color[​](#accumulationdistributionplotcolor)
• accumulation/distribution.plot.color: `string`

Default value: `#2196F3`

### accumulation/distribution.plot.display[​](#accumulationdistributionplotdisplay)
• accumulation/distribution.plot.display: `number`

Default value: `15`

### accumulation/distribution.plot.linestyle[​](#accumulationdistributionplotlinestyle)
• accumulation/distribution.plot.linestyle: `number`

Default value: `0`

### accumulation/distribution.plot.linewidth[​](#accumulationdistributionplotlinewidth)
• accumulation/distribution.plot.linewidth: `number`

Default value: `1`

### accumulation/distribution.plot.plottype[​](#accumulationdistributionplotplottype)
• accumulation/distribution.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### accumulation/distribution.plot.trackprice[​](#accumulationdistributionplottrackprice)
• accumulation/distribution.plot.trackprice: `boolean`

Default value: `false`

### accumulation/distribution.plot.transparency[​](#accumulationdistributionplottransparency)
• accumulation/distribution.plot.transparency: `number`

Default value: `0`

### accumulative swing index.asi.color[​](#accumulative-swing-indexasicolor)
• accumulative swing index.asi.color: `string`

Default value: `#2196F3`

### accumulative swing index.asi.display[​](#accumulative-swing-indexasidisplay)
• accumulative swing index.asi.display: `number`

Default value: `15`

### accumulative swing index.asi.linestyle[​](#accumulative-swing-indexasilinestyle)
• accumulative swing index.asi.linestyle: `number`

Default value: `0`

### accumulative swing index.asi.linewidth[​](#accumulative-swing-indexasilinewidth)
• accumulative swing index.asi.linewidth: `number`

Default value: `1`

### accumulative swing index.asi.plottype[​](#accumulative-swing-indexasiplottype)
• accumulative swing index.asi.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### accumulative swing index.asi.trackprice[​](#accumulative-swing-indexasitrackprice)
• accumulative swing index.asi.trackprice: `boolean`

Default value: `false`

### accumulative swing index.asi.transparency[​](#accumulative-swing-indexasitransparency)
• accumulative swing index.asi.transparency: `number`

Default value: `0`

### accumulative swing index.limit move value[​](#accumulative-swing-indexlimit-move-value)
• accumulative swing index.limit move value: `number`

- Default value: `10`
- Input type: `float`
- Min: `0.1`
- Max: `100000`

### advance/decline.length[​](#advancedeclinelength)
• advance/decline.length: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### advance/decline.plot.color[​](#advancedeclineplotcolor)
• advance/decline.plot.color: `string`

Default value: `#2196F3`

### advance/decline.plot.display[​](#advancedeclineplotdisplay)
• advance/decline.plot.display: `number`

Default value: `15`

### advance/decline.plot.linestyle[​](#advancedeclineplotlinestyle)
• advance/decline.plot.linestyle: `number`

Default value: `0`

### advance/decline.plot.linewidth[​](#advancedeclineplotlinewidth)
• advance/decline.plot.linewidth: `number`

Default value: `1`

### advance/decline.plot.plottype[​](#advancedeclineplotplottype)
• advance/decline.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### advance/decline.plot.trackprice[​](#advancedeclineplottrackprice)
• advance/decline.plot.trackprice: `boolean`

Default value: `false`

### advance/decline.plot.transparency[​](#advancedeclineplottransparency)
• advance/decline.plot.transparency: `number`

Default value: `0`

### anchored vwap. :input[​](#anchored-vwap-)
• anchored vwap. :input: `boolean`

- Default value: `false`
- Input type: `bool`
- Group: `"Bands Settings"`
- Inline: `"band_3"`

### anchored vwap.background #1.color[​](#anchored-vwapbackground-1color)
• anchored vwap.background #1.color: `string`

Default value: `#4caf50`

### anchored vwap.background #1.transparency[​](#anchored-vwapbackground-1transparency)
• anchored vwap.background #1.transparency: `number`

Default value: `95`

### anchored vwap.background #1.visible[​](#anchored-vwapbackground-1visible)
• anchored vwap.background #1.visible: `boolean`

Default value: `true`

### anchored vwap.bands calculation mode[​](#anchored-vwapbands-calculation-mode)
• anchored vwap.bands calculation mode: `string`

- Default value: `Standard Deviation`
- Input type: `text`
- Group: `"Bands Settings"`
- Options: `["Standard Deviation","Percentage"]`
- Tooltip: `"Determines the units used to calculate the distance of the bands. When 'Percentage' is selected, a multiplier of 1 means 1%."`

### anchored vwap.bands multiplier #1[​](#anchored-vwapbands-multiplier-1)
• anchored vwap.bands multiplier #1: `number`

- Default value: `1`
- Input type: `float`
- Group: `"Bands Settings"`
- Inline: `"band_1"`
- Max: `1.7976931348623157e+308`
- Min: `0`
- Step: `0.5`

### anchored vwap.bands multiplier #2[​](#anchored-vwapbands-multiplier-2)
• anchored vwap.bands multiplier #2: `number`

- Default value: `2`
- Input type: `float`
- Group: `"Bands Settings"`
- Inline: `"band_2"`
- Max: `1.7976931348623157e+308`
- Min: `0`
- Step: `0.5`

### anchored vwap.bands multiplier #3[​](#anchored-vwapbands-multiplier-3)
• anchored vwap.bands multiplier #3: `number`

- Default value: `3`
- Input type: `float`
- Group: `"Bands Settings"`
- Inline: `"band_3"`
- Max: `1.7976931348623157e+308`
- Min: `0`
- Step: `0.5`

### anchored vwap.lower band #1.color[​](#anchored-vwaplower-band-1color)
• anchored vwap.lower band #1.color: `string`

Default value: `#4caf50`

### anchored vwap.lower band #1.display[​](#anchored-vwaplower-band-1display)
• anchored vwap.lower band #1.display: `number`

Default value: `15`

### anchored vwap.lower band #1.linestyle[​](#anchored-vwaplower-band-1linestyle)
• anchored vwap.lower band #1.linestyle: `number`

Default value: `0`

### anchored vwap.lower band #1.linewidth[​](#anchored-vwaplower-band-1linewidth)
• anchored vwap.lower band #1.linewidth: `number`

Default value: `1`

### anchored vwap.lower band #1.plottype[​](#anchored-vwaplower-band-1plottype)
• anchored vwap.lower band #1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### anchored vwap.lower band #1.trackprice[​](#anchored-vwaplower-band-1trackprice)
• anchored vwap.lower band #1.trackprice: `boolean`

Default value: `false`

### anchored vwap.lower band #1.transparency[​](#anchored-vwaplower-band-1transparency)
• anchored vwap.lower band #1.transparency: `number`

Default value: `0`

### anchored vwap.lower band #2.color[​](#anchored-vwaplower-band-2color)
• anchored vwap.lower band #2.color: `string`

Default value: `#808000`

### anchored vwap.lower band #2.display[​](#anchored-vwaplower-band-2display)
• anchored vwap.lower band #2.display: `number`

Default value: `15`

### anchored vwap.lower band #2.linestyle[​](#anchored-vwaplower-band-2linestyle)
• anchored vwap.lower band #2.linestyle: `number`

Default value: `0`

### anchored vwap.lower band #2.linewidth[​](#anchored-vwaplower-band-2linewidth)
• anchored vwap.lower band #2.linewidth: `number`

Default value: `1`

### anchored vwap.lower band #2.plottype[​](#anchored-vwaplower-band-2plottype)
• anchored vwap.lower band #2.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### anchored vwap.lower band #2.trackprice[​](#anchored-vwaplower-band-2trackprice)
• anchored vwap.lower band #2.trackprice: `boolean`

Default value: `false`

### anchored vwap.lower band #2.transparency[​](#anchored-vwaplower-band-2transparency)
• anchored vwap.lower band #2.transparency: `number`

Default value: `0`

### anchored vwap.lower band #3.color[​](#anchored-vwaplower-band-3color)
• anchored vwap.lower band #3.color: `string`

Default value: `#00897b`

### anchored vwap.lower band #3.display[​](#anchored-vwaplower-band-3display)
• anchored vwap.lower band #3.display: `number`

Default value: `15`

### anchored vwap.lower band #3.linestyle[​](#anchored-vwaplower-band-3linestyle)
• anchored vwap.lower band #3.linestyle: `number`

Default value: `0`

### anchored vwap.lower band #3.linewidth[​](#anchored-vwaplower-band-3linewidth)
• anchored vwap.lower band #3.linewidth: `number`

Default value: `1`

### anchored vwap.lower band #3.plottype[​](#anchored-vwaplower-band-3plottype)
• anchored vwap.lower band #3.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### anchored vwap.lower band #3.trackprice[​](#anchored-vwaplower-band-3trackprice)
• anchored vwap.lower band #3.trackprice: `boolean`

Default value: `false`

### anchored vwap.lower band #3.transparency[​](#anchored-vwaplower-band-3transparency)
• anchored vwap.lower band #3.transparency: `number`

Default value: `0`

### anchored vwap.source[​](#anchored-vwapsource)
• anchored vwap.source: `string`

- Default value: `hlc3`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### anchored vwap.start time[​](#anchored-vwapstart-time)
• anchored vwap.start time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `9007199254740991`
- Min: `-9007199254740991`

### anchored vwap.upper band #1.color[​](#anchored-vwapupper-band-1color)
• anchored vwap.upper band #1.color: `string`

Default value: `#4caf50`

### anchored vwap.upper band #1.display[​](#anchored-vwapupper-band-1display)
• anchored vwap.upper band #1.display: `number`

Default value: `15`

### anchored vwap.upper band #1.linestyle[​](#anchored-vwapupper-band-1linestyle)
• anchored vwap.upper band #1.linestyle: `number`

Default value: `0`

### anchored vwap.upper band #1.linewidth[​](#anchored-vwapupper-band-1linewidth)
• anchored vwap.upper band #1.linewidth: `number`

Default value: `1`

### anchored vwap.upper band #1.plottype[​](#anchored-vwapupper-band-1plottype)
• anchored vwap.upper band #1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### anchored vwap.upper band #1.trackprice[​](#anchored-vwapupper-band-1trackprice)
• anchored vwap.upper band #1.trackprice: `boolean`

Default value: `false`

### anchored vwap.upper band #1.transparency[​](#anchored-vwapupper-band-1transparency)
• anchored vwap.upper band #1.transparency: `number`

Default value: `0`

### anchored vwap.upper band #2.color[​](#anchored-vwapupper-band-2color)
• anchored vwap.upper band #2.color: `string`

Default value: `#808000`

### anchored vwap.upper band #2.display[​](#anchored-vwapupper-band-2display)
• anchored vwap.upper band #2.display: `number`

Default value: `15`

### anchored vwap.upper band #2.linestyle[​](#anchored-vwapupper-band-2linestyle)
• anchored vwap.upper band #2.linestyle: `number`

Default value: `0`

### anchored vwap.upper band #2.linewidth[​](#anchored-vwapupper-band-2linewidth)
• anchored vwap.upper band #2.linewidth: `number`

Default value: `1`

### anchored vwap.upper band #2.plottype[​](#anchored-vwapupper-band-2plottype)
• anchored vwap.upper band #2.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### anchored vwap.upper band #2.trackprice[​](#anchored-vwapupper-band-2trackprice)
• anchored vwap.upper band #2.trackprice: `boolean`

Default value: `false`

### anchored vwap.upper band #2.transparency[​](#anchored-vwapupper-band-2transparency)
• anchored vwap.upper band #2.transparency: `number`

Default value: `0`

### anchored vwap.upper band #3.color[​](#anchored-vwapupper-band-3color)
• anchored vwap.upper band #3.color: `string`

Default value: `#00897b`

### anchored vwap.upper band #3.display[​](#anchored-vwapupper-band-3display)
• anchored vwap.upper band #3.display: `number`

Default value: `15`

### anchored vwap.upper band #3.linestyle[​](#anchored-vwapupper-band-3linestyle)
• anchored vwap.upper band #3.linestyle: `number`

Default value: `0`

### anchored vwap.upper band #3.linewidth[​](#anchored-vwapupper-band-3linewidth)
• anchored vwap.upper band #3.linewidth: `number`

Default value: `1`

### anchored vwap.upper band #3.plottype[​](#anchored-vwapupper-band-3plottype)
• anchored vwap.upper band #3.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### anchored vwap.upper band #3.trackprice[​](#anchored-vwapupper-band-3trackprice)
• anchored vwap.upper band #3.trackprice: `boolean`

Default value: `false`

### anchored vwap.upper band #3.transparency[​](#anchored-vwapupper-band-3transparency)
• anchored vwap.upper band #3.transparency: `number`

Default value: `0`

### anchored vwap.vwap.color[​](#anchored-vwapvwapcolor)
• anchored vwap.vwap.color: `string`

Default value: `#1e88e5`

### anchored vwap.vwap.display[​](#anchored-vwapvwapdisplay)
• anchored vwap.vwap.display: `number`

Default value: `15`

### anchored vwap.vwap.linestyle[​](#anchored-vwapvwaplinestyle)
• anchored vwap.vwap.linestyle: `number`

Default value: `0`

### anchored vwap.vwap.linewidth[​](#anchored-vwapvwaplinewidth)
• anchored vwap.vwap.linewidth: `number`

Default value: `1`

### anchored vwap.vwap.plottype[​](#anchored-vwapvwapplottype)
• anchored vwap.vwap.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### anchored vwap.vwap.trackprice[​](#anchored-vwapvwaptrackprice)
• anchored vwap.vwap.trackprice: `boolean`

Default value: `false`

### anchored vwap.vwap.transparency[​](#anchored-vwapvwaptransparency)
• anchored vwap.vwap.transparency: `number`

Default value: `0`

### areaStyle.color1[​](#areastylecolor1)
• areaStyle.color1: `string`

### areaStyle.color2[​](#areastylecolor2)
• areaStyle.color2: `string`

### areaStyle.linecolor[​](#areastylelinecolor)
• areaStyle.linecolor: `string`

### areaStyle.linestyle[​](#areastylelinestyle)
• areaStyle.linestyle: `number`

### areaStyle.linewidth[​](#areastylelinewidth)
• areaStyle.linewidth: `number`

### areaStyle.transparency[​](#areastyletransparency)
• areaStyle.transparency: `number`

### arnaud legoux moving average.offset[​](#arnaud-legoux-moving-averageoffset)
• arnaud legoux moving average.offset: `number`

- Default value: `0.85`
- Input type: `float`
- Min: `-1000000000000`
- Max: `1000000000000`

### arnaud legoux moving average.plot.color[​](#arnaud-legoux-moving-averageplotcolor)
• arnaud legoux moving average.plot.color: `string`

Default value: `#2196F3`

### arnaud legoux moving average.plot.display[​](#arnaud-legoux-moving-averageplotdisplay)
• arnaud legoux moving average.plot.display: `number`

Default value: `15`

### arnaud legoux moving average.plot.linestyle[​](#arnaud-legoux-moving-averageplotlinestyle)
• arnaud legoux moving average.plot.linestyle: `number`

Default value: `0`

### arnaud legoux moving average.plot.linewidth[​](#arnaud-legoux-moving-averageplotlinewidth)
• arnaud legoux moving average.plot.linewidth: `number`

Default value: `1`

### arnaud legoux moving average.plot.plottype[​](#arnaud-legoux-moving-averageplotplottype)
• arnaud legoux moving average.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### arnaud legoux moving average.plot.trackprice[​](#arnaud-legoux-moving-averageplottrackprice)
• arnaud legoux moving average.plot.trackprice: `boolean`

Default value: `false`

### arnaud legoux moving average.plot.transparency[​](#arnaud-legoux-moving-averageplottransparency)
• arnaud legoux moving average.plot.transparency: `number`

Default value: `0`

### arnaud legoux moving average.sigma[​](#arnaud-legoux-moving-averagesigma)
• arnaud legoux moving average.sigma: `number`

- Default value: `6`
- Input type: `float`
- Min: `-1000000000000`
- Max: `1000000000000`

### arnaud legoux moving average.window size[​](#arnaud-legoux-moving-averagewindow-size)
• arnaud legoux moving average.window size: `number`

- Default value: `9`
- Input type: `integer`
- Min: `0`
- Max: `5000`

### aroon.length[​](#aroonlength)
• aroon.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### aroon.lower.color[​](#aroonlowercolor)
• aroon.lower.color: `string`

Default value: `#2196F3`

### aroon.lower.display[​](#aroonlowerdisplay)
• aroon.lower.display: `number`

Default value: `15`

### aroon.lower.linestyle[​](#aroonlowerlinestyle)
• aroon.lower.linestyle: `number`

Default value: `0`

### aroon.lower.linewidth[​](#aroonlowerlinewidth)
• aroon.lower.linewidth: `number`

Default value: `1`

### aroon.lower.plottype[​](#aroonlowerplottype)
• aroon.lower.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### aroon.lower.trackprice[​](#aroonlowertrackprice)
• aroon.lower.trackprice: `boolean`

Default value: `false`

### aroon.lower.transparency[​](#aroonlowertransparency)
• aroon.lower.transparency: `number`

Default value: `0`

### aroon.upper.color[​](#aroonuppercolor)
• aroon.upper.color: `string`

Default value: `#FB8C00`

### aroon.upper.display[​](#aroonupperdisplay)
• aroon.upper.display: `number`

Default value: `15`

### aroon.upper.linestyle[​](#aroonupperlinestyle)
• aroon.upper.linestyle: `number`

Default value: `0`

### aroon.upper.linewidth[​](#aroonupperlinewidth)
• aroon.upper.linewidth: `number`

Default value: `1`

### aroon.upper.plottype[​](#aroonupperplottype)
• aroon.upper.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### aroon.upper.trackprice[​](#aroonuppertrackprice)
• aroon.upper.trackprice: `boolean`

Default value: `false`

### aroon.upper.transparency[​](#aroonuppertransparency)
• aroon.upper.transparency: `number`

Default value: `0`

### average directional index.adx smoothing[​](#average-directional-indexadx-smoothing)
• average directional index.adx smoothing: `number`

- Default value: `14`
- Input type: `integer`
- Min: `-1000000000000`
- Max: `1000000000000`

### average directional index.adx.color[​](#average-directional-indexadxcolor)
• average directional index.adx.color: `string`

Default value: `#FF5252`

### average directional index.adx.display[​](#average-directional-indexadxdisplay)
• average directional index.adx.display: `number`

Default value: `15`

### average directional index.adx.linestyle[​](#average-directional-indexadxlinestyle)
• average directional index.adx.linestyle: `number`

Default value: `0`

### average directional index.adx.linewidth[​](#average-directional-indexadxlinewidth)
• average directional index.adx.linewidth: `number`

Default value: `1`

### average directional index.adx.plottype[​](#average-directional-indexadxplottype)
• average directional index.adx.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### average directional index.adx.trackprice[​](#average-directional-indexadxtrackprice)
• average directional index.adx.trackprice: `boolean`

Default value: `false`

### average directional index.adx.transparency[​](#average-directional-indexadxtransparency)
• average directional index.adx.transparency: `number`

Default value: `0`

### average directional index.di length[​](#average-directional-indexdi-length)
• average directional index.di length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `-1000000000000`
- Max: `1000000000000`

### average price.other symbol[​](#average-priceother-symbol)
• average price.other symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Optional: `true`
- IsHidden: `false`

### average price.plot.color[​](#average-priceplotcolor)
• average price.plot.color: `string`

Default value: `#2196F3`

### average price.plot.display[​](#average-priceplotdisplay)
• average price.plot.display: `number`

Default value: `15`

### average price.plot.linestyle[​](#average-priceplotlinestyle)
• average price.plot.linestyle: `number`

Default value: `0`

### average price.plot.linewidth[​](#average-priceplotlinewidth)
• average price.plot.linewidth: `number`

Default value: `1`

### average price.plot.plottype[​](#average-priceplotplottype)
• average price.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### average price.plot.trackprice[​](#average-priceplottrackprice)
• average price.plot.trackprice: `boolean`

Default value: `false`

### average price.plot.transparency[​](#average-priceplottransparency)
• average price.plot.transparency: `number`

Default value: `0`

### average true range.length[​](#average-true-rangelength)
• average true range.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### average true range.plot.color[​](#average-true-rangeplotcolor)
• average true range.plot.color: `string`

Default value: `#801922`

### average true range.plot.display[​](#average-true-rangeplotdisplay)
• average true range.plot.display: `number`

Default value: `15`

### average true range.plot.linestyle[​](#average-true-rangeplotlinestyle)
• average true range.plot.linestyle: `number`

Default value: `0`

### average true range.plot.linewidth[​](#average-true-rangeplotlinewidth)
• average true range.plot.linewidth: `number`

Default value: `1`

### average true range.plot.plottype[​](#average-true-rangeplotplottype)
• average true range.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### average true range.plot.trackprice[​](#average-true-rangeplottrackprice)
• average true range.plot.trackprice: `boolean`

Default value: `false`

### average true range.plot.transparency[​](#average-true-rangeplottransparency)
• average true range.plot.transparency: `number`

Default value: `0`

### awesome oscillator.plot.color[​](#awesome-oscillatorplotcolor)
• awesome oscillator.plot.color: `string`

Default value: `#000080`

### awesome oscillator.plot.display[​](#awesome-oscillatorplotdisplay)
• awesome oscillator.plot.display: `number`

Default value: `15`

### awesome oscillator.plot.linestyle[​](#awesome-oscillatorplotlinestyle)
• awesome oscillator.plot.linestyle: `number`

Default value: `0`

### awesome oscillator.plot.linewidth[​](#awesome-oscillatorplotlinewidth)
• awesome oscillator.plot.linewidth: `number`

Default value: `1`

### awesome oscillator.plot.plottype[​](#awesome-oscillatorplotplottype)
• awesome oscillator.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `histogram`

### awesome oscillator.plot.trackprice[​](#awesome-oscillatorplottrackprice)
• awesome oscillator.plot.trackprice: `boolean`

Default value: `false`

### awesome oscillator.plot.transparency[​](#awesome-oscillatorplottransparency)
• awesome oscillator.plot.transparency: `number`

Default value: `0`

### balance of power.plot.color[​](#balance-of-powerplotcolor)
• balance of power.plot.color: `string`

Default value: `#FF5252`

### balance of power.plot.display[​](#balance-of-powerplotdisplay)
• balance of power.plot.display: `number`

Default value: `15`

### balance of power.plot.linestyle[​](#balance-of-powerplotlinestyle)
• balance of power.plot.linestyle: `number`

Default value: `0`

### balance of power.plot.linewidth[​](#balance-of-powerplotlinewidth)
• balance of power.plot.linewidth: `number`

Default value: `1`

### balance of power.plot.plottype[​](#balance-of-powerplotplottype)
• balance of power.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### balance of power.plot.trackprice[​](#balance-of-powerplottrackprice)
• balance of power.plot.trackprice: `boolean`

Default value: `false`

### balance of power.plot.transparency[​](#balance-of-powerplottransparency)
• balance of power.plot.transparency: `number`

Default value: `0`

### barStyle.barColorsOnPrevClose[​](#barstylebarcolorsonprevclose)
• barStyle.barColorsOnPrevClose: `boolean`

### barStyle.dontDrawOpen[​](#barstyledontdrawopen)
• barStyle.dontDrawOpen: `boolean`

### barStyle.downColor[​](#barstyledowncolor)
• barStyle.downColor: `string`

### barStyle.thinBars[​](#barstylethinbars)
• barStyle.thinBars: `boolean`

### barStyle.upColor[​](#barstyleupcolor)
• barStyle.upColor: `string`

### baselineStyle.baseLevelPercentage[​](#baselinestylebaselevelpercentage)
• baselineStyle.baseLevelPercentage: `number`

### baselineStyle.baselineColor[​](#baselinestylebaselinecolor)
• baselineStyle.baselineColor: `string`

### baselineStyle.bottomFillColor1[​](#baselinestylebottomfillcolor1)
• baselineStyle.bottomFillColor1: `string`

### baselineStyle.bottomFillColor2[​](#baselinestylebottomfillcolor2)
• baselineStyle.bottomFillColor2: `string`

### baselineStyle.bottomLineColor[​](#baselinestylebottomlinecolor)
• baselineStyle.bottomLineColor: `string`

### baselineStyle.bottomLineWidth[​](#baselinestylebottomlinewidth)
• baselineStyle.bottomLineWidth: `number`

### baselineStyle.topFillColor1[​](#baselinestyletopfillcolor1)
• baselineStyle.topFillColor1: `string`

### baselineStyle.topFillColor2[​](#baselinestyletopfillcolor2)
• baselineStyle.topFillColor2: `string`

### baselineStyle.topLineColor[​](#baselinestyletoplinecolor)
• baselineStyle.topLineColor: `string`

### baselineStyle.topLineWidth[​](#baselinestyletoplinewidth)
• baselineStyle.topLineWidth: `number`

### baselineStyle.transparency[​](#baselinestyletransparency)
• baselineStyle.transparency: `number`

### bollinger bands %b.hlines background.color[​](#bollinger-bands-bhlines-backgroundcolor)
• bollinger bands %b.hlines background.color: `string`

Default value: `#26A69A`

### bollinger bands %b.hlines background.transparency[​](#bollinger-bands-bhlines-backgroundtransparency)
• bollinger bands %b.hlines background.transparency: `number`

Default value: `90`

### bollinger bands %b.hlines background.visible[​](#bollinger-bands-bhlines-backgroundvisible)
• bollinger bands %b.hlines background.visible: `boolean`

Default value: `true`

### bollinger bands %b.length[​](#bollinger-bands-blength)
• bollinger bands %b.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### bollinger bands %b.lowerlimit.color[​](#bollinger-bands-blowerlimitcolor)
• bollinger bands %b.lowerlimit.color: `string`

Default value: `#787B86`

### bollinger bands %b.lowerlimit.linestyle[​](#bollinger-bands-blowerlimitlinestyle)
• bollinger bands %b.lowerlimit.linestyle: `number`

Default value: `2`

### bollinger bands %b.lowerlimit.linewidth[​](#bollinger-bands-blowerlimitlinewidth)
• bollinger bands %b.lowerlimit.linewidth: `number`

Default value: `1`

### bollinger bands %b.lowerlimit.value[​](#bollinger-bands-blowerlimitvalue)
• bollinger bands %b.lowerlimit.value: `number`

Default value: `0`

### bollinger bands %b.lowerlimit.visible[​](#bollinger-bands-blowerlimitvisible)
• bollinger bands %b.lowerlimit.visible: `boolean`

Default value: `true`

### bollinger bands %b.mult[​](#bollinger-bands-bmult)
• bollinger bands %b.mult: `number`

- Default value: `2`
- Input type: `float`
- Min: `0.001`
- Max: `50`

### bollinger bands %b.plot.color[​](#bollinger-bands-bplotcolor)
• bollinger bands %b.plot.color: `string`

Default value: `#22AB94`

### bollinger bands %b.plot.linestyle[​](#bollinger-bands-bplotlinestyle)
• bollinger bands %b.plot.linestyle: `number`

Default value: `0`

### bollinger bands %b.plot.linewidth[​](#bollinger-bands-bplotlinewidth)
• bollinger bands %b.plot.linewidth: `number`

Default value: `1`

### bollinger bands %b.plot.plottype[​](#bollinger-bands-bplotplottype)
• bollinger bands %b.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### bollinger bands %b.plot.trackprice[​](#bollinger-bands-bplottrackprice)
• bollinger bands %b.plot.trackprice: `boolean`

Default value: `false`

### bollinger bands %b.plot.transparency[​](#bollinger-bands-bplottransparency)
• bollinger bands %b.plot.transparency: `number`

Default value: `0`

### bollinger bands %b.plot.visible[​](#bollinger-bands-bplotvisible)
• bollinger bands %b.plot.visible: `boolean`

Default value: `true`

### bollinger bands %b.upperlimit.color[​](#bollinger-bands-bupperlimitcolor)
• bollinger bands %b.upperlimit.color: `string`

Default value: `#787B86`

### bollinger bands %b.upperlimit.linestyle[​](#bollinger-bands-bupperlimitlinestyle)
• bollinger bands %b.upperlimit.linestyle: `number`

Default value: `2`

### bollinger bands %b.upperlimit.linewidth[​](#bollinger-bands-bupperlimitlinewidth)
• bollinger bands %b.upperlimit.linewidth: `number`

Default value: `1`

### bollinger bands %b.upperlimit.value[​](#bollinger-bands-bupperlimitvalue)
• bollinger bands %b.upperlimit.value: `number`

Default value: `1`

### bollinger bands %b.upperlimit.visible[​](#bollinger-bands-bupperlimitvisible)
• bollinger bands %b.upperlimit.visible: `boolean`

Default value: `true`

### bollinger bands width.length[​](#bollinger-bands-widthlength)
• bollinger bands width.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### bollinger bands width.mult[​](#bollinger-bands-widthmult)
• bollinger bands width.mult: `number`

- Default value: `2`
- Input type: `float`
- Min: `0.001`
- Max: `50`

### bollinger bands width.plot.color[​](#bollinger-bands-widthplotcolor)
• bollinger bands width.plot.color: `string`

Default value: `#FF6D00`

### bollinger bands width.plot.display[​](#bollinger-bands-widthplotdisplay)
• bollinger bands width.plot.display: `number`

Default value: `15`

### bollinger bands width.plot.linestyle[​](#bollinger-bands-widthplotlinestyle)
• bollinger bands width.plot.linestyle: `number`

Default value: `0`

### bollinger bands width.plot.linewidth[​](#bollinger-bands-widthplotlinewidth)
• bollinger bands width.plot.linewidth: `number`

Default value: `1`

### bollinger bands width.plot.plottype[​](#bollinger-bands-widthplotplottype)
• bollinger bands width.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### bollinger bands width.plot.trackprice[​](#bollinger-bands-widthplottrackprice)
• bollinger bands width.plot.trackprice: `boolean`

Default value: `false`

### bollinger bands width.plot.transparency[​](#bollinger-bands-widthplottransparency)
• bollinger bands width.plot.transparency: `number`

Default value: `0`

### bollinger bands.length[​](#bollinger-bandslength)
• bollinger bands.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### bollinger bands.lower.color[​](#bollinger-bandslowercolor)
• bollinger bands.lower.color: `string`

Default value: `#2196F3`

### bollinger bands.lower.linestyle[​](#bollinger-bandslowerlinestyle)
• bollinger bands.lower.linestyle: `number`

Default value: `0`

### bollinger bands.lower.linewidth[​](#bollinger-bandslowerlinewidth)
• bollinger bands.lower.linewidth: `number`

Default value: `1`

### bollinger bands.lower.plottype[​](#bollinger-bandslowerplottype)
• bollinger bands.lower.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### bollinger bands.lower.trackprice[​](#bollinger-bandslowertrackprice)
• bollinger bands.lower.trackprice: `boolean`

Default value: `false`

### bollinger bands.lower.transparency[​](#bollinger-bandslowertransparency)
• bollinger bands.lower.transparency: `number`

Default value: `0`

### bollinger bands.lower.visible[​](#bollinger-bandslowervisible)
• bollinger bands.lower.visible: `boolean`

Default value: `true`

### bollinger bands.median.color[​](#bollinger-bandsmediancolor)
• bollinger bands.median.color: `string`

Default value: `#FF6D00`

### bollinger bands.median.linestyle[​](#bollinger-bandsmedianlinestyle)
• bollinger bands.median.linestyle: `number`

Default value: `0`

### bollinger bands.median.linewidth[​](#bollinger-bandsmedianlinewidth)
• bollinger bands.median.linewidth: `number`

Default value: `1`

### bollinger bands.median.plottype[​](#bollinger-bandsmedianplottype)
• bollinger bands.median.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### bollinger bands.median.trackprice[​](#bollinger-bandsmediantrackprice)
• bollinger bands.median.trackprice: `boolean`

Default value: `false`

### bollinger bands.median.transparency[​](#bollinger-bandsmediantransparency)
• bollinger bands.median.transparency: `number`

Default value: `0`

### bollinger bands.median.visible[​](#bollinger-bandsmedianvisible)
• bollinger bands.median.visible: `boolean`

Default value: `true`

### bollinger bands.mult[​](#bollinger-bandsmult)
• bollinger bands.mult: `number`

- Default value: `2`
- Input type: `float`
- Min: `0.001`
- Max: `50`

### bollinger bands.other symbol[​](#bollinger-bandsother-symbol)
• bollinger bands.other symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Optional: `true`
- IsHidden: `false`

### bollinger bands.plots background.color[​](#bollinger-bandsplots-backgroundcolor)
• bollinger bands.plots background.color: `string`

Default value: `#2196F3`

### bollinger bands.plots background.transparency[​](#bollinger-bandsplots-backgroundtransparency)
• bollinger bands.plots background.transparency: `number`

Default value: `95`

### bollinger bands.plots background.visible[​](#bollinger-bandsplots-backgroundvisible)
• bollinger bands.plots background.visible: `boolean`

Default value: `true`

### bollinger bands.upper.color[​](#bollinger-bandsuppercolor)
• bollinger bands.upper.color: `string`

Default value: `#2196F3`

### bollinger bands.upper.linestyle[​](#bollinger-bandsupperlinestyle)
• bollinger bands.upper.linestyle: `number`

Default value: `0`

### bollinger bands.upper.linewidth[​](#bollinger-bandsupperlinewidth)
• bollinger bands.upper.linewidth: `number`

Default value: `1`

### bollinger bands.upper.plottype[​](#bollinger-bandsupperplottype)
• bollinger bands.upper.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### bollinger bands.upper.trackprice[​](#bollinger-bandsuppertrackprice)
• bollinger bands.upper.trackprice: `boolean`

Default value: `false`

### bollinger bands.upper.transparency[​](#bollinger-bandsuppertransparency)
• bollinger bands.upper.transparency: `number`

Default value: `0`

### bollinger bands.upper.visible[​](#bollinger-bandsuppervisible)
• bollinger bands.upper.visible: `boolean`

Default value: `true`

### candleStyle.barColorsOnPrevClose[​](#candlestylebarcolorsonprevclose)
• candleStyle.barColorsOnPrevClose: `boolean`

### candleStyle.borderColor[​](#candlestylebordercolor)
• candleStyle.borderColor: `string`

### candleStyle.borderDownColor[​](#candlestyleborderdowncolor)
• candleStyle.borderDownColor: `string`

### candleStyle.borderUpColor[​](#candlestyleborderupcolor)
• candleStyle.borderUpColor: `string`

### candleStyle.downColor[​](#candlestyledowncolor)
• candleStyle.downColor: `string`

### candleStyle.drawBody[​](#candlestyledrawbody)
• candleStyle.drawBody: `boolean`

### candleStyle.drawBorder[​](#candlestyledrawborder)
• candleStyle.drawBorder: `boolean`

### candleStyle.drawWick[​](#candlestyledrawwick)
• candleStyle.drawWick: `boolean`

### candleStyle.upColor[​](#candlestyleupcolor)
• candleStyle.upColor: `string`

### candleStyle.wickColor[​](#candlestylewickcolor)
• candleStyle.wickColor: `string`

### candleStyle.wickDownColor[​](#candlestylewickdowncolor)
• candleStyle.wickDownColor: `string`

### candleStyle.wickUpColor[​](#candlestylewickupcolor)
• candleStyle.wickUpColor: `string`

### chaikin money flow.length[​](#chaikin-money-flowlength)
• chaikin money flow.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### chaikin money flow.plot.color[​](#chaikin-money-flowplotcolor)
• chaikin money flow.plot.color: `string`

Default value: `#43A047`

### chaikin money flow.plot.display[​](#chaikin-money-flowplotdisplay)
• chaikin money flow.plot.display: `number`

Default value: `15`

### chaikin money flow.plot.linestyle[​](#chaikin-money-flowplotlinestyle)
• chaikin money flow.plot.linestyle: `number`

Default value: `0`

### chaikin money flow.plot.linewidth[​](#chaikin-money-flowplotlinewidth)
• chaikin money flow.plot.linewidth: `number`

Default value: `1`

### chaikin money flow.plot.plottype[​](#chaikin-money-flowplotplottype)
• chaikin money flow.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### chaikin money flow.plot.trackprice[​](#chaikin-money-flowplottrackprice)
• chaikin money flow.plot.trackprice: `boolean`

Default value: `false`

### chaikin money flow.plot.transparency[​](#chaikin-money-flowplottransparency)
• chaikin money flow.plot.transparency: `number`

Default value: `0`

### chaikin money flow.zero.color[​](#chaikin-money-flowzerocolor)
• chaikin money flow.zero.color: `string`

Default value: `#787B86`

### chaikin money flow.zero.linestyle[​](#chaikin-money-flowzerolinestyle)
• chaikin money flow.zero.linestyle: `number`

Default value: `2`

### chaikin money flow.zero.linewidth[​](#chaikin-money-flowzerolinewidth)
• chaikin money flow.zero.linewidth: `number`

Default value: `1`

### chaikin money flow.zero.value[​](#chaikin-money-flowzerovalue)
• chaikin money flow.zero.value: `number`

Default value: `0`

### chaikin money flow.zero.visible[​](#chaikin-money-flowzerovisible)
• chaikin money flow.zero.visible: `boolean`

Default value: `true`

### chaikin oscillator.long[​](#chaikin-oscillatorlong)
• chaikin oscillator.long: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### chaikin oscillator.plot.color[​](#chaikin-oscillatorplotcolor)
• chaikin oscillator.plot.color: `string`

Default value: `#EC407A`

### chaikin oscillator.plot.display[​](#chaikin-oscillatorplotdisplay)
• chaikin oscillator.plot.display: `number`

Default value: `15`

### chaikin oscillator.plot.linestyle[​](#chaikin-oscillatorplotlinestyle)
• chaikin oscillator.plot.linestyle: `number`

Default value: `0`

### chaikin oscillator.plot.linewidth[​](#chaikin-oscillatorplotlinewidth)
• chaikin oscillator.plot.linewidth: `number`

Default value: `1`

### chaikin oscillator.plot.plottype[​](#chaikin-oscillatorplotplottype)
• chaikin oscillator.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### chaikin oscillator.plot.trackprice[​](#chaikin-oscillatorplottrackprice)
• chaikin oscillator.plot.trackprice: `boolean`

Default value: `false`

### chaikin oscillator.plot.transparency[​](#chaikin-oscillatorplottransparency)
• chaikin oscillator.plot.transparency: `number`

Default value: `0`

### chaikin oscillator.short[​](#chaikin-oscillatorshort)
• chaikin oscillator.short: `number`

- Default value: `3`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### chaikin oscillator.zero.color[​](#chaikin-oscillatorzerocolor)
• chaikin oscillator.zero.color: `string`

Default value: `#787B86`

### chaikin oscillator.zero.linestyle[​](#chaikin-oscillatorzerolinestyle)
• chaikin oscillator.zero.linestyle: `number`

Default value: `2`

### chaikin oscillator.zero.linewidth[​](#chaikin-oscillatorzerolinewidth)
• chaikin oscillator.zero.linewidth: `number`

Default value: `1`

### chaikin oscillator.zero.value[​](#chaikin-oscillatorzerovalue)
• chaikin oscillator.zero.value: `number`

Default value: `0`

### chaikin oscillator.zero.visible[​](#chaikin-oscillatorzerovisible)
• chaikin oscillator.zero.visible: `boolean`

Default value: `true`

### chaikin volatility.periods[​](#chaikin-volatilityperiods)
• chaikin volatility.periods: `number`

- Default value: `10`
- Input type: `integer`

### chaikin volatility.plot.color[​](#chaikin-volatilityplotcolor)
• chaikin volatility.plot.color: `string`

Default value: `#AB47BC`

### chaikin volatility.plot.display[​](#chaikin-volatilityplotdisplay)
• chaikin volatility.plot.display: `number`

Default value: `15`

### chaikin volatility.plot.linestyle[​](#chaikin-volatilityplotlinestyle)
• chaikin volatility.plot.linestyle: `number`

Default value: `0`

### chaikin volatility.plot.linewidth[​](#chaikin-volatilityplotlinewidth)
• chaikin volatility.plot.linewidth: `number`

Default value: `1`

### chaikin volatility.plot.plottype[​](#chaikin-volatilityplotplottype)
• chaikin volatility.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### chaikin volatility.plot.trackprice[​](#chaikin-volatilityplottrackprice)
• chaikin volatility.plot.trackprice: `boolean`

Default value: `false`

### chaikin volatility.plot.transparency[​](#chaikin-volatilityplottransparency)
• chaikin volatility.plot.transparency: `number`

Default value: `0`

### chaikin volatility.rate of change lookback[​](#chaikin-volatilityrate-of-change-lookback)
• chaikin volatility.rate of change lookback: `number`

- Default value: `10`
- Input type: `integer`

### chaikin volatility.zero.color[​](#chaikin-volatilityzerocolor)
• chaikin volatility.zero.color: `string`

Default value: `#787B86`

### chaikin volatility.zero.linestyle[​](#chaikin-volatilityzerolinestyle)
• chaikin volatility.zero.linestyle: `number`

Default value: `2`

### chaikin volatility.zero.linewidth[​](#chaikin-volatilityzerolinewidth)
• chaikin volatility.zero.linewidth: `number`

Default value: `1`

### chaikin volatility.zero.value[​](#chaikin-volatilityzerovalue)
• chaikin volatility.zero.value: `number`

Default value: `0`

### chaikin volatility.zero.visible[​](#chaikin-volatilityzerovisible)
• chaikin volatility.zero.visible: `boolean`

Default value: `true`

### chande kroll stop.long.color[​](#chande-kroll-stoplongcolor)
• chande kroll stop.long.color: `string`

Default value: `#2196F3`

### chande kroll stop.long.display[​](#chande-kroll-stoplongdisplay)
• chande kroll stop.long.display: `number`

Default value: `15`

### chande kroll stop.long.linestyle[​](#chande-kroll-stoplonglinestyle)
• chande kroll stop.long.linestyle: `number`

Default value: `0`

### chande kroll stop.long.linewidth[​](#chande-kroll-stoplonglinewidth)
• chande kroll stop.long.linewidth: `number`

Default value: `1`

### chande kroll stop.long.plottype[​](#chande-kroll-stoplongplottype)
• chande kroll stop.long.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### chande kroll stop.long.trackprice[​](#chande-kroll-stoplongtrackprice)
• chande kroll stop.long.trackprice: `boolean`

Default value: `false`

### chande kroll stop.long.transparency[​](#chande-kroll-stoplongtransparency)
• chande kroll stop.long.transparency: `number`

Default value: `0`

### chande kroll stop.p[​](#chande-kroll-stopp)
• chande kroll stop.p: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `4999`

### chande kroll stop.q[​](#chande-kroll-stopq)
• chande kroll stop.q: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### chande kroll stop.short.color[​](#chande-kroll-stopshortcolor)
• chande kroll stop.short.color: `string`

Default value: `#FF6D00`

### chande kroll stop.short.display[​](#chande-kroll-stopshortdisplay)
• chande kroll stop.short.display: `number`

Default value: `15`

### chande kroll stop.short.linestyle[​](#chande-kroll-stopshortlinestyle)
• chande kroll stop.short.linestyle: `number`

Default value: `0`

### chande kroll stop.short.linewidth[​](#chande-kroll-stopshortlinewidth)
• chande kroll stop.short.linewidth: `number`

Default value: `1`

### chande kroll stop.short.plottype[​](#chande-kroll-stopshortplottype)
• chande kroll stop.short.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### chande kroll stop.short.trackprice[​](#chande-kroll-stopshorttrackprice)
• chande kroll stop.short.trackprice: `boolean`

Default value: `false`

### chande kroll stop.short.transparency[​](#chande-kroll-stopshorttransparency)
• chande kroll stop.short.transparency: `number`

Default value: `0`

### chande kroll stop.x[​](#chande-kroll-stopx)
• chande kroll stop.x: `number`

- Default value: `1`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### chande momentum oscillator.length[​](#chande-momentum-oscillatorlength)
• chande momentum oscillator.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### chande momentum oscillator.plot.color[​](#chande-momentum-oscillatorplotcolor)
• chande momentum oscillator.plot.color: `string`

Default value: `#2196F3`

### chande momentum oscillator.plot.display[​](#chande-momentum-oscillatorplotdisplay)
• chande momentum oscillator.plot.display: `number`

Default value: `15`

### chande momentum oscillator.plot.linestyle[​](#chande-momentum-oscillatorplotlinestyle)
• chande momentum oscillator.plot.linestyle: `number`

Default value: `0`

### chande momentum oscillator.plot.linewidth[​](#chande-momentum-oscillatorplotlinewidth)
• chande momentum oscillator.plot.linewidth: `number`

Default value: `1`

### chande momentum oscillator.plot.plottype[​](#chande-momentum-oscillatorplotplottype)
• chande momentum oscillator.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### chande momentum oscillator.plot.trackprice[​](#chande-momentum-oscillatorplottrackprice)
• chande momentum oscillator.plot.trackprice: `boolean`

Default value: `false`

### chande momentum oscillator.plot.transparency[​](#chande-momentum-oscillatorplottransparency)
• chande momentum oscillator.plot.transparency: `number`

Default value: `0`

### chop zone.plot.color[​](#chop-zoneplotcolor)
• chop zone.plot.color: `string`

Default value: `#000080`

### chop zone.plot.display[​](#chop-zoneplotdisplay)
• chop zone.plot.display: `number`

Default value: `15`

### chop zone.plot.linestyle[​](#chop-zoneplotlinestyle)
• chop zone.plot.linestyle: `number`

Default value: `0`

### chop zone.plot.linewidth[​](#chop-zoneplotlinewidth)
• chop zone.plot.linewidth: `number`

Default value: `1`

### chop zone.plot.plottype[​](#chop-zoneplotplottype)
• chop zone.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `columns`

### chop zone.plot.trackprice[​](#chop-zoneplottrackprice)
• chop zone.plot.trackprice: `boolean`

Default value: `false`

### chop zone.plot.transparency[​](#chop-zoneplottransparency)
• chop zone.plot.transparency: `number`

Default value: `0`

### choppiness index.hlines background.color[​](#choppiness-indexhlines-backgroundcolor)
• choppiness index.hlines background.color: `string`

Default value: `#2196F3`

### choppiness index.hlines background.transparency[​](#choppiness-indexhlines-backgroundtransparency)
• choppiness index.hlines background.transparency: `number`

Default value: `90`

### choppiness index.hlines background.visible[​](#choppiness-indexhlines-backgroundvisible)
• choppiness index.hlines background.visible: `boolean`

Default value: `true`

### choppiness index.length[​](#choppiness-indexlength)
• choppiness index.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### choppiness index.lowerlimit.color[​](#choppiness-indexlowerlimitcolor)
• choppiness index.lowerlimit.color: `string`

Default value: `#787B86`

### choppiness index.lowerlimit.linestyle[​](#choppiness-indexlowerlimitlinestyle)
• choppiness index.lowerlimit.linestyle: `number`

Default value: `2`

### choppiness index.lowerlimit.linewidth[​](#choppiness-indexlowerlimitlinewidth)
• choppiness index.lowerlimit.linewidth: `number`

Default value: `1`

### choppiness index.lowerlimit.value[​](#choppiness-indexlowerlimitvalue)
• choppiness index.lowerlimit.value: `number`

Default value: `38.2`

### choppiness index.lowerlimit.visible[​](#choppiness-indexlowerlimitvisible)
• choppiness index.lowerlimit.visible: `boolean`

Default value: `true`

### choppiness index.plot.color[​](#choppiness-indexplotcolor)
• choppiness index.plot.color: `string`

Default value: `#2196F3`

### choppiness index.plot.display[​](#choppiness-indexplotdisplay)
• choppiness index.plot.display: `number`

Default value: `15`

### choppiness index.plot.linestyle[​](#choppiness-indexplotlinestyle)
• choppiness index.plot.linestyle: `number`

Default value: `0`

### choppiness index.plot.linewidth[​](#choppiness-indexplotlinewidth)
• choppiness index.plot.linewidth: `number`

Default value: `1`

### choppiness index.plot.plottype[​](#choppiness-indexplotplottype)
• choppiness index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### choppiness index.plot.trackprice[​](#choppiness-indexplottrackprice)
• choppiness index.plot.trackprice: `boolean`

Default value: `false`

### choppiness index.plot.transparency[​](#choppiness-indexplottransparency)
• choppiness index.plot.transparency: `number`

Default value: `0`

### choppiness index.upperlimit.color[​](#choppiness-indexupperlimitcolor)
• choppiness index.upperlimit.color: `string`

Default value: `#787B86`

### choppiness index.upperlimit.linestyle[​](#choppiness-indexupperlimitlinestyle)
• choppiness index.upperlimit.linestyle: `number`

Default value: `2`

### choppiness index.upperlimit.linewidth[​](#choppiness-indexupperlimitlinewidth)
• choppiness index.upperlimit.linewidth: `number`

Default value: `1`

### choppiness index.upperlimit.value[​](#choppiness-indexupperlimitvalue)
• choppiness index.upperlimit.value: `number`

Default value: `61.8`

### choppiness index.upperlimit.visible[​](#choppiness-indexupperlimitvisible)
• choppiness index.upperlimit.visible: `boolean`

Default value: `true`

### columnStyle.barColorsOnPrevClose[​](#columnstylebarcolorsonprevclose)
• columnStyle.barColorsOnPrevClose: `boolean`

### columnStyle.baselinePosition[​](#columnstylebaselineposition)
• columnStyle.baselinePosition: `string`

### columnStyle.downColor[​](#columnstyledowncolor)
• columnStyle.downColor: `string`

### columnStyle.upColor[​](#columnstyleupcolor)
• columnStyle.upColor: `string`

### commodity channel index.hlines background.color[​](#commodity-channel-indexhlines-backgroundcolor)
• commodity channel index.hlines background.color: `string`

Default value: `#2196F3`

### commodity channel index.hlines background.transparency[​](#commodity-channel-indexhlines-backgroundtransparency)
• commodity channel index.hlines background.transparency: `number`

Default value: `90`

### commodity channel index.hlines background.visible[​](#commodity-channel-indexhlines-backgroundvisible)
• commodity channel index.hlines background.visible: `boolean`

Default value: `true`

### commodity channel index.length[​](#commodity-channel-indexlength)
• commodity channel index.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### commodity channel index.lowerlimit.color[​](#commodity-channel-indexlowerlimitcolor)
• commodity channel index.lowerlimit.color: `string`

Default value: `#787B86`

### commodity channel index.lowerlimit.linestyle[​](#commodity-channel-indexlowerlimitlinestyle)
• commodity channel index.lowerlimit.linestyle: `number`

Default value: `2`

### commodity channel index.lowerlimit.linewidth[​](#commodity-channel-indexlowerlimitlinewidth)
• commodity channel index.lowerlimit.linewidth: `number`

Default value: `1`

### commodity channel index.lowerlimit.value[​](#commodity-channel-indexlowerlimitvalue)
• commodity channel index.lowerlimit.value: `number`

Default value: `-100`

### commodity channel index.lowerlimit.visible[​](#commodity-channel-indexlowerlimitvisible)
• commodity channel index.lowerlimit.visible: `boolean`

Default value: `true`

### commodity channel index.plot.color[​](#commodity-channel-indexplotcolor)
• commodity channel index.plot.color: `string`

Default value: `#2196F3`

### commodity channel index.plot.display[​](#commodity-channel-indexplotdisplay)
• commodity channel index.plot.display: `number`

Default value: `15`

### commodity channel index.plot.linestyle[​](#commodity-channel-indexplotlinestyle)
• commodity channel index.plot.linestyle: `number`

Default value: `0`

### commodity channel index.plot.linewidth[​](#commodity-channel-indexplotlinewidth)
• commodity channel index.plot.linewidth: `number`

Default value: `1`

### commodity channel index.plot.plottype[​](#commodity-channel-indexplotplottype)
• commodity channel index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### commodity channel index.plot.trackprice[​](#commodity-channel-indexplottrackprice)
• commodity channel index.plot.trackprice: `boolean`

Default value: `false`

### commodity channel index.plot.transparency[​](#commodity-channel-indexplottransparency)
• commodity channel index.plot.transparency: `number`

Default value: `0`

### commodity channel index.smoothed ma.display[​](#commodity-channel-indexsmoothed-madisplay)
• commodity channel index.smoothed ma.display: `number`

Default value: `0`

### commodity channel index.smoothed ma.linestyle[​](#commodity-channel-indexsmoothed-malinestyle)
• commodity channel index.smoothed ma.linestyle: `number`

Default value: `0`

### commodity channel index.smoothed ma.linewidth[​](#commodity-channel-indexsmoothed-malinewidth)
• commodity channel index.smoothed ma.linewidth: `number`

Default value: `1`

### commodity channel index.smoothed ma.plottype[​](#commodity-channel-indexsmoothed-maplottype)
• commodity channel index.smoothed ma.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### commodity channel index.smoothed ma.trackprice[​](#commodity-channel-indexsmoothed-matrackprice)
• commodity channel index.smoothed ma.trackprice: `boolean`

Default value: `false`

### commodity channel index.smoothed ma.transparency[​](#commodity-channel-indexsmoothed-matransparency)
• commodity channel index.smoothed ma.transparency: `number`

Default value: `0`

### commodity channel index.smoothing length[​](#commodity-channel-indexsmoothing-length)
• commodity channel index.smoothing length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### commodity channel index.smoothing line[​](#commodity-channel-indexsmoothing-line)
• commodity channel index.smoothing line: `string`

- Default value: `SMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### commodity channel index.upperlimit.color[​](#commodity-channel-indexupperlimitcolor)
• commodity channel index.upperlimit.color: `string`

Default value: `#787B86`

### commodity channel index.upperlimit.linestyle[​](#commodity-channel-indexupperlimitlinestyle)
• commodity channel index.upperlimit.linestyle: `number`

Default value: `2`

### commodity channel index.upperlimit.linewidth[​](#commodity-channel-indexupperlimitlinewidth)
• commodity channel index.upperlimit.linewidth: `number`

Default value: `1`

### commodity channel index.upperlimit.value[​](#commodity-channel-indexupperlimitvalue)
• commodity channel index.upperlimit.value: `number`

Default value: `100`

### commodity channel index.upperlimit.visible[​](#commodity-channel-indexupperlimitvisible)
• commodity channel index.upperlimit.visible: `boolean`

Default value: `true`

### compare.plot.color[​](#compareplotcolor)
• compare.plot.color: `string`

Default value: `#9C27B0`

### compare.plot.display[​](#compareplotdisplay)
• compare.plot.display: `number`

Default value: `15`

### compare.plot.linestyle[​](#compareplotlinestyle)
• compare.plot.linestyle: `number`

Default value: `0`

### compare.plot.linewidth[​](#compareplotlinewidth)
• compare.plot.linewidth: `number`

Default value: `2`

### compare.plot.plottype[​](#compareplotplottype)
• compare.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### compare.plot.trackprice[​](#compareplottrackprice)
• compare.plot.trackprice: `boolean`

Default value: `false`

### compare.plot.transparency[​](#compareplottransparency)
• compare.plot.transparency: `number`

Default value: `0`

### compare.source[​](#comparesource)
• compare.source: `string`

- Default value: `close`
- Input type: `text`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### compare.symbol[​](#comparesymbol)
• compare.symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- IsHidden: `true`

### connors rsi.crsi.color[​](#connors-rsicrsicolor)
• connors rsi.crsi.color: `string`

Default value: `#2196F3`

### connors rsi.crsi.display[​](#connors-rsicrsidisplay)
• connors rsi.crsi.display: `number`

Default value: `15`

### connors rsi.crsi.linestyle[​](#connors-rsicrsilinestyle)
• connors rsi.crsi.linestyle: `number`

Default value: `0`

### connors rsi.crsi.linewidth[​](#connors-rsicrsilinewidth)
• connors rsi.crsi.linewidth: `number`

Default value: `1`

### connors rsi.crsi.plottype[​](#connors-rsicrsiplottype)
• connors rsi.crsi.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### connors rsi.crsi.trackprice[​](#connors-rsicrsitrackprice)
• connors rsi.crsi.trackprice: `boolean`

Default value: `false`

### connors rsi.crsi.transparency[​](#connors-rsicrsitransparency)
• connors rsi.crsi.transparency: `number`

Default value: `0`

### connors rsi.hlines background.color[​](#connors-rsihlines-backgroundcolor)
• connors rsi.hlines background.color: `string`

Default value: `#2196F3`

### connors rsi.hlines background.transparency[​](#connors-rsihlines-backgroundtransparency)
• connors rsi.hlines background.transparency: `number`

Default value: `90`

### connors rsi.hlines background.visible[​](#connors-rsihlines-backgroundvisible)
• connors rsi.hlines background.visible: `boolean`

Default value: `true`

### connors rsi.lowerlimit.color[​](#connors-rsilowerlimitcolor)
• connors rsi.lowerlimit.color: `string`

Default value: `#787B86`

### connors rsi.lowerlimit.linestyle[​](#connors-rsilowerlimitlinestyle)
• connors rsi.lowerlimit.linestyle: `number`

Default value: `2`

### connors rsi.lowerlimit.linewidth[​](#connors-rsilowerlimitlinewidth)
• connors rsi.lowerlimit.linewidth: `number`

Default value: `1`

### connors rsi.lowerlimit.value[​](#connors-rsilowerlimitvalue)
• connors rsi.lowerlimit.value: `number`

Default value: `30`

### connors rsi.lowerlimit.visible[​](#connors-rsilowerlimitvisible)
• connors rsi.lowerlimit.visible: `boolean`

Default value: `true`

### connors rsi.roc length[​](#connors-rsiroc-length)
• connors rsi.roc length: `number`

- Default value: `100`
- Input type: `integer`
- Min: `1`

### connors rsi.rsi length[​](#connors-rsirsi-length)
• connors rsi.rsi length: `number`

- Default value: `3`
- Input type: `integer`
- Min: `1`

### connors rsi.updown length[​](#connors-rsiupdown-length)
• connors rsi.updown length: `number`

- Default value: `2`
- Input type: `integer`
- Min: `1`

### connors rsi.upperlimit.color[​](#connors-rsiupperlimitcolor)
• connors rsi.upperlimit.color: `string`

Default value: `#787B86`

### connors rsi.upperlimit.linestyle[​](#connors-rsiupperlimitlinestyle)
• connors rsi.upperlimit.linestyle: `number`

Default value: `2`

### connors rsi.upperlimit.linewidth[​](#connors-rsiupperlimitlinewidth)
• connors rsi.upperlimit.linewidth: `number`

Default value: `1`

### connors rsi.upperlimit.value[​](#connors-rsiupperlimitvalue)
• connors rsi.upperlimit.value: `number`

Default value: `70`

### connors rsi.upperlimit.visible[​](#connors-rsiupperlimitvisible)
• connors rsi.upperlimit.visible: `boolean`

Default value: `true`

### coppock curve.long roc length[​](#coppock-curvelong-roc-length)
• coppock curve.long roc length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `4999`

### coppock curve.plot.color[​](#coppock-curveplotcolor)
• coppock curve.plot.color: `string`

Default value: `#2196F3`

### coppock curve.plot.display[​](#coppock-curveplotdisplay)
• coppock curve.plot.display: `number`

Default value: `15`

### coppock curve.plot.linestyle[​](#coppock-curveplotlinestyle)
• coppock curve.plot.linestyle: `number`

Default value: `0`

### coppock curve.plot.linewidth[​](#coppock-curveplotlinewidth)
• coppock curve.plot.linewidth: `number`

Default value: `1`

### coppock curve.plot.plottype[​](#coppock-curveplotplottype)
• coppock curve.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### coppock curve.plot.trackprice[​](#coppock-curveplottrackprice)
• coppock curve.plot.trackprice: `boolean`

Default value: `false`

### coppock curve.plot.transparency[​](#coppock-curveplottransparency)
• coppock curve.plot.transparency: `number`

Default value: `0`

### coppock curve.short roc length[​](#coppock-curveshort-roc-length)
• coppock curve.short roc length: `number`

- Default value: `11`
- Input type: `integer`
- Min: `1`
- Max: `4999`

### coppock curve.wma length[​](#coppock-curvewma-length)
• coppock curve.wma length: `number`

- Default value: `10`
- Input type: `integer`
- Min: `-1000000000000`
- Max: `5000`

### correlation - log.instrument 1[​](#correlation---loginstrument-1)
• correlation - log.instrument 1: `string`

- Default value: `undefined`
- Input type: `symbol`
- Confirm: `true`

### correlation - log.instrument 2[​](#correlation---loginstrument-2)
• correlation - log.instrument 2: `string`

- Default value: `undefined`
- Input type: `symbol`
- Confirm: `true`

### correlation - log.periods[​](#correlation---logperiods)
• correlation - log.periods: `number`

- Default value: `25`
- Input type: `integer`

### correlation - log.plot.color[​](#correlation---logplotcolor)
• correlation - log.plot.color: `string`

Default value: `#2196F3`

### correlation - log.plot.display[​](#correlation---logplotdisplay)
• correlation - log.plot.display: `number`

Default value: `15`

### correlation - log.plot.linestyle[​](#correlation---logplotlinestyle)
• correlation - log.plot.linestyle: `number`

Default value: `0`

### correlation - log.plot.linewidth[​](#correlation---logplotlinewidth)
• correlation - log.plot.linewidth: `number`

Default value: `1`

### correlation - log.plot.plottype[​](#correlation---logplotplottype)
• correlation - log.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### correlation - log.plot.trackprice[​](#correlation---logplottrackprice)
• correlation - log.plot.trackprice: `boolean`

Default value: `false`

### correlation - log.plot.transparency[​](#correlation---logplottransparency)
• correlation - log.plot.transparency: `number`

Default value: `0`

### correlation coefficient.length[​](#correlation-coefficientlength)
• correlation coefficient.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### correlation coefficient.plot.color[​](#correlation-coefficientplotcolor)
• correlation coefficient.plot.color: `string`

Default value: `#2196F3`

### correlation coefficient.plot.display[​](#correlation-coefficientplotdisplay)
• correlation coefficient.plot.display: `number`

Default value: `15`

### correlation coefficient.plot.linestyle[​](#correlation-coefficientplotlinestyle)
• correlation coefficient.plot.linestyle: `number`

Default value: `0`

### correlation coefficient.plot.linewidth[​](#correlation-coefficientplotlinewidth)
• correlation coefficient.plot.linewidth: `number`

Default value: `1`

### correlation coefficient.plot.plottype[​](#correlation-coefficientplotplottype)
• correlation coefficient.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `area`

### correlation coefficient.plot.trackprice[​](#correlation-coefficientplottrackprice)
• correlation coefficient.plot.trackprice: `boolean`

Default value: `false`

### correlation coefficient.plot.transparency[​](#correlation-coefficientplottransparency)
• correlation coefficient.plot.transparency: `number`

Default value: `0`

### correlation coefficient.sym[​](#correlation-coefficientsym)
• correlation coefficient.sym: `string`

- Default value: `undefined`
- Input type: `symbol`

### detrended price oscillator.dpo.color[​](#detrended-price-oscillatordpocolor)
• detrended price oscillator.dpo.color: `string`

Default value: `#43A047`

### detrended price oscillator.dpo.display[​](#detrended-price-oscillatordpodisplay)
• detrended price oscillator.dpo.display: `number`

Default value: `15`

### detrended price oscillator.dpo.linestyle[​](#detrended-price-oscillatordpolinestyle)
• detrended price oscillator.dpo.linestyle: `number`

Default value: `0`

### detrended price oscillator.dpo.linewidth[​](#detrended-price-oscillatordpolinewidth)
• detrended price oscillator.dpo.linewidth: `number`

Default value: `1`

### detrended price oscillator.dpo.plottype[​](#detrended-price-oscillatordpoplottype)
• detrended price oscillator.dpo.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### detrended price oscillator.dpo.trackprice[​](#detrended-price-oscillatordpotrackprice)
• detrended price oscillator.dpo.trackprice: `boolean`

Default value: `false`

### detrended price oscillator.dpo.transparency[​](#detrended-price-oscillatordpotransparency)
• detrended price oscillator.dpo.transparency: `number`

Default value: `0`

### detrended price oscillator.iscentered[​](#detrended-price-oscillatoriscentered)
• detrended price oscillator.iscentered: `boolean`

- Default value: `false`
- Input type: `bool`

### detrended price oscillator.period[​](#detrended-price-oscillatorperiod)
• detrended price oscillator.period: `number`

- Default value: `21`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### detrended price oscillator.zero.color[​](#detrended-price-oscillatorzerocolor)
• detrended price oscillator.zero.color: `string`

Default value: `#787B86`

### detrended price oscillator.zero.linestyle[​](#detrended-price-oscillatorzerolinestyle)
• detrended price oscillator.zero.linestyle: `number`

Default value: `2`

### detrended price oscillator.zero.linewidth[​](#detrended-price-oscillatorzerolinewidth)
• detrended price oscillator.zero.linewidth: `number`

Default value: `1`

### detrended price oscillator.zero.value[​](#detrended-price-oscillatorzerovalue)
• detrended price oscillator.zero.value: `number`

Default value: `0`

### detrended price oscillator.zero.visible[​](#detrended-price-oscillatorzerovisible)
• detrended price oscillator.zero.visible: `boolean`

Default value: `true`

### directional movement.+di.color[​](#directional-movementdicolor)
• directional movement.+di.color: `string`

Default value: `#2196F3`

### directional movement.+di.display[​](#directional-movementdidisplay)
• directional movement.+di.display: `number`

Default value: `15`

### directional movement.+di.linestyle[​](#directional-movementdilinestyle)
• directional movement.+di.linestyle: `number`

Default value: `0`

### directional movement.+di.linewidth[​](#directional-movementdilinewidth)
• directional movement.+di.linewidth: `number`

Default value: `1`

### directional movement.+di.plottype[​](#directional-movementdiplottype)
• directional movement.+di.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### directional movement.+di.trackprice[​](#directional-movementditrackprice)
• directional movement.+di.trackprice: `boolean`

Default value: `false`

### directional movement.+di.transparency[​](#directional-movementditransparency)
• directional movement.+di.transparency: `number`

Default value: `0`

### directional movement.-di.color[​](#directional-movement-dicolor)
• directional movement.-di.color: `string`

Default value: `#FF6D00`

### directional movement.-di.display[​](#directional-movement-didisplay)
• directional movement.-di.display: `number`

Default value: `15`

### directional movement.-di.linestyle[​](#directional-movement-dilinestyle)
• directional movement.-di.linestyle: `number`

Default value: `0`

### directional movement.-di.linewidth[​](#directional-movement-dilinewidth)
• directional movement.-di.linewidth: `number`

Default value: `1`

### directional movement.-di.plottype[​](#directional-movement-diplottype)
• directional movement.-di.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### directional movement.-di.trackprice[​](#directional-movement-ditrackprice)
• directional movement.-di.trackprice: `boolean`

Default value: `false`

### directional movement.-di.transparency[​](#directional-movement-ditransparency)
• directional movement.-di.transparency: `number`

Default value: `0`

### directional movement.adx smoothing[​](#directional-movementadx-smoothing)
• directional movement.adx smoothing: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `50`

### directional movement.adx.color[​](#directional-movementadxcolor)
• directional movement.adx.color: `string`

Default value: `#F50057`

### directional movement.adx.display[​](#directional-movementadxdisplay)
• directional movement.adx.display: `number`

Default value: `15`

### directional movement.adx.linestyle[​](#directional-movementadxlinestyle)
• directional movement.adx.linestyle: `number`

Default value: `0`

### directional movement.adx.linewidth[​](#directional-movementadxlinewidth)
• directional movement.adx.linewidth: `number`

Default value: `1`

### directional movement.adx.plottype[​](#directional-movementadxplottype)
• directional movement.adx.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### directional movement.adx.trackprice[​](#directional-movementadxtrackprice)
• directional movement.adx.trackprice: `boolean`

Default value: `false`

### directional movement.adx.transparency[​](#directional-movementadxtransparency)
• directional movement.adx.transparency: `number`

Default value: `0`

### directional movement.adxr.color[​](#directional-movementadxrcolor)
• directional movement.adxr.color: `string`

Default value: `#ab47bc`

### directional movement.adxr.display[​](#directional-movementadxrdisplay)
• directional movement.adxr.display: `number`

Default value: `15`

### directional movement.adxr.linestyle[​](#directional-movementadxrlinestyle)
• directional movement.adxr.linestyle: `number`

Default value: `0`

### directional movement.adxr.linewidth[​](#directional-movementadxrlinewidth)
• directional movement.adxr.linewidth: `number`

Default value: `1`

### directional movement.adxr.plottype[​](#directional-movementadxrplottype)
• directional movement.adxr.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### directional movement.adxr.trackprice[​](#directional-movementadxrtrackprice)
• directional movement.adxr.trackprice: `boolean`

Default value: `false`

### directional movement.adxr.transparency[​](#directional-movementadxrtransparency)
• directional movement.adxr.transparency: `number`

Default value: `0`

### directional movement.di length[​](#directional-movementdi-length)
• directional movement.di length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### directional movement.dx.color[​](#directional-movementdxcolor)
• directional movement.dx.color: `string`

Default value: `#FFA726`

### directional movement.dx.display[​](#directional-movementdxdisplay)
• directional movement.dx.display: `number`

Default value: `15`

### directional movement.dx.linestyle[​](#directional-movementdxlinestyle)
• directional movement.dx.linestyle: `number`

Default value: `0`

### directional movement.dx.linewidth[​](#directional-movementdxlinewidth)
• directional movement.dx.linewidth: `number`

Default value: `1`

### directional movement.dx.plottype[​](#directional-movementdxplottype)
• directional movement.dx.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### directional movement.dx.trackprice[​](#directional-movementdxtrackprice)
• directional movement.dx.trackprice: `boolean`

Default value: `false`

### directional movement.dx.transparency[​](#directional-movementdxtransparency)
• directional movement.dx.transparency: `number`

Default value: `0`

### donchian channels.basis.color[​](#donchian-channelsbasiscolor)
• donchian channels.basis.color: `string`

Default value: `#FF6D00`

### donchian channels.basis.display[​](#donchian-channelsbasisdisplay)
• donchian channels.basis.display: `number`

Default value: `15`

### donchian channels.basis.linestyle[​](#donchian-channelsbasislinestyle)
• donchian channels.basis.linestyle: `number`

Default value: `0`

### donchian channels.basis.linewidth[​](#donchian-channelsbasislinewidth)
• donchian channels.basis.linewidth: `number`

Default value: `1`

### donchian channels.basis.plottype[​](#donchian-channelsbasisplottype)
• donchian channels.basis.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### donchian channels.basis.trackprice[​](#donchian-channelsbasistrackprice)
• donchian channels.basis.trackprice: `boolean`

Default value: `false`

### donchian channels.basis.transparency[​](#donchian-channelsbasistransparency)
• donchian channels.basis.transparency: `number`

Default value: `0`

### donchian channels.length[​](#donchian-channelslength)
• donchian channels.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### donchian channels.lower.color[​](#donchian-channelslowercolor)
• donchian channels.lower.color: `string`

Default value: `#2196F3`

### donchian channels.lower.display[​](#donchian-channelslowerdisplay)
• donchian channels.lower.display: `number`

Default value: `15`

### donchian channels.lower.linestyle[​](#donchian-channelslowerlinestyle)
• donchian channels.lower.linestyle: `number`

Default value: `0`

### donchian channels.lower.linewidth[​](#donchian-channelslowerlinewidth)
• donchian channels.lower.linewidth: `number`

Default value: `1`

### donchian channels.lower.plottype[​](#donchian-channelslowerplottype)
• donchian channels.lower.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### donchian channels.lower.trackprice[​](#donchian-channelslowertrackprice)
• donchian channels.lower.trackprice: `boolean`

Default value: `false`

### donchian channels.lower.transparency[​](#donchian-channelslowertransparency)
• donchian channels.lower.transparency: `number`

Default value: `0`

### donchian channels.offset[​](#donchian-channelsoffset)
• donchian channels.offset: `number`

- Default value: `0`
- Input type: `integer`
- Min: `-1000`
- Max: `1000`

### donchian channels.plots background.color[​](#donchian-channelsplots-backgroundcolor)
• donchian channels.plots background.color: `string`

Default value: `#2196F3`

### donchian channels.plots background.transparency[​](#donchian-channelsplots-backgroundtransparency)
• donchian channels.plots background.transparency: `number`

Default value: `95`

### donchian channels.plots background.visible[​](#donchian-channelsplots-backgroundvisible)
• donchian channels.plots background.visible: `boolean`

Default value: `true`

### donchian channels.upper.color[​](#donchian-channelsuppercolor)
• donchian channels.upper.color: `string`

Default value: `#2196F3`

### donchian channels.upper.display[​](#donchian-channelsupperdisplay)
• donchian channels.upper.display: `number`

Default value: `15`

### donchian channels.upper.linestyle[​](#donchian-channelsupperlinestyle)
• donchian channels.upper.linestyle: `number`

Default value: `0`

### donchian channels.upper.linewidth[​](#donchian-channelsupperlinewidth)
• donchian channels.upper.linewidth: `number`

Default value: `1`

### donchian channels.upper.plottype[​](#donchian-channelsupperplottype)
• donchian channels.upper.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### donchian channels.upper.trackprice[​](#donchian-channelsuppertrackprice)
• donchian channels.upper.trackprice: `boolean`

Default value: `false`

### donchian channels.upper.transparency[​](#donchian-channelsuppertransparency)
• donchian channels.upper.transparency: `number`

Default value: `0`

### double ema.length[​](#double-emalength)
• double ema.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### double ema.plot.color[​](#double-emaplotcolor)
• double ema.plot.color: `string`

Default value: `#43A047`

### double ema.plot.display[​](#double-emaplotdisplay)
• double ema.plot.display: `number`

Default value: `15`

### double ema.plot.linestyle[​](#double-emaplotlinestyle)
• double ema.plot.linestyle: `number`

Default value: `0`

### double ema.plot.linewidth[​](#double-emaplotlinewidth)
• double ema.plot.linewidth: `number`

Default value: `1`

### double ema.plot.plottype[​](#double-emaplotplottype)
• double ema.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### double ema.plot.trackprice[​](#double-emaplottrackprice)
• double ema.plot.trackprice: `boolean`

Default value: `false`

### double ema.plot.transparency[​](#double-emaplottransparency)
• double ema.plot.transparency: `number`

Default value: `0`

### ease of movement.divisor[​](#ease-of-movementdivisor)
• ease of movement.divisor: `number`

- Default value: `10000`
- Input type: `integer`
- Min: `1`
- Max: `1000000000`

### ease of movement.length[​](#ease-of-movementlength)
• ease of movement.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### ease of movement.plot.color[​](#ease-of-movementplotcolor)
• ease of movement.plot.color: `string`

Default value: `#43A047`

### ease of movement.plot.display[​](#ease-of-movementplotdisplay)
• ease of movement.plot.display: `number`

Default value: `15`

### ease of movement.plot.linestyle[​](#ease-of-movementplotlinestyle)
• ease of movement.plot.linestyle: `number`

Default value: `0`

### ease of movement.plot.linewidth[​](#ease-of-movementplotlinewidth)
• ease of movement.plot.linewidth: `number`

Default value: `1`

### ease of movement.plot.plottype[​](#ease-of-movementplotplottype)
• ease of movement.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ease of movement.plot.trackprice[​](#ease-of-movementplottrackprice)
• ease of movement.plot.trackprice: `boolean`

Default value: `false`

### ease of movement.plot.transparency[​](#ease-of-movementplottransparency)
• ease of movement.plot.transparency: `number`

Default value: `0`

### elder's force index.length[​](#elders-force-indexlength)
• elder's force index.length: `number`

- Default value: `13`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### elder's force index.plot.color[​](#elders-force-indexplotcolor)
• elder's force index.plot.color: `string`

Default value: `#F23645`

### elder's force index.plot.display[​](#elders-force-indexplotdisplay)
• elder's force index.plot.display: `number`

Default value: `15`

### elder's force index.plot.linestyle[​](#elders-force-indexplotlinestyle)
• elder's force index.plot.linestyle: `number`

Default value: `0`

### elder's force index.plot.linewidth[​](#elders-force-indexplotlinewidth)
• elder's force index.plot.linewidth: `number`

Default value: `1`

### elder's force index.plot.plottype[​](#elders-force-indexplotplottype)
• elder's force index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### elder's force index.plot.trackprice[​](#elders-force-indexplottrackprice)
• elder's force index.plot.trackprice: `boolean`

Default value: `false`

### elder's force index.plot.transparency[​](#elders-force-indexplottransparency)
• elder's force index.plot.transparency: `number`

Default value: `0`

### elder's force index.zero.color[​](#elders-force-indexzerocolor)
• elder's force index.zero.color: `string`

Default value: `#787B86`

### elder's force index.zero.linestyle[​](#elders-force-indexzerolinestyle)
• elder's force index.zero.linestyle: `number`

Default value: `2`

### elder's force index.zero.linewidth[​](#elders-force-indexzerolinewidth)
• elder's force index.zero.linewidth: `number`

Default value: `1`

### elder's force index.zero.value[​](#elders-force-indexzerovalue)
• elder's force index.zero.value: `number`

Default value: `0`

### elder's force index.zero.visible[​](#elders-force-indexzerovisible)
• elder's force index.zero.visible: `boolean`

Default value: `true`

### ema cross.crosses.color[​](#ema-crosscrossescolor)
• ema cross.crosses.color: `string`

Default value: `#2196F3`

### ema cross.crosses.display[​](#ema-crosscrossesdisplay)
• ema cross.crosses.display: `number`

Default value: `15`

### ema cross.crosses.linestyle[​](#ema-crosscrosseslinestyle)
• ema cross.crosses.linestyle: `number`

Default value: `0`

### ema cross.crosses.linewidth[​](#ema-crosscrosseslinewidth)
• ema cross.crosses.linewidth: `number`

Default value: `4`

### ema cross.crosses.plottype[​](#ema-crosscrossesplottype)
• ema cross.crosses.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `cross`

### ema cross.crosses.trackprice[​](#ema-crosscrossestrackprice)
• ema cross.crosses.trackprice: `boolean`

Default value: `false`

### ema cross.crosses.transparency[​](#ema-crosscrossestransparency)
• ema cross.crosses.transparency: `number`

Default value: `0`

### ema cross.long:input[​](#ema-crosslong)
• ema cross.long:input: `number`

- Default value: `26`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### ema cross.long:plot.color[​](#ema-crosslongcolor)
• ema cross.long:plot.color: `string`

Default value: `#43A047`

### ema cross.long:plot.display[​](#ema-crosslongdisplay)
• ema cross.long:plot.display: `number`

Default value: `15`

### ema cross.long:plot.linestyle[​](#ema-crosslonglinestyle)
• ema cross.long:plot.linestyle: `number`

Default value: `0`

### ema cross.long:plot.linewidth[​](#ema-crosslonglinewidth)
• ema cross.long:plot.linewidth: `number`

Default value: `1`

### ema cross.long:plot.plottype[​](#ema-crosslongplottype)
• ema cross.long:plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ema cross.long:plot.trackprice[​](#ema-crosslongtrackprice)
• ema cross.long:plot.trackprice: `boolean`

Default value: `false`

### ema cross.long:plot.transparency[​](#ema-crosslongtransparency)
• ema cross.long:plot.transparency: `number`

Default value: `0`

### ema cross.short:input[​](#ema-crossshort)
• ema cross.short:input: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### ema cross.short:plot.color[​](#ema-crossshortcolor)
• ema cross.short:plot.color: `string`

Default value: `#FF6D00`

### ema cross.short:plot.display[​](#ema-crossshortdisplay)
• ema cross.short:plot.display: `number`

Default value: `15`

### ema cross.short:plot.linestyle[​](#ema-crossshortlinestyle)
• ema cross.short:plot.linestyle: `number`

Default value: `0`

### ema cross.short:plot.linewidth[​](#ema-crossshortlinewidth)
• ema cross.short:plot.linewidth: `number`

Default value: `1`

### ema cross.short:plot.plottype[​](#ema-crossshortplottype)
• ema cross.short:plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ema cross.short:plot.trackprice[​](#ema-crossshorttrackprice)
• ema cross.short:plot.trackprice: `boolean`

Default value: `false`

### ema cross.short:plot.transparency[​](#ema-crossshorttransparency)
• ema cross.short:plot.transparency: `number`

Default value: `0`

### envelopes.average.color[​](#envelopesaveragecolor)
• envelopes.average.color: `string`

Default value: `#FF6D00`

### envelopes.average.display[​](#envelopesaveragedisplay)
• envelopes.average.display: `number`

Default value: `15`

### envelopes.average.linestyle[​](#envelopesaveragelinestyle)
• envelopes.average.linestyle: `number`

Default value: `0`

### envelopes.average.linewidth[​](#envelopesaveragelinewidth)
• envelopes.average.linewidth: `number`

Default value: `1`

### envelopes.average.plottype[​](#envelopesaverageplottype)
• envelopes.average.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### envelopes.average.trackprice[​](#envelopesaveragetrackprice)
• envelopes.average.trackprice: `boolean`

Default value: `false`

### envelopes.average.transparency[​](#envelopesaveragetransparency)
• envelopes.average.transparency: `number`

Default value: `0`

### envelopes.length[​](#envelopeslength)
• envelopes.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### envelopes.lower percentage[​](#envelopeslower-percentage)
• envelopes.lower percentage: `number`

- Default value: `10`
- Input type: `float`
- Min: `0`

### envelopes.lower.color[​](#envelopeslowercolor)
• envelopes.lower.color: `string`

Default value: `#2196F3`

### envelopes.lower.display[​](#envelopeslowerdisplay)
• envelopes.lower.display: `number`

Default value: `15`

### envelopes.lower.linestyle[​](#envelopeslowerlinestyle)
• envelopes.lower.linestyle: `number`

Default value: `0`

### envelopes.lower.linewidth[​](#envelopeslowerlinewidth)
• envelopes.lower.linewidth: `number`

Default value: `1`

### envelopes.lower.plottype[​](#envelopeslowerplottype)
• envelopes.lower.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### envelopes.lower.trackprice[​](#envelopeslowertrackprice)
• envelopes.lower.trackprice: `boolean`

Default value: `false`

### envelopes.lower.transparency[​](#envelopeslowertransparency)
• envelopes.lower.transparency: `number`

Default value: `0`

### envelopes.method[​](#envelopesmethod)
• envelopes.method: `string`

- Default value: `Simple`
- Input type: `text`
- Options: `["Simple","Exponential","Weighted"]`

### envelopes.plots background.color[​](#envelopesplots-backgroundcolor)
• envelopes.plots background.color: `string`

Default value: `#2196F3`

### envelopes.plots background.transparency[​](#envelopesplots-backgroundtransparency)
• envelopes.plots background.transparency: `number`

Default value: `95`

### envelopes.plots background.visible[​](#envelopesplots-backgroundvisible)
• envelopes.plots background.visible: `boolean`

Default value: `true`

### envelopes.source[​](#envelopessource)
• envelopes.source: `string`

- Default value: `close`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### envelopes.upper percentage[​](#envelopesupper-percentage)
• envelopes.upper percentage: `number`

- Default value: `10`
- Input type: `float`
- Min: `0`

### envelopes.upper.color[​](#envelopesuppercolor)
• envelopes.upper.color: `string`

Default value: `#2196F3`

### envelopes.upper.display[​](#envelopesupperdisplay)
• envelopes.upper.display: `number`

Default value: `15`

### envelopes.upper.linestyle[​](#envelopesupperlinestyle)
• envelopes.upper.linestyle: `number`

Default value: `0`

### envelopes.upper.linewidth[​](#envelopesupperlinewidth)
• envelopes.upper.linewidth: `number`

Default value: `1`

### envelopes.upper.plottype[​](#envelopesupperplottype)
• envelopes.upper.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### envelopes.upper.trackprice[​](#envelopesuppertrackprice)
• envelopes.upper.trackprice: `boolean`

Default value: `false`

### envelopes.upper.transparency[​](#envelopesuppertransparency)
• envelopes.upper.transparency: `number`

Default value: `0`

### fisher transform.fisher.color[​](#fisher-transformfishercolor)
• fisher transform.fisher.color: `string`

Default value: `#2196F3`

### fisher transform.fisher.display[​](#fisher-transformfisherdisplay)
• fisher transform.fisher.display: `number`

Default value: `15`

### fisher transform.fisher.linestyle[​](#fisher-transformfisherlinestyle)
• fisher transform.fisher.linestyle: `number`

Default value: `0`

### fisher transform.fisher.linewidth[​](#fisher-transformfisherlinewidth)
• fisher transform.fisher.linewidth: `number`

Default value: `1`

### fisher transform.fisher.plottype[​](#fisher-transformfisherplottype)
• fisher transform.fisher.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### fisher transform.fisher.trackprice[​](#fisher-transformfishertrackprice)
• fisher transform.fisher.trackprice: `boolean`

Default value: `false`

### fisher transform.fisher.transparency[​](#fisher-transformfishertransparency)
• fisher transform.fisher.transparency: `number`

Default value: `0`

### fisher transform.length[​](#fisher-transformlength)
• fisher transform.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### fisher transform.level:band.color[​](#fisher-transformlevelcolor)
• fisher transform.level:band.color: `string`

Default value: `#E91E63`

### fisher transform.level:band.linestyle[​](#fisher-transformlevellinestyle)
• fisher transform.level:band.linestyle: `number`

Default value: `2`

### fisher transform.level:band.linewidth[​](#fisher-transformlevellinewidth)
• fisher transform.level:band.linewidth: `number`

Default value: `1`

### fisher transform.level:band.value[​](#fisher-transformlevelvalue)
• fisher transform.level:band.value: `number`

Default value: `-1.5`

### fisher transform.level:band.visible[​](#fisher-transformlevelvisible)
• fisher transform.level:band.visible: `boolean`

Default value: `true`

### fisher transform.trigger.color[​](#fisher-transformtriggercolor)
• fisher transform.trigger.color: `string`

Default value: `#FF6D00`

### fisher transform.trigger.display[​](#fisher-transformtriggerdisplay)
• fisher transform.trigger.display: `number`

Default value: `15`

### fisher transform.trigger.linestyle[​](#fisher-transformtriggerlinestyle)
• fisher transform.trigger.linestyle: `number`

Default value: `0`

### fisher transform.trigger.linewidth[​](#fisher-transformtriggerlinewidth)
• fisher transform.trigger.linewidth: `number`

Default value: `1`

### fisher transform.trigger.plottype[​](#fisher-transformtriggerplottype)
• fisher transform.trigger.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### fisher transform.trigger.trackprice[​](#fisher-transformtriggertrackprice)
• fisher transform.trigger.trackprice: `boolean`

Default value: `false`

### fisher transform.trigger.transparency[​](#fisher-transformtriggertransparency)
• fisher transform.trigger.transparency: `number`

Default value: `0`

### fixed range.developing poc.color[​](#fixed-rangedeveloping-poccolor)
• fixed range.developing poc.color: `string`

Default value: `undefined`

### fixed range.developing poc.display[​](#fixed-rangedeveloping-pocdisplay)
• fixed range.developing poc.display: `number`

Default value: `0`

### fixed range.developing poc.linestyle[​](#fixed-rangedeveloping-poclinestyle)
• fixed range.developing poc.linestyle: `number`

Default value: `0`

### fixed range.developing poc.linewidth[​](#fixed-rangedeveloping-poclinewidth)
• fixed range.developing poc.linewidth: `number`

Default value: `1`

### fixed range.developing poc.plottype[​](#fixed-rangedeveloping-pocplottype)
• fixed range.developing poc.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### fixed range.developing poc.trackprice[​](#fixed-rangedeveloping-poctrackprice)
• fixed range.developing poc.trackprice: `boolean`

Default value: `false`

### fixed range.developing poc.transparency[​](#fixed-rangedeveloping-poctransparency)
• fixed range.developing poc.transparency: `number`

Default value: `0`

### fixed range.developing va high.color[​](#fixed-rangedeveloping-va-highcolor)
• fixed range.developing va high.color: `string`

Default value: `undefined`

### fixed range.developing va high.display[​](#fixed-rangedeveloping-va-highdisplay)
• fixed range.developing va high.display: `number`

Default value: `0`

### fixed range.developing va high.linestyle[​](#fixed-rangedeveloping-va-highlinestyle)
• fixed range.developing va high.linestyle: `number`

Default value: `0`

### fixed range.developing va high.linewidth[​](#fixed-rangedeveloping-va-highlinewidth)
• fixed range.developing va high.linewidth: `number`

Default value: `1`

### fixed range.developing va high.plottype[​](#fixed-rangedeveloping-va-highplottype)
• fixed range.developing va high.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### fixed range.developing va high.trackprice[​](#fixed-rangedeveloping-va-hightrackprice)
• fixed range.developing va high.trackprice: `boolean`

Default value: `false`

### fixed range.developing va high.transparency[​](#fixed-rangedeveloping-va-hightransparency)
• fixed range.developing va high.transparency: `number`

Default value: `0`

### fixed range.developing va low.color[​](#fixed-rangedeveloping-va-lowcolor)
• fixed range.developing va low.color: `string`

Default value: `undefined`

### fixed range.developing va low.display[​](#fixed-rangedeveloping-va-lowdisplay)
• fixed range.developing va low.display: `number`

Default value: `0`

### fixed range.developing va low.linestyle[​](#fixed-rangedeveloping-va-lowlinestyle)
• fixed range.developing va low.linestyle: `number`

Default value: `0`

### fixed range.developing va low.linewidth[​](#fixed-rangedeveloping-va-lowlinewidth)
• fixed range.developing va low.linewidth: `number`

Default value: `1`

### fixed range.developing va low.plottype[​](#fixed-rangedeveloping-va-lowplottype)
• fixed range.developing va low.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### fixed range.developing va low.trackprice[​](#fixed-rangedeveloping-va-lowtrackprice)
• fixed range.developing va low.trackprice: `boolean`

Default value: `false`

### fixed range.developing va low.transparency[​](#fixed-rangedeveloping-va-lowtransparency)
• fixed range.developing va low.transparency: `number`

Default value: `0`

### fixed range.first bar time[​](#fixed-rangefirst-bar-time)
• fixed range.first bar time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `253370764800`
- Min: `-253370764800`

### fixed range.last bar time[​](#fixed-rangelast-bar-time)
• fixed range.last bar time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `253370764800`
- Min: `-253370764800`

### fixed range.row size[​](#fixed-rangerow-size)
• fixed range.row size: `number`

- Default value: `24`
- Input type: `integer`
- Max: `1000000`
- Min: `1`

### fixed range.rows layout[​](#fixed-rangerows-layout)
• fixed range.rows layout: `string`

- Default value: `Number Of Rows`
- Input type: `text`
- Options: `["Number Of Rows","Ticks Per Row"]`

### fixed range.subscriberealtime[​](#fixed-rangesubscriberealtime)
• fixed range.subscriberealtime: `boolean`

- Default value: `true`
- Input type: `bool`
- IsHidden: `true`

### fixed range.value area volume[​](#fixed-rangevalue-area-volume)
• fixed range.value area volume: `number`

- Default value: `70`
- Input type: `integer`
- Max: `100`
- Min: `0`

### fixed range.volume[​](#fixed-rangevolume)
• fixed range.volume: `string`

- Default value: `Up/Down`
- Input type: `text`
- Options: `["Up/Down","Total","Delta"]`

### guppy multiple moving average.investor ema 1 length[​](#guppy-multiple-moving-averageinvestor-ema-1-length)
• guppy multiple moving average.investor ema 1 length: `number`

- Default value: `30`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.investor ema 1.color[​](#guppy-multiple-moving-averageinvestor-ema-1color)
• guppy multiple moving average.investor ema 1.color: `string`

Default value: `#FF0000`

### guppy multiple moving average.investor ema 1.display[​](#guppy-multiple-moving-averageinvestor-ema-1display)
• guppy multiple moving average.investor ema 1.display: `number`

Default value: `15`

### guppy multiple moving average.investor ema 1.linestyle[​](#guppy-multiple-moving-averageinvestor-ema-1linestyle)
• guppy multiple moving average.investor ema 1.linestyle: `number`

Default value: `0`

### guppy multiple moving average.investor ema 1.linewidth[​](#guppy-multiple-moving-averageinvestor-ema-1linewidth)
• guppy multiple moving average.investor ema 1.linewidth: `number`

Default value: `1`

### guppy multiple moving average.investor ema 1.plottype[​](#guppy-multiple-moving-averageinvestor-ema-1plottype)
• guppy multiple moving average.investor ema 1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.investor ema 1.trackprice[​](#guppy-multiple-moving-averageinvestor-ema-1trackprice)
• guppy multiple moving average.investor ema 1.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.investor ema 1.transparency[​](#guppy-multiple-moving-averageinvestor-ema-1transparency)
• guppy multiple moving average.investor ema 1.transparency: `number`

Default value: `15`

### guppy multiple moving average.investor ema 2 length[​](#guppy-multiple-moving-averageinvestor-ema-2-length)
• guppy multiple moving average.investor ema 2 length: `number`

- Default value: `35`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.investor ema 2.color[​](#guppy-multiple-moving-averageinvestor-ema-2color)
• guppy multiple moving average.investor ema 2.color: `string`

Default value: `#FF0000`

### guppy multiple moving average.investor ema 2.display[​](#guppy-multiple-moving-averageinvestor-ema-2display)
• guppy multiple moving average.investor ema 2.display: `number`

Default value: `15`

### guppy multiple moving average.investor ema 2.linestyle[​](#guppy-multiple-moving-averageinvestor-ema-2linestyle)
• guppy multiple moving average.investor ema 2.linestyle: `number`

Default value: `0`

### guppy multiple moving average.investor ema 2.linewidth[​](#guppy-multiple-moving-averageinvestor-ema-2linewidth)
• guppy multiple moving average.investor ema 2.linewidth: `number`

Default value: `1`

### guppy multiple moving average.investor ema 2.plottype[​](#guppy-multiple-moving-averageinvestor-ema-2plottype)
• guppy multiple moving average.investor ema 2.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.investor ema 2.trackprice[​](#guppy-multiple-moving-averageinvestor-ema-2trackprice)
• guppy multiple moving average.investor ema 2.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.investor ema 2.transparency[​](#guppy-multiple-moving-averageinvestor-ema-2transparency)
• guppy multiple moving average.investor ema 2.transparency: `number`

Default value: `12`

### guppy multiple moving average.investor ema 3 length[​](#guppy-multiple-moving-averageinvestor-ema-3-length)
• guppy multiple moving average.investor ema 3 length: `number`

- Default value: `40`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.investor ema 3.color[​](#guppy-multiple-moving-averageinvestor-ema-3color)
• guppy multiple moving average.investor ema 3.color: `string`

Default value: `#FF0000`

### guppy multiple moving average.investor ema 3.display[​](#guppy-multiple-moving-averageinvestor-ema-3display)
• guppy multiple moving average.investor ema 3.display: `number`

Default value: `15`

### guppy multiple moving average.investor ema 3.linestyle[​](#guppy-multiple-moving-averageinvestor-ema-3linestyle)
• guppy multiple moving average.investor ema 3.linestyle: `number`

Default value: `0`

### guppy multiple moving average.investor ema 3.linewidth[​](#guppy-multiple-moving-averageinvestor-ema-3linewidth)
• guppy multiple moving average.investor ema 3.linewidth: `number`

Default value: `1`

### guppy multiple moving average.investor ema 3.plottype[​](#guppy-multiple-moving-averageinvestor-ema-3plottype)
• guppy multiple moving average.investor ema 3.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.investor ema 3.trackprice[​](#guppy-multiple-moving-averageinvestor-ema-3trackprice)
• guppy multiple moving average.investor ema 3.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.investor ema 3.transparency[​](#guppy-multiple-moving-averageinvestor-ema-3transparency)
• guppy multiple moving average.investor ema 3.transparency: `number`

Default value: `9`

### guppy multiple moving average.investor ema 4 length[​](#guppy-multiple-moving-averageinvestor-ema-4-length)
• guppy multiple moving average.investor ema 4 length: `number`

- Default value: `45`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.investor ema 4.color[​](#guppy-multiple-moving-averageinvestor-ema-4color)
• guppy multiple moving average.investor ema 4.color: `string`

Default value: `#FF0000`

### guppy multiple moving average.investor ema 4.display[​](#guppy-multiple-moving-averageinvestor-ema-4display)
• guppy multiple moving average.investor ema 4.display: `number`

Default value: `15`

### guppy multiple moving average.investor ema 4.linestyle[​](#guppy-multiple-moving-averageinvestor-ema-4linestyle)
• guppy multiple moving average.investor ema 4.linestyle: `number`

Default value: `0`

### guppy multiple moving average.investor ema 4.linewidth[​](#guppy-multiple-moving-averageinvestor-ema-4linewidth)
• guppy multiple moving average.investor ema 4.linewidth: `number`

Default value: `1`

### guppy multiple moving average.investor ema 4.plottype[​](#guppy-multiple-moving-averageinvestor-ema-4plottype)
• guppy multiple moving average.investor ema 4.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.investor ema 4.trackprice[​](#guppy-multiple-moving-averageinvestor-ema-4trackprice)
• guppy multiple moving average.investor ema 4.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.investor ema 4.transparency[​](#guppy-multiple-moving-averageinvestor-ema-4transparency)
• guppy multiple moving average.investor ema 4.transparency: `number`

Default value: `6`

### guppy multiple moving average.investor ema 5 length[​](#guppy-multiple-moving-averageinvestor-ema-5-length)
• guppy multiple moving average.investor ema 5 length: `number`

- Default value: `50`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.investor ema 5.color[​](#guppy-multiple-moving-averageinvestor-ema-5color)
• guppy multiple moving average.investor ema 5.color: `string`

Default value: `#FF0000`

### guppy multiple moving average.investor ema 5.display[​](#guppy-multiple-moving-averageinvestor-ema-5display)
• guppy multiple moving average.investor ema 5.display: `number`

Default value: `15`

### guppy multiple moving average.investor ema 5.linestyle[​](#guppy-multiple-moving-averageinvestor-ema-5linestyle)
• guppy multiple moving average.investor ema 5.linestyle: `number`

Default value: `0`

### guppy multiple moving average.investor ema 5.linewidth[​](#guppy-multiple-moving-averageinvestor-ema-5linewidth)
• guppy multiple moving average.investor ema 5.linewidth: `number`

Default value: `1`

### guppy multiple moving average.investor ema 5.plottype[​](#guppy-multiple-moving-averageinvestor-ema-5plottype)
• guppy multiple moving average.investor ema 5.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.investor ema 5.trackprice[​](#guppy-multiple-moving-averageinvestor-ema-5trackprice)
• guppy multiple moving average.investor ema 5.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.investor ema 5.transparency[​](#guppy-multiple-moving-averageinvestor-ema-5transparency)
• guppy multiple moving average.investor ema 5.transparency: `number`

Default value: `3`

### guppy multiple moving average.investor ema 6 length[​](#guppy-multiple-moving-averageinvestor-ema-6-length)
• guppy multiple moving average.investor ema 6 length: `number`

- Default value: `60`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.investor ema 6.color[​](#guppy-multiple-moving-averageinvestor-ema-6color)
• guppy multiple moving average.investor ema 6.color: `string`

Default value: `#FF0000`

### guppy multiple moving average.investor ema 6.display[​](#guppy-multiple-moving-averageinvestor-ema-6display)
• guppy multiple moving average.investor ema 6.display: `number`

Default value: `15`

### guppy multiple moving average.investor ema 6.linestyle[​](#guppy-multiple-moving-averageinvestor-ema-6linestyle)
• guppy multiple moving average.investor ema 6.linestyle: `number`

Default value: `0`

### guppy multiple moving average.investor ema 6.linewidth[​](#guppy-multiple-moving-averageinvestor-ema-6linewidth)
• guppy multiple moving average.investor ema 6.linewidth: `number`

Default value: `1`

### guppy multiple moving average.investor ema 6.plottype[​](#guppy-multiple-moving-averageinvestor-ema-6plottype)
• guppy multiple moving average.investor ema 6.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.investor ema 6.trackprice[​](#guppy-multiple-moving-averageinvestor-ema-6trackprice)
• guppy multiple moving average.investor ema 6.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.investor ema 6.transparency[​](#guppy-multiple-moving-averageinvestor-ema-6transparency)
• guppy multiple moving average.investor ema 6.transparency: `number`

Default value: `0`

### guppy multiple moving average.trader ema 1 length[​](#guppy-multiple-moving-averagetrader-ema-1-length)
• guppy multiple moving average.trader ema 1 length: `number`

- Default value: `3`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.trader ema 1.color[​](#guppy-multiple-moving-averagetrader-ema-1color)
• guppy multiple moving average.trader ema 1.color: `string`

Default value: `#00FFFF`

### guppy multiple moving average.trader ema 1.display[​](#guppy-multiple-moving-averagetrader-ema-1display)
• guppy multiple moving average.trader ema 1.display: `number`

Default value: `15`

### guppy multiple moving average.trader ema 1.linestyle[​](#guppy-multiple-moving-averagetrader-ema-1linestyle)
• guppy multiple moving average.trader ema 1.linestyle: `number`

Default value: `0`

### guppy multiple moving average.trader ema 1.linewidth[​](#guppy-multiple-moving-averagetrader-ema-1linewidth)
• guppy multiple moving average.trader ema 1.linewidth: `number`

Default value: `1`

### guppy multiple moving average.trader ema 1.plottype[​](#guppy-multiple-moving-averagetrader-ema-1plottype)
• guppy multiple moving average.trader ema 1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.trader ema 1.trackprice[​](#guppy-multiple-moving-averagetrader-ema-1trackprice)
• guppy multiple moving average.trader ema 1.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.trader ema 1.transparency[​](#guppy-multiple-moving-averagetrader-ema-1transparency)
• guppy multiple moving average.trader ema 1.transparency: `number`

Default value: `15`

### guppy multiple moving average.trader ema 2 length[​](#guppy-multiple-moving-averagetrader-ema-2-length)
• guppy multiple moving average.trader ema 2 length: `number`

- Default value: `5`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.trader ema 2.color[​](#guppy-multiple-moving-averagetrader-ema-2color)
• guppy multiple moving average.trader ema 2.color: `string`

Default value: `#00FFFF`

### guppy multiple moving average.trader ema 2.display[​](#guppy-multiple-moving-averagetrader-ema-2display)
• guppy multiple moving average.trader ema 2.display: `number`

Default value: `15`

### guppy multiple moving average.trader ema 2.linestyle[​](#guppy-multiple-moving-averagetrader-ema-2linestyle)
• guppy multiple moving average.trader ema 2.linestyle: `number`

Default value: `0`

### guppy multiple moving average.trader ema 2.linewidth[​](#guppy-multiple-moving-averagetrader-ema-2linewidth)
• guppy multiple moving average.trader ema 2.linewidth: `number`

Default value: `1`

### guppy multiple moving average.trader ema 2.plottype[​](#guppy-multiple-moving-averagetrader-ema-2plottype)
• guppy multiple moving average.trader ema 2.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.trader ema 2.trackprice[​](#guppy-multiple-moving-averagetrader-ema-2trackprice)
• guppy multiple moving average.trader ema 2.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.trader ema 2.transparency[​](#guppy-multiple-moving-averagetrader-ema-2transparency)
• guppy multiple moving average.trader ema 2.transparency: `number`

Default value: `12`

### guppy multiple moving average.trader ema 3 length[​](#guppy-multiple-moving-averagetrader-ema-3-length)
• guppy multiple moving average.trader ema 3 length: `number`

- Default value: `8`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.trader ema 3.color[​](#guppy-multiple-moving-averagetrader-ema-3color)
• guppy multiple moving average.trader ema 3.color: `string`

Default value: `#00FFFF`

### guppy multiple moving average.trader ema 3.display[​](#guppy-multiple-moving-averagetrader-ema-3display)
• guppy multiple moving average.trader ema 3.display: `number`

Default value: `15`

### guppy multiple moving average.trader ema 3.linestyle[​](#guppy-multiple-moving-averagetrader-ema-3linestyle)
• guppy multiple moving average.trader ema 3.linestyle: `number`

Default value: `0`

### guppy multiple moving average.trader ema 3.linewidth[​](#guppy-multiple-moving-averagetrader-ema-3linewidth)
• guppy multiple moving average.trader ema 3.linewidth: `number`

Default value: `1`

### guppy multiple moving average.trader ema 3.plottype[​](#guppy-multiple-moving-averagetrader-ema-3plottype)
• guppy multiple moving average.trader ema 3.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.trader ema 3.trackprice[​](#guppy-multiple-moving-averagetrader-ema-3trackprice)
• guppy multiple moving average.trader ema 3.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.trader ema 3.transparency[​](#guppy-multiple-moving-averagetrader-ema-3transparency)
• guppy multiple moving average.trader ema 3.transparency: `number`

Default value: `9`

### guppy multiple moving average.trader ema 4 length[​](#guppy-multiple-moving-averagetrader-ema-4-length)
• guppy multiple moving average.trader ema 4 length: `number`

- Default value: `10`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.trader ema 4.color[​](#guppy-multiple-moving-averagetrader-ema-4color)
• guppy multiple moving average.trader ema 4.color: `string`

Default value: `#00FFFF`

### guppy multiple moving average.trader ema 4.display[​](#guppy-multiple-moving-averagetrader-ema-4display)
• guppy multiple moving average.trader ema 4.display: `number`

Default value: `15`

### guppy multiple moving average.trader ema 4.linestyle[​](#guppy-multiple-moving-averagetrader-ema-4linestyle)
• guppy multiple moving average.trader ema 4.linestyle: `number`

Default value: `0`

### guppy multiple moving average.trader ema 4.linewidth[​](#guppy-multiple-moving-averagetrader-ema-4linewidth)
• guppy multiple moving average.trader ema 4.linewidth: `number`

Default value: `1`

### guppy multiple moving average.trader ema 4.plottype[​](#guppy-multiple-moving-averagetrader-ema-4plottype)
• guppy multiple moving average.trader ema 4.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.trader ema 4.trackprice[​](#guppy-multiple-moving-averagetrader-ema-4trackprice)
• guppy multiple moving average.trader ema 4.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.trader ema 4.transparency[​](#guppy-multiple-moving-averagetrader-ema-4transparency)
• guppy multiple moving average.trader ema 4.transparency: `number`

Default value: `6`

### guppy multiple moving average.trader ema 5 length[​](#guppy-multiple-moving-averagetrader-ema-5-length)
• guppy multiple moving average.trader ema 5 length: `number`

- Default value: `12`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.trader ema 5.color[​](#guppy-multiple-moving-averagetrader-ema-5color)
• guppy multiple moving average.trader ema 5.color: `string`

Default value: `#00FFFF`

### guppy multiple moving average.trader ema 5.display[​](#guppy-multiple-moving-averagetrader-ema-5display)
• guppy multiple moving average.trader ema 5.display: `number`

Default value: `15`

### guppy multiple moving average.trader ema 5.linestyle[​](#guppy-multiple-moving-averagetrader-ema-5linestyle)
• guppy multiple moving average.trader ema 5.linestyle: `number`

Default value: `0`

### guppy multiple moving average.trader ema 5.linewidth[​](#guppy-multiple-moving-averagetrader-ema-5linewidth)
• guppy multiple moving average.trader ema 5.linewidth: `number`

Default value: `1`

### guppy multiple moving average.trader ema 5.plottype[​](#guppy-multiple-moving-averagetrader-ema-5plottype)
• guppy multiple moving average.trader ema 5.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.trader ema 5.trackprice[​](#guppy-multiple-moving-averagetrader-ema-5trackprice)
• guppy multiple moving average.trader ema 5.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.trader ema 5.transparency[​](#guppy-multiple-moving-averagetrader-ema-5transparency)
• guppy multiple moving average.trader ema 5.transparency: `number`

Default value: `3`

### guppy multiple moving average.trader ema 6 length[​](#guppy-multiple-moving-averagetrader-ema-6-length)
• guppy multiple moving average.trader ema 6 length: `number`

- Default value: `15`
- Input type: `integer`
- Max: `1000`
- Min: `1`

### guppy multiple moving average.trader ema 6.color[​](#guppy-multiple-moving-averagetrader-ema-6color)
• guppy multiple moving average.trader ema 6.color: `string`

Default value: `#00FFFF`

### guppy multiple moving average.trader ema 6.display[​](#guppy-multiple-moving-averagetrader-ema-6display)
• guppy multiple moving average.trader ema 6.display: `number`

Default value: `15`

### guppy multiple moving average.trader ema 6.linestyle[​](#guppy-multiple-moving-averagetrader-ema-6linestyle)
• guppy multiple moving average.trader ema 6.linestyle: `number`

Default value: `0`

### guppy multiple moving average.trader ema 6.linewidth[​](#guppy-multiple-moving-averagetrader-ema-6linewidth)
• guppy multiple moving average.trader ema 6.linewidth: `number`

Default value: `1`

### guppy multiple moving average.trader ema 6.plottype[​](#guppy-multiple-moving-averagetrader-ema-6plottype)
• guppy multiple moving average.trader ema 6.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### guppy multiple moving average.trader ema 6.trackprice[​](#guppy-multiple-moving-averagetrader-ema-6trackprice)
• guppy multiple moving average.trader ema 6.trackprice: `boolean`

Default value: `false`

### guppy multiple moving average.trader ema 6.transparency[​](#guppy-multiple-moving-averagetrader-ema-6transparency)
• guppy multiple moving average.trader ema 6.transparency: `number`

Default value: `0`

### hiLoStyle.borderColor[​](#hilostylebordercolor)
• hiLoStyle.borderColor: `string`

### hiLoStyle.color[​](#hilostylecolor)
• hiLoStyle.color: `string`

### hiLoStyle.drawBody[​](#hilostyledrawbody)
• hiLoStyle.drawBody: `boolean`

### hiLoStyle.labelColor[​](#hilostylelabelcolor)
• hiLoStyle.labelColor: `string`

### hiLoStyle.showBorders[​](#hilostyleshowborders)
• hiLoStyle.showBorders: `boolean`

### hiLoStyle.showLabels[​](#hilostyleshowlabels)
• hiLoStyle.showLabels: `boolean`

### historical volatility.length[​](#historical-volatilitylength)
• historical volatility.length: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### historical volatility.plot.color[​](#historical-volatilityplotcolor)
• historical volatility.plot.color: `string`

Default value: `#2196F3`

### historical volatility.plot.display[​](#historical-volatilityplotdisplay)
• historical volatility.plot.display: `number`

Default value: `15`

### historical volatility.plot.linestyle[​](#historical-volatilityplotlinestyle)
• historical volatility.plot.linestyle: `number`

Default value: `0`

### historical volatility.plot.linewidth[​](#historical-volatilityplotlinewidth)
• historical volatility.plot.linewidth: `number`

Default value: `1`

### historical volatility.plot.plottype[​](#historical-volatilityplotplottype)
• historical volatility.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### historical volatility.plot.trackprice[​](#historical-volatilityplottrackprice)
• historical volatility.plot.trackprice: `boolean`

Default value: `false`

### historical volatility.plot.transparency[​](#historical-volatilityplottransparency)
• historical volatility.plot.transparency: `number`

Default value: `0`

### hlcBarsStyle.color[​](#hlcbarsstylecolor)
• hlcBarsStyle.color: `string`

### hlcBarsStyle.thinBars[​](#hlcbarsstylethinbars)
• hlcBarsStyle.thinBars: `boolean`

### hull moving average.length[​](#hull-moving-averagelength)
• hull moving average.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### hull moving average.plot.color[​](#hull-moving-averageplotcolor)
• hull moving average.plot.color: `string`

Default value: `#2196F3`

### hull moving average.plot.display[​](#hull-moving-averageplotdisplay)
• hull moving average.plot.display: `number`

Default value: `15`

### hull moving average.plot.linestyle[​](#hull-moving-averageplotlinestyle)
• hull moving average.plot.linestyle: `number`

Default value: `0`

### hull moving average.plot.linewidth[​](#hull-moving-averageplotlinewidth)
• hull moving average.plot.linewidth: `number`

Default value: `1`

### hull moving average.plot.plottype[​](#hull-moving-averageplotplottype)
• hull moving average.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### hull moving average.plot.trackprice[​](#hull-moving-averageplottrackprice)
• hull moving average.plot.trackprice: `boolean`

Default value: `false`

### hull moving average.plot.transparency[​](#hull-moving-averageplottransparency)
• hull moving average.plot.transparency: `number`

Default value: `0`

### ichimoku cloud.another symbol[​](#ichimoku-cloudanother-symbol)
• ichimoku cloud.another symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Optional: `true`
- IsHidden: `false`

### ichimoku cloud.base line periods[​](#ichimoku-cloudbase-line-periods)
• ichimoku cloud.base line periods: `number`

- Default value: `26`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### ichimoku cloud.base line.color[​](#ichimoku-cloudbase-linecolor)
• ichimoku cloud.base line.color: `string`

Default value: `#801922`

### ichimoku cloud.base line.display[​](#ichimoku-cloudbase-linedisplay)
• ichimoku cloud.base line.display: `number`

Default value: `15`

### ichimoku cloud.base line.linestyle[​](#ichimoku-cloudbase-linelinestyle)
• ichimoku cloud.base line.linestyle: `number`

Default value: `0`

### ichimoku cloud.base line.linewidth[​](#ichimoku-cloudbase-linelinewidth)
• ichimoku cloud.base line.linewidth: `number`

Default value: `1`

### ichimoku cloud.base line.plottype[​](#ichimoku-cloudbase-lineplottype)
• ichimoku cloud.base line.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ichimoku cloud.base line.trackprice[​](#ichimoku-cloudbase-linetrackprice)
• ichimoku cloud.base line.trackprice: `boolean`

Default value: `false`

### ichimoku cloud.base line.transparency[​](#ichimoku-cloudbase-linetransparency)
• ichimoku cloud.base line.transparency: `number`

Default value: `0`

### ichimoku cloud.conversion line periods[​](#ichimoku-cloudconversion-line-periods)
• ichimoku cloud.conversion line periods: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### ichimoku cloud.conversion line.color[​](#ichimoku-cloudconversion-linecolor)
• ichimoku cloud.conversion line.color: `string`

Default value: `#2196F3`

### ichimoku cloud.conversion line.display[​](#ichimoku-cloudconversion-linedisplay)
• ichimoku cloud.conversion line.display: `number`

Default value: `15`

### ichimoku cloud.conversion line.linestyle[​](#ichimoku-cloudconversion-linelinestyle)
• ichimoku cloud.conversion line.linestyle: `number`

Default value: `0`

### ichimoku cloud.conversion line.linewidth[​](#ichimoku-cloudconversion-linelinewidth)
• ichimoku cloud.conversion line.linewidth: `number`

Default value: `1`

### ichimoku cloud.conversion line.plottype[​](#ichimoku-cloudconversion-lineplottype)
• ichimoku cloud.conversion line.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ichimoku cloud.conversion line.trackprice[​](#ichimoku-cloudconversion-linetrackprice)
• ichimoku cloud.conversion line.trackprice: `boolean`

Default value: `false`

### ichimoku cloud.conversion line.transparency[​](#ichimoku-cloudconversion-linetransparency)
• ichimoku cloud.conversion line.transparency: `number`

Default value: `0`

### ichimoku cloud.lagging span periods[​](#ichimoku-cloudlagging-span-periods)
• ichimoku cloud.lagging span periods: `number`

- Default value: `26`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### ichimoku cloud.lagging span.color[​](#ichimoku-cloudlagging-spancolor)
• ichimoku cloud.lagging span.color: `string`

Default value: `#43A047`

### ichimoku cloud.lagging span.display[​](#ichimoku-cloudlagging-spandisplay)
• ichimoku cloud.lagging span.display: `number`

Default value: `15`

### ichimoku cloud.lagging span.linestyle[​](#ichimoku-cloudlagging-spanlinestyle)
• ichimoku cloud.lagging span.linestyle: `number`

Default value: `0`

### ichimoku cloud.lagging span.linewidth[​](#ichimoku-cloudlagging-spanlinewidth)
• ichimoku cloud.lagging span.linewidth: `number`

Default value: `1`

### ichimoku cloud.lagging span.plottype[​](#ichimoku-cloudlagging-spanplottype)
• ichimoku cloud.lagging span.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ichimoku cloud.lagging span.trackprice[​](#ichimoku-cloudlagging-spantrackprice)
• ichimoku cloud.lagging span.trackprice: `boolean`

Default value: `false`

### ichimoku cloud.lagging span.transparency[​](#ichimoku-cloudlagging-spantransparency)
• ichimoku cloud.lagging span.transparency: `number`

Default value: `0`

### ichimoku cloud.leading shift periods[​](#ichimoku-cloudleading-shift-periods)
• ichimoku cloud.leading shift periods: `number`

- Default value: `26`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### ichimoku cloud.leading span a.color[​](#ichimoku-cloudleading-span-acolor)
• ichimoku cloud.leading span a.color: `string`

Default value: `#A5D6A7`

### ichimoku cloud.leading span a.display[​](#ichimoku-cloudleading-span-adisplay)
• ichimoku cloud.leading span a.display: `number`

Default value: `15`

### ichimoku cloud.leading span a.linestyle[​](#ichimoku-cloudleading-span-alinestyle)
• ichimoku cloud.leading span a.linestyle: `number`

Default value: `0`

### ichimoku cloud.leading span a.linewidth[​](#ichimoku-cloudleading-span-alinewidth)
• ichimoku cloud.leading span a.linewidth: `number`

Default value: `1`

### ichimoku cloud.leading span a.plottype[​](#ichimoku-cloudleading-span-aplottype)
• ichimoku cloud.leading span a.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ichimoku cloud.leading span a.trackprice[​](#ichimoku-cloudleading-span-atrackprice)
• ichimoku cloud.leading span a.trackprice: `boolean`

Default value: `false`

### ichimoku cloud.leading span a.transparency[​](#ichimoku-cloudleading-span-atransparency)
• ichimoku cloud.leading span a.transparency: `number`

Default value: `0`

### ichimoku cloud.leading span b.color[​](#ichimoku-cloudleading-span-bcolor)
• ichimoku cloud.leading span b.color: `string`

Default value: `#FAA1A4`

### ichimoku cloud.leading span b.display[​](#ichimoku-cloudleading-span-bdisplay)
• ichimoku cloud.leading span b.display: `number`

Default value: `15`

### ichimoku cloud.leading span b.linestyle[​](#ichimoku-cloudleading-span-blinestyle)
• ichimoku cloud.leading span b.linestyle: `number`

Default value: `0`

### ichimoku cloud.leading span b.linewidth[​](#ichimoku-cloudleading-span-blinewidth)
• ichimoku cloud.leading span b.linewidth: `number`

Default value: `1`

### ichimoku cloud.leading span b.plottype[​](#ichimoku-cloudleading-span-bplottype)
• ichimoku cloud.leading span b.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ichimoku cloud.leading span b.trackprice[​](#ichimoku-cloudleading-span-btrackprice)
• ichimoku cloud.leading span b.trackprice: `boolean`

Default value: `false`

### ichimoku cloud.leading span b.transparency[​](#ichimoku-cloudleading-span-btransparency)
• ichimoku cloud.leading span b.transparency: `number`

Default value: `0`

### ichimoku cloud.leading span periods[​](#ichimoku-cloudleading-span-periods)
• ichimoku cloud.leading span periods: `number`

- Default value: `52`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### ichimoku cloud.plots background.color[​](#ichimoku-cloudplots-backgroundcolor)
• ichimoku cloud.plots background.color: `string`

Default value: `#000080`

### ichimoku cloud.plots background.transparency[​](#ichimoku-cloudplots-backgroundtransparency)
• ichimoku cloud.plots background.transparency: `number`

Default value: `90`

### ichimoku cloud.plots background.visible[​](#ichimoku-cloudplots-backgroundvisible)
• ichimoku cloud.plots background.visible: `boolean`

Default value: `true`

### keltner channels.length[​](#keltner-channelslength)
• keltner channels.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### keltner channels.lower.color[​](#keltner-channelslowercolor)
• keltner channels.lower.color: `string`

Default value: `#2196F3`

### keltner channels.lower.display[​](#keltner-channelslowerdisplay)
• keltner channels.lower.display: `number`

Default value: `15`

### keltner channels.lower.linestyle[​](#keltner-channelslowerlinestyle)
• keltner channels.lower.linestyle: `number`

Default value: `0`

### keltner channels.lower.linewidth[​](#keltner-channelslowerlinewidth)
• keltner channels.lower.linewidth: `number`

Default value: `1`

### keltner channels.lower.plottype[​](#keltner-channelslowerplottype)
• keltner channels.lower.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### keltner channels.lower.trackprice[​](#keltner-channelslowertrackprice)
• keltner channels.lower.trackprice: `boolean`

Default value: `false`

### keltner channels.lower.transparency[​](#keltner-channelslowertransparency)
• keltner channels.lower.transparency: `number`

Default value: `0`

### keltner channels.middle.color[​](#keltner-channelsmiddlecolor)
• keltner channels.middle.color: `string`

Default value: `#2196F3`

### keltner channels.middle.display[​](#keltner-channelsmiddledisplay)
• keltner channels.middle.display: `number`

Default value: `15`

### keltner channels.middle.linestyle[​](#keltner-channelsmiddlelinestyle)
• keltner channels.middle.linestyle: `number`

Default value: `0`

### keltner channels.middle.linewidth[​](#keltner-channelsmiddlelinewidth)
• keltner channels.middle.linewidth: `number`

Default value: `1`

### keltner channels.middle.plottype[​](#keltner-channelsmiddleplottype)
• keltner channels.middle.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### keltner channels.middle.trackprice[​](#keltner-channelsmiddletrackprice)
• keltner channels.middle.trackprice: `boolean`

Default value: `false`

### keltner channels.middle.transparency[​](#keltner-channelsmiddletransparency)
• keltner channels.middle.transparency: `number`

Default value: `0`

### keltner channels.mult[​](#keltner-channelsmult)
• keltner channels.mult: `number`

- Default value: `1`
- Input type: `float`
- Min: `-1000000000000`
- Max: `1000000000000`

### keltner channels.plots background.color[​](#keltner-channelsplots-backgroundcolor)
• keltner channels.plots background.color: `string`

Default value: `#2196F3`

### keltner channels.plots background.transparency[​](#keltner-channelsplots-backgroundtransparency)
• keltner channels.plots background.transparency: `number`

Default value: `95`

### keltner channels.plots background.visible[​](#keltner-channelsplots-backgroundvisible)
• keltner channels.plots background.visible: `boolean`

Default value: `true`

### keltner channels.upper.color[​](#keltner-channelsuppercolor)
• keltner channels.upper.color: `string`

Default value: `#2196F3`

### keltner channels.upper.display[​](#keltner-channelsupperdisplay)
• keltner channels.upper.display: `number`

Default value: `15`

### keltner channels.upper.linestyle[​](#keltner-channelsupperlinestyle)
• keltner channels.upper.linestyle: `number`

Default value: `0`

### keltner channels.upper.linewidth[​](#keltner-channelsupperlinewidth)
• keltner channels.upper.linewidth: `number`

Default value: `1`

### keltner channels.upper.plottype[​](#keltner-channelsupperplottype)
• keltner channels.upper.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### keltner channels.upper.trackprice[​](#keltner-channelsuppertrackprice)
• keltner channels.upper.trackprice: `boolean`

Default value: `false`

### keltner channels.upper.transparency[​](#keltner-channelsuppertransparency)
• keltner channels.upper.transparency: `number`

Default value: `0`

### keltner channels.usetruerange[​](#keltner-channelsusetruerange)
• keltner channels.usetruerange: `boolean`

- Default value: `true`
- Input type: `bool`

### klinger oscillator.plot.color[​](#klinger-oscillatorplotcolor)
• klinger oscillator.plot.color: `string`

Default value: `#2196F3`

### klinger oscillator.plot.display[​](#klinger-oscillatorplotdisplay)
• klinger oscillator.plot.display: `number`

Default value: `15`

### klinger oscillator.plot.linestyle[​](#klinger-oscillatorplotlinestyle)
• klinger oscillator.plot.linestyle: `number`

Default value: `0`

### klinger oscillator.plot.linewidth[​](#klinger-oscillatorplotlinewidth)
• klinger oscillator.plot.linewidth: `number`

Default value: `1`

### klinger oscillator.plot.plottype[​](#klinger-oscillatorplotplottype)
• klinger oscillator.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### klinger oscillator.plot.trackprice[​](#klinger-oscillatorplottrackprice)
• klinger oscillator.plot.trackprice: `boolean`

Default value: `false`

### klinger oscillator.plot.transparency[​](#klinger-oscillatorplottransparency)
• klinger oscillator.plot.transparency: `number`

Default value: `0`

### klinger oscillator.signal.color[​](#klinger-oscillatorsignalcolor)
• klinger oscillator.signal.color: `string`

Default value: `#43A047`

### klinger oscillator.signal.display[​](#klinger-oscillatorsignaldisplay)
• klinger oscillator.signal.display: `number`

Default value: `15`

### klinger oscillator.signal.linestyle[​](#klinger-oscillatorsignallinestyle)
• klinger oscillator.signal.linestyle: `number`

Default value: `0`

### klinger oscillator.signal.linewidth[​](#klinger-oscillatorsignallinewidth)
• klinger oscillator.signal.linewidth: `number`

Default value: `1`

### klinger oscillator.signal.plottype[​](#klinger-oscillatorsignalplottype)
• klinger oscillator.signal.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### klinger oscillator.signal.trackprice[​](#klinger-oscillatorsignaltrackprice)
• klinger oscillator.signal.trackprice: `boolean`

Default value: `false`

### klinger oscillator.signal.transparency[​](#klinger-oscillatorsignaltransparency)
• klinger oscillator.signal.transparency: `number`

Default value: `0`

### know sure thing.kst.color[​](#know-sure-thingkstcolor)
• know sure thing.kst.color: `string`

Default value: `#089981`

### know sure thing.kst.display[​](#know-sure-thingkstdisplay)
• know sure thing.kst.display: `number`

Default value: `15`

### know sure thing.kst.linestyle[​](#know-sure-thingkstlinestyle)
• know sure thing.kst.linestyle: `number`

Default value: `0`

### know sure thing.kst.linewidth[​](#know-sure-thingkstlinewidth)
• know sure thing.kst.linewidth: `number`

Default value: `1`

### know sure thing.kst.plottype[​](#know-sure-thingkstplottype)
• know sure thing.kst.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### know sure thing.kst.trackprice[​](#know-sure-thingksttrackprice)
• know sure thing.kst.trackprice: `boolean`

Default value: `false`

### know sure thing.kst.transparency[​](#know-sure-thingksttransparency)
• know sure thing.kst.transparency: `number`

Default value: `0`

### know sure thing.roclen1[​](#know-sure-thingroclen1)
• know sure thing.roclen1: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.roclen2[​](#know-sure-thingroclen2)
• know sure thing.roclen2: `number`

- Default value: `15`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.roclen3[​](#know-sure-thingroclen3)
• know sure thing.roclen3: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.roclen4[​](#know-sure-thingroclen4)
• know sure thing.roclen4: `number`

- Default value: `30`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.siglen[​](#know-sure-thingsiglen)
• know sure thing.siglen: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.signal.color[​](#know-sure-thingsignalcolor)
• know sure thing.signal.color: `string`

Default value: `#F23645`

### know sure thing.signal.display[​](#know-sure-thingsignaldisplay)
• know sure thing.signal.display: `number`

Default value: `15`

### know sure thing.signal.linestyle[​](#know-sure-thingsignallinestyle)
• know sure thing.signal.linestyle: `number`

Default value: `0`

### know sure thing.signal.linewidth[​](#know-sure-thingsignallinewidth)
• know sure thing.signal.linewidth: `number`

Default value: `1`

### know sure thing.signal.plottype[​](#know-sure-thingsignalplottype)
• know sure thing.signal.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### know sure thing.signal.trackprice[​](#know-sure-thingsignaltrackprice)
• know sure thing.signal.trackprice: `boolean`

Default value: `false`

### know sure thing.signal.transparency[​](#know-sure-thingsignaltransparency)
• know sure thing.signal.transparency: `number`

Default value: `0`

### know sure thing.smalen1[​](#know-sure-thingsmalen1)
• know sure thing.smalen1: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.smalen2[​](#know-sure-thingsmalen2)
• know sure thing.smalen2: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.smalen3[​](#know-sure-thingsmalen3)
• know sure thing.smalen3: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.smalen4[​](#know-sure-thingsmalen4)
• know sure thing.smalen4: `number`

- Default value: `15`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### know sure thing.zero.color[​](#know-sure-thingzerocolor)
• know sure thing.zero.color: `string`

Default value: `#787B86`

### know sure thing.zero.linestyle[​](#know-sure-thingzerolinestyle)
• know sure thing.zero.linestyle: `number`

Default value: `2`

### know sure thing.zero.linewidth[​](#know-sure-thingzerolinewidth)
• know sure thing.zero.linewidth: `number`

Default value: `1`

### know sure thing.zero.value[​](#know-sure-thingzerovalue)
• know sure thing.zero.value: `number`

Default value: `0`

### know sure thing.zero.visible[​](#know-sure-thingzerovisible)
• know sure thing.zero.visible: `boolean`

Default value: `true`

### least squares moving average.length[​](#least-squares-moving-averagelength)
• least squares moving average.length: `number`

- Default value: `25`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### least squares moving average.offset[​](#least-squares-moving-averageoffset)
• least squares moving average.offset: `number`

- Default value: `0`
- Input type: `integer`
- Min: `-1000000000000`
- Max: `1000000000000`

### least squares moving average.plot.color[​](#least-squares-moving-averageplotcolor)
• least squares moving average.plot.color: `string`

Default value: `#2196F3`

### least squares moving average.plot.display[​](#least-squares-moving-averageplotdisplay)
• least squares moving average.plot.display: `number`

Default value: `15`

### least squares moving average.plot.linestyle[​](#least-squares-moving-averageplotlinestyle)
• least squares moving average.plot.linestyle: `number`

Default value: `0`

### least squares moving average.plot.linewidth[​](#least-squares-moving-averageplotlinewidth)
• least squares moving average.plot.linewidth: `number`

Default value: `1`

### least squares moving average.plot.plottype[​](#least-squares-moving-averageplotplottype)
• least squares moving average.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### least squares moving average.plot.trackprice[​](#least-squares-moving-averageplottrackprice)
• least squares moving average.plot.trackprice: `boolean`

Default value: `false`

### least squares moving average.plot.transparency[​](#least-squares-moving-averageplottransparency)
• least squares moving average.plot.transparency: `number`

Default value: `0`

### lineWithMarkersStyle.closeLineColor[​](#linewithmarkersstylecloselinecolor)
• lineWithMarkersStyle.closeLineColor: `string`

### lineWithMarkersStyle.closeLineStyle[​](#linewithmarkersstylecloselinestyle)
• lineWithMarkersStyle.closeLineStyle: `number`

### lineWithMarkersStyle.closeLineWidth[​](#linewithmarkersstylecloselinewidth)
• lineWithMarkersStyle.closeLineWidth: `number`

### lineWithMarkersStyle.closeLowFillColor[​](#linewithmarkersstylecloselowfillcolor)
• lineWithMarkersStyle.closeLowFillColor: `string`

### lineWithMarkersStyle.highCloseFillColor[​](#linewithmarkersstylehighclosefillcolor)
• lineWithMarkersStyle.highCloseFillColor: `string`

### lineWithMarkersStyle.highLineColor[​](#linewithmarkersstylehighlinecolor)
• lineWithMarkersStyle.highLineColor: `string`

### lineWithMarkersStyle.highLineStyle[​](#linewithmarkersstylehighlinestyle)
• lineWithMarkersStyle.highLineStyle: `number`

### lineWithMarkersStyle.highLineWidth[​](#linewithmarkersstylehighlinewidth)
• lineWithMarkersStyle.highLineWidth: `number`

### lineWithMarkersStyle.lowLineColor[​](#linewithmarkersstylelowlinecolor)
• lineWithMarkersStyle.lowLineColor: `string`

### lineWithMarkersStyle.lowLineStyle[​](#linewithmarkersstylelowlinestyle)
• lineWithMarkersStyle.lowLineStyle: `number`

### lineWithMarkersStyle.lowLineWidth[​](#linewithmarkersstylelowlinewidth)
• lineWithMarkersStyle.lowLineWidth: `number`

### linear regression curve.length[​](#linear-regression-curvelength)
• linear regression curve.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### linear regression curve.plot.color[​](#linear-regression-curveplotcolor)
• linear regression curve.plot.color: `string`

Default value: `#2196F3`

### linear regression curve.plot.display[​](#linear-regression-curveplotdisplay)
• linear regression curve.plot.display: `number`

Default value: `15`

### linear regression curve.plot.linestyle[​](#linear-regression-curveplotlinestyle)
• linear regression curve.plot.linestyle: `number`

Default value: `0`

### linear regression curve.plot.linewidth[​](#linear-regression-curveplotlinewidth)
• linear regression curve.plot.linewidth: `number`

Default value: `1`

### linear regression curve.plot.plottype[​](#linear-regression-curveplotplottype)
• linear regression curve.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### linear regression curve.plot.trackprice[​](#linear-regression-curveplottrackprice)
• linear regression curve.plot.trackprice: `boolean`

Default value: `false`

### linear regression curve.plot.transparency[​](#linear-regression-curveplottransparency)
• linear regression curve.plot.transparency: `number`

Default value: `0`

### linear regression slope.periods[​](#linear-regression-slopeperiods)
• linear regression slope.periods: `number`

- Default value: `14`
- Input type: `integer`
- Min: `2`

### linear regression slope.plot.color[​](#linear-regression-slopeplotcolor)
• linear regression slope.plot.color: `string`

Default value: `#FF5252`

### linear regression slope.plot.display[​](#linear-regression-slopeplotdisplay)
• linear regression slope.plot.display: `number`

Default value: `15`

### linear regression slope.plot.linestyle[​](#linear-regression-slopeplotlinestyle)
• linear regression slope.plot.linestyle: `number`

Default value: `0`

### linear regression slope.plot.linewidth[​](#linear-regression-slopeplotlinewidth)
• linear regression slope.plot.linewidth: `number`

Default value: `1`

### linear regression slope.plot.plottype[​](#linear-regression-slopeplotplottype)
• linear regression slope.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### linear regression slope.plot.trackprice[​](#linear-regression-slopeplottrackprice)
• linear regression slope.plot.trackprice: `boolean`

Default value: `false`

### linear regression slope.plot.transparency[​](#linear-regression-slopeplottransparency)
• linear regression slope.plot.transparency: `number`

Default value: `0`

### ma cross.crosses.color[​](#ma-crosscrossescolor)
• ma cross.crosses.color: `string`

Default value: `#2196F3`

### ma cross.crosses.display[​](#ma-crosscrossesdisplay)
• ma cross.crosses.display: `number`

Default value: `15`

### ma cross.crosses.linestyle[​](#ma-crosscrosseslinestyle)
• ma cross.crosses.linestyle: `number`

Default value: `0`

### ma cross.crosses.linewidth[​](#ma-crosscrosseslinewidth)
• ma cross.crosses.linewidth: `number`

Default value: `4`

### ma cross.crosses.plottype[​](#ma-crosscrossesplottype)
• ma cross.crosses.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `cross`

### ma cross.crosses.trackprice[​](#ma-crosscrossestrackprice)
• ma cross.crosses.trackprice: `boolean`

Default value: `false`

### ma cross.crosses.transparency[​](#ma-crosscrossestransparency)
• ma cross.crosses.transparency: `number`

Default value: `0`

### ma cross.long:input[​](#ma-crosslong)
• ma cross.long:input: `number`

- Default value: `26`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### ma cross.long:plot.color[​](#ma-crosslongcolor)
• ma cross.long:plot.color: `string`

Default value: `#FF6D00`

### ma cross.long:plot.display[​](#ma-crosslongdisplay)
• ma cross.long:plot.display: `number`

Default value: `15`

### ma cross.long:plot.linestyle[​](#ma-crosslonglinestyle)
• ma cross.long:plot.linestyle: `number`

Default value: `0`

### ma cross.long:plot.linewidth[​](#ma-crosslonglinewidth)
• ma cross.long:plot.linewidth: `number`

Default value: `1`

### ma cross.long:plot.plottype[​](#ma-crosslongplottype)
• ma cross.long:plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ma cross.long:plot.trackprice[​](#ma-crosslongtrackprice)
• ma cross.long:plot.trackprice: `boolean`

Default value: `false`

### ma cross.long:plot.transparency[​](#ma-crosslongtransparency)
• ma cross.long:plot.transparency: `number`

Default value: `0`

### ma cross.short:input[​](#ma-crossshort)
• ma cross.short:input: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### ma cross.short:plot.color[​](#ma-crossshortcolor)
• ma cross.short:plot.color: `string`

Default value: `#43A047`

### ma cross.short:plot.display[​](#ma-crossshortdisplay)
• ma cross.short:plot.display: `number`

Default value: `15`

### ma cross.short:plot.linestyle[​](#ma-crossshortlinestyle)
• ma cross.short:plot.linestyle: `number`

Default value: `0`

### ma cross.short:plot.linewidth[​](#ma-crossshortlinewidth)
• ma cross.short:plot.linewidth: `number`

Default value: `1`

### ma cross.short:plot.plottype[​](#ma-crossshortplottype)
• ma cross.short:plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ma cross.short:plot.trackprice[​](#ma-crossshorttrackprice)
• ma cross.short:plot.trackprice: `boolean`

Default value: `false`

### ma cross.short:plot.transparency[​](#ma-crossshorttransparency)
• ma cross.short:plot.transparency: `number`

Default value: `0`

### ma with ema cross.crosses.color[​](#ma-with-ema-crosscrossescolor)
• ma with ema cross.crosses.color: `string`

Default value: `#2196F3`

### ma with ema cross.crosses.display[​](#ma-with-ema-crosscrossesdisplay)
• ma with ema cross.crosses.display: `number`

Default value: `15`

### ma with ema cross.crosses.linestyle[​](#ma-with-ema-crosscrosseslinestyle)
• ma with ema cross.crosses.linestyle: `number`

Default value: `0`

### ma with ema cross.crosses.linewidth[​](#ma-with-ema-crosscrosseslinewidth)
• ma with ema cross.crosses.linewidth: `number`

Default value: `4`

### ma with ema cross.crosses.plottype[​](#ma-with-ema-crosscrossesplottype)
• ma with ema cross.crosses.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `cross`

### ma with ema cross.crosses.trackprice[​](#ma-with-ema-crosscrossestrackprice)
• ma with ema cross.crosses.trackprice: `boolean`

Default value: `false`

### ma with ema cross.crosses.transparency[​](#ma-with-ema-crosscrossestransparency)
• ma with ema cross.crosses.transparency: `number`

Default value: `0`

### ma with ema cross.ema.color[​](#ma-with-ema-crossemacolor)
• ma with ema cross.ema.color: `string`

Default value: `#43A047`

### ma with ema cross.ema.display[​](#ma-with-ema-crossemadisplay)
• ma with ema cross.ema.display: `number`

Default value: `15`

### ma with ema cross.ema.linestyle[​](#ma-with-ema-crossemalinestyle)
• ma with ema cross.ema.linestyle: `number`

Default value: `0`

### ma with ema cross.ema.linewidth[​](#ma-with-ema-crossemalinewidth)
• ma with ema cross.ema.linewidth: `number`

Default value: `1`

### ma with ema cross.ema.plottype[​](#ma-with-ema-crossemaplottype)
• ma with ema cross.ema.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ma with ema cross.ema.trackprice[​](#ma-with-ema-crossematrackprice)
• ma with ema cross.ema.trackprice: `boolean`

Default value: `false`

### ma with ema cross.ema.transparency[​](#ma-with-ema-crossematransparency)
• ma with ema cross.ema.transparency: `number`

Default value: `0`

### ma with ema cross.length ema[​](#ma-with-ema-crosslength-ema)
• ma with ema cross.length ema: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### ma with ema cross.length ma[​](#ma-with-ema-crosslength-ma)
• ma with ema cross.length ma: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### ma with ema cross.ma.color[​](#ma-with-ema-crossmacolor)
• ma with ema cross.ma.color: `string`

Default value: `#FF6D00`

### ma with ema cross.ma.display[​](#ma-with-ema-crossmadisplay)
• ma with ema cross.ma.display: `number`

Default value: `15`

### ma with ema cross.ma.linestyle[​](#ma-with-ema-crossmalinestyle)
• ma with ema cross.ma.linestyle: `number`

Default value: `0`

### ma with ema cross.ma.linewidth[​](#ma-with-ema-crossmalinewidth)
• ma with ema cross.ma.linewidth: `number`

Default value: `1`

### ma with ema cross.ma.plottype[​](#ma-with-ema-crossmaplottype)
• ma with ema cross.ma.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ma with ema cross.ma.trackprice[​](#ma-with-ema-crossmatrackprice)
• ma with ema cross.ma.trackprice: `boolean`

Default value: `false`

### ma with ema cross.ma.transparency[​](#ma-with-ema-crossmatransparency)
• ma with ema cross.ma.transparency: `number`

Default value: `0`

### macd.fast length[​](#macdfast-length)
• macd.fast length: `number`

- Default value: `12`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### macd.histogram.color[​](#macdhistogramcolor)
• macd.histogram.color: `string`

Default value: `#FF5252`

### macd.histogram.display[​](#macdhistogramdisplay)
• macd.histogram.display: `number`

Default value: `15`

### macd.histogram.linestyle[​](#macdhistogramlinestyle)
• macd.histogram.linestyle: `number`

Default value: `0`

### macd.histogram.linewidth[​](#macdhistogramlinewidth)
• macd.histogram.linewidth: `number`

Default value: `1`

### macd.histogram.plottype[​](#macdhistogramplottype)
• macd.histogram.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `columns`

### macd.histogram.trackprice[​](#macdhistogramtrackprice)
• macd.histogram.trackprice: `boolean`

Default value: `false`

### macd.histogram.transparency[​](#macdhistogramtransparency)
• macd.histogram.transparency: `number`

Default value: `0`

### macd.macd.color[​](#macdmacdcolor)
• macd.macd.color: `string`

Default value: `#2196F3`

### macd.macd.display[​](#macdmacddisplay)
• macd.macd.display: `number`

Default value: `15`

### macd.macd.linestyle[​](#macdmacdlinestyle)
• macd.macd.linestyle: `number`

Default value: `0`

### macd.macd.linewidth[​](#macdmacdlinewidth)
• macd.macd.linewidth: `number`

Default value: `1`

### macd.macd.plottype[​](#macdmacdplottype)
• macd.macd.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### macd.macd.trackprice[​](#macdmacdtrackprice)
• macd.macd.trackprice: `boolean`

Default value: `false`

### macd.macd.transparency[​](#macdmacdtransparency)
• macd.macd.transparency: `number`

Default value: `0`

### macd.oscillator ma type[​](#macdoscillator-ma-type)
• macd.oscillator ma type: `string`

- Default value: `EMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### macd.other symbol[​](#macdother-symbol)
• macd.other symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Optional: `true`
- IsHidden: `false`

### macd.signal length[​](#macdsignal-length)
• macd.signal length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `50`

### macd.signal line ma type[​](#macdsignal-line-ma-type)
• macd.signal line ma type: `string`

- Default value: `EMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### macd.signal.color[​](#macdsignalcolor)
• macd.signal.color: `string`

Default value: `#FF6D00`

### macd.signal.display[​](#macdsignaldisplay)
• macd.signal.display: `number`

Default value: `15`

### macd.signal.linestyle[​](#macdsignallinestyle)
• macd.signal.linestyle: `number`

Default value: `0`

### macd.signal.linewidth[​](#macdsignallinewidth)
• macd.signal.linewidth: `number`

Default value: `1`

### macd.signal.plottype[​](#macdsignalplottype)
• macd.signal.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### macd.signal.trackprice[​](#macdsignaltrackprice)
• macd.signal.trackprice: `boolean`

Default value: `false`

### macd.signal.transparency[​](#macdsignaltransparency)
• macd.signal.transparency: `number`

Default value: `0`

### macd.slow length[​](#macdslow-length)
• macd.slow length: `number`

- Default value: `26`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### macd.source[​](#macdsource)
• macd.source: `string`

- Default value: `close`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### majority rule.majority rule.color[​](#majority-rulemajority-rulecolor)
• majority rule.majority rule.color: `string`

Default value: `#FF5252`

### majority rule.majority rule.display[​](#majority-rulemajority-ruledisplay)
• majority rule.majority rule.display: `number`

Default value: `15`

### majority rule.majority rule.linestyle[​](#majority-rulemajority-rulelinestyle)
• majority rule.majority rule.linestyle: `number`

Default value: `0`

### majority rule.majority rule.linewidth[​](#majority-rulemajority-rulelinewidth)
• majority rule.majority rule.linewidth: `number`

Default value: `1`

### majority rule.majority rule.plottype[​](#majority-rulemajority-ruleplottype)
• majority rule.majority rule.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### majority rule.majority rule.trackprice[​](#majority-rulemajority-ruletrackprice)
• majority rule.majority rule.trackprice: `boolean`

Default value: `false`

### majority rule.majority rule.transparency[​](#majority-rulemajority-ruletransparency)
• majority rule.majority rule.transparency: `number`

Default value: `0`

### majority rule.rolling period[​](#majority-rulerolling-period)
• majority rule.rolling period: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`

### mass index.length[​](#mass-indexlength)
• mass index.length: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### mass index.plot.color[​](#mass-indexplotcolor)
• mass index.plot.color: `string`

Default value: `#2196F3`

### mass index.plot.display[​](#mass-indexplotdisplay)
• mass index.plot.display: `number`

Default value: `15`

### mass index.plot.linestyle[​](#mass-indexplotlinestyle)
• mass index.plot.linestyle: `number`

Default value: `0`

### mass index.plot.linewidth[​](#mass-indexplotlinewidth)
• mass index.plot.linewidth: `number`

Default value: `1`

### mass index.plot.plottype[​](#mass-indexplotplottype)
• mass index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### mass index.plot.trackprice[​](#mass-indexplottrackprice)
• mass index.plot.trackprice: `boolean`

Default value: `false`

### mass index.plot.transparency[​](#mass-indexplottransparency)
• mass index.plot.transparency: `number`

Default value: `0`

### mcginley dynamic.length[​](#mcginley-dynamiclength)
• mcginley dynamic.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### mcginley dynamic.plot.color[​](#mcginley-dynamicplotcolor)
• mcginley dynamic.plot.color: `string`

Default value: `#2196F3`

### mcginley dynamic.plot.display[​](#mcginley-dynamicplotdisplay)
• mcginley dynamic.plot.display: `number`

Default value: `15`

### mcginley dynamic.plot.linestyle[​](#mcginley-dynamicplotlinestyle)
• mcginley dynamic.plot.linestyle: `number`

Default value: `0`

### mcginley dynamic.plot.linewidth[​](#mcginley-dynamicplotlinewidth)
• mcginley dynamic.plot.linewidth: `number`

Default value: `1`

### mcginley dynamic.plot.plottype[​](#mcginley-dynamicplotplottype)
• mcginley dynamic.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### mcginley dynamic.plot.trackprice[​](#mcginley-dynamicplottrackprice)
• mcginley dynamic.plot.trackprice: `boolean`

Default value: `false`

### mcginley dynamic.plot.transparency[​](#mcginley-dynamicplottransparency)
• mcginley dynamic.plot.transparency: `number`

Default value: `0`

### median price.plot.color[​](#median-priceplotcolor)
• median price.plot.color: `string`

Default value: `#FF6D00`

### median price.plot.display[​](#median-priceplotdisplay)
• median price.plot.display: `number`

Default value: `15`

### median price.plot.linestyle[​](#median-priceplotlinestyle)
• median price.plot.linestyle: `number`

Default value: `0`

### median price.plot.linewidth[​](#median-priceplotlinewidth)
• median price.plot.linewidth: `number`

Default value: `1`

### median price.plot.plottype[​](#median-priceplotplottype)
• median price.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### median price.plot.trackprice[​](#median-priceplottrackprice)
• median price.plot.trackprice: `boolean`

Default value: `false`

### median price.plot.transparency[​](#median-priceplottransparency)
• median price.plot.transparency: `number`

Default value: `0`

### momentum.length[​](#momentumlength)
• momentum.length: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### momentum.mom.color[​](#momentummomcolor)
• momentum.mom.color: `string`

Default value: `#2196F3`

### momentum.mom.display[​](#momentummomdisplay)
• momentum.mom.display: `number`

Default value: `15`

### momentum.mom.linestyle[​](#momentummomlinestyle)
• momentum.mom.linestyle: `number`

Default value: `0`

### momentum.mom.linewidth[​](#momentummomlinewidth)
• momentum.mom.linewidth: `number`

Default value: `1`

### momentum.mom.plottype[​](#momentummomplottype)
• momentum.mom.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### momentum.mom.trackprice[​](#momentummomtrackprice)
• momentum.mom.trackprice: `boolean`

Default value: `false`

### momentum.mom.transparency[​](#momentummomtransparency)
• momentum.mom.transparency: `number`

Default value: `0`

### momentum.source[​](#momentumsource)
• momentum.source: `string`

- Default value: `close`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### momentum.zero.color[​](#momentumzerocolor)
• momentum.zero.color: `string`

Default value: `#787B86`

### momentum.zero.linestyle[​](#momentumzerolinestyle)
• momentum.zero.linestyle: `number`

Default value: `2`

### momentum.zero.linewidth[​](#momentumzerolinewidth)
• momentum.zero.linewidth: `number`

Default value: `1`

### momentum.zero.value[​](#momentumzerovalue)
• momentum.zero.value: `number`

Default value: `0`

### momentum.zero.visible[​](#momentumzerovisible)
• momentum.zero.visible: `boolean`

Default value: `true`

### money flow index.hlines background.color[​](#money-flow-indexhlines-backgroundcolor)
• money flow index.hlines background.color: `string`

Default value: `#7E57C2`

### money flow index.hlines background.transparency[​](#money-flow-indexhlines-backgroundtransparency)
• money flow index.hlines background.transparency: `number`

Default value: `90`

### money flow index.hlines background.visible[​](#money-flow-indexhlines-backgroundvisible)
• money flow index.hlines background.visible: `boolean`

Default value: `true`

### money flow index.length[​](#money-flow-indexlength)
• money flow index.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### money flow index.lowerlimit.color[​](#money-flow-indexlowerlimitcolor)
• money flow index.lowerlimit.color: `string`

Default value: `#787B86`

### money flow index.lowerlimit.linestyle[​](#money-flow-indexlowerlimitlinestyle)
• money flow index.lowerlimit.linestyle: `number`

Default value: `2`

### money flow index.lowerlimit.linewidth[​](#money-flow-indexlowerlimitlinewidth)
• money flow index.lowerlimit.linewidth: `number`

Default value: `1`

### money flow index.lowerlimit.value[​](#money-flow-indexlowerlimitvalue)
• money flow index.lowerlimit.value: `number`

Default value: `20`

### money flow index.lowerlimit.visible[​](#money-flow-indexlowerlimitvisible)
• money flow index.lowerlimit.visible: `boolean`

Default value: `true`

### money flow index.plot.color[​](#money-flow-indexplotcolor)
• money flow index.plot.color: `string`

Default value: `#7E57C2`

### money flow index.plot.display[​](#money-flow-indexplotdisplay)
• money flow index.plot.display: `number`

Default value: `15`

### money flow index.plot.linestyle[​](#money-flow-indexplotlinestyle)
• money flow index.plot.linestyle: `number`

Default value: `0`

### money flow index.plot.linewidth[​](#money-flow-indexplotlinewidth)
• money flow index.plot.linewidth: `number`

Default value: `1`

### money flow index.plot.plottype[​](#money-flow-indexplotplottype)
• money flow index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### money flow index.plot.trackprice[​](#money-flow-indexplottrackprice)
• money flow index.plot.trackprice: `boolean`

Default value: `false`

### money flow index.plot.transparency[​](#money-flow-indexplottransparency)
• money flow index.plot.transparency: `number`

Default value: `0`

### money flow index.upperlimit.color[​](#money-flow-indexupperlimitcolor)
• money flow index.upperlimit.color: `string`

Default value: `#787B86`

### money flow index.upperlimit.linestyle[​](#money-flow-indexupperlimitlinestyle)
• money flow index.upperlimit.linestyle: `number`

Default value: `2`

### money flow index.upperlimit.linewidth[​](#money-flow-indexupperlimitlinewidth)
• money flow index.upperlimit.linewidth: `number`

Default value: `1`

### money flow index.upperlimit.value[​](#money-flow-indexupperlimitvalue)
• money flow index.upperlimit.value: `number`

Default value: `80`

### money flow index.upperlimit.visible[​](#money-flow-indexupperlimitvisible)
• money flow index.upperlimit.visible: `boolean`

Default value: `true`

### moving average adaptive.period[​](#moving-average-adaptiveperiod)
• moving average adaptive.period: `number`

- Default value: `10`
- Input type: `integer`
- Min: `2`
- Max: `10000`

### moving average adaptive.plot 1.color[​](#moving-average-adaptiveplot-1color)
• moving average adaptive.plot 1.color: `string`

Default value: `#AB47BC`

### moving average adaptive.plot 1.display[​](#moving-average-adaptiveplot-1display)
• moving average adaptive.plot 1.display: `number`

Default value: `15`

### moving average adaptive.plot 1.linestyle[​](#moving-average-adaptiveplot-1linestyle)
• moving average adaptive.plot 1.linestyle: `number`

Default value: `0`

### moving average adaptive.plot 1.linewidth[​](#moving-average-adaptiveplot-1linewidth)
• moving average adaptive.plot 1.linewidth: `number`

Default value: `1`

### moving average adaptive.plot 1.plottype[​](#moving-average-adaptiveplot-1plottype)
• moving average adaptive.plot 1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average adaptive.plot 1.trackprice[​](#moving-average-adaptiveplot-1trackprice)
• moving average adaptive.plot 1.trackprice: `boolean`

Default value: `false`

### moving average adaptive.plot 1.transparency[​](#moving-average-adaptiveplot-1transparency)
• moving average adaptive.plot 1.transparency: `number`

Default value: `0`

### moving average channel.lower length[​](#moving-average-channellower-length)
• moving average channel.lower length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average channel.lower offset[​](#moving-average-channellower-offset)
• moving average channel.lower offset: `number`

- Default value: `0`
- Input type: `integer`
- Min: `-10000`
- Max: `10000`

### moving average channel.lower.color[​](#moving-average-channellowercolor)
• moving average channel.lower.color: `string`

Default value: `#FF6D00`

### moving average channel.lower.display[​](#moving-average-channellowerdisplay)
• moving average channel.lower.display: `number`

Default value: `15`

### moving average channel.lower.linestyle[​](#moving-average-channellowerlinestyle)
• moving average channel.lower.linestyle: `number`

Default value: `0`

### moving average channel.lower.linewidth[​](#moving-average-channellowerlinewidth)
• moving average channel.lower.linewidth: `number`

Default value: `1`

### moving average channel.lower.plottype[​](#moving-average-channellowerplottype)
• moving average channel.lower.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average channel.lower.trackprice[​](#moving-average-channellowertrackprice)
• moving average channel.lower.trackprice: `boolean`

Default value: `false`

### moving average channel.lower.transparency[​](#moving-average-channellowertransparency)
• moving average channel.lower.transparency: `number`

Default value: `0`

### moving average channel.plots background.color[​](#moving-average-channelplots-backgroundcolor)
• moving average channel.plots background.color: `string`

Default value: `#2196F3`

### moving average channel.plots background.transparency[​](#moving-average-channelplots-backgroundtransparency)
• moving average channel.plots background.transparency: `number`

Default value: `90`

### moving average channel.plots background.visible[​](#moving-average-channelplots-backgroundvisible)
• moving average channel.plots background.visible: `boolean`

Default value: `true`

### moving average channel.upper length[​](#moving-average-channelupper-length)
• moving average channel.upper length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average channel.upper offset[​](#moving-average-channelupper-offset)
• moving average channel.upper offset: `number`

- Default value: `0`
- Input type: `integer`
- Min: `-10000`
- Max: `10000`

### moving average channel.upper.color[​](#moving-average-channeluppercolor)
• moving average channel.upper.color: `string`

Default value: `#2196F3`

### moving average channel.upper.display[​](#moving-average-channelupperdisplay)
• moving average channel.upper.display: `number`

Default value: `15`

### moving average channel.upper.linestyle[​](#moving-average-channelupperlinestyle)
• moving average channel.upper.linestyle: `number`

Default value: `0`

### moving average channel.upper.linewidth[​](#moving-average-channelupperlinewidth)
• moving average channel.upper.linewidth: `number`

Default value: `1`

### moving average channel.upper.plottype[​](#moving-average-channelupperplottype)
• moving average channel.upper.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average channel.upper.trackprice[​](#moving-average-channeluppertrackprice)
• moving average channel.upper.trackprice: `boolean`

Default value: `false`

### moving average channel.upper.transparency[​](#moving-average-channeluppertransparency)
• moving average channel.upper.transparency: `number`

Default value: `0`

### moving average double.1st period[​](#moving-average-double1st-period)
• moving average double.1st period: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average double.2nd period[​](#moving-average-double2nd-period)
• moving average double.2nd period: `number`

- Default value: `21`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average double.another symbol[​](#moving-average-doubleanother-symbol)
• moving average double.another symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Optional: `true`
- IsHidden: `false`

### moving average double.method[​](#moving-average-doublemethod)
• moving average double.method: `string`

- Default value: `Simple`
- Input type: `text`
- Options: `["Simple","Exponential","Weighted"]`

### moving average double.plot 1.color[​](#moving-average-doubleplot-1color)
• moving average double.plot 1.color: `string`

Default value: `#FF6D00`

### moving average double.plot 1.display[​](#moving-average-doubleplot-1display)
• moving average double.plot 1.display: `number`

Default value: `15`

### moving average double.plot 1.linestyle[​](#moving-average-doubleplot-1linestyle)
• moving average double.plot 1.linestyle: `number`

Default value: `0`

### moving average double.plot 1.linewidth[​](#moving-average-doubleplot-1linewidth)
• moving average double.plot 1.linewidth: `number`

Default value: `1`

### moving average double.plot 1.plottype[​](#moving-average-doubleplot-1plottype)
• moving average double.plot 1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average double.plot 1.trackprice[​](#moving-average-doubleplot-1trackprice)
• moving average double.plot 1.trackprice: `boolean`

Default value: `false`

### moving average double.plot 1.transparency[​](#moving-average-doubleplot-1transparency)
• moving average double.plot 1.transparency: `number`

Default value: `0`

### moving average double.plot 2.color[​](#moving-average-doubleplot-2color)
• moving average double.plot 2.color: `string`

Default value: `#2196F3`

### moving average double.plot 2.display[​](#moving-average-doubleplot-2display)
• moving average double.plot 2.display: `number`

Default value: `15`

### moving average double.plot 2.linestyle[​](#moving-average-doubleplot-2linestyle)
• moving average double.plot 2.linestyle: `number`

Default value: `0`

### moving average double.plot 2.linewidth[​](#moving-average-doubleplot-2linewidth)
• moving average double.plot 2.linewidth: `number`

Default value: `1`

### moving average double.plot 2.plottype[​](#moving-average-doubleplot-2plottype)
• moving average double.plot 2.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average double.plot 2.trackprice[​](#moving-average-doubleplot-2trackprice)
• moving average double.plot 2.trackprice: `boolean`

Default value: `false`

### moving average double.plot 2.transparency[​](#moving-average-doubleplot-2transparency)
• moving average double.plot 2.transparency: `number`

Default value: `0`

### moving average exponential.length[​](#moving-average-exponentiallength)
• moving average exponential.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average exponential.offset[​](#moving-average-exponentialoffset)
• moving average exponential.offset: `number`

- Default value: `0`
- Input type: `integer`
- Min: `-10000`
- Max: `10000`

### moving average exponential.plot.color[​](#moving-average-exponentialplotcolor)
• moving average exponential.plot.color: `string`

Default value: `#2196F3`

### moving average exponential.plot.display[​](#moving-average-exponentialplotdisplay)
• moving average exponential.plot.display: `number`

Default value: `15`

### moving average exponential.plot.linestyle[​](#moving-average-exponentialplotlinestyle)
• moving average exponential.plot.linestyle: `number`

Default value: `0`

### moving average exponential.plot.linewidth[​](#moving-average-exponentialplotlinewidth)
• moving average exponential.plot.linewidth: `number`

Default value: `1`

### moving average exponential.plot.plottype[​](#moving-average-exponentialplotplottype)
• moving average exponential.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average exponential.plot.trackprice[​](#moving-average-exponentialplottrackprice)
• moving average exponential.plot.trackprice: `boolean`

Default value: `false`

### moving average exponential.plot.transparency[​](#moving-average-exponentialplottransparency)
• moving average exponential.plot.transparency: `number`

Default value: `0`

### moving average exponential.smoothed ma.display[​](#moving-average-exponentialsmoothed-madisplay)
• moving average exponential.smoothed ma.display: `number`

Default value: `0`

### moving average exponential.smoothed ma.linestyle[​](#moving-average-exponentialsmoothed-malinestyle)
• moving average exponential.smoothed ma.linestyle: `number`

Default value: `0`

### moving average exponential.smoothed ma.linewidth[​](#moving-average-exponentialsmoothed-malinewidth)
• moving average exponential.smoothed ma.linewidth: `number`

Default value: `1`

### moving average exponential.smoothed ma.plottype[​](#moving-average-exponentialsmoothed-maplottype)
• moving average exponential.smoothed ma.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average exponential.smoothed ma.trackprice[​](#moving-average-exponentialsmoothed-matrackprice)
• moving average exponential.smoothed ma.trackprice: `boolean`

Default value: `false`

### moving average exponential.smoothed ma.transparency[​](#moving-average-exponentialsmoothed-matransparency)
• moving average exponential.smoothed ma.transparency: `number`

Default value: `0`

### moving average exponential.smoothing length[​](#moving-average-exponentialsmoothing-length)
• moving average exponential.smoothing length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average exponential.smoothing line[​](#moving-average-exponentialsmoothing-line)
• moving average exponential.smoothing line: `string`

- Default value: `SMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### moving average exponential.source[​](#moving-average-exponentialsource)
• moving average exponential.source: `string`

- Default value: `close`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### moving average hamming.period[​](#moving-average-hammingperiod)
• moving average hamming.period: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average hamming.plot 1.color[​](#moving-average-hammingplot-1color)
• moving average hamming.plot 1.color: `string`

Default value: `#4CAF50`

### moving average hamming.plot 1.display[​](#moving-average-hammingplot-1display)
• moving average hamming.plot 1.display: `number`

Default value: `15`

### moving average hamming.plot 1.linestyle[​](#moving-average-hammingplot-1linestyle)
• moving average hamming.plot 1.linestyle: `number`

Default value: `0`

### moving average hamming.plot 1.linewidth[​](#moving-average-hammingplot-1linewidth)
• moving average hamming.plot 1.linewidth: `number`

Default value: `1`

### moving average hamming.plot 1.plottype[​](#moving-average-hammingplot-1plottype)
• moving average hamming.plot 1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average hamming.plot 1.trackprice[​](#moving-average-hammingplot-1trackprice)
• moving average hamming.plot 1.trackprice: `boolean`

Default value: `false`

### moving average hamming.plot 1.transparency[​](#moving-average-hammingplot-1transparency)
• moving average hamming.plot 1.transparency: `number`

Default value: `0`

### moving average multiple.1st period[​](#moving-average-multiple1st-period)
• moving average multiple.1st period: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average multiple.2nd period[​](#moving-average-multiple2nd-period)
• moving average multiple.2nd period: `number`

- Default value: `21`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average multiple.3rd period[​](#moving-average-multiple3rd-period)
• moving average multiple.3rd period: `number`

- Default value: `35`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average multiple.4th period[​](#moving-average-multiple4th-period)
• moving average multiple.4th period: `number`

- Default value: `50`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average multiple.5th period[​](#moving-average-multiple5th-period)
• moving average multiple.5th period: `number`

- Default value: `100`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average multiple.6th period[​](#moving-average-multiple6th-period)
• moving average multiple.6th period: `number`

- Default value: `200`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average multiple.method[​](#moving-average-multiplemethod)
• moving average multiple.method: `string`

- Default value: `Simple`
- Input type: `text`
- Options: `["Simple","Exponential","Weighted"]`

### moving average multiple.plot 1.color[​](#moving-average-multipleplot-1color)
• moving average multiple.plot 1.color: `string`

Default value: `#9C27B0`

### moving average multiple.plot 1.display[​](#moving-average-multipleplot-1display)
• moving average multiple.plot 1.display: `number`

Default value: `15`

### moving average multiple.plot 1.linestyle[​](#moving-average-multipleplot-1linestyle)
• moving average multiple.plot 1.linestyle: `number`

Default value: `0`

### moving average multiple.plot 1.linewidth[​](#moving-average-multipleplot-1linewidth)
• moving average multiple.plot 1.linewidth: `number`

Default value: `1`

### moving average multiple.plot 1.plottype[​](#moving-average-multipleplot-1plottype)
• moving average multiple.plot 1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average multiple.plot 1.trackprice[​](#moving-average-multipleplot-1trackprice)
• moving average multiple.plot 1.trackprice: `boolean`

Default value: `false`

### moving average multiple.plot 1.transparency[​](#moving-average-multipleplot-1transparency)
• moving average multiple.plot 1.transparency: `number`

Default value: `0`

### moving average multiple.plot 2.color[​](#moving-average-multipleplot-2color)
• moving average multiple.plot 2.color: `string`

Default value: `#FF6D00`

### moving average multiple.plot 2.display[​](#moving-average-multipleplot-2display)
• moving average multiple.plot 2.display: `number`

Default value: `15`

### moving average multiple.plot 2.linestyle[​](#moving-average-multipleplot-2linestyle)
• moving average multiple.plot 2.linestyle: `number`

Default value: `0`

### moving average multiple.plot 2.linewidth[​](#moving-average-multipleplot-2linewidth)
• moving average multiple.plot 2.linewidth: `number`

Default value: `1`

### moving average multiple.plot 2.plottype[​](#moving-average-multipleplot-2plottype)
• moving average multiple.plot 2.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average multiple.plot 2.trackprice[​](#moving-average-multipleplot-2trackprice)
• moving average multiple.plot 2.trackprice: `boolean`

Default value: `false`

### moving average multiple.plot 2.transparency[​](#moving-average-multipleplot-2transparency)
• moving average multiple.plot 2.transparency: `number`

Default value: `0`

### moving average multiple.plot 3.color[​](#moving-average-multipleplot-3color)
• moving average multiple.plot 3.color: `string`

Default value: `#43A047`

### moving average multiple.plot 3.display[​](#moving-average-multipleplot-3display)
• moving average multiple.plot 3.display: `number`

Default value: `15`

### moving average multiple.plot 3.linestyle[​](#moving-average-multipleplot-3linestyle)
• moving average multiple.plot 3.linestyle: `number`

Default value: `0`

### moving average multiple.plot 3.linewidth[​](#moving-average-multipleplot-3linewidth)
• moving average multiple.plot 3.linewidth: `number`

Default value: `1`

### moving average multiple.plot 3.plottype[​](#moving-average-multipleplot-3plottype)
• moving average multiple.plot 3.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average multiple.plot 3.trackprice[​](#moving-average-multipleplot-3trackprice)
• moving average multiple.plot 3.trackprice: `boolean`

Default value: `false`

### moving average multiple.plot 3.transparency[​](#moving-average-multipleplot-3transparency)
• moving average multiple.plot 3.transparency: `number`

Default value: `0`

### moving average multiple.plot 4.color[​](#moving-average-multipleplot-4color)
• moving average multiple.plot 4.color: `string`

Default value: `#26C6DA`

### moving average multiple.plot 4.display[​](#moving-average-multipleplot-4display)
• moving average multiple.plot 4.display: `number`

Default value: `15`

### moving average multiple.plot 4.linestyle[​](#moving-average-multipleplot-4linestyle)
• moving average multiple.plot 4.linestyle: `number`

Default value: `0`

### moving average multiple.plot 4.linewidth[​](#moving-average-multipleplot-4linewidth)
• moving average multiple.plot 4.linewidth: `number`

Default value: `1`

### moving average multiple.plot 4.plottype[​](#moving-average-multipleplot-4plottype)
• moving average multiple.plot 4.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average multiple.plot 4.trackprice[​](#moving-average-multipleplot-4trackprice)
• moving average multiple.plot 4.trackprice: `boolean`

Default value: `false`

### moving average multiple.plot 4.transparency[​](#moving-average-multipleplot-4transparency)
• moving average multiple.plot 4.transparency: `number`

Default value: `0`

### moving average multiple.plot 5.color[​](#moving-average-multipleplot-5color)
• moving average multiple.plot 5.color: `string`

Default value: `#F50057`

### moving average multiple.plot 5.display[​](#moving-average-multipleplot-5display)
• moving average multiple.plot 5.display: `number`

Default value: `15`

### moving average multiple.plot 5.linestyle[​](#moving-average-multipleplot-5linestyle)
• moving average multiple.plot 5.linestyle: `number`

Default value: `0`

### moving average multiple.plot 5.linewidth[​](#moving-average-multipleplot-5linewidth)
• moving average multiple.plot 5.linewidth: `number`

Default value: `1`

### moving average multiple.plot 5.plottype[​](#moving-average-multipleplot-5plottype)
• moving average multiple.plot 5.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average multiple.plot 5.trackprice[​](#moving-average-multipleplot-5trackprice)
• moving average multiple.plot 5.trackprice: `boolean`

Default value: `false`

### moving average multiple.plot 5.transparency[​](#moving-average-multipleplot-5transparency)
• moving average multiple.plot 5.transparency: `number`

Default value: `0`

### moving average multiple.plot 6.color[​](#moving-average-multipleplot-6color)
• moving average multiple.plot 6.color: `string`

Default value: `#2196F3`

### moving average multiple.plot 6.display[​](#moving-average-multipleplot-6display)
• moving average multiple.plot 6.display: `number`

Default value: `15`

### moving average multiple.plot 6.linestyle[​](#moving-average-multipleplot-6linestyle)
• moving average multiple.plot 6.linestyle: `number`

Default value: `0`

### moving average multiple.plot 6.linewidth[​](#moving-average-multipleplot-6linewidth)
• moving average multiple.plot 6.linewidth: `number`

Default value: `1`

### moving average multiple.plot 6.plottype[​](#moving-average-multipleplot-6plottype)
• moving average multiple.plot 6.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average multiple.plot 6.trackprice[​](#moving-average-multipleplot-6trackprice)
• moving average multiple.plot 6.trackprice: `boolean`

Default value: `false`

### moving average multiple.plot 6.transparency[​](#moving-average-multipleplot-6transparency)
• moving average multiple.plot 6.transparency: `number`

Default value: `0`

### moving average triple.1st period[​](#moving-average-triple1st-period)
• moving average triple.1st period: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average triple.2nd period[​](#moving-average-triple2nd-period)
• moving average triple.2nd period: `number`

- Default value: `21`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average triple.3rd period[​](#moving-average-triple3rd-period)
• moving average triple.3rd period: `number`

- Default value: `35`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average triple.method[​](#moving-average-triplemethod)
• moving average triple.method: `string`

- Default value: `Simple`
- Input type: `text`
- Options: `["Simple","Exponential","Weighted"]`

### moving average triple.plot 1.color[​](#moving-average-tripleplot-1color)
• moving average triple.plot 1.color: `string`

Default value: `#FF6D00`

### moving average triple.plot 1.display[​](#moving-average-tripleplot-1display)
• moving average triple.plot 1.display: `number`

Default value: `15`

### moving average triple.plot 1.linestyle[​](#moving-average-tripleplot-1linestyle)
• moving average triple.plot 1.linestyle: `number`

Default value: `0`

### moving average triple.plot 1.linewidth[​](#moving-average-tripleplot-1linewidth)
• moving average triple.plot 1.linewidth: `number`

Default value: `1`

### moving average triple.plot 1.plottype[​](#moving-average-tripleplot-1plottype)
• moving average triple.plot 1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average triple.plot 1.trackprice[​](#moving-average-tripleplot-1trackprice)
• moving average triple.plot 1.trackprice: `boolean`

Default value: `false`

### moving average triple.plot 1.transparency[​](#moving-average-tripleplot-1transparency)
• moving average triple.plot 1.transparency: `number`

Default value: `0`

### moving average triple.plot 2.color[​](#moving-average-tripleplot-2color)
• moving average triple.plot 2.color: `string`

Default value: `#2196F3`

### moving average triple.plot 2.display[​](#moving-average-tripleplot-2display)
• moving average triple.plot 2.display: `number`

Default value: `15`

### moving average triple.plot 2.linestyle[​](#moving-average-tripleplot-2linestyle)
• moving average triple.plot 2.linestyle: `number`

Default value: `0`

### moving average triple.plot 2.linewidth[​](#moving-average-tripleplot-2linewidth)
• moving average triple.plot 2.linewidth: `number`

Default value: `1`

### moving average triple.plot 2.plottype[​](#moving-average-tripleplot-2plottype)
• moving average triple.plot 2.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average triple.plot 2.trackprice[​](#moving-average-tripleplot-2trackprice)
• moving average triple.plot 2.trackprice: `boolean`

Default value: `false`

### moving average triple.plot 2.transparency[​](#moving-average-tripleplot-2transparency)
• moving average triple.plot 2.transparency: `number`

Default value: `0`

### moving average triple.plot 3.color[​](#moving-average-tripleplot-3color)
• moving average triple.plot 3.color: `string`

Default value: `#26C6DA`

### moving average triple.plot 3.display[​](#moving-average-tripleplot-3display)
• moving average triple.plot 3.display: `number`

Default value: `15`

### moving average triple.plot 3.linestyle[​](#moving-average-tripleplot-3linestyle)
• moving average triple.plot 3.linestyle: `number`

Default value: `0`

### moving average triple.plot 3.linewidth[​](#moving-average-tripleplot-3linewidth)
• moving average triple.plot 3.linewidth: `number`

Default value: `1`

### moving average triple.plot 3.plottype[​](#moving-average-tripleplot-3plottype)
• moving average triple.plot 3.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average triple.plot 3.trackprice[​](#moving-average-tripleplot-3trackprice)
• moving average triple.plot 3.trackprice: `boolean`

Default value: `false`

### moving average triple.plot 3.transparency[​](#moving-average-tripleplot-3transparency)
• moving average triple.plot 3.transparency: `number`

Default value: `0`

### moving average weighted.length[​](#moving-average-weightedlength)
• moving average weighted.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### moving average weighted.offset[​](#moving-average-weightedoffset)
• moving average weighted.offset: `number`

- Default value: `0`
- Input type: `integer`
- Min: `-10000`
- Max: `10000`

### moving average weighted.plot.color[​](#moving-average-weightedplotcolor)
• moving average weighted.plot.color: `string`

Default value: `#2196F3`

### moving average weighted.plot.display[​](#moving-average-weightedplotdisplay)
• moving average weighted.plot.display: `number`

Default value: `15`

### moving average weighted.plot.linestyle[​](#moving-average-weightedplotlinestyle)
• moving average weighted.plot.linestyle: `number`

Default value: `0`

### moving average weighted.plot.linewidth[​](#moving-average-weightedplotlinewidth)
• moving average weighted.plot.linewidth: `number`

Default value: `1`

### moving average weighted.plot.plottype[​](#moving-average-weightedplotplottype)
• moving average weighted.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average weighted.plot.trackprice[​](#moving-average-weightedplottrackprice)
• moving average weighted.plot.trackprice: `boolean`

Default value: `false`

### moving average weighted.plot.transparency[​](#moving-average-weightedplottransparency)
• moving average weighted.plot.transparency: `number`

Default value: `0`

### moving average weighted.source[​](#moving-average-weightedsource)
• moving average weighted.source: `string`

- Default value: `close`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### moving average.length[​](#moving-averagelength)
• moving average.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average.offset[​](#moving-averageoffset)
• moving average.offset: `number`

- Default value: `0`
- Input type: `integer`
- Min: `-10000`
- Max: `10000`

### moving average.other symbol[​](#moving-averageother-symbol)
• moving average.other symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Optional: `true`
- IsHidden: `false`

### moving average.plot.color[​](#moving-averageplotcolor)
• moving average.plot.color: `string`

Default value: `#2196F3`

### moving average.plot.display[​](#moving-averageplotdisplay)
• moving average.plot.display: `number`

Default value: `15`

### moving average.plot.linestyle[​](#moving-averageplotlinestyle)
• moving average.plot.linestyle: `number`

Default value: `0`

### moving average.plot.linewidth[​](#moving-averageplotlinewidth)
• moving average.plot.linewidth: `number`

Default value: `1`

### moving average.plot.plottype[​](#moving-averageplotplottype)
• moving average.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average.plot.trackprice[​](#moving-averageplottrackprice)
• moving average.plot.trackprice: `boolean`

Default value: `false`

### moving average.plot.transparency[​](#moving-averageplottransparency)
• moving average.plot.transparency: `number`

Default value: `0`

### moving average.smoothed ma.display[​](#moving-averagesmoothed-madisplay)
• moving average.smoothed ma.display: `number`

Default value: `0`

### moving average.smoothed ma.linestyle[​](#moving-averagesmoothed-malinestyle)
• moving average.smoothed ma.linestyle: `number`

Default value: `0`

### moving average.smoothed ma.linewidth[​](#moving-averagesmoothed-malinewidth)
• moving average.smoothed ma.linewidth: `number`

Default value: `1`

### moving average.smoothed ma.plottype[​](#moving-averagesmoothed-maplottype)
• moving average.smoothed ma.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### moving average.smoothed ma.trackprice[​](#moving-averagesmoothed-matrackprice)
• moving average.smoothed ma.trackprice: `boolean`

Default value: `false`

### moving average.smoothed ma.transparency[​](#moving-averagesmoothed-matransparency)
• moving average.smoothed ma.transparency: `number`

Default value: `0`

### moving average.smoothing length[​](#moving-averagesmoothing-length)
• moving average.smoothing length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### moving average.smoothing line[​](#moving-averagesmoothing-line)
• moving average.smoothing line: `string`

- Default value: `SMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### moving average.source[​](#moving-averagesource)
• moving average.source: `string`

- Default value: `close`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### net volume.plot.color[​](#net-volumeplotcolor)
• net volume.plot.color: `string`

Default value: `#2196F3`

### net volume.plot.display[​](#net-volumeplotdisplay)
• net volume.plot.display: `number`

Default value: `15`

### net volume.plot.linestyle[​](#net-volumeplotlinestyle)
• net volume.plot.linestyle: `number`

Default value: `0`

### net volume.plot.linewidth[​](#net-volumeplotlinewidth)
• net volume.plot.linewidth: `number`

Default value: `1`

### net volume.plot.plottype[​](#net-volumeplotplottype)
• net volume.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### net volume.plot.trackprice[​](#net-volumeplottrackprice)
• net volume.plot.trackprice: `boolean`

Default value: `false`

### net volume.plot.transparency[​](#net-volumeplottransparency)
• net volume.plot.transparency: `number`

Default value: `0`

### on balance volume.plot.color[​](#on-balance-volumeplotcolor)
• on balance volume.plot.color: `string`

Default value: `#2196F3`

### on balance volume.plot.display[​](#on-balance-volumeplotdisplay)
• on balance volume.plot.display: `number`

Default value: `15`

### on balance volume.plot.linestyle[​](#on-balance-volumeplotlinestyle)
• on balance volume.plot.linestyle: `number`

Default value: `0`

### on balance volume.plot.linewidth[​](#on-balance-volumeplotlinewidth)
• on balance volume.plot.linewidth: `number`

Default value: `1`

### on balance volume.plot.plottype[​](#on-balance-volumeplotplottype)
• on balance volume.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### on balance volume.plot.trackprice[​](#on-balance-volumeplottrackprice)
• on balance volume.plot.trackprice: `boolean`

Default value: `false`

### on balance volume.plot.transparency[​](#on-balance-volumeplottransparency)
• on balance volume.plot.transparency: `number`

Default value: `0`

### on balance volume.smoothed ma.display[​](#on-balance-volumesmoothed-madisplay)
• on balance volume.smoothed ma.display: `number`

Default value: `0`

### on balance volume.smoothed ma.linestyle[​](#on-balance-volumesmoothed-malinestyle)
• on balance volume.smoothed ma.linestyle: `number`

Default value: `0`

### on balance volume.smoothed ma.linewidth[​](#on-balance-volumesmoothed-malinewidth)
• on balance volume.smoothed ma.linewidth: `number`

Default value: `1`

### on balance volume.smoothed ma.plottype[​](#on-balance-volumesmoothed-maplottype)
• on balance volume.smoothed ma.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### on balance volume.smoothed ma.trackprice[​](#on-balance-volumesmoothed-matrackprice)
• on balance volume.smoothed ma.trackprice: `boolean`

Default value: `false`

### on balance volume.smoothed ma.transparency[​](#on-balance-volumesmoothed-matransparency)
• on balance volume.smoothed ma.transparency: `number`

Default value: `0`

### on balance volume.smoothing length[​](#on-balance-volumesmoothing-length)
• on balance volume.smoothing length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### on balance volume.smoothing line[​](#on-balance-volumesmoothing-line)
• on balance volume.smoothing line: `string`

- Default value: `SMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### overlay.extendtimescale[​](#overlayextendtimescale)
• overlay.extendtimescale: `boolean`

- Default value: `false`
- Input type: `boolean`
- IsHidden: `true`

### overlay.symbol[​](#overlaysymbol)
• overlay.symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- IsHidden: `true`

### parabolic sar.increment[​](#parabolic-sarincrement)
• parabolic sar.increment: `number`

- Default value: `0.02`
- Input type: `float`
- Min: `-1000000000000`
- Max: `1000000000000`

### parabolic sar.maximum[​](#parabolic-sarmaximum)
• parabolic sar.maximum: `number`

- Default value: `0.2`
- Input type: `float`
- Min: `-1000000000000`
- Max: `1000000000000`

### parabolic sar.other symbol[​](#parabolic-sarother-symbol)
• parabolic sar.other symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Optional: `true`
- IsHidden: `false`

### parabolic sar.plot.color[​](#parabolic-sarplotcolor)
• parabolic sar.plot.color: `string`

Default value: `#2196F3`

### parabolic sar.plot.display[​](#parabolic-sarplotdisplay)
• parabolic sar.plot.display: `number`

Default value: `15`

### parabolic sar.plot.linestyle[​](#parabolic-sarplotlinestyle)
• parabolic sar.plot.linestyle: `number`

Default value: `0`

### parabolic sar.plot.linewidth[​](#parabolic-sarplotlinewidth)
• parabolic sar.plot.linewidth: `number`

Default value: `1`

### parabolic sar.plot.plottype[​](#parabolic-sarplotplottype)
• parabolic sar.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `cross`

### parabolic sar.plot.trackprice[​](#parabolic-sarplottrackprice)
• parabolic sar.plot.trackprice: `boolean`

Default value: `false`

### parabolic sar.plot.transparency[​](#parabolic-sarplottransparency)
• parabolic sar.plot.transparency: `number`

Default value: `0`

### parabolic sar.start[​](#parabolic-sarstart)
• parabolic sar.start: `number`

- Default value: `0.02`
- Input type: `float`
- Min: `-1000000000000`
- Max: `1000000000000`

### pivot points standard.number of pivots back[​](#pivot-points-standardnumber-of-pivots-back)
• pivot points standard.number of pivots back: `number`

- Default value: `15`
- Input type: `integer`
- Max: `5000`
- Min: `1`

### pivot points standard.pivots timeframe[​](#pivot-points-standardpivots-timeframe)
• pivot points standard.pivots timeframe: `string`

- Default value: `Auto`
- Input type: `text`
- Options: `["Auto","Daily","Weekly","Monthly","Yearly"]`

### pivot points standard.show historical pivots[​](#pivot-points-standardshow-historical-pivots)
• pivot points standard.show historical pivots: `boolean`

- Default value: `true`
- Input type: `bool`

### pivot points standard.type[​](#pivot-points-standardtype)
• pivot points standard.type: `string`

- Default value: `Traditional`
- Input type: `text`
- Options: `["Traditional","Fibonacci","Woodie","Classic","DeMark","Camarilla","Floor"]`

### price channel.centerprice line.color[​](#price-channelcenterprice-linecolor)
• price channel.centerprice line.color: `string`

Default value: `#2196F3`

### price channel.centerprice line.display[​](#price-channelcenterprice-linedisplay)
• price channel.centerprice line.display: `number`

Default value: `15`

### price channel.centerprice line.linestyle[​](#price-channelcenterprice-linelinestyle)
• price channel.centerprice line.linestyle: `number`

Default value: `0`

### price channel.centerprice line.linewidth[​](#price-channelcenterprice-linelinewidth)
• price channel.centerprice line.linewidth: `number`

Default value: `1`

### price channel.centerprice line.plottype[​](#price-channelcenterprice-lineplottype)
• price channel.centerprice line.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### price channel.centerprice line.trackprice[​](#price-channelcenterprice-linetrackprice)
• price channel.centerprice line.trackprice: `boolean`

Default value: `false`

### price channel.centerprice line.transparency[​](#price-channelcenterprice-linetransparency)
• price channel.centerprice line.transparency: `number`

Default value: `0`

### price channel.highprice line.color[​](#price-channelhighprice-linecolor)
• price channel.highprice line.color: `string`

Default value: `#F50057`

### price channel.highprice line.display[​](#price-channelhighprice-linedisplay)
• price channel.highprice line.display: `number`

Default value: `15`

### price channel.highprice line.linestyle[​](#price-channelhighprice-linelinestyle)
• price channel.highprice line.linestyle: `number`

Default value: `0`

### price channel.highprice line.linewidth[​](#price-channelhighprice-linelinewidth)
• price channel.highprice line.linewidth: `number`

Default value: `1`

### price channel.highprice line.plottype[​](#price-channelhighprice-lineplottype)
• price channel.highprice line.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### price channel.highprice line.trackprice[​](#price-channelhighprice-linetrackprice)
• price channel.highprice line.trackprice: `boolean`

Default value: `false`

### price channel.highprice line.transparency[​](#price-channelhighprice-linetransparency)
• price channel.highprice line.transparency: `number`

Default value: `0`

### price channel.length[​](#price-channellength)
• price channel.length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### price channel.lowprice line.color[​](#price-channellowprice-linecolor)
• price channel.lowprice line.color: `string`

Default value: `#F50057`

### price channel.lowprice line.display[​](#price-channellowprice-linedisplay)
• price channel.lowprice line.display: `number`

Default value: `15`

### price channel.lowprice line.linestyle[​](#price-channellowprice-linelinestyle)
• price channel.lowprice line.linestyle: `number`

Default value: `0`

### price channel.lowprice line.linewidth[​](#price-channellowprice-linelinewidth)
• price channel.lowprice line.linewidth: `number`

Default value: `1`

### price channel.lowprice line.plottype[​](#price-channellowprice-lineplottype)
• price channel.lowprice line.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### price channel.lowprice line.trackprice[​](#price-channellowprice-linetrackprice)
• price channel.lowprice line.trackprice: `boolean`

Default value: `false`

### price channel.lowprice line.transparency[​](#price-channellowprice-linetransparency)
• price channel.lowprice line.transparency: `number`

Default value: `0`

### price channel.offset length[​](#price-channeloffset-length)
• price channel.offset length: `number`

- Default value: `0`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### price oscillator.longlen[​](#price-oscillatorlonglen)
• price oscillator.longlen: `number`

- Default value: `21`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### price oscillator.plot.color[​](#price-oscillatorplotcolor)
• price oscillator.plot.color: `string`

Default value: `#089981`

### price oscillator.plot.display[​](#price-oscillatorplotdisplay)
• price oscillator.plot.display: `number`

Default value: `15`

### price oscillator.plot.linestyle[​](#price-oscillatorplotlinestyle)
• price oscillator.plot.linestyle: `number`

Default value: `0`

### price oscillator.plot.linewidth[​](#price-oscillatorplotlinewidth)
• price oscillator.plot.linewidth: `number`

Default value: `1`

### price oscillator.plot.plottype[​](#price-oscillatorplotplottype)
• price oscillator.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### price oscillator.plot.trackprice[​](#price-oscillatorplottrackprice)
• price oscillator.plot.trackprice: `boolean`

Default value: `false`

### price oscillator.plot.transparency[​](#price-oscillatorplottransparency)
• price oscillator.plot.transparency: `number`

Default value: `0`

### price oscillator.shortlen[​](#price-oscillatorshortlen)
• price oscillator.shortlen: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### price volume trend.pvt.color[​](#price-volume-trendpvtcolor)
• price volume trend.pvt.color: `string`

Default value: `#2196F3`

### price volume trend.pvt.display[​](#price-volume-trendpvtdisplay)
• price volume trend.pvt.display: `number`

Default value: `15`

### price volume trend.pvt.linestyle[​](#price-volume-trendpvtlinestyle)
• price volume trend.pvt.linestyle: `number`

Default value: `0`

### price volume trend.pvt.linewidth[​](#price-volume-trendpvtlinewidth)
• price volume trend.pvt.linewidth: `number`

Default value: `1`

### price volume trend.pvt.plottype[​](#price-volume-trendpvtplottype)
• price volume trend.pvt.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### price volume trend.pvt.trackprice[​](#price-volume-trendpvttrackprice)
• price volume trend.pvt.trackprice: `boolean`

Default value: `false`

### price volume trend.pvt.transparency[​](#price-volume-trendpvttransparency)
• price volume trend.pvt.transparency: `number`

Default value: `0`

### rank correlation index.length[​](#rank-correlation-indexlength)
• rank correlation index.length: `number`

- Default value: `12`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### rank correlation index.rci.color[​](#rank-correlation-indexrcicolor)
• rank correlation index.rci.color: `string`

Default value: `#2196F3`

### rank correlation index.rci.display[​](#rank-correlation-indexrcidisplay)
• rank correlation index.rci.display: `number`

Default value: `15`

### rank correlation index.rci.linestyle[​](#rank-correlation-indexrcilinestyle)
• rank correlation index.rci.linestyle: `number`

Default value: `0`

### rank correlation index.rci.linewidth[​](#rank-correlation-indexrcilinewidth)
• rank correlation index.rci.linewidth: `number`

Default value: `1`

### rank correlation index.rci.plottype[​](#rank-correlation-indexrciplottype)
• rank correlation index.rci.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### rank correlation index.rci.trackprice[​](#rank-correlation-indexrcitrackprice)
• rank correlation index.rci.trackprice: `boolean`

Default value: `false`

### rank correlation index.rci.transparency[​](#rank-correlation-indexrcitransparency)
• rank correlation index.rci.transparency: `number`

Default value: `0`

### rank correlation index.zero line.color[​](#rank-correlation-indexzero-linecolor)
• rank correlation index.zero line.color: `string`

Default value: `#787B86`

### rank correlation index.zero line.linestyle[​](#rank-correlation-indexzero-linelinestyle)
• rank correlation index.zero line.linestyle: `number`

Default value: `2`

### rank correlation index.zero line.linewidth[​](#rank-correlation-indexzero-linelinewidth)
• rank correlation index.zero line.linewidth: `number`

Default value: `1`

### rank correlation index.zero line.value[​](#rank-correlation-indexzero-linevalue)
• rank correlation index.zero line.value: `number`

Default value: `0`

### rank correlation index.zero line.visible[​](#rank-correlation-indexzero-linevisible)
• rank correlation index.zero line.visible: `boolean`

Default value: `true`

### rate of change.length[​](#rate-of-changelength)
• rate of change.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### rate of change.roc.color[​](#rate-of-changeroccolor)
• rate of change.roc.color: `string`

Default value: `#2196F3`

### rate of change.roc.display[​](#rate-of-changerocdisplay)
• rate of change.roc.display: `number`

Default value: `15`

### rate of change.roc.linestyle[​](#rate-of-changeroclinestyle)
• rate of change.roc.linestyle: `number`

Default value: `0`

### rate of change.roc.linewidth[​](#rate-of-changeroclinewidth)
• rate of change.roc.linewidth: `number`

Default value: `1`

### rate of change.roc.plottype[​](#rate-of-changerocplottype)
• rate of change.roc.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### rate of change.roc.trackprice[​](#rate-of-changeroctrackprice)
• rate of change.roc.trackprice: `boolean`

Default value: `false`

### rate of change.roc.transparency[​](#rate-of-changeroctransparency)
• rate of change.roc.transparency: `number`

Default value: `0`

### rate of change.zero line.color[​](#rate-of-changezero-linecolor)
• rate of change.zero line.color: `string`

Default value: `#787B86`

### rate of change.zero line.linestyle[​](#rate-of-changezero-linelinestyle)
• rate of change.zero line.linestyle: `number`

Default value: `2`

### rate of change.zero line.linewidth[​](#rate-of-changezero-linelinewidth)
• rate of change.zero line.linewidth: `number`

Default value: `1`

### rate of change.zero line.value[​](#rate-of-changezero-linevalue)
• rate of change.zero line.value: `number`

Default value: `0`

### rate of change.zero line.visible[​](#rate-of-changezero-linevisible)
• rate of change.zero line.visible: `boolean`

Default value: `true`

### ratio.baseline.color[​](#ratiobaselinecolor)
• ratio.baseline.color: `string`

Default value: `rgba(0, 0, 0, 0)`

### ratio.baseline.display[​](#ratiobaselinedisplay)
• ratio.baseline.display: `number`

Default value: `0`

### ratio.baseline.linestyle[​](#ratiobaselinelinestyle)
• ratio.baseline.linestyle: `number`

Default value: `0`

### ratio.baseline.linewidth[​](#ratiobaselinelinewidth)
• ratio.baseline.linewidth: `number`

Default value: `2`

### ratio.baseline.plottype[​](#ratiobaselineplottype)
• ratio.baseline.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ratio.baseline.trackprice[​](#ratiobaselinetrackprice)
• ratio.baseline.trackprice: `boolean`

Default value: `false`

### ratio.baseline.transparency[​](#ratiobaselinetransparency)
• ratio.baseline.transparency: `number`

Default value: `0`

### ratio.negativefill.color[​](#rationegativefillcolor)
• ratio.negativefill.color: `string`

Default value: `undefined`

### ratio.negativefill.transparency[​](#rationegativefilltransparency)
• ratio.negativefill.transparency: `number`

Default value: `0`

### ratio.negativefill.visible[​](#rationegativefillvisible)
• ratio.negativefill.visible: `boolean`

Default value: `true`

### ratio.plot.color[​](#ratioplotcolor)
• ratio.plot.color: `string`

Default value: `#800080`

### ratio.plot.display[​](#ratioplotdisplay)
• ratio.plot.display: `number`

Default value: `15`

### ratio.plot.linestyle[​](#ratioplotlinestyle)
• ratio.plot.linestyle: `number`

Default value: `0`

### ratio.plot.linewidth[​](#ratioplotlinewidth)
• ratio.plot.linewidth: `number`

Default value: `2`

### ratio.plot.plottype[​](#ratioplotplottype)
• ratio.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ratio.plot.trackprice[​](#ratioplottrackprice)
• ratio.plot.trackprice: `boolean`

Default value: `false`

### ratio.plot.transparency[​](#ratioplottransparency)
• ratio.plot.transparency: `number`

Default value: `35`

### ratio.positivefill.color[​](#ratiopositivefillcolor)
• ratio.positivefill.color: `string`

Default value: `undefined`

### ratio.positivefill.transparency[​](#ratiopositivefilltransparency)
• ratio.positivefill.transparency: `number`

Default value: `0`

### ratio.positivefill.visible[​](#ratiopositivefillvisible)
• ratio.positivefill.visible: `boolean`

Default value: `true`

### ratio.source[​](#ratiosource)
• ratio.source: `string`

- Default value: `close`
- Input type: `text`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### ratio.symbol[​](#ratiosymbol)
• ratio.symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Confirm: `true`

### regression trend.first bar time[​](#regression-trendfirst-bar-time)
• regression trend.first bar time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `253370764800`
- Min: `-253370764800`

### regression trend.last bar time[​](#regression-trendlast-bar-time)
• regression trend.last bar time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `253370764800`
- Min: `-253370764800`

### regression trend.lower deviation[​](#regression-trendlower-deviation)
• regression trend.lower deviation: `number`

- Default value: `-2`
- Input type: `float`
- Max: `500`
- Min: `-500`

### regression trend.source[​](#regression-trendsource)
• regression trend.source: `string`

- Default value: `close`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### regression trend.upper deviation[​](#regression-trendupper-deviation)
• regression trend.upper deviation: `number`

- Default value: `2`
- Input type: `float`
- Max: `500`
- Min: `-500`

### regression trend.use lower deviation[​](#regression-trenduse-lower-deviation)
• regression trend.use lower deviation: `boolean`

- Default value: `true`
- Input type: `bool`

### regression trend.use upper deviation[​](#regression-trenduse-upper-deviation)
• regression trend.use upper deviation: `boolean`

- Default value: `true`
- Input type: `bool`

### relative strength index.hlines background.color[​](#relative-strength-indexhlines-backgroundcolor)
• relative strength index.hlines background.color: `string`

Default value: `#7E57C2`

### relative strength index.hlines background.transparency[​](#relative-strength-indexhlines-backgroundtransparency)
• relative strength index.hlines background.transparency: `number`

Default value: `90`

### relative strength index.hlines background.visible[​](#relative-strength-indexhlines-backgroundvisible)
• relative strength index.hlines background.visible: `boolean`

Default value: `true`

### relative strength index.length[​](#relative-strength-indexlength)
• relative strength index.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### relative strength index.lowerlimit.color[​](#relative-strength-indexlowerlimitcolor)
• relative strength index.lowerlimit.color: `string`

Default value: `#787B86`

### relative strength index.lowerlimit.linestyle[​](#relative-strength-indexlowerlimitlinestyle)
• relative strength index.lowerlimit.linestyle: `number`

Default value: `2`

### relative strength index.lowerlimit.linewidth[​](#relative-strength-indexlowerlimitlinewidth)
• relative strength index.lowerlimit.linewidth: `number`

Default value: `1`

### relative strength index.lowerlimit.value[​](#relative-strength-indexlowerlimitvalue)
• relative strength index.lowerlimit.value: `number`

Default value: `30`

### relative strength index.lowerlimit.visible[​](#relative-strength-indexlowerlimitvisible)
• relative strength index.lowerlimit.visible: `boolean`

Default value: `true`

### relative strength index.lowerlimit.zorder[​](#relative-strength-indexlowerlimitzorder)
• relative strength index.lowerlimit.zorder: `number`

Default value: `-1.111`

### relative strength index.middlelimit.color[​](#relative-strength-indexmiddlelimitcolor)
• relative strength index.middlelimit.color: `string`

Default value: `#787B86`

### relative strength index.middlelimit.linestyle[​](#relative-strength-indexmiddlelimitlinestyle)
• relative strength index.middlelimit.linestyle: `number`

Default value: `2`

### relative strength index.middlelimit.linewidth[​](#relative-strength-indexmiddlelimitlinewidth)
• relative strength index.middlelimit.linewidth: `number`

Default value: `1`

### relative strength index.middlelimit.value[​](#relative-strength-indexmiddlelimitvalue)
• relative strength index.middlelimit.value: `number`

Default value: `50`

### relative strength index.middlelimit.visible[​](#relative-strength-indexmiddlelimitvisible)
• relative strength index.middlelimit.visible: `boolean`

Default value: `true`

### relative strength index.middlelimit.zorder[​](#relative-strength-indexmiddlelimitzorder)
• relative strength index.middlelimit.zorder: `number`

Default value: `-1.11`

### relative strength index.plot.color[​](#relative-strength-indexplotcolor)
• relative strength index.plot.color: `string`

Default value: `#7E57C2`

### relative strength index.plot.display[​](#relative-strength-indexplotdisplay)
• relative strength index.plot.display: `number`

Default value: `15`

### relative strength index.plot.linestyle[​](#relative-strength-indexplotlinestyle)
• relative strength index.plot.linestyle: `number`

Default value: `0`

### relative strength index.plot.linewidth[​](#relative-strength-indexplotlinewidth)
• relative strength index.plot.linewidth: `number`

Default value: `1`

### relative strength index.plot.plottype[​](#relative-strength-indexplotplottype)
• relative strength index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### relative strength index.plot.trackprice[​](#relative-strength-indexplottrackprice)
• relative strength index.plot.trackprice: `boolean`

Default value: `false`

### relative strength index.plot.transparency[​](#relative-strength-indexplottransparency)
• relative strength index.plot.transparency: `number`

Default value: `0`

### relative strength index.smoothed ma.display[​](#relative-strength-indexsmoothed-madisplay)
• relative strength index.smoothed ma.display: `number`

Default value: `0`

### relative strength index.smoothed ma.linestyle[​](#relative-strength-indexsmoothed-malinestyle)
• relative strength index.smoothed ma.linestyle: `number`

Default value: `0`

### relative strength index.smoothed ma.linewidth[​](#relative-strength-indexsmoothed-malinewidth)
• relative strength index.smoothed ma.linewidth: `number`

Default value: `1`

### relative strength index.smoothed ma.plottype[​](#relative-strength-indexsmoothed-maplottype)
• relative strength index.smoothed ma.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### relative strength index.smoothed ma.trackprice[​](#relative-strength-indexsmoothed-matrackprice)
• relative strength index.smoothed ma.trackprice: `boolean`

Default value: `false`

### relative strength index.smoothed ma.transparency[​](#relative-strength-indexsmoothed-matransparency)
• relative strength index.smoothed ma.transparency: `number`

Default value: `0`

### relative strength index.smoothing length[​](#relative-strength-indexsmoothing-length)
• relative strength index.smoothing length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### relative strength index.smoothing line[​](#relative-strength-indexsmoothing-line)
• relative strength index.smoothing line: `string`

- Default value: `SMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### relative strength index.upperlimit.color[​](#relative-strength-indexupperlimitcolor)
• relative strength index.upperlimit.color: `string`

Default value: `#787B86`

### relative strength index.upperlimit.linestyle[​](#relative-strength-indexupperlimitlinestyle)
• relative strength index.upperlimit.linestyle: `number`

Default value: `2`

### relative strength index.upperlimit.linewidth[​](#relative-strength-indexupperlimitlinewidth)
• relative strength index.upperlimit.linewidth: `number`

Default value: `1`

### relative strength index.upperlimit.value[​](#relative-strength-indexupperlimitvalue)
• relative strength index.upperlimit.value: `number`

Default value: `70`

### relative strength index.upperlimit.visible[​](#relative-strength-indexupperlimitvisible)
• relative strength index.upperlimit.visible: `boolean`

Default value: `true`

### relative strength index.upperlimit.zorder[​](#relative-strength-indexupperlimitzorder)
• relative strength index.upperlimit.zorder: `number`

Default value: `-1.1`

### relative vigor index.length[​](#relative-vigor-indexlength)
• relative vigor index.length: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### relative vigor index.rvgi.color[​](#relative-vigor-indexrvgicolor)
• relative vigor index.rvgi.color: `string`

Default value: `#089981`

### relative vigor index.rvgi.display[​](#relative-vigor-indexrvgidisplay)
• relative vigor index.rvgi.display: `number`

Default value: `15`

### relative vigor index.rvgi.linestyle[​](#relative-vigor-indexrvgilinestyle)
• relative vigor index.rvgi.linestyle: `number`

Default value: `0`

### relative vigor index.rvgi.linewidth[​](#relative-vigor-indexrvgilinewidth)
• relative vigor index.rvgi.linewidth: `number`

Default value: `1`

### relative vigor index.rvgi.plottype[​](#relative-vigor-indexrvgiplottype)
• relative vigor index.rvgi.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### relative vigor index.rvgi.trackprice[​](#relative-vigor-indexrvgitrackprice)
• relative vigor index.rvgi.trackprice: `boolean`

Default value: `false`

### relative vigor index.rvgi.transparency[​](#relative-vigor-indexrvgitransparency)
• relative vigor index.rvgi.transparency: `number`

Default value: `0`

### relative vigor index.signal.color[​](#relative-vigor-indexsignalcolor)
• relative vigor index.signal.color: `string`

Default value: `#F23645`

### relative vigor index.signal.display[​](#relative-vigor-indexsignaldisplay)
• relative vigor index.signal.display: `number`

Default value: `15`

### relative vigor index.signal.linestyle[​](#relative-vigor-indexsignallinestyle)
• relative vigor index.signal.linestyle: `number`

Default value: `0`

### relative vigor index.signal.linewidth[​](#relative-vigor-indexsignallinewidth)
• relative vigor index.signal.linewidth: `number`

Default value: `1`

### relative vigor index.signal.plottype[​](#relative-vigor-indexsignalplottype)
• relative vigor index.signal.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### relative vigor index.signal.trackprice[​](#relative-vigor-indexsignaltrackprice)
• relative vigor index.signal.trackprice: `boolean`

Default value: `false`

### relative vigor index.signal.transparency[​](#relative-vigor-indexsignaltransparency)
• relative vigor index.signal.transparency: `number`

Default value: `0`

### relative volatility index.hlines background.color[​](#relative-volatility-indexhlines-backgroundcolor)
• relative volatility index.hlines background.color: `string`

Default value: `#7E57C2`

### relative volatility index.hlines background.transparency[​](#relative-volatility-indexhlines-backgroundtransparency)
• relative volatility index.hlines background.transparency: `number`

Default value: `90`

### relative volatility index.hlines background.visible[​](#relative-volatility-indexhlines-backgroundvisible)
• relative volatility index.hlines background.visible: `boolean`

Default value: `true`

### relative volatility index.length[​](#relative-volatility-indexlength)
• relative volatility index.length: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### relative volatility index.lowerlimit.color[​](#relative-volatility-indexlowerlimitcolor)
• relative volatility index.lowerlimit.color: `string`

Default value: `#787B86`

### relative volatility index.lowerlimit.linestyle[​](#relative-volatility-indexlowerlimitlinestyle)
• relative volatility index.lowerlimit.linestyle: `number`

Default value: `2`

### relative volatility index.lowerlimit.linewidth[​](#relative-volatility-indexlowerlimitlinewidth)
• relative volatility index.lowerlimit.linewidth: `number`

Default value: `1`

### relative volatility index.lowerlimit.value[​](#relative-volatility-indexlowerlimitvalue)
• relative volatility index.lowerlimit.value: `number`

Default value: `20`

### relative volatility index.lowerlimit.visible[​](#relative-volatility-indexlowerlimitvisible)
• relative volatility index.lowerlimit.visible: `boolean`

Default value: `true`

### relative volatility index.plot.color[​](#relative-volatility-indexplotcolor)
• relative volatility index.plot.color: `string`

Default value: `#7E57C2`

### relative volatility index.plot.display[​](#relative-volatility-indexplotdisplay)
• relative volatility index.plot.display: `number`

Default value: `15`

### relative volatility index.plot.linestyle[​](#relative-volatility-indexplotlinestyle)
• relative volatility index.plot.linestyle: `number`

Default value: `0`

### relative volatility index.plot.linewidth[​](#relative-volatility-indexplotlinewidth)
• relative volatility index.plot.linewidth: `number`

Default value: `1`

### relative volatility index.plot.plottype[​](#relative-volatility-indexplotplottype)
• relative volatility index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### relative volatility index.plot.trackprice[​](#relative-volatility-indexplottrackprice)
• relative volatility index.plot.trackprice: `boolean`

Default value: `false`

### relative volatility index.plot.transparency[​](#relative-volatility-indexplottransparency)
• relative volatility index.plot.transparency: `number`

Default value: `0`

### relative volatility index.upperlimit.color[​](#relative-volatility-indexupperlimitcolor)
• relative volatility index.upperlimit.color: `string`

Default value: `#787B86`

### relative volatility index.upperlimit.linestyle[​](#relative-volatility-indexupperlimitlinestyle)
• relative volatility index.upperlimit.linestyle: `number`

Default value: `2`

### relative volatility index.upperlimit.linewidth[​](#relative-volatility-indexupperlimitlinewidth)
• relative volatility index.upperlimit.linewidth: `number`

Default value: `1`

### relative volatility index.upperlimit.value[​](#relative-volatility-indexupperlimitvalue)
• relative volatility index.upperlimit.value: `number`

Default value: `80`

### relative volatility index.upperlimit.visible[​](#relative-volatility-indexupperlimitvisible)
• relative volatility index.upperlimit.visible: `boolean`

Default value: `true`

### smi ergodic indicator/oscillator.indicator.color[​](#smi-ergodic-indicatoroscillatorindicatorcolor)
• smi ergodic indicator/oscillator.indicator.color: `string`

Default value: `#2196F3`

### smi ergodic indicator/oscillator.indicator.display[​](#smi-ergodic-indicatoroscillatorindicatordisplay)
• smi ergodic indicator/oscillator.indicator.display: `number`

Default value: `15`

### smi ergodic indicator/oscillator.indicator.linestyle[​](#smi-ergodic-indicatoroscillatorindicatorlinestyle)
• smi ergodic indicator/oscillator.indicator.linestyle: `number`

Default value: `0`

### smi ergodic indicator/oscillator.indicator.linewidth[​](#smi-ergodic-indicatoroscillatorindicatorlinewidth)
• smi ergodic indicator/oscillator.indicator.linewidth: `number`

Default value: `1`

### smi ergodic indicator/oscillator.indicator.plottype[​](#smi-ergodic-indicatoroscillatorindicatorplottype)
• smi ergodic indicator/oscillator.indicator.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### smi ergodic indicator/oscillator.indicator.trackprice[​](#smi-ergodic-indicatoroscillatorindicatortrackprice)
• smi ergodic indicator/oscillator.indicator.trackprice: `boolean`

Default value: `false`

### smi ergodic indicator/oscillator.indicator.transparency[​](#smi-ergodic-indicatoroscillatorindicatortransparency)
• smi ergodic indicator/oscillator.indicator.transparency: `number`

Default value: `0`

### smi ergodic indicator/oscillator.longlen[​](#smi-ergodic-indicatoroscillatorlonglen)
• smi ergodic indicator/oscillator.longlen: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### smi ergodic indicator/oscillator.oscillator.color[​](#smi-ergodic-indicatoroscillatoroscillatorcolor)
• smi ergodic indicator/oscillator.oscillator.color: `string`

Default value: `#FF5252`

### smi ergodic indicator/oscillator.oscillator.display[​](#smi-ergodic-indicatoroscillatoroscillatordisplay)
• smi ergodic indicator/oscillator.oscillator.display: `number`

Default value: `15`

### smi ergodic indicator/oscillator.oscillator.linestyle[​](#smi-ergodic-indicatoroscillatoroscillatorlinestyle)
• smi ergodic indicator/oscillator.oscillator.linestyle: `number`

Default value: `0`

### smi ergodic indicator/oscillator.oscillator.linewidth[​](#smi-ergodic-indicatoroscillatoroscillatorlinewidth)
• smi ergodic indicator/oscillator.oscillator.linewidth: `number`

Default value: `1`

### smi ergodic indicator/oscillator.oscillator.plottype[​](#smi-ergodic-indicatoroscillatoroscillatorplottype)
• smi ergodic indicator/oscillator.oscillator.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `histogram`

### smi ergodic indicator/oscillator.oscillator.trackprice[​](#smi-ergodic-indicatoroscillatoroscillatortrackprice)
• smi ergodic indicator/oscillator.oscillator.trackprice: `boolean`

Default value: `false`

### smi ergodic indicator/oscillator.oscillator.transparency[​](#smi-ergodic-indicatoroscillatoroscillatortransparency)
• smi ergodic indicator/oscillator.oscillator.transparency: `number`

Default value: `0`

### smi ergodic indicator/oscillator.shortlen[​](#smi-ergodic-indicatoroscillatorshortlen)
• smi ergodic indicator/oscillator.shortlen: `number`

- Default value: `5`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### smi ergodic indicator/oscillator.siglen[​](#smi-ergodic-indicatoroscillatorsiglen)
• smi ergodic indicator/oscillator.siglen: `number`

- Default value: `5`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### smi ergodic indicator/oscillator.signal.color[​](#smi-ergodic-indicatoroscillatorsignalcolor)
• smi ergodic indicator/oscillator.signal.color: `string`

Default value: `#FF6D00`

### smi ergodic indicator/oscillator.signal.display[​](#smi-ergodic-indicatoroscillatorsignaldisplay)
• smi ergodic indicator/oscillator.signal.display: `number`

Default value: `15`

### smi ergodic indicator/oscillator.signal.linestyle[​](#smi-ergodic-indicatoroscillatorsignallinestyle)
• smi ergodic indicator/oscillator.signal.linestyle: `number`

Default value: `0`

### smi ergodic indicator/oscillator.signal.linewidth[​](#smi-ergodic-indicatoroscillatorsignallinewidth)
• smi ergodic indicator/oscillator.signal.linewidth: `number`

Default value: `1`

### smi ergodic indicator/oscillator.signal.plottype[​](#smi-ergodic-indicatoroscillatorsignalplottype)
• smi ergodic indicator/oscillator.signal.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### smi ergodic indicator/oscillator.signal.trackprice[​](#smi-ergodic-indicatoroscillatorsignaltrackprice)
• smi ergodic indicator/oscillator.signal.trackprice: `boolean`

Default value: `false`

### smi ergodic indicator/oscillator.signal.transparency[​](#smi-ergodic-indicatoroscillatorsignaltransparency)
• smi ergodic indicator/oscillator.signal.transparency: `number`

Default value: `0`

### smoothed moving average.length[​](#smoothed-moving-averagelength)
• smoothed moving average.length: `number`

- Default value: `7`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### smoothed moving average.plot.color[​](#smoothed-moving-averageplotcolor)
• smoothed moving average.plot.color: `string`

Default value: `#673AB7`

### smoothed moving average.plot.display[​](#smoothed-moving-averageplotdisplay)
• smoothed moving average.plot.display: `number`

Default value: `15`

### smoothed moving average.plot.linestyle[​](#smoothed-moving-averageplotlinestyle)
• smoothed moving average.plot.linestyle: `number`

Default value: `0`

### smoothed moving average.plot.linewidth[​](#smoothed-moving-averageplotlinewidth)
• smoothed moving average.plot.linewidth: `number`

Default value: `1`

### smoothed moving average.plot.plottype[​](#smoothed-moving-averageplotplottype)
• smoothed moving average.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### smoothed moving average.plot.trackprice[​](#smoothed-moving-averageplottrackprice)
• smoothed moving average.plot.trackprice: `boolean`

Default value: `false`

### smoothed moving average.plot.transparency[​](#smoothed-moving-averageplottransparency)
• smoothed moving average.plot.transparency: `number`

Default value: `0`

### smoothed moving average.source[​](#smoothed-moving-averagesource)
• smoothed moving average.source: `string`

- Default value: `close`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### spread.baseline.color[​](#spreadbaselinecolor)
• spread.baseline.color: `string`

Default value: `rgba(0, 0, 0, 0)`

### spread.baseline.display[​](#spreadbaselinedisplay)
• spread.baseline.display: `number`

Default value: `0`

### spread.baseline.linestyle[​](#spreadbaselinelinestyle)
• spread.baseline.linestyle: `number`

Default value: `0`

### spread.baseline.linewidth[​](#spreadbaselinelinewidth)
• spread.baseline.linewidth: `number`

Default value: `2`

### spread.baseline.plottype[​](#spreadbaselineplottype)
• spread.baseline.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### spread.baseline.trackprice[​](#spreadbaselinetrackprice)
• spread.baseline.trackprice: `boolean`

Default value: `false`

### spread.baseline.transparency[​](#spreadbaselinetransparency)
• spread.baseline.transparency: `number`

Default value: `0`

### spread.negative fill.color[​](#spreadnegative-fillcolor)
• spread.negative fill.color: `string`

Default value: `undefined`

### spread.negative fill.transparency[​](#spreadnegative-filltransparency)
• spread.negative fill.transparency: `number`

Default value: `0`

### spread.negative fill.visible[​](#spreadnegative-fillvisible)
• spread.negative fill.visible: `boolean`

Default value: `true`

### spread.plot.color[​](#spreadplotcolor)
• spread.plot.color: `string`

Default value: `#800080`

### spread.plot.display[​](#spreadplotdisplay)
• spread.plot.display: `number`

Default value: `15`

### spread.plot.linestyle[​](#spreadplotlinestyle)
• spread.plot.linestyle: `number`

Default value: `0`

### spread.plot.linewidth[​](#spreadplotlinewidth)
• spread.plot.linewidth: `number`

Default value: `2`

### spread.plot.plottype[​](#spreadplotplottype)
• spread.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### spread.plot.trackprice[​](#spreadplottrackprice)
• spread.plot.trackprice: `boolean`

Default value: `false`

### spread.plot.transparency[​](#spreadplottransparency)
• spread.plot.transparency: `number`

Default value: `35`

### spread.positive fill.color[​](#spreadpositive-fillcolor)
• spread.positive fill.color: `string`

Default value: `undefined`

### spread.positive fill.transparency[​](#spreadpositive-filltransparency)
• spread.positive fill.transparency: `number`

Default value: `0`

### spread.positive fill.visible[​](#spreadpositive-fillvisible)
• spread.positive fill.visible: `boolean`

Default value: `true`

### spread.source[​](#spreadsource)
• spread.source: `string`

- Default value: `close`
- Input type: `text`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### spread.symbol[​](#spreadsymbol)
• spread.symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Confirm: `true`

### standard deviation.deviations[​](#standard-deviationdeviations)
• standard deviation.deviations: `number`

- Default value: `1`
- Input type: `float`

### standard deviation.periods[​](#standard-deviationperiods)
• standard deviation.periods: `number`

- Default value: `5`
- Input type: `integer`

### standard deviation.plot.color[​](#standard-deviationplotcolor)
• standard deviation.plot.color: `string`

Default value: `#089981`

### standard deviation.plot.display[​](#standard-deviationplotdisplay)
• standard deviation.plot.display: `number`

Default value: `15`

### standard deviation.plot.linestyle[​](#standard-deviationplotlinestyle)
• standard deviation.plot.linestyle: `number`

Default value: `0`

### standard deviation.plot.linewidth[​](#standard-deviationplotlinewidth)
• standard deviation.plot.linewidth: `number`

Default value: `1`

### standard deviation.plot.plottype[​](#standard-deviationplotplottype)
• standard deviation.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### standard deviation.plot.trackprice[​](#standard-deviationplottrackprice)
• standard deviation.plot.trackprice: `boolean`

Default value: `false`

### standard deviation.plot.transparency[​](#standard-deviationplottransparency)
• standard deviation.plot.transparency: `number`

Default value: `0`

### standard error bands.averaging periods[​](#standard-error-bandsaveraging-periods)
• standard error bands.averaging periods: `number`

- Default value: `3`
- Input type: `integer`

### standard error bands.background.color[​](#standard-error-bandsbackgroundcolor)
• standard error bands.background.color: `string`

Default value: `#2196F3`

### standard error bands.background.transparency[​](#standard-error-bandsbackgroundtransparency)
• standard error bands.background.transparency: `number`

Default value: `95`

### standard error bands.background.visible[​](#standard-error-bandsbackgroundvisible)
• standard error bands.background.visible: `boolean`

Default value: `true`

### standard error bands.method[​](#standard-error-bandsmethod)
• standard error bands.method: `string`

- Default value: `Simple`
- Input type: `text`
- Options: `["Simple","Exponential","Weighted"]`

### standard error bands.periods[​](#standard-error-bandsperiods)
• standard error bands.periods: `number`

- Default value: `21`
- Input type: `integer`

### standard error bands.plot 1.color[​](#standard-error-bandsplot-1color)
• standard error bands.plot 1.color: `string`

Default value: `#2196F3`

### standard error bands.plot 1.display[​](#standard-error-bandsplot-1display)
• standard error bands.plot 1.display: `number`

Default value: `15`

### standard error bands.plot 1.linestyle[​](#standard-error-bandsplot-1linestyle)
• standard error bands.plot 1.linestyle: `number`

Default value: `0`

### standard error bands.plot 1.linewidth[​](#standard-error-bandsplot-1linewidth)
• standard error bands.plot 1.linewidth: `number`

Default value: `1`

### standard error bands.plot 1.plottype[​](#standard-error-bandsplot-1plottype)
• standard error bands.plot 1.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### standard error bands.plot 1.trackprice[​](#standard-error-bandsplot-1trackprice)
• standard error bands.plot 1.trackprice: `boolean`

Default value: `false`

### standard error bands.plot 1.transparency[​](#standard-error-bandsplot-1transparency)
• standard error bands.plot 1.transparency: `number`

Default value: `0`

### standard error bands.plot 2.color[​](#standard-error-bandsplot-2color)
• standard error bands.plot 2.color: `string`

Default value: `#FF6D00`

### standard error bands.plot 2.display[​](#standard-error-bandsplot-2display)
• standard error bands.plot 2.display: `number`

Default value: `15`

### standard error bands.plot 2.linestyle[​](#standard-error-bandsplot-2linestyle)
• standard error bands.plot 2.linestyle: `number`

Default value: `0`

### standard error bands.plot 2.linewidth[​](#standard-error-bandsplot-2linewidth)
• standard error bands.plot 2.linewidth: `number`

Default value: `1`

### standard error bands.plot 2.plottype[​](#standard-error-bandsplot-2plottype)
• standard error bands.plot 2.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### standard error bands.plot 2.trackprice[​](#standard-error-bandsplot-2trackprice)
• standard error bands.plot 2.trackprice: `boolean`

Default value: `false`

### standard error bands.plot 2.transparency[​](#standard-error-bandsplot-2transparency)
• standard error bands.plot 2.transparency: `number`

Default value: `0`

### standard error bands.plot 3.color[​](#standard-error-bandsplot-3color)
• standard error bands.plot 3.color: `string`

Default value: `#2196F3`

### standard error bands.plot 3.display[​](#standard-error-bandsplot-3display)
• standard error bands.plot 3.display: `number`

Default value: `15`

### standard error bands.plot 3.linestyle[​](#standard-error-bandsplot-3linestyle)
• standard error bands.plot 3.linestyle: `number`

Default value: `0`

### standard error bands.plot 3.linewidth[​](#standard-error-bandsplot-3linewidth)
• standard error bands.plot 3.linewidth: `number`

Default value: `1`

### standard error bands.plot 3.plottype[​](#standard-error-bandsplot-3plottype)
• standard error bands.plot 3.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### standard error bands.plot 3.trackprice[​](#standard-error-bandsplot-3trackprice)
• standard error bands.plot 3.trackprice: `boolean`

Default value: `false`

### standard error bands.plot 3.transparency[​](#standard-error-bandsplot-3transparency)
• standard error bands.plot 3.transparency: `number`

Default value: `0`

### standard error bands.standard errors[​](#standard-error-bandsstandard-errors)
• standard error bands.standard errors: `number`

- Default value: `2`
- Input type: `float`

### standard error.length[​](#standard-errorlength)
• standard error.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `3`

### standard error.plot.color[​](#standard-errorplotcolor)
• standard error.plot.color: `string`

Default value: `#FF6D00`

### standard error.plot.display[​](#standard-errorplotdisplay)
• standard error.plot.display: `number`

Default value: `15`

### standard error.plot.linestyle[​](#standard-errorplotlinestyle)
• standard error.plot.linestyle: `number`

Default value: `0`

### standard error.plot.linewidth[​](#standard-errorplotlinewidth)
• standard error.plot.linewidth: `number`

Default value: `1`

### standard error.plot.plottype[​](#standard-errorplotplottype)
• standard error.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### standard error.plot.trackprice[​](#standard-errorplottrackprice)
• standard error.plot.trackprice: `boolean`

Default value: `false`

### standard error.plot.transparency[​](#standard-errorplottransparency)
• standard error.plot.transparency: `number`

Default value: `0`

### stochastic rsi.%d.color[​](#stochastic-rsidcolor)
• stochastic rsi.%d.color: `string`

Default value: `#FF6D00`

### stochastic rsi.%d.display[​](#stochastic-rsiddisplay)
• stochastic rsi.%d.display: `number`

Default value: `15`

### stochastic rsi.%d.linestyle[​](#stochastic-rsidlinestyle)
• stochastic rsi.%d.linestyle: `number`

Default value: `0`

### stochastic rsi.%d.linewidth[​](#stochastic-rsidlinewidth)
• stochastic rsi.%d.linewidth: `number`

Default value: `1`

### stochastic rsi.%d.plottype[​](#stochastic-rsidplottype)
• stochastic rsi.%d.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### stochastic rsi.%d.trackprice[​](#stochastic-rsidtrackprice)
• stochastic rsi.%d.trackprice: `boolean`

Default value: `false`

### stochastic rsi.%d.transparency[​](#stochastic-rsidtransparency)
• stochastic rsi.%d.transparency: `number`

Default value: `0`

### stochastic rsi.%k.color[​](#stochastic-rsikcolor)
• stochastic rsi.%k.color: `string`

Default value: `#2196F3`

### stochastic rsi.%k.display[​](#stochastic-rsikdisplay)
• stochastic rsi.%k.display: `number`

Default value: `15`

### stochastic rsi.%k.linestyle[​](#stochastic-rsiklinestyle)
• stochastic rsi.%k.linestyle: `number`

Default value: `0`

### stochastic rsi.%k.linewidth[​](#stochastic-rsiklinewidth)
• stochastic rsi.%k.linewidth: `number`

Default value: `1`

### stochastic rsi.%k.plottype[​](#stochastic-rsikplottype)
• stochastic rsi.%k.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### stochastic rsi.%k.trackprice[​](#stochastic-rsiktrackprice)
• stochastic rsi.%k.trackprice: `boolean`

Default value: `false`

### stochastic rsi.%k.transparency[​](#stochastic-rsiktransparency)
• stochastic rsi.%k.transparency: `number`

Default value: `0`

### stochastic rsi.hlines background.color[​](#stochastic-rsihlines-backgroundcolor)
• stochastic rsi.hlines background.color: `string`

Default value: `#2196F3`

### stochastic rsi.hlines background.transparency[​](#stochastic-rsihlines-backgroundtransparency)
• stochastic rsi.hlines background.transparency: `number`

Default value: `90`

### stochastic rsi.hlines background.visible[​](#stochastic-rsihlines-backgroundvisible)
• stochastic rsi.hlines background.visible: `boolean`

Default value: `true`

### stochastic rsi.lengthrsi[​](#stochastic-rsilengthrsi)
• stochastic rsi.lengthrsi: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### stochastic rsi.lengthstoch[​](#stochastic-rsilengthstoch)
• stochastic rsi.lengthstoch: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### stochastic rsi.lowerlimit.color[​](#stochastic-rsilowerlimitcolor)
• stochastic rsi.lowerlimit.color: `string`

Default value: `#787B86`

### stochastic rsi.lowerlimit.linestyle[​](#stochastic-rsilowerlimitlinestyle)
• stochastic rsi.lowerlimit.linestyle: `number`

Default value: `2`

### stochastic rsi.lowerlimit.linewidth[​](#stochastic-rsilowerlimitlinewidth)
• stochastic rsi.lowerlimit.linewidth: `number`

Default value: `1`

### stochastic rsi.lowerlimit.value[​](#stochastic-rsilowerlimitvalue)
• stochastic rsi.lowerlimit.value: `number`

Default value: `20`

### stochastic rsi.lowerlimit.visible[​](#stochastic-rsilowerlimitvisible)
• stochastic rsi.lowerlimit.visible: `boolean`

Default value: `true`

### stochastic rsi.smoothd[​](#stochastic-rsismoothd)
• stochastic rsi.smoothd: `number`

- Default value: `3`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### stochastic rsi.smoothk[​](#stochastic-rsismoothk)
• stochastic rsi.smoothk: `number`

- Default value: `3`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### stochastic rsi.upperlimit.color[​](#stochastic-rsiupperlimitcolor)
• stochastic rsi.upperlimit.color: `string`

Default value: `#787B86`

### stochastic rsi.upperlimit.linestyle[​](#stochastic-rsiupperlimitlinestyle)
• stochastic rsi.upperlimit.linestyle: `number`

Default value: `2`

### stochastic rsi.upperlimit.linewidth[​](#stochastic-rsiupperlimitlinewidth)
• stochastic rsi.upperlimit.linewidth: `number`

Default value: `1`

### stochastic rsi.upperlimit.value[​](#stochastic-rsiupperlimitvalue)
• stochastic rsi.upperlimit.value: `number`

Default value: `80`

### stochastic rsi.upperlimit.visible[​](#stochastic-rsiupperlimitvisible)
• stochastic rsi.upperlimit.visible: `boolean`

Default value: `true`

### stochastic.%d smoothing[​](#stochasticd-smoothing)
• stochastic.%d smoothing: `number`

- Default value: `3`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### stochastic.%d.color[​](#stochasticdcolor)
• stochastic.%d.color: `string`

Default value: `#FF6D00`

### stochastic.%d.display[​](#stochasticddisplay)
• stochastic.%d.display: `number`

Default value: `15`

### stochastic.%d.linestyle[​](#stochasticdlinestyle)
• stochastic.%d.linestyle: `number`

Default value: `0`

### stochastic.%d.linewidth[​](#stochasticdlinewidth)
• stochastic.%d.linewidth: `number`

Default value: `1`

### stochastic.%d.plottype[​](#stochasticdplottype)
• stochastic.%d.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### stochastic.%d.trackprice[​](#stochasticdtrackprice)
• stochastic.%d.trackprice: `boolean`

Default value: `false`

### stochastic.%d.transparency[​](#stochasticdtransparency)
• stochastic.%d.transparency: `number`

Default value: `0`

### stochastic.%k length[​](#stochastick-length)
• stochastic.%k length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### stochastic.%k smoothing[​](#stochastick-smoothing)
• stochastic.%k smoothing: `number`

- Default value: `1`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### stochastic.%k.color[​](#stochastickcolor)
• stochastic.%k.color: `string`

Default value: `#2196F3`

### stochastic.%k.display[​](#stochastickdisplay)
• stochastic.%k.display: `number`

Default value: `15`

### stochastic.%k.linestyle[​](#stochasticklinestyle)
• stochastic.%k.linestyle: `number`

Default value: `0`

### stochastic.%k.linewidth[​](#stochasticklinewidth)
• stochastic.%k.linewidth: `number`

Default value: `1`

### stochastic.%k.plottype[​](#stochastickplottype)
• stochastic.%k.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### stochastic.%k.trackprice[​](#stochasticktrackprice)
• stochastic.%k.trackprice: `boolean`

Default value: `false`

### stochastic.%k.transparency[​](#stochasticktransparency)
• stochastic.%k.transparency: `number`

Default value: `0`

### stochastic.hlines background.color[​](#stochastichlines-backgroundcolor)
• stochastic.hlines background.color: `string`

Default value: `#2196F3`

### stochastic.hlines background.transparency[​](#stochastichlines-backgroundtransparency)
• stochastic.hlines background.transparency: `number`

Default value: `90`

### stochastic.hlines background.visible[​](#stochastichlines-backgroundvisible)
• stochastic.hlines background.visible: `boolean`

Default value: `true`

### stochastic.lowerlimit.color[​](#stochasticlowerlimitcolor)
• stochastic.lowerlimit.color: `string`

Default value: `#787B86`

### stochastic.lowerlimit.linestyle[​](#stochasticlowerlimitlinestyle)
• stochastic.lowerlimit.linestyle: `number`

Default value: `2`

### stochastic.lowerlimit.linewidth[​](#stochasticlowerlimitlinewidth)
• stochastic.lowerlimit.linewidth: `number`

Default value: `1`

### stochastic.lowerlimit.value[​](#stochasticlowerlimitvalue)
• stochastic.lowerlimit.value: `number`

Default value: `20`

### stochastic.lowerlimit.visible[​](#stochasticlowerlimitvisible)
• stochastic.lowerlimit.visible: `boolean`

Default value: `true`

### stochastic.upperlimit.color[​](#stochasticupperlimitcolor)
• stochastic.upperlimit.color: `string`

Default value: `#787B86`

### stochastic.upperlimit.linestyle[​](#stochasticupperlimitlinestyle)
• stochastic.upperlimit.linestyle: `number`

Default value: `2`

### stochastic.upperlimit.linewidth[​](#stochasticupperlimitlinewidth)
• stochastic.upperlimit.linewidth: `number`

Default value: `1`

### stochastic.upperlimit.value[​](#stochasticupperlimitvalue)
• stochastic.upperlimit.value: `number`

Default value: `80`

### stochastic.upperlimit.visible[​](#stochasticupperlimitvisible)
• stochastic.upperlimit.visible: `boolean`

Default value: `true`

### supertrend.down arrow.color[​](#supertrenddown-arrowcolor)
• supertrend.down arrow.color: `string`

Default value: `#FF0000`

### supertrend.down arrow.display[​](#supertrenddown-arrowdisplay)
• supertrend.down arrow.display: `number`

Default value: `15`

### supertrend.down arrow.linestyle[​](#supertrenddown-arrowlinestyle)
• supertrend.down arrow.linestyle: `number`

Default value: `0`

### supertrend.down arrow.linewidth[​](#supertrenddown-arrowlinewidth)
• supertrend.down arrow.linewidth: `number`

Default value: `3`

### supertrend.down arrow.location[​](#supertrenddown-arrowlocation)
• supertrend.down arrow.location: `string`

Default value: `AboveBar`

### supertrend.down arrow.plottype[​](#supertrenddown-arrowplottype)
• supertrend.down arrow.plottype: `string`

Default value: `shape_arrow_down`

### supertrend.down arrow.trackprice[​](#supertrenddown-arrowtrackprice)
• supertrend.down arrow.trackprice: `boolean`

Default value: `false`

### supertrend.down arrow.transparency[​](#supertrenddown-arrowtransparency)
• supertrend.down arrow.transparency: `number`

Default value: `35`

### supertrend.factor[​](#supertrendfactor)
• supertrend.factor: `number`

- Default value: `3`
- Input type: `float`
- Min: `1`
- Max: `100`

### supertrend.length[​](#supertrendlength)
• supertrend.length: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `100`

### supertrend.supertrend.color[​](#supertrendsupertrendcolor)
• supertrend.supertrend.color: `string`

Default value: `#000080`

### supertrend.supertrend.display[​](#supertrendsupertrenddisplay)
• supertrend.supertrend.display: `number`

Default value: `15`

### supertrend.supertrend.linestyle[​](#supertrendsupertrendlinestyle)
• supertrend.supertrend.linestyle: `number`

Default value: `0`

### supertrend.supertrend.linewidth[​](#supertrendsupertrendlinewidth)
• supertrend.supertrend.linewidth: `number`

Default value: `3`

### supertrend.supertrend.plottype[​](#supertrendsupertrendplottype)
• supertrend.supertrend.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### supertrend.supertrend.trackprice[​](#supertrendsupertrendtrackprice)
• supertrend.supertrend.trackprice: `boolean`

Default value: `false`

### supertrend.supertrend.transparency[​](#supertrendsupertrendtransparency)
• supertrend.supertrend.transparency: `number`

Default value: `35`

### supertrend.up arrow.color[​](#supertrendup-arrowcolor)
• supertrend.up arrow.color: `string`

Default value: `#00FF00`

### supertrend.up arrow.display[​](#supertrendup-arrowdisplay)
• supertrend.up arrow.display: `number`

Default value: `15`

### supertrend.up arrow.linestyle[​](#supertrendup-arrowlinestyle)
• supertrend.up arrow.linestyle: `number`

Default value: `0`

### supertrend.up arrow.linewidth[​](#supertrendup-arrowlinewidth)
• supertrend.up arrow.linewidth: `number`

Default value: `3`

### supertrend.up arrow.location[​](#supertrendup-arrowlocation)
• supertrend.up arrow.location: `string`

Default value: `BelowBar`

### supertrend.up arrow.plottype[​](#supertrendup-arrowplottype)
• supertrend.up arrow.plottype: `string`

Default value: `shape_arrow_up`

### supertrend.up arrow.trackprice[​](#supertrendup-arrowtrackprice)
• supertrend.up arrow.trackprice: `boolean`

Default value: `false`

### supertrend.up arrow.transparency[​](#supertrendup-arrowtransparency)
• supertrend.up arrow.transparency: `number`

Default value: `35`

### trend strength index.periods[​](#trend-strength-indexperiods)
• trend strength index.periods: `number`

- Default value: `14`
- Input type: `integer`

### trend strength index.plot.color[​](#trend-strength-indexplotcolor)
• trend strength index.plot.color: `string`

Default value: `#FF5252`

### trend strength index.plot.display[​](#trend-strength-indexplotdisplay)
• trend strength index.plot.display: `number`

Default value: `15`

### trend strength index.plot.linestyle[​](#trend-strength-indexplotlinestyle)
• trend strength index.plot.linestyle: `number`

Default value: `0`

### trend strength index.plot.linewidth[​](#trend-strength-indexplotlinewidth)
• trend strength index.plot.linewidth: `number`

Default value: `1`

### trend strength index.plot.plottype[​](#trend-strength-indexplotplottype)
• trend strength index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### trend strength index.plot.trackprice[​](#trend-strength-indexplottrackprice)
• trend strength index.plot.trackprice: `boolean`

Default value: `false`

### trend strength index.plot.transparency[​](#trend-strength-indexplottransparency)
• trend strength index.plot.transparency: `number`

Default value: `0`

### triple ema.length[​](#triple-emalength)
• triple ema.length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### triple ema.plot.color[​](#triple-emaplotcolor)
• triple ema.plot.color: `string`

Default value: `#2196F3`

### triple ema.plot.display[​](#triple-emaplotdisplay)
• triple ema.plot.display: `number`

Default value: `15`

### triple ema.plot.linestyle[​](#triple-emaplotlinestyle)
• triple ema.plot.linestyle: `number`

Default value: `0`

### triple ema.plot.linewidth[​](#triple-emaplotlinewidth)
• triple ema.plot.linewidth: `number`

Default value: `1`

### triple ema.plot.plottype[​](#triple-emaplotplottype)
• triple ema.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### triple ema.plot.trackprice[​](#triple-emaplottrackprice)
• triple ema.plot.trackprice: `boolean`

Default value: `false`

### triple ema.plot.transparency[​](#triple-emaplottransparency)
• triple ema.plot.transparency: `number`

Default value: `0`

### trix.length[​](#trixlength)
• trix.length: `number`

- Default value: `18`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### trix.trix.color[​](#trixtrixcolor)
• trix.trix.color: `string`

Default value: `#F23645`

### trix.trix.display[​](#trixtrixdisplay)
• trix.trix.display: `number`

Default value: `15`

### trix.trix.linestyle[​](#trixtrixlinestyle)
• trix.trix.linestyle: `number`

Default value: `0`

### trix.trix.linewidth[​](#trixtrixlinewidth)
• trix.trix.linewidth: `number`

Default value: `1`

### trix.trix.plottype[​](#trixtrixplottype)
• trix.trix.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### trix.trix.trackprice[​](#trixtrixtrackprice)
• trix.trix.trackprice: `boolean`

Default value: `false`

### trix.trix.transparency[​](#trixtrixtransparency)
• trix.trix.transparency: `number`

Default value: `0`

### trix.zero.color[​](#trixzerocolor)
• trix.zero.color: `string`

Default value: `#787B86`

### trix.zero.linestyle[​](#trixzerolinestyle)
• trix.zero.linestyle: `number`

Default value: `2`

### trix.zero.linewidth[​](#trixzerolinewidth)
• trix.zero.linewidth: `number`

Default value: `1`

### trix.zero.value[​](#trixzerovalue)
• trix.zero.value: `number`

Default value: `0`

### trix.zero.visible[​](#trixzerovisible)
• trix.zero.visible: `boolean`

Default value: `true`

### true strength index.long[​](#true-strength-indexlong)
• true strength index.long: `number`

- Default value: `25`
- Input type: `integer`
- Min: `1`
- Max: `4999`

### true strength index.short[​](#true-strength-indexshort)
• true strength index.short: `number`

- Default value: `13`
- Input type: `integer`
- Min: `1`
- Max: `4999`

### true strength index.siglen[​](#true-strength-indexsiglen)
• true strength index.siglen: `number`

- Default value: `13`
- Input type: `integer`
- Min: `1`
- Max: `4999`

### true strength index.signal.color[​](#true-strength-indexsignalcolor)
• true strength index.signal.color: `string`

Default value: `#E91E63`

### true strength index.signal.display[​](#true-strength-indexsignaldisplay)
• true strength index.signal.display: `number`

Default value: `15`

### true strength index.signal.linestyle[​](#true-strength-indexsignallinestyle)
• true strength index.signal.linestyle: `number`

Default value: `0`

### true strength index.signal.linewidth[​](#true-strength-indexsignallinewidth)
• true strength index.signal.linewidth: `number`

Default value: `1`

### true strength index.signal.plottype[​](#true-strength-indexsignalplottype)
• true strength index.signal.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### true strength index.signal.trackprice[​](#true-strength-indexsignaltrackprice)
• true strength index.signal.trackprice: `boolean`

Default value: `false`

### true strength index.signal.transparency[​](#true-strength-indexsignaltransparency)
• true strength index.signal.transparency: `number`

Default value: `0`

### true strength index.true strength index.color[​](#true-strength-indextrue-strength-indexcolor)
• true strength index.true strength index.color: `string`

Default value: `#2196F3`

### true strength index.true strength index.display[​](#true-strength-indextrue-strength-indexdisplay)
• true strength index.true strength index.display: `number`

Default value: `15`

### true strength index.true strength index.linestyle[​](#true-strength-indextrue-strength-indexlinestyle)
• true strength index.true strength index.linestyle: `number`

Default value: `0`

### true strength index.true strength index.linewidth[​](#true-strength-indextrue-strength-indexlinewidth)
• true strength index.true strength index.linewidth: `number`

Default value: `1`

### true strength index.true strength index.plottype[​](#true-strength-indextrue-strength-indexplottype)
• true strength index.true strength index.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### true strength index.true strength index.trackprice[​](#true-strength-indextrue-strength-indextrackprice)
• true strength index.true strength index.trackprice: `boolean`

Default value: `false`

### true strength index.true strength index.transparency[​](#true-strength-indextrue-strength-indextransparency)
• true strength index.true strength index.transparency: `number`

Default value: `0`

### true strength index.zero.color[​](#true-strength-indexzerocolor)
• true strength index.zero.color: `string`

Default value: `#787B86`

### true strength index.zero.linestyle[​](#true-strength-indexzerolinestyle)
• true strength index.zero.linestyle: `number`

Default value: `2`

### true strength index.zero.linewidth[​](#true-strength-indexzerolinewidth)
• true strength index.zero.linewidth: `number`

Default value: `1`

### true strength index.zero.value[​](#true-strength-indexzerovalue)
• true strength index.zero.value: `number`

Default value: `0`

### true strength index.zero.visible[​](#true-strength-indexzerovisible)
• true strength index.zero.visible: `boolean`

Default value: `true`

### typical price.plot.color[​](#typical-priceplotcolor)
• typical price.plot.color: `string`

Default value: `#FF6D00`

### typical price.plot.display[​](#typical-priceplotdisplay)
• typical price.plot.display: `number`

Default value: `15`

### typical price.plot.linestyle[​](#typical-priceplotlinestyle)
• typical price.plot.linestyle: `number`

Default value: `0`

### typical price.plot.linewidth[​](#typical-priceplotlinewidth)
• typical price.plot.linewidth: `number`

Default value: `1`

### typical price.plot.plottype[​](#typical-priceplotplottype)
• typical price.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### typical price.plot.trackprice[​](#typical-priceplottrackprice)
• typical price.plot.trackprice: `boolean`

Default value: `false`

### typical price.plot.transparency[​](#typical-priceplottransparency)
• typical price.plot.transparency: `number`

Default value: `0`

### ultimate oscillator.length14[​](#ultimate-oscillatorlength14)
• ultimate oscillator.length14: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### ultimate oscillator.length28[​](#ultimate-oscillatorlength28)
• ultimate oscillator.length28: `number`

- Default value: `28`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### ultimate oscillator.length7[​](#ultimate-oscillatorlength7)
• ultimate oscillator.length7: `number`

- Default value: `7`
- Input type: `integer`
- Min: `1`
- Max: `1000000000000`

### ultimate oscillator.uo.color[​](#ultimate-oscillatoruocolor)
• ultimate oscillator.uo.color: `string`

Default value: `#F23645`

### ultimate oscillator.uo.display[​](#ultimate-oscillatoruodisplay)
• ultimate oscillator.uo.display: `number`

Default value: `15`

### ultimate oscillator.uo.linestyle[​](#ultimate-oscillatoruolinestyle)
• ultimate oscillator.uo.linestyle: `number`

Default value: `0`

### ultimate oscillator.uo.linewidth[​](#ultimate-oscillatoruolinewidth)
• ultimate oscillator.uo.linewidth: `number`

Default value: `1`

### ultimate oscillator.uo.plottype[​](#ultimate-oscillatoruoplottype)
• ultimate oscillator.uo.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### ultimate oscillator.uo.trackprice[​](#ultimate-oscillatoruotrackprice)
• ultimate oscillator.uo.trackprice: `boolean`

Default value: `false`

### ultimate oscillator.uo.transparency[​](#ultimate-oscillatoruotransparency)
• ultimate oscillator.uo.transparency: `number`

Default value: `0`

### volatility close-to-close.days per year[​](#volatility-close-to-closedays-per-year)
• volatility close-to-close.days per year: `number`

- Default value: `252`
- Input type: `integer`
- Min: `1`
- Max: `366`

### volatility close-to-close.periods[​](#volatility-close-to-closeperiods)
• volatility close-to-close.periods: `number`

- Default value: `10`
- Input type: `integer`
- Min: `2`

### volatility close-to-close.plot.color[​](#volatility-close-to-closeplotcolor)
• volatility close-to-close.plot.color: `string`

Default value: `#2196F3`

### volatility close-to-close.plot.display[​](#volatility-close-to-closeplotdisplay)
• volatility close-to-close.plot.display: `number`

Default value: `15`

### volatility close-to-close.plot.linestyle[​](#volatility-close-to-closeplotlinestyle)
• volatility close-to-close.plot.linestyle: `number`

Default value: `0`

### volatility close-to-close.plot.linewidth[​](#volatility-close-to-closeplotlinewidth)
• volatility close-to-close.plot.linewidth: `number`

Default value: `1`

### volatility close-to-close.plot.plottype[​](#volatility-close-to-closeplotplottype)
• volatility close-to-close.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### volatility close-to-close.plot.trackprice[​](#volatility-close-to-closeplottrackprice)
• volatility close-to-close.plot.trackprice: `boolean`

Default value: `false`

### volatility close-to-close.plot.transparency[​](#volatility-close-to-closeplottransparency)
• volatility close-to-close.plot.transparency: `number`

Default value: `0`

### volatility index.atr mult[​](#volatility-indexatr-mult)
• volatility index.atr mult: `number`

- Default value: `3`
- Input type: `float`

### volatility index.method[​](#volatility-indexmethod)
• volatility index.method: `string`

- Default value: `Wilder Smoothing`
- Input type: `text`
- Options: `["Exponential","Wilder Smoothing"]`

### volatility index.periods[​](#volatility-indexperiods)
• volatility index.periods: `number`

- Default value: `10`
- Input type: `integer`

### volatility index.plot.color[​](#volatility-indexplotcolor)
• volatility index.plot.color: `string`

Default value: `#FF5252`

### volatility index.plot.display[​](#volatility-indexplotdisplay)
• volatility index.plot.display: `number`

Default value: `15`

### volatility index.plot.linestyle[​](#volatility-indexplotlinestyle)
• volatility index.plot.linestyle: `number`

Default value: `0`

### volatility index.plot.linewidth[​](#volatility-indexplotlinewidth)
• volatility index.plot.linewidth: `number`

Default value: `1`

### volatility index.plot.plottype[​](#volatility-indexplotplottype)
• volatility index.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### volatility index.plot.trackprice[​](#volatility-indexplottrackprice)
• volatility index.plot.trackprice: `boolean`

Default value: `false`

### volatility index.plot.transparency[​](#volatility-indexplottransparency)
• volatility index.plot.transparency: `number`

Default value: `0`

### volatility o-h-l-c.days per year[​](#volatility-o-h-l-cdays-per-year)
• volatility o-h-l-c.days per year: `number`

- Default value: `252`
- Input type: `integer`

### volatility o-h-l-c.market closed percentage[​](#volatility-o-h-l-cmarket-closed-percentage)
• volatility o-h-l-c.market closed percentage: `number`

- Default value: `0`
- Input type: `float`
- Min: `0`
- Max: `0.999`

### volatility o-h-l-c.periods[​](#volatility-o-h-l-cperiods)
• volatility o-h-l-c.periods: `number`

- Default value: `10`
- Input type: `integer`

### volatility o-h-l-c.plot.color[​](#volatility-o-h-l-cplotcolor)
• volatility o-h-l-c.plot.color: `string`

Default value: `#FF5252`

### volatility o-h-l-c.plot.display[​](#volatility-o-h-l-cplotdisplay)
• volatility o-h-l-c.plot.display: `number`

Default value: `15`

### volatility o-h-l-c.plot.linestyle[​](#volatility-o-h-l-cplotlinestyle)
• volatility o-h-l-c.plot.linestyle: `number`

Default value: `0`

### volatility o-h-l-c.plot.linewidth[​](#volatility-o-h-l-cplotlinewidth)
• volatility o-h-l-c.plot.linewidth: `number`

Default value: `1`

### volatility o-h-l-c.plot.plottype[​](#volatility-o-h-l-cplotplottype)
• volatility o-h-l-c.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### volatility o-h-l-c.plot.trackprice[​](#volatility-o-h-l-cplottrackprice)
• volatility o-h-l-c.plot.trackprice: `boolean`

Default value: `false`

### volatility o-h-l-c.plot.transparency[​](#volatility-o-h-l-cplottransparency)
• volatility o-h-l-c.plot.transparency: `number`

Default value: `0`

### volatility zero trend close-to-close.days per year[​](#volatility-zero-trend-close-to-closedays-per-year)
• volatility zero trend close-to-close.days per year: `number`

- Default value: `252`
- Input type: `integer`

### volatility zero trend close-to-close.periods[​](#volatility-zero-trend-close-to-closeperiods)
• volatility zero trend close-to-close.periods: `number`

- Default value: `10`
- Input type: `integer`
- Min: `0`
- Max: `10000`

### volatility zero trend close-to-close.plot.color[​](#volatility-zero-trend-close-to-closeplotcolor)
• volatility zero trend close-to-close.plot.color: `string`

Default value: `#2196F3`

### volatility zero trend close-to-close.plot.display[​](#volatility-zero-trend-close-to-closeplotdisplay)
• volatility zero trend close-to-close.plot.display: `number`

Default value: `15`

### volatility zero trend close-to-close.plot.linestyle[​](#volatility-zero-trend-close-to-closeplotlinestyle)
• volatility zero trend close-to-close.plot.linestyle: `number`

Default value: `0`

### volatility zero trend close-to-close.plot.linewidth[​](#volatility-zero-trend-close-to-closeplotlinewidth)
• volatility zero trend close-to-close.plot.linewidth: `number`

Default value: `1`

### volatility zero trend close-to-close.plot.plottype[​](#volatility-zero-trend-close-to-closeplotplottype)
• volatility zero trend close-to-close.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### volatility zero trend close-to-close.plot.trackprice[​](#volatility-zero-trend-close-to-closeplottrackprice)
• volatility zero trend close-to-close.plot.trackprice: `boolean`

Default value: `false`

### volatility zero trend close-to-close.plot.transparency[​](#volatility-zero-trend-close-to-closeplottransparency)
• volatility zero trend close-to-close.plot.transparency: `number`

Default value: `0`

### volume oscillator.longlen[​](#volume-oscillatorlonglen)
• volume oscillator.longlen: `number`

- Default value: `10`
- Input type: `integer`
- Min: `1`
- Max: `4999`

### volume oscillator.plot.color[​](#volume-oscillatorplotcolor)
• volume oscillator.plot.color: `string`

Default value: `#2196F3`

### volume oscillator.plot.display[​](#volume-oscillatorplotdisplay)
• volume oscillator.plot.display: `number`

Default value: `15`

### volume oscillator.plot.linestyle[​](#volume-oscillatorplotlinestyle)
• volume oscillator.plot.linestyle: `number`

Default value: `0`

### volume oscillator.plot.linewidth[​](#volume-oscillatorplotlinewidth)
• volume oscillator.plot.linewidth: `number`

Default value: `1`

### volume oscillator.plot.plottype[​](#volume-oscillatorplotplottype)
• volume oscillator.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### volume oscillator.plot.trackprice[​](#volume-oscillatorplottrackprice)
• volume oscillator.plot.trackprice: `boolean`

Default value: `false`

### volume oscillator.plot.transparency[​](#volume-oscillatorplottransparency)
• volume oscillator.plot.transparency: `number`

Default value: `0`

### volume oscillator.shortlen[​](#volume-oscillatorshortlen)
• volume oscillator.shortlen: `number`

- Default value: `5`
- Input type: `integer`
- Min: `1`
- Max: `4999`

### volume oscillator.zero.color[​](#volume-oscillatorzerocolor)
• volume oscillator.zero.color: `string`

Default value: `#787B86`

### volume oscillator.zero.linestyle[​](#volume-oscillatorzerolinestyle)
• volume oscillator.zero.linestyle: `number`

Default value: `2`

### volume oscillator.zero.linewidth[​](#volume-oscillatorzerolinewidth)
• volume oscillator.zero.linewidth: `number`

Default value: `1`

### volume oscillator.zero.value[​](#volume-oscillatorzerovalue)
• volume oscillator.zero.value: `number`

Default value: `0`

### volume oscillator.zero.visible[​](#volume-oscillatorzerovisible)
• volume oscillator.zero.visible: `boolean`

Default value: `true`

### volume profile fixed range.developing poc.color[​](#volume-profile-fixed-rangedeveloping-poccolor)
• volume profile fixed range.developing poc.color: `string`

Default value: `undefined`

### volume profile fixed range.developing poc.display[​](#volume-profile-fixed-rangedeveloping-pocdisplay)
• volume profile fixed range.developing poc.display: `number`

Default value: `0`

### volume profile fixed range.developing poc.linestyle[​](#volume-profile-fixed-rangedeveloping-poclinestyle)
• volume profile fixed range.developing poc.linestyle: `number`

Default value: `0`

### volume profile fixed range.developing poc.linewidth[​](#volume-profile-fixed-rangedeveloping-poclinewidth)
• volume profile fixed range.developing poc.linewidth: `number`

Default value: `1`

### volume profile fixed range.developing poc.plottype[​](#volume-profile-fixed-rangedeveloping-pocplottype)
• volume profile fixed range.developing poc.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### volume profile fixed range.developing poc.trackprice[​](#volume-profile-fixed-rangedeveloping-poctrackprice)
• volume profile fixed range.developing poc.trackprice: `boolean`

Default value: `false`

### volume profile fixed range.developing poc.transparency[​](#volume-profile-fixed-rangedeveloping-poctransparency)
• volume profile fixed range.developing poc.transparency: `number`

Default value: `0`

### volume profile fixed range.developing va high.color[​](#volume-profile-fixed-rangedeveloping-va-highcolor)
• volume profile fixed range.developing va high.color: `string`

Default value: `undefined`

### volume profile fixed range.developing va high.display[​](#volume-profile-fixed-rangedeveloping-va-highdisplay)
• volume profile fixed range.developing va high.display: `number`

Default value: `0`

### volume profile fixed range.developing va high.linestyle[​](#volume-profile-fixed-rangedeveloping-va-highlinestyle)
• volume profile fixed range.developing va high.linestyle: `number`

Default value: `0`

### volume profile fixed range.developing va high.linewidth[​](#volume-profile-fixed-rangedeveloping-va-highlinewidth)
• volume profile fixed range.developing va high.linewidth: `number`

Default value: `1`

### volume profile fixed range.developing va high.plottype[​](#volume-profile-fixed-rangedeveloping-va-highplottype)
• volume profile fixed range.developing va high.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### volume profile fixed range.developing va high.trackprice[​](#volume-profile-fixed-rangedeveloping-va-hightrackprice)
• volume profile fixed range.developing va high.trackprice: `boolean`

Default value: `false`

### volume profile fixed range.developing va high.transparency[​](#volume-profile-fixed-rangedeveloping-va-hightransparency)
• volume profile fixed range.developing va high.transparency: `number`

Default value: `0`

### volume profile fixed range.developing va low.color[​](#volume-profile-fixed-rangedeveloping-va-lowcolor)
• volume profile fixed range.developing va low.color: `string`

Default value: `undefined`

### volume profile fixed range.developing va low.display[​](#volume-profile-fixed-rangedeveloping-va-lowdisplay)
• volume profile fixed range.developing va low.display: `number`

Default value: `0`

### volume profile fixed range.developing va low.linestyle[​](#volume-profile-fixed-rangedeveloping-va-lowlinestyle)
• volume profile fixed range.developing va low.linestyle: `number`

Default value: `0`

### volume profile fixed range.developing va low.linewidth[​](#volume-profile-fixed-rangedeveloping-va-lowlinewidth)
• volume profile fixed range.developing va low.linewidth: `number`

Default value: `1`

### volume profile fixed range.developing va low.plottype[​](#volume-profile-fixed-rangedeveloping-va-lowplottype)
• volume profile fixed range.developing va low.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### volume profile fixed range.developing va low.trackprice[​](#volume-profile-fixed-rangedeveloping-va-lowtrackprice)
• volume profile fixed range.developing va low.trackprice: `boolean`

Default value: `false`

### volume profile fixed range.developing va low.transparency[​](#volume-profile-fixed-rangedeveloping-va-lowtransparency)
• volume profile fixed range.developing va low.transparency: `number`

Default value: `0`

### volume profile fixed range.first bar time[​](#volume-profile-fixed-rangefirst-bar-time)
• volume profile fixed range.first bar time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `253370764800`
- Min: `-253370764800`

### volume profile fixed range.last bar time[​](#volume-profile-fixed-rangelast-bar-time)
• volume profile fixed range.last bar time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `253370764800`
- Min: `-253370764800`

### volume profile fixed range.row size[​](#volume-profile-fixed-rangerow-size)
• volume profile fixed range.row size: `number`

- Default value: `24`
- Input type: `integer`
- Max: `1000000`
- Min: `1`

### volume profile fixed range.rows layout[​](#volume-profile-fixed-rangerows-layout)
• volume profile fixed range.rows layout: `string`

- Default value: `Number Of Rows`
- Input type: `text`
- Options: `["Number Of Rows","Ticks Per Row"]`

### volume profile fixed range.subscriberealtime[​](#volume-profile-fixed-rangesubscriberealtime)
• volume profile fixed range.subscriberealtime: `boolean`

- Default value: `true`
- Input type: `bool`
- IsHidden: `true`

### volume profile fixed range.value area volume[​](#volume-profile-fixed-rangevalue-area-volume)
• volume profile fixed range.value area volume: `number`

- Default value: `70`
- Input type: `integer`
- Max: `100`
- Min: `0`

### volume profile fixed range.volume[​](#volume-profile-fixed-rangevolume)
• volume profile fixed range.volume: `string`

- Default value: `Up/Down`
- Input type: `text`
- Options: `["Up/Down","Total","Delta"]`

### volume profile visible range.developing poc.color[​](#volume-profile-visible-rangedeveloping-poccolor)
• volume profile visible range.developing poc.color: `string`

Default value: `undefined`

### volume profile visible range.developing poc.display[​](#volume-profile-visible-rangedeveloping-pocdisplay)
• volume profile visible range.developing poc.display: `number`

Default value: `0`

### volume profile visible range.developing poc.linestyle[​](#volume-profile-visible-rangedeveloping-poclinestyle)
• volume profile visible range.developing poc.linestyle: `number`

Default value: `0`

### volume profile visible range.developing poc.linewidth[​](#volume-profile-visible-rangedeveloping-poclinewidth)
• volume profile visible range.developing poc.linewidth: `number`

Default value: `1`

### volume profile visible range.developing poc.plottype[​](#volume-profile-visible-rangedeveloping-pocplottype)
• volume profile visible range.developing poc.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### volume profile visible range.developing poc.trackprice[​](#volume-profile-visible-rangedeveloping-poctrackprice)
• volume profile visible range.developing poc.trackprice: `boolean`

Default value: `false`

### volume profile visible range.developing poc.transparency[​](#volume-profile-visible-rangedeveloping-poctransparency)
• volume profile visible range.developing poc.transparency: `number`

Default value: `0`

### volume profile visible range.developing va high.color[​](#volume-profile-visible-rangedeveloping-va-highcolor)
• volume profile visible range.developing va high.color: `string`

Default value: `undefined`

### volume profile visible range.developing va high.display[​](#volume-profile-visible-rangedeveloping-va-highdisplay)
• volume profile visible range.developing va high.display: `number`

Default value: `0`

### volume profile visible range.developing va high.linestyle[​](#volume-profile-visible-rangedeveloping-va-highlinestyle)
• volume profile visible range.developing va high.linestyle: `number`

Default value: `0`

### volume profile visible range.developing va high.linewidth[​](#volume-profile-visible-rangedeveloping-va-highlinewidth)
• volume profile visible range.developing va high.linewidth: `number`

Default value: `1`

### volume profile visible range.developing va high.plottype[​](#volume-profile-visible-rangedeveloping-va-highplottype)
• volume profile visible range.developing va high.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### volume profile visible range.developing va high.trackprice[​](#volume-profile-visible-rangedeveloping-va-hightrackprice)
• volume profile visible range.developing va high.trackprice: `boolean`

Default value: `false`

### volume profile visible range.developing va high.transparency[​](#volume-profile-visible-rangedeveloping-va-hightransparency)
• volume profile visible range.developing va high.transparency: `number`

Default value: `0`

### volume profile visible range.developing va low.color[​](#volume-profile-visible-rangedeveloping-va-lowcolor)
• volume profile visible range.developing va low.color: `string`

Default value: `undefined`

### volume profile visible range.developing va low.display[​](#volume-profile-visible-rangedeveloping-va-lowdisplay)
• volume profile visible range.developing va low.display: `number`

Default value: `0`

### volume profile visible range.developing va low.linestyle[​](#volume-profile-visible-rangedeveloping-va-lowlinestyle)
• volume profile visible range.developing va low.linestyle: `number`

Default value: `0`

### volume profile visible range.developing va low.linewidth[​](#volume-profile-visible-rangedeveloping-va-lowlinewidth)
• volume profile visible range.developing va low.linewidth: `number`

Default value: `1`

### volume profile visible range.developing va low.plottype[​](#volume-profile-visible-rangedeveloping-va-lowplottype)
• volume profile visible range.developing va low.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `step_line`

### volume profile visible range.developing va low.trackprice[​](#volume-profile-visible-rangedeveloping-va-lowtrackprice)
• volume profile visible range.developing va low.trackprice: `boolean`

Default value: `false`

### volume profile visible range.developing va low.transparency[​](#volume-profile-visible-rangedeveloping-va-lowtransparency)
• volume profile visible range.developing va low.transparency: `number`

Default value: `0`

### volume profile visible range.first visible bar time[​](#volume-profile-visible-rangefirst-visible-bar-time)
• volume profile visible range.first visible bar time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `253370764800`
- Min: `-253370764800`

### volume profile visible range.last visible bar time[​](#volume-profile-visible-rangelast-visible-bar-time)
• volume profile visible range.last visible bar time: `number`

- Default value: `0`
- Input type: `time`
- IsHidden: `true`
- Max: `253370764800`
- Min: `-253370764800`

### volume profile visible range.row size[​](#volume-profile-visible-rangerow-size)
• volume profile visible range.row size: `number`

- Default value: `24`
- Input type: `integer`
- Max: `1000000`
- Min: `1`

### volume profile visible range.rows layout[​](#volume-profile-visible-rangerows-layout)
• volume profile visible range.rows layout: `string`

- Default value: `Number Of Rows`
- Input type: `text`
- Options: `["Number Of Rows","Ticks Per Row"]`

### volume profile visible range.value area volume[​](#volume-profile-visible-rangevalue-area-volume)
• volume profile visible range.value area volume: `number`

- Default value: `70`
- Input type: `integer`
- Max: `100`
- Min: `0`

### volume profile visible range.volume[​](#volume-profile-visible-rangevolume)
• volume profile visible range.volume: `string`

- Default value: `Up/Down`
- Input type: `text`
- Options: `["Up/Down","Total","Delta"]`

### volume.color based on previous close[​](#volumecolor-based-on-previous-close)
• volume.color based on previous close: `boolean`

- Default value: `false`
- Input type: `bool`

### volume.ma length[​](#volumema-length)
• volume.ma length: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### volume.other symbol[​](#volumeother-symbol)
• volume.other symbol: `string`

- Default value: `undefined`
- Input type: `symbol`
- Optional: `true`
- IsHidden: `false`

### volume.show ma[​](#volumeshow-ma)
• volume.show ma: `boolean`

- Default value: `false`
- Input type: `bool`
- IsHidden: `true`

### volume.smoothed ma.color[​](#volumesmoothed-macolor)
• volume.smoothed ma.color: `string`

Default value: `#2196F3`

### volume.smoothed ma.display[​](#volumesmoothed-madisplay)
• volume.smoothed ma.display: `number`

Default value: `0`

### volume.smoothed ma.linestyle[​](#volumesmoothed-malinestyle)
• volume.smoothed ma.linestyle: `number`

Default value: `0`

### volume.smoothed ma.linewidth[​](#volumesmoothed-malinewidth)
• volume.smoothed ma.linewidth: `number`

Default value: `1`

### volume.smoothed ma.plottype[​](#volumesmoothed-maplottype)
• volume.smoothed ma.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### volume.smoothed ma.trackprice[​](#volumesmoothed-matrackprice)
• volume.smoothed ma.trackprice: `boolean`

Default value: `false`

### volume.smoothed ma.transparency[​](#volumesmoothed-matransparency)
• volume.smoothed ma.transparency: `number`

Default value: `0`

### volume.smoothing length[​](#volumesmoothing-length)
• volume.smoothing length: `number`

- Default value: `9`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### volume.smoothing line[​](#volumesmoothing-line)
• volume.smoothing line: `string`

- Default value: `SMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### volume.volume ma:input[​](#volumevolume-ma)
• volume.volume ma:input: `string`

- Default value: `SMA`
- Input type: `text`
- Options: `["SMA","EMA","WMA"]`

### volume.volume ma:plot.color[​](#volumevolume-macolor)
• volume.volume ma:plot.color: `string`

Default value: `#2196F3`

### volume.volume ma:plot.display[​](#volumevolume-madisplay)
• volume.volume ma:plot.display: `number`

Default value: `0`

### volume.volume ma:plot.linestyle[​](#volumevolume-malinestyle)
• volume.volume ma:plot.linestyle: `number`

Default value: `0`

### volume.volume ma:plot.linewidth[​](#volumevolume-malinewidth)
• volume.volume ma:plot.linewidth: `number`

Default value: `1`

### volume.volume ma:plot.plottype[​](#volumevolume-maplottype)
• volume.volume ma:plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### volume.volume ma:plot.trackprice[​](#volumevolume-matrackprice)
• volume.volume ma:plot.trackprice: `boolean`

Default value: `false`

### volume.volume ma:plot.transparency[​](#volumevolume-matransparency)
• volume.volume ma:plot.transparency: `number`

Default value: `0`

### volume.volume.color[​](#volumevolumecolor)
• volume.volume.color: `string`

Default value: `#000080`

### volume.volume.display[​](#volumevolumedisplay)
• volume.volume.display: `number`

Default value: `15`

### volume.volume.linestyle[​](#volumevolumelinestyle)
• volume.volume.linestyle: `number`

Default value: `0`

### volume.volume.linewidth[​](#volumevolumelinewidth)
• volume.volume.linewidth: `number`

Default value: `1`

### volume.volume.plottype[​](#volumevolumeplottype)
• volume.volume.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `columns`

### volume.volume.trackprice[​](#volumevolumetrackprice)
• volume.volume.trackprice: `boolean`

Default value: `false`

### volume.volume.transparency[​](#volumevolumetransparency)
• volume.volume.transparency: `number`

Default value: `50`

### vortex indicator.period[​](#vortex-indicatorperiod)
• vortex indicator.period: `number`

- Default value: `14`
- Input type: `integer`
- Min: `2`
- Max: `1000000000000`

### vortex indicator.vi +.color[​](#vortex-indicatorvi-color)
• vortex indicator.vi +.color: `string`

Default value: `#2196F3`

### vortex indicator.vi +.display[​](#vortex-indicatorvi-display)
• vortex indicator.vi +.display: `number`

Default value: `15`

### vortex indicator.vi +.linestyle[​](#vortex-indicatorvi-linestyle)
• vortex indicator.vi +.linestyle: `number`

Default value: `0`

### vortex indicator.vi +.linewidth[​](#vortex-indicatorvi-linewidth)
• vortex indicator.vi +.linewidth: `number`

Default value: `1`

### vortex indicator.vi +.plottype[​](#vortex-indicatorvi-plottype)
• vortex indicator.vi +.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### vortex indicator.vi +.trackprice[​](#vortex-indicatorvi-trackprice)
• vortex indicator.vi +.trackprice: `boolean`

Default value: `false`

### vortex indicator.vi +.transparency[​](#vortex-indicatorvi-transparency)
• vortex indicator.vi +.transparency: `number`

Default value: `0`

### vortex indicator.vi -.color[​](#vortex-indicatorvi--color)
• vortex indicator.vi -.color: `string`

Default value: `#E91E63`

### vortex indicator.vi -.display[​](#vortex-indicatorvi--display)
• vortex indicator.vi -.display: `number`

Default value: `15`

### vortex indicator.vi -.linestyle[​](#vortex-indicatorvi--linestyle)
• vortex indicator.vi -.linestyle: `number`

Default value: `0`

### vortex indicator.vi -.linewidth[​](#vortex-indicatorvi--linewidth)
• vortex indicator.vi -.linewidth: `number`

Default value: `1`

### vortex indicator.vi -.plottype[​](#vortex-indicatorvi--plottype)
• vortex indicator.vi -.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### vortex indicator.vi -.trackprice[​](#vortex-indicatorvi--trackprice)
• vortex indicator.vi -.trackprice: `boolean`

Default value: `false`

### vortex indicator.vi -.transparency[​](#vortex-indicatorvi--transparency)
• vortex indicator.vi -.transparency: `number`

Default value: `0`

### vwap.anchor period[​](#vwapanchor-period)
• vwap.anchor period: `string`

- Default value: `Session`
- Input type: `text`
- Options: `["Session","Week","Month","Quarter","Year","Decade","Century"]`

### vwap.source[​](#vwapsource)
• vwap.source: `string`

- Default value: `hlc3`
- Input type: `source`
- Options: `["open","high","low","close","hl2","hlc3","ohlc4"]`

### vwap.vwap.color[​](#vwapvwapcolor)
• vwap.vwap.color: `string`

Default value: `#2196F3`

### vwap.vwap.display[​](#vwapvwapdisplay)
• vwap.vwap.display: `number`

Default value: `15`

### vwap.vwap.linestyle[​](#vwapvwaplinestyle)
• vwap.vwap.linestyle: `number`

Default value: `0`

### vwap.vwap.linewidth[​](#vwapvwaplinewidth)
• vwap.vwap.linewidth: `number`

Default value: `1`

### vwap.vwap.plottype[​](#vwapvwapplottype)
• vwap.vwap.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### vwap.vwap.trackprice[​](#vwapvwaptrackprice)
• vwap.vwap.trackprice: `number`

Default value: `0`

### vwap.vwap.transparency[​](#vwapvwaptransparency)
• vwap.vwap.transparency: `number`

Default value: `0`

### vwma.len[​](#vwmalen)
• vwma.len: `number`

- Default value: `20`
- Input type: `integer`
- Min: `1`
- Max: `10000`

### vwma.plot.color[​](#vwmaplotcolor)
• vwma.plot.color: `string`

Default value: `#2196F3`

### vwma.plot.display[​](#vwmaplotdisplay)
• vwma.plot.display: `number`

Default value: `15`

### vwma.plot.linestyle[​](#vwmaplotlinestyle)
• vwma.plot.linestyle: `number`

Default value: `0`

### vwma.plot.linewidth[​](#vwmaplotlinewidth)
• vwma.plot.linewidth: `number`

Default value: `1`

### vwma.plot.plottype[​](#vwmaplotplottype)
• vwma.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### vwma.plot.trackprice[​](#vwmaplottrackprice)
• vwma.plot.trackprice: `boolean`

Default value: `false`

### vwma.plot.transparency[​](#vwmaplottransparency)
• vwma.plot.transparency: `number`

Default value: `0`

### williams %r.hlines background.color[​](#williams-rhlines-backgroundcolor)
• williams %r.hlines background.color: `string`

Default value: `#7E57C2`

### williams %r.hlines background.transparency[​](#williams-rhlines-backgroundtransparency)
• williams %r.hlines background.transparency: `number`

Default value: `90`

### williams %r.hlines background.visible[​](#williams-rhlines-backgroundvisible)
• williams %r.hlines background.visible: `boolean`

Default value: `true`

### williams %r.length[​](#williams-rlength)
• williams %r.length: `number`

- Default value: `14`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### williams %r.lowerlimit.color[​](#williams-rlowerlimitcolor)
• williams %r.lowerlimit.color: `string`

Default value: `#787B86`

### williams %r.lowerlimit.linestyle[​](#williams-rlowerlimitlinestyle)
• williams %r.lowerlimit.linestyle: `number`

Default value: `2`

### williams %r.lowerlimit.linewidth[​](#williams-rlowerlimitlinewidth)
• williams %r.lowerlimit.linewidth: `number`

Default value: `1`

### williams %r.lowerlimit.value[​](#williams-rlowerlimitvalue)
• williams %r.lowerlimit.value: `number`

Default value: `-80`

### williams %r.lowerlimit.visible[​](#williams-rlowerlimitvisible)
• williams %r.lowerlimit.visible: `boolean`

Default value: `true`

### williams %r.plot.color[​](#williams-rplotcolor)
• williams %r.plot.color: `string`

Default value: `#7E57C2`

### williams %r.plot.display[​](#williams-rplotdisplay)
• williams %r.plot.display: `number`

Default value: `15`

### williams %r.plot.linestyle[​](#williams-rplotlinestyle)
• williams %r.plot.linestyle: `number`

Default value: `0`

### williams %r.plot.linewidth[​](#williams-rplotlinewidth)
• williams %r.plot.linewidth: `number`

Default value: `1`

### williams %r.plot.plottype[​](#williams-rplotplottype)
• williams %r.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### williams %r.plot.trackprice[​](#williams-rplottrackprice)
• williams %r.plot.trackprice: `boolean`

Default value: `false`

### williams %r.plot.transparency[​](#williams-rplottransparency)
• williams %r.plot.transparency: `number`

Default value: `0`

### williams %r.upperlimit.color[​](#williams-rupperlimitcolor)
• williams %r.upperlimit.color: `string`

Default value: `#787B86`

### williams %r.upperlimit.linestyle[​](#williams-rupperlimitlinestyle)
• williams %r.upperlimit.linestyle: `number`

Default value: `2`

### williams %r.upperlimit.linewidth[​](#williams-rupperlimitlinewidth)
• williams %r.upperlimit.linewidth: `number`

Default value: `1`

### williams %r.upperlimit.value[​](#williams-rupperlimitvalue)
• williams %r.upperlimit.value: `number`

Default value: `-20`

### williams %r.upperlimit.visible[​](#williams-rupperlimitvisible)
• williams %r.upperlimit.visible: `boolean`

Default value: `true`

### williams alligator.jaw length[​](#williams-alligatorjaw-length)
• williams alligator.jaw length: `number`

- Default value: `21`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### williams alligator.jaw offset[​](#williams-alligatorjaw-offset)
• williams alligator.jaw offset: `number`

- Default value: `8`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### williams alligator.jaw.color[​](#williams-alligatorjawcolor)
• williams alligator.jaw.color: `string`

Default value: `#2196F3`

### williams alligator.jaw.display[​](#williams-alligatorjawdisplay)
• williams alligator.jaw.display: `number`

Default value: `15`

### williams alligator.jaw.linestyle[​](#williams-alligatorjawlinestyle)
• williams alligator.jaw.linestyle: `number`

Default value: `0`

### williams alligator.jaw.linewidth[​](#williams-alligatorjawlinewidth)
• williams alligator.jaw.linewidth: `number`

Default value: `1`

### williams alligator.jaw.plottype[​](#williams-alligatorjawplottype)
• williams alligator.jaw.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### williams alligator.jaw.trackprice[​](#williams-alligatorjawtrackprice)
• williams alligator.jaw.trackprice: `boolean`

Default value: `false`

### williams alligator.jaw.transparency[​](#williams-alligatorjawtransparency)
• williams alligator.jaw.transparency: `number`

Default value: `0`

### williams alligator.lips length[​](#williams-alligatorlips-length)
• williams alligator.lips length: `number`

- Default value: `8`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### williams alligator.lips offset[​](#williams-alligatorlips-offset)
• williams alligator.lips offset: `number`

- Default value: `3`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### williams alligator.lips.color[​](#williams-alligatorlipscolor)
• williams alligator.lips.color: `string`

Default value: `#66BB6A`

### williams alligator.lips.display[​](#williams-alligatorlipsdisplay)
• williams alligator.lips.display: `number`

Default value: `15`

### williams alligator.lips.linestyle[​](#williams-alligatorlipslinestyle)
• williams alligator.lips.linestyle: `number`

Default value: `0`

### williams alligator.lips.linewidth[​](#williams-alligatorlipslinewidth)
• williams alligator.lips.linewidth: `number`

Default value: `1`

### williams alligator.lips.plottype[​](#williams-alligatorlipsplottype)
• williams alligator.lips.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### williams alligator.lips.trackprice[​](#williams-alligatorlipstrackprice)
• williams alligator.lips.trackprice: `boolean`

Default value: `false`

### williams alligator.lips.transparency[​](#williams-alligatorlipstransparency)
• williams alligator.lips.transparency: `number`

Default value: `0`

### williams alligator.teeth length[​](#williams-alligatorteeth-length)
• williams alligator.teeth length: `number`

- Default value: `13`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### williams alligator.teeth offset[​](#williams-alligatorteeth-offset)
• williams alligator.teeth offset: `number`

- Default value: `5`
- Input type: `integer`
- Min: `1`
- Max: `2000`

### williams alligator.teeth.color[​](#williams-alligatorteethcolor)
• williams alligator.teeth.color: `string`

Default value: `#E91E63`

### williams alligator.teeth.display[​](#williams-alligatorteethdisplay)
• williams alligator.teeth.display: `number`

Default value: `15`

### williams alligator.teeth.linestyle[​](#williams-alligatorteethlinestyle)
• williams alligator.teeth.linestyle: `number`

Default value: `0`

### williams alligator.teeth.linewidth[​](#williams-alligatorteethlinewidth)
• williams alligator.teeth.linewidth: `number`

Default value: `1`

### williams alligator.teeth.plottype[​](#williams-alligatorteethplottype)
• williams alligator.teeth.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### williams alligator.teeth.trackprice[​](#williams-alligatorteethtrackprice)
• williams alligator.teeth.trackprice: `boolean`

Default value: `false`

### williams alligator.teeth.transparency[​](#williams-alligatorteethtransparency)
• williams alligator.teeth.transparency: `number`

Default value: `0`

### williams fractal.down fractals.color[​](#williams-fractaldown-fractalscolor)
• williams fractal.down fractals.color: `string`

Default value: `#F23645`

### williams fractal.down fractals.display[​](#williams-fractaldown-fractalsdisplay)
• williams fractal.down fractals.display: `number`

Default value: `15`

### williams fractal.down fractals.location[​](#williams-fractaldown-fractalslocation)
• williams fractal.down fractals.location: `string`

Default value: `BelowBar`

### williams fractal.down fractals.plottype[​](#williams-fractaldown-fractalsplottype)
• williams fractal.down fractals.plottype: `string`

Default value: `shape_triangle_down`

### williams fractal.down fractals.transparency[​](#williams-fractaldown-fractalstransparency)
• williams fractal.down fractals.transparency: `number`

Default value: `0`

### williams fractal.periods[​](#williams-fractalperiods)
• williams fractal.periods: `number`

- Default value: `2`
- Input type: `integer`
- Min: `2`
- Max: `1000000000000`

### williams fractal.up fractals.color[​](#williams-fractalup-fractalscolor)
• williams fractal.up fractals.color: `string`

Default value: `#089981`

### williams fractal.up fractals.display[​](#williams-fractalup-fractalsdisplay)
• williams fractal.up fractals.display: `number`

Default value: `15`

### williams fractal.up fractals.location[​](#williams-fractalup-fractalslocation)
• williams fractal.up fractals.location: `string`

Default value: `AboveBar`

### williams fractal.up fractals.plottype[​](#williams-fractalup-fractalsplottype)
• williams fractal.up fractals.plottype: `string`

Default value: `shape_triangle_up`

### williams fractal.up fractals.transparency[​](#williams-fractalup-fractalstransparency)
• williams fractal.up fractals.transparency: `number`

Default value: `0`

### zig zag.depth[​](#zig-zagdepth)
• zig zag.depth: `number`

- Default value: `10`
- Input type: `integer`
- Min: `2`
- Max: `1000`

### zig zag.deviation[​](#zig-zagdeviation)
• zig zag.deviation: `number`

- Default value: `5`
- Input type: `float`
- Min: `0.001`
- Max: `100`

### zig zag.plot.color[​](#zig-zagplotcolor)
• zig zag.plot.color: `string`

Default value: `#2196F3`

### zig zag.plot.display[​](#zig-zagplotdisplay)
• zig zag.plot.display: `number`

Default value: `15`

### zig zag.plot.linestyle[​](#zig-zagplotlinestyle)
• zig zag.plot.linestyle: `number`

Default value: `0`

### zig zag.plot.linewidth[​](#zig-zagplotlinewidth)
• zig zag.plot.linewidth: `number`

Default value: `2`

### zig zag.plot.plottype[​](#zig-zagplotplottype)
• zig zag.plot.plottype: [`LineStudyPlotStyleName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linestudyplotstylename)

Default value: `line`

### zig zag.plot.trackprice[​](#zig-zagplottrackprice)
• zig zag.plot.trackprice: `boolean`

Default value: `false`

### zig zag.plot.transparency[​](#zig-zagplottransparency)
• zig zag.plot.transparency: `number`

Default value: `0`

- [Indexable](#indexable)- [Properties](#properties)[52 week high/low.high source](#52-week-highlowhigh-source)- [52 week high/low.low source](#52-week-highlowlow-source)- [accelerator oscillator.plot.color](#accelerator-oscillatorplotcolor)- [accelerator oscillator.plot.display](#accelerator-oscillatorplotdisplay)- [accelerator oscillator.plot.linestyle](#accelerator-oscillatorplotlinestyle)- [accelerator oscillator.plot.linewidth](#accelerator-oscillatorplotlinewidth)- [accelerator oscillator.plot.plottype](#accelerator-oscillatorplotplottype)- [accelerator oscillator.plot.trackprice](#accelerator-oscillatorplottrackprice)- [accelerator oscillator.plot.transparency](#accelerator-oscillatorplottransparency)- [accumulation/distribution.plot.color](#accumulationdistributionplotcolor)- [accumulation/distribution.plot.display](#accumulationdistributionplotdisplay)- [accumulation/distribution.plot.linestyle](#accumulationdistributionplotlinestyle)- [accumulation/distribution.plot.linewidth](#accumulationdistributionplotlinewidth)- [accumulation/distribution.plot.plottype](#accumulationdistributionplotplottype)- [accumulation/distribution.plot.trackprice](#accumulationdistributionplottrackprice)- [accumulation/distribution.plot.transparency](#accumulationdistributionplottransparency)- [accumulative swing index.asi.color](#accumulative-swing-indexasicolor)- [accumulative swing index.asi.display](#accumulative-swing-indexasidisplay)- [accumulative swing index.asi.linestyle](#accumulative-swing-indexasilinestyle)- [accumulative swing index.asi.linewidth](#accumulative-swing-indexasilinewidth)- [accumulative swing index.asi.plottype](#accumulative-swing-indexasiplottype)- [accumulative swing index.asi.trackprice](#accumulative-swing-indexasitrackprice)- [accumulative swing index.asi.transparency](#accumulative-swing-indexasitransparency)- [accumulative swing index.limit move value](#accumulative-swing-indexlimit-move-value)- [advance/decline.length](#advancedeclinelength)- [advance/decline.plot.color](#advancedeclineplotcolor)- [advance/decline.plot.display](#advancedeclineplotdisplay)- [advance/decline.plot.linestyle](#advancedeclineplotlinestyle)- [advance/decline.plot.linewidth](#advancedeclineplotlinewidth)- [advance/decline.plot.plottype](#advancedeclineplotplottype)- [advance/decline.plot.trackprice](#advancedeclineplottrackprice)- [advance/decline.plot.transparency](#advancedeclineplottransparency)- [anchored vwap. ](#anchored-vwap-)- [anchored vwap.background #1.color](#anchored-vwapbackground-1color)- [anchored vwap.background #1.transparency](#anchored-vwapbackground-1transparency)- [anchored vwap.background #1.visible](#anchored-vwapbackground-1visible)- [anchored vwap.bands calculation mode](#anchored-vwapbands-calculation-mode)- [anchored vwap.bands multiplier #1](#anchored-vwapbands-multiplier-1)- [anchored vwap.bands multiplier #2](#anchored-vwapbands-multiplier-2)- [anchored vwap.bands multiplier #3](#anchored-vwapbands-multiplier-3)- [anchored vwap.lower band #1.color](#anchored-vwaplower-band-1color)- [anchored vwap.lower band #1.display](#anchored-vwaplower-band-1display)- [anchored vwap.lower band #1.linestyle](#anchored-vwaplower-band-1linestyle)- [anchored vwap.lower band #1.linewidth](#anchored-vwaplower-band-1linewidth)- [anchored vwap.lower band #1.plottype](#anchored-vwaplower-band-1plottype)- [anchored vwap.lower band #1.trackprice](#anchored-vwaplower-band-1trackprice)- [anchored vwap.lower band #1.transparency](#anchored-vwaplower-band-1transparency)- [anchored vwap.lower band #2.color](#anchored-vwaplower-band-2color)- [anchored vwap.lower band #2.display](#anchored-vwaplower-band-2display)- [anchored vwap.lower band #2.linestyle](#anchored-vwaplower-band-2linestyle)- [anchored vwap.lower band #2.linewidth](#anchored-vwaplower-band-2linewidth)- [anchored vwap.lower band #2.plottype](#anchored-vwaplower-band-2plottype)- [anchored vwap.lower band #2.trackprice](#anchored-vwaplower-band-2trackprice)- [anchored vwap.lower band #2.transparency](#anchored-vwaplower-band-2transparency)- [anchored vwap.lower band #3.color](#anchored-vwaplower-band-3color)- [anchored vwap.lower band #3.display](#anchored-vwaplower-band-3display)- [anchored vwap.lower band #3.linestyle](#anchored-vwaplower-band-3linestyle)- [anchored vwap.lower band #3.linewidth](#anchored-vwaplower-band-3linewidth)- [anchored vwap.lower band #3.plottype](#anchored-vwaplower-band-3plottype)- [anchored vwap.lower band #3.trackprice](#anchored-vwaplower-band-3trackprice)- [anchored vwap.lower band #3.transparency](#anchored-vwaplower-band-3transparency)- [anchored vwap.source](#anchored-vwapsource)- [anchored vwap.start time](#anchored-vwapstart-time)- [anchored vwap.upper band #1.color](#anchored-vwapupper-band-1color)- [anchored vwap.upper band #1.display](#anchored-vwapupper-band-1display)- [anchored vwap.upper band #1.linestyle](#anchored-vwapupper-band-1linestyle)- [anchored vwap.upper band #1.linewidth](#anchored-vwapupper-band-1linewidth)- [anchored vwap.upper band #1.plottype](#anchored-vwapupper-band-1plottype)- [anchored vwap.upper band #1.trackprice](#anchored-vwapupper-band-1trackprice)- [anchored vwap.upper band #1.transparency](#anchored-vwapupper-band-1transparency)- [anchored vwap.upper band #2.color](#anchored-vwapupper-band-2color)- [anchored vwap.upper band #2.display](#anchored-vwapupper-band-2display)- [anchored vwap.upper band #2.linestyle](#anchored-vwapupper-band-2linestyle)- [anchored vwap.upper band #2.linewidth](#anchored-vwapupper-band-2linewidth)- [anchored vwap.upper band #2.plottype](#anchored-vwapupper-band-2plottype)- [anchored vwap.upper band #2.trackprice](#anchored-vwapupper-band-2trackprice)- [anchored vwap.upper band #2.transparency](#anchored-vwapupper-band-2transparency)- [anchored vwap.upper band #3.color](#anchored-vwapupper-band-3color)- [anchored vwap.upper band #3.display](#anchored-vwapupper-band-3display)- [anchored vwap.upper band #3.linestyle](#anchored-vwapupper-band-3linestyle)- [anchored vwap.upper band #3.linewidth](#anchored-vwapupper-band-3linewidth)- [anchored vwap.upper band #3.plottype](#anchored-vwapupper-band-3plottype)- [anchored vwap.upper band #3.trackprice](#anchored-vwapupper-band-3trackprice)- [anchored vwap.upper band #3.transparency](#anchored-vwapupper-band-3transparency)- [anchored vwap.vwap.color](#anchored-vwapvwapcolor)- [anchored vwap.vwap.display](#anchored-vwapvwapdisplay)- [anchored vwap.vwap.linestyle](#anchored-vwapvwaplinestyle)- [anchored vwap.vwap.linewidth](#anchored-vwapvwaplinewidth)- [anchored vwap.vwap.plottype](#anchored-vwapvwapplottype)- [anchored vwap.vwap.trackprice](#anchored-vwapvwaptrackprice)- [anchored vwap.vwap.transparency](#anchored-vwapvwaptransparency)- [areaStyle.color1](#areastylecolor1)- [areaStyle.color2](#areastylecolor2)- [areaStyle.linecolor](#areastylelinecolor)- [areaStyle.linestyle](#areastylelinestyle)- [areaStyle.linewidth](#areastylelinewidth)- [areaStyle.transparency](#areastyletransparency)- [arnaud legoux moving average.offset](#arnaud-legoux-moving-averageoffset)- [arnaud legoux moving average.plot.color](#arnaud-legoux-moving-averageplotcolor)- [arnaud legoux moving average.plot.display](#arnaud-legoux-moving-averageplotdisplay)- [arnaud legoux moving average.plot.linestyle](#arnaud-legoux-moving-averageplotlinestyle)- [arnaud legoux moving average.plot.linewidth](#arnaud-legoux-moving-averageplotlinewidth)- [arnaud legoux moving average.plot.plottype](#arnaud-legoux-moving-averageplotplottype)- [arnaud legoux moving average.plot.trackprice](#arnaud-legoux-moving-averageplottrackprice)- [arnaud legoux moving average.plot.transparency](#arnaud-legoux-moving-averageplottransparency)- [arnaud legoux moving average.sigma](#arnaud-legoux-moving-averagesigma)- [arnaud legoux moving average.window size](#arnaud-legoux-moving-averagewindow-size)- [aroon.length](#aroonlength)- [aroon.lower.color](#aroonlowercolor)- [aroon.lower.display](#aroonlowerdisplay)- [aroon.lower.linestyle](#aroonlowerlinestyle)- [aroon.lower.linewidth](#aroonlowerlinewidth)- [aroon.lower.plottype](#aroonlowerplottype)- [aroon.lower.trackprice](#aroonlowertrackprice)- [aroon.lower.transparency](#aroonlowertransparency)- [aroon.upper.color](#aroonuppercolor)- [aroon.upper.display](#aroonupperdisplay)- [aroon.upper.linestyle](#aroonupperlinestyle)- [aroon.upper.linewidth](#aroonupperlinewidth)- [aroon.upper.plottype](#aroonupperplottype)- [aroon.upper.trackprice](#aroonuppertrackprice)- [aroon.upper.transparency](#aroonuppertransparency)- [average directional index.adx smoothing](#average-directional-indexadx-smoothing)- [average directional index.adx.color](#average-directional-indexadxcolor)- [average directional index.adx.display](#average-directional-indexadxdisplay)- [average directional index.adx.linestyle](#average-directional-indexadxlinestyle)- [average directional index.adx.linewidth](#average-directional-indexadxlinewidth)- [average directional index.adx.plottype](#average-directional-indexadxplottype)- [average directional index.adx.trackprice](#average-directional-indexadxtrackprice)- [average directional index.adx.transparency](#average-directional-indexadxtransparency)- [average directional index.di length](#average-directional-indexdi-length)- [average price.other symbol](#average-priceother-symbol)- [average price.plot.color](#average-priceplotcolor)- [average price.plot.display](#average-priceplotdisplay)- [average price.plot.linestyle](#average-priceplotlinestyle)- [average price.plot.linewidth](#average-priceplotlinewidth)- [average price.plot.plottype](#average-priceplotplottype)- [average price.plot.trackprice](#average-priceplottrackprice)- [average price.plot.transparency](#average-priceplottransparency)- [average true range.length](#average-true-rangelength)- [average true range.plot.color](#average-true-rangeplotcolor)- [average true range.plot.display](#average-true-rangeplotdisplay)- [average true range.plot.linestyle](#average-true-rangeplotlinestyle)- [average true range.plot.linewidth](#average-true-rangeplotlinewidth)- [average true range.plot.plottype](#average-true-rangeplotplottype)- [average true range.plot.trackprice](#average-true-rangeplottrackprice)- [average true range.plot.transparency](#average-true-rangeplottransparency)- [awesome oscillator.plot.color](#awesome-oscillatorplotcolor)- [awesome oscillator.plot.display](#awesome-oscillatorplotdisplay)- [awesome oscillator.plot.linestyle](#awesome-oscillatorplotlinestyle)- [awesome oscillator.plot.linewidth](#awesome-oscillatorplotlinewidth)- [awesome oscillator.plot.plottype](#awesome-oscillatorplotplottype)- [awesome oscillator.plot.trackprice](#awesome-oscillatorplottrackprice)- [awesome oscillator.plot.transparency](#awesome-oscillatorplottransparency)- [balance of power.plot.color](#balance-of-powerplotcolor)- [balance of power.plot.display](#balance-of-powerplotdisplay)- [balance of power.plot.linestyle](#balance-of-powerplotlinestyle)- [balance of power.plot.linewidth](#balance-of-powerplotlinewidth)- [balance of power.plot.plottype](#balance-of-powerplotplottype)- [balance of power.plot.trackprice](#balance-of-powerplottrackprice)- [balance of power.plot.transparency](#balance-of-powerplottransparency)- [barStyle.barColorsOnPrevClose](#barstylebarcolorsonprevclose)- [barStyle.dontDrawOpen](#barstyledontdrawopen)- [barStyle.downColor](#barstyledowncolor)- [barStyle.thinBars](#barstylethinbars)- [barStyle.upColor](#barstyleupcolor)- [baselineStyle.baseLevelPercentage](#baselinestylebaselevelpercentage)- [baselineStyle.baselineColor](#baselinestylebaselinecolor)- [baselineStyle.bottomFillColor1](#baselinestylebottomfillcolor1)- [baselineStyle.bottomFillColor2](#baselinestylebottomfillcolor2)- [baselineStyle.bottomLineColor](#baselinestylebottomlinecolor)- [baselineStyle.bottomLineWidth](#baselinestylebottomlinewidth)- [baselineStyle.topFillColor1](#baselinestyletopfillcolor1)- [baselineStyle.topFillColor2](#baselinestyletopfillcolor2)- [baselineStyle.topLineColor](#baselinestyletoplinecolor)- [baselineStyle.topLineWidth](#baselinestyletoplinewidth)- [baselineStyle.transparency](#baselinestyletransparency)- [bollinger bands %b.hlines background.color](#bollinger-bands-bhlines-backgroundcolor)- [bollinger bands %b.hlines background.transparency](#bollinger-bands-bhlines-backgroundtransparency)- [bollinger bands %b.hlines background.visible](#bollinger-bands-bhlines-backgroundvisible)- [bollinger bands %b.length](#bollinger-bands-blength)- [bollinger bands %b.lowerlimit.color](#bollinger-bands-blowerlimitcolor)- [bollinger bands %b.lowerlimit.linestyle](#bollinger-bands-blowerlimitlinestyle)- [bollinger bands %b.lowerlimit.linewidth](#bollinger-bands-blowerlimitlinewidth)- [bollinger bands %b.lowerlimit.value](#bollinger-bands-blowerlimitvalue)- [bollinger bands %b.lowerlimit.visible](#bollinger-bands-blowerlimitvisible)- [bollinger bands %b.mult](#bollinger-bands-bmult)- [bollinger bands %b.plot.color](#bollinger-bands-bplotcolor)- [bollinger bands %b.plot.linestyle](#bollinger-bands-bplotlinestyle)- [bollinger bands %b.plot.linewidth](#bollinger-bands-bplotlinewidth)- [bollinger bands %b.plot.plottype](#bollinger-bands-bplotplottype)- [bollinger bands %b.plot.trackprice](#bollinger-bands-bplottrackprice)- [bollinger bands %b.plot.transparency](#bollinger-bands-bplottransparency)- [bollinger bands %b.plot.visible](#bollinger-bands-bplotvisible)- [bollinger bands %b.upperlimit.color](#bollinger-bands-bupperlimitcolor)- [bollinger bands %b.upperlimit.linestyle](#bollinger-bands-bupperlimitlinestyle)- [bollinger bands %b.upperlimit.linewidth](#bollinger-bands-bupperlimitlinewidth)- [bollinger bands %b.upperlimit.value](#bollinger-bands-bupperlimitvalue)- [bollinger bands %b.upperlimit.visible](#bollinger-bands-bupperlimitvisible)- [bollinger bands width.length](#bollinger-bands-widthlength)- [bollinger bands width.mult](#bollinger-bands-widthmult)- [bollinger bands width.plot.color](#bollinger-bands-widthplotcolor)- [bollinger bands width.plot.display](#bollinger-bands-widthplotdisplay)- [bollinger bands width.plot.linestyle](#bollinger-bands-widthplotlinestyle)- [bollinger bands width.plot.linewidth](#bollinger-bands-widthplotlinewidth)- [bollinger bands width.plot.plottype](#bollinger-bands-widthplotplottype)- [bollinger bands width.plot.trackprice](#bollinger-bands-widthplottrackprice)- [bollinger bands width.plot.transparency](#bollinger-bands-widthplottransparency)- [bollinger bands.length](#bollinger-bandslength)- [bollinger bands.lower.color](#bollinger-bandslowercolor)- [bollinger bands.lower.linestyle](#bollinger-bandslowerlinestyle)- [bollinger bands.lower.linewidth](#bollinger-bandslowerlinewidth)- [bollinger bands.lower.plottype](#bollinger-bandslowerplottype)- [bollinger bands.lower.trackprice](#bollinger-bandslowertrackprice)- [bollinger bands.lower.transparency](#bollinger-bandslowertransparency)- [bollinger bands.lower.visible](#bollinger-bandslowervisible)- [bollinger bands.median.color](#bollinger-bandsmediancolor)- [bollinger bands.median.linestyle](#bollinger-bandsmedianlinestyle)- [bollinger bands.median.linewidth](#bollinger-bandsmedianlinewidth)- [bollinger bands.median.plottype](#bollinger-bandsmedianplottype)- [bollinger bands.median.trackprice](#bollinger-bandsmediantrackprice)- [bollinger bands.median.transparency](#bollinger-bandsmediantransparency)- [bollinger bands.median.visible](#bollinger-bandsmedianvisible)- [bollinger bands.mult](#bollinger-bandsmult)- [bollinger bands.other symbol](#bollinger-bandsother-symbol)- [bollinger bands.plots background.color](#bollinger-bandsplots-backgroundcolor)- [bollinger bands.plots background.transparency](#bollinger-bandsplots-backgroundtransparency)- [bollinger bands.plots background.visible](#bollinger-bandsplots-backgroundvisible)- [bollinger bands.upper.color](#bollinger-bandsuppercolor)- [bollinger bands.upper.linestyle](#bollinger-bandsupperlinestyle)- [bollinger bands.upper.linewidth](#bollinger-bandsupperlinewidth)- [bollinger bands.upper.plottype](#bollinger-bandsupperplottype)- [bollinger bands.upper.trackprice](#bollinger-bandsuppertrackprice)- [bollinger bands.upper.transparency](#bollinger-bandsuppertransparency)- [bollinger bands.upper.visible](#bollinger-bandsuppervisible)- [candleStyle.barColorsOnPrevClose](#candlestylebarcolorsonprevclose)- [candleStyle.borderColor](#candlestylebordercolor)- [candleStyle.borderDownColor](#candlestyleborderdowncolor)- [candleStyle.borderUpColor](#candlestyleborderupcolor)- [candleStyle.downColor](#candlestyledowncolor)- [candleStyle.drawBody](#candlestyledrawbody)- [candleStyle.drawBorder](#candlestyledrawborder)- [candleStyle.drawWick](#candlestyledrawwick)- [candleStyle.upColor](#candlestyleupcolor)- [candleStyle.wickColor](#candlestylewickcolor)- [candleStyle.wickDownColor](#candlestylewickdowncolor)- [candleStyle.wickUpColor](#candlestylewickupcolor)- [chaikin money flow.length](#chaikin-money-flowlength)- [chaikin money flow.plot.color](#chaikin-money-flowplotcolor)- [chaikin money flow.plot.display](#chaikin-money-flowplotdisplay)- [chaikin money flow.plot.linestyle](#chaikin-money-flowplotlinestyle)- [chaikin money flow.plot.linewidth](#chaikin-money-flowplotlinewidth)- [chaikin money flow.plot.plottype](#chaikin-money-flowplotplottype)- [chaikin money flow.plot.trackprice](#chaikin-money-flowplottrackprice)- [chaikin money flow.plot.transparency](#chaikin-money-flowplottransparency)- [chaikin money flow.zero.color](#chaikin-money-flowzerocolor)- [chaikin money flow.zero.linestyle](#chaikin-money-flowzerolinestyle)- [chaikin money flow.zero.linewidth](#chaikin-money-flowzerolinewidth)- [chaikin money flow.zero.value](#chaikin-money-flowzerovalue)- [chaikin money flow.zero.visible](#chaikin-money-flowzerovisible)- [chaikin oscillator.long](#chaikin-oscillatorlong)- [chaikin oscillator.plot.color](#chaikin-oscillatorplotcolor)- [chaikin oscillator.plot.display](#chaikin-oscillatorplotdisplay)- [chaikin oscillator.plot.linestyle](#chaikin-oscillatorplotlinestyle)- [chaikin oscillator.plot.linewidth](#chaikin-oscillatorplotlinewidth)- [chaikin oscillator.plot.plottype](#chaikin-oscillatorplotplottype)- [chaikin oscillator.plot.trackprice](#chaikin-oscillatorplottrackprice)- [chaikin oscillator.plot.transparency](#chaikin-oscillatorplottransparency)- [chaikin oscillator.short](#chaikin-oscillatorshort)- [chaikin oscillator.zero.color](#chaikin-oscillatorzerocolor)- [chaikin oscillator.zero.linestyle](#chaikin-oscillatorzerolinestyle)- [chaikin oscillator.zero.linewidth](#chaikin-oscillatorzerolinewidth)- [chaikin oscillator.zero.value](#chaikin-oscillatorzerovalue)- [chaikin oscillator.zero.visible](#chaikin-oscillatorzerovisible)- [chaikin volatility.periods](#chaikin-volatilityperiods)- [chaikin volatility.plot.color](#chaikin-volatilityplotcolor)- [chaikin volatility.plot.display](#chaikin-volatilityplotdisplay)- [chaikin volatility.plot.linestyle](#chaikin-volatilityplotlinestyle)- [chaikin volatility.plot.linewidth](#chaikin-volatilityplotlinewidth)- [chaikin volatility.plot.plottype](#chaikin-volatilityplotplottype)- [chaikin volatility.plot.trackprice](#chaikin-volatilityplottrackprice)- [chaikin volatility.plot.transparency](#chaikin-volatilityplottransparency)- [chaikin volatility.rate of change lookback](#chaikin-volatilityrate-of-change-lookback)- [chaikin volatility.zero.color](#chaikin-volatilityzerocolor)- [chaikin volatility.zero.linestyle](#chaikin-volatilityzerolinestyle)- [chaikin volatility.zero.linewidth](#chaikin-volatilityzerolinewidth)- [chaikin volatility.zero.value](#chaikin-volatilityzerovalue)- [chaikin volatility.zero.visible](#chaikin-volatilityzerovisible)- [chande kroll stop.long.color](#chande-kroll-stoplongcolor)- [chande kroll stop.long.display](#chande-kroll-stoplongdisplay)- [chande kroll stop.long.linestyle](#chande-kroll-stoplonglinestyle)- [chande kroll stop.long.linewidth](#chande-kroll-stoplonglinewidth)- [chande kroll stop.long.plottype](#chande-kroll-stoplongplottype)- [chande kroll stop.long.trackprice](#chande-kroll-stoplongtrackprice)- [chande kroll stop.long.transparency](#chande-kroll-stoplongtransparency)- [chande kroll stop.p](#chande-kroll-stopp)- [chande kroll stop.q](#chande-kroll-stopq)- [chande kroll stop.short.color](#chande-kroll-stopshortcolor)- [chande kroll stop.short.display](#chande-kroll-stopshortdisplay)- [chande kroll stop.short.linestyle](#chande-kroll-stopshortlinestyle)- [chande kroll stop.short.linewidth](#chande-kroll-stopshortlinewidth)- [chande kroll stop.short.plottype](#chande-kroll-stopshortplottype)- [chande kroll stop.short.trackprice](#chande-kroll-stopshorttrackprice)- [chande kroll stop.short.transparency](#chande-kroll-stopshorttransparency)- [chande kroll stop.x](#chande-kroll-stopx)- [chande momentum oscillator.length](#chande-momentum-oscillatorlength)- [chande momentum oscillator.plot.color](#chande-momentum-oscillatorplotcolor)- [chande momentum oscillator.plot.display](#chande-momentum-oscillatorplotdisplay)- [chande momentum oscillator.plot.linestyle](#chande-momentum-oscillatorplotlinestyle)- [chande momentum oscillator.plot.linewidth](#chande-momentum-oscillatorplotlinewidth)- [chande momentum oscillator.plot.plottype](#chande-momentum-oscillatorplotplottype)- [chande momentum oscillator.plot.trackprice](#chande-momentum-oscillatorplottrackprice)- [chande momentum oscillator.plot.transparency](#chande-momentum-oscillatorplottransparency)- [chop zone.plot.color](#chop-zoneplotcolor)- [chop zone.plot.display](#chop-zoneplotdisplay)- [chop zone.plot.linestyle](#chop-zoneplotlinestyle)- [chop zone.plot.linewidth](#chop-zoneplotlinewidth)- [chop zone.plot.plottype](#chop-zoneplotplottype)- [chop zone.plot.trackprice](#chop-zoneplottrackprice)- [chop zone.plot.transparency](#chop-zoneplottransparency)- [choppiness index.hlines background.color](#choppiness-indexhlines-backgroundcolor)- [choppiness index.hlines background.transparency](#choppiness-indexhlines-backgroundtransparency)- [choppiness index.hlines background.visible](#choppiness-indexhlines-backgroundvisible)- [choppiness index.length](#choppiness-indexlength)- [choppiness index.lowerlimit.color](#choppiness-indexlowerlimitcolor)- [choppiness index.lowerlimit.linestyle](#choppiness-indexlowerlimitlinestyle)- [choppiness index.lowerlimit.linewidth](#choppiness-indexlowerlimitlinewidth)- [choppiness index.lowerlimit.value](#choppiness-indexlowerlimitvalue)- [choppiness index.lowerlimit.visible](#choppiness-indexlowerlimitvisible)- [choppiness index.plot.color](#choppiness-indexplotcolor)- [choppiness index.plot.display](#choppiness-indexplotdisplay)- [choppiness index.plot.linestyle](#choppiness-indexplotlinestyle)- [choppiness index.plot.linewidth](#choppiness-indexplotlinewidth)- [choppiness index.plot.plottype](#choppiness-indexplotplottype)- [choppiness index.plot.trackprice](#choppiness-indexplottrackprice)- [choppiness index.plot.transparency](#choppiness-indexplottransparency)- [choppiness index.upperlimit.color](#choppiness-indexupperlimitcolor)- [choppiness index.upperlimit.linestyle](#choppiness-indexupperlimitlinestyle)- [choppiness index.upperlimit.linewidth](#choppiness-indexupperlimitlinewidth)- [choppiness index.upperlimit.value](#choppiness-indexupperlimitvalue)- [choppiness index.upperlimit.visible](#choppiness-indexupperlimitvisible)- [columnStyle.barColorsOnPrevClose](#columnstylebarcolorsonprevclose)- [columnStyle.baselinePosition](#columnstylebaselineposition)- [columnStyle.downColor](#columnstyledowncolor)- [columnStyle.upColor](#columnstyleupcolor)- [commodity channel index.hlines background.color](#commodity-channel-indexhlines-backgroundcolor)- [commodity channel index.hlines background.transparency](#commodity-channel-indexhlines-backgroundtransparency)- [commodity channel index.hlines background.visible](#commodity-channel-indexhlines-backgroundvisible)- [commodity channel index.length](#commodity-channel-indexlength)- [commodity channel index.lowerlimit.color](#commodity-channel-indexlowerlimitcolor)- [commodity channel index.lowerlimit.linestyle](#commodity-channel-indexlowerlimitlinestyle)- [commodity channel index.lowerlimit.linewidth](#commodity-channel-indexlowerlimitlinewidth)- [commodity channel index.lowerlimit.value](#commodity-channel-indexlowerlimitvalue)- [commodity channel index.lowerlimit.visible](#commodity-channel-indexlowerlimitvisible)- [commodity channel index.plot.color](#commodity-channel-indexplotcolor)- [commodity channel index.plot.display](#commodity-channel-indexplotdisplay)- [commodity channel index.plot.linestyle](#commodity-channel-indexplotlinestyle)- [commodity channel index.plot.linewidth](#commodity-channel-indexplotlinewidth)- [commodity channel index.plot.plottype](#commodity-channel-indexplotplottype)- [commodity channel index.plot.trackprice](#commodity-channel-indexplottrackprice)- [commodity channel index.plot.transparency](#commodity-channel-indexplottransparency)- [commodity channel index.smoothed ma.display](#commodity-channel-indexsmoothed-madisplay)- [commodity channel index.smoothed ma.linestyle](#commodity-channel-indexsmoothed-malinestyle)- [commodity channel index.smoothed ma.linewidth](#commodity-channel-indexsmoothed-malinewidth)- [commodity channel index.smoothed ma.plottype](#commodity-channel-indexsmoothed-maplottype)- [commodity channel index.smoothed ma.trackprice](#commodity-channel-indexsmoothed-matrackprice)- [commodity channel index.smoothed ma.transparency](#commodity-channel-indexsmoothed-matransparency)- [commodity channel index.smoothing length](#commodity-channel-indexsmoothing-length)- [commodity channel index.smoothing line](#commodity-channel-indexsmoothing-line)- [commodity channel index.upperlimit.color](#commodity-channel-indexupperlimitcolor)- [commodity channel index.upperlimit.linestyle](#commodity-channel-indexupperlimitlinestyle)- [commodity channel index.upperlimit.linewidth](#commodity-channel-indexupperlimitlinewidth)- [commodity channel index.upperlimit.value](#commodity-channel-indexupperlimitvalue)- [commodity channel index.upperlimit.visible](#commodity-channel-indexupperlimitvisible)- [compare.plot.color](#compareplotcolor)- [compare.plot.display](#compareplotdisplay)- [compare.plot.linestyle](#compareplotlinestyle)- [compare.plot.linewidth](#compareplotlinewidth)- [compare.plot.plottype](#compareplotplottype)- [compare.plot.trackprice](#compareplottrackprice)- [compare.plot.transparency](#compareplottransparency)- [compare.source](#comparesource)- [compare.symbol](#comparesymbol)- [connors rsi.crsi.color](#connors-rsicrsicolor)- [connors rsi.crsi.display](#connors-rsicrsidisplay)- [connors rsi.crsi.linestyle](#connors-rsicrsilinestyle)- [connors rsi.crsi.linewidth](#connors-rsicrsilinewidth)- [connors rsi.crsi.plottype](#connors-rsicrsiplottype)- [connors rsi.crsi.trackprice](#connors-rsicrsitrackprice)- [connors rsi.crsi.transparency](#connors-rsicrsitransparency)- [connors rsi.hlines background.color](#connors-rsihlines-backgroundcolor)- [connors rsi.hlines background.transparency](#connors-rsihlines-backgroundtransparency)- [connors rsi.hlines background.visible](#connors-rsihlines-backgroundvisible)- [connors rsi.lowerlimit.color](#connors-rsilowerlimitcolor)- [connors rsi.lowerlimit.linestyle](#connors-rsilowerlimitlinestyle)- [connors rsi.lowerlimit.linewidth](#connors-rsilowerlimitlinewidth)- [connors rsi.lowerlimit.value](#connors-rsilowerlimitvalue)- [connors rsi.lowerlimit.visible](#connors-rsilowerlimitvisible)- [connors rsi.roc length](#connors-rsiroc-length)- [connors rsi.rsi length](#connors-rsirsi-length)- [connors rsi.updown length](#connors-rsiupdown-length)- [connors rsi.upperlimit.color](#connors-rsiupperlimitcolor)- [connors rsi.upperlimit.linestyle](#connors-rsiupperlimitlinestyle)- [connors rsi.upperlimit.linewidth](#connors-rsiupperlimitlinewidth)- [connors rsi.upperlimit.value](#connors-rsiupperlimitvalue)- [connors rsi.upperlimit.visible](#connors-rsiupperlimitvisible)- [coppock curve.long roc length](#coppock-curvelong-roc-length)- [coppock curve.plot.color](#coppock-curveplotcolor)- [coppock curve.plot.display](#coppock-curveplotdisplay)- [coppock curve.plot.linestyle](#coppock-curveplotlinestyle)- [coppock curve.plot.linewidth](#coppock-curveplotlinewidth)- [coppock curve.plot.plottype](#coppock-curveplotplottype)- [coppock curve.plot.trackprice](#coppock-curveplottrackprice)- [coppock curve.plot.transparency](#coppock-curveplottransparency)- [coppock curve.short roc length](#coppock-curveshort-roc-length)- [coppock curve.wma length](#coppock-curvewma-length)- [correlation - log.instrument 1](#correlation---loginstrument-1)- [correlation - log.instrument 2](#correlation---loginstrument-2)- [correlation - log.periods](#correlation---logperiods)- [correlation - log.plot.color](#correlation---logplotcolor)- [correlation - log.plot.display](#correlation---logplotdisplay)- [correlation - log.plot.linestyle](#correlation---logplotlinestyle)- [correlation - log.plot.linewidth](#correlation---logplotlinewidth)- [correlation - log.plot.plottype](#correlation---logplotplottype)- [correlation - log.plot.trackprice](#correlation---logplottrackprice)- [correlation - log.plot.transparency](#correlation---logplottransparency)- [correlation coefficient.length](#correlation-coefficientlength)- [correlation coefficient.plot.color](#correlation-coefficientplotcolor)- [correlation coefficient.plot.display](#correlation-coefficientplotdisplay)- [correlation coefficient.plot.linestyle](#correlation-coefficientplotlinestyle)- [correlation coefficient.plot.linewidth](#correlation-coefficientplotlinewidth)- [correlation coefficient.plot.plottype](#correlation-coefficientplotplottype)- [correlation coefficient.plot.trackprice](#correlation-coefficientplottrackprice)- [correlation coefficient.plot.transparency](#correlation-coefficientplottransparency)- [correlation coefficient.sym](#correlation-coefficientsym)- [detrended price oscillator.dpo.color](#detrended-price-oscillatordpocolor)- [detrended price oscillator.dpo.display](#detrended-price-oscillatordpodisplay)- [detrended price oscillator.dpo.linestyle](#detrended-price-oscillatordpolinestyle)- [detrended price oscillator.dpo.linewidth](#detrended-price-oscillatordpolinewidth)- [detrended price oscillator.dpo.plottype](#detrended-price-oscillatordpoplottype)- [detrended price oscillator.dpo.trackprice](#detrended-price-oscillatordpotrackprice)- [detrended price oscillator.dpo.transparency](#detrended-price-oscillatordpotransparency)- [detrended price oscillator.iscentered](#detrended-price-oscillatoriscentered)- [detrended price oscillator.period](#detrended-price-oscillatorperiod)- [detrended price oscillator.zero.color](#detrended-price-oscillatorzerocolor)- [detrended price oscillator.zero.linestyle](#detrended-price-oscillatorzerolinestyle)- [detrended price oscillator.zero.linewidth](#detrended-price-oscillatorzerolinewidth)- [detrended price oscillator.zero.value](#detrended-price-oscillatorzerovalue)- [detrended price oscillator.zero.visible](#detrended-price-oscillatorzerovisible)- [directional movement.+di.color](#directional-movementdicolor)- [directional movement.+di.display](#directional-movementdidisplay)- [directional movement.+di.linestyle](#directional-movementdilinestyle)- [directional movement.+di.linewidth](#directional-movementdilinewidth)- [directional movement.+di.plottype](#directional-movementdiplottype)- [directional movement.+di.trackprice](#directional-movementditrackprice)- [directional movement.+di.transparency](#directional-movementditransparency)- [directional movement.-di.color](#directional-movement-dicolor)- [directional movement.-di.display](#directional-movement-didisplay)- [directional movement.-di.linestyle](#directional-movement-dilinestyle)- [directional movement.-di.linewidth](#directional-movement-dilinewidth)- [directional movement.-di.plottype](#directional-movement-diplottype)- [directional movement.-di.trackprice](#directional-movement-ditrackprice)- [directional movement.-di.transparency](#directional-movement-ditransparency)- [directional movement.adx smoothing](#directional-movementadx-smoothing)- [directional movement.adx.color](#directional-movementadxcolor)- [directional movement.adx.display](#directional-movementadxdisplay)- [directional movement.adx.linestyle](#directional-movementadxlinestyle)- [directional movement.adx.linewidth](#directional-movementadxlinewidth)- [directional movement.adx.plottype](#directional-movementadxplottype)- [directional movement.adx.trackprice](#directional-movementadxtrackprice)- [directional movement.adx.transparency](#directional-movementadxtransparency)- [directional movement.adxr.color](#directional-movementadxrcolor)- [directional movement.adxr.display](#directional-movementadxrdisplay)- [directional movement.adxr.linestyle](#directional-movementadxrlinestyle)- [directional movement.adxr.linewidth](#directional-movementadxrlinewidth)- [directional movement.adxr.plottype](#directional-movementadxrplottype)- [directional movement.adxr.trackprice](#directional-movementadxrtrackprice)- [directional movement.adxr.transparency](#directional-movementadxrtransparency)- [directional movement.di length](#directional-movementdi-length)- [directional movement.dx.color](#directional-movementdxcolor)- [directional movement.dx.display](#directional-movementdxdisplay)- [directional movement.dx.linestyle](#directional-movementdxlinestyle)- [directional movement.dx.linewidth](#directional-movementdxlinewidth)- [directional movement.dx.plottype](#directional-movementdxplottype)- [directional movement.dx.trackprice](#directional-movementdxtrackprice)- [directional movement.dx.transparency](#directional-movementdxtransparency)- [donchian channels.basis.color](#donchian-channelsbasiscolor)- [donchian channels.basis.display](#donchian-channelsbasisdisplay)- [donchian channels.basis.linestyle](#donchian-channelsbasislinestyle)- [donchian channels.basis.linewidth](#donchian-channelsbasislinewidth)- [donchian channels.basis.plottype](#donchian-channelsbasisplottype)- [donchian channels.basis.trackprice](#donchian-channelsbasistrackprice)- [donchian channels.basis.transparency](#donchian-channelsbasistransparency)- [donchian channels.length](#donchian-channelslength)- [donchian channels.lower.color](#donchian-channelslowercolor)- [donchian channels.lower.display](#donchian-channelslowerdisplay)- [donchian channels.lower.linestyle](#donchian-channelslowerlinestyle)- [donchian channels.lower.linewidth](#donchian-channelslowerlinewidth)- [donchian channels.lower.plottype](#donchian-channelslowerplottype)- [donchian channels.lower.trackprice](#donchian-channelslowertrackprice)- [donchian channels.lower.transparency](#donchian-channelslowertransparency)- [donchian channels.offset](#donchian-channelsoffset)- [donchian channels.plots background.color](#donchian-channelsplots-backgroundcolor)- [donchian channels.plots background.transparency](#donchian-channelsplots-backgroundtransparency)- [donchian channels.plots background.visible](#donchian-channelsplots-backgroundvisible)- [donchian channels.upper.color](#donchian-channelsuppercolor)- [donchian channels.upper.display](#donchian-channelsupperdisplay)- [donchian channels.upper.linestyle](#donchian-channelsupperlinestyle)- [donchian channels.upper.linewidth](#donchian-channelsupperlinewidth)- [donchian channels.upper.plottype](#donchian-channelsupperplottype)- [donchian channels.upper.trackprice](#donchian-channelsuppertrackprice)- [donchian channels.upper.transparency](#donchian-channelsuppertransparency)- [double ema.length](#double-emalength)- [double ema.plot.color](#double-emaplotcolor)- [double ema.plot.display](#double-emaplotdisplay)- [double ema.plot.linestyle](#double-emaplotlinestyle)- [double ema.plot.linewidth](#double-emaplotlinewidth)- [double ema.plot.plottype](#double-emaplotplottype)- [double ema.plot.trackprice](#double-emaplottrackprice)- [double ema.plot.transparency](#double-emaplottransparency)- [ease of movement.divisor](#ease-of-movementdivisor)- [ease of movement.length](#ease-of-movementlength)- [ease of movement.plot.color](#ease-of-movementplotcolor)- [ease of movement.plot.display](#ease-of-movementplotdisplay)- [ease of movement.plot.linestyle](#ease-of-movementplotlinestyle)- [ease of movement.plot.linewidth](#ease-of-movementplotlinewidth)- [ease of movement.plot.plottype](#ease-of-movementplotplottype)- [ease of movement.plot.trackprice](#ease-of-movementplottrackprice)- [ease of movement.plot.transparency](#ease-of-movementplottransparency)- [elder's force index.length](#elders-force-indexlength)- [elder's force index.plot.color](#elders-force-indexplotcolor)- [elder's force index.plot.display](#elders-force-indexplotdisplay)- [elder's force index.plot.linestyle](#elders-force-indexplotlinestyle)- [elder's force index.plot.linewidth](#elders-force-indexplotlinewidth)- [elder's force index.plot.plottype](#elders-force-indexplotplottype)- [elder's force index.plot.trackprice](#elders-force-indexplottrackprice)- [elder's force index.plot.transparency](#elders-force-indexplottransparency)- [elder's force index.zero.color](#elders-force-indexzerocolor)- [elder's force index.zero.linestyle](#elders-force-indexzerolinestyle)- [elder's force index.zero.linewidth](#elders-force-indexzerolinewidth)- [elder's force index.zero.value](#elders-force-indexzerovalue)- [elder's force index.zero.visible](#elders-force-indexzerovisible)- [ema cross.crosses.color](#ema-crosscrossescolor)- [ema cross.crosses.display](#ema-crosscrossesdisplay)- [ema cross.crosses.linestyle](#ema-crosscrosseslinestyle)- [ema cross.crosses.linewidth](#ema-crosscrosseslinewidth)- [ema cross.crosses.plottype](#ema-crosscrossesplottype)- [ema cross.crosses.trackprice](#ema-crosscrossestrackprice)- [ema cross.crosses.transparency](#ema-crosscrossestransparency)- [ema cross.long](#ema-crosslong)- [ema cross.long.color](#ema-crosslongcolor)- [ema cross.long.display](#ema-crosslongdisplay)- [ema cross.long.linestyle](#ema-crosslonglinestyle)- [ema cross.long.linewidth](#ema-crosslonglinewidth)- [ema cross.long.plottype](#ema-crosslongplottype)- [ema cross.long.trackprice](#ema-crosslongtrackprice)- [ema cross.long.transparency](#ema-crosslongtransparency)- [ema cross.short](#ema-crossshort)- [ema cross.short.color](#ema-crossshortcolor)- [ema cross.short.display](#ema-crossshortdisplay)- [ema cross.short.linestyle](#ema-crossshortlinestyle)- [ema cross.short.linewidth](#ema-crossshortlinewidth)- [ema cross.short.plottype](#ema-crossshortplottype)- [ema cross.short.trackprice](#ema-crossshorttrackprice)- [ema cross.short.transparency](#ema-crossshorttransparency)- [envelopes.average.color](#envelopesaveragecolor)- [envelopes.average.display](#envelopesaveragedisplay)- [envelopes.average.linestyle](#envelopesaveragelinestyle)- [envelopes.average.linewidth](#envelopesaveragelinewidth)- [envelopes.average.plottype](#envelopesaverageplottype)- [envelopes.average.trackprice](#envelopesaveragetrackprice)- [envelopes.average.transparency](#envelopesaveragetransparency)- [envelopes.length](#envelopeslength)- [envelopes.lower percentage](#envelopeslower-percentage)- [envelopes.lower.color](#envelopeslowercolor)- [envelopes.lower.display](#envelopeslowerdisplay)- [envelopes.lower.linestyle](#envelopeslowerlinestyle)- [envelopes.lower.linewidth](#envelopeslowerlinewidth)- [envelopes.lower.plottype](#envelopeslowerplottype)- [envelopes.lower.trackprice](#envelopeslowertrackprice)- [envelopes.lower.transparency](#envelopeslowertransparency)- [envelopes.method](#envelopesmethod)- [envelopes.plots background.color](#envelopesplots-backgroundcolor)- [envelopes.plots background.transparency](#envelopesplots-backgroundtransparency)- [envelopes.plots background.visible](#envelopesplots-backgroundvisible)- [envelopes.source](#envelopessource)- [envelopes.upper percentage](#envelopesupper-percentage)- [envelopes.upper.color](#envelopesuppercolor)- [envelopes.upper.display](#envelopesupperdisplay)- [envelopes.upper.linestyle](#envelopesupperlinestyle)- [envelopes.upper.linewidth](#envelopesupperlinewidth)- [envelopes.upper.plottype](#envelopesupperplottype)- [envelopes.upper.trackprice](#envelopesuppertrackprice)- [envelopes.upper.transparency](#envelopesuppertransparency)- [fisher transform.fisher.color](#fisher-transformfishercolor)- [fisher transform.fisher.display](#fisher-transformfisherdisplay)- [fisher transform.fisher.linestyle](#fisher-transformfisherlinestyle)- [fisher transform.fisher.linewidth](#fisher-transformfisherlinewidth)- [fisher transform.fisher.plottype](#fisher-transformfisherplottype)- [fisher transform.fisher.trackprice](#fisher-transformfishertrackprice)- [fisher transform.fisher.transparency](#fisher-transformfishertransparency)- [fisher transform.length](#fisher-transformlength)- [fisher transform.level.color](#fisher-transformlevelcolor)- [fisher transform.level.linestyle](#fisher-transformlevellinestyle)- [fisher transform.level.linewidth](#fisher-transformlevellinewidth)- [fisher transform.level.value](#fisher-transformlevelvalue)- [fisher transform.level.visible](#fisher-transformlevelvisible)- [fisher transform.trigger.color](#fisher-transformtriggercolor)- [fisher transform.trigger.display](#fisher-transformtriggerdisplay)- [fisher transform.trigger.linestyle](#fisher-transformtriggerlinestyle)- [fisher transform.trigger.linewidth](#fisher-transformtriggerlinewidth)- [fisher transform.trigger.plottype](#fisher-transformtriggerplottype)- [fisher transform.trigger.trackprice](#fisher-transformtriggertrackprice)- [fisher transform.trigger.transparency](#fisher-transformtriggertransparency)- [fixed range.developing poc.color](#fixed-rangedeveloping-poccolor)- [fixed range.developing poc.display](#fixed-rangedeveloping-pocdisplay)- [fixed range.developing poc.linestyle](#fixed-rangedeveloping-poclinestyle)- [fixed range.developing poc.linewidth](#fixed-rangedeveloping-poclinewidth)- [fixed range.developing poc.plottype](#fixed-rangedeveloping-pocplottype)- [fixed range.developing poc.trackprice](#fixed-rangedeveloping-poctrackprice)- [fixed range.developing poc.transparency](#fixed-rangedeveloping-poctransparency)- [fixed range.developing va high.color](#fixed-rangedeveloping-va-highcolor)- [fixed range.developing va high.display](#fixed-rangedeveloping-va-highdisplay)- [fixed range.developing va high.linestyle](#fixed-rangedeveloping-va-highlinestyle)- [fixed range.developing va high.linewidth](#fixed-rangedeveloping-va-highlinewidth)- [fixed range.developing va high.plottype](#fixed-rangedeveloping-va-highplottype)- [fixed range.developing va high.trackprice](#fixed-rangedeveloping-va-hightrackprice)- [fixed range.developing va high.transparency](#fixed-rangedeveloping-va-hightransparency)- [fixed range.developing va low.color](#fixed-rangedeveloping-va-lowcolor)- [fixed range.developing va low.display](#fixed-rangedeveloping-va-lowdisplay)- [fixed range.developing va low.linestyle](#fixed-rangedeveloping-va-lowlinestyle)- [fixed range.developing va low.linewidth](#fixed-rangedeveloping-va-lowlinewidth)- [fixed range.developing va low.plottype](#fixed-rangedeveloping-va-lowplottype)- [fixed range.developing va low.trackprice](#fixed-rangedeveloping-va-lowtrackprice)- [fixed range.developing va low.transparency](#fixed-rangedeveloping-va-lowtransparency)- [fixed range.first bar time](#fixed-rangefirst-bar-time)- [fixed range.last bar time](#fixed-rangelast-bar-time)- [fixed range.row size](#fixed-rangerow-size)- [fixed range.rows layout](#fixed-rangerows-layout)- [fixed range.subscriberealtime](#fixed-rangesubscriberealtime)- [fixed range.value area volume](#fixed-rangevalue-area-volume)- [fixed range.volume](#fixed-rangevolume)- [guppy multiple moving average.investor ema 1 length](#guppy-multiple-moving-averageinvestor-ema-1-length)- [guppy multiple moving average.investor ema 1.color](#guppy-multiple-moving-averageinvestor-ema-1color)- [guppy multiple moving average.investor ema 1.display](#guppy-multiple-moving-averageinvestor-ema-1display)- [guppy multiple moving average.investor ema 1.linestyle](#guppy-multiple-moving-averageinvestor-ema-1linestyle)- [guppy multiple moving average.investor ema 1.linewidth](#guppy-multiple-moving-averageinvestor-ema-1linewidth)- [guppy multiple moving average.investor ema 1.plottype](#guppy-multiple-moving-averageinvestor-ema-1plottype)- [guppy multiple moving average.investor ema 1.trackprice](#guppy-multiple-moving-averageinvestor-ema-1trackprice)- [guppy multiple moving average.investor ema 1.transparency](#guppy-multiple-moving-averageinvestor-ema-1transparency)- [guppy multiple moving average.investor ema 2 length](#guppy-multiple-moving-averageinvestor-ema-2-length)- [guppy multiple moving average.investor ema 2.color](#guppy-multiple-moving-averageinvestor-ema-2color)- [guppy multiple moving average.investor ema 2.display](#guppy-multiple-moving-averageinvestor-ema-2display)- [guppy multiple moving average.investor ema 2.linestyle](#guppy-multiple-moving-averageinvestor-ema-2linestyle)- [guppy multiple moving average.investor ema 2.linewidth](#guppy-multiple-moving-averageinvestor-ema-2linewidth)- [guppy multiple moving average.investor ema 2.plottype](#guppy-multiple-moving-averageinvestor-ema-2plottype)- [guppy multiple moving average.investor ema 2.trackprice](#guppy-multiple-moving-averageinvestor-ema-2trackprice)- [guppy multiple moving average.investor ema 2.transparency](#guppy-multiple-moving-averageinvestor-ema-2transparency)- [guppy multiple moving average.investor ema 3 length](#guppy-multiple-moving-averageinvestor-ema-3-length)- [guppy multiple moving average.investor ema 3.color](#guppy-multiple-moving-averageinvestor-ema-3color)- [guppy multiple moving average.investor ema 3.display](#guppy-multiple-moving-averageinvestor-ema-3display)- [guppy multiple moving average.investor ema 3.linestyle](#guppy-multiple-moving-averageinvestor-ema-3linestyle)- [guppy multiple moving average.investor ema 3.linewidth](#guppy-multiple-moving-averageinvestor-ema-3linewidth)- [guppy multiple moving average.investor ema 3.plottype](#guppy-multiple-moving-averageinvestor-ema-3plottype)- [guppy multiple moving average.investor ema 3.trackprice](#guppy-multiple-moving-averageinvestor-ema-3trackprice)- [guppy multiple moving average.investor ema 3.transparency](#guppy-multiple-moving-averageinvestor-ema-3transparency)- [guppy multiple moving average.investor ema 4 length](#guppy-multiple-moving-averageinvestor-ema-4-length)- [guppy multiple moving average.investor ema 4.color](#guppy-multiple-moving-averageinvestor-ema-4color)- [guppy multiple moving average.investor ema 4.display](#guppy-multiple-moving-averageinvestor-ema-4display)- [guppy multiple moving average.investor ema 4.linestyle](#guppy-multiple-moving-averageinvestor-ema-4linestyle)- [guppy multiple moving average.investor ema 4.linewidth](#guppy-multiple-moving-averageinvestor-ema-4linewidth)- [guppy multiple moving average.investor ema 4.plottype](#guppy-multiple-moving-averageinvestor-ema-4plottype)- [guppy multiple moving average.investor ema 4.trackprice](#guppy-multiple-moving-averageinvestor-ema-4trackprice)- [guppy multiple moving average.investor ema 4.transparency](#guppy-multiple-moving-averageinvestor-ema-4transparency)- [guppy multiple moving average.investor ema 5 length](#guppy-multiple-moving-averageinvestor-ema-5-length)- [guppy multiple moving average.investor ema 5.color](#guppy-multiple-moving-averageinvestor-ema-5color)- [guppy multiple moving average.investor ema 5.display](#guppy-multiple-moving-averageinvestor-ema-5display)- [guppy multiple moving average.investor ema 5.linestyle](#guppy-multiple-moving-averageinvestor-ema-5linestyle)- [guppy multiple moving average.investor ema 5.linewidth](#guppy-multiple-moving-averageinvestor-ema-5linewidth)- [guppy multiple moving average.investor ema 5.plottype](#guppy-multiple-moving-averageinvestor-ema-5plottype)- [guppy multiple moving average.investor ema 5.trackprice](#guppy-multiple-moving-averageinvestor-ema-5trackprice)- [guppy multiple moving average.investor ema 5.transparency](#guppy-multiple-moving-averageinvestor-ema-5transparency)- [guppy multiple moving average.investor ema 6 length](#guppy-multiple-moving-averageinvestor-ema-6-length)- [guppy multiple moving average.investor ema 6.color](#guppy-multiple-moving-averageinvestor-ema-6color)- [guppy multiple moving average.investor ema 6.display](#guppy-multiple-moving-averageinvestor-ema-6display)- [guppy multiple moving average.investor ema 6.linestyle](#guppy-multiple-moving-averageinvestor-ema-6linestyle)- [guppy multiple moving average.investor ema 6.linewidth](#guppy-multiple-moving-averageinvestor-ema-6linewidth)- [guppy multiple moving average.investor ema 6.plottype](#guppy-multiple-moving-averageinvestor-ema-6plottype)- [guppy multiple moving average.investor ema 6.trackprice](#guppy-multiple-moving-averageinvestor-ema-6trackprice)- [guppy multiple moving average.investor ema 6.transparency](#guppy-multiple-moving-averageinvestor-ema-6transparency)- [guppy multiple moving average.trader ema 1 length](#guppy-multiple-moving-averagetrader-ema-1-length)- [guppy multiple moving average.trader ema 1.color](#guppy-multiple-moving-averagetrader-ema-1color)- [guppy multiple moving average.trader ema 1.display](#guppy-multiple-moving-averagetrader-ema-1display)- [guppy multiple moving average.trader ema 1.linestyle](#guppy-multiple-moving-averagetrader-ema-1linestyle)- [guppy multiple moving average.trader ema 1.linewidth](#guppy-multiple-moving-averagetrader-ema-1linewidth)- [guppy multiple moving average.trader ema 1.plottype](#guppy-multiple-moving-averagetrader-ema-1plottype)- [guppy multiple moving average.trader ema 1.trackprice](#guppy-multiple-moving-averagetrader-ema-1trackprice)- [guppy multiple moving average.trader ema 1.transparency](#guppy-multiple-moving-averagetrader-ema-1transparency)- [guppy multiple moving average.trader ema 2 length](#guppy-multiple-moving-averagetrader-ema-2-length)- [guppy multiple moving average.trader ema 2.color](#guppy-multiple-moving-averagetrader-ema-2color)- [guppy multiple moving average.trader ema 2.display](#guppy-multiple-moving-averagetrader-ema-2display)- [guppy multiple moving average.trader ema 2.linestyle](#guppy-multiple-moving-averagetrader-ema-2linestyle)- [guppy multiple moving average.trader ema 2.linewidth](#guppy-multiple-moving-averagetrader-ema-2linewidth)- [guppy multiple moving average.trader ema 2.plottype](#guppy-multiple-moving-averagetrader-ema-2plottype)- [guppy multiple moving average.trader ema 2.trackprice](#guppy-multiple-moving-averagetrader-ema-2trackprice)- [guppy multiple moving average.trader ema 2.transparency](#guppy-multiple-moving-averagetrader-ema-2transparency)- [guppy multiple moving average.trader ema 3 length](#guppy-multiple-moving-averagetrader-ema-3-length)- [guppy multiple moving average.trader ema 3.color](#guppy-multiple-moving-averagetrader-ema-3color)- [guppy multiple moving average.trader ema 3.display](#guppy-multiple-moving-averagetrader-ema-3display)- [guppy multiple moving average.trader ema 3.linestyle](#guppy-multiple-moving-averagetrader-ema-3linestyle)- [guppy multiple moving average.trader ema 3.linewidth](#guppy-multiple-moving-averagetrader-ema-3linewidth)- [guppy multiple moving average.trader ema 3.plottype](#guppy-multiple-moving-averagetrader-ema-3plottype)- [guppy multiple moving average.trader ema 3.trackprice](#guppy-multiple-moving-averagetrader-ema-3trackprice)- [guppy multiple moving average.trader ema 3.transparency](#guppy-multiple-moving-averagetrader-ema-3transparency)- [guppy multiple moving average.trader ema 4 length](#guppy-multiple-moving-averagetrader-ema-4-length)- [guppy multiple moving average.trader ema 4.color](#guppy-multiple-moving-averagetrader-ema-4color)- [guppy multiple moving average.trader ema 4.display](#guppy-multiple-moving-averagetrader-ema-4display)- [guppy multiple moving average.trader ema 4.linestyle](#guppy-multiple-moving-averagetrader-ema-4linestyle)- [guppy multiple moving average.trader ema 4.linewidth](#guppy-multiple-moving-averagetrader-ema-4linewidth)- [guppy multiple moving average.trader ema 4.plottype](#guppy-multiple-moving-averagetrader-ema-4plottype)- [guppy multiple moving average.trader ema 4.trackprice](#guppy-multiple-moving-averagetrader-ema-4trackprice)- [guppy multiple moving average.trader ema 4.transparency](#guppy-multiple-moving-averagetrader-ema-4transparency)- [guppy multiple moving average.trader ema 5 length](#guppy-multiple-moving-averagetrader-ema-5-length)- [guppy multiple moving average.trader ema 5.color](#guppy-multiple-moving-averagetrader-ema-5color)- [guppy multiple moving average.trader ema 5.display](#guppy-multiple-moving-averagetrader-ema-5display)- [guppy multiple moving average.trader ema 5.linestyle](#guppy-multiple-moving-averagetrader-ema-5linestyle)- [guppy multiple moving average.trader ema 5.linewidth](#guppy-multiple-moving-averagetrader-ema-5linewidth)- [guppy multiple moving average.trader ema 5.plottype](#guppy-multiple-moving-averagetrader-ema-5plottype)- [guppy multiple moving average.trader ema 5.trackprice](#guppy-multiple-moving-averagetrader-ema-5trackprice)- [guppy multiple moving average.trader ema 5.transparency](#guppy-multiple-moving-averagetrader-ema-5transparency)- [guppy multiple moving average.trader ema 6 length](#guppy-multiple-moving-averagetrader-ema-6-length)- [guppy multiple moving average.trader ema 6.color](#guppy-multiple-moving-averagetrader-ema-6color)- [guppy multiple moving average.trader ema 6.display](#guppy-multiple-moving-averagetrader-ema-6display)- [guppy multiple moving average.trader ema 6.linestyle](#guppy-multiple-moving-averagetrader-ema-6linestyle)- [guppy multiple moving average.trader ema 6.linewidth](#guppy-multiple-moving-averagetrader-ema-6linewidth)- [guppy multiple moving average.trader ema 6.plottype](#guppy-multiple-moving-averagetrader-ema-6plottype)- [guppy multiple moving average.trader ema 6.trackprice](#guppy-multiple-moving-averagetrader-ema-6trackprice)- [guppy multiple moving average.trader ema 6.transparency](#guppy-multiple-moving-averagetrader-ema-6transparency)- [hiLoStyle.borderColor](#hilostylebordercolor)- [hiLoStyle.color](#hilostylecolor)- [hiLoStyle.drawBody](#hilostyledrawbody)- [hiLoStyle.labelColor](#hilostylelabelcolor)- [hiLoStyle.showBorders](#hilostyleshowborders)- [hiLoStyle.showLabels](#hilostyleshowlabels)- [historical volatility.length](#historical-volatilitylength)- [historical volatility.plot.color](#historical-volatilityplotcolor)- [historical volatility.plot.display](#historical-volatilityplotdisplay)- [historical volatility.plot.linestyle](#historical-volatilityplotlinestyle)- [historical volatility.plot.linewidth](#historical-volatilityplotlinewidth)- [historical volatility.plot.plottype](#historical-volatilityplotplottype)- [historical volatility.plot.trackprice](#historical-volatilityplottrackprice)- [historical volatility.plot.transparency](#historical-volatilityplottransparency)- [hlcBarsStyle.color](#hlcbarsstylecolor)- [hlcBarsStyle.thinBars](#hlcbarsstylethinbars)- [hull moving average.length](#hull-moving-averagelength)- [hull moving average.plot.color](#hull-moving-averageplotcolor)- [hull moving average.plot.display](#hull-moving-averageplotdisplay)- [hull moving average.plot.linestyle](#hull-moving-averageplotlinestyle)- [hull moving average.plot.linewidth](#hull-moving-averageplotlinewidth)- [hull moving average.plot.plottype](#hull-moving-averageplotplottype)- [hull moving average.plot.trackprice](#hull-moving-averageplottrackprice)- [hull moving average.plot.transparency](#hull-moving-averageplottransparency)- [ichimoku cloud.another symbol](#ichimoku-cloudanother-symbol)- [ichimoku cloud.base line periods](#ichimoku-cloudbase-line-periods)- [ichimoku cloud.base line.color](#ichimoku-cloudbase-linecolor)- [ichimoku cloud.base line.display](#ichimoku-cloudbase-linedisplay)- [ichimoku cloud.base line.linestyle](#ichimoku-cloudbase-linelinestyle)- [ichimoku cloud.base line.linewidth](#ichimoku-cloudbase-linelinewidth)- [ichimoku cloud.base line.plottype](#ichimoku-cloudbase-lineplottype)- [ichimoku cloud.base line.trackprice](#ichimoku-cloudbase-linetrackprice)- [ichimoku cloud.base line.transparency](#ichimoku-cloudbase-linetransparency)- [ichimoku cloud.conversion line periods](#ichimoku-cloudconversion-line-periods)- [ichimoku cloud.conversion line.color](#ichimoku-cloudconversion-linecolor)- [ichimoku cloud.conversion line.display](#ichimoku-cloudconversion-linedisplay)- [ichimoku cloud.conversion line.linestyle](#ichimoku-cloudconversion-linelinestyle)- [ichimoku cloud.conversion line.linewidth](#ichimoku-cloudconversion-linelinewidth)- [ichimoku cloud.conversion line.plottype](#ichimoku-cloudconversion-lineplottype)- [ichimoku cloud.conversion line.trackprice](#ichimoku-cloudconversion-linetrackprice)- [ichimoku cloud.conversion line.transparency](#ichimoku-cloudconversion-linetransparency)- [ichimoku cloud.lagging span periods](#ichimoku-cloudlagging-span-periods)- [ichimoku cloud.lagging span.color](#ichimoku-cloudlagging-spancolor)- [ichimoku cloud.lagging span.display](#ichimoku-cloudlagging-spandisplay)- [ichimoku cloud.lagging span.linestyle](#ichimoku-cloudlagging-spanlinestyle)- [ichimoku cloud.lagging span.linewidth](#ichimoku-cloudlagging-spanlinewidth)- [ichimoku cloud.lagging span.plottype](#ichimoku-cloudlagging-spanplottype)- [ichimoku cloud.lagging span.trackprice](#ichimoku-cloudlagging-spantrackprice)- [ichimoku cloud.lagging span.transparency](#ichimoku-cloudlagging-spantransparency)- [ichimoku cloud.leading shift periods](#ichimoku-cloudleading-shift-periods)- [ichimoku cloud.leading span a.color](#ichimoku-cloudleading-span-acolor)- [ichimoku cloud.leading span a.display](#ichimoku-cloudleading-span-adisplay)- [ichimoku cloud.leading span a.linestyle](#ichimoku-cloudleading-span-alinestyle)- [ichimoku cloud.leading span a.linewidth](#ichimoku-cloudleading-span-alinewidth)- [ichimoku cloud.leading span a.plottype](#ichimoku-cloudleading-span-aplottype)- [ichimoku cloud.leading span a.trackprice](#ichimoku-cloudleading-span-atrackprice)- [ichimoku cloud.leading span a.transparency](#ichimoku-cloudleading-span-atransparency)- [ichimoku cloud.leading span b.color](#ichimoku-cloudleading-span-bcolor)- [ichimoku cloud.leading span b.display](#ichimoku-cloudleading-span-bdisplay)- [ichimoku cloud.leading span b.linestyle](#ichimoku-cloudleading-span-blinestyle)- [ichimoku cloud.leading span b.linewidth](#ichimoku-cloudleading-span-blinewidth)- [ichimoku cloud.leading span b.plottype](#ichimoku-cloudleading-span-bplottype)- [ichimoku cloud.leading span b.trackprice](#ichimoku-cloudleading-span-btrackprice)- [ichimoku cloud.leading span b.transparency](#ichimoku-cloudleading-span-btransparency)- [ichimoku cloud.leading span periods](#ichimoku-cloudleading-span-periods)- [ichimoku cloud.plots background.color](#ichimoku-cloudplots-backgroundcolor)- [ichimoku cloud.plots background.transparency](#ichimoku-cloudplots-backgroundtransparency)- [ichimoku cloud.plots background.visible](#ichimoku-cloudplots-backgroundvisible)- [keltner channels.length](#keltner-channelslength)- [keltner channels.lower.color](#keltner-channelslowercolor)- [keltner channels.lower.display](#keltner-channelslowerdisplay)- [keltner channels.lower.linestyle](#keltner-channelslowerlinestyle)- [keltner channels.lower.linewidth](#keltner-channelslowerlinewidth)- [keltner channels.lower.plottype](#keltner-channelslowerplottype)- [keltner channels.lower.trackprice](#keltner-channelslowertrackprice)- [keltner channels.lower.transparency](#keltner-channelslowertransparency)- [keltner channels.middle.color](#keltner-channelsmiddlecolor)- [keltner channels.middle.display](#keltner-channelsmiddledisplay)- [keltner channels.middle.linestyle](#keltner-channelsmiddlelinestyle)- [keltner channels.middle.linewidth](#keltner-channelsmiddlelinewidth)- [keltner channels.middle.plottype](#keltner-channelsmiddleplottype)- [keltner channels.middle.trackprice](#keltner-channelsmiddletrackprice)- [keltner channels.middle.transparency](#keltner-channelsmiddletransparency)- [keltner channels.mult](#keltner-channelsmult)- [keltner channels.plots background.color](#keltner-channelsplots-backgroundcolor)- [keltner channels.plots background.transparency](#keltner-channelsplots-backgroundtransparency)- [keltner channels.plots background.visible](#keltner-channelsplots-backgroundvisible)- [keltner channels.upper.color](#keltner-channelsuppercolor)- [keltner channels.upper.display](#keltner-channelsupperdisplay)- [keltner channels.upper.linestyle](#keltner-channelsupperlinestyle)- [keltner channels.upper.linewidth](#keltner-channelsupperlinewidth)- [keltner channels.upper.plottype](#keltner-channelsupperplottype)- [keltner channels.upper.trackprice](#keltner-channelsuppertrackprice)- [keltner channels.upper.transparency](#keltner-channelsuppertransparency)- [keltner channels.usetruerange](#keltner-channelsusetruerange)- [klinger oscillator.plot.color](#klinger-oscillatorplotcolor)- [klinger oscillator.plot.display](#klinger-oscillatorplotdisplay)- [klinger oscillator.plot.linestyle](#klinger-oscillatorplotlinestyle)- [klinger oscillator.plot.linewidth](#klinger-oscillatorplotlinewidth)- [klinger oscillator.plot.plottype](#klinger-oscillatorplotplottype)- [klinger oscillator.plot.trackprice](#klinger-oscillatorplottrackprice)- [klinger oscillator.plot.transparency](#klinger-oscillatorplottransparency)- [klinger oscillator.signal.color](#klinger-oscillatorsignalcolor)- [klinger oscillator.signal.display](#klinger-oscillatorsignaldisplay)- [klinger oscillator.signal.linestyle](#klinger-oscillatorsignallinestyle)- [klinger oscillator.signal.linewidth](#klinger-oscillatorsignallinewidth)- [klinger oscillator.signal.plottype](#klinger-oscillatorsignalplottype)- [klinger oscillator.signal.trackprice](#klinger-oscillatorsignaltrackprice)- [klinger oscillator.signal.transparency](#klinger-oscillatorsignaltransparency)- [know sure thing.kst.color](#know-sure-thingkstcolor)- [know sure thing.kst.display](#know-sure-thingkstdisplay)- [know sure thing.kst.linestyle](#know-sure-thingkstlinestyle)- [know sure thing.kst.linewidth](#know-sure-thingkstlinewidth)- [know sure thing.kst.plottype](#know-sure-thingkstplottype)- [know sure thing.kst.trackprice](#know-sure-thingksttrackprice)- [know sure thing.kst.transparency](#know-sure-thingksttransparency)- [know sure thing.roclen1](#know-sure-thingroclen1)- [know sure thing.roclen2](#know-sure-thingroclen2)- [know sure thing.roclen3](#know-sure-thingroclen3)- [know sure thing.roclen4](#know-sure-thingroclen4)- [know sure thing.siglen](#know-sure-thingsiglen)- [know sure thing.signal.color](#know-sure-thingsignalcolor)- [know sure thing.signal.display](#know-sure-thingsignaldisplay)- [know sure thing.signal.linestyle](#know-sure-thingsignallinestyle)- [know sure thing.signal.linewidth](#know-sure-thingsignallinewidth)- [know sure thing.signal.plottype](#know-sure-thingsignalplottype)- [know sure thing.signal.trackprice](#know-sure-thingsignaltrackprice)- [know sure thing.signal.transparency](#know-sure-thingsignaltransparency)- [know sure thing.smalen1](#know-sure-thingsmalen1)- [know sure thing.smalen2](#know-sure-thingsmalen2)- [know sure thing.smalen3](#know-sure-thingsmalen3)- [know sure thing.smalen4](#know-sure-thingsmalen4)- [know sure thing.zero.color](#know-sure-thingzerocolor)- [know sure thing.zero.linestyle](#know-sure-thingzerolinestyle)- [know sure thing.zero.linewidth](#know-sure-thingzerolinewidth)- [know sure thing.zero.value](#know-sure-thingzerovalue)- [know sure thing.zero.visible](#know-sure-thingzerovisible)- [least squares moving average.length](#least-squares-moving-averagelength)- [least squares moving average.offset](#least-squares-moving-averageoffset)- [least squares moving average.plot.color](#least-squares-moving-averageplotcolor)- [least squares moving average.plot.display](#least-squares-moving-averageplotdisplay)- [least squares moving average.plot.linestyle](#least-squares-moving-averageplotlinestyle)- [least squares moving average.plot.linewidth](#least-squares-moving-averageplotlinewidth)- [least squares moving average.plot.plottype](#least-squares-moving-averageplotplottype)- [least squares moving average.plot.trackprice](#least-squares-moving-averageplottrackprice)- [least squares moving average.plot.transparency](#least-squares-moving-averageplottransparency)- [lineWithMarkersStyle.closeLineColor](#linewithmarkersstylecloselinecolor)- [lineWithMarkersStyle.closeLineStyle](#linewithmarkersstylecloselinestyle)- [lineWithMarkersStyle.closeLineWidth](#linewithmarkersstylecloselinewidth)- [lineWithMarkersStyle.closeLowFillColor](#linewithmarkersstylecloselowfillcolor)- [lineWithMarkersStyle.highCloseFillColor](#linewithmarkersstylehighclosefillcolor)- [lineWithMarkersStyle.highLineColor](#linewithmarkersstylehighlinecolor)- [lineWithMarkersStyle.highLineStyle](#linewithmarkersstylehighlinestyle)- [lineWithMarkersStyle.highLineWidth](#linewithmarkersstylehighlinewidth)- [lineWithMarkersStyle.lowLineColor](#linewithmarkersstylelowlinecolor)- [lineWithMarkersStyle.lowLineStyle](#linewithmarkersstylelowlinestyle)- [lineWithMarkersStyle.lowLineWidth](#linewithmarkersstylelowlinewidth)- [linear regression curve.length](#linear-regression-curvelength)- [linear regression curve.plot.color](#linear-regression-curveplotcolor)- [linear regression curve.plot.display](#linear-regression-curveplotdisplay)- [linear regression curve.plot.linestyle](#linear-regression-curveplotlinestyle)- [linear regression curve.plot.linewidth](#linear-regression-curveplotlinewidth)- [linear regression curve.plot.plottype](#linear-regression-curveplotplottype)- [linear regression curve.plot.trackprice](#linear-regression-curveplottrackprice)- [linear regression curve.plot.transparency](#linear-regression-curveplottransparency)- [linear regression slope.periods](#linear-regression-slopeperiods)- [linear regression slope.plot.color](#linear-regression-slopeplotcolor)- [linear regression slope.plot.display](#linear-regression-slopeplotdisplay)- [linear regression slope.plot.linestyle](#linear-regression-slopeplotlinestyle)- [linear regression slope.plot.linewidth](#linear-regression-slopeplotlinewidth)- [linear regression slope.plot.plottype](#linear-regression-slopeplotplottype)- [linear regression slope.plot.trackprice](#linear-regression-slopeplottrackprice)- [linear regression slope.plot.transparency](#linear-regression-slopeplottransparency)- [ma cross.crosses.color](#ma-crosscrossescolor)- [ma cross.crosses.display](#ma-crosscrossesdisplay)- [ma cross.crosses.linestyle](#ma-crosscrosseslinestyle)- [ma cross.crosses.linewidth](#ma-crosscrosseslinewidth)- [ma cross.crosses.plottype](#ma-crosscrossesplottype)- [ma cross.crosses.trackprice](#ma-crosscrossestrackprice)- [ma cross.crosses.transparency](#ma-crosscrossestransparency)- [ma cross.long](#ma-crosslong)- [ma cross.long.color](#ma-crosslongcolor)- [ma cross.long.display](#ma-crosslongdisplay)- [ma cross.long.linestyle](#ma-crosslonglinestyle)- [ma cross.long.linewidth](#ma-crosslonglinewidth)- [ma cross.long.plottype](#ma-crosslongplottype)- [ma cross.long.trackprice](#ma-crosslongtrackprice)- [ma cross.long.transparency](#ma-crosslongtransparency)- [ma cross.short](#ma-crossshort)- [ma cross.short.color](#ma-crossshortcolor)- [ma cross.short.display](#ma-crossshortdisplay)- [ma cross.short.linestyle](#ma-crossshortlinestyle)- [ma cross.short.linewidth](#ma-crossshortlinewidth)- [ma cross.short.plottype](#ma-crossshortplottype)- [ma cross.short.trackprice](#ma-crossshorttrackprice)- [ma cross.short.transparency](#ma-crossshorttransparency)- [ma with ema cross.crosses.color](#ma-with-ema-crosscrossescolor)- [ma with ema cross.crosses.display](#ma-with-ema-crosscrossesdisplay)- [ma with ema cross.crosses.linestyle](#ma-with-ema-crosscrosseslinestyle)- [ma with ema cross.crosses.linewidth](#ma-with-ema-crosscrosseslinewidth)- [ma with ema cross.crosses.plottype](#ma-with-ema-crosscrossesplottype)- [ma with ema cross.crosses.trackprice](#ma-with-ema-crosscrossestrackprice)- [ma with ema cross.crosses.transparency](#ma-with-ema-crosscrossestransparency)- [ma with ema cross.ema.color](#ma-with-ema-crossemacolor)- [ma with ema cross.ema.display](#ma-with-ema-crossemadisplay)- [ma with ema cross.ema.linestyle](#ma-with-ema-crossemalinestyle)- [ma with ema cross.ema.linewidth](#ma-with-ema-crossemalinewidth)- [ma with ema cross.ema.plottype](#ma-with-ema-crossemaplottype)- [ma with ema cross.ema.trackprice](#ma-with-ema-crossematrackprice)- [ma with ema cross.ema.transparency](#ma-with-ema-crossematransparency)- [ma with ema cross.length ema](#ma-with-ema-crosslength-ema)- [ma with ema cross.length ma](#ma-with-ema-crosslength-ma)- [ma with ema cross.ma.color](#ma-with-ema-crossmacolor)- [ma with ema cross.ma.display](#ma-with-ema-crossmadisplay)- [ma with ema cross.ma.linestyle](#ma-with-ema-crossmalinestyle)- [ma with ema cross.ma.linewidth](#ma-with-ema-crossmalinewidth)- [ma with ema cross.ma.plottype](#ma-with-ema-crossmaplottype)- [ma with ema cross.ma.trackprice](#ma-with-ema-crossmatrackprice)- [ma with ema cross.ma.transparency](#ma-with-ema-crossmatransparency)- [macd.fast length](#macdfast-length)- [macd.histogram.color](#macdhistogramcolor)- [macd.histogram.display](#macdhistogramdisplay)- [macd.histogram.linestyle](#macdhistogramlinestyle)- [macd.histogram.linewidth](#macdhistogramlinewidth)- [macd.histogram.plottype](#macdhistogramplottype)- [macd.histogram.trackprice](#macdhistogramtrackprice)- [macd.histogram.transparency](#macdhistogramtransparency)- [macd.macd.color](#macdmacdcolor)- [macd.macd.display](#macdmacddisplay)- [macd.macd.linestyle](#macdmacdlinestyle)- [macd.macd.linewidth](#macdmacdlinewidth)- [macd.macd.plottype](#macdmacdplottype)- [macd.macd.trackprice](#macdmacdtrackprice)- [macd.macd.transparency](#macdmacdtransparency)- [macd.oscillator ma type](#macdoscillator-ma-type)- [macd.other symbol](#macdother-symbol)- [macd.signal length](#macdsignal-length)- [macd.signal line ma type](#macdsignal-line-ma-type)- [macd.signal.color](#macdsignalcolor)- [macd.signal.display](#macdsignaldisplay)- [macd.signal.linestyle](#macdsignallinestyle)- [macd.signal.linewidth](#macdsignallinewidth)- [macd.signal.plottype](#macdsignalplottype)- [macd.signal.trackprice](#macdsignaltrackprice)- [macd.signal.transparency](#macdsignaltransparency)- [macd.slow length](#macdslow-length)- [macd.source](#macdsource)- [majority rule.majority rule.color](#majority-rulemajority-rulecolor)- [majority rule.majority rule.display](#majority-rulemajority-ruledisplay)- [majority rule.majority rule.linestyle](#majority-rulemajority-rulelinestyle)- [majority rule.majority rule.linewidth](#majority-rulemajority-rulelinewidth)- [majority rule.majority rule.plottype](#majority-rulemajority-ruleplottype)- [majority rule.majority rule.trackprice](#majority-rulemajority-ruletrackprice)- [majority rule.majority rule.transparency](#majority-rulemajority-ruletransparency)- [majority rule.rolling period](#majority-rulerolling-period)- [mass index.length](#mass-indexlength)- [mass index.plot.color](#mass-indexplotcolor)- [mass index.plot.display](#mass-indexplotdisplay)- [mass index.plot.linestyle](#mass-indexplotlinestyle)- [mass index.plot.linewidth](#mass-indexplotlinewidth)- [mass index.plot.plottype](#mass-indexplotplottype)- [mass index.plot.trackprice](#mass-indexplottrackprice)- [mass index.plot.transparency](#mass-indexplottransparency)- [mcginley dynamic.length](#mcginley-dynamiclength)- [mcginley dynamic.plot.color](#mcginley-dynamicplotcolor)- [mcginley dynamic.plot.display](#mcginley-dynamicplotdisplay)- [mcginley dynamic.plot.linestyle](#mcginley-dynamicplotlinestyle)- [mcginley dynamic.plot.linewidth](#mcginley-dynamicplotlinewidth)- [mcginley dynamic.plot.plottype](#mcginley-dynamicplotplottype)- [mcginley dynamic.plot.trackprice](#mcginley-dynamicplottrackprice)- [mcginley dynamic.plot.transparency](#mcginley-dynamicplottransparency)- [median price.plot.color](#median-priceplotcolor)- [median price.plot.display](#median-priceplotdisplay)- [median price.plot.linestyle](#median-priceplotlinestyle)- [median price.plot.linewidth](#median-priceplotlinewidth)- [median price.plot.plottype](#median-priceplotplottype)- [median price.plot.trackprice](#median-priceplottrackprice)- [median price.plot.transparency](#median-priceplottransparency)- [momentum.length](#momentumlength)- [momentum.mom.color](#momentummomcolor)- [momentum.mom.display](#momentummomdisplay)- [momentum.mom.linestyle](#momentummomlinestyle)- [momentum.mom.linewidth](#momentummomlinewidth)- [momentum.mom.plottype](#momentummomplottype)- [momentum.mom.trackprice](#momentummomtrackprice)- [momentum.mom.transparency](#momentummomtransparency)- [momentum.source](#momentumsource)- [momentum.zero.color](#momentumzerocolor)- [momentum.zero.linestyle](#momentumzerolinestyle)- [momentum.zero.linewidth](#momentumzerolinewidth)- [momentum.zero.value](#momentumzerovalue)- [momentum.zero.visible](#momentumzerovisible)- [money flow index.hlines background.color](#money-flow-indexhlines-backgroundcolor)- [money flow index.hlines background.transparency](#money-flow-indexhlines-backgroundtransparency)- [money flow index.hlines background.visible](#money-flow-indexhlines-backgroundvisible)- [money flow index.length](#money-flow-indexlength)- [money flow index.lowerlimit.color](#money-flow-indexlowerlimitcolor)- [money flow index.lowerlimit.linestyle](#money-flow-indexlowerlimitlinestyle)- [money flow index.lowerlimit.linewidth](#money-flow-indexlowerlimitlinewidth)- [money flow index.lowerlimit.value](#money-flow-indexlowerlimitvalue)- [money flow index.lowerlimit.visible](#money-flow-indexlowerlimitvisible)- [money flow index.plot.color](#money-flow-indexplotcolor)- [money flow index.plot.display](#money-flow-indexplotdisplay)- [money flow index.plot.linestyle](#money-flow-indexplotlinestyle)- [money flow index.plot.linewidth](#money-flow-indexplotlinewidth)- [money flow index.plot.plottype](#money-flow-indexplotplottype)- [money flow index.plot.trackprice](#money-flow-indexplottrackprice)- [money flow index.plot.transparency](#money-flow-indexplottransparency)- [money flow index.upperlimit.color](#money-flow-indexupperlimitcolor)- [money flow index.upperlimit.linestyle](#money-flow-indexupperlimitlinestyle)- [money flow index.upperlimit.linewidth](#money-flow-indexupperlimitlinewidth)- [money flow index.upperlimit.value](#money-flow-indexupperlimitvalue)- [money flow index.upperlimit.visible](#money-flow-indexupperlimitvisible)- [moving average adaptive.period](#moving-average-adaptiveperiod)- [moving average adaptive.plot 1.color](#moving-average-adaptiveplot-1color)- [moving average adaptive.plot 1.display](#moving-average-adaptiveplot-1display)- [moving average adaptive.plot 1.linestyle](#moving-average-adaptiveplot-1linestyle)- [moving average adaptive.plot 1.linewidth](#moving-average-adaptiveplot-1linewidth)- [moving average adaptive.plot 1.plottype](#moving-average-adaptiveplot-1plottype)- [moving average adaptive.plot 1.trackprice](#moving-average-adaptiveplot-1trackprice)- [moving average adaptive.plot 1.transparency](#moving-average-adaptiveplot-1transparency)- [moving average channel.lower length](#moving-average-channellower-length)- [moving average channel.lower offset](#moving-average-channellower-offset)- [moving average channel.lower.color](#moving-average-channellowercolor)- [moving average channel.lower.display](#moving-average-channellowerdisplay)- [moving average channel.lower.linestyle](#moving-average-channellowerlinestyle)- [moving average channel.lower.linewidth](#moving-average-channellowerlinewidth)- [moving average channel.lower.plottype](#moving-average-channellowerplottype)- [moving average channel.lower.trackprice](#moving-average-channellowertrackprice)- [moving average channel.lower.transparency](#moving-average-channellowertransparency)- [moving average channel.plots background.color](#moving-average-channelplots-backgroundcolor)- [moving average channel.plots background.transparency](#moving-average-channelplots-backgroundtransparency)- [moving average channel.plots background.visible](#moving-average-channelplots-backgroundvisible)- [moving average channel.upper length](#moving-average-channelupper-length)- [moving average channel.upper offset](#moving-average-channelupper-offset)- [moving average channel.upper.color](#moving-average-channeluppercolor)- [moving average channel.upper.display](#moving-average-channelupperdisplay)- [moving average channel.upper.linestyle](#moving-average-channelupperlinestyle)- [moving average channel.upper.linewidth](#moving-average-channelupperlinewidth)- [moving average channel.upper.plottype](#moving-average-channelupperplottype)- [moving average channel.upper.trackprice](#moving-average-channeluppertrackprice)- [moving average channel.upper.transparency](#moving-average-channeluppertransparency)- [moving average double.1st period](#moving-average-double1st-period)- [moving average double.2nd period](#moving-average-double2nd-period)- [moving average double.another symbol](#moving-average-doubleanother-symbol)- [moving average double.method](#moving-average-doublemethod)- [moving average double.plot 1.color](#moving-average-doubleplot-1color)- [moving average double.plot 1.display](#moving-average-doubleplot-1display)- [moving average double.plot 1.linestyle](#moving-average-doubleplot-1linestyle)- [moving average double.plot 1.linewidth](#moving-average-doubleplot-1linewidth)- [moving average double.plot 1.plottype](#moving-average-doubleplot-1plottype)- [moving average double.plot 1.trackprice](#moving-average-doubleplot-1trackprice)- [moving average double.plot 1.transparency](#moving-average-doubleplot-1transparency)- [moving average double.plot 2.color](#moving-average-doubleplot-2color)- [moving average double.plot 2.display](#moving-average-doubleplot-2display)- [moving average double.plot 2.linestyle](#moving-average-doubleplot-2linestyle)- [moving average double.plot 2.linewidth](#moving-average-doubleplot-2linewidth)- [moving average double.plot 2.plottype](#moving-average-doubleplot-2plottype)- [moving average double.plot 2.trackprice](#moving-average-doubleplot-2trackprice)- [moving average double.plot 2.transparency](#moving-average-doubleplot-2transparency)- [moving average exponential.length](#moving-average-exponentiallength)- [moving average exponential.offset](#moving-average-exponentialoffset)- [moving average exponential.plot.color](#moving-average-exponentialplotcolor)- [moving average exponential.plot.display](#moving-average-exponentialplotdisplay)- [moving average exponential.plot.linestyle](#moving-average-exponentialplotlinestyle)- [moving average exponential.plot.linewidth](#moving-average-exponentialplotlinewidth)- [moving average exponential.plot.plottype](#moving-average-exponentialplotplottype)- [moving average exponential.plot.trackprice](#moving-average-exponentialplottrackprice)- [moving average exponential.plot.transparency](#moving-average-exponentialplottransparency)- [moving average exponential.smoothed ma.display](#moving-average-exponentialsmoothed-madisplay)- [moving average exponential.smoothed ma.linestyle](#moving-average-exponentialsmoothed-malinestyle)- [moving average exponential.smoothed ma.linewidth](#moving-average-exponentialsmoothed-malinewidth)- [moving average exponential.smoothed ma.plottype](#moving-average-exponentialsmoothed-maplottype)- [moving average exponential.smoothed ma.trackprice](#moving-average-exponentialsmoothed-matrackprice)- [moving average exponential.smoothed ma.transparency](#moving-average-exponentialsmoothed-matransparency)- [moving average exponential.smoothing length](#moving-average-exponentialsmoothing-length)- [moving average exponential.smoothing line](#moving-average-exponentialsmoothing-line)- [moving average exponential.source](#moving-average-exponentialsource)- [moving average hamming.period](#moving-average-hammingperiod)- [moving average hamming.plot 1.color](#moving-average-hammingplot-1color)- [moving average hamming.plot 1.display](#moving-average-hammingplot-1display)- [moving average hamming.plot 1.linestyle](#moving-average-hammingplot-1linestyle)- [moving average hamming.plot 1.linewidth](#moving-average-hammingplot-1linewidth)- [moving average hamming.plot 1.plottype](#moving-average-hammingplot-1plottype)- [moving average hamming.plot 1.trackprice](#moving-average-hammingplot-1trackprice)- [moving average hamming.plot 1.transparency](#moving-average-hammingplot-1transparency)- [moving average multiple.1st period](#moving-average-multiple1st-period)- [moving average multiple.2nd period](#moving-average-multiple2nd-period)- [moving average multiple.3rd period](#moving-average-multiple3rd-period)- [moving average multiple.4th period](#moving-average-multiple4th-period)- [moving average multiple.5th period](#moving-average-multiple5th-period)- [moving average multiple.6th period](#moving-average-multiple6th-period)- [moving average multiple.method](#moving-average-multiplemethod)- [moving average multiple.plot 1.color](#moving-average-multipleplot-1color)- [moving average multiple.plot 1.display](#moving-average-multipleplot-1display)- [moving average multiple.plot 1.linestyle](#moving-average-multipleplot-1linestyle)- [moving average multiple.plot 1.linewidth](#moving-average-multipleplot-1linewidth)- [moving average multiple.plot 1.plottype](#moving-average-multipleplot-1plottype)- [moving average multiple.plot 1.trackprice](#moving-average-multipleplot-1trackprice)- [moving average multiple.plot 1.transparency](#moving-average-multipleplot-1transparency)- [moving average multiple.plot 2.color](#moving-average-multipleplot-2color)- [moving average multiple.plot 2.display](#moving-average-multipleplot-2display)- [moving average multiple.plot 2.linestyle](#moving-average-multipleplot-2linestyle)- [moving average multiple.plot 2.linewidth](#moving-average-multipleplot-2linewidth)- [moving average multiple.plot 2.plottype](#moving-average-multipleplot-2plottype)- [moving average multiple.plot 2.trackprice](#moving-average-multipleplot-2trackprice)- [moving average multiple.plot 2.transparency](#moving-average-multipleplot-2transparency)- [moving average multiple.plot 3.color](#moving-average-multipleplot-3color)- [moving average multiple.plot 3.display](#moving-average-multipleplot-3display)- [moving average multiple.plot 3.linestyle](#moving-average-multipleplot-3linestyle)- [moving average multiple.plot 3.linewidth](#moving-average-multipleplot-3linewidth)- [moving average multiple.plot 3.plottype](#moving-average-multipleplot-3plottype)- [moving average multiple.plot 3.trackprice](#moving-average-multipleplot-3trackprice)- [moving average multiple.plot 3.transparency](#moving-average-multipleplot-3transparency)- [moving average multiple.plot 4.color](#moving-average-multipleplot-4color)- [moving average multiple.plot 4.display](#moving-average-multipleplot-4display)- [moving average multiple.plot 4.linestyle](#moving-average-multipleplot-4linestyle)- [moving average multiple.plot 4.linewidth](#moving-average-multipleplot-4linewidth)- [moving average multiple.plot 4.plottype](#moving-average-multipleplot-4plottype)- [moving average multiple.plot 4.trackprice](#moving-average-multipleplot-4trackprice)- [moving average multiple.plot 4.transparency](#moving-average-multipleplot-4transparency)- [moving average multiple.plot 5.color](#moving-average-multipleplot-5color)- [moving average multiple.plot 5.display](#moving-average-multipleplot-5display)- [moving average multiple.plot 5.linestyle](#moving-average-multipleplot-5linestyle)- [moving average multiple.plot 5.linewidth](#moving-average-multipleplot-5linewidth)- [moving average multiple.plot 5.plottype](#moving-average-multipleplot-5plottype)- [moving average multiple.plot 5.trackprice](#moving-average-multipleplot-5trackprice)- [moving average multiple.plot 5.transparency](#moving-average-multipleplot-5transparency)- [moving average multiple.plot 6.color](#moving-average-multipleplot-6color)- [moving average multiple.plot 6.display](#moving-average-multipleplot-6display)- [moving average multiple.plot 6.linestyle](#moving-average-multipleplot-6linestyle)- [moving average multiple.plot 6.linewidth](#moving-average-multipleplot-6linewidth)- [moving average multiple.plot 6.plottype](#moving-average-multipleplot-6plottype)- [moving average multiple.plot 6.trackprice](#moving-average-multipleplot-6trackprice)- [moving average multiple.plot 6.transparency](#moving-average-multipleplot-6transparency)- [moving average triple.1st period](#moving-average-triple1st-period)- [moving average triple.2nd period](#moving-average-triple2nd-period)- [moving average triple.3rd period](#moving-average-triple3rd-period)- [moving average triple.method](#moving-average-triplemethod)- [moving average triple.plot 1.color](#moving-average-tripleplot-1color)- [moving average triple.plot 1.display](#moving-average-tripleplot-1display)- [moving average triple.plot 1.linestyle](#moving-average-tripleplot-1linestyle)- [moving average triple.plot 1.linewidth](#moving-average-tripleplot-1linewidth)- [moving average triple.plot 1.plottype](#moving-average-tripleplot-1plottype)- [moving average triple.plot 1.trackprice](#moving-average-tripleplot-1trackprice)- [moving average triple.plot 1.transparency](#moving-average-tripleplot-1transparency)- [moving average triple.plot 2.color](#moving-average-tripleplot-2color)- [moving average triple.plot 2.display](#moving-average-tripleplot-2display)- [moving average triple.plot 2.linestyle](#moving-average-tripleplot-2linestyle)- [moving average triple.plot 2.linewidth](#moving-average-tripleplot-2linewidth)- [moving average triple.plot 2.plottype](#moving-average-tripleplot-2plottype)- [moving average triple.plot 2.trackprice](#moving-average-tripleplot-2trackprice)- [moving average triple.plot 2.transparency](#moving-average-tripleplot-2transparency)- [moving average triple.plot 3.color](#moving-average-tripleplot-3color)- [moving average triple.plot 3.display](#moving-average-tripleplot-3display)- [moving average triple.plot 3.linestyle](#moving-average-tripleplot-3linestyle)- [moving average triple.plot 3.linewidth](#moving-average-tripleplot-3linewidth)- [moving average triple.plot 3.plottype](#moving-average-tripleplot-3plottype)- [moving average triple.plot 3.trackprice](#moving-average-tripleplot-3trackprice)- [moving average triple.plot 3.transparency](#moving-average-tripleplot-3transparency)- [moving average weighted.length](#moving-average-weightedlength)- [moving average weighted.offset](#moving-average-weightedoffset)- [moving average weighted.plot.color](#moving-average-weightedplotcolor)- [moving average weighted.plot.display](#moving-average-weightedplotdisplay)- [moving average weighted.plot.linestyle](#moving-average-weightedplotlinestyle)- [moving average weighted.plot.linewidth](#moving-average-weightedplotlinewidth)- [moving average weighted.plot.plottype](#moving-average-weightedplotplottype)- [moving average weighted.plot.trackprice](#moving-average-weightedplottrackprice)- [moving average weighted.plot.transparency](#moving-average-weightedplottransparency)- [moving average weighted.source](#moving-average-weightedsource)- [moving average.length](#moving-averagelength)- [moving average.offset](#moving-averageoffset)- [moving average.other symbol](#moving-averageother-symbol)- [moving average.plot.color](#moving-averageplotcolor)- [moving average.plot.display](#moving-averageplotdisplay)- [moving average.plot.linestyle](#moving-averageplotlinestyle)- [moving average.plot.linewidth](#moving-averageplotlinewidth)- [moving average.plot.plottype](#moving-averageplotplottype)- [moving average.plot.trackprice](#moving-averageplottrackprice)- [moving average.plot.transparency](#moving-averageplottransparency)- [moving average.smoothed ma.display](#moving-averagesmoothed-madisplay)- [moving average.smoothed ma.linestyle](#moving-averagesmoothed-malinestyle)- [moving average.smoothed ma.linewidth](#moving-averagesmoothed-malinewidth)- [moving average.smoothed ma.plottype](#moving-averagesmoothed-maplottype)- [moving average.smoothed ma.trackprice](#moving-averagesmoothed-matrackprice)- [moving average.smoothed ma.transparency](#moving-averagesmoothed-matransparency)- [moving average.smoothing length](#moving-averagesmoothing-length)- [moving average.smoothing line](#moving-averagesmoothing-line)- [moving average.source](#moving-averagesource)- [net volume.plot.color](#net-volumeplotcolor)- [net volume.plot.display](#net-volumeplotdisplay)- [net volume.plot.linestyle](#net-volumeplotlinestyle)- [net volume.plot.linewidth](#net-volumeplotlinewidth)- [net volume.plot.plottype](#net-volumeplotplottype)- [net volume.plot.trackprice](#net-volumeplottrackprice)- [net volume.plot.transparency](#net-volumeplottransparency)- [on balance volume.plot.color](#on-balance-volumeplotcolor)- [on balance volume.plot.display](#on-balance-volumeplotdisplay)- [on balance volume.plot.linestyle](#on-balance-volumeplotlinestyle)- [on balance volume.plot.linewidth](#on-balance-volumeplotlinewidth)- [on balance volume.plot.plottype](#on-balance-volumeplotplottype)- [on balance volume.plot.trackprice](#on-balance-volumeplottrackprice)- [on balance volume.plot.transparency](#on-balance-volumeplottransparency)- [on balance volume.smoothed ma.display](#on-balance-volumesmoothed-madisplay)- [on balance volume.smoothed ma.linestyle](#on-balance-volumesmoothed-malinestyle)- [on balance volume.smoothed ma.linewidth](#on-balance-volumesmoothed-malinewidth)- [on balance volume.smoothed ma.plottype](#on-balance-volumesmoothed-maplottype)- [on balance volume.smoothed ma.trackprice](#on-balance-volumesmoothed-matrackprice)- [on balance volume.smoothed ma.transparency](#on-balance-volumesmoothed-matransparency)- [on balance volume.smoothing length](#on-balance-volumesmoothing-length)- [on balance volume.smoothing line](#on-balance-volumesmoothing-line)- [overlay.extendtimescale](#overlayextendtimescale)- [overlay.symbol](#overlaysymbol)- [parabolic sar.increment](#parabolic-sarincrement)- [parabolic sar.maximum](#parabolic-sarmaximum)- [parabolic sar.other symbol](#parabolic-sarother-symbol)- [parabolic sar.plot.color](#parabolic-sarplotcolor)- [parabolic sar.plot.display](#parabolic-sarplotdisplay)- [parabolic sar.plot.linestyle](#parabolic-sarplotlinestyle)- [parabolic sar.plot.linewidth](#parabolic-sarplotlinewidth)- [parabolic sar.plot.plottype](#parabolic-sarplotplottype)- [parabolic sar.plot.trackprice](#parabolic-sarplottrackprice)- [parabolic sar.plot.transparency](#parabolic-sarplottransparency)- [parabolic sar.start](#parabolic-sarstart)- [pivot points standard.number of pivots back](#pivot-points-standardnumber-of-pivots-back)- [pivot points standard.pivots timeframe](#pivot-points-standardpivots-timeframe)- [pivot points standard.show historical pivots](#pivot-points-standardshow-historical-pivots)- [pivot points standard.type](#pivot-points-standardtype)- [price channel.centerprice line.color](#price-channelcenterprice-linecolor)- [price channel.centerprice line.display](#price-channelcenterprice-linedisplay)- [price channel.centerprice line.linestyle](#price-channelcenterprice-linelinestyle)- [price channel.centerprice line.linewidth](#price-channelcenterprice-linelinewidth)- [price channel.centerprice line.plottype](#price-channelcenterprice-lineplottype)- [price channel.centerprice line.trackprice](#price-channelcenterprice-linetrackprice)- [price channel.centerprice line.transparency](#price-channelcenterprice-linetransparency)- [price channel.highprice line.color](#price-channelhighprice-linecolor)- [price channel.highprice line.display](#price-channelhighprice-linedisplay)- [price channel.highprice line.linestyle](#price-channelhighprice-linelinestyle)- [price channel.highprice line.linewidth](#price-channelhighprice-linelinewidth)- [price channel.highprice line.plottype](#price-channelhighprice-lineplottype)- [price channel.highprice line.trackprice](#price-channelhighprice-linetrackprice)- [price channel.highprice line.transparency](#price-channelhighprice-linetransparency)- [price channel.length](#price-channellength)- [price channel.lowprice line.color](#price-channellowprice-linecolor)- [price channel.lowprice line.display](#price-channellowprice-linedisplay)- [price channel.lowprice line.linestyle](#price-channellowprice-linelinestyle)- [price channel.lowprice line.linewidth](#price-channellowprice-linelinewidth)- [price channel.lowprice line.plottype](#price-channellowprice-lineplottype)- [price channel.lowprice line.trackprice](#price-channellowprice-linetrackprice)- [price channel.lowprice line.transparency](#price-channellowprice-linetransparency)- [price channel.offset length](#price-channeloffset-length)- [price oscillator.longlen](#price-oscillatorlonglen)- [price oscillator.plot.color](#price-oscillatorplotcolor)- [price oscillator.plot.display](#price-oscillatorplotdisplay)- [price oscillator.plot.linestyle](#price-oscillatorplotlinestyle)- [price oscillator.plot.linewidth](#price-oscillatorplotlinewidth)- [price oscillator.plot.plottype](#price-oscillatorplotplottype)- [price oscillator.plot.trackprice](#price-oscillatorplottrackprice)- [price oscillator.plot.transparency](#price-oscillatorplottransparency)- [price oscillator.shortlen](#price-oscillatorshortlen)- [price volume trend.pvt.color](#price-volume-trendpvtcolor)- [price volume trend.pvt.display](#price-volume-trendpvtdisplay)- [price volume trend.pvt.linestyle](#price-volume-trendpvtlinestyle)- [price volume trend.pvt.linewidth](#price-volume-trendpvtlinewidth)- [price volume trend.pvt.plottype](#price-volume-trendpvtplottype)- [price volume trend.pvt.trackprice](#price-volume-trendpvttrackprice)- [price volume trend.pvt.transparency](#price-volume-trendpvttransparency)- [rank correlation index.length](#rank-correlation-indexlength)- [rank correlation index.rci.color](#rank-correlation-indexrcicolor)- [rank correlation index.rci.display](#rank-correlation-indexrcidisplay)- [rank correlation index.rci.linestyle](#rank-correlation-indexrcilinestyle)- [rank correlation index.rci.linewidth](#rank-correlation-indexrcilinewidth)- [rank correlation index.rci.plottype](#rank-correlation-indexrciplottype)- [rank correlation index.rci.trackprice](#rank-correlation-indexrcitrackprice)- [rank correlation index.rci.transparency](#rank-correlation-indexrcitransparency)- [rank correlation index.zero line.color](#rank-correlation-indexzero-linecolor)- [rank correlation index.zero line.linestyle](#rank-correlation-indexzero-linelinestyle)- [rank correlation index.zero line.linewidth](#rank-correlation-indexzero-linelinewidth)- [rank correlation index.zero line.value](#rank-correlation-indexzero-linevalue)- [rank correlation index.zero line.visible](#rank-correlation-indexzero-linevisible)- [rate of change.length](#rate-of-changelength)- [rate of change.roc.color](#rate-of-changeroccolor)- [rate of change.roc.display](#rate-of-changerocdisplay)- [rate of change.roc.linestyle](#rate-of-changeroclinestyle)- [rate of change.roc.linewidth](#rate-of-changeroclinewidth)- [rate of change.roc.plottype](#rate-of-changerocplottype)- [rate of change.roc.trackprice](#rate-of-changeroctrackprice)- [rate of change.roc.transparency](#rate-of-changeroctransparency)- [rate of change.zero line.color](#rate-of-changezero-linecolor)- [rate of change.zero line.linestyle](#rate-of-changezero-linelinestyle)- [rate of change.zero line.linewidth](#rate-of-changezero-linelinewidth)- [rate of change.zero line.value](#rate-of-changezero-linevalue)- [rate of change.zero line.visible](#rate-of-changezero-linevisible)- [ratio.baseline.color](#ratiobaselinecolor)- [ratio.baseline.display](#ratiobaselinedisplay)- [ratio.baseline.linestyle](#ratiobaselinelinestyle)- [ratio.baseline.linewidth](#ratiobaselinelinewidth)- [ratio.baseline.plottype](#ratiobaselineplottype)- [ratio.baseline.trackprice](#ratiobaselinetrackprice)- [ratio.baseline.transparency](#ratiobaselinetransparency)- [ratio.negativefill.color](#rationegativefillcolor)- [ratio.negativefill.transparency](#rationegativefilltransparency)- [ratio.negativefill.visible](#rationegativefillvisible)- [ratio.plot.color](#ratioplotcolor)- [ratio.plot.display](#ratioplotdisplay)- [ratio.plot.linestyle](#ratioplotlinestyle)- [ratio.plot.linewidth](#ratioplotlinewidth)- [ratio.plot.plottype](#ratioplotplottype)- [ratio.plot.trackprice](#ratioplottrackprice)- [ratio.plot.transparency](#ratioplottransparency)- [ratio.positivefill.color](#ratiopositivefillcolor)- [ratio.positivefill.transparency](#ratiopositivefilltransparency)- [ratio.positivefill.visible](#ratiopositivefillvisible)- [ratio.source](#ratiosource)- [ratio.symbol](#ratiosymbol)- [regression trend.first bar time](#regression-trendfirst-bar-time)- [regression trend.last bar time](#regression-trendlast-bar-time)- [regression trend.lower deviation](#regression-trendlower-deviation)- [regression trend.source](#regression-trendsource)- [regression trend.upper deviation](#regression-trendupper-deviation)- [regression trend.use lower deviation](#regression-trenduse-lower-deviation)- [regression trend.use upper deviation](#regression-trenduse-upper-deviation)- [relative strength index.hlines background.color](#relative-strength-indexhlines-backgroundcolor)- [relative strength index.hlines background.transparency](#relative-strength-indexhlines-backgroundtransparency)- [relative strength index.hlines background.visible](#relative-strength-indexhlines-backgroundvisible)- [relative strength index.length](#relative-strength-indexlength)- [relative strength index.lowerlimit.color](#relative-strength-indexlowerlimitcolor)- [relative strength index.lowerlimit.linestyle](#relative-strength-indexlowerlimitlinestyle)- [relative strength index.lowerlimit.linewidth](#relative-strength-indexlowerlimitlinewidth)- [relative strength index.lowerlimit.value](#relative-strength-indexlowerlimitvalue)- [relative strength index.lowerlimit.visible](#relative-strength-indexlowerlimitvisible)- [relative strength index.lowerlimit.zorder](#relative-strength-indexlowerlimitzorder)- [relative strength index.middlelimit.color](#relative-strength-indexmiddlelimitcolor)- [relative strength index.middlelimit.linestyle](#relative-strength-indexmiddlelimitlinestyle)- [relative strength index.middlelimit.linewidth](#relative-strength-indexmiddlelimitlinewidth)- [relative strength index.middlelimit.value](#relative-strength-indexmiddlelimitvalue)- [relative strength index.middlelimit.visible](#relative-strength-indexmiddlelimitvisible)- [relative strength index.middlelimit.zorder](#relative-strength-indexmiddlelimitzorder)- [relative strength index.plot.color](#relative-strength-indexplotcolor)- [relative strength index.plot.display](#relative-strength-indexplotdisplay)- [relative strength index.plot.linestyle](#relative-strength-indexplotlinestyle)- [relative strength index.plot.linewidth](#relative-strength-indexplotlinewidth)- [relative strength index.plot.plottype](#relative-strength-indexplotplottype)- [relative strength index.plot.trackprice](#relative-strength-indexplottrackprice)- [relative strength index.plot.transparency](#relative-strength-indexplottransparency)- [relative strength index.smoothed ma.display](#relative-strength-indexsmoothed-madisplay)- [relative strength index.smoothed ma.linestyle](#relative-strength-indexsmoothed-malinestyle)- [relative strength index.smoothed ma.linewidth](#relative-strength-indexsmoothed-malinewidth)- [relative strength index.smoothed ma.plottype](#relative-strength-indexsmoothed-maplottype)- [relative strength index.smoothed ma.trackprice](#relative-strength-indexsmoothed-matrackprice)- [relative strength index.smoothed ma.transparency](#relative-strength-indexsmoothed-matransparency)- [relative strength index.smoothing length](#relative-strength-indexsmoothing-length)- [relative strength index.smoothing line](#relative-strength-indexsmoothing-line)- [relative strength index.upperlimit.color](#relative-strength-indexupperlimitcolor)- [relative strength index.upperlimit.linestyle](#relative-strength-indexupperlimitlinestyle)- [relative strength index.upperlimit.linewidth](#relative-strength-indexupperlimitlinewidth)- [relative strength index.upperlimit.value](#relative-strength-indexupperlimitvalue)- [relative strength index.upperlimit.visible](#relative-strength-indexupperlimitvisible)- [relative strength index.upperlimit.zorder](#relative-strength-indexupperlimitzorder)- [relative vigor index.length](#relative-vigor-indexlength)- [relative vigor index.rvgi.color](#relative-vigor-indexrvgicolor)- [relative vigor index.rvgi.display](#relative-vigor-indexrvgidisplay)- [relative vigor index.rvgi.linestyle](#relative-vigor-indexrvgilinestyle)- [relative vigor index.rvgi.linewidth](#relative-vigor-indexrvgilinewidth)- [relative vigor index.rvgi.plottype](#relative-vigor-indexrvgiplottype)- [relative vigor index.rvgi.trackprice](#relative-vigor-indexrvgitrackprice)- [relative vigor index.rvgi.transparency](#relative-vigor-indexrvgitransparency)- [relative vigor index.signal.color](#relative-vigor-indexsignalcolor)- [relative vigor index.signal.display](#relative-vigor-indexsignaldisplay)- [relative vigor index.signal.linestyle](#relative-vigor-indexsignallinestyle)- [relative vigor index.signal.linewidth](#relative-vigor-indexsignallinewidth)- [relative vigor index.signal.plottype](#relative-vigor-indexsignalplottype)- [relative vigor index.signal.trackprice](#relative-vigor-indexsignaltrackprice)- [relative vigor index.signal.transparency](#relative-vigor-indexsignaltransparency)- [relative volatility index.hlines background.color](#relative-volatility-indexhlines-backgroundcolor)- [relative volatility index.hlines background.transparency](#relative-volatility-indexhlines-backgroundtransparency)- [relative volatility index.hlines background.visible](#relative-volatility-indexhlines-backgroundvisible)- [relative volatility index.length](#relative-volatility-indexlength)- [relative volatility index.lowerlimit.color](#relative-volatility-indexlowerlimitcolor)- [relative volatility index.lowerlimit.linestyle](#relative-volatility-indexlowerlimitlinestyle)- [relative volatility index.lowerlimit.linewidth](#relative-volatility-indexlowerlimitlinewidth)- [relative volatility index.lowerlimit.value](#relative-volatility-indexlowerlimitvalue)- [relative volatility index.lowerlimit.visible](#relative-volatility-indexlowerlimitvisible)- [relative volatility index.plot.color](#relative-volatility-indexplotcolor)- [relative volatility index.plot.display](#relative-volatility-indexplotdisplay)- [relative volatility index.plot.linestyle](#relative-volatility-indexplotlinestyle)- [relative volatility index.plot.linewidth](#relative-volatility-indexplotlinewidth)- [relative volatility index.plot.plottype](#relative-volatility-indexplotplottype)- [relative volatility index.plot.trackprice](#relative-volatility-indexplottrackprice)- [relative volatility index.plot.transparency](#relative-volatility-indexplottransparency)- [relative volatility index.upperlimit.color](#relative-volatility-indexupperlimitcolor)- [relative volatility index.upperlimit.linestyle](#relative-volatility-indexupperlimitlinestyle)- [relative volatility index.upperlimit.linewidth](#relative-volatility-indexupperlimitlinewidth)- [relative volatility index.upperlimit.value](#relative-volatility-indexupperlimitvalue)- [relative volatility index.upperlimit.visible](#relative-volatility-indexupperlimitvisible)- [smi ergodic indicator/oscillator.indicator.color](#smi-ergodic-indicatoroscillatorindicatorcolor)- [smi ergodic indicator/oscillator.indicator.display](#smi-ergodic-indicatoroscillatorindicatordisplay)- [smi ergodic indicator/oscillator.indicator.linestyle](#smi-ergodic-indicatoroscillatorindicatorlinestyle)- [smi ergodic indicator/oscillator.indicator.linewidth](#smi-ergodic-indicatoroscillatorindicatorlinewidth)- [smi ergodic indicator/oscillator.indicator.plottype](#smi-ergodic-indicatoroscillatorindicatorplottype)- [smi ergodic indicator/oscillator.indicator.trackprice](#smi-ergodic-indicatoroscillatorindicatortrackprice)- [smi ergodic indicator/oscillator.indicator.transparency](#smi-ergodic-indicatoroscillatorindicatortransparency)- [smi ergodic indicator/oscillator.longlen](#smi-ergodic-indicatoroscillatorlonglen)- [smi ergodic indicator/oscillator.oscillator.color](#smi-ergodic-indicatoroscillatoroscillatorcolor)- [smi ergodic indicator/oscillator.oscillator.display](#smi-ergodic-indicatoroscillatoroscillatordisplay)- [smi ergodic indicator/oscillator.oscillator.linestyle](#smi-ergodic-indicatoroscillatoroscillatorlinestyle)- [smi ergodic indicator/oscillator.oscillator.linewidth](#smi-ergodic-indicatoroscillatoroscillatorlinewidth)- [smi ergodic indicator/oscillator.oscillator.plottype](#smi-ergodic-indicatoroscillatoroscillatorplottype)- [smi ergodic indicator/oscillator.oscillator.trackprice](#smi-ergodic-indicatoroscillatoroscillatortrackprice)- [smi ergodic indicator/oscillator.oscillator.transparency](#smi-ergodic-indicatoroscillatoroscillatortransparency)- [smi ergodic indicator/oscillator.shortlen](#smi-ergodic-indicatoroscillatorshortlen)- [smi ergodic indicator/oscillator.siglen](#smi-ergodic-indicatoroscillatorsiglen)- [smi ergodic indicator/oscillator.signal.color](#smi-ergodic-indicatoroscillatorsignalcolor)- [smi ergodic indicator/oscillator.signal.display](#smi-ergodic-indicatoroscillatorsignaldisplay)- [smi ergodic indicator/oscillator.signal.linestyle](#smi-ergodic-indicatoroscillatorsignallinestyle)- [smi ergodic indicator/oscillator.signal.linewidth](#smi-ergodic-indicatoroscillatorsignallinewidth)- [smi ergodic indicator/oscillator.signal.plottype](#smi-ergodic-indicatoroscillatorsignalplottype)- [smi ergodic indicator/oscillator.signal.trackprice](#smi-ergodic-indicatoroscillatorsignaltrackprice)- [smi ergodic indicator/oscillator.signal.transparency](#smi-ergodic-indicatoroscillatorsignaltransparency)- [smoothed moving average.length](#smoothed-moving-averagelength)- [smoothed moving average.plot.color](#smoothed-moving-averageplotcolor)- [smoothed moving average.plot.display](#smoothed-moving-averageplotdisplay)- [smoothed moving average.plot.linestyle](#smoothed-moving-averageplotlinestyle)- [smoothed moving average.plot.linewidth](#smoothed-moving-averageplotlinewidth)- [smoothed moving average.plot.plottype](#smoothed-moving-averageplotplottype)- [smoothed moving average.plot.trackprice](#smoothed-moving-averageplottrackprice)- [smoothed moving average.plot.transparency](#smoothed-moving-averageplottransparency)- [smoothed moving average.source](#smoothed-moving-averagesource)- [spread.baseline.color](#spreadbaselinecolor)- [spread.baseline.display](#spreadbaselinedisplay)- [spread.baseline.linestyle](#spreadbaselinelinestyle)- [spread.baseline.linewidth](#spreadbaselinelinewidth)- [spread.baseline.plottype](#spreadbaselineplottype)- [spread.baseline.trackprice](#spreadbaselinetrackprice)- [spread.baseline.transparency](#spreadbaselinetransparency)- [spread.negative fill.color](#spreadnegative-fillcolor)- [spread.negative fill.transparency](#spreadnegative-filltransparency)- [spread.negative fill.visible](#spreadnegative-fillvisible)- [spread.plot.color](#spreadplotcolor)- [spread.plot.display](#spreadplotdisplay)- [spread.plot.linestyle](#spreadplotlinestyle)- [spread.plot.linewidth](#spreadplotlinewidth)- [spread.plot.plottype](#spreadplotplottype)- [spread.plot.trackprice](#spreadplottrackprice)- [spread.plot.transparency](#spreadplottransparency)- [spread.positive fill.color](#spreadpositive-fillcolor)- [spread.positive fill.transparency](#spreadpositive-filltransparency)- [spread.positive fill.visible](#spreadpositive-fillvisible)- [spread.source](#spreadsource)- [spread.symbol](#spreadsymbol)- [standard deviation.deviations](#standard-deviationdeviations)- [standard deviation.periods](#standard-deviationperiods)- [standard deviation.plot.color](#standard-deviationplotcolor)- [standard deviation.plot.display](#standard-deviationplotdisplay)- [standard deviation.plot.linestyle](#standard-deviationplotlinestyle)- [standard deviation.plot.linewidth](#standard-deviationplotlinewidth)- [standard deviation.plot.plottype](#standard-deviationplotplottype)- [standard deviation.plot.trackprice](#standard-deviationplottrackprice)- [standard deviation.plot.transparency](#standard-deviationplottransparency)- [standard error bands.averaging periods](#standard-error-bandsaveraging-periods)- [standard error bands.background.color](#standard-error-bandsbackgroundcolor)- [standard error bands.background.transparency](#standard-error-bandsbackgroundtransparency)- [standard error bands.background.visible](#standard-error-bandsbackgroundvisible)- [standard error bands.method](#standard-error-bandsmethod)- [standard error bands.periods](#standard-error-bandsperiods)- [standard error bands.plot 1.color](#standard-error-bandsplot-1color)- [standard error bands.plot 1.display](#standard-error-bandsplot-1display)- [standard error bands.plot 1.linestyle](#standard-error-bandsplot-1linestyle)- [standard error bands.plot 1.linewidth](#standard-error-bandsplot-1linewidth)- [standard error bands.plot 1.plottype](#standard-error-bandsplot-1plottype)- [standard error bands.plot 1.trackprice](#standard-error-bandsplot-1trackprice)- [standard error bands.plot 1.transparency](#standard-error-bandsplot-1transparency)- [standard error bands.plot 2.color](#standard-error-bandsplot-2color)- [standard error bands.plot 2.display](#standard-error-bandsplot-2display)- [standard error bands.plot 2.linestyle](#standard-error-bandsplot-2linestyle)- [standard error bands.plot 2.linewidth](#standard-error-bandsplot-2linewidth)- [standard error bands.plot 2.plottype](#standard-error-bandsplot-2plottype)- [standard error bands.plot 2.trackprice](#standard-error-bandsplot-2trackprice)- [standard error bands.plot 2.transparency](#standard-error-bandsplot-2transparency)- [standard error bands.plot 3.color](#standard-error-bandsplot-3color)- [standard error bands.plot 3.display](#standard-error-bandsplot-3display)- [standard error bands.plot 3.linestyle](#standard-error-bandsplot-3linestyle)- [standard error bands.plot 3.linewidth](#standard-error-bandsplot-3linewidth)- [standard error bands.plot 3.plottype](#standard-error-bandsplot-3plottype)- [standard error bands.plot 3.trackprice](#standard-error-bandsplot-3trackprice)- [standard error bands.plot 3.transparency](#standard-error-bandsplot-3transparency)- [standard error bands.standard errors](#standard-error-bandsstandard-errors)- [standard error.length](#standard-errorlength)- [standard error.plot.color](#standard-errorplotcolor)- [standard error.plot.display](#standard-errorplotdisplay)- [standard error.plot.linestyle](#standard-errorplotlinestyle)- [standard error.plot.linewidth](#standard-errorplotlinewidth)- [standard error.plot.plottype](#standard-errorplotplottype)- [standard error.plot.trackprice](#standard-errorplottrackprice)- [standard error.plot.transparency](#standard-errorplottransparency)- [stochastic rsi.%d.color](#stochastic-rsidcolor)- [stochastic rsi.%d.display](#stochastic-rsiddisplay)- [stochastic rsi.%d.linestyle](#stochastic-rsidlinestyle)- [stochastic rsi.%d.linewidth](#stochastic-rsidlinewidth)- [stochastic rsi.%d.plottype](#stochastic-rsidplottype)- [stochastic rsi.%d.trackprice](#stochastic-rsidtrackprice)- [stochastic rsi.%d.transparency](#stochastic-rsidtransparency)- [stochastic rsi.%k.color](#stochastic-rsikcolor)- [stochastic rsi.%k.display](#stochastic-rsikdisplay)- [stochastic rsi.%k.linestyle](#stochastic-rsiklinestyle)- [stochastic rsi.%k.linewidth](#stochastic-rsiklinewidth)- [stochastic rsi.%k.plottype](#stochastic-rsikplottype)- [stochastic rsi.%k.trackprice](#stochastic-rsiktrackprice)- [stochastic rsi.%k.transparency](#stochastic-rsiktransparency)- [stochastic rsi.hlines background.color](#stochastic-rsihlines-backgroundcolor)- [stochastic rsi.hlines background.transparency](#stochastic-rsihlines-backgroundtransparency)- [stochastic rsi.hlines background.visible](#stochastic-rsihlines-backgroundvisible)- [stochastic rsi.lengthrsi](#stochastic-rsilengthrsi)- [stochastic rsi.lengthstoch](#stochastic-rsilengthstoch)- [stochastic rsi.lowerlimit.color](#stochastic-rsilowerlimitcolor)- [stochastic rsi.lowerlimit.linestyle](#stochastic-rsilowerlimitlinestyle)- [stochastic rsi.lowerlimit.linewidth](#stochastic-rsilowerlimitlinewidth)- [stochastic rsi.lowerlimit.value](#stochastic-rsilowerlimitvalue)- [stochastic rsi.lowerlimit.visible](#stochastic-rsilowerlimitvisible)- [stochastic rsi.smoothd](#stochastic-rsismoothd)- [stochastic rsi.smoothk](#stochastic-rsismoothk)- [stochastic rsi.upperlimit.color](#stochastic-rsiupperlimitcolor)- [stochastic rsi.upperlimit.linestyle](#stochastic-rsiupperlimitlinestyle)- [stochastic rsi.upperlimit.linewidth](#stochastic-rsiupperlimitlinewidth)- [stochastic rsi.upperlimit.value](#stochastic-rsiupperlimitvalue)- [stochastic rsi.upperlimit.visible](#stochastic-rsiupperlimitvisible)- [stochastic.%d smoothing](#stochasticd-smoothing)- [stochastic.%d.color](#stochasticdcolor)- [stochastic.%d.display](#stochasticddisplay)- [stochastic.%d.linestyle](#stochasticdlinestyle)- [stochastic.%d.linewidth](#stochasticdlinewidth)- [stochastic.%d.plottype](#stochasticdplottype)- [stochastic.%d.trackprice](#stochasticdtrackprice)- [stochastic.%d.transparency](#stochasticdtransparency)- [stochastic.%k length](#stochastick-length)- [stochastic.%k smoothing](#stochastick-smoothing)- [stochastic.%k.color](#stochastickcolor)- [stochastic.%k.display](#stochastickdisplay)- [stochastic.%k.linestyle](#stochasticklinestyle)- [stochastic.%k.linewidth](#stochasticklinewidth)- [stochastic.%k.plottype](#stochastickplottype)- [stochastic.%k.trackprice](#stochasticktrackprice)- [stochastic.%k.transparency](#stochasticktransparency)- [stochastic.hlines background.color](#stochastichlines-backgroundcolor)- [stochastic.hlines background.transparency](#stochastichlines-backgroundtransparency)- [stochastic.hlines background.visible](#stochastichlines-backgroundvisible)- [stochastic.lowerlimit.color](#stochasticlowerlimitcolor)- [stochastic.lowerlimit.linestyle](#stochasticlowerlimitlinestyle)- [stochastic.lowerlimit.linewidth](#stochasticlowerlimitlinewidth)- [stochastic.lowerlimit.value](#stochasticlowerlimitvalue)- [stochastic.lowerlimit.visible](#stochasticlowerlimitvisible)- [stochastic.upperlimit.color](#stochasticupperlimitcolor)- [stochastic.upperlimit.linestyle](#stochasticupperlimitlinestyle)- [stochastic.upperlimit.linewidth](#stochasticupperlimitlinewidth)- [stochastic.upperlimit.value](#stochasticupperlimitvalue)- [stochastic.upperlimit.visible](#stochasticupperlimitvisible)- [supertrend.down arrow.color](#supertrenddown-arrowcolor)- [supertrend.down arrow.display](#supertrenddown-arrowdisplay)- [supertrend.down arrow.linestyle](#supertrenddown-arrowlinestyle)- [supertrend.down arrow.linewidth](#supertrenddown-arrowlinewidth)- [supertrend.down arrow.location](#supertrenddown-arrowlocation)- [supertrend.down arrow.plottype](#supertrenddown-arrowplottype)- [supertrend.down arrow.trackprice](#supertrenddown-arrowtrackprice)- [supertrend.down arrow.transparency](#supertrenddown-arrowtransparency)- [supertrend.factor](#supertrendfactor)- [supertrend.length](#supertrendlength)- [supertrend.supertrend.color](#supertrendsupertrendcolor)- [supertrend.supertrend.display](#supertrendsupertrenddisplay)- [supertrend.supertrend.linestyle](#supertrendsupertrendlinestyle)- [supertrend.supertrend.linewidth](#supertrendsupertrendlinewidth)- [supertrend.supertrend.plottype](#supertrendsupertrendplottype)- [supertrend.supertrend.trackprice](#supertrendsupertrendtrackprice)- [supertrend.supertrend.transparency](#supertrendsupertrendtransparency)- [supertrend.up arrow.color](#supertrendup-arrowcolor)- [supertrend.up arrow.display](#supertrendup-arrowdisplay)- [supertrend.up arrow.linestyle](#supertrendup-arrowlinestyle)- [supertrend.up arrow.linewidth](#supertrendup-arrowlinewidth)- [supertrend.up arrow.location](#supertrendup-arrowlocation)- [supertrend.up arrow.plottype](#supertrendup-arrowplottype)- [supertrend.up arrow.trackprice](#supertrendup-arrowtrackprice)- [supertrend.up arrow.transparency](#supertrendup-arrowtransparency)- [trend strength index.periods](#trend-strength-indexperiods)- [trend strength index.plot.color](#trend-strength-indexplotcolor)- [trend strength index.plot.display](#trend-strength-indexplotdisplay)- [trend strength index.plot.linestyle](#trend-strength-indexplotlinestyle)- [trend strength index.plot.linewidth](#trend-strength-indexplotlinewidth)- [trend strength index.plot.plottype](#trend-strength-indexplotplottype)- [trend strength index.plot.trackprice](#trend-strength-indexplottrackprice)- [trend strength index.plot.transparency](#trend-strength-indexplottransparency)- [triple ema.length](#triple-emalength)- [triple ema.plot.color](#triple-emaplotcolor)- [triple ema.plot.display](#triple-emaplotdisplay)- [triple ema.plot.linestyle](#triple-emaplotlinestyle)- [triple ema.plot.linewidth](#triple-emaplotlinewidth)- [triple ema.plot.plottype](#triple-emaplotplottype)- [triple ema.plot.trackprice](#triple-emaplottrackprice)- [triple ema.plot.transparency](#triple-emaplottransparency)- [trix.length](#trixlength)- [trix.trix.color](#trixtrixcolor)- [trix.trix.display](#trixtrixdisplay)- [trix.trix.linestyle](#trixtrixlinestyle)- [trix.trix.linewidth](#trixtrixlinewidth)- [trix.trix.plottype](#trixtrixplottype)- [trix.trix.trackprice](#trixtrixtrackprice)- [trix.trix.transparency](#trixtrixtransparency)- [trix.zero.color](#trixzerocolor)- [trix.zero.linestyle](#trixzerolinestyle)- [trix.zero.linewidth](#trixzerolinewidth)- [trix.zero.value](#trixzerovalue)- [trix.zero.visible](#trixzerovisible)- [true strength index.long](#true-strength-indexlong)- [true strength index.short](#true-strength-indexshort)- [true strength index.siglen](#true-strength-indexsiglen)- [true strength index.signal.color](#true-strength-indexsignalcolor)- [true strength index.signal.display](#true-strength-indexsignaldisplay)- [true strength index.signal.linestyle](#true-strength-indexsignallinestyle)- [true strength index.signal.linewidth](#true-strength-indexsignallinewidth)- [true strength index.signal.plottype](#true-strength-indexsignalplottype)- [true strength index.signal.trackprice](#true-strength-indexsignaltrackprice)- [true strength index.signal.transparency](#true-strength-indexsignaltransparency)- [true strength index.true strength index.color](#true-strength-indextrue-strength-indexcolor)- [true strength index.true strength index.display](#true-strength-indextrue-strength-indexdisplay)- [true strength index.true strength index.linestyle](#true-strength-indextrue-strength-indexlinestyle)- [true strength index.true strength index.linewidth](#true-strength-indextrue-strength-indexlinewidth)- [true strength index.true strength index.plottype](#true-strength-indextrue-strength-indexplottype)- [true strength index.true strength index.trackprice](#true-strength-indextrue-strength-indextrackprice)- [true strength index.true strength index.transparency](#true-strength-indextrue-strength-indextransparency)- [true strength index.zero.color](#true-strength-indexzerocolor)- [true strength index.zero.linestyle](#true-strength-indexzerolinestyle)- [true strength index.zero.linewidth](#true-strength-indexzerolinewidth)- [true strength index.zero.value](#true-strength-indexzerovalue)- [true strength index.zero.visible](#true-strength-indexzerovisible)- [typical price.plot.color](#typical-priceplotcolor)- [typical price.plot.display](#typical-priceplotdisplay)- [typical price.plot.linestyle](#typical-priceplotlinestyle)- [typical price.plot.linewidth](#typical-priceplotlinewidth)- [typical price.plot.plottype](#typical-priceplotplottype)- [typical price.plot.trackprice](#typical-priceplottrackprice)- [typical price.plot.transparency](#typical-priceplottransparency)- [ultimate oscillator.length14](#ultimate-oscillatorlength14)- [ultimate oscillator.length28](#ultimate-oscillatorlength28)- [ultimate oscillator.length7](#ultimate-oscillatorlength7)- [ultimate oscillator.uo.color](#ultimate-oscillatoruocolor)- [ultimate oscillator.uo.display](#ultimate-oscillatoruodisplay)- [ultimate oscillator.uo.linestyle](#ultimate-oscillatoruolinestyle)- [ultimate oscillator.uo.linewidth](#ultimate-oscillatoruolinewidth)- [ultimate oscillator.uo.plottype](#ultimate-oscillatoruoplottype)- [ultimate oscillator.uo.trackprice](#ultimate-oscillatoruotrackprice)- [ultimate oscillator.uo.transparency](#ultimate-oscillatoruotransparency)- [volatility close-to-close.days per year](#volatility-close-to-closedays-per-year)- [volatility close-to-close.periods](#volatility-close-to-closeperiods)- [volatility close-to-close.plot.color](#volatility-close-to-closeplotcolor)- [volatility close-to-close.plot.display](#volatility-close-to-closeplotdisplay)- [volatility close-to-close.plot.linestyle](#volatility-close-to-closeplotlinestyle)- [volatility close-to-close.plot.linewidth](#volatility-close-to-closeplotlinewidth)- [volatility close-to-close.plot.plottype](#volatility-close-to-closeplotplottype)- [volatility close-to-close.plot.trackprice](#volatility-close-to-closeplottrackprice)- [volatility close-to-close.plot.transparency](#volatility-close-to-closeplottransparency)- [volatility index.atr mult](#volatility-indexatr-mult)- [volatility index.method](#volatility-indexmethod)- [volatility index.periods](#volatility-indexperiods)- [volatility index.plot.color](#volatility-indexplotcolor)- [volatility index.plot.display](#volatility-indexplotdisplay)- [volatility index.plot.linestyle](#volatility-indexplotlinestyle)- [volatility index.plot.linewidth](#volatility-indexplotlinewidth)- [volatility index.plot.plottype](#volatility-indexplotplottype)- [volatility index.plot.trackprice](#volatility-indexplottrackprice)- [volatility index.plot.transparency](#volatility-indexplottransparency)- [volatility o-h-l-c.days per year](#volatility-o-h-l-cdays-per-year)- [volatility o-h-l-c.market closed percentage](#volatility-o-h-l-cmarket-closed-percentage)- [volatility o-h-l-c.periods](#volatility-o-h-l-cperiods)- [volatility o-h-l-c.plot.color](#volatility-o-h-l-cplotcolor)- [volatility o-h-l-c.plot.display](#volatility-o-h-l-cplotdisplay)- [volatility o-h-l-c.plot.linestyle](#volatility-o-h-l-cplotlinestyle)- [volatility o-h-l-c.plot.linewidth](#volatility-o-h-l-cplotlinewidth)- [volatility o-h-l-c.plot.plottype](#volatility-o-h-l-cplotplottype)- [volatility o-h-l-c.plot.trackprice](#volatility-o-h-l-cplottrackprice)- [volatility o-h-l-c.plot.transparency](#volatility-o-h-l-cplottransparency)- [volatility zero trend close-to-close.days per year](#volatility-zero-trend-close-to-closedays-per-year)- [volatility zero trend close-to-close.periods](#volatility-zero-trend-close-to-closeperiods)- [volatility zero trend close-to-close.plot.color](#volatility-zero-trend-close-to-closeplotcolor)- [volatility zero trend close-to-close.plot.display](#volatility-zero-trend-close-to-closeplotdisplay)- [volatility zero trend close-to-close.plot.linestyle](#volatility-zero-trend-close-to-closeplotlinestyle)- [volatility zero trend close-to-close.plot.linewidth](#volatility-zero-trend-close-to-closeplotlinewidth)- [volatility zero trend close-to-close.plot.plottype](#volatility-zero-trend-close-to-closeplotplottype)- [volatility zero trend close-to-close.plot.trackprice](#volatility-zero-trend-close-to-closeplottrackprice)- [volatility zero trend close-to-close.plot.transparency](#volatility-zero-trend-close-to-closeplottransparency)- [volume oscillator.longlen](#volume-oscillatorlonglen)- [volume oscillator.plot.color](#volume-oscillatorplotcolor)- [volume oscillator.plot.display](#volume-oscillatorplotdisplay)- [volume oscillator.plot.linestyle](#volume-oscillatorplotlinestyle)- [volume oscillator.plot.linewidth](#volume-oscillatorplotlinewidth)- [volume oscillator.plot.plottype](#volume-oscillatorplotplottype)- [volume oscillator.plot.trackprice](#volume-oscillatorplottrackprice)- [volume oscillator.plot.transparency](#volume-oscillatorplottransparency)- [volume oscillator.shortlen](#volume-oscillatorshortlen)- [volume oscillator.zero.color](#volume-oscillatorzerocolor)- [volume oscillator.zero.linestyle](#volume-oscillatorzerolinestyle)- [volume oscillator.zero.linewidth](#volume-oscillatorzerolinewidth)- [volume oscillator.zero.value](#volume-oscillatorzerovalue)- [volume oscillator.zero.visible](#volume-oscillatorzerovisible)- [volume profile fixed range.developing poc.color](#volume-profile-fixed-rangedeveloping-poccolor)- [volume profile fixed range.developing poc.display](#volume-profile-fixed-rangedeveloping-pocdisplay)- [volume profile fixed range.developing poc.linestyle](#volume-profile-fixed-rangedeveloping-poclinestyle)- [volume profile fixed range.developing poc.linewidth](#volume-profile-fixed-rangedeveloping-poclinewidth)- [volume profile fixed range.developing poc.plottype](#volume-profile-fixed-rangedeveloping-pocplottype)- [volume profile fixed range.developing poc.trackprice](#volume-profile-fixed-rangedeveloping-poctrackprice)- [volume profile fixed range.developing poc.transparency](#volume-profile-fixed-rangedeveloping-poctransparency)- [volume profile fixed range.developing va high.color](#volume-profile-fixed-rangedeveloping-va-highcolor)- [volume profile fixed range.developing va high.display](#volume-profile-fixed-rangedeveloping-va-highdisplay)- [volume profile fixed range.developing va high.linestyle](#volume-profile-fixed-rangedeveloping-va-highlinestyle)- [volume profile fixed range.developing va high.linewidth](#volume-profile-fixed-rangedeveloping-va-highlinewidth)- [volume profile fixed range.developing va high.plottype](#volume-profile-fixed-rangedeveloping-va-highplottype)- [volume profile fixed range.developing va high.trackprice](#volume-profile-fixed-rangedeveloping-va-hightrackprice)- [volume profile fixed range.developing va high.transparency](#volume-profile-fixed-rangedeveloping-va-hightransparency)- [volume profile fixed range.developing va low.color](#volume-profile-fixed-rangedeveloping-va-lowcolor)- [volume profile fixed range.developing va low.display](#volume-profile-fixed-rangedeveloping-va-lowdisplay)- [volume profile fixed range.developing va low.linestyle](#volume-profile-fixed-rangedeveloping-va-lowlinestyle)- [volume profile fixed range.developing va low.linewidth](#volume-profile-fixed-rangedeveloping-va-lowlinewidth)- [volume profile fixed range.developing va low.plottype](#volume-profile-fixed-rangedeveloping-va-lowplottype)- [volume profile fixed range.developing va low.trackprice](#volume-profile-fixed-rangedeveloping-va-lowtrackprice)- [volume profile fixed range.developing va low.transparency](#volume-profile-fixed-rangedeveloping-va-lowtransparency)- [volume profile fixed range.first bar time](#volume-profile-fixed-rangefirst-bar-time)- [volume profile fixed range.last bar time](#volume-profile-fixed-rangelast-bar-time)- [volume profile fixed range.row size](#volume-profile-fixed-rangerow-size)- [volume profile fixed range.rows layout](#volume-profile-fixed-rangerows-layout)- [volume profile fixed range.subscriberealtime](#volume-profile-fixed-rangesubscriberealtime)- [volume profile fixed range.value area volume](#volume-profile-fixed-rangevalue-area-volume)- [volume profile fixed range.volume](#volume-profile-fixed-rangevolume)- [volume profile visible range.developing poc.color](#volume-profile-visible-rangedeveloping-poccolor)- [volume profile visible range.developing poc.display](#volume-profile-visible-rangedeveloping-pocdisplay)- [volume profile visible range.developing poc.linestyle](#volume-profile-visible-rangedeveloping-poclinestyle)- [volume profile visible range.developing poc.linewidth](#volume-profile-visible-rangedeveloping-poclinewidth)- [volume profile visible range.developing poc.plottype](#volume-profile-visible-rangedeveloping-pocplottype)- [volume profile visible range.developing poc.trackprice](#volume-profile-visible-rangedeveloping-poctrackprice)- [volume profile visible range.developing poc.transparency](#volume-profile-visible-rangedeveloping-poctransparency)- [volume profile visible range.developing va high.color](#volume-profile-visible-rangedeveloping-va-highcolor)- [volume profile visible range.developing va high.display](#volume-profile-visible-rangedeveloping-va-highdisplay)- [volume profile visible range.developing va high.linestyle](#volume-profile-visible-rangedeveloping-va-highlinestyle)- [volume profile visible range.developing va high.linewidth](#volume-profile-visible-rangedeveloping-va-highlinewidth)- [volume profile visible range.developing va high.plottype](#volume-profile-visible-rangedeveloping-va-highplottype)- [volume profile visible range.developing va high.trackprice](#volume-profile-visible-rangedeveloping-va-hightrackprice)- [volume profile visible range.developing va high.transparency](#volume-profile-visible-rangedeveloping-va-hightransparency)- [volume profile visible range.developing va low.color](#volume-profile-visible-rangedeveloping-va-lowcolor)- [volume profile visible range.developing va low.display](#volume-profile-visible-rangedeveloping-va-lowdisplay)- [volume profile visible range.developing va low.linestyle](#volume-profile-visible-rangedeveloping-va-lowlinestyle)- [volume profile visible range.developing va low.linewidth](#volume-profile-visible-rangedeveloping-va-lowlinewidth)- [volume profile visible range.developing va low.plottype](#volume-profile-visible-rangedeveloping-va-lowplottype)- [volume profile visible range.developing va low.trackprice](#volume-profile-visible-rangedeveloping-va-lowtrackprice)- [volume profile visible range.developing va low.transparency](#volume-profile-visible-rangedeveloping-va-lowtransparency)- [volume profile visible range.first visible bar time](#volume-profile-visible-rangefirst-visible-bar-time)- [volume profile visible range.last visible bar time](#volume-profile-visible-rangelast-visible-bar-time)- [volume profile visible range.row size](#volume-profile-visible-rangerow-size)- [volume profile visible range.rows layout](#volume-profile-visible-rangerows-layout)- [volume profile visible range.value area volume](#volume-profile-visible-rangevalue-area-volume)- [volume profile visible range.volume](#volume-profile-visible-rangevolume)- [volume.color based on previous close](#volumecolor-based-on-previous-close)- [volume.ma length](#volumema-length)- [volume.other symbol](#volumeother-symbol)- [volume.show ma](#volumeshow-ma)- [volume.smoothed ma.color](#volumesmoothed-macolor)- [volume.smoothed ma.display](#volumesmoothed-madisplay)- [volume.smoothed ma.linestyle](#volumesmoothed-malinestyle)- [volume.smoothed ma.linewidth](#volumesmoothed-malinewidth)- [volume.smoothed ma.plottype](#volumesmoothed-maplottype)- [volume.smoothed ma.trackprice](#volumesmoothed-matrackprice)- [volume.smoothed ma.transparency](#volumesmoothed-matransparency)- [volume.smoothing length](#volumesmoothing-length)- [volume.smoothing line](#volumesmoothing-line)- [volume.volume ma](#volumevolume-ma)- [volume.volume ma.color](#volumevolume-macolor)- [volume.volume ma.display](#volumevolume-madisplay)- [volume.volume ma.linestyle](#volumevolume-malinestyle)- [volume.volume ma.linewidth](#volumevolume-malinewidth)- [volume.volume ma.plottype](#volumevolume-maplottype)- [volume.volume ma.trackprice](#volumevolume-matrackprice)- [volume.volume ma.transparency](#volumevolume-matransparency)- [volume.volume.color](#volumevolumecolor)- [volume.volume.display](#volumevolumedisplay)- [volume.volume.linestyle](#volumevolumelinestyle)- [volume.volume.linewidth](#volumevolumelinewidth)- [volume.volume.plottype](#volumevolumeplottype)- [volume.volume.trackprice](#volumevolumetrackprice)- [volume.volume.transparency](#volumevolumetransparency)- [vortex indicator.period](#vortex-indicatorperiod)- [vortex indicator.vi +.color](#vortex-indicatorvi-color)- [vortex indicator.vi +.display](#vortex-indicatorvi-display)- [vortex indicator.vi +.linestyle](#vortex-indicatorvi-linestyle)- [vortex indicator.vi +.linewidth](#vortex-indicatorvi-linewidth)- [vortex indicator.vi +.plottype](#vortex-indicatorvi-plottype)- [vortex indicator.vi +.trackprice](#vortex-indicatorvi-trackprice)- [vortex indicator.vi +.transparency](#vortex-indicatorvi-transparency)- [vortex indicator.vi -.color](#vortex-indicatorvi--color)- [vortex indicator.vi -.display](#vortex-indicatorvi--display)- [vortex indicator.vi -.linestyle](#vortex-indicatorvi--linestyle)- [vortex indicator.vi -.linewidth](#vortex-indicatorvi--linewidth)- [vortex indicator.vi -.plottype](#vortex-indicatorvi--plottype)- [vortex indicator.vi -.trackprice](#vortex-indicatorvi--trackprice)- [vortex indicator.vi -.transparency](#vortex-indicatorvi--transparency)- [vwap.anchor period](#vwapanchor-period)- [vwap.source](#vwapsource)- [vwap.vwap.color](#vwapvwapcolor)- [vwap.vwap.display](#vwapvwapdisplay)- [vwap.vwap.linestyle](#vwapvwaplinestyle)- [vwap.vwap.linewidth](#vwapvwaplinewidth)- [vwap.vwap.plottype](#vwapvwapplottype)- [vwap.vwap.trackprice](#vwapvwaptrackprice)- [vwap.vwap.transparency](#vwapvwaptransparency)- [vwma.len](#vwmalen)- [vwma.plot.color](#vwmaplotcolor)- [vwma.plot.display](#vwmaplotdisplay)- [vwma.plot.linestyle](#vwmaplotlinestyle)- [vwma.plot.linewidth](#vwmaplotlinewidth)- [vwma.plot.plottype](#vwmaplotplottype)- [vwma.plot.trackprice](#vwmaplottrackprice)- [vwma.plot.transparency](#vwmaplottransparency)- [williams %r.hlines background.color](#williams-rhlines-backgroundcolor)- [williams %r.hlines background.transparency](#williams-rhlines-backgroundtransparency)- [williams %r.hlines background.visible](#williams-rhlines-backgroundvisible)- [williams %r.length](#williams-rlength)- [williams %r.lowerlimit.color](#williams-rlowerlimitcolor)- [williams %r.lowerlimit.linestyle](#williams-rlowerlimitlinestyle)- [williams %r.lowerlimit.linewidth](#williams-rlowerlimitlinewidth)- [williams %r.lowerlimit.value](#williams-rlowerlimitvalue)- [williams %r.lowerlimit.visible](#williams-rlowerlimitvisible)- [williams %r.plot.color](#williams-rplotcolor)- [williams %r.plot.display](#williams-rplotdisplay)- [williams %r.plot.linestyle](#williams-rplotlinestyle)- [williams %r.plot.linewidth](#williams-rplotlinewidth)- [williams %r.plot.plottype](#williams-rplotplottype)- [williams %r.plot.trackprice](#williams-rplottrackprice)- [williams %r.plot.transparency](#williams-rplottransparency)- [williams %r.upperlimit.color](#williams-rupperlimitcolor)- [williams %r.upperlimit.linestyle](#williams-rupperlimitlinestyle)- [williams %r.upperlimit.linewidth](#williams-rupperlimitlinewidth)- [williams %r.upperlimit.value](#williams-rupperlimitvalue)- [williams %r.upperlimit.visible](#williams-rupperlimitvisible)- [williams alligator.jaw length](#williams-alligatorjaw-length)- [williams alligator.jaw offset](#williams-alligatorjaw-offset)- [williams alligator.jaw.color](#williams-alligatorjawcolor)- [williams alligator.jaw.display](#williams-alligatorjawdisplay)- [williams alligator.jaw.linestyle](#williams-alligatorjawlinestyle)- [williams alligator.jaw.linewidth](#williams-alligatorjawlinewidth)- [williams alligator.jaw.plottype](#williams-alligatorjawplottype)- [williams alligator.jaw.trackprice](#williams-alligatorjawtrackprice)- [williams alligator.jaw.transparency](#williams-alligatorjawtransparency)- [williams alligator.lips length](#williams-alligatorlips-length)- [williams alligator.lips offset](#williams-alligatorlips-offset)- [williams alligator.lips.color](#williams-alligatorlipscolor)- [williams alligator.lips.display](#williams-alligatorlipsdisplay)- [williams alligator.lips.linestyle](#williams-alligatorlipslinestyle)- [williams alligator.lips.linewidth](#williams-alligatorlipslinewidth)- [williams alligator.lips.plottype](#williams-alligatorlipsplottype)- [williams alligator.lips.trackprice](#williams-alligatorlipstrackprice)- [williams alligator.lips.transparency](#williams-alligatorlipstransparency)- [williams alligator.teeth length](#williams-alligatorteeth-length)- [williams alligator.teeth offset](#williams-alligatorteeth-offset)- [williams alligator.teeth.color](#williams-alligatorteethcolor)- [williams alligator.teeth.display](#williams-alligatorteethdisplay)- [williams alligator.teeth.linestyle](#williams-alligatorteethlinestyle)- [williams alligator.teeth.linewidth](#williams-alligatorteethlinewidth)- [williams alligator.teeth.plottype](#williams-alligatorteethplottype)- [williams alligator.teeth.trackprice](#williams-alligatorteethtrackprice)- [williams alligator.teeth.transparency](#williams-alligatorteethtransparency)- [williams fractal.down fractals.color](#williams-fractaldown-fractalscolor)- [williams fractal.down fractals.display](#williams-fractaldown-fractalsdisplay)- [williams fractal.down fractals.location](#williams-fractaldown-fractalslocation)- [williams fractal.down fractals.plottype](#williams-fractaldown-fractalsplottype)- [williams fractal.down fractals.transparency](#williams-fractaldown-fractalstransparency)- [williams fractal.periods](#williams-fractalperiods)- [williams fractal.up fractals.color](#williams-fractalup-fractalscolor)- [williams fractal.up fractals.display](#williams-fractalup-fractalsdisplay)- [williams fractal.up fractals.location](#williams-fractalup-fractalslocation)- [williams fractal.up fractals.plottype](#williams-fractalup-fractalsplottype)- [williams fractal.up fractals.transparency](#williams-fractalup-fractalstransparency)- [zig zag.depth](#zig-zagdepth)- [zig zag.deviation](#zig-zagdeviation)- [zig zag.plot.color](#zig-zagplotcolor)- [zig zag.plot.display](#zig-zagplotdisplay)- [zig zag.plot.linestyle](#zig-zagplotlinestyle)- [zig zag.plot.linewidth](#zig-zagplotlinewidth)- [zig zag.plot.plottype](#zig-zagplotplottype)- [zig zag.plot.trackprice](#zig-zagplottrackprice)- [zig zag.plot.transparency](#zig-zagplottransparency)