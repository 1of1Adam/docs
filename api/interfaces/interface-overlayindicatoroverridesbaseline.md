---
title: "Interface: OverlayIndicatorOverridesBaseline | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OverlayIndicatorOverridesBaseline"
extracted_at: "2025-06-22T09:42:36.349Z"
---

- [](/charting-library-docs/)- Interfaces- OverlayIndicatorOverridesBaselineOn this page# Interface: OverlayIndicatorOverridesBaseline[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).OverlayIndicatorOverridesBaseline

## Hierarchy[​](#hierarchy)

`Partial`<[`BaselineStylePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BaselineStylePreferences)>

↳ `OverlayIndicatorOverridesBaseline`

## Indexable[​](#indexable)
▪ [key: `string`]: [`StudyOverrideValueType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyoverridevaluetype) | `undefined`

Use the properties as follow: `baselineStyle.baselineColor`: `pink`

## Properties[​](#properties)
### baseLevelPercentage[​](#baselevelpercentage)
• `Optional` baseLevelPercentage: `number`

Baseline level percentage

#### Inherited from[​](#inherited-from)
Partial.baseLevelPercentage

### baselineColor[​](#baselinecolor)
• `Optional` baselineColor: `string`

Baseline line color

#### Inherited from[​](#inherited-from-1)
Partial.baselineColor

### bottomFillColor1[​](#bottomfillcolor1)
• `Optional` bottomFillColor1: `string`

Top fill color of negative area

#### Inherited from[​](#inherited-from-2)
Partial.bottomFillColor1

### bottomFillColor2[​](#bottomfillcolor2)
• `Optional` bottomFillColor2: `string`

Bottom fill color of negative area

#### Inherited from[​](#inherited-from-3)
Partial.bottomFillColor2

### bottomLineColor[​](#bottomlinecolor)
• `Optional` bottomLineColor: `string`

Negative area line color

#### Inherited from[​](#inherited-from-4)
Partial.bottomLineColor

### bottomLineWidth[​](#bottomlinewidth)
• `Optional` bottomLineWidth: `number`

Negative area line width

#### Inherited from[​](#inherited-from-5)
Partial.bottomLineWidth

### style[​](#style)
• style: [`Baseline`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle#baseline)

### topFillColor1[​](#topfillcolor1)
• `Optional` topFillColor1: `string`

Top fill color of positive area

#### Inherited from[​](#inherited-from-6)
Partial.topFillColor1

### topFillColor2[​](#topfillcolor2)
• `Optional` topFillColor2: `string`

Bottom fill color of positive area

#### Inherited from[​](#inherited-from-7)
Partial.topFillColor2

### topLineColor[​](#toplinecolor)
• `Optional` topLineColor: `string`

Positive area line color

#### Inherited from[​](#inherited-from-8)
Partial.topLineColor

### topLineWidth[​](#toplinewidth)
• `Optional` topLineWidth: `number`

Positive area line width

#### Inherited from[​](#inherited-from-9)
Partial.topLineWidth

### transparency[​](#transparency)
• `Optional` transparency: `number`

Transparency. Range [0..100]
`0` - fully opaque,
`100` - fully transparent.
Note: Rather use `rgba` color string for setting transparency.

#### Inherited from[​](#inherited-from-10)
Partial.transparency

- [Hierarchy](#hierarchy)- [Indexable](#indexable)- [Properties](#properties)[baseLevelPercentage](#baselevelpercentage)- [baselineColor](#baselinecolor)- [bottomFillColor1](#bottomfillcolor1)- [bottomFillColor2](#bottomfillcolor2)- [bottomLineColor](#bottomlinecolor)- [bottomLineWidth](#bottomlinewidth)- [style](#style)- [topFillColor1](#topfillcolor1)- [topFillColor2](#topfillcolor2)- [topLineColor](#toplinecolor)- [topLineWidth](#toplinewidth)- [transparency](#transparency)