---
title: "Interface: StudyOhlcPlotInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOhlcPlotInfo"
extracted_at: "2025-06-22T09:46:54.767Z"
---

- [](/charting-library-docs/)- Interfaces- StudyOhlcPlotInfoOn this page# Interface: StudyOhlcPlotInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyOhlcPlotInfo

A description of an OHLC plot.

## Hierarchy[​](#hierarchy)

[`StudyTargetedPlotInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo)

↳ `StudyOhlcPlotInfo`

## Properties[​](#properties)
### id[​](#id)
• `Readonly` id: `string`

Plot ID.

#### Inherited from[​](#inherited-from)
[StudyTargetedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo#id)

### target[​](#target)
• `Readonly` target: `string`

ID of another target plot.

#### Inherited from[​](#inherited-from-1)
[StudyTargetedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo).[target](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo#target)

### targetField[​](#targetfield)
• `Optional` `Readonly` targetField: `"topColor"` | `"bottomColor"` | `"topValue"` | `"bottomValue"`

Target field.

#### Inherited from[​](#inherited-from-2)
[StudyTargetedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo).[targetField](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo#targetfield)

### type[​](#type)
• `Readonly` type: [`OhlcOpen`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyPlotType#ohlcopen) | [`OhlcHigh`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyPlotType#ohlchigh) | [`OhlcLow`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyPlotType#ohlclow) | [`OhlcClose`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyPlotType#ohlcclose)

Plot type.

#### Overrides[​](#overrides)
[StudyTargetedPlotInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo).[type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTargetedPlotInfo#type)

- [Hierarchy](#hierarchy)- [Properties](#properties)[id](#id)- [target](#target)- [targetField](#targetfield)- [type](#type)