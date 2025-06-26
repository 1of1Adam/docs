---
title: "Interface: ActionState | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState"
extracted_at: "2025-06-22T09:32:25.595Z"
---

- [](/charting-library-docs/)- Interfaces- ActionStateOn this page# Interface: ActionState[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ActionState

## Properties[​](#properties)
### actionId[​](#actionid)
• actionId: [`ActionId`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ActionId)

Human-readable, non-unique ID of an action item. Similar to [label](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#label), but language-agnostic.

### active[​](#active)
• active: `boolean`

Is active

### checkable[​](#checkable)
• checkable: `boolean`

Whether an action should have a checkbox next to it.

### checked[​](#checked)
• checked: `boolean`

If [checkable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#checkable) is `true` then whether current state is checked or not.

### disabled[​](#disabled)
• disabled: `boolean`

Whether an action is disabled or not (disabled actions are usually cannot be executed and displayed grayed out)

### doNotCloseOnClick[​](#donotcloseonclick)
• doNotCloseOnClick: `boolean`

A flag indicating whether the menu should remain open after clicking on the item.
When `true` the menu will remain open.

### hint[​](#hint)
• `Optional` hint: `string`

A hint of an action.

### icon[​](#icon)
• `Optional` icon: `string`

A string of SVG icon for an action. A string should be a string representation of SVG (not a path/URL).

### iconChecked[​](#iconchecked)
• `Optional` iconChecked: `string`

If [checkable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#checkable) is `true` then an icon to be used when [checked](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#checked) is `true`.

### label[​](#label)
• label: `string`

Text title of an action

### loading[​](#loading)
• loading: `boolean`

Whether an action is still in loading state (it means that it's data is not ready yet).
Usually in this case a spinner/loader will be displayed instead of this action.

### noInteractive[​](#nointeractive)
• `Optional` noInteractive: `boolean`

This flag indicates that this action is static content only and is not interactive.

### shortcutHint[​](#shortcuthint)
• `Optional` shortcutHint: `string`

A string that represents a shortcut hint for this action.

### styledLabel[​](#styledlabel)
• `Optional` styledLabel: [`StyledText`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StyledText)[]

Text title of an action consisting of several styled sections. If not defined then [label](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionState#label) is used instead.

### subItems[​](#subitems)
• subItems: [`IActionVariant`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#iactionvariant)[]

Sub-items of an action

- [Properties](#properties)[actionId](#actionid)- [active](#active)- [checkable](#checkable)- [checked](#checked)- [disabled](#disabled)- [doNotCloseOnClick](#donotcloseonclick)- [hint](#hint)- [icon](#icon)- [iconChecked](#iconchecked)- [label](#label)- [loading](#loading)- [noInteractive](#nointeractive)- [shortcutHint](#shortcuthint)- [styledLabel](#styledlabel)- [subItems](#subitems)