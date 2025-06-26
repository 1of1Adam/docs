---
title: "Interface: ICustomSymbolStatusAdapter | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter"
extracted_at: "2025-06-22T09:38:42.400Z"
---

- [](/charting-library-docs/)- Interfaces- ICustomSymbolStatusAdapterOn this page# Interface: ICustomSymbolStatusAdapter[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ICustomSymbolStatusAdapter

Adapter API for reading and setting the state of a
custom symbol status item.
The 'set' methods return the same adapter so that you can
chain multiple set functions together.
Example

```
const adapter = widget.customSymbolStatus().symbol('ABC');adapter.setVisible(true).setColor('#336699').setTooltip('Custom Status')
```
## Methods[​](#methods)
### getColor[​](#getcolor)
▸ getColor(): `string`

Get the current color of the status item.

#### Returns[​](#returns)
`string`

the current color

### getDropDownContent[​](#getdropdowncontent)
▸ getDropDownContent(): [`CustomStatusDropDownContent`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomStatusDropDownContent)[]

Get the current content of the status item displayed within
the pop-up tooltip.
#### Returns[​](#returns-1)
[`CustomStatusDropDownContent`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomStatusDropDownContent)[]

the current pop-up content

### getIcon[​](#geticon)
▸ getIcon(): `string`

Get the current icon for the status item.

#### Returns[​](#returns-2)
`string`

the current icon SVG string

### getTooltip[​](#gettooltip)
▸ getTooltip(): `string`

Get the current tooltip text for the status item.

#### Returns[​](#returns-3)
`string`

the current tooltip text

### getVisible[​](#getvisible)
▸ getVisible(): `boolean`

Get the current visibility of the status item.

#### Returns[​](#returns-4)
`boolean`

the current visibility

### setColor[​](#setcolor)
▸ setColor(`color`): [`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

Set the color for the status item.

#### Parameters[​](#parameters)
NameTypeDescription`color``string`color to be used for the status item. It is recommended that you test that the color works well for both light and dark themes.
#### Returns[​](#returns-5)
[`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

the current symbol status adapter so you can
chain 'set' functions together.
`Default`

```
'#9598a1'
```

### setDropDownContent[​](#setdropdowncontent)
▸ setDropDownContent(`content`): [`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

Set the content to be displayed within the pop-up which appears
when the user clicks on the symbol statuses.
#### Parameters[​](#parameters-1)
NameTypeDescription`content`[`CustomStatusDropDownContent`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomStatusDropDownContent)[]content to be displayed, set to `null` to display nothing. More than one section can be specified.
#### Returns[​](#returns-6)
[`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

the current symbol status adapter so you can
chain 'set' functions together.
`Default`

```
null
```

### setIcon[​](#seticon)
▸ setIcon(`icon`): [`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

Set the icon for the status item.

#### Parameters[​](#parameters-2)
NameTypeDescription`icon``string`svg markup string to be used as the icon, or `null` to display no icon
#### Returns[​](#returns-7)
[`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

the current symbol status adapter so you can
chain 'set' functions together.
`Default`

blank
The icon should be provided as an svg markup. It is
recommended that the icon works well at small sizes.
Example

```
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">  <!-- Icon source: https://heroicons.com -->  <path fill-rule="evenodd" d="M13.5 4.938a7 7 0 11-9.006 1.737c.202-.257.59-.218.793.039.278.352.594.672.943.954.332.269.786-.049.773-.476a5.977 5.977 0 01.572-2.759 6.026 6.026 0 012.486-2.665c.247-.14.55-.016.677.238A6.967 6.967 0 0013.5 4.938zM14 12a4 4 0 01-4 4c-1.913 0-3.52-1.398-3.91-3.182-.093-.429.44-.643.814-.413a4.043 4.043 0 001.601.564c.303.038.531-.24.51-.544a5.975 5.975 0 011.315-4.192.447.447 0 01.431-.16A4.001 4.001 0 0114 12z" clip-rule="evenodd" /></svg>
```

### setTooltip[​](#settooltip)
▸ setTooltip(`tooltip`): [`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

Set the text to be displayed within the tooltip displayed
when hovering over the statuses for the symbol.
#### Parameters[​](#parameters-3)
NameTypeDescription`tooltip``string`text to be displayed within the tooltip.
#### Returns[​](#returns-8)
[`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

the current symbol status adapter so you can
chain 'set' functions together.
`Default`

```
''
```

### setVisible[​](#setvisible)
▸ setVisible(`visible`): [`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

Set the visibility for the status item.

#### Parameters[​](#parameters-4)
NameTypeDescription`visible``boolean`visibility for the status item, where `true` makes the item visible.
#### Returns[​](#returns-9)
[`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

the current symbol status adapter so you can
chain 'set' functions together.
`Default`

```
false
```- [Methods](#methods)[getColor](#getcolor)- [getDropDownContent](#getdropdowncontent)- [getIcon](#geticon)- [getTooltip](#gettooltip)- [getVisible](#getvisible)- [setColor](#setcolor)- [setDropDownContent](#setdropdowncontent)- [setIcon](#seticon)- [setTooltip](#settooltip)- [setVisible](#setvisible)