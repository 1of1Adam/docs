---
title: "Interface: IDropdownApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDropdownApi"
extracted_at: "2025-06-22T09:38:52.063Z"
---

- [](/charting-library-docs/)- Interfaces- IDropdownApiOn this page# Interface: IDropdownApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IDropdownApi

Dropdown menu API

## Methods[​](#methods)
### applyOptions[​](#applyoptions)
▸ applyOptions(`options`): `void`

Apply options to the dropdown menu.
Note that this method does not affect the menu's alignment. To change the alignment, you should remove and recreate the menu as follows:
```
myCustomDropdownApi.remove();widget.createDropdown(optionsWithDifferentAlignment);
```
#### Parameters[​](#parameters)
NameTypeDescription`options``Partial`<`Omit`<[`DropdownParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DropdownParams), `"align"`>>Partial options for the dropdown menu
#### Returns[​](#returns)
`void`

### remove[​](#remove)
▸ remove(): `void`

Remove the dropdown menu.

#### Returns[​](#returns-1)
`void`

- [Methods](#methods)[applyOptions](#applyoptions)- [remove](#remove)