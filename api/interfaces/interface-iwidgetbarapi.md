---
title: "Interface: IWidgetbarApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWidgetbarApi"
extracted_at: "2025-06-22T09:40:00.424Z"
---

- [](/charting-library-docs/)- Interfaces- IWidgetbarApiOn this page# Interface: IWidgetbarApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IWidgetbarApi

Widget Bar API

## Hierarchy[​](#hierarchy)

[`IDestroyable`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDestroyable)

↳ `IWidgetbarApi`

## Methods[​](#methods)
### changeWidgetBarVisibility[​](#changewidgetbarvisibility)
▸ changeWidgetBarVisibility(`visible`): `void`

Change the visibility of the right toolbar

#### Parameters[​](#parameters)
NameTypeDescription`visible``boolean`true to display the toolbar, false to hide
#### Returns[​](#returns)
`void`

### closeOrderPanel[​](#closeorderpanel)
▸ closeOrderPanel(): `void`

Close order panel widget

#### Returns[​](#returns-1)
`void`

### destroy[​](#destroy)
▸ destroy(): `void`

Clean up (destroy) any subscriptions, intervals, or other resources that this `IDestroyable` instance has.

#### Returns[​](#returns-2)
`void`

#### Inherited from[​](#inherited-from)
[IDestroyable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDestroyable).[destroy](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDestroyable#destroy)

### hidePage[​](#hidepage)
▸ hidePage(`pageName`): `void`

Hide page

#### Parameters[​](#parameters-1)
NameTypeDescription`pageName`[`PageName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#pagename)name of page to hide
#### Returns[​](#returns-3)
`void`

### isPageVisible[​](#ispagevisible)
▸ isPageVisible(`pageName`): `boolean`

Checks if page is visible

#### Parameters[​](#parameters-2)
NameTypeDescription`pageName`[`PageName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#pagename)page to check if visible
#### Returns[​](#returns-4)
`boolean`

true` when page is visible

### openOrderPanel[​](#openorderpanel)
▸ openOrderPanel(): `void`

Open order panel widget

#### Returns[​](#returns-5)
`void`

### showPage[​](#showpage)
▸ showPage(`pageName`): `void`

Show page

#### Parameters[​](#parameters-3)
NameTypeDescription`pageName`[`PageName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#pagename)name of page to show
#### Returns[​](#returns-6)
`void`

- [Hierarchy](#hierarchy)- [Methods](#methods)[changeWidgetBarVisibility](#changewidgetbarvisibility)- [closeOrderPanel](#closeorderpanel)- [destroy](#destroy)- [hidePage](#hidepage)- [isPageVisible](#ispagevisible)- [openOrderPanel](#openorderpanel)- [showPage](#showpage)