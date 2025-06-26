---
title: "Interface: IAction | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IAction"
extracted_at: "2025-06-22T09:38:18.021Z"
---

- [](/charting-library-docs/)- Interfaces- IActionOn this page# Interface: IAction[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IAction

## Hierarchy[​](#hierarchy)

[`IMenuItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IMenuItem)

[`IDestroyable`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDestroyable)

↳ `IAction`

## Properties[​](#properties)
### id[​](#id)
• `Readonly` id: `string`

An unique ID of an action item. Could be used to distinguish actions between each other.

#### Inherited from[​](#inherited-from)
[IMenuItem](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IMenuItem).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IMenuItem#id)

### type[​](#type)
• `Readonly` type: [`Action`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.MenuItemType#action)

Menu item type

#### Overrides[​](#overrides)
[IMenuItem](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IMenuItem).[type](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IMenuItem#type)

## Methods[​](#methods)
### destroy[​](#destroy)
▸ destroy(): `void`

Clean up (destroy) any subscriptions, intervals, or other resources that this `IDestroyable` instance has.

#### Returns[​](#returns)
`void`

#### Inherited from[​](#inherited-from-1)
[IDestroyable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDestroyable).[destroy](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDestroyable#destroy)

### execute[​](#execute)
▸ execute(): `void`

A method which will be called when an action should be executed (e.g. when a user clicks on the item)

#### Returns[​](#returns-1)
`void`

### getState[​](#getstate)
▸ getState(): `Readonly`<[`ActionState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState)>

#### Returns[​](#returns-2)
`Readonly`<[`ActionState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState)>

Returns a state object of the action.

### onUpdate[​](#onupdate)
▸ onUpdate(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`OnActionUpdateHandler`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#onactionupdatehandler)>

#### Returns[​](#returns-3)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<[`OnActionUpdateHandler`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#onactionupdatehandler)>

A subscription for an event when an action is updated.

- [Hierarchy](#hierarchy)- [Properties](#properties)[id](#id)- [type](#type)- [Methods](#methods)[destroy](#destroy)- [execute](#execute)- [getState](#getstate)- [onUpdate](#onupdate)