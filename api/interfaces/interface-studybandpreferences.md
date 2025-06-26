---
title: "Interface: StudyBandPreferences | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandPreferences"
extracted_at: "2025-06-22T09:45:44.239Z"
---

- [](/charting-library-docs/)- Interfaces- StudyBandPreferencesOn this page# Interface: StudyBandPreferences[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).StudyBandPreferences

Study band style preferences.

## Hierarchy[​](#hierarchy)

[`StudyBandStyle`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle)

[`StudyBandInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo)

↳ `StudyBandPreferences`

## Properties[​](#properties)
### color[​](#color)
• color: `string`

Color.

`Example`

```
'#ffffff'.
```
#### Inherited from[​](#inherited-from)
[StudyBandStyle](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle).[color](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle#color)

### id[​](#id)
• `Optional` `Readonly` id: `string`

Band ID. Used in [StudyFilledAreaInfo.objAId](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo#objaid) and [StudyFilledAreaInfo.objBId](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyFilledAreaInfo#objbid).

`See`

StudyFilledAreaInfo

#### Inherited from[​](#inherited-from-1)
[StudyBandInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo#id)

### isHidden[​](#ishidden)
• `Optional` `Readonly` isHidden: `boolean`

Band style inputs visibility flag. Used to hide the band from the style tab of study properties dialogs.

#### Inherited from[​](#inherited-from-2)
[StudyBandInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo).[isHidden](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo#ishidden)

### linestyle[​](#linestyle)
• linestyle: `number`

Line style.

`Example`

```
2 // Dotted line.
```
#### Inherited from[​](#inherited-from-3)
[StudyBandStyle](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle).[linestyle](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle#linestyle)

### linewidth[​](#linewidth)
• linewidth: `number`

Line width.

#### Inherited from[​](#inherited-from-4)
[StudyBandStyle](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle).[linewidth](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle#linewidth)

### name[​](#name)
• `Readonly` name: `string`

Band name.

#### Inherited from[​](#inherited-from-5)
[StudyBandInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo).[name](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo#name)

### value[​](#value)
• value: `number`

Value at which the band will be drawn.

`Example`

```
75 // Drawn at price = 75.
```
#### Inherited from[​](#inherited-from-6)
[StudyBandStyle](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle).[value](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle#value)

### visible[​](#visible)
• visible: `boolean`

Band visibility flag.

#### Inherited from[​](#inherited-from-7)
[StudyBandStyle](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle).[visible](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandStyle#visible)

### zorder[​](#zorder)
• `Optional` `Readonly` zorder: `number`

Band z-order.

#### Inherited from[​](#inherited-from-8)
[StudyBandInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo).[zorder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyBandInfo#zorder)

- [Hierarchy](#hierarchy)- [Properties](#properties)[color](#color)- [id](#id)- [isHidden](#ishidden)- [linestyle](#linestyle)- [linewidth](#linewidth)- [name](#name)- [value](#value)- [visible](#visible)- [zorder](#zorder)