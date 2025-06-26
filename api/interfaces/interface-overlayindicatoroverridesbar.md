---
title: "Interface: OverlayIndicatorOverridesBar | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OverlayIndicatorOverridesBar"
extracted_at: "2025-06-22T09:42:34.507Z"
---

- [](/charting-library-docs/)- Interfaces- OverlayIndicatorOverridesBarOn this page# Interface: OverlayIndicatorOverridesBar[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).OverlayIndicatorOverridesBar

## Hierarchy[​](#hierarchy)

`Partial`<[`BarStylePreferences`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BarStylePreferences)>

↳ `OverlayIndicatorOverridesBar`

## Indexable[​](#indexable)
▪ [key: `string`]: [`StudyOverrideValueType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyoverridevaluetype) | `undefined`

Use the properties as follow: `barStyle.downColor`: `pink`

## Properties[​](#properties)
### barColorsOnPrevClose[​](#barcolorsonprevclose)
• `Optional` barColorsOnPrevClose: `boolean`

Bar color determined by previous close value

#### Inherited from[​](#inherited-from)
Partial.barColorsOnPrevClose

### dontDrawOpen[​](#dontdrawopen)
• `Optional` dontDrawOpen: `boolean`

Whether to draw opening value for bar

#### Inherited from[​](#inherited-from-1)
Partial.dontDrawOpen

### downColor[​](#downcolor)
• `Optional` downColor: `string`

Down bar color

#### Inherited from[​](#inherited-from-2)
Partial.downColor

### style[​](#style)
• style: [`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle#bar)

### thinBars[​](#thinbars)
• `Optional` thinBars: `boolean`

Draw thin bars. Default - `true`

#### Inherited from[​](#inherited-from-3)
Partial.thinBars

### upColor[​](#upcolor)
• `Optional` upColor: `string`

Up bar color

#### Inherited from[​](#inherited-from-4)
Partial.upColor

- [Hierarchy](#hierarchy)- [Indexable](#indexable)- [Properties](#properties)[barColorsOnPrevClose](#barcolorsonprevclose)- [dontDrawOpen](#dontdrawopen)- [downColor](#downcolor)- [style](#style)- [thinBars](#thinbars)- [upColor](#upcolor)