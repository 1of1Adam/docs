---
title: "Interface: CreateContextMenuParams | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateContextMenuParams"
extracted_at: "2025-06-22T09:34:51.125Z"
---

- [](/charting-library-docs/)- Interfaces- CreateContextMenuParamsOn this page# Interface: CreateContextMenuParams[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CreateContextMenuParams

## Properties[​](#properties)
### detail[​](#detail)
• `Optional` detail: { `id`: `string` ; `type`: `"series"`  } | { `id`: `string` ; `type`: `"study"`  } | { `id`: `string` | `number` ; `type`: `"shape"`  } | { `id`: `string` ; `type`: `"groupOfShapes"`  } | { `id`: `string` ; `type`: `"position"`  } | { `id`: `string` ; `type`: `"order"`  }

Additional details for the context menu.
`type` field can be one of the following: `series`, `study`, `shape`, or `groupOfShapes`

### menuName[​](#menuname)
• menuName: `string`

name of the menu

- [Properties](#properties)[detail](#detail)- [menuName](#menuname)