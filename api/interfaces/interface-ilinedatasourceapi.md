---
title: "Interface: ILineDataSourceApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi"
extracted_at: "2025-06-22T09:39:03.934Z"
---

- [](/charting-library-docs/)- Interfaces- ILineDataSourceApiOn this page# Interface: ILineDataSourceApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ILineDataSourceApi

Drawing API

You can retrieve this interface by using the [IChartWidgetApi.getShapeById](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getshapebyid) method.

## Methods[​](#methods)
### bringToFront[​](#bringtofront)
▸ bringToFront(): `void`

Places the drawing on top of all other chart objects.

#### Returns[​](#returns)
`void`

### getAnchoredPosition[​](#getanchoredposition)
▸ getAnchoredPosition(): [`PositionPercents`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionPercents)

Get the position percents of a fixed drawing.

#### Returns[​](#returns-1)
[`PositionPercents`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionPercents)

### getPoints[​](#getpoints)
▸ getPoints(): [`PricedPoint`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PricedPoint)[]

Returns the points of the drawing.

#### Returns[​](#returns-2)
[`PricedPoint`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PricedPoint)[]

### getProperties[​](#getproperties)
▸ getProperties<`P`>(): `P`

Get all the properties of the drawing.

#### Type parameters[​](#type-parameters)
NameType`P`extends `Record`<`string`, `any`> = `Record`<`string`, `any`>
#### Returns[​](#returns-3)
`P`

properties of the drawing

### isSavingEnabled[​](#issavingenabled)
▸ isSavingEnabled(): `boolean`

Can the drawing be saved in the chart layout

#### Returns[​](#returns-4)
`boolean`

`true` when the drawing can be saved

### isSelectionEnabled[​](#isselectionenabled)
▸ isSelectionEnabled(): `boolean`

Is the drawing selectable by the user.

#### Returns[​](#returns-5)
`boolean`

`true` when the drawing can be selected

### isShowInObjectsTreeEnabled[​](#isshowinobjectstreeenabled)
▸ isShowInObjectsTreeEnabled(): `boolean`

Is the drawing shown in the Object Tree Panel

#### Returns[​](#returns-6)
`boolean`

`true` when the drawing is visible in the tree.

### isUserEditEnabled[​](#isusereditenabled)
▸ isUserEditEnabled(): `boolean`

Is the drawing editable by the user.

#### Returns[​](#returns-7)
`boolean`

`true` when the drawing is editable

### sendToBack[​](#sendtoback)
▸ sendToBack(): `void`

Places the drawing behind all other chart objects.

#### Returns[​](#returns-8)
`void`

### setAnchoredPosition[​](#setanchoredposition)
▸ setAnchoredPosition(`positionPercents`): `void`

Set the position percents for a fixed drawing.
For example `setPoints([{ x: 0.1, y: 0.1 }])` would set a fixed drawing defined by
a single point to be 10% top the left edge of the chart and 10% from the top edge.
#### Parameters[​](#parameters)
NameTypeDescription`positionPercents`[`PositionPercents`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionPercents)The new position percents.
#### Returns[​](#returns-9)
`void`

### setPoints[​](#setpoints)
▸ setPoints(`points`): `void`

Set the new points of the drawing. All points must be provided: for example if the drawing is defined by 5 points then all 5 must be provided.

#### Parameters[​](#parameters-1)
NameTypeDescription`points`[`ShapePoint`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapepoint)[]The new points.
#### Returns[​](#returns-10)
`void`

### setProperties[​](#setproperties)
▸ setProperties<`P`>(`newProperties`, `saveDefaults?`): `void`

Sets the properties of the drawing.

#### Type parameters[​](#type-parameters-1)
NameType`P`extends `Record`<`string`, `any`> = `Record`<`string`, `any`>
#### Parameters[​](#parameters-2)
NameTypeDescription`newProperties``P`Drawing properties to be set on the drawing. It should have the same structure as an object from [ILineDataSourceApi.getProperties](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ILineDataSourceApi#getproperties). It can only include the properties that you want to override.`saveDefaults?``boolean`If `true`, the properties will be saved as defaults for the drawing. Defaults are used when the drawing is created.
#### Returns[​](#returns-11)
`void`

### setSavingEnabled[​](#setsavingenabled)
▸ setSavingEnabled(`enable`): `void`

Enables or disables saving of the drawing in the chart layout (see `disableSave` option of `createMultipointShape`).

#### Parameters[​](#parameters-3)
NameTypeDescription`enable``boolean`if `true`, the drawing can be saved to the chart
#### Returns[​](#returns-12)
`void`

### setSelectionEnabled[​](#setselectionenabled)
▸ setSelectionEnabled(`enable`): `void`

Set whether the drawing can be selected by the user or not.

#### Parameters[​](#parameters-4)
NameTypeDescription`enable``boolean`if `true` then the user can select the drawing (see `disableSelection` option of `createMultipointShape`)
#### Returns[​](#returns-13)
`void`

### setShowInObjectsTreeEnabled[​](#setshowinobjectstreeenabled)
▸ setShowInObjectsTreeEnabled(`enabled`): `void`

Enables or disables the visibility of the drawing in the Object Tree panel

#### Parameters[​](#parameters-5)
NameTypeDescription`enabled``boolean`if `true` then the drawing will be visible
#### Returns[​](#returns-14)
`void`

### setUserEditEnabled[​](#setusereditenabled)
▸ setUserEditEnabled(`enabled`): `void`

Enables or disables whether the drawing is editable

#### Parameters[​](#parameters-6)
NameTypeDescription`enabled``boolean`if `true`, then the drawing will be editable
#### Returns[​](#returns-15)
`void`

- [Methods](#methods)[bringToFront](#bringtofront)- [getAnchoredPosition](#getanchoredposition)- [getPoints](#getpoints)- [getProperties](#getproperties)- [isSavingEnabled](#issavingenabled)- [isSelectionEnabled](#isselectionenabled)- [isShowInObjectsTreeEnabled](#isshowinobjectstreeenabled)- [isUserEditEnabled](#isusereditenabled)- [sendToBack](#sendtoback)- [setAnchoredPosition](#setanchoredposition)- [setPoints](#setpoints)- [setProperties](#setproperties)- [setSavingEnabled](#setsavingenabled)- [setSelectionEnabled](#setselectionenabled)- [setShowInObjectsTreeEnabled](#setshowinobjectstreeenabled)- [setUserEditEnabled](#setusereditenabled)