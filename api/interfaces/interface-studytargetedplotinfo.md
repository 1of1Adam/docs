---
title: "Interface: StudyTargetedPlotInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo"
extracted_at: "2025-06-22T09:47:53.480Z"
---

- [](/charting-library-docs/)- Interfaces- StudyTargetedPlotInfoOn this page# Interface: StudyTargetedPlotInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyTargetedPlotInfo

A description of a study plot with a target.

## Hierarchy[​](#hierarchy)

[`StudyPlotBaseInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBaseInfo)

↳ `StudyTargetedPlotInfo`

↳↳ [`StudyCandleBorderColorerPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyCandleBorderColorerPlotInfo)

↳↳ [`StudyCandleWickColorerPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyCandleWickColorerPlotInfo)

↳↳ [`StudyColorerPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyColorerPlotInfo)

↳↳ [`StudyDataOffsetPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyDataOffsetPlotInfo)

↳↳ [`StudyDataPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyDataPlotInfo)

↳↳ [`StudyDownColorerPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyDownColorerPlotInfo)

↳↳ [`StudyOhlcColorerPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOhlcColorerPlotInfo)

↳↳ [`StudyOhlcPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOhlcPlotInfo)

↳↳ [`StudyRgbaColorerPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyRgbaColorerPlotInfo)

↳↳ [`StudyTextColorerPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTextColorerPlotInfo)

↳↳ [`StudyUpColorerPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyUpColorerPlotInfo)

## Properties[​](#properties)
### id[​](#id)
• `Readonly` id: `string`

Plot ID.

#### Inherited from[​](#inherited-from)
[StudyPlotBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBaseInfo).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBaseInfo#id)

### target[​](#target)
• `Readonly` target: `string`

ID of another target plot.

### targetField[​](#targetfield)
• `Optional` `Readonly` targetField: `"topColor"` | `"bottomColor"` | `"topValue"` | `"bottomValue"`

Target field.

### type[​](#type)
• `Readonly` type: `string`

Plot type.

#### Inherited from[​](#inherited-from-1)
[StudyPlotBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBaseInfo).[type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPlotBaseInfo#type)

- [Hierarchy](#hierarchy)- [Properties](#properties)[id](#id)- [target](#target)- [targetField](#targetfield)- [type](#type)