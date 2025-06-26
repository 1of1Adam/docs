---
title: "Interface: ISelectionApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISelectionApi"
extracted_at: "2025-06-22T09:39:34.454Z"
---

- [](/charting-library-docs/)- Interfaces- ISelectionApiOn this page# Interface: ISelectionApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ISelectionApi

Allows you to select entities ([drawings](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/) and [indicators](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/)) on the chart. Consider the following example:

```
var chart = tvWidget.activeChart();// Prints all selection changes to the consolechart.selection().onChanged().subscribe(null, s => console.log(chart.selection().allSources()));// Creates an indicator and saves its IDvar studyId = chart.createStudy("Moving Average", false, false, { length: 10 });// Adds the indicator to the selection ([<id>] is printed to the console)chart.selection().add(studyId);// Clears the selection ([] is printed to the console)chart.selection().clear();
```
#### Multiple Selection[​](#multiple-selection)
Multiple selection has the following specifics:

- Either indicators or drawings can be selected at the same time.
- If you add an indicator to the selection, other entities are removed from it.
- Adding an array of objects to the selection works the same as adding these objects one by one.

## Methods[​](#methods)
### add[​](#add)
▸ add(`entities`): `void`

Add entity / entities to selection

#### Parameters[​](#parameters)
NameTypeDescription`entities`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]entities to be added to selection
#### Returns[​](#returns)
`void`

### allSources[​](#allsources)
▸ allSources(): [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]

Returns all the entities in the selection

#### Returns[​](#returns-1)
[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]

### canBeAddedToSelection[​](#canbeaddedtoselection)
▸ canBeAddedToSelection(`entity`): `boolean`

Whether the entity can be added to the selection

#### Parameters[​](#parameters-1)
NameTypeDescription`entity`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)entity to be checked
#### Returns[​](#returns-2)
`boolean`

`true` when entity can be added to the selection

### clear[​](#clear)
▸ clear(): `void`

Clear selection

#### Returns[​](#returns-3)
`void`

### contains[​](#contains)
▸ contains(`entity`): `boolean`

Does the selection contain the entity

#### Parameters[​](#parameters-2)
NameTypeDescription`entity`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)entity to be checked
#### Returns[​](#returns-4)
`boolean`

`true` when entity is in the selection

### isEmpty[​](#isempty)
▸ isEmpty(): `boolean`

Is the selection empty

#### Returns[​](#returns-5)
`boolean`

`true` when empty

### onChanged[​](#onchanged)
▸ onChanged(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

Subscription for selection changes.

#### Returns[​](#returns-6)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

### remove[​](#remove)
▸ remove(`entities`): `void`

Remove entities from the selection

#### Parameters[​](#parameters-3)
NameTypeDescription`entities`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]entities to be removed from the selection
#### Returns[​](#returns-7)
`void`

### set[​](#set)
▸ set(`entities`): `void`

Set entity / entities as the selection

#### Parameters[​](#parameters-4)
NameTypeDescription`entities`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]entities to be selected
#### Returns[​](#returns-8)
`void`

- [Methods](#methods)[add](#add)- [allSources](#allsources)- [canBeAddedToSelection](#canbeaddedtoselection)- [clear](#clear)- [contains](#contains)- [isEmpty](#isempty)- [onChanged](#onchanged)- [remove](#remove)- [set](#set)