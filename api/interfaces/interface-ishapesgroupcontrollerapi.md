---
title: "Interface: IShapesGroupControllerApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IShapesGroupControllerApi"
extracted_at: "2025-06-22T09:39:39.860Z"
---

- [](/charting-library-docs/)- Interfaces- IShapesGroupControllerApiOn this page# Interface: IShapesGroupControllerApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IShapesGroupControllerApi

Drawing Groups API. Refer to the [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#drawing-groups-api) article for more information.

## Methods[​](#methods)
### addShapeToGroup[​](#addshapetogroup)
▸ addShapeToGroup(`groupId`, `shapeId`): `void`

Add a drawing to a group.

#### Parameters[​](#parameters)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.`shapeId`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)A drawing ID.
#### Returns[​](#returns)
`void`

### availableZOrderOperations[​](#availablezorderoperations)
▸ availableZOrderOperations(`groupId`): [`AvailableZOrderOperations`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AvailableZOrderOperations)

Get an object containing the available Z-order operations for a group.

#### Parameters[​](#parameters-1)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-1)
[`AvailableZOrderOperations`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AvailableZOrderOperations)

The available Z-order operations.

### bringForward[​](#bringforward)
▸ bringForward(`groupId`): `void`

Move the group one level up in the Z-order.

#### Parameters[​](#parameters-2)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-2)
`void`

### bringToFront[​](#bringtofront)
▸ bringToFront(`groupId`): `void`

Move the group to the top of the Z-order.

#### Parameters[​](#parameters-3)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-3)
`void`

### canBeGroupped[​](#canbegroupped)
▸ canBeGroupped(`shapes`): `boolean`

Check if some drawings can be grouped.

#### Parameters[​](#parameters-4)
NameTypeDescription`shapes`readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]An array of drawing IDs.
#### Returns[​](#returns-4)
`boolean`

`true` if the drawings can be grouped, `false` otherwise.

### createGroupFromSelection[​](#creategroupfromselection)
▸ createGroupFromSelection(): [`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)

Create a group of drawings from the selection.

#### Returns[​](#returns-5)
[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)

The ID of the created group.

`Throws`

If selection is empty, or selection contains non-drawings, or selection contains drawings from more than one pane.

### excludeShapeFromGroup[​](#excludeshapefromgroup)
▸ excludeShapeFromGroup(`groupId`, `shapeId`): `void`

Remove a drawing from a group. If the drawing is the only drawing in the group then the group is also removed.

#### Parameters[​](#parameters-5)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.`shapeId`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)A drawing ID.
#### Returns[​](#returns-6)
`void`

### getGroupName[​](#getgroupname)
▸ getGroupName(`groupId`): `string`

Get the name of a group.

#### Parameters[​](#parameters-6)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-7)
`string`

The name of the group.

### groupLock[​](#grouplock)
▸ groupLock(`groupId`): [`GroupLockState`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#grouplockstate)

Get locked state of a group.

#### Parameters[​](#parameters-7)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-8)
[`GroupLockState`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#grouplockstate)

The locked state.

### groupVisibility[​](#groupvisibility)
▸ groupVisibility(`groupId`): [`GroupVisibilityState`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#groupvisibilitystate)

Get the visibility state of a group.

#### Parameters[​](#parameters-8)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-9)
[`GroupVisibilityState`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#groupvisibilitystate)

The visibility state.

### groups[​](#groups)
▸ groups(): readonly [`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)[]

Get an array of all drawing groups.

#### Returns[​](#returns-10)
readonly [`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)[]

An array of group IDs.

### insertAfter[​](#insertafter)
▸ insertAfter(`groupId`, `target`): `void`

Move the group immediately below the target in the Z-order.

#### Parameters[​](#parameters-9)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.`target`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | [`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A target ID.
#### Returns[​](#returns-11)
`void`

### insertBefore[​](#insertbefore)
▸ insertBefore(`groupId`, `target`): `void`

Move the group immediately above the target in the Z-order.

#### Parameters[​](#parameters-10)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.`target`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | [`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A target ID.
#### Returns[​](#returns-12)
`void`

### removeGroup[​](#removegroup)
▸ removeGroup(`groupId`): `void`

Remove a group of drawings.

#### Parameters[​](#parameters-11)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-13)
`void`

### sendBackward[​](#sendbackward)
▸ sendBackward(`groupId`): `void`

Move the group one level down in the Z-order.

#### Parameters[​](#parameters-12)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-14)
`void`

### sendToBack[​](#sendtoback)
▸ sendToBack(`groupId`): `void`

Move the group to the bottom of the Z-order.

#### Parameters[​](#parameters-13)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-15)
`void`

### setGroupLock[​](#setgrouplock)
▸ setGroupLock(`groupId`, `value`): `void`

Lock or unlock a group.

#### Parameters[​](#parameters-14)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.`value``boolean`A boolean flag. `true` to lock, `false` to unlock.
#### Returns[​](#returns-16)
`void`

### setGroupName[​](#setgroupname)
▸ setGroupName(`groupId`, `name`): `void`

Set the name of a group. Names do not need to be unique.

#### Parameters[​](#parameters-15)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.`name``string`The new name of the group.
#### Returns[​](#returns-17)
`void`

### setGroupVisibility[​](#setgroupvisibility)
▸ setGroupVisibility(`groupId`, `value`): `void`

Show or hide all drawings in a group.

#### Parameters[​](#parameters-16)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.`value``boolean`A boolean flag. `true` to show, `false` to hide.
#### Returns[​](#returns-18)
`void`

### shapesInGroup[​](#shapesingroup)
▸ shapesInGroup(`groupId`): readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]

Get an array of IDs for each drawing in a group.

#### Parameters[​](#parameters-17)
NameTypeDescription`groupId`[`ShapesGroupId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#shapesgroupid)A group ID.
#### Returns[​](#returns-19)
readonly [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)[]

An array of drawing IDs.

- [Methods](#methods)[addShapeToGroup](#addshapetogroup)- [availableZOrderOperations](#availablezorderoperations)- [bringForward](#bringforward)- [bringToFront](#bringtofront)- [canBeGroupped](#canbegroupped)- [createGroupFromSelection](#creategroupfromselection)- [excludeShapeFromGroup](#excludeshapefromgroup)- [getGroupName](#getgroupname)- [groupLock](#grouplock)- [groupVisibility](#groupvisibility)- [groups](#groups)- [insertAfter](#insertafter)- [insertBefore](#insertbefore)- [removeGroup](#removegroup)- [sendBackward](#sendbackward)- [sendToBack](#sendtoback)- [setGroupLock](#setgrouplock)- [setGroupName](#setgroupname)- [setGroupVisibility](#setgroupvisibility)- [shapesInGroup](#shapesingroup)