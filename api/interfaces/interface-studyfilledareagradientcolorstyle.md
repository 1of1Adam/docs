---
title: "Interface: StudyFilledAreaGradientColorStyle | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaGradientColorStyle"
extracted_at: "2025-06-22T09:46:21.215Z"
---

- [](/charting-library-docs/)- Interfaces- StudyFilledAreaGradientColorStyleOn this page# Interface: StudyFilledAreaGradientColorStyle[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyFilledAreaGradientColorStyle

Study filled area gradient styles.

## Hierarchy[​](#hierarchy)

[`StudyFilledAreaStyleBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaStyleBase)

↳ `StudyFilledAreaGradientColorStyle`

## Properties[​](#properties)
### bottomColor[​](#bottomcolor)
• `Optional` bottomColor: `string`

Gradient bottom color.

### bottomValue[​](#bottomvalue)
• `Optional` bottomValue: `number`

Value at which the bottom of the gradient is drawn.

`Example`

```
75 // Drawn at price = 75
```

### fillType[​](#filltype)
• fillType: `"gradient"`

Gradient fill type

### topColor[​](#topcolor)
• `Optional` topColor: `string`

Gradient top color.

### topValue[​](#topvalue)
• `Optional` topValue: `number`

Value at which the top of the gradient is drawn.

`Example`

```
75 // Drawn at price = 75
```

### transparency[​](#transparency)
• `Optional` transparency: `number`

Filled area's transparency.

`Min`

0

`Max`

100

#### Inherited from[​](#inherited-from)
[StudyFilledAreaStyleBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaStyleBase).[transparency](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaStyleBase#transparency)

### visible[​](#visible)
• visible: `boolean`

Filled area's visibility.

#### Inherited from[​](#inherited-from-1)
[StudyFilledAreaStyleBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaStyleBase).[visible](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaStyleBase#visible)

- [Hierarchy](#hierarchy)- [Properties](#properties)[bottomColor](#bottomcolor)- [bottomValue](#bottomvalue)- [fillType](#filltype)- [topColor](#topcolor)- [topValue](#topvalue)- [transparency](#transparency)- [visible](#visible)