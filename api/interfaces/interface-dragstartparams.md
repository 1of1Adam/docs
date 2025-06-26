---
title: "Interface: DragStartParams | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DragStartParams"
extracted_at: "2025-06-22T09:36:20.850Z"
---

- [](/charting-library-docs/)- Interfaces- DragStartParamsOn this page# Interface: DragStartParams[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).DragStartParams

Drag start parameters

## Properties[​](#properties)
### exportData[​](#exportdata)
• exportData: (`exportOptions`: `Partial`<[`ExportDataOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportDataOptions)>) => `void`

Export data function

#### Type declaration[​](#type-declaration)
▸ (`exportOptions`): `void`

Parameters[​](#parameters)
NameType`exportOptions``Partial`<[`ExportDataOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportDataOptions)>
Returns[​](#returns)
`void`

### hoveredSourceId[​](#hoveredsourceid)
• hoveredSourceId: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)

Hovered source ID

### preventDefault[​](#preventdefault)
• preventDefault: () => `void`

Prevent default drag event

#### Type declaration[​](#type-declaration-1)
▸ (): `void`

Returns[​](#returns-1)
`void`

### setData[​](#setdata)
• setData: (`format`: `string`, `data`: `string`) => `void`

Set data function

#### Type declaration[​](#type-declaration-2)
▸ (`format`, `data`): `void`

Parameters[​](#parameters-1)
NameType`format``string``data``string`
Returns[​](#returns-2)
`void`

### setDragImage[​](#setdragimage)
• setDragImage: (`image`: `HTMLElement`, `xOffset`: `number`, `yOffset`: `number`) => `void`

Set drag image

#### Type declaration[​](#type-declaration-3)
▸ (`image`, `xOffset`, `yOffset`): `void`

Parameters[​](#parameters-2)
NameType`image``HTMLElement``xOffset``number``yOffset``number`
Returns[​](#returns-3)
`void`

- [Properties](#properties)[exportData](#exportdata)- [hoveredSourceId](#hoveredsourceid)- [preventDefault](#preventdefault)- [setData](#setdata)- [setDragImage](#setdragimage)