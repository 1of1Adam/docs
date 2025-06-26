---
title: "Interface: StudyInputBaseInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo"
extracted_at: "2025-06-22T09:46:30.149Z"
---

- [](/charting-library-docs/)- Interfaces- StudyInputBaseInfoOn this page# Interface: StudyInputBaseInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyInputBaseInfo

## Hierarchy[​](#hierarchy)

`StudyInputBaseInfo`

↳ [`StudyBarTimeInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBarTimeInputInfo)

↳ [`StudyBooleanInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBooleanInputInfo)

↳ [`StudyColorInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyColorInputInfo)

↳ [`StudyNumericInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyNumericInputInfo)

↳ [`StudyPriceInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyPriceInputInfo)

↳ [`StudyResolutionInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyResolutionInputInfo)

↳ [`StudySessionInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudySessionInputInfo)

↳ [`StudySourceInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudySourceInputInfo)

↳ [`StudySymbolInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudySymbolInputInfo)

↳ [`StudyTextInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTextInputInfo)

↳ [`StudyTextareaInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTextareaInputInfo)

↳ [`StudyTimeInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTimeInputInfo)

## Properties[​](#properties)
### confirm[​](#confirm)
• `Optional` `Readonly` confirm: `boolean`

if true, then user will be asked to confirm input value before indicator is added to chart. Default value is false.

### defval[​](#defval)
• `Optional` `Readonly` defval: [`StudyInputValue`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyinputvalue)

default value of the input variable. It has the specific type for a given input and can be optional.

### hideWhenPlotsHidden[​](#hidewhenplotshidden)
• `Optional` `Readonly` hideWhenPlotsHidden: `string`[]

An array of plot ids, upon the hiding of which, this input should also be hidden within the legend

### id[​](#id)
• `Readonly` id: `string`

Id for the input

### isHidden[​](#ishidden)
• `Optional` `Readonly` isHidden: `boolean`

Is the input hidden

### name[​](#name)
• `Readonly` name: `string`

Title of the input

### type[​](#type)
• `Readonly` type: [`StudyInputType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyInputType)

Input type

### visible[​](#visible)
• `Optional` `Readonly` visible: `string`

Is the input visible

- [Hierarchy](#hierarchy)- [Properties](#properties)[confirm](#confirm)- [defval](#defval)- [hideWhenPlotsHidden](#hidewhenplotshidden)- [id](#id)- [isHidden](#ishidden)- [name](#name)- [type](#type)- [visible](#visible)