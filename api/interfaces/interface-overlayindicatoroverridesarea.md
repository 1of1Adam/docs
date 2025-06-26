---
title: "Interface: OverlayIndicatorOverridesArea | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OverlayIndicatorOverridesArea"
extracted_at: "2025-06-22T09:42:33.323Z"
---

- [](/charting-library-docs/)- Interfaces- OverlayIndicatorOverridesAreaOn this page# Interface: OverlayIndicatorOverridesArea[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).OverlayIndicatorOverridesArea

## Hierarchy[​](#hierarchy)

`Partial`<[`AreaStylePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AreaStylePreferences)>

↳ `OverlayIndicatorOverridesArea`

## Indexable[​](#indexable)
▪ [key: `string`]: [`StudyOverrideValueType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyoverridevaluetype) | `undefined`

Use the properties as follow: `areaStyle.color1`: `pink`

## Properties[​](#properties)
### color1[​](#color1)
• `Optional` color1: `string`

Top color

#### Inherited from[​](#inherited-from)
Partial.color1

### color2[​](#color2)
• `Optional` color2: `string`

Bottom color

#### Inherited from[​](#inherited-from-1)
Partial.color2

### linecolor[​](#linecolor)
• `Optional` linecolor: `string`

Line Color

#### Inherited from[​](#inherited-from-2)
Partial.linecolor

### linestyle[​](#linestyle)
• `Optional` linestyle: `number`

Line Style [LineStyle](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.LineStyle)

#### Inherited from[​](#inherited-from-3)
Partial.linestyle

### linewidth[​](#linewidth)
• `Optional` linewidth: `number`

Line width

#### Inherited from[​](#inherited-from-4)
Partial.linewidth

### style[​](#style)
• style: [`Area`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle#area)

### transparency[​](#transparency)
• `Optional` transparency: `number`

Transparency. Range [0..100]
`0` - fully opaque,
`100` - fully transparent.
Note: Rather use `rgba` color string for setting transparency.

#### Inherited from[​](#inherited-from-5)
Partial.transparency

- [Hierarchy](#hierarchy)- [Indexable](#indexable)- [Properties](#properties)[color1](#color1)- [color2](#color2)- [linecolor](#linecolor)- [linestyle](#linestyle)- [linewidth](#linewidth)- [style](#style)- [transparency](#transparency)