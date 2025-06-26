---
title: "Interface: StudyBooleanInputInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBooleanInputInfo"
extracted_at: "2025-06-22T09:45:52.279Z"
---

- [](/charting-library-docs/)- Interfaces- StudyBooleanInputInfoOn this page# Interface: StudyBooleanInputInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyBooleanInputInfo

## Hierarchy[​](#hierarchy)

[`StudyInputBaseInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo)

↳ `StudyBooleanInputInfo`

## Properties[​](#properties)
### confirm[​](#confirm)
• `Optional` `Readonly` confirm: `boolean`

if true, then user will be asked to confirm input value before indicator is added to chart. Default value is false.

#### Inherited from[​](#inherited-from)
[StudyInputBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo).[confirm](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo#confirm)

### defval[​](#defval)
• `Readonly` defval: `boolean`

Default value for the input

#### Overrides[​](#overrides)
[StudyInputBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo).[defval](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo#defval)

### hideWhenPlotsHidden[​](#hidewhenplotshidden)
• `Optional` `Readonly` hideWhenPlotsHidden: `string`[]

An array of plot ids, upon the hiding of which, this input should also be hidden within the legend

#### Inherited from[​](#inherited-from-1)
[StudyInputBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo).[hideWhenPlotsHidden](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo#hidewhenplotshidden)

### id[​](#id)
• `Readonly` id: `string`

Id for the input

#### Inherited from[​](#inherited-from-2)
[StudyInputBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo#id)

### isHidden[​](#ishidden)
• `Optional` `Readonly` isHidden: `boolean`

Is the input hidden

#### Inherited from[​](#inherited-from-3)
[StudyInputBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo).[isHidden](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo#ishidden)

### name[​](#name)
• `Readonly` name: `string`

Title of the input

#### Inherited from[​](#inherited-from-4)
[StudyInputBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo).[name](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo#name)

### type[​](#type)
• `Readonly` type: [`Bool`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.StudyInputType#bool)

Input type is Boolean

#### Overrides[​](#overrides-1)
[StudyInputBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo).[type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo#type)

### visible[​](#visible)
• `Optional` `Readonly` visible: `string`

Is the input visible

#### Inherited from[​](#inherited-from-5)
[StudyInputBaseInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo).[visible](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputBaseInfo#visible)

- [Hierarchy](#hierarchy)- [Properties](#properties)[confirm](#confirm)- [defval](#defval)- [hideWhenPlotsHidden](#hidewhenplotshidden)- [id](#id)- [isHidden](#ishidden)- [name](#name)- [type](#type)- [visible](#visible)