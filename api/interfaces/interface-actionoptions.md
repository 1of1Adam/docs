---
title: "Interface: ActionOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionOptions"
extracted_at: "2025-06-22T09:32:20.773Z"
---

- [](/charting-library-docs/)- Interfaces- ActionOptionsOn this page# Interface: ActionOptions[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ActionOptions

## Hierarchy[​](#hierarchy)

`Partial`<[`OmitActionId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#omitactionid)<[`ActionState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState)>>

`Pick`<[`ActionState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState), `"actionId"`>

↳ `ActionOptions`

## Properties[​](#properties)
### actionId[​](#actionid)
• actionId: [`ActionId`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ActionId)

Human-readable, non-unique ID of an action item. Similar to [label](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#label), but language-agnostic.

#### Inherited from[​](#inherited-from)
Pick.actionId

### active[​](#active)
• `Optional` active: `boolean`

Is active

#### Inherited from[​](#inherited-from-1)
Partial.active

### checkable[​](#checkable)
• `Optional` checkable: `boolean`

Whether an action should have a checkbox next to it.

#### Inherited from[​](#inherited-from-2)
Partial.checkable

### checked[​](#checked)
• `Optional` checked: `boolean`

If [checkable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#checkable) is `true` then whether current state is checked or not.

#### Inherited from[​](#inherited-from-3)
Partial.checked

### disabled[​](#disabled)
• `Optional` disabled: `boolean`

Whether an action is disabled or not (disabled actions are usually cannot be executed and displayed grayed out)

#### Inherited from[​](#inherited-from-4)
Partial.disabled

### doNotCloseOnClick[​](#donotcloseonclick)
• `Optional` doNotCloseOnClick: `boolean`

A flag indicating whether the menu should remain open after clicking on the item.
When `true` the menu will remain open.
#### Inherited from[​](#inherited-from-5)
Partial.doNotCloseOnClick

### hint[​](#hint)
• `Optional` hint: `string`

A hint of an action.

#### Inherited from[​](#inherited-from-6)
Partial.hint

### icon[​](#icon)
• `Optional` icon: `string`

A string of SVG icon for an action. A string should be a string representation of SVG (not a path/URL).

#### Inherited from[​](#inherited-from-7)
Partial.icon

### iconChecked[​](#iconchecked)
• `Optional` iconChecked: `string`

If [checkable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#checkable) is `true` then an icon to be used when [checked](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#checked) is `true`.

#### Inherited from[​](#inherited-from-8)
Partial.iconChecked

### label[​](#label)
• `Optional` label: `string`

Text title of an action

#### Inherited from[​](#inherited-from-9)
Partial.label

### loading[​](#loading)
• `Optional` loading: `boolean`

Whether an action is still in loading state (it means that it's data is not ready yet).
Usually in this case a spinner/loader will be displayed instead of this action.
#### Inherited from[​](#inherited-from-10)
Partial.loading

### noInteractive[​](#nointeractive)
• `Optional` noInteractive: `boolean`

This flag indicates that this action is static content only and is not interactive.

#### Inherited from[​](#inherited-from-11)
Partial.noInteractive

### onExecute[​](#onexecute)
• `Optional` onExecute: [`OnActionExecuteHandler`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#onactionexecutehandler)

A function which will be called when an action should be executed (e.g. when a user clicks on the item).

### shortcutHint[​](#shortcuthint)
• `Optional` shortcutHint: `string`

A string that represents a shortcut hint for this action.

#### Inherited from[​](#inherited-from-12)
Partial.shortcutHint

### styledLabel[​](#styledlabel)
• `Optional` styledLabel: [`StyledText`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StyledText)[]

Text title of an action consisting of several styled sections. If not defined then [label](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#label) is used instead.

#### Inherited from[​](#inherited-from-13)
Partial.styledLabel

### subItems[​](#subitems)
• `Optional` subItems: [`IActionVariant`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#iactionvariant)[]

Sub-items of an action

#### Inherited from[​](#inherited-from-14)
Partial.subItems

- [Hierarchy](#hierarchy)- [Properties](#properties)[actionId](#actionid)- [active](#active)- [checkable](#checkable)- [checked](#checked)- [disabled](#disabled)- [doNotCloseOnClick](#donotcloseonclick)- [hint](#hint)- [icon](#icon)- [iconChecked](#iconchecked)- [label](#label)- [loading](#loading)- [noInteractive](#nointeractive)- [onExecute](#onexecute)- [shortcutHint](#shortcuthint)- [styledLabel](#styledlabel)- [subItems](#subitems)