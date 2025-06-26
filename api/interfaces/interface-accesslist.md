---
title: "Interface: AccessList | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccessList"
extracted_at: "2025-06-22T09:31:55.066Z"
---

- [](/charting-library-docs/)- Interfaces- AccessListOn this page# Interface: AccessList[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).AccessList

Defines a whitelist / blacklist of studies or drawing tools.

## Properties[​](#properties)
### tools[​](#tools)
• tools: [`AccessListItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccessListItem)[]

Array of items which should be considered part of the access list

### type[​](#type)
• type: `"black"` | `"white"`

List type.
Supported values are:
`black` (all listed items should be disabled),
`white` (only the listed items should be enabled).- [Properties](#properties)[tools](#tools)- [type](#type)