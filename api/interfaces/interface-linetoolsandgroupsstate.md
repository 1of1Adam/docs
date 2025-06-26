---
title: "Interface: LineToolsAndGroupsState | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState"
extracted_at: "2025-06-22T09:40:58.968Z"
---

- [](/charting-library-docs/)- Interfaces- LineToolsAndGroupsStateOn this page# Interface: LineToolsAndGroupsState[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).LineToolsAndGroupsState

Represents the state of drawings and groups

## Properties[​](#properties)
### groups[​](#groups)
• groups: `Map`<`string`, [`LineToolsGroupState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsGroupState)>

A map of group IDs to drawings group states

### sources[​](#sources)
• sources: `Map`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid), [`LineToolState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolState)>

A map of sources to drawing states

### symbol[​](#symbol)
• `Optional` symbol: `string`

The symbol ID associated with the drawings and groups

- [Properties](#properties)[groups](#groups)- [sources](#sources)- [symbol](#symbol)