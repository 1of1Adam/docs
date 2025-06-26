---
title: "Interface: StudyCandleWickColorerPlotInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyCandleWickColorerPlotInfo"
extracted_at: "2025-06-22T09:45:59.204Z"
---

- [](/charting-library-docs/)- Interfaces- StudyCandleWickColorerPlotInfoOn this page# Interface: StudyCandleWickColorerPlotInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyCandleWickColorerPlotInfo

A description of a wick colorer plot.

## Hierarchy[​](#hierarchy)

[`StudyPalettedPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPalettedPlotInfo)

[`StudyTargetedPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo)

↳ `StudyCandleWickColorerPlotInfo`

## Properties[​](#properties)
### id[​](#id)
• `Readonly` id: `string`

Plot ID.

#### Inherited from[​](#inherited-from)
[StudyTargetedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo#id)

### palette[​](#palette)
• `Readonly` palette: `string`

A color palette ID.

#### Inherited from[​](#inherited-from-1)
[StudyPalettedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPalettedPlotInfo).[palette](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPalettedPlotInfo#palette)

### target[​](#target)
• `Readonly` target: `string`

ID of another target plot.

#### Inherited from[​](#inherited-from-2)
[StudyTargetedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo).[target](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo#target)

### targetField[​](#targetfield)
• `Optional` `Readonly` targetField: `"topColor"` | `"bottomColor"` | `"topValue"` | `"bottomValue"`

Target field.

#### Inherited from[​](#inherited-from-3)
[StudyTargetedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo).[targetField](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo#targetfield)

### type[​](#type)
• `Readonly` type: [`CandleWickColorer`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyPlotType#candlewickcolorer)

Plot type.

#### Overrides[​](#overrides)
[StudyTargetedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo).[type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo#type)

- [Hierarchy](#hierarchy)- [Properties](#properties)[id](#id)- [palette](#palette)- [target](#target)- [targetField](#targetfield)- [type](#type)